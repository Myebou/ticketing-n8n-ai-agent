# Módulo 4 — Integraciones Avanzadas

Archivo principal: `checkpoint4_alexis_paredes.json`

## Objetivo

Extender el workflow del Módulo 3 con integraciones externas reales de negocio: Gmail, HubSpot y Slack.

## Controles obligatorios

1. IF anti auto-reply/no-reply inmediatamente después del trigger de Gmail.
2. Look up en HubSpot antes de Create Contact para evitar duplicados.
3. Gmail Create Draft como barrera Human-in-the-loop.
4. Set de limpieza antes de Slack/Gmail/CRM.

## Datos

Caso académico ficticio de ticketing cultural. No contiene datos reales de clientes ni proyectos productivos.


# Checkpoint 4 — Integraciones Avanzadas v2

Workflow principal: `checkpoint4_alexis_paredes_v2_guardrails.json`

## Propósito

Evoluciona el Módulo 3: conserva memoria persistente por `Session_ID` y suma integraciones externas con Gmail, HubSpot y Slack, incorporando controles preventivos no-code antes de que el agente actúe sobre sistemas externos.

## Nodos clave

1. Gmail Trigger — Email entrante soporte
2. IF — Anti auto-reply y no-reply
3. Guardrails — Datos sensibles
4. Guardrails — Jailbreak y tópico
5. HubSpot — Look up contacto por email
6. IF — ¿Existe contacto CRM?
7. HubSpot — Update contacto existente
8. HubSpot — Create contacto nuevo
9. Gmail — Create Draft respuesta HITL
10. Slack — Notificar operaciones
11. Airtable — Update memoria existente
12. Airtable — Create memoria inicial

## Configuración post-importación

Reasignar credenciales en n8n: Gmail OAuth2, HubSpot, Slack OAuth2, Airtable OAuth2 y OpenAI.

Reemplazar placeholders:

- REEMPLAZAR_BASE_AIRTABLE
- REEMPLAZAR_TABLA_MEMORIA
- REEMPLAZAR_CANAL_SLACK

## Seguridad

El JSON está preparado para repositorio público. No incluye API keys ni credenciales reales.

