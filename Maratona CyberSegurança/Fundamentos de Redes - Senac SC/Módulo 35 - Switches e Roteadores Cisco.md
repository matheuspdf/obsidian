# 35.0 Introdução

## 35.0.1 Webster - Por que devo fazer este módulo?

Estou de volta! Halimah me contou que recebeu sua primeira missão. Ela ajudará a projetar e configurar uma nova rede de filiais. Ela está muito animada com essa oportunidade!

Se eu tivesse essa tarefa, não sei se saberia por onde começar. Eu sei sobre os dispositivos e a mídia necessários e sobre os esquemas de endereçamento. Mas nunca configurei um switch, muito menos mais de um switch. Configurei meu roteador de rede doméstica, mas um roteador corporativo é provavelmente um pouco mais complexo.

Acho que esse módulo é exatamente o que preciso. E você?

## 35.0.2 O que vou aprender neste módulo?

**Título do módulo:** Switches e roteadores Cisco

**Objetivo do módulo:** Descrever roteadores e switches Cisco.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Switches Cisco|Descrever switches LAN Cisco.|
|Métodos de encaminhamento e velocidades de switches|Descrever os métodos de encaminhamento de switch e as configurações da porta disponíveis nas portas de switch de Camada 2.|
|Processo de inicialização do switch|Descrever o processo de inicialização do switch de LAN da Cisco.|
|Roteadores Cisco|Descrever os roteadores da Cisco para empresas de pequeno porte.|
|Processo de inicialização do roteador|Descrever o processo de inicialização do roteador da Cisco.|

# 35.1 Switches Cisco

## 35.1.1 Conectar mais dispositivos

As redes residenciais e de pequenas empresas geralmente não exigem mais de um ou dois dispositivos de rede para funcionarem com eficiência. Um roteador sem fio, equipado com conexões sem fio e algumas conexões cabeadas, é o único equipamento de rede necessário para oferecer conectividade suficiente para um grupo pequeno de usuários. Esses roteadores são configurados através de um navegador da Web e têm uma interface gráfica do usuário (GUI) de fácil utilização que orienta você pelos itens de configuração mais comuns.

Os roteadores sem fio que são elaborados basicamente para uso doméstico não são apropriados para a maioria das redes empresariais, que devem comportar mais usuários. As redes modernas usam vários dispositivos de conectividade. Cada dispositivo tem recursos para controlar o fluxo de dados através de uma rede. A regra geral é a seguinte: quanto mais alto estiver o dispositivo no modelo OSI, mais inteligente ele será. Isso significa que um dispositivo de nível mais alto pode analisar melhor o tráfego de dados e desviá-lo de acordo com as informações que não estão disponíveis em camadas inferiores. Por exemplo, um switch de Camada 2 pode filtrar os dados e enviá-los apenas pela porta conectada ao destino, com base no endereço MAC.

À medida que os switches e os roteadores evoluem, a distinção entre eles pode parecer tênue. Uma distinção simples permanece: os switches LAN proporcionam conectividade nas redes locais da empresa, enquanto os roteadores interconectam redes locais e são necessários em um ambiente de rede de longa distância (WAN). Ou seja, um switch é usado para conectar dispositivos na mesma rede. Um roteador serve para conectar várias redes entre si.

**Clique abaixo para ver exemplos de switches e roteadores Cisco.**

### Switches Cisco Catalyst 9300 Series
![[Pasted image 20260630214539.png]]

### Roteadores Cisco Serie 4300
![[Pasted image 20260630214548.png]]

Além dos switches e roteadores, há outras opções de conectividade disponíveis para LANs. Os pontos de acesso sem fio que são implantados em empresas permitem que computadores e outros dispositivos, como telefones IP, estabeleçam uma conexão sem fio à rede ou compartilhem a conectividade de banda larga. Os firewalls protegem contra ameaças de rede e fornecem segurança, controle de rede e contenção.

## 35.1.2 Switches Cisco LAN

Quando uma rede LAN aumenta até o ponto onde as quatro portas Ethernet fornecidas pelo roteador sem fio não são suficientes para todos os dispositivos que precisam se conectar à rede com fio, é hora de adicionar um switch LAN à rede. Um switch pode fornecer conectividade na camada de acesso de uma rede, conectando dispositivos a uma LAN. Um switch pode permitir que a rede cresça sem substituir os dispositivos centrais. Ao escolher um switch, há vários fatores a serem considerados, incluindo os seguintes:

- Tipo de portas
- Velocidade necessária
- Capacidade de expansão
- Capacidade de gerenciamento

**Clique em cada fator abaixo para obter mais informações.**

### **Tipo de portas**

Ao selecionar um switch para a LAN, é essencial escolher o número e o tipo apropriados de portas. A maioria dos switches mais baratos são compatíveis apenas com as portas de interface de par trançado de cobre. Os switches mais caros podem ter conexões de fibra óptica. Esses são utilizados para conectar o switch a outros switches mais distantes O Cisco Catalyst 9300 series tem uma variedade de opções dependendo do seu ambiente.
![[Pasted image 20260630214619.png]]

