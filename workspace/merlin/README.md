# README.md — El mapa de la carpeta-cerebro de Merlín 🗺️

> Qué hay en esta carpeta, dónde está cada cosa y para qué sirve.
> Borrador 2026-07-29 (Leeloo).

## Los tres archivos que hacen el cerebro
| Archivo | Rol | Qué contiene |
|---|---|---|
| `CLAUDE.md` | La constitución | Quién es Merlín, su misión, cómo trabaja, qué nunca hace, perfil de Pablo. |
| `README.md` | El mapa (este archivo) | Qué hay en la carpeta y dónde encontrarlo. |
| `bitacora.md` | La memoria | Qué pasó, qué se decidió, qué sigue pendiente (orden cronológico inverso). |

## Las carpetas (el "cuerpo" del cerebro)
- **`empresas/`** — una nota por empresa objetivo. Negocio, cultura, comp, noticias, por qué encaja Pablo, quién entrevista. Nombre de archivo = `[[NombreEmpresa]].md` (ej. `Stripe.md`).
- **`vacantes/`** — una nota por posición concreta. Link, requisitos, fit vs. perfil de Pablo, estado, fecha. Enlaza a su `[[empresa]]`.
- **`contactos/`** — reclutadores, referencias, gente del círculo. Cómo se conectó, último contacto, próximos pasos.
- **`entrevistas/`** — prep y notas por entrevista. Preguntas probables, respuestas STAR, feedback post-entrevista.
- **`materiales/`** — CV(s), cover letters, pitch personal, banco de historias STAR, versiones por rol.

## Convenciones
- **Todo es Markdown (.md)** = texto plano legible. Se edita en cualquier editor (Bloc de notas, VS Code) o en Obsidian.
- **Enlaces `[[wikilink]]`**: conectan notas entre sí (empresa ↔ vacante ↔ contacto ↔ entrevista). Eso convierte la carpeta en un grafo navegable en Obsidian.
- **Nombres claros y estables**: mejor `Stripe.md` que `stripe_final_v2.md`.
- **Fechas absolutas** siempre (`2026-07-29`), nunca "ayer" / "la próxima semana".

## Pipeline (dónde ver el estado de todo)
El seguimiento vivo del proceso de cada aplicación se lleva en `bitacora.md` (por ahora) y se resume por empresa/vacante en sus notas. Si crece, se separa a un `pipeline.md` tipo tablero (Prospecto → Aplicado → Entrevista → Oferta → Cerrado).

## Cómo se usa
1. Merlín investiga y **escribe** en las notas correspondientes.
2. Registra los movimientos y decisiones en `bitacora.md`.
3. Le reporta a Leeloo; Leeloo cura y se lo pasa a Pablo.
4. Nada externo (aplicar, escribir a alguien) sale sin OK de Pablo.
