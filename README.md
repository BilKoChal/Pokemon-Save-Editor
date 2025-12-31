# BilKo's PC: Gen 1 Save Editor

**BilKo's PC** is a comprehensive Pokemon game save editor curated by BilKoChal. It runs entirely in your browser using local file processing, ensuring your save data never leaves your device. Designed with modularity for future generations.

## Features
- **Gen 1 Support**: Fully parses `.sav` and `.srm` files (32KB).
- **Trainer Editing**: Edit Trainer Name and Money directly from the dashboard and **Save Changes** back to a `.sav` file.
- **Trade Evolutions**: Evolve Kadabra, Haunter, Machoke, and Graveler with a single click without trading!
- **Box Stats**: View calculated stats (Atk/Def/Spc/Spd) for Pokemon even when they are stored in the PC.
- **Pokedex Viewer**: Visualize your Catch/Seen progress with detailed descriptions and sprite tracking.
- **Original Filename**: Downloads preserve the original uploaded filename.
- **Improved Version Detection**: Uses Heuristics (Pokedex exclusives) to distinguish between Red and Blue versions.
- **Advanced Stats**: View IVs (DVs) and EVs (Stat Experience) for every Pokemon to check legality and training progress.
- **Interactive Charts**: Analyze stats using Radar (Spider) or Bar charts.
- **Red/Blue/Yellow Support**: Automatically detects Yellow version. For Red/Blue, users can toggle the theme manually if preferred.
- **Full PC Storage**: View and navigate all 12 PC Boxes.
- **Modern Trainer Card**: Beautifully designed trainer card showing Play Time, Money, Badges, Rival Name, and Pokedex Stats.
- **Detailed Pokemon Viewer**: Click any Pokemon to see Stats, Moves, EXP, and Status.
- **Accurate Visuals**: Uses Generation 1 specific sprites (magnified pixel-art style).
- **Inventory Management**: View Bag items and PC items.
- **Secure**: Runs entirely in the browser using the FileReader API. No data is sent to any server.

## Deployment Instructions
1. Download this repository.
2. Rename `deploy.txt` to `deploy.bat`.
3. Run `deploy.bat` in Windows.
4. **Important**: Go to your `BilKos-PC-Source` repository settings on GitHub -> Secrets and Variables -> Actions. Create a new repository secret named `ACTION_TOKEN` and paste your GitHub Personal Access Token there.

## Project Structure
```
/
├── components/       # UI Components (Footer, Viewer, Grid, Card, Pokedex)
├── core/             # Business Logic
│   ├── gen1/         # Generation 1 specific logic (Parser, Constants, Writer)
│   ├── theme.ts      # UI Theming Logic
│   ├── sprites.ts    # Sprite URL generation
│   └── types.ts      # Shared interfaces
├── data/             # Static resources (text.ts, pokedex_entries.ts)
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
