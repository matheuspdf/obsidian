
# 13.0 Introdução

## 13.0.1 Webster — Por que devo fazer este módulo?

Kishori estava olhando para seu telefone e notou que seu telefone, na verdade, tem seu próprio endereço IP. Ela foi para casa e percebeu que o endereço IP havia mudado para um valor diferente do endereço que ela tinha no hospital. Ela lembrou que o DHCP fornece endereços aos dispositivos automaticamente, então ela percebe que obtém endereços IP de diferentes locais, dependendo de onde ela esteja. Isso faz sentido para ela porque ela sabe que esses endereços permitem que os dispositivos acessem redes diferentes. Kishori também nota que seu telefone tem um endereço MAC. Ela verificou e notou que o endereço MAC é sempre o mesmo, independentemente da rede onde está conectada. Faz sentido para Kishori que seu endereço IP mude quando ela está conectada a redes diferentes em locais diferentes, mas seu endereço MAC é sempre o mesmo, porque seu telefone é o telefone, não importa onde ela esteja.

Isso significa que os endereços IP e MAC devem ser necessários para que o telefone receba dados. O endereço IP informa, ao remetente dos dados, onde ela está e, assim que os dados chegam à sua localização, o endereço MAC do telefone permite que o dispositivo receba dados com destino apenas para ela. Pensando mais um pouco, Kishori se pergunta como os endereços MAC podem ser conhecidos pela rede. O DHCP fornece os endereços IP corretos para a rede, mas cada dispositivo tem seu próprio endereço MAC.

Kisori está pronta a aprender mais! E você? Continue lendo!


## 13.0.2 O que vou aprender neste módulo?

**Título do Módulo:** O Processo de ARP

**Objetivo do Módulo:** Explicar como o ARP permite a comunicação em uma rede.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|MAC e IP|Comparar as funções do endereço MAC e do endereço IP.|
|Contenção de Broadcast|Explicar por que é importante conter broadcasts em uma rede.|

# 13.1 MAC e IP

## 13.1.1 Destino na mesma rede

Às vezes, um host deve enviar uma mensagem, mas ele só sabe o endereço IP do dispositivo de destino. O host precisa saber o endereço MAC desse dispositivo, mas como ele pode ser descoberto? É aí que a resolução de endereços se torna crítica.

Dois endereços principais são atribuídos a um dispositivo em uma LAN Ethernet:

- **Endereço físico (o endereço MAC)** - Usado para comunicações de NIC para NIC na mesma rede Ethernet.
- **Endereço lógico (o endereço IP)** – Usado para enviar o pacote do dispositivo de origem para o dispositivo de destino. O endereço IP de destino pode estar na mesma rede IP que a origem ou pode estar em uma rede remota.

Os endereços físicos da camada 2 (ou seja, endereços MAC Ethernet) são usados para entregar o quadro de enlace de dados, contendo o pacote IP encapsulado, a partir de uma NIC para outra NIC que está na mesma rede. Se o endereço IP de destino estiver na mesma rede, o endereço MAC de destino será o do dispositivo de destino.

Considere o exemplo a seguir usando representações de endereço MAC simplificadas.

![[Pasted image 20260609195721.png]]

Neste exemplo, PC1 deseja enviar um pacote para PC2. A figura exibe os endereços MAC de destino e de origem da Camada 2 e o endereçamento IPv4 da Camada 3 que seriam incluídos no pacote enviado a partir do PC1.

O quadro Ethernet da camada 2 contém o seguinte:

- **Endereço MAC de destino** — Este é o endereço MAC simplificado de PC2, 55-55-55.
- **Endereço MAC de origem** — Este é o endereço MAC simplificado da NIC Ethernet em PC1, aa-aa-aa .

O pacote IP da camada 3 contém o seguinte:

- **Endereço IPv4 de origem** — Este é o endereço IPv4 de PC1, 192.168.10.10 .
- **Endereço IPv4 dedestino** — Este é o endereço IPv4 de PC2, 192.168.10.11.


## 13.1.2 Destino em uma Rede Remota

