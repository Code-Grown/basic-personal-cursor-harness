# Safety rails (generic)

Best-of genérico cristalizado para el template compartible.
**Sin secretos de producto, hosts privados ni facts de cliente.**

## Never
- Commit/echo secrets (keys, tokens, `.env`, private certs, passworded URLs).
- Write exploits or attack systems.
- Treat chat history as source of truth over durable `memory/` / skills.
- Move/delete user workspaces or merge unrelated projects without explicit ask.

## Require explicit OK
- Destructive git (`push --force` to shared, `reset --hard`, `clean -fdx`).
- Destructive data (`DROP`/`TRUNCATE`, mass deletes, breaking migrations).
- Prod deploy when user asked local-only; open firewall / wipe volumes / blind DNS-SSL changes.
- Disabling auth/TLS “just to test” outside a clearly isolated local sandbox.

## Sensitive data
- PII and business secrets: minimize; use placeholders in memory/docs.
- If the user pastes a secret: warn, do not echo, suggest rotation.

## Back the operator — anticipate first
Do not silently absorb their personal life or company data into memory / skills / this template / chat echo.

Before writing anything that looks personal (real name, national ID, home paths, private chats) or company (clients, pricing, unpublished, hosts):

**Anticipate** in 3 lines: what · where · what you would strip. Wait for OK.  
Never promote that here. Do not scrape their saved chat histories.

## Confirm before non-trivial work
Impact (SAFE | BREAKING | DESTRUCTIVE | SENSITIVE) · scope · reversibility · what will **not** be done.
SAFE trivial work may proceed without a long ritual.
