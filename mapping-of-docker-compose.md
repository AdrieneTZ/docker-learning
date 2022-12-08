### Destructure the `docker-compose.yaml`

#### Example docker command:
```
docker run -d --name mongodb -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password --name mongodb --net mongo-network mongo

```
#### Example docker-compose in yaml file:
``` yaml
version: '3'
services:
  mongodb:
    image: mongo
    ports:
      - 27017:27017
    environment:
      - MONGO_INITDB_ROOT_USERNAME=admin
      - MONGO_INITDB_ROOT_PASSWORD=password
```

#### Docker-compose <--mapping--> Docker command

``` yaml
version: '3'
```
- version of the docker-compose

``` yaml
services:
```
- above services are the container lists, ie. `mongodb`, `mongo-express`

``` yaml
services:
  mongodb:
```
- the container name
- mapping to command  `--name mongodb`

``` yaml
services:
  mongodb:
    image:mongo:version
```
- mapping to command  `mongo` (the last part of dokcer cli on the top)


``` yaml
services:
  mongodb:
    image:...
    ports:
      -27017:27017
```
- HOST:CONTAINER
- mapping to command  `-p 27017:27017`


``` yaml
services:
  mongodb:
    image:...
    ports:...
    environment:
      - MONGO_INITDB_ROOT_USERNAME=admin
      - MONGO_INITDB_ROOT_PASSWORD=password
```
- mapping to command `-e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password`
