# Screenshot Only

A Codex skill that captures the visible rendering of a webpage, PDF, slide deck, spreadsheet, or app and uses those images as the source evidence for your task.

Use it when you want Codex to work from what you can see on screen. For example, it can summarize a PDF, check the labels in a diagram, or compare the figures in two screenshots.

## Install

Clone the repository into your Codex skills directory. The destination should be a new directory.

```sh
git clone https://github.com/ScottChen0115/screenshot-only.git "${CODEX_HOME:-$HOME/.codex}/skills/screenshot-only"
```

## Use

Provide a URL, a file, or screenshots, and specify what you want Codex to do.

> Use $screenshot-only on the attached PDF. Check whether the three figures I listed appear in the document and cite the page where each one appears.

The skill uses the screenshot or rendering tools available in your Codex environment. For PDFs, it describes a Poppler command that renders pages to PNG. Other file formats may require a viewer or a visual export. If a detail is unreadable, the skill asks for a clearer view.

The skill guides which evidence Codex uses. Anything visibly rendered in the screenshot can still be read, including text embedded in an image.

Released under the [MIT License](LICENSE).