Quando o endereço IP de destino (IPv4 ou IPv6) estiver em uma rede remota, o endereço MAC de destino será o endereço do gateway padrão do host (ou seja, a interface do roteador).

Considere o exemplo a seguir usando uma representação de endereço MAC simplificada.

![[Pasted image 20260609195818.png]]

Neste exemplo, PC1 deseja enviar um pacote para PC2. O PC2 está localizado na rede remota. Como o endereço IPv4 de destino não está na mesma rede local que PC1, o endereço MAC de destino é o do gateway padrão local, no roteador.

Os roteadores examinam o endereço IPv4 destino para determinar o melhor caminho para encaminhar o pacote IPv4. Quando o roteador recebe o quadro Ethernet, ele desencapsula as informações da Camada 2. Usando o endereço IPv4 de destino, ele determina o dispositivo do próximo salto e, em seguida, encapsula o pacote IPv4 em um novo quadro (da camada de enlace) para a interface de saída.

No nosso exemplo, o R1 agora encapsularia o pacote com novas informações de endereço da Camada 2, conforme mostrado na figura.

![[Pasted image 20260609195832.png]]
O novo endereço MAC de destino seria o da interface G0/0/1 em R2 e o novo endereço MAC de origem seria o da interface G0/0/1 em R1.

Ao longo de cada link do caminho, um pacote IP é encapsulado em um quadro. O quadro é específico para a tecnologia do enlace associado a esse link, como Ethernet. Se o dispositivo do próximo salto for o destino final, o endereço MAC de destino será o da NIC Ethernet do dispositivo, conforme mostrado na figura.

![[Pasted image 20260609195847.png]]

Como os endereços IP dos pacotes IP em um fluxo de dados são associados aos endereços MAC em cada link ao longo do caminho até o destino? Para pacotes IPv4, isso é feito através de um processo chamado ARP (Address Resolution Protocol). Para pacotes IPv6, o processo é ICMPv6 Neighbor Discovery (ND).


## 13.1.3 Packet Tracer – Identificar endereços MAC e IP

Nesta atividade do Packet Tracer, você atingirá os seguintes objetivos:

- Reunir informações de PDU para comunicação em Rede Local
- Reunir informações de PDU para comunicação em Rede Remota

Esta atividade é otimizada para a visualização de PDUs. Os dispositivos já estão configurados. Você reunirá informações das PDUs no modo de simulação e responderá a uma série de perguntas sobre os dados coletados.

Packet Tracer – Identificação de Endereços MAC e IP

## Objetivos

Parte 1: Reunir informações de PDU para comunicação em uma Rede Local

Parte 2: Reunir informações de PDU para  comunicação com uma Rede Remota

## Background

Se você estiver interessado em uma carreira em administração de redes ou segurança de redes, é importante entender os processos normais de comunicação de rede. Nesta atividade do Packet Tracer, você inspecionará quadros Ethernet e pacotes IP em diferentes pontos da rede à medida que viajam da origem ao destino. Você se concentrará na maneira como os endereços MAC e IP mudam dependendo do destino (local ou remoto) e do local onde as PDUs são capturadas.

O Packet Tracer possui um modo de simulação que permite investigar detalhes sobre como as PDUs trafegam nas redes. Ele permite que você verifique o endereçamento MAC da camada 2 e o endereçamento IPv4 da camada 3 das PDUs em diferentes locais da rede à medida que as PDUs fluem da origem para o destino.

Essa atividade é otimizada para a visualização de PDUs enquanto viajam em redes locais e remotas. Você reunirá informações de PDU no modo de simulação PT e responderá uma série de perguntas sobre os dados coletados. Não será necessário configurar os dispositivos.

## Instruções

## Parte 1: Reunir informações de PDU para uma comunicação em Rede Local

Nesta parte, você estudará como um dispositivo em uma rede local não precisa de um gateway padrão para se comunicar com outro dispositivo na mesma rede local.

**Observação**: revise as Perguntas para Reflexão na Parte 3 antes de prosseguir nesta parte. Ele lhe dará uma idéia do tipo de informação que você precisará coletar.

a.   Clique no host **172.16.31.3** e abra o **Command Prompt**.

