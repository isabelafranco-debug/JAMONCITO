# Farm Pro — copia independiente

Farm Pro se prepara a partir del código fuente de Júpiter Jr. Se conservan los módulos de planificación agrícola, mapas, comparación de rotaciones, análisis climático NASA POWER, cuentas e informes.

## Identidad y configuración

- Marca visible: Farm Pro.
- Servicio Render: `farm-pro`.
- Base de datos Render: `farm-pro-db`.
- Base y usuario PostgreSQL: `farm_pro`.
- Proyecto Docker Compose: `farm-pro`, con volumen local de base de datos independiente.
- Variables y credenciales se configuran en el entorno de Farm Pro; no se deben reutilizar las de la aplicación original.

## Publicación

1. Sube el contenido de la carpeta `Farm-Pro` al repositorio `isabelafranco-debug/JAMONCITO`.
2. En Render, crea un Blueprint conectado a `JAMONCITO` y revisa los recursos definidos en `render.yaml`.
3. Configura cualquier secreto únicamente en el servicio Farm Pro.
4. Tras el despliegue, copia la URL que Render asigne y prueba `/api/health`, registro, inicio de sesión, análisis y generación de informes.

La URL `farm-pro.onrender.com` incluida como nombre descriptivo no está reservada ni se garantiza que esté disponible; la URL definitiva es la que asigne Render.

## Importante

Este ZIP contiene el código fuente adaptado. No se ha ejecutado una compilación de frontend ni pruebas de integración en este entorno, y no se ha podido subir directamente a GitHub porque la integración conectada devuelve HTTP 403 al intentar escribir.
