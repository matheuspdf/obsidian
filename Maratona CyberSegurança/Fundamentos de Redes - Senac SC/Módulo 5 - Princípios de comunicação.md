# 5.0 Introdução

## 5.0.1 Webster - Por que devo fazer este módulo?

No dia seguinte, Kishori tem um novo paciente, Srinivas, que acaba de ser admitido em um quarto. Ele é de Narayanpet e fala Telugu. Kishori fala Marathi. Esses dois idiomas indianos são muito diferentes. Kishori e Srinivas não falam a língua nativa do outro. No entanto, os dois falam inglês. Portanto, eles decidem se comunicar usando o inglês.

Antes de começar a nos comunicar, estabelecemos regras ou acordos para reger a conversa. Assim como Kishori e Srinivas, decidimos que método de comunicação devemos usar e qual linguagem devemos usar. Também podemos precisar confirmar se nossas mensagens foram recebidas. Por exemplo, Kishori pode fazer com que Srinivas assine um documento verificando se ele entendeu as instruções de cuidado de Kishori.

As redes também precisam de regras ou protocolos para garantir uma comunicação bem-sucedida. Este módulo abordará os princípios de comunicação em redes. Vamos começar!

## 5.0.2 O que vou aprender neste módulo?

### Princípios de Comunicação

**Objetivo do módulo:** Explicar a importância dos padrões e protocolos nas comunicações de rede.

|Tópico|Objetivo|
|---|---|
|**Protocolos de comunicação**|Descrever os protocolos de comunicação de rede.|
|**Padrões de comunicação**|Descrever os padrões de comunicação de rede.|
|**Modelos de comunicação de rede**|Comparar os modelos OSI e TCP/IP.|

# 5.1 Protocolos de comunicação

## 5.1.1 Protocolos de comunicação

A comunicação em nossa vida diária apresenta muitas formas e ocorre em vários ambientes. Temos diferentes expectativas se estamos conversando por meio da Internet ou participando de uma entrevista de emprego. Cada situação tem seus comportamentos e estilos correspondentes esperados.

Antes de começar a nos comunicar, estabelecemos regras ou acordos para reger a conversa. Esses contratos incluem o seguinte:

- Que método de comunicação devemos usar?
- Qual idioma devemos usar?
- Precisamos confirmar que nossas mensagens são recebidas?

**Clique abaixo para ver um exemplo de como determinar o método, o idioma e as estratégias de confirmação.**

### Método

1. Utiliza língua de sinais...
2. Anotações: *Desculpe, eu não compreendo sinais.*
3. Anotações: *Podemos usar anotações?*
4. Anotações: *Sim, assim fica bom.*

Antes que a comunicação possa começar, talvez tenhamos que chegar a um acordo sobre o idioma usado.

---

### Idioma

1. Eu falo japonês e inglês.
2. Eu falo espanhol e inglês.
3. Nós podemos conversar em inglês então!

Antes que a comunicação possa começar, talvez tenhamos que chegar a um acordo sobre o idioma usado.

---

### Confirmação

1. Gostaria de pedir três camisas pretas, tamanho médio.
2. Sim, entendi seu pedido: três camisas pretas médias.
3. Sim, está correto. Obrigada.

A comunicação é bem-sucedida quando a mensagem pretendida foi recebida e confirmada.


Essas regras, ou protocolos, devem ser seguidas para que a mensagem seja transmitida e entendida adequadamente. Entre os protocolos que direcionam a comunicação humana bem sucedida estão:

- Um emissor e um receptor identificados
- Acordo sobre o método de comunicação (face a face, por telefone, carta, foto)
- Língua e gramática comum
- Velocidade e ritmo de transmissão
- Requisitos de confirmação ou recepção

As técnicas usadas nas comunicações de rede compartilham esses fundamentos com as conversas humanas.

Pense nos protocolos aceitos normalmente para enviar mensagens de texto para seus amigos.


## 5.1.2 Por que protocolos são importantes

Assim como os seres humanos, os computadores usam regras (ou seja, protocolos) para se comunicarem. Os protocolos são necessários para que os computadores se comuniquem corretamente na rede. Em ambientes com e sem fio, uma rede local é definida como uma área onde todos os hosts devem "falar a mesma linguagem" ou, na terminologia dos computadores, "compartilhar um protocolo em comum".

