
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

#### 21.2.6 Laboratório - Observar o tráfego capturado pelo Wireshark

[Abrir laboratório](Fundamentos%20de%20Redes%20-%20Senac%20SC/Labs/21.2.6%20Laboratório/Observar_o_tráfego_capturado_pelo_Wireshark.html)



## 21.2.7 Laboratório - Use o Wireshark para examinar quadros Ethernet

Neste laboratório, você cumprirá os seguintes objetivos:

- Parte 1: Examinar os campos do cabeçalho de um quadro Ethernet II
- Parte 2: Usar o Wireshark para capturar e analisar quadros Ethernet

[Abrir laboratório](Labs/21.2.7/Use%20o%20Wireshark%20para%20examinar%20quadros%20Ethernet.html)


# 21.3 Endereços MAC Ethernet

## 21.3.1 Endereço MAC e Hexadecimal

Equivalentes decimais e binários de 0 a F Hexadecimal

Na rede, os endereços IPv4 são representados usando o sistema de dez números base decimal e o sistema de números de base binária 2. Endereços IPv6 e endereços Ethernet são representados usando o sistema hexadecimal base dezesseis números. Para entender hexadecimal, você deve primeiro estar muito familiarizado com binário e decimal.

O sistema de numeração hexadecimal usa os números de 0 a 9 e as letras de A a F.

Um endereço MAC Ethernet consiste em um valor binário de 48 bits. Hexadecimal é usado para identificar um endereço Ethernet porque um único dígito hexadecimal representa quatro bits binários. Portanto, um endereço MAC Ethernet de 48 bits pode ser expresso usando apenas 12 valores hexadecimais.

A figura compara os valores decimal e hexadecimais equivalentes para o binário 0000 a 1111.

### Equivalentes decimais e binários de 0 a F Hexadecimal

|Decimal|Binário|Hexadecimal|
|---|---|---|
|0|0000|0|
|1|0001|1|
|2|0010|2|
|3|0011|3|
|4|0100|4|
|5|0101|5|
|6|0110|6|
|7|0111|7|
|8|1000|8|
|9|1001|9|
|10|1010|A|
|11|1011|B|
|12|1100|C|
|13|1101|D|
|14|1110|E|
|15|1111|F|

### Equivalentes decimais, binários e hexadecimais selecionados

Dado que 8 bits (um byte) é um agrupamento binário comum, os binários 00000000 a 11111111 podem ser representados em hexadecimal como o intervalo de 00 a FF, conforme mostrado na figura a seguir.

### Equivalentes decimais, binários e hexadecimais selecionados

| Decimal | Binário   | Hexadecimal |
| ------- | --------- | ----------- |
| 0       | 0000 0000 | 00          |
| 1       | 0000 0001 | 01          |
| 2       | 0000 0010 | 02          |
| 3       | 0000 0011 | 03          |
| 4       | 0000 0100 | 04          |
| 5       | 0000 0101 | 05          |
| 6       | 0000 0110 | 06          |
| 7       | 0000 0111 | 07          |
| 8       | 0000 1000 | 08          |
| 10      | 0000 1010 | 0A          |
| 15      | 0000 1111 | 0F          |
| 16      | 0001 0000 | 10          |
| 32      | 0010 0000 | 20          |
| 64      | 0100 0000 | 40          |
| 128     | 1000 0000 | 80          |
| 192     | 1100 0000 | C0          |
| 202     | 1100 1010 | CA          |
| 240     | 1111 0000 | F0          |
| 255     | 1111 1111 | FF          |

Ao usar hexadecimal, os zeros à esquerda são sempre exibidos para concluir a representação de 8 bits. Por exemplo, na tabela, o valor binário 0000 1010 é mostrado em hexadecimal como 0A.

Números hexadecimais são frequentemente representados pelo valor precedido por **0x** (por exemplo, 0x73) para distinguir entre valores decimal e hexadecimais na documentação.

O hexadecimal também pode ser representado por um subscript 16, ou o número hexadecimal seguido por um H (por exemplo, 73H).

