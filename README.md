# BilKo's PC: Gen 1 Save Editor

![Version](https://img.shields.io/badge/version-1.34.1-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Gen 1 Compatible](https://img.shields.io/badge/Game-Pokemon%20Red%2FBlue%2FYellow-red.svg)

**BilKo's PC** is a state-of-the-art web-based save editor for the original Generation 1 Pokemon games (Red, Blue, and Yellow). Built with modern web technologies, it runs entirely in your browser, ensuring your save files never leave your device.

Curated by **BilKo(Ch)al** with advanced AI support, this project aims to provide the most intuitive and powerful editing experience for retro enthusiasts.

---

## 🌟 Key Features

### 🛡️ Secure & Client-Side
- **Local Processing**: Uses the HTML5 FileReader API to parse files directly on your machine.
- **Privacy First**: No save data is ever uploaded to a server.

### 🎮 Comprehensive Save Management
- **Universal Support**: Fully compatible with `.sav` and `.srm` files (32KB standard size).
- **Intelligent Version Detection**: Automatically identifies Red, Blue, or Yellow versions using heuristic analysis of the Pokedex and specialized memory flags.
- **Binary Export**: Saves changes back to a binary format that works on emulators and flash carts.

### 🔄 Trade Center
- **Import Pokemon**: Load a second `.sav` file alongside your main one.
- **Cross-Save Trading**: Drag and drop (or select and click) to move Pokemon between two different save files.
- **Batch Import**: Select multiple Pokemon from an external save and move them all at once to your game.
- **Mobile Friendly**: New tabbed interface designed specifically for trading on mobile devices.
- **Backup Support**: Safely export Pokemon to another file before starting a new game.

### 🛠️ Advanced Editing Tools
- **Smart Move Mode**: 
    - **Power Selection**: Use **Ctrl+Click** to toggle selections and **Shift+Click** to select ranges of Pokemon.
    - **Select All**: Quickly select all Pokemon in a Box with one click.
    - **Smart Swap**: Select multiple Pokemon and click on an occupied slot to sequentially swap them.
    - **Capacity Checks**: Prevents you from moving more Pokemon than a Box or Party can hold.
- **Toast Notifications**: Modern, non-intrusive alerts for feedback and errors.
- **Trainer Editor**: Modify your name, money (capped at 999,999), and view badges/playtime.
- **Level Editor**: Edit your Pokemon's level (1-100) with automatic stat recalculation.
- **Move Editor**: Change your Pokemon's moveset by selecting from any Gen 1 move.
- **Party Management**: View your active team with detailed stats. Move Pokemon between Party and Boxes.
- **PC Storage**: Browse all 12 PC Boxes with visual sprites. Fully supports moving and swapping Pokemon with improved precision and visual feedback.
- **Inventory & Item Editor**: Manage Bag and PC items. Select any item from a searchable list with sorting (Name/ID) and adjust quantities.
- **Pokedex Editor**: Manually toggle "Seen" and "Caught" flags for all 151 Pokemon. Hear Pokemon cries with the new audio feature!
- **Trade Evolutions**: Evolve Kadabra, Haunter, Machoke, and Graveler instantly with a single button click (No trading cable required!).
- **Evolution Animation**: Watch a retro-style animation when evolving your Pokemon!

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

---

## 🧩 Technical Architecture

This project follows a strict **modular architecture** to support future generations and ensure maintainability.

```
/src
├── components/       # Reusable UI components (TrainerCard, PokedexViewer, TradeCenter, Toast, etc.)
├── core/             # Business Logic Layer
│   ├── parser.ts     # Main Parser Factory (Dispatcher)
│   ├── version.ts    # Centralized Version Management
│   ├── gen1/         # Gen 1 specific logic (Parser, Writer, Offsets, Constants)
│   ├── move_manager.ts # Logic for moving Pokemon within a save (Single & Batch)
│   ├── trade_manager.ts # Logic for moving Pokemon BETWEEN saves (Single & Batch)
│   ├── toast.tsx     # Toast Notification System
│   ├── theme.ts      # Dynamic theming engine
│   └── types.ts      # TypeScript interfaces
├── data/             # Static Data (Base Stats, Text Strings)
├── pages/            # Page Controllers
└── App.tsx           # Main Entry Point
```

**Tech Stack:**
- **Frontend**: React 18, TypeScript, Vite
- **Styling**: Tailwind CSS
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