# Módulo 15: TCP e UDP

## Números de porta
Serviços como DNS, Web, e-mail e FTP são identificados por números de porta, que ficam entre 1 e 65.535, geridos pela ICANN. Existem três faixas:
- **Bem conhecidas (1–1023)**: associadas a aplicativos comuns
- **Registradas (1024–49151)**: usadas por empresas pra aplicativos específicos
- **Privadas (49152–65535)**: geralmente usadas como porta de origem, por qualquer aplicativo

Algumas portas comuns: 21 (FTP), 22 (SSH), 23 (Telnet), 25 (SMTP), 53 (DNS), 80 (HTTP), 443 (HTTPS), 110 (POP3), 143 (IMAP).

## Pares de sockets
Um socket é a combinação do endereço IP com o número da porta (ex: `192.168.1.5:1099`). Quando um cliente se comunica com um servidor, o par formado pelo socket de origem e o socket de destino identifica exclusivamente aquela conversa específica, permitindo que vários processos rodem ao mesmo tempo sem se confundir.

## O comando netstat
Serve pra listar as conexões TCP ativas no host: protocolo, endereço local, endereço remoto e status da conexão. Útil pra identificar conexões suspeitas ou desconhecidas, um sinal de possível risco de segurança.
