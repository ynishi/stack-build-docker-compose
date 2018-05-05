# stack-build-docker-compose
docker-compose for stack-build image

## Usage
* short cut is made with make
```
make usage
```
### ghci
```
docker-compose run stack stack ghci
# or
# make ghci
# in project
# make do COMM=ghci PRJ=${PROJECT_NAME}
```
### create new project
```sh
$ docker-compose run stack stack new ${PROJECT_NAME}
# or 
# make new PRJ=${PROJECT_NAME}
```
### build
```sh
$ docker-compose run --workdir=/stack/${PROJECT_NAME} stack stack build
# or
# make build PRJ=${PROJECT_NAME}
```
### exec
```sh
$docker-comse run --workdir=/stack/${PROJECT_NAME} stack stack exec ${PROJECT_NAME}-exe
# or
# make exec PRJ=${PROJECT_NAME}
```
### do stack command
```sh
$docker-comse run --workdir=/stack/${PROJECT_NAME} stack stack ${COMMAND} ${ARGS}
# or
make do PRJ=${PROJECT_NAME} COMM=${COMMAND} ARGS=${ARGS}
```
