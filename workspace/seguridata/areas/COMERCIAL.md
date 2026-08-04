# Área: Comercial / Desarrollo de Negocios

Insumo para el pitch de agentes de IA a Seguridata. Basado en los 6 procesos oficiales del área Comercial / Desarrollo de Negocios. Stack conocido: HubSpot Sales Hub (columna vertebral del pipeline), SAP (facturación), Monday (tareas/renovaciones).

---

### Proceso Marketing – Leads (SD-COMERCIAL-01, V4)

- **Objetivo:** Captar, registrar, enriquecer, contactar y calificar leads de múltiples fuentes (inbound y outbound) hasta convertirlos en MQL/SQL y entregarlos al BDM.
- **Sistemas:** HubSpot (Marketing Hub y Sales Hub / CRM), Monday (solicitud de campañas ABM y outbound), Google Ads, Apollo (obtención de contactos ABM), Canva (materiales), correos inbound (info@, informes@, ventas@, sales.marketing@, info-firma@seguridata.com), formularios HubSpot, WhatsApp/teléfono.
- **Roles clave:** SDR (y en su ausencia equipo Marketing), Marketing / Responsable de Marketing, Infraestructura-mensajería (conmutador), Proveedor (Google Ads), Solicitante de campaña, Director/Dirección Comercial, BDM, Agente Certificador.
- **Pasos clave y OLAs/SLAs:**
  - Recepción de mailing inbound: OLA diario; primer contacto en máx. 2 horas; registro/análisis en CRM 8 horas hábiles.
  - Llamadas telefónicas inbound: registro inmediato en la llamada.
  - Automatización HubSpot: registra lead como "nuevo", valida no-duplicados y campos obligatorios (nombre, cargo, correo, teléfono, empresa, país/estado, sector gobierno/IP, giro/dependencia, interés, desafíos); si interés = "Certificado" se deriva a proceso de emisión de certificados (inmediato).
  - Contacto/actualización a etapa "Contactado": 1 a 3 días hábiles.
  - Leads de licitación por Marketing-SDR: recepción inmediata; regla de descarte si ya hay 3 invitaciones y Seguridata no está; decisión con Director Comercial en 3 horas.
  - Webinars: secuencia post-evento de 3 correos durante 3 semanas; campañas ABM: secuencia de 6 correos ejecutada 6 semanas, seguimiento SDR (llamadas/WhatsApp) 3 meses, base de 30 contactos en Apollo en 4 hrs.
  - Subproceso Prospección: registro/enriquecimiento 2 horas; verificar registro previo en HubSpot 30 min; perfilamiento (BANT: interés, rol, decisor, presupuesto, tiempo) de 2 horas a 2 días.
  - Subproceso Calificación: scoring MQL en 2-3 horas (modelo <50 = no calificado, 50-100 = MQL); requisito para MQL: necesidad confirmada + reunión agendada y presentada al BDM; asignación de BDM por reglas (renovaciones, gobierno uno-a-uno, IP por vertical, self-service a BDM Junior SMB / Agente Certificador). Preparación de discovery por BDM: 3 días.
- **🎯 Oportunidades de agente IA:**
  - **(Quick win)** Agente que lea los buzones inbound (5 correos), extraiga y normalice los datos obligatorios del prospecto (empresa, sector gobierno/IP, giro, interés) y precargue/enriquezca el registro en HubSpot, reduciendo la OLA de 8 hrs y evitando información incompleta.
  - **(Estratégico)** Agente de scoring/calificación MQL que aplique el modelo (0-100) sobre las respuestas del perfilamiento y proponga la asignación de BDM según las reglas de ruteo (gobierno/IP/self-service/vertical), con handoff estandarizado para evitar el "re-trabajo del BDM" que el propio doc marca como riesgo.
  - **(Quick win)** Agente que genere el borrador de las secuencias de correos (webinar 3 correos / ABM 6 correos) y materiales base (One Page, FAQ, script) a partir del brief, acelerando OLAs de días.
  - **(Estratégico)** Agente SDR de perfilamiento que conduzca el cuestionario diferenciado Gobierno vs IP (contexto, dolor, marco regulatorio NOM-151/firma, presupuesto) por chat/correo y documente todo en CRM automáticamente.

---

### Proceso de Ventas (SD-COMERCIAL-02, V3)

