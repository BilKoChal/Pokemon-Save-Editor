# Pokemon Save Editor

A web-based tool for editing Pokemon save files, specifically optimized for Generation 1 (Red/Blue/Yellow) with a modular design to support future generations.

## Features
- **Gen 1 Support**: Fully parses `.sav` and `.srm` files (32KB).
- **Inventory Management**: View Bag items and PC items.
- **PC Storage**: Visualize Pokemon in the current PC Box.
- **Detailed Trainer Card**: View ID, Money, Play Time (HH:MM:SS), and Badges.
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
├── components/       # UI Components (TrainerCard, PartyGrid, PCBoxViewer, etc.)
├── core/             # Business Logic
│   ├── gen1/         # Generation 1 specific logic (Parser, Constants)
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
- [x] Gen 1 Read Support (Party, PC, Items, Trainer)
- [ ] Gen 1 Write Support (Checksum calculation)
- [ ] Gen 2 Support (Gold/Silver/Crystal)
- [ ] Advanced PC Management (Switch boxes)