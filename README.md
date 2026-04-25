🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

# Soc Ops

Social bingo for in-person mixers, team offsites, workshops, and community events.

Find people who match the prompts, mark the board, and race to 5 in a row.

This repository is also a hands-on GitHub Copilot agent lab: you can use it as a working FastAPI app, or as a guided workshop for prompt design, multi-agent workflows, UI iteration, and test-driven changes.

## Why This Project

- Lightweight social game with a fast feedback loop
- Small Python codebase that is easy to understand and modify
- Practical workshop for building with GitHub Copilot in VS Code
- Good demo surface for UI, prompts, testing, and agent-assisted refactors

## What You Can Do Here

- Run the social bingo app locally with FastAPI
- Redesign the interface and interaction flow
- Customize the bingo prompts for different events or teams
- Practice agent workflows for design, planning, TDD, and review
- Use the workshop materials online or offline

---

## Quick Start

```bash
uv sync
uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

Open `http://127.0.0.1:8000` after the server starts.

Quality checks:

```bash
uv run ruff check .
uv run pytest
```

## Project At A Glance

| Area | Details |
|------|---------|
| App | FastAPI + Jinja2 + HTMX social bingo game |
| Language | Python 3.13 |
| Goal | Ship features quickly while practicing AI-assisted development |
| Best for | Workshops, demos, team exercises, and Copilot labs |
| Entry point | `app/main.py` |

## 📚 Lab Guide

| Part | Title |
|------|-------|
| [**00**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) | Overview & Checklist |
| [**01**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=01-setup) | Setup & Context Engineering |
| [**02**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=02-design) | Design-First Frontend |
| [**03**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=03-quiz-master) | Custom Quiz Master |
| [**04**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=04-multi-agent) | Multi-Agent Development |

> 📝 Lab guides are also available in the [`workshop/`](workshop/) folder for offline reading.

---

## Workshop Path

Head to **[Part 00: Overview](https://copilot-dev-days.github.io/agent-lab-python/step.html?step=00-overview)** for prerequisites and setup instructions.

Suggested flow:

1. Read Part 00 to get the environment ready.
2. Start with Part 01 to set up prompt and workspace context.
3. Use Part 02 to push the UI beyond the default starter state.
4. Continue with Parts 03 and 04 for custom agents and multi-agent workflows.

## Tech Stack

- FastAPI for routing and server rendering
- Jinja2 templates for HTML composition
- HTMX for lightweight interactivity
- Ruff for linting
- Pytest for tests
- uv for environment and command management

## Repository Map

| Path | Purpose |
|------|---------|
| `app/main.py` | FastAPI routes and template rendering |
| `app/game_service.py` | Session and game state transitions |
| `app/game_logic.py` | Pure bingo rules and board logic |
| `app/models.py` | Pydantic models and enums |
| `app/templates/` | Jinja2 pages and HTMX partials |
| `app/static/` | CSS and JS assets |
| `tests/` | API and game logic tests |
| `workshop/` | Offline lab instructions |

## Good First Customizations

- Swap the bingo prompt set for your event or team culture
- Redesign the board and start screen
- Add a new game mode or win condition
- Tighten linting and typing rules
- Extend the workshop with your own agent prompts

## Learn More

- [Workshop quick guide](workshop/GUIDE.md)
- [Online lab docs](https://copilot-dev-days.github.io/agent-lab-python/docs/)
- [FastAPI documentation](https://fastapi.tiangolo.com/)
- [HTMX documentation](https://htmx.org/docs/)
