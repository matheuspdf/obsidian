
# 18.0 Introdução

## 18.0.1 Webster - Por que devo fazer este módulo?

Deixe-me apresentá-lo ao meu amigo Bob! Bob trabalha na área de TI em Vancouver, no Canadá, e tem alguma experiência em redes. Ele está prestando consultoria para seus amigos, Marcy e Vincent, que compraram uma loja de móveis. Eles querem expandir suas operações físicas e se estabelecer na loja online também. Atualmente, a rede interna da loja lida com transações e estoque na loja. Marcy e Vincent querem adicionar câmeras de segurança, telefones VoIP e também expandi-la para incluir comércio eletrônico e remessa. Bob explica que isso vai ser mais caro do que seus amigos tinham previsto. Ele está pensando em projetar a futura rede para a loja de móveis. Ele explica que deve considerar a tolerância a falhas, a escalabilidade, o QoS e a segurança. Além disso, a rede atualmente é plana, não hierárquica. As redes hierárquicas são bem dimensionadas e acomodarão melhor esse negócio em crescimento.

Uau! Isso é muito para Marcy e Vincent entenderem. Eles não estão familiarizados com esses problemas de rede. E você? Aproveite este módulo para saber mais sobre redes confiáveis e design de rede hierárquica!

## 18.0.2 O que vou aprender neste módulo?

**Titulo do módulo:** Design de rede

**Módulo Objetivo:** Explicar os componentes de um projeto de rede hierárquica.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Redes confiáveis|Descrever os quatro requisitos básicos de uma rede confiável.|
|Projeto de rede hierárquica|Explicar a função em cada camada do modelo de design de rede de 3 camadas.|

# 18.1 Redes confiáveis

Você já esteve ocupado trabalhando on-line, e achou que "a internet caiu" ? Como você sabe até agora, a internet não caiu, você acabou de perder sua conexão com ela. Isso é muito frustrante. Com tantas pessoas no mundo confiando no acesso à rede para trabalhar e aprender, é imperativo que as redes sejam confiáveis. Nesse contexto, confiabilidade significa mais do que sua conexão à Internet. Este tópico se concentra nos quatro aspectos da confiabilidade da rede.

O papel da rede mudou de uma rede somente de dados para um sistema que permite a conexão de pessoas, dispositivos e informações em um ambiente de rede convergente rico em mídia. Para que as redes funcionem com eficiência e cresçam nesse tipo de ambiente, a rede deve ser construída sobre uma arquitetura de rede padrão.

As redes também suportam uma ampla gama de aplicativos e serviços. Elas devem operar sobre muitos tipos diferentes de cabos e dispositivos, que compõem a infraestrutura física. O termo arquitetura de redes, neste contexto, refere-se às tecnologias que apoiam a infraestrutura e os serviços programados e as regras, ou protocolos, que movimentam os dados na rede.

À medida que as redes evoluem, aprendemos que há quatro características básicas que os arquitetos de rede devem atender para atender às expectativas do usuário:

- Tolerância a falhas
- Escalabilidade
- Qualidade de serviço (QoS)
- Segurança


## 18.1.2 Vídeo - Tolerância a falhas

**Selecione o botão Reproduzir para assistir ao vídeo.**

Neste cenário, temos duas partes em nossa rede. Cada uma com seu próprio caminho para nosso ISP e a Internet. Pacotes originados no PC um são encaminhados para o Roteador A e para o ISP. Enquanto os pacotes provenientes do PC dois são encaminhados para o Roteador B e, em seguida, para o mesmo ISP.

Mas, o que acontece quando há um problema com o Roteador A, ou com um link usado no caminho para o Roteador A? Pacotes que precisam do roteador A para encaminhá-los para a Internet serão descartados, e não podem mais alcançar o destino final.

Uma rede tolerante a falhas é aquela que pode continuar suas operações, sem interrupção, quando um ou mais componentes da rede falham. Agora instalamos links adicionais em nossa rede, oferecendo múltiplos caminhos para alcançar nosso ISP e a Internet. Ter vários caminhos para um destino é conhecido como redundância, que é uma das formas de tornar a rede tolerante a falhas. Se um caminho falhar, os pacotes são automaticamente encaminhados usando um link diferente. Quanto mais redundância em uma rede, mais tolerante a falhas a rede se torna.


