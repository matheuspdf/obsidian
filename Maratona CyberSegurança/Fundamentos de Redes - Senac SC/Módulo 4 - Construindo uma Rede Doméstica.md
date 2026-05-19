# 4.0 Introdução
## 4.0.1 Webster - Por que devo fazer este módulo?

Kishori e Shridhar estão lavando a louça depois do jantar. Kishori está assistindo a um filme favorito em seu tablet enquanto guarda a louça. Ela pergunta a Shridhar se o tablet funciona exatamente como o celular. Ele explica que existem alguns tablets que usam uma rede móvel, mas que o tablet funciona na rede Wi-Fi da casa dela. Ela diz a ele que sabe que deve entrar pela caixa no canto da sala de estar. Isso é tudo que ela sabe!

Shridhar explica que a caixa no canto é um roteador doméstico. O roteador está conectado à Internet. Roteadores domésticos normalmente têm dois tipos principais de portas: portas Ethernet e uma porta de Internet. Além das portas com fio, muitos roteadores residenciais incluem antena sem fio e um ponto de acesso interno sem fio. A Kishori usa principalmente a rede sem fio em casa. Agora, Shridhar está preocupado com a segurança sem fio de sua mãe. Como ela não sabia o que era o roteador, ela provavelmente não alterou sua senha padrão no roteador! O Shridhar faz login no roteador e faz algumas alterações para manter a rede e os dispositivos da Kishori mais seguros.

Você já configurou um roteador? Você já pensou em ter comunicações seguras em dispositivos sem fio? Este módulo oferece a você o conhecimento necessário para construir uma rede doméstica e configurar dispositivos sem fio para uma comunicação segura.


## 4.0.2 O que irei aprender neste módulo?

### Construindo uma Rede Doméstica

**Objetivo do módulo:** Configurar um roteador sem fio integrado e cliente sem fio para estabelecer uma conexão segura com a Internet.

| Tópico                                  | Objetivo                                                            |
| --------------------------------------- | ------------------------------------------------------------------- |
| **Conceitos básicos da rede doméstica** | Descrever os componentes necessários para criar uma rede doméstica. |
| **Tecnologias de rede na residência**   | Descrever as tecnologias de rede com e sem fio.                     |
| **Padrões de Redes Sem Fio**            | Descrever o Wi-Fi.                                                  |
| **Configurar um roteador doméstico**    | Configurar dispositivos sem fio para comunicações seguras.          |

# 4.1 Conceitos básicos da rede doméstica
## 4.1.1 Vídeo - Configuração típica de rede doméstica

### Equipamentos de uma Rede Doméstica

**Modem** – Converte os sinais do provedor (cabo ou DSL) para o formato da rede doméstica. – Possui entrada coaxial (do provedor) e saída para a rede local. – Alguns roteadores já vêm com modem embutido.

**Roteador sem fio (Wireless Router)** – Dispositivo central da rede doméstica. – Possui porta de Internet (WAN) e portas LAN para dispositivos com fio. – Inclui access point wireless integrado. – Separa a rede do provedor (pública) da rede doméstica (local).

**Redes separadas** – A rede doméstica é composta de pelo menos duas redes distintas:

- Rede pública — vinda do provedor (cabo ou DSL).
- Rede local (LAN) — dispositivos da casa.

**Conectividade** – Dispositivos com fio e sem fio normalmente pertencem à mesma rede local. – Ambos recebem endereços IP na mesma faixa de rede. – Portas LAN do roteador funcionam como portas de switch.


## 4.1.2 Componentes de uma Rede Doméstica

Além de um roteador integrado, há muitos tipos diferentes de dispositivos que podem se conectar a uma rede doméstica, como mostrado na figura. Veja alguns exemplos:

- Computador desktop
- Sistemas de jogos
- Sistemas de smart TV
- Impressoras
- Scanners
- Câmeras de segurança
- Telefones
- Dispositivos de controle climático

Com a chegada das novas tecnologias no mercado, cada vez mais funções domiciliares dependerão da rede para fornecer conectividade e controle.

