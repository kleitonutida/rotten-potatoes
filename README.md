# Criação do cluster no K3D

Para criar o cluster no K3D é necessário executar o comando:

```bash
k3d cluster create kubedev --servers 1 --agents 3 --port 8080:30000@loadbalancer --port 9090:31000@loadbalancer --port 3000:31001@loadbalancer
```

Onde:

| Parâmetro | Descrição |
|---|---|
|--server 1| Quantidade de `masters` criadas |
|--agents 3| Quantidade de `nodes` criados |
|--port 8080:30000@loadbalancer| Porta mapeada para a Aplicação no LoadBalancer da Master |
|--port 9090:31000@loadbalancer| Porta mapeada para o Prometheus no LoadBalancer da Master|
|--port 3000:31001@loadbalancer| Porta mapeada para o Grafana no LoadBalancer da Master |

## Grafana

Usuário: admin
Senha: rp9ESweqS8kbOXOHb8omk904fQIBDjUMRsO80RyQ
