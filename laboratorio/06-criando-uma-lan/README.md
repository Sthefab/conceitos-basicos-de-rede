# Criando uma LAN

Prática de conexão de hosts, endereçamento IPv4 e verificação de conectividade em uma LAN de filial, usando o modo Physical do Cisco Packet Tracer.

**O que foi feito:**
- Liguei os dispositivos finais e o Office Router, e conectei Admin PC, Manager PC e Impressora ao switch com cabos copper straight-through
- Configurei Admin PC e Manager PC pra receber endereçamento via DHCP, fornecido pelo Office Router
- Configurei a impressora com IP estático, prática comum pra dispositivos acessados por outros hosts na rede
- Verifiquei conectividade com ping entre os PCs e a impressora, e testei acesso ao servidor de internet por IP e por URL
- Usei `ipconfig` / `ipconfig /all` e `tracert` pra inspecionar o endereçamento do host e rastrear o caminho até o destino remoto

**Resultado:** 13/13 na avaliação da atividade

**Aprendizado:** entendi na prática por que hosts na mesma rede têm IPs diferentes mas compartilham a mesma máscara de sub-rede e o mesmo gateway padrão (o gateway define a rede, o host ID identifica cada dispositivo), e vi que conseguir pingar por IP mas não acessar por URL geralmente indica falha de DNS, não de conectividade.
