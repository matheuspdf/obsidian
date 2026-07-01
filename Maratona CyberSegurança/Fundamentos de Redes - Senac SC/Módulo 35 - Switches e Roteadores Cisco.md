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


# 35.2 Velocidades do Switch e Métodos de Encaminhamento

## 35.2.1 Métodos de Encaminhamento de Quadros em Switches da Cisco

Como você aprendeu no tópico anterior, os switches usam suas tabelas de endereço MAC para determinar qual porta usar para encaminhar quadros. Com os switches Cisco, existem realmente dois métodos de encaminhamento de quadros e há boas razões para usar um em vez do outro, dependendo da situação.

Os switches usam um dos seguintes métodos de encaminhamento para o switching (comutação) de dados entre suas interfaces de rede:

- **Comutação Armazenar e encaminhar** - Este método de encaminhamento de quadros recebe o quadro inteiro e calcula o CRC. O CRC usa uma fórmula matemática, baseada no número de bits (valores 1) no quadro, para determinar se o quadro recebido apresenta erro. Se o CRC é válido, o switch procura o endereço de destino, que determina a interface de saída. Em seguida, o quadro é encaminhado para fora da porta correta.
- **Comutação corte direto** - Esse método de encaminhamento de quadros encaminha o quadro antes de ser totalmente recebido. Pelo menos o endereço de destino do quadro deve ser lido para que o quadro possa ser encaminhado.

Uma grande vantagem da Comutação Armazenar e encaminhar é que ele determina se um quadro tem erros antes de propagar o quadro. Quando um erro é detectado em um quadro, o switch o descarta. O descarte de quadros com erros reduz o consumo de largura de banda por dados corrompidos. A comutação Armazenar e encaminhar é necessária para a análise de qualidade de serviço (QoS) em redes convergentes onde a classificação de quadros para priorização de tráfego é necessária. Por exemplo, os fluxos de dados de voz sobre IP (VoIP) precisam ter prioridade sobre o tráfego de navegação na web.

Clique em Reproduzir na animação para obter uma demonstração do processo armazenar e encaminhar.

![[brave_K1QEGLcVyl.mp4]]


## 35.2.2 Comutação corte direto

Na comutação corte direto, o switch atua nos dados assim que eles são recebidos, mesmo que a transmissão não tenha sido concluída. O switch armazena em buffer apenas o parte do quadro suficiente para ler o endereço MAC de destino para que possa determinar para qual porta ele deve encaminhar os dados. O endereço MAC de destino está localizado nos primeiros 6 bytes do quadro após o preâmbulo. O switch consulta o endereço MAC de destino na tabela de comutação , determina a porta da interface de saída e encaminha o quadro ao seu destino pela porta de switch designada. O switch não realiza nenhuma verificação de erros no quadro.

Reproduza a animação para obter uma demonstração do processo de comutação corte direto.

![[brave_3kMK9pm2cA.mp4]]

Há duas formas de comutação corte direto:

- **Comutação avanço rápido -**  A comutação avanço rápido oferece o menor nível de latência e encaminha imediatamente um pacote depois de ler o endereço de destino. Como a comutação avanço rápido começa o encaminhamento antes de receber todo o pacote, alguns pacotes podem ser retransmitidos com erros. Isso ocorre com pouca freqüência e a NIC de destino descarta o pacote com defeito após o recebimento. No modo avanço rápido, a latência é medida do primeiro bit recebido até o primeiro bit transmitido. Comutação avanço rápido é o método corte direto típico de comutação.
- **Comutação livre de fragmentos -** Na comutação livre de fragmentos, o switch armazena os primeiros 64 bytes do quadro antes de encaminhar. Esse tipo de comutação pode ser encarado como um compromisso entre o switching armazenar e encaminhar e o switching avanço rápido. O motivo da comutação livre de fragmentos armazenar somente os primeiros 64 bytes do quadro é que a maioria dos erros e das colisões de rede ocorre durante os primeiros 64 bytes. A comutação livre de fragmentos tenta melhorar a comutação avanço rápido executando uma pequena verificação de erros nos primeiros 64 bytes do quadro para garantir que não ocorra uma colisão antes de encaminhar o quadro. A comutação livre de fragmentos é um compromisso entre a alta latência e a alta integridade da comutação armazenar e encaminhar e a baixa latência e a integridade reduzida da comutação avanço rápido.

