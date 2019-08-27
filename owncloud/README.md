# Owncloud

default port: 8080

## requirement
- docker-compose: 17.09.0+

## How to run with docker-compose

- start owncloud & mysql

```
    git clone https://github.com/haxqer/docker.git \
        && cd docker/owncloud \
        && docker-compose up
```

- default db(mysql5.7) configure:

```bash
    driver=mysql5.7+
    host=mysql-owncloud
    port=3306
    db=owncloud
    user=owncloud
    passwd=123123
```