b.  Digite o comando **ping 172.16.31.2**. Este comando emitirá uma série de pacotes ICMP echo request para o destino. Se os pacotes chegarem ao destino, ele enviará pacotes echo-reply para a origem dos  ping requests.

c.  Clique no botão **Simulation** Mode para alternar para o modo de simulação. Repita o comando **ping 172.16.31.2** Um ícone de envelope, que representa uma PDU, aparece próximo a **172.16.31.3**.

d.  Clique na PDU e localize as seguintes informações nas guias **OSI** **Model** e **Outbound PDU Details**. A guia **Outbound PDU Details** mostra cabeçalhos simplificados de pacotes e quadros para a PDU. Você deve observar os seguintes detalhes sobre o endereçamento da PDU.

·  No dispositivo: **172.16.31.3**

·  Endereço MAC de origem: **0060.7036.2849**

·  Endereço MAC de destino: **000C:85CC:1DA7**

·  Endereço IP Origem: **172.16.31.3**

·  Endereço IP Destino: **172.16.31.2**

e.  Clique em **Capture / Forward (a seta para a direita seguida por uma barra vertical)** e a PDU passa para a próxima etapa em sua jornada. Use a guia do modelo OSI para coletar as mesmas informações da Etapa 1d. Repita esse processo até que a PDU chegue ao seu destino. Para cada etapa no caminho até a entrega, registre as informações de cada PDU em uma planilha que usa um formato como mostrado na tabela abaixo. As informações da primeira etapa são mostradas na tabela.

Exemplo em Formato de Planilha

||||||
|---|---|---|---|---|
||||||
||||||
||||||
||||||

||||||
|---|---|---|---|---|
||||||
||||||
||||||
||||||

Ocultar resposta

f.  Você vai notar que as informações da PDU de entrada não mudam.

#### Pergunta:

Na janela PDU information , clique na guia Outbound PDU Details (PDU de saída). Como o endereçamento difere, e por quê? Registre o endereçamento em sua tabela.

Área de Resposta

Os endereços de origem e destino são revertidos no quadro e no pacote porque essa PDU será enviada de volta ao host 172.16.31.3. Esta mensagem será uma resposta de eco de ping.0he frame e pacote porque esta PDU será enviada de volta ao host 172.16.31.3. Esta mensagem será uma resposta de eco de ping.

Ocultar resposta

g.   Volte ao modo de **Realtime**.

## Parte 2: Reúna informações de PDU para comunicação com uma Rede Remota

Para se comunicar com redes remotas, é necessário um dispositivo gateway. O dispositivo gateway conecta duas ou mais redes. Nesta parte, você estudará o processo que ocorre quando um dispositivo se comunica com outro dispositivo que está em uma rede remota. Preste muita atenção aos endereços MAC usados.

**Observação**: Coloque o mouse sobre o **Router**. Você verá informações sobre o endereçamento das interfaces do roteador. Consulte esses endereços ao observar o fluxo de PDUs que atravessa o roteador.

a.  Retorne ao **Command Prompt** de 172.16.31.3.

b.  Insira o comando **ping 10.10.10.2**. O primeiro par de pings pode expirar.

c.  Alterne para o modo **Simulation** e repita o comando **ping 10.10.10.2**. Uma PDU aparece ao lado de **172.16.31.3**.

d.  Clique na PDU e observe a guia de informações a seguir:

·  No dispositivo: 172.16.31.3

·  Endereço MAC de origem: 0060.7036.2849

·  Endereço MAC de Destino: 00D0:BA8E:741A

·  Endereço IP Origem: 172.16.31.3

·  Endereço IP de Destino: 10.10.10.2

#### Pergunta:

Qual dispositivo e interface tem o endereço MAC de destino mostrado?

Área de Resposta

A interface do roteador FasteEthernet1/0

Ocultar resposta

e.  Clique em **Capture/Forward** (Capturar/Encaminhar) para mover a PDU para o próximo dispositivo. Colete as mesmas informações da Etapa 1d. Repita esse processo até que a PDU chegue ao seu destino. Registre as informações de PDU, que você coletou com o ping desde 172.16.31.5 para 10.10.10.2, em uma planilha usando um formato como o da tabela de amostra mostrada abaixo. Insira detalhes para ambas PDUs de entrada e saída no roteador.

