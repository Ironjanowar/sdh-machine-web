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

### Docker - Environment:

* API Configuration

|Variable|Description|Example|
|:---------|:----------|:----------|
|SDH_API_HOST|URL or IP address|127.0.0.1 or other|
|SDH_API_PROTOCOL|Protocol|http or https|
|SDH_API_PORT|Container Port|9002 or other|
|SDH_LDAP_HOST|LDAP URL or IP addresss|ldap://...|
|SDH_LDAP_PASSWORD|Password|user_password_test|
|SDH_RABBIT_HOST|Rabbit URL or IP address|amqp://...|
|SDH_RABBIT_PORT|Rabbit MQ Port|5672 or other|

Note: if you change redirection container port (ports section) you need to change SDH_API_PORT.

* Laravel Configuration

|Variable|Description|Example|
|:---------|:----------|:----------|
|SDH_API_HOST|API URL or IP address|http://...:9002 or https://...:9002|

Note: if you change SDH_API_PORT at API container, use the same port at laravel configuration.