## 18.1.3 Tolerância a Falhas

Uma rede tolerante a falhas é aquela que limita o número de dispositivos afetados durante uma falha. Ela foi desenvolvida para permitir uma recuperação rápida quando ocorre uma falha. Essas redes dependem de vários caminhos entre a origem e o destino de uma mensagem. Se um caminho falhar, as mensagens serão instantaneamente enviadas por um link diferente. Ter vários caminhos para um destino é conhecido como redundância.

A implementação de uma rede comutada por pacotes é uma das maneiras pelas quais redes confiáveis fornecem redundância. A comutação de pacotes divide os dados do tráfego em pacotes que são roteados por uma rede compartilhada. Uma única mensagem, como um e-mail ou stream de vídeo, é dividido em vários blocos, chamados pacotes. Cada pacote tem as informações de endereço necessárias da origem e do destino da mensagem. Os roteadores na rede alternam os pacotes com base na condição da rede no momento. Isso significa que todos os pacotes em uma única mensagem podem seguir caminhos muito diferentes para o mesmo destino. Na figura, o usuário desconhece e não é afetado pelo roteador que está alterando dinamicamente a rota quando um link falha.

![[Pasted image 20260612185348.png]]

## 18.1.4 Escalabilidade

Uma rede escalável se expande rapidamente para oferecer suporte a novos usuários e aplicativos. Ela faz isso sem degradar o desempenho dos serviços que estão sendo acessados por usuários existentes. A figura mostra como uma nova rede é facilmente adicionada a uma rede existente. Essas redes são escaláveis porque os projetistas seguem padrões e protocolos aceitos. Isso permite que os fornecedores de software e hardware se concentrem em melhorar produtos e serviços sem precisar criar um novo conjunto de regras para operar na rede.

![[Pasted image 20260612185406.png]]

## 18.1.5 Qualidade de Serviço

A qualidade do serviço (QoS) é um requisito crescente das redes atualmente. Novos aplicativos disponíveis para usuários em redes, como transmissões de voz e vídeo ao vivo, criam expectativas mais altas em relação à qualidade dos serviços entregues. Você já tentou assistir a um vídeo com intervalos e pausas constantes? Conforme o conteúdo de vídeo, voz e dados convergem na mesma rede, o QoS se torna um mecanismo essencial para gerenciar os congestionamentos e garantir a entrega confiável do conteúdo para todos os usuários.

O congestionamento acontece quando a demanda por largura de banda excede a quantidade disponível. A largura de banda é medida pelo número de bits que podem ser transmitidos em um único segundo, ou bits por segundo (bps). Ao tentar uma comunicação simultânea pela rede, a demanda pela largura de banda pode exceder sua disponibilidade, criando um congestionamento na rede.

Quando o volume de tráfego é maior do que o que pode ser transportado pela rede, os dispositivos retêm os pacotes na memória até que os recursos estejam disponíveis para transmiti-los. Na figura, um usuário está solicitando uma página da Web e outro está em uma ligação. Com uma política de QoS configurada, o roteador é capaz de gerenciar o fluxo do tráfego de voz e de dados, priorizando as comunicações por voz se a rede ficar congestionada. O foco do QoS é priorizar o tráfego sensível ao tempo. O tipo de tráfego, e não o conteúdo, é o que é importante.

![[Pasted image 20260612185420.png]]

## 18.1.6 Segurança de rede

A infraestrutura da rede, os serviços e os dados contidos nos dispositivos conectados à rede são recursos pessoais e comerciais críticos. Os administradores de rede devem abordar dois tipos de preocupações de segurança de rede: segurança da infraestrutura de rede e segurança da informação.

Proteger a infraestrutura de rede inclui proteger fisicamente os dispositivos que fornecem conectividade de rede e impedir o acesso não autorizado ao software de gerenciamento que reside neles, conforme mostrado na figura.

![[Pasted image 20260612185431.png]]

Os administradores de rede também devem proteger as informações contidas nos pacotes transmitidos pela rede e as informações armazenadas nos dispositivos conectados à rede. Para atingir os objetivos de segurança de rede, existem três requisitos principais.

