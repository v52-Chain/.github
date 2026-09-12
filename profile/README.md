# Vector52 — carpeta oficial de ejecución

Esta carpeta es la fuente de verdad del equipo para la **Ethereum Bolivia Buildathon 2026**. Consolida el proyecto, la arquitectura de repositorios, los contratos de integración y las responsabilidades individuales.

## Orden de lectura

1. [PROYECTO-FINAL.md](PROYECTO-FINAL.md)
2. [ARQUITECTURA-REPOSITORIOS.md](ARQUITECTURA-REPOSITORIOS.md)
3. [CONTRATO-INTEGRACION.md](CONTRATO-INTEGRACION.md)
4. [CHECKLIST-DEMO-SUBMISSION.md](CHECKLIST-DEMO-SUBMISSION.md)
5. Guías personales:
   - [SAUL.md](SAUL.md)
   - [FRANCO.md](FRANCO.md)
   - [JHAMIL.md](JHAMIL.md)
   - [OMAR.md](OMAR.md)
6. [REPOS/README.md](REPOS/README.md) — copias locales listas para los repositorios creados

## Regla de estado

No marcar una tarea como terminada por conversación o captura aislada.

| Estado | Significado |
|---|---|
| `REPORTED_WORKING` | Un integrante informa que funciona, pero falta evidencia reproducible compartida |
| `PASS_BOOT` | Existe evidencia de que el proceso inicia/carga; todavía no prueba el flujo end-to-end |
| `CONFIGURED` | La configuración existe, pero falta demostrar ejecución real |
| `COPIED/TO_ADAPT` | Código reutilizado y separado; aún conserva supuestos del proyecto origen |
| `PASS` | Otro integrante puede reproducirlo con README, comando y fixture |
| `IN_PROGRESS` | Existe trabajo ejecutable incompleto |
| `BLOCKED` | Hay un bloqueo identificado con owner y siguiente acción |
| `PENDING` | Aún no se inició o no existe evidencia |

## Baseline declarado por el equipo

| Componente | Estado inicial | Owner |
|---|---|---|
| Peticiones backend a The Graph | `REPORTED_WORKING` | Saúl |
| OpenZeppelin Relayer escuchando en `0.0.0.0:8080` | `PASS_BOOT` por captura; falta health reproducible | Saúl |
| Plugin x402 compilado/cargado | `PASS_BOOT` por captura; falta flujo E2E | Saúl |
| HSK Mainnet/Testnet en configuración del Relayer | `CONFIGURED/TO_VERIFY` | Saúl |
| Settlement x402 específicamente en Avalanche | `TO_VERIFY` | Saúl |
| RPC autenticado Alchemy | `PENDING` | Franco |
| Adapter RPC HSK | `PENDING/TO_CONFIRM` | Franco + Saúl |
| Baseline PWA reutilizado de ETHOnline | `COPIED/TO_ADAPT` | Omar + Jhamil |
| Interfaz Agent Access lista para MCP | `IN_PROGRESS` | Omar + Jhamil |
| Servidor MCP | `PENDING`; posterior a congelar contrato UI/API | Omar + Jhamil |
| Claim Auditor reproducible | `TO_CONFIRM` | Franco; revisión Omar/Jhamil |
| Contribution Analysis reproducible | `TO_CONFIRM` | Franco |
| `.v52` con evidencia real + tamper test | `TO_CONFIRM` | Franco; UI Omar/Jhamil |
| Contratos HSK/Avalanche desplegados y verificados | `PENDING/TO_CONFIRM` | Saúl |

## Organización creada

Organización GitHub: `v52-Chain`. Repositorios observados en la captura del equipo:

- `v52`;
- `v52-backend`;
- `v52-onchain`;
- `v52-subgraph-hsk`;
- `v52-mcp`.

Actualmente aparecen privados. Revisar los requisitos de publicación antes del submission.

## Objetivo de la entrega

```text
TX + CLAIM
   ↓
THE GRAPH + RPC ALCHEMY
   ↓
EVIDENCIA PRESERVADA
   ↓
CONTRIBUTION + CLAIM AUDIT
   ↓
.V52 + VERIFY
   ↓
HSK ANCHOR + SUBGRAPH

AGENTE MCP
   ↓
X402 EN AVALANCHE
   ↓
MISMO CORE FORENSE
```

La integración vale únicamente si aparece en el camino real de la demo.
