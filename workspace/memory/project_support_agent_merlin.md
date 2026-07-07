---
name: Agente de soporte bajo Leeloo (Merlín)
description: Iniciativa Kaizen para crear un sub-agente de soporte (contenido de redes) que reporte a Leeloo; reutilizar la persona de "Merlín"
type: project
---

# Agente de soporte para Leeloo — "Merlín"

Idea de JP (2026-07-06, dentro de Kaizen): crear **otro agente, tipo soporte de Leeloo**, que se encargue del **contenido de redes sociales** y lo **revise con Leeloo antes de publicar** — que **reporte directamente a Leeloo**.

**Why:** JP quiere delegar la producción de contenido de redes a un agente de apoyo, manteniendo control (revisión antes de publicar). Ya tenía creado un agente llamado **Merlín** en Claude (dijo "hace días"); quiere aprovecharlo en vez de partir de cero.

**How to apply / decisiones de diseño:**
- **Verificado (2026-07-06):** Merlín NO existe dentro del entorno Claude Code de Leeloo (no está en la lista de agentes ni hay `.claude/agents/`). Vive en claude.ai (Proyecto o Agente) — pendiente que JP confirme cuál.
- Distinción clave que le expliqué a JP: de Merlín lo reutilizable es su **ALMA** (personalidad, nombre, propósito, prompt). El **MÚSCULO** (Telegram, puentes, autonomía, reportar a Leeloo) NO vive en un Proyecto de claude.ai; se conecta en un entorno como el de Leeloo (Claude Code + conectores + plugin Telegram + cron). El músculo se arma aquí en cualquier caso.
- **Recomendación dada:** opción A = portar la esencia de Merlín a un **sub-agente bajo el entorno de Leeloo** (custom subagent), que Leeloo invoca; redacta contenido y se lo reporta a Leeloo para revisión; nada se publica sin OK de JP. (Opción B, más ambiciosa: agente separado tipo Patti con su propio bot/identidad/autonomía — más infra y cambio de config.)
- **Caveat / dependencia:** hoy NO hay capacidad de publicar en redes (falta el conector de navegador = el "puente", tema de la sesión del **lunes 6-jul... (ver pendiente)**). Hasta habilitarlo, el agente solo puede DEJAR el contenido listo; publicar es manual (JP).

## Task en Asana
- Capturada en el Backlog de Kaizen (2026-07-06) por petición de JP: task GID **1216328208091783** — "🤖 Agente de soporte (Merlín) — contenido de redes que reporta a Leeloo". Contiene todo el contexto/decisiones de arriba. Retomar desde ahí.

## Pendiente de JP (para avanzar)
1. Dónde vive Merlín exactamente (Proyecto vs Agente en claude.ai).
2. Que copie y pegue las **instrucciones/personalidad actuales de Merlín** → Leeloo revisa y arma su "charter" portado, y lo confirma por texto ANTES de crear nada (regla: confirmar antes de entregables).
