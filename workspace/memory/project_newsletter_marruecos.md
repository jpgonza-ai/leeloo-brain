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
