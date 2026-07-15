# 🩺 FileDoctor

**Detect. Diagnose. Repair.** — A browser-based forensic tool that identifies the true format of a corrupted file and repairs deliberately broken headers, magic bytes, dimension fields, and checksums — entirely client-side. Nothing is ever uploaded to a server.

🔗 **Live Demo:** [prasadchinnapati.github.io/filedoctor](https://prasadchinnapati.github.io/filedoctor/)

---

## 📖 About

FileDoctor is a lightweight, single-file HTML/CSS/JavaScript tool designed for CTF (Capture The Flag) forensics challenges and general file-corruption debugging. Many CTF "forensics" challenges give you a file with a wrong extension or a deliberately corrupted header. FileDoctor reads the raw bytes of any file, figures out what it *actually* is (regardless of its extension), and patches common corruption patterns automatically.

---

## ✨ Features

- 🔍 **Format Auto-Detection** — Reads raw magic bytes to identify the true file type, ignoring the extension entirely
- 🛠 **Header Repair** — Fixes corrupted magic bytes/signatures back to valid values
- 📐 **Structural Validation** — Checks for required trailers/markers (e.g. `%%EOF` for PDFs, End-of-Central-Directory for ZIPs)
- 🖼 **Live Preview** — Instantly preview repaired images and PDFs in-browser
- 📊 **Detailed Repair Log** — Step-by-step log of every check performed and every fix applied
- 💾 **One-Click Download** — Download the repaired file immediately
- 🔒 **100% Client-Side** — No uploads, no server, no tracking — everything happens locally in your browser

### Supported Formats
| Format | Extension |
|--------|-----------|
| PNG | `.png` |
| JPEG / JFIF | `.jpg`, `.jpeg` |
| PDF | `.pdf` |
| GIF | `.gif` |
| BMP | `.bmp` |
| ZIP | `.zip` |

---

## ⚙️ How It Works

1. **Load** — Drag and drop any file, or click to browse. Extension is ignored.
2. **Detect** — The tool reads the first few bytes (the "magic bytes") of the file and matches them against known format signatures.
3. **Analyze** — Click **Analyze & Repair**. FileDoctor checks:
   - File signature / magic bytes
   - Format-specific structural markers (e.g. IHDR chunk for PNG, xref table for PDF)
   - Missing trailers or footers
4. **Repair** — Any corrupted bytes are patched to valid values automatically, and a log explains exactly what was changed.
5. **Preview & Download** — View the repaired file inline (for images/PDFs) and download the fixed version.

---

## 🖥️ Screenshot

![FileDoctor UI](screenshot.png)

---

## 🚀 Usage

### Run Locally
```bash
git clone git@github.com:prasadchinnapati/filedoctor.git
cd filedoctor
# just open index.html in any browser
```

### Run Online
Just visit: [prasadchinnapati.github.io/filedoctor](https://prasadchinnapati.github.io/filedoctor/)

No installation, no dependencies, no build step required.

---

## 🧑‍💻 Tech Stack
- Pure HTML5, CSS3, and vanilla JavaScript
- No frameworks, no external libraries, no backend

---

## ⚠️ Disclaimer
This tool is intended for **educational and CTF practice purposes** — repairing intentionally corrupted challenge files. It performs basic header/signature-level repairs only; it is not a full data-recovery tool for genuinely damaged files.

---

## 📄 License
MIT License — free to use, modify, and distribute.

---

## 👤 Author
**Prasad Chinnapati**
