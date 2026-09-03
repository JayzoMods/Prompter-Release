# Prompter

Windows app by **Jayden O'Grady**. Interview a rough idea, then compile a production-grade prompt for any target agent.

Download the latest `.exe` from [Releases](https://github.com/JayzoMods/Prompter-Release/releases). This repository holds release artifacts only — not the application source.

## Install

- **Installer:** `Prompter-*-win-x64.exe` — NSIS installer (choose a folder, Start Menu shortcut).
- **Portable:** `Prompter-*-portable.exe` — run without installing.

Windows may show a SmartScreen prompt for an unsigned build. Choose **More info → Run anyway** if you trust this download.

## Connect

1. Open Prompter.
2. **Connect**.
3. **Mode G (Cursor):** sign in with Cursor or paste a Cursor API key. Requires a Cursor account. The Cursor IDE does not need to be open.
4. **Mode C (Claude):** paste an Anthropic API key.

Keys stay on this PC (Windows DPAPI). They are not uploaded to GitHub.

## Use

1. Left **AGENT** = the engine that writes the prompt (curated list).
2. Right **AGENT** = who the compiled prompt is *for*.
3. **EFFORT LEVEL** = suggested effort when *you* run that prompt on the target.
4. Type your idea → **Run**. Skip questions if you already know the answers.
5. **Copy** or **Save .md** the compiled prompt.

## Publisher

Jayden O'Grady · [OG Digital Designs](https://ogdigitaldesigns.com.au)