- **Objetivo:** Convertir el lead calificado en negocio cerrado y cobrado, moviendo la oportunidad por el pipeline de HubSpot (MQL 1% → SQL 5% → Arquitectura 10% → Propuesta 30% → Negociación 50% → Aceptación verbal 70% → Contrato firmado 90% → Prefactura/Facturación 95% → Cobrado 100%).
- **Sistemas:** HubSpot Sales Hub (pipeline, notas, tareas, automatizaciones, playbooks), SAP (prefactura/factura), cotizador (con tabla de descuentos), correo electrónico, carpeta electrónica y física (resguardo jurídico).
- **Roles clave:** BDM, Responsable de Arquitectura / Arquitecto (Bernardo), Jurídico (Carlos Jiménez), Admin y Finanzas (Jesús), Sales Admin, Ejecutivo de Administración y Finanzas, Dirección Comercial / General, VP Tecnología.
- **Pasos clave y OLAs/SLAs:**
  - Asignación de lead calificado a BDM: automática/inmediata; documentar 1a entrevista (playbook de 7 preguntas) en 8 hrs hábiles; concluir reunión y decidir SQL/perdido en 1 hr hábil.
  - MQL→SQL: máximo 15 días (reasignación automática de BDM si no hay avance en 15 días; notificaciones semanales de estacionalidad). SQL→Arquitectura: máx. 1 semana.
  - Arquitectura asigna arquitecto: 1 día hábil. Elaboración de propuesta técnica: proyecto pequeño 4 días, mediano 8 días, grande 8-12 días hábiles. Mover a Propuesta 30%: 1 hr hábil.
  - Adecuaciones a propuesta: 1 a 5 días. Propuesta técnica → Negociación final: máx. 4 meses. Negociación → Aceptación verbal 70%: máx. 1 mes.
  - Automatizaciones al llegar a 70%: disparo de solicitud de fianza (Admin/Finanzas) y de contrato (Jurídico). Revisión jurídica: contrato cliente/aliado 2 días, NDA/otras 1 día, proceso abreviado 1 día; info faltante 4 hrs. Firma: inicia con Seguridata en 2 hrs hábiles; resguardo mínimo 10 años. Aceptación verbal → Contrato firmado 90%: máx. 1 semana.
  - Fianza: 1 a 5 días. Prefactura 95%: inmediato. Sales Admin captura en SAP (contrato/OC si monto < 10,000) en 4 hrs; Admin/Finanzas autoriza prefactura en 2 hrs y elabora factura en 2 hrs; sube XML/PDF en 2 hrs.
  - Cobranza: primer contacto 2 hrs, segundo contacto a 7 días naturales; política de pago 50% inicio / 50% entrega; reprogramación y notificación de morosidad al BDM. Cierre "Cobrado 100%".
  - Tabla de descuentos: 0-5% Ejecutivo Comercial, 6-15% y 16-25% Dirección Comercial, >25% Dirección General; ningún descuento automático, todo requiere contraprestación.
- **🎯 Oportunidades de agente IA:**
  - **(Estratégico)** Agente de higiene y forecasting de pipeline: detecta negocios estancados que rompen las OLAs (MQL→SQL 15 días, →Negociación 4 meses, →Aceptación 1 mes), avisa al BDM/dirección y sugiere próxima acción; alto impacto porque hoy depende de disciplina manual de cada BDM.
  - **(Quick win)** Agente que redacte el borrador de propuesta técnico-comercial y la nota de resumen de la reunión (a partir del playbook de 7 preguntas y los datos del negocio), liberando tiempo de Arquitectura y BDM.
  - **(Quick win)** Agente validador de prefactura: verifica el checklist de datos SAP (solución de catálogo, número de oportunidad, correos de facturación/cobranza, cuerpo de factura) antes de solicitar, previniendo cancelaciones (que el doc marca como afectación a ISR/flujo).
  - **(Estratégico)** Agente de cobranza que orqueste los contactos (correo/teléfono/WhatsApp) según la política 50/50 y las fechas programadas, detecte "stoppers" (errores de factura, problemas de entrega) y escale morosidad al BDM.
  - **(Quick win)** Agente que aplique la tabla de descuentos: valida el % solicitado, exige la contraprestación y ruta la autorización al nivel correcto (Ejecutivo/Dir Comercial/Dir General).

