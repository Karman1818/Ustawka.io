# Ustawka.io 🥊

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev/)
[![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/)
[![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

**Ustawka.io** is a satirical mobile application designed for football culture enthusiasts and supporters who appreciate "honorable confrontations in scenic natural surroundings". Forget boring messaging apps – organize turf clashes with class, analyze real-time tactical weather forecasts, and defend your club colors.

> ⚠️ **Disclaimer:** *This application is purely satirical and created for entertainment/humor purposes. It does not promote, endorse, or encourage real-world violence.*

---

## ✨ Key Features

- 🛡️ **Authentication & Club Colors**: User registration with mandatory allegiance selection powered by **Supabase Auth**. Integrated profile tracking warrior identity and stats.
- 🌲 **Dynamic Arena Generator (Overpass API)**: Automatic discovery of authentic clash locations (forests, clearings, abandoned sites) across Poland using real-time OpenStreetMap data.
- 🌤️ **Tactical Weather Reports (Open-Meteo)**: Live weather telemetry for each arena, complete with satirical condition assessments (shoe grip index, mud coefficient, and visibility metrics).
- ⚔️ **Clash Marketplace & Realtime Balances**: Browse upcoming matchups nearby, join clashes with a single tap, and observe live balance of forces between rival club factions in real time.
- 📊 **Witness Voting & Global Leaderboards**: Post-clash community voting ("Witness System") feeding into a live global club leaderboard powered by PostgreSQL SQL Views.
- 🩹 **L4 Medical Leave (Injury System)**: Suffered injuries in combat? File for L4 sick leave on your profile to initiate a 24-hour convalescence cooldown before joining future fights.
- 🌐 **Multilingual Support (i18n)**: Fully internationalized with seamless language switching between **Polish** and **English**.

---

## 🎨 Design System: BRUTALISM

Built with a bold, raw **Brutalist UI** identity:
- **High-contrast Palette**: Deep blacks, blood reds, and tactical neon yellows.
- **Heavy Borders & Shadows**: Crisp, sharp-edged UI components with prominent outlines.
- **Aggressive Typography**: Oversized bold headers emphasizing the application's unique atmosphere.

---

## 🛠️ Tech Stack

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Frontend** | [Flutter](https://flutter.dev) (Dart) | Cross-platform mobile & web client |
| **Backend** | [Supabase](https://supabase.com) | Auth, PostgreSQL Database, Realtime Subscriptions & RPCs |
| **Maps & Geo** | [Overpass API](https://overpass-api.de/) | OpenStreetMap query engine for arena locations |
| **Weather** | [Open-Meteo API](https://open-meteo.com/) | Real-time weather telemetry data |
| **State & Navigation** | Animated Bottom Bar | Custom navigation system |
| **Localization** | `flutter_localizations` | `arb`-based i18n support (EN / PL) |

---

## 📁 Repository Structure

```
Ustawka.io/
├── README.md               # Main project documentation
└── nav_bars/               # Flutter mobile & web application root
    ├── lib/
    │   ├── core/           # Theme definitions & Brutalist UI styles
    │   ├── l10n/           # Localization files (app_en.arb, app_pl.arb)
    │   ├── models/         # Data models
    │   ├── screens/        # UI screens (Auth, Market, Leaderboard, Profile, Settings)
    │   ├── services/       # Supabase, Overpass & Weather services
    │   └── widgets/        # Reusable UI widgets
    ├── supabase/
    │   └── schema.sql      # Database schema, RLS policies & SQL functions
    ├── .env                # Environment configuration (Supabase credentials)
    └── pubspec.yaml        # Flutter dependencies & assets
```

---

## 🚀 Getting Started

### Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install) (v3.5.0 or higher)
- A [Supabase](https://supabase.com) account (for backend services)

### Installation & Local Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Karman1818/Ustawko.io.git
   cd Ustawka.io/nav_bars
   ```

2. **Install Flutter dependencies:**
   ```bash
   flutter pub get
   ```

3. **Configure Environment Variables:**
   Create a `.env` file in the `nav_bars/` directory:
   ```env
   SUPABASE_URL=https://your-project.supabase.co
   SUPABASE_PUBLISHABLE_KEY=your-supabase-anon-key
   ```

4. **Set up the Database:**
   - Execute the SQL script found in [`nav_bars/supabase/schema.sql`](nav_bars/supabase/schema.sql) inside your Supabase SQL Editor to set up tables, Row Level Security (RLS), and functions.

5. **Run the Application:**
   ```bash
   # Run on Chrome
   flutter run -d chrome

   # Run as Desktop App on Windows
   flutter run -d windows
   ```

---

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

---

<p align="center">
  <i>Created with humor and satire. Respect your opponents and stay safe! 🥊</i>
</p>
