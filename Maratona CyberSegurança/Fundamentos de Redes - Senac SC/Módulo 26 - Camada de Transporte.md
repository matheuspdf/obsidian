
# 26.0 Introdução

## 26.0.1 Webster - Por que devo fazer este módulo?

Parece que Olcay e Abay estão terminando seu turno na fábrica de utilidades. Olcay diz a Abay para ter uma boa noite. Ela diz para ele estar preparado para conversar sobre tudo o que tem a ver com a camada de transporte pela manhã.

Abay pode querer usar este módulo antes de falar com Olcay pela manhã. Você está familiarizado com a camada de transporte? Você deve estar se quiser entender a rede. A camada de transporte é responsável pela comunicação lógica entre aplicativos executados em hosts diferentes. Vamos começar com este módulo para aprender mais!

## 26.0.2 O Que Vou Aprender Neste Módulo?

**Titulo do Módulo:** A Camada de Transporte

**Objetivo do módulo:** comparar as operações dos protocolos da camada de transporte no suporte à comunicação de ponta a ponta.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Transporte de dados|Explicar a função da camada de transporte no gerenciamento do transporte de dados na comunicação de ponta a ponta.|
|Visão Geral do TCP|Explicar as características do TCP.|
|Visão Geral do UDP|Explicar as características da UDP.|
|Números de porta|Explicar como o TCP e o UDP usam números de porta.|
|Processo de comunicação TCP|Explicar como os processos de estabelecimento e encerramento de sessão TCP tornam a comunicação confiável.|
|Confiabilidade e controle de fluxo|Explicar como as unidades de dados de protocolo TCP são transmitidas e confirmadas para garantir a entrega.|
|Comunicação UDP|Descrever os processos do cliente UDP para estabelecer a comunicação com um servidor.|

# 26.1 Transporte de dados

## 26.1.1 Propósito da Camada de Transporte

Os programas da camada de aplicação geram dados que devem ser trocados entre os hosts de origem e de destino. A camada de transporte é responsável pela comunicação lógica entre aplicativos executados em hosts diferentes. Isso pode incluir serviços como o estabelecimento de uma sessão temporária entre dois hosts e a transmissão confiável de informações para um aplicativo.

Como mostra a figura, a camada de transporte é o link entre a camada de aplicação e as camadas inferiores que são responsáveis pela transmissão pela rede.

![[Pasted image 20260622063842.png]]
A camada de transporte não tem conhecimento do tipo de host de destino, o tipo de mídia pela qual os dados devem percorrer, o caminho percorrido pelos dados, o congestionamento em um link ou o tamanho da rede.

A camada de transporte inclui dois protocolos:

- Protocolo TCP
- Protocolo UDP (User Datagram Protocol)


## 26.1.2 Responsabilidades da Camada de Transporte

A camada de transporte tem muitas responsabilidades.

**Selecione cada guia para obter mais informações.**

### **Rastreamento de Conversações Individuais**

Na camada de transporte, cada conjunto de dados que flui entre um aplicativo de origem e um aplicativo de destino é conhecido como conversa e é rastreado separadamente. É responsabilidade da camada de transporte manter e monitorar essas várias conversações.

Como ilustrado na figura, um host pode ter vários aplicativos que estão se comunicando pela rede simultaneamente.

A maioria das redes tem uma limitação da quantidade de dados que pode ser incluída em um único pacote. Portanto, os dados devem ser divididos em partes gerenciáveis.

![[Pasted image 20260622063919.png]]

### **Segmentação de Dados e Remontagem de Segmentos**

É responsabilidade da camada de transporte dividir os dados do aplicativo em blocos de tamanho adequado. Dependendo do protocolo de camada de transporte usado, os blocos de camada de transporte são chamados de segmentos ou datagramas. A figura ilustra a camada de transporte usando blocos diferentes para cada conversa.

A camada de transporte divide os dados em blocos menores (ou seja, segmentos ou datagramas) que são mais fáceis de gerenciar e transportar.

![[Pasted image 20260622063935.png]]

### **Adicionar Informações de Cabeçalho**

O protocolo da camada de transporte também adiciona informações de cabeçalho contendo dados binários organizados em vários campos a cada bloco de dados. São os valores nesses campos que permitem que os vários protocolos da camada de transporte realizem diferentes funções no gerenciamento da comunicação de dados.

Por exemplo, as informações de cabeçalho são usadas pelo host de recebimento para remontar os blocos de dados em um fluxo de dados completo para o programa de camada de aplicativo de recebimento.

A camada de transporte garante que, mesmo com vários aplicativos em execução em um dispositivo, todos os aplicativos recebam os dados corretos.
![[Pasted image 20260622063948.png]]


### **Identificação das Aplicações**

A camada de transporte deve separar e gerenciar várias comunicações com as diferentes necessidades de requisitos de transporte. Para passar fluxos de dados para os aplicativos adequados, a camada de transporte identifica o aplicativo de destino usando um identificador chamado número da porta. Conforme ilustrado na figura, cada processo de software que precisa acessar a rede recebe um número de porta exclusivo para esse host.
![[Pasted image 20260622064006.png]]

### **Multiplexação das Conversas**

O envio de alguns tipos de dados (por exemplo, um vídeo de streaming) através de uma rede, como um fluxo de comunicação completo, pode consumir toda a largura de banda disponível. Isso impediria que outras conversas de comunicação ocorressem ao mesmo tempo. Isso também dificultaria a recuperação de erro e retransmissão dos dados danificados.

