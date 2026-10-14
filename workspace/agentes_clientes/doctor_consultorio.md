# Caso "Doctor" — agente para consultorio médico (2026-10-08)
Pablo tendrá llamada con un doctor (nombre aún no dado) para explorar agente que automatice tareas del doctor y su secretaria.
Dolor principal (Pablo): agenda (agendar/confirmar/cancelar, liberar huecos), pacientes escriben al WhatsApp personal del doctor en vez de llamar a la secretaria → número de WhatsApp propio 24/7.
Mapa de ideas enviado: agenda (confirmación 24-48h, lista de espera, recordatorios, no-shows); WhatsApp como recepción (FAQ, escalamiento, emergencias 911); pre-consulta (pre-registro, estudios, documentos); cobranza/admin (pagos, CFDI, seguros); post-consulta (seguimiento, controles, reseñas Google); para el doctor (resumen diario, pendientes, dictado).
Preguntas de descubrimiento: citas/día y no-shows; tiempo de secretaria en tel/WhatsApp; FAQ; sistema actual; anticipos/factura/seguros; qué le quita tiempo al doctor.
Cuidados: datos de salud (LFPDPPP / HIPAA), consentimiento, nunca consejo médico. ⚠️ Contrato HotlumPowell: construir = orden de cambio de Mario.
Relacionado: calendario de Pablo "Casos - doctores / condominios / OMA".

## 2026-10-13 — Ideas por fases enviadas a Pablo (Telegram msg ~3708)
- F1 MVP "Recepcionista de WhatsApp" (2-4 sem): número WA Business propio; agendar, confirmar, cambiar y cancelar sobre su agenda real; recordatorio 24-48 h con botones; lista de espera; FAQ; escalamiento a la secretaria o al doctor; emergencias → 911.
- F2 Antes y después de la consulta: pre-registro (datos, alergias, motivo, estudios), anticipos o link de pago contra no-shows, seguimiento post-consulta + reseñas en Google.
- F3 Para el doctor: resumen diario, dictado de notas, CFDI y aseguradoras.
- Pitch con números (costo de no-shows; mensajes/día que deja de contestar la secretaria).
- Líneas rojas: nunca consejo médico; datos sensibles (LFPDPPP/HIPAA), aviso de privacidad + consentimiento; solo la API oficial de WhatsApp Business.
- Contrato: ideas/pitch/descubrimiento OK; construir = HotlumPowell/Mario con orden de cambio.
- Pregunté: ¿ya habló con el doctor? Nombre, especialidad, país (México vs. EE. UU.), citas/día, herramienta de agenda actual; ¿one-pager para el doctor o para Mario?

## Modo de trabajo (Pablo, 2026-10-13, msg 3712)
Pablo irá compartiendo sus notas e ideas poco a poco; yo las guardo aquí (por tema) y con cada una aporto ideas, mejoras y puntos de vista que lo cuestionen. Meta: "un producto elevado y bien pensado". Actualizar Mapa_Agente_Consultorio.pdf (doctor_plan.py) conforme se avance.

## Preguntas de producto planteadas (13-oct)
1. ¿Un doctor o muchos? (producto estandarizado vs. solución a la medida; cambia precio, pitch y quién construye/contrato)
2. ¿Cliente real = doctor (paga) o secretaria (usa)? Posicionar como asistente, no reemplazo.
3. ¿Qué tan humano debe sonar? Mi voto: transparente como asistente virtual + salida fácil a humano.

## Notas de Pablo (en orden de llegada)
### Nota 1 (13-oct, msg 3714)
- El doctor es **el papá de Pablo: Dr. Osvaldo González, Internista y Reumatólogo**. Por ahora solo él (no producto multi-doctor).
- Acceso: doctor Y secretaria; la secretaria lo usará más.
- Tono: transparente (asistente virtual declarado).

### Mis aportes a la nota 1
- Especialidad → pacientes crónicos (AR, lupus), mayores, controles frecuentes, laboratorios antes de cita.
- Ideas: (1) entender notas de voz (artritis = difícil escribir); (2) familiares/cuidadores que agendan por el paciente; (3) recordatorio de labs (ayuno) + recibir PDF/foto y ordenarlos para el doctor antes de la consulta; (4) seguimiento proactivo de controles crónicos; (5) solicitudes de receta/resurtido → aprobación SIEMPRE del doctor; (6) bandeja compartida doctor+secretaria con "tomar conversación"; (7) permisos distintos (secretaria: agenda/pagos; doctor: además lo clínico escalado); (8) nombre propio del asistente + aviso de que es virtual en el 1er mensaje.
- Pregunté: ciudad/país del consultorio, ¿uno o varios consultorios?, ¿qué agenda usa hoy la secretaria?

