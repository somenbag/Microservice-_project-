©️Somen

🔖 Microservice project
---------------------------

🐋Docker Commands used in the project
------------------------------------

Run RabbitMQ Docker Container : docker run -d --name rabbitmq-management -p 15672:15672 -p 5672:5672 -p 5671:5671 rabbitmq:3-management

RabbitMQ and change Default user name and password : docker run -d --name rabbitmq-management -p 15672:15672 -p 5672:5672 -p 5671:5671 -e RABBITMQ_DEFAULT_USER=user –e RABBITMQ_DEFAULT_PASS=password rabbitmq:3-management

Run Zipkin Docker Container : docker run -d --name zipkin-container -p 9411:9411 openzipkin/zipkin

steps to use ELK
----------------

>Elasticsearch download- https://www.elastic.co/downloads/elasticsearch

bin/elasticsearch.bat

***Reset Passwoed for elastic user :***

bin/elasticsearch-reset-password.bat -u elastic

***Generate enrollment token for kibana:***

bin/elasticsearch-create-enrollment-token.bat --scope kibana

>logstash download - https://www.elastic.co/downloads/logstash

bin/logstash -f logstash.conf

>kibana download - https://www.elastic.co/downloads/kibana

bin/kibana.bat

*** some endpoints to search ***

https://localhost:9200/_cat

https://localhost:9200/_cat/indices

https://localhost:9200/users-ms-2024.10.301/_search?q=*
