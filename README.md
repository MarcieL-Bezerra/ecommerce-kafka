# ecommerce-kafka
Curso de Kafka: Produtores, Consumidores e streams - Alura

# Faça esse curso de Mensageria/Streams e:
- Utilize Kafka para comunicação assíncrona
- Aprenda a criar microsserviços com Kafka
- Entenda as vantagens de Kafka para paralelismo e execução serializada
- Entenda como funciona a serialização e deserialização no Kafka
- Extraia uma camada de abstração própria com boas práticas

# **Iniciando estudos de Kafka (Windows):**

- 1 - Faça o download do Kafka: 
---- https://kafka.apache.org/downloads
- 2 - Abra 4 terminais na pasta extraída;
- 3 - Em um dos terminais execute o Zookeeper: 
---- .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
- 4 - Em outro terminal execute o Kafka: 
---- .\bin\windows\kafka-server-start.bat .\config\server.properties
- 5 - Em outro terminal crie um tópico:
---- .\bin\windows\kafka-topics.bat --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic ECOMMERCE_NEW_ORDER
- 6 - Criando um Producer e enviando msg: 
---- .\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic ECOMMERCE_NEW_ORDER
  - Exemplo:
    - >pedido0,650
    - >pedido1,550
- 7 - Criando consumer: 
---- .\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic ECOMMERCE_NEW_ORDER --from-beginning
