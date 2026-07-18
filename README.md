# Gestor de Anuncios - Iglesia

![Portada del proyecto](./icon/github-cover.png)

Aplicación web responsiva y PWA para crear y administrar anuncios privados de la iglesia. El diseño está optimizado para computadora y teléfono.

## Funciones incluidas

- Vista privada: cada dispositivo consulta únicamente sus propios anuncios.
- Panel administrativo: el administrador consulta todos los anuncios.
- Creación, edición, detalles, descarga de archivos y eliminación.
- Selección y eliminación múltiple desde el panel administrativo.
- Botones **Mostrar al público** y **Ocultar del público**.
- Sincronización en tiempo real con la misma Firebase Realtime Database.
- Instalación como aplicación PWA desde Chrome o Edge.
- Fecha y hora de inicio obligatorias; finalización opcional.

## Rutas preparadas en Firebase

```text
announcements/{id}
publicAnnouncements/{id}
publicNotifications/{id}
```

- `announcements`: conserva los anuncios privados del gestor.
- `publicAnnouncements`: recibe una copia del anuncio cuando el administrador pulsa **Mostrar al público**. Incluye los archivos para que la futura versión pública pueda descargarlos.
- `publicNotifications`: recibe una señal `new_announcement` que la futura versión pública podrá escuchar para mostrar una notificación.

La interfaz pública todavía no forma parte de este proyecto.

## Estructura

```text
/
├── index.html
├── manifest.webmanifest
├── service-worker.js
├── assets/
│   └── bootstrap-icons.min.css
└── icon/
    ├── logo.png
    ├── icon-192.png
    ├── icon-512.png
    ├── apple-touch-icon.png
    └── github-cover.png
```

## Publicación en GitHub Pages

1. Sube todos los archivos conservando la estructura.
2. Abre **Settings → Pages** en GitHub.
3. Selecciona la rama principal y la carpeta raíz `/`.
4. Abre la dirección HTTPS generada.
5. En Chrome móvil usa **Instalar aplicación** o **Agregar a pantalla principal**.

## Nota de seguridad

La privacidad visual se aplica mediante el identificador persistente del dispositivo y consultas filtradas por `authorId`. Para una protección contra accesos directos a la base de datos, las reglas de Firebase deben restringir lectura y escritura cuando posteriormente se incorpore autenticación real de usuarios.
