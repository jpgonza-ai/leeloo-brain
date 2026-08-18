---
name: Publicar en X (Twitter) a nombre de Pablo
description: Capacidad y setup para postear en la cuenta de X de Pablo (@jpablo11g) vía API v2 + OAuth 1.0a; script, llaves, reglas y pendientes.
type: project
---

# Publicar en X a nombre de Pablo — ONLINE (2026-08-07)

Capacidad montada dentro de Kaizen (F1·5 el Puente / permisos de redes). Sustituye a LinkedIn nativo para el objetivo de PUBLICAR, porque LinkedIn queda bloqueado por la IP de datacenter.

**Why:** Pablo (2026-08-07) decidió soltar LinkedIn nativo (Merlín leerá vacantes en bolsas públicas) y pidió que Leeloo postee en X a su nombre ~1 vez al día o cada 2 días. Eligió el Camino 1 = API oficial de X (robusto, sin cookies ni problema de IP), sobre el Camino 2 (Puente con cookie de sesión, frágil, mismo riesgo de IP).

**How to apply:** cuando Pablo pida un tweet o toque publicar en X, usar el script de abajo. Al inicio SIEMPRE mostrar borrador por Telegram y publicar SOLO con su OK (aún no hay "libertades" de publicación directa).

## Datos técnicos
- Cuenta: **@jpablo11g** (id 171508218, name Juan Pablo Gonzalez).
- Método: **API v2 + OAuth 1.0a user context**, permiso **Read and Write**.
- **Script: `workspace/scripts/x_post.py`** (SOLO stdlib: hmac/hashlib/base64/urllib, para no depender de pip por el firewall).
  - `python3 x_post.py --verify` → GET `/2/users/me`, valida credenciales, NO publica.
  - `python3 x_post.py --text "..."` o `--text-file /tmp/t.txt` → POST `/2/tweets`. Avisa si el texto pasa de 280 chars.
  - Firma OAuth1: firma method+URL+params ordenados (los oauth_* + query; el body JSON de v2 NO va en la firma); signing key = `consumer_secret&token_secret`; HMAC-SHA1 → base64.
- **Llaves cifradas/protegidas en `/home/leeloo/openclaude/.secrets/x_api.json`** (chmod 600, mismo almacén que la app-pw de Gmail): `consumer_key`, `consumer_key_secret`, `access_token`, `access_token_secret`.
- Se publica directo desde **nbg1** (api.x.com alcanzable; verificado 401 y luego --verify OK).

## Setup (hecho 2026-08-07)
- Pablo creó la app dev en el portal de X. Aprendizajes del alta: para guardar "User authentication settings" el **Callback URI es obligatorio** (puse `https://localhost/`, no se usa); type de app = Web App/Automated App (Confidential client); el OAuth 2.0 Client ID/Secret que ofrece NO se usa (usamos OAuth 1.0a). Si el permiso Read+Write se pone DESPUÉS de generar el Access Token, hay que **regenerar** el Access Token para que tome escritura.
- Verificado con `--verify`: conectada a @jpablo11g con escritura.

## ✅ BLOQUEO RESUELTO: saldo cargado + 1er post publicado (2026-08-17)
- **El 402 histórico quedó atrás.** Pablo cargó **$15 USD de créditos prepagados** (modo **personal**, NO business) en el developer portal → Billing/Credits. El balance en USD 0.00 era la causa exacta del 402.
- **Detalle de UI (para futuras cargas):** la tarjeta NO se registra en pantalla suelta; se captura dentro del flujo de **"Purchase credits"** (botón negro arriba-der en la pantalla Credits), o completando primero **"Billing information"**. El aviso "Auto Recharge unavailable — add at least 1 payment method" confirma que sin tarjeta no deja cargar.
- **Costo por acción (histórico feb-2026):** publicar **~$0.015 USD/tweet**, leer ~$0.005. Con $15 hay saldo para AÑOS a cadencia de 1/día. (Nota: no lo tenía de memoria en la conversación y fui cauta; el dato vive aquí.)
- **PRIMER TWEET REAL PUBLICADO (2026-08-17):** nota de McDonald's (expediente de 515 págs), tono ácido/sarcástico, con link de Morning Brew. Pablo eligió la versión "ALT". Tweet id **2089537157706739787** → https://x.com/jpablo11g/status/2089537157706739787
- El borrador viejo de Bank of America/Ozempic (opción 1, msg 1773) quedó SUPERADO por este primer post; ya no aplica.

## Cadencia acordada (2026-08-17 noche)
- Pablo confirmó **cadencia DIARIA** (1 post/día). Flujo: Leeloo propone borrador con tono ácido/sarcástico → Pablo da OK → se sube. Le confirmé que no hay riesgo de bloqueo: a $0.015/tweet, 1/día ≈ $0.45/mes → los $15 rinden AÑOS; los límites de la API sobran (30/mes es mínimo).
- **Cuidados que le señalé:** (1) no repetir texto idéntico muchas veces (X lo marca spam); (2) si pone Spend Cap, no dejarlo muy bajo para que no corte a media racha ($5-10/mes sobra a este ritmo).

## Pendientes
- **Confirmar/poner el Spend Cap mensual** en el portal (~$5-10 USD basta) para topar gasto (opcional, consumo mínimo).
- Más adelante: ¿Pablo otorga "libertades" para publicar sin confirmar cada vez? Por ahora, **borrador + OK siempre**.
- Definir de dónde saldrá el tema diario (¿del Morning/Evening Brew?, ¿temas que dé Pablo?) y a qué hora subir.
