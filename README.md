# Gestor de Anuncios - Iglesia

PWA responsiva para crear y administrar anuncios privados de la iglesia.

## Funciones
- Anuncios privados por dispositivo/cuenta.
- Panel administrativo con acceso a todos los anuncios.
- Creación, edición, detalles, descarga de archivos y eliminación.
- Selección y eliminación múltiple.
- Publicar u ocultar anuncios en `publicAnnouncements`.
- Notificaciones preparadas mediante `publicNotifications`.
- Fecha y hora de inicio obligatorias; fecha y hora de finalización opcionales.
- Instalación PWA en teléfono y computadora.
- En móvil, el botón **Nuevo** siempre lleva primero a **Elegir departamento**.
- Cuando la PWA ya está instalada, el botón **Instalar** desaparece y la barra móvil se reorganiza sin espacios vacíos.

## Firebase
Se conserva la misma configuración y arquitectura del proyecto original.

```text
announcements/{id}
publicAnnouncements/{id}
publicNotifications/{id}
```

## Estructura
```text
/
├── index.html
├── manifest.webmanifest
├── service-worker.js
├── README.md
└── icon/
    ├── logo.png
    ├── icon-192.png
    ├── icon-512.png
    ├── apple-touch-icon.png
    └── github-cover.png
```

Bootstrap Icons se carga desde CDN para mantener la interfaz con iconos Bootstrap sin añadir una carpeta de fuentes al repositorio.

## GitHub Pages
Sube el contenido de esta carpeta directamente a la raíz del repositorio y habilita GitHub Pages sobre HTTPS.
