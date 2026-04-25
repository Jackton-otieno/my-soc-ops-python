# Copilot Workspace Instructions

## Development Checklist

Before committing any changes, ensure:

- [ ] `uv run ruff check .` passes with no errors
- [ ] `uv run pytest` passes
- [ ] Code follows Python conventions (snake_case, type hints)
- [ ] No unused variables or imports

## Project Overview

**Soc Ops** is a Social Bingo game built with Python (FastAPI + Jinja2 + HTMX). Players find people who match questions to mark squares and get 5 in a row.

## Architecture

```
app/
├── templates/       # Jinja2 HTML templates
│   ├── base.html
│   ├── home.html
│   └── components/  # bingo_board, bingo_modal, game_screen, start_screen
├── static/          # CSS & JS assets
├── models.py        # Pydantic models (GameState, BingoSquare)
├── game_logic.py    # Board generation & bingo detection
├── game_service.py  # Session management (GameSession)
├── data.py          # Question bank
└── main.py          # FastAPI routes & HTMX endpoints
tests/
├── test_api.py      # API endpoint tests (httpx + TestClient)
└── test_game_logic.py  # Game logic unit tests
```

## Key Commands

```bash
uv run uvicorn app.main:app --reload --port 8000  # Run dev server
uv run pytest                                       # Run tests
uv run ruff check .                                 # Lint
```

## Styling

Uses custom CSS utility classes (Tailwind-like) in `app/static/css/app.css`:

- Layout: `.flex`, `.grid`, `.items-center`
- Spacing: `.p-4`, `.mb-2`, `.mx-auto`
- Colors: `.bg-accent`, `.bg-marked`, `.text-gray-700`

## Design Guide: Playful Candy Pop Aesthetic

**Goal:** Make every user touchpoint (README, UI, docs) feel fun, energetic, and memorable—like a toybox or anime bubble world.

### Visual Identity

- Use bright, saturated primary colors (pink, blue, yellow, green, purple)
- Prefer round, bubbly shapes and soft edges in UI and visuals
- Add playful banners, emoji dividers, and ASCII art to docs and landing pages

### Typography & Icons

- Use bold, friendly fonts (in code: prefer large, rounded headings)
- Sprinkle emojis liberally in section headers, lists, and callouts
- Use badges with playful text and color (e.g., “🍬 Candy-Ready”, “🧸 Toybox Fun”)

### Layout & Effects

- Use creative section dividers: emoji lines (🍭🍬🧸✨), dotted/dashed HTML `<hr>`, or ASCII art
- Add blockquote callouts for tips, fun facts, or warnings (with emoji)
- Use collapsible `<details>` for FAQs, spoilers, or bonus content

### Color & Theming

- Use HTML `<span>` for color highlights in markdown (e.g., `<span style="background:#ffe4fa; color:#ff69b4;">Candy Pop!</span>`)
- Stick to a consistent, energetic palette throughout

### Accessibility

- Always provide alt text for images and banners
- Ensure color contrast is readable and not the only means of conveying info

### README/Docs Example

See the main `README.md` for a full playful, candy pop redesign example.

**Remember:**

- Prioritize fun and clarity—never sacrifice readability for style
- Test rendering on GitHub and in the app for visual consistency
