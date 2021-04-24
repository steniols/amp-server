# AMP server for local development in linux

A local web server with PHP, Apache, Mysql and PHPMyadmin using Docker Compose

## Step 1:

run
```
docker run -d -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer
```
or
```
/bin/bash portainer.sh
```
you'll be able to access `localhost:9000` to acess [Portainer](https://www.portainer.io/).

### Step 2:

access `./php_7_2` folder and run (ports 80, 5080, 6080 will be used here):

```
docker-compose up -d
```

you can do the same in `./php_5_6` folder

### Step 3:

Result:

- http://localhost/ to use php 7.2
- http://localhost:5080/ to use php 5.6
- http://localhost:6080/ to use PHPMyadmin
- http://localhost:9000/ to access Portainer tool and manage containers
- Login in MYSQL with ` user: root` and `password: teste123`

All in your local machine:

- your databases will be saved in your local `./db` folder
- your php.ini config can be added in `./php-ini` folder
- your php files can be added in `./www` folder
