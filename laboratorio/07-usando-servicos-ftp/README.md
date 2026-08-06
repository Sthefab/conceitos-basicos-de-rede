# Usando Serviços FTP

Prática de upload, download, renomeação e exclusão de arquivo em um servidor FTP via linha de comando, usando o Cisco Packet Tracer.

**O que foi feito:**
- Conectei ao servidor FTP (`ftp 209.165.200.226`) autenticando com usuário e senha
- Fiz upload do arquivo `sampleFile.txt` pro servidor com o comando `put`
- Renomeei o arquivo no servidor pra `sampleFile_FTP.txt` com o comando `rename`
- Baixei o arquivo renomeado de volta pro PC com o comando `get`
- Excluí o arquivo do servidor FTP

**Resultado:** 1/1 na avaliação da atividade

**Aprendizado:** entendi na prática o fluxo de comandos do cliente FTP (`put`, `get`, `rename`, `dir`, `delete`) e reforcei que o FTP transmite login e dados sem criptografia — o que o torna inadequado pra ambientes que exigem segurança, sendo SFTP ou FTPS as alternativas seguras pra esse mesmo tipo de transferência.
