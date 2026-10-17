The following is a guide on how the docker-compose.yaml guide is structured. This will go into the concepts of the file and provide information on what things do.

# `services:` block
The services block is where you define your services, containers, and more. This also allows for ways to provide rules and configurations for the services you wish to add.

> The services block is a top level key for every container, you'd most likely see this *after* the version number!

# How Nextcloud finds the database container
Within the configuration of Nextcloud for our setup, we have made it so our database is simply called database!

```version: '3'
services:
 database:
 image: mariadb:10.6
 environment:
 - MYSQL_ROOT_PASSWORD=cloudnova_root
 - MYSQL_PASSWORD=cloudnova_pass
 - MYSQL_DATABASE=nextcloud_db
 - MYSQL_USER=nextcloud_user
 app:
 image: nextcloud
 ports:
 - 8080:80
 environment:
 - MYSQL_PASSWORD=cloudnova_pass
 - MYSQL_DATABASE=nextcloud_db
 - MYSQL_USER=nextcloud_user
 - MYSQL_HOST=database 
```

Now, with that in mind, take a look at Nextcloud's configuration. The `MYSQL_HOST` is the same as where the database resides. Not only that, the `MYSQL_DATABASE` has the exact name of the database's name.

# `docker run` / `docker-compose up -d` comparison

- `docker run` starts up singular containers . You would use this if ever you want to run or install one container with just the default configuration.

- `docker-compose up -d` on the other hand starts up multiple containers within the docker-compose.yaml file.