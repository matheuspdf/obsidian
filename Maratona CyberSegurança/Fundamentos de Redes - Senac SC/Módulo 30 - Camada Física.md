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


# 30.4 Cabeamento UTP

## 30.4.1 Propriedades do Cabo UTP

No tópico anterior, você aprendeu um pouco sobre o cabeamento de cobre de par trançado não blindado (UTP). Como o cabeamento UTP é o padrão para uso em LANs, este tópico entra em detalhes sobre suas vantagens e limitações e o que pode ser feito para evitar problemas.

Quando usado como meio de rede, o cabeamento UTP consiste em quatro pares de fios de cobre com código de cores que foram torcidos juntos e depois envoltos em uma bainha de plástico flexível. Seu tamanho reduzido pode ser vantajoso durante a instalação.

O cabo UTP não usa blindagem para contrabalançar os efeitos de EMI e RFI. Em vez disso, os projetistas de cabos descobriram outras maneiras de limitar o efeito negativo da diafonia:

- **Cancelamento** - Os designers agora dispõe os fios em um circuito em pares. Quando dois fios de um circuito elétrico são colocados próximos um do outro, seus campos magnéticos serão opostos. Assim, os dois campos magnéticos cancelam um ao outro e também podem cancelar sinais externos de EMI e RFI.
- **Variando o número de torções por par de fios -** Para aumentar ainda mais o efeito de cancelamento de fios de circuitos pareados, os projetistas variam o número de torções de cada par de fios em um cabo. O cabo UTP deve seguir especificações precisas que orientam quantas tranças são permitidas por metro (3,28 pés) do cabo. Observe na figura que o par laranja/laranja e branco é menos trançado do que o par azul/azul e branco. Cada par colorido é trançado um número de vezes diferente.

O cabo UTP depende exclusivamente do efeito de cancelamento produzido pelos pares de fios trançados para limitar a degradação de sinal e fornecer efetivamente a autoblindagem para cabos trançados na mídia de rede.![[Pasted image 20260628225413.png]]


## 30.4.2 Padrões de Cabeamento e Conectores UTP

O cabeamento UTP está em conformidade com os padrões estabelecidos conjuntamente pela ANSI/TIA. Especificamente, o ANSI/TIA-568 estipula os padrões de cabeamento comercial para instalações de LAN e é o padrão mais comumente usado em ambientes de cabeamento de LAN. Alguns dos elementos definidos são os seguintes:

- Tipos de cabo
- Comprimento do cabo
- Conectores
- Terminação do cabo
- Métodos de teste de cabo

As características elétricas do cabeamento de cobre são definidas pelo Instituto de Engenharia Elétrica e Eletrônica (IEEE). O IEEE classifica o cabeamento UTP de acordo com o desempenho. Os cabos são colocados nas categorias, com base na capacidade de transportar taxas de largura de banda mais altas. Por exemplo, o cabo Categoria 5 é usado normalmente em instalações 100BASE-TX Fast Ethernet. Outras categorias incluem cabo Categoria 5 aprimorado (5e), Categoria 6 e Categoria 6a.

Os cabos em categorias mais altas são desenvolvidos e construídos para suportar taxas de dados mais elevadas. À medida que novas tecnologias Ethernet de velocidade de gigabit estão sendo desenvolvidas e adotadas, a Categoria 5e é agora o tipo de cabo minimamente aceitável, com a Categoria 6 sendo o tipo recomendado para novas instalações prediais.

A figura mostra três categorias de cabo UTP:

- A categoria 3 foi originalmente usada para comunicação de voz por linhas de voz, mas posteriormente usada para transmissão de dados.
- As categorias 5 e 5e são usadas para transmissão de dados. A Categoria 5 suporta 100Mbps e a Categoria 5e suporta 1000 Mbps.
- A categoria 6 tem um separador adicionado entre cada par de fios para suportar velocidades mais altas. Categoria 6 suporta até 10 Gbps.
- Categoria 7 também suporta 10 Gbps.
- Categoria 8 suporta 40 Gbps.

Alguns fabricantes produzem cabos que excedem as especificações da Categoria ANSI/TIA 6a e os classificam como Categoria 7.

![[Pasted image 20260628225453.png]]

