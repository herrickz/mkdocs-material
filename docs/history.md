# History

## 4/24/2018 (Tue)
### MySQL Docker [MySQL-Docker](https://hub.docker.com/_/mysql/)
- Create and run the docker container
```sh
docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql:tag
```
- Connect to container from terminal
```sh
docker run -it --link some-mysql:mysql --rm mysql sh -c 'exec mysql -h"$MYSQL_PORT_3306_TCP_ADDR" -P"$MYSQL_PORT_3306_TCP_PORT" -uroot -p"$MYSQL_ENV_MYSQL_ROOT_PASSWORD"'
```

### Create Django App from docker-compose [Django-Docker](https://stackoverflow.com/questions/31035887/linking-django-and-mysql-containers-using-docker-compose)