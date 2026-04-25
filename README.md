🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

# 🎯 Soc Ops — Social Bingo

> **Break the ice, make connections, win at networking!**

Soc Ops is an interactive social bingo game designed for in-person mixers, team events, and conferences. Find people who match the prompts, mark your card, and race to get 5 in a row!

![Python](https://img.shields.io/badge/Python-3.13+-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-0.115+-009688?logo=fastapi&logoColor=white)
![HTMX](https://img.shields.io/badge/HTMX-powered-36C?logo=htmx&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

---

## ✨ Features

- 🎲 **Randomized boards** — Every player gets a unique card arrangement
- 💾 **Auto-save progress** — Pick up exactly where you left off
- 🏆 **Bingo detection** — Automatic win detection for rows, columns, and diagonals
- 🎉 **Celebration modal** — Confetti-worthy victory screen
- 📱 **Mobile-first** — Works great on phones at live events

---

## 🚀 Quick Start

### Prerequisites
- [Python 3.13+](https://www.python.org/downloads/)
- [uv](https://docs.astral.sh/uv/) (Python package manager)

### Run Locally
```bash
uv sync
uv run uvicorn app.main:app --reload --port 8000
# Open http://localhost:8000
```

### Test
```bash
uv run pytest
```

### Lint
```bash
uv run ruff check .
```

---

## 🎨 Customize Your Game

### Change Questions
Edit `app/data.py` to add your own icebreaker prompts:
```python
QUESTIONS: list[str] = [
    "has a pet",
    "speaks more than 2 languages",
    "your custom question here",
    # ... 24+ questions for a full 5×5 board
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
