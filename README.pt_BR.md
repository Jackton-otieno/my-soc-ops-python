<!-- l10n-sync: source-file="README.md" -->
🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

# 🎯 Soc Ops — Bingo Social

> **Quebre o gelo, faça conexões, vença no networking!**

Soc Ops é um jogo interativo de bingo social projetado para encontros presenciais, eventos de equipe e conferências. Encontre pessoas que correspondam às perguntas, marque seu cartão e corra para conseguir 5 em linha!

![Python](https://img.shields.io/badge/Python-3.13+-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-0.115+-009688?logo=fastapi&logoColor=white)
![HTMX](https://img.shields.io/badge/HTMX-powered-36C?logo=htmx&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

---

## ✨ Funcionalidades

- 🎲 **Cartões aleatórios** — Cada jogador recebe uma disposição única
- 💾 **Salvamento automático** — Continue exatamente de onde parou
- 🏆 **Detecção de bingo** — Detecção automática de linhas, colunas e diagonais
- 🎉 **Modal de celebração** — Tela de vitória digna de confete
- 📱 **Mobile-first** — Funciona perfeitamente em celulares durante eventos

---

## 🚀 Início Rápido

### Pré-requisitos
- [Python 3.13+](https://www.python.org/downloads/)
- [uv](https://docs.astral.sh/uv/) (gerenciador de pacotes Python)

### Executar Localmente
```bash
uv sync
uv run uvicorn app.main:app --reload --port 8000
# Abra http://localhost:8000
```

### Testes
```bash
uv run pytest
```

### Lint
```bash
uv run ruff check .
```

---

## 🎨 Personalize seu Jogo

### Alterar Perguntas
Edite `app/data.py` para adicionar suas próprias perguntas de apresentação:
```python
QUESTIONS: list[str] = [
    "tem um animal de estimação",
    "fala mais de 2 idiomas",
    "sua pergunta personalizada aqui",
    # ... 24+ perguntas para um cartão completo 5×5
]
```

---

## 🛠️ Stack Tecnológico

| Camada | Tecnologia |
|--------|-----------|
| **Framework** | FastAPI + Jinja2 |
| **Interatividade** | HTMX |
| **Estilos** | Utilitários CSS personalizados (inspirados no Tailwind) |
| **Estado** | Sessões no servidor com persistência em cookies |

---

## 📁 Estrutura do Projeto

```
app/
├── templates/           # Templates Jinja2
│   ├── base.html
│   ├── home.html
│   └── components/      # bingo_board, bingo_modal, game_screen, start_screen
├── static/              # Recursos CSS e JS
├── models.py            # Modelos de estado do jogo (GameState)
├── game_logic.py        # Detecção de bingo e geração do tabuleiro
├── game_service.py      # Gerenciamento de sessões
├── data.py              # Banco de perguntas
└── main.py              # Rotas FastAPI
tests/
├── test_api.py          # Testes de endpoints da API
└── test_game_logic.py   # Testes unitários da lógica do jogo
workshop/                # Guias do laboratório passo a passo
```

---

## 📚 Guia do Lab

Este repositório também é um workshop prático para desenvolver com o **GitHub Copilot Agent Mode** no VS Code.

| Parte | Título | Tempo |
|-------|--------|-------|
| [**00**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) | Visão Geral & Lista de Verificação | — |
| [**01**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=01-setup) | Configuração & Engenharia de Contexto | 15 min |
| [**02**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=02-design) | Frontend Design-First | 15 min |
| [**03**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=03-quiz-master) | Quiz Master Personalizado | 10 min |
| [**04**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=04-multi-agent) | Desenvolvimento Multi-Agente | 20 min |

> 📝 Os guias do lab também estão disponíveis na pasta [`workshop/`](workshop/) para leitura offline.

👉 Comece aqui: **[Parte 00: Visão Geral & Lista de Verificação](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview)**

---

## 🚢 Implantação

O app é implantado automaticamente no GitHub Pages a cada push na branch `main`:

```
https://{usuario}.github.io/{nome-repo}
```

---

## 📝 Licença

[MIT](LICENSE) — use livremente para seu próximo evento!