Talvez seja necessário converter entre valores decimal e hexadecimais. Se tais conversões forem necessárias, converta o valor decimal ou hexadecimal em binário e, em seguida, converta o valor binário em decimal ou hexadecimal, conforme apropriado.


## 21.3.2 Endereço MAC Unicast

Na Ethernet, são utilizados diferentes endereços MAC para comunicação unicast, broadcast e multicast da Camada 2.

Um endereço MAC de unicast é o endereço exclusivo usado quando um quadro é enviado de um único dispositivo de transmissão para um único dispositivo de destino.

Clique em Reproduzir na animação para ver como um quadro de unicast é processado. Neste exemplo, o endereço MAC de destino e o endereço IP de destino são unicast.

![[Pasted image 20260615213011.png]]

No exemplo mostrado na figura, um host com endereço IPv4 192.168.1.5 (origem) requisita uma página Web do servidor no endereço IPv4 192.168.1.200. Para que um pacote unicast seja enviado e recebido, um endereço IP de destino deve estar no cabeçalho do pacote IP. Um endereço MAC de destino correspondente também deve estar presente no cabeçalho do quadro Ethernet. O endereço IP e o endereço MAC se combinam para entregar dados a um host de destino específico.

O processo que um host de origem usa para determinar o endereço MAC de destino associado a um endereço IPv4 é conhecido como ARP (Address Resolution Protocol). O processo que um host de origem usa para determinar o endereço MAC de destino associado a um endereço IPv6 é conhecido como ND (Neighbour Discovery Discovery).

**Nota:** O endereço MAC de origem deve ser sempre um unicast.


## 21.3.3 Endereço MAC de broadcast

Um quadro de transmissão Ethernet é recebido e processado por cada dispositivo na LAN Ethernet. Os recursos de uma transmissão Ethernet são os seguintes:

- Possui um endereço MAC de destino de FF-FF-FF-FF-FF-FF em hexadecimal (48 endereços em binário).
- É inundada todas as portas de switch Ethernet, exceto a porta de entrada.
- Ele não é encaminhado por um roteador.

Se os dados encapsulados forem um pacote de transmissão IPv4, isso significa que o pacote contém um endereço IPv4 de destino que possui todos os 1s na parte do host. Essa numeração no endereço significa que todos os hosts naquela rede local (domínio de broadcast) receberão e processarão o pacote.

Clique em Reproduzir na animação para ver como um quadro de broadcast é processado. Neste exemplo, o endereço MAC de destino e o endereço IP de destino são transmissões.

![[Pasted image 20260615213043.png]]

Como mostrado na animação, o host de origem envia um pacote IPv4 broadcast a todos os dispositivos de sua rede. O endereço IPv4 destino é um endereço de broadcast, 192.168.1.255. Quando o pacote IPv4 broadcast é encapsulado no quadro Ethernet, o endereço MAC de destino é o endereço MAC de broadcast FF-FF-FF-FF-FF-FF em hexadecimal (48 uns em binário).

DHCP para IPv4 é um exemplo de um protocolo que usa endereços de broadcast Ethernet e IPv4.

No entanto, nem todas as transmissões Ethernet carregam um pacote de difusão IPv4. Por exemplo, as Solicitações ARP não usam IPv4, mas a mensagem ARP é enviada como uma transmissão Ethernet.


## 21.3.4 Endereço MAC Multicast

Um quadro de multicast Ethernet é recebido e processado por um grupo de dispositivos na LAN Ethernet que pertencem ao mesmo grupo de multicast. Os recursos de um multicast Ethernet são os seguintes:

- Há um endereço MAC de destino 01-00-5E quando os dados encapsulados são um pacote multicast IPv4 e um endereço MAC de destino de 33-33 quando os dados encapsulados são um pacote multicast IPv6.
- Há outros endereços MAC de destino multicast reservados para quando os dados encapsulados não são IP, como STP (Spanning Tree Protocol) e LLDP (Link Layer Discovery Protocol).
- É inundada todas as portas de switch Ethernet, exceto a porta de entrada, a menos que o switch esteja configurado para espionagem multicast.
- Ele não é encaminhado por um roteador, a menos que o roteador esteja configurado para rotear pacotes multicast.