O cabo UTP geralmente é terminado com um conector RJ-45. O padrão ANSI/TIA-568 descreve os códigos de cores dos fios, para atribuições de pinos (pinagem), para cabos Ethernet.

Conforme mostrado na figura, o conector RJ-45 é o componente macho, prensado na extremidade do cabo.

### Plugues RJ-45 para UTP

![[Pasted image 20260628225512.png]]
O soquete, mostrado na figura, é o componente fêmea de um dispositivo de rede, tomada de parede, tomada de conduíte ou painel de conexões. Quando terminado incorretamente, o cabo é uma fonte potencial de degradação do desempenho da camada física.

### Sockets UTP RJ-45

![[Pasted image 20260628225634.png]]

Esta figura mostra um exemplo de um cabo UTP mal terminado. Esse conector defeituoso possui fios expostos, sem torção e não totalmente cobertos pela bainha.

### Cabo UTP mal terminado

![[Pasted image 20260628225646.png]]

A figura seguinte mostra um cabo UTP devidamente terminado. É um bom conector com fios que não são torcidos apenas na extensão necessária para conectar o conector.

### Cabo UTP devidamente encerrado

![[Pasted image 20260628225658.png]]

**Nota**: A terminação inadequada do cabo pode afetar o desempenho da transmissão.

## 30.4.3 Cabos UTP diretos e cruzados

Situações diversas podem exigir que os cabos UTP sejam conectados de acordo com diferentes convenções de fiação. Isso significa que os fios individuais do cabo precisam ser conectados em ordem diferente para conjuntos diferentes de pinos nos conectores RJ-45.

Estes são os principais tipos de cabo obtidos com o uso de convenções de cabeamento específicas:

- **Ethernet direto -** o tipo mais comum de cabo de rede. Geralmente é usado para interconectar um host a um switch e um switch a um roteador.
- **Ethernet Cruzado (Crossover) -** Um cabo usado para interconectar dispositivos semelhantes. Por exemplo, para conectar um switch a um switch, um host a um host ou um roteador a um roteador. No entanto, os cabos cruzados agora são considerados legados, pois as NICs usam o cruzamento de interface dependente médio (Auto-MDIX) para detectar automaticamente o tipo de cabo e fazer a conexão interna.

**Nota**: Outro tipo de cabo é o cabo rollover, que é proprietário da Cisco. É usado para conectar uma estação de trabalho a uma porta do console do roteador ou do switch.

O uso incorreto de um cabo crossover ou direto entre dois dispositivos não danifica os dispositivos, mas a conectividade e comunicação entre os dispositivos não será realizada. Este é um erro comum e verificar se as conexões do dispositivo estão corretas deve ser a primeira ação de solução de problemas se a conectividade não for alcançada.

A figura identifica os pares de fios individuais para os padrões T568A e T568B.

### PadrõesT568A e T568B

![[Pasted image 20260628225721.png]]

A tabela mostra o tipo de cabo UTP, padrões relacionados e aplicação típica desses cabos.

**Tipos e padrões de cabos**

|Tipo do Cabo|Padrão|Aplicação|
|---|---|---|
|Ethernet Direto|Ambas as extremidades T568A ou T568B|Conecta um host de rede a um dispositivo de rede, como um switch ou hub|
|Ethernet Cruzado|Uma extremidade T568A, outra extremidade T568B|Conecta dois dispositivos intermediários de rede (switch para switch ou roteador para roteador)|
|Rollover|Proprietário da Cisco|Conecta uma porta serial de estação de trabalho a uma porta de console do roteador usando um adaptador|

## 30.4.4 Atividade - Pinagens de Cabo

Para esta atividade, ordene corretamente as cores dos fios para uma pinagem de cabo ANSI/TIA. Selecione uma cor do encapamento do fio clicando nela. Em seguida, clique em um fio para aplicar esse invólucro a ele.

**Selecione a caixa do pino e, em seguida, o pino do cabo para aplicar o invólucro.**

![[Pasted image 20260628225844.png]]

Para esta atividade, ordene corretamente as cores dos fios para uma pinagem de cabo ANSI/TIA. Selecione uma cor do encapamento do fio clicando nela. Em seguida, clique em um fio para aplicar esse invólucro a ele.

