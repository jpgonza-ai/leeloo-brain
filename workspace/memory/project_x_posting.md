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

## ⚠️ BLOQUEO ACTUAL: X quiere saldo (modelo de créditos, feb-2026)
- **El primer POST /2/tweets devolvió HTTP 402 "credits depleted / Payment Required"** (2026-08-07). La LECTURA (--verify) sí funciona; la ESCRITURA está topada por saldo $0.
- **Causa:** en **febrero 2026 X eliminó el tier gratis** y pasó a **pago por uso con créditos**. Ya NO es la suscripción cara (Basic ~$100-200/mes); ahora se carga saldo y descuentan por acción: **publicar ~$0.015 USD/tweet**, leer ~$0.005. Postear 1/día ≈ **~$0.45/mes (~$5-6/año)**, baratísimo.
- **Remedio:** Pablo debe **cargar saldo (con tarjeta) en el developer portal → billing/credits**. Con $5-10 alcanza para mucho tiempo. Cuando cargue, reintentar el tweet.
- Tono/estilo de X = definido: español, ácido/sarcástico (ver `feedback_x_tone.md`). Cadencia ~1/día o cada 2 días.
- Primer borrador acordado (Pablo eligió opción 1, msg 1773): "Bank of America gasta 250 millones de dólares al año en Ozempic para sus empleados. Hace 5 años: cero. Nada dice 'te valoramos' como pagarte la dieta mientras te niegan el aumento. 💉📉" — **pendiente de publicar en cuanto haya saldo.**

## Pendientes
- **Que Pablo cargue saldo de créditos en el portal** (o decidir seguir con "yo redacto, tú pegas" para X sin tarjeta).
- Publicar el primer tweet (opción 1, ya aprobada) al haber saldo.
- Más adelante: ¿Pablo otorga "libertades" para publicar sin confirmar cada vez? Por ahora, borrador + OK siempre.