Como mostrado na figura, a camada de transporte usa segmentação e multiplexação para permitir que diferentes conversas de comunicação sejam intercaladas na mesma rede.

A verificação de erros pode ser realizada nos dados do segmento, para determinar se o segmento foi alterado durante a transmissão.

![[Pasted image 20260622064020.png]]

## 26.1.3 Protocolos da Camada de Transporte

O IP está preocupado apenas com a estrutura, endereçamento e roteamento de pacotes. O IP não especifica como a entrega ou o transporte de pacotes ocorrem.

Os protocolos de camada de transporte especificam como transferir mensagens entre hosts e são responsáveis pelo gerenciamento dos requisitos de confiabilidade de uma conversa. A camada de transporte inclui os protocolos TCP e UDP.

Diferentes aplicações têm diferentes necessidades de confiabilidade de transporte. Portanto, o TCP/IP fornece dois protocolos de camada de transporte, conforme mostrado na figura.

![[Pasted image 20260622064038.png]]

## 26.1.4 Protocolo de Controle de Transmissão (TCP)

O IP se preocupa apenas com a estrutura, o endereçamento e o roteamento de pacotes, do remetente original ao destino final. A IP não é responsável por garantir a entrega ou determinar se uma conexão entre o remetente e o destinatário precisa ser estabelecida.

O TCP é considerado um protocolo de camada de transporte confiável, completo, que garante que todos os dados cheguem ao destino. O TCP inclui campos que garantem a entrega dos dados do aplicativo. Esses campos exigem processamento adicional pelos hosts de envio e recebimento.

**Nota**: O TCP divide os dados em segmentos.

O transporte TCP é análogo a enviar pacotes que são rastreados da origem ao destino. Se um pedido pelo correio estiver dividido em vários pacotes, um cliente poderá verificar on-line a sequência de recebimento do pedido.

O TCP fornece confiabilidade e controle de fluxo usando estas operações básicas:

- Número e rastreamento de segmentos de dados transmitidos para um host específico a partir de um aplicativo específico
- Confirmar dados recebidos
- Retransmitir quaisquer dados não reconhecidos após um certo período de tempo
- Dados de sequência que podem chegar em ordem errada
- Enviar dados a uma taxa eficiente que seja aceitável pelo receptor

Para manter o estado de uma conversa e rastrear as informações, o TCP deve primeiro estabelecer uma conexão entre o remetente e o receptor. É por isso que o TCP é conhecido como um protocolo orientado a conexão.

**Pressione Reproduzir na figura para ver como os segmentos TCP e as confirmações são transmitidos entre o remetente e o destinatário.**

![[Pasted image 20260622064113.png]]
![[Pasted image 20260622064136.png]]
![[Pasted image 20260622064155.png]]
![[Pasted image 20260622064228.png]]
![[Pasted image 20260622064247.png]]
![[Pasted image 20260622065441.png]]
![[Pasted image 20260622065517.png]]

## 26.1.5 Protocolo UDP (User Datagram Protocol)

O UDP é um protocolo de camada de transporte mais simples do que o TCP. Ele não fornece confiabilidade e controle de fluxo, o que significa que requer menos campos de cabeçalho. Como o remetente e os processos UDP receptor não precisam gerenciar confiabilidade e controle de fluxo, isso significa que datagramas UDP podem ser processados mais rápido do que segmentos TCP. O UDP fornece as funções básicas para fornecer datagramas entre os aplicativos apropriados, com muito pouca sobrecarga e verificação de dados.

**Nota**: O UDP divide os dados em datagramas que também são chamados de segmentos.

UDP é um protocolo sem conexão. Como o UDP não fornece confiabilidade ou controle de fluxo, ele não requer uma conexão estabelecida. Como o UDP não controla informações enviadas ou recebidas entre o cliente e o servidor, o UDP também é conhecido como um protocolo sem estado.

UDP também é conhecido como um protocolo de entrega de melhor esforço porque não há confirmação de que os dados são recebidos no destino. Com o UDP, não há processo de camada de transporte que informe ao remetente se a entrega foi bem-sucedida.

O UDP é como colocar uma carta regular, não registrada, no correio. O remetente da carta não tem conhecimento se o destinatário está disponível para receber a carta. Nem a agência de correio é responsável por rastrear a carta ou informar ao remetente se ela não chegar ao destino final.

**Clique no botão Reproduzir na figura para ver uma animação dos segmentos UDP que estão sendo transmitidos do remetente ao destinatário.**

![[Pasted image 20260622065741.png]]
![[Pasted image 20260622065841.png]]

## 26.1.6 O Protocolo de Camada de Transporte Certo para a Aplicação Certa

Alguns aplicativos podem tolerar a perda de dados durante a transmissão pela rede, mas atrasos na transmissão são inaceitáveis. Para esses aplicativos, o UDP é a melhor escolha, pois requer menos sobrecarga da rede. O UDP é preferível para aplicativos como Voz sobre IP (VoIP). Agradecimentos e retransmissão atrasariam a entrega e tornariam a conversa por voz inaceitável.

