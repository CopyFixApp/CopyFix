# CopyFix — Private Clipboard Manager, Note Taker & AI Writing Tool

> A private macOS clipboard workspace with notes, searchable images, completely offline local AI, and direct BYOK provider support. Free to use, with a one-time Pro unlock and no subscriptions.

**Website:** [copyfix.app](https://copyfix.app) · **Download:** [copyfix.app/download](https://copyfix.app/download) · **Pricing:** [copyfix.app/#pricing](https://copyfix.app/#pricing)

---

## What is CopyFix?

CopyFix is an **all-in-one workspace for Mac** that combines a clipboard manager, a note taker, and an AI writing tool into a single application working seamlessly together.

As a **clipboard manager**, it captures what you copy — text and images — keeps it searchable, and pastes any clip back into any app with a global hotkey. As a **note taker**, it lets you pin clips, organize them, and attach personal notes. And as an **AI writing tool**, it can rewrite, translate, summarise, or reformat your text with local models that run completely offline on your Mac, or with your own OpenAI-compatible, Claude, or Gemini key.

These tools work together, but AI is always opt-in and never runs unless you trigger it. BYOK requests are sent directly from the app to the provider you choose, without proxying through CopyFix middleware.

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

- **Clipboard history you control.** Every text and image you copy is captured automatically. Free users can keep up to 1,000 items; Pro raises the limit to 10,000. Older non-pinned items are trimmed automatically.
- **Integrated Note Taker.** Pin the clips you care about, organize them, and attach detailed notes directly within the app, turning your clipboard into a powerful knowledge base.
- **Search images by what's in them.** CopyFix runs on-device OCR and image classification on screenshots and copied pictures, so you can find them later by typing words you remember seeing.
- **Paste anywhere with one hotkey.** A configurable global hotkey opens CopyFix as a non-intrusive panel, grabs your current selection, and pastes the chosen item straight back into the app you were using.
- **Works in every app.** Mail, Pages, Xcode, VS Code, Slack, your browser — if the macOS Accessibility API can read a selection, CopyFix can work with it. A Services menu entry is included too.
- **Optional offline local AI.** When you want a quick rewrite, translation, or summary, CopyFix can run a language model locally on Apple Silicon via Apple's MLX framework. After the model is downloaded, prompts are processed completely offline and your selection never leaves the Mac.
- **Optional BYOK provider support.** Prefer a provider model? Pro unlocks bring-your-own-key support for OpenAI-compatible APIs, Claude, and Gemini. Requests go directly from CopyFix to the provider, not through CopyFix middleware.

## How CopyFix works

1. **Copy as usual.** Use ⌘C as you normally would, or trigger CopyFix's global hotkey to grab the current selection from any app. Text and images both work.
2. **Pick a clip — or ask for a rewrite.** Browse the history, search, and pin what matters. If you want help, type an instruction like *"make it formal"* or *"translate to French"* and CopyFix will run it through the AI model of your choice.
3. **Paste the result back.** CopyFix returns focus to the app you were in and pastes the clip — original or rewritten — straight in place. The history is always there if you want to go back.

## Privacy

Your clipboard is some of the most sensitive data on your Mac. CopyFix runs on-device by default, and any AI integration is strictly opt-in.

- **Clipboard stays on your Mac.** Clipboard history, prompt history, image OCR, and local model execution are local. Nothing is uploaded anywhere unless you explicitly send selected content to a BYOK provider.
- **Local AI is completely offline.** When you choose the local provider, CopyFix runs an Apple MLX model on your Mac. After the model is downloaded, prompts are processed without network access.
- **BYOK is direct.** API keys are stored in the macOS Keychain, not in plain-text preferences. BYOK requests are sent directly to OpenAI-compatible APIs, Claude, or Gemini without a CopyFix proxy or middleware.

Read the full [privacy policy](https://copyfix.app/privacy).

## Use cases

- **Writers and editors** — jump between drafts, quotes, and references without losing what you copied an hour ago; tighten a paragraph with an optional AI rewrite when you want one.
- **Developers** — keep snippets, error messages, and screenshots one search away. Reformat JSON or pull text out of an image with OCR, and call on an AI model only when it actually helps.
- **Support and ops** — pin canned responses, search past replies instantly, and paste them back into your help desk. Optional AI smoothing is there for the trickier messages.
- **Students and researchers** — collect every snippet, citation, and figure from a long session in one searchable place. Format or summarise with AI on demand — never automatically.

## System requirements

- macOS 14 (Sonoma) or later.
- Apple Silicon Mac (M1 or newer) for optional local AI features. The clipboard manager itself runs on both Apple Silicon and Intel Macs.
- Accessibility permission, so CopyFix can read selections from and paste into other apps.

## Install

1. Download the latest release from [copyfix.app/download](https://copyfix.app/download).
2. Move `CopyFix.app` into `/Applications`.
3. Launch it and grant Accessibility permission when prompted (System Settings → Privacy & Security → Accessibility).
4. Configure a global hotkey in Preferences.

CopyFix is distributed directly from copyfix.app and updates itself via [Sparkle](https://sparkle-project.org/). This is necessary so it can access the macOS Accessibility APIs and on-device AI models that the App Store sandbox would otherwise restrict.

## FAQ

### What is CopyFix?

CopyFix is an all-in-one solution for macOS featuring a clipboard manager, a note taker, and an AI writing tool. It captures everything you copy, lets you attach notes to your clips, and includes an optional AI integration to rewrite, translate, summarise, or reformat your text. All of this is within a single app, working seamlessly together. The clipboard and notes work perfectly well entirely on their own, and AI is strictly opt-in.

### Do I have to use the AI features?

No. The clipboard manager, image search, pinning, notes, and paste-anywhere hotkey all work without ever touching an AI model. The AI integration is strictly opt-in — it only runs when you type a prompt and ask for a transformation.

### Does CopyFix work without an internet connection?

Yes. The clipboard manager and image OCR are entirely local. If you want AI rewrites offline, CopyFix can run language models locally on Apple Silicon using Apple's MLX framework. BYOK providers are optional and only used when you explicitly select one.

### How does the AI integration work?

If you choose to use the AI integration, CopyFix can run a model on-device via Apple's MLX framework. Pro users can also bring their own OpenAI-compatible, Claude, or Gemini key. BYOK requests are sent directly from the app to the provider, without CopyFix proxying them.

### Where is my clipboard history stored?

Locally, in a SwiftData store under your Mac's Application Support directory. Full-resolution clipboard images are saved as PNG files on disk; only thumbnails are kept in memory. Nothing is uploaded unless you explicitly run a BYOK provider request.

### How big can the clipboard history get?

Free users can keep up to 1,000 items. Pro unlocks up to 10,000 items. Older non-pinned items are trimmed automatically; pinned items are kept regardless of the limit.

### Can I search my clipboard images?

Yes. CopyFix runs on-device OCR and image classification on every captured image, so you can find old screenshots or copied pictures by typing words that appear in them.

### How much does CopyFix cost?

CopyFix is free to use. CopyFix Pro is a one-time lifetime license that unlocks advanced features forever, including the 10,000-item history limit and BYOK support for OpenAI-compatible APIs, Claude, and Gemini. There are no subscriptions. See [copyfix.app/#pricing](https://copyfix.app/#pricing) for current pricing.

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
