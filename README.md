```
 _________      __ ______  __  __________  ___  _________ 
/_  __/ _ \____/ // / __ \/  |/  / __/ _ \/ _ |/ ___/ __/ 
 / / / , _/___/ _  / /_/ / /|_/ / _// ___/ __ / (_ / _/  
/_/ /_/|_|   /_//_/\____/_/  /_/___/_/  /_/ |_\___/___/
```

# Terminal Homepage

> A terminal-style browser homepage with smart URL/search detection.

---

## Features

```bash
$ ./homepage --features

[✓] Terminal-style UI with green-on-black theme
[✓] Smart input detection (URL vs Search)
[✓] Bing search integration (cn.bing.com)
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

## Input Behavior

| Input Type | Example | Action |
|------------|---------|--------|
| URL with protocol | `https://github.com` | Direct visit |
| URL without protocol | `google.com` | Direct visit |
| Domain with www | `www.baidu.com` | Direct visit |
| IP Address | `192.168.1.1` | Direct visit |
| Search keywords | `how to learn python` | Bing search |

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + L` | Clear input & focus |
| `Enter` | Submit input |

---

```
user@terminal-homepage:~$ echo "Enjoy your browsing!"
```
