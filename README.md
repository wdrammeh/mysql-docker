# MySQL + PhpMyAdmin

Allows to install and run MySQL DB along side a PhpMyAdmin instance on a Docker container.

## Getting started

```
docker-compose up -d --build
```

## Grant non-root user full access to a db

`docker exec -it mysql mysql -uroot -p`

```
CREATE DATABASE IF NOT EXISTS digitalschool CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
GRANT ALL PRIVILEGES ON digitalschool.* TO 'appuser'@'%';
SHOW GRANTS FOR 'appuser'@'%';
```