### **Velocidade necessária**

As interfaces de par trançado Ethernet em um switch têm velocidades definidas. Uma porta Ethernet 10/100 só pode funcionar a 10 megabits por segundo (Mbps) ou a 100 Mbps. Isso significa que se o dispositivo que você está conectando à porta de interface de switch 10/100 puder se conectar a velocidades de gigabit, a velocidade máxima na qual ele poderá se comunicar será 100 Mbps. Os switches também podem incluir portas Ethernet Gigabit. Se a conexão com a Internet for superior a 100 Mbps, uma porta gigabit será necessária para aproveitar a largura de banda de Internet mais alta. Portas Ethernet Gigabit também funcionarão a 10/100 Mbps. Às vezes, a Ethernet Gigabit é representada como 1000 Mbps. O switch Cisco Catalyst 9300 48S na figura tem duas portas de uplink de 40 Gbps para fornecer um caminho rápido para que as 48 portas acessem o resto da rede e da Internet.

Semelhantes a uma porta de switch, as NICs Ethernet operam em larguras de banda específicas, como 10/100 ou de 10/100/1000 Mbps. A largura de banda real do dispositivo conectado será a largura de banda comum mais alta entre a NIC do dispositivo e a porta do switch.
![[Pasted image 20260630214632.png]]


### **Expansibilidade**

Os dispositivos de rede são fornecidos tanto em configurações físicas fixas quanto modulares. As configurações fixas têm número e tipo específicos de portas ou interfaces. Os dispositivos modulares têm slots de expansão que oferecem flexibilidade para a adição de novos módulos, conforme necessário. A figura mostra um chassi Cisco Catalyst 9600 no qual é possível instalar diferentes configurações de hardware para lidar com seu ambiente específico.
![[Pasted image 20260630214643.png]]


### **Capacidade de gerenciamento**

Muitos switches básicos baratos não são configuráveis. Um switch gerenciado que usa um sistema operacional da Cisco permite o controle de portas individuais ou do switch como um todo. Os controles podem alterar as configurações de um dispositivo, adicionar segurança de porta e monitorar o desempenho. O administrador de rede na figura está se conectando diretamente a um switch Cisco Catalyst usando um cabo console.


## 35.1.3 Vídeo - Componentes de um Switch LAN - Parte 1

**Selecione o botão Reproduzir para assistir o vídeo.**

Neste vídeo, vamos dar uma olhada nos componentes de um switch Ethernet.

Atrás do switch, temos o cabo de alimentação que se conecta à fonte de alimentação. Na frente, temos algumas luzes. Essas são os LEDs do sistema, informam se temos energia no switch e algumas outras informações de status.

Temos algumas portas por aqui, que são as portas Ethernet. É aqui que conectamos os sistemas de usuário final, os computadores e os laptops. Aqui conectamos roteadores ao switch, podemos conectar outro switch a esse switch, impressoras, etc.

Por aqui, no canto, temos o que é conhecido como a porta de console. Então, conectado ao meu computador, tenho o que é conhecido como um cabo de console ou um cabo rollover. Este cabo aqui está conectado à porta USB do meu computador. Antigamente, costumávamos conectar esses cabos em portas seriais, então eu tenho um conversor USB para serial que conecta o cabo de rollover à minha porta USB.

E tudo o que preciso fazer é conectar esse cabo de console na porta do console. Isso permitirá que eu faça a configuração inicial do switch, ou quando quiser configurar o switch, sem precisar de qualquer tipo de acesso à rede. Apenas o acesso físico ao switch permite configurar o switch.

## 35.1.4 Vídeo - Componentes de um Switch LAN - Parte 2

**Selecione o botão Reproduzir para assistir o vídeo.**

Neste vídeo, vamos observar como configurar inicialmente o switch, ou quando temos acesso físico ao switch, para configurá-lo.

Então, eu tenho minha máquina Windows 10 aqui, e eu estou rodando um software chamado Tera Term. É conhecido como um software de emulação de terminal. Existem outros disponíveis, mas vou usar o Tera Term. Então, eu já estou fisicamente conectado ao switch, usando o cabo USB conectado ao cabo serial rollover, conectado à porta de console do switch.

Vou seguir em frente e clicar duas vezes em Tera Term. Então, eu vou escolher a conexão serial. E como estou usando minha porta USB, escolherei COM3, conexão de porta de comunicação USB para Serial, e clicar em Ok. Agora, para que possamos ver isso um pouco mais fácil, vou passar aqui para Setup, Fonte, para ter certeza de que podemos ver isso um pouco mais fácil.

Agora observe que não estou vendo nenhum tipo de prompt. Bem, isso porque o switch já inicializou e está esperando por algum tipo de interação minha. Na verdade, ele já forneceu saída, mas ainda não o vi porque o Tera Term não havia iniciado. Então, vou pressionar Enter.

Ele diz: "Deseja entrar na caixa de diálogo de configuração inicial?" Sempre diga não a isso. Se você responder que sim, isso fará uma série de perguntas que, para ser sincero, vai confundir você. Usar a interface de linha de comando é muito mais fácil para configurar o switch ou o roteador. Então, vou digitar `n` para não. Se você digitar acidentalmente sim ou começar a fazer isso, e você decidir que quer sair desse modo, basta pressionar `Ctrl C`.

