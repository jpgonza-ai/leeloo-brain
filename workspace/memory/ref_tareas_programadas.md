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

**⚠️ AGENDADOR DURABLE (Helsinki) — montado 2026-08-28 con Patti (@TradingAssistant_AI_bot), pero FALLÓ en su 1ª prueba real.** Patti confirmó que existe un agendador durable en Helsinki y montó 3 timers nuevos; Leeloo retiró los crons de sesión duplicados para no disparar doble. **Pero el 2026-08-28, primera prueba real, NINGÚN timer durable ejecutó**: brief, ambos barridos y evening brew hubo que correrlos A MANO. Al parecer el durable despierta pero sin sesión con herramientas para actuar → y al quitar los crons de sesión se perdió el fallback que sí jalaba. **Patti maneja sistema/sudo; NO pegar disparadores/scripts en el grupo (info privada de JP); coordinar directo por la caja de Helsinki.**

**Decisión de Pablo (2026-08-28 msg 2303):** "dejémoslo así, ya veremos el lunes" → **retomar con Patti el lunes 2026-08-31.** Por ahora Leeloo cubre las 6 tareas A MANO; **NO re-armar crons de sesión todavía** (decisión de Pablo). Fallback bajo demanda: Pablo pide "brief"/"brew"/"radar" si no salen.

**Timers durables de Patti que se montaron (en UTC, referencia):**
- **brief, evening brew, dreaming** → supuestamente en el durable desde 14-ago (pero brief y brew NO ejecutaron el 28-ago).
- **3 nuevos (28-ago):** barrido vacantes AM `18:00 UTC` (=11 AM PT), barrido PM `02:00 UTC` (=7 PM PT), radar acciones lunes `13:30 UTC` (=6:30 AM PT). Ninguno ejecutó el 28-ago.
- **Newsletter WAMT/Tavo (vie 10 AM PT)** → nunca fue durable; sigue como cron de sesión `504d75ce`. Ofrecido a Patti (pendiente).

**Detalle de cada rutina:** morning/evening brief y anti-duplicado → sección "Flujos operativos recurrentes" de MEMORY.md + `feedback_evening_brew.md`. Radar → `project_radar_acciones.md`. Barridos de empleo → `project_barrido_vacantes.md`. WAMT/Tavo → proyecto WAMT/Marruecos.
