# Área: Administración y Finanzas

Insumo para el pitch de agentes de IA a Seguridata. Basado en los 8 diagramas de flujo oficiales del área. Stack de referencia: HubSpot Sales Hub (pipeline comercial), SAP (facturación/finanzas), Monday (gestión de tareas/gastos).

---

### Pre-factura y Factura (SD-ADMINYFINANZAS-01, V3)
- **Objetivo:** Generar la prefactura en SAP a partir de la info de Sales Hub, autorizarla, emitir la factura y enviarla al cliente con su resguardo documental.
- **Sistemas:** Sales Hub (origen de datos y tareas), SAP (captura/autorización/emisión), correo electrónico, plataformas del cliente para subir factura, carpeta física/electrónica.
- **Roles clave:** BDM (mueve etapas y valida cuerpo de factura con cliente), Sales Admin (captura prefactura en SAP), Ejecutivo de Administración y Finanzas (autoriza/emite), Operaciones y Jurídico (resguardo).
- **Pasos clave y OLAs/SLAs:**
  - Sales Admin captura datos de prefactura en SAP (checklist de calidad): OLA 4 horas hábiles (montos < $10,000).
  - Aceptación/rechazo de prefactura en SAP: 2 horas hábiles tras recibir aviso.
  - Elaborar factura tras aprobar prefactura: 2 horas hábiles.
  - Envío de factura al cliente (plataforma o correo, con copia a cobranza/sales admin/jurídico): 30 minutos después de generada.
  - Operaciones entrega documentación física a Jurídico: 1 día hábil tras carta entrega firmada. Resguardo mínimo 10 años (OLA 1 día hábil).
- **🎯 Oportunidades de agente IA:**
  - **[Quick win]** Agente que arma el checklist de prefactura leyendo la oportunidad en Sales Hub y precapturando los campos en SAP (solución, No. oportunidad, correos de envío/cobranza, cuerpo de factura), reduciendo la OLA de 4 h.
  - **[Quick win]** Agente validador que revisa importe, cliente, CP y régimen fiscal contra el contrato/ODC antes de la autorización, marcando discrepancias para evitar rechazos y cancelaciones (que afectan cobranza, ISR y flujo).
  - **[Estratégico]** Agente que dispara y monitorea el envío de factura por plataforma/correo, confirma acuse y notifica automáticamente a cobranza/jurídico dentro de la ventana de 30 min.

---

### Cobranza (SD-ADMINYFINANZAS-2, V4)
- **Objetivo:** Gestionar el cobro de facturas emitidas según condiciones de crédito del contrato, dar seguimiento, resolver stoppers y registrar el pago.
- **Sistemas:** Sales Hub (fecha programada de pago automatizada por días crédito, propiedades de primer contacto/seguimiento, notificación a BDM), SAP (registro contable del pago), correo, teléfono, WhatsApp, lista/reporte de cobranza en Excel.
- **Roles clave:** Ejecutivo de Administración y Finanzas (dueño del proceso), BDM (apoyo en morosidad y refacturación), Sales Admin (refacturación), Operaciones (pendientes de entrega).
- **Pasos clave y OLAs/SLAs:**
  - Primer contacto para asegurar recepción de factura: OLA 2 horas.
  - Segundo contacto / seguimiento de cobranza (correo, teléfono, WhatsApp): a partir de 7 días naturales de recibida la factura.
  - Notificar pendientes de entrega/errores de facturación al área y a Sales Admin: OLA 2 horas.
  - Ante impago: contactar cliente, renegociar y capturar nueva fecha en Sales Hub; notificar morosidad a BDM.
  - Registro de pago: actualizar Sales Hub con fecha/evidencia (notifica automático a BDM) y registrar en SAP; reporte de cobranza semanal por correo a Dirección.
- **🎯 Oportunidades de agente IA:**
  - **[Quick win]** Agente de recordatorios multicanal (correo/WhatsApp) que dispara el primer contacto (2 h) y el seguimiento a los 7 días de forma automática, con escalamiento a BDM ante morosidad.
  - **[Quick win]** Agente que concilia el pago recibido, actualiza Sales Hub y registra en SAP, cerrando el ciclo sin captura manual.
  - **[Estratégico]** Agente que genera el reporte de cobranza semanal (aging, DSO, morosos) automáticamente para Dirección, más un modelo de priorización de cuentas por riesgo de impago.
  - **[Estratégico]** Agente que detecta stoppers (errores de facturación / pendientes de entrega) y arma la tarea de refacturación o la queja a Operaciones.

