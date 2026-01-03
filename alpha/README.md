
# BilKo's PC: Universal Pokémon Save Editor

![Version](https://img.shields.io/badge/version-1.1.0_Alpha-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![PWA](https://img.shields.io/badge/PWA-Offline%20Ready-purple.svg)

**BilKo's PC** is a state-of-the-art, browser-based save file editor for retro Pokémon games. Built with modern web technologies, it runs entirely on your device, ensuring your save files never leave your computer.

---

## 🌐 Live Versions

| Version | Status | Link |
| :--- | :--- | :--- |
| **Stable Demo** | 🟢 Public Release | [Launch App](https://bilkochal.github.io/BilKos-PC/) |
| **Alpha / Dev** | 🟡 Latest Features | [Launch Alpha](https://bilkochal.github.io/BilKos-PC/alpha/) |

---

## 🎮 Game Support Status

| Generation | Versions | Status | Notes |
| :--- | :--- | :--- | :--- |
| **Gen 1** | Red, Blue, Yellow | ✅ **Full Support** | Complete editing & management. |
| **Gen 2** | Gold, Silver, Crystal | ⚠️ **Beta** | Items, Party, & Box management operational. |
| **Gen 3** | R, S, E, FR, LG | 🚧 **Broken / Experimental** | Basic Parser Only. Writing is unstable. |
| **Gen 4** | D, P, Pt, HG, SS | 🚧 **Broken / Experimental** | Basic Parser Only. Encrypted blocks may fail. |
| **Gen 5** | B, W, B2, W2 | 🚧 **Broken / Experimental** | Basic Parser Only. Checksum logic incomplete. |

---

## 🌟 Key Features

### 🛡️ Secure & Private
- **Local Processing**: Uses HTML5 FileReader. No data is sent to any server.
- **Offline Capable (PWA)**: Installable as a native app on iOS/Android/Desktop. Works without internet.

### 📦 Storage & Management
- **Visual PC Storage**: View all boxes with sprites.
- **Drag & Drop**: Seamlessly move Pokémon between Party and Boxes.
- **Batch Operations**: Select multiple Pokémon (Ctrl/Shift+Click) to move or release them at once.
- **BilKo Bank**: Create external storage files (`.bkbank`) to store up to 20 extra boxes outside your save file.
- **Sorting**: Powerful algorithms to sort boxes by Dex ID, Level, Type, or organize a **Living Dex** instantly.

### 🛠️ Editor Tools
- **Trainer Card**: Edit Name, ID, Money, Coins, Badges, and Playtime.
- **Pokémon Editor**:
    - Edit Nickname, Level, and Experience.
    - **Stats**: Edit IVs (DVs) and EVs (Stat Exp).
    - **Moves**: Teach any move from the game generation.
    - **Gen 2 Features**: Edit Held Items, Shiny status, and Unown Forms.
- **Inventory**: Manage Bag, PC Items, Key Items, and TMs/HMs.
- **Pokedex**: Toggle "Seen" and "Caught" flags with a visual interface.

### 🔄 Trade Center
- **Cross-Save Trading**: Load a second `.sav` file to trade Pokémon between files.
- **Import/Export**:
    - Export individual Pokémon as `.pk1` or `.pk2` files.
    - Batch import Pokémon files into your save.
- **Event Database**: Direct injection of historical Event Pokémon (Mew, Celebi, Surfing Pikachu, etc.) sourced from Project Pokémon.

### 📚 Guides & Extras
- **Battle Guide**: View Gym Leader and Elite Four teams tailored to your specific game version.
- **Hall of Fame**: View your past victories in a cinematic interface.
- **Asset Downloader**: Pre-download all sprites and audio cries for a complete offline experience.

---

## 🤝 Credits & Acknowledgements

This project was built standing on the shoulders of giants. Huge thanks to the following projects and communities:

### **PKHeX**
[https://github.com/kwsch/PKHeX](https://github.com/kwsch/PKHeX)
> For providing the gold standard in save editing logic. The save parsing structure of this project learned immensely from PKHeX's source code.

### **PokeAPI**
[https://pokeapi.co/](https://pokeapi.co/)
> For providing an extensive database of Pokémon data and base assets.

### **Pokémon Showdown**
[https://play.pokemonshowdown.com/](https://play.pokemonshowdown.com/)
> For the high-quality sprite assets used throughout the Trainer Cards and UI.

### **Project Pokémon**
[https://projectpokemon.org/](https://projectpokemon.org/)
> For archiving and preserving Event Pokémon data, which powers the "Event Database" feature.

### **PKVault**
[https://github.com/Chnapy/PKVault](https://github.com/Chnapy/PKVault)
> For inspiring several UI/UX concepts and features.

---

<p align="center">
  <sub>Created by BilKo(Ch)al • Open Source • Free to Use</sub>
</p>
