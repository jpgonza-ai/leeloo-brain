# Área: Operaciones

### Proceso Arquitectura (SD-OPE-04 PROCESO ARQUITECTURA, v03 — elab. 30 abril 2026)
- **Objetivo:** Que el área de Arquitectura reciba solicitudes del BDM, clasifique el proyecto y elabore la propuesta técnica y económica (incluyendo terceros/proveedores cuando aplique) para dar soporte al ciclo comercial.
- **Sistemas:** HubSpot Sales Hub (etapas, asignación de arquitecto, notas, propuestas y fechas), Monday (proceso de Requerimiento a Desarrollo y recepción de dimensionamiento de desarrollo/QA), correo.
- **Roles clave:** BDM, Responsable de Arquitectura, Arquitecto asignado, VP de Tecnología (validación de viabilidad), área de Desarrollo.
- **Pasos clave y OLAs/SLAs:**
  - BDM mueve etapa SQL → Arquitectura y define si requiere arquitecto (OLA: según etapas de venta).
  - Responsable de Arquitectura asigna arquitecto en Sales Hub (OLA: 1 día).
  - Verificación de catálogo de proveedores autorizados (OLA: 1 día hábil).
  - Clasificación del proyecto y compromiso de tiempos: pequeño 4 días hábiles, mediano 8 días hábiles, grande 8–12 días hábiles (OLA de clasificación: 1 día).
  - Inicio de elaboración de propuesta / solicitud a proveedor (OLA: 1 hora).
  - Validación de viabilidad con VP de Tecnología (OLA: 1 día).
  - Requerimiento a Desarrollo en Monday y recepción de dimensionamiento desarrollo/QA (OLA: 2 días hábiles cada uno).
  - Ajuste de propuesta vía tarea en Monday (OLA: 1 a 2 días).
- **🎯 Oportunidades de agente IA:**
  - **[Quick win]** Agente que, al asignarse el arquitecto, precompile en Sales Hub el "expediente del negocio" (notas de reuniones, requerimiento, historial) para el paso 11, reduciendo tiempo de preparación de propuesta.
  - **[Quick win]** Agente que sugiera la clasificación del proyecto (pequeño/mediano/grande) y proponga OLA/fecha de entrega automáticamente según criterios del paso 1, evitando estimación manual.
  - **[Estratégico]** Agente que consulte el catálogo de proveedores autorizados y recomiende el tercero adecuado según tipo de proyecto, y solicite/integre la propuesta técnica-económica del proveedor.
  - **[Estratégico]** Agente que orqueste el hand-off Sales Hub ↔ Monday (requerimiento a Desarrollo, recepción de dimensionamiento) y actualice fechas planeadas automáticamente, vigilando incumplimiento de OLAs.

### Proceso Entregas — Entrega de Producto o Servicio al Cliente (SD-OPE-04 PROCESO ENTREGAS, v03 — elab. 13 marzo 2026)
- **Objetivo:** Entregar al cliente el producto/servicio vendido, desde el kickoff interno hasta la carta de cierre firmada, coordinando postventa, desarrollo, integraciones e insumos.
- **Sistemas:** HubSpot Sales Hub (etapas, plan de trabajo, fechas, carta de cierre), Project (cronograma), Jira (reporte y seguimiento de incidentes durante implementación). Prerrequisito: factura o contrato firmado.
- **Roles clave:** BDM, Arquitecto, Responsable de Operaciones, Gerente de Operaciones, Ingeniero de Postventa, QA, Desarrollo, Cliente.
- **Pasos clave y OLAs/SLAs:**
  - BDM mueve a etapa Kickoff interno; tarea/correo a Operaciones (OLA: 2 horas).
  - Responsable de Operaciones asigna Ingeniero de Postventa en Sales Hub (OLA: 4 horas).
  - Kickoff interno BDM+Arquitecto entregan a postventa (OLA: 2 días).
  - Postventa elabora cronograma en Project (OLA: 2 días); valida con Desarrollo/Integraciones fecha de liberación (OLA: 1 día).
  - Sube plan de trabajo a Sales Hub (OLA: 1 hora); Kickoff con cliente (OLA: 2 horas); coordina fechas (OLA: 2 horas).
  - Coordina insumos (HSM, equipo) con Admin/Finanzas (OLA: 4 horas la solicitud).
  - Prepara implementación y check list (OLA: 3 horas).
  - Incidentes en implementación: reporte en Jira a QA/Desarrollo (OLA: 5 horas); correcciones (OLA: 1 día).
  - Carta de cierre: elaboración y entrega (OLA: 1 día hábil); firma del cliente (OLA: no definido).
- **🎯 Oportunidades de agente IA:**
  - **[Quick win]** Agente que valide el prerrequisito (factura/contrato firmado) y arme automáticamente el borrador de cronograma en Project a partir del alcance y entregables del negocio en Sales Hub.
  - **[Quick win]** Agente que genere el documento check list de configuraciones (paso 7a) y la carta de cierre (paso 14) a partir de la información del proyecto, y dé seguimiento a la firma pendiente (OLA sin definir).
  - **[Estratégico]** Agente que monitoree en tiempo real las OLAs de la entrega y escale al Gerente de Operaciones ante retrasos, actualizando etapas y fechas en Sales Hub automáticamente.
  - **[Estratégico]** Agente puente Sales Hub ↔ Jira que sincronice el estado de incidentes de implementación con la etapa del negocio y notifique al cliente/BDM sin intervención manual.

