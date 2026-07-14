
# 12.0 Introdução

## 12.0.1 Webster — Por que devo fazer este módulo?

Kishori recebe um e-mail de Rina perguntando se elas podem se encontrar no refeitório para o almoço. Kishori conhece Rina e está ansiosa para lhe fazer mais algumas perguntas sobre redes. Rina está sempre feliz em compartilhar seu conhecimento. Quando Kishori estava conversando com Madhav, ela soube que seu departamento faz parte de uma LAN. Cada departamento dentro do hospital tem sua própria LAN. Kishori pergunta a Rina como ela consegue enviar e receber e-mails que estão fora de sua rede. Rina explica que os gateways e a Tradução de Endereço de Rede (NAT) possibilitam tudo isso. Rina está impressionada com o novo conhecimento e o interesse de Kishori pelas redes! Ela cita que há vários enfermeiros no hospital que têm esse conhecimento e recebem mais por serem capazes de solucionar os problemas dos aparelhos no quarto do paciente. Ela recomenda que Kishori faça alguns cursos para que ela possa se candidatar a essa promoção. Uau! Quem diria que os enfermeiros podem ser promovidos aprendendo tecnologia!

Este módulo ajudará a Kishori a entender gateways e NAT. Você quer saber mais? Vamos lá!

## 12.0.2 O que vou aprender neste módulo?

**Título do módulo:** Gateways para outras redes

**Objetivo do módulo:** Explicar como os roteadores conectam as redes.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Limites de rede|Descrever os limites da rede.|
|Tradução de Endereço de Rede|Explicar o propósito de Tradução de Endereço de Rede em redes pequenas.|

# 12.1 Limites de rede