Se todas as pessoas em uma sala falarem uma linguagem diferente, não conseguirão se comunicar. Da mesma forma, se os dispositivos em uma rede local não usarem os mesmos protocolos, eles não poderão se comunicar.

Os protocolos de rede definem as regras de comunicação pela rede local. Como mostrado na tabela, eles incluem o formato, o tamanho, o tempo, a codificação, o encapsulamento e os padrões de mensagem.

### Características de Protocolo

| Característica de protocolo | Descrição |
|-----------------------------|-----------|
| Formato da mensagem | Quando uma mensagem é enviada, ela deve usar um formato ou estrutura específica. Os formatos da mensagem dependem do tipo de mensagem e do canal usado para entregá-la. |
| Tamanho da mensagem | As regras que regem o tamanho das partes transmitidas por meio da rede são muito rígidas. Eles também podem ser diferentes, dependendo do canal usado. Quando uma mensagem longa é enviada de um host para outro em uma rede, pode ser necessário dividir a mensagem em partes menores para garantir que ela seja entregue de forma confiável. |
| Temporização | Muitas funções de comunicação de rede dependem de temporização. A temporização determina a velocidade com que os bits são transmitidos na rede. Também afeta quando um host individual pode enviar dados e a quantidade total de dados que pode ser enviada em qualquer transmissão. |
| Codificação | As mensagens enviadas pela rede são convertidas primeiramente em bits pelo host emissor. Cada bit é codificado em um padrão de sons, de ondas de luz ou de impulsos elétricos, dependendo da mídia de rede em que os bits são transmitidos. O host de destino recebe e decodifica os sinais para interpretar a mensagem. |
| Encapsulamento | Cada mensagem transmitida em uma rede deve incluir um cabeçalho com informações de endereçamento que identifique os hosts de origem e destino. Caso contrário, ela não poderá ser entregue. Encapsulamento é o processo de adicionar essas informações aos dados que compõem a mensagem. Além do endereçamento, podem existir outras informações no cabeçalho que garantem que a mensagem foi entregue ao aplicativo correto no host de destino. |
| Padrão da mensagem | Algumas mensagens exigem uma confirmação antes que a próxima mensagem possa ser enviada. Esse tipo de padrão de solicitação/resposta é um aspecto comum em muitos protocolos de rede. No entanto, existem outros tipos de mensagens que podem ser simplesmente transmitidas pela rede, sem a preocupação de chegarem ao seu destino. |

## 5.1.3 Verifique a sua compreensão - Protocolos de Comunicação


## Pergunta 1

Bianka, uma viajante polaca em Hanói, no Vietnã, para e pergunta a Nguyệt como chegar ao templo de Ngoc Son. Eles se comunicam verbalmente e determinam que os dois falam inglês. Depois de receber instruções em inglês para chegar no templo, Bianka as repete para Nguyệt. Nguyệt diz: "Sim, isso está correto." Selecione a ordem dos protocolos de comunicação usados neste cenário?

- confirmação, método, idioma
- idioma, método, confirmação
- método, confirmação, idioma
- **[CORRETO] método, idioma, confirmação**

**Feedback:** Bianka e Nguyệt primeiro decidiram sobre o método de comunicação (verbal). Então eles determinaram que ambos falam inglês (idioma). Por fim, Bianka repetiu as instruções (confirmação).

---

## Pergunta 2

Rory está estudando os campos dentro de um quadro Ethernet para um próximo teste e percebe que o endereço MAC (Media Access Control) de destino é listado primeiro antes do endereço MAC de origem. Qual das seguintes características de protocolo que Rory está investigando?

- **[CORRETO] encapsulamento**
- temporização de mensagem
- codificação
- temporização
- padrão de mensagem

**Feedback:** Os protocolos de rede geralmente têm algum tipo de informação de endereçamento para indicar a origem e o destino da mensagem.

---

## Pergunta 3

À medida que Rory continua estudando Ethernet, ele descobre que um quadro pode normalmente ter de 64 a 1518 bytes de informações que são convertidas em uma série de bits antes de serem enviadas para a rede. Quais são as duas características do protocolo Ethernet que Rory aprendeu?

- **[CORRETO] codificação**
- encapsulamento
- padrão de mensagem
- **[CORRETO] tamanho da mensagem**
- temporização