Se os dados encapsulados forem um pacote multicast IP, os dispositivos que pertencem a um grupo multicast recebem um endereço IP do grupo multicast. O intervalo de endereços IPv4 multicast vai de 224.0.0.0 a 239.255.255.255. O intervalo de endereços multicast IPv6 começa com ff00::/8. Como os endereços multicast representam um grupo de endereços (às vezes chamado de grupo de hosts), eles só podem ser utilizados como destino de um pacote. A origem sempre será um endereço unicast.

Assim como nos endereços unicast e broadcast, o endereço IP multicast requer um endereço MAC multicast correspondente para entregar quadros em uma rede local. O endereço MAC multicast está associado e usa informações de endereçamento do endereço multicast IPv4 ou IPv6.

Pressione Reproduzir na animação para ver como um quadro multicast é processado. Neste exemplo, o endereço MAC de destino e o endereço IP de destino são multicasts.

![[Pasted image 20260615213115.png]]

Protocolos de roteamento e outros protocolos de rede usam endereçamento multicast. Aplicativos como software de vídeo e imagem também podem usar endereçamento multicast, embora aplicativos multicast não sejam tão comuns.

## 21.3.5 Verifique a sua compreensão - Endereço MAC Ethernet

### Pergunta 1

Que tipo de endereço MAC a seguir é endereço MAC de unicast?

- [ ] 01-00-5E-00-00-C8
- [x] 00-07-E9-42-AC-28
- [ ] 33-33-00-58-94-5C
- [ ] FF-FF-FF-FF-FF-FF

✅ RESPOSTA CORRETA: 00-07-E9-42-AC-28

> 00-07-E9-42-AC-28 é o endereço MAC de unicast.

---

### Pergunta 2

Que tipo de endereço MAC a seguir é transmitido por endereço MAC?

- [ ] 01-00-5E-00-00-C8
- [ ] 00-07-E9-42-AC-28
- [ ] 33-33-00-58-94-5C
- [x] FF-FF-FF-FF-FF-FF

✅ RESPOSTA CORRETA: FF-FF-FF-FF-FF-FF

> FF-FF-FF-FF-FF-FF é um endereço MAC de broadcast.

---

### Pergunta 3

Que tipo do seguinte endereço MAC é um endereço MAC multicast IPv4?

- [x] 01-00-5E-00-00-C8
- [ ] 00-07-E9-42-AC-28
- [ ] 33-33-00-58-94-5C
- [ ] FF-FF-FF-FF-FF-FF

✅ RESPOSTA CORRETA: 01-00-5E-00-00-C8

> 01-00-5E-00-00-C8 é um endereço MAC multicast IPv4.

---

### Pergunta 4

Que tipo de endereço MAC a seguir é um endereço IP multicast de IPv6?

- [ ] 01-00-5E-00-00-C8
- [ ] 00-07-E9-42-AC-28
- [x] 33-33-00-58-94-5C
- [ ] FF-FF-FF-FF-FF-FF

✅ RESPOSTA CORRETA: 33-33-00-58-94-5C

> 33-33-00-58-94-5C é um endereço MAC multicast IPv6.


# 21.4 A tabela de endereços MAC

## 21.4.1 Noções Básicas sobre Switches

Agora que você sabe tudo sobre endereços MAC Ethernet, é hora de falar sobre como um switch usa esses endereços para encaminhar (ou descartar) quadros para outros dispositivos em uma rede. Se um switch apenas encaminhasse cada quadro recebido de todas as portas, sua rede ficaria tão congestionada que provavelmente chegaria a uma parada completa.

