#AMP server for local development for linux

A local web server using PHP, Apache, Mysql and PHPMyadmin using Docker Composer

##Step 1:

run
```
docker run -d -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer

```
or
```
/bin/bash portainer.sh

```
you'll be able to access localhost:9000 to acess [Portainer](https://www.portainer.io/) <<< nice tool >>>

###Step 2:

access php_7_2 folder and run (Atention: ports 80, 5080, 6080 will be used here):

```
docker-compose up -d
```

you can do the same in php_5_6 folder

###Step 3:

Result:

- http://localhost/ to use php_7_2
- http://localhost:5080/ to use php_5_6
- http://localhost:6080/ to use PHPMyadmin
- http://localhost:9000/ to acess Portainer tool and manage containers
- To acess mysql use MYSQL container ip, user: root and password: teste123

All in your local machine:

- your data will be saved in your local ./data folder
- your php.ini config can be add in ./php-ini folder
- your php files can be add in ./www folder