---

### Proceso de Licitaciones (SD-COMERCIAL-03, V1/V2)

- **Objetivo:** Gestionar la participación en licitaciones desde la invitación hasta la adjudicación, coordinando áreas (arquitectura, legal, técnica) y entregables dentro de los plazos del convocante.
- **Sistemas:** HubSpot Sales Hub / CRM (pipeline de licitación), Monday (proyecto de licitación, asignación de tareas y tiempos a áreas), CompraNet / portal del cliente, correo electrónico.
- **Roles clave:** BDM (dueño operativo), Sales Admin, Representante legal, Comité de proyectos (Dir General, VP Tecnología), Convocante, áreas de Arquitectura/Legal/Operaciones.
- **Pasos clave y OLAs/SLAs:**
  - Dar de alta el negocio en el pipeline de licitación: 1 hr hábil; análisis de bases: 2 hrs hábiles; generar proyecto y asignar tareas en Monday: 3 hrs hábiles.
  - Junta de aclaraciones: convocatoria con al menos 24 hrs de anticipación; análisis de respuestas 2 hrs después de la junta; convoca comité de proyectos si es necesario; documentar no-participación y mover a perdido 2 hrs tras la decisión.
  - Recopilación de información / checklist: entregar 2 a 3 días hábiles antes de la fecha; convocar a Sales Admin para checklist de entregables al menos 2 días antes.
  - Armado de carpeta (Sales Admin) 1 día; supervisión y VoBo del BDM 1 día; entrega al responsable (rep. legal) al menos 1 día antes de la fecha de entrega (tarea cerrada en Monday). Entrega física fuera de ciudad: tarea en Monday para vuelos.
  - Contraoferta/negociación: según tiempos de la licitación. Adjudicación → cambia CRM a "adjudicación" y genera tareas de implementación en Monday (tablero de Operaciones); no adjudicación → CRM a "perdido".
- **🎯 Oportunidades de agente IA:**
  - **(Estratégico)** Agente lector de bases de licitación: extrae requisitos administrativos/jurídicos/técnicos, fechas clave y entregables, y genera automáticamente el checklist y el proyecto con tareas y tiempos en Monday; alto impacto por el volumen de lectura manual y el riesgo de omitir requisitos.
  - **(Quick win)** Agente que arme y prepare el borrador de preguntas para la junta de aclaraciones a partir de las bases.
  - **(Quick win)** Agente de control de fechas/entregables que vigile las OLAs de la licitación (2-3 días antes, 1 día antes) y alerte a BDM/áreas ante riesgo de incumplimiento.
  - **(Estratégico)** Agente que ayude al comité a decidir participación (go/no-go) resumiendo bases, competencia probable y ajuste al portafolio Seguridata.

---

### Proceso de Renovaciones (SD-COMERCIAL-05, V2)

- **Objetivo:** Anticipar y gestionar la renovación de contratos existentes (con upselling) desde la detección temprana hasta la nueva facturación y la creación del negocio del siguiente ciclo.
- **Sistemas:** HubSpot Sales Hub (detección automática, pipeline de renovaciones, account planning, evidencias), Monday (tareas a Operaciones para pólizas), SAP (facturación), correo.
- **Roles clave:** BDM (responsable principal), Operaciones (pólizas), Jurídico, Administración y Finanzas, Sales Admin, Dirección Comercial (autorización de descuentos).
- **Pasos clave y OLAs/SLAs:**
  - Automatización HubSpot: detecta renovación próxima y genera tarea al BDM al menos 90 días antes del cierre (OLA permanente).
  - Preparación de reunión (account planning, tickets, satisfacción, riesgo): 2 días. Contacto inicial y cuestionario diferenciado (Gobierno / Enterprise-IP / SMB): al menos 6 meses antes de la renovación.
  - Propuesta económica con upselling: al menos 6 meses antes; entrega de propuesta 2 hrs (candado: sin archivos no avanza). Negociación / autorización de descuento a Dir Comercial: 2 hrs.
  - Aceptación (orden de compra, candado de evidencia): 2 hrs. Contrato/anexo + firmas por Jurídico: 2 hrs. Fianza si aplica: 2 hrs. Emisión de pólizas por Operaciones vía Monday: 2 días. Aceptación de entrega de pólizas/fianza: 2 días.
  - Prefactura/factura: 5 hrs después de la aceptación. Cobranza continua hasta pago (validar deudas históricas). Al emitir factura, BDM genera el nuevo negocio en el pipeline de renovaciones con la fecha del siguiente año y documenta lecciones aprendidas.
