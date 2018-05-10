# Configure and Install ELK stack on eEntOS using Ansible

## ELK Components

> 1. Logstash: : The server component of Logstash that processes incoming logs
> 2. Elasticsearch : Stores all of the logs
> 3. Kibana : Web interface for searching and visualizing logs, which will be proxied through Nginx



*Install the first three components on a single server. The current setup pulls
all the syslog files and visualizes them via Kibana*

## Usage

This is the URL to access the environment:

http://local-ip-address/

> * Username - kibanaadmin
> * Password - password


*NOTE: You will need to update the kibana.conf file with the correct
server IP Address and restart Nginx to get the reverse proxy working correctly.*

*You will also need to:*

> *  sudo vi(or vim) /etc/init.d/logstash
> *  Update LS_GROUP=logstash to LS_GROUP=adm

*This will allow logstash the permission to access syslogs. You should then
reboot the server for the updates to process*


Run installation of Elk Stack
> * cd ansible
> * ./elk-install.sh
