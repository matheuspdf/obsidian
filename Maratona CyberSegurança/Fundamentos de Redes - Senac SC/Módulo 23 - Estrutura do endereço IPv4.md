# 23.0 Introdução

23.0.1 Webster - Por que devo fazer este módulo?

Bob investigou a rede atual e garantiu a Marcy e Vincent que eles podem usá-la até que ele faça as atualizações. Bob convenceu Marcy e Vincent a criar uma nova rede hierárquica que usará serviços em nuvem. Com as pesquisas de Bob e as explicações sobre redes, eles têm certeza de que essa é a melhor solução para eles. Eles realmente apreciam o conhecimento de Bob!

Você pode ter um longo caminho a percorrer antes de ter todo o conhecimento e a habilidade de Bob, mas acho que você está no caminho certo! Este módulo vai se aprofundar no estrutura do endereço IPv4. Preparado? Continue lendo.

## 23.0.2 O que vou aprender neste módulo?

**Titulo do módulo:** Estrutura do endereço IPv4

**Objetivo do módulo:** Calcular um esquema de sub-rede IPv4 para segmentar com eficiência sua rede.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Estrutura do endereço IPv4|Descrever a estrutura de um endereço IPv4, incluindo a parte de rede, a parte de host e a máscara de sub-rede.|

# 23.1 Estrutura do endereço IPv4

## 23.1.1 Porções de Rede e Host

Endereço IPv4

Um endereço IPv4 é um endereço hierárquico de 32-bits, composto por uma parte da rede e uma parte do host. Ao determinar a parte da rede versus a parte do host, você deve observar o fluxo de 32-bits, conforme mostrado na figura.

**Endereço IPv4**

![[Pasted image 20260618204051.png]]

Os bits na parte de rede do endereço devem ser iguais em todos os dispositivos que residem na mesma rede. Os bits na parte de host do endereço devem ser exclusivos para identificar um host específico dentro de uma rede. Se dois hosts tiverem o mesmo padrão de bits na parte de rede especificada do fluxo de 32 bits, esses dois hosts residirão na mesma rede.

Mas como os hosts sabem qual parte dos 32 bits identifica a rede e qual identifica o host? Esse é o papel da máscara de sub-rede.

## 23.1.2 A Máscara de Sub-Rede

Conforme mostrado na figura, atribuir um endereço IPv4 a um host requer o seguinte:

- **Endereço IPv4** - este é o endereço IPv4 exclusivo do host.
- **Máscara de sub-rede** – É usada para determinar a parte de rede de um endereço IPv4.

**Configuração IPv4 em um computador Windows**

![[Pasted image 20260618204107.png]]


### Máscara de sub-rede

**Observação**: Um endereço IPv4 de gateway padrão é necessário para acessar redes remotas e os endereços IPv4 do servidor DNS são necessários para converter nomes de domínio em endereços IPv4.

A máscara de sub-rede IPv4 é usada para diferenciar a parte da rede da parte do host de um endereço IPv4. Quando um endereço IPv4 é atribuído a um dispositivo, a máscara de sub-rede é usada para determinar o endereço de rede do dispositivo. O endereço de rede representa todos os dispositivos na mesma rede.

A próxima figura mostra uma máscara de sub-rede de 32 bits em formatos decimais e binários com pontos.

**Máscara de Sub-Rede**

![[Pasted image 20260618204130.png]]

### Associando um endereço IPv4 à sua máscara de sub-rede

Observe como a máscara de sub-rede é uma sequência consecutiva de 1 bits, seguida por uma sequência consecutiva de 0 bits.

Para identificar as partes da rede e do host de um endereço IPv4, a máscara de sub-rede é comparada com o endereço IPv4 bit por bit, da esquerda para a direita, conforme mostrado na figura.

**Associando um endereço IPv4 à sua máscara de sub-rede**

![[Pasted image 20260618204145.png]]

Observe que, na verdade, a máscara de sub-rede não contém a parte da rede ou host de um endereço IPv4, apenas informa ao computador onde procurar a parte do endereço IPv4 que é a parte da rede e qual parte é a parte do host.

O processo real usado para identificar a parte da rede e a parte de host é chamado de AND.

## 23.1.3 O Comprimento do Prefixo

Expressar os endereços de rede e os endereços de host com o endereço da máscara de sub-rede em decimal com pontos pode ser complicado. Felizmente, existe um método alternativo para identificar uma máscara de sub-rede, um método chamado comprimento do prefixo.

O comprimento do prefixo é o número de bits definido como 1 na máscara de sub-rede. Está escrito em "notação de barra", que é anotada por uma barra (/) seguida pelo número de bits definido como 1. Portanto, conte o número de bits da máscara de sub-rede e preceda-o com uma barra.

Consulte a tabela para exemplos. A primeira coluna lista várias máscaras de sub-rede que podem ser usadas com um endereço de host. A segunda coluna mostra o endereço binário de 32 bits convertido. A última coluna mostra o comprimento do prefixo resultante.

