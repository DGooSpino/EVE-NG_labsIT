# Lab de Redes: Servidor DHCP con Dnsmasq en EVE-NG

Implementación práctica de un servidor DHCP centralizado utilizando **Alpine Linux** (`dnsmasq`) en **EVE-NG** para asignar direcciones IP dinámicas dentro de una red local.
## Topología y Direccionamiento

* **R1 (Router):** `192.168.10.1` (Puerta de enlace / Gateway, interfaz `e0/0`).
* **DHCP-Server (Alpine + Dnsmasq):** `192.168.10.2` (Interfaz `e0`).
* **Switch S1:** Interconecta el router (`e0/2`), el servidor (`e0/3`) y los equipos clientes (`PC4`, `PC5`, `PC6`, `PC7`).

## Configuración de Dnsmasq (`/etc/dnsmasq.conf`)

```text
interface=eth0
bind-interfaces
dhcp-range=192.168.10.50,192.168.10.150,255.255.255.0,12h
dhcp-option=3,192.168.10.1
dhcp-option=6,8.8.8.8
```