**Selecione a caixa do pino e, em seguida, o pino do cabo para aplicar o invólucro.**

![[Pasted image 20260628225902.png]]

# 30.5 Cabeamento de Fibra Óptica

## 30.5.1 Propriedades do cabeamento de fibra óptica

Como você aprendeu, o cabeamento de fibra óptica é o outro tipo de cabeamento usado em redes. Por ser caro, não é tão comumente usado quanto os vários tipos de cabeamento de cobre. Mas o cabeamento de fibra óptica tem certas propriedades que o tornam a melhor opção em certas situações, que você descobrirá neste tópico.

O cabo de fibra óptica transmite dados por longas distâncias e a larguras de banda mais altas do que qualquer outra mídia de rede. Diferentemente dos fios de cobre, o cabo de fibra óptica pode transmitir sinais com menos atenuação e é completamente imune à interferência de EMI e RFI. A fibra óptica é comumente usada para interconectar dispositivos de rede.

A fibra óptica é um fio flexível, extremamente fino e transparente de vidro muito puro, não muito mais espesso do que um fio de cabelo humano. Os bits são codificados na fibra como pulsos de luz. O cabo de fibra óptica atua como um guia de onda, ou “tubo de luz”, para transmitir luz entre as duas extremidades com o mínimo de perda do sinal.

Como uma analogia, considere um rolo de papel toalha vazio com o interior revestido como um espelho. Ele tem mil metros de comprimento e um pequeno ponteiro laser é usado para enviar sinais de código Morse na velocidade da luz. Basicamente, é assim que o cabo de fibra óptica funciona, só que tem um diâmetro menor e usa tecnologias de luz sofisticadas.

![[Pasted image 20260628230000.png]]

## 30.5.2 Tipos de Fibra

Os cabos de fibra óptica são amplamente classificados em dois tipos:

- Fibra monomodo (SMF)
- Fibra multimodo (MMF)

**Clique em cada botão para obter uma ilustração e explicação de cada tipo.**

### **Fibra Monomodo**

O SMF consiste em um núcleo muito pequeno e usa a tecnologia laser cara para enviar um único raio de luz, conforme mostrado na figura. O SMF é popular em situações de longa distância que se estendem por centenas de quilômetros, como os exigidos em aplicações de telefonia de longo curso e TV a cabo.
![[Pasted image 20260628230037.png]]

### **Fibra Multimodo**

O MMF consiste em um núcleo maior e usa emissores de LED para enviar pulsos de luz. Especificamente, a luz de um LED entra na fibra multimodo em diferentes ângulos, como mostrado na figura. Os MMFs são populares em LANs porque podem ser alimentados por LEDs de baixo custo. Ele fornece largura de banda de até 10 Gbps em links de até 550 metros de comprimentos.
![[Pasted image 20260628230046.png]]

Uma das diferenças destacadas entre MMF e SMF é a quantidade de dispersão. O termo dispersão se refere ao espalhamento do pulso de luz com o tempo. Maior dispersão significa aumento da perda de força do sinal. MMF tem uma dispersão maior do que SMF. É por isso que o MMF só pode viajar até 500 metros antes da perda de sinal.


## 30.5.3 Uso de cabeamento de fibra óptica

Agora, o cabeamento de fibra óptica é usado em quatro setores:

- **Redes Corporativas -** Isso é usado para aplicativos de cabeamento de backbone e dispositivos de infraestrutura de interconexão.
- **Fiber-to-the-Home (FTTH) -** Isso é usado para fornecer serviços de banda larga sempre ativos para residências e pequenas empresas.
- **Redes de longa distância -** Isso é usado por provedores de serviços para conectar países e cidades.
- **Redes de Cabos Submarinos -** São usadas para fornecer soluções confiáveis de alta velocidade e alta capacidade, capazes de sobreviver em ambientes submarinos hostis em distâncias transoceânicas. Pesquise na internet por “mapa de telegeografia de cabos submarinos” para visualizar vários mapas on-line.

Nosso foco neste curso é o uso de fibra dentro da empresa.

## 30.5.4 Conectores de fibra óptica

