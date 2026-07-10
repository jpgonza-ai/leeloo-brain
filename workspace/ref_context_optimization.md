# Optimización de tokens / contexto — referencia (Kaizen F0·4)

Cápsula verificada contra la doc oficial de Claude Code (2026-07-09, vía agente `claude-code-guide`). Para consulta de Pablo cuando quiera.

## Modelo mental
El contexto es una "memoria de trabajo" finita. Todo lo que entra ocupa espacio: la conversación, los archivos abiertos, las herramientas cargadas. Al llenarse, se pierde/resume lo más viejo. Optimizar = mantener ese espacio limpio y enfocado.

## Los comandos (de operador — se teclean en la REPL interactiva)
- **/context** → radiografía: muestra qué está ocupando el contexto ahora (archivos, reglas, hooks, definiciones de herramientas MCP). Para diagnosticar.
- **/compact** → resume/condensa la conversación para liberar espacio SIN cambiar de sesión. Acepta instrucción opcional: `/compact enfócate en X`. La compactación misma cuesta tokens.
- **/clear** → borrón y cuenta nueva (limpia el historial de la sesión). Relacionado: **/rewind** puede retomar algo previo al clear (función reciente, 2026).
- **/init** → MITO: NO optimiza tokens. Solo crea/inicializa el archivo `CLAUDE.md` (instrucciones persistentes del proyecto).
- **/usage** → reporta qué está impulsando tus límites (función reciente, 2026).

## Auto-compactación (automática)
Claude gestiona el contexto solo al acercarse al límite: primero borra outputs viejos de herramientas, luego resume la conversación. Conserva peticiones y fragmentos clave; puede perder instrucciones tempranas muy detalladas. Si un solo archivo es tan grande que rellena el contexto de inmediato, se detiene ("thrashing").

## Buenas prácticas
1. Un tema por sesión; al cambiar de tema grande → /clear (borrón limpio).
2. En sesiones largas, /context para monitorear; si vas alto, /compact.
3. Lo permanente va en ARCHIVOS (`CLAUDE.md`, memoria `.md`), no repetido en el chat — sobrevive a la compactación.
4. Trabajo pesado (research, muchos archivos) → subagentes: contexto aislado, no ensucian el hilo principal.
5. Skills y herramientas MCP cargan bajo demanda (los schemas se difieren) → menos peso base.

## Cómo aplica a Leeloo (mi caso)
Los comandos manuales son de operador; yo NO me los ejecuto sola. En mí la optimización corre por: (a) **auto-compactación** automática del sistema, (b) **memoria en archivos .md** (por eso persisto entre sesiones), (c) **subagentes** para trabajo pesado. Por eso Pablo puede brincar de tema sin previo: cargo el hilo y releo mi memoria al iniciar.