## 12.1.1 Vídeo - Gateways para outras redes
![[12.1.1.mp4#subtitle=anexos/12.1.1.vtt]]
Nesta lição, falarei sobre gateways e, em particular, gateways padrão.

Então, o que é um gateway? Um gateway, como a palavra indica, é uma maneira de o tráfego sair de uma rede local e ser encaminhado para outras redes remotas. Basicamente, pense no gateway padrão como a porta para fora da sala. Se eu quiser sair para o corredor, vou ter que sair pela porta. Quando um computador deseja enviar uma mensagem de sua rede local, precisa também sair de sua rede local e ser encaminhado para o destino real.

Como aprendemos anteriormente, os computadores descobrem se um destino está ou não em sua rede local passando por um processo de binário ANDing, que leva a máscara de sub-rede e faz um AND com o endereço IP de destino para determinar se a parte de rede do endereço é exatamente igual à parte da rede do host de envio. Então, no caso disso não ser verdade, o computador precisa realmente enviar o pacote para o gateway.

Aprendemos que todo host em uma rede precisa ter, no mínimo, um endereço IP e uma máscara de sub-rede. Agora, se esse host pretende falar com destinos que não estão em sua rede local, também tem que ser configurado com o endereço de seu gateway padrão.

Normalmente na rede de hoje, o gateway padrão configurado em um dispositivo é a interface do roteador que o tráfego chegaria em primeiro lugar em seu caminho para a internet. Então, basicamente, no departamento de gerenciamento de rede, se estivesse tentando acessar um servidor que está fora na internet, o tráfego viajaria através do switch e terminaria no endereço atribuído à interface do roteador mais próxima no caminho para a internet.

Agora, se formos para um host diferente — digamos, por exemplo, um no departamento de contabilidade — e eles estivessem tentando acessar exatamente o mesmo servidor, seu tráfego passaria novamente pelo switch, mas entraria no roteador em uma interface do roteador diferente. Portanto, o gateway padrão configurado em hosts no departamento de contabilidade é diferente do gateway padrão configurado no departamento de gerenciamento de rede.

Uma vez que o host determina que o endereço do destino não está na mesma rede local, o que ele faz é enviar ARPs para o endereço MAC do gateway padrão. Agora, isso é importante lembrar, porque um dos problemas que você encontra em redes com frequência é que um erro pode ser cometido e o endereço de gateway padrão não está na mesma rede local. Por exemplo, se acidentalmente fosse configurado com 11 em vez de um, o computador não seria capaz de enviar tráfego usando ARP para seu endereço de gateway padrão.

Então temos que ter muito cuidado quando estamos definindo as configurações de rede: temos que ter o endereço IP correto, as máscaras de sub-rede corretas, para que o computador possa prever com precisão quem está em sua própria rede local e quem está fora da rede local localizado em uma rede remota, e o endereço de gateway padrão para que ele saiba para qual roteador enviar tráfego para fora de sua própria rede local.

## 12.1.2 Roteadores como Gateways

O roteador fornece um gateway pelo qual os hosts de uma rede podem se comunicar com hosts de diferentes redes. Cada interface em um roteador está conectada a uma rede separada.

O endereço IPv4 atribuído à interface identifica a rede local que está diretamente conectada a ele.

Todo host de uma rede deve usar o roteador como um gateway para outras redes. Portanto, cada host deve conhecer o endereço IPv4 da interface do roteador conectada à rede na qual o host está conectado. Esse endereço é conhecido como endereço de gateway padrão. Ele pode ser configurado estaticamente no host ou recebido dinamicamente por DHCP.

Quando um roteador sem fio está configurado para ser um servidor DHCP da rede local, ele envia automaticamente o endereço IPv4 correto da interface para os hosts como o endereço de gateway padrão. Dessa forma, todos os hosts na rede podem usar o endereço IPv4 para encaminhar mensagens aos hosts localizados no ISP e obter acesso a hosts na Internet. Os roteadores sem fio geralmente são definidos para serem servidores DHCP por padrão.

O endereço IPv4 dessa interface do roteador local passa a ser o endereço de gateway padrão para a configuração do host. O gateway padrão é fornecido estaticamente ou por DHCP.

Quando um roteador sem fio está configurado como servidor DHCP, ele fornece seu próprio endereço IPv4 interno como gateway padrão aos clientes DHCP. Também fornece a eles seu endereço IPv4 e sua máscara de sub-rede, como mostrado na figura.

![[Pasted image 20260609083223.png]]

## 12.1.3 Roteadores como limites entre redes

O roteador sem fio atua como servidor DHCP para todos os hosts locais conectados a ele, por cabo de Ethernet ou sem fio. Esses hosts locais estão localizados em uma rede interna. A maioria dos servidores DHCP são configurados para atribuir endereços privados aos hosts na rede interna, em vez de endereços públicos roteáveis da Internet. Isso garante que, por padrão, a rede interna não possa ser acessada diretamente da Internet.

O endereço IPv4 padrão configurado na interface do roteador local sem fio geralmente é o primeiro endereço de host naquela rede. Os hosts internos devem receber endereços dentro da mesma rede do roteador sem fio, sejam eles configurados estaticamente ou através do DHCP. Quando configurado como um servidor DHCP, o roteador sem fio fornece endereços nesse intervalo. Ele também fornece informações de máscara de sub-rede e seu próprio endereço IPv4 da interface como gateway padrão, como mostrado na figura.

Muitos ISPs usam o servidor DHCP para fornecer endereços IPv4 do lado de Internet do roteador sem fio localizado nas instalações de clientes. A rede atribuída ao lado de Internet do roteador sem fio é conhecida como rede externa.

Quando um roteador sem fio está conectado a um ISP, ele atua como um cliente DHCP para receber o endereço IPv4 correto de rede externa para a interface de Internet. Os ISPs normalmente fornecem um endereço roteável pela Internet, o que permite que os hosts conectados ao roteador sem fio tenham acesso à Internet.

O roteador sem fio serve como limite entre a rede interna local e a Internet externa.

![[Pasted image 20260609083239.png]]

## 12.1.4 Verifique a sua compreensão - Limites da rede

**Verifique sua compreensão sobre Limites da rede escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Para dois hosts que estão na mesma rede, quais das seguintes afirmações são verdadeiras? (Escolha três.)

- [ ] Ambos os hosts terão os diferentes endereços de gateway padrão.
- [x] Ambos os hosts terão endereços IP diferentes.
- [x] Ambos os hosts terão o mesmo endereço de gateway padrão.
- [ ] Ambos os hosts terão o mesmo endereço IP.
- [x] Ambos os hosts terão diferentes endereços MAC.
- [ ] Ambos os hosts terão o mesmo endereço MAC.

✅ RESPOSTA CORRETA: Ambos os hosts terão endereços IP diferentes, Ambos os hosts terão o mesmo endereço de gateway padrão, Ambos os hosts terão diferentes endereços MAC.

> Os hosts normalmente sempre terão diferentes endereços IP e MAC. No entanto, os hosts na mesma rede usarão o mesmo endereço de gateway padrão. Um host em outra rede usaria um endereço de gateway padrão diferente.

---

### Pergunta 2

Para dois hosts, cada um em uma rede diferente, quais das afirmações a seguir são verdadeiras? (Escolha três.)

- [ ] Ambos os hosts terão o mesmo endereço MAC.
- [ ] Ambos os hosts terão o mesmo endereço de gateway padrão.
- [ ] Ambos os hosts terão o mesmo endereço IP.
- [x] Ambos os hosts terão os diferentes endereços de gateway padrão.
- [x] Ambos os hosts terão diferentes endereços MAC.
- [x] Ambos os hosts terão endereços IP diferentes.

✅ RESPOSTA CORRETA: Ambos os hosts terão os diferentes endereços de gateway padrão, Ambos os hosts terão diferentes endereços MAC, Ambos os hosts terão endereços IP diferentes.

> Os hosts normalmente sempre terão diferentes endereços IP e MAC. No entanto, os hosts na mesma rede usarão o mesmo endereço de gateway padrão. Um host em outra rede usaria um endereço de gateway padrão diferente.


# 12.2 Tradução de Endereço de Rede (NAT)

## 12.2.1 Vídeo - Introdução ao NAT
![[12.2.1.mp4#subtitle=anexos/12.2.1.vtt]]
Nesta aula vamos conversar sobre como o DHCP funciona.

Anteriormente, você aprendeu que as atribuições de endereço IP podem ser atribuídas de duas maneiras: estaticamente, significando que alguém realmente se senta e configura o endereço IP, ou dinamicamente, onde o dispositivo obtém seu endereço de um servidor DHCP.

DHCP significa protocolo de configuração de host dinâmico. Então, como funciona esse protocolo? O protocolo descreve um conjunto de mensagens que vão entre o host que deseja um endereço IP e o servidor DHCP que fornece o endereço IP.

Basicamente, o que temos é um sistema host que envia um pacote chamado **descoberta de DHCP**. O que este pacote está fazendo é procurar por um servidor DHCP. O pacote é um pacote de broadcast, e contém o endereço MAC do dispositivo solicitando o endereço IP, e é destinado para qualquer dispositivo na rede que esteja configurado para ser um servidor DHCP.

Que tipo de dispositivos podem ser servidores DHCP? Normalmente, em uma rede doméstica, o roteador doméstico — o roteador sem fio ou o roteador com fio — está configurado para fornecer DHCP. Em ambientes maiores, muitas vezes este é um servidor que estaria fazendo outras funções, como o controle de domínio da Microsoft, ou pode ser um servidor Linux que também funciona como um servidor web. Então, basicamente, o servidor DHCP pode ser um número de diferentes tipos de dispositivos.

Quando a descoberta DHCP sai, uma vez que é um broadcast, qualquer servidor DHCP conectado à rede vai ouvir isso. O servidor DHCP então responde com uma **oferta DHCP**.

O pacote de oferta DHCP contém um endereço IP que o host, o dispositivo individual, poderia usar, se aceitar. Quando o host recebe o pacote de oferta DHCP do servidor DHCP, este contém o endereço IP que foi enviado, a máscara de sub-rede, bem como o endereço de gateway padrão.

Uma vez que o host recebe isso, ele envia de volta um pacote de **solicitação DHCP** que aceitará a oferta, e solicitará o endereço IP que o servidor enviou, 192.168.1.15. O dispositivo irá então levar esta informação e inseri-la em suas configurações de endereço IP.

E nesse momento, uma vez que o servidor recebe a solicitação DHCP, o servidor enviará de volta uma **confirmação de DHCP** que indicará ao host que o servidor está colocando este endereço IP em sua tabela associada ao endereço MAC que foi enviado pelo host.

## 12.2.2 Packet Tracer – Examinando o NAT em um roteador sem fio

Nesta atividade, você completará os seguintes objetivos:

- Examinar a configuração da NAT em um roteador sem fio
- Configurar 4 PCs para que se conectem a um roteador sem fio com DHCP
- Examinar o tráfego que cruza a rede usando NAT


### Packet Tracer – Examinando o NAT em um roteador sem fio (wireless router)

## Objetivos

- Examinar a configuração do NAT em um roteador sem fio

- Configurar 4 PCs para que se conectem a um roteador sem fio com DHCP

- Examinar o tráfego que cruza a rede usando NAT

## Instruções

## Parte 1: Examine a configuração para acessar a rede externa.

a.   Adicione 1 PC e conecte-o ao roteador wireless com um cabo direto. Aguarde que todas as luzes dos links fiquem verdes antes de passar para a próxima etapa ou clique em **Fast Forward**.

b.   No PC, clique em **Desktop**. Selecione **IP Configuration**. Clique em **DHCP** para permitir que cada dispositivo receba um endereço IP através do DHCP no roteador sem fio.

c.   Anote o endereço IP do gateway padrão. Feche a janela **IP Configuration** ao terminar.

d.   Navegue   até o  web browser e insira o endereço IP do gateway padrão no campo URL. Entre com username **admin** e password **admin** quando solicitado.

e.  Clique na opção do menu **Status** no canto superior direito. Quando essa opção estiver selecionada, a página do sub-menu Router é exibida.

f.   Role a página do roteador para baixo para ver a opção Internet connection . O endereço IP atribuído aqui é o atribuído pelo ISP. Se não houver nenhum endereço IP (0.0.0.0 é exibido), feche a janela, aguarde alguns segundos e tente novamente. O roteador sem fio está no processo de obtenção de endereço IP do servidor DHCP do ISP.

O endereço visto aqui é o endereço atribuído à porta Internet no roteador wireless.

#### Pergunta:

Ele é um endereço público ou privado?

Área de Resposta

Endereço IP público

Ocultar resposta

## Parte 2: Examine as configurações para acessar a rede externa.

a.  Clique em **Local Network** na barra do sub-menu Status.

b.  Role para baixo e examine as informações da Rede Local. Este é o endereço atribuído para a rede interna.

c.  Role mais para baixo e examine as informações do servidor DHCP e a faixa dos endereços IP que podem ser atribuídos para conectar hosts.

#### Pergunta:

Esses endereços são públicos ou privados?

Área de Resposta

Endereço IP privado

Ocultar resposta

d.  Feche a janela de configuração do roteador sem fio.

## Parte 3: Conecte 3 PCs ao roteador sem fio.

a.  Adicione mais 3 PCs e conecte-os ao roteador wireless com cabos diretos. Aguarde que todas as luzes dos links fiquem verdes antes de passar para a próxima etapa ou clique em **Fast Forward**.

b.  Em cada PC, clique em **Desktop**. Selecione IP **Configuration**. Clique em **DHCP** para permitir que cada dispositivo receba um endereço IP através do DHCP no roteador sem fio. Feche a janela **IP Configuration** ao terminar.

c.  Clique em **Command Prompt** para verificar a configuração IP de cada dispositivo usando o comando **ipconfig /all.**

**Observação**: esses dispositivos receberão um endereço privado. Endereços privados não conseguem cruzar a Internet, portanto, a tradução NAT deve ocorrer.

## Parte 4: Visualize a tradução NAT no roteador sem fio.

a.  Entre no Modo de Simulação ao clicar na guia Simulation no canto inferior direito. O botão Simulation está localizada ao lado do botão Realtime e possui um símbolo de cronômetro.

b.   Visualize   o tráfego ao criar uma PDU complexa no Simulation mode.

1)  A partir do Simulation Panel, clique **Show All/None** para alterar eventos visualizáveis para nenhum. Agora, clique em **Edit Filters**, e na guia **Misc**, marque as caixas **TCP** e **HTTP**. Feche a janela quando terminar.

2)  Adicione uma PDU Complexa clicando no envelope aberto localizado no menu superior.

3)  Clique em um dos PCs para especificá-lo como a origem.

c.  Especifique as configurações de PDU complexa ao alterar o seguinte na janela de PDU complexa:

1)  Em **PDU Settings** > Select Application deve estar setado para: **HTTP**.

