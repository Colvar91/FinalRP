# RP Chat Window (Prototype) – Test ZIP

Dieses ZIP enthält ein lauffähiges **Prototype-Dalamud-Plugin** mit einem **eigenen RP-Chatfenster**:

- Eigenes Chat-Window (wie „Chat 2“, aber minimal)
- **Emotes orange**, „gesprochene“ Nachrichten weiß
- Basic Filter (Say / Emote / Tell / Party / Yell/Shout)
- Search
- **Composer** mit „Split & Clipboard-Queue“ für lange RP-Posts

## Voraussetzungen

- Aktuelles Dalamud API 14 (Stable)
- **.NET 10** SDK (für API 14)
- Visual Studio / Rider

## Build

1. `RPChatWindow.sln` öffnen
2. `Release` builden

Die DLL findest du dann unter:

`RpChatWindow/bin/Release/net10.0-windows/RpChatWindow.dll`

## In-Game testen (Dev Plugin)

1. Spiel starten
2. `/xlsettings` → **Experimental** → **Dev Plugin Locations**
3. Pfad zur **RpChatWindow.dll** hinzufügen (oder den Ordner)
4. `/xlplugins` → **Dev Tools** → Installed Dev Plugins → `RP Chat Window` aktivieren

Dann im Chat:

- `/rpchat` = Fenster toggeln

## Hinweise

- Das Server-Chatlimit kann ein Plugin **nicht entfernen**. Der Composer splittet und kopiert die Chunks in die Zwischenablage.
- **Auto-Senden als Charakter ist über die öffentliche Dalamud-API nicht vorgesehen.**
  Darum nutzt dieses Plugin einen sicheren Workflow: Beim Senden wird **Chunk 1/N** in die Zwischenablage kopiert.
  Du fügst ihn im normalen Chat mit **Strg+V** ein und drückst Enter.
  Sobald deine Nachricht im Chat erscheint, kopiert das Plugin automatisch den nächsten Chunk.
- MVP rendert aktuell Plaintext. Später kann man echte SeString-Payloads (Icons, Links, etc.) sauber rendern.