**Rede local residencial sem fio (WLAN)**


### Home Wireless Local Area Network (WLAN)

![[Pasted image 20260519070747.png]]


## 4.1.3 Roteadores típicos de rede doméstica

Os roteadores de residências e pequenas empresas normalmente têm dois tipos de porta principais:

### Portas Ethernet

Estas portas se conectam à parte interna do switch no roteador. Essas portas são geralmente rotuladas como “Ethernet” ou “LAN”, como mostrado na figura. Todos os dispositivos conectados às portas do switch estão na mesma rede local.

### Porta da Internet

Essa porta é usada para conectar o dispositivo a outra rede. A porta Internet conecta o roteador a uma rede diferente das portas Ethernet. Esta porta costuma ser usada para conectar o modem DSL ou a cabo para acessar a Internet.

![[Pasted image 20260519070906.png]]


## 4.1.4 Verifique sua compreensão - Noções básicas de rede doméstica

**Verifique sua compreensão sobre noções básicas de rede doméstica escolhendo a resposta correta para as seguintes perguntas.**


**P1 –** Verdadeiro ou falso: Um roteador doméstico normalmente só oferece acesso com fio à rede. Você precisa comprar um dispositivo separado para acesso sem fio.

- verdadeiro
- **falso** ✓

> **Feedback:** Normalmente, uma rede doméstica usa um roteador integrado equipado com recursos com e sem fio.

---

**P2 –** Qual das opções a seguir é usada para conectar um dispositivo com fio ao switch interno do roteador doméstico?

- porta Internet
- Porta sem fio
- **Porta Ethernet** ✓
- PORTA DE ADAPTADOR DE ENERGIA

> **Feedback:** As portas Ethernet se conectam à parte interna do switch do roteador. Essas portas são geralmente rotuladas como "Ethernet" ou "LAN".



# 4.2 Tecnologia de rede na residência
## 4.2.1 Frequência de LAN sem fio

As tecnologias sem fio mais usadas em redes residenciais estão nas faixas de frequências não licenciadas de 2,4 GHz e 5 GHz.

Bluetooth é uma tecnologia que utiliza a banda de 2,4 GHz. Embora restrita a comunicações de curto alcance e baixa velocidade, ela tem a vantagem de estabelecer comunicação com vários dispositivos ao mesmo tempo. Essa comunicação um para muitos tornou a tecnologia Bluetooth o método preferido para conectar periféricos de computador, como mouses, teclados e impressoras sem fio. O Bluetooth é útil como método de transmissão de áudio para alto-falantes ou fones de ouvido.

Outras tecnologias que usam as bandas 2,4 GHz e 5 GHz são as modernas tecnologias de LAN sem fio que estão em conformidade com vários padrões IEEE 802.11. A diferença em relação à tecnologia de Bluetooth é que elas transmitem em um nível de potência muito maior, o que lhes dá maior alcance e melhor rendimento. Determinadas áreas do espectro eletromagnético podem ser usadas sem permissão.

A figura mostra onde existem tecnologias sem fio no espectro eletromagnético.

![[Pasted image 20260519074528.png]]


## 4.2.2 Tecnologias de Redes com fio

Embora muitos dispositivos de rede doméstica comportem comunicações sem fio, ainda há algumas aplicações em que os dispositivos utilizam uma conexão por switch com fio que não é compartilhada com outros usuários na rede.

O protocolo com fio implementado com mais frequência é o protocolo Ethernet. A Ethernet usa um conjunto de protocolos que permite que os dispositivos de rede se comuniquem através de uma conexão LAN com fio. Uma LAN Ethernet pode conectar dispositivos usando muitos tipos diferentes de mídia de fiação.

Dispositivos conectados diretamente usam um cabo de ligação Ethernet, normalmente par trançado não blindado. Esses cabos podem ser comprados com os conectores RJ-45 já instalados e vêm em vários comprimentos. Casas construídas recentemente podem já ter tomadas Ethernet cabeadas nas paredes. Para residências que não têm cabeamento UTP, há outras tecnologias, como o uso da rede elétrica, que podem distribuir conectividade com fio nos ambientes.

