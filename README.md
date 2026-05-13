# 🌐 ISP Proyecto - Cisco Packet Tracer

## 📋 Descripción
Red ISP completa diseñada y configurada en Cisco Packet Tracer.
Simula la infraestructura real de un proveedor de servicios de internet
con routing dinámico, segmentación por VLANs y servicios de red.

## 🛠️ Tecnologías implementadas
- **BGP** — Protocolo de enrutamiento entre AS100 (ISP) y AS200 (Internet)
- **OSPF** — Enrutamiento dinámico interno del ISP
- **VLANs** — Segmentación de red por tipo de cliente
- **Inter-VLAN Routing** — Comunicación entre segmentos
- **HTTP Server** — Servidor web del ISP
- **NOC Server** — Centro de operaciones de red

## 🖧 Dispositivos utilizados
| Dispositivo | Modelo | Función |
|---|---|---|
| Router ISP-Internet | 2911 | Backbone / AS200 |
| Router-edge | 2911 | Borde BGP AS100 |
| Router-core | 2911 | Core OSPF |
| SW-Distribucion | 3560-24PS | Inter-VLAN L3 |
| SW-Residencial | 2960 | Acceso VLAN 10 |
| SW-Empresarial | 2960 | Acceso VLAN 20 |
| SRV-DHCP-DNS | Server-PT | HTTP + DNS |
| SRV-NOC | Server-PT | Monitoreo |

## 🌍 Direccionamiento IP
| Red | Segmento | Uso |
|---|---|---|
| 10.0.0.0/30 | WAN | ISP-Internet ↔ Router-edge |
| 10.0.1.0/30 | WAN | Router-edge ↔ Router-core |
| 10.0.2.0/30 | LAN | Router-core ↔ SW-Distribucion |
| 192.168.10.0/24 | VLAN 10 | Clientes residenciales |
| 192.168.20.0/24 | VLAN 20 | Clientes empresariales |
| 172.16.0.0/24 | Servidores | DHCP, DNS, NOC |

## ✅ Pruebas realizadas
- Ping inter-VLAN exitoso
- Comunicación PC → Servidores
- Conectividad BGP con Internet
- Servidor HTTP respondiendo desde browser

## 👤 Autor
adrian alvarez jaramillo
Proyecto de infraestructura de red ISP profesional
