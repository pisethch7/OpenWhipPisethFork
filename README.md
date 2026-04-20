# OpenWhip (dashty8 fork)

![Whip divider](assets/divider.png)

Sometimes Claude Code is going too shlow, and you must whip him into shape..

This fork adds:
- A **tray-launched config window** to add / remove the phrases yelled at Claude.
- **Unicode phrase support** (Arabic, emoji, anything) via `SendInput` with a VK-first / Unicode-fallback strategy so terminals still receive real key events for ASCII.
- **Persistent phrases** stored in your Electron `userData` folder.
- Single-instance lock + GPU cache fix to stop Chromium spamming `Access is denied` on Windows.

## Install + run

```bash
npm install -g openwhip-plus
openwhip-plus
```

Windows and macOS work out of the box. Linux needs `xdotool` for keyboard automation:

```bash
sudo apt install xdotool
```

## Controls

- **Click the tray icon** → phrase editor opens.
- **Add** phrases (one per line). **Start Whipping** spawns the whip overlay.
- Move the mouse to crack the whip → it sends **Ctrl+C** then types a random phrase + Enter into the currently focused app.
- **Click** inside the overlay to drop the whip. Clicking the tray icon while the whip is live also drops it and reopens the editor.
- Right-click tray → **Quit**.

## Development

```bash
git clone https://github.com/dashty8/openwhip
cd openwhip
npm install
npm start
```

## Credits

Originally based on [GitFrog1111/OpenWhip](https://github.com/GitFrog1111/OpenWhip). MIT licensed.

## Roadmap

- [x] Configurable phrase list
- [x] Unicode / Arabic phrases
- [x] Persisted config
- [ ] Clipboard-paste fallback for terminals that swallow `KEYEVENTF_UNICODE`
- [ ] Crack counter