Alguns switches são configurados para executar a comutação corte direto por porta até que um limite de erro definido pelo usuário seja atingido e, depois, mudam automaticamente para armazenar e encaminhar. Quando a taxa de erros fica abaixo do limite, a porta retorna automaticamente para a comutação corte direto.


### 35.2.3 Buffer de Memória em Switches

Um switch Ethernet pode usar uma técnica de armazenamento de quadros em buffers antes de enviá-los. O buffer também pode ser usado quando a porta de destino está ocupada devido ao congestionamento. O switch armazena o quadro até que ele possa ser transmitido.

Como mostrado na tabela, existem dois métodos de buffer de memória:

#### Métodos de buffer de memória

| Método                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Memória por porta     | Os quadros são armazenados em filas vinculadas a portas específicas de entrada e saída.<br>Um quadro é transmitido para a porta de saída somente quando todos os quadros à frente na fila foram transmitidos com êxito.<br>É possível que um único quadro atrase a transmissão de todos os quadros na memória caso uma porta de destino esteja ocupada.<br>Esse atraso ocorre mesmo se os outros quadros puderem ser transmitidos para portas de destino que estejam livres. |
| Memória compartilhada | Deposita todos os quadros em um buffer de memória comum compartilhado por todas as portas do switch e a quantidade de memória buffer necessária por uma porta é alocada dinamicamente.<br>Os quadros no buffer são dinamicamente vinculados à porta de destino, permitindo que um pacote seja recebido em uma porta e depois transmitido em outra porta, sem movê-lo para uma fila diferente.                                                                                |

## 35.2.4 Configurações de Velocidade e Duplex

Duas das configurações mais básicas em um switch são as configurações de largura de banda (às vezes denominada "velocidade") e duplex para cada porta do switch individual. É fundamental a correspondência dessas configurações na porta do switch e nos dispositivos conectados, como um computador ou outro switch.

Há dois tipos de configurações duplex usadas para comunicação em uma rede Ethernet:

- **duplex completo** – As duas extremidades da conexão podem enviar e receber ao mesmo tempo.
- **Meio duplex** - Somente uma das extremidades da conexão pode enviar e receber por vez.

A negociação automática é uma função opcional encontrada na maioria dos switches Ethernet e das placas de interface de rede (NICs). Ela permite que dois dispositivos negociem automaticamente as melhores capacidades de velocidade e duplex. duplex completo será escolhido se os dois dispositivos tiverem essa capacidade e com a largura de banda mais alta em comum entre eles.

Na figura, a NIC Ethernet para PC-A pode operar em duplex completo ou Meio duplex e em 10 Mbps ou 100 Mbps.

![[Pasted image 20260630220910.png]]

O PC-A está conectado ao switch S2 na porta 1, que pode operar em duplex completo ou Meio duplex e em 10 Mbps, 100 Mbps ou 1000 Mbps (1 Gbps). Se os dois dispositivos estiverem usando negociação automática, o modo operacional será duplex completo e 100 Mbps.

**Nota**: A maioria dos switches Cisco e das NICs Ethernet faz a negociação automática por padrão para velocidade e duplex. Portas Gigabit Ethernet só operam em duplex completo.

A incompatibilidade duplex é uma das causas mais comuns de problemas de desempenho nos links Ethernet 10/100 Mbps. Ocorre quando uma porta no link opera em Meio duplex, enquanto a outra porta opera em duplex completo, conforme mostrado na figura.

![[Pasted image 20260630220923.png]]

S2 continuará a detectar colisões porque S1 continua mandando quadros sempre que tem algo para enviar.

A incompatibilidade duplex ocorre quando uma ou ambas as portas em um link são redefinidas e o processo de negociação automática não resulta nos dois parceiros de link com a mesma configuração. Também pode ocorrer quando os usuários reconfiguram um lado de um link e esquecem de reconfigurar o outro. Os dois lados de um link devem estar ambos com a negociação automática ligada ou desligada. A prática recomendada é configurar ambas as portas de switch Ethernet como duplex completo.

## 35.2.5 MDIX automático

As conexões entre dispositivos exigiram uma vez o uso de um cabo cruzado ou direto. O tipo de cabo necessário dependia do tipo de dispositivos de interconexão.

Por exemplo, a figura identifica o tipo de cabo correto necessário para interconectar dispositivos switch para switch, switch para roteador, switch para host ou roteador para host. Um cabo cruzado é usado ao conectar dispositivos semelhantes, e um cabo direto é usado para conectar dispositivos diferentes.

