# Docker-based Drupal stack

[![Build Status](https://travis-ci.org/wodby/docker4drupal.svg?branch=master)](https://travis-ci.org/wodby/docker4drupal)

## Introduction

Docker4Drupal is a set of docker images optimized for Drupal. Use `docker-compose.yml` file from the [latest stable release](https://github.com/wodby/docker4drupal/releases) to spin up local environment on Linux, Mac OS X and Windows. 

* Read the docs on [**how to use**](https://docs.wodby.com/stacks/drupal/local#usage)
* Follow [@wodbycloud](https://twitter.com/wodbycloud) for future announcements
* Join [community slack](https://slack.wodby.com) to ask questions

## Stack

The Drupal stack consist of the following containers:

| Container     | Versions                | Service name    | Image                              | Default |
| ------------- | ----------------------- | --------------- | ---------------------------------- | ------- |
| [Nginx]       | 1.15, 1.14, 1.13        | `nginx`         | [wodby/drupal-nginx]               | ✓       |
| [Apache]      | 2.4                     | `apache`        | [wodby/php-apache]                 |         |
| [Drupal]      | 8, 7, 6                 | `php`           | [wodby/drupal]                     | ✓       |
| [PHP]         | 7.x, 5.6, 5.3           | `php`           | [wodby/drupal-php]                 |         |
| [MariaDB]     | 10.3, 10.2, 10.1        | `mariadb`       | [wodby/mariadb]                    | ✓       |
| [PostgreSQL]  | 10, 9.x                 | `postgres`      | [wodby/postgres]                   |         |
| [Redis]       | 4.0, 3.2                | `redis`         | [wodby/redis]                      |         |
| [Varnish]     | 4.1                     | `varnish`       | [wodby/drupal-varnish]             |         |
| [Node.js]     | 9.11, 8.11, 6.14        | `node`          | [wodby/node]                       |         |
| [Drupal node] | 1.0                     | `drupal-node`   | [wodby/drupal-node]                |         |
| [Solr]        | 7.x, 6.6, 5.5, 5.4      | `solr`          | [wodby/drupal-solr]                |         |
| Elasticsearch | 6.x, 5.6, 5.5, 5.4      | `elasticsearch` | [wodby/elasticsearch]              |         |
| Kibana        | 6.x, 5.6, 5.5, 5.4      | `kibana`        | [wodby/kibana]                     |         |
| [Memcached]   | 1.5                     | `memcached`     | [wodby/memcached]                  |         |
| [Webgrind]    | 1.5                     | `webgrind`      | [wodby/webgrind]                   |         |
| [Blackfire]   | latest                  | `blackfire`     | [blackfire/blackfire]              |         |
| [Rsyslog]     | latest                  | `rsyslog`       | [wodby/rsyslog]                    |         |
| [AthenaPDF]   | 2.10.0                  | `athenapdf`     | [arachnysdocker/athenapdf-service] |         |
| [Mailhog]     | latest                  | `mailhog`       | [mailhog/mailhog]                  | ✓       |
| [OpenSMTPD]   | 6.0                     | `opensmtpd`     | [wodby/opensmtpd]                  |         |
| Adminer       | 4.6                     | `adminer`       | [wodby/adminer]                    |         |
| phpMyAdmin    | latest                  | `pma`           | [phpmyadmin/phpmyadmin]            |         |
| Portainer     | latest                  | `portainer`     | [portainer/portainer]              | ✓       |
| Traefik       | latest                  | `traefik`       | [_/traefik]                        | ✓       |

Supported Drupal versions: 8 / 7 / 6

## Documentation

Full documentation is available at https://docs.wodby.com/stacks/drupal/local.

## Beyond local environment

Docker4Drupal is a project designed to help you spin up local environment with docker-compose. If you want to deploy a consistent stack with orchestrations to your own server, check out [Drupal stack](https://wodby.com/stacks/drupal) on Wodby ![](https://www.google.com/s2/favicons?domain=wodby.com).

## Maintenance

We regularly update images used in this stack and release them together, see [releases page](https://github.com/wodby/docker4drupal/releases) for full changelog and update instructions.  

## License

This project is licensed under the MIT open source license.

[Nginx]: https://wodby.com/stacks/drupal/docs/containers/nginx
[Apache]: https://wodby.com/stacks/drupal/docs/containers/apache
[Drupal]: https://wodby.com/stacks/drupal/docs/containers/php/
[PHP]: https://wodby.com/stacks/drupal/docs/containers/php/
[MariaDB]: https://wodby.com/stacks/drupal/docs/containers/mariadb
[PostgreSQL]: https://wodby.com/stacks/drupal/docs/containers/postgres
[Redis]: https://wodby.com/stacks/drupal/docs/containers/redis
[Varnish]: https://wodby.com/stacks/drupal/docs/containers/varnish
[Node.js]: https://wodby.com/stacks/drupal/docs/containers/node
[Drupal node]: https://wodby.com/stacks/drupal/docs/containers/drupal-node
[Solr]: https://wodby.com/stacks/drupal/docs/containers/solr/
[Memcached]: https://wodby.com/stacks/drupal/docs/containers/memcached/
[Webgrind]: https://wodby.com/stacks/drupal/docs/containers/webgrind/
[Blackfire]: https://wodby.com/stacks/drupal/docs/containers/blackfire/
[Rsyslog]: https://wodby.com/stacks/drupal/docs/containers/rsyslog/
[AthenaPDF]: https://wodby.com/stacks/drupal/docs/containers/athenapdf/
[Mailhog]: https://wodby.com/stacks/drupal/docs/containers/mailhog/
[OpenSMTPD]: https://wodby.com/stacks/drupal/docs/containers/opensmtpd/

[wodby/drupal-nginx]: https://github.com/wodby/drupal-nginx
[wodby/php-apache]: https://github.com/wodby/php-apache
[wodby/drupal]: https://github.com/wodby/drupal
[wodby/drupal-php]: https://github.com/wodby/drupal-php
[wodby/mariadb]: https://github.com/wodby/mariadb
[wodby/postgres]: https://github.com/wodby/postgres
[wodby/redis]: https://github.com/wodby/redis
[wodby/drupal-varnish]: https://github.com/wodby/drupal-varnish
[wodby/drupal-solr]: https://github.com/wodby/drupal-solr
[wodby/elasticsearch]: https://github.com/wodby/elasticsearch
[wodby/kibana]: https://github.com/wodby/kibana
[wodby/node]: https://github.com/wodby/node
[wodby/drupal-node]: https://github.com/wodby/drupal-node
[wodby/memcached]: https://github.com/wodby/memcached
[wodby/opensmtpd]: https://github.com/wodby/opensmtpd
[wodby/webgrind]: https://hub.docker.com/r/wodby/webgrind
[blackfire/blackfire]: https://hub.docker.com/r/blackfire/blackfire
[wodby/rsyslog]: https://hub.docker.com/r/wodby/rsyslog
[arachnysdocker/athenapdf-service]: https://hub.docker.com/r/arachnysdocker/athenapdf-service
[mailhog/mailhog]: https://hub.docker.com/r/mailhog/mailhog
[wodby/adminer]: https://hub.docker.com/r/wodby/adminer
[phpmyadmin/phpmyadmin]: https://hub.docker.com/r/phpmyadmin/phpmyadmin
[portainer/portainer]: https://hub.docker.com/r/portainer/portainer
[_/traefik]: https://hub.docker.com/_/traefik