|Máscara de Sub-Rede|Endereço de 32 bits|Comprimento do Prefixo|
|---|---|---|
|255.0.0.0|11111111.00000000.00000000.00000000|/8|
|255.255.0.0|11111111.11111111.00000000.00000000|/16|
|255.255.255.0|11111111.11111111.11111111.00000000|/24|
|255.255.255.128|11111111.11111111.11111111.10000000|/25|
|255.255.255.192|11111111.11111111.11111111.11000000|/26|
|255.255.255.224|11111111.11111111.11111111.11100000|/27|
|255.255.255.240|11111111.11111111.11111111.11110000|/28|
|255.255.255.248|11111111.11111111.11111111.11111000|/29|
|255.255.255.252|11111111.11111111.11111111.11111100|/30|

**Observação:** Um endereço de rede também é conhecido como prefixo ou prefixo de rede. Portanto, o comprimento do prefixo é o número de 1 bits na máscara de sub-rede.

Ao representar um endereço IPv4 usando um comprimento de prefixo, o endereço IPv4 é gravado seguido do comprimento do prefixo sem espaços. Por exemplo, 192.168.10.10 255.255.255.0 seria gravado como 192.168.10.10/24. O uso de vários tipos de comprimentos do prefixo será discutido mais tarde. Por enquanto, o foco estará no prefixo /24 (ou seja, 255.255.255.0)


## 23.1.4 Determinando a rede: "AND" lógico

Um AND lógico é uma das três operações booleanas usadas na lógica booleana ou digital. As outras duas são OR e NOT. A operação AND é usada para determinar o endereço de rede.

AND lógico é a comparação de dois bits que produz os resultados mostrados abaixo. Observe como somente 1 AND 1 produz um 1. Qualquer outra combinação resulta em um 0.

- 1 E 1 = 1
- 0 E 1 = 0
- 1 E 0 = 0
- 0 E 0 = 0

**Observação** : Na lógica digital, 1 representa Verdadeiro e 0 representa Falso. Ao usar uma operação AND, ambos os valores de entrada devem ser Verdadeiro (1) para que o resultado seja Verdadeiro (1).

Para identificar o endereço de rede de um host IPv4, é feito um AND lógico, bit a bit, entre o endereço IPv4 e a máscara de sub-rede. Quando se usa AND entre o endereço e a máscara de sub-rede, o resultado é o endereço de rede.

Para ilustrar como AND é usado para descobrir um endereço de rede, considere um host com endereço IPv4 192.168.10.10 e máscara de sub-rede 255.255.255.0, conforme mostrado na figura:

- **Endereço de host IPv4** (192.168.10.10) - O endereço IPv4 do host em formato decimal com pontos e binário.
- **Máscara de sub-rede (255.255.255.0)** - A máscara de sub-rede do host nos formatos decimal com pontos e binário.
- **Endereço de rede (192.168.10.0)** - A operação lógica AND entre o endereço IPv4 e a máscara de sub-rede resulta em um endereço de rede IPv4 mostrado nos formatos decimal com pontos e binário.

![[Pasted image 20260618204253.png]]

Usando a primeira sequência de bits como exemplo, observe que a operação AND é executada no 1 bit do endereço do host com o 1 bit da máscara de sub-rede. Isso resulta em um bit 1 para o endereço de rede. 1 AND 1 = 1.

A operação AND entre um endereço de host IPv4 e uma máscara de sub-rede resulta no endereço de rede IPv4 para este host. Neste exemplo, a operação AND entre o endereço de host 192.168.10.10 e a máscara de sub-rede 255.255.255.0 (/24) resulta no endereço de rede IPv4 192.168.10.0/24. Esta é uma operação IPv4 importante, pois informa ao host a qual rede pertence.


## 23.1.5 Vídeo - Endereços de Rede, Host e Broadcast

**Selecione o botão Reproduzir para assistir ao vídeo.**

Todos os dispositivos em uma rede IPv4 precisam de um endereço lógico de 32 bits para se comunicar. Este endereço de host IPv4 lógico de 32 bits consiste em uma parte de rede ou ID de rede à esquerda, e uma parte do host ou ID do host à direita. O comprimento destes depende do tamanho da rede. Redes maiores terão uma porção de host mais longa.

Uma rede pode ser pensada como uma gama de endereços. Todos os dispositivos na mesma rede têm o mesmo padrão de bits para o ID de rede, mas eles terão um ID de host diferente.

Alguns endereços neste intervalo são reservados e têm um nome e significado especiais. Por exemplo, o primeiro endereço no intervalo é usado para identificar a própria rede, e não pode ser atribuído a nenhum host. É referido como o endereço de rede. O último no intervalo é chamado o endereço de difusão, e é usado para enviar uma mensagem a todos os dispositivos na rede de uma só vez. Ele também não pode ser atribuído a nenhum host. Todos os endereços IP entre a rede e os endereços de transmissão compõem o intervalo de host válido, e podem ser usados para endereçar os hosts na rede.

