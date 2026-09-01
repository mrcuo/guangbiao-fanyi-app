# Pointrans

Hold a key and hover over text to see Chinese or English definitions and translations near the pointer.

> **Preparing for release**
>
> This is the official product hub for Pointrans. It is intended for product documentation, release notes, support, and security reporting. No public download is available yet.
>
> Product source code is not published in this repository. Public visibility does not make the product open source or grant a source-code license.

## What it does

Pointrans is a macOS menu bar app designed to reduce copying, pasting, and switching windows while reading.

The current implementation:

- uses Left Option plus pointer hover as the default trigger;
- supports Chinese–English word lookup and contextual translation;
- prefers bundled dictionaries for word definitions;
- uses macOS system translation for sentences and text fragments;
- can use on-device OCR for a small region near the pointer when text cannot be read directly;
- does not require users to provide a translation-service API key.

Only implemented and verified capabilities are documented here. Unreleased AI features, pricing, service levels, and launch dates are not promised.

## Requirements

- macOS 15 or later;
- supported Mac architectures will be published after the signed and notarized release candidate passes device testing.

## Download

There is no public download yet.

A release will not be published until it is Developer ID signed, Apple-notarized and stapled, tested on supported systems, and covered by an approved privacy policy. The production AI gateway must also pass authentication, rate-limit, abuse-prevention, security, and reliability review; when network-based AI is disabled, its entry points must remain closed and must not be advertised as available.

Official releases will include a version number, file size, SHA-256 checksum, release notes, and verification guidance.

## Permissions and privacy

Pointrans uses Accessibility permission to read accessible text near the pointer after an explicit trigger. When that is not possible, Screen Recording permission enables on-device OCR of a small nearby region.

In the current implementation, OCR images are processed in memory on the Mac and are not saved or uploaded. These statements will be rechecked against the final release build and the approved privacy policy before distribution.

Do not post private text, personal information, access tokens, unredacted screenshots, or complete logs in public issues or discussions.

See [Permissions and data](./docs/permissions-and-data.md), [Support](./SUPPORT.md), and [Security](./SECURITY.md).

## Repository scope

This is a product repository, not a source repository. Product source code, build systems, signing material, and production configuration remain in a controlled private environment. Product source contributions cannot be accepted here, while documentation corrections and reproducible reports are welcome.

Copyright © 2026 CuoStudio. All rights reserved.
