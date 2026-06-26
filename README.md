# Ahora — Horario

App de horario diario. La abres y te dice **qué toca ahora mismo**, cuánto le queda y qué sigue. Sin decisiones: mirar y hacer.

## Archivos (van todos en la raíz del repo)

- `index.html` — la app
- `manifest.json` — la hace instalable
- `sw.js` — service worker (instalación real + funciona sin conexión)
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` — el ícono
- `horario.ics` — *(opcional)* eventos para Google Calendar, si quieres notificaciones entre bloques

## Subir a GitHub Pages

1. Repo nuevo, sube los 5 archivos del app (sin contar el `.ics`) a la raíz.
2. Settings → Pages → Branch: `main` → `/root` → Save.
3. Te queda en `https://je7remy.github.io/<repo>/`.

## Instalar en el teléfono (Android)

1. Abre esa URL en **Brave o Chrome** (DuckDuckGo no instala PWAs).
2. Menú (⋮) → **Instalar aplicación** / Agregar a pantalla de inicio.
3. Queda con su ícono, a pantalla completa y abre sin barra de navegador.

> La instalación y el funcionamiento offline solo van servidos por HTTPS (GitHub Pages lo da). Abrir el archivo local `file://` no instala ni guarda cambios.

## Primer uso

Toca **✎ Editar el día** y pon tus horas reales (las que vienen son un ejemplo). Hay dos perfiles separados: **Entre semana** y **Finde**. Cada bloque dura hasta que empieza el siguiente. Los cambios se guardan en ese dispositivo.

## Notificaciones entre bloques (opcional)

La web no puede lanzar avisos con la app cerrada sin un servidor. La vía simple y confiable en Android: importa `horario.ics` en Google Calendar (⚙️ → Importar y exportar) y cada bloque te llega como notificación al inicio. Edita las horas en Calendar o regenera el `.ics` con tus horas reales.

## Nota

Los datos viven por dispositivo (no se sincronizan entre teléfono y PC). Para un horario que consultas en el teléfono, suele bastar.
