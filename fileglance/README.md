# FileGlance

**Look before you open.**

A native Windows tray utility that shows an instant preview popup when you hover over a file in Explorer or on the Desktop. No keyboard shortcut. No browser runtime. Just hover.

---

## Download

👉 **[Download FileGlance-2026.09.20.003-Setup.exe →](https://github.com/NXJim/releases/raw/main/fileglance/FileGlance-2026.09.20.003-Setup.exe)**

| | |
|---|---|
| **Platform** | Windows 10 / 11 (64-bit) |
| **Install size** | < 5 MB |
| **Elevation** | Not required — installs per-user |
| **Runtime** | None — single native `.exe` |

---

## What it previews

- **Images** — JPEG, PNG, TIFF, GIF, BMP, HEIC, RAW, and anything Windows Imaging Component supports
- **Video** — MP4, MKV, AVI, MOV, WMV (Media Foundation)
- **PDF** — all pages, keyboard-navigable
- **File metadata** — size, dimensions, duration, codec, configurable display template

---

## Installation

1. Download the installer linked above, or browse the [`fileglance/`](https://github.com/NXJim/releases/tree/main/fileglance) folder.
2. Run the installer. No administrator prompt.
3. FileGlance starts in the notification area. Hover any file in Explorer.

> **Note — Windows SmartScreen warning:** Because FileGlance is not yet code-signed, Windows may show an "Unknown publisher" warning on first run. Click **More info → Run anyway** to proceed. This is expected for unsigned freeware and does not indicate malware.

---

## How it works

FileGlance installs as a tray icon with zero background CPU usage. A low-level mouse hook watches for a configurable dwell time (default 250 ms) over an Explorer or Desktop item. When triggered, a native Direct2D popup renders the file's content with no file-association launch and no temp files on disk.

---

## Self-update

FileGlance has a built-in update checker. When **Settings → General → Automatically check for updates on startup** is enabled, it fetches a small version manifest from this repo over HTTPS and offers any newer release as a Yes/No prompt. All downloads are SHA-256 verified before the swap.

You can also check manually on the **About** page at any time.

---

## Donate

FileGlance is free. If it saves you time, a small donation is appreciated.

**[Buy me a coffee ☕](https://buymeacoffee.com/jclements)** — or use the **Support** button inside the app.

---

## License

FileGlance is freeware. See [LICENSE.txt](LICENSE.txt) for the full terms.

Short version: free to use, not open source, no redistribution without permission.

---

## Release verification

Each release lists a SHA-256 hash in its release notes. Verify your download:

```powershell
Get-FileHash -Algorithm SHA256 FileGlance-2026.09.20.003-Setup.exe
```

The hash must match exactly before you run the installer.

---

## Recovery

If FileGlance fails to launch after a self-update, rename `fileglance.exe.old` back to `fileglance.exe` in `%LOCALAPPDATA%\Programs\FileGlance\` to restore the previous working build.

---

## Support / Issues

Open an issue on this repo for bug reports or feature requests. Include your Windows version and the FileGlance version from **About** (in the tray right-click menu).
