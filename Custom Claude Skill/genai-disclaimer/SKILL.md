---
name: genai-disclaimer
description: "Add an AI-generated disclaimer to every document Claude produces. Use this skill whenever creating or editing presentations (.pptx), Word documents (.docx), PDFs, reports, spreadsheets, or any deliverable file. This skill should trigger alongside the relevant document-creation skill (pptx, docx, pdf, xlsx) — it layers on top of the normal creation workflow. Trigger whenever Claude is producing a file that will be shared, reviewed, or archived."
---

# GenAI Disclaimer

## Overview

Every document Claude produces should include a disclaimer so that readers know it was AI-generated. This skill ensures that disclaimer is placed consistently across all output formats.

## Disclaimer Text

Use this exact text unless the user provides an alternative:

> This document was produced using Claude, an AI assistant by Anthropic. Content should be reviewed for accuracy.

## Placement by Document Type

### PowerPoint (.pptx)

Add the disclaimer as a small text element in the footer area of every slide. Use a muted gray color (e.g., `#888888`) and a small font size (8–9pt) so it's visible but not distracting. Place it at the bottom-center or bottom-right of each slide, below the main content area.

If the presentation uses a master slide or template, add the disclaimer to the master so it appears on all slides automatically rather than adding it slide by slide.

### Word Documents (.docx)

Add the disclaimer as a document footer that appears on every page. Use a smaller font size than the body text (typically 8–9pt), in a muted gray. Center-align or right-align it in the footer region.

If the document already has footers (e.g., page numbers), place the disclaimer on a separate line above or below the existing footer content — don't replace it.

### PDFs

When creating a PDF from scratch, add the disclaimer as footer text on every page, similar to the Word document approach — small, gray, centered at the bottom.

When generating a PDF via HTML/CSS (which is common), add a footer element styled with:
- Font size ~8pt
- Color `#888888`
- Centered at the page bottom
- A thin top border or some spacing to separate it from the content

### Spreadsheets (.xlsx)

Add the disclaimer in a dedicated row at the top of the first sheet (Row 1), merged across all used columns, in a small italic gray font. Then start the actual data below it.

Alternatively, if the spreadsheet has a "Summary" or "Cover" sheet, place the disclaimer there instead.

### HTML / Markdown / Other Text Formats

For HTML files, add a `<footer>` element at the bottom of the page with the disclaimer styled subtly.

For Markdown files, add the disclaimer as an italic line at the very end of the document:

```
*This document was produced using Claude, an AI assistant by Anthropic. Content should be reviewed for accuracy.*
```

## When the User Customizes the Disclaimer

If the user provides their own disclaimer text, use that instead — the exact wording is theirs to decide. The placement and styling guidance above still applies.

If the user explicitly says they don't want a disclaimer on a particular document, respect that and skip it.
