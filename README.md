# SAMS DB Envy RP

Sistema de Atención Médica de San Andreas Medical Services (SAMS) para Envy RP.

## Compatibilidad de datos

La ruta interna `samuData` se mantiene para conservar la base existente. El acceso utiliza Firebase Authentication con Google; las contraseñas no se almacenan en el repositorio, el HTML, el navegador ni Realtime Database.

Los expedientes requieren una cuenta autorizada. Las solicitudes nuevas se registran en `accessRequests` y deben aprobarse asignando un registro activo en `access/<uid>`.

## Construcción

```bash
node scripts/build.js
```

El resultado se genera en `dist/`. La aplicación canónica se publica en https://programmer-professionnal.github.io/samsdbenvy/. El acceso alternativo https://samsdbenvy.web.app redirige a esa publicación. La autenticación usa el dominio auxiliar `samsdbenvy.web.app`, por lo que Google Sign-In no muestra el identificador histórico del proyecto.
