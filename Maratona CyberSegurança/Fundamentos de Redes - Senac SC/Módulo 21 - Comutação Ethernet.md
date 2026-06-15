
# 21.0 Introdução

## 21.0.1 Webster - Por que devo fazer este módulo?

Oi! É Webster novamente! Marcy e Vincent estão começando a entender o valor dos conselhos de Bob. Mas eles não podem arcar com muitos períodos de inatividade e precisam operar com a rede atual até que Bob possa fazer as atualizações. Eles não vão adicionar VoIP, câmeras de segurança ou sistema de pedidos on-line até lá. Bob precisa avaliar a rede atual antes da atualização para entender melhor o que precisa ser feito.

A rede da loja de móveis é uma rede Ethernet. Os protocolos Ethernet definem como os dados são formatados e como são transmitidos pela rede cabeada e especificam os protocolos que operam na camada 1 e na camada 2 do modelo OSI.

Você está familiarizado com Ethernet? Por que os sistemas de números hexadecimal e binário são importantes em uma rede Ethernet? Acho que você deve usar este módulo para aprender mais sobre Ethernet, Quadreos Ethernet e Endereços MAC Ethernet! Vamos começar!

## 21.0.2 O que irei aprender neste módulo?

**Titulo do módulo:** Ethernet Switching

**Objetivo do módulo:** Explicar como a Ethernet funciona em uma rede comutada.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Ethernet|Explicar as funções das camadas 1 e 2 do modelo OSI em uma rede Ethernet.|
|Quadros Ethernet|Explicar como as subcamadas da Ethernet se relacionam com os campos do quadro.|
|Endereços MAC Ethernet|Explique os tipos de endereços MAC Ethernet.|
|A tabela de endereços MAC|Explicar como um switch cria sua tabela de endereços MAC e encaminha os quadros.|

# 21.1 Ethernet

## 21.1.1 A ascensão da Ethernet

Nos primórdios das redes, cada fornecedor utilizava seus próprios métodos de interconexão de dispositivos de rede e protocolos de rede. Se você adquirisse equipamentos de fornecedores diferentes, não havia garantias de que eles funcionariam em conjunto. O equipamento de um fornecedor podia não se comunicar com o equipamento de outro.

Com a expansão das redes, foram desenvolvidos padrões que definiram regras para a operação de equipamentos de rede de diferentes fornecedores. Os padrões são vantajosos para as redes porque:

- Facilitam o design
- Simplificam o desenvolvimento de produtos
- Promovem a concorrência
- Fornecem interconexões consistentes
- Facilitam o treinamento
- Oferecem mais opções de fornecedor aos clientes

Não há um protocolo oficial de padrão de rede local, mas, com o tempo, uma tecnologia se tornou mais comum do que as outras: a Ethernet. Os protocolos Ethernet definem como os dados são formatados e transmitidos pela rede com fio. Os padrões Ethernet especificam protocolos que operam nas Camadas 1 e 2 do modelo OSI. Ela passou a ser um padrão de fato, o que significa que a Ethernet é a tecnologia usada por quase todas as redes locais com fio, como mostrado na figura.

![[Pasted image 20260615200404.png]]


## 21.1.2 Evolução da Ethernet

"O Instituto de Engenheiros Elétricos e Eletrônicos, ou IEEE", mantém os padrões de rede, incluindo Ethernet e padrões sem fio. Os comitês do IEEE são responsáveis por aprovar e manter os padrões para conexões, requisitos de mídia e protocolos de comunicação. Cada padrão de tecnologia recebe um número referente ao comitê responsável por aprovar e manter o padrão. O comitê responsável pelos padrões de Ethernet é o 802.3.

Desde a criação da Ethernet em 1973, os padrões evoluíram para especificar versões mais rápidas e flexíveis da tecnologia. Essa capacidade da Ethernet de melhorar ao longo do tempo é um dos principais motivos de ela ter se tornado tão popular. Cada versão da Ethernet tem um padrão associado. Por exemplo, o 802.3 100BASE-T representa o 100 Megabits Ethernet com padrões de cabo de par trançado. A notação padrão significa que:

- 100 é a velocidade em Mbps
- BASE significa transmissão de banda base
- T significa o tipo de cabo, neste caso, par trançado.

As primeiras versões da Ethernet eram relativamente lentas, a 10 Mbps. As versões mais recentes da Ethernet operam a 10 Gbps ou mais. Imagine o quanto mais rápidas são essas novas versões em relação às redes Ethernet originais.

Arraste a barra deslizante na figura pela linha do tempo para ver como os padrões de Ethernet evoluíram ao longo do tempo.

## 21.1.3 Vídeo - Endereçamento Ethernet

Neste vídeo, vamos ver sobre endereçamento Ethernet.

Em nossa topologia, temos os hosts H1, H2, H3 e H4. H1 tem o endereço MAC de origem — MAC significa controle de acesso ao meio — composto por todos os As.

H1 tem um quadro Ethernet para enviar para o host H3. No quadro Ethernet, há um endereço MAC de destino, que é o endereço MAC do host H3, composto por todos os Cs. O endereço MAC de origem é o do host H1, com todos os As.

H1 envia esse quadro Ethernet para o switch. Quando o switch recebe este quadro Ethernet, ele irá encaminhar o quadro para todas as portas, exceto a porta de entrada. Mais tarde, aprenderemos mais sobre como os switches Ethernet podem realmente filtrar os quadros para que eles apenas enviem o quadro para o próprio destino.

Como resultado, todos os dispositivos na rede recebem o quadro Ethernet. H2 e H4 ignoram o quadro Ethernet. Por que eles fazem isso? Eles examinam o endereço MAC de destino — todos os Cs — e comparam com seu próprio endereço MAC. Na verdade, a placa Ethernet NIC faz isso. Como não há uma correspondência, a placa Ethernet NIC ignorará o resto do quadro, e esses hosts acabam por não receber a mensagem.

H3, por sua vez, quando sua placa Ethernet NIC recebe este quadro Ethernet, compara o endereço MAC de destino no quadro com seu próprio endereço MAC em sua placa NIC. Como há uma correspondência, ela vai em frente, recebe o restante do quadro, e a mensagem é processada.


## 21.1.4 Laboratório – Como determinar o endereço MAC de um host

Neste laboratório, você completará os seguintes objetivos:

- Determinar o endereço MAC de um computador Windows em uma rede Ethernet ao usar o comando **ipconfig /all**.
- Analisar um endereço MAC para determinar o fabricante.

### Laboratório – Como determinar o endereço MAC de um host

#### Tabela de Endereçamento

|Dispositivo|Interface|Endereço IP|Máscara de Sub-Rede|
|---|---|---|---|
|PC|VLAN 1|192.168.1.2|255.255.255.0|

#### Objetivos

- Determinar o endereço MAC de um computador Windows em uma rede Ethernet ao usar o comando ipconfig /all.
- Analisar um endereço MAC para determinar o fabricante.

#### Histórico / Cenário

Todos os computadores em uma rede local de Ethernet têm um endereço de controle de acesso ao meio (MAC) que é gravado na placa de rede (NIC). Os endereços MAC do computador normalmente são exibidos como seis conjuntos de dois números hexadecimais separados por travessão ou dois pontos (exemplo: 15-EF-A3-45-9B-57). O comando ipconfig /all exibe o endereço MAC do computador. Você pode trabalhar individualmente ou em equipes.

#### Recursos necessários

- PC executando Windows 10 com pelo menos uma placa de rede (NIC) Ethernet
- Conectividade à Internet

#### Instruções

##### Parte 1: Localização do endereço MAC em um computador

Nesta parte do laboratório, você determinará o endereço MAC de um computador com o comando ipconfig do Windows.

###### Etapa 1: Exibir informações para o comando ipconfig /all