---

### Jurídico (SD-ADMINYFINANZAS-04, V1)
- **Objetivo:** Elaborar, revisar, negociar y firmar documentos jurídicos (contratos cliente/aliado, NDAs, proceso abreviado de gobierno) y resguardarlos.
- **Sistemas:** Sales Hub (solicitud, tareas, notas, etapas, resguardo), correo, plataformas de firma electrónica, CLM-JIRA (contratos de proveedores), carpetas física y electrónica. Políticas en SD-AD-politicas-doctosjuridicos.pdf y SD-PRACTICASCOMERCIALES.PDF.
- **Roles clave:** BDM/Canales (captura documentación y dispara tareas), Jurídico (elaboración, revisión, firma, resguardo), Contador general (envío a firma física), Administración y Finanzas.
- **Pasos clave y OLAs/SLAs:**
  - Solicitud de información faltante al BDM: OLA 4 horas hábiles.
  - Elaboración/revisión de documento: contrato cliente-aliado 2 días hábiles; NDA/otras solicitudes 1 día hábil; proceso abreviado 1 día hábil.
  - Disparo de proceso de firma (siempre inicia SeguriData): 2 horas hábiles.
  - Fianza (si aplica): subir contrato firmado 2 horas hábiles tras firma SeguriData.
  - Envío a firma física / actualización de fecha de envío: 2 horas hábiles tras aceptación del cliente.
  - Firma por plataforma y seguimiento con recordatorios: 2 horas hábiles; seguimiento semanal de firmas.
  - Resguardo documental los jueves; conservación mínimo 10 años.
- **🎯 Oportunidades de agente IA:**
  - **[Quick win]** Agente que valida completitud del expediente en Sales Hub (acta constitutiva, poder, constancia fiscal, ID del firmante) y solicita lo faltante al BDM dentro de las 4 h.
  - **[Estratégico]** Agente de revisión contractual (LLM) que precompara el contrato contra políticas y prácticas comerciales (descuentos, días de crédito) y sugiere comentarios en Sales Hub, acelerando la OLA de 2 días.
  - **[Quick win]** Agente que da seguimiento a firmas electrónicas, envía recordatorios y actualiza fechas de inicio/vencimiento y etapa en Sales Hub.
  - **[Estratégico]** Agente que monitorea vencimientos de contratos y alerta renovaciones, apoyando el resguardo semanal de los jueves.

---

### Presupuesto (SD-ADMINFINANZAS-06, V2)
- **Objetivo:** Construir el presupuesto anual (ingresos por pipeline + gastos base cero por área), aprobarlo por dirección/consejo y darle seguimiento trimestral (forecast).
- **Sistemas:** Sales Hub (pipeline presupuestado/draft de ventas, márgenes brutos), Drive (presupuestos de áreas, evidencia de flujo), plataforma de firma, correo, Excel/reportes.
- **Roles clave:** Dirección de Administración y Finanzas (dueño), Dirección Comercial (ingresos/pipeline), Líderes de área (gasto base 0), Gerencia de Contabilidad (reportes), Dirección General, Presidencia y VP Tecnología (aprobación).
- **Pasos clave y OLAs/SLAs:**
  - Draft de ventas / ingresos en Sales Hub: al menos 1 mes antes del cierre de año.
  - Revisión de pipeline y definición de metas: 1 día cada una.
  - Cada área plantea gasto con metodología base 0 en Drive: OLA 5 días. Consolidación: 5 días.
  - Ciclos de propuesta/ajuste: preparar V1 (2 días), revisar con Dirección (1 día), ajustes (3 días), segundo draft (3 días).
  - Pasar a utilidad neta / flujo de ventas: 2 días. Aprobaciones DG y Presidencia/VP: 2 días / 1 día+.
  - Dar a conocer presupuesto final: al menos 2 semanas antes de inicio de año.
  - Seguimiento: reporte de ejecución mensual (2 días), reunión trimestral (RTP) el segundo lunes de mes trimestral; forecast primera semana del mes siguiente al trimestre; ajustes por desviación 2 días.
