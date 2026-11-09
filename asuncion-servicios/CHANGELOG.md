# Changelog

Todos los cambios importantes de Asuncion Servicios se anotan acá.

## [1.0.0] - 2026-11-05

### Creado
- Página de inicio con botón "Ir a Proveedores".
- Página de proveedores con tarjetas generadas desde `proveedores.json`.
- Página de detalle de cada proveedor, usando el id por URL.

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
- Optimización de LCP (Largest Contentful Paint) mediante mejores prácticas de carga de imagen.