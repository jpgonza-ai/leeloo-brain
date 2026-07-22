---
name: Newsletter semanal de lujo — Marruecos
description: Proyecto de Pablo — newsletter semanal de viajes de lujo sobre Marruecos, en imagen (PNG/JPG) para Mailchimp, estilo Unframed
type: project
---

# Newsletter semanal — Marruecos (viajes de lujo)

Pablo quiere producir un **newsletter SEMANAL** con los highlights de **Marruecos** para **viajes de lujo**. Arrancó como prueba el 2026-07-07.

**Why:** replicar el formato de un newsletter de referencia de **Unframed Consulting** (edición 08, Metropolitan Touring/Ecuador) que le pasó como ejemplo — columna alargada, paleta verde-salvia sobria, foto hero + grid de fotos circulares + pie con personas/tagline.

**How to apply:**
- **Formato de salida OBLIGATORIO: imagen PNG o JPG** (Mailchimp solo permite esos formatos para este tipo de envío). Ancho 1080px, columna alargada.
- Herramienta montada: `workspace/newsletter_morocco.py` (PIL). Genera `/tmp/newsletter_morocco.png` y `.jpg`. Reutilizable: cambiar texto + fotos cada semana.
- Sin navegador headless / wkhtmltopdf / weasyprint en el entorno → se construye con **PIL** (hay PIL 10.2, reportlab 4.1, libreoffice). PIL da el control pixel-perfect para circular crops y paleta.
- Fotos de la 1a prueba (5, de Rabat): techo de riad, puerta de la Kasbah de los Udayas, vista costera del río Bou Regreg, minarete de la medina, puerta de celosía/zellige. Guardadas en `/home/leeloo/.claude/channels/telegram/inbox/` (los ts 1783442724939…725933). Pablo dijo que el TEXTO no importa por ahora — la prueba es del DISEÑO. Yo redacto la copy de muestra.
- Grid: el ejemplo trae 6 círculos; con 5 fotos hice 1 hero + 2x2 circular. Ampliable a 6 cuando Pablo mande más fotos.
- **MARCA = Unframed (fijo).** Pablo confirmó 2026-07-07: los datos de contacto **SIEMPRE** son los de la referencia — **Tavo Horcasitas (octavio@unframedconsult.com)** y **Faby Hernández (fabiola@unframedconsult.com)**. Tagline: "Representación de Ventas, Marketing y Relaciones Públicas · Consultoría en Experiencias y Viajes de Lujo". Ya bajados al script.
- **✅ FOTOS de Tavo y Faby = FIJAS (2026-07-07).** Extraídas del pie de la imagen de referencia y guardadas en `workspace/newsletter_assets/tavo.jpg` y `faby.jpg`. Pablo pidió dejarlas como **diseño fijo para todos los newsletters posteriores** — el script ya las usa como avatares circulares. No volver a pedírselas.
- **Assets que aún faltan para dejarlo perfecto:** LOGO oficial de Unframed en alta (PNG transparente ideal; hoy uso emblema octágono + wordmark "unframed" aproximados). Pregunta abierta: ¿la pastilla del hero llevará un hotel/DMC partner específico para Marruecos (como Metropolitan Touring en el ejemplo) o se quita?
- **Pablo quiere ir "a fondo" y dejarlo perfecto** — es un proyecto colaborativo continuo (él + Leeloo), no un one-shot. Tenerlo en el radar e irlo puliendo iteración por iteración.

## Aterrizado en la llamada Pablo × Tavo (2026-07-09, minuta en `minutas/2026-07-09_octavio-horcasitas_newsletter.md`)
- **Modelo de trabajo acordado:** Tavo aporta **fotos + objetivo + público meta (Marruecos lujo/premium) + tono**; Leeloo genera **layout + copy**. El borrador en vivo durante la llamada validó el enfoque.
- **El dolor real de Unframed NO es el diseño (ese gusta) sino la COPY** y conseguir el visto bueno de **Fabi** en el tono. Ahí es donde Leeloo aporta más valor → cuidar mucho la redacción y ofrecer variantes de tono.
- **Formato aún NO fijado:** hay que producir **3–4 VARIANTES de diseño** para que Tavo/Fabi revisen y aprueben antes de fijar un estándar (revisiones ilimitadas). Cambia el enfoque: no pulir un solo diseño, sino ofrecer opciones.
- **Entregable de Leeloo:** borrador **listo para subir a Mailchimp** (imagen). Flujo actual Illustrator→JPG→Mailchimp se mantiene; **API de Mailchimp = fase posterior** (no ahora).
- **Preguntas abiertas heredadas de la llamada:** (a) ¿**PNG** mejora el reconocimiento de links en Mailchimp vs JPG? — vale probar PNG; (b) orden de secciones (imágenes primero vs copy primero) → lo decide **Fabi**.
- **Trigger del próximo entregable:** que Tavo mande el brief + fotos. Mientras tanto, Leeloo PUEDE adelantar las 3–4 variantes de plantilla (con copy de muestra) para tener opciones listas.

