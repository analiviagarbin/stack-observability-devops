# Stack de Observabilidade

- Focada na parte de métricas, a stack executa um Prometheus, Node exporter, Grafana e uma aplicação que simula a quantidade de pessoas na fila de um petshop, e a avaliação delas. O node exporter e a aplicação do pet shop geram métricas que são recuperadas pelo Prometheus, com o Grafana foram criados 2 dashboards e um alerta.

## Ferramentas:
- Docker
- Prometheus
- Node-exporter
- Grafana

1. Requisitos:
- Docker
- Docker compose