# 🇩🇪 Viaje Berlín — 24, 25, 26 y 27 Abril 2026

**Guía de viaje interactiva** — 4 días en Berlín para 5 viajeros.
Mayte, Sílvia, Xavi, Victor y Biel.

## 🔗 Acceso directo

👉 **[Abrir la guía](https://victorvqg.github.io/viaje-abril-2026-BERLIN/)**

## 📱 Cómo usar

1. Abre el enlace en el móvil
2. **iPhone:** Compartir → "Añadir a pantalla de inicio"
3. Se comporta como una app — funciona offline

## 🎨 Design System

**"The Nocturnal Concierge"** — Tonal layering, glassmorphism, ambient glow.
Ver `.claude/skills/nocturnal-concierge.md` para especificaciones completas.

## 📂 Estructura

```
viaje-abril-2026-BERLIN/
├── index.html                          ← La guía (single-file PWA)
├── sw.js                               ← Service Worker (cache v6)
├── manifest.json                       ← PWA manifest
├── .nojekyll                           ← GitHub Pages config
├── CLAUDE.md                           ← Instrucciones para Claude Code
├── .claude/skills/
│   ├── nocturnal-concierge.md          ← Design system completo
│   ├── visual-improvements.md          ← Técnicas avanzadas CSS
│   ├── berlin-itinerary.md             ← Contenido y datos del viaje
│   └── pwa-deployment.md              ← PWA + deploy
├── .vscode/settings.json               ← Config VS Code
└── README.md
```

## 🚀 Dev local

```bash
# Servir
python3 -m http.server 8080
# o con Live Server en VS Code

# Deploy
git add . && git commit -m "v6.x" && git push
```

## ✅ Antes de cada deploy

1. Verificar que `sw.js` tiene CACHE_NAME bumpeado
2. Zero `border: 1px solid` en el CSS
3. Todos los tap targets ≥ 44px
4. JetBrains Mono en números y timestamps

---
Creado por Xavi Camins y Victor Quintana & CO.