- **Confidencialidade** - A confidencialidade dos dados significa que apenas os destinatários pretendidos e autorizados podem acessar e ler os dados.
- **Integridade** - A integridade dos dados garante aos usuários que as informações não foram alteradas na transmissão, da origem ao destino.
- **Disponibilidade** - A disponibilidade de dados garante aos usuários acesso oportuno e confiável aos serviços de dados para usuários autorizados.


## 18.1.7 Verifique sua compreensão - Redes Confiáveis

**Verifique sua compreensão sobre Redes Confiáveis escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Quando os designers seguem padrões e protocolos aceitos, qual das quatro características básicas da arquitetura de rede é alcançado?

- [ ] Tolerância a falhas
- [x] Escalabilidade
- [ ] QoS
- [ ] Segurança

✅ RESPOSTA CORRETA: Escalabilidade

> A escalabilidade ocorre quando os designers seguem padrões e protocolos aceitos.

---

### Pergunta 2

Confidencialidade, integridade e disponibilidade são requisitos de qual das quatro características básicas da arquitetura de rede?

- [ ] Tolerância a falhas
- [ ] Escalabilidade
- [ ] QoS
- [x] Segurança

✅ RESPOSTA CORRETA: Segurança

> Confidencialidade, integridade e disponibilidade são requisitos de segurança.

---

### Pergunta 3

Com qual tipo de política, um roteador pode gerenciar o fluxo de dados e tráfego de voz, dando prioridade às comunicações de voz se a rede sofrer congestionamento?

- [ ] Tolerância a falhas
- [ ] Escalabilidade
- [x] QoS
- [ ] Segurança

✅ RESPOSTA CORRETA: QoS

> QoS significa que um roteador gerenciará o fluxo de dados e tráfego de voz, dando prioridade às comunicações de voz.

---

### Pergunta 4

Ter vários caminhos para um destino é conhecido como redundância. Este é um exemplo de qual característica da arquitetura de rede?

- [x] Tolerância a falhas
- [ ] Escalabilidade
- [ ] QoS
- [ ] Segurança

✅ RESPOSTA CORRETA: Tolerância a falhas

> Redundância é um exemplo de arquitetura de rede tolerante a falhas.


# 18.2 Projeto de rede hierárquica

## 18.2.1 Endereços Físicos e Lógicos

O nome de uma pessoa normalmente não muda. O endereço de uma pessoa, por outro lado, refere-se a onde a pessoa mora e pode mudar. Em um host, o endereço MAC não muda; ele é atribuído fisicamente à NIC do host e é conhecido como endereço físico. O endereço físico permanece o mesmo, independentemente de onde o host está localizado na rede.

O endereço IP é semelhante ao endereço de uma pessoa. Ele é conhecido como endereço lógico porque é atribuído logicamente com base na localização do host. O endereço IP (ou endereço de rede) é atribuído a cada host por um administrador de rede com base na rede local.

Os endereços IP contêm duas partes. Uma parte identifica a porção de rede. A porção de rede do endereço IP será a mesma para todos os hosts conectados à mesma rede local. A segunda parte do endereço IP identifica o host individualmente nesta rede Dentro da mesma rede local, a porção de host do endereço IP é exclusiva para cada host como mostrado na figura.

Os endereços MAC físico e IP lógico são necessários para que um computador se comunique em uma rede hierárquica, assim como o nome e o endereço de uma pessoa são necessários para enviar uma carta.

![[Pasted image 20260613104812.png]]

## 18.2.2 Vídeo - Visualizar Informações de Rede em Meus Dispositivos

**Selecione o botão Reproduzir para assistir ao vídeo.**

Neste vídeo, vamos ver como obtemos informações sobre as várias placas de interface de rede que estão contidas em nossos PCs. No caso deste laptop, há tanto uma placa de rede com fio como uma placa de rede sem fio.

Para visualizar as propriedades desses dispositivos, é preciso ir para a Central de Rede e Compartilhamento. Isso pode ser feito facilmente indo para o ícone da bandeja do sistema, clicando com o botão direito do mouse e abrindo a Central de Rede e Compartilhamento. Isso traz à tona a lista de conexões que estão atualmente ativas.

Para ver os adaptadores individuais, é necessário ir para Alterar as Configurações do Adaptador. Lá é possível ver uma conexão de área local, que é uma conexão com fio, e também uma conexão de rede sem fio. Para visualizar as propriedades de uma conexão específica, basta clicar com o botão direito e ir até as propriedades.

