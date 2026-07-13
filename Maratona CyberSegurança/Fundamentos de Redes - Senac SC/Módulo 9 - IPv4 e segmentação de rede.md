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
![[9.1.1.mp4#subtitle=anexos/9.1.1.vtt]]
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
![[9.1.3.mp4#subtitle=anexos/9.1.3.vtt]]
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
![[9.1.5.mp4#subtitle=anexos/9.1.5.vtt]]
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

# 9.2 Tipos de endereços IPv4

## 9.2.1 Endereços IPv4 públicos e privados

Assim como existem diferentes maneiras de transmitir um pacote IPv4, existem também diferentes tipos de endereços IPv4. Alguns endereços IPv4 não podem ser usados para sair para a Internet, e outros são especificamente alocados para roteamento para a Internet. Alguns são usados para verificar uma conexão e outros são auto-atribuídos. Como administrador de rede, você acabará se familiarizando com os tipos de endereços IPv4, mas por enquanto, você deve pelo menos saber o que eles são e quando usá-los.

Endereços IPv4 públicos são endereços roteados globalmente entre os roteadores do provedor de serviços de Internet (ISP). No entanto, nem todos os endereços IPv4 disponíveis podem ser usados na Internet. Existem blocos de endereços (conhecidos como endereços privados) que são usados pela maioria das organizações para atribuir endereços IPv4 a hosts internos.

Em meados dos anos 90, com a introdução da World Wide Web (WWW), endereços IPv4 privados foram introduzidos devido ao esgotamento do espaço de endereços IPv4. Os endereços IPv4 privados não são exclusivos e podem ser usados internamente em qualquer rede.

**Observação:** A solução a longo prazo para o esgotamento de endereços IPv4 foi o IPv6.

|Endereço de rede e prefixo|RFC 1918 Intervalo de endereços privados|
|---|---|
|10.0.0.0/8|10.0.0.0 – 10.255.255.255|
|172.16.0.0/12|172.16.0.0 – 172.31.255.255|
|192.168.0.0/16|192.168.0.0 – 192.168.255.255|

**Observação:** Endereços privados são definidos no RFC 1918 e às vezes referido como espaço de endereço RFC 1918.

## 9.2.2 Roteamento para a Internet

### Private IPv4 Addresses and Network Address Translation (NAT)

A maioria das redes internas, de grandes empresas a redes domésticas, usa endereços IPv4 privados para endereçar todos os dispositivos internos (intranet), incluindo hosts e roteadores. No entanto, os endereços privados não são globalmente roteáveis.

Na figura, as redes de clientes 1, 2 e 3 estão enviando pacotes fora de suas redes internas. Esses pacotes têm um endereço IPv4 de origem que é um endereço privado e um endereço IPv4 de destino público (globalmente roteável). Os pacotes com um endereço privado devem ser filtrados (descartados) ou traduzidos para um endereço público antes de encaminhar o pacote para um ISP.

### Endereços IPv4 privados e Tradução de Endereços de Rede (NAT)

![[Pasted image 20260530160324.png]]
Antes que o ISP possa encaminhar esse pacote, ele deve traduzir o endereço IPv4 de origem, que é um endereço privado, para um endereço IPv4 público usando a Conversão de Endereços de Rede (NAT). O NAT é usado para converter entre endereços IPv4 privados e IPv4 públicos. Isso geralmente é feito no roteador que conecta a rede interna à rede ISP. Os endereços IPv4 privados na intranet da organização serão traduzidos para endereços IPv4 públicos antes do encaminhamento para a Internet.

## 9.2.3 Atividade - Passar ou bloquear endereços IPv4

Instruções:

Decida passar ou bloquear cada endereço IP, dependendo de ser público (a Internet) ou privado (pequena rede local). Clique em Iniciar para começar e clique em Passar ou Bloquear.

## 9.2.4 Endereços IPv4 de Uso Especial

Existem determinados endereços, como o endereço de rede e o endereço de broadcast, que não podem ser atribuídos aos hosts. Há também endereços especiais que podem ser atribuídos a hosts, mas com restrições quanto ao modo como interagem na rede.

**Endereços de loopback**

Os endereços de loopback (127.0.0.0 / 8 ou 127.0.0.1 a 127.255.255.254) são comumente identificados apenas como 127.0.0.1. Eles são endereços especiais usados por um host para direcionar tráfego para ele mesmo Por exemplo, o comando **ping** é comumente usado para testar conexões com outros hosts. Mas você também pode usar o comando **ping** para testar a configuração de IP do seu próprio dispositivo, como mostrado na figura.

**Observação:** você aprenderá mais sobre o comando **ping** posteriormente neste curso.

### Ping na Interface Loopback

```
C:∖Users∖NetAcad> ping 127.0.0.1

Pinging 127.0.0.1 with 32 bytes of data:

Reply from 127.0.0.1: bytes=32 time<1ms TTL=128

Reply from 127.0.0.1: bytes=32 time<1ms TTL=128

Reply from 127.0.0.1: bytes=32 time<1ms TTL=128

Reply from 127.0.0.1: bytes=32 time<1ms TTL=128

Ping statistics for 127.0.0.1:

    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),

Approximate round trip times in milli-seconds:

    Minimum = 0ms, Maximum = 0ms, Average = 0ms

C:∖Users∖NetAcad> ping 127.1.1.1

Pinging 127.1.1.1 with 32 bytes of data:

Reply from 127.1.1.1: bytes=32 time<1ms TTL=128

Reply from 127.1.1.1: bytes=32 time<1ms TTL=128

Reply from 127.1.1.1: bytes=32 time<1ms TTL=128

Reply from 127.1.1.1: bytes=32 time<1ms TTL=128

Ping statistics for 127.1.1.1:

    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),

Approximate round trip times in milli-seconds:

    Minimum = 0ms, Maximum = 0ms, Average = 0ms

C:∖Users∖NetAcad>
```

**Endereços locais de link**

Os endereços locais de link (169.254.0.0 / 16 ou 169.254.0.1 a 169.254.255.254) são mais conhecidos como endereços APIPA ( endereçamento IP privado automático ) ou endereços auto-atribuídos. Eles são usados por um cliente Windows para se autoconfigurar caso o cliente não consiga obter um endereçamento IP por outros métodos. Endereços de link local podem ser usados em uma conexão ponto a ponto, mas não são comumente usados para esse fim.

## 9.2.5 Endereçamento Classful Legado

Em 1981, os endereços IPv4 foram atribuídos usando o endereço classful, conforme definido na RFC 790 ([https://tools.ietf.org/html/rfc790](https://datatracker.ietf.org/doc/html/rfc790)), Números Atribuídos Os clientes receberam um endereço de rede com base em uma das três classes, A, B ou C. A RFC dividiu os intervalos de unicast em classes específicas da seguinte maneira:

- **Classe A (0.0.0.0/8 to 127.0.0.0/8)** – Projetado para suportar redes extremamente grandes com mais de 16 milhões de endereços de host. A Classe A usou um prefixo fixo /8 com o primeiro octeto para indicar o endereço de rede e os três octetos restantes para endereços de host (mais de 16 milhões de endereços de host por rede).
- **Classe B (128.0.0.0 / 16 - 191.255.0.0 / 16)** - Projetada para oferecer suporte às necessidades de redes de tamanho moderado a grande com até aproximadamente 65.000 endereços de host. A Classe B usou um prefixo fixo /16 com os dois octetos de alta ordem para indicar o endereço de rede e os dois octetos restantes para endereços de host (mais de 65.000 endereços de host por rede).
- **Classe C (192.0.0.0 / 24 - 223.255.255.0 / 24)** - Projetado para oferecer suporte a pequenas redes com no máximo 254 hosts. A Classe C usou um prefixo fixo / 24 com os três primeiros octetos para indicar a rede e o octeto restante para os endereços de host (apenas 254 endereços de host por rede).

**Observação:** Há também um bloco multicast Classe D consistindo de 224.0.0.0 a 239.0.0.0 e um bloco de endereço experimental Classe E consistindo de 240.0.0.0 - 255.0.0.0.

Na época, com um número limitado de computadores usando a internet, o endereçamento clássico era um meio eficaz para alocar endereços. Como mostrado na figura, as redes de classe A e B têm um número muito grande de endereços de host e Classe C tem muito poucos. As redes de classe A representaram 50% das redes IPv4. Isso fez com que a maioria dos endereços IPv4 disponíveis não fossem utilizados.

**Distribuição de Classes de Endereços IPv4**

|Classe|Participação|Total de Redes|Total de Hosts/Redes|
|---|---|---|---|
|Classe A|50%|128|16.777.214|
|Classe B|25%|16.384|65.534|
|Classe C|12,5%|2.097.152|254|
|Classes D e E|12,5%|—|—|
Em meados da década de 1990, com a introdução da World Wide Web (WWW), o endereçamento clássico foi obsoleto para alocar de forma mais eficiente o espaço de endereços IPv4 limitado. A alocação de endereço de classe foi substituída por endereçamento sem classe, que é usado hoje. O endereçamento sem classe ignora as regras das classes (A, B, C). Endereços de rede IPv4 públicos (endereços de rede e máscaras de sub-rede) são alocados com base no número de endereços que podem ser justificados.

## 9.2.6 Atribuição de Endereços IP

Regional Internet Registries

Endereços IPv4 públicos são endereços roteados globalmente pela Internet. Endereços IPv4 públicos devem ser exclusivos.

Os endereços IPv4 e IPv6 são gerenciados pela IANA (Internet Assigned Numbers Authority). A IANA gerencia e aloca blocos de endereços IP aos registros regionais de Internet (RIRs). Os cinco RIRs são mostrados na figura.

Os RIRs são responsáveis por alocar endereços IP aos ISPs que fornecem blocos de endereços IPv4 para organizações e ISPs menores. As organizações também podem obter seus endereços diretamente de um RIR (sujeito às políticas desse RIR).

### Registros Regionais da Internet

![[Pasted image 20260530163806.png]]

## 9.2.7 Atividade - Endereço IPv4 público ou privado

|Endereço|Tipo|Correto|
|---|---|---|
|172.16.35.2|Privada|✅|
|192.168.3.5|Privada|✅|
|192.0.3.15|Pública|✅|
|64.104.0.22|Pública|✅|
|209.165.201.30|Pública|✅|
|192.168.11.5|Privada|✅|
|172.16.30.30|Privada|✅|
|10.55.3.168|Privada|✅|

## 9.2.8 Verifique sua compreensão - Tipos de endereços IPv4

### Pergunta 1

Quais duas afirmações estão corretas sobre endereços IPv4 privados?

- [x] Qualquer organização (casa, escola, escritório, empresa) pode usar o endereço 10.0.0.0/8.
- [ ] 172.99.1.1 é um endereço IPv4 privado.
- [ ] Os roteadores de Internet normalmente encaminharão qualquer pacote com um endereço de destino que seja um endereço IPv4 privado.
- [x] Endereços IPv4 privados são atribuídos a dispositivos dentro da intranet de uma organização (rede interna).

✅ RESPOSTAS CORRETAS: Qualquer organização (casa, escola, escritório, empresa) pode usar o endereço 10.0.0.0/8. / Endereços IPv4 privados são atribuídos a dispositivos dentro da intranet de uma organização (rede interna).

> Endereços IPv4 privados são atribuídos a dispositivos dentro da intranet de uma organização (rede interna) e qualquer organização (casa, escola, escritório, empresa) pode usar o endereço 10.0.0.0/8.

---

### Pergunta 2

Quais duas afirmações estão corretas sobre endereços IPv4 privados? (Escolha duas)

- [ ] 192.168.1.10 é um endereço IPv4 público.
- [x] Para acessar um dispositivo pela Internet, o endereço IPv4 de destino deve ser um endereço público.
- [x] O esgotamento do endereço IPv4 público é uma razão pela qual existem endereços IPv4 privados e por que as organizações estão fazendo a transição para o IPv6.
- [ ] Endereços IPv4 públicos podem ser atribuídos a dispositivos na intranet de uma organização (rede interna).

✅ RESPOSTAS CORRETAS: Para acessar um dispositivo pela Internet, o endereço IPv4 de destino deve ser um endereço público. / O esgotamento do endereço IPv4 público é uma razão pela qual existem endereços IPv4 privados e por que as organizações estão fazendo a transição para o IPv6.

> Para acessar um dispositivo pela Internet, o endereço IPv4 de destino deve ser um endereço público. O esgotamento do endereço IPv4 público é uma razão pela qual existem endereços IPv4 privados e por que as organizações estão fazendo a transição para o IPv6.

---

### Pergunta 3

Qual organização ou grupo de organizações recebe endereços IP da IANA e é responsável por alocar esses endereços para ISPs e algumas organizações?

- [x] RIR
- [ ] IETF
- [ ] ISPs de nível 1
- [ ] IEEE

✅ RESPOSTA CORRETA: RIR

> Os RIRs recebem endereços IP da IANA e são responsáveis por alocar esses endereços para ISPs e algumas outras organizações.


# 9.3 Segmentação de Rede

## 9.3.1 Vídeo - Segmentação de Rede

Em uma LAN Ethernet, dispositivos utilizam broadcast Ethernet para entrar em contato com todos os dispositivos na mesma rede local. Por exemplo, um dispositivo enviará uma solicitação ARP na rede local para descobrir o endereço MAC associado. Isto é um broadcast Ethernet pesquisando um endereço IPv4 conhecido. Switches propagam broadcast em todas as interfaces exceto a interface que o quadro foi recebido. Roteadores não propagam broadcast. Quando um roteador recebe um broadcast, ele não o encaminha para outras interfaces. Isso é conhecido como domínio de broadcast.

Outro exemplo de um broadcast Ethernet é um host que envia uma mensagem de descoberta DHCP para localizar um servidor DHCP. O servidor DHCP fornece um endereço IPv4 e outras informações para o cliente. Mais uma vez, os switches propagam esses broadcast em todas as interfaces, exceto a interface em que foi recebido. O roteador não vai propagar este broadcast Ethernet para as outras interfaces.

Como podem ver, há uma camada separada para domínio de broadcast. Um roteador segmenta ou separa a camada em domínios de broadcast.

## 9.3.2 Domínios de Broadcast e Segmentação

### Domínios de transmissão de segmentos de roteadores

Você já recebeu um e-mail que foi endereçado a todas as pessoas do seu trabalho ou escola? Este foi um e-mail de transmissão. Felizmente continha informações que cada um de vocês precisava saber. Mas muitas vezes uma transmissão não é realmente pertinente para todos na lista de discussão. Às vezes, apenas um segmento da população precisa ler essa informação.

Em uma LAN Ethernet, os dispositivos usam broadcast e o Protocolo de Resolução de Endereços (ARP) para localizar outros dispositivos. O ARP envia broadcasts dea Camada 2 para um endereço IPv4 conhecido na rede local para descobrir o endereço MAC associado. Os dispositivos em LANs Ethernet também localizam outros dispositivos usando serviços. Um host normalmente adquire sua configuração de endereço IPv4 usando o protocolo DHCP (Dynamic Host Configuration Protocol) que envia broadcasts na rede local para localizar um servidor DHCP.

Os switches propagam broadcasts por todas as interfaces, exceto a interface em que foram recebidos. Por exemplo, se um switch na figura recebesse um broadcast, ele o encaminharia para os outros switches e os outros usuários conectados na rede.

### Roteadores segmentam domínios de broadcast

![[Pasted image 20260530164639.png]]


Roteadores não propagam broadcasts. Quando um roteador recebe um broadcast, ele não o encaminha por outras interfaces. Por exemplo, quando R1 recebe um broadcast na interface Gigabit Ethernet 0/0, ele não o encaminha por outra interface.

Portanto, cada interface do roteador se conecta a um domínio de broadcast e as transmissões são propagadas apenas dentro desse domínio de broadcast específico.

## 9.3.3 Problemas com Domínios de Broadcast Grandes

### Um Domínio de Broadcast Grande

Um grande domínio de broadcast é uma rede que conecta vários hosts. Um problema desse tipo de domínio é que os hosts podem gerar broadcasts em excesso e afetar a rede de forma negativa. Na figura, a LAN 1 conecta 400 usuários que podem gerar uma quantidade excessiva de tráfego de broadcast. Isso resulta em operações de rede lentas devido à quantidade significativa de tráfego que pode causar e operações de dispositivo lentas porque um dispositivo deve aceitar e processar cada pacote de difusão.

### Um Domínio de Broadcast Grande

![[Pasted image 20260530164703.png]]

### Comunicação entre Redes

A solução é reduzir o tamanho da rede para criar domínios de broadcast menores em um processo denominado divisão em sub-redes. Os espaços de rede menores são chamados de sub-redes.

Na figura, os 400 usuários da LAN 1 com endereço de rede 172.16.0.0/16 foram divididos em duas sub-redes de 200 usuários cada: 172.16.0.0/24 e 172.16.1.0/24. Os broadcasts são propagados apenas dentro dos domínios de broadcast menores. Portanto, um broadcast em LAN 1 não se propagaria para LAN 2.

### Comunicação entre Redes

![[Pasted image 20260530164719.png]]

Observe como o comprimento do prefixo mudou de /16 para /24. Esta é a base da divisão em sub-redes: usar bits de host para criar sub-redes adicionais.

**Observação**: os termos sub-rede e rede costumam ser usados de maneira intercambiável. A maioria das redes são uma sub-rede de um bloco de endereços maior.

## 9.3.4 Razões para Segmentar Redes

A divisão em sub-redes reduz o tráfego total da rede e melhora seu desempenho. Além disso, permite que o administrador implemente políticas de segurança como, por exemplo, quais sub-redes podem ou não se comunicar com quais sub-redes. Outra razão é que reduz o número de dispositivos afetados pelo tráfego anormal de transmissão devido a configurações incorretas, problemas de hardware/software ou intenção mal-intencionada.

Há várias maneiras de usar sub-redes para gerenciar dispositivos de rede.

**Clique em cada imagem para obter uma ilustração de como os administradores de rede podem agrupar dispositivos e serviços em sub-redes.**

### Localização

Divisão em Sub-Redes por Local

![[Pasted image 20260530164804.png]]

### Grupo ou Função

Sub-redes por grupo ou função

![[Pasted image 20260530165411.png]]

### Tipo de dispositivo

Divisão em sub-Redes por Tipo de Dispositivo

O diagrama mostra um roteador, R1, conectando três LANs/sub-redes juntas que foram atribuídas de acordo com o tipo de dispositivo. A LAN 1 no endereço 10.0.1.0/24 está conectada ao G0/0 e inclui todos os hosts. A LAN 2 no endereço 10.0.2.0/24 está conectada ao G0/1 e inclui todas as impressoras. A LAN 3 no endereço 10.0.3.0/24 está conectada ao G0/2 e inclui todos os servidores. R1 também tem uma conexão com a Internet.

![[Pasted image 20260530165427.png]]

Os administradores de rede podem criar sub-redes usando qualquer outra divisão que faça sentido para a rede. Observe nas figuras que as sub-redes usam comprimentos de prefixo para identificar redes.

É fundamental que todos os administradores de redes entendam a divisão da rede em sub-redes. Vários métodos foram criados para ajudar a entender esse processo. Embora um pouco esmagador a princípio, preste muita atenção aos detalhes e, com a prática, a sub-rede se tornará mais fácil.

### 9.3.5 Verifique sua compreensão - Segmentação de rede

**Verifique sua compreensão sobre segmentação de rede escolhendo a melhor resposta para as seguintes perguntas**.

### Pergunta 1

Quais dispositivos não encaminharão um pacote de difusão IPv4 por padrão?

- [ ] Switch Ethernet
- [x] roteador
- [ ] PC com Windows
- [ ] Nenhuma das alternativas acima. Todos os dispositivos encaminha pacotes de difusão IPv4 por padrão.

✅ RESPOSTA CORRETA: roteador

> Por padrão, os roteadores não encaminham um pacote de transmissão IPv4.

---

### Pergunta 2

Quais duas situações são o resultado de tráfego excessivo de transmissão? (Escolha duas)

- [ ] quando o roteador tem que encaminhar um número excessivo de pacotes
- [x] operações de dispositivos lentas
- [x] operações de rede lentas
- [ ] quando os dispositivos em todas as redes adjacentes são afetados

✅ RESPOSTAS CORRETAS: operações de dispositivos lentas, operações de rede lentas

> Operações de rede lentas e operações lentas de dispositivos são o resultado de tráfego broadcast excessivo.


# 9.4 Resumo - IPv4 e segmentação de rede

## 9.4.1 O que eu aprendi neste módulo?

### Unicast, broadcast e multicast IPv4

Transmissão unicast refere-se a um dispositivo que envia uma mensagem para outro dispositivo em comunicações um-para-um. Um pacote unicast tem um endereço IP de destino que é um endereço unicast que vai para um único destinatário. Um endereço IP de origem só pode ser um endereço unicast, porque o pacote só pode originar-se de uma única origem. Isso independentemente de o endereço IP de destino ser unicast, broadcast ou multicast. Os endereços de host unicast IPv4 estão no intervalo de endereços de 1.1.1.1 a 223.255.255.255.

Transmissão broadcast refere-se a um dispositivo enviando uma mensagem para todos os dispositivos em uma rede, ou seja, comunicação de um para todos. Um pacote de broadcast possui um endereço IP de destino com todos os (1s) na parte do host ou 32 (um) bits. Um pacote de broadcast deve ser processado por todos os dispositivos no mesmo domínio de difusão. Um broadcast pode ser direcionado ou limitado. Um broadcast direcionado é enviado para todos os hosts em uma rede específica. Uma broadcast limitado é enviado para 255.255.255.255. Por padrão, os roteadores não encaminham broadcasts.

Transmissão multicast reduz o tráfego, permitindo que um host envie um único pacote para um conjunto de hosts selecionados que participem de um grupo multicast. Um pacote multicast é um pacote com um endereço IP de destino que é um endereço multicast. O IPv4 reservou os endereços 224.0.0.0 a 239.255.255.255 como intervalo de multicast. Cada grupo multicast é representado por um único endereço IPv4 multicast de destino. Quando um host IPv4 se inscreve em um grupo multicast, o host processa pacotes endereçados tanto a esse endereço multicast como a seu endereço unicast alocado exclusivamente.

---

### Tipos de endereços IPv4

Os endereços IPv4 públicos são endereços roteados globalmente entre os roteadores ISP. No entanto, nem todos os endereços IPv4 disponíveis podem ser usados na Internet. Existem blocos de endereços (conhecidos como endereços privados) que são usados pela maioria das organizações para atribuir endereços IPv4 a hosts internos. A maioria das redes internas, de grandes empresas a redes domésticas, usa endereços IPv4 privados para endereçar todos os dispositivos internos (intranet), incluindo hosts e roteadores. No entanto, os endereços privados não são globalmente roteáveis. Antes que o ISP possa encaminhar esse pacote, ele deve traduzir o endereço IPv4 de origem, que é um endereço privado, para um endereço IPv4 público usando NAT (Tradução de Endereços de Rede).

Os endereços de loopback (127.0.0.0 / 8 ou 127.0.0.1 a 127.255.255.254) são mais comumente identificados como apenas 127.0.0.1, esses são endereços especiais usados por um host para direcionar o tráfego para si próprio. Os endereços locais de link (169.254.0.0 / 16 ou 169.254.0.1 a 169.254.255.254) são mais conhecidos como endereços APIPA (endereçamento IP privado automático) ou endereços auto-atribuídos. Eles são usados por um cliente DHCP do Windows para auto-configurar no caso de não existirem servidores DHCP disponíveis.

Em 1981, os endereços IPv4 foram atribuídos usando o endereço classful, conforme definido na RFC 790 (https://tools.ietf.org/html/rfc790), Números Atribuídos. Os clientes receberam um endereço de rede com base em uma das três classes, A, B ou C. A RFC dividiu os intervalos de unicast em classes específicas da seguinte maneira:

- **Classe A (0.0.0.0/8 to 127.0.0.0/8)** – Projetado para suportar redes extremamente grandes com mais de 16 milhões de endereços de host.
- **Classe B (128.0.0.0 / 16 – 191.255.0.0 / 16)** – Projetada para oferecer suporte às necessidades de redes de tamanho moderado a grande com até aproximadamente 65.000 endereços de host.
- **Classe C (192.0.0.0 / 24 – 223.255.255.0 / 24)** – Projetado para oferecer suporte a pequenas redes com no máximo 254 hosts.

Há também um bloco multicast de Classe D que consiste em 224.0.0.0 a 239.0.0.0 e um bloco de endereço experimental de Classe E que consiste em 240.0.0.0 – 255.0.0.0.

Endereços IPv4 públicos são endereços roteados globalmente pela Internet. Endereços IPv4 públicos devem ser exclusivos. Os endereços IPv4 e IPv6 são gerenciados pela IANA (Internet Assigned Numbers Authority). A IANA gerencia e aloca blocos de endereços IP aos registros regionais de Internet (RIRs). Os RIRs são responsáveis por alocar endereços IP aos ISPs que fornecem blocos de endereços IPv4 para organizações e ISPs menores. As organizações também podem obter seus endereços diretamente de um RIR.

---

### Segmentação de Rede

Em uma LAN Ethernet, os dispositivos utilizam broadcast e ARP para localizar outros dispositivos. O ARP envia broadcast de Camada 2 para um endereço IPv4 conhecido na rede local para descobrir o endereço MAC associado. Os dispositivos em LANs Ethernet também localizam outros dispositivos usando serviços. Um host normalmente adquire sua configuração de endereço IPv4 usando o protocolo DHCP que envia broadcasts na rede local para localizar um servidor DHCP. Os switches propagam broadcasts por todas as interfaces, exceto a interface em que foram recebidos.

Um grande domínio de broadcast é uma rede que conecta vários hosts. Um problema desse tipo de domínio é que os hosts podem gerar broadcasts em excesso e afetar a rede de forma negativa. A solução é reduzir o tamanho da rede para criar domínios de broadcast menores em um processo denominado divisão em sub-redes. Os espaços de rede menores são chamados de sub-redes. Esta é a base da divisão em sub-redes: usar bits de host para criar sub-redes adicionais. A divisão em sub-redes reduz o tráfego total da rede e melhora seu desempenho. Permite o administrador implemente políticas de segurança como, por exemplo, quais sub-redes podem ou não se comunicar com quais sub-redes. Ela reduz o número de dispositivos afetados pelo tráfego broadcast anormal de devido a configurações incorretas, problemas de hardware/software ou propósito malicioso.

## 9.4.2 Webster – Questões para Reflexão

Acabei de enviar convites para uma festa para vários amigos e familiares. Os convites foram para endereços diferentes, mas o cartão dentro é o mesmo para todos. É como um e-mail de multicast, não é? Eu não sabia que era possível fazer isso e também não sabia que era possível enviar um e-mail de broadcast para todas as pessoas na rede! Você consegue pensar em um bom motivo para enviar um e-mail de broadcast a todos na rede? Você consegue pensar em uma razão pela qual deve tomar cuidado antes de enviar um e-mail de broadcast?

## 9.4.3 Questionário sobre IPv4 e segmentação de rede

### Pergunta 1

Qual afirmação descreve uma finalidade da configuração de máscara de sub-rede para um host?

- [ ] É usado para determinar o número máximo de bits em um pacote que pode ser colocado em uma rede específica.
- [ ] É usado para identificar o gateway padrão.
- [x] É usado para determinar a qual rede o host está conectado.
- [ ] É usado para descrever o tipo de sub-rede.

✅ RESPOSTA CORRETA: É usado para determinar a qual rede o host está conectado.

---

### Pergunta 2

Qual é um dos motivos para criar sub-redes em uma rede IP?

- [ ] para aumentar o número de endereços de host disponíveis na rede
- [ ] para garantir que todos os dispositivos possam se comunicar entre si sem a necessidade de um roteador
- [x] para reduzir o escopo de inundações de broadcast
- [ ] para eliminar a necessidade de serviços de rede que dependem de broadcast, como DHCP

✅ RESPOSTA CORRETA: para reduzir o escopo de inundações de broadcast

---

### Pergunta 3

Uma mensagem é enviada para todos os hosts em uma rede remota. Que tipo de mensagem é essa?

- [ ] unicast
- [ ] multicast
- [ ] broadcast limitado
- [x] broadcast direcionado

✅ RESPOSTA CORRETA: broadcast direcionado

---

### Pergunta 4

Um usuário não consegue acessar o servidor da empresa de um computador. Ao emitir o comando **ipconfig**, o usuário descobre que o endereço IP do computador é exibido como 169.254.0.2. Que tipo de endereço é este?

- [ ] experimental
- [x] link-local
- [ ] privado
- [ ] loopback

✅ RESPOSTA CORRETA: link-local

---

### Pergunta 5

Quais são os três endereços IP privados? (Escolha três.)

- [ ] 224.6.6.6
- [x] 10.1.1.1
- [x] 192.168.5.5
- [x] 172.16.4.4
- [ ] 172.32.5.2
- [ ] 192.167.10.10

✅ RESPOSTA CORRETA: 10.1.1.1, 192.168.5.5, 172.16.4.4

---

### Pergunta 6

Faça a correspondência de cada descrição com um endereço IP apropriado.

|Categoria|Resposta correta|
|---|---|
|240.2.6.255|um endereço experimental|
|198.133.219.2|um endereço público|
|169.254.1.5|um endereço link-local|
|127.0.0.1|um endereço loopback|

---

### Pergunta 7

Qual dispositivo de rede pode servir como um limite para dividir um domínio de broadcast de camada 2 ?

- [x] roteador
- [ ] pontes Ethernet
- [ ] Ponto de Acesso
- [ ] Hub Ethernet

✅ RESPOSTA CORRETA: roteador

---

### Pergunta 8

Qual é a função da IANA?

- [ ] promover o desenvolvimento e a evolução da Internet em todo o mundo
- [ ] manter os padrões relacionados à fiação elétrica e aos conectores
- [x] gerenciar a alocação de endereços IP e nomes de domínio
- [ ] documentar os desenvolvimentos de novos protocolos e atualizar os protocolos atuais

✅ RESPOSTA CORRETA: gerenciar a alocação de endereços IP e nomes de domínio

---

### Pergunta 9

Qual é o intervalo de prefixo de endereço reservado para o multicast IPv4?

- [ ] 169.254.0.0 – 169.254.255.255
- [ ] 127.0.0.0 – 127.255.255.255
- [x] 224.0.0.0 – 239.255.255.255
- [ ] 240.0.0.0 – 254.255.255.255

✅ RESPOSTA CORRETA: 224.0.0.0 – 239.255.255.255

---

### Pergunta 10

Uma escola secundária em Nova York (escola A) está usando tecnologia de videoconferência para estabelecer interações estudantis com outra escola secundária (escola B) na Rússia. A videoconferência é realizada entre dois dispositivos finais através da Internet. O administrador de rede da escola A configura o dispositivo final com o endereço IP 209.165.201.10. O administrador envia uma solicitação para o endereço IP para o dispositivo final na escola B e a resposta é 192.168.25.10. Nenhuma escola está usando uma VPN. O administrador sabe imediatamente que este IP não funcionará. Por quê?

- [ ] Há um conflito de endereço IP.
- [x] Este é um endereço IP privado.
- [ ] Este é um endereço de loopback.
- [ ] Este é um endereço local do link.

✅ RESPOSTA CORRETA: Este é um endereço IP privado.

---

### Pergunta 11

Um host está fazendo broadcast de uma transmissão. Qual host ou hosts o receberão?

- [ ] todos os hosts na Internet
- [ ] um grupo especialmente definido de hosts
- [ ] o vizinho mais próximo na mesma rede
- [x] todos os hosts na mesma rede

✅ RESPOSTA CORRETA: todos os hosts na mesma rede