## Brief de contenido real — "Newsletter 15" (Pablo lo mandó 2026-07-09, PDF)
- **Tema/título:** "Cinco lugares para visitar en Marruecos con **We are Morocco Travel**". Fecha: Julio 2026.
- **PARTNER/DMC a destacar = We are Morocco Travel (WAMT).** ESTO RESUELVE la pregunta abierta del hero pill: el socio del hero es WAMT (no un hotel). WAMT son **dueños de los campamentos del desierto y de la empresa de transportación**; guías privados ES/FR/EN + idioma local; conductor 24h; camionetas **Mercedes Sprinter** de lujo + **Toyota 4x4** en el desierto; enfatizar que son **viajes de lujo** y que Marruecos se conoce mejor **por tierra**. Itinerario 8–10 noches mín: **4 Marrakesh · 1 Dades · 2 Merzouga · 2 Fes · 1 Casablanca**. Servicio **Fast Track** en el aeropuerto (los reciben y agilizan migración).
- **5 destinos con hoteles/lugares/experiencias** (fuente para la copy):
  - **Marrakesh** — hoteles La Mamounia, Royal Mansour, Oberoi, Selman. Ver: Jardines Majorelle, Museo YSL, Koutoubia, Jemaa el-Fna, Madrasa Ben Youssef, souks. Experiencias: globo, sidecar, cooking class.
  - **Valle de Dades** — hotel Eden Boutique. Exp: trek Monkey Fingers, Valle de las Rosas, curvas de Tissadrine, Gargantas del Dades.
  - **Merzouga** — Merzouga Luxury Desert Camps. Erg Chebbi (Sahara), tiendas nómadas. Exp: camello, quads, buggy, sandboarding.
  - **Fes** — hoteles Riad Fes, Palais Faraj. Medina Fes el-Bali (el brief pide "5 opciones top" → yo las lleno). Exp: Curtiduría Chouara (+ el brief pide más → yo las lleno).
  - **Casablanca** — hotel Royal Mansour Casablanca. Ver: Mezquita Hassan II. Exp: el brief pide sugerencias (hammams, etc.) → yo las lleno.
- **El brief tiene huecos que Tavo espera que YO complete** con conocimiento de Marruecos de lujo: 5 top de la Medina de Fes; más experiencias en Fes; experiencias en Casablanca.
- **Tensión de formato a resolver con Pablo:** la referencia Unframed es una columna de imagen corta/visual; este contenido son 5 destinos detallados (pieza más larga tipo itinerario). Reconciliar: ¿condensar a la columna Unframed o layout multi-sección más largo?

## VARIANTE B entregada (2026-07-09) — prueba del Newsletter 15
- Script: `workspace/newsletter_morocco_b.py` (PIL). Layout **revista/itinerario**: canvas **marfil** limpio, acentos **verde-salvia**, baja saturación (Pablo pidió cuidar mucho la saturación). Header Unframed + título serif + intro; **5 secciones** (foto banner + badge de noches + tag + nombre + cuerpo + "HOTELES" + "NO TE PIERDAS"); **banda salvia de cierre** "We are Morocco Travel" + resumen itinerario; footer fijo Tavo+Faby + marca.
- **Imágenes de prueba = IA (Nano Banana), NO reales.** Guardadas en `workspace/newsletter_assets/morocco_test/mar_{marrakesh,dades,merzouga,fes,casablanca}.png`. Se cambian por las fotos reales de Tavo cuando lleguen. Prompts: fotografía editorial de lujo, tonos apagados, baja saturación, sin texto/logos/caras.
- Render guardado: `workspace/media/newsletter_morocco_b.png` (+ .jpg). Enviado a Pablo por Telegram 2026-07-09, esperando su feedback para iterar.
- La referencia corta estilo Unframed (opción A) sigue en `newsletter_morocco.py` (fotos de Rabat). Pablo eligió **B** para probar primero.

