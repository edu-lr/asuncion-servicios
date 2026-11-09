# Changelog

Todos los cambios importantes de Asunción Servicios se anotan acá.

El formato sigue [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/) y el versionado es semántico (MAYOR.MENOR.PARCHE).

## [1.2.0] - 2026-11-09

Cambios que responden directamente a los comentarios de las pruebas con usuarios (ver sección "Juicio Humano").

### Añadido
- **Filtro por categoría** en `proveedores.html`: un selector cuyas opciones se generan solas a partir de `proveedores.json`, sin categorías repetidas.
- **Foto de cada proveedor** en las tarjetas del listado y en la página de detalle, tomada del campo `foto` del JSON. Las imágenes del listado cargan de forma diferida (`loading="lazy"`).
- **Detalle del proveedor enriquecido:** calificación en estrellas con etiqueta accesible (`aria-label`) e indicador de disponibilidad.
- Nuevo campo `foto` en `proveedores.json`.

### Modificado
- Las tarjetas se dibujan con una función `mostrar(lista)` reutilizable, que se llama al cargar la página y cada vez que cambia el filtro.
- Estilos de la imagen del proveedor (`.fotoP`) con altura fija y `object-fit: cover`, para que todas las tarjetas queden del mismo tamaño y evitar saltos de diseño al cargar.

## [1.1.0] - 2026-11-09

### Añadido
- Imagen de fondo con degradado lila en la sección principal (Hero) de `index.html`.
- Texto real descriptivo en la página de inicio, reemplazando el Lorem Ipsum.
- Favicon para evitar errores 404 en la consola.

### Modificado
- **Estructura (HTML):** Mejora de la semántica usando `<article>` para cada tarjeta y `<section>` para el contenedor.

### Corregido
- Enlaces de teléfono en las tarjetas que no tenían `href="tel:"`.

### Rendimiento
- Tras las pruebas de Lighthouse, se optimizó el LCP (Largest Contentful Paint) mediante mejores prácticas de carga de imagen. Fue el cambio realizado a partir de los resultados de esas pruebas.

## [1.0.0] - 2026-11-05

### Creado
- Página de inicio con botón "Ir a Proveedores".
- Página de proveedores con tarjetas generadas desde `proveedores.json`.
- Página de detalle de cada proveedor, usando el id por URL.

---

## Juicio Humano

Se probó la app con 5 personas del círculo cercano (amigos y familiares),
sin conocimientos técnicos, cada uno en su propio celular y durante 5–10
minutos. En todos los casos se les asignó la misma tarea: "Encontrá al
carpintero con mejor calificación y decime su nombre." Ninguna persona tuvo
dificultades mayores para completarla: todas llegaron al resultado en menos
de un minuto, sin ayuda ni preguntas de por medio.

Los comentarios que surgieron de forma espontánea fueron dos, y se repitieron
entre las 5 personas:

- "Una imagen de los proveedores para más confianza."

- "Un filtro por categoría para poder buscar mejor a los proveedores."

Ambos comentarios se implementaron en la versión 1.2.0.