# Desarrollo guiado por spec (versión liviana)

El pitch es la spec del cambio. La spec viva de la app dice qué hace el producto. El CI exige el piso.

## El pitch es la spec

Su «listo cuando» son los criterios de aceptación. El cuerpo del PR copia esos criterios y marca cuáles cumple. La primera línea del bloque es `Pitch:`. Esa línea es el enlace que mira el check. La plantilla está en `plantillas/pitch.md`.

## Spec viva de cada app

Cada app tiene una spec corta en `specs/README.md`. Si la app ya guarda su conocimiento en `.ai/conocimiento.md`, vive ahí. Dice qué hace, sus reglas de negocio y lo que no se toca. La plantilla está en `plantillas/spec-app.md`.

El agente la lee antes de construir. Si el cambio mueve el comportamiento, la actualiza en el mismo PR.

## Cuándo la spec es larga

Solo un cambio irreversible lleva spec larga antes del código: migración de datos, pagos o auth. El resto se construye con el pitch y la spec viva.

## Los estándares se exigen en CI

En la app, el workflow corre lint, pruebas y build, y falla si el cuerpo del PR no trae una línea `Pitch:`. Axe y Lighthouse CI van en modo aviso: avisan y no bloquean. El ejemplo, inactivo en este hub, está en `plantillas/ci-estandares.yml`. El piso de páginas y portales está en `estandares/piso-frontend.md`.
