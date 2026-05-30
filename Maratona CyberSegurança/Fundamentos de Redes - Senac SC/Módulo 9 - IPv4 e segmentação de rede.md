# 9.0 Introdução

## 9.0.1 Webster - Por que devo fazer este módulo?

Kishori tem um novo paciente, Divya, que foi internado hoje. Como Srinivas, Divya não fala a mesma língua que Kishori fala. O Divya só fala telugu e tem inglês limitado. Kishori quer enviar um e-mail para as enfermeiras no próximo turno para determinar se alguma delas fala Telugu. Kishori pode enviar uma mensagem de e-mail multicast, que é uma única mensagem de e-mail enviada para vários destinatários específicos. Você já sabe sobre a estrutura de endereços IPv4. Agora é a hora de aprender mais sobre eles. Você já ouviu falar de endereços IPv4 unicast, broadcast e multicast? O que são endereços IPv4 públicos e privados? Explore este módulo para entender melhor os endereços IPv4!

## 9.0.2 O Que Vou Aprender Neste Módulo?

**Titulo do módulo:** IPv4 e segmentação de rede

**Objetivo do Módulo:** explicar como os endereços IPv4 são usados na comunicação e segmentação de rede.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Unicast, broadcast e multicast IPv4|Comparar as características e os usos dos endereços IPv4 unicast, multicast e broadcast.|
|Tipos de endereços IPv4|Explicar os endereços IPv4 públicos, privados e reservados.|
|Segmentação de Rede|Explicar como a divisão em sub-redes segmenta uma rede para facilitar a comunicação.|

# 9.1 Unicast, broadcast e multicast IPv4

## 9.1.1 Vídeo - Unicast IPv4

Neste vídeo, vamos dar uma olhada na transmissão IP unicast. Então aqui temos o HOST 172.16.4.1. Ele vai enviar um pacote unicast — é um pacote onde o endereço IP de destino é destinado a um único dispositivo. E vai enviá-lo para o endereço IP de destino da impressora em 172.16.4.253.

Portanto, o endereço IP de origem é 172.16.4.1 e o endereço IP de destino do pacote é 172.16.4.253. Podemos ver aqui que o pacote vai de um único dispositivo para um único dispositivo, neste caso a impressora. E, a propósito, um endereço IP de origem só pode ser unicast. O que queremos dizer com isso é que um pacote só pode se originar a partir de um único dispositivo. Neste caso, o endereço de destino também é um unicast, o que significa que é destinado apenas a um único dispositivo.

## 9.1.2 Unicast

No tópico anterior, você aprendeu sobre a estrutura de um endereço IPv4; cada um tem uma parte de rede e uma parte de host. Existem diferentes maneiras de enviar um pacote de um dispositivo de origem, e essas transmissões diferentes afetam os endereços IPv4 de destino.

Transmissão unicast refere-se a um dispositivo que envia uma mensagem para outro dispositivo em comunicações um-para-um.

Um pacote unicast tem um endereço IP de destino que é um endereço unicast que vai para um único destinatário. Um endereço IP de origem só pode ser um endereço unicast, porque o pacote só pode originar-se de uma única origem. Isso independentemente de o endereço IP de destino ser unicast, broadcast ou multicast.

**Observação:** Neste curso, todas as comunicações entre dispositivos são unicast, a menos que especificado de outra forma.

Os endereços de host unicast IPv4 estão no intervalo de endereços de 1.1.1.1 a 223.255.255.255. Contudo, dentro desse intervalo há muitos endereços que já são reservados para fins especiais. Esses endereços para fins especiais serão discutidos mais adiante neste módulo.

**Observação:** Na animação, observe que a máscara de sub-rede para 255.255.255.0 é representada usando a notação de barra ou / 24. Isso indica que a máscara de sub-rede tem 24 bits. A máscara de sub-rede 255.255.255.0 em binário é 11111111.11111111.11111111.00000000.

## 9.1.3 Vídeo - Broadcast IPv4

Neste vídeo, vamos dar uma olhada nas transmissões de broadcast. Então temos um pacote com o endereço IPv4 de origem 172.16.4.1 e um endereço IPv4 de destino de 255.255.255.255.

Esse é um endereço especial, o que significa que é destinado a todos os dispositivos da rede. É conhecido como broadcast. Se olharmos aqui, o pacote sai da fonte 172.16.4.1 e observe que nosso switch Ethernet inundou o pacote em todas as portas, exceto a porta de entrada. E foi recebido por todos os dispositivos da rede.

