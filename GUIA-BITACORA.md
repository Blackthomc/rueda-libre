# Guía para escribir tu bitácora (Semana 6)

La bitácora la escribes tú: es tu evidencia de que entendiste lo que hiciste. Esta guía
te dice **qué dato buscar, dónde encontrarlo y cómo contarlo**. Los números de ejemplo
salen de mi revisión de los archivos; verifícalos tú antes de usarlos.

## Cómo escribir bien una entrada
Una buena entrada tiene tres partes: **qué viste** → **por qué pasaba** → **qué hiciste**.
Evita frases como "quedó mejor". Prefiere "a 1280 px la flota pasó de 3 a 4 columnas sin escribir CSS".

---

## Mini reto 5: la flota con la grilla
**Qué necesitas medir**
1. **Tiempo:** el que marcó tu cronómetro. Si no lo tomaste, dilo con honestidad y estima.
2. **CSS propio de distribución de la flota (v1.5):** en `.flota-grid` hay 3 declaraciones
   (`display`, `grid-template-columns`, `gap`) y en el media query de 1200 px hay otras 2.
   Cuéntalas tú en el `styles.css` de la v1.5 y anota tu número.
3. **Clases de Bootstrap ahora:** `container`, `row`, `g-4` y `col-12 col-sm-6 col-lg-4 col-xl-3`.

**Ideas para "qué me dio sin esfuerzo / qué perdí"**
- Sin esfuerzo: cuatro puntos de quiebre, gutters parejos, mobile-first, sin escribir media queries.
- Perdí control: los breakpoints y los tamaños de gutter son los de Bootstrap (los míos eran 768 y 1200 px).
  Un `auto-fit` con `minmax` ya no existe: las columnas son fijas por rango.

## Mini reto 6: cinco clases de la documentación
Busca en el buscador de getbootstrap.com y escribe qué hace cada una con **tus palabras**.
Candidatas que usé: `d-none` / `d-md-block`, `flex-md-row`, `text-bg-*`, `gap-*`, `fs-*`, `rounded-pill`.
Anota también una clase de la versión 4 que **ya no existe** (`ml-*`, `mr-*`) y cuál la reemplazó (`ms-*`, `me-*`).

## Mini reto 7: tres conflictos
En DevTools (pestaña **Styles**) busca declaraciones **tachadas**. Mis tres hallazgos, para que los compruebes:
1. `* { margin: auto }` repartía el espacio libre de la última fila de la grilla → ahora `margin: 0`.
2. `body { background-color: white }` tapaba el Crema → se quitó y el fondo sale de `--bs-body-bg`.
3. `a:hover` de Bootstrap pintaba la marca al pasar el mouse, y su regla de listas sangraba el menú → `.marca:hover` y `list-unstyled`.

Si alguno no lo ves tachado en tu navegador, **no lo copies**: escribe uno que sí hayas visto.
Prueba también `index.html` a **360, 768 y 1280 px** y anota qué ves en cada ancho.

## Mini reto 8: la comparativa con datos reales
| Dato | v1.5 | v2.0-beta |
|---|---|---|
| Líneas de `styles.css` (con comentarios y vacías) | 574 | 122 |
| Líneas de **código** (sin comentarios ni vacías) | 307 | 68 |

Con esos números la reducción de código es de unas **78 %**. Cuéntalo en tu texto
(`1 − 68/307`), pero **comprueba la v1.5 en el historial de commits de GitHub**, porque el
archivo del .zip puede no ser idéntico al del commit.

**Tiempo:** suma el que invertiste en cada versión (tu cronómetro de la semana 5 vs. el de esta).

**Para ventajas, desventajas y conclusión** puedes responder tú mismo:
- ¿Qué hice más rápido y qué me tomó más tiempo entender?
- ¿Tuve que pelear con Bootstrap en algún punto? ¿Dónde?
- ¿Volvería a usar solo CSS propio en algún caso? ¿Cuál?
- Cierra con una frase tipo: "Bootstrap redujo X % el CSS y me ahorró Y, pero a cambio ...".

## Publicación (orden sugerido)
1. Un commit por Mini reto (mensajes claros: `Mini reto 5: flota con grilla`, etc.).
2. `git push` y revisa que GitHub Pages esté activo (Settings → Pages).
3. Prueba la URL en tu celular y en DevTools (360, 768, 1280 px).
4. Crea la etiqueta/release **v2.0-beta** y pega la URL en la bitácora.

## Lista final antes de entregar
- [ ] Network sin errores al cargar Bootstrap (si falla un `integrity`, cópialo de la documentación oficial).
- [ ] Ninguna página enlaza clases que no existen.
- [ ] El formulario sigue validando (campos vacíos, correo mal escrito).
- [ ] Tándem: reemplazar el texto y el precio provisionales por los reales.