**Feedback:** Os protocolos de rede normalmente especificam o tamanho máximo de uma mensagem. No caso do Ethernet, também há um tamanho mínimo de 64 bytes. Além disso, o Ethernet especifica um método para codificar os bits para que o destino possa decodificar a mensagem.

# 5.2 Padrões de comunicação

## 5.2.1 Vídeo - Dispositivos em uma bolha

### Como os Dispositivos Veem a Rede

#### Diagramas de Topologia

Nós visualizamos a rede por meio de diagramas de topologia, que mostram os dispositivos presentes, incluindo dispositivos finais (como desktops e servidores) e dispositivos intermediários (como switches e roteadores). Esses diagramas também podem conter informações detalhadas sobre cada dispositivo, como endereço MAC da Ethernet, endereço da NIC sem fio, endereço IP, endereço de gateway padrão e endereço do servidor DNS.

#### A Perspectiva do Dispositivo

Enquanto nós enxergamos toda a rede, cada dispositivo vive em sua própria "bolha": ele conhece apenas sua própria informação de endereçamento. Isso levanta várias questões:

- Como um dispositivo sabe seu endereço IP e a qual rede pertence?
- Como ele sabe se o destino está na mesma rede ou em outra?
- Se o destino estiver em outra rede, como o dispositivo sabe para qual intermediário encaminhar o pacote?
- Como o dispositivo sabe se a informação enviada foi recebida, ou se precisa reenviar algo?

A resposta para todas essas perguntas são os **protocolos** — as regras que governam como os dispositivos se comunicam.

#### Pacotes e Protocolos

A maioria das comunicações de rede é dividida em unidades menores chamadas **pacotes**. Quando pacotes são enviados pela rede, múltiplos protocolos atuam em conjunto, cada um com uma função específica:

- **Ethernet / Protocolos sem fio:** conectam fisicamente o dispositivo à rede.
- **DHCP / ICMPv6:** fornecem informações de endereçamento IP, incluindo:
  - O endereço IP, que identifica a qual rede o dispositivo pertence.
  - O endereço do gateway padrão, que indica para onde enviar pacotes destinados a outras redes.
  - O endereço do servidor DNS, usado quando o dispositivo conhece o nome de domínio do destino, mas precisa resolver o endereço IP correspondente.
- **IP:** responsável por entregar o pacote da origem ao destino final, de forma similar ao envio de uma carta.
- **TCP:** garante a confiabilidade da comunicação, assegurando que todas as informações enviadas foram recebidas. Se algum pacote IP não chegar ao destino, o TCP o reenvia.

#### Exemplo Prático

Quando um usuário acessa uma página web como `www.example.com`, o seguinte ocorre:

1. O dispositivo consulta o servidor DNS para obter o endereço IP do domínio.
2. O protocolo IP entrega os pacotes da origem até o servidor web.
3. O servidor web responde com a página solicitada.
4. O TCP garante que todos os pacotes que compõem a página chegaram corretamente.

#### Conclusão

Embora visualizemos a rede de forma ampla, o que permite que os dispositivos se localizem e se comuniquem é a combinação de múltiplos protocolos atuando em conjunto.


## 5.2.2. A Internet e os Padrões

Com o número cada vez maior de novos dispositivos e tecnologias on-line, como é possível gerenciar todas as mudanças e continuar oferecendo serviços como e-mail de maneira confiável? A resposta está nos padrões da Internet.

Um padrão é um conjunto de regras que determina como algo deve ser feito. Os padrões de rede e de Internet asseguram que todos os dispositivos conectados à rede implementem o mesmo conjunto de regras ou protocolos da mesma forma. O uso de padrões permite que diferentes tipos de dispositivos enviem informações entre si pela Internet. Por exemplo, o modo como um e-mail é formatado, encaminhado e recebido por todos os dispositivos segue um padrão. Se uma pessoa enviar um e-mail através de um computador pessoal, outra pessoa poderá usar um celular para receber e ler o e-mail, desde que o telefone celular utilize os mesmos padrões do computador pessoal.

## 5.2.3 Organizações de padronização de rede

Um padrão da Internet é o resultado final de um ciclo completo de discussão, solução de problemas e testes. Esses diferentes padrões são desenvolvidos, publicados e mantidos por diversas organizações, conforme mostrado na figura. Quando um novo padrão é proposto, cada etapa do processo de desenvolvimento e aprovação é registrada em um documento numerado de Solicitação de Comentários (Request for Comments - RFC), para que a evolução do padrão seja monitorada. As RFCs sobre padrões da Internet são publicadas e gerenciadas pelo IETF (Internet Engineering Task Force).