2)  Clique no servidor **ciscolearn.nat.com** para especificá-lo como o dispositivo de destino.

3)  Em Source Port, insira **1000**.

4)  Em Simulation Settings, selecione **Periodic**. Defina **120** segundos como o Interval.

5)  Clique **Create PDU** na janela Create Complex PDU.

d.  Clique duas vezes em simulation panel para destacá-lo da janela PT. Isso permite mover o painel de simulação para visualizar toda a topologia da rede.

e.  Observe o fluxo de tráfego clicando em **Play** no simulation panel. Acelere a animação movendo o controle deslizante de reprodução para a direita.

**Observação**: clique em **View Previous Events** quando a mensagem de Buffer cheio for exibida.

## Parte 5: Visualize as informações de cabeçalho dos pacotes que trafegaram através da rede.

a.  Examine os cabeçalhos dos pacotes enviados entre um PC e o servidor da Web.

1)  No Painel de Simulação, clique duas vezes na terceira linha de baixo na lista de eventos. Essa ação exibirá um envelope na área de trabalho representando essa linha.

2)  Clique no envelope na janela da área de trabalho para visualizar as informações do pacote e do cabeçalho.

b.  Clique na guia Detalhes da PDU de Entrada (Inbound) Examine as informações de endereço IP de origem (SRC) e o endereço IP de destino do pacote.