O UDP também é usado por aplicativos de solicitação e resposta onde os dados são mínimos, e a retransmissão pode ser feita rapidamente. Por exemplo, o Domain Name System (DNS) usa UDP para esse tipo de transação. O cliente solicita endereços IPv4 e IPv6 para um nome de domínio conhecido de um servidor DNS. Se o cliente não receber uma resposta em um período predeterminado de tempo, ele simplesmente envia a solicitação novamente.

Por exemplo, se um ou dois segmentos de uma transmissão de vídeo ao vivo não conseguir chegar, isso criará apenas uma interrupção momentânea na transmissão. Isso pode aparecer como uma distorção na imagem ou no som, mas pode não ser notado pelo usuário. Se o dispositivo de destino considerasse os dados perdidos, a transmissão poderia atrasar, enquanto aguardasse as retransmissões, causando, portanto, grandes perdas de áudio e vídeo. Nesse caso, é melhor fornecer a melhor experiência de mídia com os segmentos recebidos e descartar a confiabilidade.

Para outras aplicações, é importante que todos os dados cheguem e que possam ser processados em sua sequência adequada. Para esses tipos de aplicativos, o TCP é usado como o protocolo de transporte. Por exemplo, aplicações como bancos de dados, navegadores e clientes de e-mail exigem que todos os dados enviados cheguem ao destino em seu estado original. Quaisquer dados ausentes podem corromper uma comunicação, tornando-a incompleta ou ilegível. Por exemplo, é importante ao acessar informações bancárias pela web certificar-se de que todas as informações são enviadas e recebidas corretamente.

Os desenvolvedores de aplicações devem escolher que tipo de protocolo de transporte é apropriado com base nas necessidades de suas aplicações. O vídeo pode ser enviado através de TCP ou UDP. Os aplicativos que transmitem áudio e vídeo armazenados normalmente usam TCP. O aplicativo usa TCP para executar buffer, sondagem de largura de banda e controle de congestionamento, a fim de controlar melhor a experiência do usuário.

Vídeo e voz em tempo real geralmente usam UDP, mas também podem usar TCP, ou UDP e TCP. Um aplicativo de videoconferência pode usar UDP por padrão, mas como muitos firewalls bloqueiam UDP, o aplicativo também pode ser enviado por TCP.

Os aplicativos que transmitem áudio e vídeo armazenados usam TCP. Por exemplo, se sua rede, repentinamente, não comportar a largura de banda necessária para a transmissão de um filme sob demanda, a aplicação interrompe a reprodução. Durante essa interrupção, você deverá ver uma mensagem de “buffering...” , enquanto o TCP age para restabelecer a transmissão. Quando todos os segmentos estão em ordem e um nível mínimo de largura de banda é restaurado, a sessão TCP é retomada e o filme retoma a reprodução.

A figura resume as diferenças entre UDP e TCP.

![[Pasted image 20260622065907.png]]

## 26.1.7 Verifique a sua Compreensão- Transporte de Dados

### Pergunta 1

Qual camada é responsável por estabelecer uma sessão de comunicação temporária entre os aplicativos de host de origem e destino?

- [ ] Camada de aplicação
- [ ] Camada de enlace de dados
- [ ] Camada de rede
- [ ] Camada física
- [x] camada de transporte

✅ RESPOSTA CORRETA: camada de transporte

> A camada de transporte é responsável por estabelecer uma sessão de comunicação temporária entre os aplicativos host de origem e de destino.

---

### Pergunta 2

Quais são as três responsabilidades da camada de transporte? (Escolha três.)

- [x] Multiplexação das conversas
- [ ] Identificação de quadros
- [ ] identificando informações de roteamento
- [x] Segmentando dados e remontando segmentos
- [x] Rastreamento de conversas individuais

✅ RESPOSTA CORRETA: Multiplexação das conversas, Segmentando dados e remontando segmentos, Rastreamento de conversas individuais

> A camada de transporte é responsável pela multiplexação de conversações, segmentação de dados e remontagem de segmentos e rastreamento de conversas individuais.

---

### Pergunta 3

Qual instrução de protocolo de camada de transporte é verdadeira?

- [ ] O TCP tem menos campos do que o UDP.
- [ ] O TCP é mais rápido do que o UDP.
- [x] UDP é um protocolo de entrega com o melhor esforço.
- [ ] O UDP fornece confiabilidade.

✅ RESPOSTA CORRETA: UDP é um protocolo de entrega com o melhor esforço.

> UDP é um protocolo de entrega de melhor esforço enquanto TCP é um protocolo de transporte confiável.

---

### Pergunta 4

Qual protocolo de camada de transporte seria usado para aplicativos VoIP?

- [ ] Protocolo de informações da sessão (SIP)
- [ ] Protocolo TCP
- [x] Protocolo UDP (User Datagram Protocol)
- [ ] Protocolo de Transferência VoIP

✅ RESPOSTA CORRETA: Protocolo UDP (User Datagram Protocol)

> UDP seria usado por aplicativos VoIP sensíveis ao tempo.


# 26.2 Visão geral do TCP

## 26.2.1 Recursos TCP

No tópico anterior, você aprendeu que TCP e UDP são os dois protocolos de camada de transporte. Este tópico fornece mais detalhes sobre o que o TCP faz e quando é uma boa idéia usá-lo em vez de UDP.

Para entender as diferenças entre TCP e UDP, é importante entender como cada protocolo implementa recursos específicos de confiabilidade e como cada protocolo rastreia conversas.

Além de suportar as funções básicas de segmentação e remontagem de dados, o TCP também fornece os seguintes serviços:

