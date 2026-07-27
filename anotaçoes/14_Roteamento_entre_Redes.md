# Módulo 14: Roteamento Entre Redes

## Por que roteamento é necessário
Quando a porção de rede do IP de origem e de destino é diferente, é preciso um roteador pra encaminhar a mensagem. O roteador lê a parte de rede do IP de destino e decide qual caminho seguir. Diferente do switch (que decide pelo MAC), o roteador decide pelo endereço IP.

## Tabela de roteamento
O roteador usa uma tabela de roteamento pra saber qual interface usar pra alcançar cada rede. Essa tabela pode ser:
- Preenchida automaticamente, através de troca de informação com outros roteadores
- Configurada manualmente pelo administrador

Se o roteador não sabe pra onde mandar um pacote, ele descarta. Pra evitar isso, é comum configurar uma **rota padrão**, que serve como destino de qualquer pacote cuja rede não esteja na tabela.

## Gateway padrão
Quando o destino está na mesma rede, o host usa ARP e envia direto. Quando o destino é remoto, o host encapsula o pacote (com o IP de destino real) mas usa o **MAC do roteador** (gateway padrão) no quadro. O host descobre o IP do gateway padrão pela configuração de rede, e o MAC dele através do ARP.

Se o gateway padrão estiver configurado errado ou ausente, o host simplesmente não consegue se comunicar com redes remotas.

## LAN e segmentação
Uma LAN pode ser uma rede única ou várias redes locais interligadas sob o mesmo controle administrativo.

**Todos os hosts num único segmento:**
- Vantagens: mais simples, mais barato, comunicação mais direta e rápida
- Desvantagens: todo mundo compartilha o mesmo domínio de broadcast, dificulta segurança e QoS

**Hosts divididos em segmentos remotos (via roteador):**
- Vantagens: reduz tráfego de broadcast, melhora desempenho, mais segurança e organização
- Desvantagens: mais complexidade, exige roteador, pode introduzir latência