- **🎯 Oportunidades de agente IA:**
  - **(Estratégico)** Agente de "salud de cuenta" para renovación: al dispararse los 90 días, arma el account planning (tickets, satisfacción, riesgo, uso) y un score de riesgo de churn + oportunidades de upselling, entregando al BDM la reunión preparada. Alto impacto en ingresos recurrentes.
  - **(Quick win)** Agente que genere el borrador de la propuesta económica de renovación aplicando nuevos precios y la política de descuentos, y prepare el cuestionario según segmento (Gobierno/IP/SMB).
  - **(Quick win)** Agente que orqueste los candados y tareas (pólizas en Monday a Operaciones, fianza, contrato) y verifique que se suban las evidencias requeridas para avanzar de etapa.
  - **(Estratégico)** Agente que cierre el ciclo creando automáticamente el negocio del siguiente año y sintetice "lecciones aprendidas" a partir del histórico del cliente.

---

### Proceso de Asignación-Actualización de Precios (SD-COMERCIAL-04, V2)

- **Objetivo:** Revisar y ajustar semestralmente los precios de productos/soluciones (y fijar el precio inicial de productos nuevos), y ejecutar el ajuste con clientes.
- **Sistemas:** Monday (solicitud de precio de producto nuevo, firma/aprobación de propuesta), HubSpot (account planning, ajuste de valores de negocios), IA (benchmark, simulaciones), documentos de aprobación firmados.
- **Roles clave:** Dirección Comercial (responsable), Dirección General (aprobación), Arquitectura y Finanzas (costos), Marketing (benchmark), BDM (ejecución con clientes), Operaciones.
- **Pasos clave y OLAs/SLAs:**
  - Revisión semestral (mayo y noviembre) por Dirección Comercial (desviación de margen, presión competitiva, bajo cierre, costos, inflación, tipo de cambio). Producto nuevo: solicitud vía Monday, 2 días hábiles.
  - Análisis precio vs costos con Arquitectura/Finanzas y renegociación con proveedores: 10 días hábiles. Benchmark de mercado por Marketing con apoyo de IA: 2 a 4 horas. Propuesta de ajuste (con simulaciones IA): 1-2 días hábiles.
  - Presentación a Dirección General y firma de documento (se sube a Monday): 2 hrs; ajustes si no se aprueba: 1 día hábil.
  - Comunicar nuevos precios a BDMs y Operaciones: 1 día hábil. Análisis de clientes (contrato, riesgo-beneficio) documentado en account planning HubSpot: 1 día hábil. Negociación con cliente: 1 día hábil.
  - Si el cliente acepta: ajuste de negocios en HubSpot 2 hrs. Si no procede: se mantiene precio y solo cambia en negocios futuros (2 hrs). Monitoreo post-ajuste (ventas, margen, conversión): 30 días de seguimiento inicial.
- **🎯 Oportunidades de agente IA:**
  - **(Estratégico)** Agente de pricing que ejecute el benchmark de mercado (competencia, tendencias, sensibilidad de precio) y corra simulaciones de margen/impacto — el propio proceso ya prevé "apoyo de la IA"; formalizarlo como agente reduce las 2-4 hrs y los 1-2 días a casi cero.
  - **(Quick win)** Agente que ajuste masivamente los valores de los negocios abiertos en HubSpot conforme a la nueva lista de precios (hoy tarea manual del BDM).
  - **(Estratégico)** Agente de segmentación de impacto que clasifique clientes por contrato y riesgo-beneficio (perder cliente vs ganar margen) y proponga a qué clientes aplicar el aumento y a cuáles preservar precio.
  - **(Quick win)** Agente de monitoreo post-ajuste que mida ventas/margen/conversión a 30 días y genere el reporte a Dirección General.

---

### Proceso de Gestión de Producto — MVP y Go To Market (SD-DESARROLLO-02, V5)

