# SAMS DB Envy RP

Sistema de Atención Médica de San Andreas Medical Services (SAMS) para Envy RP.

## Compatibilidad de datos

La ruta interna `samuData` se mantiene para conservar la base existente. El acceso utiliza Firebase Authentication con Google o correo; las contraseñas no se almacenan en el repositorio, el HTML, el navegador ni Realtime Database.

## Autorizar personal

Los médicos pueden entrar con Google o crear una cuenta con correo y contraseña. Una cuenta nueva no puede consultar expedientes hasta que un administrador abra **Médicos**, cree o seleccione su perfil y pulse **Autorizar** en la solicitud pendiente. Las contraseñas son administradas exclusivamente por Firebase Authentication.

Los expedientes requieren una cuenta autorizada. Las solicitudes nuevas se registran en `accessRequests` y deben aprobarse asignando un registro activo en `access/<uid>`.

## Construcción

```bash
node scripts/build.js
```

El resultado se genera en `dist/`. La aplicación canónica se publica en https://programmer-professionnal.github.io/samsdbenvy/. El acceso alternativo https://samsdbenvy.web.app redirige a esa publicación. La autenticación usa el dominio auxiliar `samsdbenvy.web.app`, por lo que Google Sign-In no muestra el identificador histórico del proyecto.
