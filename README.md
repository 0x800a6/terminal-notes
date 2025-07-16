# Terminal Notes

A feature-rich, keyboard-driven, markdown-compatible note-taking app that runs entirely in your terminal.  
Built with `curses` and `rich` for a clean and efficient terminal UI.

---

## Features

- All notes stored as Markdown files
- Full keyboard control (Vim-like UX)
- Modern terminal UI using `curses` and `rich`
- Customizable theme and config (colors, editor, etc)
- Live Markdown preview with rich formatting
- Optional note limit to manage clutter
- **Customizable note templates** with frontmatter support

---

## Requirements

- Python 3.8+
- `rich` library

```bash
pip install rich
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/0x800a6/terminal-notes.git
cd terminal-notes
```

### 2. Run the App

```bash
python3 src/main.py
```

_Note: You can also make it executable and run it directly._

---

## ⌨️ Keybindings

| Key        | Action                  |
|------------|-------------------------|
| `n`        | Create new note         |
| `Enter`    | Open note in editor     |
| `p`        | Preview note (markdown) |
| `d`        | Delete selected note    |
| `↑ / ↓`    | Navigate notes          |
| `q`        | Quit app                |

---

## ⚙️ Configuration

On first run, the app creates a config file at:

```
~/.terminal_notes/config.json
```

### Example config:

```json
{
  "editor": "nvim",
  "preview_cmd": "cat",
  "date_format": "%Y-%m-%d %H:%M",
  "max_notes": 100,
  "theme": {
    "highlight_fg": "black",
    "highlight_bg": "cyan",
    "normal_fg": "white",
    "normal_bg": "black"
  },
  "storage": "/home/yourname/.terminal_notes"
}
```

You can change:
- `editor`: the terminal text editor (e.g. `nano`, `nvim`, `vim`, `micro`)
- `max_notes`: max number of stored notes
- `theme`: terminal color settings
- `date_format`: how timestamps appear

---

## 📝 Custom Templates

The app supports customizable note templates. On first run, a default template is created at:

```
~/.terminal_notes/TEMPLATE.md
```

You can find the default template at [`TEMPLATE.md`](TEMPLATE.md).


### Template Variables:

- `{title}` - The note title you enter
- `{description}` - The note description you enter (required)
- `{created_at}` - Timestamp when the note was created
- `{updated_at}` - Same as created_at (for future use)

You can customize this template file to match your preferred note structure, add custom frontmatter, or include default sections that fit your workflow.

---

## 📁 Storage Structure

All notes and configs live in `~/.terminal_notes/`:

```
~/.terminal_notes/
├── index.json           # Metadata index
├── config.json          # Config file
├── TEMPLATE.md          # Note template (customizable)
└── 2024-07-16_13-23.md  # Individual notes
```

---

## 📌 Roadmap Ideas

- [ ] Tag-based filtering
- [ ] Search and fuzzy match
- [ ] Git sync / backup
- [ ] Archive/deletion system
- [ ] Local website / webserver

---

## 📜 License

MIT — do whatever you want.

---

## 🧠 Author

Built with caffeine and a keyboard by [Lexi](https://github.com/0x800a6).
