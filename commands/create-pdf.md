---
description: Compile documentation sections into a formatted PDF (Step 3 of 4)
---

# Task 3: PDF Creation

Now that all documentation sections have been generated, please compile them into a professionally formatted PDF.

## Compilation Instructions

Use a separate sub-agent to concatenate the documentation sections into a single PDF document.

### Tooling Preferences

1. **Preferred**: Use Typst if it is available to generate attractive documentation.
2. **Fallback**: If Typst is not available, use whatever tooling is available on the environment (e.g., Pandoc, WeasyPrint, or similar).

### PDF Formatting Requirements

- **Font**: Use IBM Plex Sans as the font. If it is not available or installed, you can install it into this repository or, ideally, onto the host system.
- **Footer**: Include a footer displaying the current page number and the total page count.
- **Version**: Display the version number prominently on the title page.
- **Date**: Include the creation date on the title page.

### Compilation Procedure

1. Concatenate all sections from `docs/sections/` in numerical order.
2. Render any Mermaid diagrams from `docs/assets/` and embed them in the appropriate locations.
3. Generate the PDF and save it to `docs/output/` with a descriptive filename (e.g., `user-manual-v1.0.pdf`).

Once the PDF has been generated, confirm completion and provide the path to the output file. Await the next task instruction for dissemination.