**Nota**: Uma conexão direta entre um roteador e um host requer uma conexão cruzada.

![[Pasted image 20260630220939.png]]

A maioria dos dispositivos de switch agora suporta o recurso de (Auto-MDIX) interface dependente automática. Quando ativado, o switch detecta automaticamente o tipo de cabo conectado à porta e configura as interfaces de acordo. Com isso, você pode utilizar um cabo cruzado ou direto para conexões a uma porta 10/100/1000 de cobre no switch, seja qual for o tipo de dispositivo na outra extremidade da conexão.

O recurso auto-MDIX é ativado por padrão em switches que executam o Cisco IOS Release 12.2 (18) SE ou posterior. No entanto, o recurso pode ser desativado. Por esse motivo, você sempre deve usar o tipo de cabo correto e não confiar no recurso Auto-MDIX. O Auto-MDIX pode ser reativado usando o comando **mdix auto** no modo de configuração da interface.

## 35.2.6 Verifique sua compreensão - Velocidades do Switch e métodos de encaminhamento

**Verifique sua compreensão das velocidades do switch e métodos de encaminhamento escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Quais são os dois métodos para comutar dados entre portas em um switch? (Escolha duas.)

- [x] comutação armazenar e encaminhar
- [ ] comutação armazenar e fornecer
- [x] comutação corte direto
- [ ] comutação armazenar e restaurar
- [ ] comutação corte fora

✅ RESPOSTA CORRETA: comutação armazenar e encaminhar; comutação corte direto

> Está certo. Os dois métodos para comutar dados entre portas em um switch são comutação corte direto e comutação armazenar e encaminhar.

### Pergunta 2

Qual método de comutação pode ser implementado usando comutação rápida ou comutação sem fragmentos?

- [ ] comutação armazenar e restaurar
- [ ] comutação corte fora
- [ ] comutação armazenar e encaminhar
- [x] comutação corte direto

✅ RESPOSTA CORRETA: comutação corte direto

> Está certo. A comutação corte direto é implementada usando comutação rápida ou comutação sem fragmentos.

### Pergunta 3

Quais dois tipos de técnicas de buffer de memória são usadas por switches? (Escolha duas.)

- [x] buffer de memória baseado em porta
- [ ] buffer de memória de longo prazo
- [x] buffer de memória compartilhada
- [ ] buffer de memória de curto prazo

✅ RESPOSTA CORRETA: buffer de memória baseado em porta; buffer de memória compartilhada

> Está certo. Os switches usam duas técnicas de buffer de memória: buffer de memória baseado em porta e buffer de memória compartilhada.

### Pergunta 4

Qual recurso negocia automaticamente a melhor velocidade e configuração duplex entre dispositivos de interconexão?

- [x] Negociação automática
- [ ] MDIX Automático
- [ ] Autobots
- [ ] Auto-tune

✅ RESPOSTA CORRETA: Negociação automática

> Está certo. A negociação automática é uma tecnologia que negocia automaticamente a velocidade e o duplex entre dois dispositivos conectados.

# 35.3 Processo de inicialização do switch

## 35.3.1 Ligue o Switch

Os switches Cisco são pré-configurados para operar em uma LAN quando são inicializados. Todas as portas de interface no switch estão ativas e começam a encaminhar o tráfego imediatamente quando os dispositivos são conectados. É importante lembrar que nenhuma configuração de segurança está habilitada por padrão. Defina as configurações básicas de segurança antes de colocar o switch na rede.

As três etapas básicas para inicializar um switch são:

**Etapa 1**. Verifique os componentes.  
**Etapa 2**. Conecte os cabos ao switch.  
**Etapa 3**. Inicialize o switch.  

**Nota**: Você também pode conectar cabos após a alimentação.

Quando o switch está ativado, o Power On Self Test (POST) é iniciado. Durante o POST, os LEDs piscam enquanto uma série de testes determina se o switch funciona corretamente.

O POST é concluído quando o SYST LED está verde e pisca rapidamente. Se o POST falhar, o SYST LED fica na cor âmbar. Quando um POST falha, é necessário retornar o switch para reparos.

Quando todos os procedimentos de inicialização são concluídos, o switch Cisco está pronto para ser configurado.

**Clique em cada etapa para obter mais informações**

