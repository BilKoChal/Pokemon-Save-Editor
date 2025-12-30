# Pokemon Save Editor

A web-based tool for editing Pokemon save files, specifically optimized for Generation 1 (Red/Blue/Yellow) with a modular design to support future generations.

## Features
- **Gen 1 Support**: Fully parses `.sav` and `.srm` files (32KB).
- **Trainer Editing**: Edit Trainer Name and Money directly from the dashboard and **Save Changes** back to a `.sav` file.
- **Improved Version Detection**: Uses Heuristics (Pokedex exclusives) to distinguish between Red and Blue versions.
- **Red/Blue/Yellow Support**: Automatically detects Yellow version. For Red/Blue (which are binary identical), users can toggle the theme by clicking the version badge in the header.
- **Full PC Storage**: View and navigate all 12 PC Boxes.
- **Empty Slots**: Visualizes empty slots in Party, PC, and Inventory for future editing capabilities.
- **Modern Trainer Card**: Beautifully designed trainer card showing Play Time, Money, Badges, Rival Name, and Pokedex Stats.
- **Detailed Pokemon Viewer**: Click any Pokemon to see Stats, Moves, EXP, and Status.
- **Accurate Visuals**: Uses Generation 1 specific sprites (magnified pixel-art style) with corrected Internal-to-Dex ID mapping.
- **Inventory Management**: View Bag items and PC items.
- **Party Analysis**: Visualizes stats and sprites of your current team.
- **Secure**: Runs entirely in the browser using the FileReader API. No data is sent to any server.

## Deployment Instructions
1. Download this repository.
2. Rename `deploy.txt` to `deploy.bat`.
3. Run `deploy.bat` in Windows.
4. **Important**: Go to your `Pokemon-Save-Editor-Source` repository settings on GitHub -> Secrets and Variables -> Actions. Create a new repository secret named `ACTION_TOKEN` and paste your GitHub Personal Access Token there.

## Project Structure
```
/
├── components/       # UI Components (Viewer, Grid, Card, etc.)
├── core/             # Business Logic
│   ├── gen1/         # Generation 1 specific logic (Parser, Constants, Writer)
│   ├── theme.ts      # UI Theming Logic
│   ├── sprites.ts    # Sprite URL generation
│   └── types.ts      # Shared interfaces
├── data/             # Static resources (text.ts)
├── pages/            # View Controllers (UploadPage, EditorPage)
├── App.tsx           # Main Application Entry & Router
└── index.tsx         # React DOM Entry
```

## Tech Stack
- React 18
- TypeScript
- Tailwind CSS
- Vite
- Recharts (Data Visualization)
- Lucide React (Icons)

## Roadmap
- [x] Gen 1 Read Support
- [x] Trainer Editing (UI State)
- [x] Game Version Detection & Theming
- [x] Full PC Box Support (12 Boxes)
- [x] Detailed Stat Viewer
- [x] Pokedex & Rival Parsing
- [x] Fix: Sprite Mapping (Internal ID vs National Dex)
- [x] Heuristic Red/Blue Detection
- [x] Gen 1 Write Support (Checksum calculation & Download modified save)
- [ ] Gen 2 Support (Gold/Silver/Crystal)
- [ ] Advanced PC Management (Switch boxes)