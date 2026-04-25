<!-- README redesigned: Candy Pop, Toybox Primary Colors, Anime Bubble style -->

<p align="right">
    <a href="README.pt_BR.md">🇧🇷 Português (BR)</a> | <a href="README.es.md">Español</a>
</p>


<p align="center" style="font-size:2rem;">🍭🍬🧸✨🍭🍬🧸✨🍭🍬🧸✨</p>

## 🛠️ Tech Stack

| 🍬 Layer | 🧸 Technology |
|----------|--------------|
| <b>Framework</b> | FastAPI + Jinja2 |
| <b>Interactivity</b> | HTMX |
| <b>Styling</b> | Custom CSS utilities (Tailwind-inspired) |
| <b>State</b> | Server-side sessions with cookie persistence |

<p align="center" style="font-size:2rem;">🍭🍬🧸✨🍭🍬🧸✨🍭🍬🧸✨</p>

## 📁 Project Structure

<pre style="background:#ffe4fa; color:#ff69b4; border-radius:12px; padding:8px;">
app/
├── templates/           # Jinja2 templates
│   ├── base.html
│   ├── home.html
│   └── components/      # bingo_board, bingo_modal, game_screen, start_screen
├── static/              # CSS & JS assets
├── models.py            # Game state models
├── game_logic.py        # Bingo detection & board generation
├── game_service.py      # Session management
├── data.py              # Question bank
└── main.py              # FastAPI routes

├── test_api.py          # API endpoint tests
└── test_game_logic.py   # Game logic unit tests
workshop/                # Step-by-step lab guides
</pre>

<p align="center" style="font-size:2rem;">🍭🍬🧸✨🍭🍬🧸✨🍭🍬🧸✨</p>

## 📚 Lab Guide

<blockquote>
    <b>📝 This repo is also a hands-on workshop for building with <span style="color:#ff69b4;">GitHub Copilot Agent Mode</span> in VS Code!</b>
</blockquote>

| 🍬 Part | 🧸 Title | ⏱️ Time |
|---------|---------|---------|
| [<b>00</b>](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) | Overview & Checklist | — |
| [<b>01</b>](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=01-setup) | Setup & Context Engineering | 15 min |
| [<b>02</b>](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=02-design) | Design-First Frontend | 15 min |
| [<b>03</b>](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=03-quiz-master) | Custom Quiz Master | 10 min |
| [<b>04</b>](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=04-multi-agent) | Multi-Agent Development | 20 min |

> 🍬 Lab guides are also available in the [`workshop/`](workshop/) folder for offline reading.

👉 <b>Start here:</b> [Part 00: Overview & Checklist](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview)

<p align="center" style="font-size:2rem;">🍭🍬🧸✨🍭🍬🧸✨🍭🍬🧸✨</p>

## 🚢 Deployment

<details>
<summary><b>✨ How to Deploy</b></summary>

The app automatically deploys to GitHub Pages on push to <code>main</code>:

```text
https://{username}.github.io/{repo-name}
```
</details>

<p align="center" style="font-size:2rem;">🍭🍬🧸✨🍭🍬🧸✨🍭🍬🧸✨</p>

## 📝 License

<span style="background:#ffe4fa; color:#ff69b4; border-radius:8px; padding:2px 8px;">[MIT](LICENSE) — use it freely for your next event!</span>
```bash
uv run pytest
```
</details>

<details>
<summary><b>🎉 Lint</b></summary>

```bash
uv run ruff check .
```
</details>

<p align="center" style="font-size:2rem;">🍭🍬🧸✨🍭🍬🧸✨🍭🍬🧸✨</p>

## 🎨 Customize Your Game

<details>
<summary><b>🍭 Change Questions</b></summary>

Edit <code>app/data.py</code> to add your own icebreaker prompts:

```python
QUESTIONS: list[str] = [
        "has a pet",
        "speaks more than 2 languages",
        "your custom question here",
        # ... 24+ questions for a full 5×5 board
]
]
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Framework** | FastAPI + Jinja2 |
| **Interactivity** | HTMX |
| **Styling** | Custom CSS utilities (Tailwind-inspired) |
| **State** | Server-side sessions with cookie persistence |

---

## 📁 Project Structure

```
app/
├── templates/           # Jinja2 templates
│   ├── base.html
│   ├── home.html
│   └── components/      # bingo_board, bingo_modal, game_screen, start_screen
├── static/              # CSS & JS assets
├── models.py            # Game state models
├── game_logic.py        # Bingo detection & board generation
├── game_service.py      # Session management
├── data.py              # Question bank
└── main.py              # FastAPI routes
tests/
├── test_api.py          # API endpoint tests
└── test_game_logic.py   # Game logic unit tests
workshop/                # Step-by-step lab guides
```

---

## 📚 Lab Guide

This repo is also a hands-on workshop for building with **GitHub Copilot Agent Mode** in VS Code.

| Part | Title | Time |
|------|-------|------|
| [**00**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) | Overview & Checklist | — |
| [**01**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=01-setup) | Setup & Context Engineering | 15 min |
| [**02**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=02-design) | Design-First Frontend | 15 min |
| [**03**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=03-quiz-master) | Custom Quiz Master | 10 min |
| [**04**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=04-multi-agent) | Multi-Agent Development | 20 min |

> 📝 Lab guides are also available in the [`workshop/`](workshop/) folder for offline reading.

👉 Start here: **[Part 00: Overview & Checklist](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview)**

---

## 🚢 Deployment

The app automatically deploys to GitHub Pages on push to `main`:

```
https://{username}.github.io/{repo-name}
```

---

## 📝 License

[MIT](LICENSE) — use it freely for your next event!
