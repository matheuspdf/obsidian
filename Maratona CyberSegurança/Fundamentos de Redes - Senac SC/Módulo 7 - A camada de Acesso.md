# 7.0 Introdução

## 7.0.1 Webster - Por que devo fazer este módulo?

Durante uma pausa para o almoço, Kishori vê sua amiga, Rina, e elas decidem comer juntas. Rina trabalha como técnica de suporte de TI no hospital. Kishori acha que esta pode ser uma boa oportunidade para fazer a Rina uma pergunta que ela estava pensando. Kishori agora sabe que seu computador desktop no posto das enfermeiras se conecta à rede usando um cabo de par trançado. A maioria dos outros dispositivos que ela usa se conecta à rede sem fio. Ela se pergunta se há alguma diferença na forma como os dispositivos com e sem fio se comunicam na rede. Rina sabe que Kishori tem parentes nos Estados Unidos. Ela explica que as diferenças entre a comunicação de rede com e sem fio são semelhantes às diferenças nos formatos de endereçamento usados para enviar pacotes para países diferentes. O conteúdo dentro pode ser exatamente o mesmo, mas o endereço e, possivelmente, o pacote podem ser muito diferentes.

Como uma mensagem é entregue? Ao escrever uma carta e colocá-la no envelope, você precisa verificar se ela tem as informações de endereço corretas para serem entregues ao destinatário. O processo de colocar um formato de mensagem (a carta) em outro formato de mensagem (o envelope) é chamado encapsulamento. Pronto para saber mais? Aproveite este módulo!

## 7.0.2 O que vou aprender neste módulo?

**Titulo do Módulo:** A Camada de Acesso

**Objetivo do Módulo:** Explicar como ocorre a comunicação em redes Ethernet.

|Titulo do Tópico|Objetivo do Tópico|
|---|---|
|Encapsulamento e o quadro Ethernet|Explicar o processo de encapsulamento e o enquadramento Ethernet.|
|A Camada de Acesso|Explicar como melhorar a comunicação de rede na camada de acesso.|

# 7.1 Encapsulamento e o quadro Ethernet

