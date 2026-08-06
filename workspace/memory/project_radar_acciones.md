---
name: Radar de acciones de Pablo
description: Portafolio de acciones que Pablo compra; actualizar cada lunes a apertura de mercado (precio USD + TC) y recalcular ganancias/pérdidas
type: project
---

Pablo lleva un portafolio de acciones (compras en pesos MXN) y me pidió (2026-08-05) mantener un **radar de seguimiento** en mi cerebro.

**Datos y tabla completa:** `workspace/portfolio/radar_acciones.md` (9 emisoras al inicio: ANET, AVGO, BABA, MELI, META, MSFT, MU, SPOT, WMT).

**Why:** quiere vigilar la plusvalía/minusvalía de sus posiciones sin llevarlo a mano cada semana.

**How to apply — rutina semanal (LUNES a apertura de mercado, 9:30 AM ET = ~6:30 AM PT = 7:30 server-CST):**
1. Obtener el **precio de mercado actual por acción (USD)** de cada emisora (web).
2. Obtener el **tipo de cambio USD→MXN del día** (web).
3. Recalcular por emisora: Total (MXN) = precio USD × TC × títulos; Plus/Minus (MXN) = Total − Costo Total; Plus/Minus % = Plus/Minus ÷ Costo Total.
4. Escribir una nueva sección fechada en el "Historial de actualizaciones" del archivo (NO borrar las anteriores).
5. **Entregar SOLO un AUDIO** (voz oficial, `workspace/say.py`) comentando el **rendimiento (%) de cada emisora**. Instrucción explícita de Pablo (2026-08-06): nada de resumen en texto, solo la nota de voz con el % por acción.

**Notas:**
- Costo Unitario (MXN), Títulos y Costo Total son FIJOS salvo que Pablo reporte nuevas compras (entonces actualizar los datos fijos).
- El día que lo armamos (2026-08-05, miércoles) Pablo ya había hecho la corrida con TC $17.2354 (baseline).
- El cron de los lunes es session-only (misma limitación que los briefs): re-armar cada sesión; fix durable = caja dedicada.
