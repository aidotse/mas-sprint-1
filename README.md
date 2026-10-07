# WP3 Sprint 1 review: presentation

Quarto + Reveal.js deck for the WP3 (Self-evolving MAS & Knowledge Management) Sprint 1 review. Built on the [aidotse/quarto-pres](https://github.com/aidotse/quarto-pres) template.

## Present

```bash
quarto render index.qmd          # writes index.html + index_files/
xdg-open index.html              # or open it in any browser
```

Or run `quarto preview index.qmd` for live reload while editing.

In the browser: `S` opens speaker notes (with timings), `O`/`Esc` shows the slide overview, `F` goes full screen.

## Layout

The width is fixed at 1920 px, and the slide height follows the browser window's aspect ratio, limited to between 16:9 (1080) and 4:3 (1440) by `responsive.html`. That way 16:10 laptops get no letterboxing. Slides are flex columns: the title stays on top and the free vertical space is shared out evenly between the content blocks (see the end of `style.css`). PDF export (`?print-pdf`) keeps the fixed 1920×1080 layout.

## Structure

- **Main deck (~15 min):** Sprint 1 (capability, team, SOTA, benchmark, other results, risks) → Sprint 2 (field context, seven-option menu, partner pull, proposed focus, timeline) → workshop questions
- **Backup:** FLIWBO details, competitor tables, one slide per Sprint 2 option, debate vs. voting, frontier platforms, Claude Managed Agents

## Export to PDF (later)

Open `index.html?print-pdf` in Chrome and print to PDF, or:

```bash
quarto render index.qmd -M embed-resources:true   # single self-contained HTML
```