**Clique em cada tipo de rede sem fio para obter mais informações.**

### Cabo categoria 5e

A categoria 5e é o cabeamento mais comum usado em uma LAN. O cabo é composto de 4 pares de fios que são trançados para reduzir a interferência elétrica.

### Cabo Coaxial

O cabo coaxial possui um fio interno circundado por uma camada isolante tubular, que é então circundada por uma blindagem condutora tubular. A maioria dos cabos coaxiais também possui uma capa ou um revestimento de isolamento externo.

### Cabo de Fibra-óptica

O cabo de fibra óptica pode ser de vidro ou plástico com diâmetro aproximadamente igual ao de um cabelo humano e pode transportar informações digitais em velocidades muito altas por longas distâncias. Cabo de fibra óptica têm uma largura de banda muito alta, o que permite transportar grandes quantidades de dados.


## 4.2.3 Verifique sua compreensão - Tecnologias de rede doméstica

**Verifique a sua compreensão de tecnologias de rede doméstica escolhendo a resposta correta para as seguintes perguntas.**

**P1 –** Verdadeiro ou falso: Determinadas áreas do espectro eletromagnético podem ser usadas sem permissão.

- **verdadeiro** ✓
- falso

> **Feedback:** Determinadas áreas do espectro foram reservadas para uso público sem necessidade de autorizações especiais.

---

**P2 –** Verdadeiro ou falso: Wi-Fi, Bluetooth e telefones sem fio usam os mesmos intervalos de frequência.

- **falso** ✓
- verdadeiro

> **Feedback:** Wi-Fi usa 2,4 GHz e 5 GHz. Bluetooth usa 2,4 GHz. Telefones sem fio operam em ~900 MHz.

---

**P3 –** Qual tecnologia de rede com fio tem um fio interno envolto por uma camada isolante tubular, que é então envolta por uma blindagem condutiva tubular?

- **Cabo coaxial** ✓
- Cabo de fibra ótica
- Cabo categoria 5 (Cat5)

> **Feedback:** O cabo coaxial possui um fio interno circundado por uma camada isolante tubular, que é então circundada por uma blindagem condutora tubular.



# 4.3 Padrões de Redes Sem Fio
## 4.3.1 Redes Wi-Fi

Foram desenvolvidos vários padrões para garantir a comunicação entre dispositivos sem fio. Eles especificam o espectro de RF usado, as taxas de dados, o modo como as informações são transmitidas, etc. O principal organismo responsável pela criação de padrões técnicos sem fio é o IEEE (Instituto dos Engenheiros Eletricistas e eletrônicos)

O padrão IEEE 802.11 controla o ambiente WLAN. Algumas alterações no padrão IEEE 802.11 descrevem as características dos diferentes padrões de comunicação sem fio. Os padrões sem fio de LANs usam as bandas de frequência de 2,4 GHz e 5 GHz. Coletivamente, essas tecnologias são conhecidas como Wi-Fi.

Outro organismo, conhecido como Wi-Fi Alliance, é responsável por testar dispositivos de LAN sem fio de diferentes fabricantes. O logotipo de Wi-Fi em um dispositivo significa que esse equipamento atende aos padrões e deve operar com outros dispositivos que usam o mesmo padrão.

Os padrões sem fio estão melhorando continuamente a conectividade e a velocidade das redes Wi-Fi. É importante saber quando novos padrões serão introduzidos porque os fabricantes de dispositivos sem fio implementarão esses novos padrões rapidamente em novos produtos.

Você tem uma rede sem fio na sua casa? Você sabe quais padrões são compatíveis com o seu roteador sem fio?

## 4.3.2 Configurações de rede sem fio

A interface de Configurações sem fio básicas do Packet Tracer é mostrada na figura. Os roteadores sem fio que usam os padrões 802.11 têm várias configurações que devem ser ajustadas. Estas configurações incluem:

