# Módulo 10: Formatos e Regras de Endereçamento IPv6

## Por que o IPv6 é necessário
O IPv4 tem um limite teórico de 4,3 bilhões de endereços, e esse número está se esgotando com o crescimento da internet, dos dispositivos móveis e da Internet das Coisas (IoT). Soluções como NAT ajudaram a segurar esse esgotamento, mas trazem problemas, como latência e limitações pra comunicação direta entre dispositivos.

O IPv6 resolve isso com um espaço de endereços muito maior: 128 bits, contra os 32 bits do IPv4, permitindo uma quantidade absurda de endereços possíveis. Além disso, o IPv6 trouxe melhorias, como o ICMPv6, que já inclui resolução de endereço e configuração automática.

## Coexistência entre IPv4 e IPv6
Não existe uma data única de transição, os dois protocolos convivem juntos por um bom tempo. Existem três formas de fazer essa transição:

- **Pilha dupla**: o dispositivo roda IPv4 e IPv6 ao mesmo tempo
- **Tunelamento**: o pacote IPv6 é encapsulado dentro de um pacote IPv4 pra atravessar uma rede que só suporta IPv4
- **Conversão (NAT64)**: traduz pacotes entre IPv4 e IPv6, parecido com o NAT tradicional

## Sistema hexadecimal
Diferente do IPv4 (que usa números decimais), o IPv6 usa números hexadecimais, de base 16 (0 a 9 e A a F). Isso permite representar endereços bem maiores de forma mais compacta.

## Formato do endereço IPv6
Um endereço IPv6 tem 128 bits, dividido em 8 grupos de 16 bits cada, chamados hextetos, separados por dois-pontos:
2001:0db8:0000:1111:0000:0000:0000:0200
## Regra 1: omitir zeros à esquerda
Zeros à esquerda de cada hexteto podem ser removidos:
- `01AB` vira `1AB`
- `0a00` vira `a00`

Só funciona pros zeros à esquerda, nunca à direita (senão o endereço fica ambíguo).

## Regra 2: dois-pontos duplos (::)
Uma sequência contínua de hextetos zerados pode ser substituída por `::`, mas só pode ser usada **uma vez** no mesmo endereço (senão fica impossível saber quantos zeros foram omitidos).

Exemplo:

Preferencial: 2001:0db8:0000:1111:0000:0000:0000:0200
Compactado: 2001:db8:0:1111::200
Se tiver mais de uma sequência de zeros, usa o `::` na mais longa. Se forem do mesmo tamanho, usa na primeira.