Um switch Ethernet da camada 2 usa endereços MAC da camada 2 para tomar decisões de encaminhamento. Desconhece completamente os dados (protocolo) que estão sendo transportados na parte de dados do quadro, como um pacote IPv4, uma mensagem ARP ou um pacote ND IPv6. O switch toma decisões de encaminhamento com base apenas nos endereços MAC Ethernet da camada 2.

Um switch Ethernet examina sua tabela de endereços MAC para tomar uma decisão de encaminhamento para cada quadro, ao contrário dos hubs Ethernet herdados que repetem bits em todas as portas, exceto a porta de entrada. Na figura, o switch de quatro portas acaba de ser ligado. O switch toma decisões de encaminhamento com base apenas nos endereços MAC Ethernet da camada 2.

**Nota**: Os endereços MAC são abreviados neste tópico para fins de demonstração.

![[Pasted image 20260615213714.png]]
**Nota**: A tabela de endereços MAC às vezes é chamada de tabela de memória endereçável de conteúdo (CAM). Embora o termo "tabela CAM" seja muito comum, neste curso nós a chamaremos de tabela de endereços MAC.

## 21.4.2 Switch Aprendizado e Encaminhamento

O switch cria a tabela de endereços MAC dinamicamente examinando o endereço MAC de origem dos quadros recebidos em uma porta. O switch encaminha quadros procurando uma correspondência entre o endereço MAC de destino no quadro e uma entrada na tabela de endereços MAC.

**Clique nos botões Aprender e Encaminhar para obter uma ilustração e explicação desse processo.**

### Aprendizado

**Examine o endereço MAC de origem**

Todo quadro que entra em um switch é verificado quanto ao aprendizado de novas informações. Isso é feito examinando o endereço MAC de origem do quadro e o número da porta em que o quadro entrou no comutador. Se o endereço MAC de origem não existe, é adicionado à tabela juntamente com o número da porta de entrada. Se o endereço MAC de origem existir, o switch atualizará o cronômetro de atualização para essa entrada na tabela. Por padrão, a maioria dos switches Ethernet mantém uma entrada na tabela por 5 minutos.

Na figura, por exemplo, o PC-A está enviando um quadro Ethernet para o PC-D. A tabela mostra que o switch adiciona o endereço MAC do PC-A à tabela de endereços MAC.

**Nota**: Se o endereço MAC de origem não existir na tabela, mas em uma porta diferente, o switch tratará isso como uma nova entrada. A entrada é substituída usando o mesmo endereço MAC, mas com o número de porta mais atual.

![[Pasted image 20260615213805.png]]

### Encaminhamento

**Encontre o endereço MAC de destino**

Se o endereço MAC de destino for um endereço unicast, o switch procurará uma correspondência entre o endereço MAC de destino do quadro e uma entrada em sua tabela de endereços MAC. Se o endereço MAC de destino estiver na tabela, ele encaminhará o quadro pela porta especificada. Se o endereço MAC de destino não estiver na tabela, o switch encaminhará o quadro por todas as portas, exceto a de entrada. Isso é chamado de unicast desconhecido.

Conforme mostrado na figura, o switch não possui o endereço MAC de destino em sua tabela para PC-D; portanto, envia o quadro para todas as portas, exceto a porta 1.

**Nota**: Se o endereço MAC de destino for um broadcast ou multicast, o quadro também inundará todas as portas, exceto a porta de entrada.

![[Pasted image 20260615213853.png]]

## 21.4.3 Filtrando Quadros

A medida que um switch recebe quadros de dispositivos diferentes, ele é capaz de preencher sua tabela de endereços MAC examinando o endereço MAC de origem de cada quadro. Quando a tabela de endereços MAC do switch contém o endereço MAC de destino, ele pode filtrar o quadro e encaminhar uma única porta.

**Clique em cada botão para obter uma ilustração e explicação de como um switch filtra quadros.**

### PC-D para Switch

Na figura, PC-D está respondendo ao PC-A. O switch vê o endereço MAC do PC-D no quadro de entrada na porta 4. Em seguida, o switch coloca o endereço MAC do PC-D na Tabela de Endereços MAC associada à porta 4.
![[Pasted image 20260615213955.png]]

