# Pokemon Save Editor

A web-based tool for editing Pokemon save files.

## Features
- **Visual Editor**: Modify stats, money, and items.
- **Party Management**: View and edit current party Pokemon.
- **Secure**: Runs entirely in the browser.

## Deployment Instructions
1. Download this repository.
2. Rename `deploy.txt` to `deploy.bat`.
3. Run `deploy.bat` in Windows.
4. **Important**: Go to your `Pokemon-Save-Editor-Source` repository settings on GitHub -> Secrets and Variables -> Actions. Create a new repository secret named `ACTION_TOKEN` and paste your GitHub Personal Access Token there. This allows the automated build system to deploy the website.

## Tech Stack
- React 18
- TypeScript
- Tailwind CSS
- Vite