## 7.1.1 Vídeo - Os campos do quadro Ethernet
![[7.1.1.mp4#subtitle=anexos/7.1.1.vtt]]
Ethernet é a tecnologia mais usada em redes locais. Os dispositivos usam um NIC (Network Interface Card, placa de interface de rede) Ethernet para acessar a LAN Ethernet. Cada NIC Ethernet tem um endereço único incorporado permanentemente à placa que é conhecido como endereço MAC (Media Access Control). O endereço MAC da origem e do destino são campos em um quadro Ethernet.

#### Vídeo

Neste vídeo, vamos apresentar os campos de um quadro Ethernet. Lembre-se de que Ethernet é da placa de interface de rede à placa de interface de rede, na mesma rede.

E para mencionar, veja esses números abaixo aqui — estes são o número de bytes para cada um desses campos. Se você quiser traduzir isso em bits, basta multiplicar cada um desses números por oito, e ele lhe dará o número de bits.

Assim, o primeiro campo é o preâmbulo. Isso é usado apenas para obter sincronização de bits entre a placa NIC e a NIC do receptor que estão vindo pelo cabo.

O delimitador de início de quadro indica para a placa de interface de rede receptora que, após este delimitador de início de quadro, virá a informação real associada com o quadro Ethernet.

Em seguida, temos o endereço MAC de destino. O endereço mac de destino é o endereço MAC do destino nessa rede. Então esse é o endereço MAC da placa NIC para onde esse quadro Ethernet irá.

O endereço MAC de origem é o endereço MAC do dispositivo que originou este quadro Ethernet, o endereço MAC da placa de interface de rede, o NIC Ethernet, que originou este quadro Ethernet.

Em seguida, temos o comprimento, ou campo de tipo. Portanto, este campo aqui pode ser uma das duas coisas: pode ser o comprimento, e esse seria o comprimento dos dados, o que às vezes chamamos de carga útil, quantos bytes estão na porção de dados deste quadro Ethernet; ou pode ser um campo de tipo que diz que tipo de dados são esses — este é um pacote IPv4, este é um pacote IPv6.

Em seguida, estão os dados encapsulados reais. Este pode ser um pacote IPv4, poderia ser um pacote IPv6, e então, junto com o pacote IPv4, digamos, poderia ser outros protocolos também. Pode ser todos os dados, pode ser o pacote IPv4 com o cabeçalho TCP ou junto com o cabeçalho HTTP, ou qualquer informação que tenha sido encapsulada. E na verdade a Ethernet não se importa que tipo de dados são — está apenas entregando esses dados da placa de interface de rede para a placa de interface de rede.

Por último, temos o que é conhecido como FCS, sequência de verificação de quadros. Isso é usado pelo dispositivo receptor para fazer alguma verificação de erros, para ter certeza que não houve erros ao longo do caminho na transmissão.

## 7.1.2 Encapsulamento

Ao enviar uma carta, quem a escreve usa um formato aceito para garantir que ela seja entregue e compreendida pelo destinatário. Da mesma forma, a mensagem enviada por uma rede de computadores segue regras específicas de formato para que seja entregue e processada.

O processo de colocar um formato de mensagem (a carta) em outro formato de mensagem (o envelope) é chamado encapsulamento. O desencapsulamento ocorre quando o processo é invertido pelo destinatário e a carta é retirada do envelope. Assim como uma carta é colocada dentro de um envelope para ser entregue, no caso das mensagens de computador, elas são encapsuladas.

Cada mensagem de computador é encapsulada em um formato específico, chamado de quadro, antes de ser enviada pela rede. Um quadro atua como um envelope: ele fornece o endereço do destino desejado e o endereço do host de origem. O formato e o conteúdo de um quadro são determinados pelo tipo de mensagem que está sendo enviada e pelo canal no qual é comunicada. As mensagens que não são formatadas corretamente não são entregues ao host destino com êxito, nem processadas por ele.

### Analogia

Um exemplo comum de exigir o uso de formato correto nas comunicações humanas é o que ocorre ao enviar uma carta. Clique em Reproduzir na figura para exibir uma animação de formatação e encapsulamento de uma carta.

Um envelope tem o endereço do remetente e do destinatário, cada um localizado no local apropriado do envelope. Se o endereço de destino e a formatação não estiverem corretos, a carta não será entregue.

O processo de colocar um formato de mensagem (a carta) em outro formato de mensagem (o envelope) é chamado encapsulamento. O desencapsulamento ocorre quando o processo é invertido pelo destinatário e a carta é retirada do envelope.
![[brave_PWuJbbPo7Q.mp4]]

---
### Rede

Semelhante ao envio de uma carta, uma mensagem enviada por uma rede de computadores segue regras específicas de formato para que ela seja entregue e processada.

Internet Protocol (IP) é um protocolo com uma função semelhante ao exemplo de envelope. Na figura, os campos do pacote IPv6 (Internet Protocol versão 6) identificam a origem do pacote e seu destino. O IP é responsável por enviar uma mensagem da origem para o destino através de uma ou mais redes.

**Nota:** Os campos do pacote IPv6 são discutidos em detalhes em outro módulo.
#### Estrutura do pacote IPv6 — 40 bytes

<svg viewBox="0 0 600 280" xmlns="http://www.w3.org/2000/svg" style="width:100%; font-family:sans-serif; font-size:13px; color:white;">

  <!-- Header row -->
  <rect x="0" y="0" width="75" height="30" fill="none" stroke="#888"/>
  <rect x="75" y="0" width="175" height="30" fill="none" stroke="#888"/>
  <rect x="250" y="0" width="175" height="30" fill="none" stroke="#888"/>
  <rect x="425" y="0" width="175" height="30" fill="none" stroke="#888"/>
  <text x="37" y="20" text-anchor="middle" font-weight="bold" fill="white">Byte 1</text>
  <text x="162" y="20" text-anchor="middle" font-weight="bold" fill="white">Byte 2</text>
  <text x="337" y="20" text-anchor="middle" font-weight="bold" fill="white">Byte 3d</text>
  <text x="512" y="20" text-anchor="middle" font-weight="bold" fill="white">Byte 4</text>

  <!-- Row 1 -->
  <rect x="0"   y="30" width="40"  height="30" fill="none" stroke="#888"/>
  <rect x="40"  y="30" width="160" height="30" fill="none" stroke="#888"/>
  <rect x="200" y="30" width="400" height="30" fill="none" stroke="#888"/>
  <text x="20"  y="50" text-anchor="middle" fill="white">Versão</text>
  <text x="120" y="50" text-anchor="middle" fill="white">Classe de tráfego</text>
  <text x="400" y="50" text-anchor="middle" fill="white">Rótulo de fluxo</text>

  <!-- Row 2 -->
  <rect x="0"   y="60" width="250" height="30" fill="none" stroke="#888"/>
  <rect x="250" y="60" width="175" height="30" fill="none" stroke="#888"/>
  <rect x="425" y="60" width="175" height="30" fill="none" stroke="#888"/>
  <text x="125" y="80" text-anchor="middle" fill="white">Tamanho da carga</text>
  <text x="337" y="80" text-anchor="middle" fill="white">Próximo cabeçalho</text>
  <text x="512" y="80" text-anchor="middle" fill="white">Limite de saltos</text>

  <!-- Row 3 -->
  <rect x="0" y="90" width="600" height="55" fill="none" stroke="#888"/>
  <text x="300" y="122" text-anchor="middle" fill="white">Endereço IP de origem</text>

  <!-- Row 4 -->
  <rect x="0" y="145" width="600" height="55" fill="none" stroke="#888"/>
  <text x="300" y="177" text-anchor="middle" fill="white">Endereço IP de destino</text>

  <!-- Row 5 -->
  <rect x="0" y="200" width="600" height="25" fill="none" stroke="#888"/>
  <text x="590" y="217" text-anchor="end" font-style="italic" fill="white">↕ 40 bytes</text>

</svg>
![[Pasted image 20260717233104.png]]
## 7.1.3 Verifique sua compreensão - Encapsulamento e o quadro Ethernet

### Pergunta 1

O processo de anexar informações de protocolo com informações de outro protocolo é chamado:

- [ ] enquadramento
- [x] encapsulamento
- [ ] codificação
- [ ] empacotamento

✅ RESPOSTA CORRETA: encapsulamento

> Encapsulamento é o processo de anexar um prefixo de informações de protocolo, com informações de outro protocolo.

---

### Pergunta 2

Quando um quadro Ethernet é enviado, o endereço MAC de destino indica:

- [x] O endereço MAC do dispositivo, que está nesta rede, que receberá o quadro Ethernet.
- [ ] O endereço MAC do roteador
- [ ] O endereço MAC da placa de rede (NIC) de um dispositivo que esteja nesta rede ou em outra rede e que receberá o quadro Ethernet.
- [ ] O endereço MAC da placa de rede (NIC) do dispositivo que enviou o quadro Ethernet.

✅ RESPOSTA CORRETA: O endereço MAC do dispositivo, que está nesta rede, que receberá o quadro Ethernet.

> Quando um quadro Ethernet é enviado em uma interface, o endereço MAC de destino indica o endereço MAC do dispositivo, que está nesta rede e que receberá o quadro Ethernet.

---

### Pergunta 3

Qual campo do quadro Ethernet indica o inicio de um quadro Ethernet?

- [x] Preâmbulo e SFD
- [ ] Endereço MAC de destino
- [ ] Tipo/tamanho
- [ ] FCS

✅ RESPOSTA CORRETA: Preâmbulo e SFD

> O preâmbulo e o Delimitador de Início de Quadro (SFD- Start Frame Delimiter) indicam o início de um quadro Ethernet.

---

### Pergunta 4

O protocolo Ethernet está em qual camada do modelo OSI?

- [x] Camada 2 Enlace de dados
- [ ] Camada 1 Física
- [ ] Camada 4 Transporte
- [ ] Camada 3 Rede

✅ RESPOSTA CORRETA: Camada 2 Enlace de dados

> Ethernet opera na camada 2, a camada de enlace de dados do modelo OSI.


# 7.2 A Camada de Acesso

## 7.2.1 Vídeo - Switches Ethernet
![[7.2.1.mp4#subtitle=anexos/7.2.1.vtt]]
Neste vídeo, vamos dar uma olhada como funcionam os switches Ethernet. Os switches Ethernet operam na camada dois, camada de enlace de dados do modelo OSI. Isso porque eles tomam suas decisões de encaminhamento com base nas informações da camada dois, as informações do cabeçalho Ethernet, do quadro Ethernet.

Os switches Ethernet possuem tabelas de endereços MAC. Neste exemplo, a tabela de endereços MAC já está totalmente preenchido. Aprenderemos em um vídeo posterior como a tabela de endereços MAC é construída. Mas vamos ver como um switch usa essa informação.

Aqui temos quatro hosts, H1 a H4. Eu tenho em cada host um endereço MAC abreviado, como AAAA para o host um. Esse é o endereço MAC de sua NIC Ethernet.

Então, se H1 vai enviar um quadro Ethernet para H4, bem, ele constrói um quadro Ethernet com o endereço MAC de origem o seu próprio endereço MAC. Então, no endereço MAC de origem, colocaremos AAAA, o endereço MAC de H1, e o endereço MAC de destino será o de H4, DDDD. Mais uma vez, estes são apenas endereços MAC abreviados.

Então, este quadro Ethernet é encaminhado por H1 e é recebido no switch em sua porta Ethernet, Fast Ethernet zero um. O switch, aprenderemos mais tarde como ele constrói esta tabela, mas para encaminhar as informações, ele olha para o endereço MAC de destino do quadro Ethernet. O endereço MAC de destino é DDDD. Então, ele olha em sua tabela de endereços MAC para esse endereço MAC e aqui está, DDDD, que está na porta FA, Fast Ethernet, zero quatro. Assim, o switch encaminhará este quadro apenas para a Fast Ethernet zero quatro em direção ao destino.

## 7.2.2 Vídeo - Tabela de Endereços MAC
![[7.2.2.mp4#subtitle=anexos/7.2.2.vtt]]
Neste vídeo, vamos dar uma olhada em como um switch constrói sua tabela de endereços MAC. Mais uma vez, um switch faz sua decisão de encaminhamento com base nas informações da camada dois, neste caso as informações do cabeçalho Ethernet do quadro Ethernet.

Então, vamos dar uma olhada em como esse switch constrói sua tabela de endereços MAC. Nesses quatro hosts, abreviei endereços MAC AA-AA até DD-DD.

Então aqui vamos ter H1 envia um quadro Ethernet para H4, então o endereço MAC de origem será AA-AA, o endereço MAC da NIC Ethernet do H1, e o endereço de destino será aquele da NIC Ethernet do H4, DD-DD.

Ok, então H1 envia esse quadro para o switch Ethernet. Quando o switch recebe qualquer quadro Ethernet, a primeira coisa que faz é olhar para o endereço MAC de origem e dizer "Eu aprendi alguma coisa?" O que está olhando, e vê isso na porta Fast Ethernet 01, é o endereço MAC de origem AA-AA. Isso existe em sua tabela? E vê, diz não, não — e porque ainda não existe, adiciona este MAC de origem a sua porta de entrada fast Ethernet 01.

Então é assim que o switch constrói sua tabela. Agora ele quer ir em frente e encaminhar o quadro. Então agora ele olha para o endereço MAC de destino. Ele diz "Este endereço MAC está na minha tabela?" e como podemos ver, DD-DD não está em sua tabela.

Isso é conhecido como um unicast desconhecido. Da perspectiva do switch, é como, eu não sabia para onde enviá-lo, então o que ele faz — ele age como os antigos hubs Ethernet. Na verdade, ele irá enviá-lo para todas as portas exceto a porta de entrada. Assim, cada um desses dispositivos receberá este quadro Ethernet.

Quando H2 o recebe, em sua placa Ethernet NIC compara seu endereço MAC com o endereço MAC de destino do quadro Ethernet e diz "não combinamos". Assim, ele ignora o resto do quadro. Veja, o H3 faz a mesma coisa — meu endereço MAC não corresponde ao endereço MAC do MAC de destino, ignore o quadro. H4, ao receber este quadro Ethernet, sua placa Ethernet NIC diz "Sim, esse é o meu endereço MAC. Nós combinamos." Então ele vai em frente e recebe todo o quadro.

Agora vamos ver o que acontece quando o DD envia um quadro Ethernet de volta para AA-AA, ou H4 envia um quadro Ethernet para H1. Então, neste caso, temos H4 como fonte e o destino é H1.

Agora até agora, esta é a tabela de endereços MAC do nosso switch. Então H4 envia o quadro Ethernet, que é recebido na porta fast Ethernet 04 pelo switch. Lembre-se, a primeira coisa que um switch faz é querer aprender. Ele examina o endereço MAC de origem e diz "Aprendi algo novo? Como recebi este endereço MAC de origem na minha porta, fast Ethernet 04. Não está na minha tabela de endereços MAC." Então ele adiciona o endereço MAC.

Em seguida, preciso encaminhar o quadro. Eu sei onde está o endereço MAC de destino? Ele olha e diz "Sim, eu sei que está na minha porta Fast Ethernet 01." Então ele vai em frente, neste caso ele sabe onde está o endereço MAC de destino e pode filtrar o quadro e apenas enviá-lo para a porta única.

Assim você pode ver como os switches Ethernet constroem suas tabelas, aprender sobre onde estão os endereços MAC de origem Ethernet, e então pode começar a filtrar esses quadros para portas específicas.

Vamos dar uma olhada final aqui em outro quadro indo de H1 para H4 e veja como as coisas mudaram agora. Se H1 tiver outro quadro para enviar de volta para H4, o endereço MAC de origem é AA-AA, o endereço MAC de destino é DD-DD — e vamos dar uma olhada na diferença desde a primeira vez que isso aconteceu.

O quadro entra no switch, a porta diz "Eu sei sobre este endereço MAC de origem em Fast Ethernet 01?" Ele diz "sim, eu aprendi sobre isso anteriormente." Então, os switches tendem a manter essas informações lá por cerca de cinco minutos. Ele diz tudo bem, eu aprendi isso, sem problemas. Que tal encaminhar o quadro? Para onde vou enviar? Então ele olha para o endereço MAC de destino e diz "Eu sei onde DD-DD está? Desta vez, eu sei. Está aqui na porta Fast Ethernet 04." Então, em vez de enviar todas as portas como fizemos originalmente, quando esta informação não estava aqui, agora ele pode enviar apenas fast Ethernet 04 a caminho do H4.

## 7.2.3 Verifique a sua compreensão - A camada de acesso

### Pergunta 1

Os switches Ethernet tomam a decisão de encaminhamento com base em qual campo do quadro Ethernet?

- [ ] SFD (Delimitador de Início de Quadro)
- [ ] FCS
- [x] Endereço MAC destino
- [ ] Endereço MAC origem
- [ ] Tipo/tamanho

✅ RESPOSTA CORRETA: Endereço MAC destino

> Os switches Ethernet tomam sua decisão de encaminhamento com base no endereço MAC de destino.

---

### Pergunta 2

Os switches Ethernet adicionam entradas à tabela de endereços MAC com base em qual campo do quadro Ethernet?

- [ ] endereço MAC destino
- [ ] Tipo/tamanho
- [ ] FCS
- [ ] SFD (Delimitador de Início de Quadro)
- [x] Endereço MAC origem

✅ RESPOSTA CORRETA: Endereço MAC origem

> Os switches Ethernet adicionam entradas à sua tabela de endereços MAC com base no endereço MAC de origem.

---

### Pergunta 3

Quando um switch recebe um quadro Ethernet e o endereço MAC de destino desse quadro não está em sua tabela de endereços MAC, o switch:

- [x] Encaminha o quadro para todas as portas de saída exceto a porta pela qual recebeu o quadro
- [ ] Adiciona o endereço MAC de origem à tabela
- [ ] Descarta o quadro.
- [ ] Adciiona o endereço MAC de destino à tabela

✅ RESPOSTA CORRETA: Encaminha o quadro para todas as portas de saída exceto a porta pela qual recebeu o quadro

> Ao receber um quadro de entrada com um endereço MAC de destino que não está listado na tabela de endereços MAC, o switch encaminha o quadro para todas as portas, exceto para a porta de entrada do quadro.

---

### Pergunta 4

Os hubs Ethernet são considerados:

- [ ] inovadores
- [ ] um dispositivo de segurança
- [x] Obsoletos
- [ ] um dispositivo sem fio

✅ RESPOSTA CORRETA: Obsoletos

> Os hubs Ethernet são considerados obsoletos.



# 7.3 Resumo: Camada de Acesso

## 7.3.1 O que aprendi neste módulo?

### Encapsulamento e o quadro Ethernet

O processo de colocar um formato de mensagem dentro de outro formato de mensagem é chamado de encapsulamento. O desencapsulamento ocorre quando o processo é invertido pelo destinatário e a carta é retirada do envelope. Assim como uma carta é colocada dentro de um envelope para ser entregue, no caso das mensagens de computador, elas são encapsuladas. Uma mensagem enviada por uma rede de computadores segue regras específicas de formato para que seja entregue e processada.

Os padrões do protocolo Ethernet definem muitos aspectos da comunicação de rede, como o formato e o tamanho do quadro, a temporização e a codificação. O formato dos quadros Ethernet especifica a localização dos endereços MAC de destino e de origem e informações adicionais, incluindo preâmbulo para sequenciamento e temporização, início do delimitador de quadro, comprimento e tipo de quadro e sequência de verificação de quadro para detectar erros de transmissão.

---

### A Camada de Acesso

É a parte da rede em que as pessoas recebem acesso a outros hosts e a arquivos compartilhados e impressoras. A camada de acesso atua como a primeira linha nos dispositivos de rede que conectam hosts à rede Ethernet com fio. Em uma rede Ethernet, cada host pode se conectar diretamente a um dispositivo de rede da camada de acesso usando um cabo Ethernet. Os hubs Ethernet contêm várias portas que são usadas para conectar hosts à rede. Apenas uma mensagem de cada vez pode ser enviada por um hub Ethernet. Duas ou mais mensagens enviadas ao mesmo tempo causarão um colisão. Como retransmissões excessivas podem congestionar a rede e reduzir o tráfego, os hubs passaram a ser considerados obsoletos e foram substituídos por switches Ethernet.

Um switch Ethernet é um dispositivo usado na camada 2. Quando um host envia uma mensagem para outro host conectado à mesma rede comutada, o switch aceita e decodifica os quadros para ler a parte do endereço MAC da mensagem. Uma tabela no switch, chamada de tabela de endereços MAC, contém uma lista de todas as portas ativas e dos endereços MAC de host conectados a elas. Quando uma mensagem é enviada entre hosts, o switch verifica se o endereço MAC de destino está na tabela. Se estiver, o switch criará uma conexão temporária, chamada de circuito, entre as portas de origem e de destino. Os switches Ethernet também permitem o envio e o recebimento de quadros no mesmo cabo Ethernet simultaneamente. Isso melhora o desempenho da rede eliminando colisões.

Um switch cria a tabela de endereços MAC examinando o endereço MAC de origem de cada quadro enviado entre hosts. Quando um novo host envia uma mensagem ou responde a uma mensagem inundada, o switch descobre imediatamente o endereço MAC e a porta à qual ele está conectado. A tabela é atualizada dinamicamente toda vez que um novo endereço MAC de origem é lido pelo switch.

## 7.3.2 Webster – Questões para Reflexão

Há muita coisa acontecendo nos bastidores quando envio um e-mail a um amigo. Muito mais do que eu sabia! Os dados são encapsulados quando eu envio um e-mail e, em seguida, são desencapsulados quando meu amigo abre o e-mail. A camada de acesso do modelo OSI é onde tudo isso acontece. Agora que você conhece o encapsulamento e a camada de acesso, o que mais você faz em seu computador, tablet ou smartphone que requer encapsulamento e os protocolos usados na camada de acesso?


## 7.3.3 Quiz sobre a Camada de Acesso

### Pergunta 1

O que um switch de Camada 2 fará quando o endereço MAC de destino de um quadro recebido não estiver na tabela MAC?

- [ ] Ele inicia uma solicitação ARP.
- [ ] Ele transmite o quadro em broadcast, para fora, por todas as portas do switch.
- [ ] Ele notifica o host, que originou o envio, de que o quadro não pode ser entregue.
- [x] Encaminha o quadro para todas as portas, exceto a porta na qual o quadro foi recebido.

✅ RESPOSTA CORRETA: Encaminha o quadro para todas as portas, exceto a porta na qual o quadro foi recebido.

---

### Pergunta 2

Qual dispositivo de rede tem a função principal de enviar dados para um destino específico com base nas informações encontradas na tabela de endereços MAC?

- [ ] hub
- [ ] roteador
- [x] switch
- [ ] modem

✅ RESPOSTA CORRETA: switch

---

### Pergunta 3

Que informações de endereçamento são registradas por um switch para construir sua tabela de endereços MAC?

- [ ] o endereço destino da camada 3 dos pacotes recebidos
- [ ] o endereço destino da camada 2 dos quadros enviados
- [ ] o endereço origem da camada 3 dos pacotes enviados
- [x] o endereço origem da camada 2 dos quadros recebidos

✅ RESPOSTA CORRETA: o endereço origem da camada 2 dos quadros recebidos

---

### Pergunta 4

Qual é a finalidade do campo FCS em um quadro?

- [ ] para obter o endereço MAC do nó remetente
- [ ] para verificar o endereço lógico do nó de envio
- [ ] para calcular o cabeçalho CRC do campo de dados
- [x] para determinar se ocorreram erros na transmissão e recepção

✅ RESPOSTA CORRETA: para determinar se ocorreram erros na transmissão e recepção

---

### Pergunta 5

Qual é uma função de um switch de Camada 2?

- [ ] encaminha dados com base em endereçamento lógico
- [ ] duplica o sinal elétrico de cada quadro para cada porta
- [ ] aprende a porta atribuída a um host examinando o endereço MAC de destino
- [x] determina qual interface é usada para encaminhar um quadro com base no endereço MAC de destino

✅ RESPOSTA CORRETA: determina qual interface é usada para encaminhar um quadro com base no endereço MAC de destino

---

### Pergunta 6

Quais informações um switch usa para manter as informações da tabela de endereços MAC atualizadas?

- [ ] o endereço MAC de destino e a porta de entrada
- [ ] o endereço MAC de destino e a porta de saída
- [ ] os endereços MAC de origem e destino e a porta de entrada
- [ ] os endereços MAC de origem e destino e a porta de saída
- [x] o endereço MAC de origem e a porta de entrada

✅ RESPOSTA CORRETA: o endereço MAC de origem e a porta de entrada

---

### Pergunta 7

Qual é o processo usado para inserir uma mensagem dentro de outra mensagem para a transferência da origem para o destino?

- [ ] controle de acesso
- [ ] decodificação
- [x] encapsulamento
- [ ] controle de fluxo
- [ ] o endereço MAC de origem e a porta de entrada

✅ RESPOSTA CORRETA: encapsulamento

---

### Pergunta 8

Consulte a figura. A figura mostra uma pequena rede comutada e o conteúdo da tabela de endereços MAC do switch. O PC1 enviou um quadro com destino a PC3. O que o switch fará com o quadro?

**Tabela de Endereços MAC do switch:**

|Porta|Endereço MAC|
|---|---|
|1|12-34-56-78-9A-BF|
|3|12-34-56-78-9A-BD|

**Endereços MAC dos hosts:**

- PC1: 12-34-56-78-9A-BC (porta 4)
    
- PC2: 12-34-56-78-9A-BD (porta 3)
    
- PC3: 12-34-56-78-9A-BE (porta 2)
    
- PC4: 12-34-56-78-9A-BF (porta 1)
    
- [ ] O switch descartará o quadro.
    
- [ ] O switch encaminhará o quadro somente para a porta 2.
    
- [x] O switch encaminhará o quadro para todas as portas, exceto a porta 4.
    
- [ ] O switch encaminhará o quadro para todas as portas.
    
- [ ] O switch encaminhará o quadro apenas para as portas 1 e 3.
    

✅ RESPOSTA CORRETA: O switch encaminhará o quadro para todas as portas, exceto a porta 4.

---

### Pergunta 9

Quais são os três campos encontrados em um quadro Ethernet 802.3? (Escolha três.)

- [x] endereço físico de origem
- [ ] endereço lógico de origem
- [ ] identificador do tipo de mídia
- [x] sequência de verificação de quadro (FCS)
- [x] endereço físico de destino
- [ ] endereço lógico de destino

✅ RESPOSTAS CORRETAS: endereço físico de origem, sequência de verificação de quadro (FCS), endereço físico de destino

---

### Pergunta 10

O que um host em uma rede Ethernet fará se receber um quadro com um endereço MAC de destino unicast que não corresponde ao seu próprio endereço MAC?

- [x] Ele descartará o quadro.
- [ ] Ele encaminhará o quadro para o próximo host.
- [ ] Ele removerá o quadro da mídia.
- [ ] Ele removerá o quadro de link de dados para verificar o endereço IP de destino.

✅ RESPOSTA CORRETA: Ele descartará o quadro.

---

### Pergunta 11

Qual das afirmativas abaixo, relacionada a decisões de encaminhamento dos quadros de switch da Ethernet, está correta?

- [x] As decisões de encaminhamento de quadros são baseadas no endereço MAC e nos mapeamentos de porta na tabela de endereços MAC.
- [ ] Os quadros endereçados a endereços MAC desconhecidos são descartados.
- [ ] Os switches constroem suas tabelas de endereços MAC com base no endereço MAC de destino dos quadros de entrada.
- [ ] Os quadros unicast são sempre encaminhados, independentemente do endereço MAC de destino.

✅ RESPOSTA CORRETA: As decisões de encaminhamento de quadros são baseadas no endereço MAC e nos mapeamentos de porta na tabela de endereços MAC.


# Exame de ponto de verificação

### Pergunta 1

Qual afirmação é verdadeira sobre os modelos TCP/IP e OSI?

- [ ] A camada de acesso à rede TCP/IP tem funções semelhantes à camada de rede OSI.
- [x] A camada de transporte TCP/IP e a Camada OSI 4 fornecem serviços e funções semelhantes.
- [ ] As três primeiras camadas do modelo OSI descrevem serviços gerais que também são fornecidos pela camada de Internet do modelo TCP/IP.
- [ ] A camada 7 do modelo OSI e a camada de aplicação do modelo TCP/IP têm funções idênticas.

✅ RESPOSTA CORRETA: A camada de transporte TCP/IP e a Camada OSI 4 fornecem serviços e funções semelhantes.

---

### Pergunta 2

Quais são as três camadas de modelos OSI que correspondem à camada de aplicação do modelo TCP/IP? (Escolha três.)

- [ ] enlace de dados
- [ ] rede
- [ ] Transporte
- [x] Apresentação
- [x] sessão
- [x] Aplicação

✅ RESPOSTAS CORRETAS: Apresentação, sessão, Aplicação

---

### Pergunta 3

Quais são as duas camadas do modelo OSI que têm a mesma funcionalidade no modelo TCP/IP? (Escolha dois.)

- [ ] transporte
- [x] físico
- [ ] rede
- [ ] sessão
- [x] enlace de dados

✅ RESPOSTAS CORRETAS: físico, enlace de dados

---

### Pergunta 4

Quais são os três acrônimos/siglas que representam as organizações padronizadoras? (Escolha três.)

- [ ] MAC
- [x] IETF
- [ ] OSI
- [x] IANA
- [ ] TCP/IP
- [x] IEEE

✅ RESPOSTAS CORRETAS: IETF, IANA, IEEE

---

### Pergunta 5

Qual afirmação define um protocolo de comunicações de dados?

- [ ] uma parceria de fabricantes de dispositivos de rede
- [x] um conjunto de regras que regem o processo de comunicação
- [ ] um acordo de troca de dispositivos de rede entre fornecedores
- [ ] um conjunto de padrões de produto para tipos de dispositivos de rede

✅ RESPOSTA CORRETA: um conjunto de regras que regem o processo de comunicação

---

### Pergunta 6

Quais são os três elementos comuns a todos os métodos de comunicação? (Escolha três.)

- [x] origem da mensagem
- [x] meio de transmissão comum
- [ ] dados da mensagem
- [x] destino da mensagem
- [ ] tipo de mensagem
- [ ] prioridade da mensagem

✅ RESPOSTAS CORRETAS: origem da mensagem, meio de transmissão comum, destino da mensagem

---

### Pergunta 7

Combine a função do protocolo com a descrição, levando em consideração que um cliente de rede está visitando um site.

|Categoria|Resposta correta|
|---|---|
|preparando pacotes a serem transmitidos pela mídia de rede|protocolo de acesso à rede|
|tomando os segmentos do Protocolo de Transporte, encapsulando-os em pacotes e atribuindo-os com endereços apropriados|protocolo de internet|
|governando a maneira como um servidor web e um cliente web interagem|protocolo de aplicação|
|gerenciando as conversas individuais entre servidores Web e clientes Web|protocolo de transporte|

---

### Pergunta 8

Quais são as duas características que descrevem um cabo Ethernet? (Escolha duas.)

- [ ] único núcleo de cobre envolto por uma camada de isolamento
- [x] 4 pares de cabos trançados
- [x] pares de cabos codificados por cor
- [ ] núcleo de vidro cercado por várias camadas para isolamento e proteção
- [ ] núcleo de plástico cercado por várias camadas para isolamento e proteção

✅ RESPOSTAS CORRETAS: 4 pares de cabos trançados, pares de cabos codificados por cor

---

### Pergunta 9

Que tipo de cabo de rede é usado normalmente em redes de backbone e em companhias telefônicas?

- [ ] cabo de par trançado blindado
- [x] cabo de fibra ótica
- [ ] cabo de par trançado
- [ ] cabo coaxial

✅ RESPOSTA CORRETA: cabo de fibra ótica

---

### Pergunta 10

Um técnico de rede está pesquisando o uso do cabeamento de fibra óptica em um novo centro de tecnologia. Quais duas questões devem ser consideradas antes de implementar meios de fibra óptica? (Escolha duas.)

- [ ] O cabo de fibra óptica é capaz de suportar manuseio brusco.
- [ ] O cabeamento de fibra óptica é suscetível à perda de sinal devido ao RFI.
- [x] A fibra óptica fornece maior capacidade de dados, mas é mais cara do que o cabeamento de cobre.
- [ ] O cabeamento de fibra óptica requer aterramento específico para ser imune à EMI.
- [x] O cabeamento de fibra ótica requer uma especialização em terminação e emenda diferente do que o cabeamento de cobre exige.

✅ RESPOSTAS CORRETAS: A fibra óptica fornece maior capacidade de dados, mas é mais cara do que o cabeamento de cobre. / O cabeamento de fibra ótica requer uma especialização em terminação e emenda diferente do que o cabeamento de cobre exige.

---

### Pergunta 11

Consulte o gráfico. Que tipo de cabeamento é mostrado?

- [ ] coaxial
- [ ] fibra óptica em plástico
- [x] par trançado
- [ ] fibra óptica de vidro

✅ RESPOSTA CORRETA: par trançado

---

### Pergunta 12

Qual critério pode ser usado para selecionar o tipo apropriado de mídia de rede para uma rede?

- [ ] o número de dispositivos intermediários instalados na rede
- [ ] o custo dos dispositivos finais usados na rede
- [ ] os tipos de dados que precisam ter prioridade
- [x] o ambiente em que a mídia selecionada será instalada

✅ RESPOSTA CORRETA: o ambiente em que a mídia selecionada será instalada

---

### Pergunta 13

Qual tecnologia de codificação de dados é usada em cabos de fibra óptica?

- [ ] modulação da tensão elétrica
- [ ] pulsos elétricos
- [ ] modulação de frequências específicas de ondas eletromagnéticas
- [x] pulsos de luz

✅ RESPOSTA CORRETA: pulsos de luz

---

### Pergunta 14

Qual é a vantagem de usar cabeamento de fibra óptica em vez de cabeamento de cobre?

- [ ] Pode ser instalado em curvas fechadas.
- [ ] Geralmente é mais barato do que o cabeamento de cobre.
- [x] Ele é capaz de transportar sinais muito mais longe do que o cabeamento de cobre.
- [ ] É mais fácil terminar e instalar do que o cabeamento de cobre.

✅ RESPOSTA CORRETA: Ele é capaz de transportar sinais muito mais longe do que o cabeamento de cobre.

---

### Pergunta 15

Qual termo se refere ao processo de inserir um formato de mensagem em outro formato de mensagem?

- [x] encapsulamento
- [ ] segmentação
- [ ] codificação
- [ ] manipulação

✅ RESPOSTA CORRETA: encapsulamento

---

### Pergunta 16

Consulte a figura. Um PC com o endereço MAC 0800.069d.3841 ligado à porta Fa0/8 está enviando dados para um dispositivo que tenha o endereço MAC 6400.6a5a.6821. O que o switch fará primeiro para lidar com a transferência de dados?

**Tabela de Endereço MAC:**

```
SW_B1_F2# show mac-address-table
          Tabela de Endereço MAC
----------------------------------------------------------
Vlan  Endereço MAC       Tipo      Portos
----  ---------          -------   ------
1     0001.42ee.4ae7     DYNAMIC   Fa0/4
1     6400.6a5a.6821     DYNAMIC   Fa0/6
```

- [ ] O switch enviará o quadro para a porta Fa0/6.
- [ ] O switch adicionará o endereço 6400.6151.6821 à tabela de endereços MAC.
- [x] O switch adicionará o endereço 0800.069d.3841 à tabela de endereços MAC.
- [ ] O switch inundará o quadro em todas as portas, exceto na porta Fa0/8.
- [ ] O switch enviará o quadro para as portas Fa0/4 e Fa0/6.

✅ RESPOSTA CORRETA: O switch adicionará o endereço 0800.069d.3841 à tabela de endereços MAC.

---

### Pergunta 17

Qual é o tipo de endereço é usado por um switch na construção de uma tabela de endereços MAC?

- [ ] endereço MAC destino
- [ ] endereço IP origem
- [x] Endereço MAC origem
- [ ] endereço IP destino

✅ RESPOSTA CORRETA: Endereço MAC origem

---

### Pergunta 18

Qual a quantidade de dados que podem ser encapsulados em um quadro Ethernet, de tamanho normal, antes de serem enviados pela rede?

- [ ] 0 a 1024 bytes
- [ ] de 32 a 1500 bytes
- [ ] de 64 a 1518 bytes
- [x] de 46 a 1500 bytes

✅ RESPOSTA CORRETA: de 46 a 1500 bytes

---

### Pergunta 19

Consulte a figura. Como um quadro é enviado do PC A para o PC C se a tabela de endereço MAC no switch SW1 está vazia?

**Topologia:**

- SW1: Fa0/1 → PCA, Fa0/2 → PCB, Fa0/23 → SW2
    
- SW2: Fa0/24 → SW1, Fa0/3 → PCC, Fa0/4 → PCD
    
- [x] O SW1 inunda o quadro em todas as portas no SW1, excluindo a porta pela qual o quadro entrou no switch.
    
- [ ] O SW1 encaminha o quadro diretamente para o SW2. O SW2 inunda o quadro em todas as portas conectadas ao SW2, excluindo a porta pela qual o quadro entrou no switch.
    
- [ ] O SW1 descarta o quadro porque não sabe o endereço MAC de destino.
    
- [ ] O SW1 inunda o quadro em todas as portas do switch, excluindo a porta interconectada do switch SW2 e a porta através da qual o quadro entrou no switch.
    

✅ RESPOSTA CORRETA: O SW1 inunda o quadro em todas as portas no SW1, excluindo a porta pela qual o quadro entrou no switch.

---

### Pergunta 20

Quais são duas ações executadas por um switch Cisco? (Escolha duas.)

- [ ] examinar o endereço MAC destino para adicionar novas entrada à tabela de endereços MAC
- [ ] criar uma tabela de roteamento com base no primeiro endereço IP no cabeçalho do quadro
- [x] usar a tabela de endereços MAC para encaminhar quadros via endereço MAC de destino
- [x] usar os endereços MAC origem dos quadros para criar e manter um tabela de endereços MAC
- [ ] encaminhar quadros com endereços IP de destino desconhecidos para o gateway padrão

✅ RESPOSTAS CORRETAS: usar a tabela de endereços MAC para encaminhar quadros via endereço MAC de destino / usar os endereços MAC origem dos quadros para criar e manter um tabela de endereços MAC

### Pergunta 21

Qual informação um switch usa para povoar a tabela de endereços MAC?

- [x] o endereço MAC de origem e a porta de entrada
- [ ] o endereço MAC de destino e a porta de entrada
- [ ] os endereços MAC de origem e destino e a porta de saída
- [ ] o endereço MAC de destino e a porta de saída
- [ ] o endereço MAC de origem e a porta de saída
- [ ] os endereços MAC de origem e destino e a porta de entrada

✅ RESPOSTA CORRETA: o endereço MAC de origem e a porta de entrada