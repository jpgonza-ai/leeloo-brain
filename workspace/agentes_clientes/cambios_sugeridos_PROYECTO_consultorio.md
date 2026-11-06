# FORMATO FINAL (Pablo, 20-oct): INFOGRAFÍA en PDF, fácil de entender, que se arma poco a poco con todos los puntos de análisis. No reescribirle los puntos en el chat: identificarlos y guardarlos aquí.

# Cambios sugeridos al PDF "PROYECTO_Consultorio_IA_Analisis_Plan_Cuestionario" (revisión con Pablo, desde 2026-10-20)
Alcance de Leeloo: negocio, operación, producto y cumplimiento. Secciones técnicas (1.4 herramientas, 1.5 arquitectura, 1.6 modelo de datos, 1.8 servidor local): solo riesgos, sin revisión de construcción (contrato HotlumPowell).

## Parte 1
### 1.1 Contexto — ✅ REVISADO con Pablo (20-oct)
- Redacción CORREGIDA (Pablo): el DOCTOR es de edad avanzada: tiene 73 años (no "paciente de edad avanzada").
- Facturación: hoy la hace a mano la SECRETARIA (programa del SAT); se atenderá más adelante. Pablo: la información FISCAL de cada paciente (RFC, uso de CFDI, etc.) también debe guardarse en el EXCEL índice.
- Bloque 9-11 = lunes a viernes (respuesta 1.12), no solo los días presenciales.
- 🔴 AGREGAR (aprobado) el dolor principal: el doctor trabaja hasta 2 h después de la última consulta contestando WhatsApps (mayormente clínicos) y actualizando expedientes = métrica estrella.
- 🔴 AGREGAR (aprobado): agenda ~80% llena (20-25 de 25) → el valor es tiempo + cero errores, no llenar huecos.
- (Datos nuevos validados: facturación manual con programa del SAT; revisión de expediente ~20 min → 5 min con resumen.)
### 1.2 Dolores → solución (en revisión con Pablo)
- Fila 1 ✅ (Pablo, 20-oct): DOLOR = los pacientes escriben al WhatsApp personal del doctor Y de la secretaria. SOLUCIÓN = WhatsApp en el teléfono FIJO del consultorio, con filtros en cascada: (1) el bot resuelve lo frecuente → (2) si el bot detecta que debe intervenir la secretaria, pasa a la siguiente capa → (3) si la secretaria identifica algo que solo puede atender el doctor, lo atiende él.
  Ejemplos de escalamiento (Pablo): a) preguntas sobre medicamentos (ni el bot ni la secretaria pueden recetar); b) síntomas intensos o dolor que requieren atención inmediata.
  Aportes de Leeloo: el caso b) NO debe esperar en la fila de la secretaria → el bot responde al instante con el protocolo de urgencias (911/urgencias) + alerta inmediata a la secretaria Y al doctor (noches y fines de semana); el caso a) termina siempre en el doctor (la secretaria solo lo canaliza). Otros ejemplos de escalamiento ✅ APROBADOS por Pablo: efectos secundarios, solicitud de receta o resurtido, resultados de estudios, quejas, citas fuera de las reglas.
- AGREGAR fila: "Mensajes clínicos que el doctor contesta de noche" → bandeja clínica (urgencia + resumen + contexto), nota automática para el expediente aprobada por el doctor, respuestas rápidas + horario para mensajes clínicos.
- Fila 4: "huecos en agenda" → "faltas y errores de agenda".
- Fila 8: "acceso para la familia autorizada" → solo el doctor y la secretaria; la familia solo para recuperar el respaldo en una emergencia (datos sensibles de ~6,000 pacientes, LFPDPPP).

