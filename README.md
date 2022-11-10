# Projeto para estudos do Apache Kafka com Producer/Consumer em NodeJS e serialização com Avro.
## Prerequisites
- node
- docker
- docker-compose
---
## Running locally

**Subir os containers kafka e zookeeper**
`docker-compose up`

**Entrar em modo interativo no container kafka e criar um tópico com nome test**
`docker exec -it kafka /opt/bitnami/kafka/bin/kafka-topics.sh \`
`--bootstrap-server localhost:9092 \`
`--create \`
`--replication-factor 1 \`
`--partitions 1 \`
`--topic test`

**Instalar as dependências do projeto**
`npm install`

**Iniciar o producer**
`npm run start:producer`

**Iniciar o consumer**
`npm run start:consumer`
