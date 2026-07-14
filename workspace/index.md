# index.md — Catálogo del workspace de Leeloo ⚡

## Identidad (leer al iniciar)
- `../identity/SOUL.md` — quién soy (Leeloo).
- `../identity/USER.md` — quién es JP, su perfil profesional, preferencias, contexto personal (esposa Fer Kobeh, mudanza a Sunnyvale, Fran Papapietro).
- `../CLAUDE.md` — instrucciones de operación y círculo de confianza.

## Memoria activa
- `MEMORY.md` — memoria de largo plazo: proyectos, flujos, herramientas/capacidades, notas y reglas.
- `log.md` — bitácora de infra y pases nocturnos (DREAMING).
- `memory/AAAA-MM-DD.md` — logs diarios.
  - `memory/2026-07-02.md` — renacimiento v2, migración v1→v2, grupo Telegram Mario+Patti, tarea reseñas Fran, cron matutino.
  - `memory/2026-07-03.md` — ejecución del brief matutino de newsletters (en texto, sin TTS).
  - `memory/2026-07-04.md` — creación proyecto Kaizen ⚡ en Asana + 1er brain dump (6 ideas).
  - `memory/2026-07-05.md` — resumen Morning Brew (edición aniversario 250) + archivado; evento "Dubs 🎾" en calendario.
  - `memory/2026-07-07.md` — fechas Fase 0 Kaizen; cursos PM de JP (triple constraint); inicio F0·1 (definir voz TTS), entorno sin motor de voz.
  - `memory/2026-07-08.md` — rutina diaria de briefs por audio (5:30 AM Morning Brew+eventos, 5:00 PM CFO/Brew Markets, con archivado); hallazgo cron session-only; prueba de generación de imágenes (Nano Banana) → retrato RF final.
  - `memory/2026-07-09.md` — rutina matutina; Kaizen F0·2 cerrada (checklist loops 8 pts + medición A+B+C); llamada Seguridata; newsletter Unframed variante B + **brief para Tavo entregado en PDF y Word** (logo lazos verdes).
  - `memory/2026-07-10.md` — **nueva capacidad STT** (entiendo notas de voz vía ElevenLabs Scribe); logos oficiales de Unframed recibidos; **newsletter variante B2 reordenada** (valor WAMT arriba) + feedback de Tavo fijado.
- `memory/feedback_naming.md` — trato: SIEMPRE "Pablo", nunca "JP"/"Yeipi" (texto y audio).
- `memory/feedback_linkedin_posts.md` — estilo validado de posts de LinkedIn que le gustan a Pablo.
- `memory/feedback_verification_loops.md` — cultura de verificación / double checks (loops), bidireccional.
- `memory/feedback_confirm_before_pdf.md` — confirmar contenido por texto antes de generar PDFs/entregables.
- `memory/project_kaizen_asana.md` — proyecto Kaizen ⚡: GIDs, secciones, backlog de 6 ideas y decisiones.
- `memory/project_ny_trip.md` — viaje a NY (40 de Fer, 12–19 jul 2026): agenda de museos final + PDF entregado.
- `memory/project_support_agent_merlin.md` — iniciativa Kaizen: agente de soporte de redes ("Merlín") que reporta a Leeloo.
- `memory/project_newsletter_marruecos.md` — newsletter semanal de lujo sobre Marruecos (imagen PNG/JPG para Mailchimp, estilo Unframed); script `newsletter_morocco.py`.
- `memory/project_seguridata_agentes.md` — oportunidad: agentes de IA para Seguridata (Alberto Yarza, Director General); minuta y próximos pasos.
- `memory/project_salesforce_job.md` — proceso de reclutamiento de Pablo con Salesforce (rol Financial Services Account Executive); reclutadora Michelle Tobey; hitos y seguimiento.
- `memory/project_infra_caja_voz.md` — aviso Patti/Mario (2026-07-14): retiran motor de voz local (~4.2GB) el 24-jul (no afecta mi voz, uso ElevenLabs nube); oferta caja dedicada $240/año, decisión pendiente de Pablo.

## Minutas
- `minutas/2026-07-09_seguridata_alberto-yarza.md` — 1ª llamada Seguridata (casos de uso de agentes, próximos pasos).
- `minutas/2026-07-09_octavio-horcasitas_newsletter.md` — llamada Pablo × Tavo (Unframed): modelo IA para el newsletter, 3–4 variantes, WAMT como partner.

## Referencias / how-tos
- `ref_context_optimization.md` — optimización de tokens/contexto (Kaizen F0·4): comandos /context, /compact, /clear, /init, /usage; auto-compactación y buenas prácticas. Verificado vs. doc oficial.

## Scripts y assets
- `say.py` — TTS voz oficial (ElevenLabs "Dani") → nota de voz OGG/Opus para Telegram.
- `gen_image.py` — generación/edición de imágenes por IA (Google Gemini "Nano Banana"); ver capacidad en MEMORY.md.
- `newsletter_morocco.py` — newsletter Marruecos, opción A (columna corta estilo Unframed, fotos Rabat).
- `newsletter_morocco_b.py` — newsletter Marruecos, **opción B** (revista/itinerario, canvas marfil, 5 destinos, banda WAMT). Variante elegida por Pablo.
- `newsletter_morocco_b2.py` — **variante B REORDENADA** (2026-07-10): oferta de valor WAMT como hero arriba, destinos al cuerpo, recap+CTA al cierre, emblema oficial verde en el pie. Render en `media/newsletter_morocco_b2.png/.jpg`.
- `brief_pdf.py` — genera el brief de estado Unframed×WAMT en **PDF** (1 pág, PIL, logo arriba-derecha).
- `brief_docx.py` — genera el mismo brief en **Word editable** (.docx, python-docx) para que Tavo comente/edite.
- `newsletter_assets/` — fotos de contactos y recursos del newsletter. Incluye `unframed_ig_profile.jpg` (captura de referencia de la cuenta), `unframed_logo.png` (logo recortado del IG) y `unframed_logo_green.png` (lazos verdes, fondo transparente — el que se usa en el brief).
- `media/` — imágenes definitivas guardadas. `media/pablo_retrato_RF_final.jpg` = retrato RF de Pablo elegido como definitivo (2026-07-08). `media/newsletter_morocco_b.png/.jpg` = render variante B. `media/newsletter_morocco_b2_A.*` y `_C.*` = variante B REORDENADA, tratamientos de hero A (tarjeta) y C (manifiesto). `media/Newsletter_Marruecos_A.pdf` y `_C.pdf` = las dos opciones enviadas a Tavo (2026-07-10). `media/Brief_Unframed_WAMT.pdf/.docx` = brief para Tavo (PDF + Word editable).

## Archivo histórico v1
- `v1/` — histórico curado de OpenClaw (17 bitácoras, 22 sesiones, main.sqlite, notas, media, identidad v1 de referencia). Ver `v1/README.md`.
- `inbox/Info-1.zip` — ZIP maestro v1 (184M), respaldo re-extraíble.
