# Módulo 4: Construindo uma Rede Doméstica

## Componentes de uma rede doméstica
Além do roteador, vários outros dispositivos se conectam à rede de casa: computador, smart TV, console de jogos, impressora, câmera de segurança, dispositivos de controle climático, entre outros.

## Portas do roteador
Um roteador doméstico típico tem dois tipos principais de porta:
- **Portas Ethernet/LAN**: conectam dispositivos da rede local (todos ficam na mesma rede)
- **Porta Internet/WAN**: conecta o roteador ao modem (DSL ou cabo), ligando à internet

Por padrão, os dispositivos conectados via Wi-Fi também ficam na mesma rede local dos que estão conectados por cabo nas portas Ethernet.

## Tecnologias sem fio e com fio
- **Bluetooth**: opera em 2,4 GHz, curto alcance, ótimo pra conectar periféricos (mouse, teclado, fone)
- **Wi-Fi**: opera em 2,4 GHz e 5 GHz, segue os padrões IEEE 802.11, com alcance e velocidade maiores que o Bluetooth
- **Ethernet com fio**: ainda usada quando se quer uma conexão dedicada, sem compartilhar sinal com outros dispositivos. O cabo mais comum é o categoria 5e (par trançado)

## Padrões Wi-Fi
O IEEE define os padrões técnicos (802.11 e suas variações, como 802.11n, 802.11ac). A Wi-Fi Alliance testa e certifica que os dispositivos de fabricantes diferentes seguem esses padrões e funcionam entre si.

Configurações básicas de uma rede sem fio:
- **Modo de rede**: define quais padrões 802.11 são aceitos (pode ser modo misto pra aceitar vários)
- **SSID**: nome da rede, até 32 caracteres, diferencia maiúscula de minúscula
- **Canal**: normalmente automático, o próprio access point escolhe o melhor
- **Broadcast SSID**: se ativado, o nome da rede aparece pra qualquer dispositivo por perto. Desativar dificulta um pouco a descoberta da rede, mas não substitui uma boa criptografia

## Configurando o roteador doméstico
Pra configurar o roteador pela primeira vez, normalmente é preciso conectar um computador via cabo Ethernet numa porta LAN (nunca na porta Internet). Depois disso, o computador recebe um IP automaticamente via DHCP, e dá pra acessar a interface de configuração do roteador pelo navegador.

Alguns cuidados na hora de configurar:
- Evitar colocar marca ou modelo do roteador no nome da rede (SSID), pra não facilitar ataques
- Verificar se os dispositivos que vão conectar são compatíveis com o padrão Wi-Fi configurado
- Alguns roteadores permitem criar uma rede separada para convidados, com acesso restrito só à internet
