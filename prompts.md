# Prompts

Settings every time: Studio → Presentation → **Presenter slides**, language **English**, length **Default**. The dialog forgets them.

## Plan: two decks, one resource at a time

| Round | Sources | Prompt | Output |
|---|---|---|---|
| 1 | the article | B | deck 1 |
| 2 | the article + deck 1 PDF (if it passed the check) + the two photos in `fonti/` | C | deck 2 |

Deck A (one-line prompt) is only shown by the teacher: `Create a 7-slide presentation on this article for a non-specialist academic audience.`

## B · content rules

```
Create a 7-slide presentation on this article for a non-specialist academic audience. Rules: use only what is written in the uploaded article; do not add facts, dates, names, numbers or examples that are not in the text. Every slide title is a full sentence stating what the article claims, not a topic label. Where the author is tentative (suggests, may, possibly), keep the same caution; never turn a hypothesis into a proven fact. Do not generate images of places, buildings or people; use only text, simple diagrams or a timeline. The last slide states the limits and open questions the author acknowledges.
```

## C · rules + keep deck 1's structure + only the uploaded photos + UNIPG theme

```
Create a 7-slide presentation on this article for a non-specialist academic audience. Rules: use only what is written in the uploaded article; do not add facts, dates, names, numbers or examples that are not in the text. Every slide title is a full sentence stating what the article claims, not a topic label. Where the author is tentative (suggests, may, possibly), keep the same caution; never turn a hypothesis into a proven fact. If a presentation is among the sources, keep its order and its titles unless the article contradicts them. For pictures of the cathedral use only the uploaded photographs, with their credit on the slide; never generate an image of a building, a place or a person. The last slide states the limits and open questions the author acknowledges. Visual theme, University of Perugia, apply it to every slide: white background #FFFFFF; titles and main accent in UNIPG blue #27348B; red #E30613 only for one key word per slide; grey #8D8F95 for captions and sources; light grey #E8E8E8 for boxes and table headers. Font: Roboto for everything. A thin blue rule under each title. Keep the top-right corner empty for the university logo. Flat design: no gradients, no shadows.
```

## Rivedi · theme only (when the generations are gone)

```
Restyle only, keep every word, diagram and the layout: white background #FFFFFF; title in UNIPG blue #27348B, Roboto bold, with a thin blue rule under it; one key word in red #E30613; captions in grey #8D8F95; boxes in light grey #E8E8E8; diagram colours only blue #27348B and grey; Roboto for all text; top-right corner left empty.
```

## What we measured on 29/9

- Daily limit: **3 presentations per account per day**, on the personal account and on the @unipg tenant alike. The 4th attempt shows "Hai raggiunto il limite giornaliero di slide".
- Latency on the tenant: 3 decks launched in parallel at 08:27, all ready by ~08:34 (about 7 minutes).
- The same prompt B run on two accounts gave two different decks: different titles, different number of diagrams, one with label titles despite the rule. Style is steerable, structure is not reproducible.
- Generated slides are images (PNG 1376x768): text cannot be edited in place, only through Rivedi.
- The quota did **not** reset at 09:00 (retried 09:03: still blocked). It is not a midnight-Pacific reset.
- Rivedi on 1 slide: ~2 minutes. Rivedi on all 7 slides (theme change): 13+ minutes.
- Download: ⋮ → PDF or .pptx. The .pptx is 7 pictures, no text boxes: nothing to edit in PowerPoint either.
- Source: the direct PDF link https://journal.eahn.org/article/7590/galley/21444/download/ imports fine as a "website" source.

- Images cannot be added as sources by URL (both Wikimedia links failed): upload them as files.
- Photos uploaded as files after the decks existed; Rivedi on deck A asked to use them: **failed twice** ("Revisione della presentazione non riuscita"). Rivedi runs "in base a 1 fonte": only the sources the deck was generated from. New sources need a new generation.
