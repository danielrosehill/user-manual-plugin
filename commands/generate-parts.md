---
description: Generate individual documentation sections using a writing agent (Step 2 of 4)
---

# Task 2: Generating Documentation Parts

Now that the documentation folder structure is in place, please generate the individual documentation sections.

## Agent Instructions

Engage a documentation writing agent and provide it with the following context:

The instructions provided to the documentation generation subagent should explain why this distinction and context are being provided: Private documentation may contain feature outlines, specific code snippets, or credentials that would otherwise never be included in public documentation.

## Formatting and Tone of Voice Guidelines

Relative to public-facing documentation, the documentation can be written in a friendlier tone of voice while still adhering to best standards of technical documentation writing.

Assuming you know my name, you can include it in the documentation, such as "Homebox Backup Script Operation User Manual for Daniel's Attention," and reference the date of creation.

### Document Authoring Rules

- Do not use emojis
- Provide code samples in proper codefences
- Add diagrams where appropriate and valuable. Use Mermaid if possible. You can install the CLI on the host or use an MCP.
- Include a version number. If there are previous iterations of the user manual visible, please use the next sequential version number for this creation.

## Generation Procedure

The documentation should be generated in an organized and planned manner:

1. **Feature Inventory**: Generate a comprehensive list of features to document based on the codebase analysis.
2. **Section-by-Section Generation**: Generate each documentation section individually, saving each to the `docs/sections/` directory with clear, numbered filenames (e.g., `01-introduction.md`, `02-installation.md`, etc.).
3. **Diagram Creation**: For any diagrams, save the Mermaid source files to `docs/assets/` and reference them from the relevant sections.

Once all sections have been generated, confirm completion and provide a summary of the sections created. Await the next task instruction for PDF compilation.
