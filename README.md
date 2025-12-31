# BilKo's PC: Gen 1 Save Editor

![Version](https://img.shields.io/badge/version-1.50.3-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Gen 1 Compatible](https://img.shields.io/badge/Game-Pokemon%20Red%2FBlue%2FYellow-red.svg)
![PWA Ready](https://img.shields.io/badge/PWA-Offline%20Ready-purple.svg)

**BilKo's PC** is a state-of-the-art web-based save editor for the original Generation 1 Pokemon games (Red, Blue, and Yellow). Built with modern web technologies, it runs entirely in your browser, ensuring your save files never leave your device.

Curated by **BilKo(Ch)al** with advanced AI support, this project aims to provide the most intuitive and powerful editing experience for retro enthusiasts.

---

## 🌟 Key Features

### 🛡️ Secure & Client-Side
- **Local Processing**: Uses the HTML5 FileReader API to parse files directly on your machine.
- **Privacy First**: No save data is ever uploaded to a server.
- **Offline Capable**: **UPDATED!** Install the app as a PWA. Go to **Settings > Offline Data** to pre-download all 151 Pokemon sprites (Original, Modern, and Artwork) and cries for a completely offline experience.

### 🎮 Comprehensive Save Management
- **Universal Support**: Fully compatible with `.sav` and `.srm` files (32KB standard size).
- **Intelligent Version Detection**: Automatically identifies Red, Blue, or Yellow versions using heuristic analysis of the Pokedex and specialized memory flags.
- **Binary Export**: Saves changes back to a binary format that works on emulators and flash carts.

### 🔄 Trade Center (Refactored)
- **Modular Architecture**: The Trade Center features a highly modular codebase (`components/trade/`) with separate panels for Save Import, Bank, and Pk1 Files, ready for future Gen 2/3 expansions.
- **Multi-Source Trading**: 
    1. **File Trade**: Load a second `.sav` file to trade between your own saves. **NEW:** Export the modified secondary save file directly!
    2. **BilKo Bank**: Create, Import, and Export personal Pokemon Banks (`.bkbank` format). Store up to 20 boxes of Pokemon externally!
    3. **Import .pk1 (New!)**: Batch upload multiple `.pk1` files into a staging area. Transfer them one-way into your save file.
    4. **Events & Specials (Updated!)**: Access official distributions and rare event Pokemon. **NEW:** Sort by ID/Name, colored tags, and "Direct Injection" button.
- **Direct Injection**: Click "Add to Box" on an Event Pokemon to instantly add it to your current PC Box without needing to trade.
- **Batch Import**: Select multiple Pokemon from a source and move them all at once to your game.
- **Staging Area**: When importing .pk1 files, the grid hides empty slots and provides a dedicated "Import" button to append more files easily.
- **Smart Pokedex**: Automatically updates your Pokedex (Seen & Caught) when you import a new species!
- **Mobile Friendly**: Tabbed interface designed specifically for trading on mobile devices.

### 🛠️ Advanced Editing Tools
- **Smart Move Mode**: 
    - **Power Selection**: Use **Ctrl+Click** to toggle selections and **Shift+Click** to select ranges of Pokemon.
    - **Select All**: Quickly select all Pokemon in a Box with one click.
    - **Smart Swap**: Select multiple Pokemon and click on an occupied slot to sequentially swap them.
    - **Release**: **NEW!** Delete single or multiple Pokemon instantly with a confirmation prompt. Works in both Main Editor and Trade Center.
- **Toast Notifications**: Modern, non-intrusive alerts for feedback and errors.
- **Settings & Customization**: Switch between Original Game Boy sprites, Modern pixel art, or Official Artwork via the settings menu.
- **Trainer Editor**: Modify your name, money (capped at 999,999), and view badges/playtime.
- **Level Editor**: Edit your Pokemon's level (1-100) with automatic stat recalculation.
- **Move Editor**: Change your Pokemon's moveset by selecting from any Gen 1 move.
- **Party Management**: View your active team with detailed stats. Move Pokemon between Party and Boxes. **NEW:** Displays Species Name under Nickname for clarity.
- **PC Storage**: Browse all 12 PC Boxes with visual sprites. Fully supports moving and swapping Pokemon with improved precision and visual feedback.
- **Inventory & Item Editor**: Manage Bag and PC items. Select any item from a searchable list with sorting (Name/ID) and adjust quantities.
- **Pokedex Editor**: Manually toggle "Seen" and "Caught" flags for all 151 Pokemon. Hear Pokemon cries with the new audio feature!
- **Location Guide**: View detailed "How to Obtain" information for every Pokemon, customized to your specific game version (Red, Blue, or Yellow).
- **Authentic Lore**: Displays version-accurate Pokedex entries. Yellow version saves see unique descriptions compared to Red/Blue.
- **Trade Evolutions**: Evolve Kadabra, Haunter, Machoke, and Graveler instantly with a single button click (No trading cable required!).
- **Evolution Animation**: Watch a retro-style animation when evolving your Pokemon!
- **PK1 Export**: Export individual Pokemon as `.pk1` files directly from the Pokemon details screen. Supports standard **69-byte format** for full PKHeX compatibility.

### 📊 Deep Statistics & Visualization
- **IVs & EVs**: View hidden Determination Values (DVs/IVs) and Stat Experience (EVs) for every Pokemon.
- **OT Info**: View Original Trainer Name and ID for any Pokemon to verify legitimacy.
- **Interactive Charts**: Toggle between Radar and Bar charts to visualize stat distribution.
- **Modern UI**: A responsive interface built with Tailwind CSS, featuring version-specific themes (Red/Blue/Yellow).

---

## 🚀 Getting Started

### Prerequisites
- A web browser (Chrome, Firefox, Edge, Safari).
- A valid save file (`.sav`) from Pokemon Red, Blue, or Yellow.

### Usage
1. Open the application.
2. Drag and drop your `.sav` file into the upload zone.
3. Edit your data (money, pokedex, evolutions, items, etc.).
4. Click **Save Changes** in the top right to download your modified save file.

### Installation (PWA)
1. Open the site in Chrome or Safari.
2. Click "Install" in the address bar (Chrome) or "Add to Home Screen" (Safari/Mobile).
3. Open **Settings (Gear Icon)**.
4. Click **"Download Assets"** to cache all images/audio for offline use.

---

## 🧩 Technical Architecture

This project follows a strict **modular architecture** to support future generations and ensure maintainability.

```
/src
├── components/       # Reusable UI components (TrainerCard, PokedexViewer, TradeCenter, Toast, etc.)
│   ├── trade/        # Trade Center
│   │   ├── headers/  # Dock Headers (File, Bank, Pkm)
│   │   ├── panels/   # Selection Panels (File, Bank, Pkm, Event)
│   │   ├── TradeDock.tsx
│   │   ├── TradeSourceSelector.tsx
│   │   ├── TradeActionControls.tsx
│   │   └── TradeHeader.tsx
├── core/             # Business Logic Layer
│   ├── parser.ts     # Main Parser Factory (Dispatcher)
│   ├── version.ts    # Centralized Version Management
│   ├── bank.ts       # Bank Logic (Create, Import, Export)
│   ├── cache_manager.ts # Offline Asset Pre-fetcher logic
│   ├── settings.tsx  # Global Settings Context
│   ├── gen1/         # Gen 1 specific logic (Parser, Writer, Offsets, Constants)
│   │   ├── pk1.ts    # .pk1 File Parser/Writer
│   │   ├── utils.ts  # .pk1 Filename Generation & Hashing
│   ├── move_manager.ts # Logic for moving Pokemon within a save (Single & Batch)
│   ├── trade_manager.ts # Logic for moving Pokemon BETWEEN saves (Single & Batch)
│   ├── toast.tsx     # Toast Notification System
│   ├── theme.ts      # Dynamic theming engine
│   └── types.ts      # TypeScript interfaces
├── data/             # Static Data (Base Stats, Text Strings, Pokedex Entries, Locations)
│   ├── events.ts     # Event Distribution Data
├── pages/            # Page Controllers
└── App.tsx           # Main Entry Point
```

**Tech Stack:**
- **Frontend**: React 18, TypeScript, Vite
- **Styling**: Tailwind CSS
- **PWA**: Vite Plugin PWA, Workbox
- **Visualization**: Recharts
- **Icons**: Lucide React

---

## 🤝 Credits

- **Curator & Lead**: BilKo(Ch)al
- **Development Support**: Artificial Intelligence Assistant
- **Assets**: Pokemon sprites and data provided by PokeAPI.

---

<p align="center">
  <sub>Created by BilKo(Ch)al with the help of AI • &copy; 2024</sub>
</p>