Outras organizações de padrões que suportam a Internet são mostradas na figura.

![[Pasted image 20260525204439.png]]

## 5.2.4 Verifique a sua compreensão - Padrões de comunicação

## Pergunta 1

As regras que regem as comunicações de rede, incluindo o formato, o tamanho, o tempo e o encapsulamento, são conhecidas como:

- sinalização
- mensagens
- **[CORRETO] protocolos**
- codificação

**Feedback:** Protocolos são as regras que regem as comunicações de rede, incluindo o formato, o tamanho, a temporização e o encapsulamento da mensagem.

---

## Pergunta 2

A IETF (Internet Engineering Task Force) registra e publica padrões da Internet em documentos conhecidos como:

- **[CORRETO] Request for Comments (RFC)**
- Internet Protocol Standards (IPS)
- Internet Specification Standards (ISS)
- IETF Standards Documentos (ISD)

**Feedback:** O IETF publica padrões da Internet conhecidos como RFCs.

# 5.3 Modelos de comunicação de rede

## 5.3.1 Vídeo - Protocolos de Rede

### Protocolos de Rede

#### O que são Protocolos

Protocolos são as regras que regem as comunicações. Nas comunicações humanas, usamos protocolos como linguagem comum, formalidade ou informalidade ao falar, formas de cumprimento, vestimenta e comportamento. De forma análoga, redes de computadores usam protocolos para controlar as comunicações entre dois dispositivos.

#### Protocolos Comuns em uma Mensagem de Rede

Uma mensagem de computador é composta por vários protocolos atuando em conjunto. Os principais são:

##### Ethernet
Rege a comunicação entre placa de interface de rede (NIC) na mesma rede local.

##### IP — Internet Protocol
Rege a comunicação desde a origem até o destino final. Dispositivos chamados roteadores utilizam o IP para determinar o caminho que os pacotes devem percorrer pela rede.

##### TCP — Transmission Control Protocol
Garante que as informações cheguem ao destino de forma confiável. Se os pacotes chegarem fora de ordem, o TCP os reordena corretamente.

##### HTTP — Hypertext Transfer Protocol
Rege a troca e transferência de HTML (Hypertext Markup Language). É o protocolo utilizado quando um usuário solicita ou baixa uma página da web.

#### Por que Estudar Protocolos

Aprender sobre protocolos de rede fornece uma melhor compreensão de como as redes operam, como implementá-las e configurá-las, e como solucionar problemas em redes.

## 5.3.2 Vídeo - A pilha de protocolos

### Pilha de Protocolos (Protocol Stack)

Comunicações bem-sucedidas requerem o uso de vários protocolos em conjunto. Quando um dispositivo envia uma mensagem, ele utiliza protocolos de diferentes camadas, formando o que é chamado de **Pilha de Protocolos**.

#### O Modelo TCP/IP

O modelo TCP/IP é organizado em quatro camadas, cada uma com protocolos específicos:

| Camada        | Protocolo (exemplo) | Função                                                                            |
| ------------- | ------------------- | --------------------------------------------------------------------------------- |
| Aplicação     | HTTP                | Rege a troca e transferência de HTML                                              |
| Transporte    | TCP                 | Garante a entrega confiável da mensagem                                           |
| Internet      | IP (v4 ou v6)       | Encaminha a mensagem da origem ao destino final, mesmo através de múltiplas redes |
| Acesso à Rede | Ethernet            | Comunica placa de interface de rede (NIC) para NIC na mesma rede                  |

#### Como Funciona na Prática

Ao enviar uma mensagem, o dispositivo utiliza protocolos de cada camada:

1. **Ethernet (Acesso à Rede):** atua na comunicação entre NICs dentro da mesma rede local.
2. **IP (Internet):** garante que a mensagem chegue da origem ao destino final, independentemente de quantas redes intermediárias existam.
3. **TCP (Transporte):** assegura que todas as informações cheguem de forma confiável e na ordem correta.
4. **HTTP (Aplicação):** governa a troca de conteúdo HTML entre o cliente e o servidor web.

O envio de qualquer mensagem de rede envolve o uso simultâneo de protocolos de todas essas camadas.


