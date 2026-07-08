# 2.1 Clientes e Servidores
## 2.1.1 Vídeo - Clientes e Servidores

![[2.1.1.mp4#subtitle=anexos/2.1.1.vtt]]
### Clientes e Servidores

Em redes modernas, um host pode atuar como **cliente**, **servidor** ou **ambos**. O software instalado no computador determina a sua função.

---

#### Servidores

Servidores são hosts com softwares instalados que lhes permitem **fornecer informações** para outros hosts na rede, como e-mail ou páginas Web. Cada serviço de servidor requer um **software de servidor separado**.

#### Clientes

Clientes são hosts que possuem softwares instalados que permitem **solicitar e exibir** as informações obtidas do servidor.

---

#### Exemplos

**Navegador Web**

- Software cliente: Chrome, Edge, Safari, Firefox
- O cliente solicita a página Web ao servidor
- O servidor Web responde com a página Web

**E-mail**

- Software cliente: Microsoft Outlook
- O cliente acessa o e-mail no servidor
- O cliente pode enviar e receber mensagens do servidor de e-mail


## 2.1.2 Funções de Clientes e Servidores
Todos os computadores conectados a uma rede que participam diretamente na comunicação de rede são classificados como hosts. Os hosts podem enviar e receber mensagens na rede. Nas redes modernas, um host pode atuar como cliente, servidor ou ambos. O software instalado no computador determina qual função o computador desempenha.
![[Pasted image 20260509220151.png]]

**Servidores** são hosts que têm um software instalado que os permite fornecer informações, como e-mail ou páginas Web, a outros hosts na rede. Cada serviço exige um software de servidor separado. Cada destino que você acessa on-line é fornecido por um servidor localizado em algum lugar de uma rede conectada à Internet global.

**Clientes** são computadores host que têm um software instalado que os permite solicitar e exibir as informações obtidas do servidor. Um exemplo de software cliente é um navegador da Web, como Internet Explorer, Safari, Mozilla Firefox ou Chrome.

|Tipo|Descrição|
|---|---|
|**E-mail**|O servidor executa o software do servidor de e-mail. Clientes usam um software de e-mail, como o Microsoft Outlook, para acessar e-mails no servidor.|
|**Web**|O servidor web executa o software do servidor web. Os clientes usam navegadores, como o Windows Internet Explorer, para acessar páginas da Web no servidor.|
|**Arquivo**|O servidor de arquivos armazena arquivos corporativos e de usuário em um local central. Os dispositivos clientes acessam esses arquivos com softwares clientes, como o Windows Explorer.|

## 2.1.3 Redes Ponto-a-Ponto

Os softwares de cliente e de servidor geralmente são executados em computadores separados, mas também é possível que um computador execute as duas funções ao mesmo tempo. Em pequenas empresas e em casas, muitos computadores funcionam como servidores e clientes na rede. Esse tipo de rede é chamado de rede ponto a ponto(P2P).

A rede ponto-a-ponto mais simples consiste em dois computadores diretamente conectados por uma conexão com ou sem fio. Ambos os computadores podem usar essa rede simples para trocar dados e serviços entre si, atuando como cliente ou servidor conforme necessário.

Vários PCs também podem ser conectados para criar uma rede ponto-a-ponto maior, mas isso exige um dispositivo de rede (como um switch) para interconectar os computadores.

A principal desvantagem de um ambiente ponto-a-ponto é que o desempenho de um host pode ser reduzido se ele estiver atuando como cliente e servidor ao mesmo tempo. A figura lista algumas das vantagens e desvantagens das redes ponto-a-ponto.

Em empresas de grande porte, devido ao potencial para quantidades altas de tráfego de rede, geralmente é necessário ter servidores dedicados para suportar o número de solicitações de serviço.

As vantagens e desvantagens das redes P2P são resumidas na figura.
![[Pasted image 20260509221000.png]]

## 2.1.4 Aplicações Ponto-a-ponto

Um aplicação P2P permite que um dispositivo atue como cliente e servidor na mesma comunicação, como mostra a figura. Nesse modelo, todo cliente é um servidor e todo servidor é um cliente. Aplicações P2P exigem que cada dispositivo final forneça uma interface de usuário e execute um serviço em segundo plano.

Algumas aplicações P2P utilizam um sistema híbrido no qual o compartilhamento de recursos é descentralizado, mas os índices que apontam para as localizações de recursos são armazenados em um diretório centralizado. Em um sistema híbrido, cada peer acessa um servidor de índice para obter a localização de um recurso armazenado em outro peer.

![[Pasted image 20260509221203.png]]

## 2.1.5. Múltiplas Funções na Rede

Um computador com software de servidor pode fornecer serviços simultaneamente a um ou vários clientes, como mostrado na figura.

Além disso, um único computador pode executar vários tipos de software de servidor. Em casa ou em uma empresa pequena, pode ser necessário que um computador atue como um servidor de arquivos, um servidor Web e um servidor de e-mail.

Um único computador pode também executar vários tipos de software cliente. Deve haver um software cliente para cada serviço necessário. Com vários softwares cliente instalados, um cliente pode se conectar a vários servidores ao mesmo tempo. Por exemplo, um usuário pode verificar e-mails e exibir uma página Web enquanto envia mensagens instantâneas e ouve rádio pela Internet.
![[Pasted image 20260509221244.png]]

## 2.1.6 Verifique sua compreensão - Clientes e Servidores

**Verifique sua compreensão sobre Clientes e Servidores escolhendo a resposta correta para as seguintes perguntas.**

#### Quiz — Clientes e Servidores

**P1** Um computador com software instalado para fornecer informações como e-mail ou páginas da Web para outros dispositivos é conhecido como:

- [x] **servidor**
- [ ] smartphone
- [ ] host inteligente
- [ ] cliente

> Servidores são hosts que têm um software instalado que os permite fornecer informações, como e-mail ou páginas Web, a outros hosts na rede.

---

**P2** Um smartphone usa um software de navegador da Web para solicitar e exibir uma página da Web. O smartphone é considerado que tipo de computador?

- [ ] host inteligente
- [ ] solicitante
- [ ] servidor
- [x] **cliente**

> Clientes são computadores host que têm um software instalado que os permite solicitar e exibir as informações obtidas do servidor.

---

**P3** Uma rede em que dois computadores estão se comunicando como cliente e como servidor é conhecida como:

- [ ] rede cliente-cliente
- [ ] rede cliente-servidor
- [ ] rede servidor-servidor
- [x] **rede ponto-a-ponto**

> Uma rede ponto-a-ponto consiste de dois computadores diretamente conectados onde ambos são capazes de trocar dados e serviços com o outro, agindo como cliente ou servidor quando necessário.

## 2.2 Componentes de rede

## 2.2.1 Vídeo - Símbolos de infraestrutura de rede

![[2.2.1.mp4#subtitle=anexos/2.2.1.vtt]]
### Dispositivos Intermediários

|Símbolo|Dispositivo|
|---|---|
|🔀|Roteador|
|📡|Roteador sem fio|
|🔲|Switch|
|📶|Ponto de acesso sem fio|

### Dispositivos Finais

|Símbolo|Dispositivo|
|---|---|
|💻|Laptop|
|🖨️|Impressora|
|📱|Smartphone|
|☎️|Telefone IP|

### Mídias de Rede

|Mídia|Descrição|
|---|---|
|**LAN**|Rede local — mais comumente uma LAN Ethernet|
|**WAN**|Rede de longa distância — usada para comunicações de provedores de serviços de Internet (ISP)|
|**Sem fio**|Mídia de transmissão wireless|
|**Nuvem**|Representa outra rede ou a Internet|

## 2.2.2 Infraestrutura de Rede

O caminho que uma mensagem percorre da sua origem ao destino pode ser tão simples quanto um único cabo conectando um computador a outro ou tão complexo quanto uma rede que literalmente atravessa o globo. A infraestrutura de rede é a plataforma que suporta a rede. Ela fornece o canal estável e confiável sobre o qual nossas comunicações podem ocorrer.

A infraestrutura de rede contém três categorias de componentes de rede, como mostrada na figura:

- Dispositivos finais
- Dispositivos intermediários
- Meios físicos de rede

![[Pasted image 20260511064405.png]]

Dispositivos e meios físicos são os elementos físicos ou o hardware da rede. O hardware é geralmente composto pelos componentes visíveis da plataforma de rede, tais como um laptop, um PC, um switch, um roteador, um access point sem fio ou os cabos usados para conectar os dispositivos. Ocasionalmente, alguns componentes podem não ser tão visíveis. No caso de meios físicos sem fio, as mensagens são transmitidas pelo ar com a utilização de freqüência de rádio invisível ou ondas infravermelhas.

Faça uma lista dos componentes de infraestrutura de rede instalados na rede residencial. Inclua os cabos ou os pontos de acessos sem fio que fornecem as conexões de rede.

## 2.2.3 Dispositivos Finais

Os dispositivos de rede com os quais as pessoas são mais familiarizadas são chamados de dispositivos finais. Estes dispositivos formam a interface entre usuários e a rede de comunicação subjacente

Alguns exemplos de dispositivos finais são:

- Computadores (estações de trabalho, laptops, servidores de arquivo, servidores Web);
- Impressoras de rede;
- Telefones e equipamento de teleconferência
- Câmeras de segurança;
- Dispositivos móveis (como smartphones, tablets, PDAs, leitores de cartão de débito/crédito sem fio e scanners de código de barras)

Um dispositivo final (ou host) é a origem ou o destino de uma mensagem transmitida pela rede, como mostrado na animação. Para identificar hosts de forma exclusiva, endereços são usados. Quando um host inicia a comunicação, ele usa o endereço do host de destino para especificar onde a mensagem deve ser enviada.

Clique em Play na figura para ver uma animação dos dados fluindo por uma rede.

## 2.2.4 Verifique sua compreensão - Componentes de rede

### Quiz — Dispositivos e Mídias de Rede

**P1** Marjani mora em uma fazenda a vários quilômetros de Msolwa, na Tanzânia. Qual dos dispositivos finais a seguir é mais provável que ela use para se conectar à Internet? _(Escolha duas.)_

- [x] **smartphone**
- [ ] roteador sem fio
- [ ] Terminal de telepresença
- [x] **tablet sem fio**
- [ ] impressora da rede

> Em áreas rurais sem infraestrutura de telecomunicações com fio, o acesso sem fio através de um serviço de celular é muitas vezes a única opção para acesso à Internet.

---

**P2** Eilert conseguiu recentemente um emprego em uma empresa de serviços de suporte a computadores em Falun, na Suécia. Um cliente solicitou que alguém conectasse a rede doméstica à Internet. Ele têm apenas um modem a cabo. Qual dos seguintes dispositivos intermediários Eilert provavelmente levaria para o trabalho?

- [ ] dispositivo de firewall
- [x] **roteador sem fio**
- [ ] switch LAN
- [ ] Switch multicamada
- [ ] Computador desktop

> As redes domésticas normalmente se conectam ao provedor de Internet usando um modem e um roteador com recursos sem fio. Nesse cenário, Eilert precisará levar o roteador sem fio, pois o cliente só tem o modem.

---

**P3** Rosalia trabalha como agente de saúde comunitária em Rio Claro, Brasil, fazendo visitas domiciliares para fornecer atendimento primário. Ela precisa de acesso à Internet para manter registros de pacientes e oferecer videoconferência com um médico. Que tipo de dispositivo final e mídia ela provavelmente usa? _(Escolha duas.)_

- [x] **Mídia Sem Fio**
- [x] **tablet**
- [ ] Mídia LAN
- [ ] roteador
- [ ] Computador desktop
- [ ] Mídia WAN

> Agentes de saúde comunitários que viajam de casa em casa dependem muito do acesso sem fio. Rosalía provavelmente usaria um tablet com mídia sem fio para atualizar registros médicos e fazer videoconferência quando necessário.


# 2.3 Opções de conectividade com o ISP

## 2.3.1 Serviços ISP

Um provedor de serviços de Internet (ISP) fornece o link entre a rede doméstica e a Internet. Um ISP pode ser o provedor de TV a cabo local, um provedor de serviços de telefonia fixa, a rede celular que fornece seu serviço de smartphone ou um provedor independente que aluga largura de banda na infraestrutura de rede física de outra empresa.  
  
Muitos ISPs também oferecem serviços adicionais aos assinantes, como mostrado na figura. Esses serviços podem englobar contas de e-mail, armazenamento de rede, hospedagem de sites e serviços de segurança ou backup automático.  
  
Os ISPs são essenciais para a comunicação na Internet global. Cada ISP conecta-se a outros ISPs para formar uma rede de links que interconectam usuários em todo o mundo. Os ISPs são conectados de maneira hierárquica que garante que o tráfego da Internet geralmente siga o caminho mais curto da origem ao destino.  
  
O backbone de Internet é como uma autoestrada de informações que fornece links de dados de alta velocidade para conectar as diversas redes de provedores de serviços nas grandes áreas metropolitanas do mundo todo. O principal meio físico que conecta o backbone de Internet é o cabo de fibra óptica. Esse cabo normalmente é instalado no subterrâneo para conectar cidades dentro de continentes. Os cabos de fibra óptica também passam sob o mar para conectar continentes, países e cidades.

![[Pasted image 20260511065633.png]]

## 2.3.2 Conexões ISP

A interconexão de ISPs, que forma a espinha dorsal da internet, é uma teia complexa de cabos de fibra ótica com switches e roteadores de rede caros que direcionam o fluxo de informações entre os hosts de origem e destino. Os usuários domésticos médios não estão cientes da infraestrutura fora de sua rede. Para ele, conectar-se ao ISP é um processo bastante simples.  
  
A parte superior da figura mostra a opção mais simples de conexão com o ISP. Consiste em um modem que fornece uma conexão direta entre um computador e o ISP. Esta opção não deve ser usada, pois seu computador não está protegido na internet.  
  
Como mostrado na parte inferior da figura, é necessário um roteador para conectar com segurança um computador a um ISP. Esta é a opção de conexão mais comum. Consiste em usar um roteador integrado sem fio para se conectar ao ISP. O roteador inclui um switch para conectar hosts com fio e um AP sem fio para conectar hosts sem fio. O roteador também fornece informações de endereçamento IP do cliente e segurança para hosts internos.

![[Pasted image 20260511065854.png]]

## 2.3.3 Conexões de Cabo DSL

A maioria dos usuários de rede doméstica não se conecta aos provedores de serviços com cabos de fibra óptica. A figura ilustra as opções comuns de conexão para usuários de residências e pequenos escritórios. Os dois métodos mais comuns são os seguintes:

- **Cabo -** Normalmente oferecido por provedores de serviços de televisão a cabo, o sinal de dados de internet é transportado no mesmo cabo coaxial que entrega a televisão a cabo. Ele fornece uma conexão com a internet sempre ativa com alta largura de banda. Um cable modem especial separa o sinal de dados da Internet dos outros sinais transmitidos pelo cabo e fornece uma conexão Ethernet para um computador host ou LAN.
- **DSL - Linha digital do Assinante** fornece uma conexão com a internet sempre ativa e com alta largura de banda. Ele requer um modem especial de alta velocidade que separa o sinal DSL do sinal de telefone e fornece uma conexão Ethernet para um computador host ou LAN. A DSL passa por uma linha telefônica, com a linha dividida em três canais. Um canal é usado para chamadas telefônicas. Esse canal permite que um indivíduo receba chamadas telefônicas sem se desconectar da Internet. Um segundo canal é um canal de download mais rápido, usado para receber informações da Internet. O terceiro canal é usado para enviar ou carregar informações. Esse canal geralmente é um pouco mais lento do que o canal de download. A qualidade e a velocidade da conexão DSL depende principalmente da qualidade da linha telefônica e da distância da central telefônica da operadora de telefonia. Quanto mais longe você estiver da central telefônica, mais lenta será a conexão.

![[Pasted image 20260511070231.png]]

## 2.3.4 Opções Adicionais para Conectividade

Outras opções de conexão ISP para usuários domésticos incluem o seguinte:

**Celular**:
O acesso do celular à Internet usa uma rede de telefonia celular para se conectar. Onde quer que você possa obter um sinal de celular, você pode obter acesso à Internet por celular. O desempenho será limitado pelos recursos do telefone e da torre do celular à qual ele está conectado. A disponibilidade do acesso à Internet via celular é um benefício real para pessoas que vivem em áreas que, de outra forma, não teriam nenhuma conectividade à Internet ou para aquelas que estão sempre em movimento. O problema da conectividade por celular é que a operadora geralmente mede o uso da largura de banda da conexão e pode cobrar taxas extras caso ele exceda o plano de dados do contrato.

**Satélite**:
Serviço de satélite é uma boa opção para casas ou escritórios que não tenham acesso a DSL ou cabo. As antenas parabólicas (veja a figura) exigem uma linha de visão clara para o satélite e isso pode ser difícil de conseguir em áreas muito arborizadas ou em locais com outras obstruções aéreas. As velocidades variam de acordo com o contrato, embora geralmente sejam boas. Os custos de equipamento e instalação podem ser altos (consulte o provedor para ofertas especiais), com uma taxa mensal moderada a partir de então. Assim como o acesso por celular, a disponibilidade de acesso à Internet via satélite é um benefício real em áreas que, de outra forma, não teriam nenhuma conectividade com a Internet.

**Conexão discada (dial-up)**:
Uma opção de baixo custo que usa qualquer linha telefônica e um modem. Para se conectar ao ISP, um usuário chama o número de telefone de acesso do ISP. A pequena largura de banda fornecida por uma conexão discada via modem geralmente não é suficiente para grandes transferências de dados, mas pode ser útil quando se esta deslocando em viagens. Uma conexão discada por modem só deve ser considerada quando as opções de conexão de velocidade mais alta não estiverem disponíveis.


#### Satellite Connection

Em áreas metropolitanas, muitos apartamentos e pequenos escritórios estão conectados diretamente com cabos de fibra óptica. Isso permite que um provedor de serviços de Internet forneça velocidades de largura de banda mais altas e suporte a mais serviços, como Internet, telefone e TV.

A escolha da conexão varia dependendo da localização geográfica e da disponibilidade do provedor de serviço.

#### Conexão via Satélite
![[Pasted image 20260513060537.png]]



## 2.3.5 Verifique a sua compreensão - Opções de conectividade com o ISP

**P1** O que é um serviço que fornece um sinal de dados da Internet na mesma rede que oferece serviços de transmissão de televisão e telefone?

- [x] **Internet a cabo**
- [ ] Digital Subscriber Line (DSL)
- [ ] Acesso para convidados
- [ ] Plano de dados de celular

> O cabo de Internet fornece um sinal de dados de Internet na mesma rede que oferece serviços de televisão e telefone de transmissão.

---

**P2** O que é um serviço que fornece conexão de banda larga sempre ativa, usando fios de telefonia fixa existentes?

- [x] **Digital Subscriber Line (DSL)**
- [ ] Plano de dados de celular
- [ ] Internet a cabo
- [ ] Acesso para convidados

> Uma conexão DSL é um serviço que fornece banda larga sempre ativa, usando fios de telefonia fixa existentes.

---

**P3** O que é um serviço de Internet que usa redes de telefonia móvel para transmitir dados?

- [x] **Plano de dados de celular**
- [ ] Internet a cabo
- [ ] Digital Subscriber Line (DSL)
- [ ] Acesso para convidados

> Um plano de dados de celular é um serviço de Internet que usa redes de telefonia móvel para transmitir dados.



# 2.4 Resumo de componentes de rede, tipos de conexões

## 2.4.1 O que aprendi neste módulo?

### Clientes e Servidores

Todos os computadores conectados a uma rede que participam diretamente na comunicação de rede são classificados como hosts. Os hosts podem enviar e receber mensagens na rede. Nas redes modernas, um host pode atuar como cliente, servidor ou ambos. O software instalado no computador determina qual função o computador desempenha.

Os softwares de cliente e de servidor geralmente são executados em computadores separados, mas também é possível que um computador execute as duas funções ao mesmo tempo. Em pequenas empresas e em casas, muitos computadores funcionam como servidores e clientes na rede. Esse tipo de rede é chamado de rede ponto a ponto (P2P). Em empresas de grande porte, devido ao potencial para quantidades altas de tráfego de rede, geralmente é necessário ter servidores dedicados para suportar o número de solicitações de serviço. As redes P2P são fáceis de configurar, menos complexas, de custo mais baixo e podem ser usadas para tarefas simples, como transferência de arquivos e compartilhamento de impressoras. No entanto, não existe uma administração centralizada. Elas têm menos segurança, não são escaláveis e podem ter um desempenho mais lento.

---

### Componentes de Rede

Existem símbolos que representam vários tipos de equipamentos de rede. A infraestrutura de rede é a plataforma que suporta a rede. Ela fornece o canal estável e confiável sobre o qual nossas comunicações podem ocorrer. A infraestrutura de rede contém três categorias de componentes de hardware: dispositivos intermediários, dispositivos final e meios físicos de rede. O hardware é geralmente composto pelos componentes visíveis da plataforma de rede, tais como um laptop, um PC, um switch, um roteador, um access point sem fio ou os cabos usados para conectar os dispositivos. Os componentes que não estão visíveis incluem mídia sem fio.

Os dispositivos finais, ou hosts, formam a interface entre os usuários e a rede de comunicação subjacente. Alguns exemplos de dispositivos finais são:

- Computadores (estações de trabalho, laptops, servidores de arquivo, servidores Web);
- Impressoras de rede
- Telefones e equipamento de teleconferência
- Câmeras de segurança
- Dispositivos móveis (como smartphones, tablets, PDAs, leitores de cartão de débito/crédito sem fio e scanners de código de barras)

---

### Opções de conectividade com o ISP

Um ISP fornece um link entre a rede doméstica e a Internet. Um ISP pode ser o provedor de TV a cabo local, um provedor de serviços de telefonia fixa, a rede celular que fornece seu serviço de smartphone ou um provedor independente que aluga largura de banda na infraestrutura de rede física de outra empresa. Cada ISP conecta-se a outros ISPs para formar uma rede de links que interconectam usuários em todo o mundo. Os ISPs são conectados de maneira hierárquica que garante que o tráfego da Internet geralmente siga o caminho mais curto da origem ao destino.

A interconexão de ISPs, que forma a espinha dorsal da internet, é uma teia complexa de cabos de fibra ótica com switches e roteadores de rede caros que direcionam o fluxo de informações entre os hosts de origem e destino.

Para ele, conectar-se ao ISP é um processo bastante simples. Esta é a opção de conexão mais comum. Consiste em usar um roteador integrado sem fio para se conectar ao ISP. O roteador inclui um switch para conectar hosts com fio e um AP sem fio para conectar hosts sem fio. O roteador também fornece informações de endereçamento IP do cliente e segurança para hosts internos. Os dois métodos mais comuns são cabo e DSL. Outras opções incluem celular, satélite e conexão discada usando uma linha telefônica.

## 2.4.2 Webster - Questões para Reflexão

Você já pediu algum móvel que precisava montar? A caixa tem todas as peças e partes necessárias, juntamente com as instruções de montagem. Ele ajuda você a analisar todos esses itens enquanto lê as instruções. Pense na sua rede. Você sabia quais eram os diferentes dispositivos e tipos de conexão antes de usar este módulo? Você observa essas peças e partes de forma diferente agora?


## 2.4.3 Quiz sobre Componentes de Rede, Tipos e Perguntas

**P1 –** Que tipo de rede é definida por dois computadores que podem enviar e receber solicitações para recursos?

- **ponto-a-ponto** ✓

---

**P2 –** Quais são as duas funções dos dispositivos finais na rede? (Escolha duas.)

- **Eles são a interface entre as pessoas e a rede de comunicação.** ✓
- **Eles originam os dados que fluem na rede.** ✓

---

**P3 –** Um usuário doméstico busca conexão de ISP com transmissão digital de alta velocidade via linhas telefônicas. Que tipo de conexão deve ser usada?

- **DSL** ✓

---

**P4 –** Que tipo de conexão seria melhor para uma residência em área remota sem cobertura celular ou cabeada?

- **satélite** ✓

---

**P5 –** Qual termo descreve corretamente a função de um ISP?

- **Responsável por fornecer o link entre uma rede privada e a Internet.** ✓

---

**P6 –** Qual dispositivo é um dispositivo intermediário?

- **firewall** ✓

---

**P7 –** Qual cenário descreve uma rede ponto-a-ponto?

- **Um usuário compartilhou uma impressora conectada à estação de trabalho.** ✓

---

**P8 –** Que termo descreve um dispositivo de rede cuja função principal é fornecer informações a outros dispositivos?

- **servidor** ✓

---

**P9 –** Qual é uma vantagem do modelo de rede ponto-a-ponto?

- **facilidade de configuração** ✓

---

**P10 –** Qual é uma característica de um aplicativo ponto a ponto?

- **Cada dispositivo que usa o aplicativo provê uma interface de usuário e executa um serviço em segundo plano.** ✓

