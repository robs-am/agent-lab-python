<!-- l10n-sync: source-file="README.md" -->
# Soc Ops

Jogo de Bingo Social para encontros presenciais. Encontre pessoas que correspondam às perguntas e consiga 5 em linha!

🎮 **[Jogar](https://copilot-dev-days.github.io/agent-lab-python/)** • 📚 **[Ver Guia do Lab](https://copilot-dev-days.github.io/agent-lab-python/docs/)**

---

## 📚 Guia do Lab

| Parte | Título |
|-------|--------|
| [**00**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) | Visão Geral & Lista de Verificação |
| [**01**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=01-setup) | Configuração & Engenharia de Contexto |
| [**02**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=02-design) | Frontend Design-First |
| [**03**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=03-quiz-master) | Quiz Master Personalizado |
| [**04**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=04-multi-agent) | Desenvolvimento Multi-Agente |

> 📝 Os guias do lab também estão disponíveis na pasta [`workshop/pt_BR/`](workshop/pt_BR/) para leitura offline.

---

## Pré-requisitos

- [Python 3.13](https://www.python.org/downloads/) ou superior
- [uv](https://docs.astral.sh/uv/) gerenciador de pacotes

## Configuração

```bash
uv sync
```

## Executar

```bash
uv run uvicorn app.main:app --reload
```

Depois abra http://localhost:8000 no seu navegador.

## Testes

```bash
uv run pytest
```

## Lint

```bash
uv run ruff check .
uv run ruff format .
```

Deploys automáticos para GitHub Pages a cada push no `main`.
