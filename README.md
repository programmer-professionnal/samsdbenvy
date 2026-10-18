# SAMS DB Envy RP

Sistema de Atención Médica de San Andreas Medical Services (SAMS) para Envy RP.

## Compatibilidad de datos

La ruta interna `samuData` se mantiene para conservar la base existente. El acceso utiliza Firebase Authentication con Google; las contraseñas no se almacenan en el repositorio, el HTML, el navegador ni Realtime Database.

Los expedientes requieren una cuenta autorizada. Las solicitudes nuevas se registran en `accessRequests` y deben aprobarse asignando un registro activo en `access/<uid>`.

## Construcción

```bash
node scripts/build.js
```

El resultado se genera en `dist/`. La aplicación se publica en https://samsdbenvy.web.app y también mediante GitHub Pages. Ambos despliegues usan `samsdbenvy.web.app` como dominio de autenticación para que Google Sign-In no muestre el identificador histórico del proyecto.
