# Asunción Servicios

Directorio en línea para encontrar proveedores de servicios locales en Asunción, Paraguay: perfiles claros, calificaciones visibles y contacto directo por teléfono. Pensado para acabar con el problema de los proveedores fantasma.

**Versión actual:** 1.2.0 (ver [CHANGELOG.md](CHANGELOG.md))

## 🚀 Demo

https://edu-lr.github.io/asuncion-servicios/

## ✨ Funcionalidades

- **Inicio:** presentación de la app y botón para ir al listado.
- **Listado de proveedores:** tarjetas con foto, nombre, categoría, descripción, calificación, zona y teléfono.
- **Filtro por categoría:** las categorías se generan automáticamente desde los datos.
- **Detalle de proveedor:** ficha individual con calificación en estrellas, disponibilidad y botón para llamar.
- **Estados de la interfaz:** mensajes de "cargando", "sin resultados" y "error" tanto en el listado como en el detalle.

## 🛠️ Tecnologías

HTML5, CSS3, JavaScript vanilla (módulos ES) y JSON. Sin frameworks ni librerías externas.

## 📁 Estructura del proyecto

```
asuncion-servicios/
├── index.html           - Página de inicio con descripción y llamado a la acción
├── proveedores.html     - Listado de proveedores (fetch al JSON, filtro y estados)
├── detalle.html         - Ficha de un proveedor, seleccionado por ?id= en la URL
├── css/
│   └── styles.css       - Estilos con variables CSS, organizados por página
├── data/
│   └── proveedores.json - Datos de los proveedores (9 registros)
├── img/                 - Favicon, fondo del inicio y fotos de proveedores
├── README.md            - Este archivo
└── CHANGELOG.md         - Historial de cambios y pruebas con usuarios
```

El JavaScript de cada página está incluido en su propio HTML, dentro de un `<script type="module">` en el `<head>`.

## 🗂️ Formato de los datos

`data/proveedores.json` es un objeto con un arreglo `proveedores`. Cada proveedor tiene esta forma:

```json
{
  "id": 2,
  "nombre": "María González",
  "categoria": "Electricidad",
  "calificacion": 4.8,
  "telefono": "+595981222222",
  "zona": "San Lorenzo",
  "descripcion": "Electricista residencial. Instalaciones y reparaciones eléctricas rápidas.",
  "disponible": true,
  "foto": "img/proveedores/maria-gonzalez.svg"
}
```

Para agregar un proveedor, sumá un objeto más al arreglo con un `id` nuevo y único. Las páginas se actualizan solas.

## 💻 Cómo ejecutar en local

1. Instalar VS Code y la extensión **Live Server**.
2. Abrir la carpeta del proyecto en VS Code.
3. Clic derecho sobre `index.html` → "Open with Live Server".
4. Navegar a http://localhost:5500

**Importante:** no abrir los HTML con doble clic. Al usar `fetch()` y módulos de JavaScript, el navegador los bloquea desde `file://`. Es necesario un servidor local.

## 🌐 Cómo desplegar en GitHub Pages

1. Subir el proyecto a un repositorio de GitHub, con `index.html` en la raíz.
2. Ir a **Settings → Pages**.
3. En **Source**, elegir **Deploy from a branch**; en **Branch**, `main` y la carpeta `/ (root)`. Guardar.
4. Esperar uno o dos minutos. El sitio queda publicado en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`.

Todas las rutas del proyecto son relativas (`css/styles.css`, `data/proveedores.json`), por lo que funcionan igual en local y publicado. Los nombres de archivos y carpetas distinguen mayúsculas de minúsculas en GitHub Pages.

## ♿ Accesibilidad

- HTML semántico (`header`, `nav`, `main`, `section`, `article`, `footer`) y `lang="es"`.
- Texto alternativo descriptivo en las fotos de los proveedores.
- Calificación en estrellas con `aria-label` para lectores de pantalla.
- Teléfonos como enlaces `tel:` para llamar con un toque desde el celular.
- Diseño adaptable a pantallas de celular, tablet y computadora.

## 📊 Evidencia Lighthouse

Reportes generados sobre el sitio publicado:

| Página | Rendimiento | Accesibilidad | Buenas prácticas | SEO |
|---|---|---|---|---|
| Inicio | _completar_ | _completar_ | _completar_ | _completar_ |
| Proveedores | _completar_ | _completar_ | _completar_ | _completar_ |
| Detalle | _completar_ | _completar_ | _completar_ | _completar_ |

**Mejora aplicada tras las pruebas de Lighthouse:** se optimizó el LCP (Largest Contentful Paint) mediante mejores prácticas de carga de imagen. Fue el cambio realizado a partir de los resultados de esas pruebas (ver versión 1.1.0 en [CHANGELOG.md](CHANGELOG.md)).

## 🧪 Pruebas con usuarios

Se probó la app con 5 personas sin conocimientos técnicos, cada una desde su celular. Todas completaron la tarea asignada en menos de un minuto. Sus dos sugerencias (fotos de los proveedores y filtro por categoría) se implementaron en la versión 1.2.0. El detalle completo está en [CHANGELOG.md](CHANGELOG.md), sección "Juicio Humano".
