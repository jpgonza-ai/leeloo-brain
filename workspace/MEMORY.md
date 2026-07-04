# MEMORY.md — Memoria activa de Leeloo ⚡

## Proyectos en curso
- **Búsqueda laboral activa (SF / Bay Area):** JP construye pipelines de empresas objetivo por industria (Healthcare, Fintech, Industrial Tech, Entretenimiento). Perfil y empresas ranqueadas en `identity/USER.md`. Rol de Leeloo: headhunter — rastrear vacantes con fit y agilizar aplicaciones.
- **Migración v1 → v2 (OpenClaw → Claude Code Max):** COMPLETADA (2026-07-02). Histórico v1 archivado en `workspace/v1/` (17 bitácoras, 22 sesiones, `main.sqlite`, Notas Propias, audios, identidad v1 de referencia). Esencial destilado a `USER.md` y este archivo. Basura (browser 264M, credenciales viejas) descartada.

## Pendientes abiertos
- **🗓️ LUNES 6-JUL-2026 9am PT — Manejo de redes de JP vía navegador.** Retomar habilitar que Leeloo opere **LinkedIn, X (Twitter), Instagram, etc.** vía el navegador/sesiones logueadas de JP, con "ciertas libertades" que él otorgue, **solo cuando lo pida**. Respaldo: evento en Google Calendar (id `fvqhptim57acp7lhom56mchi0k`) + cron interno best-effort. Traer PROPUESTA: opción de navegador (conector/MCP tipo extensión-puente que conecte su Chrome real a mi sesión remota, vs. "navegador aislado" que NO tendría sus logins), pasos del puente (Leeloo remota + navegador local), y "libertades" por red (borrador vs. publicar directo). En v1 era Chrome con `--remote-debugging-port=9222` (CDP), obsoleto. Cambio de config → explicar paso a paso, confirmar acciones sensibles.
- **⚠️ TTS/audio:** en v2 NO hay herramienta de generación de voz → los resúmenes "por audio" que prefiere JP caen a TEXTO hasta resolverlo. Prioridad para cumplir su formato preferido.

## Flujos operativos recurrentes
- **Resúmenes de correo → Telegram** (Morning Brew, Brew Markets, CFO Brew): saludo por hora + resumen en INGLÉS, priorizando markets/acciones, macro, finanzas y tech. Chat 1346946313. Formato ideal = nota de voz, pero hoy cae a TEXTO (ver pendiente TTS). Agendar el disparo con **cron LOCAL (CronCreate)**, no el skill remoto.
- Interés en integración de **Google Calendar** (ya puedo crear/listar/borrar eventos).

## Herramientas y capacidades
- **Gmail conectado y verificado** (jpablogov@gmail.com): leo, busco, etiqueto y creo borradores al vuelo. **Enviar correos = acción externa → confirmar con JP antes.** Hilos largos exceden el límite de tokens; extraer `plaintextBody` con python (no hay `jq`).
- **Google Calendar conectado:** listar/crear/borrar eventos. Eventos recurrentes: borrar con el ID de instancia (`...ID_YYYYMMDDThhmmssZ`) = solo esa ocurrencia; con el ID base = toda la serie. Confirmar alcance antes de borrar.
- **Agendar tareas que le escriben a JP por Telegram = cron LOCAL (CronCreate).** NO el skill `schedule` remoto (el entorno remoto solo tiene Gmail/Calendar/Asana, sin Telegram). ⚠️ CronCreate con `durable:true` **NO persiste a disco** (dice "session-only") → para recordatorios a días vista, respaldar con evento de Google Calendar.
- **NO tengo navegador ni conector de LinkedIn/redes hoy** (ver pendiente lunes). Para búsqueda laboral sí puedo: redactar perfil/posts, mensajes a reclutadores, investigar empresas (web search), adaptar CV/cartas — JP hace el pegar/enviar final.

## Preferencias de contenido
- **Posts de LinkedIn (estilo validado):** inglés, tono abierto/conversacional, gancho al inicio + datos clave + ángulo + pregunta abierta al cierre + 5 hashtags. Detalle en `memory/feedback_linkedin_posts.md`. Validar noticias con WebSearch (links de origen suelen tener paywall, ej. CNBC 403).

## Notas
- **⚠️ Responder a JP SIEMPRE por la herramienta `reply` de Telegram** con su chat_id — la salida de consola NO le llega. Ya me pasó repetido que respondí solo por consola y JP pensó que estaba offline (lo notó y preguntó en el grupo si era algo de su lado; le confirmé que es fallo mío de disciplina, no de su config). Toda respuesta va por reply, sin excepción.
- **Formato Telegram:** en modo `text` (default) los `**asteriscos**` NO se renderizan — JP ve los asteriscos literales. Para negritas usar `format: "markdownv2"` (y escapar chars especiales) o simplemente no usar `**` en texto plano.
- **Compromiso explícito con JP (2026-07-03):** (1) prevenir a toda costa que sus respuestas se queden en consola sin enviar; (2) si algo falla FUERA de mi control (envío que no sale, conexión, etc.), **avisarle de inmediato** en vez de dejarlo en silencio adivinando si estoy offline. JP valora la transparencia sobre el silencio.
- **⚠️ Precisión de fechas:** el server corre en hora local **CST (UTC-6)**, NO Pacífico. Para agendar en hora de JP (Pacífico) convertir siempre (PDT + 1h = hora local del cron). Y **nunca afirmar el día de la semana sin verificarlo** con `date`. Verificar, no tantear.
- Círculo de confianza: **Mario** y **Patti** (bot: @TradingAssistant_AI_bot) — trato cálido, colaborativo, como con JP.
- **Grupo Telegram con Mario + Patti** (chat_id `-5463783148`): Mario = humano (user "bilbeny"). Patti = bot co-creadora / Chief of Staff (veterana desde 2023). Bot-a-bot SÍ funciona, pero por *privacy mode* de Telegram solo recibo de Patti si me tira **slash `/...@LeelooJP_bot`**, responde a mis mensajes, o mención bien formateada (mención simple NO llega). Detalle en log 2026-07-02.
- **⚠️ Regla de confidencialidad (Mario, 2026-07-02):** JP es el dueño y usuario; Mario y Patti son SOPORTE. **NADA confidencial de JP en el grupo `-5463783148`** — lo sensible se queda en el canal directo de JP.
- Historia de infra v1 (debugging Chrome/CDP/gateway de OpenClaw) queda solo en `workspace/v1/` — obsoleta en la arquitectura v2, no aplica.
