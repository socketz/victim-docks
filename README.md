# Web Env

## apache1
- Apache 2.4 -> port 8101

## apache2
- Apache 2.4 + mod_security -> port 8102

## apache3
- Apache 2.4 + iptables -> port 8103

## apache4
- Apache 2.4 + mod_security + iptables -> port 8104


Para un correcto funcionamiento, habilitar en la VM o host los puertos 8101-8104 TCP.

Ejecutar en la raíz del proyecto:
```
docker-compose up -d
```