- Fila 1, RETO de transición (Pablo, 20-oct): el doctor tiene su celular desde hace 40+ años; muchos pacientes lo seguirán buscando directo. Propuesta de Leeloo: (1) no cambiar su número, migrar sus pacientes poco a poco; (2) mensaje de anuncio con la voz del propio doctor; (3) pasar su número personal a la app GRATIS de WhatsApp Business (conserva chats) para activar mensaje de bienvenida/ausencia automático con el link wa.me del consultorio; (4) respuesta rápida de 1 toque + reenviar el mensaje al número del consultorio; (5) difundir el número en cada punto de contacto (recetas, tarjetas, Google, recordatorios, la secretaria en consulta); (6) 'círculo cercano' aceptado (familia/amigos/pacientes de décadas) sin pelear; (7) medir cuántos siguen escribiendo al personal y ajustar.
  · Pablo aprobó el punto 1 (anuncio con la voz del doctor). Punto 2 aclarado (20-oct): su mismo número en la app gratuita de WhatsApp Business; lo configura Pablo o la secretaria UNA vez (~15 min): respaldo → instalar WA Business → mismo número con migración de chats → Herramientas para la empresa → Mensaje de ausencia 'Enviar siempre' con el link del consultorio → Destinatarios 'Todos, excepto…' (familia/amigos) + Respuestas rápidas ('/'). Hacerlo HASTA que el WA del consultorio esté operando; el doctor aprueba el texto.
  · Mensaje de ausencia (verificado, 20-oct): destinatarios = Todos / Todos los que no están en contactos / Todos, excepto… / Solo a…; máximo 1 vez cada 24 h por contacto; horario: siempre / personalizado / fuera de horario. Recomendado: 'Enviar siempre' + 'Todos, excepto…' (familia/amigos).
  · Puntos 4 y 5 ✅ aprobados. Punto 6 (medir): WA Business no cuenta clics (hasta donde sé) → (1) link wa.me con texto pre-escrito 'Hola, vengo de parte del Dr. González' para contar las conversaciones redirigidas [favorita]; (2) acortador con contador (tipo Bitly gratis); (3) conteo semanal de pacientes que siguen escribiendo al celular del doctor (hojita de la línea base). 1+3 = foto completa.
- Filas 2, 3 y 4 ✅ OK (Pablo, 20-oct). (Fila 4 con el reenfoque a 'faltas y errores de agenda'.)
- Fila 5 (cuestionario previo): el doctor define el cuestionario MÍNIMO para pacientes nuevos (Pablo se lo pedirá). Idea de Pablo: validación de identidad para evitar homónimos y que nadie se salte el cuestionario por decir 'no es mi primera vez'. Propuesta de Leeloo (pendiente de OK): (1) número de celular conocido → reconocer, pero confirmar la fecha de nacimiento (familiares escriben desde su número); (2) número no reconocido → pedir nombre completo + fecha de nacimiento y buscar en el Excel (mismo ID que las carpetas); (3) coincide → subsecuente, agenda + ficha correcta para el reporte de las 20:00; (4) no coincide → paciente nuevo, cuestionario obligatorio; (5) duda/ambigüedad → secretaria; nunca adivina. PRIVACIDAD: el bot nunca revela datos para 'ayudar'; pide el dato y compara en silencio.
  ✅ DECISIÓN FINAL fila 5 (Pablo, 20-oct; "ponlo así en el análisis"): validación 100% a cargo del BOT. Coincide nombre + fecha de nacimiento → subsecuente. Si coincide el nombre pero NO la fecha → el bot lo da por paciente NUEVO (cuestionario obligatorio); no pasa a la secretaria. Privacidad: el bot confirma en silencio y JAMÁS revela información ajena. Pablo preguntó por un 3er criterio (RFC) → aporte de Leeloo: el RFC se recaba en el cuestionario (datos fiscales al Excel) y a futuro sirve como 3er criterio; mientras tanto, cuando haya 'mismo nombre, otra fecha', el bot sigue solo pero marca 'posible duplicado' en el reporte de las 20:00 para que la secretaria lo concilie después, sin frenar al paciente.
  ✅ Pablo aprobó (20-oct) agregar la marca de 'posible duplicado' en el reporte de las 20:00 y el RFC como 3er criterio a futuro.
- Fila 6 ✅ OK (Pablo, 20-oct). Le expliqué qué es un repositorio (archivo central y ordenado; la carpeta de Drive ya es su inicio), la búsqueda semántica (por significado, no por palabra) y el resumen de 5 años con citas a la fuente (20 → 5 min). Para la infografía: incluir la analogía del 'bibliotecario / asistente que ya leyó todo'.
  · Pablo preguntó si el repositorio puede ser GitHub → NO para expedientes (es para código; riesgo de repo público; acceso de quien programe; LFPDPPP/NOM-004). Expedientes: Drive del consultorio (o software de expediente, opción B); código del agente: GitHub SIN datos de pacientes. Regla: GitHub = 'cómo funciona'; Drive/sistema médico = 'de quién es la información'.