- **Estabelece uma sessão -** O TCP é um protocolo orientado à conexão que negocia e estabelece uma conexão (ou sessão) permanente entre os dispositivos de origem e de destino antes de encaminhar qualquer tráfego. Com o estabelecimento da sessão, os dispositivos negociam o volume de tráfego esperado que pode ser encaminhado em determinado momento e os dados de comunicação entre os dois podem ser gerenciados atentamente.
- **Garante a entrega confiável -** Por várias razões, é possível que um segmento seja corrompido ou perdido completamente, pois é transmitido pela rede. O TCP garante que cada segmento enviado pela fonte chegue ao destino.
- **Fornece entrega no mesmo pedido -** Como as redes podem fornecer várias rotas que podem ter taxas de transmissão diferentes, os dados podem chegar na ordem errada. Ao numerar e sequenciar os segmentos, o TCP garante que os segmentos sejam remontados na ordem correta.
- **Suporta controle de fluxo -** os hosts de rede têm recursos limitados (ou seja, memória e poder de processamento). Quando percebe que esses recursos estão sobrecarregados, o TCP pode requisitar que a aplicação emissora reduza a taxa de fluxo de dados. Para isso, o TCP regula o volume de dados transmitido pelo dispositivo origem. O controle de fluxo pode impedir a necessidade de retransmissão dos dados quando os recursos do host receptor estão sobrecarregados.

Para obter mais informações sobre o TCP, procure o RFC 793 na Internet.

## 26.2.2 Cabeçalho TCP

TCP é um protocolo stateful, o que significa que ele controla o estado da sessão de comunicação. Para manter o controle do estado de uma sessão, o TCP registra quais informações ele enviou e quais informações foram confirmadas. A sessão com estado começa com o estabelecimento da sessão e termina com o encerramento da sessão.

Um segmento TCP adiciona 20 bytes (ou seja, 160 bits) de sobrecarga ao encapsular os dados da camada de aplicativo. A figura mostra os campos em um cabeçalho TCP.

![[Pasted image 20260622070333.png]]

## 26.2.3 Campos de cabeçalho TCP

A tabela identifica e descreve os dez campos em um cabeçalho TCP.

|Campo de cabeçalho TCP|Descrição|
|---|---|
|Porta de origem|Um campo de 16 bits usado para identificar o aplicativo de origem por número de porta.|
|Porta de destino|Um campo de 16 bits usado para identificar o aplicativo de destino pelo número da porta.|
|Número de Sequência|Um campo de 32 bits usado para fins de remontagem de dados.|
|Número de Confirmação|Um campo de 32 bits usado para indicar que os dados foram recebidos e o próximo byte esperado da origem.|
|Tamanho do cabeçalho|Um campo de 4 bits conhecido como "offset de dados" que indica o comprimento do cabeçalho de segmento TCP.|
|Reservado|Um campo de 6 bits que é reservado para uso futuro.|
|Bits de controle|Um campo de 6 bits que inclui códigos de bits, ou sinalizadores, que indicam a finalidade e a função do segmento TCP.|
|Tamanho da janela|Um campo de 16 bits usado para indicar o número de bytes que podem ser aceitos ao mesmo tempo.|
|Checksum|Um campo de 16 bits usado para verificação de erros do cabeçalho e dos dados do segmento.|
|Urgente|Um campo de 16 bits usado para indicar se os dados contidos são urgentes.|

## 26.2.4 Aplicações que usam TCP

O TCP é um bom exemplo de como as diferentes camadas do conjunto de protocolos TCP/IP têm funções específicas. O TCP lida com todas as tarefas associadas à divisão do fluxo de dados em segmentos, fornecendo confiabilidade, controlando o fluxo de dados e reordenando segmentos. O TCP libera a aplicação da obrigação de gerenciar todas essas tarefas. Aplicações como as mostradas na figura, podem simplesmente enviar o fluxo de dados à camada de transporte e usar os serviços TCP.

![[Pasted image 20260622070447.png]]

## 26.2.5 Verifique sua compreensão - Visão geral do TCP

### Pergunta 1

Qual protocolo de camada de transporte garante entrega confiável da mesma ordem?

- [ ] ICMP
- [ ] IP
- [x] TCP
- [ ] UDP

✅ RESPOSTA CORRETA: TCP

> O protocolo de camada de transporte TCP garante entrega confiável de mesma ordem.

---

### Pergunta 2

Qual instrução de cabeçalho TCP é verdadeira?

- [ ] Ele consiste em 4 campos em um cabeçalho de 8 bytes.
- [ ] Consiste em 8 campos em um cabeçalho de 10 bytes.
- [x] Ele consiste em 10 campos em um cabeçalho de 20 bytes.
- [ ] Ele consiste em 20 campos em um cabeçalho de 40 bytes.

✅ RESPOSTA CORRETA: Ele consiste em 10 campos em um cabeçalho de 20 bytes.

> O cabeçalho TCP consiste em 10 campos em um cabeçalho de 20 bytes.

---

### Pergunta 3

Quais dois aplicativos usariam o protocolo de camada de transporte TCP? (Escolha duas.)

- [x] FTP
- [x] HTTP
- [ ] ICMP
- [ ] TFTP
- [ ] VoIP

✅ RESPOSTA CORRETA: FTP, HTTP

> FTP e HTTP requerem o uso do protocolo de camada de transporte TCP.


