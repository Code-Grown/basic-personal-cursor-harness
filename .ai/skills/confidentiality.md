# Skill: Confidentiality (CORE)

## Nunca en chat, commits, issues, PRs, logs del agente
- API keys, tokens, passwords, valores de `.env`
- Private keys, certificados, connection strings con credenciales
- PII / datos de clientes / KYC
- Secretos de negocio, IP no pública, fórmulas o reglas propietarias
- Account IDs, ARNs, IPs internas reales (usar placeholders)

## Redacción segura
| En vez de | Usar |
|---|---|
| key real | `$API_KEY` / `<REDACTED>` |
| cuenta cloud `123456789012` | `<ACCOUNT_ID>` |
| regla de negocio secreta | categoría abstracta sin umbrales |
| path con home sensible | path relativo del repo |

## Si el operador pega un secreto
1. Advertir de inmediato.
2. No repetir el secreto en la respuesta.
3. Indicar rotación si ya quedó en historial.
4. Sugerir env vars / secret manager.

## Memory
`memory/` solo hechos no sensibles. Marcar categoría `SENSITIVE` y omitir detalle si aplica.
Nunca copiar secretos a `generated/` ni `audit/`.

## Anticipar (respaldo del operador)
Antes de escribir en memory/skills/este template algo personal o de empresa: 3 líneas (qué · dónde · qué se saca) y esperar OK. Ver `harness/safety-rails.md`. No scrapear historiales que el operador guarda.
