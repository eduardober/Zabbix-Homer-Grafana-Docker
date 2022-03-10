# Zabbix-Homer-Grafana-Docker
## Instalação

Para começarmos a instalação vamos precisar instalar alguns pacotes para monitorar tanto os dockers quanto a própria máquina
```
wget https://repo.zabbix.com/zabbix/6.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_6.0-1+ubuntu20.04_all.deb
dpkg -i zabbix-release_6.0-1+ubuntu20.04_all.deb
apt update
apt install zabbix-agent2 docker docker-compose
usermod -aG docker zabbix
service zabbix-agent2 restart
vim /lib/systemd/system/docker.service
```
Após estas instalações vamos precisar a linha que começa com ExecStart do deamon do docker
```
ExecStart=/usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock -H tcp://0.0.0.0:4243 -H unix:///var/run/docker.sock
```
```
git clone https://github.com/eduardober/Zabbix-Homer-Grafana-Docker.git
cd Zabbix-Homer-Grafana-Docker
vim docker-compose.yml
```
após estas configurações temos ainda que alterar o link do banco do zabbix colocando o ip da máquina. Após essa alteração poderemos subir todos os sistemas
```
docker-compose up -d
```

## Grafana: IP:9030

## Zabbix: IP:9070

## Homer: IP:9080

##### Many thanks to [Zabbix](https://github.com/zabbix), [SipCapture](https://github.com/sipcapture), [Grafana](https://github.com/grafana), [Prometheus](https://github.com/prometheus) and [Grupo ABL](https://grupoabl.com.br/)
