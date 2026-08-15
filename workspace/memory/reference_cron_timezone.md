---
name: Reloj del programador de crons corre en hora de México (no en PT)
description: El scheduler de CronCreate usa la TZ del sistema = America/Mexico_City (UTC-6), NO Pacífico. Convertir SIEMPRE los horarios de PT a hora del sistema antes de programar.
type: reference
---

# El programador de crons NO corre en hora del Pacífico

**Hecho (verificado 2026-08-14):** la caja donde corro tiene `/etc/timezone = America/Mexico_City` (CST, **UTC-6, sin horario de verano**). El scheduler de `CronCreate` interpreta el cron en ESA hora local del sistema, no en la de Pablo (Pacífico).

**Why:** el 2026-08-14 programé el envío a Tavo para las "10:01" pensando en PT; disparó a las **10:01 CST = 9:01 AM PT**, ~1 hora antes. Pablo lo notó ("debió ser a las 10am PT... son las 9:05am"). Es la causa raíz de que las rutinas no salgan puntuales.

**Desfase (OJO, cambia con el horario de verano de EE.UU.):**
- México NO cambia de hora (siempre UTC-6).
- Pacífico SÍ: **PDT (verano, ~mar–nov) = UTC-7** → sistema va **PT+1**. **PST (invierno) = UTC-8** → sistema va **PT+2**.
- O sea NO es un +1 fijo. Hay que recalcular en cada cambio de DST (marzo y noviembre).

**How to apply — regla robusta (no hardcodear +1):**
Para programar algo a una hora-objetivo en PT, calcula primero qué hora del sistema (México) corresponde y usa ESA en el cron. Verifica con:
```
# ¿qué hora del sistema (México) es ahora, y qué hora PT?
date "+%H:%M %Z"                         # hora del sistema (la que usa el cron)
TZ=America/Los_Angeles date "+%H:%M %Z"  # hora real de Pablo (PT)
```
La diferencia entre ambas líneas es el desfase a sumar. Ejemplos con el desfase actual (+1, verano PDT):
- 5:30 AM PT → 6:30 CST → cron `30 6 * * *`
- 5:00 PM PT → 6:00 PM CST → cron `0 18 * * *`
- 10:00 AM PT (envío Tavo) → 11:00 CST → cron `0 11 * * 5`

**Crons ya corregidos (2026-08-14, session-only):** morning brew `32 6 * * *` (=5:32 AM PT); evening brew `3 18 * * 1-5` (=5:03 PM PT).
**Por revisar:** el radar de acciones del lunes (76e4f697, "7:30 AM" del sistema = 6:30 AM PT) — si se quería 7:30 AM PT, mover a `30 8 * * 1`.

**Recordatorio aparte:** aunque el flag `durable:true` existe, en este entorno NO persiste a disco (no escribe scheduled_tasks.json) → los crons siguen muriendo al reiniciar. Ver log 2026-08-14.
