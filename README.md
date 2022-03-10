# Zabbix-Homer-Grafana-Docker
## Instalação

```
wget https://repo.zabbix.com/zabbix/6.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_6.0-1+ubuntu20.04_all.deb
dpkg -i zabbix-release_6.0-1+ubuntu20.04_all.deb
apt update
apt install zabbix-agent2 docker docker-compose
usermod -aG docker zabbix
service zabbix-agent2 restart
```
```
git clone https://github.com/eduardober/Zabbix-Homer-Grafana-Docker.git
cd Zabbix-Homer-Grafana-Docker
docker-compose up -d
```
## Grafana: IP:9030

## Zabbix: IP:9070

## Homer: IP:9080

##### Many thanks to [Zabbix](https://github.com/zabbix), [SipCapture](https://github.com/sipcapture), [Grafana](https://github.com/grafana), [Prometheus](https://github.com/prometheus) and [Grupo ABL](https://grupoabl.com.br/)
