# bitacora.md — La memoria de Merlín 📓

> Qué pasó, qué se decidió, qué sigue pendiente. Orden cronológico inverso (lo más nuevo arriba).
> Merlín escribe aquí cada movimiento: aplicaciones, entrevistas, hallazgos, decisiones.

---

## Pendientes / próximos pasos
- [x] Criterios de selección de vacantes fusionados en `CLAUDE.md`. ✅ 2026-07-30
- [x] Constitución del Merlín de claude.ai fusionada en `CLAUDE.md` ✅ 2026-07-30 (era el docx `ClaudeMD.Merlin` del 29-jul; ya integrado y ampliado).
- [x] Tono y voz definidos por Pablo ✅ 2026-07-30: amigable, directo, no tan formal; le dice "Pablo"; bromista/sarcástico/pícaro; sugiere y cuestiona (Big Picture); feedback mutuo. Ya en `CLAUDE.md`.
- [ ] Sembrar `empresas/` con los pipelines ranqueados de v1 (Healthcare, Fintech, Industrial Tech, Ticketing).
- [ ] Recuperar del archivo v1 (`workspace/v1/`) el trabajo previo de headhunter/pipelines para no empezar de cero.
- [x] Traer el CV vigente de Pablo a `materiales/`. ✅ 2026-07-30
- [ ] Esperar el **Puente** (navegador) para research/aplicación web automatizada.

---

## Bitácora

### 2026-07-30 — Plantilla de Cover Letter recibida
- Pablo compartió su molde de cover letter (`materiales/CoverLetter_JP_template_2026-07-30.pdf`; estructurado en `materiales/CoverLetter_JP_template.md`). Ejemplo real: Anthropic - Strategic Account Executive, Healthcare.
- **Reglas de formato (no romper):** nunca más largo que el molde (1 página); máximo 2 o 3 párrafos; **sin guiones medios (—)**, usar comas u otra puntuación; siempre en inglés; adaptar empresa/rol/experiencia al job description sin inventar.
- Estructura: encabezado + fecha + destinatario + `Re: [rol]` + saludo + 3 párrafos (hook / evidencia con métricas / diferenciador + misión + cierre) + `Warm regards,` + firma. Ya en `CLAUDE.md`.
- Merlín-app: Pablo subió el molde a "Context" del proyecto y se le dio una línea de reglas para pegar en Instructions.

### 2026-07-30 — Plataformas de búsqueda + proyecto Asana ya existente
- **Plataformas:** además de LinkedIn (grueso de vacantes), Pablo usa y le funcionan **GreenHouse, TeamWork Online, BuiltIn, Jobright** y el **careers directo de cada empresa**. Merlín no debe casarse solo con LinkedIn.
- **Asana:** NO crear tablero nuevo. Ya existe el proyecto **"Job Search"** (gid `1216466305816539`, dueño Pablo, 107 tareas / 16 abiertas al 2026-07-30). Pipeline por secciones: 🎯 To Apply → ⚡ Active → 📜 Applied → 📞 Recruiter Screen → 🎤 Interviews → 🏆 Offer → ❌ Closed. Merlín trabaja sobre ese proyecto.
- Pablo compartió los **criterios de selección de vacantes** (ya en `CLAUDE.md`): (1) publicadas hace ≤20 días desde la fecha de consulta; (2) match 80%+ contra su CV (tareas, capacidades, experiencia, key words); (3) tiempo completo; (4) preferente SF / Bay Area; (5) abierto a remoto.

### 2026-07-30 — CV maestro recibido
- Pablo compartió su última versión de CV (`materiales/CV_JP_master_2026-07-30.pdf`). Guardada también versión estructurada `materiales/CV_JP_master.md`, fuente de la que se derivan todas las variantes por vacante.
- **Regla de formato dada por Pablo (no romper):** respetar secciones y su contenido → Professional Summary; Core Competencies y Technical Skills (se pueden separar o juntar, única libertad); Professional Experience con fechas y **orden cronológico inverso** intactos; Education. Al adaptar por vacante solo se ajusta énfasis/wording dentro de las secciones.
- **Reglas extra (Pablo, mismo día):** Merlín puede ajustar palabras o líneas completas para hacer match con las "Key Words" del job description (tipo ATS); el CV **nunca pasa de 2 páginas**; **siempre en inglés**.

### 2026-07-29 — Decisión: control de versiones de CV
- Pablo decidió que los CVs NO se adjuntan en Asana (Leeloo no puede subir archivos ahí, solo leer). Cada versión de CV vive en `materiales/` con nombre claro (ej. `CV_Amazon_SrPartnerships.md`), enlazada a su `[[empresa]]`/`[[vacante]]` y con fecha. El SEGUIMIENTO de qué versión se usó para qué vacante se lleva aquí en la bitácora. Esa es la fuente de control; Asana solo apunta a ella si hace falta.

### 2026-07-29 — Nace el cerebro de Merlín
- Pablo definió el reenfoque de Merlín: de "contenido de redes" → **búsqueda de trabajo** (vacantes, empresas, entrevistas, seguimiento, materiales).
- Leeloo creó esta carpeta-cerebro con el patrón de 3 archivos (constitución / mapa / memoria) visto en un taller.
- Estructura base creada: `empresas/`, `vacantes/`, `contactos/`, `entrevistas/`, `materiales/`.
- Estado: BORRADOR para revisión de Pablo. Aún no se ha construido el sub-agente Merlín como tal ni se ha sembrado contenido real.
- Decidido: Obsidian será la ventana de Pablo sobre este cerebro (grafo `[[enlaces]]`).