||||||
|---|---|---|---|---|
||||||
||||||
||||||
||||||
||||||
||||||
||||||

||||||
|---|---|---|---|---|
||||||
||||||
||||||
||||||
||||||
||||||
||||||

Ocultar resposta

f.   Repita o processo para a mensagem echo-reply originada no host 10.10.10.2. Preencha a tabela referente a cada etapa.

||||||
|---|---|---|---|---|
||||||
||||||
||||||
||||||
||||||
||||||
||||||
||||||

||||||
|---|---|---|---|---|
||||||
||||||
||||||
||||||
||||||
||||||
||||||
||||||

Ocultar resposta

## Questões para Reflexão

Responda às perguntas a seguir sobre os dados capturados:

1.  Que diferentes tipos de cabos/mídia foram usados para conectar dispositivos?

Área de Resposta

cobre, fibra e sem fio

Ocultar resposta

2.  Os cabos mudaram o processamento das PDUs de alguma forma?

Área de Resposta

Não

Ocultar resposta

3.  O Wireless **Access Point** fez alguma coisa com as PDUs que recebeu?

Área de Resposta

Sim. Ele os reembalou como quadros 802.11 sem fio.

Ocultar resposta

4.  O endereçamento da PDU foi alterado pelo access point?

Área de Resposta

Não

Ocultar resposta

5.  Qual foi a camada OSI mais alta que o **Access Point** usou?

Área de Resposta

Camada 1

Ocultar resposta

6.  Em qual camada do modelo OSI os cabos e Access Points operam?

Área de Resposta

Camada 1

Ocultar resposta

7.  Ao examinar a guia **PDU Details** (Detalhes da PDU), qual endereço MAC apareceu primeiro: o Origem ou o Destino?

Área de Resposta

Destino

Ocultar resposta

8.  Às vezes, as PDUs eram marcadas com Xs vermelhos, enquanto outras tinham marcas de seleção verdes. Qual é o significado dessas marcações?

Área de Resposta

As PDUs marcadas com Xs não foram aceitas por um dispositivo porque o endereço de destino não corresponde ao endereço MAC do dispositivo.

Ocultar resposta

9.  Cada vez que a PDU foi enviada entre a rede 10 e a rede 172, havia um ponto em que os endereços MAC mudavam de repente. Onde isso aconteceu?

Área de Resposta

Ocorreu no roteador

Ocultar resposta

10.  Qual dispositivo usa endereços MAC que começam com 00D0:BA?

Área de Resposta

O roteador

Ocultar resposta

11.  A quais dispositivos os outros endereços MAC pertencem?

Área de Resposta

Para o dispositivo emissor e o dispositivo receptor

Ocultar resposta

12.  Os endereços IPv4 de envio e recebimento foram alterados em alguma das PDUs?

Área de Resposta

Não

Ocultar resposta

13.  Quando você acompanha a resposta a um ping, às vezes chamado de _pong_, o que acontece com os endereços de origem e destino?

Área de Resposta

Eles mudam porque o dispositivo receptor agora é a fonte.

Ocultar resposta

14.  Por que você acha que as interfaces do roteador fazem parte de duas redes IP diferentes?

Área de Resposta

A função de um roteador é interconectar diferentes redes IP. Deve ser um membro de ambas as redes para fazer isso.

Ocultar resposta

15.  Quais redes IP são conectadas pelo roteador?

Área de Resposta

As redes 10.10.10.0/24 e 172.16.31.0/24.

## 13.1.4 Verifique sua Compreensão - MAC e **IP**

**Verifique sua compreensão sobre endereçamento MAC e IP escolhendo a melhor resposta para as seguintes perguntas.**


### Pergunta 1

Qual endereço MAC de destino seria incluído em um quadro enviado de um dispositivo de origem para um dispositivo de destino na mesma rede local?

