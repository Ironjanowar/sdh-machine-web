# SDH-Machine-Web

Docker deployment of Framework and SDH-API.

This repository deploys these containers:
* Lightweight Directory Access Protocol
* SDH Open API Initiative
* MySQL Database for Laravel
* phpMyAdmin Container
* Laravel Framework

### Ports (container - host):
* Laravel: 80 - 9000
* API: 8080 - 9002
* LDAP: 80 - 9005
* LDAP: 389 - 9010
* LDAP: 636 - 9011

### Docker - Requirements:

* docker > 1.7.0
* docker-compose > 1.3.1

### Docker - Usage:

|Alias|Command|
|:---------|:----------|
|Start|```docker-compose up -d```|
|Stop|```docker-compose stop```|
|Delete|```docker-compose rm -f```|
|Rebuild|```docker-compose build```|

### Docker - Tips:

If you want to change port redirection or configuration, we suggest you:

1. Stop
2. Delete
3. Build (if you have changed any file or physical configuration)
4. Start

### Web - Usage:

To Do.
