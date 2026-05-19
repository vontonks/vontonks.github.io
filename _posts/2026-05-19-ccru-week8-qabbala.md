---
layout: ccru-static
title: "Qabbala"
date: 2026-05-19
week: 8
tags: [ccru, qabbalism, numogram, philosophy]
---

Week eight, qabbalism. Built a thing instead of writing the lecture up.

Alphanumeric Qabbala (AQ) assigns digits 0–9 to their numeric values and letters a–z to the values 10–35. Base 36. The value of a word is the sum of its characters. `ccru` is c(12) + c(12) + r(27) + u(30) = **81**. The Cybernetic Culture Research Unit used the scheme to surface coincidences across language — treating numerical equivalence as a signal worth attending to, or pretending to, depending on the mood.

The trace below takes a number from 0 to 999 and returns a word, or composes a phrase, whose AQ value equals your input.

<style>
  .aq-trace {
    margin: 40px 0;
    padding: 24px 20px 28px;
    border: 1px solid var(--border-color);
    background: rgba(0, 0, 0, 0.5);
    position: relative;
  }
  .aq-trace::before {
    content: 'AQ TRACE';
    position: absolute;
    top: -10px;
    left: 16px;
    background: var(--darker-bg);
    padding: 0 8px;
    font-size: 0.7em;
    letter-spacing: 0.3em;
    color: var(--neon-green);
    opacity: 0.75;
  }
  .aq-status {
    text-align: center;
    font-size: 0.85em;
    opacity: 0.6;
    letter-spacing: 0.1em;
    margin-bottom: 1.2em;
    min-height: 1.5em;
  }
  .aq-form {
    display: flex;
    gap: 12px;
    justify-content: center;
    margin-bottom: 1.5em;
    flex-wrap: wrap;
  }
  .aq-form input[type=number] {
    background: transparent;
    border: 1px solid var(--neon-green);
    color: var(--neon-green);
    font-family: inherit;
    font-size: 1.3em;
    padding: 0.55em 1em;
    width: 140px;
    text-align: center;
    outline: none;
    caret-color: var(--neon-green-bright);
    -moz-appearance: textfield;
  }
  .aq-form input[type=number]::-webkit-outer-spin-button,
  .aq-form input[type=number]::-webkit-inner-spin-button {
    -webkit-appearance: none;
    margin: 0;
  }
  .aq-form input[type=number]:focus { box-shadow: 0 0 12px var(--neon-green); }
  .aq-form button {
    background: transparent;
    border: 1px solid var(--neon-green);
    color: var(--neon-green);
    font-family: inherit;
    font-size: 1.3em;
    padding: 0.55em 1.4em;
    cursor: pointer;
    letter-spacing: 0.25em;
    text-shadow: 0 0 5px var(--neon-green);
    transition: background 0.15s, color 0.15s;
  }
  .aq-form button:hover,
  .aq-form button:focus {
    background: var(--neon-green);
    color: var(--dark-bg);
    outline: none;
  }
  .aq-form button:disabled { opacity: 0.4; cursor: not-allowed; }
  .aq-output {
    text-align: center;
    padding: 1.5em 1em;
    border: 1px dashed var(--border-color);
    min-height: 6em;
  }
  .aq-partition {
    font-size: 0.85em;
    opacity: 0.65;
    margin-bottom: 1em;
    letter-spacing: 0.12em;
  }
  .aq-words {
    font-size: 1.55em;
    line-height: 1.8;
    letter-spacing: 0.14em;
    text-shadow: 0 0 6px var(--neon-green);
  }
  .aq-words .word { display: inline-block; margin: 0.2em 0.45em; }
  .aq-words .word.canonical { opacity: 0.55; font-style: italic; }
</style>

<div class="aq-trace">
  <div id="aq-status" class="aq-status">&gt; ccru.aq.trace BOOTING…</div>
  <form id="aq-form" class="aq-form" autocomplete="off">
    <input type="number" id="aq-input" min="0" max="999" placeholder="0–999" inputmode="numeric" required>
    <button type="submit" id="aq-go" disabled>TRACE</button>
  </form>
  <section id="aq-output" class="aq-output" hidden aria-live="polite">
    <div id="aq-partition" class="aq-partition"></div>
    <div id="aq-words" class="aq-words"></div>
  </section>
</div>

