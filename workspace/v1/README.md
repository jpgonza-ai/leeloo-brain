# Archivo histórico — Leeloo v1 (OpenClaw)

Respaldo curado de la primera versión de Leeloo (agente en OpenClaw), incorporado el 2026-07-02.
Fuente: `Info-1.zip` (respaldo `.openclaw` completo, conservado en `workspace/inbox/`).
La basura del respaldo (perfil/caché de Chrome ~264MB, locks, temporales, scripts de update, credenciales caducas) fue descartada.

## Contenido
- **memory/** — 17 bitácoras diarias (2026-03-04 → 2026-06-17) + `2026-05-19-executive-summary.md`. La historia real de JP + Leeloo.
- **sessions/** — 22 sesiones/trajectories de conversación (`.jsonl`).
- **db/main.sqlite** — base de datos de memoria de OpenClaw (16MB).
- **notas/** — `Notas.docx`, `Taller - Open Claw.docx` (notas propias de JP).
- **media/** — audios generados (resúmenes Morning Brew / CFO Brew, etc.).
- **identity-v1/** — SOUL/USER/IDENTITY/AGENTS/TOOLS/HEARTBEAT/MEMORY.md de la v1. Solo referencia histórica: la identidad v2 actual ya es más rica.

## Qué se destiló a memoria activa v2
- Perfil profesional de JP y pipelines de búsqueda laboral → `identity/USER.md`.
- Contexto personal (Giants, viajes Tahoe/Madrid/Barcelona, newsletters) → `identity/USER.md`.
- Flujos recurrentes (resúmenes de correo por voz, Google Calendar) → `USER.md` + `workspace/MEMORY.md`.

## Qué NO se migró (obsoleto en v2)
- Toda la saga de infraestructura OpenClaw: debugging de Chrome/CDP, puerto 9222, gateway restarts, `size-drop`, etc. No aplica en la arquitectura Claude Code Max.
