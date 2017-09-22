# WIP: kafka-elasticsearch-docker
The objective is to have single docker image that run zookeeper, kafka, and elasticsearch. Or, minimaly have a single docker-compose.yml to up these services.

### For the time being, here are the docker command to run the service separately.

Up zookeeper and kafka:
```
docker run -p 2181:2181 -p 9092:9092 --env ADVERTISED_HOST=`docker-machine ip \`docker-machine active\`` --env ADVERTISED_PORT=9092 spotify/kafka
```

Up elasticsearch:
```
docker run -p 9200:9200 -p 9300:9300 docker.elastic.co/elasticsearch/elasticsearch:5.3.3
```

Reference:
* https://hub.docker.com/r/spotify/kafka/
* https://www.elastic.co/guide/en/elasticsearch/reference/5.3/docker.html
