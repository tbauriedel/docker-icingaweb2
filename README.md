# docker-icingaweb2
docker-compose file for Icinga Web 2. Based on the Icinga/Icingaweb2 Image

It will start a container with apache2 and icingaweb2 (IP: 15.0.1.2) and a mariadb container for icingaweb2 (15.0.1.3)

After starting with docker-compose you have a completely configured Icinga Web 2 standalone environment.

Login data:
* Icinga Web 2: admin - admin
* Mysql root: onlyforadmin
* Mysql icingaweb2: rosebud

You can change them by editing docker-compose.yml

# Usage

docker-compose.yml requires a Docker volume that contains the current setup token.
To generate this:  
`docker run --rm -v icingaweb:/data icinga/icingaweb2 icingacli setup token create`

Start Docker Container in background:  
`docker compose up -d`
