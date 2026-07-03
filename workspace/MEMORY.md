# MEMORY.md — Memoria activa de Leeloo ⚡

## Proyectos en curso
- **Búsqueda laboral activa (SF / Bay Area):** JP construye pipelines de empresas objetivo por industria (Healthcare, Fintech, Industrial Tech, Entretenimiento). Perfil y empresas ranqueadas en `identity/USER.md`. Rol de Leeloo: headhunter — rastrear vacantes con fit y agilizar aplicaciones.
- **Migración v1 → v2 (OpenClaw → Claude Code Max):** COMPLETADA (2026-07-02). Histórico v1 archivado en `workspace/v1/` (17 bitácoras, 22 sesiones, `main.sqlite`, Notas Propias, audios, identidad v1 de referencia). Esencial destilado a `USER.md` y este archivo. Basura (browser 264M, credenciales viejas) descartada.

## Flujos operativos recurrentes
- **Resúmenes de correo → Telegram** (Morning Brew, Brew Markets, CFO Brew): saludo por hora + resumen en INGLÉS, priorizando markets/acciones, macro, finanzas y tech. Chat 1346946313. Formato ideal = nota de voz, pero **hoy cae a TEXTO** (ver pendiente TTS). Para agendar el disparo usar **cron LOCAL (CronCreate)**, no el skill remoto.
- Interés en integración de **Google Calendar**.

## Herramientas y capacidades
- **Gmail conectado y verificado** (jpablogov@gmail.com): leo, busco, etiqueto y creo borradores al vuelo. **Enviar correos = acción externa → confirmar con JP antes.** Los hilos largos exceden el límite de tokens; extraer `plaintextBody` con python (no hay `jq`).
- **Agendar tareas que le escriben a JP por Telegram = cron LOCAL (CronCreate)**, NO el skill `schedule` remoto (el entorno remoto solo tiene Gmail/Calendar/Asana, sin Telegram).
- **⚠️ PENDIENTE — TTS/audio:** en v2 NO hay herramienta de generación de voz. Los resúmenes "por audio" que prefiere JP caen a texto hasta resolverlo. Prioridad para cumplir su formato preferido.

## Notas
- **⚠️ Responder a JP SIEMPRE por la herramienta `reply` de Telegram** con su chat_id — la salida de consola NO le llega. Ya me pasó repetido que respondí solo por consola y JP pensó que estaba offline. Toda respuesta va por reply.
- **⚠️ Precisión de fechas:** el server corre en hora local **CST (UTC-6)**, NO Pacífico. Para agendar en hora de JP (Pacífico) convertir siempre (PDT + 1h = hora local del cron). Y **nunca afirmar el día de la semana sin verificarlo** con `date`. Verificar, no tantear.
- Círculo de confianza: **Mario** y **Patti** (bot: @TradingAssistant_AI_bot) — trato cálido, colaborativo, como con JP.
- **Grupo Telegram con Mario + Patti** (chat_id `-5463783148`): Mario = humano (user "bilbeny"). Patti = bot co-creadora / Chief of Staff (veterana desde 2023). Bot-a-bot SÍ funciona, pero por *privacy mode* de Telegram solo recibo de Patti si me tira **slash `/...@LeelooJP_bot`**, responde a mis mensajes, o mención bien formateada (mención simple NO llega). Detalle en log 2026-07-02.
- **⚠️ Regla de confidencialidad (Mario, 2026-07-02):** JP es el dueño y usuario; Mario y Patti son SOPORTE. **NADA confidencial de JP en el grupo `-5463783148`** — lo sensible se queda en el canal directo de JP.
- Historia de infra v1 (debugging Chrome/CDP/gateway de OpenClaw) queda solo en `workspace/v1/` — obsoleta en la arquitectura v2, no aplica.