<script>
(function() {
  "use strict";

  let DICT = null;
  const CANONICAL_MAX = 35;
  const STOPWORD_SKIP = 40;

  const statusEl = document.getElementById('aq-status');
  const formEl = document.getElementById('aq-form');
  const inputEl = document.getElementById('aq-input');
  const goBtn = document.getElementById('aq-go');
  const outputEl = document.getElementById('aq-output');
  const partitionEl = document.getElementById('aq-partition');
  const wordsEl = document.getElementById('aq-words');

  function pickRandom(arr) {
    return arr[Math.floor(Math.random() * arr.length)];
  }

  function pickWord(dict, value) {
    const bucket = dict[String(value)];
    if (!bucket || !bucket.length) return null;
    const pool = bucket.length > STOPWORD_SKIP * 2
      ? bucket.slice(STOPWORD_SKIP)
      : bucket;
    return pickRandom(pool);
  }

  function partition(n, minChunk, maxChunk) {
    if (n <= maxChunk) return [n];
    const chunks = [];
    let remaining = n;
    while (remaining > maxChunk) {
      const max = Math.min(maxChunk, remaining - minChunk);
      const c = minChunk + Math.floor(Math.random() * (max - minChunk + 1));
      chunks.push(c);
      remaining -= c;
    }
    if (remaining > 0) chunks.push(remaining);
    for (let i = chunks.length - 1; i > 0; i--) {
      const j = Math.floor(Math.random() * (i + 1));
      [chunks[i], chunks[j]] = [chunks[j], chunks[i]];
    }
    return chunks;
  }

  function trace(n) {
    const dictName = n > DICT.input_threshold ? 'clean' : 'noisy';
    const dict = DICT[dictName];
    const chunks = partition(n, 36, DICT.max_aq || 200);
    const words = chunks.map(c => pickWord(dict, c));

    partitionEl.textContent = chunks.length > 1
      ? n + ' = ' + chunks.join(' + ')
      : '';

    wordsEl.innerHTML = words.map((w, i) => {
      const v = chunks[i];
      const canonical = v <= CANONICAL_MAX;
      const cls = canonical ? 'word canonical' : 'word';
      const display = canonical ? w : w.toUpperCase();
      return '<span class="' + cls + '">' + display + '</span>';
    }).join(' ');

    outputEl.hidden = false;
  }

  formEl.addEventListener('submit', function(e) {
    e.preventDefault();
    const n = parseInt(inputEl.value.trim(), 10);
    if (Number.isNaN(n) || n < 0 || n > 999) return;
    trace(n);
  });

  fetch('/assets/aq_buckets.json')
    .then(function(r) {
      if (!r.ok) throw new Error('HTTP ' + r.status);
      return r.json();
    })
    .then(function(data) {
      DICT = data;
      statusEl.innerHTML = '&gt; ccru.aq.trace ARMED <span class="cursor"></span>';
      goBtn.disabled = false;
      inputEl.focus();
    })
    .catch(function(err) {
      statusEl.textContent = '> ccru.aq.trace FAILED: ' + err.message;
      statusEl.style.color = '#f55';
    });
})();
</script>

The trace is real-time. No precomputed phrases. Inputs **0–35** return the canonical character mapped to that value (`17` → `h`; `35` → `z`). **36–111** draws from a broad dictionary including short fragments, abbreviations, and decades like `80s`. **112–200** restricts to longer alphabetic words. **201–999** partitions the input into smaller sums and looks up a word for each. The seams are intentional — the partition arithmetic is shown above the phrase, and the noise at low values isn't smoothed over.

## Corpus

The trace is compiled from a corpus deliberately weighted toward the register the Ccru wrote inside of:

- CCRU — *Writings 1997–2003*
- Nick Land et al. — *Hyperstition* (collective blog, 2004–2008)
- Mark Fisher — *k-punk* (blog, 2003–2016)
- Gilles Deleuze and Félix Guattari — *Anti-Oedipus* (1972)
- Gilles Deleuze and Félix Guattari — *A Thousand Plateaus* (1980)
- H. P. Lovecraft — collected fiction
- William Gibson — *Neuromancer* (1984)
- Cory Doctorow — *Little Brother*, *Down and Out in the Magic Kingdom*, *Makers*
- Bram Stoker — *Dracula* (1897)
- John Milton — *Paradise Lost* (1667)
- Mary Shelley — *Frankenstein* (1818)
- Robert W. Chambers — *The King in Yellow* (1895)
- Arthur Machen — *The Great God Pan* (1894)
- Sigmund Freud — *The Interpretation of Dreams*, *Totem and Taboo*
- Aleister Crowley — *Liber AL vel Legis* (The Book of the Law)
- King James Bible — Genesis, Matthew, Revelation

About three million tokens, eighty thousand unique types after normalisation.

---

The original intent was a debunking tool — to show that any number can be made to mean any thing, given a sufficiently large corpus; that the meaning is supplied by the reader, not the system. What got built is closer to evocative randomness than to debunking, but the apparatus is still pointed at the same target. Whether the resulting coincidence carries meaning is left to the reader.
