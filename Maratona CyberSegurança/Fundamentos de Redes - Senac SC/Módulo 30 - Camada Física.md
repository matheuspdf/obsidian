# 30.0 Introdução

## 30.0.1 Webster - Por que devo fazer este módulo?

Tenho uma amiga que gostaria que você conhecesse. O nome dela é Halimah. Ela começou a trabalhar como membro júnior do departamento de TI de uma grande empresa de petróleo e gás especializada em exploração e produção. Sua empresa tem uma sede com vários edifícios e várias filiais em toda a Nigéria.

Neste módulo, você aprenderá sobre a camada física de redes. Halimah já conhece essas informações e precisa usá-las para entender melhor a forma como a rede na sede é construída.

Você está pronto para começar?

## 30.0.2 O que vou aprender neste módulo?

**Título do módulo:** Camada física

**Objetivo do Módulo:** Explicar como os protocolos da camada física, serviços e mídia de rede suportam comunicações entre redes de dados.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Propósito da Camada Física|Descrever a finalidade e as funções da camada física na rede.|
|Características da Camada Física|Descrever as características da camada física.|
|Cabeamento de Cobre|Identificar as características básicas do cabeamento de cobre.|
|Cabeamento UTP|Explicar como o cabo UTP é usado em redes Ethernet.|
|Cabeamento de Fibra Óptica|Descrever o cabeamento de fibra óptica e suas principais vantagens em relação a outros meios físicos.|

# 30.1 Propósito da Camada Física

## 30.1.1 A conexão física

Seja na conexão com uma impressora local em casa ou em um site em outro país, antes que ocorra qualquer comunicação em rede, é necessário estabelecer uma conexão física com uma rede local. Uma conexão física pode ser uma conexão com fio usando um cabo ou uma conexão sem fio usando ondas de rádio.

O tipo de conexão física usada depende da configuração da rede. Por exemplo, em muitos escritórios corporativos, os funcionários têm computadores de mesa ou laptops conectados fisicamente, via cabo, a um switch compartilhado. Esse tipo de configuração é uma rede conectada. Os dados são transmitidos por meio de um cabo físico.

Além das conexões com fio, muitas empresas também oferecem conexões sem fio para notebooks, tablets e smartphones. Com dispositivos sem fio, os dados são transmitidos usando ondas de rádio. A conectividade sem fio é comum, pois indivíduos e empresas descobrem suas vantagens. Os dispositivos em uma rede sem fio devem estar conectados a um ponto de acesso sem fio (AP) ou roteador sem fio como o mostrado na figura.

### Roteador Sem Fio

![[Pasted image 20260626072927.png]]

Estes são os componentes de um ponto de acesso:

1. As antenas sem fio (Elas estão incorporadas dentro da versão do roteador mostrada na figura acima.)
2. Várias portas de switch Ethernet;
3. Uma porta de internet

Semelhante a um escritório corporativo, a maioria das casas oferece conectividade com fio e sem fio para a rede. As figuras mostram um roteador doméstico e um laptop conectando-se à rede local (LAN).

### Conexão com fio ao roteador sem fio

![[Pasted image 20260626072941.png]]**Placas de Interface de Rede**

As placas de interface de rede (NICs) conectam um dispositivo à rede. As NICs Ethernet são usadas para uma conexão com fio, como mostrado na figura, enquanto as NICs da rede local sem fio (WLAN) são usadas para a conexão sem fio. Um dispositivo de usuário final pode incluir um ou os dois tipos de NICs. Uma impressora de rede, por exemplo, pode só ter uma NIC Ethernet e, portanto, deve ser conectada à rede com um cabo Ethernet. Outros dispositivos, como tablets e smartphones, só contém uma NIC WLAN e devem usar uma conexão sem fio.

### Conexão com fio usando uma NIC Ethernet

![[Pasted image 20260626072954.png]]

Nem todas as conexões físicas são iguais, em termos de nível de desempenho, durante uma conexão com uma rede.

## 30.1.2 A Camada Física

A camada física do modelo OSI fornece os meios para transportar os bits que formam o quadro da camada de enlace de dados na mídia de rede. Essa camada aceita um quadro completo da camada de enlace de dados e o codifica como uma série de sinais que são transmitidos à mídia local. Os bits codificados que formam um quadro são recebidos por um dispositivo final ou por um dispositivo intermediário.

