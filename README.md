# Stack de Observabilidade

Focada na parte de métricas, a stack executa um Prometheus, Node exporter, Grafana e uma aplicação que simula a quantidade de pessoas na fila de um petshop, e a avaliação delas. O node exporter e a aplicação do pet shop geram métricas que são recuperadas pelo Prometheus, com o Grafana foram criados 2 dashboards e um alerta.

1. Ferramentas:
- Docker
- Prometheus
- Node-exporter
- Grafana


2. Requisitos:
- Docker
- Docker Compose


### Executando

1. Clonar o repositório
```
git clone https://github.com/analiviagarbin/devops-ps.git
```

2. Rodar os containers
```
sudo docker compose up -d
```

3. Verificar a execução:
```
sudo docker ps
```


### Aplicações

Disponibilidade de métricas e funcionalidades para cada ferramenta:

- Prometheus:
```
https://localhost:9090/
```

- Node Exporter:
```
https://localhost:9100/
```

- Pet Shop:
```
https://localhost:3000/
```

- Grafana:
```
https://localhost:3001/
```


### Visualizando Dashboards (Grafana)

- Acessar credenciais disponíveis na pasta ```./grafana/credenciais.md```