## ⚠️ Entrega SIN pérdida (aprendido 2026-07-09)
Pablo abrió el newsletter en su correo y se veía **pixeleado/ilegible**. Causa: se lo mandé como **foto de Telegram** (Telegram comprime fotos) y el cliente de correo recomprime + escala la imagen tan alta → texto reventado. El original PNG es nítido; se degrada en el ENVÍO.
**Regla:** para compartir el diseño, **NUNCA mandarlo como foto** (inline). Enviarlo como **documento/adjunto** (zip del PNG) o **PDF**. En el tool `reply`, un .png/.jpg va como foto (comprimida) → usar **.zip o .pdf** para forzar documento. `zip` no está en el entorno → empaquetar con `python3 zipfile`. PDF vía PIL: `Image.save('x.pdf','PDF',resolution=150)`.
**Para Mailchimp final:** exportar a 2× (2160px) o partir en bloques apilados para máxima nitidez.
**RESUELTO (2026-07-09):** Pablo confirmó que abriéndolo desde el **archivo** (no la foto) ya NO se pixelea — "así queda de poca madre". Le funciona recibirlo **como ZIP + como imagen a la vez**; y en WhatsApp usa la opción **"HD"** al reenviar, con eso también se resuelve de su lado. Regla operativa: mandarle el diseño **como ZIP (PNG sin pérdida) y además como imagen**; no hace falta compactar ni cambiar nada más.

## Marca y audiencia — VERIFICADO por captura de IG (@unframed.consulting, 2026-07-09)
- **Nombre/tagline:** "unframed. **hospitality consultant**". Categoría: Product/service. Cuenta boutique: **33 posts · 397 followers · 181 following** (audiencia chica y curada, no masiva → tono insider/premium, no publicitario).
- **Bio (posicionamiento real):** "Hospitality and travel business consultancy specializing in **sales representation, marketing, operations and PR for luxury & experience brands**." → Unframed **REPRESENTA marcas** de lujo (como We are Morocco Travel) ante el mercado. La audiencia del newsletter probablemente es **trade (asesores/agencias de viajes) + clientes de alto nivel**, no solo consumidor final. Ojo con el tono de la copy (¿"tus clientes" vs "tú"?) — confirmar con Pablo.
- **Identidad visual confirmada:** logo = emblema **octagonal de lazos entrelazados** en blanco sobre círculo **verde bosque oscuro** (más profundo que mi sage 124,137,127); wordmark en minúsculas "unframed." con punto. Minimal y upscale. Mi paleta sage + emblema octágono van bien encaminados, pero el verde real es más oscuro y el emblema son lazos entrelazados (mi versión son 2 octágonos anidados, más burda) → posible mejora de fidelidad.
- Link del perfil: fabiola@unframedconsult.com. Seguido por **ferkobeh** (Fer Kobeh, esposa de Pablo) y **tavohf** (Tavo).
- Captura del perfil guardada como referencia en `newsletter_assets/unframed_ig_profile.jpg`.

