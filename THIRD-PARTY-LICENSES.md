# Third-party notices for Luxraj Editor

This project loads its PDF libraries from jsDelivr instead of storing their full distribution files in this repository.

- **PDF.js 5.7.284** — developed by Mozilla and contributors; [Apache License 2.0](https://github.com/mozilla/pdf.js/blob/v5.7.284/LICENSE). The official release is [Mozilla PDF.js v5.7.284](https://github.com/mozilla/pdf.js/releases/tag/v5.7.284).
- **pdf-lib 1.17.1** — [project](https://github.com/Hopding/pdf-lib), [MIT License](https://github.com/Hopding/pdf-lib/blob/master/LICENSE.md).

## Clarification about the earlier bundled PDF.js

The original [mikispag/pdf-editor](https://github.com/mikispag/pdf-editor) repository contains a `vendor/pdf.min.mjs` bundle whose embedded API version is **4.10.38**. That bundle begins with the notice **Copyright 2024 Mozilla Foundation** and identifies the Apache License 2.0. PDF.js is Mozilla's project and that bundle's copyright notice should not be attributed to the editor repository's author.

In this temporary test repository, `vendor/pdf.min.mjs` is not that full bundle: it is a small CDN shim exporting `pdfjs-dist@5.7.284`. The application code also points the PDF.js worker to the 5.7.284 CDN build.

## Separate editor-source attribution

Luxraj Editor is adapted from the MIT-licensed [mikispag/pdf-editor project](https://github.com/mikispag/pdf-editor). The upstream MIT license notice is preserved in [UPSTREAM-MIT-LICENSE.md](UPSTREAM-MIT-LICENSE.md); see the root [LICENSE](LICENSE) for the separate Luxraj-owned-materials notice. That acknowledgement applies to the adapted editor application code, not to ownership of PDF.js or pdf-lib.

Because both libraries are loaded from a CDN, an internet connection is required.
