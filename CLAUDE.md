# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Static HTML/CSS/JS portfolio site hosted on GitHub Pages at https://markmanm.github.io.

## Deployment

Every push to `main` deploys automatically via GitHub Pages. There is no build step — edit `index.html` and push.

```bash
git add -A && git commit -m "message" && git push
```

## Architecture

Single-file site (`index.html`). Styles and scripts are inline — no bundler, no framework, no dependencies.

### Password gate

The page is protected by a client-side password gate (JavaScript + Web Crypto SHA-256). The hash stored in the script corresponds to the real password; do not replace it with plaintext. The gate is bypassed for the current browser session via `sessionStorage`.