Existem várias propriedades diferentes associadas a um adaptador de rede em um computador Windows. Normalmente, o que mais nos interessa são as configurações para o protocolo de internet. Nas propriedades do IPv4, é possível ver se o dispositivo está recebendo seu endereço IP automaticamente, o que significa que está sendo distribuído por um servidor DHCP e não foi configurado estaticamente. No adaptador de rede com fio, o endereço IP pode estar configurado estaticamente, o que significa que um administrador atribuiu o endereço IP para o PC especificamente e foi digitado manualmente.

Mais informações podem ser obtidas olhando as informações de status da conexão específica. É possível ver rapidamente se há acesso à Internet e a qualidade do sinal chegando do ponto de acesso sem fio. Nos detalhes, há ainda mais informações: os diferentes tipos de conexão, onde está sendo obtido o DNS, e a configuração DHCP para aquele adaptador específico, incluindo a data de expiração da concessão. Também é possível obter informações sobre o endereço MAC, o tipo de conexão e as redes sem fio em que se está conectado.

Na conexão de área local, as informações são ligeiramente diferentes. Nos detalhes, é possível obter o endereço MAC, o endereço IPv4 e, se um endereço IPv6 estivesse configurado, ele também seria exibido.

A maioria dessas informações que aparecem no status do driver NIC também pode ser visualizada acessando o prompt de comando dentro do Windows e executando o comando `ipconfig`. O `ipconfig /all` fornece muito mais informações sobre como o dispositivo está configurado, exibindo os adaptadores wireless e cabeado com todos os seus detalhes. É uma prática muito comum ter que encontrar o endereço MAC, o endereço IP e o status atual de um adaptador de PC, portanto esta é uma habilidade que se desenvolve com bastante prática.


## 18.2.3 Laboratório - Visualizando informações das placas de redes com e sem fio

Neste laboratório, você completará os seguintes objetivos:

- Identificar e trabalhar com as placas de rede do PC.
- Identificar e usar os ícones de rede da barra de tarefas.

### Laboratório – Exibição de informações da placa de rede com e sem fio

#### Objetivos

- Parte 1: Identificar e trabalhar com placas de rede do PC
- Parte 2: Identificar e usar os ícones de rede da barra de tarefas

#### Histórico / Cenário

Este laboratório requer que você determine a existência e o status das placas de rede (NICs) no PC. O Windows fornece diversas formas de ver e trabalhar com os suas placas de rede.

Neste laboratório, você terá acesso às informações da placa de rede do PC e alterará o status dessas placas.

#### Recursos Necessários

- 1 PC (Windows 10 com duas placas de rede, com e sem fio, e uma conexão sem fio)
- Um roteador sem fio

#### Instruções

##### Parte 1: Identificar e trabalhar com placas de rede do PC

Na Parte 1, você identificará os tipos de placa de rede no PC. Você irá explorar formas diferentes de extrair informações sobre essas placas de rede e como ativá-las e desativá-las.

> **Nota:** Este laboratório foi realizado usando um PC em execução no sistema operacional Windows 10. Você deve conseguir realizar o laboratório com outras versões de sistemas operacionais Windows. Entretanto, as telas e seleções de menu podem variar.

###### Etapa 1: Use as conexões de rede.

Você verificará quais conexões de rede estão disponíveis.

a. Clique com o botão direito do mouse em Iniciar e selecione Conexões de Rede.

b. A janela Conexões de Rede exibirá a lista das placas de rede disponíveis neste PC. Procure os adaptadores de Conexão local e Conexão de Rede sem Fio nesta janela.

> **Observação:** se a página Status da rede for exibida, clique em Alterar opções do adaptador para navegar até a janela Conexões de rede.

> **Observação:** Outros tipos de adaptadores de rede, como os de conexões de rede Bluetooth e de rede privada virtual (VPN), também podem aparecer nessa janela.

###### Etapa 2: Trabalhar com placas de rede sem fio.

Verifique as configurações de conexão de rede sem fio.

a. Clique com o botão direito do mouse na Conexão de rede sem fio. A primeira opção mostrará se sua placa de rede sem fio está ativada ou desativada. Se sua placa de rede sem fio estiver desativada, você terá uma opção para Ativá-la.

