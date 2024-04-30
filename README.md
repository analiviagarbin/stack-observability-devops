# Stack de Observabilidade 🔍📊

Focada na parte de métricas, a stack executa um Prometheus, Node exporter, Grafana e uma aplicação que simula a quantidade de pessoas na fila de um petshop, e a avaliação delas. O node exporter e a aplicação do pet shop geram métricas que são recuperadas pelo Prometheus, com o Grafana foram criados 2 dashboards e um alerta.

### Tecnologias:
<div  style="display: inline-block" >

 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" width="40" />
 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="40">
 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/prometheus/prometheus-original.svg" width="40" />
 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/grafana/grafana-original.svg" width="40"  />
 <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ansible/ansible-original.svg" width="40" />
          
</div>


### Requisitos:
- Docker
- Docker Compose
- Ansible


<br />

### Executando Localmente

1. Clonar o repositório
```
git clone https://github.com/analiviagarbin/stack-observability-devops.git
```

2. Rodar os containers
```
sudo docker compose up -d
```

3. Verificar a execução:
```
sudo docker ps
```

<br />

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

<br />

### Visualizando Dashboards (Grafana)

- Acessar credenciais disponíveis na pasta ```./grafana/credenciais.md```

<br />

### Execução Remota

- Instruções para executar o programa em uma máquina remota utilizando o ansible-playbook.

1. Navegar até a pasta ```./ansible``` do repositório.

2. Executar o comando de export da variável (caminho para a chave ssh privada):

```
export PATH_SSH_PRIVATE_KEY=/caminho/do/arquivo/ssh/privado
```

3. Iniciar o Ansible Playbook:

```
ansible-playbook -i hosts ansible-playbook.yml
```

<br />

### Acessando remotamente o Grafana da Máquina

- Em um terminal, executar o comando:

```
ssh -i /caminho/do/arquivo/ssh/privado -L localhost:3001:localhost:3001 [USUARIO]@[IP_DA_MAQUINA]
```