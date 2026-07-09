---
name: Proyecto Kaizen ⚡ (Asana)
description: Proyecto Asana "Kaizen ⚡" — sistema de evolución continua de Leeloo; GIDs, estructura y método de trabajo
type: project
---

# Kaizen ⚡ — Asana

Proyecto en Asana creado con JP el **2026-07-04** para estructurar de forma robusta la evolución/mejora continua de Leeloo como asistente de JP. Nombre elegido por JP entre varias opciones (Kaizen = mejora continua en japonés).

**Why:** JP quiere armar "una estructura más robusta" y un espacio que aluda a Leeloo en constante transformación. Filosofía Kaizen = iteración perpetua.

**How to apply:** Se construye **poco a poco**, con orden y coherencia. Método acordado: JP hace **brain dumps** (vacía ideas desordenadas tal cual) y Leeloo las acomoda en la sección correcta. No meter tareas de relleno inventadas.

## IDs
- **Proyecto GID:** 1216278087559836
- **Permalink:** https://app.asana.com/1/1213637453331441/project/1216278087559836
- **Workspace GID:** 1213637453331441
- **Team GID:** 1213637453331443 (name "My workspace")
- **Owner / JP user GID:** 1213637453331429 (Pablo Gonzalez, jpablogov@gmail.com)

## Secciones (ciclo Kaizen: captura → construye → vive → reflexiona)
- 🧠 Backlog de Ideas — GID `1216278091739554` (aquí cae el brain dump crudo)
- 🔧 En Construcción — GID `1216278087600493`
- ✅ Activo / Implementado — GID `1216278247920626`
- 📚 Aprendizajes & Retro — GID `1216278241497222`

Vista por defecto: board. Color: dark-purple.

## ORDEN / hoja de ruta acordada (2026-07-06)
JP pidió ordenar el backlog por dependencias. Principio suyo: **habilitar primero las capacidades en Leeloo, ya probadas, antes de construirlas para Merlín** (él le reporta a Leeloo y ambos revisan antes de publicar). El orden se reflejó **renombrando cada task con prefijo de fase/número** (no hay tool para reordenar posición en Asana):
- **F0 · 1)** Voz TTS (GID 1216278242268473) — JP la puso primera.
- **F0 · 2)** Cultura de loops/verificación (1216278350363414).
- **F0 · 3)** Mapear capacidades (1216278241906203) — la sub-idea "Explorar Obsidian" (1216278349881262) cuelga de aquí, sin número.
- **F0 · 4)** Optimización tokens/contexto (1216278350662259).
- **F1 · 5)** Puente/accesos navegador (1216278242162994) — arranca lunes.
- **F1 · 6)** Edición de reels (1216278296386866).
- **F2 · 7)** Agente Merlín (1216328208091783).
Pendiente: que JP dé el visto bueno final al orden.

## FORMALIZACIÓN ejecutada (2026-07-06, opción A)
JP aprobó formalizar "ligero" (solo dependencias reales + mover arranques; sin desglosar en sub-tasks todavía). Ejecutado en Asana:
- **Dependencia real:** F2·7 Merlín (1216328208091783) **depende de** F1·5 Puente (1216278242162994) **y** F1·6 Reels (1216278296386866). Las de F0 quedan en paralelo (sin dependencias entre sí).
- **Movidas a 🔧 En Construcción** (section 1216278087600493): F0·1 Voz TTS y F1·5 Puente (los dos arranques).
- **Movida a ✅ Activo** (section 1216278247920626): F0·2 Loops (1216278350363414) — por decisión de JP, la cultura de verificación ya es práctica viva, no algo "por construir".
- El resto (F0·3 Mapear, F0·4 Tokens, F1·6 Reels, F2·7 Merlín) sigue en 🧠 Backlog.
Pendiente futuro: si JP pide "a fondo", desglosar cada task en sub-tasks accionables.

