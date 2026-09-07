# Pointrans “Guangbiao Fanyi”

Place the pointer on an English target and hold Option: see a local Simplified Chinese dictionary result for an ordinary word, or click AI for a source-line-aware Chinese explanation of code, paths, variables, and abbreviations.

> **Product preview — no public download yet**
>
> This page reflects the internally accepted product baseline `0.1.0 (13)`. Product acceptance confirms the current behavior; it does not mean that a public installer has passed signing, notarization, privacy, or production-service review.
>
> This is the official public product hub for the Chinese-user edition of Pointrans. It contains product information, release notes, help, and feedback channels, but no product source code. Public visibility does not make the product open source or grant a source-code license.

## Current product scope

Local English lookup and on-demand AI explanation are the accepted product's two core capabilities. It:

- is a macOS menu bar app with no Dock icon;
- supports English-to-Simplified-Chinese lookup only, with no Chinese-to-English mode, automatic direction, or sentence translation;
- uses a bundled read-only ECDICT database with 390,573 valid English–Chinese entries and 58,369 inflection mappings;
- classifies code, paths, variables, abbreviations, specialist terms, and proper names, while retaining an available dictionary definition;
- offers “AI help for this context” on classified targets, invoked only after the user clicks it;
- falls back to on-device OCR of a small area near the pointer when accessible text cannot be read;
- processes screenshot pixels in memory on the Mac without saving or uploading them.

It does not include a reverse dictionary, Apple's Translation framework, sentence/context translation, or a “meaning in sentence” section. Pricing, service levels, open-source plans, and launch dates are not promised here.

## Interaction

1. Put the pointer inside the exact character bounds of an English word or continuous technical target.
2. Hold the selected trigger key. Left Option is the default; Right Option is the only alternative.
3. The pointer coordinate is frozen at key-down, with one recognition request per key press.
4. A card appears only after recognition and lookup succeed, so invalid targets do not flash a placeholder card.
5. The card remains while Option is held. If the pointer has entered the card, the key may be released and the card closes after the pointer leaves; otherwise releasing the key closes it immediately.

Chinese text, other scripts, punctuation, whitespace, and gaps between words do not produce a card.

## Requirements

- macOS 15 or later;
- supported Mac architectures will be published after the signed and notarized release candidate passes device testing.

Xcode 26 is a private build-tool requirement, not an installation requirement.

## Download status

There is no public download and no formal GitHub Release yet. Do not install copies from file-sharing sites, chat attachments, search ads, or third-party mirrors.

Product positioning, accepted behavior, permission usage, local processing, help, and feedback channels may be published now. A download will be added only after all of the following are complete:

- valid Developer ID Application signing;
- successful Apple notarization and ticket stapling;
- installation, permission, core-interaction, and upgrade testing on every advertised macOS and Mac architecture;
- production AI gateway authentication, rate limiting, abuse prevention, security, and reliability review;
- an approved privacy policy matching the installer's permissions, network requests, third-party processing, and logging behavior;
- final filename, version, size, SHA-256 checksum, and verification instructions.

A website is not required for the first safe download: GitHub Releases can be the initial verified channel once these conditions are met. The planned website address is `pointrans.cuostudio.com`, but it has not been verified as accessible and is not currently a download channel. If a website or CDN is added later, its same-version installer must be byte-for-byte identical to the GitHub Release asset.

## Permissions and data

The accepted build requires both permissions below. Without either one, the app does not enter its ready state:

| Permission | Purpose | When used |
| --- | --- | --- |
| Accessibility | Read the exact accessible characters and bounds under the pointer | Tried first after an explicit trigger |
| Screen & System Audio Recording | Capture a small area near the pointer when accessible text is unavailable | Used only when the current request needs OCR fallback |

Screen Recording is required by the current build, but the app does not continuously record the screen. A screenshot is created only after an explicit trigger when accessible-text extraction fails; its pixels are processed in memory, not saved, and not uploaded.

Normal dictionary lookup is entirely local. AI explanation is requested only after the user clicks the AI button. The request contains the target and up to 400 characters from the same source line; it does not contain a screenshot. The current design has no separate AI privacy switch, so avoiding that button prevents an AI request.

The production AI service is not ready for public distribution. The final privacy policy must disclose the actual provider, processing regions, retention, model-training treatment, and other production behavior before a download is published.

Do not post private text, personal information, access tokens, internal paths, unredacted screenshots, or complete logs in public issues or discussions. See [Permissions and data](./docs/permissions-and-data.md), [Support](./SUPPORT.md), and [Security](./SECURITY.md).

## Repository scope

This is a product repository, not a source repository. Product source code, build systems, signing material, and production configuration remain in a controlled private environment. Source contributions cannot be accepted here, while documentation corrections and reproducible reports are welcome.

Copyright © 2026 CuoStudio. All rights reserved.