a. Clique com o botão direito no botão Iniciar e selecione Prompt de Comando.

b. Insira o comando ipconfig /all no prompt de comando.

###### Etapa 2: Localize os endereços MAC (físicos) na saída do comando ipconfig /all

Use a tabela abaixo para completar a descrição do adaptador Ethernet e do endereço (MAC) físico:

|Descrição|Endereço físico|
|---|---|
|Digite suas respostas aqui.|Digite suas respostas aqui.|
|Digite suas respostas aqui.|Digite suas respostas aqui.|
|Digite suas respostas aqui.|Digite suas respostas aqui.|

**Exemplo de resposta:**

|Descrição|Endereço físico|
|---|---|
|Intel(R) Ethernet Connection I219-LM|54-EE-75-C3-2B-33|

**Pergunta:** Quantos endereços MAC você encontrou no seu PC?

**Resposta:** As respostas variaram de acordo com a configuração do PC.

---

##### Parte 2: Análise das partes de um endereço MAC

Todas as interfaces de rede Ethernet têm um endereço físico atribuído a elas na fabricação. Esses endereços têm 48 bit (seis bytes) e são escritos em notação hexadecimal. Os endereços MAC têm duas partes. Uma parte do endereço MAC, os três primeiros bytes, representa o fornecedor que fabricou a interface de rede. Essa parte do MAC é chamada de OUI (identificador organizacionalmente único). Cada fornecedor que desejar fazer e vender interfaces de rede Ethernet deve se registrar com o IEEE para ter um OUI atribuído.

A segunda parte do endereço, os três bytes restantes, é o ID único para a interface. Todos os endereços MAC que começam com o mesmo OUI precisam ter valores únicos nos últimos três bytes.

Neste exemplo, o endereço MAC físico para a interface Ethernet LAN é D4-BE-D9-13-63-00.

|OUI do fabricante|Identificador único para a interface|Nome do fornecedor|
|---|---|---|
|D4-BE-D9|13-63-00|Dell Incorporated|

###### Etapa 1: Liste os endereços MAC descobertos por você e seus colegas na parte anterior.

Liste o OUI do fabricante de três bytes e o identificador de interface único de três bytes. Você preencherá o nome do fornecedor na tabela abaixo.

|OUI do fabricante|Identificador único para a interface|Nome do fornecedor|
|---|---|---|
|Digite suas respostas aqui.|Digite suas respostas aqui.|Digite suas respostas aqui.|
|Digite suas respostas aqui.|Digite suas respostas aqui.|Digite suas respostas aqui.|
|Digite suas respostas aqui.|Digite suas respostas aqui.|Digite suas respostas aqui.|

###### Etapa 2: Consulte os fornecedores que são proprietários registrados do OUI listado na tabela.

a. A Wireshark.org disponibiliza uma ferramenta de fácil utilização em https://www.wireshark.org/tools/oui-lookup.html. Use essa ferramenta ou a Internet para pesquisar outras formas de identificar um OUI.

b. Use as informações encontradas para atualizar a coluna do fornecedor no gráfico na Etapa 1.

**Pergunta:** Quantos fornecedores diferentes você encontrou?

**Resposta:** As respostas variaram de acordo com a configuração do PC.

---

#### Reflexão

**1. Por que um computador pode ter mais de um endereço MAC?**

**Resposta:** Um computador pode ter várias placas de rede, incluindo duas ou mais placas de rede Ethernet e sem fio.

**2. A saída de exemplo do comando ipconfig /all mostrada anteriormente tinha somente um endereço MAC. Suponha que a saída fosse de um computador que também tinha recursos Ethernet sem fio. Como a saída poderia mudar?**

**Resposta:** A tela listaria as informações para todas as placas de rede ativadas no computador.

**3. Tente conectar e desconectar os cabos de rede dos seus adaptadores de rede e use ipconfig /all novamente. Que alterações podem ser observadas? O endereço MAC ainda é exibido? O endereço MAC mudará em algum momento?**

