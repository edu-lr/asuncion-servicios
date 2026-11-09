# Asunción Servicios

Directorio en línea para encontrar y calificar proveedores de servicios locales en Asunción, Paraguay. Un "Tinder de servicios" pero sin drama: perfiles reales, calificaciones verificables y contacto directo. El problema de los proveedores fantasmas acaba de terminar.

## 🚀 Demo

[Enlace al sitio en Netlify — dejar como placeholder `https://TU-SITIO.netlify.app` con nota de reemplazar]

## 🛠️ Tecnologías

HTML5, CSS3, JavaScript vanilla, JSON

## 📁 Estructura del proyecto

```
asuncion-servicios/
├── index.html           - Página de inicio con descripción y llamado a la acción
├── proveedores.html     - Listado de proveedores consumido desde JSON vía fetch
├── detalle.html         - Ficha detallada de un proveedor específico
├── css/
│   └── styles.css       - Estilos puros con variables CSS, responsive y accesibilidad
├── js/
│   ├── proveedores.js   - Lógica de carga, renderizado y estados (cargando/vacío/error)
│   └── detalle.js       - Lógica de detalle con parámetros URL y fetch
├── data/
│   └── proveedores.json - 8 proveedores variados con categorías reales
├── img/
│   └── .gitkeep         - Para control de versiones de imágenes futuras
├── README.md            - Este archivo
└── CHANGELOG.md         - Historial de cambios
```

## 💻 Cómo ejecutar en local

1. Instalar VS Code + extensión Live Server
2. Abrir la carpeta del proyecto en VS Code
3. Clic derecho sobre index.html → "Open with Live Server"
4. Navegar a http://localhost:5500

**IMPORTANTE:** NO abrir los HTML con doble clic, porque fetch() falla por CORS. Es obligatorio usar Live Server.

## 🌐 Cómo desplegar en Netlify

1. Ir a netlify.com
2. "Add new site" → "Deploy manually"
3. Arrastrar la carpeta completa del proyecto
4. Netlify devuelve URL pública automáticamente

## ♿ Accesibilidad implementada

- HTML semántico con lang="es"
- aria-live y aria-busy en el listado
- Navegación 100% por teclado con :focus-visible visible
- Contraste AA según WCAG
- Labels y alt descriptivos
- Botones reales <button> donde corresponde

## 📊 Evidencia Lighthouse

[Sección con instrucciones para que el usuario agregue capturas antes/después]
Placeholder: "Agregar capturas img/lighthouse-antes.png e img/lighthouse-despues.png"

## 🧪 Pruebas con usuarios

Ver CHANGELOG.md sección "Pruebas de usuario".

## 📝 Licencia

MIT