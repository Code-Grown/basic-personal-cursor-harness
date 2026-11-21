# <Nombre de la app>

Spec viva. El agente la lee antes de construir y, si el comportamiento cambia, la actualiza en el mismo PR.

## Qué hace
<Para quién es y qué resuelve, en una frase.>

## Reglas de negocio
- <Regla que el código tiene que cumplir.>
- <Segunda regla.>
- <Tercera regla.>

## No se toca
- <Dato, integración o flujo que este trabajo no mueve.>
- Secretos, infra y otros proyectos.

## Dónde vive
`specs/README.md`, o `.ai/conocimiento.md` si la app ya guarda ahí su conocimiento.

## Spec del cambio
El pitch es la spec del cambio. El PR copia su «listo cuando» y marca cuáles criterios cumple. Spec larga, antes del código, solo en cambios irreversibles: migración de datos, pagos, auth.