**Resposta:** Embora os endereços IP possam mudar, os endereços MAC sempre permanecem os mesmos.

**4. Quais são os outros nomes para o endereço MAC?**

**Resposta:** Um endereço MAC também é conhecido como endereço de hardware, endereço Ethernet ou endereço gravado (BIA).

# 21.2 Quadros Ethernet

## 21.2.1 Encapsulamento Ethernet

Ethernet e o modelo OSI

Este módulo começa com uma discussão sobre a tecnologia Ethernet, incluindo uma explicação da subcamada MAC e os campos de quadro Ethernet.

A Ethernet é uma das duas tecnologias de LAN usadas atualmente, sendo a outra LANs sem fio (WLANs). A Ethernet utiliza comunicações com fios, incluindo par trançado, ligações de fibra óptica e cabos coaxiais.

Ela opera na camada de enlace de dados e na camada física. É uma família de tecnologias de rede definidas nos padrões IEEE 802.2 e 802.3. A Ethernet suporta as seguintes larguras de banda:

- 10 Mbps
- 100 Mbps
- 1000 Mbps (1 Gbps)
- 10,000 Mbps (10 Gbps)
- 40,000 Mbps (40 Gbps)
- 100,000 Mbps (100 Gbps)

Conforme mostrado na figura, os padrões Ethernet definem os protocolos da camada 2 e as tecnologias da camada 1.

### Ethernet e o modelo OSI

![[Pasted image 20260615200742.png]]

## 21.2.2 Subcamadas de Enlace de Dados

Protocolos IEEE 802 LAN/MAN, incluindo Ethernet, usam as seguintes duas subcamadas separadas da camada de link de dados para operar. Eles são o controle de link lógico (LLC) e o controle de acesso de mídia (MAC), como mostrado na figura.

Lembre-se de que LLC e MAC têm as seguintes funções na camada de enlace:

- **Subcamada** LLC - Esta subcamada IEEE 802.2 se comunica entre o software de rede nas camadas superiores e o hardware do dispositivo nas camadas inferiores. Ela coloca a informação no quadro que identifica qual protocolo de camada de rede está sendo usado para o quadro. Essas informações permitem que vários protocolos da camada 3, como IPv4 e IPv6, usem a mesma interface de rede e mídia.
- **Subcamada** MAC - Esta subcamada (IEEE 802.3, 802.11 ou 802.15 por exemplo) é implementada em hardware e é responsável pelo encapsulamento de dados e controle de acesso ao meio. Ele fornece endereçamento de camada de link de dados e é integrado com várias tecnologias de camada física.

![[Pasted image 20260615200806.png]]

## 21.2.3 Subcamada MAC

Padrões Ethernet na subcamada MAC

A subcamada MAC é responsável pelo encapsulamento de dados e acesso à mídia.

**Encapsulamento de dados**

O encapsulamento de dados IEEE 802.3 inclui o seguinte:

- **Quadro Ethernet** - Esta é a estrutura interna do quadro Ethernet.
- **Endereçamento Ethernet** - O quadro Ethernet inclui um endereço MAC de origem e de destino para entregar o quadro Ethernet de NIC Ethernet para NIC Ethernet na mesma LAN.
- **Detecção de erro Ethernet** - O quadro Ethernet inclui um trailer de seqüência de verificação de quadro (FCS) usado para detecção de erro.

**Acessando a mídia**

Como mostrado na figura, a subcamada MAC IEEE 802.3 inclui as especificações para diferentes padrões de comunicações Ethernet em vários tipos de mídia, incluindo cobre e fibra.

### Padrões Ethernet na subcamada MAC

![[Pasted image 20260615200825.png]]
Lembre-se que a Ethernet legada que usa uma topologia de barramento ou hubs, é um meio compartilhado e half-duplex. Ethernet em um meio half-duplex usa um método de acesso baseado em contenção, detecção de múltiplos acessos/detecção de colisão (CSMA/CD). Isso garante que apenas um dispositivo esteja transmitindo por vez. O CSMA/CD permite que vários dispositivos compartilhem o mesmo meio half-duplex, detectando uma colisão quando mais de um dispositivo tenta transmitir simultaneamente. Ele também fornece um algoritmo de back-off para retransmissão.

