# A minimal configuration to set up a docker with Ubuntu 16.04 + SSH access + LAMP
### How to Use:
1. Modify `Dockerfile` to set up password for SSH
1. Execute: `docker-compose up -d` (remove `-d` for foreground mode)
2. Log into server: `ssh root@localhost -p 2022`
2. Set up root password for mysql: `mysqladmin -u root password '<NEW_PASSWORD>'`

# Before starting container, please create network bridge_eth1,
# if not, docker-compose will use default profile network as host-ip 0.0.0.0
docker network create -o "com.docker.network.bridge.host_binding_ipv4"="171.244.27.177" bridge_eth1

Ref to: https://github.com/docker/compose/issues/2999


Download https://www.phpmyadmin.net/downloads/ into /www/html/phpadmin 

Login with 
User: root
Pass: at step (2)
