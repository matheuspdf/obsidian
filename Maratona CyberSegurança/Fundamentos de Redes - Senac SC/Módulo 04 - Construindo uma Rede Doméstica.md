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

![[4.1.1.mp4#subtitle=anexos/4.1.1.vtt]]
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

### Questões de Revisão

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


# 4.4 Configurar um roteador doméstico
## 4.4.1 Primeira configuração

Muitos roteadores sem fio para residências têm um utilitário de configuração automática que pode ser usado para ajustar as configurações básicas no roteador. Esses utilitários geralmente exigem que um computador ou um notebook seja conectado a uma porta com fio no roteador. Se não houver nenhum dispositivo disponível que tenha uma conexão com fio, talvez seja necessário configurar primeiro o software de cliente sem fio no notebook ou no tablet.

Para se conectar ao roteador usando uma conexão com fio, conecte um cabo de ligação Ethernet à porta de rede no computador Conecte a outra extremidade a uma porta LAN no roteador. Não conecte o cabo à porta ou à interface denominada "Internet". A porta Internet será conectada ao modem DSL ou a cabo. Alguns roteadores residenciais podem ter um modem incorporado para conexões com a Internet. Nesse caso, verifique se o tipo de conexão está correto para o serviço de Internet. Uma conexão de cable modem terá um terminal coaxial para aceitar um conector do tipo BNC. Uma conexão DSL terá uma porta para um cabo de telefone, geralmente um conector RJ-11.

Após a confirmação de que o computador está conectado ao roteador de rede e que as luzes dos links na NIC (placa de interface de rede) indicam uma conexão ativa, o computador precisa de um endereço IP. A maioria dos roteadores de rede estão configurados para que o computador receba um endereço IP automaticamente de um servidor DHCP local. Se o computador não tiver um endereço IP, verifique a documentação do roteador e configure o PC ou tablet com um endereço IP, máscara de sub-rede, gateway padrão e informações de DNS exclusivas.

## 4.4.2 Considerações de Design

Antes de entrar no utilitário de configuração ou configurar manualmente o roteador através de um navegador da Web, você deve considerar como a rede será usada. Você não deseja configurar o roteador e ter essa configuração limitando o que pode fazer na rede, mas também não quer deixar sua rede desprotegida.

### Que nome devo dar à minha rede?

Se a transmissão SSID estiver ativa, o nome SSID será visto por todos os clientes sem fio no intervalo de sinal. Muitas vezes, o SSID revela informações demais sobre a rede para dispositivos clientes desconhecidos. Não é recomendável incluir o modelo de dispositivo ou a marca como parte do SSID. Os dispositivos sem fio têm configurações padrão que podem ser facilmente encontradas na Internet, bem como pontos fracos na segurança conhecidos.


### Que tipos de dispositivos se conectarão à minha rede?

Os dispositivos sem fio têm transmissor de rádio/receptores que funcionam dentro de uma determinada faixa de frequências. Se um dispositivo tiver apenas o rádio necessário para 802.11 b/g, ele não se conectará caso o roteador sem fio ou o ponto de acesso esteja configurado para aceitar somente os padrões 802.11n ou 802.11ac. Se todos os dispositivos forem compatíveis com o mesmo padrão, a rede funcionará na velocidade máxima. Se você tiver dispositivos incompatíveis com os padrões n ou ac, você terá que habilitar o mode enable legacy Um ambiente de rede sem fio do modo legado varia entre os modelos de roteador, mas pode incluir uma combinação de 802.11a, 802.11b, 802.11g, 802.11n e 802.11ac. Esse ambiente fornece acesso fácil para dispositivos antigos que precisam de uma conexão sem fio.


### Como adiciono novos dispositivos?

O modo de uso da rede determina quem pode acessar a rede doméstica. Em alguns roteadores sem fio, é possível configurar o acesso para convidado. Essa é uma área de cobertura do SSID que permite o acesso aberto, restringindo-o apenas ao uso da Internet.

A figura mostra uma tela de configuração sem fio.

**Observação:** alguns roteadores sem fio podem rotular o modo legado como modo misto.


## 4.4.3 Vídeo - Configuração de Roteador e Cliente sem fio
![[4.4.3.mp4#subtitle=anexos/4.3.3.vtt]]
### 1. Conectar os dispositivos

**Cabos coaxiais:** – Divisor de cabo → Cable Modem (Port 0) – Divisor de cabo → TV (porta coaxial 2)

**Cabos straight-through de cobre:** – Cable Modem → porta Internet do Wireless Router – Office PC (FastEthernet 0) → porta GigabitEthernet 1 do Wireless Router – Bedroom PC → Wireless Router (configurar sozinho)

---

### 2. Configurar endereçamento IP

– No Office PC: Desktop > IP Configuration > selecionar **DHCP** – Anotar o **gateway padrão: 192.168.0.1** (IP do roteador) – Se não receber IP imediatamente, clicar em **Fast Forward Time**

---

### 3. Acessar a interface do roteador

– Abrir Web Browser no Office PC – Acessar **192.168.0.1** – Login padrão: usuário `admin` / senha `admin`

---

### 4. Configurações do roteador

**Setup:** – Limitar número de usuários DHCP para **10** – Clicar em **Save Settings**

**Administration:** – Alterar senha para `MyPassword1!` – Salvar e fazer login com a nova senha

---

### 5. Configurar rede sem fio

**Wireless > Basic:** – Ativar rádio de **2,4 GHz** – Nome da rede (SSID): `MyHome` – Salvar configurações

**Wireless > Security:** – Modo de segurança: **WPA2 Personal** – Senha: `MyPassphrase1!` – Salvar configurações

---

### 6. Conectar o Laptop ao Wi-Fi

– Laptop > Desktop > PC Wireless > aba Connect – Selecionar a rede `MyHome` e clicar em **Connect** – Inserir chave: `MyPassphrase1!` – Verificar IP iniciando com `192.168.x.x`

---

### 7. Testar conectividade

– Abrir Web Browser em qualquer dispositivo – Acessar `skillsforall.srv` – Mensagem esperada: **"Welcome to Skills for All"** – Verificar conclusão em **Check Results** (meta: 100%)


## 4.4.4 Packet Tracer - Configurar um Roteador sem fio e um cliente

Nesta atividade do Packet Tracer, você completará os seguintes objetivos.

- Parte 1: Conectar os Dispositivos
- Parte 2: Configurar o roteador sem fio
- Parte 3: Configurar o endereçamento IP e testar a conectividade

Packet Tracer - Configurar um roteador sem fio e clientes

> [!example]- 🖧 Recursos do Lab
> - 📄 [[anexos/4.4.4.html|Instruções]]
> - 📥 [[anexos/4.4.4.pka|Abrir no Packet Tracer]]


# 4.5 Resumo Construindo uma rede doméstica

## 4.5.1 O que aprendi neste módulo?

### Conceitos básicos da rede doméstica

A maioria das redes domésticas consiste em pelo menos duas redes separadas. A rede pública vem do provedor de serviços. O roteador está conectado à Internet. Provavelmente, o roteador doméstico tem recursos com e sem fio. Uma rede doméstica é uma pequena LAN com dispositivos que normalmente se conectam uns aos outros e a um roteador integrado para trocar informações.

A tecnologia sem fio é razoavelmente econômica e fácil de instalar. Vantagens da tecnologia de LAN sem fio incluem mobilidade, escalabilidade, flexibilidade, economia de custos, tempo de instalação reduzido e confiabilidade em ambientes hostis.

Além de um roteador integrado, há muitos tipos diferentes de dispositivos que podem estar se conectando a uma rede doméstica. Por exemplo, computadores desktop, sistemas de jogos, sistemas de smart TV, impressoras, scanners, câmeras de segurança e dispositivos de controle do clima.

Roteadores residenciais e de pequenas empresas normalmente têm dois tipos principais de portas: portas Ethernet e uma porta de Internet. Além das portas com fio, muitos roteadores residenciais incluem antena sem fio e um ponto de acesso interno sem fio.

---

### Tecnologias de rede na residência

As tecnologias sem fio usam ondas eletromagnéticas para transportar informações entre dispositivos. O espectro eletromagnético inclui bandas de transmissão de rádio e televisão, luz visível, raios x e raios gama. Alguns tipos de ondas eletromagnéticas não são apropriados para transmitir dados. Outras partes do espectro são reguladas pelos governos e licenciadas a várias empresas para aplicações específicas.

Essas faixas não licenciadas do espectro são incorporadas a produtos de consumo, como os roteadores Wi-Fi encontrados na maioria das casas. As tecnologias sem fio mais usadas em redes residenciais estão nas faixas de frequências não licenciadas de 2,4 GHz e 5 GHz. Bluetooth é uma tecnologia que utiliza a banda de 2,4 GHz. Outras tecnologias que usam as bandas 2,4 GHz e 5 GHz são as modernas tecnologias de LAN sem fio que estão em conformidade com vários padrões IEEE 802.11. A diferença em relação à tecnologia de Bluetooth é que elas transmitem em um nível de potência muito maior, o que lhes dá maior alcance e melhor rendimento.

Embora muitos dispositivos de rede doméstica suportem comunicações sem fio, ainda existem algumas aplicações em que os dispositivos se beneficiam de uma conexão de switch com fio. O protocolo com fio implementado com mais frequência é o protocolo Ethernet. Dispositivos conectados diretamente usam um cabo de ligação Ethernet, normalmente par trançado não blindado. A categoria 5e é o cabeamento mais comum usado em uma LAN. O cabo é composto de 4 pares de fios que são trançados para reduzir a interferência elétrica. Para residências que não têm cabeamento UTP, há outras tecnologias, como o uso da rede elétrica, que podem distribuir conectividade com fio nos ambientes.

---

### Padrões de Redes Sem Fio

O padrão IEEE 802.11 controla o ambiente WLAN. Os padrões sem fio de LANs usam as bandas de frequência de 2,4 GHz e 5 GHz. Coletivamente, essas tecnologias são conhecidas como Wi-Fi. O Wi-Fi Alliance é responsável por testar dispositivos de LAN sem fio de diferentes fabricantes.

Os roteadores sem fio que usam os padrões 802.11 têm várias configurações que devem ser ajustadas. Estas configurações incluem:

- **Modo de Rede –** Determina o tipo de tecnologia que deve ser suportada. Por exemplo, 802.11b, 802.11g, 802.11n ou Mixed Mode (Modo misto).
- **Nome da rede (SSID) –** Usado para identificar a WLAN. Todos os dispositivos que desejam participar na WLAN devem ter o mesmo SSID.
- **Canal Padrão –** Especifica o canal no qual a comunicação ocorrerá. Por padrão, é configurado para Automático para permitir que o ponto de acesso (AP) determine o melhor canal a usar.
- **Broadcast SSID –** Determina se o SSID será transmitido para todos os dispositivos dentro do intervalo. Por padrão, é configurado para Ativado.

O protocolo 802.11 pode fornecer melhor taxa de transferência, dependendo do ambiente de rede sem fio. Se todos os dispositivos sem fio se conectarem com o mesmo padrão 802.11, poderão ser obtidas as velocidades máximas desse padrão. Se o ponto de acesso estiver configurado para aceitar apenas um padrão 802.11, os dispositivos que não usarem esse padrão não poderão se conectar ao access point. Um ambiente de rede sem fio com modo misto pode incluir dispositivos que utilizem qualquer padrão Wi-Fi atual.

Ao criar uma rede sem fio, é importante que os componentes sem fio se conectem à WLAN apropriada. Isso é feito por meio do SSID. O SSID é usado para informar aos dispositivos sem fio, chamados STAs, à qual WLAN eles pertencem e com quais outros dispositivos eles podem se comunicar. O broadcast SSID permite que outros dispositivos e clientes sem fio detectem automaticamente o nome da rede sem fio. Se o broadcast SSID estiver desativado, insira manualmente o SSID nos dispositivos sem fio.

---

### Configurar um roteador doméstico

Muitos roteadores sem fio para residências têm um utilitário de configuração automática que pode ser usado para ajustar as configurações básicas no roteador. Para se conectar ao roteador usando uma conexão com fio, conecte um cabo de ligação Ethernet à porta de rede no computador. Conecte a outra extremidade a uma porta LAN no roteador.

Após a confirmação de que o computador está conectado ao roteador de rede e que as luzes dos links na NIC (placa de interface de rede) indicam uma conexão ativa, o computador precisa de um endereço IP. A maioria dos roteadores de rede estão configurados para que o computador receba um endereço IP automaticamente de um servidor DHCP local.

Antes de entrar no utilitário de configuração ou configurar manualmente o roteador através de um navegador da Web, você deve considerar como a rede será usada. Considere o que você chamará de rede e quais dispositivos devem se conectar à rede. Não é uma boa prática incluir o modelo do dispositivo ou o nome da marca como parte do SSID, pois as pesquisas na Internet podem expor falhas de segurança.

O modo de uso da rede determina quem pode acessar a rede doméstica. Muitos roteadores são compatíveis com a filtragem de endereços MAC. Isso permite identificar especificamente quem tem permissão na rede sem fio. Isso torna a rede sem fio mais segura, mas também reduz a flexibilidade ao conectar dispositivos novos. Em alguns roteadores sem fio, é possível configurar o acesso para convidado. Essa é uma área de cobertura do SSID que permite o acesso aberto, restringindo-o apenas ao uso da Internet.

---

# 4.5.2 Webster – Questões para Reflexão

Eu me diverti tanto usando este módulo na praia que acho que vou configurar uma rede sem fio em casa. Dessa forma, posso acompanhar este curso em qualquer lugar da minha casa. Construir sua rede doméstica para ser uma rede sem fio faz sentido. Posso trabalhar no lado oeste da Web, pegar o pôr do sol e voltar para o lado leste pela manhã. É muito melhor do que ficar preso na minha mesa o dia todo! Você configurou sua rede doméstica? Caso contrário, você poderia fazer isso se fosse necessário?

# 4.5.3 Questionário - Construindo uma rede doméstica

**P1 –** Que tipo de comunicação sem fio se baseia nos padrões 802.11?

- WAN por Celular
- Infravermelho
- **Wi-Fi** ✓
- Bluetooth

> **Feedback:** Os padrões IEEE 802.11 definem as especificações de LAN sem fio Wi-Fi.

---

**P2 –** Qual configuração de roteador sem fio impediria que intrusos usassem sua rede doméstica?

- Endereço IP
- **criptografia** ✓
- o local dos roteadores
- nome da rede

> **Feedback:** A criptografia configurada no roteador sem fio pode fornecer comunicações seguras e impedir que intrusos usem sua rede doméstica.

---

**P3 –** Que tipo de dispositivo geralmente é conectado às portas Ethernet em um roteador sem fio doméstico?

- modem DSL
- antena sem fio
- **dispositivo LAN** ✓
- cable modem

> **Feedback:** Os dispositivos de rede de área local (LAN) normalmente são conectados às portas Ethernet de um roteador sem fio para se comunicarem na mesma rede com fio local.

---

**P4 –** Que tipo de tecnologia de rede é usada para a comunicação de baixa velocidade entre dispositivos periféricos?

- Ethernet
- **Bluetooth** ✓
- 802.11
- próprios e adquiridos

> **Feedback:** Bluetooth é uma tecnologia de conexão sem fio que usa a frequência de 2,4 GHz para conectar dispositivos periféricos em uma conexão de curta distância e de baixa velocidade.

---

**P5 –** O que pode ser usado para permitir que dispositivos móveis visitantes se conectem a uma rede sem fio e restrinja o acesso desses dispositivos somente à Internet?

- criptografia
- filtragem de endereços MAC
- autenticação
- **SSID de convidado** ✓

> **Feedback:** Muitos roteadores sem fio oferecem suporte a um SSID de convidado especial que permite que dispositivos não confiáveis acessem a Internet, mas restringem o acesso deles aos recursos de rede local.

---

**P6 –** Qual seria o objetivo de um usuário doméstico ter implementado WiFi?

- **para criar uma rede sem fio que pode ser usada por outros dispositivos** ✓
- para ouvir várias estações de rádio
- para conectar fones de ouvido sem fio a um dispositivo móvel
- para conectar um teclado a um PC

> **Feedback:** Uma rede WiFi ou LAN sem fio é usada para se conectar a um roteador sem fio que, por sua vez, se conecta à Internet. Os dispositivos sem fio conectam-se à rede WiFi pelo roteador sem fio.

---

**P7 –** Qual é o outro termo para a porta de Internet de um roteador sem fio?

- porta do switch
- **porta WAN** ✓
- porta LAN
- porta local

> **Feedback:** A porta da Internet de um roteador sem fio também pode ser conhecida ou rotulada como a porta WAN. Esta porta conecta o roteador para a Internet usado modem DSL ou a cabo.

---

**P8 –** Que tipo de cabo de rede consiste em 4 pares de fios trançados?

- Ethernet sobre linha de energia (Ethernet sobre powerline)
- **Categoria 5e** ✓
- coaxial
- Fibra Óptica

> **Feedback:** O cabo de categoria 5e, que é um cabo de par trançado não blindado, consiste em 4 pares de fios trançados para reduzir a interferência elétrica.

---

**P9 –** Qual é a configuração padrão para broadcast em um roteador sem fio?

- Automático
- Desabilitado
- Desativado
- **Habilitado** ✓

> **Feedback:** Quando um roteador sem fio está sendo configurado, a configuração padrão para o broadcast SSID é ativada. Isso significa que o roteador sem fio transmitirá o SSID para todos os dispositivos. Isso pode ser uma preocupação de segurança e a melhor prática é desativar a configuração de broadcast.

---

**P10 –** Qual é uma característica do SSID da rede?

- Ele contém exatamente 16 caracteres.
- Isso só é necessário para acesso para convidados
- Ele é criptografado por padrão
- **Ele é case sensitive** ✓

> **Feedback:** O SSID é o nome da rede e faz distinção entre maiúsculas e minúsculas. Pode conter até 32 caracteres. Todos os computadores que se conectam à rede sem fio devem saber o SSID.
