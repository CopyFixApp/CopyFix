# CopyFix — Clipboard Manager for Mac with History, OCR & AI

> An advanced clipboard manager for macOS with clipboard history, image OCR search, and optional AI integration. Free download.

**Website:** [copyfix.app](https://copyfix.app) · **Download:** [copyfix.app/download](https://copyfix.app/download) · **Pricing:** [copyfix.app/#pricing](https://copyfix.app/#pricing)

---

## What is CopyFix?

CopyFix is a **clipboard manager for Mac** that captures everything you copy — text and images — keeps it searchable, and pastes any clip back into any app with a global hotkey. When you want help editing, an **optional AI integration** can rewrite, translate, summarise, or reformat the clip you just grabbed — locally on your Mac via Apple's MLX framework, or in the cloud via CopyFix Cloud.

The clipboard manager works perfectly well on its own. AI is opt-in and never runs unless you trigger it.

## Table of contents

- [Features](#features)
- [How CopyFix works](#how-copyfix-works)
- [Privacy](#privacy)
- [Use cases](#use-cases)
- [System requirements](#system-requirements)
- [Install](#install)
- [FAQ](#faq)
- [Links](#links)

## Features

- **10,000-item clipboard history.** Every text and image you copy is captured automatically. Pin the ones you care about, attach notes, and trim the rest with configurable history limits.
- **Search images by what's in them.** CopyFix runs on-device OCR and image classification on screenshots and copied pictures, so you can find them later by typing words you remember seeing.
- **Paste anywhere with one hotkey.** A configurable global hotkey opens CopyFix as a non-intrusive panel, grabs your current selection, and pastes the chosen item straight back into the app you were using.
- **Works in every app.** Mail, Pages, Xcode, VS Code, Slack, your browser — if the macOS Accessibility API can read a selection, CopyFix can work with it. A Services menu entry is included too.
- **Optional local AI integration.** When you want a quick rewrite, translation, or summary, CopyFix can run a language model locally on Apple Silicon via Apple's MLX framework. Your selection never leaves the Mac.
- **Optional cloud AI integration.** Prefer a stronger model? CopyFix Cloud handles the heavier rewrites without you needing to manage any external accounts or API keys. AI is fully opt-in and never runs unless you trigger it.

## How CopyFix works

1. **Copy as usual.** Use ⌘C as you normally would, or trigger CopyFix's global hotkey to grab the current selection from any app. Text and images both work.
2. **Pick a clip — or ask for a rewrite.** Browse the history, search, and pin what matters. If you want help, type an instruction like *"make it formal"* or *"translate to French"* and CopyFix will run it through the AI model of your choice.
3. **Paste the result back.** CopyFix returns focus to the app you were in and pastes the clip — original or rewritten — straight in place. The history is always there if you want to go back.

## Privacy

Your clipboard is some of the most sensitive data on your Mac. CopyFix runs entirely on-device by default, and any AI integration is strictly opt-in.

- **Clipboard stays on your Mac.** The clipboard history and image OCR both run locally. Nothing is uploaded anywhere unless you explicitly start a cloud AI request.
- **AI is opt-in, local-first.** When you do ask for a rewrite, CopyFix can run a model on-device via Apple's MLX framework. CopyFix Cloud is only used when you choose it, and a privacy reminder is shown before the first cloud request.
- **Keys in the Keychain.** API keys are stored in the macOS Keychain, not in plain-text preferences. Clipboard history lives in a local SwiftData store under Application Support.

Read the full [privacy policy](https://copyfix.app/privacy).

## Use cases

- **Writers and editors** — jump between drafts, quotes, and references without losing what you copied an hour ago; tighten a paragraph with an optional AI rewrite when you want one.
- **Developers** — keep snippets, error messages, and screenshots one search away. Reformat JSON or pull text out of an image with OCR, and call on an AI model only when it actually helps.
- **Support and ops** — pin canned responses, search past replies instantly, and paste them back into your help desk. Optional AI smoothing is there for the trickier messages.
- **Students and researchers** — collect every snippet, citation, and figure from a long session in one searchable place. Format or summarise with AI on demand — never automatically.

## System requirements

- macOS 14 (Sonoma) or later.
- Apple Silicon Mac (M1 or newer) for the optional on-device AI features. The clipboard manager itself runs on both Apple Silicon and Intel Macs.
- Accessibility permission, so CopyFix can read selections from and paste into other apps.

## Install

1. Download the latest release from [copyfix.app/download](https://copyfix.app/download).
2. Move `CopyFix.app` into `/Applications`.
3. Launch it and grant Accessibility permission when prompted (System Settings → Privacy & Security → Accessibility).
4. Configure a global hotkey in Preferences.

CopyFix is distributed directly from copyfix.app and updates itself via [Sparkle](https://sparkle-project.org/). This is necessary so it can access the macOS Accessibility APIs and on-device AI models that the App Store sandbox would otherwise restrict.

## FAQ

### What is CopyFix?

CopyFix is an advanced clipboard manager for macOS. It captures everything you copy — text and images — keeps it searchable, and pastes any clip back into any app with a global hotkey. An optional AI integration can rewrite, translate, summarise, or reformat the clip you just grabbed when you want it to, but the clipboard manager works perfectly well on its own.

### Do I have to use the AI features?

No. The clipboard manager, image search, pinning, notes, and paste-anywhere hotkey all work without ever touching an AI model. The AI integration is strictly opt-in — it only runs when you type a prompt and ask for a transformation.

### Does CopyFix work without an internet connection?

Yes. The clipboard manager and image OCR are entirely local. If you want AI rewrites offline, CopyFix can run language models locally on Apple Silicon using Apple's MLX framework. Cloud providers are optional and only used when you explicitly select one.

### How does the AI integration work?

If you choose to use the AI integration, CopyFix can run a model on-device via Apple's MLX framework, or use CopyFix Cloud for stronger models. You can switch between them at any time from settings, or turn the AI features off entirely.

### Where is my clipboard history stored?

Locally, in a SwiftData store under your Mac's Application Support directory. Full-resolution clipboard images are saved as PNG files on disk; only thumbnails are kept in memory. Nothing is uploaded unless you explicitly run a cloud transformation.

### How big can the clipboard history get?

You can keep up to roughly 10,000 items. Older non-pinned items are trimmed automatically; pinned items are kept regardless of the limit.

### Can I search my clipboard images?

Yes. CopyFix runs on-device OCR and image classification on every captured image, so you can find old screenshots or copied pictures by typing words that appear in them.

### How much does CopyFix cost?

The clipboard manager, image search, and the optional local AI integration are free. CopyFix Pro is a paid subscription that unlocks higher rate limits and stronger cloud models for users who want the cloud AI integration. See [copyfix.app/#pricing](https://copyfix.app/#pricing) for current pricing.

### Is CopyFix on the Mac App Store?

CopyFix is distributed directly from [copyfix.app](https://copyfix.app) and updates itself via Sparkle. This lets it access the macOS Accessibility APIs and on-device AI models that the App Store sandbox would otherwise restrict.

## Links

- **Website:** https://copyfix.app
- **Download:** https://copyfix.app/download
- **Pricing:** https://copyfix.app/#pricing
- **Privacy policy:** https://copyfix.app/privacy
- **Terms of service:** https://copyfix.app/terms

---

<sub>Keywords: clipboard manager for Mac · macOS clipboard manager · clipboard history Mac · clipboard manager with OCR · image clipboard search · Mac copy paste history · clipboard manager with AI · advanced clipboard manager · AI text rewriter Mac · CopyFix.</sub>
