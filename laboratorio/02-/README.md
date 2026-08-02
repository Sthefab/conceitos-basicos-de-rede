**Conectando-se a um Servidor Web (Packet Tracer)**

Prática de conectividade IP usando Cisco Packet Tracer. O objetivo foi observar como pacotes trafegam pela rede usando endereçamento IP direto (sem DNS).

**O que foi feito:**

- Topologia simples: PC0 (192.168.1.100) → Internet → Servidor Web LearnIP (172.33.100.50)
- Testei conectividade com ping 172.33.100.50 via prompt de comando, confirmando resposta do servidor (com uma leve perda de pacote, normal durante ARP/carregamento dos dispositivos)
- Acessei o servidor pelo navegador do PC0 digitando o IP direto na URL (172.33.100.50), sem usar o nome do domínio
- A página carregou confirmando que o cliente web se conectou ao servidor via IP

**Aprendizado:** reforça o entendimento de como a resolução de endereço IP é a base da comunicação na internet, mesmo antes de qualquer camada de DNS entrar em jogo.