- **🎯 Oportunidades de agente IA:**
  - **[Estratégico]** Agente que consolida los presupuestos base cero de todas las áreas desde Drive en un modelo unificado, detectando inconsistencias y reduciendo los 5 días de consolidación.
  - **[Estratégico]** Agente de análisis de variación presupuestal (real vs presupuestado) que genera el forecast trimestral y detecta sobre/sub-ejecución automáticamente.
  - **[Quick win]** Agente que arma los paquetes ejecutivos y convocatorias para las reuniones RTP y de aprobación, con calendarización automática.
  - **[Quick win]** Agente que jala el pipeline presupuestado de Sales Hub y calcula el draft de ingresos con estacionalidad y renovaciones.

---

### Financiamiento externo (SD-ADMINFINANZAS-07 ProcesoFinanciamiento, V2)
- **Objetivo:** Identificar necesidades de financiamiento, evaluar y negociar opciones, formalizar el contrato, disponer recursos y monitorear obligaciones.
- **Sistemas:** Modelos financieros (Excel), sistemas contables, formatos bancarios, comité financiero, benchmark de mercado. (No se citan HubSpot/SAP/Monday explícitamente.)
- **Roles clave:** Administración y Finanzas (necesidades, proyección), Dirección de Administración y Finanzas (estrategia, opciones, negociación), Legal (revisión contractual), VP Tecnología / Presidente de consejo (firma), Ejecutivo/Contador (registro), Dirección (evaluación).
- **Pasos clave y OLAs/SLAs (con KPIs):**
  - Identificar necesidades y proyectar flujo: 1 día c/u (KPI precisión >90%, desviación <10%).
  - Definir estrategia: 1 día (KPI >90% alineación). Identificar opciones: 5 días (KPI >3 alternativas).
  - Evaluar condiciones: 2 días. Preparar expediente: 5 días (KPI 100% completos).
  - Propuesta/cotización de la financiadora: 30 días. Negociación: 5 días.
  - Cierre revisión legal: 2 días. Firma de contrato: 2 días.
  - Registro, disposición y control de recursos: 5 días c/u. Monitoreo de obligaciones: calendario de pagos (KPI >99% pagos puntuales). Evaluar desempeño: 6 días (KPI ROI).
- **🎯 Oportunidades de agente IA:**
  - **[Estratégico]** Agente que arma la proyección de flujo de efectivo y el modelo comparativo de alternativas (tasas/plazos/costos) para acelerar los pasos de 1–5 días.
  - **[Quick win]** Agente que integra el expediente financiero contra checklist documental y verifica completitud (KPI 100%).
  - **[Estratégico]** Agente que monitorea el calendario de pagos y obligaciones financieras, alertando vencimientos para sostener el >99% de pagos puntuales.

---

### Gestión de Informes Financieros (SD-ADMINYFINANZAS-07 Informes, V1/V3)
- **Objetivo:** Recopilar y validar información contable, conciliar, consolidar estados financieros y producir el informe financiero mensual aprobado por Dirección.
- **Sistemas:** Sistema contable, SAP financiero (resguardo), Drive/repositorio interno, correo, firma electrónica, WhatsApp; controles de accesos/backups por TI.
- **Roles clave:** Contabilidad (recopilar, validar, conciliar), Finanzas (consolidar, elaborar, revisar), Dirección/Dirección General (revisión y aprobación), Administración (archivo), Legal, TI.
- **Pasos clave y OLAs/SLAs:**
  - Recopilar y recibir información contable: 1 día c/u. Validar registros: 2 días.
  - Conciliaciones bancarias: 2 días. Revisar consistencia: 2 días.
  - Consolidar estados financieros (resultados, balance, flujo, presupuestado vs real, vs año anterior): 3 días.
  - Elaborar informe mensual: 3 días. Revisión de consistencia: 4 días. Revisión ejecutiva: 1 hora.
  - Solicitar/realizar ajustes: 2 horas / 1 día. Aprobar informe: 2 horas. Enviar informe: 2 horas.
  - Archivo y control documental (SAP financiero + físico): 5 horas; resguardo 5 años (SAT).
  - Matriz de riesgos: destacan "Información incorrecta" y "Falta trazabilidad" (nivel 20, error humano/documentación incompleta), "Errores de consolidación" por integración manual.
