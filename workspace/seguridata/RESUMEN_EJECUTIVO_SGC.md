# Seguridata — Mapa de Procesos y Oportunidades de Agentes de IA
### Resumen ejecutivo del Sistema de Gestión de Calidad (30 procesos, 8 áreas)
*Preparado por Leeloo para Juan Pablo · 3-ago-2026 · insumo para pelotear antes de ir con Mario y Patti*

---

## 1. Qué revisé y el hallazgo grande

Revisé los **30 documentos de procesos** del Sistema de Gestión de Calidad de Seguridata, organizados en 8 áreas. Cada proceso está muy bien documentado: diagramas de flujo con roles, sistemas y **OLAs/SLAs (tiempos comprometidos) numéricos** por paso.

**Los tres hallazgos que cambian el pitch:**

1. **Seguridata ya vive de OLAs manuales.** Casi todos los procesos definen tiempos estrictos por paso (ej. primer contacto de cobranza 2 h, respuesta a incidente crítico 2 h, reasignación de lead a 15 días). Hoy el cumplimiento depende de la disciplina humana. Un agente que **vigile OLAs y orqueste hand-offs entre sistemas** es la oportunidad más repetida de toda la empresa.

2. **Seguridata YA usa IA en producción** en al menos 5 procesos (ver sección 3). No hay que convencerlos de "si IA sí o no": el pitch es **"extendamos lo que ya les funciona"**, fricción de adopción bajísima.

3. **El ADN de Seguridata es seguridad documental** (firma electrónica, NOM-151, TSA, resguardo 10 años). Los agentes que **leen, validan y resguardan documentos** (bases de licitación, contratos, cotizaciones, expedientes) no solo automatizan: hablan su idioma y refuerzan su propuesta de valor.

---

## 2. El stack de Seguridata (mapa de sistemas)

- **HubSpot Sales Hub** — columna vertebral del pipeline comercial (marketing, ventas, renovaciones, licitaciones, cotizador).
- **SAP** — facturación y finanzas (prefactura, factura, registro de pagos).
- **Monday** — gestión de tareas, proyectos, licitaciones, adquisiciones/gastos, canales.
- **Freshdesk** — ticketing de soporte a cliente.
- **Jira** (+ Zephyr Scale, Selenium, GitHub, Jenkins, SonarQube) — desarrollo, QA, incidencias.
- **Factorial** — desempeño/talento (RH). **Crehana** — evaluación de candidatos. **Clockify** — tiempos.
- **Otros:** Cotizador Web, Apollo + Google Ads (marketing), Mentimeter (comité de innovación), Drive/Excel, firma electrónica, banca en línea.

> Implicación: los agentes deben ser **multi-sistema**. El mayor dolor no está *dentro* de un sistema, sino en los **puentes entre ellos** (HubSpot↔Monday↔SAP↔Jira↔Freshdesk).

---

## 3. Seguridata YA usa IA aquí (nuestra rampa de entrada)

| Proceso | Uso actual de IA | Cómo lo escalamos a agente |
|---|---|---|
| Adquisiciones/Gastos | "Matriz de Solicitantes Autorizados" consultada con IA | Extender a validar presupuesto, inventario, OC duplicadas y comparar 3 cotizaciones |
| Capacitación interna | IA para informes de brechas y exámenes | Agente que aplica exámenes, detecta brechas y genera microlearning |
| Actualización de precios | IA para benchmark y simulaciones | Agente de pricing con benchmark competitivo + simulación de margen |
| Gestión de producto (MVP/GTM) | IA para competidores, materiales, campañas | Agente de inteligencia de mercado + generador de materiales |
| Distribución de partners | IA para competencia y TAM/SAM/SOM | Agente de due diligence de partners |

**Este es el mejor gancho del pitch:** no venimos a experimentar, venimos a industrializar lo que ya probaron.

---

## 4. Los 5 patrones transversales (donde un agente conecta varias áreas)

Más allá de oportunidades sueltas, hay **5 tipos de agente que se repiten en casi todas las áreas**. Aquí está la tesis de la propuesta:

1. **Vigilante de OLAs + sincronizador de hand-offs.** Monitorea los tiempos comprometidos de cada etapa y sincroniza estados entre HubSpot, Monday, SAP, Jira y Freshdesk; escala antes de que se venza un SLA. *(Aplica a: Ventas, Operaciones, Licitaciones, Renovaciones, Soporte, Cobranza…)*

2. **Generador de documentos.** Propuestas, cotizaciones, contratos, cartas de cierre, PRDs, job postings, informes financieros, materiales comerciales. *(Aplica a: Ventas, Cotizaciones, Jurídico, Entregas, Producto, RH, Finanzas.)*

3. **Lector/extractor documental.** Extrae datos y requisitos de documentos densos: bases de licitación, contratos, CVs, cotizaciones, estados de cuenta. *(Aplica a: Licitaciones, Jurídico, Reclutamiento, Adquisiciones, Conciliación.)* **← el que más resuena con su ADN.**

4. **Triage + ruteo inteligente.** Clasifica y enruta: leads (scoring MQL), tickets de soporte (Freshdesk), bugs (Jira), pagos por riesgo. *(Aplica a: Marketing, Soporte, Desarrollo/QA, Cobranza.)*

5. **Conciliación y validación financiera.** Cruza y valida datos numéricos: cobranza vs SAP, tesorería vs flujo, prefactura vs contrato, bonos/sueldos vs presupuesto. *(Aplica a: toda Admin y Finanzas.)*

---

