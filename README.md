# Pokédex Data Fetcher & GUI

A modern, dual-interface Python application to fetch and display Pokémon data using the [PokéAPI](https://pokeapi.co/). Features both a quick **Command Line Interface (CLI)** for scripts and a beautiful **Graphical User Interface (GUI)** for a visual experience.

![PokéAPI Logo](https://raw.githubusercontent.com/PokeAPI/media/master/logo/pokeapi_256.png)

---

## Features

- **CLI Mode**: Quickly fetch stats, height, weight, and abilities in the terminal.
- **GUI Mode**: A modern, dark-themed interface built with customtkinter.
  - All **6 base stats** with animated progress bars (HP · ATK · DEF · SP.ATK · SP.DEF · SPD).
  - High-quality official Pokémon artwork.
  - Responsive search (press Enter or click Search) with specific error messages.
  - Displays Types and Abilities.
- **Windows MSI Installer**: Install via Pokedex-Setup.msi — adds Desktop & Start Menu shortcuts and a proper uninstaller.
- **Portable EXE**: Standalone executable — no Python installation needed.

---

## Installation

### Option A — Windows Installer (recommended)
Download Pokedex-Setup.msi from the [Releases](../../releases) page and run it.

### Option B — Portable EXE
Download Pokedex.exe from the [Releases](../../releases) page and double-click it.

### Option C — Run from Source

**Prerequisites:** Python 3.8+

`bash
git clone https://github.com/toxicbishop/Poke-Fetch.git
cd Poke-Fetch
pip install -r requirements.txt
`

---

## Usage

### Graphical Interface (GUI)
`bash
python pokedex_gui.py
`
Enter a Pokémon name (e.g., charizard) and press **Enter** or click **Search**.

### Command Line (CLI)
`bash
python request_API_From_PokeAPI.py
`

---

## Distribution

### MSI Installer (recommended for sharing)
`bash
# Requires WiX 4
dotnet tool install --global wix --version 4.0.5
python -m PyInstaller Pokedex.spec --noconfirm
wix build installer/Pokedex.wxs -o dist/Pokedex-Setup.msi
`

### Portable EXE
`bash
pip install pyinstaller
python -m PyInstaller Pokedex.spec --noconfirm
# Output: dist/Pokedex.exe
`

---

## Tech Stack

| Layer | Library |
|-------|---------|
| GUI framework | customtkinter |
| Image handling | Pillow |
| HTTP requests | 
equests |
| Packaging | PyInstaller + WiX 4 |
| Data source | [PokéAPI v2](https://pokeapi.co/api/v2/) |

---

## License

This project is open source under the [MIT License](LICENSE).
Data provided by [PokéAPI](https://pokeapi.co/).