- **🎯 Oportunidades de agente IA:**
  - **[Estratégico]** Agente que automatiza conciliaciones bancarias (banco vs registros contables), atacando el riesgo top de "integración manual" y los 2 días de OLA.
  - **[Estratégico]** Agente que consolida estados financieros y genera el informe mensual con análisis de variaciones e indicadores, reduciendo los 3+4 días de elaboración/revisión.
  - **[Quick win]** Agente de control de versiones y trazabilidad documental que resguarda en repositorio oficial y evita "versiones incorrectas" y "falta trazabilidad".
  - **[Quick win]** Agente que arma el paquete de revisión ejecutiva (cifras clave, variaciones) para la revisión de 1 hora previa a comité.

---

### Adquisiciones / Gastos (SD-ADMINFINANZAS-03, V7)
- **Objetivo:** Gestionar compras de bienes/servicios, viáticos, anticipos, reembolsos, importación de equipos Entrust, renovación de licencias y proveedores estratégicos, con cotizaciones, autorización y pago.
- **Sistemas:** Monday (flujo de gestión de gastos, aprobaciones), SAP (registro de facturas/anticipos/reembolsos/pagos), Clockify (proyectos/visitas), Factorial (aprobaciones), correo, formatos Excel (FOR-ADF-03 orden de compra, FOR-ADF-02 reembolso), matrices (SD-MATRIZ-APROBACION-GASTO.PDF), portal Entrust, agente aduanal. **Ya usan IA:** "Matriz de Solicitantes Autorizados" consultada con apoyo de IA.
- **Roles clave:** Cabeza/Responsable de área (requerimiento, verificación de entrega), Ejecutivo de Administración y Finanzas (cotizaciones, negociación, OC, pagos), Dirección de Administración y Finanzas (Entrust), Solicitante (reembolsos/viáticos), Responsables de aprobación (matriz de montos).
- **Pasos clave y OLAs/SLAs:**
  - Requerimiento con mínimo 3 cotizaciones en Monday: OLA 2 h (compras de proyecto: primeros 5 días hábiles tras cierre de contrato; Entrust: 30 días hábiles de anticipación).
  - Validar solicitante autorizado (IA): 20 min. Validar presupuesto + verificaciones anti-duplicado: 20 min.
  - Validar cotizaciones (mystery shopper): 16 h. Negociar (push comercial 3–5% desc. + 10–15 días crédito): 8 h. Documentar: 30 min.
  - Viáticos: 3 cotizaciones (1 día), respuesta al solicitante (2 h hábiles), tope hotel colaborador $1,200 +IVA / directivo $1,500 +IVA, anticipación 4 días.
  - Aprobaciones en plataforma según matriz de montos: máximo 8 horas hábiles.
  - Entrust: envío a México 4 días hábiles (con existencia) o 15+ días (sin existencia); gestión aduanal 5 días hábiles.
  - Pago a proveedores: 15 días hábiles, los viernes. Anticipos: miércoles/viernes antes de 12:00 pm.
  - Reembolsos: pago viernes hábiles; cargo a favor de empresa: 1 semana hábil para depositar.
  - Renovación de licencias: monitoreo permanente (primer lunes del mes revisión de vencimientos a 90 días), solicitud 60 días antes del vencimiento. Proveedores estratégicos: negociación anual (diciembre), 1 día por proveedor.
- **🎯 Oportunidades de agente IA:**
  - **[Quick win]** Extender el agente de "Matriz de Solicitantes Autorizados" (ya existente) a validar presupuesto, inventario, duplicidad de OC y proyecto activo automáticamente (paso 3, 20 min).
  - **[Estratégico]** Agente que recopila/compara las 3 cotizaciones, aplica el push comercial y recomienda proveedor, documentando la negociación (ataca 16 h + 8 h de OLA).
  - **[Quick win]** Agente que monitorea vencimientos de licencias/mantenimientos (ventana 90/60 días) y detona la solicitud de renovación a tiempo, evitando interrupciones de servicio.
  - **[Estratégico]** Agente de viáticos que cotiza vuelos/hotel/auto en 3 agencias, valida topes ($1,200/$1,500 +IVA) y responde al solicitante dentro de las 2 h.
  - **[Quick win]** Agente que valida reembolsos (formato + comprobantes + justificación) contra la matriz de aprobación y registra en SAP.

