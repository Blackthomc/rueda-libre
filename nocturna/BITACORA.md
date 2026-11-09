# Bitácora · Rueda Nocturna v0.1

**Autor:** Thomas Calle Durango  
**Actividad:** Sesión 7 — Introducción a Tailwind CSS

## 1. Del botón de Bootstrap al botón de Tailwind

En los ejercicios anteriores construí botones usando clases de Bootstrap, que ofrece componentes y estilos predefinidos. En Tailwind construí el botón combinando clases pequeñas directamente en el HTML, por ejemplo, utilidades para el color de fondo, el espacio interno, el redondeado, la tipografía y los estados `hover:` y `focus:`.

La diferencia principal que identifiqué es que Bootstrap entrega componentes con una apariencia más definida, mientras que Tailwind permite construir el diseño a partir de utilidades de bajo nivel. Esto da más control sobre cada elemento, aunque exige elegir y mantener las clases de forma consistente.

## 2. Verificación del CSS generado

El archivo `src/input.css` contiene la importación de Tailwind:

```css
@import "tailwindcss";
```

El archivo `src/output.css` se compiló con Tailwind CSS 4.1.10 a partir de las clases utilizadas en `prototipo.html`, `index.html` y `componentes.html`. La compilación incluyó 156 candidatos de clase y generó aproximadamente 26,6 KB de CSS.

Como comprobación, una utilidad utilizada como `bg-slate-950` sí aparece en el CSS generado. Una utilidad que no se utiliza, como `bg-pink-500`, no aparece. Tailwind analiza los archivos fuente y genera las reglas que encuentra en uso, evitando incluir utilidades que no necesita el proyecto.

Para instalar las dependencias y ejecutar el flujo CLI desde esta carpeta, los comandos configurados son:

```bash
npm install
npm run watch:css
```

El script `watch:css` ejecuta `@tailwindcss/cli` en modo observación. Para generar una compilación minificada de entrega se puede ejecutar `npm run build:css`. La carpeta `node_modules/` está excluida mediante `.gitignore`; el CSS compilado sí se conserva porque GitHub Pages sirve archivos estáticos y no ejecuta npm.

## 3. Reglas del kit de componentes

- Mantengo una escala de espaciado coherente mediante utilidades de Tailwind como `p-*`, `px-*`, `py-*`, `mb-*` y `gap-*`.
- Uso esquinas redondeadas consistentes: `rounded-lg`, `rounded-xl`, `rounded-2xl` y `rounded-3xl`, según el tamaño del elemento.
- El verde esmeralda identifica las acciones principales y los estados positivos.
- El azul se utiliza para información y el ámbar para advertencias. La dificultad de las rutas también aparece escrita como Fácil, Medio o Difícil; no depende únicamente del color.
- Los botones y campos tienen estados `hover:` y `focus:` visibles. Los estados de interacción no cambian el tamaño ni desplazan el contenido.
- Las tarjetas mantienen la misma estructura; cambian los datos, la imagen y el color que acompaña al nivel de dificultad.
- Los campos del formulario tienen etiquetas visibles vinculadas con `for` e `id`, y textos de ayuda asociados.
- La alerta de confirmación usa `role="status"` para comunicar el mensaje a tecnologías de asistencia.

## 4. Comprobaciones pendientes en el navegador

La estructura HTML incluye enlaces relativos, textos alternativos en las imágenes, etiquetas asociadas a los campos y estados visibles de foco. Antes de publicar, debo abrir `index.html` y `componentes.html`, recorrer los controles con Tab y Shift+Tab, comprobar el envío de ejemplo del formulario y confirmar que `src/output.css` carga sin errores 404 en el navegador.

La publicación solicitada corresponde a `nocturna/componentes.html`. Después de subir la carpeta al repositorio y activar GitHub Pages, debo abrir la URL pública y confirmar que la página carga correctamente.