Um conector de fibra óptica termina o final de uma fibra óptica. Uma variedade de conectores de fibra óptica estão disponíveis. As principais diferenças entre os tipos de conectores são as dimensões e os métodos de acoplamento. As empresas decidem os tipos de conectores que serão usados, com base no seu equipamento.

**Nota**: Alguns switches e roteadores têm portas que suportam conectores de fibra óptica por meio de um transceptor plugável de fator de forma pequeno (SFP). Pesquise na internet para vários tipos de SFPs.

**Clique em cada tipo de conector de fibra óptica para obter uma imagem e obter mais informações.**


### Conectores de Ponta Reta (Straight-Tip - ST)

Os conectores ST foram um dos primeiros tipos de conectores usados. O conector trava com segurança com um mecanismo estilo baioneta 'twist-on/twist-off'.
![[Pasted image 20260628230208.png]]

### Conectores SC (Conectores de Assinante)

Os conectores SC às vezes são chamados de 'conectores quadrados' ou 'conectores padrão'. Eles são um conector LAN e WAN amplamente adotado que usa um mecanismo push-pull para garantir uma inserção positiva. Esse tipo de conector é usado com fibra multimodo e monomodo.
![[Pasted image 20260628230219.png]]
### Conectores Lucent (LC) Simplex

Os conectores LC simplex são uma versão menor do conector SC. Às vezes, eles são chamados de conectores pequenos ou locais e estão crescendo rapidamente em popularidade devido ao seu tamanho menor.
![[Pasted image 20260628230241.png]]



### Conectores LC duplex, multimodo

Um conector LC multimodo duplex é semelhante a um conector LC simplex, mas usa um conector duplex.
![[Pasted image 20260628230301.png]]

Até recentemente, a luz só podia viajar em uma direção sobre fibra óptica. Duas fibras eram necessárias para suportar a operação full duplex. Portanto, os cabos de conexão de fibra óptica agrupam dois cabos de fibra óptica e os terminam com um par de conectores padrão de fibra única. Alguns conectores de fibra aceitam fibras de transmissão e de recepção em um único conector, conhecido como conector duplex, conforme mostrado no Conector LC Duplex Multimodo na Figura. Padrões BX, como 100BASE-BX, usam comprimentos de onda diferentes para enviar e receber através de uma única fibra.

## 30.5.5 Patch Cords de Fibra

Os cabos de fibra são necessários para interconectar dispositivos da infraestrutura. O uso das cores diferencia entre cabos monomodo e multimodo. A cor amarela indica cabos de fibra monomodo e o laranja é para cabos de fibra multimodo.

**Clique em cada cabo de fibra para obter uma imagem.**

### Cabo multimodo SC-SC
![[Pasted image 20260628230357.png]]

### Cabo de ligação monomodo LC-LC
![[Pasted image 20260628230415.png]]

### Cabo multimodo ST-LC
![[Pasted image 20260628230621.png]]

### Cabo de ligação monomodo SC-ST
![[Pasted image 20260628230641.png]]

**Nota**: Os cabos de fibra devem ser protegidos com uma pequena tampa plástica quando não estiverem em uso.

## 30.5.6 Fibra Versus Cobre

Há muitas vantagens em usar o cabo de fibra óptica em comparação com o cabo de cobre. A tabela destaca algumas dessas diferenças.

Atualmente, na maioria dos ambientes empresariais, a fibra óptica é usada principalmente como cabeamento de backbone para conexões ponto a ponto de alto tráfego entre instalações de distribuição de dados. Ele também é usado para a interconexão de edifícios em campus multi-construção. Como os cabos de fibra ótica não conduzem eletricidade e têm uma baixa perda de sinal, eles são adequados para esses usos.

**Comparação de cabeamento UTP e fibra óptica**

|Problemas de Implementação|Cabeamento UTP|Cabeamento de Fibra Óptica|
|---|---|---|
|Largura de banda suportada|10 Mbps – 10 Gbps|10 Mbps – 100 Gbps|
|Distância|Relativamente curto (1 – 100 metros)|Relativamente longo (1 – 100.000 metros)|
|Imunidade a interferência eletromagnética e de frequências de rádio|Baixa|Alto (totalmente imune)|
|Imunidade a perigos elétricos|Baixa|Alto (totalmente imune)|
|Custos da mídia e dos conectores|Mais baixo|Mais alta|
|Habilidades necessárias para a instalação|Mais baixo|Mais alta|
|Precauções de segurança|Mais baixo|Mais alta|