b. Verifique se a rede sem fio está conectada. Caso contrário, clique em Connect/Disconnect para conectar-se à rede desejada. Clique em Status para abrir a janela Status da Conexão de Rede sem Fio.

**Perguntas:**

O que é o Identificador do Conjunto de Serviços (SSID - Service Set Identifier) para o roteador sem fio de sua conexão?

**Resposta:** Digite suas respostas aqui.

Qual é a velocidade de sua conexão sem fio?

**Resposta:** Digite suas respostas aqui.

c. Clique em Detalhes para exibir a janela Detalhes da Conexão de Rede.

**Pergunta:**

Qual é o endereço MAC de sua placa de rede sem fio?

**Resposta:** Digite suas respostas aqui.

d. Abra um prompt de comando e digite ipconfig /all.

```
C:\Users\Bob> ipconfig /all
```

Observe que as informações exibidas são parecidas com as informações na janela Detalhes de Conexão de Rede. Quando tiver analisado os detalhes, clique em Fechar para retornar à janela Status da Conexão de Rede sem Fio.

e. Retorne para a janela Status da Conexão de Rede sem Fio. Clique em Propriedades sem Fio para abrir a janela Propriedades da Rede sem Fio na rede Home-Net.

f. Sempre use a segurança sem fio quando ela estiver disponível. Para verificar (ou configurar) as opções de segurança sem fio, clique na guia Segurança.

A janela exibirá o tipo de segurança e o método de criptografia ativados. Também é possível digitar (ou alterar) a security key (chave de segurança) nesta janela. Feche todas as janelas.

###### Etapa 3: Trabalhar com placas de rede cabeada.

Agora, vamos verificar as configurações de conexão de rede com fio.

a. Abra a janela Conexões de Rede ao clicar com o botão direito em Iniciar > Conexões de Rede no Windows.

> **Observação:** se a página Status da rede for exibida, clique em Alterar opções do adaptador para navegar até a janela Conexões de rede.

b. Selecione e clique com o botão direito na opção Conexão de Área Local para exibir a lista suspensa. Se a placa de rede estiver desativada, ative-a.

c. Clique na opção Status para abrir a janela Status da Conexão Local. Essa janela exibe as informações sobre a conexão cabeada à LAN.

d. Clique em Detalhes... para visualizar as informações de endereço da sua conexão LAN.

e. Abra um prompt de comando e digite ipconfig /all. Localize as informações de Conexão Local e compare com as informações exibidas na janela Detalhes da Conexão de Rede.

f. Feche todas as janelas no desktop.

##### Parte 2: Identificar e usar os ícones rede da notificação do sistema

Na Parte 2, você usará os ícones de rede na bandeja do sistema para exibir as redes disponíveis na rede.

a. O canto inferior direito da tela do Windows 10 contém a bandeja do sistema. Mova o mouse para exibir a bandeja do sistema.

b. Se você passar o mouse sobre o ícone de rede na bandeja do sistema, ele exibirá as redes conectadas no momento.

c. Clique no ícone de rede sem fio para ver os SSIDs da rede com e sem fio que estão ao alcance da placa de rede sem fio.

d. Clique com o botão direito no ícone da rede sem fio para ver uma opção de solução de problemas e abrir a janela Central de Rede e Compartilhamento.

e. Clique na opção Abrir Central de Rede e Compartilhamento.

f. A janela Central de Rede e Compartilhamento é uma janela central que exibe as informações sobre a rede ou as redes ativas, o tipo de rede e o tipo de acesso.

#### Reflexão

Por que você ativaria mais de uma placa de rede em um PC?

**Resposta:** As respostas podem variar. Várias placas de rede podem ser usadas se for necessário mais de um caminho para o PC. Um exemplo disso seria se o PC estivesse sendo utilizado como servidor proxy.

## 18.2.4 Analogia hierárquica

Imagine como a comunicação seria difícil se a única forma de enviar uma mensagem para alguém fosse usar o nome da pessoa. Se não houvesse limites de endereço, cidade ou país, entregar uma mensagem a uma pessoa específica no mundo inteiro seria quase impossível.

****Clique em cada botão abaixo para ver um exemplo de uma maneira hierárquica de localizar um local.**

América do Norte

![[Pasted image 20260614182828.png]]

Canadá

![[Pasted image 20260614182847.png]]

Nova Escócia

![[Pasted image 20260614182901.png]]

