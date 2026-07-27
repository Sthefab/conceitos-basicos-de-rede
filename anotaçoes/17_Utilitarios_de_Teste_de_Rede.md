# Módulo 17: Utilitários de Teste de Rede

## ipconfig
Mostra a configuração IP atual do host (endereço IP, máscara de sub-rede, gateway padrão).
- `ipconfig /all`: mostra informações completas, incluindo MAC, servidor DNS e status do DHCP
- `ipconfig /release`: libera a configuração IP atual obtida via DHCP
- `ipconfig /renew`: solicita uma nova configuração ao servidor DHCP

Útil quando o host está com configuração de IP desatualizada ou incorreta, já que renovar pode resolver o problema de conectividade.

## ping
Testa se um dispositivo consegue ser alcançado na rede. Envia um pacote (echo request) e espera uma resposta (echo reply).

- Ping bem-sucedido pro IP mas falho pro nome → problema de DNS
- Ping falho em geral → problema de conectividade no caminho
- Ping falho só pro gateway padrão → problema é local
- Ping falho pro gateway, mas rede local ok → problema é fora da rede local

Às vezes o ping falha mesmo com a rede funcionando, por causa de firewall bloqueando o tráfego.
