# Módulo 2: Componentes, Tipos e Conexões de Rede

## Clientes e servidores
Todo dispositivo conectado a uma rede é um host, e pode atuar como:
- **Servidor**: tem um software instalado que fornece algum serviço (email, páginas web, arquivos) pra outros hosts.
- **Cliente**: tem um software que solicita e exibe essas informações (ex: navegador).

Um mesmo computador pode ser cliente e servidor ao mesmo tempo, dependendo do software instalado.

## Redes ponto a ponto (P2P)
Quando o mesmo dispositivo funciona como cliente e servidor simultaneamente, é uma rede P2P. É comum em casas e empresas pequenas.

**Vantagens**: fácil de configurar, barata, boa pra tarefas simples (compartilhar arquivo, impressora)
**Desvantagens**: sem administração centralizada, menos segura, não escala bem, pode deixar o desempenho lento (porque o mesmo dispositivo faz os dois papéis)

## Componentes da infraestrutura de rede
A rede é formada por três tipos de componente:
- **Dispositivos finais**: onde a mensagem começa ou termina (computador, celular, impressora, câmera de segurança etc)
- **Dispositivos intermediários**: fazem a mensagem passar de um ponto a outro (switch, roteador, firewall, access point)
- **Meios físicos**: por onde o sinal passa (cabo, fibra, sinal sem fio)

## Conexão com o provedor (ISP)
O ISP é quem faz a ponte entre a rede local (de casa, por exemplo) e a internet. Os ISPs se conectam entre si formando o backbone da internet, majoritariamente com cabos de fibra óptica.

Formas comuns de conexão até o ISP:
- **Cabo**: usa o mesmo cabo coaxial da TV a cabo, sempre ativo, boa largura de banda
- **DSL**: usa linha telefônica, também sempre ativo, mas a velocidade depende da distância até a central telefônica
- **Celular**: acesso via rede de telefonia móvel, prático mas limitado por franquia de dados
- **Satélite**: opção pra áreas sem cabo ou DSL, mas exige linha de visão livre pro satélite
- **Discada (dial-up)**: opção antiga e bem lenta, praticamente em desuso

A escolha da conexão depende muito da localização e do que está disponível na região.
