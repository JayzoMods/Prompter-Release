# Prompter

Windows app by **Jayden O'Grady**. You type a rough idea. Prompter interviews you, then compiles a prompt you paste into another AI (Cursor, Claude, ChatGPT, and so on). It is a prompt compiler, not a chatbot — it will not answer the idea in this window.

Current build: **0.2.3**. Download it from [Releases](https://github.com/JayzoMods/Prompter-Release/releases). This repository holds release artifacts only — not the application source.

## What to run

Install **`Prompter-0.2.3-win-x64.exe`** (NSIS installer). You can choose a folder; it adds Start Menu and desktop shortcuts.

The zip **`Prompter-0.2.3-win-x64.zip`** is fine if you prefer to unpack a folder.

Do **not** run `Prompter.exe` from a `win-unpacked` folder on its own, and do **not** use the `*-portable.exe` build. Those are eaten by Windows Defender on some PCs.

## Windows SmartScreen

This build is **unsigned**. Windows may say Windows protected your PC.

1. Click **More info**.
2. Click **Run anyway**.

That is expected. A self-signed certificate would not clear SmartScreen. Only a paid Authenticode certificate would.

## First launch

A short interactive tour highlights each control as it explains it. Skip it if you already know the app. Replay anytime: **Settings → How Prompter works**.

First launch asks you to **Accept** or **Decline** the Terms of Use (licence, privacy notice, and anti-piracy rules). Decline closes Prompter. Settings → **Terms of use** shows the same text later. The NSIS installer also shows that licence before install.

## Connect

Open Prompter → **Connect**. Pick an engine on the IDEA pane, then connect that engine. You only need the one you will actually use.

| Engine | What you need |
|--------|----------------|
| **Cursor** | **Sign in with Cursor** (browser). Requires a Cursor account. The Cursor IDE does not need to be open, and Prompter does not use the IDE login. **Or paste CURSOR_API_KEY** is optional — only if you would rather paste a key from the [Cursor dashboard](https://cursor.com/dashboard). |
| **Claude** | An **API key** from the [Anthropic Console](https://console.anthropic.com/settings/keys) (same product as [platform.claude.com](https://platform.claude.com)), with **prepaid API credits** on that account. A [Claude.ai](https://claude.ai) Pro month is **not** an API key and will not connect. |
| **Gemini** | A Google AI Studio key from [aistudio.google.com/apikey](https://aistudio.google.com/apikey). |
| **Ollama** | [Ollama](https://ollama.com/download) running on this PC. No cloud key. |
| **Cline** | [Ollama](https://ollama.com/download) or [LM Studio](https://lmstudio.ai/) running on this PC. No cloud key. |

Cloud keys stay on **this PC** (Windows DPAPI). Prompter has no servers of its own. Keys are not uploaded to GitHub.

If Claude connects but **Run** fails, it is almost always billing (no credits on the API key), not the paste box.

## Use

1. **IDEA** (left) = what you want. **PROMPT** (right) = the compiled text you copy.
2. Left **AGENT** = which engine writes the prompt. Connect first so the list loads.
3. Right **AGENT** = who you will paste into. Right **EFFORT LEVEL** = how hard they should work (or let Prompter suggest).
4. Set left AGENT, right AGENT, and right EFFORT LEVEL, then **Run**.
5. Answer Diagnostics questions, then **Send answers**. **Compile now** uses whatever you have answered. **Skip questions** (centre) compiles with no interview.
6. **Copy** from the right pane (or Save file as JSON, Markdown, or text). That text is for the target agent, not Prompter answering you. After a compile, you can edit the **ASSUMPTIONS** line under the panes, then **Save line** (keep the prompt) or **Recompile with these** (fold those facts into a new prompt).

Left EFFORT LEVEL is how thorough the *compile* is. It is not the same as the right-hand target effort.

## Publisher

Jayden O'Grady · [OG Digital Designs](https://ogdigitaldesigns.com.au) · [enquiries@ogdigitaldesigns.com.au](mailto:enquiries@ogdigitaldesigns.com.au)
