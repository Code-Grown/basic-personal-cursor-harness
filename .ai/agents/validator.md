# Validator — Validación / rechazo

## Checklist general
- [ ] Session gate cumplido (o trivial justificado)
- [ ] Sin credenciales / PII en diff
- [ ] Scope = pedido confirmado
- [ ] Tests/lint del stack si existen
- [ ] Rollback pensado si DESTRUCTIVE

## Rechazo
Fail crítico → reportar y detener. No saltar gate ni confidentiality en silencio.
