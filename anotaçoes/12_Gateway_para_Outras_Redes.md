# Módulo 12: Gateway para Outras Redes

## Roteador como gateway
O roteador é o que permite que hosts de uma rede se comuniquem com hosts de outra rede diferente. Cada interface do roteador está conectada a uma rede separada, e o endereço IPv4 dessa interface identifica a rede local ligada a ela.

Todo host precisa saber o endereço da interface do roteador ligada à sua própria rede, esse endereço é o **gateway padrão**. Ele pode ser configurado manualmente no host ou recebido automaticamente via DHCP.

Quando o roteador (geralmente sem fio, em casa) está configurado como servidor DHCP, ele mesmo já envia seu próprio endereço IPv4 como gateway padrão pros hosts da rede, junto com o IP e a máscara de sub-rede de cada um.

## Roteador como limite entre redes
O roteador sem fio funciona como servidor DHCP pra todos os hosts locais (por cabo ou Wi-Fi), a chamada **rede interna**. Geralmente esses hosts internos recebem endereços privados, não públicos, o que já garante que a rede interna não fique diretamente acessível pela internet.

Do outro lado, o próprio roteador atua como **cliente** DHCP, recebendo do ISP um endereço IPv4 público pra sua interface de internet. Essa conexão do lado de fora é chamada de **rede externa**.

Ou seja, o roteador serve como fronteira: de um lado a rede interna (privada, dele mesmo como servidor DHCP), do outro a rede externa/internet (onde ele é cliente DHCP do ISP).
