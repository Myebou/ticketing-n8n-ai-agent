# Módulo 4 — Arquitectura de Integraciones Externas

Gmail Trigger → IF anti auto-reply → Set payload limpio → Airtable Memory → AI Manager → Set mínimo integraciones → HubSpot Look up → IF contacto existe → Update/Create → Set Slack → Slack → Gmail Create Draft → Auditoría.

## Mínimo privilegio

- Gmail: lectura de entrada y creación de borradores.
- HubSpot: búsqueda por email y create/update mínimo.
- Slack: escritura acotada en canal operativo.
- Airtable: lectura de memoria por Session_ID.

## Human-in-the-loop

La respuesta final queda como borrador Gmail. No se envía automáticamente.
