# Review — Proceso de Ventas Seguridata (SD-COMERCIAL-02 v3)

> Doc fuente: `Diagrama de Flujo — Proceso de Ventas`, clave SD-COMERCIAL-02, versión 03, elaborado 29-jun-2026 (7 págs).
> Recibido de Olga García (Subdirección de Control de Calidad) por correo; Pablo lo reenvió por Telegram (inbox `1785425286295`).
> Contexto: Pablo + Mario (VentureCapital) + Patti están evaluando **agentes de IA** para Seguridata. Este review busca dónde un agente aporta valor.

## Stack que usan
- **HubSpot Sales Hub** — columna vertebral del pipeline de punta a punta (lead → cobrado).
- **SAP** — facturación final (prefactura, factura XML/PDF).
- **Monday** — gestión de tareas fuera de HubSpot (apoyo en renovaciones).

## Pipeline (etapas, % y OLAs/SLAs)
1. **MQL 1%** — Marketing asigna lead calificado al BDM (automatización Hub). Máx 15 días para pasar a SQL; si no, se reasigna a otro BDM.
2. **SQL 5%** — BDM aplica cuestionario de 1a entrevista (7 preguntas, playbook en Hub), define roles del contacto. Máx 1 semana a Arquitectura.
3. **Arquitectura 10%** — se asigna arquitecto (Bernardo). OLA asignación 1 día hábil.
4. **Propuesta técnica-comercial 30%** — arquitecto elabora propuesta + cotización (cotizador). OLA 4–12 días hábiles según tamaño.
5. **Negociación final 50%** — máx 4 meses desde propuesta.
6. **Aceptación verbal 70%** — dispara solicitud de fianza (Admin/Finanzas, Jesús) y de contrato (Jurídico, Carlos Jiménez). Máx 1 mes.
7. **Contrato firmado 90%** — Jurídico revisa vs políticas (`SD-AD-políticas-doctosjuridicos.pdf`, `SD-PRACTICASCOMERCIALES.pdf`), proceso de firma, resguardo mín. 10 años. Máx 1 semana.
8. **Prefactura 95%** — Sales Admin captura en SAP con checklist de calidad de datos.
9. **Facturación 95%** — Admin/Finanzas autoriza (2h) y elabora factura (2h); Sales Admin sube XML/PDF.
10. **Cobrado 100%** — Ejecutivo de finanzas: primer contacto 2h, segundo a 7 días naturales; política de pago 50% inicio / 50% entrega.

## Roles
- **BDM** — dueño del deal de punta a punta (prospección, documentación, seguimiento, cobranza de apoyo).
- **Arquitectura** (Bernardo) — propuesta técnica + cotización; costos no editables por BDM.
- **Jurídico** (Carlos Jiménez) — contratos, NDAs, firma, resguardo.
- **Admin y Finanzas** (Jesús para fianzas) — fianzas, autorización de factura, cobranza.
- **Sales Admin** — captura en SAP / prefactura.

## Automatizaciones que YA tienen (Hub)
- Asignación automática de lead calificado al BDM por criterios.
- Reasignación automática de leads estancados >15 días en MQL.
- Notificaciones automáticas a arquitectura/jurídico/finanzas al cambiar de etapa.
- Disparo automático de solicitud de fianza y contrato en aceptación verbal.
- Notificación al BDM de contrato firmado / factura / cobrado.

## 🎯 Oportunidades para agentes de IA (dónde agregamos valor)
1. **Calificación y documentación de leads (MQL→SQL).** Agente que enriquece el lead, y a partir de la transcripción de la llamada/reunión **auto-responde el playbook de 7 preguntas** y documenta nota/reunión/llamada en HubSpot. Ataca la OLA de 8h y la fuga de contexto.
2. **Borrador de propuesta técnica-comercial.** Agente que arma un primer draft de la propuesta desde el levantamiento de necesidades + cotizador, para que el arquitecto solo edite. Ataca la OLA de 4–12 días.
3. **Pre-revisión jurídica.** Agente que valida el contrato contra `SD-AD-políticas-doctosjuridicos` y `SD-PRACTICASCOMERCIALES`, checa descuento/días de crédito vs la tabla de descuentos, y detecta documentación faltante (acta constitutiva, poder, constancia fiscal, ID del firmante). Reduce el ida-y-vuelta.
4. **Cobranza asistida.** Agente de dunning que ejecuta primer/segundo contacto (correo, teléfono, WhatsApp), detecta stoppers (errores de factura, problemas de entrega), y actualiza HubSpot. Ataca las OLAs de cobranza.
5. **Vigilante de OLAs / higiene de pipeline.** Agente que monitorea las OLAs de TODAS las etapas (hoy solo hay regla de reasignación a 15 días en MQL) y avisa al dueño cuando un deal se estanca.
6. **QA de prefactura antes de SAP.** Agente que corre el checklist de datos antes de capturar en SAP (ellos mismos marcan el riesgo de cancelación de factura → afecta cobranza, ISR, flujo). Valida completitud/calidad.

## Tabla de descuentos (pág. 7) — insumo clave para agentes
- 0–5%: Ejecutivo Comercial (registrar razón en CRM).
- 6–15%: Dirección Comercial (justificación + contraprestación).
- 16–25%: Dirección Comercial (justificación formal + análisis de margen).
- >25%: Dirección General (caso de negocio documentado).
- Regla: ningún descuento es automático; todo descuento debe generar contraprestación (renovación multianual, más licencias, pago anticipado, etc.).

## Pendiente para completar el review
- **Falta el 2º documento de Olga:** `SD-COMERCIAL-05-ProcesoRenovacionesv2.pdf` (Proceso de Renovaciones). Existe como adjunto en el correo pero el conector de Gmail no baja adjuntos y no llegó por Telegram. **Pedir a Pablo que lo reenvíe por Telegram** para cerrar el análisis (renovaciones es justo donde usan Monday + donde hay más upside de agentes de retención).
