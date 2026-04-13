# Viaje Berlín — Abril 2026

## Proyecto
PWA single-file (index.html) — guía de viaje interactiva para 5 personas.
Repo GitHub Pages: `https://victorvqg.github.io/viaje-abril-2026-BERLIN/`

## Stack
- HTML + CSS + JS vanilla (todo en index.html)
- PWA: manifest.json + sw.js
- GitHub Pages (main branch, root)
- Fonts: Google Fonts (Sora, Plus Jakarta Sans, JetBrains Mono)

## Viaje
- **Destino:** Berlín, 24-27 Abril 2026
- **Grupo:** Mayte, Sílvia, Xavi, Victor y Biel (4 adultos + 1 niño 12 años)
- **Hotel:** Mercure Hotel & Residenz Checkpoint Charlie, Schützenstraße 11, 10117 Berlin-Mitte
- **Metro base:** U Kochstraße (U6), 3 min a pie

## Design System: The Nocturnal Concierge

### Tokens de color (dark mode)
| Token | Valor | Uso |
|-------|-------|-----|
| `--floor` | `#0B0E14` | Body background, capa más profunda |
| `--surface` | `#10131A` | Cards, bloques |
| `--section` | `#191C22` | Secciones, badge backgrounds |
| `--interact` | `#32353C` | Elementos interactivos, hover |
| `--accent` | `#FF3D5A` | Coral Pulse — acciones, CTAs |
| `--blue` | `#4B9EFF` | Info, transporte, links Maps |
| `--green` | `#10B981` | Éxito, consejos, walking |
| `--orange` | `#F59E0B` | Warnings, uber |
| `--text` | `#E1E2EB` | Texto principal |
| `--dim` | `#8B8FA0` | Texto secundario |
| `--dim2` | `#5A5E6E` | Texto terciario |

### Reglas ESTRICTAS
1. **No-Line Rule:** PROHIBIDO `border: 1px solid` para separar secciones. Usar tonal shifts entre surface tokens.
2. **Bordes decorativos:** Solo `2px solid` con tokens de alta opacidad (`--card-border`, `--loc-border`).
3. **Glassmorphism:** Tabs y botón share: `backdrop-filter: blur(24px)` + 60% opacidad.
4. **Radios:** Cards `32px`, nested `20px`, pills `100px`.
5. **Sombras:** NUNCA negras. Usar `--glow: 0 0 40px rgba(225,226,235,.06)`.
6. **Nav indicator:** Punto coral 6px debajo del tab activo. NO icono relleno.
7. **Spacing entre bloques:** `2.75rem` (spacing-8).
8. **Tap targets:** Mínimo `44x44px`.
9. **Micro-interacciones:** `transform: scale(.96-.98)` en `:active`.

### Tipografía
| Nivel | Font | Size | Weight | Uso |
|-------|------|------|--------|-----|
| Display | Sora | 3.5rem | Black (800) | Hero H1 |
| Headline | Sora | 1.75rem | Bold (700) | Day headers H2 |
| Body | Plus Jakarta Sans | 1rem/18px | Regular (400) | Texto corriente |
| Metadata | JetBrains Mono | 0.75rem | Medium (500) | Horas, precios, direcciones |

## Estructura de pestañas (6)
| # | Tab | Panel ID | Contenido |
|---|-----|----------|-----------|
| 0 | 🏠 | phome | Índice visual del viaje |
| 1 | VIE | p0 | Día 1: Llegada |
| 2 | SÁB | p1 | Día 2: Historia + Vibe |
| 3 | DOM | p2 | Día 3: Ciencia + Río |
| 4 | LUN | p3 | Día 4: Despedida |
| 5 | 🏨 | p4 | Hotel + detalles (amenities, desayuno, habs) |

Cada `.blk` de los días VIE-LUN incluye su propia guía detallada (`guide-txt`, `guide-tags`, `guide-tip`) + link web oficial (`bmap sm` verde). Los pins globales y la guía separada fueron consolidados dentro de cada bloque del día.

## Convenciones de código
- CSS inline en `<style>` dentro del HTML (single-file PWA)
- Variables CSS en `:root` (dark) y `[data-theme="light"]`
- JS vanilla al final del `<body>`
- Idioma contenido: **español** (con toques catalanes en nombres)
- Bloques accordion: `class="blk"`, toggle con `tog(id)`
- Map buttons: `class="bmap"` con Google Maps URLs

## Service Worker
- Cache name: `berlin-mission-v28` (IMPORTANTE: bumpar al modificar)
- Si cambias index.html, bumpar el CACHE_NAME en sw.js

## Comandos útiles
```bash
# Validar HTML
npx html-validate index.html

# Servir local
python3 -m http.server 8080

# Deploy
git add . && git commit -m "v6.x — descripción" && git push
```