As LANs Ethernet de hoje usam switches que operam em full-duplex. As comunicações full-duplex com switches Ethernet não exigem controle de acesso através do CSMA/CD.

## 21.2.4 Campos do Quadro Ethernet

Campos do quadro Ethernet

O tamanho mínimo do quadro Ethernet é de 64 bytes e o máximo esperado é de 1518 bytes. Isso inclui todos os bytes do campo de endereço MAC de destino até o campo FCS (Frame Check Sequence). O campo de preâmbulo não é incluído ao descrever o tamanho do quadro.

**Observação**: o tamanho do quadro pode ser maior se requisitos adicionais forem incluídos, como a marcação de VLAN. A marcação de VLAN está além do escopo deste curso.

Qualquer quadro com comprimento menor que 64 bytes é considerado um"fragmento de colisão" ou um "quadro desprezível" e é automaticamente descartado pelas estações receptoras. Quadros com mais de 1.500 bytes de dados são considerados “jumbo” ou “baby giant”.

Se o tamanho de um quadro transmitido for menor que o mínimo ou maior que o máximo, o dispositivo receptor descarta o quadro. É provável que quadros perdidos sejam resultado de colisões ou outros sinais indesejados. Eles são considerados inválidos. Os quadros jumbo geralmente são suportados pela maioria dos switches e NICs Fast Ethernet e Gigabit Ethernet.

A figura mostra cada campo no quadro Ethernet. Consulte a tabela para obter mais informações sobre a função de cada campo.

### Campos de um Quadro Ethernet

![[Pasted image 20260615201049.png]]

|Campo|Descrição|
|---|---|
|Campos Preâmbulo e Delimitador Início de Quadro|Os campos Preâmbulo (7 bytes) e Delimitador de Início de Quadro (SFD), também chamado de Início de Quadro (1 byte), são utilizados para sincronização entre os dispositivos emissor e receptor. Esses primeiros oito bytes do quadro servem para chamar a atenção dos nós receptores. Basicamente, os primeiros bytes dizem aos receptores para se prepararem para receber um novo quadro.|
|Campo Endereço MAC de Destino|Este campo de 6 bytes é o identificador do destinatário desejado. Como você se lembra, este endereço é usado pela Camada 2 para ajudar os dispositivos a determinar se um quadro é endereçado a eles. O endereço no quadro é comparado com o endereço MAC do dispositivo. Se houver correspondência, o dispositivo aceitará o quadro. Pode ser um endereço unicast, broadcast ou multicast.|
|Campo Endereço MAC de Origem|Este campo de 6 bytes identifica o NIC ou interface de origem do quadro.|
|Tipo/Comprimento|Este campo de 2 bytes identifica o protocolo da camada superior encapsulado no quadro Ethernet. Os valores comuns em hexadecimal são 0x800 para IPv4, 0x86DD para IPv6 e 0x806 para ARP. Você também pode ver este campo conhecido como EtherType, tipo ou comprimento.|
|Campo Dados|Este campo (46 a 1500 bytes) contém os dados encapsulados de uma camada superior, que é uma PDU genérica da Camada 3 ou um pacote IPv4, o que é mais comum. Todos os quadros devem ter pelo menos 64 bytes. Se um pacote pequeno for encapsulado, bits adicionais chamados de pad serão usados para aumentar o quadro até seu tamanho mínimo.|
|Campo Sequência de Verificação de Quadro|Este campo (4 bytes) é usado para detectar erros em um quadro. Ele utiliza uma verificação de redundância cíclica (CRC). O dispositivo emissor inclui os resultados de uma CRC no campo FCS do quadro. O dispositivo receptor recebe o quadro e gera uma CRC para buscar erros. Se o cálculo corresponder, significa que não houve erro. Cálculos não correspondentes são uma indicação de que os dados foram alterados. Nesse caso, o quadro é descartado. Uma alteração nos dados pode ser resultado de interrupção dos sinais elétricos que representam os bits.|