### Mudar para PC-A
Em seguida, como o switch possui o endereço MAC de destino para PC-A na tabela de endereços MAC, ele enviará o quadro apenas para a porta 1, conforme mostrado na figura.

![[Pasted image 20260615214010.png]]


### PC-A para mudar para PC-D
Em seguida, PC-A envia outro quadro para PC-D como mostrado na figura. A tabela de endereços MAC já contém o endereço MAC para PC-A; portanto, o cronômetro de atualização de cinco minutos para essa entrada é redefinido. Em seguida, como a tabela de switches contém o endereço MAC de destino para PC-D, ela envia o quadro apenas para a porta 4.

![[Pasted image 20260615214024.png]]

## 21.4.4 Vídeo - Tabelas de endereços MAC em switches conectados

Um switch pode ter vários endereços MAC associados a uma única porta. Isso é comum quando o switch está conectado a outro switch. O switch terá uma entrada separada na tabela de endereços MAC para cada quadro recebido com um endereço MAC de origem diferente.

Clique em Reproduzir na figura para ver uma demonstração de como dois switches conectados criam tabelas de endereços MAC.

**Selecione o botão Reproduzir para assistir ao vídeo.**

Neste vídeo, PC-A vai enviar um quadro Ethernet para PC-B, e PC-B enviará um quadro Ethernet para o PC-A. Vamos examinar como os switches S1 e S2 constroem suas tabelas de endereços MAC e como eles encaminham quadros com base nas informações dessas tabelas.

O PC-A tem um quadro Ethernet para enviar ao PC-B. O endereço MAC de origem do quadro é 00-0A e o de destino é 00-0B. O quadro Ethernet é enviado para o switch S1. S1 recebe o quadro Ethernet, examina o endereço MAC de origem, e observa que esse endereço não está na tabela de endereços MAC, então adiciona o endereço MAC e o número da porta de entrada. Em seguida, o switch S1 examina o endereço MAC de destino e observa que este endereço MAC não está na tabela, então o envia para todas as portas.

O PC-B recebe o quadro Ethernet, compara o endereço MAC de destino contra seu próprio endereço MAC e observa que há uma correspondência, e recebe o restante do quadro. O quadro Ethernet continua a ser encaminhado para o switch S2. O switch S2 examina o endereço MAC de origem do quadro e percebe que não está em sua tabela de endereços MAC, então ele adiciona o endereço MAC e a porta de entrada para sua tabela de endereços MAC. Em seguida, o switch S2 examina o endereço MAC de destino e observa que ele não está na tabela, então o envia para todas as portas.

O PC-C recebe o quadro Ethernet e seu endereço MAC não corresponde ao endereço MAC de destino do quadro Ethernet, então não aceita o restante do quadro. O roteador recebe o quadro Ethernet, compara o endereço MAC de destino contra seu próprio endereço MAC e percebe que não há correspondência, então não recebe o restante do quadro.

Agora, vamos pedir ao PC-B que envie um quadro de volta para o PC-A. O endereço MAC de origem do quadro é 00-0B e o de destino é 00-0A. O PC-B o envia para o switch S1. O S1 observa que o endereço MAC de origem não está na tabela de endereços MAC, por isso adiciona o endereço MAC e o número da porta de entrada. Em seguida, o switch S1 examina o endereço MAC de destino e percebe que o endereço MAC está em sua tabela de endereços MAC, então o envia apenas para a porta 1.

O PC-A recebe o quadro Ethernet, compara o endereço MAC de destino contra seu próprio endereço MAC, observa que há uma correspondência e recebe o restante do quadro.

## 21.4.5 Vídeo - Envie o Quadro para o Gateway Padrão

Quando um dispositivo tem um endereço IP em uma rede remota, o quadro Ethernet não pode ser enviado diretamente para o dispositivo de destino. Em vez disso, o quadro Ethernet é enviado ao endereço MAC do gateway padrão, o roteador.

