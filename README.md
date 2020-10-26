# ansible-zabbix-server-mysql
Deploy docker container with zabbix server (MySQL DB)  based on official zabbix-server-mysql container (https://hub.docker.com/r/zabbix/zabbix-server-mysql).

## Role variables
| Variable | Default value | Description |
| :---:        |     :---:      |         :---: |  
service_name                    |       zabbix-srv-docker           |   Service name in OS
uninstall_service               |       false                       |
DB_SERVER_HOST                  |       mysql-docker                |   MySQL-server host hostname
ZBX_JAVAGATEWAY                 |       zabbix-jgw-docker           |   Zabbix java gateway host hostname
DB_CONTAINER                    |       mysql                       |   MySQL-server docker container name 
ZBX_JAVAGATEWAY_CONTAINER       |       zabbix-java-gateway         |   Zabbix java gateway docker container name
ZBX_CACHESIZE                   |       32M                         |   Zabbix server cashe size
zabbix_host_port                |       10051                       |   Host network port
zabbix_container_port           |       10051                       |   Container network port
port_type                       |       tcp                         |   Port type
docker_image                    |       zabbix/zabbix-server-mysql  |   Docker image (https://hub.docker.com/)

### How to use
    - installation: just start the role
    - uninstallation: add --extra-vars "uninstall_service=true"