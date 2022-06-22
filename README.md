### FULL CYCLE

# Sistemas de entregas que permite visualizar em tempo real o veículo do entregador.
# Há a possibilidade de múltiplos entregadores simultâneos.
# Serviço simulador que enviará a posição em tempo real de cada entregador.
# Os dados de cada entrega, bem como as posições, serão armazenados no Elasticsearch para futuras análises.

### Desafios

# Para evitar perda de informação caso o serviço backend fique indisponível por alguns momentos, não trabalharemos com REST.
# Solução: Trabalharemos com o Apache Kafka para o envio e recebimento de dados entre os sistemas.

# Não é responsabilidade do serviço de banckend persistir os dados no Elasticsearch. Logo, como armazenar as informações no Elasticsearch?
# Solução: Utilizaremos o Kafka Connect que também consumirá os dados do simulador e fará a inserção no Elasticsearch.

# Precisaramos exibir em tempo real a localização de cada entregador.
# Trabalharemos com websockets. O backend receberá os dados do simulador, e enviará as posições para o frontend via websocket.

### Dinâmica do sistema


### Tecnologias utilizadas

# Simulador: Golang
# Backend: Nest.js & Mongo
# Frontend: React
# Kafka & Kafka Connect
# Elasticsearch & Kibana
# Docker & Kubernetes
# Istio, Kiali, Prometheus & Grafana
