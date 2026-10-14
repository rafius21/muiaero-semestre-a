# MUIA Semestre A

Panel de seguimiento del Semestre A del Máster en Ingeniería Aeronáutica (UPV), instalable como app (PWA).

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La app completa (HTML, CSS y JS en un solo archivo) |
| `seed.json` | Datos iniciales extraídos de las guías. Solo se usan la primera vez o al pulsar "Restablecer datos de las guías" |
| `manifest.webmanifest` | Nombre, icono y modo pantalla completa de la app |
| `sw.js` | Service worker: permite usar la app sin conexión |
| `icons/` | Iconos de la app |

## Publicar en GitHub Pages

1. En GitHub, crea un repositorio nuevo, por ejemplo `muia-semestre-a`. Puede ser público o, si tu plan lo permite, privado con Pages activado.
2. Sube **el contenido** de esta carpeta a la raíz del repositorio (no la carpeta en sí). La forma más sencilla es *Add file → Upload files* y arrastrar todos los archivos y la carpeta `icons`.
3. Ve a *Settings → Pages*, en *Build and deployment* elige *Deploy from a branch*, rama `main` y carpeta `/ (root)`, y guarda.
4. Al cabo de un minuto la app estará en `https://<tu-usuario>.github.io/muia-semestre-a/`.

> Si el repositorio es público, cualquiera con el enlace verá el panel, pero **no tus datos**: tus notas y tareas se guardan solo en tu dispositivo, no en GitHub.

## Instalar en el móvil

- **iPhone (Safari):** abre la URL → botón Compartir → *Añadir a pantalla de inicio*.
- **Android (Chrome):** abre la URL → menú ⋮ → *Instalar app* (o *Añadir a pantalla de inicio*).

Ábrela una vez con conexión. Desde ese momento funciona sin red.

## Tus datos

- Se guardan en el almacenamiento local de cada navegador o app instalada. El móvil y el ordenador **no se sincronizan solos**.
- Para pasar datos de un dispositivo a otro: *Horas → Copia de seguridad → Exportar JSON* en uno, e *Importar JSON* en el otro.
- Exporta una copia con regularidad. Si borras los datos del navegador o desinstalas la app, se pierden.

## Publicar una versión nueva

Cuando cambies `index.html` (u otro archivo), sube el cambio y **aumenta `VERSION` en `sw.js`**. Así los dispositivos instalados detectan la nueva versión y muestran el botón *Actualizar*.