Como podem ver, estou agora no prompt do switch com o símbolo `>`. Estou agora no Cisco IOS Internetwork Operating System, linha de comando do sistema operacional, e posso começar a configurar o switch neste momento.


## 35.1.5 Componentes do switch LAN

O switch Cisco Catalyst 9300 mostrado na figura é adequado para redes de pequeno e médio porte. Ele fornece 24 portas de dados de 1 Gbps com Power over Ethernet (PoE) para que alguns tipos de dispositivos possam ser alimentados diretamente pelo switch. Ele também tem duas portas de uplink modulares de 40 Gbps. Os LEDs indicam o status da porta e do sistema para o switch. O switch tem uma porta de console e uma de armazenamento para gerenciamento de dispositivos.

### Switch Cisco Catalyst 9300 24 UPOE

![[Pasted image 20260630214902.png]]


## 35.1.6 Verifique sua compreensão - Switches Cisco

**Verifique sua compreensão sobre switches Cisco escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Verdadeiro ou falso? Quanto mais baixo o dispositivo estiver no modelo OSI, mais inteligente ele será.

- [ ] verdadeiro
- [x] falso

✅ RESPOSTA CORRETA: falso

> A resposta correta é falsa. Quanto mais alto o dispositivo estiver no modelo OSI, mais inteligente ele será. Um dispositivo de nível mais alto pode analisar melhor o tráfego de dados e encaminhá-lo baseado em informações não disponíveis em camadas inferiores.

---

### Pergunta 2

Verdadeiro ou falso? Os switches normalmente oferecem conectividade LAN e os roteadores interconectam redes locais.

- [x] verdadeiro
- [ ] falso

✅ RESPOSTA CORRETA: verdadeiro

> A resposta correta é verdadeira. Um switch é usado para conectar dispositivos na mesma rede. Um roteador serve para conectar várias redes entre si.

---

### Pergunta 3

Qual fator de seleção de switch você normalmente considera ao decidir que deseja que o switch seja configurável?

- [ ] Capacidade de expansão
- [x] Gerenciabilidade
- [ ] Tipo de portas
- [ ] Velocidade necessária

✅ RESPOSTA CORRETA: Gerenciabilidade

> A capacidade de gerenciamento depende da seleção de um switch que possa ser configurado.

---

### Pergunta 4

Qual fator de seleção de switch você normalmente considera ao decidir sobre o tipo de portas de uplink?

- [ ] Capacidade de expansão
- [ ] Gerenciabilidade
- [ ] Tipo de portas
- [x] Velocidade necessária

✅ RESPOSTA CORRETA: Velocidade necessária

> A velocidade necessária para o switch incluirá uma determinação da velocidade das portas de uplink.

---

### Pergunta 5

Qual fator de seleção de switch você normalmente considera ao decidir sobre interfaces que suportam conexões de par trançado?

- [ ] Velocidade necessária
- [x] Tipo de portas
- [ ] Gerenciabilidade
- [ ] Capacidade de expansão

✅ RESPOSTA CORRETA: Tipo de portas

> O tipo de porta usada para acesso com fio à LAN normalmente será a Ethernet de par trançado. Você também deve considerar o número de portas necessárias.

---

### Pergunta 6

Qual fator de seleção de switch você normalmente considera ao decidir entre configurações modulares ou fixas?

- [x] Capacidade de expansão
- [ ] Gerenciabilidade
- [ ] Tipo de portas
- [ ] Velocidade necessária

✅ RESPOSTA CORRETA: Capacidade de expansão

> A capacidade de expansão depende de vários outros fatores, inclusive a modularidade do switch.


### Pergunta 7

Um cabo console também é chamado de ?

- [ ] cabo Ethernet
- [ ] cabo straight-through
- [x] cabo rollover
- [ ] cabo cruzado

✅ RESPOSTA CORRETA: cabo rollover

> Está certo. Como discutido no vídeo, o cabo console também é chamado de cabo rollover.

### Pergunta 8

Ao conectar pela primeira vez a um switch para configurá-lo, você deve responder "não" à pergunta inicial do diálogo. Depois de responder "não", qual é o prompt?

- [ ] Switch#
- [ ] Switch(config)#
- [ ] Switch(config-if)#
- [x] Switch>

✅ RESPOSTA CORRETA: Switch>

> Está certo. Como mostrado no vídeo, o prompt de comando após responder "no" à pergunta inicial do diálogo é Switch>.

### Pergunta 9

Quais são as duas portas normalmente usadas para gerenciamento de dispositivos? (Escolha duas.)

- [x] porta de armazenamento
- [ ] porta de adaptador de energia
- [x] porta console
- [ ] porta de uplink
- [ ] porta de acesso LAN

✅ RESPOSTA CORRETA: porta de armazenamento; porta console

> Está certo. O gerenciamento de dispositivos normalmente usa a porta console e a porta de armazenamento.