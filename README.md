```
 _________      __ ______  __  __________  ___  _________ 
/_  __/ _ \____/ // / __ \/  |/  / __/ _ \/ _ |/ ___/ __/ 
 / / / , _/___/ _  / /_/ / /|_/ / _// ___/ __ / (_ / _/  
/_/ /_/|_|   /_//_/\____/_/  /_/___/_/  /_/ |_\___/___/
```

# Terminal Homepage

> A terminal-style browser homepage with smart URL/search detection and bookmarks.

---

## Features

```bash
$ ./homepage --features

[✓] Full-window terminal UI, text anchored top-left
[✓] Smart input detection (URL vs Search)
[✓] Bing search integration (cn.bing.com)
[✓] Force-search command (-f / -F)
[✓] Bookmark commands (-add / -j / -ls / -rm)
[✓] Clear-history command (-clr)
[✓] Customizable theme (text color, background color, image, opacity, blur, bleed)
[✓] Auto-focus input field
[✓] Real-time clock display
[✓] Keyboard shortcuts support
```

## Usage

```bash
# Open index.html in your browser
$ open index.html

# Or serve locally
$ python -m http.server 8080
```

## Commands

| Command | Example | Action |
|---------|---------|--------|
| `-f` | `-f how to learn python` | Force search (ignores URL detection) |
| `-add` | `-add github https://github.com` | Add/update a bookmark |
| `-j` | `-j github` | Jump to a bookmark's URL |
| `-ls` | `-ls` | List all bookmarks |
| `-rm` | `-rm github` | Remove a bookmark |
| `-clr` | `-clr` | Clear terminal history |

> All commands are case-insensitive (`-F`, `-LS`, `-CLR`, ...).

## Input Behavior

| Input Type | Example | Action |
|------------|---------|--------|
| URL with protocol | `https://github.com` | Direct visit |
| URL without protocol | `google.com` | Direct visit |
| Domain with www | `www.baidu.com` | Direct visit |
| IP Address | `192.168.1.1` | Direct visit |
| Search keywords | `how to learn python` | Bing search |
| Force search | `-f how to learn python` | Bing search |

## Settings

Open the `[ Settings ]` panel (top-right) to customize:

- **Username** — shown in the prompt
- **Open links in new tab** — toggle new-tab navigation
- **Background Image Path** — relative to `index.html` (e.g. `images/bg.jpg`), or a full URL
- **Background Image Opacity** — 0–100%
- **Background Image Blur** — 0–40px
- **Background Bleed** — 0–100px (extends the background to cover blur edges)
- **Text Color** — restrained retro palette
- **Background Color** — dark palette

Click `Save Settings` to persist changes (stored in `localStorage`).

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + L` | Clear input & focus |
| `Enter` | Submit input |

---

```
user@terminal-homepage:~$ echo "Enjoy your browsing!"
```