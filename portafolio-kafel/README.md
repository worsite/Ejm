# Portafolio KAFEL

Presentación comercial en un solo archivo: `index.html` (sin dependencias de build; el logo va embebido).
Solo la tipografía viene de Google Fonts y tiene respaldo del sistema si no hay internet.

## Cómo abrirlo
Doble clic en `index.html`, o publicarlo tal cual (Netlify, GitHub Pages, etc.).
Para presentar: botón de pantalla completa (arriba a la derecha) y flechas ← → del teclado para pasar de sección.

## Qué se edita (todo dentro del `<script>` de `index.html`)

| Qué | Dónde | Notas |
|---|---|---|
| Catálogos reales (sección "Trabajos") | `var WORKS = [ … ]` | `{ name, plan:'base'\|'normal'\|'premium', url, es, en }`. El nombre de la empresa no se traduce; `es`/`en` son la descripción. |
| WhatsApp / correo del cierre | `var CONFIG = { whatsapp, email }` | WhatsApp solo con dígitos e indicativo (`573001234567`). Si queda vacío, el botón no aparece. |
| Cualquier texto | `var T = { 'clave': [español, inglés] }` | Cada texto tiene sus dos idiomas lado a lado. |
| Planes del catálogo | `var PLANS` + claves `pf.*` en `T` | Los precios están omitidos a propósito. |

## Notas
- Tema oscuro/claro e idioma ES/EN se recuerdan en el navegador (localStorage). Si no hay preferencia guardada, el idioma sigue el del navegador.
- Las demos (carrito, inventario, agenda) son **ilustrativas** y están rotuladas así; no usan datos reales.
- Skills de diseño instaladas en `.claude/skills/` (repositorio `worsite/Agentes-Construccion`).