- [x] O endereço MAC do dispositivo de destino.
- [ ] O endereço MAC de broadcast FF-FF-FF-FF-FF-FF.
- [ ] O endereço MAC da interface do roteador local.

✅ RESPOSTA CORRETA: O endereço MAC do dispositivo de destino.

> Ao enviar um quadro para outro dispositivo na mesma rede local, o dispositivo que envia o quadro usará o endereço MAC do dispositivo de destino.

---

### Pergunta 2

Qual endereço MAC de destino seria incluído em um quadro enviado de um dispositivo de origem para um dispositivo de destino em uma rede local remota?

- [ ] O endereço MAC de broadcast FF-FF-FF-FF-FF-FF.
- [ ] O endereço MAC do dispositivo de destino.
- [x] O endereço MAC da interface do roteador local.

✅ RESPOSTA CORRETA: O endereço MAC da interface do roteador local.

> Ao enviar um quadro para outro dispositivo em uma rede remota, o dispositivo que envia o quadro usará o endereço MAC da interface do roteador local, que é o gateway padrão.

---

### Pergunta 3

Quais dois protocolos são usados para determinar o endereço MAC de um endereço IP de dispositivo de destino conhecido (IPv4 e IPv6)?

- [x] ARP
- [ ] DHCP
- [ ] DNS
- [x] ND

✅ RESPOSTA CORRETA: ARP, ND

> O Protocolo de Resolução de Endereços (Address Resolution Protocol - ARP) é usado para determinar o endereço MAC de um dispositivo com um endereço IPv4 de destino conhecido. Neighbor Discovery (ND) é usado para determinar o endereço MAC de um dispositivo com um endereço IPv6 de destino conhecido.


# 13.2 Contenção de Broadcast