### Modo de rede

Determina o tipo de tecnologia que deve ser suportada. Por exemplo,**802.11b**, **802.11g**,**802.11n** ou **Mixed Mode (Modo misto).**

### Nome da rede (SSID)

Usada para identificar a WLAN. Todos os dispositivos que desejam participar na WLAN devem ter o mesmo SSID.

### Canal padrão

Especifica o canal no qual a comunicação ocorrerá. Por padrão, é configurado para **Automático** para permitir que o ponto de acesso (AP) determine o melhor canal a usar.

### Broadcast de SSID

Determina se o SSID será transmitido para todos os dispositivos dentro do intervalo. Por padrão, é configurado para **Ativado**.

**Observação:** SSID significa Identificador do Conjunto de Serviços

![[Pasted image 20260519075740.png]]

**Modo de rede**

O protocolo 802.11 pode fornecer melhor taxa de transferência, dependendo do ambiente de rede sem fio. Se todos os dispositivos sem fio se conectarem com o mesmo padrão 802.11, poderão ser obtidas as velocidades máximas desse padrão. Se o ponto de acesso estiver configurado para aceitar apenas um padrão 802.11, os dispositivos que não usarem esse padrão não poderão se conectar ao access point.

Um ambiente de rede sem fio com modo misto pode incluir dispositivos que utilizem qualquer padrão Wi-Fi atual. Esse ambiente oferece acesso fácil para dispositivos antigos que precisam de uma conexão sem fio, mas não são compatíveis com os padrões mais recentes.

Ao criar uma rede sem fio, é importante que os componentes sem fio se conectem à WLAN apropriada. Isso é feito por meio do SSID.

O SSID é uma string alfanumérica que diferencia maiúsculas e minúsculas até 32 caracteres. Ele é enviado no cabeçalho de todos os quadros transmitidos pela WLAN. O SSID serve para informar a dispositivos sem fio, chamados estações sem fio (STA), qual WLAN eles pertencem e com quais outros dispositivos eles podem se comunicar.

Usamos o SSID para identificar uma rede sem fio específica. É basicamente o nome da rede. Roteadores sem fio usualmente transmitem seu SSIDs configurados por default. O broadcast SSID permite que outros dispositivos e clientes sem fio detectem automaticamente o nome da rede sem fio. Se o broadcast SSID estiver desativado, insira manualmente o SSID nos dispositivos sem fio.

A desativação do broadcast SSID pode dificultar a detecção da rede sem fio para clientes legítimos. Entretanto, simplesmente desativar o broadcast SSID não é suficiente para evitar que clientes não autorizados se conectem à rede sem fio. Todas as redes sem fio devem usar a criptografia mais forte disponível para restringir o acesso não autorizado.

## 4.3.3 Verifique sua compreensão - Padrões de redes sem fio

**Verifique sua compreensão sobre padrões de rede sem fio escolhendo a resposta corretas para as seguintes perguntas**

# Questões de Revisão

**P1 –** Qual organização é responsável por testar os dispositivos de LAN sem fio?

- IETF
- TIA/EIA
- **Wi-Fi Alliance** ✓
- IEEE

> **Feedback:** A Wi-Fi Alliance é responsável por testar dispositivos de LAN sem fio de diferentes fabricantes.

---

**P2 –** O que é usado para identificar uma rede sem fio?

- o endereço IP do roteador
- O endereço de rede
- o modo de rede
- **SSID – Service Set Identifier** ✓

> **Feedback:** O SSID é o nome da rede sem fio.

---

**P3 –** Verdadeiro ou falso: Se houver dispositivos na rede sem fio que usem diferentes padrões 802.11, você deve definir a rede para o padrão mais alto para obter a melhor taxa de transferência.

- verdadeiro
- **falso** ✓

> **Feedback:** A rede deve ser configurada no modo misto para incluir dispositivos que usem qualquer um dos padrões Wi-Fi atuais.