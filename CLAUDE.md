# Presentación: la exploración como motor de la humanidad

Presentación en React (Vite) para una juntada de amigos nacidos entre el 82 y el 90, no especialistas. Dura 15 min como máximo. Tesis, tono y reglas viven en `brief.md`: es la fuente de verdad.

## Quién hace qué
Claude (la sesión principal) es el **orchestrator**: coordina a los subagentes de `.claude/agents/`, implementa el código de las slides y consulta al usuario en cada checkpoint.

| Agente | Rol | Escribe |
|--------|-----|---------|
| `researcher` | Datos, citas e imágenes verificados, con fuente y clasificación HECHO / PLAN / ESPECULACIÓN | `research.md` |
| `designer` | Sistema visual, specs de slide, revisión de render | `design-system.md` |
| `critic` | Evalúa un bloque contra el brief; solo lee | nada |

El orchestrator, no los agentes, toca el código de `src/`.

## Flujo (con checkpoints)
Cada checkpoint **frena hasta que el usuario aprueba en el chat**. Un archivo escrito no equivale a una aprobación.

1. **Brief.** Refinar con el usuario y escribir `brief.md`. *Checkpoint: el usuario aprueba el brief.*
2. **Estructura y sistema visual.** Definir la lista concreta de slides y sus transiciones (cierra los puntos "Abierto" del brief). El `designer` propone 2–3 direcciones visuales. *Checkpoint: el usuario elige la dirección y aprueba la estructura.*
3. **Por cada bloque (1, 2, 3), en orden:**
   1. `researcher` investiga el bloque.
   2. `designer` entrega el spec de cada slide.
   3. El orchestrator implementa.
   4. `designer` revisa screenshots del render.
   5. `critic` evalúa el bloque (**máximo 2 rondas**).
   *Checkpoint: el usuario aprueba el bloque antes de pasar al siguiente.*
4. **Integración.** Transiciones entre bloques, ensayo de tiempos (cabe en 15 min), pasada final del `critic` sobre el conjunto.

## Reglas duras
- **No se arranca ningún bloque sin `brief.md` aprobado** y sin el paso 2 completo.
- Ningún dato, cifra, fecha o cita llega a una slide sin pasar por `research.md`. Un PLAN nunca se presenta como HECHO.
- Los quotes (p. ej. los Nomai de Outer Wilds) se verifican, no se citan de memoria.
- **Cero imágenes generadas por IA.** Fotos y material de archivo reales (NASA, ESA, dominio público), retocados, con licencia clara.
- Una idea por slide, poco texto, sin horror vacui.
- Los agentes leen `brief.md` primero; si cambia el brief, se avisa a los agentes afectados.

## Técnico
- Stack: React + Vite (JavaScript). Desarrollo con `npm run dev`; en PowerShell, si la política de scripts lo bloquea, usar `npm.cmd run dev`.
- Lint con oxlint (`.oxlintrc.json`).
- Commits chicos y descriptivos, uno por avance con sentido (por ejemplo, un bloque aprobado).

## Cuaderno de agentes
Cada vez que un agente (o el orchestrator) haga algo raro, anotarlo en `notas-agentes.md`: qué pasó y qué se cambió. Si el orchestrator vuelve a intentar saltear un checkpoint, la regla de arriba ya cubre el caso: aplicarla y anotarlo.