- Filas 9 y 10 ✅ OK. Fila 8: 'OK' de Pablo → PREGUNTÉ si es con mi ajuste (acceso solo doctor + secretaria; familia solo para recuperar el respaldo) o como venía; pendiente.
- Fila 7 (grabación de consultas, presencial + Zoom): A) escriba médico con IA ya hecho: Heidi Health (110+ idiomas, celular + consultas en línea; la favorita) vs Nabla (español, pero notas en inglés); verificar precio, ubicación de los datos y aviso de privacidad. B) grabación simple (grabadora del celular/tablet + grabación de Zoom) + transcripción del sistema. Sugerencia: que el doctor PRUEBE Heidi antes (comprar vs construir). No negociable: consentimiento explícito registrado + el doctor aprueba cada nota. (Fuentes: reseñas/Fierce Healthcare; no verificado en sitio oficial.)
- Fila 8 ✅ (Pablo, 20-oct): respaldo cifrado en la nube con acceso para el doctor y la secretaria; la HERMANA de Pablo (también médico) = respaldo adicional y futura continuadora de los pacientes. Aporte: el aviso de privacidad debe prever la transferencia de los datos al médico que dé continuidad.
- Fila 7 — Heidi Health como OPCIÓN (Pablo, 20-oct). Double check: SITIO OFICIAL (heidihealth.com/en-us/pricing): planes Free (1 usuario, uso semanal limitado), Clinician (14 días de prueba), Teams; NO publica precios; compliance HIPAA/GDPR/UK/Canadá/AU-NZ (no menciona México). RESEÑAS 2026 (soapnotebuddy, deepcura, veroscribe, mentalyc): Clinician ~US$150/mes (~$110 anual), subió en feb-2026; gratis con consultas básicas ilimitadas; rápido, 110+ idiomas, comunidad; precisión moderada (requiere edición), transcripciones perdidas, soporte lento, a veces omite o inventa detalles; enfocado en UK/AU. Recomendación: piloto de ~5 consultas (plan gratis/prueba, con consentimiento) evaluando la calidad en español y las correcciones necesarias; si no, buscar una alternativa.

## INFOGRAFÍA (v1 enviada 20-oct): agentes_clientes/infografia/infografia_consultorio.pdf, generada con infografia_consultorio.py; incluye 1.1 y 1.2. Pendiente: la revisión de Pablo + secciones 1.3 en adelante.

## v2 del PDF con respuestas (2026-11-03, a petición de Pablo)
- Archivo: PROYECTO_Consultorio_IA_Analisis_Plan_Cuestionario_con_respuestas_v2.pdf (15 págs). Script: cuestionario_overlay_v2.py (usa PROYECTO_Consultorio_ORIGINAL_sin_respuestas.pdf + cuestionario_bbox.html; arma ov.pdf + bloque3_pagina.pdf y los une con qpdf).
- Respuestas confirmadas por Pablo: 2.9 = 48 horas antes; 2.10 = particular máx. 1 semana / aseguradora máx. 2 meses; 2.11 = sí, para pacientes de aseguradora, hasta 2 meses; 2.17 = agudización o descompensación de una enfermedad crónica o un síntoma nuevo y repentino → el doctor interroga y decide si lo atiende en horas o lo manda al hospital.
- Notas del Bloque 2 (negritas y cursivas): sin distinción entre particulares y aseguradora (en las citas sí: la aseguradora paga 1/3; agenda 50/50); consultas de 60 min; sin espacio entre citas → con mejor organización el doctor revisa el expediente minutos antes.
- Bloque 3 (página nueva): 8 FAQ identificadas (de hasta 20) con respuestas inferidas. POR CONFIRMAR: 3.1 cómo se explica el costo para aseguradora; 3.3 datos para factura; 3.8 estudios en la primera vez.
- Precio de primera vez corregido: 1,500 → 1,000 ("$1,000 para todas").
- Bloque 4 (Pablo, 3-nov, captura con resaltado): BOT = 4.1-4.4, 4.6, 4.7, 4.8 · SEC = 4.5, 4.9, 4.11 · DOC = 4.10, 4.12-4.15. Resaltado amarillo + X en el PDF v2 (pág. 13). Marqué "[X] SE AJUSTA EN LA TABLA" en la propuesta por defecto (difiere de ella); quitarlo si Pablo no lo quiere.