## 5. Mapa por área (30 procesos)

**Comercial / Desarrollo de Negocios (6):** Marketing-Leads · Ventas · Licitaciones · Renovaciones · Actualización de Precios · Gestión de Producto MVP-GTM.
> *Mejor jugada:* higiene/forecasting de pipeline + captación y calificación de leads + lector de bases de licitación.

**Administración y Finanzas (8):** Prefactura/Factura · Cobranza · Jurídico · Presupuesto · Financiamiento · Informes Financieros · Adquisiciones/Gastos · Tesorería.
> *Mejor jugada:* cobranza multicanal + conciliación financiera + adquisiciones (extiende IA existente).

**Operaciones (4):** Arquitectura · Entregas · Atención de Incidentes · Cotizaciones.
> *Mejor jugada:* triage/auto-respuesta de soporte en Freshdesk + sincronizador Freshdesk↔Jira↔Sales Hub.

**Ingeniería y Desarrollo (3):** Gestión de Producto · Distribución de Producto · Desarrollo tradicional.
> *Mejor jugada:* triage de incidencias en Jira + copiloto de QA/pruebas.

**Recursos Humanos (6):** Feedback · Onboarding · Reclutamiento · Bonos · Sueldos · Capacitación.
> *Mejor jugada:* orquestador de onboarding + screening de CVs + cálculo/validación de compensaciones.

**Innovación (2) + Aseguramiento de Calidad (1):** Innovación Incremental/Disruptiva · Distribución-Integración de Partners · Testing/QA.
> *Mejor jugada:* due diligence de partners (extiende IA existente) + generación/automatización de pruebas.

---

## 6. Top 8 oportunidades priorizadas (toda la empresa)

Ordenadas por combinación de **impacto** y **facilidad de adopción**. Marco cada una como **Quick win** (arrancar ya) o **Estratégica** (mayor alcance).

| # | Oportunidad | Área | Tipo | Por qué |
|---|---|---|---|---|
| 1 | **Cobranza multicanal + conciliación de pagos** | Admin/Finanzas | Quick win | ROI directo en flujo de efectivo; tiempos y canales ya definidos; cierra ciclo en HubSpot+SAP |
| 2 | **Triage + auto-respuesta de soporte (Freshdesk)** | Operaciones | Quick win | Alto volumen, SLAs numéricos claros (crítica 2 h); reduce carga a Desarrollo |
| 3 | **Lector de bases de licitación → checklist + Monday** | Comercial | Estratégica | Evita descalificaciones por requisitos omitidos; puro ADN documental de Seguridata |
| 4 | **Captación y calificación de leads (scoring MQL + ruteo)** | Comercial | Quick win | Alimenta todo el motor de ingresos; ataca captura manual de 8 h y re-trabajo del BDM |
| 5 | **Vigilante de OLAs + sincronizador de hand-offs** | Transversal | Estratégica | El tejido conectivo; ataca la fuga más repetida (cumplimiento de SLAs entre sistemas) |
| 6 | **Adquisiciones: validación + cotización + push comercial** | Admin/Finanzas | Quick win | Ahorro directo (descuentos 3–5%); extiende la IA que YA usan (Matriz de Solicitantes) |
| 7 | **Due diligence de partners (score + competencia + TAM/SAM/SOM)** | Innovación | Estratégica | Comprime el cuello de 5–8 días; extiende IA existente; crece el negocio de canales |
| 8 | **Salud de cuenta y renovación (churn + upselling a 90 días)** | Comercial | Estratégica | Protege y expande ingresos recurrentes; se dispara solo con la automatización de HubSpot |

---

## 7. Mi recomendación para el arranque (qué peloteamos)

Para una **prueba de valor (POC) rápida con Seguridata**, propondría arrancar con **2-3 agentes que combinen ROI medible + adopción fácil + efecto demostración:**

- **#1 Cobranza** — el ROI más fácil de medir (días de cobro, DSO). Habla el idioma del CFO.
- **#2 Soporte/Freshdesk** — el más visible y de mayor volumen; impacto en satisfacción del cliente.
- **#3 o #6** (Licitaciones o Adquisiciones) — el "wow" documental que refuerza su ADN, o el ahorro duro en compras.

**El gancho narrativo:** *"Ya usan IA en 5 procesos. No venimos a experimentar; venimos a industrializar lo que ya funciona y a conectar los puentes entre sus sistemas, con la seguridad y trazabilidad que es su sello."*

---

## 8. Preguntas abiertas para pelotear tú y yo

1. ¿El enganche es por **ROI duro** (cobranza/adquisiciones) o por **efecto wow** (licitaciones/soporte)? Define con qué abrir el pitch.
2. ¿Vamos por **1 agente estrella** bien pulido para el POC, o por **el patrón transversal** (vigilante de OLAs) que enseña alcance de plataforma?
3. ¿Qué tanto peso le damos a su **ADN de seguridad documental** como diferenciador nuestro frente a otros que también ofrecen "IA"?
4. ¿Cómo se reparte el trabajo entre tú, Mario y Patti para el pitch/deck?
5. ¿Modelo comercial: POC pagado, revenue-share, retainer? (define cómo dimensionamos el primer agente).

---

*Detalle proceso por proceso (objetivo, sistemas, roles, OLAs y oportunidades) en `workspace/seguridata/areas/`: COMERCIAL, ADMIN_FINANZAS, OPERACIONES, RH, INGENIERIA, INNOVACION_QA. Análisis a fondo de Ventas en `2026-08-03_review-proceso-ventas.md`.*