# 26.3 Visão Geral do UDP

## 26.3.1 Recursos UDP

Este tópico abordará o UDP, o que ele faz e quando é uma boa idéia usá-lo em vez de TCP. UDP é um protocolo de transporte de melhor esforço. O UDP é um protocolo de transporte leve que oferece a mesma segmentação de dados e remontagem que o TCP, mas sem a confiabilidade e o controle de fluxo do TCP.

O UDP é um protocolo simples, normalmente descrito nos termos do que ele não faz em comparação ao TCP.

Os recursos UDP incluem o seguinte:

- Os dados são reagrupados na ordem em que são recebidos.
- Quaisquer segmentos perdidos não são reenviados.
- Nenhum estabelecimento de seção.
- O envio não é informado sobre a disponibilidade do recurso.

Para obter mais informações sobre o UDP, pesquise na Internet o RFC.

## 26.3.2 Cabeçalho UDP

UDP é um protocolo sem estado, o que significa que nem o cliente nem o servidor rastreiam o estado da sessão de comunicação. Se a confiabilidade for necessária ao usar o UDP como protocolo de transporte, ela deve ser tratada pela aplicação.

Um dos requisitos mais importantes para transmitir vídeo ao vivo e voz sobre a rede é que os dados continuem fluindo rapidamente. Vídeo ao vivo e aplicações de voz podem tolerar alguma perda de dados com efeito mínimo ou sem visibilidade e são perfeitos para o UDP.

Os blocos de comunicação no UDP são chamados de datagramas ou segmentos. Esses datagramas são enviados como o melhor esforço pelo protocolo da camada de transporte.

O cabeçalho UDP é muito mais simples do que o cabeçalho TCP porque só tem quatro campos e requer 8 bytes (ou seja, 64 bits). A figura mostra os campos em um cabeçalho UDP.

![[Pasted image 20260622071149.png]]

## 26.3.3 Campos de Cabeçalho UDP

A tabela identifica e descreve os quatro campos em um cabeçalho UDP.

|Campos de Cabeçalho UDP|Descrição|
|---|---|
|Porta de origem|Um campo de 16 bits usado para identificar o aplicativo de origem por número de porta.|
|Porta de destino|Um campo de 16 bits usado para identificar o aplicativo de destino pelo número da porta.|
|Comprimento|Um campo de 16 bits que indica o comprimento do cabeçalho do datagrama UDP.|
|Checksum|Um campo de 16 bits usado para verificação de erros do cabeçalho e dos dados do datagrama.|

## 26.3.4 Aplicações que usam UDP

Há três tipos de aplicações que são mais adequadas para o UDP:

- **Aplicações de vídeo e multimídia ao vivo** - Esses aplicativos podem tolerar a perda de dados, mas requerem pouco ou nenhum atraso. Os exemplos incluem VoIP e transmissão de vídeo ao vivo.
- **Aplicações de solicitação e resposta simples** - Aplicativos com transações simples em que um host envia uma solicitação e pode ou não receber uma resposta. Os exemplos incluem DNS e DHCP.
- **Aplicativos que lidam com a confiabilidade** - Comunicações unidirecionais em que o controle de fluxo, a detecção de erros, as confirmações e a recuperação de erros não são necessários ou podem ser gerenciados pela aplicação. Os exemplos incluem SNMP e TFTP.

A figura identifica aplicativos que exigem UDP.

![[Pasted image 20260622071322.png]]

Embora por padrão DNS e SNMP usem UDP, ambos podem usar TCP. O DNS usará o TCP se a solicitação ou resposta de DNS for maior que 512 bytes, como quando uma resposta de DNS inclui muitas resoluções de nome. Da mesma forma, em algumas situações o administrador de redes pode querer configurar o SNMP para usar o TCP.

## 26.3.5 Verifique seu entendimento — Visão geral do UDP

### Pergunta 1

Qual dos seguintes é um protocolo de camada de transporte de entrega de melhor esforço sem estado?

- [ ] ICMP
- [ ] IP
- [ ] TCP
- [x] UDP

✅ RESPOSTA CORRETA: UDP

> UDP é um protocolo de camada de transporte de entrega de melhor esforço sem estado.

---

### Pergunta 2

Qual instrução de cabeçalho UDP é verdadeira?

- [x] Ele consiste em 4 campos em um cabeçalho de 8 bytes.
- [ ] Consiste em 8 campos em um cabeçalho de 10 bytes.
- [ ] Ele consiste em 10 campos em um cabeçalho de 20 bytes.
- [ ] Ele consiste em 20 campos em um cabeçalho de 40 bytes.

✅ RESPOSTA CORRETA: Ele consiste em 4 campos em um cabeçalho de 8 bytes.

> O cabeçalho UDP consiste em quatro campos em um cabeçalho de 8 bytes.

---

### Pergunta 3

Quais dois aplicativos usariam o protocolo de camada de transporte UDP? (Escolha duas.)

- [ ] FTP
- [ ] HTTP
- [ ] ICMP
- [x] TFTP
- [x] VoIP

✅ RESPOSTA CORRETA: TFTP, VoIP

> TFTP e VoIP exigem o uso do protocolo de camada de transporte UDP.

---

### Pergunta 4

Quais dois campos são os mesmos em um cabeçalho TCP e UDP? (Escolha duas.)

