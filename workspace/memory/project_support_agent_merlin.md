---
name: Agente de soporte bajo Leeloo (Merlín)
description: Iniciativa Kaizen para crear un sub-agente que reporte a Leeloo; reenfocado (2026-07-29) a BÚSQUEDA DE TRABAJO. Reutilizar la persona de "Merlín"
type: project
---

# Agente de soporte para Leeloo — "Merlín"

**🔄 REENFOQUE DE ALCANCE (2026-07-29):** Pablo redefinió el reparto de roles.
- **Merlín = copiloto de BÚSQUEDA DE TRABAJO.** Vacantes, posiciones, research de empresas, prep de entrevistas (preguntas, STAR, pitch), seguimiento de aplicaciones y contactos, radar del mercado (Bay Area / SF). Vertical especializado que le **reporta a Leeloo**; nada externo sale sin revisión de Leeloo + OK de Pablo.
- **Leeloo (yo) = día a día operativo de Pablo:** redes sociales, programar, organizar, analizar y ejecutar proyectos con él (el contenido de redes que ANTES era de Merlín ahora lo llevo yo).
- **Why:** Pablo está en búsqueda laboral activa (SF/Bay Area) y quiere un agente dedicado a ese frente, mientras me quiere a mí más cerca de su operación diaria.
- **How to apply:** al armar a Merlín, su "charter" ya NO es contenido de redes → es job-hunting. Su bóveda de conocimiento es ideal para **Obsidian como grafo** (Empresa ↔ Vacante ↔ Contacto/reclutador ↔ Notas de entrevista ↔ material CV/cover letter), estructurada con enlaces `[[empresa]]`, `[[vacante]]`, `[[contacto]]` desde el día uno para que Pablo la navegue. Sigue dependiendo del Puente (F1·5) para research/aplicar en la web.

---

**🧭 DECISIÓN DE ARQUITECTURA (2026-07-30):** Pablo eligió **NO** construir a Merlín como sub-agente de Leeloo. Merlín se queda **viviendo en su proyecto de claude.ai** (app de Claude), donde Pablo le habla directo, en un **chat dedicado solo a Merlín** para no mezclar la búsqueda de trabajo con los demás temas del chat de Telegram con Leeloo.
- **Rol de Leeloo:** mantener el **cerebro** (`workspace/merlin/`: CLAUDE.md, bitácora, CV maestro, criterios) como fuente de verdad, y entregarle a Pablo **artefactos listos para pegar** en el proyecto de claude.ai (Custom Instructions + subir el CV como conocimiento del proyecto).
- **Why:** Pablo quiere un solo hilo limpio con Merlín y a Leeloo enfocada en su operación diaria. La app (web/desktop/móvil) es el mismo proyecto sincronizado; descargar la desktop es solo comodidad, no requisito.
- **How to apply:** cuando cambien criterios/tono/CV, actualizar el cerebro Y darle a Pablo el texto nuevo para re-pegar en claude.ai. Si algún día quiere integración total (Puente + Asana + memoria en un lugar), se migra a sub-agente; por ahora NO.
- **Estado del cerebro (completo 2026-07-30):** constitución con quién es + objetivos + tono/voz + qué nunca hace + perfil + industrias; **criterios de selección** (≤20 días desde consulta, match 80%+, full-time, pref. Bay Area, abierto a remoto); **plataformas** (LinkedIn + GreenHouse + TeamWork Online + BuiltIn + Jobright + careers); **reglas de CV** (7 candados + libertad de diseño) y **CV maestro** en `materiales/`; pipeline = proyecto Asana **"Job Search"** (gid `1216466305816539`), NO crear otro.

---

**🧠 CARPETA-CEREBRO CREADA (2026-07-29):** Pablo pidió armar el cerebro de Merlín con el patrón "3 archivos" de un taller. Existe en `workspace/merlin/` = `CLAUDE.md` (constitución), `README.md` (mapa), `bitacora.md` (memoria) + subcarpetas `empresas/ vacantes/ contactos/ entrevistas/ materiales/`. Es un BORRADOR en papel (el sub-agente Merlín aún NO se construye). Sembrado con el perfil de Pablo + industrias objetivo. Pendiente: fusionar alma del Merlín de claude.ai + rescatar pipelines de v1 + traer CV.

---

**Origen (2026-07-06, dentro de Kaizen):** crear **otro agente, tipo soporte de Leeloo**, que reporte directamente a Leeloo. *(Alcance original = contenido de redes; reenfocado a job-hunting el 2026-07-29, ver arriba.)*

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