Clique em Reproduzir na figura para ver uma demonstração de como PCA-A se comunica com o gateway padrão.

**Nota**: No vídeo, o pacote IP enviado do PC-A para um destino em uma rede remota tem um endereço IP de origem PC-A e um endereço IP de destino do host remoto. O pacote IP retornado terá o endereço IP de origem do host remoto, e o endereço IP de destino será o de PC-A.

**Selecione o botão Reproduzir para assistir ao vídeo.**

Neste vídeo, o PC-A enviará um pacote para a Internet, pois o endereço IP de destino está em outra rede. Nesse caso, o endereço MAC de origem é o do PC-A e o endereço MAC de destino é o do roteador, 00-0D. O quadro Ethernet é enviado para o switch S1.

O switch S1 recebe o quadro, examina o endereço MAC de origem, que já está em sua tabela de endereços MAC, e apenas atualiza o temporizador de 5 minutos. Em seguida, examina o endereço MAC de destino e, como ele não está na tabela de endereços MAC do switch S1, o envia por todas as portas.

O PC-B recebe o quadro Ethernet e, como o endereço MAC de destino não corresponde a seu próprio endereço MAC, ele não aceita o restante do quadro. O switch S2 recebe o quadro Ethernet, examina o endereço MAC de origem, que já está em sua tabela de endereços MAC, e também apenas atualiza o temporizador de 5 minutos. Em seguida, examina o endereço MAC de destino do quadro, que não está em sua tabela de endereços MAC, então o envia para todas as portas.

O PC-C recebe o quadro Ethernet e, como o endereço MAC de destino não corresponde a seu próprio endereço MAC, ele não aceita o restante do quadro. O roteador recebe o quadro Ethernet e, como o endereço MAC de destino corresponde a seu próprio endereço MAC, ele aceita o restante do quadro.

Agora vamos olhar para o quadro Ethernet vindo do roteador de volta para o PC-A. O endereço IP de origem é o endereço IP do dispositivo em uma rede remota. O endereço MAC de origem é o do roteador, 00-0D, e o endereço MAC de destino é o do PC-A. O quadro é encaminhado para o switch S2.

O S2 recebe o quadro, examina o endereço MAC de origem, que não está em sua tabela de endereços MAC, e então o adiciona. Em seguida, examina o endereço MAC de destino, que já está em sua tabela de endereços MAC, e o encaminha pela porta 1.

O switch S1 recebe o quadro Ethernet, examina o endereço MAC de origem, que não está em sua tabela de endereços MAC, e então o adiciona. Em seguida, examina o endereço MAC de destino, que já está em sua tabela de endereços MAC, e encaminha pela porta 1 para o PC-A.

O PC-A examina o endereço MAC de destino e, como corresponde ao seu próprio endereço MAC, aceita o restante do quadro.

## 21.4.6 Atividade - Use o Switch!

Determine como o switch encaminha um quadro com base no endereço MAC de origem, no endereço MAC de destino e nas informações na tabela MAC do switch. Responda às perguntas usando as informações fornecidas.

![[Pasted image 20260615214230.png]]

### Ajuda

Esta atividade questiona você sobre o conhecimento de como um quadro é encaminhado em um switch.

Clique no botão "Verificar" para verificar sua resposta. Clique no botão "Novo Problema" para iniciar uma nova atividade prática gerada pelo computador.

Você recebe a topologia física e a tabela de endereços MAC do switch. Também receberá um quadro que consiste em um endereço MAC de origem e de destino. As atividades geradas pelo computador terão um par origem e destino que usam os endereços mostrados na topologia. Atividades personalizadas podem usar qualquer endereço desejado na tabela MAC e no quadro.

1. Seu objetivo é determinar como o switch lidará com esse quadro diante da tabela de endereços MAC mostrada.
2. Na primeira pergunta, confira os números de porta para indicar o local (se houver) para onde o switch encaminhará esse quadro.
3. Na segunda pergunta, verifique as opções correspondentes para indicar como o switch lidará com o quadro.
4. Clique no botão "Verificar" para ver se sua resposta está certa.