Clique em Reproduzir na figura para ver um exemplo do processo de encapsulamento. A última parte deste processo mostra os bits que estão sendo enviados através do meio físico. A camada física codifica os quadros e cria os sinais de onda elétrica, óptica ou de rádio que representam os bits em cada quadro. Esses sinais são então enviados pela mídia, um de cada vez.

A camada física do nó destino recupera esses sinais individuais do meio físico, restaura-os às suas representações de bits e passa os bits para a camada de enlace de dados como um quadro completo.

![[brave_dUXuky1l3v.mp4]]

## 30.1.3 Verifique Seu Entendimento - Objetivo da Camada Física

**Verifique sua compreensão da camada física escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Verdadeiro ou falso? A camada física está relacionada apenas às conexões de rede com fio.

- [ ] Verdadeiro
- [x] Falso

✅ RESPOSTA CORRETA: Falso

> A camada física fornece os meios para transportar bits através da rede, quer a rede esteja com ou sem fio.

---

### Pergunta 2

Verdadeiro ou falso? Quando um quadro é codificado pela camada física, todos os bits são enviados pela mídia ao mesmo tempo.

- [ ] Verdadeiro
- [x] Falso

✅ RESPOSTA CORRETA: Falso

> Quando codificados, os bits que compõem um quadro são transmitidos pela mídia um de cada vez.

---

### Pergunta 3

A camada física do dispositivo receptor passa bits até qual camada de nível superior?

- [ ] Aplicação
- [ ] Apresentação
- [ ] Captura de dados
- [x] Enlace de Dados

✅ RESPOSTA CORRETA: Enlace de Dados

> A camada física recebe quadros da camada de Enlace de Dados e os converte em bits para transmissão. No dispositivo de envio, a camada física passa os bits transmitidos até a camada de Enlace de Dados como um quadro completo.

---

### Pergunta 4

Qual PDU é recebida pela camada física para codificação e transmissão?

- [x] Quadro
- [ ] Segmento
- [ ] Pacote

✅ RESPOSTA CORRETA: Quadro

> A camada física recebe quadros da camada de enlace de Dados para codificação e transmissão


# 30.2 Características da Camada Física

## 30.2.1 Padrões da Camada Física

No tópico anterior, você obteve uma visão geral de alto nível da camada física e seu lugar em uma rede. Este tópico mergulha um pouco mais fundo nas especificidades da camada física. Isso inclui os componentes e a mídia usada para construir uma rede, bem como os padrões necessários para que tudo funcione em conjunto.

Os protocolos e operações das camadas OSI superiores são executados usando software desenvolvido por engenheiros de software e cientistas da computação. Os serviços e protocolos na suíte TCP/IP são definidos pela Internet Engineering Task Force (IETF).

A camada física consiste em circuitos eletrônicos, meios físicos e conectores desenvolvidos pelos engenheiros. Portanto, é aconselhável que os padrões que regem esse hardware sejam definidos pelas organizações de engenharia de comunicações e elétrica relevantes.

Há muitas organizações nacionais e internacionais diferentes, organizações reguladoras de governo e empresas privadas envolvidas no estabelecimento e na manutenção de padrões da camada física. Por exemplo, os padrões de hardware, mídia, codificação e sinalização da camada física são definidos e governados por essas organizações de padrões:

- Organização Internacional para Padronização (ISO)
- Instituto Nacional de Padrões Americano (ANSI) / Associação da Indústria de Telecomunicações (TIA)
- União Internacional de Telecomunicações (ITU)
- Instituto de Engenheiros Elétricos e Eletrônicos (IEEE)
- Autoridades reguladoras de telecomunicações nacionais, incluem Comissão Federal de Comunicação (FCC) nos EUA e Instituto Europeu de Padrões de Telecomunicações (ETSI)

Além desses, geralmente existem grupos regionais de padrões de cabeamento, como CSA (Associação Canadense de Padrões), CENELEC (Comitê Europeu de Padronização Eletrotécnica) e JSA / JIS (Associação Japonesa de Padrões), que desenvolvem especificações locais.

![[Pasted image 20260626073334.png]]

## 30.2.2 Componentes Físicos

Os padrões da camada física abordam três áreas funcionais:

- Componentes Físicos
- Codificação
- Sinalização

**Componentes Físicos**

