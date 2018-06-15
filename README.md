# Druid Docker Image

This repository contains a single Docker image which spins up a Druid cluster.

## Run a simple Druid cluster

Download and launch the docker image:

```sh
docker pull thuylevn/druid-docker
docker run --rm -i -p 8082:8082 -p 8081:8081 thuylevn/druid-docker
```

```
- List datasources

curl http://localhost:8082/druid/v2/datasources
```

```
- Access the coordinator console at http://localhost:8081/ 
- Access the overlord indexing console at http://localhost:8081/console.html
```

 
## Build Druid Docker Image

To build the docker image yourself

```sh
git clone https://github.com/thuylevn/druid-docker.git
docker build -t thuylevn druid-docker
docker run --rm -i -p 8082:8082 -p 8081:8081 druid-docker
```

 