**Ajuda Adicional:**

"FF" é um endereço MAC de difusão e é encaminhado para todas as portas, com exceção da porta de origem.

Um quadro é **flooded** para todas as portas (exceto a origem) somente se o switch não tiver o MAC de destino dentro da tabela MAC.

O switch só adicionará um novo endereço MAC à tabela MAC com base no endereço MAC de origem. Se o endereço MAC de origem já estiver na tabela, nada será adicionado ou aprendido. Se o endereço MAC de origem não estiver na tabela, o endereço será adicionado.

Um switch eliminará um quadro se os dispositivos de destino e de origem estiverem conectados à mesma porta e o switch tiver o endereço MAC de destino na tabela MAC. Nesta atividade, isso ocorre na única porta conectada ao hub com dois dispositivos host.

# 21.5 Resumo do Ethernet Switching

## 21.5.1 O que eu aprendi neste módulo?

### Ethernet

Não há um protocolo oficial de padrão de rede local, mas, com o tempo, uma tecnologia se tornou mais comum do que as outras: a Ethernet. Os protocolos Ethernet definem como os dados são formatados e transmitidos pela rede com fio. Os padrões Ethernet especificam protocolos que operam nas Camadas 1 e 2 do modelo OSI. Ethernet tornou-se um padrão de fato, o que significa que é a tecnologia usada por quase todas as redes locais com fio.

O IEEE mantém os padrões de rede, incluindo os padrões Ethernet e sem fio. Cada padrão de tecnologia recebe um número referente ao comitê responsável por aprovar e manter o padrão. O padrão Ethernet 802.3 melhorou ao longo do tempo.

Os switches Ethernet podem enviar um quadro para todas as portas (exceto a porta da qual ele foi recebido). Cada host que recebe esse quadro examina o endereço MAC de destino e o compara com o seu endereço MAC. É a placa NIC Ethernet que examina e compara o endereço MAC. Se ele não corresponder ao endereço MAC do host, o restante do quadro será ignorado. Quando é uma correspondência, esse host recebe o restante do quadro e a mensagem que ele contém.

---

### Quadros Ethernet

A Ethernet é definida pelos protocolos 802.2 e 802.3 da camada de enlace de dados. Ethernet suporta larguras de banda de dados de 10 Mbps a 100 Gbps. Os protocolos IEEE 802 LAN/MAN, incluindo Ethernet, usam duas subcamadas separadas da camada de enlace de dados para operar: LLC e MAC.

- **Subcamada LLC** - Esta subcamada IEEE 802.2 se comunica entre o software de rede nas camadas superiores e o hardware do dispositivo nas camadas inferiores. Ela coloca a informação no quadro que identifica qual protocolo de camada de rede está sendo usado para o quadro. Essas informações permitem que vários protocolos da camada 3, como IPv4 e IPv6, usem a mesma interface de rede e mídia.
- **Subcamada MAC** - Esta subcamada (IEEE 802.3, 802.11 ou 802.15 por exemplo) é implementada em hardware e é responsável pelo encapsulamento de dados e controle de acesso ao meio. Ele fornece endereçamento de camada de link de dados e é integrado com várias tecnologias de camada física. O encapsulamento de dados inclui o seguinte: Quadro Ethernet, endereçamento Ethernet e detecção de erros Ethernet.

As LANs Ethernet de hoje usam switches que operam em full-duplex. As comunicações full-duplex com switches Ethernet não exigem controle de acesso através do CSMA/CD. O tamanho mínimo do quadro Ethernet é de 64 bytes e o máximo esperado é de 1518 bytes. Os campos são Preâmbulo e delimitador de quadro inicial, endereço MAC de destino, endereço MAC de origem, tipo/comprimento, dados e FCS. Isso inclui todos os bytes do campo de endereço MAC de destino até o campo FCS.

---

### Endereços MAC Ethernet

