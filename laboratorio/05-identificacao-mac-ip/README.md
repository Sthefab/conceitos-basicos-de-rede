## Identificação de Endereços MAC e IP

Prática de análise de cabeçalhos de camada 2 (MAC) e camada 3 (IP) usando o modo Simulation do Cisco Packet Tracer.

**O que foi feito:**
- Analisei a comunicação entre dois dispositivos na mesma rede local (172.16.31.3 → 172.16.31.2), observando que o endereço MAC de destino aponta direto pro host, sem passar por gateway
- Analisei a comunicação entre um dispositivo remoto (10.10.10.2) e um host em outra rede (172.16.31.5), rastreando a PDU em cada salto: Switch, Router (in/out), Access Point
- Repeti o processo pra mensagem de echo-reply, no sentido contrário (10.10.10.2 → 172.16.31.5)
- Registrei em tabela como os endereços MAC mudam a cada salto (encapsulamento por segmento), enquanto o endereço IP de origem/destino permanece o mesmo do início ao fim

**Aprendizado:** entendimento prático da diferença entre endereçamento de camada 2 (MAC, muda a cada segmento de rede) e camada 3 (IP, permanece constante fim a fim), e do papel do roteador na tradução entre esses dois domínios de endereçamento.

### Comunicação Local (172.16.31.3 → 172.16.31.2)

| No Dispositivo | MAC de Origem | MAC de Destino | IPv4 de Origem | IPv4 de Destino |
|---|---|---|---|---|
| 172.16.31.3 | 0060.7036.2849 | 000C:85CC:1DA7 | 172.16.31.3 | 172.16.31.2 |
| Switch 2 | 0060.7036.2849 | 000C:85CC:1DA7 | N/A | N/A |
| 172.16.31.2 (in) | 000C:85CC:1DA7 | 000C:85CC:1DA7 | 172.16.31.3 | 172.16.31.2 |
| 172.16.31.2 (out) | 0060.7036.2849 | 0060.7036.2849 | 172.16.31.2 | 172.16.31.3 |

### Comunicação Remota — Echo Request (172.16.31.3 → 10.10.10.2)

| No Dispositivo | MAC de Origem | MAC de Destino | IPv4 de Origem | IPv4 de Destino |
|---|---|---|---|---|
| 172.16.31.3 | 00D0:D311:C788 | 00D0:BA8E:741A | 172.16.31.3 | 10.10.10.2 |
| Switch 2 | 0060.7036.2849 | 00D0:BA8E:741A | N/A | N/A |
| Router (in) | 0060.7036.2849 | 00D0:BA8E:741A | 172.16.31.3 | 10.10.10.2 |
| Router (out) | 00D0:588C:2401 | 0060:2F84:4AB6 | 172.16.31.3 | 10.10.10.2 |
| Switch 1 | 00D0:588C:2401 | 0060:2F84:4AB6 | N/A | N/A |
| Access Point | N/A | N/A | N/A | N/A |
| 10.10.10.2 | 0060:2F84:4AB6 | 00D0:588C:2401 | 10.10.10.2 | 172.16.31.5 |

### Comunicação Remota — Echo Reply (10.10.10.2 → 172.16.31.5)

| No Dispositivo | MAC de Origem | MAC de Destino | IPv4 de Origem | IPv4 de Destino |
|---|---|---|---|---|
| 10.10.10.2 | 0060:2F84:4AB6 | 00D0:588C:2401 | 10.10.10.2 | 172.16.31.3 |
| Access Point | N/A | N/A | N/A | N/A |
| Switch 1 | 0060:2F84:4AB6 | 00D0:588C:2401 | N/A | N/A |
| Router (in) | 0060:2F84:4AB6 | 00D0:588C:2401 | 10.10.10.2 | 172.16.31.3 |
| Router (out) | 00D0.BA8E.741A | 0060.7036.2849 | 10.10.10.2 | 172.16.31.3 |
| Switch 1 | 00D0.BA8E.741A | 0060.7036.2849 | N/A | N/A |
| Access Point | N/A | N/A | N/A | N/A |
| 10.10.10.2 | 00D0.BA8E.741A | 0060.7036.2849 | 10.10.10.2 | 172.16.31.5 |