c.  Clique na guia Detalhes da PDU de Saída (Outbound) Examine as informações de endereço IP de origem (SRC) e o endereço IP de destino do pacote.

Observe a alteração no endereço IP SRC.

d.  Clique em outras linhas de evento para visualizar os cabeçalhos durante o processo.

e.  Quando terminar, clique em Check Results para verificar seu trabalho.


# 12.3 Resumo: Gateways para Outras Redes

## 12.3.1 O que aprendi neste módulo?

### Limites de rede

Todo host de uma rede deve usar o roteador como um gateway para outras redes. Portanto, cada host deve conhecer o endereço IPv4 da interface do roteador conectada à rede na qual o host está conectado. Esse endereço é conhecido como endereço de gateway padrão. Ele pode ser configurado estaticamente no host ou recebido dinamicamente por DHCP.

O roteador sem fio atua como servidor DHCP para todos os hosts locais conectados a ele, por cabo de Ethernet ou sem fio. Esses hosts locais estão localizados em uma rede interna. Quando um roteador sem fio está conectado a um ISP, ele atua como um cliente DHCP para receber o endereço IPv4 correto de rede externa para a interface de Internet. Os ISPs normalmente fornecem um endereço roteável pela Internet, o que permite que os hosts conectados ao roteador sem fio tenham acesso à Internet. O roteador sem fio serve como limite entre a rede interna local e a Internet externa.

