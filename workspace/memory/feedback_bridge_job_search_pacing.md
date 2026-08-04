---
name: Espaciar las búsquedas de vacantes con el Puente (sin prisa)
description: Preferencia de Pablo para que Leeloo pace las búsquedas de empleo vía el Puente, con tiempo entre cargas, para evitar el anti-bot de LinkedIn
type: feedback
---

Cuando Pablo pida buscar vacantes (LinkedIn u otras plataformas vía el Puente), **espaciar las cargas/consultas con suficiente tiempo entre una y otra; NO hacerlo "de volada".** No hay prisa: prefiere lentitud a rapidez.

**Why:** El 2026-08-03, tras ~5 cargas headless seguidas, LinkedIn soft-bloqueó la caja Helsinki (IP de datacenter) con `ERR_TOO_MANY_REDIRECTS`. Al explicárselo, Pablo dio la directiva explícita: "cada vez que te pida buscar vacantes, búscalas con suficiente tiempo entre una y otra, no necesito que lo hagas de volada." Es una preferencia confirmada, no una corrección.

**How to apply:**
- Navegar con ritmo humano: delays entre páginas, reutilizar el mismo contexto/página del navegador en vez de relanzar, no disparar muchas cargas en pocos minutos.
- No borrar el `~/bridge/profile/` persistente sin necesidad (LinkedIn siembra ahí cookies suplementarias —JSESSIONID/bcookie/lidc— que /jobs/ necesita; el wipe reactiva los redirect loops).
- Si aparece el soft-block, NO insistir (empeora): dejar enfriar ~1–2 h y reintentar, avisándole a Pablo.
- Como no hay urgencia, está OK diferir la búsqueda (programar reintento) en vez de forzarla en el momento.