- [ ] Bits de controle
- [x] Número da porta de destino
- [ ] Número de sequência
- [x] Número da porta de origem
- [ ] Número de porta conhecido

✅ RESPOSTA CORRETA: Número da porta de destino, Número da porta de origem

> Os cabeçalhos TCP e UDP incluem campos de número de porta de origem e destino.


# 26.4 Números de porta

## 26.4.1 Várias comunicações separadas

Como você aprendeu, existem algumas situações em que o TCP é o protocolo certo para o trabalho e outras situações em que o UDP deve ser usado. Independentemente do tipo de dados que estão sendo transportados, tanto o TCP quanto o UDP usam números de porta.

Os protocolos de camada de transporte TCP e UDP usam números de porta para gerenciar várias conversas simultâneas. Conforme mostrado na figura, os campos de cabeçalho TCP e UDP identificam um número de porta do aplicativo de origem e destino.

![[Pasted image 20260622071554.png]]

O número da porta de origem está associado ao aplicativo de origem no host local, enquanto o número da porta de destino está associado ao aplicativo de destino no host remoto.

Por exemplo, suponha que um host está iniciando uma solicitação de página da Web a partir de um servidor Web. Quando o host inicia a solicitação de página da Web, o número da porta de origem é gerado dinamicamente pelo host para identificar exclusivamente a conversa. Cada solicitação gerada por um host usará um número de porta de origem criado dinamicamente diferente. Este processo permite que várias conversações ocorram simultaneamente.

Na solicitação, o número da porta de destino é o que identifica o tipo de serviço que está sendo solicitado do servidor web de destino. Por exemplo, quando um cliente especifica a porta 80 na porta de destino, o servidor que receber a mensagem sabe que os serviços Web são solicitados.

Um servidor pode oferecer mais de um serviço simultaneamente, como serviços web na porta 80, enquanto oferece o estabelecimento de conexão FTP (File Transfer Protocol) na porta 21.

## 26.4.2 Pares de Sockets

As portas origem e destino são colocadas no segmento. Os segmentos são encapsulados em um pacote IP. O pacote IP contém o endereço IP de origem e destino. A combinação do endereço IP de origem e o número de porta de origem, ou do endereço IP de destino e o número de porta de destino é conhecida como um socket.

No exemplo na figura, o PC está solicitando simultaneamente serviços FTP e Web do servidor de destino.

![[Pasted image 20260622071909.png]]

No exemplo, a solicitação FTP gerada pelo PC inclui os endereços MAC da Camada 2 e os endereços IP da Camada 3. A solicitação também identifica o número da porta de origem 1305 (ou seja, gerado dinamicamente pelo host) e a porta de destino, identificando os serviços de FTP na porta 21. O host também solicitou uma página da Web do servidor usando os mesmos endereços de Camada 2 e Camada 3. No entanto, ele está usando o número da porta de origem 1099 (ou seja, gerado dinamicamente pelo host) e a porta de destino identificando o serviço Web na porta 80.

O socket é usado para identificar o servidor e o serviço que está sendo solicitado pelo cliente. Um socket do cliente pode ser assim, com 1099 representando o número da porta de origem: 192.168.1.5:1099

O soquete em um servidor da web pode ser 192.168.1.7:80

Juntos, esses dois soquetes se combinam para formar um _par de soquetes:_ 192.168.1.5:1099, 192.168.1.7:80

Os sockets permitem que vários processos em execução em um cliente se diferenciem uns dos outros, e várias conexões com um processo no servidor sejam diferentes umas das outras.

Este número de porta age como um endereço de retorno para a aplicação que faz a solicitação. A camada de transporte rastreia essa porta e a aplicação que iniciou a solicitação, de modo que quando uma resposta é retornada, ela pode ser encaminhada para a aplicação correta.

## 26.4.3 Grupos de Números de Portas

A Internet Assigned Numbers Authority (IANA) é a organização de padrões responsável por atribuir vários padrões de endereçamento, incluindo os números de porta de 16 bits. Os 16 bits usados para identificar os números de porta de origem e destino fornecem um intervalo de portas de 0 a 65535.

A IANA dividiu a gama de números nos três grupos de portos seguintes.

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed; word-wrap:break-word;"> <tr> <th>Grupo de Portas</th> <th>Intervalo de números</th> <th>Descrição</th> </tr> <tr> <td><strong>Portas bem conhecidas</strong></td> <td>0 a 1,023</td> <td> <ul> <li>Esses números de porta são reservados para serviços e aplicativos comuns ou populares, como navegadores da web, clientes de email e clientes de acesso remoto.</li> <li>Portas bem conhecidas definidas para aplicativos comuns de servidor permite que os clientes identifiquem facilmente o serviço associado necessário.</li> </ul> </td> </tr> <tr> <td><strong>Portas registradas</strong></td> <td>1,024 a 49,151</td> <td> <ul> <li>Esses números de porta são atribuídos pela IANA a uma entidade solicitante para uso com processos ou aplicativos específicos.</li> <li>Esses processos são principalmente aplicações que o usuário optou por instalar, e não aplicações comuns que receberiam um número de porta muito conhecida.</li> <li>Por exemplo, a Cisco registrou a porta 1812 para o processo de autenticação do servidor RADIUS.</li> </ul> </td> </tr> <tr> <td><strong>Portas Privadas e/ou Dinâmicas</strong></td> <td>49,152 a 65,535</td> <td> <ul> <li>Essas portas também são conhecidas como portas <em>efêmeras</em>.</li> <li>O sistema operacional do cliente geralmente atribui números de porta dinamicamente quando uma conexão a um serviço é iniciada.</li> <li>A porta dinâmica é usada para identificar a aplicação cliente durante a comunicação.</li> </ul> </td> </tr> </table>

