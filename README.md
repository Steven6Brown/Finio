# finio 💸

A privacy-first iOS budget tracker that automatically parses your bank charge notifications — no bank login, no subscriptions, no data ever leaving your device.

![Swift](https://img.shields.io/badge/Swift-5.9-F97316?style=flat&logo=swift&logoColor=white)
![iOS](https://img.shields.io/badge/iOS-17+-0F172A?style=flat&logo=apple&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-22C55E?style=flat)

---

## What is Finio?

Most budgeting apps require you to connect your bank account or manually type every purchase. Finio does neither.

When you get a charge notification from your bank, you long-press it, copy the text, and open Finio — it detects the notification automatically, parses the merchant name, amount, and category instantly, and has it ready to add to your budget in one tap. You can also say **"Hey Siri, add to Finio"** and speak your charge completely hands-free.

---

## Features

- **Smart notification parsing** — Supports 20+ banks including Discover, Chase, Amex, Capital One, Wells Fargo, and more
- **Siri integration** — Say "Hey Siri, add to Finio" for completely hands-free logging
- **Auto-categorization** — Automatically categorizes 500+ merchants across Food & Dining, Groceries, Transport, Shopping, Subscriptions, Health, Travel, and Bills
- **Monthly budget tracking** — Set limits per category and track spending with visual breakdowns
- **Bills tracker** — Log recurring bills with due date reminders; marking a bill paid automatically creates a transaction
- **Savings goals** — Set goals with emoji icons and track progress
- **Home screen widget** — Small and medium widgets showing real-time budget status
- **Face ID authentication** — Secure local account with biometric login
- **Dark & light mode** — Full support for both appearance modes
- **100% offline** — All data stored locally using App Groups and UserDefaults
- **CSV export** — Export your transaction history at any time

---

## How It Works

```
Bank sends charge notification
        ↓
Long-press notification → Proofread → Copy
        ↓
Open Finio → Add tab
        ↓
Clipboard auto-detected and parsed instantly
        ↓
Tap "Add to Budget" — done
```

Or hands-free:
```
"Hey Siri, add to Finio"
        ↓
Speak your charge
        ↓
Finio opens with transaction pre-filled
        ↓
Tap "Add to Budget" — done
```

---

## Tech Stack

| Technology | Usage |
|---|---|
| **SwiftUI** | Entire UI layer |
| **WidgetKit** | Home screen widgets |
| **AppIntents** | Siri integration |
| **UserNotifications** | Bill reminders & monthly summaries |
| **LocalAuthentication** | Face ID |
| **Security (Keychain)** | Secure password storage |
| **App Groups** | Shared data between app and widget |
| **UserDefaults** | Local data persistence |

---

## Project Structure

```
Finio/
├── Models/
│   └── Models.swift              # Transaction, SpendingCategory, Bill, SavingsGoal
├── ViewModels/
│   └── BudgetViewModel.swift     # Core app state and business logic
├── Views/
│   ├── DashboardView.swift       # Main dashboard with charts and overview
│   ├── AddNotificationView.swift # Notification parsing and transaction entry
│   ├── HistoryAndBudgetsView.swift # Transaction history and budget management
│   ├── AccountView.swift         # Bills, goals, income, settings
│   ├── SettingsView.swift        # App settings and preferences
│   ├── OnboardingView.swift      # Onboarding flow, auth, sign in
│   ├── ContentView.swift         # Root tab navigation
│   └── DesignSystem.swift        # Shared UI components and design tokens
├── Services/
│   ├── NotificationParser.swift  # Core parsing engine
│   ├── NotificationManager.swift # Push notification handling
│   └── FinioIntents.swift        # Siri / AppIntents integration
└── FinioWidget/
    └── FinioWidget.swift         # Home screen widget
```

---

## Getting Started

### Requirements
- Xcode 15+
- iOS 17+
- Apple Developer account (for device testing)

### Setup

1. Clone the repo
```bash
git clone https://github.com/Steven6Brown/finio-ios.git
cd finio-ios
```

2. Open in Xcode
```bash
open Finio.xcodeproj
```

3. Set your development team in **Signing & Capabilities** for both the `Finio` and `FinioWidgetExtension` targets

4. Make sure both targets have the App Group `group.com.stevenbrown.Finio` in **Signing & Capabilities**

5. Build and run on your device

> **Note:** The debug reset block in `FinioApp.swift` wipes all data on every launch during development. Remove the `#if DEBUG` block before releasing.

---

## Supported Banks

Discover · Chase · Amex · Capital One · Bank of America · Wells Fargo · Citi · US Bank · PNC · TD Bank · Navy Federal · Apple Card · PayPal · Venmo · Cash App · Zelle · and more

---

## Privacy

Finio is built with privacy as a core principle:

- ✅ No bank credentials ever required
- ✅ No internet connection needed
- ✅ No analytics or tracking
- ✅ No data ever leaves your device
- ✅ All data stored locally with App Groups
- ✅ Password stored securely in iOS Keychain

---

## License

Copyright © 2026 Aquila Digital. All rights reserved.

This code is proprietary and shared publicly for portfolio and demonstration purposes only. No permission is granted to use, copy, modify, distribute, or create derivative works from this software without explicit written consent from Aquila Digital.

Interested in licensing or acquiring rights to this project? Reach out via [Aquila Digital](https://github.com/Steven6Brown).

---

## Author

**Stevie Brown**
[Portfolio](https://www.stevenrbrown.org) · [GitHub](https://github.com/Steven6Brown)