### **Passo 1. Verifique os componentes.**

Certifique-se de que todos os componentes fornecidos com o switch Cisco 2960 estão disponíveis. São eles: o cabo console, o cabo de alimentação, o cabo de Ethernet e a documentação do switch.

![[Pasted image 20260630221144.png]]


### **Etapa 2. Conecte os cabos ao switch.**

Conecte o PC ao switch com um cabo console e inicie uma sessão com um emulador de terminal. Conecte o cabo de alimentação CA ao switch e a uma tomada CA aterrada.

#### Conexão da console do Switch para o Laptop

![[Pasted image 20260630221206.png]]


### **Etapa 3. Inicialize o switch.**

Alguns modelos de switch Cisco não têm um chave liga / desliga, como o switch Cisco Catalyst 9300 48S mostrado na figura. Para ligar o switch, conecte uma extremidade do cabo de alimentação CA ao conector de alimentação CA do switch e a outra extremidade a uma tomada CA.

**Observação:** O switch Cisco Catalyst 9300 na figura tem fontes de alimentação redundantes caso haja falha.

#### Painel traseiro do Cisco Catalyst 9300 48S
![[Pasted image 20260630221221.png]]

## 35.3.2 Vídeo - Gerenciamento de dispositivos por dentro (Dentro da banda) e por fora da rede (Fora da banda)

**Selecione o botão Reproduzir para assistir o vídeo.**

Neste vídeo, vamos dar uma olhada no gerenciamento remoto fora da rede (out-of-band) e gerenciamento via rede (in-band). O gerenciamento fora da rede requer que o computador esteja diretamente conectado à porta de console do dispositivo. Nesse caso, um switch Ethernet. Também pode ser um roteador. Isso permite que o técnico acesse o dispositivo sem ter qualquer tipo de conexão de rede. Isso pode ser para configurar o dispositivo inicialmente, ou pode ser na solução de problemas do dispositivo, ou quando quiser configurar o dispositivo sem ter ou precisar de uma conexão de rede.

O gerenciamento em rede significa simplesmente que queremos ser capazes de acessar remotamente o dispositivo pela rede. Nesse caso, nosso switch Ethernet. Então, tanto nosso switch Ethernet quanto o dispositivo que estamos usando para acessá-lo devem ser capazes de se comunicar um com o outro através da rede. Podemos acessar e configurar o dispositivo remotamente usando Telnet, SSH, o SSH é muito melhor, e mais seguro que o Telnet, ou HTTP, ou HTTPS.

Então, essas são as duas maneiras pelas quais podemos acessar um dispositivo. Ou gerenciamento fora da rede, onde temos que ter conectividade física ao dispositivo, mas não há conectividade de rede, ou gerenciamento pela rede, onde podemos acessar o dispositivo remotamente, mas precisamos ter conectividade de rede com o dispositivo.


## 35.3.3 Arquivos de inicialização do IOS

Como mostrado na figura, um dispositivo da Cisco carrega estes dois arquivos na RAM quando é iniciado:

- **Arquivo de imagem do IOS -** O IOS facilita a operação básica dos componentes de hardware do dispositivo. A imagem do IOS geralmente é armazenada na memória flash.
- **Arquivo de configuração de inicialização -** Contém os comandos utilizados para configurar inicialmente um roteador e criar o arquivo de configuração de execução armazenado na RAM. O arquivo de configuração de inicialização é armazenado na NVRAM. Todas as alterações de configuração são armazenadas no arquivo de configuração em execução e são implementadas imediatamente pelo IOS.

O arquivo de configuração de execução é modificado quando o administrador de rede desempenha a configuração do dispositivo. Quando as alterações são feitas no arquivo running-config, ele deve ser salvo na NVRAM como arquivo de configuração de inicialização, caso o roteador seja reinicializado ou perca energia.

![[Pasted image 20260630221320.png]]

## 35.3.4 Verifique a sua compreensão - Processo de inicialização do switch

**Verifique sua compreensão sobre processo de inicialização do switch, escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Qual das alternativas a seguir é a ordem correta das três etapas básicas para ligar um switch?

- [ ] ligar o switch, verificar os componentes, conectar os cabos ao switch
- [x] verifique os componentes, conecte os cabos ao switch, ligue o switch
- [ ] conectar os cabos ao switch, verificar os componentes, ligar o switch