### Nota 2 (13-oct, msg 3716): operación actual
- Presencial: lunes, miércoles y viernes. Remota (Zoom): martes.
- Horario 11:00-20:00 (última cita 19:00). 9:00-11:00 = espacio abierto que el doctor guarda para consultas "especiales/urgentes" que surgen de improviso.
- 60 min por consulta; ~7/día o ~20/semana.
- Hoy: la secretaria manda a las 20:00 la agenda del día siguiente (hora + paciente).
- Los pacientes agendan por teléfono fijo del consultorio o por el WhatsApp de la secretaria.

### Mis aportes a la nota 2
- Capacidad: 9 lugares/día x 4 días ≈ 36/semana vs ~20 usados ≈ 55% de ocupación (falta confirmar hora de comida y horario del martes) → el agente también LLENA la agenda (lista de espera, recordatorio de controles a crónicos, recuperar inactivos), no solo ahorra tiempo.
- 9-11 = espacio protegido: el agente no lo ofrece; solo con autorización y escalamiento.
- Martes por Zoom: liga en la confirmación, recordatorio 1 h antes con instrucciones, labs por adelantado, cobro previo opcional.
- Quick win: automatizar la agenda de las 20:00, enriquecida (1ª vez/subsecuente, confirmó, estudios recibidos, motivo).
- Teléfono fijo: mensaje en el conmutador → WhatsApp; REGLA DE ORO: una sola agenda para teléfono + WhatsApp (sin empalmes).
- Migrar del WhatsApp de la secretaria al número del consultorio + respuesta automática en su número personal.
- Lo cuestioné: ¿subsecuentes de 30-40 min en vez de 60? (decisión del doctor).
- Pregunté: hora de comida, horario del martes, precio por consulta (presencial y Zoom), ciudad.
- Aclaración de capacidad (13-oct, msg 3718): Pablo dijo '11 a 7 son 8 horas'. Le expliqué: si la última cita EMPIEZA a las 19:00 son 9 citas por día (36/semana, ~55% de ocupación); si TERMINA a las 19:00 son 8 (32/semana, ~63%). Pendiente su confirmación + hora de comida.
- ✅ Confirmado (13-oct, msg 3720): la última cita EMPIEZA a las 19:00; suponer comida de 14:00 a 15:00 cada día de consulta → 8 citas por día (11, 12, 13, 15, 16, 17, 18, 19) x 4 días = 32/semana; ~20 usadas ≈ 62% → ~12 huecos/semana (~50/mes).
- Reglas de agenda hasta ahora: no agendar de 14 a 15 ni de 9 a 11 (salvo autorización); martes = Zoom (asumo el mismo horario, por confirmar); 60 min; última cita a las 19:00.
- Falta: precio por consulta (para el argumento de valor), ciudad, horario del martes.

### Nota 3 (13-oct, msg 3722): precio
- Costo por consulta variable, Pablo no lo conoce → SUPUESTO $1,000 MXN.
- Cuentas (x 52/12 semanas por mes): hoy ~$20k/semana ≈ $86.7k/mes; los ~12 huecos/semana valen hasta ~$52k/mes. Conservador +3 citas/sem = +$13k/mes; medio +6/sem = +$26k/mes ≈ +$312k/año (+30%). Sin contar menos faltas ni horas de la secretaria.
- Pitch: "si te llena solo 3 huecos a la semana, ya se pagó solo". Honestidad: el agente facilita llenar, no inventa demanda → medir la ocupación antes y después en el piloto.

### Nota 4 (13-oct, msg 3724): EL OBJETIVO DE FONDO ⭐
- Pablo: una agenda bien organizada permite dar más consultas SIN que su papá se "explote"; lo que busca es que tenga MÁS TIEMPO LIBRE DE CALIDAD, no estar organizando la agenda ni buscando expedientes.
- → Éxito = más consultas O más tiempo libre (que decida el doctor). Dos métricas desde el día 1: (1) ingresos/ocupación, (2) horas libres del doctor.
- Mis aportes: agente "guardián del tiempo" (tope de citas por día definido por el doctor, comida intocable, cero mensajes de pacientes al WhatsApp del doctor → un resumen diario salvo urgencias, noches y fines de semana en silencio); "ficha de 1 minuto" por paciente antes de cada cita (última visita, diagnóstico, medicamentos, estudios nuevos, motivo), solo ordena la información, nunca diagnostica.
- Pregunté: ¿expedientes en papel, Word/Excel o software médico? (si son de papel, digitalizar = proyecto aparte; empezar con pacientes nuevos); ¿el doctor contesta mensajes en noches y fines de semana?

