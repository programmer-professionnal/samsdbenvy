# SAMS DB Envy RP

Sistema de Atención Médica de San Andreas Medical Services (SAMS) para Envy RP.

## Compatibilidad de datos

Los identificadores internos heredados (`samu_ems_db`, `samuData`, `samu_session` y otras claves `samu_*`) se mantienen deliberadamente para conservar los datos locales y la compatibilidad con Firebase. La identidad visible, los documentos, las copias de seguridad nuevas y la caché PWA usan SAMS Envy RP.

## Construcción

```bash
node scripts/build.js
```

El resultado se genera en `dist/`. La publicación mediante GitHub Pages utiliza las variables y secretos de Firebase configurados en el repositorio.