Os componentes físicos são os dispositivos de hardware eletrônico, mídia e outros conectores que transmitem os sinais que representam os bits. Os componentes de hardware, como NICs, interfaces e conectores, materiais de cabo e projetos de cabo são especificados nos padrões associados à camada física. As várias portas e interfaces em um roteador Cisco 1941 também são exemplos de componentes físicos com conectores e conexões específicos decorrentes de padrões.

## 30.2.3 Codificação

Codificação ou codificação de linha é um método de conversão de um fluxo de bits de dados em um "código" predefinido. Os códigos são agrupamentos de bits usados para fornecer um padrão previsível que pode ser reconhecido tanto pelo emissor quanto pelo receptor. Em outras palavras, a codificação é o método ou o padrão usado para representar as informações digitais. É semelhante a como o código Morse codifica uma mensagem usando uma série de pontos e traços.

Por exemplo, a codificação Manchester representa um bit 0 por uma transição de alta para baixa voltagem, e um bit 1 é representado como uma transição de baixa para alta voltagem. Um exemplo de codificação Manchester é ilustrado na figura. A transição ocorre no meio de cada período de bit. Esse tipo de codificação é usado na Ethernet de 10 Mbps. Taxas de dados mais rápidas exigem uma codificação mais complexa. A codificação Manchester é usada em padrões Ethernet mais antigos, como o 10BASE-T. A Ethernet 100BASE-TX usa codificação 4B/5B e 1000BASE-T usa codificação 8B/10B.

![[Pasted image 20260626073358.png]]

## 30.2.4 Sinalização

A camada física deve gerar os sinais elétricos, ópticos ou sem fio que representam os valores “1” e “0” no meio físico. A maneira como os bits são representados é chamada de método de sinalização. Os padrões de camada física devem definir que tipo de sinal representa o valor “1” e que tipo de sinal representa o valor “0”. Isso pode ser tão simples quanto uma alteração no nível de um sinal elétrico ou de um pulso óptico. Por exemplo, um pulso longo pode representar um 1, enquanto um pulso curto pode representar um 0.

Isso é semelhante ao método de sinalização usado no código Morse, que pode usar uma série de tons de ligar e desligar, luzes ou cliques para enviar o texto por fios telefônicos ou entre as embarcações no mar.

As figuras exibem sinalização

**Clique em cada botão para ver ilustrações de sinalização para cabo de cobre, cabo de fibra óptica e mídia sem fio.**

### Cabo de cobre

**Sinais elétricos sobre cabo de cobre**
![[Pasted image 20260626073507.png]]
### Cabo de fibra ótica
**Pulsos de luz sobre cabo de fibra óptica**

![[Pasted image 20260626073522.png]]

### Mídia Sem Fio
**Sinais de Microondas através de Wireless**

![[Pasted image 20260626073536.png]]

## 30.2.5 Vídeo - Largura de banda

**Selecione o botão Reproduzir para assistir o vídeo.**

Largura de banda é a quantidade de dados que podem ser transmitidos e recebidos durante um período específico, medida em bits por segundo. Os bits vão viajar a uma certa velocidade dependendo do meio físico, como a velocidade da luz usada para enviar bits através de cabo de fibra óptica.

Aqui estão um grupo de 10 bits a serem transmitidos. Vamos enviar esses bits usando uma largura de banda de um bit por segundo. Isso significa que a cada segundo, um bit será transmitido. Com 10 bits sendo transmitidos a uma largura de banda de um bit por segundo, está levando 10 segundos para enviar todos os 10 bits. Claro, isso é incrivelmente lento e as redes atuais normalmente enviam e recebem em milhões de bits por segundo, megabits, ou bilhões de bits por segundo, gigabits.

E se quisermos aumentar nossa largura de banda no mesmo meio físico? Não podemos aumentar a velocidade real com que os bits são enviados pela mídia física, mas podemos aumentar o número de bits que enviamos a cada segundo. Vamos dobrar o número de bits que transmitimos para dois bits por segundo. Usando esses mesmos 10 bits, mas desta vez estão sendo transmitidos a uma largura de banda de dois bits por segundo, então leva apenas cinco segundos para enviar os 10 bits. Observe que a velocidade de deslocamento dos bits não mudou, mas enviamos o dobro de bits a cada segundo, aumentando a Largura de Banda.

