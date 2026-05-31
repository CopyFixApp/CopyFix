# CopyFix — Mac Clipboard Manager with Notes and Local AI

> CopyFix is a Mac clipboard manager with notes and local AI built into the same workflow. Search text and images, rewrite text when you ask, and paste back in place.

**Website:** [copyfix.app](https://copyfix.app) · **Download:** [copyfix.app/download](https://copyfix.app/download) · **Pricing:** [copyfix.app/#pricing](https://copyfix.app/#pricing)

---

## What is CopyFix?

CopyFix is a **Mac clipboard manager with notes and local AI** built into the same workflow.

It captures text and images, keeps clipboard history searchable, lets you attach notes to clips, and can rewrite, translate, summarise, or reformat text when you ask. CopyFix then pastes the original or rewritten result back into the app you were using.

Clipboard history stays on your Mac. Local AI runs on-device after the model is downloaded. BYOK is Pro-only, and BYOK requests are sent directly from the app to the provider you choose, without proxying through CopyFix middleware.

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

- **Clipboard history you control.** Text and image clips are captured automatically. Free users can keep up to 1,000 items; Pro raises the limit to 10,000. Older non-pinned items are trimmed automatically.
- **Integrated notes.** Pin the clips you care about and attach detailed notes directly within the app.
- **Search images by what's in them.** CopyFix runs Apple Vision OCR and image classification on-device for screenshots and copied pictures, so you can find them later by typing words you remember seeing.
- **Paste with one hotkey.** A configurable global hotkey opens CopyFix as a utility panel, grabs the current selection when macOS Accessibility can read it, and pastes the chosen item back into the app you were using.
- **Services menu support.** A "Fix with CopyFix" macOS Services entry is included for selected text.
- **Optional local AI.** When you want a quick rewrite, translation, or summary, CopyFix can run a language model locally on Apple Silicon via Apple's MLX framework. After the model is downloaded, prompts are processed on-device and your selection stays on the Mac.
- **Optional BYOK provider support.** Prefer a provider model? Pro unlocks bring-your-own-key support for OpenAI-compatible APIs, Claude, and Gemini. Requests go directly from CopyFix to the provider, not through CopyFix middleware.

## How CopyFix works

1. **Copy as usual.** Use ⌘C as you normally would, or trigger CopyFix's global hotkey to grab the current selection from apps where macOS Accessibility can read it. Text and images both work.
2. **Pick a clip or ask for a rewrite.** Browse the history, search, pin what matters, and add notes. If you want help, type an instruction like *"make it formal"* or *"translate to French"* and CopyFix will run it through the AI provider you selected.
3. **Paste the result back.** CopyFix returns focus to the app you were in and pastes the clip, original or rewritten. The history is always there if you want to go back.

## Privacy

Your clipboard is some of the most sensitive data on your Mac. CopyFix runs on-device by default, and any AI integration is strictly opt-in.

- **Clipboard stays on your Mac.** Clipboard history, prompt history, notes, image OCR, and local model execution are local. Nothing is uploaded anywhere unless you explicitly send selected content to a BYOK provider.
- **Local AI runs on-device.** When you choose the local provider, CopyFix runs an Apple MLX model on your Mac. After the model is downloaded, prompts are processed on-device.
- **BYOK is direct.** API keys are stored in the macOS Keychain, not in plain-text preferences. BYOK requests are sent directly to OpenAI-compatible APIs, Claude, or Gemini without a CopyFix proxy or middleware.
- **Backend scope is limited.** CopyFix backend handles account login, pricing, one-time Pro payments through PayPal, redeem codes, refund/payment records, and request metadata logs. It does not receive BYOK prompt payloads or clipboard content.
- **Local cleanup controls exist.** You can clear local history, reset settings, delete downloaded local models, remove provider keys, and prepare app state for uninstall from CopyFix settings.

Read the full [privacy policy](https://copyfix.app/privacy).

## Use cases

- **Writers and editors** — jump between drafts, quotes, and references without losing what you copied an hour ago; tighten a paragraph with an optional AI rewrite when you want one.
- **Developers** — keep snippets, error messages, and screenshots one search away. Reformat JSON or pull text out of an image with OCR, and call on an AI model only when it actually helps.
- **Support and ops** — pin canned responses, search past replies instantly, and paste them back into your help desk. Optional AI smoothing is there for the trickier messages.
- **Students and researchers** — collect every snippet, citation, and figure from a long session in one searchable place. Format or summarise with AI on demand — never automatically.

## System requirements

- macOS 14.6 or later.
- Apple Silicon Mac (M1 or newer) for optional local AI features. The clipboard manager itself runs on both Apple Silicon and Intel Macs.
- Accessibility permission, so CopyFix can read selections from and paste into other apps.

## Install

1. Download the latest release from [copyfix.app/download](https://copyfix.app/download).
2. Move `CopyFix.app` into `/Applications`.
3. Launch it and grant Accessibility permission when prompted (System Settings → Privacy & Security → Accessibility).
4. Configure a global hotkey in Preferences.

CopyFix is distributed directly from copyfix.app and updates itself via [Sparkle](https://sparkle-project.org/). It is not currently available on the Mac App Store.

## FAQ

### What is CopyFix?

CopyFix is a Mac clipboard manager with notes and local AI built into the same workflow. It captures text and images, lets you attach notes, can rewrite or summarise text when you ask, and pastes results back into the app you were using. The clipboard and notes work on their own, and AI is strictly opt-in.

### Do I have to use the AI features?

No. The clipboard manager, image search, pinning, notes, and paste-anywhere hotkey all work without ever touching an AI model. The AI integration is strictly opt-in — it only runs when you type a prompt and ask for a transformation.

### Does CopyFix work without an internet connection?

Yes. The clipboard manager and image OCR are local. If you want on-device AI rewrites, CopyFix can run language models locally on Apple Silicon using Apple's MLX framework after model download. BYOK providers are optional and only used when you explicitly select one.

### How does the AI integration work?

If you choose to use the AI integration, CopyFix can run a model on-device via Apple's MLX framework. Pro users can also bring their own OpenAI-compatible, Claude, or Gemini key. BYOK requests are sent directly from the app to the provider, without CopyFix proxying them.

### Where is my clipboard history stored?

Locally, in a SwiftData store under your Mac's Application Support directory. Full-resolution clipboard images are saved as PNG files on disk; medium previews and thumbnails are used for display and provider payloads. Nothing is uploaded unless you explicitly run a BYOK provider request.

### How big can the clipboard history get?

Free users can keep up to 1,000 items. Pro unlocks up to 10,000 items. Older non-pinned items are trimmed automatically; pinned items are kept regardless of the limit.

### Can I search my clipboard images?

Yes. CopyFix runs on-device OCR and image classification on every captured image, so you can find old screenshots or copied pictures by typing words that appear in them.

### How much does CopyFix cost?

CopyFix is free to use. CopyFix Pro is a one-time lifetime license that unlocks advanced features forever, including the 10,000-item history limit and BYOK support for OpenAI-compatible APIs, Claude, and Gemini. There are no subscriptions. See [copyfix.app/#pricing](https://copyfix.app/#pricing) for current pricing.

### Is CopyFix on the Mac App Store?

CopyFix is distributed directly from [copyfix.app](https://copyfix.app) and updates itself via Sparkle. It is not currently available on the Mac App Store.

## Links

- **Website:** https://copyfix.app
- **Download:** https://copyfix.app/download
- **Pricing:** https://copyfix.app/#pricing
- **Privacy policy:** https://copyfix.app/privacy
- **Terms of service:** https://copyfix.app/terms

---

<sub>Keywords: clipboard manager for Mac · macOS clipboard manager · clipboard history Mac · clipboard manager with OCR · image clipboard search · Mac copy paste history · clipboard manager with AI · clipboard notes · AI text rewriter Mac · CopyFix.</sub>
