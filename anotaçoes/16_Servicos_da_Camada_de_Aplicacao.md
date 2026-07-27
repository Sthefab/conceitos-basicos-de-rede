# Módulo 16: Serviços da Camada de Aplicação

## Relação cliente-servidor
Um servidor executa um software que disponibiliza algum serviço (email, web, arquivos) pra outros hosts. Um mesmo computador pode rodar vários softwares cliente ao mesmo tempo (navegador, email, mensagens).

## URI, URN e URL
- **URN**: identifica o nome do recurso, sem indicar onde ele está
- **URL**: indica a localização exata de um recurso na rede (ex: endereço de site)

Uma URL é composta por protocolo (https, ftp etc), nome do host, caminho do arquivo e, às vezes, um fragmento específico da página.

## Web (HTTP/HTTPS)
O navegador usa a porta 80 (HTTP) pra pedir páginas ao servidor. O conteúdo é formatado em HTML. Como o HTTP não é seguro (dados trafegam sem criptografia), existe o HTTPS, que usa a porta 443 e criptografa a comunicação.

## FTP
Permite transferir arquivos entre dispositivos. Usa duas portas: 21 pra controle da conexão e 20 pra transferência dos dados em si.

## Telnet e SSH
- **Telnet** (porta 23): acesso remoto a um dispositivo por linha de comando, mas transmite tudo em texto simples, sem criptografia — inseguro
- **SSH** (porta 22): faz a mesma coisa, mas com autenticação mais forte e dados criptografados. É a opção recomendada hoje em dia

## E-mail
Protocolos envolvidos:
- **SMTP** (porta 25): usado pra enviar mensagens
- **POP3** (porta 110): baixa as mensagens pro cliente e geralmente remove do servidor
- **IMAP4** (porta 143): mantém as mensagens no servidor, sincronizando entre dispositivos

## Mensagens e chamadas pela internet
Mensagens de texto (WhatsApp, Teams etc) e chamadas por VoIP (telefonia via internet) usam tecnologia peer-to-peer, convertendo voz analógica em dados digitais encapsulados em pacotes IP.
