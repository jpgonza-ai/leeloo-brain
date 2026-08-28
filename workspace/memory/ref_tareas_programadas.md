---
name: Lista canónica de tareas programadas (recurrentes)
description: Las 6 tareas recurrentes que Pablo confirmó como oficiales, con horarios PT y cron equivalente
type: reference
---

**Lista oficial confirmada por Pablo (2026-08-27) — "guarda bien esta info".** Sistema corre en CST (America/Mexico_City, UTC-6); PT (PDT) = UTC-7 → cron del sistema = hora PT + 1h.

| # | Tarea | Horario (PT) | Frecuencia | Entrega | Cron sistema |
|---|-------|-------------|-----------|---------|--------------|
| 1 | Brief matutino | 5:30 AM | Diario | Nota de voz (Morning Brew EN + agenda ES) | `30 6 * * *` |
| 2 | Evening brew | 5:00 PM | Diario (días hábiles*) | Nota de voz (CFO Brew + Brew Markets) | `0 18 * * *` |
| 3 | Radar de acciones | ~6:30 AM (apertura mercado US, 9:30 ET) | Solo lunes | Nota de voz con % por emisora | `30 7 * * 1` |
| 4 | Newsletter para Tavo (WAMT) | 10:00 AM | Viernes | Correo directo a Tavo + Pablo en copia | `0 11 * * 5` |
| 5 | Barrido de correos de empleo #1 | 11:00 AM | Diario | Silencioso: ordena bandeja (sin Telegram) | `6 12 * * *` |
| 6 | Barrido de correos de empleo #2 | 7:00 PM | Diario | Silencioso: ordena bandeja (sin Telegram) | `9 20 * * *` |

*Evening brew: CFO Brew y Brew Markets solo salen días hábiles; fin de semana suele ser aviso por texto.

**✅ AGENDADOR DURABLE (Helsinki) — resuelto 2026-08-28 con Patti (@TradingAssistant_AI_bot).** Ya existe un agendador durable e independiente de la sesión (sobrevive reinicios, no expira). Patti maneja la parte de sistema/sudo; Leeloo aporta el script/disparador de cada tarea. **NO pegar disparadores/scripts en el grupo (info privada de JP); coordinar directo por la caja de Helsinki.**

**Estado de durabilidad (2026-08-28):**
- **brief, evening brew, dreaming** → ya corren en el durable (confirmado por Patti, probados desde 14-ago). **Crons de sesión de brief/brew YA retirados** (2026-08-28) para no duplicar.
- **3 nuevos timers durables de Patti (en UTC):** barrido vacantes AM `18:00 UTC` (=11 AM PT), barrido vacantes PM `02:00 UTC` (=7 PM PT), radar acciones lunes `13:30 UTC` (=6:30 AM PT). Corren independientes de la sesión. **Los crons de sesión equivalentes YA se retiraron** (2026-08-28) para no duplicar.
- **Newsletter WAMT/Tavo (vie 10 AM PT)** → aún NO durable; sigue como cron de sesión `504d75ce`. Ofrecido a Patti para hacerlo durable (pendiente respuesta).

**Nota:** con el durable ya no debería hacer falta re-armar en cada sesión las tareas que Patti dejó firmes. Verificar con CronList si acaso, pero evitar duplicar los timers durables.

**Detalle de cada rutina:** morning/evening brief y anti-duplicado → sección "Flujos operativos recurrentes" de MEMORY.md + `feedback_evening_brew.md`. Radar → `project_radar_acciones.md`. Barridos de empleo → `project_barrido_vacantes.md`. WAMT/Tavo → proyecto WAMT/Marruecos.
