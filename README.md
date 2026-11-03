# ZamDict — Zambia's Living Dictionary

> **Beta software:** ZamDict is still being improved. Entries, translations, offline behavior, AI answers, and scanning features may be incomplete or incorrect. Please test thoughtfully and share constructive feedback.

ZamDict is a mobile-friendly dictionary and phrasebook project for exploring English alongside major Zambian languages. The current app includes **Nyanja, Bemba, Chewa, Tonga, Lozi, Nsenga, and Tumbuka**. It is built in Zambia by World Of Discoveries (WOD), and collaboration, corrections, and testing feedback are welcome.

## Try it

This repository contains the single-file web app at [`index.html`](index.html). To test it, download the file from GitHub (or choose **Code → Download ZIP**), then open it in a modern browser. Some browser features—especially camera access for Scan & Translate—may require serving the file from `localhost` or HTTPS rather than opening it directly from disk.

The app is a beta, not a production service. Network access is used for some shared dictionary data and online features. Offline lookup is supported for cached data, but availability depends on what has already been loaded on your device.

## What it does

- Search and browse English and Zambian-language entries and phrase collections.
- Explore language categories, alphabetical browsing, word details, examples, and related entries where available.
- Save preferences and some offline/search data locally in your browser.
- Use **Zama**, an optional AI assistant, with Groq models. The public release does **not** include an API key; AI use requires your own Groq key in the app settings.
- Try **Scan & Translate**, an experimental camera/OCR feature that is explicitly marked beta in the app.
- Use the responsive interface on mobile or desktop.

## AI setup and key safety

AI assistance is optional. If you choose to test it, provide your own Groq API key in the app settings on a device you control. The key is saved in that browser's local storage and is used directly by the browser to call Groq; it is not a secure production secret store. Do not use a valuable, long-lived key, do not share the device/browser profile, and revoke the key when you are done. Never paste keys into GitHub issues or pull requests.

## Data, privacy, and beta limitations

The app is a client-side HTML/CSS/JavaScript application. It connects to a preconfigured Firebase Realtime Database for some shared data and online behavior, and may load resources from external providers such as Groq, EmailJS, CDNs, and the OCR library. The public-release copy has no embedded AI credential or personal email address, and its email feedback delivery is disabled. Local preferences and cached data may remain in your browser storage.

The backend's ownership, access rules, data contents, privacy practices, and retention have **not** been independently audited as part of this repository preparation. Avoid entering confidential or sensitive information. Before using the app for production or collecting community submissions at scale, review the backend rules, data handling, abuse protections, and third-party services.

Language content is provided for exploration and learning, not as an authoritative linguistic, educational, legal, or medical source. Please report suspected errors with context and, where possible, a source or a fluent-speaker review.

## Help improve ZamDict

You are welcome to collaborate. Open a GitHub issue to report a bug, suggest a feature, or propose a language correction. Include the language, the word or phrase, what you expected, what happened, and your device/browser when relevant. Do not include personal data, private messages, or API keys. Pull requests are welcome; see [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Technical notes

- **App format:** one standalone `index.html`; no build step or package installation is required.
- **Browser storage:** local storage and IndexedDB are used for preferences and selected cached data.
- **External integrations:** Firebase Realtime Database, Groq (optional AI), EmailJS (feedback delivery disabled in this public copy), CDN-hosted fonts and OCR code.
- **License:** no license has been selected for this project yet. Public availability allows people to view and download the repository, but does not by itself grant permission to reuse, redistribute, or modify the code. Please contact the maintainer before reusing it; a license can be added once the project owner chooses one.

## Project status

ZamDict is an evolving beta. The interface and feature set may change, some services may be unavailable, and language coverage is incomplete. Testing and community collaboration are encouraged; please use issues and pull requests to make improvements visible and reviewable.