### Nota 5 (13-oct, msg 3726): expedientes
- Hoy: (1) Excel con nombre, diagnóstico, contacto y fecha de última consulta; (2) un Word ÚNICO con el historial y el detalle de todas las consultas ("infinidad de páginas"). El doctor los revisa antes de la consulta o temprano el mismo día. Idea de Pablo: organizarlo por paciente.
- Mis aportes: el Excel sirve para recuperar crónicos por fecha de última consulta → llenar los ~12 huecos con pacientes existentes (con consentimiento para contactarlos por WA). El Word único = mayor riesgo (corrupción/pérdida, búsqueda lenta, datos sin protección; NOM-004-SSA3-2012 pide conservar mínimo 5 años desde el último acto médico, con confidencialidad; verificado en DOF/sidof + guías). Mejora: carpeta por paciente APELLIDO_Nombre_ID + mismo ID en el Excel + respaldo automático cifrado YA (sin IA, quick win).
- Decisión estratégica: A) Excel+Word ordenados + ficha de 1 minuto (mi recomendación para el piloto) vs. B) software de expediente clínico electrónico (NOM-024-SSA3-2012 para sistemas electrónicos) con agenda integrada; evaluar B después del piloto.
- LÍMITE: yo NO recibo ni proceso los expedientes de los pacientes (datos de salud de terceros + contrato). Separar el Word = script en la computadora del doctor o con quien lo construya (Mario); yo diseño el método.
- Pregunté: ¿cada consulta del Word tiene un encabezado uniforme (nombre + fecha)? ¿Tiene respaldo hoy y dónde vive el archivo?

### Nota 6 (13-oct, msg 3728)
- Formato del Word: Pablo no lo sabe, se lo preguntará a su papá (¿cada consulta con encabezado nombre + fecha?).
- Respaldo actual: uno o más USB.
- Mis aportes: huecos (manual/desactualizado; USB sin cifrar = filtración si se pierde; mismo lugar que la PC = robo/incendio). Propuesta 3-2-1: computadora + USB + nube, una copia fuera del consultorio, todo cifrado, nube automática (OneDrive/Google Drive con verificación en dos pasos). Pregunté: ¿Windows o Mac? (para guiar el cifrado: BitLocker/FileVault + respaldo automático).
- El doctor usa **Windows**. Le mandé un plan de 6 pasos (13-oct, msg ~3731): (1) ver la edición Home/Pro; (2) cifrado de dispositivo/BitLocker del disco; (3) USB: BitLocker To Go si es Pro; si es Home → VeraCrypt o USB con cifrado de hardware; clave de recuperación impresa, separada del USB; (4) OneDrive con verificación en dos pasos + carpeta de expedientes dentro + historial de versiones; (5) rutina semanal de USB (viernes) + un USB en casa; (6) probar la restauración. Ofrecí una hoja imprimible de 1 página.

## Asana (13-oct)
Proyecto '🩺 Agente Consultorio · Dr. Osvaldo González' (gid 1219476204985151, board, privado): secciones 0 Bases (gid 1219476097606839), 1 MVP WhatsApp (1219476450441223), 2 Antes/después (1219476204984928), 3 Para el doctor (1219476097643521), 💡 Ideas (1219476097574414); 31 tarjetas + 2 hitos; sin fechas; nunca datos de pacientes. Actualizar con cada nota de Pablo.