✅ RESPOSTA CORRETA: verifique os componentes, conecte os cabos ao switch, ligue o switch

> Está certo.
> 
> 1. As três etapas básicas para inicializar um switch são:
>     
> 
> - Passo 1. Verifique os componentes.
> - Etapa 2. Conecte os cabos ao switch.
> - Etapa 3. Inicialize o switch.

### Pergunta 2

Quando um switch é conectado a uma tomada, o POST começa. Como você sabe que o POST foi concluído?

- [x] Os LEDs SYS piscam rapidamente em verde.
- [ ] Os LEDs SYS piscam rapidamente na cor âmbar.
- [ ] Os LEDs de porta piscam rapidamente em verde.
- [ ] Os LEDs de porta piscam rapidamente em âmbar.

✅ RESPOSTA CORRETA: Os LEDs SYS piscam rapidamente em verde.

> Está certo. O POST é concluído quando o SYST LED está verde e pisca rapidamente. Se o POST falhar, o SYST LED fica na cor âmbar.

### Pergunta 3

Verdadeiro ou falso? O gerenciamento fora da banda exige que as conexões de rede local no dispositivo estejam ativas.

- [ ] verdadeiro
- [x] falso

✅ RESPOSTA CORRETA: falso

> Está certo. A resposta correta é falsa. O gerenciamento fora de banda requer que um computador seja conectado diretamente à porta de console do dispositivo de rede que está sendo configurado. Contudo, ele não exige que as conexões de rede local no dispositivo estejam ativas.

### Pergunta 4

Verdadeiro ou falso? Uma conexão de gerenciamento em banda requer que pelo menos uma interface de rede no dispositivo esteja conectada à rede e tenha um endereço IP configurado nela.

- [x] verdadeiro
- [ ] falso

✅ RESPOSTA CORRETA: verdadeiro

> Está certo. A resposta correta é verdadeira. Para que um computador se conecte-se ao dispositivo e realize as tarefas de gerenciamento em banda, pelo menos uma interface de rede no dispositivo deve estar conectada à rede e ter um endereço IP configurado.

### Pergunta 5

Onde o arquivo de imagem do IOS normalmente é armazenado?

- [ ] Unidade USB
- [ ] RAM
- [ ] NVRAM
- [x] Memória flash

✅ RESPOSTA CORRETA: Memória flash

> Está certo. A imagem do IOS geralmente é armazenada na memória flash.


# 35.4 Roteadores Cisco

## 35.4.1 Vídeo - Componentes do roteador Cisco

**Selecione o botão Reproduzir para assistir o vídeo.**

Neste vídeo, vamos explorar alguns dos componentes de um roteador 1941 da Cisco. Vou virar o roteador para trás, porque facilita muito a visualização dos diferentes componentes.

A primeira coisa que você vai notar é significativamente diferentes dos switches, e o motivo é que o switch tinha muitas portas Ethernet, pois o switch fornece a conectividade com os dispositivos da camada de acesso. Agora, um roteador conecta apenas redes individuais, então o roteador tem muito menos portas. Então vamos observar algumas delas.

O que você pode ver aqui é a cor amarela revestida das portas Ethernet. Aqui, elas são chamadas de interfaces Ethernet. E, nesse caso, elas fornecem conectividade gigabit. Então, vocês podem ver que há duas interfaces amarelas, Gigabit Ethernet no roteador.

Você também verá uma interface revestida de cor azul, que fornece a conexão serial para o cabo de console. O cabo do console oferece conectividade entre o laptop ou o computador e o dispositivo de rede para que você tenha um canal através do qual comunicar-se com o dispositivo para as configurações iniciais. Você também vai notar que há uma mini USB que você pode usar como um cabo de console e também algumas portas USB que você pode usar como um armazenamento adicional.

Caso contrário, algumas coisas são muito semelhantes com o switch. Você tem uma conexão de cabo de alimentação, agora um roteador você também tem um interruptor de liga e desliga. Muitos switches vêm automaticamente para que, quando você os conecte em uma fonte de alimentação, eles automaticamente são ligados e a única maneira que você consegue fisicamente desligá-los é desconectando o cabo. Agora, em um roteador, ele tem um botão liga/desliga, então você tem que ter cuidado quando conectá-lo para você realmente ligar o dispositivo.

Então, basicamente, esses são os componentes de um roteador, assim que saem da caixa. Agora você também vai notar que o roteador tem algo que o switch não tem, tem slots de expansão e, neste roteador, você vai notar que existem três slots em que é possível colocar peças adicionais do equipamento.

