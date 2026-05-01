# Taller de Pruebas de Rendimiento

## Objetivo
Evaluar rendimiento del endpoint /register usando k6.

## SLA / SLO

| Métrica | Objetivo |
|---|---|
| p95 | <= 300ms |
| p99 | <= 800ms |
| Error Rate | < 1% |

## Escenarios

- baseline
- load
- stress

## Ejecución

```bash
set BASE_URL=http://localhost:8080
set SCENARIO=baseline
k6 run perf/scripts/register_voter_k6.js -o json=perf/results/baseline.json
```
