# Ultimate YT Downloader (GUI) - Windows Installer

Professional Windows installer distribution for **Ultimate YT Downloader**.

This repository is for **app delivery only** (installer files and assets). Source code is maintained in a separate development repository.

## Repository Contents

- `setup.exe` - Recommended installer package
- `YT-M Downloader.msi` - Alternative MSI installer package
- `GUI YT-M.png` - GUI preview image
- `releases/` - Published release index and per-version notes

## What the App Does

Ultimate YT Downloader provides a Windows GUI for downloading media with configurable defaults.

Main capabilities:
- Download types: `single`, `playlist`, `audio`
- Profile presets: `compatible`, `best`
- Optional subtitle download
- Built-in setup action to prepare required download tools
- Save reusable defaults from the GUI
- Optional dark mode
- Output console panel for runtime logs/status

## System Requirements

- Windows 10 or Windows 11
- Internet connection
- Local write permission for your chosen download folder

## Installation

### Option A (Recommended): `setup.exe`

1. Download `setup.exe` from this repository.
2. Right-click the file and choose **Run as administrator** (recommended).
3. Complete the installer wizard.
4. Launch **Ultimate YT Downloader** from Start Menu or Desktop shortcut.

### Option B: `YT-M Downloader.msi`

1. Download `YT-M Downloader.msi`.
2. Double-click to install (or deploy through enterprise software tools).
3. Launch **Ultimate YT Downloader** after installation.

## First Run (Recommended)

1. Open the app.
2. Click **Run Setup** to initialize required runtime tools.
3. Set:
   - **Type** (`single` / `playlist` / `audio`)
   - **Profile** (`compatible` / `best`)
   - **Download Path**
   - **Log Mode** (`cmd` or `file`)
   - **Download Subtitles** (optional)
4. Click **Save Defaults**.
5. Paste a valid media URL.
6. Click **Start Download**.

## UI Overview

From the current GUI:
- Top actions: **Run Setup**, **Save Defaults**, **Dark Mode**
- Main form fields: URL, Type, Profile, Download Path, Log Mode, Subtitles toggle
- Utility actions: **Browse**, **Open Folder**, **Copy Output**, **Clear Output**
- Bottom status area: live state (for example, `Ready`)

## Troubleshooting

- **Installer blocked by SmartScreen**: Click **More info** -> **Run anyway** only if downloaded from a trusted project source.
- **Cannot start download**: Run **Run Setup** first, then retry.
- **No files downloaded**: Verify URL validity, internet connection, and that target folder is writable.
- **Permission errors**: Change download path to a user-writable folder (for example `D:\Downloads`).
- **No visible logs**: Switch Log Mode and retry; use output panel and copy logs for support.

## Security and Verification

For safer installation:
- Download installers only from trusted project releases.
- Verify file hashes when a checksum is provided.
- Scan installers with your endpoint security solution before execution.

Generate a local SHA-256 hash in PowerShell:

```powershell
Get-FileHash ".\setup.exe" -Algorithm SHA256
Get-FileHash ".\YT-M Downloader.msi" -Algorithm SHA256
```

## Releases

Latest stable release:
- Version: `v1.0.0`
- Date: `2026-03-24`
- Status: First and currently only published app release

Release documentation:
- `CHANGELOG.md` - Full change history
- `releases/README.md` - Published versions index
- `releases/v1.0.0/README.md` - v1.0.0 release details

## Notes

- This repository is intended for distribution and installation.
- For feature requests, bug reports, or source changes, use the main development repository.
