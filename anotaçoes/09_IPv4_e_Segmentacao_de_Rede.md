# Módulo 9: IPv4 e Segmentação de Rede

## Tipos de transmissão

Quando um pacote é enviado numa rede, ele pode ser transmitido de três formas diferentes:

- **Unicast**: comunicação um-para-um, de um dispositivo pra outro específico. É o tipo mais comum.
- **Broadcast**: um dispositivo envia a mensagem pra todos os outros da mesma rede. Existe só no IPv4 (o IPv6 não usa broadcast).
- **Multicast**: um dispositivo envia a mensagem pra um grupo específico de dispositivos que se inscreveram naquele grupo, sem precisar mandar pra rede inteira.

## Endereços públicos e privados

Nem todo IP pode navegar direto na internet. Existem faixas reservadas de endereços privados, usadas dentro de redes internas (empresas, casas), que não são exclusivas e podem se repetir em redes diferentes:

- 10.0.0.0/8
- 172.16.0.0/12
- 192.168.0.0/16

Pra esses endereços privados conseguirem sair pra internet, é feita uma tradução pra um endereço público, processo chamado NAT (Network Address Translation).

## Endereços especiais

- **Loopback (127.0.0.1)**: usado pelo próprio dispositivo pra testar a si mesmo, tipo dar um ping em si mesmo.
- **Link-local (169.254.x.x)**: endereço que o próprio dispositivo assume automaticamente quando não consegue receber um IP por outro meio (também conhecido como APIPA).

## Endereçamento classful (histórico)

Antigamente os endereços IPv4 eram divididos em classes fixas (A, B e C), cada uma com uma quantidade determinada de endereços de host. Esse modelo foi deixado de lado nos anos 90 porque desperdiçava muitos endereços, sendo substituído pelo endereçamento sem classe, usado até hoje.

## Por que segmentar a rede

Redes muito grandes geram excesso de tráfego de broadcast, porque cada dispositivo precisa processar cada pacote de broadcast recebido. Isso deixa a rede mais lenta.

A solução é dividir a rede em sub-redes menores (subnetting), diminuindo o domínio de broadcast. Isso também ajuda a:
- aplicar políticas de segurança entre setores diferentes
- isolar problemas de configuração ou hardware
- organizar dispositivos por local, função ou tipo