Halifax

![[Pasted image 20260614182916.png]]

Em uma rede Ethernet, o endereço MAC do host é semelhante ao nome de uma pessoa. Um endereço MAC exibe a identidade individual de um host específico, mas não indica onde ele está localizado na rede. Se cada um dos hosts na Internet (milhões e milhões deles) fosse identificado apenas por seu endereço MAC exclusivo, imagine como seria difícil localizar um host específico.

Além disso, a tecnologia Ethernet gera uma grande quantidade de tráfego de broadcast para que os hosts se comuniquem. Os broadcasts são enviados para todos os hosts dentro de uma única rede. Eles consomem largura de banda e reduzem o desempenho da rede. O que aconteceria se todos milhões de hosts conectados à Internet estivessem em uma única rede Ethernet e usassem broadcasts?

Por essas duas razões, grandes redes Ethernet com vários hosts não são eficientes. É melhor dividir redes maiores em redes menores e mais gerenciáveis. Uma forma de fazer isso é usar um modelo de design hierárquico.

## 18.2.5 Vantagens de um Design Hierárquico

Neste vídeo, vamos falar sobre os benefícios de um design hierárquico ao planejar uma rede.

Normalmente, as redes crescem organicamente. Começamos com um pequeno dispositivo e algumas estações de trabalho. Pense na sua rede doméstica: você tem alguns computadores, alguns outros dispositivos, talvez uma impressora e um console de jogos. Todas essas coisas se conectam, com fio ou sem fio, à sua rede doméstica.

Mas imagine se você começasse um negócio baseado em casa. Sua rede precisaria então crescer. Você pode precisar de dispositivos adicionais, estações de trabalho adicionais, scanners e impressoras. De repente, o pequeno dispositivo de rede doméstica não tem mais portas suficientes para suportar todos os vários dispositivos. À medida que a pequena empresa cresce, é necessário adicionar outro dispositivo, que é geralmente anexado ao dispositivo anterior, e então a rede começa a crescer organicamente.

Isso vale para a rede doméstica, mas também vale para redes corporativas. Muitas vezes, empresas de todos os tamanhos não pensam em como estão criando sua rede. Elas apenas permitem que ela cresça conforme precisam de mais dispositivos. Mas muito em breve, acabam com uma rede que tem dispositivos de missão crítica — como um servidor que os clientes precisam acessar — conectado junto com coisas que realmente não precisam ver esses tipos de tráfego, ou que podem até interferir com ele, como um console de jogos ou alguém baixando um filme. Basicamente, uma rede que cresce organicamente às vezes não é tão eficiente.

Ao longo do tempo, um tipo diferente de arquitetura de rede tornou-se praticamente o padrão: o projeto de rede hierárquica. Em um design hierárquico, pensamos em como vamos organizar a rede de forma que tenhamos coisas importantes, como servidores, separadas dos grupos de usuários que podem estar baixando Netflix ou jogando videogame. As redes hierárquicas são capazes de escalar porque são logicamente projetadas de tal forma que o tráfego que precisa sair de determinados usuários para determinados servidores não precisa viajar para áreas da rede onde não é necessário.

Vale lembrar o conceito de broadcast: pacotes de broadcast vão para todos que estão na mesma rede local, ou seja, na mesma área da rede conectada apenas por um switch. Em alguns casos, isso pode envolver centenas de dispositivos. Nas redes hierárquicas, todo o tráfego gerado por esses dispositivos permanece dentro de sua área da rede, o que faz com que essas redes escalem muito bem.

Em um projeto de rede hierárquica, existem nomes dados às várias camadas:

A **camada de acesso** é onde residem os dispositivos que realmente conectam usuários e outros dispositivos de usuário final. A principal função dessa camada é fornecer um ponto de entrada para os dispositivos "entrar" na rede. Alguns exemplos de dispositivos na camada de acesso são computadores de usuário final, telefones IP, pontos de acesso sem fio e, em algum grau, servidores e serviços.

A **camada de distribuição** fica acima da camada de acesso. Sua principal função é interconectar as redes da camada de acesso e direcionar o tráfego de tal forma que o tráfego que precisa permanecer local permaneça local, e o tráfego que precisa atravessar para redes remotas tenha um caminho para chegar a essas redes.

