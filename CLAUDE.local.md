# Mockups Builder — Contexto del Proyecto

## Descripción
Herramienta web SPA (Single Page Application) para crear mockups de interfaces durante tomas de requerimiento. Desarrollada por andyjara.dev.

## Arquitectura
- **Un solo archivo**: `index.html` con CSS y JS embebidos, sin frameworks ni build step.
- **Persistencia**: `localStorage` con clave `mockups_data_v1`.
- **Exportación PNG**: usa `html2canvas` desde CDN.
- **Docker**: nginx:alpine sirviendo el archivo estático en puerto `9005`.

## Estructura de datos (localStorage)
```
projects[]
  └── groups[]
        └── mockups[]
              └── elements[]  ← widgets del canvas
```

## Paleta de colores (cloudops.andyjara.dev)
```css
--bg-main: #0d1117        /* fondo general */
--bg-sidebar: #131a2e     /* sidebar */
--bg-card: #1a2540        /* cards y paneles */
--accent: #29b6d8         /* cyan/teal principal */
--text-primary: #e2e8f0
--text-muted: #8b9ab0
--border: #1e2d45
```

## Widgets disponibles
`text`, `label`, `input`, `textarea`, `button`, `select`, `checkbox`, `radio`, `image`, `rectangle`, `navbar`, `card`, `separator`

## Despliegue
```bash
git pull
docker compose up -d --build
# Acceso: http://servidor:9005
```

## Repositorio
`git@github.com:andyjara-dev/mockups.git` — branch `main`

## Convenciones
- No usar frameworks externos (vanilla JS únicamente).
- Todo en `index.html` — no crear archivos JS/CSS separados.
- Marca de agua en PNG: `mockups by andyjara.dev` (esquina inferior derecha).
- Footer: `Creado por andyjara.dev — Licencia CC BY`.
- Seguir paleta de cloudops.andyjara.dev para cualquier cambio visual.
