# 🇩🇪 Misión Berlín 2026

**Guía de viaje interactiva** — 3 días en Berlín para 5 viajeros (4 adultos + 1 teen).  
Navegación paso a paso desde Mercure Hotel & Residenz, Checkpoint Charlie.

## 🔗 Acceso directo

👉 **[Abrir la guía](https://<TU-USUARIO>.github.io/berlin-mission-guide/)**

> Sustituye `<TU-USUARIO>` por tu usuario de GitHub una vez desplegado.

## 📱 Cómo usar

1. **Abre el enlace** en el móvil (Safari / Chrome)
2. **Añade a pantalla de inicio:**
   - **iPhone:** Compartir → "Añadir a pantalla de inicio"
   - **Android:** Menú ⋮ → "Añadir a pantalla de inicio"
3. **Se comporta como una app** — funciona offline después de la primera carga
4. **Comparte con el grupo:** Pulsa el botón 📤 en la esquina inferior izquierda

## ✅ Funcionalidades

| Feature | Detalle |
|---------|---------|
| 📍 Google Maps | Cada trayecto tiene enlace directo que abre Maps con la ruta |
| 🌙/☀️ Tema | Oscuro por defecto, cambia con el botón flotante |
| 📡 Offline | Service Worker cachea todo. Funciona sin conexión |
| 📤 Compartir | Web Share API (iOS/Android) o copia al portapapeles |
| 🎯 Misiones Teen | Retos interactivos en cada parada |
| 🏷️ Categorías | Badges de color: MUSEO, RESTAURANTE, HOTEL, VUELO, etc. |
| 🚇/👟/🚕 Transporte | Opciones alternativas claramente diferenciadas |
| 🔵 Salidas metro | Badges teal con la salida exacta de cada estación |

## 📂 Estructura del repo

```
berlin-mission-guide/
├── index.html      ← La guía completa (todo en 1 archivo)
├── manifest.json   ← PWA manifest para instalar como app
├── sw.js           ← Service Worker para offline
├── .nojekyll       ← Indica a GitHub Pages que no use Jekyll
└── README.md       ← Este archivo
```

## 🚀 Desplegar en GitHub Pages

### Opción A: Desde la web de GitHub (más fácil)

1. Crea un repositorio nuevo en GitHub: `berlin-mission-guide`
2. Sube los 4 archivos (`index.html`, `manifest.json`, `sw.js`, `.nojekyll`)
3. Ve a **Settings → Pages → Source → Deploy from branch → `main` → `/ (root)`**
4. Espera 1-2 minutos. La URL será `https://<tu-usuario>.github.io/berlin-mission-guide/`

### Opción B: Desde terminal (Claude Code / Git)

```bash
cd berlin-mission-guide
git init
git add .
git commit -m "Misión Berlín V5 — guía completa"
git branch -M main
git remote add origin https://github.com/<TU-USUARIO>/berlin-mission-guide.git
git push -u origin main
```

Después activa GitHub Pages en Settings → Pages → `main` branch.

## 📋 Contenido del viaje

### Día 1 — Viernes: Llegada + Inmersión Nocturna
- ✈️ Llegada BER → 🏨 Check-in → 🍽️ Katz Orange → 🌙 Brandenburger Tor

### Día 2 — Sábado: Tecnología, Historia + Vibe
- 🏛️ Reichstag → ◼️ Memorial → 🕵️ Spy Museum → 🍽️ Markthalle Neun → 🎨 East Side Gallery → 🎮 Computerspielemuseum → 🛹 Boxhagener Platz → 🍽️🌅 Klunkerkranich

### Día 3 — Domingo: Futuro, Aventura + Despedida
- 🔮 Futurium → 🚲 Tempelhofer Feld → 🍽️ Burgermeister → 🏘️ DDR Museum → 🛍️ Hackescher Markt → 🛫 BER

## 📄 Licencia

Uso privado. Guía creada por Claude para Victor — LUCY Matrix.
