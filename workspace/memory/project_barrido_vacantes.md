---
name: Barrido de vacantes en Gmail (2x/día)
description: Rutina recurrente para revisar Gmail 2 veces al día y filtrar correos de sitios de empleo según el perfil de Pablo
type: project
---

**Rutina nueva (Pablo, 2026-08-27):** revisar la bandeja de Gmail de Pablo (jpablogov@gmail.com) **dos veces al día, ~11:00 y ~19:00 hora de California** (= 12:00 y 20:00 CST del sistema, que corre en America/Mexico_City), todos los días.

**Qué hacer en cada barrido:**
1. Buscar correos de **sitios de búsqueda de empleo** (BuiltIn, LinkedIn job alerts, Glassdoor, Indeed, Jobright, ZipRecruiter, Wellfound, Otta, Greenhouse, etc.).
2. Evaluar si el contenido anuncia vacantes que encajen con el perfil de Pablo.
3. **Correos con al menos una vacante relevante → DEJARLOS en la bandeja** (no archivar).
4. **Correos de sitios de empleo SIN nada relevante → archivar** (unlabel_thread quitando INBOX), igual que los Brews.
5. **NO tocar** correos que no sean de sitios de empleo (ej. hilos personales como el de Rashmi, newsletters editoriales de LinkedIn).

**⚠️ MODO SILENCIOSO (Pablo, 2026-08-27):** NO mandar resumen por Telegram en cada barrido. Pablo entiende que **lo que queda en la bandeja = lo que vale la pena revisar**. Solo escribirle si algo falla (ej. no se puede acceder a Gmail). El primer barrido (2026-08-27) SÍ llevó resumen porque era la puesta en marcha; de ahí en adelante es silencioso.

**Roles objetivo (los de mejor respuesta con Merlín):** Strategic Partnerships, Account Management, Partner Development, Enterprise Account Management. También cuentan adyacentes fuertes: Client Partner, Strategic Account Executive, roles con ángulo healthcare/payments/fintech.

**Perfil de Pablo (CV "JP_Resume_Std", 2026-08-27):** 15 años en partnerships / account management / vendor finance (Amex, GE Capital, DLL, Credijusto/Covalto, CSI Leasing). Payments/fintech/lending + healthcare finance. Fortalezas: construir canal de socios desde cero, expansión de portafolio ($10M en DLL), negociación ejecutiva con CFOs/CEOs (cerró acuerdo Amazon en Amex), análisis de crédito. Bilingüe EN/ES. Radica en Sunnyvale, CA. Master en Digital Marketing (UNIR 2025) + certificaciones (Yale Financial Markets, Google Agile PM, IBM Data Science).

**Why:** Pablo está en búsqueda activa de empleo; quiere que le pre-filtre el ruido de los job boards y solo destaque lo que vale la pena, manteniendo la bandeja limpia.
**How to apply:** ejecutar en cada disparo de cron (jobs 9044e37e @12:06 y 72b90b1f @20:09 CST, session-only, expiran a 7 días → re-armar). Trabajar EN SILENCIO (sin Telegram). Manejar el overflow de tokens de get_thread con el patrón de parseo de htmlBody (guardar a tool-results → python strip HTML → grep títulos).

**Limitación pendiente:** los crons son session-only + expiran a 7 días (durable:true no persistió en este runtime). El fix a prueba de fallos es la infra de Helsinki (tema Mario/Patti, ya pendiente).