A **camada core** fica acima de tudo isso e é responsável pelo processamento de alta velocidade. Ela agrega todo o tráfego que vem dos vários dispositivos e garante que ele seja transmitido de forma eficiente através dos links WAN para a Internet.

Basicamente, esta é uma das principais razões pelas quais precisamos pensar na parte de planejamento de nossas redes antes de construí-las. Não é criticamente importante quando se está construindo uma rede doméstica, mas uma vez que você começa em uma rede que precisa estar ativa e operacional a maior parte do tempo, é essencial ter um design no qual a falha de um componente não afete todo o resto da rede.


## 18.2.6 Acesso, Distribuição e Núcleo

O tráfego IP é gerenciado de acordo com as características e os dispositivos associados a cada uma das três camadas do modelo de design hierárquico na rede: acesso, distribuição e núcleo.

**Clique abaixo para obter uma descrição de cada camada.**

**Camada de Acesso**

A camada de acesso fornece um ponto de conexão à rede para dispositivos de usuário final e permite que vários hosts se conectem a outros hosts por um dispositivo de rede, geralmente um switch ou um access point. Normalmente, todos os dispositivos dentro de uma única camada de acesso terão a mesma porção de rede do endereço IP.

Se uma mensagem é destinada a um host local, com base na porção de rede do endereço IP, a mensagem permanece local. Caso ela seja destinada a uma rede diferente, será passada para a camada de distribuição. Os switches fornecem a conexão para os dispositivos da camada de distribuição, geralmente um dispositivo layer 3 tal como um roteador ou um switch layer 3.

**Cisco 2960-XR**
![[Pasted image 20260614183105.png]]

**Camada de distribuição**

A camada de distribuição fornece um ponto de conexão para redes separadas e controla o fluxo de informações entre as redes. Normalmente, ela contém switches mais eficientes do que a camada de acesso, além de roteadores para fazer o roteamento entre redes. Os dispositivos da camada de distribuição controlam o tipo e a quantidade de tráfego que flui da camada de acesso para a camada do núcleo.

**Cisco C9300 Series**
![[Pasted image 20260614183121.png]]

**Camada de Núcleo**

A camada do núcleo é uma camada de backbone de alta velocidade com conexões (de backup) redundantes. Ela é responsável por transmitir grandes quantidades de dados entre várias redes finais. Os dispositivos da camada de núcleo normalmente incluem roteadores e switches de alta velocidade e muito eficientes,tais como um Cisco Catalyst 9600 mostrado na figura. O objetivo principal da camada do núcleo é transportar dados rapidamente.

**Cisco Catalyst 9600 Series**
![[Pasted image 20260614183142.png]]

## 18.2.7 Verifique sua compreensão - Projeto de Redes hierárquicas

### Pergunta 1

Um endereço IP é considerado que tipo de endereço:

- [ ] físico
- [x] lógica

✅ RESPOSTA CORRETA: lógica

> Um endereço IP é um endereço lógico.

---

### Pergunta 2

Um endereço MAC Ethernet é considerado que tipo de endereço:

- [x] físico
- [ ] lógica

✅ RESPOSTA CORRETA: físico

> Um endereço MAC Ethernet é um endereço físico.

---

### Pergunta 3

Qual endereço não muda quando um dispositivo está conectado a uma nova rede?

- [x] físico
- [ ] lógica

✅ RESPOSTA CORRETA: físico

> O endereço físico não muda quando o dispositivo está conectado a uma nova rede.

---

### Pergunta 4

Qual parte de um endereço IP identifica exclusivamente esse dispositivo na rede?

- [ ] físico
- [ ] lógica
- [ ] rede
- [x] host

✅ RESPOSTA CORRETA: host

> A parte Host de um endereço IP identifica um dispositivo em uma rede local.

---

### Pergunta 5

Qual camada de projeto oferece conectividade para dispositivos em uma LAN Ethernet?

- [ ] núcleo
- [ ] distribuição
- [x] acesso
- [ ] físico

✅ RESPOSTA CORRETA: acesso

> A camada de acesso oferece conectividade para dispositivos em uma LAN Ethernet.


# 18.3 Resumo de Design de Rede

## 18.3.1 O que aprendi neste módulo?

### Redes Confiáveis

À medida que as redes evoluem, aprendemos que existem quatro características básicas que os arquitetos de rede devem abordar para atender às expectativas dos usuários: tolerância a falhas, escalabilidade, QoS e segurança.