## 21.2.5 Verifique sua compreensão - Campos do quadro Ethernet

### Pergunta 1

Qual parte de um quadro Ethernet usa um pad para aumentar o campo de quadro para pelo menos 64 bytes?

- [ ] EtherType
- [ ] Preâmbulo
- [ ] Delimitador de Início de Quadro
- [x] Campo de dados

✅ RESPOSTA CORRETA: Campo de dados

> Todos os quadros devem ter pelo menos 64 bytes. Bits adicionais chamados "pad" são usados para aumentar o tamanho de quadros pequenos para o tamanho mínimo.

---

### Pergunta 2

Qual parte de um quadro Ethernet detecta erros no quadro?

- [ ] Preâmbulo
- [ ] Delimitador de Início de Quadro
- [x] Sequência de Verificação de Quadro (FCS)

✅ RESPOSTA CORRETA: Sequência de Verificação de Quadro (FCS)

> O campo FCS usa um CRC para detectar erros em um quadro.

---

### Pergunta 3

Qual parte de um quadro Ethernet descreve o protocolo de camada superior encapsulado?

- [x] EtherType
- [ ] Preâmbulo
- [ ] Delimitador de Início de Quadro
- [ ] Sequência de Verificação de Quadro (FCS)

✅ RESPOSTA CORRETA: EtherType

> O campo EtherType identifica o protocolo da camada superior que está encapsulado no quadro Ethernet.

---

### Pergunta 4

Qual parte de um quadro Ethernet notifica o receptor para se preparar para um novo quadro?

- [ ] Delimitador de Início de Quadro
- [ ] Sequência de Verificação de Quadro (FCS)
- [x] Introdução
- [ ] Campo de dados

✅ RESPOSTA CORRETA: Introdução

> Os primeiros bytes do preâmbulo informam o receptor de um novo quadro.

---

### Pergunta 5

Qual subcamada de link de dados controla a interface de rede através de drivers de software?

- [ ] MAC
- [x] LLC

✅ RESPOSTA CORRETA: LLC

> A subcamada LLC é responsável por controlar a placa de interface de rede através de drivers de software.

---

### Pergunta 6

Qual subcamada de link de dados trabalha com as camadas superiores para adicionar informações de aplicativos para entrega de dados a protocolos de nível superior?

- [ ] MAC
- [x] LLC

✅ RESPOSTA CORRETA: LLC

> A LLC trabalha com camadas superiores para suportar protocolos de nível superior.

---

### Pergunta 7

O que é uma função da subcamada MAC? (Escolha três.)

- [x] controla o acesso à mídia
- [x] verifica se há erros em bits recebidos
- [x] usa CSMA/CD ou CSMA/CA para oferecer suporte à tecnologia Ethernet
- [ ] comunica entre o software nas camadas superiores e o hardware do dispositivo nas camadas inferiores
- [ ] permite que vários protocolos da camada 3 usem a mesma interface de rede e mídia

✅ RESPOSTA CORRETA: controla o acesso à mídia / verifica se há erros em bits recebidos / usa CSMA/CD ou CSMA/CA para oferecer suporte à tecnologia Ethernet

> A subcamada MAC verifica erros de bits, suporta tecnologias Ethernet e controla o acesso à mídia.


## 21.2.6 Laboratório - Observar o tráfego capturado pelo Wireshark

Neste laboratório, você completará os seguintes objetivos:

- Baixe e instale o Wireshark.
- Capturar e analisar dados ARP no Wireshark.
- Visualizar as entradas do cache ARP no PC.

[Laboratório - Observar o tráfego capturado pelo Wireshark](Labs/21.2.6 Laboratório/Observar_o_tráfego_capturado_pelo_Wireshark.html)