### Pergunta 1

Qual dos seguintes tipos de cabos de fibra óptica pode ajudar os dados a percorrer aproximadamente 500 metros?

- [ ] Monomodo
- [x] Multimodo

✅ RESPOSTA CORRETA: Multimodo

> A fibra multimodo tem uma limitação de distância mais curta do que a fibra monomodo. Comumente usado em LANs com uma distância de algumas centenas de metros, mas pode ser de até 2 km.

---

### Pergunta 2

Qual dos seguintes tipos de cabos de fibra óptica usa diodos emissores de luz (LEDs) como fonte de luz para transmissão de dados?

- [ ] Monomodo
- [x] Multimodo

✅ RESPOSTA CORRETA: Multimodo

> A fibra multimodo usou LEDs como fonte de luz.

---

### Pergunta 3

Qual dos seguintes tipos de cabos de fibra óptica usa lasers em um único fluxo como fonte de luz para transmissão de dados?

- [x] Monomodo
- [ ] Multimodo

✅ RESPOSTA CORRETA: Monomodo

> A fibra monomodo usa a tecnologia laser como fonte de luz.

---

### Pergunta 4

Qual dos seguintes tipos de cabo de fibra óptica é usado para conectar aplicativos de telefonia de longa distância e TV a cabo?

- [x] Monomodo
- [ ] Multimodo

✅ RESPOSTA CORRETA: Monomodo

> A fibra monomodo é comumente usada para aplicações de TV e telefonia de longo curso.

---

### Pergunta 5

Qual dos seguintes tipos de cabos de fibra óptica pode percorrer aproximadamente 100 km?

- [x] Monomodo
- [ ] Multimodo

✅ RESPOSTA CORRETA: Monomodo

> A fibra monomodo é usada para aplicações de longo curso até 100 km.

---

### Pergunta 6

Qual dos seguintes tipos de cabos de fibra óptica é usado em uma rede de campus?

- [ ] Monomodo
- [x] Multimodo

✅ RESPOSTA CORRETA: Multimodo

> A fibra multimodo tem uma limitação de distância mais curta do que a fibra monomodo. Comumente usado em LANs dentro de uma rede de campus.


# 30.6 Resumo da Camada Física

## 30.6.1 O Que Aprendi Neste Módulo?

### Propósito da Camada Física

Antes que qualquer comunicação de rede possa ocorrer, é necessário estabelecer uma conexão física com uma rede local. Uma conexão física pode ser uma conexão com fio usando um cabo ou uma conexão sem fio usando ondas de rádio. As placas de interface de rede (NICs) conectam um dispositivo à rede. As NICs Ethernet são usadas para uma conexão com fio, enquanto as NICs WLAN (Rede Local Sem Fio) são usadas para conexão sem fio. A camada física do modelo OSI fornece os meios para transportar os bits que formam um quadro da camada de enlace de dados no meio físico de rede. Ela aceita um quadro completo da camada de enlace de dados e o codifica como uma série de sinais que são transmitidos para o meio físico local. Os bits codificados que compreendem um quadro são recebidos por um dispositivo final ou um dispositivo intermediário.

---

### Características da Camada Física

A camada física consiste em circuitos eletrônicos, meios físicos e conectores desenvolvidos pelos engenheiros. Os padrões da camada física abordam três áreas funcionais: componentes físicos, codificação e sinalização. Largura de banda é a capacidade na qual um meio pode transportar dados. A largura de banda digital mede a quantidade de dados que podem fluir de um lugar para outro durante um determinado tempo. A taxa de transferência é a medida da transferência de bits pela mídia durante um determinado período de tempo e geralmente é menor que a largura de banda. O termo latência se refere ao tempo necessário para os dados viajarem de um ponto a outro, incluindo atrasos. Goodput é a medida de dados usáveis transferidos em um determinado período. A camada física produz a representação e os agrupamentos de bits para cada tipo de mídia da seguinte maneira:

