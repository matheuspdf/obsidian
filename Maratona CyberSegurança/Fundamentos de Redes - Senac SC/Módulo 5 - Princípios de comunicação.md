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