---

**Observação:** alguns sistemas operacionais de cliente podem usar números de portas registradas, em vez de números de portas dinâmicas para atribuir portas origem.

A tabela exibe alguns números de porta conhecidos comuns e seus aplicativos associados.

| Número da Porta | Protocolo | Aplicação                                                                                    |
| --------------- | --------- | -------------------------------------------------------------------------------------------- |
| 20              | TCP       | File Transfer Protocol (FTP) – Dados                                                         |
| 21              | TCP       | Protocolo de transferência de arquivos (FTP) – Controle                                      |
| 22              | TCP       | Secure Shell (Shell seguro) – SSH                                                            |
| 23              | TCP       | Telnet                                                                                       |
| 25              | TCP       | Protocolo SMTP                                                                               |
| 53              | UDP, TCP  | Protocolo DNS                                                                                |
| 67              | UDP       | Dynamic Host Configuration Protocol (DHCP) – Servidor                                        |
| 68              | UDP       | Protocolo de configuração dinâmica de host – cliente                                         |
| 69              | UDP       | Protocolo de Transferência Trivial de Arquivo (TFTP)                                         |
| 80              | TCP       | Protocolo HTTP                                                                               |
| 110             | TCP       | Protocolo POP3 (Post Office Protocol – Protocolo dos Correios)                               |
| 143             | TCP       | Protocolo IMAP                                                                               |
| 161             | UDP       | Protocolo de Gerenciamento Simples de Rede (SNMP)                                            |
| 443             | TCP       | HTTPS (Secure Hypertext Transfer Protocol – Protocolo de Transferência de Hipertexto Seguro) |

Algumas aplicações podem usar tanto TCP quanto UDP. Por exemplo, o DNS usa o protocolo UDP quando os clientes enviam requisições a um servidor DNS. Contudo, a comunicação entre dois servidores DNS sempre usa TCP.

Pesquise no site da IANA o registro de portas para visualizar a lista completa de números de portas e aplicativos associados.

## 26.4.4 O Comando netstat

Conexões TCP desconhecidas podem ser uma ameaça de segurança maior. Elas podem indicar que algo ou alguém está conectado ao host local. Às vezes é necessário conhecer quais conexões TCP ativas estão abertas e sendo executadas em um host de rede. O netstat é um utilitário de rede importante que pode ser usado para verificar essas conexões. Como mostrado abaixo, digite o comando **netstat** para listar os protocolos em uso, o endereço local e os números de porta, o endereço externo e os números de porta e o estado da conexão.

```
C:∖> netstat

Active Connections

  Proto    Local Address          Foreign Address           State
  TCP      192.168.1.124:3126     192.168.0.2:netbios-ssn   ESTABLISHED
  TCP      192.168.1.124:3158     207.138.126.152:http      ESTABLISHED
  TCP      192.168.1.124:3159     207.138.126.169:http      ESTABLISHED
  TCP      192.168.1.124:3160     207.138.126.169:http      ESTABLISHED
  TCP      192.168.1.124:3161     sc.msn.com:http           ESTABLISHED
  TCP      192.168.1.124:3166     www.cisco.com:http        ESTABLISHED
(output omitted)
C:∖>
```

Por padrão, o comando **netstat** tentará resolver os endereços IP para os nomes de domínio e os números de porta para aplicações bem conhecidas. A opção **-n** pode ser usada para exibir endereços IP e números de porta em sua forma numérica.

## 26.4.5 Verifique sua compreensão - Números de Porta

### Pergunta 1

Suponha que um host com endereço IP 10.1.1.10 deseja solicitar serviços Web de um servidor em 10.1.1.254. Qual das opções a seguir exibe o par de soquetes correto?

- [ ] 1099:10.1.1.10, 80:10.1.1.254
- [ ] 10.1.1.10:80, 10.1.1.254:1099
- [x] 10.1.1.10:1099, 10.1.1.254:80
- [ ] 80:10.1.1.10, 1099:10.1.1.254

✅ RESPOSTA CORRETA: 10.1.1.10:1099, 10.1.1.254:80

> O par de soquetes para um host com endereço IP 10.1.1.10 solicitando serviços Web de um servidor em 10.1.1.254 seria 10.1.1.10:1099, 10.1.1.254:80.

---

### Pergunta 2

Qual grupo de portas inclui números de porta para aplicativos FTP, HTTP e TFTP?

- [ ] portas dinâmicas
- [ ] portas privadas
- [ ] portas registradas
- [x] portas bem conhecidas

✅ RESPOSTA CORRETA: portas bem conhecidas

> Os números de porta de aplicativos FTP, HTTP e TFTP são definidos no grupo de números de porta bem conhecido.

---

### Pergunta 3

Qual comando do Windows exibirá os protocolos em uso, o endereço local e os números de porta, o endereço externo e os números de porta e o estado da conexão?

- [ ] ipconfig/all
- [ ] ping
- [x] netstat
- [ ] traceroute

✅ RESPOSTA CORRETA: netstat