## 30.2.6 Largura de banda

Meios físicos diferentes aceitam a transferência de bits a taxas diferentes. A transferência de dados é geralmente discutida em termos de largura de banda. Largura de banda é a capacidade na qual um meio pode transportar dados. A largura de banda digital mede a quantidade de dados que podem fluir de um lugar para outro durante um determinado tempo. A largura de banda é normalmente medida em kilobits por segundo (kbps), megabits por segundo (Mbps) ou gigabits por segundo (Gbps). Às vezes, a largura de banda é pensada como a velocidade em que os bits viajam, no entanto, isso não é preciso. Por exemplo, na Ethernet de 10 Mbps e 100 Mbps, os bits são enviados na velocidade da eletricidade. A diferença é o número de bits que são transmitidos por segundo.

Uma combinação de fatores determina a largura de banda prática de uma rede:

- As propriedades do meio físico
- As tecnologias escolhidas para sinalização e detecção de sinais de rede

As propriedades do meio físico, as tecnologias atuais e as leis da física desempenham sua função na determinação da largura de banda disponível.

A tabela mostra as unidades de medida comumente usadas para largura de banda.

|Unidades de Largura de Banda|Sigla|Equivalência|
|---|---|---|
|Bits por segundo|bps|1 bps = unidade fundamental de largura de banda|
|Quilobits por segundo|Kbps|1 Kbps = 1,000 bps = 10³ bps|
|Megabits por segundo|Mbps|1 Mbps = 1,000,000 bps = 10⁶ bps|
|Gigabits por segundo|Gbps|1 Gbps = 1,000,000,000 bps = 10⁹ bps|
|Terabits por segundo|Tbps|1 Tbps = 1,000,000,000,000 bps = 10¹² bps|

## 30.2.7 Terminologia de largura de banda

Os termos usados para medir a qualidade da largura de banda incluem:

- Latência
- Rendimento
- Goodput

**Latência**

O termo latência se refere ao tempo necessário para os dados viajarem de um ponto a outro, incluindo atrasos.

Em uma internetwork ou em uma rede com vários segmentos, a taxa de transferência não pode ser mais rápida que o link mais lento no caminho da origem ao destino. Mesmo que todos ou a maioria dos segmentos tenham alta largura de banda, será necessário apenas um segmento no caminho com baixa taxa de transferência para criar um gargalo na taxa de transferência de toda a rede.

**Taxa de Transferência**

Taxa de transferência é a medida da transferência de bits através da mídia durante um determinado período.

Devido a alguns fatores, geralmente a taxa de transferência não corresponde à largura de banda especificada nas implementações da camada física. A taxa de transferência geralmente é menor que a largura de banda. Existem muitos fatores que influenciam a taxa de transferência:

- A quantidade de tráfego
- O tipo de tráfego
- A latência criada pelo número de dispositivos de rede encontrados entre a origem e o destino

Existem muitos testes de velocidade on-line que podem revelar a taxa de transferência de uma conexão com a Internet. A figura fornece exemplos de resultados de um teste de velocidade.

**Goodput**

Há uma terceira medida para avaliar a transferência de dados utilizáveis; é conhecido como goodput. Goodput é a medida de dados usáveis transferidos em um determinado período. Goodput é a taxa de transferência menos a sobrecarga de tráfego para estabelecer sessões, reconhecimentos, encapsulamento e bits retransmitidos. O goodput é sempre menor que a taxa de transferência, que geralmente é menor do que a largura de banda.![[Pasted image 20260626073918.png]]

## 30.2.8 Verifique Seu Entendimento - Características da camada física

**Verifique sua compreensão das características da camada física escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Que mídia usa padrões de microondas para representar bits?

- [ ] fibra óptica
- [ ] cobre
- [x] sem fio

✅ RESPOSTA CORRETA: sem fio

> Em redes sem fio, os dados são representados por padrões de transmissões de microondas.

---

### Pergunta 2

Que mídia usa padrões de luz para representar bits?

- [x] fibra óptica
- [ ] cobre
- [ ] sem fio

✅ RESPOSTA CORRETA: fibra óptica

> Cabos de fibra óptica usam padrões de luz para representar bits.

---

### Pergunta 3

Que mídia usa pulsos elétricos para representar bits?

- [ ] fibra óptica
- [ ] sem fio
- [x] cobre