Basicamente, são os componentes de um roteador 1941 Cisco.


## 35.4.2 Componentes do roteador

Independentemente de função, tamanho ou complexidade, todos os modelos de roteador são basicamente computadores. E assim como computadores, tablets e dispositivos inteligentes, o roteador também exige:

- Sistema operacional (SO)
- Unidade central de processamento (CPU)
- RAM (memória de acesso aleatório)
- ROM (memória somente de leitura)
- NVRAM (memória de acesso aleatório não volátil)

Como todos os computadores, tablets e dispositivos inteligentes, os roteadores da Cisco exigem uma CPU para executar instruções do sistema operacional, como a inicialização do sistema, as funções de roteamento e as funções de switching.

A CPU precisa de um sistema operacional para prover funções de roteamento e switching. O Cisco IOS (Internetwork Operating System) é o software de sistema usado para a maioria dos dispositivos Cisco, independentemente do tamanho e tipo. Ele é usado para roteadores, switches LAN, pequenos access points sem fio, grandes roteadores com dezenas de interfaces e muitos outros dispositivos.


## 35.4.3 Portas das interfaces dos roteadores

Embora existam vários tipos e modelos diferentes de roteadores, cada roteador Cisco tem os mesmos componentes gerais de hardware.

A figura mostra um Roteador de Serviços Integrado (ISR) do modelo Cisco 4321. O roteador inclui as seguintes conexões:

- **Portas console** - Duas portas console da configuração inicial e interface de linha de comando (CLI) usando uma porta RJ-45 regular e um novo conector USB do Tipo-B (USB mini-b).
- **Duas interfaces LAN** - Duas interfaces Gigabit Ethernet para acesso LAN GE 0/0/0 e GE 0/0/1. A porta GE 0/0/0 pode ser acessada por uma conexão RJ-45 ou usando uma conexão SFP (tamanho pequeno) para fornecer uma conexão de fibra óptica.
- **Módulo de Interface de Redes (NIMs)** - Dois slots de expansão NIM que proporcionam modularidade e flexibilidade ao habilitar o roteador para dar suporte aos tipos diferentes de módulos de interface, incluindo serial, a linha digital de assinante (DSL), porta do switch e sem fio.

O Cisco 4321 ISR também tem uma porta USB, uma interface de gerenciamento e uma porta auxiliar. A porta USB pode ser usada para transferências de arquivos. A porta de gerenciamento pode ser usada para acesso de gerenciamento remoto quando as duas interfaces Gigabit Ethernet estiverem indisponíveis. A porta auxiliar fornece suporte antigo para um método de conexão de um modem dial-up ao roteador para acesso remoto. A porta auxiliar é hoje raramente usada em redes.

![[Pasted image 20260630221654.png]]

## 35.4.4 Verifique a sua compreensão - Roteadores Cisco

**Verifique sua compreensão sobre roteadores Cisco escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Verdadeiro ou falso? Um roteador tem muitas portas Ethernet para fornecer acesso aos dispositivos na rede.

- [ ] verdadeiro
- [x] falso

✅ RESPOSTA CORRETA: falso

> Está certo. A resposta correta é falsa. Um roteador normalmente tem apenas algumas portas Ethernet para conectar redes. Um switch fornece muitas portas Ethernet para acesso ao dispositivo.

### Pergunta 2

Qual das seguintes interfaces pode ser usada para gerenciar o roteador? (Escolha três.)

- [x] Porta Auxiliar
- [x] Portas console
- [ ] Slots NIM
- [x] Interface de gerenciamento
- [ ] Porta USB

✅ RESPOSTA CORRETA: Porta Auxiliar; Portas console; Interface de gerenciamento

> Está certo. As portas console, a interface de gerenciamento e a porta auxiliar podem ser usadas para gerenciar o roteador.

### Pergunta 3

Verdadeiro ou falso? Com a porta de fibra óptica baseada em SFP, o roteador 4321 tem três interfaces Gigabit Ethernet que podem ser usadas para tráfego de dados.

- [x] falso
- [ ] verdadeiro

✅ RESPOSTA CORRETA: falso

> Está certo. A resposta correta é falsa. A porta baseada em SFP pode ser usada como uma opção de fibra óptica para a porta RJ-45 GE 0/0/0.