Um endereço MAC Ethernet consiste em um valor binário de 48 bits. Hexadecimal é usado para identificar um endereço Ethernet porque um único dígito hexadecimal representa quatro bits binários. Portanto, um endereço MAC Ethernet de 48 bits pode ser expresso usando apenas 12 valores hexadecimais.

Um endereço MAC de unicast é o endereço exclusivo usado quando um quadro é enviado de um único dispositivo de transmissão para um único dispositivo de destino. O processo que um host de origem usa para determinar o endereço MAC de destino associado a um endereço IPv4 é conhecido como ARP (Address Resolution Protocol). O processo que um host de origem usa para determinar o endereço MAC de destino associado a um endereço IPv6 é o ND.

Os recursos de uma transmissão Ethernet são os seguintes:

- Possui um endereço MAC de destino de FF-FF-FF-FF-FF-FF em hexadecimal (48 endereços em binário).
- É inundada todas as portas de switch Ethernet, exceto a porta de entrada.
- Ele não é encaminhado por um roteador.

Os recursos de um multicast Ethernet são os seguintes:

- Há um endereço MAC de destino 01-00-5E quando os dados encapsulados são um pacote multicast IPv4 e um endereço MAC de destino de 33-33 quando os dados encapsulados são um pacote multicast IPv6.
- Há outros endereços MAC de destino multicast reservados para quando os dados encapsulados não são IP, como STP e LLDP.
- É inundada todas as portas de switch Ethernet, exceto a porta de entrada, a menos que o switch esteja configurado para espionagem multicast.
- Ele não é encaminhado por um roteador, a menos que o roteador esteja configurado para rotear pacotes multicast.

---

### A tabela de endereços MAC

Um switch Ethernet da camada 2 usa endereços MAC da camada 2 para tomar decisões de encaminhamento. Ele desconhece completamente os dados (protocolo) que estão sendo transportados na parte de dados do quadro. Um switch Ethernet examina sua tabela de endereços MAC para tomar uma decisão de encaminhamento para cada quadro. A tabela de endereços MAC às vezes é chamada de tabela CAM.

O switch cria a tabela de endereços MAC dinamicamente examinando o endereço MAC de origem dos quadros recebidos em uma porta. O switch encaminha quadros procurando uma correspondência entre o endereço MAC de destino no quadro e uma entrada na tabela de endereços MAC. Se o endereço MAC de destino for um endereço unicast, o switch procurará uma correspondência entre o endereço MAC de destino do quadro e uma entrada em sua tabela de endereços MAC. Se o endereço MAC de destino estiver na tabela, ele encaminhará o quadro pela porta especificada. Se o endereço MAC de destino não estiver na tabela, o switch encaminhará o quadro por todas as portas, exceto a de entrada. Isso é chamado de unicast desconhecido.

À medida que um switch recebe quadros de dispositivos diferentes, ele é capaz de preencher sua tabela de endereços MAC examinando o endereço MAC de origem de cada quadro. Quando a tabela de endereços MAC do switch contém o endereço MAC de destino, ele pode filtrar o quadro e encaminhar uma única porta. Um switch pode ter vários endereços MAC associados a uma única porta. Isso é comum quando o switch está conectado a outro switch. O switch terá uma entrada separada na tabela de endereços MAC para cada quadro recebido com um endereço MAC de origem diferente. Quando um dispositivo tem um endereço IP em uma rede remota, o quadro Ethernet não pode ser enviado diretamente para o dispositivo de destino. Em vez disso, o quadro Ethernet é enviado ao endereço MAC do gateway padrão, o roteador.

---

## 21.5.2 Webster - Reflexão

Marcy e Vincent não tinham ideia de como a rede de pequenas empresas operava. Não é muito mais complicado do que minha própria rede doméstica. Não sabia que havia protocolos que garantiam a interação entre meus dispositivos e com a Internet. Pense na sua rede doméstica ou da escola ou do trabalho. Você entende a diferença entre o endereço IP do seu dispositivo e o endereço MAC? Como esse conhecimento ajuda você a entender melhor o funcionamento da rede?