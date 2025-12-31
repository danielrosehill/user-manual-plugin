---
description: Generate a complete personal user manual for the current project (full workflow)
---

I would like to create a user manual to document what we created today and ensure I remember how to operate this codebase in the future.

Please note that the intended use of this user manual is strictly for my own private reference. This is not intended as public documentation.

In the unlikely event that this repository also contains a public-facing document, please create these private documents in a separate path that is `.gitignore`d.

In most cases, however, there will not be any public-facing documentation created within a private repository.

The instructions provided to the documentation generation subagent should explain why this distinction and context are being provided: Private documentation may contain feature outlines, specific code snippets, or credentials that would otherwise never be included in public documentation.

## Formatting And Tone Of Voice Guidelines

Relative to public-facing documentation, the documentation can be written in a friendlier tone of voice while still adhering to best standards of technical documentation writing.

Assuming you know my name, you can include it in the documentation, such as "Homebox Backup Script Operation User Manual for Daniel's Attention," and reference the date of creation.

Other document authoring rules:

- Do not use emojis
- Provide code samples in proper codefences
- Add diagrams where appropriate and valuable. Use Mermaid if possible. You can install the CLI on the host or use an MCP.

Also, include a version number. If there are previous iterations of the user manual visible, please use the next sequential version number for this creation.

Make sure to include a footer displaying the current page number and the total page count. Use IBM Sans as the font. If it is not available or installed, you can install it into this repository or, ideally, onto the host system.

## Creation Procedure

To create the user manual, please proceed as follows:

1.  Create a `docs` folder.
2.  Engage a documentation writing agent.
3.  Instruct the documentation authoring agent on the nature of this documentation creation project. Make the agent aware that the documentation should be written in a suitable tone of voice for my own reference.

The documentation should be generated in an organized and planned manner:

1.  Generate a list of features to document.
2.  Generate the documentation section by section.
3.  Use a separate sub-agent to concatenate the documentation into a PDF.

Use typst if it is available to generate attractive documentation. If not, use whatever tooling is available on the environment.

Once the task has been completed, you can inform me that the documentation is ready. You can assume that all documentation may be committed to the repository and pushed. I may also want to use an MCP to store the readable version of the documentation in PDF format elsewhere.
