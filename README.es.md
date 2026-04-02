<!-- l10n-sync: source-file="README.md" -->
# Soc Ops

Juego de Bingo Social para encuentros presenciales. ¡Encuentra personas que coincidan con las preguntas y consigue 5 en línea!

🎮 **[Jugar](https://copilot-dev-days.github.io/agent-lab-python/)** • 📚 **[Ver Guía del Lab](https://copilot-dev-days.github.io/agent-lab-python/docs/)**

---

## 📚 Guía del Lab

| Parte | Título |
|-------|--------|
| [**00**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) | Descripción General & Lista de Verificación |
| [**01**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=01-setup) | Configuración & Ingeniería de Contexto |
| [**02**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=02-design) | Frontend Design-First |
| [**03**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=03-quiz-master) | Quiz Master Personalizado |
| [**04**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=04-multi-agent) | Desarrollo Multi-Agente |

> 📝 Las guías del lab también están disponibles en la carpeta [`workshop/es/`](workshop/es/) para lectura offline.

---

## Requisitos Previos

- [Python 3.13](https://www.python.org/downloads/) o superior
- [uv](https://docs.astral.sh/uv/) gestor de paquetes

## Configuración

```bash
uv sync
```

## Ejecutar

```bash
uv run uvicorn app.main:app --reload
```

Luego abre http://localhost:8000 en tu navegador.

## Pruebas

```bash
uv run pytest
```

## Lint

```bash
uv run ruff check .
uv run ruff format .
```

Se despliega automáticamente a GitHub Pages con cada push a `main`.
