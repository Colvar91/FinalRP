# RP Chat Window (Dalamud Plugin)

A dedicated roleplay chat window for **Final Fantasy XIV (Dalamud)** that makes RP conversations easier to read and long posts easier to write.

## Features

- **Custom RP Chat Window**
  - Separate from the default FFXIV chat log
  - Designed to feel similar to “Chat 2”, but focused on roleplay

- **RP-friendly formatting**
  - **/s (Say):** normal text shown in **white**
  - **Inline emotes inside /s** are highlighted in **orange**
    - `*...*`
    - `<...>`
  - **/em (Emote):** the whole message is shown in **orange**
    - Text inside quotes `"..."` is shown in **white** (spoken dialogue)
  - Emotes are rendered in an FFXIV-style format:
    - `Name text` (no colon)

- **No timestamps**
  - Messages are displayed as `Name: Text`
  - Emotes are displayed as `Name Text`

- **Word-like line wrapping**
  - Long lines automatically wrap downwards
  - Nothing disappears off the right side of the window

- **Composer (Writing Box)**
  - Paste text from Word or anywhere else
  - **Enter = Send**
  - **Shift + Enter = New line**
  - Automatically **splits long messages** to respect the in-game chat limit

- **Filters & Search**
  - Toggle channels: Say / Emote / Tell / Party / Yell / Shout
  - Search messages in the log

- **Settings Button**
  - Extra options are accessible through a **Settings** menu so nothing goes out of view

---

## Installation

This plugin is currently meant to be tested as a **Dev Plugin**.

### Requirements
- **Dalamud API 14**
- **.NET 10 SDK**
- **Visual Studio Code** (or Visual Studio / Rider)

### Build (VS Code)
Open the project folder and run:

```powershell
dotnet restore
dotnet build -c Release
