# Lab 3 — From paper to slides

IA@UNIPG · Incontro 3 "Ricerca e IA" · Lab 3 SSH "Scrittura accademica e presentazioni" · 29 settembre 2026 · Centro Linguistico di Ateneo · tre turni da 55'

**Online:** https://niccolosalvini.github.io/unipg_ai_workshop/ (pagina materiali) · [slide](https://niccolosalvini.github.io/unipg_ai_workshop/deck/deck.html) · [slide PDF](https://niccolosalvini.github.io/unipg_ai_workshop/deck/deck.pdf)

| Cartella / file | Cosa c'è |
|---|---|
| `deck/deck.qmd` | Il deck in inglese, Quarto + reveal.js, tema UNIPG in `deck/unipg.scss`. `quarto render deck/deck.qmd` |
| `deck/deck.html`, `deck/deck.pdf` | Output: HTML da proiettare, PDF per la chiavetta (decktape) |
| `generated/` | I deck generati il 29/9 con Gemini Notebook, come li esporta lo strumento (PDF, un .pptx) |
| `site/index.html` | Pagina per i partecipanti: link al PDF, i tre prompt da copiare, checklist, Rivedi, deck d'esempio |
| `prompts.md` | I prompt A/B/C, l'istruzione Rivedi per il tema, le misure fatte il 29/9 |
| `regia/canovaccio_regia.md` | Una pagina: scaletta, fatti misurati, deck di demo, piano B |
| `articolo/` | Van Ooijen 2019, PDF open access (CC BY) |
| `scheda/` | Scheda laboratorio UNIPG (PDF) |

**L'ora.** Who I am → tre modi di fare slide (app, Beamer, HTML, con la lezione ESE come esempio) → Gemini Notebook: tre deck A/B/C lanciati insieme → trucchi mentre generano → confronto A/B/C e Rivedi slide per slide → tre regole.

**Vincolo.** 3 presentazioni al giorno per account, anche su @unipg.it. Rivedi non consuma quota.

**Rigenerare le slide:** `quarto render deck/deck.qmd`, poi dal folder `deck/` con un server locale: `npx decktape reveal http://127.0.0.1:8899/deck/deck.html deck/deck.pdf`.
