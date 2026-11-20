# Flowchart Master

(formerly ORGANIGRAM) – offline Windows desktop application to create, edit, reconstruct, manage and export flowcharts, organisational charts and logical block diagrams.

- **User guide (EN/IT):** [USER_GUIDE.md](USER_GUIDE.md)
- **Behaviour numbers:** [MECHANICS.md](MECHANICS.md) / `mechanics.json`
- **Installer:** `dist/FlowchartMaster-Setup-<version>-r<release>.exe` – double-click to install (no administrator rights)
- **Portable build:** `dist/Flowchart Master/` (copy the folder anywhere and run `FlowchartMaster.exe`)
- **Samples:** `samples/` – org charts, flowcharts, swimlanes, decision tree, architecture, RACI matrix (`*.orgm`, English and Italian) and rendered PNGs to try the picture reconstruction.

## Releases, installer and updates

- The release number is progressive and lives in `release.txt`; it is shown in *Help › About*, in the installer, in Windows' file properties (file version `1.1.0.<release>`) and in *Settings › Installed apps*.
- `package.ps1` makes the next release: it raises the number, builds, and writes the installer plus the portable folder into `dist/` (`-Keep` rebuilds the same number).
- The installer is the program itself saved under a "Setup" name: it copies itself to `%LOCALAPPDATA%\Programs\Flowchart Master`, adds Start-menu/desktop shortcuts, the `.orgm` file type and an uninstall entry (`FlowchartMaster.exe --uninstall`). Run over an older installation it upgrades it and keeps projects and settings.
- **Updates (offline):** the program looks for a newer `FlowchartMaster-Setup-*-r<N>.exe` in its update folder at start-up (and on *Help › Check for updates*). The folder is the one it was installed from unless another one (local or a network share) is set in *Tools › Settings › Updates*. When a higher release is found it offers *Install now / Later / Skip this release*; installing saves the work, closes the program, upgrades and restarts it. Nothing goes on the internet.

## Technology

The specification preferred Python/Qt and allowed "another suitable desktop development framework". None of the Python stack (PySide6, OpenCV, Tesseract) was installed on the target PC, and the deliverable had to be a portable, offline Windows program, so Flowchart Master is written in **Rust** and ships as **one self-contained executable** (no runtime):

| Need | Implementation |
|---|---|
| GUI | egui / eframe (OpenGL), native Windows file dialogs (rfd); light, dark and custom-coloured interface |
| Rendering & export | own vector renderer shared by canvas, SVG, PDF and PowerPoint; PNG/JPG via resvg |
| Fonts | built-in families plus every installed Windows font, read on first use |
| Image processing | own implementation (crop, perspective, deskew, contrast, denoise, sharpen, background cleanup, morphology, connected components) |
| OCR | Windows built-in OCR engine (Windows.Media.Ocr – local, free, Italian/English); optional local Tesseract |
| PDF import | Windows built-in PDF renderer (Windows.Data.Pdf) + reconstruction; Flowchart Master PDFs re-open losslessly |
| Layout | own hierarchical (balanced/compact contour) and layered (Sugiyama-style) engines |
| Storage | `.orgm` JSON projects with embedded pictures and version history; settings as JSON in `%APPDATA%\Flowchart Master` (moved once from `%APPDATA%\Organigram`; or `portable_data`) |
| Icon & version info | `assets/icon.ico` + VERSIONINFO compiled by `build.rs` with the Windows SDK `rc.exe` |

All libraries are open source (MIT / Apache-2.0 / Zlib). No cloud services, no paid APIs, no network access.

## Build

```
cargo build --release
```

The executable is `target/release/FlowchartMaster.exe`.

Command line:

```
FlowchartMaster [file.orgm | picture.png | drawing.svg | document.pdf | staff.csv]
FlowchartMaster --screenshot out.png      # automated check: draw 120 frames, save the window, exit
FlowchartMaster --self-test out.json      # automated check of editing, exports, reconstruction, keys
FlowchartMaster --export-samples folder   # write the sample projects
FlowchartMaster --recognize picture.png   # print what the reconstruction engine finds
FlowchartMaster --install [--update]      # installer window (also when the file name contains "Setup")
FlowchartMaster --uninstall               # remove the installed program
FlowchartMaster --find-update [folder]    # print which installer would be offered as an update
FlowchartMaster --setup-screenshot out.png
```

## Source map

| File | Purpose |
|---|---|
| `model.rs` | projects, diagrams, blocks, connectors, line styles, arrowheads, org data |
| `geometry.rs` | shapes, anchors, routing, merging of overlapping connectors, arrowheads, double lines |
| `content.rs` | text/photo/icon layout inside blocks (shared by all outputs) |
| `render.rs`, `canvas.rs` | canvas drawing and interaction (wheel zoom, multi-resize, minimap) |
| `panels.rs`, `ui_main.rs`, `ui_dialogs.rs` | library, properties, menus, toolbar, tabs, dialogs |
| `app.rs` | state, undo/redo, org commands, clipboard, files, autosave |
| `layout.rs` | automatic layouts, align/distribute, validation |
| `theme.rs` | themes (incl. Original and Dark), palettes, department colours |
| `fonts.rs` | interface looks and colours, system fonts |
| `update.rs` | name, release number, installer, uninstaller, updates |
| `vision.rs`, `recog.rs`, `ocr.rs`, `wizard.rs` | picture pre-processing, recognition, OCR, import wizard |
| `export_svg.rs`, `export_pdf.rs`, `interop.rs` | SVG/PNG/JPG, PDF/print, PPTX, CSV, SVG import |
| `samples.rs`, `i18n.rs`, `settings.rs`, `selftest.rs` | templates, Italian/English, settings & recovery, automated checks |