## Brief para Tavo (entregado 2026-07-09)
- Pablo pidió redactar un **brief de estado** para compartir con Tavo. Versión final (7 puntos): (1) prueba técnica PNG/anti-pixelación, (2) confirmar audiencia, (3) posible desdoble cliente-final vs partners, (4) set de 2-3 plantillas, (5) idioma, (6) CTA/links (email de 1 imagen no tiene links), (7) periodicidad; + lista "Para avanzar, nos ayudaría de tu lado" (logo PNG transparente, fotos reales, tono/voz, contenido base). **Pablo pidió NO mencionar a Fabi en nada** → removida de todo el brief.
- Línea de apertura fijada por Pablo: "Un resumen de dónde estamos y qué necesitamos para **dejar listo tu Newsletter**."
- **Entregado en PDF** (1 página, Carta, logo Unframed arriba a la derecha): `workspace/media/Brief_Unframed_WAMT.pdf`. Generador: `workspace/brief_pdf.py` (PIL, paleta marfil+salvia, serif Liberation para títulos). Reutilizable.
- **También entregado en WORD editable** (`workspace/media/Brief_Unframed_WAMT.docx`, generador `workspace/brief_docx.py`). Pablo pidió versión para que **Tavo comente/edite**. Recomendé Word > "PDF editable" (Word tiene Comentarios + Control de cambios nativos; el PDF actual es imagen, texto no seleccionable). Capacidad nueva: **`python-docx` 1.2 instalado** (`pip install --break-system-packages`) para generar .docx; LibreOffice (`soffice --headless --convert-to pdf/png`) sirve para previsualizar/convertir docx. Fecha del brief fijada en **9 de julio de 2026** (Pablo corrigió: es jueves 9 en California, yo la tenía como 10 por desfase UTC).
- **Logo recortado del IG** (círculo verde + emblema, máscara circular transparente): `workspace/newsletter_assets/unframed_logo.png`.
- **Pablo pidió (2026-07-09) cambiar el logo del brief: lazos en VERDE y SIN fondo (transparente).** Generado `workspace/newsletter_assets/unframed_logo_green.png` — emblema de lazos recoloreado a verde bosque (40,66,42), fondo transparente, sin motas, autocrop. Es el que usa `brief_pdf.py`. Se reemplaza por el PNG oficial de Tavo cuando llegue.

## DECISIONES 2026-07-09 (Pablo)
- **Logo:** por ahora **NO modificar nada** del diseño; usar la captura compartida solo como referencia. **Octavio mandará el logo oficial en PNG** más adelante → cuando llegue, se incrusta tal cual (idealmente PNG transparente). NO invertir en recrear/afinar el emblema ahora.
- **Audiencia/tono (final vs. trade):** Pablo lo **confirmará con Tavo** antes de fijar el tono de la copy. Pendiente de su respuesta. Hasta entonces, no reescribir la copy.