- **Cabo de cobre** – Os sinais são padrões de pulsos elétricos.
- **Cabo de fibra óptica** – Os sinais são padrões de luz.
- **Sem fio** – Os sinais são padrões de transmissões por microondas.

---

### Cabeamento de Cobre

As redes usam mídia de cobre porque é barata, fácil de instalar e tem baixa resistência à corrente elétrica. Entretanto, ela é limitada pela distância e interferência de sinal. Os valores de tempo e tensão dos pulsos elétricos também são suscetíveis à interferência de duas fontes: EMI e diafonia. Três tipos de cabeamento de cobre são: UTP, STP e cabo coaxial (coaxial). UTP tem uma jaqueta externa para proteger os fios de cobre contra danos físicos, pares torcidos para proteger o sinal de interferência e isolamento plástico codificado por cores que isolam eletricamente os fios uns dos outros e identifica cada par. O cabo STP usa quatro pares de fios, cada um enrolado em uma blindagem de alumínio, que é enrolada em uma trança ou folha metálica geral. O cabo coaxial recebe esse nome pelo fato de haver dois condutores que compartilham o mesmo eixo. Coax é usado para conectar antenas a dispositivos sem fio. Os provedores de internet por cabo usam coaxial dentro das instalações de seus clientes.

---

### Cabeamento UTP

O cabeamento UTP consiste em quatro pares de fios de cobre com código de cores que foram torcidos juntos e depois envoltos em uma bainha de plástico flexível. O cabo UTP não usa blindagem para contrabalançar os efeitos de EMI e RFI. Em vez disso, os projetistas de cabos descobriram outras maneiras de limitar o efeito negativo da diafonia: cancelamento e variação do número de torções por par de fios. O cabeamento UTP está em conformidade com os padrões estabelecidos conjuntamente pela ANSI/TIA. As características elétricas do cabeamento de cobre são definidas pelo Instituto de Engenharia Elétrica e Eletrônica (IEEE). O cabo UTP geralmente é terminado com um conector RJ-45. Os principais tipos de cabos que são obtidos usando convenções de fiação específicas são Ethernet Direto (Straight-through) e Ethernet Cruzado (Crossover). A Cisco tem um cabo UTP proprietário chamado rollover que conecta uma estação de trabalho a uma porta de console do roteador.

---

### Cabeamento de Fibra Óptica

O cabo de fibra óptica transmite dados por longas distâncias e a larguras de banda mais altas do que qualquer outra mídia de rede. O cabo de fibra óptica pode transmitir sinais com menos atenuação que o fio de cobre e é completamente imune a EMI e RFI. A fibra óptica é um fio flexível, extremamente fino e transparente de vidro muito puro, não muito mais espesso que um fio de cabelo humano. Os bits são codificados na fibra como pulsos de luz. O cabeamento de fibra óptica está sendo utilizado agora em quatro tipos de indústria: redes empresariais, FTTH, redes de longo curso e redes de cabos submarinos. Existem quatro tipos de conectores de fibra óptica: ST, SC, LC e LC multimodo duplex. Os cabos de patch de fibra óptica incluem multimodo SC-SC, monomodo LC-LC, multimodo ST-LC e monomodo SC-ST. Na maioria dos ambientes empresariais, a fibra óptica é usada principalmente como cabeamento de backbone para conexões ponto a ponto de alto tráfego entre instalações de distribuição de dados e para a interconexão de edifícios em campi de vários edifícios.

---

## 30.6.2 Webster – Questões para Reflexão

Halimah já sabia sobre a camada física na rede. E você?

Neste módulo, você aprendeu que uma conexão física pode ser uma conexão com fio usando um cabo ou uma conexão sem fio usando ondas de rádio. Os tipos de mídia também foram discutidos.

Faça a si mesmo estas perguntas de reflexão:

Já pensou na diferença entre cabo de cobre, cabo de fibra óptica e rede sem fio?

Que tipos de mídia são usados em sua casa?

Quais são as vantagens e desvantagens desses tipos de mídia que você tem em sua casa? Onde você pode encontrar cabos de fibra óptica sendo usados?

Quais vantagens os cabos de fibra óptica oferecem?