## 13.2.1 Vídeo - O Broadcast Ethernet
![[13.2.1.mp4#subtitle=anexos/13.2.1.vtt]]
Neste vídeo, vamos dar uma olhada em uma transmissão Ethernet.

Uma transmissão Ethernet é quando o endereço MAC de destino é de 48 bits de um, ou em hexadecimal, todos os Fs. Olhando para a animação, temos H1 que irá enviar um broadcast para todos os outros dispositivos. Esta pode ser uma mensagem que seja preciso que todos os dispositivos em sua rede recebam.

Podemos ver que H1 envia o broadcast. Quando um switch recebe um broadcast Ethernet, ele inunda, ou encaminha, o quadro Ethernet para todas as portas, exceto a porta de entrada. O resultado é que todos os dispositivos na rede receberão a transmissão.

Se tivermos um roteador na rede, ele também receberá a transmissão. No entanto, o roteador não encaminhará o broadcast para outras redes.


## 13.2.2 Domínios de Broadcast

Quando um host recebe uma mensagem endereçada ao endereço de broadcast, ele aceita e processa a mensagem como se ela tivesse sido endereçada diretamente a ele. Quando um host envia uma mensagem de broadcast, os switches encaminham a mensagem para cada host conectado na mesma rede local. Por esse motivo, uma rede local (ou seja, uma rede com um ou mais switches Ethernet) também é conhecida como domínio de broadcast.

Se muitos hosts estiverem conectados ao mesmo domínio de broadcast, o tráfego de broadcast poderá ficar excessivo. O número de hosts e a quantidade de tráfego de rede que pode ser suportada na rede local são limitados pelos recursos dos switches usados para conectá-los. À medida que a rede cresce e mais hosts são adicionados, o tráfego de rede aumenta, inclusive o tráfego de broadcast. Para melhorar o desempenho, geralmente é necessário dividir uma rede local em várias redes (ou seja, domínios de broadcast), como mostrado na figura. Os roteadores são usados para dividir a rede em vários domínios de broadcast.

![[Pasted image 20260609200338.png]]

## 13.2.3 Comunicação na camada de Acesso

Em uma rede Ethernet local, uma NIC só aceitará um quadro se o endereço de destino for o endereço MAC de broadcast ou corresponder ao endereço MAC da NIC.

A maioria dos aplicativos de rede, entretanto, baseiam-se no endereço IP lógico de destino para identificar a localização de servidores e clientes. A figura ilustra o problema de um host emissor ter apenas o endereço IP lógico do host de destino. Como o host emissor determina o endereço MAC de destino a ser colocado no quadro?

O host emissor pode usar um protocolo IPv4 chamado ARP (Address Resolution Protocol) para descobrir o endereço MAC de qualquer host na mesma rede local. O IPv6 usa um método semelhante conhecido como Descoberta de Vizinhos (Neighbor Discovery).

![[Pasted image 20260609200356.png]]

## 13.2.4 Vídeo - ARP (Protocolo de Resolução de Endereços)

![[13.2.4.mp4#subtitle=anexos/13.2.4.vtt]]
Neste vídeo, vamos apresentar o ARP, Protocolo de Resolução de Endereço.

ARP é usado quando sabemos o endereço IPv4 para onde queremos enviar o pacote, mas o que não sabemos é o endereço MAC Ethernet do dispositivo.

Por exemplo, temos o PC 1, que deseja enviar um pacote para o destino com endereço IPv4 de 192.168.1.9, o servidor FTP. O PC 1 conhece o endereço IPv4 do servidor FTP, mas o que ele precisa saber é seu endereço MAC, porque ele precisa encapsular esse pacote IPv4 em um quadro Ethernet.

Então, o que o PC 1 faz é olhar primeiro em sua tabela ARP. Ele procura o endereço IPv4 de 192.168.1.9. Se o endereço não estiver em sua tabela ARP, ele enviará uma solicitação ARP.

A animação mostra o PC 1 enviando a solicitação ARP. Observe que a solicitação ARP é uma transmissão Ethernet. O que isso significa é que quando o switch recebe esta transmissão Ethernet — que é um endereço MAC de destino de todos os bits 1 — o switch irá inundar o broadcast Ethernet, a solicitação ARP, para todas as portas, exceto a porta de entrada.

O motivo da transmissão é que o PC 1 precisa saber quem nesta rede tem o endereço IPv4 192.168.1.9. Está dizendo: "Ei, todo mundo na minha rede, quem tiver 192.168.1.9 como seu endereço IPv4, por favor me responda com seu endereço MAC".

Então esta solicitação ARP vai para todos os dispositivos na rede, incluindo o roteador. Agora, quando o roteador recebe esta transmissão Ethernet, ele não a encaminhará para outras redes. Assim, a transmissão Ethernet, esta solicitação ARP, permanece nesta rede.

Como podemos ver, o pedido ARP vai para todos e o servidor FTP diz: "Ei, esse é o meu endereço IPv4 que você está procurando. Vou enviar-lhe uma resposta ARP com meu endereço MAC". Agora o PC 1 tem o endereço MAC Ethernet do servidor FTP em 192.168.1.9 e agora pode enviar esse pacote em um quadro Ethernet para o servidor FTP.


## 13.2.5 ARP

O ARP usa um processo de três etapas para descobrir e armazenar o endereço MAC de um host na rede local quando apenas o endereço IPv4 do host é conhecido.

1. O host remetente cria e envia um quadro destinado ao endereço MAC de broadcast. Incluído no quadro, está uma mensagem com o endereço IPv4 do host do destino a ser alcançado.
2. Cada host na rede recebe o quadro de broadcast e compara o endereço IPv4 na mensagem com o endereço IPv4 configurado. O host com o endereço IPv4 correspondente envia o endereço MAC de volta para o host emissor original.
3. O host emissor recebe a mensagem e armazena informações do endereço IPv4 e do endereço MAC em uma tabela chamada de tabela ARP.

Quando o host emissor tem o endereço MAC do host de destino em sua tabela ARP, ele pode enviar quadros diretamente ao destino sem fazer uma solicitação ARP. Como as mensagens ARP dependem de quadros de broadcast para entregar as solicitações, todos os hosts na rede IPv4 local devem estar no mesmo domínio de broadcast.

**Clique em Play na figura para ver uma animação do processo de ARP.**

![[brave_RNsZTLDpwv.mp4]]
## 13.2.6 Verifique sua compreensão - Contenção de broadcast

**Verifique sua compreensão sobre contenção de broadcast, escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

O endereço MAC de destino de um broadcast Ethernet em hexadecimal é:

- [ ] 48 dígitos F
- [ ] 1111.1111.1111
- [x] FFFF.FFFF.FFFF
- [ ] 48 bits iguais a 1

✅ RESPOSTA CORRETA: FFFF.FFFF.FFFF

> O endereço MAC de destino para um broadcast Ethernet é FFFF.FFFF.FFFF.

---

### Pergunta 2

Quando um switch Ethernet recebe um quadro que é broadcast, ele:

- [ ] Descarta o quadro.
- [x] Encaminha o quadro para todas as portas, exceto a porta de entrada.
- [ ] Encaminha o quadro para todas as portas, inclusive a porta de entrada.
- [ ] Encaminha o quadro apenas para portas que precisam do broadcast.

✅ RESPOSTA CORRETA: Encaminha o quadro para todas as portas, exceto a porta de entrada.

> Quando um switch Ethernet recebe um quadro broadcast, ele encaminhará o quadro para todas as portas, exceto à porta na qual o quadro foi recebido.

---
### Pergunta 3

O Host-A tem um quadro Ethernet para enviar ao Host-B na mesma rede. O Host-A conhece o endereço IP do Host-B, mas não o endereço MAC. Que mensagem o Host-A enviará para determinar o endereço MAC do Host B?

- [x] Solicitação ARP
- [ ] Broadcast ARP
- [ ] Resposta ARP
- [ ] Descoberta ARP

✅ RESPOSTA CORRETA: Solicitação ARP

> Um host enviará uma solicitação ARP para determinar o endereço MAC de outro dispositivo.

---

### Pergunta 4

Uma solicitação ARP é enviada como:

- [x] um broadcast, para que todos os dispositivos na mesma rede recebam.
- [ ] um broadcast, para que todos os dispositivos na rede e em outras redes recebam
- [ ] um unicast, onde apenas o dispositivo com o endereço IP adequado receba
- [ ] um unicast, para que somente o dispositivo com o endereço MAC adequado receba

✅ RESPOSTA CORRETA: um broadcast, para que todos os dispositivos na mesma rede recebam.

> Uma solicitação ARP é um broadcast, então todos os dispositivos na rede receberão.

---

### Pergunta 5

O Host-B recebe uma solicitação ARP. O Host-B retornará uma resposta ARP se:

- [ ] O endereço MAC na solicitação ARP corresponder ao seu próprio endereço MAC.
- [x] O endereço IP na solicitação ARP corresponder ao seu próprio endereço IP.
- [ ] Os endereços IP e MAC na solicitação ARP corresponderem a seus próprios endereços IP e MAC.

✅ RESPOSTA CORRETA: O endereço IP na solicitação ARP corresponder ao seu próprio endereço IP.

> Um host enviará uma resposta ARP se o endereço IP na solicitação ARP corresponder ao seu próprio endereço IP.

---

### Pergunta 6

O Host-A envia uma solicitação ARP e recebe uma resposta ARP do Host-B. O que está na resposta ARP que o Host-A não conhecia e que precisa para se comunicar com o Host-B?

- [x] Endereço MAC do host B
- [ ] Endereços IP e MAC do Host B
- [ ] Endereço IP do host B

✅ RESPOSTA CORRETA: Endereço MAC do host B

> Uma resposta ARP incluirá o endereço IP e MAC do host que enviou a resposta.

# 13.3 Resumo do processo de ARP

## 13.3.1 O que eu aprendi neste módulo?

### MAC e IP

Às vezes, um host deve enviar uma mensagem, mas ele só sabe o endereço IP do dispositivo de destino. O host precisa saber o endereço MAC desse dispositivo. O endereço MAC pode ser descoberto usando resolução de endereços. Dois endereços principais são atribuídos a um dispositivo em uma LAN Ethernet:

- **Endereço físico (o endereço MAC)** — Usado para comunicações de NIC para NIC na mesma rede Ethernet.
- **Endereço lógico (o endereço IP)** — Usado para enviar o pacote do dispositivo de origem para o dispositivo de destino. O endereço IP de destino pode estar na mesma rede IP que a origem ou pode estar em uma rede remota.

Quando o endereço IP de destino (IPv4 ou IPv6) estiver em uma rede remota, o endereço MAC de destino será o endereço do gateway padrão do host (ou seja, a interface do roteador). Os roteadores examinam o endereço IPv4 destino para determinar o melhor caminho para encaminhar o pacote IPv4. Quando o roteador recebe o quadro Ethernet, ele desencapsula as informações da Camada 2. Usando o endereço IPv4 de destino, ele determina o dispositivo do próximo salto e, em seguida, encapsula o pacote IPv4 em um novo quadro (da camada de enlace) para a interface de saída. Ao longo de cada link do caminho, um pacote IP é encapsulado em um quadro. O quadro é específico para a tecnologia do enlace associada a esse link, como Ethernet. Se o dispositivo do próximo salto for o destino final, o endereço MAC de destino será o da NIC Ethernet do dispositivo.

---

### Contenção de Broadcast

Uma mensagem pode conter apenas um endereço MAC de destino. A resolução de endereços permite que um host envie uma mensagem de broadcast para um endereço MAC exclusivo que é reconhecido por todos os hosts. O endereço MAC de broadcast é um endereço de 48 bits, com todos eles iguais a 1. Os endereços MAC geralmente são representados em notação hexadecimal. O endereço MAC de broadcast em notação hexadecimal é FFFF.FFFF.FFFF. Cada F em notação hexadecimal representa quatro uns em binário.

Quando um host envia uma mensagem de broadcast, os switches encaminham a mensagem para cada host conectado na mesma rede local. Por esse motivo, uma rede local (ou seja, uma rede com um ou mais switches Ethernet) também é conhecida como domínio de broadcast.

Se muitos hosts estiverem conectados ao mesmo domínio de broadcast, o tráfego de broadcast poderá ficar excessivo. O número de hosts e a quantidade de tráfego de rede que pode ser suportada na rede local são limitados pelos recursos dos switches usados para conectá-los. Para melhorar o desempenho, pode ser necessário dividir uma rede local em várias redes ou domínios de broadcast. Os roteadores são usados para dividir a rede em vários domínios de broadcast.

Em uma rede Ethernet local, uma NIC só aceitará um quadro se o endereço de destino for o endereço MAC de broadcast ou corresponder ao endereço MAC da NIC. A maioria dos aplicativos de rede depende do endereço IP de destino lógico para identificar a localização dos servidores e clientes. Como o host emissor determina o endereço MAC de destino a ser colocado no quadro? O host remetente pode fazer uma consulta ARP para descobrir o endereço MAC de qualquer host na mesma rede local.

O ARP usa um processo de três etapas para descobrir e armazenar o endereço MAC de um host da rede local, quando apenas o endereço IPv4 do host é conhecido:

1. O host remetente cria e envia um quadro destinado ao endereço MAC de broadcast. Incluído no quadro, está uma mensagem com o endereço IPv4 do host do destino a ser alcançado.
2. Cada host na rede recebe o quadro de broadcast e compara o endereço IPv4 na mensagem com o endereço IPv4 configurado. O host com o endereço IPv4 correspondente envia o endereço MAC de volta para o host emissor original.
3. O host emissor recebe a mensagem e armazena informações do endereço IPv4 e do endereço MAC em uma tabela chamada de tabela ARP.

O IPv6 usa um método semelhante conhecido como Descoberta de vizinhos ( Neighbor Discovery).


## 13.3.2 Webster — Questões para Reflexão

Todos os meus dispositivos (e todos os seus dispositivos) têm um endereço IP e um endereço MAC. Quando alguém deseja enviar uma mensagem para o meu telefone, meu endereço IP informa, ao roteador dele, onde está meu dispositivo. Meu endereço MAC é como meu telefone é conhecido, para me deixar ver a mensagem. Esse roteador também precisa saber meu endereço MAC e usa o ARP para encontrá-lo. Você sabe como procurar o endereço MAC de cada um dos seus dispositivos conectados?