Agora, quando este roteador recebe a transmissão, ele não encaminhará o pacote de broadcast para outras redes. Mas um broadcast significa que todos os dispositivos na rede receberão o pacote IPv4.

## 9.1.4 Broadcast

Transmissão broadcast refere-se a um dispositivo enviando uma mensagem para todos os dispositivos em uma rede, ou seja, comunicação de um para todos.

Um pacote de broadcast possui um endereço IP de destino com todos os (1s) na parte do host ou 32 (um) bits.

**Observação:** O IPv4 usa pacotes de broadcast. No entanto, não há pacotes de broadcast com IPv6.

Um pacote de broadcast deve ser processado por todos os dispositivos no mesmo domínio de broadcast. Um domínio de broadcast identifica todos os hosts no mesmo segmento de rede. Um broadcast pode ser direcionado ou limitado. Um broadcast direcionado é enviado para todos os hosts em uma rede específica. Por exemplo, um host na rede 172.16.4.0/24 envia um pacote para 172.16.4.255. Uma broadcast limitado é enviado para 255.255.255.255. Por padrão, os roteadores não encaminham broadcasts.

---

Pacotes de transmissão usam recursos na rede e fazem com que todos os hosts receptores da rede processem o pacote. Portanto, o tráfego broadcast deve ser limitado para não prejudicar o desempenho da rede ou dos dispositivos. Como os roteadores separam domínios de broadcast, subdividir as redes pode melhorar seu desempenho ao eliminar o excesso de tráfego broadcast.


## 9.1.5 Vídeo - Multicast IPv4

Neste vídeo, vamos dar uma olhada nas transmissões de multicast. Então temos um pacote com o endereço IPv4 de origem 172.16.4.1 e um endereço IPv4 de destino de 224.0.0.10.

Esse é um endereço multicast especial. O multicast é diferente do broadcast porque é destinado apenas a um grupo específico de dispositivos que optaram por receber o tráfego multicast. Não é destinado a todos os dispositivos da rede como no broadcast.

Se olharmos aqui, o pacote sai da fonte 172.16.4.1 e é entregue apenas aos dispositivos que fazem parte do grupo multicast 224.0.0.10. Os dispositivos que não fazem parte desse grupo simplesmente ignorarão o pacote.

Os endereços multicast estão no intervalo de 224.0.0.0 a 239.255.255.255. Assim, o multicast permite que um único pacote seja enviado a um grupo selecionado de hosts ao mesmo tempo, o que é muito eficiente para coisas como streaming de vídeo ou protocolos de roteamento onde você quer enviar informações para múltiplos roteadores, mas não para todos os dispositivos da rede.

## 9.1.6 Multicast

Transmissão multicast reduz o tráfego, permitindo que um host envie um único pacote para um conjunto de hosts selecionados que participem de um grupo multicast.

Um pacote multicast é um pacote com um endereço IP de destino que é um endereço multicast. O IPv4 reservou os endereços 224.0.0.0 a 239.255.255.255 como intervalo de multicast.

Os hosts que recebem pacotes multicast específicos são chamados de clientes multicast. Os clientes multicast usam serviços solicitados por um programa cliente para se inscrever no grupo multicast.

Cada grupo multicast é representado por um único endereço IPv4 multicast de destino. Quando um host IPv4 se inscreve em um grupo multicast, o host processa pacotes endereçados tanto a esse endereço multicast como a seu endereço unicast alocado exclusivamente.

Protocolos de roteamento, como OSPF, usam transmissões multicast. Por exemplo, os roteadores habilitados com OSPF se comunicam entre si usando o endereço multicast OSPF reservado 224.0.0.5. Somente dispositivos habilitados com OSPF processarão esses pacotes com 224.0.0.5 como endereço IPv4 de destino. Todos os outros dispositivos ignorarão esses pacotes.

## 9.1.7 Atividade - Unicast, Broadcast ou Multicast

**Instruções:**

Clique em Iniciar para visualizar o endereço de IP de destino. Em seguida, clique no host ou hosts que receberão um pacote com base no tipo de endereço (unicast, broadcast ou multicast). Clique **Verificar** para verificar sua resposta. Clique **Novo Problemar** novamente para obter um novo problema.