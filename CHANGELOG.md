# Changelog

## 3.0 — 2026-10-21
- Avisos al pie de la pantalla de inicio (herramienta independiente y sin aval, basada en la Guía v5 con fecha, criterio ante contradicciones de la guía, canal de reportes) y línea con versión, autor y código fuente.
- Licencias explicitadas: consignas de la Guía v5 (CNV, CC BY 4.0), distractores CC BY 4.0, código MIT.
- Enlace "Reportar un error en esta pregunta" en cada pregunta; plantilla de issue en el repositorio.
- Eliminados los modos "Repaso rápido" (flashcards) y "Muerte súbita", con su interfaz, código y estilos.
- Autoría: Valentin Fabre (README, LICENSE, pie de página).

## 2.3 — 2026-10-13
- Repaso de errores por módulo: en la pantalla de cada módulo, botón "Repasar mis errores de este módulo (N)"; la grilla de módulos muestra los pendientes de cada uno. "Mis errores" del inicio sigue agrupando todos.

## 2.2 — 2026-10-09
- Ícono e instalación como app en iPhone/Android: `icon-180.png`, `icon-512.png`, `manifest.webmanifest` y metaetiquetas para pantalla completa.

## 2.1 — 2026-10-09
- Eliminado por completo el juego Snake ("Break de estudio"): tarjeta, pantalla, código y estilos. En 2.0 solo estaba oculto por script y seguía apareciendo en visores que no ejecutan JavaScript.

## 2.0 — 2026-10-09
- Interfaz rediseñada con lenguaje visual de terminal (fondo negro, acento ámbar, monoespaciada, sin radios ni sombras). Tokens en `docs/design-tokens.json`.
- Práctica por módulo: selección de preguntas por número o rango.
- Promedio en el historial de simulacros y de intentos por módulo.
- Enlace a la guía oficial (argentina.gob.ar) desde el inicio y desde el disclaimer.
- Eliminados mensajes de ánimo, confeti, emojis y símbolos decorativos.

## 1.4
- "Mis errores": las preguntas falladas se acumulan en el navegador y se repasan juntas hasta acertarlas.
- Campo `src` en las 735 preguntas.

## 1.3
- Reescritura de 878 distractores en 409 preguntas para eliminar sesgos de forma (ver `docs/METODOLOGIA.md`).

## 1.2
- Auditoría del banco contra la guía oficial v5: 16 claves corregidas, 22 preguntas devueltas al formato Verdadero/Falso, opciones duplicadas eliminadas, preguntas ajenas a la guía eliminadas.

## 1.1
- Versión inicial: 60 preguntas en 45 minutos, práctica por módulo, historial local, atajos de teclado.