### Nota 7 (13-oct, msg 3742): ¿WhatsApp Business con el número FIJO del consultorio?
- SÍ: WhatsApp Business (app y Cloud API) acepta fijos; verificación por llamada de voz ("Llamarme"). Alguien contesta en el consultorio (ojo con conmutadores). El fijo sigue funcionando para llamadas. El número no debe estar en otra cuenta de WA. (Fuentes: Infobip, Sanuker, respond.io.)
- MEJOR que un número nuevo: los pacientes ya conocen el fijo → cero fricción. (Reemplaza mi propuesta de "número nuevo".)
- App (manual, no automatizable) vs. Plataforma/API (la que necesita el agente). Coexistencia desde mayo de 2025: el mismo número en la app y en la Cloud API, chats 1 a 1 sincronizados (los grupos, las llamadas y el catálogo se quedan solo en la app) → la secretaria responde desde la app mientras el agente usa la API. Disponibilidad según país y proveedor: CONFIRMAR para el consultorio. (Fuentes: Kommo, Wati, YCloud.)
- Propuesta: (1) ya: registrar el fijo en la app de WA Business para la secretaria (quick win); (2) después: conectarlo a la API con el agente. Pregunté si lo agrego en Asana, Fase 0.

### Nota 8 (13-oct, msg 3744): ubicación = CIUDAD DE MÉXICO
- Coexistencia de WhatsApp: México fue de los países del lanzamiento inicial (con India, Brasil, Indonesia, EE. UU., Hong Kong, Singapur); hoy está disponible en todo el mundo (chakrahq, msg91) → confirmado para el consultorio.
- Ley de datos: NUEVA LFPDPPP publicada en el DOF el 20-mar-2025, vigente desde el 21-mar-2025 (abrogó la de 2010); el INAI desapareció y la autoridad ahora es la Secretaría Anticorrupción y Buen Gobierno (diputados.gob.mx, Basham, GT Law, Cuatrecasas). Salud = dato sensible → aviso de privacidad + consentimiento expreso; sugerí que lo revise un abogado.
- NOM-004-SSA3-2012 (expediente, 5 años) y NOM-024-SSA3-2012 (sistemas electrónicos).
- Herramientas locales: Mercado Pago (links de pago), CFDI con Facturama/Facturapi, Zoom.

### Nota 9 (13-oct, msg 3748): ¿la sesión de WA debe quedar logueada en una computadora?
- NO: con la Cloud API el agente vive en la nube (Meta → servidor del agente), sin celular ni computadora encendidos.
- Escenario 1 (nadie interviene): solo API; el agente escala por WA o correo.
- Escenario 2 (coexistencia): app de WA Business en el celular de la secretaria; no tiene que estar abierta siempre, pero hay que ABRIR LA APP AL MENOS 1 VEZ CADA 14 DÍAS o la coexistencia puede desconectarse (respond.io, seven.io, sleekflow).
- Recomendé el escenario 2 (supervisión + tomar chats; los 14 días se cumplen solos con el uso diario; cubrir vacaciones).

### Nota 10 (13-oct, msg 3752): "¿primero crear el agente en Claude y luego ligarlo a WhatsApp?"
- Aclaré: un Proyecto o chat de claude.ai NO se conecta a WhatsApp; se necesita Claude por API + un servidor/plataforma puente (webhook de WA → Claude → agenda → respuesta).
- Orden conceptual: (1) el cerebro en papel (reglas, FAQ, escalamiento, tono) = lo que estamos haciendo; (2) WhatsApp: el fijo en la app + verificar Meta Business; (3) puente + Claude API + agenda; (4) pruebas → piloto.
- LÍMITE DEL CONTRATO: no doy la guía de construcción paso a paso (13A(c)); yo me quedo en diseño, reglas, pitch y plan; la construcción va por Mario. Sugerí llevar el tablero a 'Solución IA' (mié 14-oct 11:00 PT) y ofrecí un resumen de 1 página.

### Nota 11 (13-oct, msg 3754): "¿me explicas el paso 3 para hacerlo por mi cuenta, sin servidores de HotlumPowell?"
- Respondí que NO: el contrato (13A(c)) prohíbe usarme para desarrollar o ayudar a desarrollar un agente similar, sin importar los servidores; el Anexo A limita mi uso a temas personales de Pablo (no al negocio de un tercero, aunque sea su papá); riesgo de revocación inmediata. No soy abogada.
- Alternativas ofrecidas: (1) orden de cambio con Mario (mañana, 'Solución IA'); (2) COMPRAR software existente para consultorios en México (agenda + WhatsApp + expediente) → me ofrecí a investigar y comparar contra nuestro mapa; (3) seguir con el diseño; (4) si Pablo aprende por su cuenta, fuera de mí y confirmándolo antes con Mario (la cláusula podría tocarlo a él también).
- Ofrecí: comparativo de software + resumen de 1 página para Mario.
