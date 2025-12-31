# BilKo's PC: Gen 1 Save Editor

![Version](https://img.shields.io/badge/version-1.15.1-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Gen 1 Compatible](https://img.shields.io/badge/Game-Pokemon%20Red%2FBlue%2FYellow-red.svg)

**BilKo's PC** is a state-of-the-art web-based save editor for the original Generation 1 Pokemon games (Red, Blue, and Yellow). Built with modern web technologies, it runs entirely in your browser, ensuring your save files never leave your device.

Curated by **BilKoChal** with advanced AI support, this project aims to provide the most intuitive and powerful editing experience for retro enthusiasts.

---

## 🌟 Key Features

### 🛡️ Secure & Client-Side
- **Local Processing**: Uses the HTML5 FileReader API to parse files directly on your machine.
- **Privacy First**: No save data is ever uploaded to a server.

### 🎮 Comprehensive Save Management
- **Universal Support**: Fully compatible with `.sav` and `.srm` files (32KB standard size).
- **Intelligent Version Detection**: Automatically identifies Red, Blue, or Yellow versions using heuristic analysis of the Pokedex and specialized memory flags.
- **Binary Export**: Saves changes back to a binary format that works on emulators and flash carts.

### 🛠️ Advanced Editing Tools
- **Trainer Editor**: Modify your name, money, and view badges/playtime.
- **Party Management**: View your active team with detailed stats.
- **PC Storage**: Browse all 12 PC Boxes with visual sprites.
- **Inventory**: View items in your Bag and PC storage.
- **Pokedex Editor**: Manually toggle "Seen" and "Caught" flags for all 151 Pokemon.
- **Trade Evolutions**: Evolve Kadabra, Haunter, Machoke, and Graveler instantly with a single button click (No trading cable required!).

### 📊 Deep Statistics & Visualization
- **IVs & EVs**: View hidden Determination Values (DVs/IVs) and Stat Experience (EVs) for every Pokemon.
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
3. Edit your data (money, pokedex, evolutions, etc.).
4. Click **Save Changes** in the top right to download your modified save file.

---

## 🧩 Technical Architecture

This project follows a strict **modular architecture** to support future generations and ensure maintainability.

```
/src
├── components/       # Reusable UI components (TrainerCard, PokedexViewer, etc.)
├── core/             # Business Logic Layer
│   ├── gen1/         # Gen 1 specific logic (Parser, Writer, Offsets)
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

- **Curator & Lead**: BilKoChal
- **Development Support**: Artificial Intelligence Assistant
- **Assets**: Pokemon sprites and data provided by PokeAPI.

---

<p align="center">
  <sub>Created by BilKo with the help of AI • &copy; 2024</sub>
</p>