Uma rede tolerante a falhas é aquela que limita o número de dispositivos afetados durante uma falha. Isso permite uma recuperação rápida quando ocorre uma falha. Essas redes dependem de vários caminhos entre a origem e o destino de uma mensagem. Se um caminho falhar, as mensagens serão instantaneamente enviadas por um link diferente.

Uma rede escalável se expande rapidamente para oferecer suporte a novos usuários e aplicativos. Ela faz isso sem degradar o desempenho dos serviços que estão sendo acessados por usuários existentes. As redes podem ser escaláveis porque os projetistas seguem padrões e protocolos aceitos.

Atualmente, o QoS é um requisito cada vez maior das redes. Conforme o conteúdo de vídeo, voz e dados converge na mesma rede, o QoS se torna um mecanismo essencial para gerenciar os congestionamentos e garantir a entrega confiável do conteúdo para todos os usuários. A largura de banda da rede é medida em bps. Ao tentar uma comunicação simultânea pela rede, a demanda pela largura de banda pode exceder sua disponibilidade, criando um congestionamento na rede. O foco do QoS é priorizar o tráfego sensível ao tempo. O tipo de tráfego, e não o conteúdo, é o que é importante.

Os administradores de rede devem abordar dois tipos de preocupações de segurança de rede: segurança da infraestrutura de rede e segurança da informação. Os administradores de rede também devem proteger as informações contidas nos pacotes transmitidos pela rede e as informações armazenadas nos dispositivos conectados à rede. Para atingir os objetivos de segurança da rede, existem três requisitos principais: Confidencialidade, Integridade e Disponibilidade.

---

### Projeto de Rede Hierárquica

Os endereços IP contêm duas partes. Uma parte identifica a porção de rede. A porção de rede do endereço IP será a mesma para todos os hosts conectados à mesma rede local. A segunda parte do endereço IP identifica o host individualmente nesta rede. Os endereços IP lógicos e MAC físicos são necessários para que um computador se comunique em uma rede hierárquica.

A Central de Rede e Compartilhamento em um PC mostra suas informações básicas de rede e configura conexões, incluindo suas redes ativas e se você está conectado com ou sem fio à Internet e em sua LAN. Você pode ver as propriedades das conexões aqui.

Em uma rede Ethernet, o endereço MAC do host é semelhante ao nome de uma pessoa. Um endereço MAC exibe a identidade individual de um host específico, mas não indica onde ele está localizado na rede. Se cada um dos hosts na Internet (milhões e milhões deles) fosse identificado apenas por seu endereço MAC exclusivo, imagine como seria difícil localizar um host específico. É melhor dividir redes maiores em redes menores e mais gerenciáveis. Uma forma de fazer isso é usar um modelo de design hierárquico.

As redes hierárquicas são bem dimensionadas. A camada de acesso fornece um ponto de conexão para dispositivos de usuário final à rede e permite que vários hosts se conectem a outros hosts por meio de um dispositivo de rede, geralmente um switch ou um ponto de acesso sem fio. Normalmente, todos os dispositivos dentro de uma única camada de acesso terão a mesma porção de rede do endereço IP. A camada de distribuição fornece um ponto de conexão para redes separadas e controla o fluxo de informações entre as redes. Os dispositivos da camada de distribuição controlam o tipo e a quantidade de tráfego que flui da camada de acesso para a camada do núcleo. A camada de núcleo é uma camada de backbone de alta velocidade com conexões redundantes. Ela é responsável por transmitir grandes quantidades de dados entre várias redes finais. O objetivo principal da camada do núcleo é transportar dados rapidamente.


## 18.3.2 Webster - Perguntas para reflexão

Marcy e Vincent têm a sorte de ter a consultoria de Bob a respeito da rede em sua loja. Muitas pequenas empresas têm redes que crescem ao longo do tempo, mas não são projetadas para escalar de forma confiável ou segura. Marcy e Vincent entendem que, se dedicarem algum tempo e gastarem algum dinheiro agora, evitarão muitos problemas à medida que sua rede continue a crescer. Sabendo o que você sabe agora sobre redes confiáveis e escaláveis, há algo que você gostaria de fazer para atualizar sua própria rede em casa, na escola ou no trabalho?