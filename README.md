# docker-database

## Postgresql
mkdir ${HOME}/postgres-data/

docker run -d \
    --name dev-postgres \
    -e POSTGRES_PASSWORD=secret \    
    -v ${HOME}/postgres-data/:/var/lib/postgresql/data \
    -p 5432:5432 \
    postgres

## MySQL
mkdir ${HOME}/mysql-data/

docker run -d \
    --name dev-mysql \
    -p 3306:3306 \
    -e MYSQL_ROOT_PASSWORD=secret \
    -v ${HOME}/mysql-data/:/var/lib/mysql \
    mysql