> O comando netstat do Windows exibe protocolos em uso, o endereço local e os números de porta, o endereço externo e os números de porta e o estado da conexão.


# 26.5 Processo de comunicação TCP

## 26.5.1 Processos em Servidores TCP

Você já conhece os fundamentos do TCP. Compreender a função dos números de porta irá ajudá-lo a compreender os detalhes do processo de comunicação TCP. Neste tópico, você também aprenderá sobre os processos de handshake de três vias e terminação de sessão TCP.

Cada processo de aplicativo em execução em um servidor está configurado para usar um número de porta. O número da porta é atribuído automaticamente ou configurado manualmente por um administrador do sistema.

Um servidor individual não pode ter dois serviços atribuídos ao mesmo número de porta dentro dos mesmos serviços de camada de transporte. Por exemplo, um host executando um aplicativo de servidor web e um aplicativo de transferência de arquivos não pode ter os dois configurados para usar a mesma porta, como a porta TCP 80.

Um aplicativo de servidor ativo atribuído a uma porta específica é considerado aberto, o que significa que a camada de transporte aceita e processa os segmentos endereçados a essa porta. Qualquer solicitação de cliente que chega endereçada ao soquete correto é aceita e os dados são transmitidos à aplicação do servidor. Pode haver muitas portas abertas ao mesmo tempo em um servidor, uma para cada aplicação de servidor ativa.

**Selecione cada guia para obter mais informações sobre os processos do servidor TCP.**

### **Clientes Enviando Requisições TCP**

O Cliente 1 está a solicitar serviços Web e o Cliente 2 está a solicitar o serviço de correio electrónico do mesmo servidor.

![[Pasted image 20260622072736.png]]

### **Portas de Destino das Requisições**

O cliente 1 está solicitando serviços da web usando a porta de destino bem conhecida 80 (HTTP) e o cliente 2 está solicitando serviço de e-mail usando a porta 25 (SMTP) bem conhecida.
![[Pasted image 20260622072749.png]]

### **Portas de Origem das Requisições**

As solicitações do cliente geram dinamicamente um número de porta de origem. Nesse caso, o cliente 1 está usando a porta de origem 49152 e o cliente 2 está usando a porta de origem 51152.

![[Pasted image 20260622072804.png]]

### **Portas de Destino das Respostas**

Quando o servidor responde às solicitações do cliente, ele reverte as portas de destino e de origem da solicitação inicial. Observe que a resposta do servidor à solicitação da Web agora tem a porta de destino 49152 e a resposta de e-mail agora tem a porta de destino 51152.

![[Pasted image 20260622072816.png]]


### **Portas de Origem das Respostas**

A porta de origem na resposta do servidor é a porta de destino original nas solicitações iniciais.

![[Pasted image 20260622072832.png]]

## 26.5.2 Estabelecimento de Conexão TCP

Em algumas culturas, quando duas pessoas se encontram, elas costumam se cumprimentar apertando as mãos. Ambas as partes entendem o ato de apertar as mãos como um sinal para uma saudação amigável. As conexões de rede são semelhantes. Nas conexões TCP, o cliente host estabelece a conexão com o servidor usando o processo de handshake de três vias.

**Selecione cada guia para obter mais informações sobre cada etapa de estabelecimento de conexão TCP.**

### Etapa 1. SYN

O cliente iniciador requisita uma sessão de comunicação cliente-servidor com o servidor.
![[Pasted image 20260622072910.png]]


### **Etapa 2. ACK e SYN**

O servidor confirma a sessão de comunicação cliente-servidor e requisita uma sessão de comunicação de servidor-cliente.
![[Pasted image 20260622072930.png]]


### **Etapa 3. ACK**

O cliente iniciador confirma a sessão de comunicação de servidor-cliente.
![[Pasted image 20260622073022.png]]

O handshake de três vias valida se o host de destino está disponível para comunicação. Neste exemplo, o host A validou que o host B está disponível.

## 26.5.3 Encerramento da Sessão

Para fechar uma conexão, o flag de controle Finish (FIN) deve ser ligado no cabeçalho do segmento. Para terminar cada sessão TCP de uma via, um handshake duplo, consistindo de um segmento FIN e um segmento ACK (Acknowledgment) é usado. Portanto, para terminar uma conversação única permitida pelo TCP, quatro trocas são necessárias para finalizar ambas as sessões. O cliente ou o servidor podem iniciar o encerramento.

No exemplo, os termos cliente e servidor são usados como referência para simplificar, mas dois hosts que possuem uma sessão aberta podem iniciar o processo de finalização.

**Clique em cada guia para obter mais informações sobre as etapas de fechamento da sessão.**

### **Etapa 1. FIN**

Quando o cliente não tem mais dados para enviar no fluxo, ele envia um segmento com um flag FIN ligado.
![[Pasted image 20260622073104.png]]

### **Etapa 2. ACK**

O servidor envia ACK para confirmar o recebimento de FIN para encerrar a sessão do cliente com o servidor.
![[Pasted image 20260622073119.png]]

### **Etapa 3. FIN**

O servidor envia um FIN ao cliente para encerrar a sessão do servidor-para-cliente.
![[Pasted image 20260622073135.png]]

### **Etapa 4. ACK**

O cliente responde com um ACK para reconhecer o FIN do servidor.
![[Pasted image 20260622073153.png]]

Quando todos os segmentos tiverem sido confirmados, a conexão é encerrada.

