# Portafolio KAFEL

Presentación comercial en un solo archivo: `index.html` (sin dependencias de build; el logo va embebido).
Solo la tipografía viene de Google Fonts y tiene respaldo del sistema si no hay internet.

## Cómo abrirlo
Doble clic en `index.html`, o publicarlo tal cual (Netlify, GitHub Pages, etc.).
Para presentar: botón de pantalla completa (arriba a la derecha) y flechas ← → del teclado para pasar de sección.

## Qué se edita (todo dentro del `<script>` de `index.html`)

| Qué | Dónde | Notas |
|---|---|---|
| Catálogos reales (aparecen al elegir un plan) | `var WORKS = [ … ]` | `{ name, plan:'base'\|'normal'\|'premium', url, es, en }`. El nombre de la empresa no se traduce; `es`/`en` son la descripción. |
| WhatsApp / correo del cierre | `var CONFIG = { whatsapp, email }` | WhatsApp solo con dígitos e indicativo (`573001234567`). Si queda vacío, el botón no aparece. |
| Cualquier texto | `var T = { 'clave': [español, inglés] }` | Cada texto tiene sus dos idiomas lado a lado. |
| Planes y precios del catálogo | `var PLANS` (`price`) + claves `pf.*` en `T` | Precios únicos en COP. |
| Suscripciones mensuales | `var SUBS` (`price`) + claves `sub.*`/`sf.*` en `T` | Se muestran dentro del plan elegido. |

## Cómo se revela la información
Precios, ejemplos reales, suscripciones y demos **no se ven** hasta que el usuario abre el servicio y elige un plan (o pulsa el botón de la demo). En celular y tablet hay un menú de secciones en la barra superior.

## Notas
- Tema oscuro/claro e idioma ES/EN se recuerdan en el navegador (localStorage). Si no hay preferencia guardada, el idioma sigue el del navegador.
- Las demos (carrito, inventario, agenda) son **ilustrativas** y están rotuladas así; no usan datos reales.
- Skills de diseño instaladas en `.claude/skills/` (repositorio `worsite/Agentes-Construccion`).
