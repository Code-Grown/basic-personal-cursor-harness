# Patterns — patrones del proyecto

Sin secretos. Describir categoría, no detalle propietario fino.

### P-001: Diff mínimo
Editar solo lo necesario; evitar reescrituras totales.

### P-002: Proponer antes de BREAKING
Cambios de contrato/API/schema → propuesta A/B + confirmación.

### P-003: Redacción segura en memory
Placeholders para IDs; nunca keys ni PII.

### P-004: El piso común se apunta
Los estándares del hub viven en `estandares/` y `plantillas/`. La regla core solo enlaza. El workflow de ejemplo no se activa en el hub.
