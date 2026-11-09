Bitácora, Rueda Libre v1.5
1. Encabezado y pie al estrechar la ventana (MiniReto 2)
- Encabezado: Al reducir el ancho de la ventana, aproximadamente a 768 px, la marca permanece visible y el menú se ajusta al espacio disponible.
- Menú: Aproximadamente a 600 px, los enlaces comienzan a bajar de línea.
- Pie: Aproximadamente a 768 px, los bloques dejan de caber en una fila y se reorganizan verticalmente.
2. Columnas de la flota por ancho (MiniReto 3)
Ancho	Columnas
1280 px	3 columnas
900 px	2 columnas
500 px	1 columna

Con el 7.º modelo (Tándem), ¿cambió algo sin tocar el CSS?

Sí. Al agregar el séptimo modelo, la cuadrícula distribuyó automáticamente las tarjetas sin necesidad de modificar el CSS.
3. Decisiones Flexbox / Grid (MiniReto 4)
Caso	¿Flexbox o Grid?	¿Por qué?
Portada	Flexbox	Organiza el contenido en una dimensión.
Galería de rutas	Grid	Distribuye los elementos en filas y columnas.
Reservas (2:1)	Grid	Permite establecer dos columnas con diferentes proporciones.
Fila del formulario	Flexbox	Organiza los campos horizontalmente.
Encabezado	Flexbox	Distribuye la marca y el menú en una fila.
Pie de página	Grid	Organiza los bloques en filas y columnas.

4. Problemas responsive encontrados (MiniReto 5)
#	Problema (qué viste)	Ancho donde ocurre	Causa	Solución
1	Las tarjetas se veían demasiado estrechas.	500 px	Había demasiadas columnas.	Adaptar la cuadrícula a una columna.
2	Los enlaces del menú se desorganizaban.	600 px	No había suficiente espacio horizontal.	Ajustar la distribución del menú.
3	Los bloques del pie se veían comprimidos.	768 px	Intentaban mantenerse en una fila.	Reorganizar los bloques en columnas.

5. Pruebas por dispositivo
- 360 px: El contenido se adapta a una columna y no debería presentar scroll horizontal.
- 768 px: La distribución se ajusta para tabletas y disminuye la cantidad de columnas.
- 1280 px: Se muestra la versión de escritorio con varias columnas y menú horizontal.
- Celular real: La versión 1.5 publicada debe permitir navegar y visualizar correctamente las tarjetas y las imágenes.
6. Publicación
- URL de GitHub Pages: Pendiente de agregar.

- Commits (uno por MiniReto):
- MiniReto 1: Ajustes iniciales de Rueda Libre v1.5.
- MiniReto 2: Adaptación responsive del encabezado y pie.
- MiniReto 3: Distribución responsive de la flota.
- MiniReto 4: Implementación de Flexbox y Grid.
- MiniReto 5: Corrección de problemas responsive y pruebas.