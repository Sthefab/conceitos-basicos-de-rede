# Módulo 11: Endereçamento Dinâmico com DHCP

## Endereçamento estático
No endereçamento estático, o administrador configura manualmente, em cada host, pelo menos:
- Endereço IP
- Máscara de sub-rede
- Gateway padrão

**Vantagens**: útil pra dispositivos que precisam ter sempre o mesmo IP, como servidores e impressoras, já que clientes acessam esses serviços por um endereço fixo.

**Desvantagens**: configurar manualmente em cada host toma tempo e aumenta a chance de erro, porque a verificação feita é bem básica. Também exige manter um controle preciso de quais IPs já foram atribuídos, já que endereços estáticos normalmente não são reutilizados.

## Endereçamento dinâmico (DHCP)
Como a quantidade de dispositivos numa rede muda o tempo todo (gente entrando com notebook novo, trocando de aparelho etc), é mais prático deixar a atribuição de IP automática. Isso é feito pelo **DHCP** (Dynamic Host Configuration Protocol), que distribui automaticamente:
- Endereço IPv4
- Máscara de sub-rede
- Gateway padrão
- Outras configurações de rede

O DHCP é o método preferido em redes grandes, porque reduz o trabalho da equipe de suporte e praticamente elimina erro de digitação.

Uma característica importante: o endereço não é permanente, ele é "alugado" por um tempo. Quando o host desliga ou sai da rede, o endereço volta pro pool disponível pra ser reutilizado por outro dispositivo. Isso é bem útil em ambientes com muitos usuários móveis entrando e saindo, como um hotspot de aeroporto.

## Onde fica o servidor DHCP
- Em redes médias/grandes, geralmente é um servidor dedicado (baseado em PC)
- Em redes residenciais, geralmente é o próprio ISP, ou o roteador sem fio de casa

No caso do roteador doméstico, ele acumula os dois papéis: é **cliente** DHCP pra receber o IP público do ISP, e é **servidor** DHCP pra distribuir IPs privados pros dispositivos da rede interna.
