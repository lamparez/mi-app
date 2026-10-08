# Notas de agentes

Registro de cada vez que un agente (o el orchestrator) hizo algo raro y qué se cambió. Formato: fecha · quién · qué pasó · qué se cambió.

## 2026-10-08 · orchestrator · ofreció arrancar un bloque sin brief.md
Tras copiar los agentes, el orchestrator ofreció "arrancar con el bloque que quieras" cuando todavía no existía `brief.md`. Se corrigió a mano: el paso 1 es refinar el brief con el usuario.
- **Cambio aplicado:** `CLAUDE.md` ahora tiene la regla dura "no se arranca ningún bloque sin `brief.md` aprobado" y checkpoints explícitos en el flujo.

## 2026-10-08 · setup · `CLAUDE.md` no existía
El pedido mencionaba "el paso 1 del CLAUDE.md", pero el repo no tiene `CLAUDE.md`. Los pasos del flujo hay que definirlos (o pegarlos) antes de depender de ellos. Se creó `CLAUDE.md` con el flujo propuesto por el orchestrator (a revisar por el usuario).
