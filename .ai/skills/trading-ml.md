# Skill: Trading / ML de mercados (OPCIONAL · pack de dominio)

Actívalo solo si el proyecto consumidor trabaja con datos de mercado, señales, modelos o ejecución.  
**No asumas expertise.** Explica en lenguaje claro; define términos la primera vez si el perfil no es quant/senior.

## Principios (accesibles)
1. **Paper primero** — pruebas sin dinero real; “live” (dinero real) solo con confirmación explícita.
2. Separar: datos → features → modelo/señal → riesgo → ejecución.
3. Debe existir forma de **apagar** la estrategia (flag / kill switch).
4. Cuidado con **look-ahead** (usar info del futuro sin querer en el backtest).
5. Límites de riesgo antes de tamaño de orden.
6. No pegar en chat: keys de broker, fórmulas alpha secretas, posiciones reales.

## Glosario mínimo (para no expertos)
| Término | Significado simple |
|---|---|
| paper | simulación, sin capital real |
| live | órdenes con dinero real |
| backtest | probar reglas con datos históricos |
| signal | indicación de comprar/vender (no es orden aún) |
| slippage | diferencia entre precio esperado y ejecutado |

## Checklist pre-cambio
- [ ] ¿El pedido toca paper o live? Confirmar.
- [ ] ¿Cómo validar sin exponer el edge? (backtest / paper)
- [ ] ¿Hay rollback / flag?
- [ ] ¿El operador entendió el riesgo en 1 frase llana?

## Tono
Conciliador: advertir riesgos sin alarmismo ni jerga innecesaria. Si el operador duda → pausar y reexplicar con ejemplo del **su** repo (archivos leídos).