- **Objetivo:** Llevar una idea de producto desde la identificación de oportunidad y validación de MVP hasta el lanzamiento comercial (Go To Market), pasando por comités, validación con clientes beta y capacitación de la fuerza comercial.
- **Sistemas:** Monday (Task Manager: registro de oportunidades, requerimientos, evidencias, aprobaciones), IA (evaluación de competidores, precios, materiales, campañas, consolidación de hallazgos), HubSpot (deriva a proceso comercial), Canva/Marketing Hub (materiales).
- **Roles clave:** Dueño/Líder de producto (responsable del proceso), BDM, Postventa, Innovación, Desarrollo, VP Tecnología, Comité de Innovación, Dirección Comercial y General, Marketing, SDR/Preventa/Postventa/Operaciones.
- **Pasos clave y OLAs/SLAs:**
  - Planeación e identificación de oportunidad (registro en Monday): 1 día. Solicitud de evaluación de requerimiento al área de Innovación: 3 días. Análisis y dimensionamiento (con legal-fiscal-especialistas, viabilidad de hipótesis): 3 a 10 días.
  - Reunión con VP Tecnología para clasificar requerimientos: 1 día. Conceptualización de hipótesis/roadmap/business case (IA evalúa competidores): 3 días. Comité de Innovación (aprueba/rechaza, se documenta): 2 hrs. Modelo de precios (a Dir Comercial, con IA): 2 días.
  - Recopilar info de validación MVP: 2 días. Material básico (One Page, presentación): 3 días. Presentación a comercial: 1 día. Definir prospectos beta (al menos 5): 2 días.
  - Campaña de exploración (diseño 2 días con IA, ejecución 10 días, consolidación 2 días con IA). Sesión de aprendizaje MVP (validado con al menos 5 clientes y 2 especialistas): 4 hrs. Recibir resultados firmados: 1 día.
  - Go To Market: ICP/Buyer Persona 2 días; materiales comerciales con IA (brochure, caso de éxito, video, FAQ, script): 10 días; estrategia de lanzamiento 3 días; aprobar plan GTM (firma, evidencia en Monday) 1 día; capacitar fuerza comercial y Operaciones 3 días.
  - Ejecución de campaña (según plan), lanzamiento 1 día, reporte de resultados iniciales (demanda, pipeline, conversión, adopción): 30 días.
- **🎯 Oportunidades de agente IA:**
  - **(Quick win)** Agente que genere los materiales comerciales y de validación (One Page, brochure, FAQ, script, guion de video) a partir del business case — el proceso ya asume "apoyo de la IA"; convertirlo en agente reduce los 10 días.
  - **(Estratégico)** Agente de inteligencia de mercado/competencia que alimente el business case, el benchmark de competidores y el modelo de precios con datos actualizados.
  - **(Quick win)** Agente que consolide los hallazgos de la campaña de exploración beta (objeciones, sensibilidad al precio, interés) en el documento de resultados del MVP.
  - **(Estratégico)** Agente que documente ICP/Buyer Persona y diseñe la estrategia/campaña de lanzamiento (mensajes, canales, KPIs) enlazándola con el pipeline de HubSpot.

---

## Top 3 oportunidades del área (priorizadas)

1. **Agente de higiene y forecasting de pipeline (Ventas + Renovaciones).** Detecta negocios que rompen OLAs (MQL→SQL 15 días, →Negociación 4 meses, →Aceptación 1 mes) y dispara la tarea de renovación 90 días antes, con próxima-mejor-acción. *Por qué:* impacto directo en ingresos y en fugas por olvido; facilidad alta porque opera sobre datos ya estructurados en HubSpot.

2. **Agente de captación y calificación de leads (Marketing).** Lee los 5 buzones inbound, normaliza y enriquece el registro en HubSpot, aplica el scoring MQL (0-100) y rutea al BDM correcto con handoff estandarizado. *Por qué:* ataca el cuello de botella de 8 hrs de captura manual y el "re-trabajo del BDM" que el propio doc señala como riesgo; facilidad media-alta (reglas y modelo ya definidos).

3. **Agente lector de bases de licitación (Licitaciones).** Extrae requisitos, fechas y entregables de las bases y genera el checklist y el proyecto con tareas/tiempos en Monday, más alertas de vencimiento. *Por qué:* alto valor (evita descalificaciones por requisitos omitidos y ahorra horas de lectura manual); facilidad media, apalancado en la capacidad de lectura documental del agente.
