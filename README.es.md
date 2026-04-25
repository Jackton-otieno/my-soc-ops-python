<!-- l10n-sync: source-file="README.md" -->
🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

# 🎯 Soc Ops — Bingo Social

> **¡Rompe el hielo, crea conexiones, gana en el networking!**

Soc Ops es un juego interactivo de bingo social diseñado para encuentros presenciales, eventos de equipo y conferencias. ¡Encuentra personas que coincidan con las preguntas, marca tu cartón y corre a conseguir 5 en fila!

![Python](https://img.shields.io/badge/Python-3.13+-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-0.115+-009688?logo=fastapi&logoColor=white)
![HTMX](https://img.shields.io/badge/HTMX-powered-36C?logo=htmx&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

---

## ✨ Características

- 🎲 **Tableros aleatorios** — Cada jugador recibe una disposición única
- 💾 **Guardado automático** — Retoma exactamente donde lo dejaste
- 🏆 **Detección de bingo** — Detección automática de filas, columnas y diagonales
- 🎉 **Modal de celebración** — Pantalla de victoria digna de confeti
- 📱 **Mobile-first** — Funciona genial en teléfonos durante los eventos

---

## 🚀 Inicio Rápido

### Requisitos
- [Python 3.13+](https://www.python.org/downloads/)
- [uv](https://docs.astral.sh/uv/) (gestor de paquetes de Python)

### Ejecutar Localmente
```bash
uv sync
uv run uvicorn app.main:app --reload --port 8000
# Abre http://localhost:8000
```

### Pruebas
```bash
uv run pytest
```

### Lint
```bash
uv run ruff check .
```

---

## 🎨 Personaliza tu Juego

### Cambiar Preguntas
Edita `app/data.py` para agregar tus propias preguntas de presentación:
```python
QUESTIONS: list[str] = [
    "tiene una mascota",
    "habla más de 2 idiomas",
    "tu pregunta personalizada aquí",
    # ... 24+ preguntas para un tablero completo 5×5
]
```

---

## 🛠️ Stack Tecnológico

| Capa | Tecnología |
|------|-----------|
| **Framework** | FastAPI + Jinja2 |
| **Interactividad** | HTMX |
| **Estilos** | Utilidades CSS personalizadas (inspiradas en Tailwind) |
| **Estado** | Sesiones del servidor con persistencia en cookies |

---

## 📁 Estructura del Proyecto

```
app/
├── templates/           # Plantillas Jinja2
│   ├── base.html
│   ├── home.html
│   └── components/      # bingo_board, bingo_modal, game_screen, start_screen
├── static/              # Recursos CSS y JS
├── models.py            # Modelos de estado del juego (GameState)
├── game_logic.py        # Detección de bingo y generación del tablero
├── game_service.py      # Gestión de sesiones
├── data.py              # Banco de preguntas
└── main.py              # Rutas de FastAPI
tests/
├── test_api.py          # Tests de endpoints API
└── test_game_logic.py   # Tests unitarios de la lógica del juego
workshop/                # Guías del laboratorio paso a paso
```

---

## 📚 Guía del Laboratorio

Este repositorio también es un taller práctico para desarrollar con **GitHub Copilot Agent Mode** en VS Code.

| Parte | Título | Tiempo |
|-------|--------|--------|
| [**00**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) | Visión General y Lista de Verificación | — |
| [**01**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=01-setup) | Configuración y Context Engineering | 15 min |
| [**02**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=02-design) | Desarrollo Frontend Orientado al Diseño | 15 min |
| [**03**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=03-quiz-master) | Quiz Master Personalizado | 10 min |
| [**04**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=04-multi-agent) | Desarrollo Multi-Agente | 20 min |

> 📝 Las guías del laboratorio también están disponibles en la carpeta [`workshop/`](workshop/) para lectura sin conexión.

👉 Empieza aquí: **[Parte 00: Visión General y Lista de Verificación](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview)**

---

## 🚢 Despliegue

La aplicación se despliega automáticamente en GitHub Pages al hacer push a `main`:

```
https://{usuario}.github.io/{nombre-repo}
```

---

## 📝 Licencia

[MIT](LICENSE) — ¡úsalo libremente en tu próximo evento!
