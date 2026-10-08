# Sistema visual — Dirección A: "Observatorio a la deriva"

> Elegida por el usuario el 2026-10-08. Propuesta original del `designer`. Se usa la dirección **A pura**; el papel crema del bloque 2 (idea tomada de la dirección B) queda como ajuste de registro, no como híbrido completo. A revisar al llegar al bloque 2.

## Concepto
Alguien mirando desde una cabina chiquita un cosmos grande, tibio y analógico. Un solo plano continuo que cambia de escala y de luz: los fondos no se cortan, se funden. Referencias: la sensación de Outer Wilds (sin copiar assets), carteles de planetario, cartas estelares impresas.

## Paleta (tokens)
| Token | Hex | Uso |
|-------|-----|-----|
| `--noche` | `#0B0F1E` | Fondo base |
| `--tinta` | `#E9E2D0` | Texto principal |
| `--ambar` | `#E8A33D` | **La luz de la curiosidad.** Siempre es eso y nada más |
| `--terracota` | `#C4553A` | Acento secundario, riesgo / límite |
| `--azul-apagado` | `#3A4A6B` | Líneas, constelaciones, fondos secundarios |

El ámbar no se usa de adorno: solo aparece donde hay curiosidad, descubrimiento o un punto de luz que importa.

## Tipografía (Google Fonts)
- Títulos: **Fraunces** (serif cálida).
- Cuerpo: **Inter**.
- Datos y cifras: **JetBrains Mono**.
- Texto mínimo: 48 px (legible a 4 metros).

## Grilla
12 columnas, mucho margen. El texto abajo a la izquierda y el aire arriba.

## Motion y transiciones
Cámara que se aleja o se acerca; nunca cortes. Cada transición significa algo:
- **S1 → S2:** una luz ámbar (una fogata) se enciende y la cámara baja hasta ella.
- **S2 → S3:** el cielo gira lentamente (rotación de constelaciones SVG).
- **S3 → S4:** el cielo "se apoya" y se vuelve horizonte marino.
- **S7 → S8:** la cámara se aleja hasta ver un punto ámbar solo.
- Las demás transiciones (S4→S5, S5→S6, S6→S7) las define el `designer` en el spec de cada bloque, con el mismo criterio: cambiar de escala o de luz, con significado.

## Variación por registro
| Registro | Bloque | Luz |
|----------|--------|-----|
| Evocativo | 1 (S1–S3) | Oscuro, ámbar, serif grande |
| Humanístico | 2 (S4–S5) | El fondo sube a papel crema de carta náutica, con tinta azul |
| Técnico | 3 (S6–S7) | Vuelve a oscuro frío, mono y líneas finas |
| Cierre | S8 | Oscuro y ámbar: vuelve al punto de luz del principio |

## Anti AI-slop
- Imágenes: fotos reales NASA/ESA (Hubble, Apollo, Tierra desde la ISS, sondas) con **grano de película y duotono ámbar/azul**, retocadas. Licencia clara siempre.
- SVG simple: constelaciones, órbitas, un punto ámbar.
- Cero ilustración "épica" generada. Cero imágenes generadas por IA.
- Sin horror vacui: pocos elementos, el aire trabaja a favor.
- No se copian assets de Outer Wilds ni de ningún juego; se evoca la sensación.
