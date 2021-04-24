# AMP server for local development in linux

A local web server with PHP, Apache, Mysql and PHPMyadmin using Docker Compose

## Install Portainer:

Install Portainer for better container management:

```bash
git git@github.com:steniols/amp-server.git
cd amp-server
```
```bash
docker run -d -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer
```
or
```bash
/bin/bash portainer.sh
```
After this go to `http://localhost:9000`.
<br/>
<br/>

## Install Apache, PHP, MySQL and PHPMyAdmin:

```bash
cd php_7.2
docker-compose up -d
```
After this go to `http://localhost/` for PHP 7.2 access and `http://localhost:6080/` for PHPMyAdmin access. 
The MySQL user and password are: `user: root` and `password: teste123`.
<br/>
<br/>

## Install other PHP versions

In project's root folder you must have seen the `php_5.6` folder, this means that you can install this version by doing this:

```
cd php_5.6
docker-compose up -d
```

You can optionally install other versions of PHP by creating new folders for the new versions by copying the contents of `php_5.6` to this new folder, in addition to editing the first line of` Dockerfile` inside it with the desired version.

```
cd php_x.x
docker-compose up -d
```

## All in your local machine:

- your databases will be saved in project`./db` folder
- your `php.ini` config can be added in `./php-ini` folder
- your php files can be added in `./www` folder