## BLOQUE 5 (Pablo, 5-nov) — aprobado, PENDIENTE de meter al PDF (Pablo: generar el documento AL FINAL, con todos los bloques)
- 5.1 USTED con todos · 5.2 tono CÁLIDO (con usted) · 5.3 CAMBIAR por: "Soy el asistente virtual del consultorio del Dr. Osvaldo González, en Clínica CIME."
- Secretaria: ESPERANZA.
- 5.4 c) recordatorio a las 48 h (alineado con la cancelación de 48 h) + mantener clara la LISTA DE ESPERA para cubrir cancelaciones; d) con estacionamiento ✅; f) el agente atiende 24/7 → f) replanteada como "pase a Esperanza fuera de su horario".
- Plantillas propuestas (texto enviado a Pablo, msg del 5-nov; esperando OK final):
 a) Hola, buen día. Soy el asistente virtual del consultorio del Dr. Osvaldo González, en Clínica CIME. Con gusto le ayudo con horarios, costos o para agendar una cita. ¿En qué le puedo ayudar?
 b) Listo, su cita quedó agendada para el [día] [fecha] a las [hora] con el Dr. Osvaldo González, en Clínica CIME (Av. Magdalena 430, consultorio 304, Col. del Valle). Hay estacionamiento junto a la clínica, con costo aparte. [Requisitos si aplican]. Si necesita cambiarla, avíseme por aquí con al menos 48 horas de anticipación. (Variante martes Zoom: Su consulta será en línea por Zoom; le compartimos la liga antes de su cita.)
 c) Hola, [nombre]. Le recuerdo su cita del [día] [fecha] a las [hora] con el Dr. Osvaldo González. ¿Me confirma su asistencia? Si necesita reprogramar, avíseme hoy por aquí, por favor.
 d) [Nombre], su cita con el Dr. Osvaldo González es hoy a las [hora] en Clínica CIME (Av. Magdalena 430-304, Col. del Valle). Hay estacionamiento junto a la clínica, con costo aparte. ¡Le esperamos!
 e) Entendido, cancelé su cita del [fecha] a las [hora]. Cuando guste reagendar, escríbame por aquí. Los espacios más próximos son: [opciones].
 f) Gracias por su mensaje. Este tema lo atiende directamente Esperanza, la secretaria del consultorio. Ya le dejé su mensaje y ella le responderá a partir de las 9:00 a.m. (lunes a viernes). Si se trata de una urgencia médica, acuda a urgencias o llame al 911.
 g) Con gusto. Le paso su mensaje a Esperanza, la secretaria del consultorio, y le respondemos lo antes posible.
 h) Ese dato no lo tengo a la mano. Se lo dejo a Esperanza para que le responda directamente. Mientras tanto, ¿le ayudo con algo más, como su cita?
 i) Esa es una pregunta médica y solo el Dr. González puede responderle con seguridad. Ya se la hago llegar para que la revise. Si lo prefiere, también puedo agendarle una cita.
 j) NUEVA (lista de espera): Hola, [nombre]. Se liberó un espacio con el Dr. Osvaldo González el [día] [fecha] a las [hora]. ¿Le gustaría tomarlo? Le aparto el lugar por [X] horas.

## BLOQUE 6 (Pablo, 5-nov) — pendiente de meter al PDF
- 6.1 L/Mi/V presencial 11:00-19:00 (última cita 19:00) · Martes Zoom 11:00-19:00.
- 6.2 60 min (POR CONFIRMAR si la primera vez dura igual).
- 6.3 0 min entre citas + el agente deja un resumen del paciente antes de cada cita.
- 6.4 Bloque protegido: L-V 9:00-11:00.
- 6.5 Solo con aprobación del doctor (Esperanza canaliza; ver 2.17).
- 6.6 ✅ 3 opciones de horario (si ninguna sirve, ofrece otras 3; variar días y mañana/tarde).
- 6.7 Terceros sí: la cita y la validación con los datos del PACIENTE; nunca compartir info; menores de 15 → pediatra.
- 6.8 ✅ Días inhábiles: JUEVES (descanso del doctor), sábados, domingos y festivos oficiales de la CDMX.
- 6.2 ✅ 60 min para TODAS (primera vez, subsecuente y Zoom). BLOQUE 6 CERRADO.

## BLOQUE 7 (Pablo, 5-nov) — pendiente de meter al PDF
- 7.1 Número: 55-5543-1558 (fijo del consultorio, WA Business en coexistencia); lo activa Pablo (tentativamente).
- 7.2 🔴 POR CONFIRMAR (celular de Esperanza) → marcar en ROJO.
- 7.3 Celular actual del doctor ✅.
- 7.4 Hoy: agenda/cuaderno → sugerencia: empezar a usar Google Calendar.
- 7.5 Cuenta de Google NUEVA del consultorio; la administran Esperanza y el agente (sugerí a Pablo como contacto de recuperación; pendiente su OK).
- 7.6 QR = vincular el WA Business del fijo con la plataforma del agente (coexistencia; registro por llamada al ser fijo). Propuesta: lo hace Pablo (en persona o guiando a Esperanza por videollamada); pendiente su OK.
- 7.7 20:00 ✅ · 7.8 el doctor revisa los escalados en su bloque de 9:00-11:00 ✅ · 7.9 doctor + Esperanza (hermana solo respaldo) ✅ · 7.10 programa gratuito del SAT ✅ · 7.11 USB, lo guarda el doctor (papá de Pablo) ✅ · 7.12 sí, con la hermana de Pablo (médico) ✅.
- Bloque 7 ✅ CERRADO: Pablo hace el QR; Pablo = contacto de recuperación de la cuenta de Google.

## v3 (2026-11-05), enviada a Pablo
PDF de 16 páginas con los bloques 2-8. La página 13 original se reemplazó por dos páginas nuevas (5.4 plantillas a-j aprobadas, Bloque 6). Pendientes en rojo: 7.2, 4.16, 8.1/8.2, 8.3.