---

### Operação NAT

O roteador sem fio recebe um endereço público do ISP, que permite que ele envie e receba pacotes pela internet. Ele, por sua vez, fornece endereços privados para clientes da rede local.

O processo usado para converter endereços privados em endereços roteáveis pela Internet é chamado de NAT. Com o NAT, um endereço IPv4 de origem privado (local) é convertido em um endereço público (global). O processo é o inverso para pacotes que chegam. Usando NAT, o roteador sem fio é capaz de converter vários endereços IPv4 internos no mesmo endereço público.

Só precisam ser convertidos pacotes destinados para outras redes. Esses pacotes devem passar pelo gateway. Nele, o roteador sem fio substitui o endereço IPv4 privado do host de origem pelo seu próprio endereço IPv4 público.


## 12.3.2 Webster — Questões para Reflexão

Acontece que os endereços IPv4 nos dispositivos na minha rede doméstica são endereços privados que são usados apenas na minha LAN. Mas se eu precisar me aventurar além da minha rede doméstica, talvez acessar a Internet ou enviar um e-mail para alguém fora da minha rede, meu dispositivo precisará receber um endereço público. Como o roteador sabe se você está tentando obter acesso a um dispositivo ou site que esteja fora da LAN? Como você sabe que seu endereço privado foi traduzido para um endereço público?