---

### Tesorería (SD-ADMINFINANZAS-05, V6)
- **Objetivo:** Programar y ejecutar pagos aprobados según flujo semanal y política de montos, capturarlos en banca, validar y conciliar.
- **Sistemas:** Excel de flujo (evidencia en Drive), software de control y aprobación de gastos (prerequisito), sistema bancario (con token y firmas mancomunadas), SAP (registro de pagos), correo.
- **Roles clave:** Ejecutivo de Administración y Finanzas (captura y ejecución), Director de Administración y Finanzas (revisión/autorización), Contador general (respaldo de captura y conciliación), Dirección General y VP Tecnología (autorización mancomunada de montos altos).
- **Pasos clave y OLAs/SLAs:**
  - Validación de pagos autorizados (recurrentes/contratos anuales): 1 hora. Captura del pago en el flujo (Excel): 3 horas diarias, una vez aprobado y presupuestado.
  - Revisión de flujo y actualización de listado de pagos: jueves de cada semana (flujo disponible a 4 semanas / 5 meses). Autorización de flujo: viernes 10:00 am (evidencia en Drive). Reunión con DG: lunes.
  - Reprogramación de pago: 2 horas (si es >1 mes se renegocia con proveedor).
  - Liberación por montos: >$500,000 (excepto nómina) autoriza mancomunadamente DG + VP Tecnología; <$500,000 Ejecutivo + Dirección de A&F. Anticipación 1 día.
  - Captura en banca (pesos/dólares): 2–3 horas. Validación captura vs Excel aprobado: 1 hora. Registro de pago en SAP: 20 min.
  - OLAs de pago: reembolsos/anticipos (llegan martes mediodía → miércoles; jueves mediodía → viernes); proveedores a días crédito (mínimo 15); nómina 1 día antes.
  - Conciliación bancaria (contador general): semanal y mensual firmada, para auditorías. Controles: firmas mancomunadas, validación captura vs flujo; riesgos: banca caída (mitigación >1 banco), transferencias inseguras (mitigación autorizaciones mancomunadas).
- **🎯 Oportunidades de agente IA:**
  - **[Quick win]** Agente que valida que cada pago esté autorizado en el software de gastos y presupuestado, y precarga el listado de pagos del jueves (ataca la validación de 1 h + captura de 3 h).
  - **[Estratégico]** Agente que cruza la captura del sistema bancario contra el Excel de flujo aprobado y señala discrepancias antes de liberar (control clave del proceso).
  - **[Quick win]** Agente que registra los pagos en SAP y envía el aviso de pago al proveedor/solicitante automáticamente (OLA 20 min).
  - **[Estratégico]** Agente de conciliación bancaria (estado de cuenta vs contabilizado) semanal/mensual para el contador general, listo para auditoría.

---

## Top 3 oportunidades del área (priorizadas)

1. **Agente de cobranza multicanal y conciliación de pagos (Cobranza).** Alto impacto directo en flujo de efectivo (acelera DSO) y facilidad alta: los tiempos y canales ya están definidos (primer contacto 2 h, seguimiento 7 días) y solo hay que orquestar recordatorios en Sales Hub + WhatsApp/correo y cerrar el ciclo actualizando Sales Hub y SAP. Quick win con ROI medible.

2. **Agente de conciliación y consolidación financiera (Informes Financieros + Tesorería).** Impacto alto porque ataca el riesgo top del área ("integración manual", nivel 20) y libera muchos días de OLA (conciliaciones 2 días, consolidación 3 días, informe 3+4 días). Facilidad media: requiere integrar sistema contable/SAP y banca, pero los datos son estructurados y el control de conciliación ya existe.

3. **Agente de adquisiciones (validación + cotización + push comercial).** Impacto alto (ahorro directo en compras vía descuentos 3–5% y días de crédito, más control anti-duplicidad) y facilidad alta porque Seguridata ya usa IA en la "Matriz de Solicitantes Autorizados": es extender un agente probado a validar presupuesto/inventario/OC duplicadas y a comparar las 3 cotizaciones en Monday. Quick win apalancado en algo que ya funciona.
