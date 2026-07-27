# Módulo 13: O Processo de ARP

## MAC x IP
Todo dispositivo numa LAN Ethernet tem dois endereços:
- **Endereço físico (MAC)**: usado pra comunicação direta entre placas de rede na mesma rede
- **Endereço lógico (IP)**: usado pra levar o pacote da origem até o destino, seja na mesma rede ou numa rede remota

## Destino na mesma rede
Se o destino está na mesma rede local, o endereço MAC de destino no quadro é o do próprio dispositivo de destino.

## Destino em rede remota
Se o destino está numa rede remota, o endereço MAC de destino no quadro é o do **gateway padrão** (a interface do roteador), não o do destino final. O roteador recebe o quadro, olha o IP de destino, decide o próximo salto e reencapsula o pacote com um novo endereço MAC pra continuar o caminho. Isso se repete em cada roteador do trajeto, até chegar no destino final.

## O processo ARP
Quando um host só sabe o IP de destino e precisa descobrir o MAC correspondente (dentro da mesma rede), ele usa o ARP (Address Resolution Protocol), em 3 passos:

1. O host envia um quadro de broadcast perguntando "quem tem esse IP?"
2. Todos os hosts da rede recebem o broadcast, mas só quem tem aquele IP responde com seu MAC
3. O host de origem guarda essa relação IP-MAC numa tabela ARP, pra não precisar repetir o processo toda vez

Como o ARP depende de broadcast, todos os hosts envolvidos precisam estar no mesmo domínio de broadcast.
