# Módulo 7: A Camada de Acesso

## Encapsulamento
Assim como uma carta precisa de um envelope formatado corretamente (com endereço de origem e destino) pra ser entregue, cada mensagem enviada numa rede também precisa ser "empacotada" seguindo um formato específico. Esse processo se chama **encapsulamento**: a mensagem original é colocada dentro de um quadro, que contém o endereço de destino e de origem.

O processo inverso, quando o destinatário retira a mensagem do quadro, é o **desencapsulamento**. Se o formato do quadro estiver incorreto, a mensagem simplesmente não é entregue nem processada.

## O que é a camada de acesso
É a parte da rede por onde os dispositivos (hosts) se conectam pra ter acesso a arquivos compartilhados, impressoras e outros hosts. Numa rede Ethernet com fio, cada host se conecta a um dispositivo de camada de acesso através de um cabo Ethernet.

## Hub x Switch
- **Hub**: dispositivo mais antigo, envia a mensagem pra todas as portas ao mesmo tempo. Só permite uma mensagem por vez, e se duas chegarem juntas, causa colisão. Por isso caiu em desuso.
- **Switch**: substituiu o hub. Trabalha na camada 2 e lê o endereço MAC de cada quadro pra saber exatamente pra qual porta enviar a mensagem, em vez de mandar pra todo mundo.

## Tabela de endereços MAC
O switch mantém uma tabela interna que relaciona cada porta com o endereço MAC do host conectado nela. Essa tabela é criada e atualizada automaticamente: toda vez que chega um quadro novo, o switch olha o endereço MAC de origem e aprende em qual porta aquele host está.

Quando uma mensagem chega, o switch verifica na tabela se o MAC de destino é conhecido. Se for, ele cria uma conexão direta (circuito) só entre a porta de origem e a de destino, em vez de espalhar a mensagem pela rede toda. Isso evita colisões e melhora bastante o desempenho da rede.