Para encaminhar dados, um dispositivo precisa saber em que rede está. Usando seu endereço IP de host, sua máscara de sub-rede, e um processo chamado binário, um dispositivo pode encontrar o que é chamado de endereço de rede. Este endereço representa a rede à qual o host pertence, e será ligeiramente diferente do IP do host. Para fazer isso, o dispositivo compara seu IP de host e sua máscara de sub-rede bit para bit. Se os valores de bit forem ambos binários, o resultado é binário. Se um ou ambos os valores de bit for zero, o resultado é um zero binário.

Vamos dar uma olhada em um exemplo. Digamos que temos um PC com um endereço IP de host e uma máscara de sub-rede de `192.168.2.38/24`, e usaremos o Anding para localizar o endereço de rede do host. Aqui está o IP do host em binário, aqui está a máscara de sub-rede em binário. Se os compararmos bit para bit, podemos ver que um e um resulta em um um, um zero e um resulta em um zero, e assim por diante, até que tenhamos comparado todos os 32 bits. Observe que o último octeto é todos zeros binários.

Porque estamos usando uma máscara de sub-rede `/24`, os três primeiros octetos representam a parte da rede, e o último octeto é a parte hospedeira. Endereços de rede sempre terão zeros binários em toda a sua porção de host, por mais longa que seja. Neste caso, os últimos oito bits. Se convertermos em decimal com pontos, podemos ver que este host pertence à rede `192.168.2.0/24`.

Agora vamos determinar o endereço de transmissão para esta rede, que é usado para enviar uma mensagem para todos os dispositivos na rede de uma só vez. Considerando que o endereço de rede tinha todos os zeros binários na parte do host, o endereço de transmissão terá todos os binários um na parte do host. Neste exemplo, a parte do host é apenas o último octeto. Para determinar o endereço de transmissão, mantemos a parte da rede a mesma, e alteramos a parte do host para todos os binários um. Isso resulta em um endereço de transmissão de `192.168.2.255`.

Em seguida, determinaremos os endereços de host utilizáveis que se encontram entre a rede e os endereços de transmissão. O primeiro host utilizável em binário serão todos zeros binários, com um binário um no final da parte do host. Convertendo para decimal com pontos, isso nos diz que o primeiro host utilizável nesta rede é `192.168.2.1`.

Finalmente, determinaremos o último host utilizável, que serão todos os binários um com um zero no final, o padrão de bits oposto do primeiro host utilizável. Convertendo para decimal com pontos, obtemos `192.168.2.254`.

---

Vamos recapitular nossos cálculos. Começamos com o endereço IP do host `192.168.2.38/24`. Usando o Anding binário, determinamos que este host pertence à rede `192.168.2.0`. Mantendo a parte da rede a mesma, mas colocando todos os binários um na parte do host, determinamos que o endereço de transmissão para esta rede é `192.168.2.255`. Novamente, mantendo a parte da rede a mesma mas alterando a parte do host, determinamos que o intervalo de host utilizável para atribuir endereços a dispositivos nesta rede é `192.168.2.1` — que é um número acima do endereço de rede — e `192.168.2.254`, que é um número abaixo do endereço de transmissão. O endereço IP de host original cai dentro deste intervalo.

---

Coisas a ter em mente ao trabalhar com endereços IPv4:

- Todos os endereços de host IPv4 têm 32 bits de comprimento.
- Uma parte do endereço representa a rede à qual o host pertence, e essa parte começa à esquerda.
- A parte restante é a parte do host, que identifica o host na rede.
- Há dois endereços reservados especiais em todas as redes que não podem ser atribuídas ao host:
    - O **endereço de rede**, que é o mais baixo no intervalo de endereços e representa a rede à qual pertencem todos os dispositivos.
    - O **endereço de transmissão**, que é o endereço mais alto no intervalo e pode ser usado para enviar uma mensagem a todos os dispositivos na rede de uma só vez.

Felizmente, existem atalhos que você pode usar para calcular esses endereços sem ter que converter para binários primeiro, mas examinar esses endereços no nível de bits deve ajudá-lo a entender como os dispositivos de rede os interpretam e também como o formato decimal com pontos é derivado.


## 23.1.6 Atividade - ANDing para determinar o endereço de rede

**Instruções:**

Usar a operação ANDing para determinar o endereço de rede (em formatos binário e decimal).

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed; word-wrap:break-word;"> <tr> <th>Campo</th> <th>Octeto 1</th> <th>Octeto 2</th> <th>Octeto 3</th> <th>Octeto 4</th> </tr> <tr> <td>Host Address</td> <td>172</td> <td>95</td> <td>106</td> <td>195</td> </tr> <tr> <td>Subnet Mask</td> <td>255</td> <td>255</td> <td>224</td> <td>0</td> </tr> <tr> <td>Host Address in binary</td> <td>10101100</td> <td>01011111</td> <td>01101010</td> <td>11000011</td> </tr> <tr> <td>Subnet Mask in binary</td> <td>11111111</td> <td>11111111</td> <td>11100000</td> <td>00000000</td> </tr> <tr> <td>Network Address in binary</td> <td>10101100</td> <td>01011111</td> <td>01100000</td> <td>00000000</td> </tr> <tr> <td>Network Address in decimal</td> <td>172</td> <td>95</td> <td>96</td> <td>0</td> </tr> </table>

