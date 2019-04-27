# Limani

[Orignal Repo](https://git.daedalus-project.io/docker/Limani)

Docker manifests of images used by one or more Daedalus Project Sub-projects.

## Images available

### Base images

* [base](/base): base image containing Daedalus Project and Windmaker repos only.

### Utilities

* [base_curl](/base_curl): base image with curl.
* [base_node8](/base_node8): base image with nodejs 8 LTS.
* [base_hugo](/base_hugo): base image with [Hugo](https://gohugo.io/).
* [base_xml_utils](/base_xml_utils): base image containing XML utils.
* [base_bash_utils](/base_bash_utils): base image containing bash development utils.
* [base_percona_client](/base_percona_client): base image with Percona server client.
* [base_docker](/base_docker): base image with Docker and Docker utils installed.

### Services

* [base_nginx_light](/base_nginx_light): base image with Nginx (light flavour).
* [base_redis_server](/base_redis_server): base image containing Redis server.
* [base_rabbitmq_server](/base_rabbitmq_server): base image containing Rabbitmq server.
* [base_percona_server](/base_percona_server): base image with Percona server.

### Packaging

* [base_deb_builder](/base_deb_builder): base image containing Debian packaging utilities.
* [base_deb_perl_builder](/base_deb_perl_builder): base image containing Debian packaging utilities (perl flavour).
* [base_deb_golang_builder](/base_deb_golang_builder): base image containing Debian packaging utilities (golang flavour).

### Misc

* [base_daedaluscore](/base_daedaluscore): base image with [Daedalus Core](https://git.daedalus-project.io/daedalusproject/Daedalus-Core) dependences.

## Develop images

* [base](/base_develop): base image containing Daedalus Project testing and Windmaker repos only.
* [base_develop_hugo](/base_develop_hugo): base develop image with [Hugo](https://gohugo.io/).
