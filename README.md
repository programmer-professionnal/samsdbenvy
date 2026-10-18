# SAMS DB Envy RP

Sistema de Atención Médica de San Andreas Medical Services (SAMS) para Envy RP.

## Compatibilidad de datos

La ruta interna `samuData` se mantiene para conservar la base existente. El acceso utiliza Firebase Authentication con Google; las contraseñas no se almacenan en el repositorio, el HTML, el navegador ni Realtime Database.

Los expedientes requieren una cuenta autorizada. Las solicitudes nuevas se registran en `accessRequests` y deben aprobarse asignando un registro activo en `access/<uid>`.

## Construcción

```bash
node scripts/build.js
```

El resultado se genera en `dist/`. La publicación mediante GitHub Pages utiliza las variables y secretos de Firebase configurados en el repositorio.