### Proceso Atención de Incidentes (SD-OPERACIONES-04, v03 — elab. 12-11-2025)
- **Objetivo:** Atender solicitudes de soporte del cliente (incidentes, dudas, asesoría) recibidas por correo, resolverlas o escalarlas a Desarrollo/QA, y cerrar el ticket con aceptación del cliente.
- **Sistemas:** Freshdesk (ticketing, generación automática de ticket y respuesta), Jira (escalamiento y seguimiento a Desarrollo/QA), correo (soporte@ / ayuda@seguridata.com).
- **Roles clave:** Cliente, Ingeniero de Soporte, QA, Desarrollo.
- **Pasos clave y OLAs/SLAs:**
  - Generación automática de ticket en Freshdesk y respuesta al cliente.
  - Análisis de la solicitud (OLA: máx. 2 horas); solicitud de info adicional (OLA: 5 min); validación de solución (OLA: 30 min).
  - **SLA de respuesta al cliente (soporte directo):** crítica 2 h, alta 4 h, media 7 h, baja 8 h.
  - Escalamiento a Jira (QA/Desarrollo): revisión de avance (OLA: 5 horas hábiles tras reporte); análisis (5 horas hábiles); documentación como nota interna (10 min); asignación a Desarrollo (10 min).
  - **SLA de entrega de solución (escalado):** crítica 8 h, alta 2 días, media 40 h, baja 80 h.
  - Cierre: notificación al cliente, aceptación por correo y cambio de estado a "cerrado" en Freshdesk y Jira.
- **🎯 Oportunidades de agente IA:**
  - **[Quick win]** Agente de triage que clasifique automáticamente el ticket de Freshdesk por prioridad (crítica/alta/media/baja) y tipo, asignando SLA y ruteando al ingeniero correcto.
  - **[Quick win]** Agente de respuesta que redacte la solicitud de información adicional al cliente y sugiera solución con base en el histórico de tickets/base de conocimiento (asistiendo pasos 4, 8 y 9).
  - **[Estratégico]** Agente que sincronice Freshdesk ↔ Jira, actualice estados ("Progreso", "Solventado", "Cerrado") y vigile el cumplimiento de SLAs, escalando antes de vencerse.
  - **[Estratégico]** Agente de auto-resolución de incidentes recurrentes/de configuración (sin modificar código) que documente la solución en el ticket, reduciendo carga a Desarrollo/QA.

### Proceso de Cotizaciones (SD-OPERACIONES 04 ProcesodeCotizaciones, v02 — elab. mayo 2026)
- **Objetivo:** Generar la cotización y propuesta económica para el cliente por dos caminos (con o sin arquitecto), aplicando políticas de descuento y autorizaciones antes de la entrega.
- **Sistemas:** HubSpot Sales Hub (cotizador integrado para soluciones transaccionales, etapas, notificación a BDM), Cotizador Web (arquitectura, genera cotización en PDF).
- **Roles clave:** BDM, Arquitectura, Dirección Comercial.
- **Pasos clave y OLAs/SLAs:**
  - Camino sin arquitecto: cotización con cotizador de Sales Hub (NOM, TSA, Premium sin flujos, Logalty), con descuento máximo por política (OLA: 2–4 horas).
  - Camino con arquitecto: cotización con Cotizador Web, genera PDF y sube a Sales Hub notificando al BDM (OLA: 2 horas tras contar con la propuesta).
  - Propuesta económica del BDM (OLA: 3 horas después de tener la cotización).
  - Autorización de descuento con Dirección Comercial (OLA: 3 horas).
  - Entrega de propuesta comercial y económica al cliente (OLA: 3 horas).
- **🎯 Oportunidades de agente IA:**
  - **[Quick win]** Agente que arme automáticamente la propuesta económica en PDF a partir de la cotización (Sales Hub o Cotizador Web) usando plantilla de marca, ahorrando las 3 horas del paso 3.
  - **[Quick win]** Agente validador de políticas de descuento que verifique si el descuento excede el máximo permitido y dispare/enrute la autorización a Dirección Comercial automáticamente.
  - **[Estratégico]** Agente que enrute la solicitud al camino correcto (con/sin arquitecto) según tipo de solución y aplique el cotizador adecuado sin decisión manual del BDM.
  - **[Estratégico]** Agente que dé seguimiento a las autorizaciones de Dirección Comercial y escale por vencimiento de OLA, manteniendo trazabilidad en Sales Hub.

## Top 3 oportunidades del área (priorizadas)

1. **Triage + auto-respuesta de incidentes en Freshdesk (Atención de Incidentes) — [Quick win].** Es el proceso de mayor volumen y con SLAs numéricos claros (crítica 2 h / alta 4 h de respuesta); un agente que clasifique, rutee y sugiera solución con base en histórico reduce carga directa y riesgo de incumplimiento de SLA de forma medible.

2. **Sincronizador Freshdesk ↔ Jira y Sales Hub ↔ Jira/Monday con vigilancia de OLAs — [Estratégico].** Los tres procesos operativos dependen de hand-offs manuales entre sistemas y de mover etapas/estados; un agente orquestador que sincronice estados, actualice fechas y escale antes de vencer OLAs elimina el punto de fuga más transversal del área.

3. **Generador de propuestas y cotizaciones con validación de descuentos (Cotizaciones + Arquitectura) — [Quick win].** Los pasos de elaborar propuesta económica en PDF y validar políticas de descuento son repetitivos y de tiempo fijo (3 h + 3 h); automatizarlos acelera el ciclo comercial y garantiza cumplimiento de políticas antes de llegar al cliente.
