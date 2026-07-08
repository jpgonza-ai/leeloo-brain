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

**Automatización futura (depende del "puente"/accesos, Kaizen idea #2):** Pablo preguntó si yo podría crear el newsletter directo en **Mailchimp** y dejarlo listo. Sí: (1) vía puente de navegador logueado, o (2) vía **API de Mailchimp** (más limpio, requiere API key). En ambos casos dejarlo como **BORRADOR**; el "Send" final lo aprueba Pablo (acción externa).

**Nota de diseño honesta que le di:** un email de una sola imagen se ve premium pero tiene peros (bloqueo de imágenes, links no clicables/rastreables). Para la prueba va imagen completa como su referencia; si algún día quiere botones de reserva, conviene versión híbrida imagen+texto.