✅ RESPOSTA CORRETA: cobre

> Os pulsos elétricos são usados para representar bits em redes usando mídia de cabo de cobre.

---

### Pergunta 4

Qual deles é o nome para a capacidade de um meio para transportar dados?

- [ ] goodput
- [ ] taxa de transferência
- [x] largura de banda

✅ RESPOSTA CORRETA: largura de banda

> Largura de banda é a capacidade de um meio de rede para transportar dados.

---

### Pergunta 5

Qual destes é uma medida da transferência de bits pela mídia?

- [ ] largura de banda
- [ ] goodput
- [x] taxa de transferência

✅ RESPOSTA CORRETA: taxa de transferência

> A transferência de bits pela mídia da rede durante um período de tempo é conhecida como taxa de transferência.


# 30.3 Cabeamento de Cobre

## 30.3.1 Características do Cabeamento de Cobre

O cabeamento de cobre é o tipo mais comum de cabeamento usado nas redes hoje em dia. Na verdade, o cabeamento de cobre não é apenas um tipo de cabo. Existem três tipos diferentes de cabeamento de cobre que são usados em situações específicas.

As redes usam mídia de cobre porque é barata, fácil de instalar e tem baixa resistência à corrente elétrica. Entretanto, ela é limitada pela distância e interferência de sinal.

Os dados são transmitidos por cabos de cobre como pulsos elétricos. Um detector na interface de rede de um dispositivo destino tem que receber um sinal que poderá ser decodificado com êxito para corresponder ao sinal enviado. No entanto, quanto mais o sinal viaja, mais ele se deteriora. Isso se chama atenuação de sinal. Por isso, todas as mídias de cobre devem seguir limitações de distância rigorosas, conforme especificado nos padrões de orientação.

A temporização e a voltagem dos pulsos elétricos também são suscetíveis à interferência de duas fontes:

- **Interferência eletromagnética (EMI) ou interferência de radiofrequência (RFI) –** os sinais EMI e RFI podem distorcer e corromper os sinais de dados transportados pelo meio físico de cobre. Possíveis fontes de EMI e RFI são dispositivos de ondas de rádio e eletromagnéticos, como luzes fluorescentes ou motores elétricos.
- **Crosstalk -** Crosstalk é um distúrbio causado pelos campos elétricos ou magnéticos de um sinal em um fio para o sinal em um fio adjacente. Nos circuitos de telefone, a diafonia pode fazer com que parte de outra conversa de voz de um circuito adjacente seja ouvida (linha cruzada). Especificamente, quando uma corrente elétrica flui através de um cabo, ela cria um pequeno campo magnético circular ao redor do cabo, que pode ser captado por um cabo adjacente.

A figura mostra como a transmissão de dados pode ser afetada pela interferência.

![[Pasted image 20260626074208.png]]


Para contrabalançar os efeitos negativos da EMI e da RFI, alguns tipos de cabos de cobre têm proteção metálica e exigem conexões devidamente aterradas.

Para contrabalançar os efeitos negativos do crosstalk, alguns tipos de cabos de cobre têm pares de cabos de circuitos opostos juntos, o que efetivamente cancela o crosstalk.

A suscetibilidade dos cabos de cobre ao ruído eletrônico também pode ser limitada usando estas recomendações:

- Selecionar o tipo ou categoria de cabo mais adequado para um determinado ambiente de rede
- Projetar uma infraestrutura de cabos para evitar fontes conhecidas e potenciais de interferência na estrutura do edifício
- Usar técnicas de cabeamento que incluem o manuseio e a terminação adequados dos cabos

## 30.3.2 Tipos de Cabeamento de Cobre

Há três tipos principais de mídias de cobre usadas em redes.

![[Pasted image 20260626074239.png]]

## 30.3.3 Par trançado não blindado (UTP)

O cabeamento de par trançado não blindado (UTP) é o meio físico de rede mais comum. O cabeamento UTP, terminado com conectores RJ-45, é usado para interconectar hosts de rede com dispositivos de rede intermediários, como switches e roteadores.

Nas LANs, o cabo UTP consiste em quatro pares de cabos codificados por cores que foram trançados e depois colocados em uma capa plástica flexível que protege contra danos físicos menores. O processo de trançar cabos ajuda na proteção contra interferência de sinais de outros cabos.

