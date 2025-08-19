# TestGameCI_DevOps

# 🎮 Unity CI/CD Templates (GameCI + GitHub Actions)

Este repositorio contiene **workflows reutilizables y parametrizables** para automatizar procesos de integración y despliegue en proyectos Unity, aprovechando GameCI, GitHub Actions y herramientas externas como Discord e Itch.io.

> 🧠 **Objetivo:** Centralizar y estandarizar la automatización de builds Unity (WebGL y Windows) entre múltiples repositorios, facilitando su mantenimiento y configuración.

---

## 🚀 ¿Qué ofrece este repositorio?

- Workflows listos para compilar proyectos Unity en WebGL y Windows.
- Publicación opcional de WebGL directamente en [Itch.io](https://itch.io/).
- Notificaciones automáticas en [Discord](https://discord.com/) (también opcionales).
- Métricas de build en resumen Markdown y JSON (tamaño, duración, versión, etc.).
- Versionado automático inteligente (`UnityVersion + GitHub Run + Entorno`).
- Separación por entorno: `DES`, `PRE`, `PRO` (controlado por parámetro).
- Reutilización a través de `workflow_call` para mantener consistencia entre proyectos.

---

## 🗂️ Estructura del repositorio

```txt
unity-ci-templates/
├── .github/
│   └── workflows/
│       ├── build-core.yml         # 🧠 Workflow genérico, configurable por inputs
│       ├── build-webgl.yml        # 🎯 Alias para compilar WebGL
│       ├── build-windows.yml      # 💻 Alias para compilar StandaloneWindows64
│       ├── notify-discord.yml     # 🔔 (Opcional) Subworkflow para enviar mensajes a Discord
│       └── publish-itchio.yml     # 🌐 (Opcional) Subworkflow para publicar a Itch.io
└── README.md                      # 📘 Este archivo
