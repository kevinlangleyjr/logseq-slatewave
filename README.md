# Slatewave (Logseq)

A dark Logseq theme on a slate foundation with a teal signature. Designed as a twin to the [Slatewave VSCode theme](https://github.com/kevinlangleyjr/vscode-slatewave), the [Slatewave Obsidian theme](https://github.com/kevinlangleyjr/obsidian-slatewave), and the [Slatewave oh-my-posh prompt](https://github.com/kevinlangleyjr/slatewave-omp) — editor, terminal, and notes share a single color vocabulary.

> _Slate below, teal above._

---

## What it styles

Slatewave is written against Logseq's `--ls-*` CSS variable API — no upstream theme dependencies. It tunes:

- **Headings** — teal cascade (H1–H3 `#5eead4`, H4 `#99f6e4`, H5 `#7dd3fc`, H6 `#b388ff`)
- **Bullets** — pink `#fb7185` markers so lists read at a glance
- **Accent states** — active block, command palette selection, cursor, and focus rings resolve to `#5eead4`
- **Links** — page refs teal, external links sky, unresolved refs pink
- **Block refs** — dashed sky underline; teal on hover
- **Tags** — teal on a faint teal pill
- **Code** — inline pill with pale-teal foreground on `#1e293b`; fenced blocks get a soft border and Slatewave-flavoured `hljs` tokens
- **Task markers** — `TODO` pink, `DOING` amber, `DONE` muted teal, `WAITING` sky
- **Sidebars & header** — darker slate (`#21252b`) to frame the editor canvas (`#282c34`)

Dark mode only.

---

## Installation

### From the Logseq Marketplace

_(TBD — not yet published)_

### From a local clone

1. Clone this repo somewhere stable:

   ```sh
   git clone https://github.com/kevinlangleyjr/logseq-slatewave ~/logseq-plugins/logseq-slatewave
   ```

2. In Logseq, open **⋯ → Plugins → Load unpacked plugin** and select the cloned folder.
3. Open **Settings → Themes** and pick **Slatewave Dark**.

---

## Palette

Slatewave shares its palette with the companion themes. The anchor colors:

| | Hex | Tailwind | Role |
|---|---|---|---|
| ![#282c34](https://placehold.co/20x20/282c34/282c34.png) | `#282c34` | — | editor background |
| ![#21252b](https://placehold.co/20x20/21252b/21252b.png) | `#21252b` | — | sidebars, header |
| ![#1e293b](https://placehold.co/20x20/1e293b/1e293b.png) | `#1e293b` | slate-800 | code blocks, modals |
| ![#334155](https://placehold.co/20x20/334155/334155.png) | `#334155` | slate-700 | borders, dividers |
| ![#e2e8f0](https://placehold.co/20x20/e2e8f0/e2e8f0.png) | `#e2e8f0` | slate-200 | body text |
| ![#5eead4](https://placehold.co/20x20/5eead4/5eead4.png) | `#5eead4` | teal-300 | **primary accent** — headings, cursor, active state |
| ![#99f6e4](https://placehold.co/20x20/99f6e4/99f6e4.png) | `#99f6e4` | teal-200 | hover accent, H4 |
| ![#7dd3fc](https://placehold.co/20x20/7dd3fc/7dd3fc.png) | `#7dd3fc` | sky-300 | H5, block refs, functions |
| ![#38bdf8](https://placehold.co/20x20/38bdf8/38bdf8.png) | `#38bdf8` | sky-400 | external links, keywords |
| ![#b388ff](https://placehold.co/20x20/b388ff/b388ff.png) | `#b388ff` | — | H6, decorators |
| ![#fb7185](https://placehold.co/20x20/fb7185/fb7185.png) | `#fb7185` | rose-400 | **bullets**, unresolved refs, TODO |
| ![#fbbf24](https://placehold.co/20x20/fbbf24/fbbf24.png) | `#fbbf24` | amber-400 | DOING, highlights |

See the [VSCode theme README](https://github.com/kevinlangleyjr/vscode-slatewave#palette) for the full scale and syntax mapping.

---

## Customize

Slatewave is a single CSS file built around CSS custom properties. To override a variable without forking, drop rules into Logseq's `custom.css` (open your graph folder → `logseq/custom.css`):

```css
:root {
  --ls-active-primary-color: #34d399;  /* swap teal for emerald */
  --ls-block-bullet-color: #fbbf24;    /* amber bullets instead of pink */
}
```

`custom.css` loads after the theme, so your overrides win.

---

## Companion themes

Slatewave is one palette, four surfaces. Run them together and your editor, terminal, notes, and outliner speak the same visual language.

- **Editor** — [vscode-slatewave](https://github.com/kevinlangleyjr/vscode-slatewave)
- **Prompt** — [slatewave-omp](https://github.com/kevinlangleyjr/slatewave-omp)
- **Notes (Obsidian)** — [obsidian-slatewave](https://github.com/kevinlangleyjr/obsidian-slatewave)
- **Outliner (Logseq)** — this repo

---

## Contributing

Issues and PRs welcome. For palette changes, include a before/after screenshot of the same graph so the visual tradeoff is obvious.

---

## License

WTFPL — Do What The Fuck You Want To Public License. See [LICENSE](LICENSE).
