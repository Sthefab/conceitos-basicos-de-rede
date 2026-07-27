# Módulo 8: Protocolo de Internet (IPv4)

## Pra que serve o endereço IPv4
Qualquer host que queira acessar a internet precisa de um endereço IPv4, que é um endereço de rede lógico único que identifica aquele dispositivo. Ele precisa ser único tanto dentro da rede local quanto no mundo, pra garantir comunicação local e remota.

O endereço fica associado à interface de rede do dispositivo (a placa de rede, ou NIC). Um servidor com mais de uma placa de rede pode até ter mais de um IPv4, um pra cada interface. Todo pacote enviado na internet carrega o IP de origem e o de destino, pra garantir que os dados cheguem certo e as respostas voltem.

## Como o endereço é representado
O IPv4 tem 32 bits, mas escrito em binário é praticamente ilegível. Por isso ele é dividido em 4 grupos de 8 bits (octetos), e cada octeto é convertido pra decimal, separado por ponto. É a famosa notação decimal com ponto, tipo `209.165.200.1`.

## Estrutura do endereço: rede e host
O endereço IPv4 tem duas partes: a porção de **rede** e a porção de **host**. A máscara de sub-rede é o que define onde uma parte termina e a outra começa.

Exemplo: no endereço `192.168.5.11` com máscara `255.255.255.0`, os três primeiros octetos (`192.168.5`) identificam a rede, e o último octeto (`11`) identifica o host específico dentro dela.

Esse é um endereçamento hierárquico: o roteador só precisa saber como chegar até a rede certa, sem precisar conhecer a localização de cada host individualmente (parecido com um número de telefone, onde o DDD identifica a região e o resto identifica a linha específica).

Dois hosts só conseguem se comunicar diretamente (sem roteamento) se tiverem a mesma porção de rede no endereço IPv4. Inclusive é possível ter mais de uma rede lógica dentro da mesma rede física, se os hosts tiverem porções de rede diferentes.