## FECHAS por fase (2026-07-06)
JP quiere trazar tiempos poniendo start/due a cada fase y task. **Fase 0 = hoy 6-jul → sábado 11-jul** (cerrar ANTES del viaje a NY del dom 12). Escalonado (puedo trabajar F0 en paralelo):
- F0·1 Voz TTS (1216278242268473): **6→8 jul**.
- F0·2 Loops (1216278350363414): **7→9 jul** — ventana = volver la cultura de verificación MEDIBLE (checklist); la práctica ya vive en Activo.
- F0·3 Mapear capacidades (1216278241906203): **9→11 jul**.
- F0·4 Optimización tokens (1216278350662259): **due 11 jul** (día suelto).
**Decisión JP (2026-07-06):** dejar las fechas de Fase 0 como están y ver si se mueven (son tentativas, no rígidas). **Fase 1 (Puente, Reels) y Fase 2 (Merlín) SIN fecha por ahora** — a propósito, para dejar LIBRE el viaje a NY (12–19 jul, no trabajar Kaizen en el viaje). Se fechan a la vuelta.

## Backlog — 1er brain dump (2026-07-04), 6 ideas
Todas en 🧠 Backlog. (Ver orden/fases arriba.)

1. **Mapear cómo está creada Leeloo** (GID `1216278241906203`) — qué capacidades tengo / no tengo / podría tener y bajo qué implicaciones. Se entiende poco a poco cada que surja el tema. 1er dato: Obsidian NO instalado. Ligada: "Explorar Obsidian juntos" (GID `1216278349881262`).
2. **Conector/MCP de navegador** (GID `1216278242162994`) — acceso con consentimiento a plataformas de JP (LinkedIn/X/IG). Sesión formal **lunes 6-jul 2026** (anclada start/due). Puente Chrome real vs. navegador aislado; libertades por red.
3. **Voz nueva TTS desde cero** (GID `1216278242268473`) — audios más reales. Decisión JP: empezar de cero, no afinar ElevenLabs; abierto a otra plataforma. Destraba el gap TTS (hoy audios caen a texto).
4. **Cultura de verificación / loops** (GID `1216278350363414`) — double checks en toda interacción, BIDIRECCIONAL (JP pidió que lo corrija). Pendiente: volverlo medible (checklist). Ya en `feedback_verification_loops.md`.
5. **Optimización de tokens / contexto** (GID `1216278350662259`) — comandos: /context (diagnóstico), /compact (resume, mismo tema), /clear (fresh). /init NO es optimizador (crea CLAUDE.md). Bonus: auto-compactación, subagentes aislados, memoria en .md, /usage.
6. **Editar reels IG/TikTok** (GID `1216278296386866`) — CapCut confirmado; prioridad velocidad-IA (reels casi listos) > control fino. Rol Leeloo: A) copiloto creativo, B) ffmpeg programático (sin GUI). Liga con #1 y #2.

## Backlog — 2º ingreso (2026-07-06)
7. **🤖 Agente de soporte (Merlín)** (GID `1216328208091783`) — sub-agente que produce contenido de redes y lo revisa con Leeloo antes de publicar; reporta a Leeloo. Reutilizar el "alma" de Merlín (agente que JP creó en claude.ai). Detalle en `project_support_agent_merlin.md`. Depende del puente (#2) para publicar.

## Backlog — 3er ingreso (2026-07-08)
8. **📧 Correo propio de Leeloo (envío de mails con CC a Pablo)** (GID `1216408680019470`) — cuenta Gmail dedicada para que Leeloo ENVÍE correos autónomamente copiando siempre a Pablo. Vía preferida: SMTP + app-password (script tipo say.py), no depende del conector de Gmail ni del navegador. Pasos: Pablo crea cuenta → app-password → llave en `.secrets` (requiere config) → Leeloo arma script. Confirmar antes de enviar salvo libertades. Detalle también en MEMORY.md. Se conecta con el puente pero puede habilitarse aparte. En 🧠 Backlog, asignado a Pablo.
