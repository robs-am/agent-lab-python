# Project Guidelines

## Mandatory Development Checklist
Complete before finishing any change:

- [ ] Lint: `uv run ruff check .`
- [ ] Build/Setup: `uv sync`
- [ ] Test: `uv run pytest`

## Architecture
Soc Ops is a FastAPI + Jinja2 + HTMX social bingo app.

- `app/main.py`: thin routes + template rendering
- `app/game_service.py`: session state transitions
- `app/game_logic.py`: pure bingo rules/board logic
- `app/models.py`: immutable Pydantic models/enums
- `app/templates/components/`: HTMX partials

Keep boundaries strict:

- Keep rules in `app/game_logic.py`, state transitions in `app/game_service.py`, and routes thin in `app/main.py`.

## HTMX and Template Conventions
- Return component partials for HTMX actions (`start`, `toggle`, `reset`, `dismiss-modal`).
- Keep `#game-container` as the primary swap target unless restructuring is required.

## Styling Conventions
- Reuse utilities in `app/static/css/app.css`; add new ones in the same style.
- Do not introduce external CSS frameworks.
- Details: `.github/instructions/css-utilities.instructions.md`.

## Testing and Quality
- Game rules: update `tests/test_game_logic.py`.
- Routes/rendering: update `tests/test_api.py`.
- Keep Ruff/pytest conventions from `pyproject.toml`.

## Pitfalls
- Do not use VS Code Simple Browser.
- In browser Codespaces, set port 8000 visibility to Public if HTMX/CSS fails.
- Sessions are in-memory (`_sessions` in `app/game_service.py`) and reset on process restart.

## Docs Map (Link, Do Not Duplicate)
- Project overview: `README.md`
- Workshop guide: `workshop/GUIDE.md`
- Setup/environment gotchas: `workshop/01-setup.md`
- Frontend guidance: `.github/instructions/frontend-design.instructions.md`
