**Examinando o NAT em um Roteador Wireless**

Prática de NAT (Network Address Translation) em ambiente doméstico simulado no Cisco Packet Tracer.

**O que foi feito:**

- Conectei 4 PCs a um roteador wireless, todos recebendo IP privado via DHCP
- Acessei a interface web do roteador (admin/admin) e examinei o IP público atribuído pelo ISP na porta de Internet, além das configurações de rede local e faixa de DHCP
- Usei o modo Simulation do Packet Tracer pra criar uma PDU complexa (HTTP) de um PC até o servidor externo ciscolearn.nat.com
- Analisei os cabeçalhos dos pacotes nas versões Inbound e Outbound, observando a troca do endereço IP de origem (privado → público) feita pelo NAT

**Aprendizado:** visualização prática de como o NAT traduz endereços privados em um endereço público pra permitir que dispositivos da rede interna acessem a internet, já que endereços privados não conseguem trafegar diretamente pela rede externa.