Conforme visto na figura, os códigos de cores identificam os pares e fios individuais para auxiliar na terminação do cabo.

![[Pasted image 20260626074255.png]]

## 30.3.4 Par Trançado Blindado (STP)

O par trançado blindado (STP) oferece maior proteção contra ruído do que o cabeamento UTP. No entanto, em comparação com o cabo UTP, o cabo STP é significativamente mais caro e difícil instalação. Assim como o cabo UTP, o STP usa um conector RJ-45.

Os cabos STP combinam as técnicas de blindagem para contrabalançar a EMI e a RFI, e são trançados para conter o crosstalk. Para aproveitar totalmente a blindagem, os cabos STP são terminados com conectores de dados STP blindados especiais. Se o cabo não estiver devidamente aterrado, a blindagem poderá atuar como uma antena e captar sinais indesejados.

O cabo STP mostrado usa quatro pares de cabo, envolvidos em blindagens, que são colocados em uma proteção ou revestimento geral metálico.

![[Pasted image 20260626074311.png]]

## 30.3.5 Cabo Coaxial

O cabo coaxial, ou coax para abreviar, recebeu seu nome porque tem dois condutores que compartilham o mesmo eixo. Conforme mostrado na figura, o cabo coaxial consiste no seguinte:

- Um condutor de cobre é usado para transmitir os sinais eletrônicos.
- Uma camada de isolamento plástico flexível envolve um condutor de cobre.
- O material de isolamento é envolvido em uma malha de cobre com tecido, ou uma folha metálica, que atua como o segundo cabo no circuito e uma proteção para o condutor interno. Essa segunda camada, ou blindagem, também reduz a quantidade de interferência eletromagnética externa.
- Todo o cabo é coberto com um revestimento para evitar danos físicos menores.

Há tipos diferentes de conectores utilizados com o cabo coax. Os conectores Bayonet Neill-Concelman (BNC), tipo N e tipo F são mostrados na figura.

Embora o cabo UTP tenha substituído essencialmente o cabo coaxial nas modernas instalações Ethernet, o design do cabo coaxial é usado nas seguintes situações:

- **Instalações sem fio** - Cabos coaxiais conectam antenas aos dispositivos sem fio. O cabo coaxial transporta a energia de radiofrequência (RF) entre as antenas e o equipamento de rádio.
- **Instalações de Internet a cabo** - Os provedores de serviços a cabo fornecem conectividade à Internet para seus clientes, substituindo partes do cabo coaxial e suportando elementos de amplificação por cabo de fibra óptica. No entanto, o cabeamento dentro das instalações do cliente ainda é coaxial.

![[Pasted image 20260626074326.png]]

## 30.3.6 Verifique Seu Entendimento - Cabeamento de Cobre

**Verifique sua compreensão do cabeamento de cobre escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Qual das seguintes opções conecta antenas a dispositivos sem fio? Também pode associado a cabeamento de fibra óptica para transmissão de dados bidirecionais.

- [x] coaxial
- [ ] STP
- [ ] UTP

✅ RESPOSTA CORRETA: coaxial

> O cabo coaxial, que é usado para TV a cabo e serviço de internet, também é usado para conectar antenas a dispositivos sem fio.

---

### Pergunta 2

Qual dos seguintes opções evita EMI e RFI usando técnicas de blindagem e conectores especiais?

- [ ] UTP
- [ ] coaxial
- [x] STP

✅ RESPOSTA CORRETA: STP

> O cabo de par trançado blindado (STP) incorpora blindagem e conectores especiais para evitar interferência de sinal de outros fios, EMI e RFI.

---

### Pergunta 3

Qual dos seguintes é a mídia de rede mais comum?

- [ ] STP
- [ ] coaxial
- [x] UTP

✅ RESPOSTA CORRETA: UTP

> O cabo de par trançado (UTP) não blindado é o tipo mais comum de mídia de rede com fio.

---

### Pergunta 4

Qual das alternativas a seguir termina com conectores BNC, tipo N e tipo F?

- [ ] UTP
- [x] coaxial
- [ ] STP

✅ RESPOSTA CORRETA: coaxial

> O cabo coaxial, que é usado para TV a cabo e serviço de internet e para conectar antenas a dispositivos sem fio, usa vários tipos de conectores para incluir conectores BNC, tipo N e tipo F.