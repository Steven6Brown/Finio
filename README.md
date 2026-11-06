<div align="center">
  <img src="branding/finio-icon.png" alt="Finio logo" width="140">
  <h1>Finio</h1>

  <p><strong>Privacy-first budgeting from your bank notifications.</strong></p>

  <img src="https://img.shields.io/badge/status-In%20development-C2410C?style=flat-square" alt="status"> <img src="https://img.shields.io/badge/platform-iOS%2017%2B-C2410C?style=flat-square" alt="platform"> <img src="https://img.shields.io/badge/license-proprietary-555555?style=flat-square" alt="license"> <img src="https://img.shields.io/badge/by-Aquila%20Digital%20LLC-14213D?style=flat-square" alt="Aquila Digital LLC">
</div>

> **Showcase repository.** The source code for Finio is not published. This page presents what the product is and how it works.

## Overview

A budget tracker that parses bank charge notifications on-device: no bank login, no subscription, no data leaving the phone. Copy a notification (or tell Siri) and Finio files it in the right category.

## How it works

```mermaid
flowchart LR
  A["Bank sends a charge notification"] --> B["Long-press, copy the text"] --> C["Finio detects the clipboard and parses merchant, amount and category"] --> D["Tap 'Add to Budget' (or say 'Hey Siri, add to Finio')"]
```

## Features

- Parser for 20+ banks and auto-categorization of 500+ merchants
- Siri / App Intents hands-free logging and a Share Extension
- Monthly category budgets, bills tracker with due reminders, savings goals
- Home-screen widgets (small and medium)
- Face ID local account, dark and light mode, CSV export
- 100% offline using App Groups

## Tech stack

| Layer | Choice |
|---|---|
| Language / UI | Swift, SwiftUI, iOS 17+ |
| Targets | App, Widget extension, Share extension |
| Integration | App Intents / Siri, Face ID, App Groups |
| Tests | NotificationParserTests + UI tests |

## Privacy & security

No bank login, no analytics, no server. All data stays on-device in an App Group.

## Brand

| | Name | Hex | Role |
|---|---|---|---|
| <img src="https://placehold.co/44x22/C2410C/C2410C.png" alt="#C2410C" /> | Burnt Orange | `#C2410C` | Accent (light) |
| <img src="https://placehold.co/44x22/F97316/F97316.png" alt="#F97316" /> | Orange | `#F97316` | Accent (dark) |
| <img src="https://placehold.co/44x22/0F172A/0F172A.png" alt="#0F172A" /> | Slate | `#0F172A` | Text / dark |
| <img src="https://placehold.co/44x22/EF4444/EF4444.png" alt="#EF4444" /> | Alert Red | `#EF4444` | Danger |

**Mark.** Orange accent on a slate base; clean, finance-calm.

**Voice.** Plain, reassuring, privacy-first.

## Roadmap

- Pre-release polish
- More bank formats
- App Store launch

## License

Proprietary. Shared publicly for portfolio and demonstration purposes only. See [LICENSE](LICENSE).

---

<div align="center">

Built by [Aquila Digital LLC](https://github.com/Steven6Brown) · *Per Aspera Ad Astra*

</div>
