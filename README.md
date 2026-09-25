# OpenWhip Piseth Fork

![Whip divider](assets/divider.png)

Sometimes Claude Code is going too shlow, and you must whip him into shape..

This fork adds:
- A **tray-launched config window** to add / remove the phrases yelled at Claude.
- **Unicode phrase support** (Arabic, emoji, anything) via `SendInput` with a VK-first / Unicode-fallback strategy so terminals still receive real key events for ASCII.
- **Persistent phrases** stored in your Electron `userData` folder.
- Single-instance lock + GPU cache fix to stop Chromium spamming `Access is denied` on Windows.

## Install + run

### Windows

```bash
npm install -g openwhippisethfork
openwhippisethfork
```

### macOS

```bash
npm install -g openwhippisethfork
openwhippisethfork
```

### Linux

Install the required keyboard automation dependency, then run:

```bash
sudo apt install xdotool
npm install -g openwhippisethfork
openwhippisethfork
```

This app is designed to work on Windows, macOS, and Linux.

## Controls

- **Click the tray icon** → phrase editor opens.
- **Add** phrases (one per line). **Start Whipping** spawns the whip overlay.
- Move the mouse to crack the whip → it sends **Ctrl+C** then types a random phrase + Enter into the currently focused app.
- **Click** inside the overlay to drop the whip. Clicking the tray icon while the whip is live also drops it and reopens the editor.
- Right-click tray → **Quit**.

## Development

```bash
git clone https://github.com/pisethch7/OpenWhipPisethFork
cd openwhippisethfork
npm install
npm start
```

## Credits

Originally based on GitFrog1111's [OpenWhip](https://github.com/GitFrog1111/OpenWhip) and openwhip-plus's [openwhip-plus](https://github.com/dashty8/openwhip-plus). MIT licensed.

## Roadmap

- [x] Configurable phrase list
- [x] Unicode / Arabic phrases
- [x] Persisted config
- [ ] Clipboard-paste fallback for terminals that swallow `KEYEVENTF_UNICODE`
- [ ] Crack counter
"# OpenWhipPisethFork" 