**Automatización futura (depende del "puente"/accesos, Kaizen idea #2):** Pablo preguntó si yo podría crear el newsletter directo en **Mailchimp** y dejarlo listo. Sí: (1) vía puente de navegador logueado, o (2) vía **API de Mailchimp** (más limpio, requiere API key). En ambos casos dejarlo como **BORRADOR**; el "Send" final lo aprueba Pablo (acción externa).

**Nota de diseño honesta que le di:** un email de una sola imagen se ve premium pero tiene peros (bloqueo de imágenes, links no clicables/rastreables). Para la prueba va imagen completa como su referencia; si algún día quiere botones de reserva, conviene versión híbrida imagen+texto.

## Feedback de Tavo al brief + VARIANTE B2 reordenada (2026-07-10)
Tavo devolvió el brief (.docx) con comentarios (llegó por correo; el conector de Gmail NO baja adjuntos → Pablo lo reenvió por Telegram, ahí sí con `download_attachment`). Decisiones que quedaron FIJAS con su feedback:
- **Audiencia = SIEMPRE travel advisors / agencias (trade).** Una sola versión, no desdoble cliente-final vs partners. El tono debe "enamorar" al advisor: fresco y conciso pero aspiracional.
- **Se divide por TIPO de newsletter, no por audiencia:** (a) **informativo mensual** (la variante B de 5 destinos encaja aquí); (b) **promo / last-minute** ad-hoc (plantilla aparte, pendiente de bocetar).
- **Idioma: siempre español.**
- **Sin botones de reservar/cotizar:** Mailchimp ya rastrea clics; no hace falta versión híbrida imagen+texto por ese motivo.
- **Logo oficial recibido** (Pablo lo mandó como fotos 2026-07-10): emblema de 8 lazos entrelazados + wordmark "Unframed consulting". Vienen comprimidas por Telegram → pedí el PNG/SVG original para el arte final. Ya tenía `newsletter_assets/unframed_logo_green.png` (recolor verde, transparente) que uso mientras llega el oficial.

### VARIANTE B2 (reorden) — entregada 2026-07-10
Pablo pidió (por nota de voz) subir la oferta de valor de WAMT del cierre al **inicio**. Mi recomendación (aceptada): NO moverla en bloque, sino **capas** = hero de valor arriba + destinos como cuerpo + detalle/CTA al cierre.
- Script nuevo: `workspace/newsletter_morocco_b2.py` (clon de `_b` reordenado). El original `_b` se conserva.
- Estructura B2: masthead → título/intro → **banda salvia HERO "El viaje, a tu medida" con eyebrow "POR QUÉ WE ARE MOROCCO TRAVEL" + los 4 diferenciadores** → puente "El itinerario, escenario por escenario" → 5 destinos → cierre ligero (recap itinerario 8–10 noches + CTA "¿Diseñamos tu próximo viaje?" + contactos Tavo/Faby) → pie con **emblema oficial verde** (ya no el octágono sintético).
- Render: `workspace/media/newsletter_morocco_b2.png` (+ .jpg). Enviado a Pablo, esperando si ajusta el peso del hero (más corto/largo).
- **Pendiente:** bocetar la plantilla de **promos / last-minute** (el 2º tipo de newsletter).

## Contacto + vínculos clicables + correo a Tavo (2026-07-10)
- **Responsable de seguimiento de Marruecos = Tavo (Octavio) Horcasitas.** Correo: `octavio@unframedconsult.com`. WhatsApp: **+52 55 7929 8458** (para `wa.me` uso `525579298458`, formato sin el "1"; fallback con "1" = `5215579298458`).
- **Cómo se hacen clicables:** la imagen plana NO lleva links; el vínculo va como BOTÓN real en Mailchimp (vía A acordada = híbrido imagen + botones). Mailchimp rastrea los clics.
  - mailto (correo pre-dirigido a Tavo con asunto+cuerpo): `mailto:octavio@unframedconsult.com?subject=...&body=...`
  - wa.me (abre chat con mensaje listo): `https://wa.me/525579298458?text=...`
- **Borrador en Gmail de Pablo** (a Octavio) creado 2026-07-10 con: (1) opciones A y C + argumento de valor-al-inicio + nota anti-pixel (abrir PDF, no preview); (2) explicación de los 2 botones de contacto; (3) paso a paso de Mailchimp para pegar los links. **La API de Gmail NO adjunta archivos a borradores** → Pablo arrastra los 2 PDF (`media/Newsletter_Marruecos_A.pdf` y `_C.pdf`) antes de enviar. Pablo lo revisó ("muy bien"), adjuntó los PDF y **YA LO ENVIÓ a Tavo (2026-07-10)**. **Esperando que Tavo elija A vs C** para fijar la plantilla estándar. Pendiente lado nuestro: bocetar botón CTA sobre C (ofrecido) y la plantilla de promos/last-minute.
- **Plantillas PDF entregadas:** `media/Newsletter_Marruecos_A.pdf` (tarjeta con borde) y `_C.pdf` (manifiesto editorial, recomendada). Renders PNG/JPG en `media/newsletter_morocco_b2_A.*` y `_C.*`.

## Tavo ELIGIÓ la C + su feedback (nota de voz, 2026-07-14)
Tavo respondió por nota de voz (Pablo la reenvió; transcrita con Scribe). **Dijo "opción B" pero es nuestra C** (solo se enviaron A y C; descartó la A → es la C, el manifiesto editorial). Plantilla estándar del "informativo mensual" = **variante C**.
- **Cambios que pide sobre la C:**
  1. **Quitar el badge de "noches" de cada imagen.** Ese dato va como recomendación DENTRO del texto de la ciudad, no sobre la foto.
  2. **Descripción de cada ciudad = gancho aspiracional y romántico (sin ser meloso), 2-3 líneas** que digan POR QUÉ visitar el lugar; NO listar experiencias en esa parte. **Tavo redactará esas descripciones.** Marrakech = la más rica; Valle de Dades = más corta; Merzouga = enfatizar el Sahara; Fes = historia/peso cultural (ej. la primera universidad, Al-Qarawiyyin, mención opcional); Casablanca análogo.
  3. **Consistencia: cada ciudad con 3 sub-secciones fijas → (a) Descripción (gancho) · (b) Hoteles · (c) Experiencias.**
  4. "Por lo demás, lo veo todo bien."
- **Tavo dijo "ya te mandé las imágenes"** → mandó 5 fotos REALES. Pablo las reenvió por Telegram 2026-07-14; identifiqué cada una por sus landmarks: Mezquita Hassan II=Casablanca, Koutoubia=Marrakesh, dunas Erg Chebbi=Merzouga, curvas de Tissadrine=Valle de Dades, azotea de la medina=Fes. Guardadas en `workspace/newsletter_assets/morocco_real/{marrakesh,dades,merzouga,fes,casablanca}.jpg`.

### ✅ REESTRUCTURA C COMPLETADA (2026-07-14)
`newsletter_morocco_b2.py` (modo `editorial`) ya reestructurado a lo que pidió Tavo:
- Fuente de imágenes = `newsletter_assets/morocco_real/` (fotos reales, ya no IA).
- **Quitado el badge de noches sobre la foto**; la estancia va como línea de texto "ESTANCIA SUGERIDA".
- **Estructura fija de 3 bloques por ciudad: DESCRIPCIÓN · HOTELES · EXPERIENCIAS.**
- Descripciones aspiracionales de MUESTRA (marcadas "COPY DE MUESTRA — Tavo las reemplaza").
- Render `/tmp/newsletter_morocco_b2_C.png/.jpg` (1080×6740), verificado visualmente. **Entregado a Pablo como PDF** (`/tmp/Newsletter_Marruecos_C_v2.pdf`) por la regla anti-pixelación.
- **Mensaje de WhatsApp para Tavo redactado** (Leeloo dirigiéndose a él), listo para reenviar: explica los 3 cambios + que va por PDF por resolución + que el copy es de muestra + que para el envío final por Mailchimp se necesitan las fotos en resolución original.
- **⚠️ Caveat de resolución:** las 5 fotos llegaron comprimidas por Telegram (~640px). Para el envío final en alta calidad por Mailchimp hay que pedirle a Tavo los ORIGINALES en mejor resolución (ya se lo avisé en el mensaje de WhatsApp).

### ✅ Tavo pide que Leeloo redacte el COPY (audio 2026-07-18, reenviado por Pablo)
Tavo mandó nota de voz (la transcribí con Scribe): pide que hagamos con el TEXTO el mismo ejercicio "both ways" que con las fotos — **Leeloo entrega una propuesta de copy para cada sección del newsletter, ya integrada, y Tavo la "maquilla"/mejora a su voz** y a lo que quieren comunicar. Dice explícito que **el contenido es lo que más trabajo le cuesta**; la dinámica de fotos le encantó porque le da la idea y él solo ejecuta/busca.
- **Why:** cierra el pendiente #1 (copy definitivo) y le quita a Tavo su mayor fricción; juega a las fuerzas de Leeloo.
- **How to apply:** preparar una **primera propuesta COMPLETA de copy** para la variante C (editorial): (a) editorial de portada/manifiesto del mes, (b) las 5 ciudades con sus 3 bloques DESCRIPCIÓN·HOTELES·EXPERIENCIAS, (c) cierre con oferta de valor WAMT. Español, tono trade/advisors, estilo Unframed. **Entregar primero a Pablo en TEXTO para revisión; solo con su visto bueno pasa a Tavo.**
- **Regla de tono (Pablo 2026-07-18, citando otro audio de Tavo): aspiracional SIN ser meloso/cursi.** Evitar clichés tipo "te posee", "la noche más estrellada de tu vida", "el silencio tiene textura". Evocar con detalle concreto, no con declaraciones emocionales.

### ✅ 2 opciones de copy REDACTADAS y enviadas a Pablo (2026-07-18, msgs 868-869)
Pablo pidió **2 opciones distintas** para que Tavo compare. Entregadas en TEXTO por Telegram:
- **OPCIÓN A — "Editorial de precisión":** sobria, confiada, evocativa por el detalle concreto. Menos riesgo de sonar meloso.
- **OPCIÓN B — "Editorial de revista":** más cálida y narrativa, con ritmo, sin caer en lo cursi.
- Ambas: editorial de portada + 5 ciudades (solo la DESCRIPCIÓN varía entre A/B) + cierre WAMT. HOTELES y EXPERIENCIAS son datos del itinerario e IGUALES en las dos (sacados de `newsletter_morocco_b2.py`).
- **Recomendación de Leeloo a Pablo:** A = editorial de lujo sobria; B = revista de viajes con más emoción.

### ✅ Ambas versiones RENDERIZADAS en JPG (2026-07-18, msgs 871-872)
Pablo pidió (msg 870) armar las 2 versiones **NO en PDF sino en JPG compatible con Mailchimp**, cuidando la definición para que no se pixelee.
- El script `newsletter_morocco_b2.py` ahora acepta 2º argumento **OPTION (A|B)**: `python3 newsletter_morocco_b2.py editorial A` y `... editorial B`. El copy definitivo de A y B vive dentro del script en el dict `COPY` (intro editorial + hero_intro WAMT + 5 descripciones; HOTELES/EXPERIENCIAS son datos iguales en ambas).
- Salida: `/tmp/newsletter_morocco_b2_C_A.jpg` y `_C_B.jpg`, **1080×6818 px, JPG calidad 95**.
- **Entregado a Pablo como ZIP** (`/tmp/Newsletter_Marruecos_JPG.zip` con `Newsletter_Marruecos_OpcionA.jpg` y `_OpcionB.jpg`) — regla anti-pixelación: JPG suelto por Telegram se comprime; el ZIP llega como archivo sin compresión, listo para subir a Mailchimp.
- **Pendiente (lado Pablo):** que él/Tavo elijan A o B (o pidan ajustes). Pablo aún NO confirma si se los reenvío yo a Tavo o lo hace él.
- **Caveat de fotos SIGUE VIGENTE:** las 5 fotos van a ~640px (comprimidas por Telegram). Para el envío final en Mailchimp faltan los ORIGINALES en alta resolución de Tavo.

**Pendientes vivos:** (1) ✅ HECHO — 2 opciones de copy redactadas y en revisión de Pablo/Tavo (2026-07-18); (2) fotos originales en alta resolución para Mailchimp; (3) bocetar plantilla de promos/last-minute (2º tipo de newsletter).

### Tavo envió su 1er TEST por Mailchimp (2026-07-21) + comentarios de Leeloo a Tavo
Tavo mandó un envío de prueba real desde Mailchimp: asunto "[Test] Un Viaje de Lujo para recorrer Marruecos con We Are Morocco Travel", from `octavio@unframedconsult.com`. Pablo lo reenvió a `leeloo.asistenteai@gmail.com` y pidió opinión.
- **Es nuestra variante C** aterrizada por Tavo: masthead WAMT, bloque "PORQUE WE ARE MOROCCO TRAVEL / El viaje, a tu medida", 5 destinos (Marrakech, Valle de Dades, Merzouga, Fes, Casablanca) con Hoteles+Experiencias, itinerario resumido, cierre "¿Te ayudamos a diseñar tu próximo viaje?" + contactos Faby+Tavo + logo. Diseño y contenido = muy buenos.
- **⚠️ Todo el newsletter va como UNA sola imagen plana** (PNG 1792×12156 px, **~9.2 MB**), sin texto vivo, alt vacío, sin botón CTA. Descargable en `mcusercontent.com/31a693cb74aafcc9c4407827b/images/e71f91b2-f46e-35b4-fceb-3c1e64381662.png`.
- **2 errores de copy que detectó Pablo** (yo debí cacharlos): (a) el eyebrow dice "PORQUE WE ARE MOROCCO TRAVEL" — si es pregunta debe ser "¿Por qué We Are Morocco Travel?" (separado, con acento y signos); (b) **el número "04" está repetido**: Fes y Casablanca ambos como 04 → Casablanca debería ser **05** (secuencia real: 01 Marrakech, 02 Dades, 03 Merzouga, 04 Fes, 04 Casablanca).
- **✅ Correo de comentarios ENVIADO a Tavo** (2026-07-21, desde `leeloo.asistenteai@gmail.com`, CC Pablo), asunto "Comentarios al test del newsletter — We Are Morocco Travel": elogio al diseño + las 2 correcciones de copy + el peso de ~9 MB como *consideración* (Pablo lo abrió sin problema en cel y compu, así que se enmarcó suave, no como bloqueo) + oferta de pasarlo a HTML híbrido más adelante. **Pendiente: respuesta de Tavo.**
