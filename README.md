# Configure and Install ELK stack on CentOS using Ansible

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

Run installation of Elk Stack
> * cd ansible
> * ./elk-install.sh
