# The three prompts

Same article, same settings: Studio → Presentation → **Presenter slides**, language **English**, length **Default**.

## A · Minimal

```
Create a 7-slide presentation on this article for a non-specialist academic audience.
```

## B · Grounded (anti-hallucination)

```
Create a 7-slide presentation on this article for a non-specialist academic audience. Rules: use only what is written in the uploaded article; do not add facts, dates, names, numbers or examples that are not in the text. Every slide title is a full sentence stating what the article claims, not a topic label. Where the author is tentative (suggests, may, possibly), keep the same caution; never turn a hypothesis into a proven fact. Do not generate images of places, buildings or people; use only text, simple diagrams or a timeline. The last slide states the limits and open questions the author acknowledges.
```

## C · Grounded + UNIPG theme

In class: generated from scratch by each participant. For the demo deck, the quota was gone, so C was made by applying this theme to deck B **with Rivedi**, one instruction per slide (same words as B, only the look changes):

```
Restyle only, keep every word, diagram and the layout: white background #FFFFFF; title in UNIPG blue #27348B, Roboto bold, with a thin blue rule under it; one key word in red #E30613; captions in grey #8D8F95; boxes in light grey #E8E8E8; diagram colours only blue #27348B and grey; Roboto for all text; top-right corner left empty.
```

Prompt for a fresh generation:

Same content rules as B, only the look changes. Colours and font taken from unipg.it (CSS and official logo).

```
Create a 7-slide presentation on this article for a non-specialist academic audience. Rules: use only what is written in the uploaded article; do not add facts, dates, names, numbers or examples that are not in the text. Every slide title is a full sentence stating what the article claims, not a topic label. Where the author is tentative (suggests, may, possibly), keep the same caution; never turn a hypothesis into a proven fact. Do not generate images of places, buildings or people; use only text, simple diagrams or a timeline. The last slide states the limits and open questions the author acknowledges. Visual theme, University of Perugia, apply it to every slide: white background #FFFFFF; titles and main accent in UNIPG blue #27348B; red #E30613 only for one key word per slide; grey #8D8F95 for captions and sources; light grey #E8E8E8 for boxes and table headers. Font: Roboto for everything. A thin blue rule under each title. Keep the top-right corner empty for the university logo. Flat design: no gradients, no shadows, no stock photos.
```

For a conference theme, swap the hex codes and the font with the ones in the conference template.

## C0 · Grounded + limestone palette (generated 29/9 morning, kept for comparison)

```
... same as B ... Visual style, apply it to every slide: background limestone #F3EDE2; text dark stone #2B2622; one accent terracotta #A4552F for titles and key words; secondary olive #5E6B4A only for diagrams and timelines. Serif font for titles, clean sans-serif for body text. Flat design: no gradients, no shadows, no stock photos, generous white space.
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
