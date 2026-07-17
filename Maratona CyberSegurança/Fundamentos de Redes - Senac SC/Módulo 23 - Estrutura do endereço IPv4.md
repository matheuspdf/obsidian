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
![[23.1.5.mp4#subtitle=anexos/23.1.5.vtt]]
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


## 23.1.7 Verifique sua compreensão - Estrutura do endereço IPv4

**Verifique sua compreensão sobre Estrutura do endereço IPv4 escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

O Host-A tem o endereço IPv4 e a máscara de sub-rede 10.5.4.100 255.255.255.0. Qual é o endereço de rede do Host-A?

- [ ] 10.0.0.0
- [ ] 10.5.0.0
- [x] 10.5.4.0
- [ ] 10.5.4.100

✅ RESPOSTA CORRETA: 10.5.4.0

> O endereço de rede para 10.5.4.100 com uma máscara de sub-rede de 255.255.255.0 é 10.5.4.0.

---

### Pergunta 2

O Host-A tem endereço IPv4 e máscara de sub-rede 172.16.4.100 255.255.0.0. Qual é o endereço de rede do Host-A?

- [ ] 172.0.0.0
- [x] 172.16.0.0
- [ ] 172.16.4.0
- [ ] 172.16.4.100

✅ RESPOSTA CORRETA: 172.16.0.0

> O endereço de rede para 172.16.4.100 com uma máscara de sub-rede de 255.255.0.0 é 172.16.0.0.

---

### Pergunta 3

O Host-A tem o endereço IPv4 e a máscara de sub-rede 10.5.4.100 255.255.255.0. Quais dos seguintes endereços IPv4 estariam na mesma rede que o Host-A? (Escolha todas que se aplicam)

- [x] 10.5.4.1
- [ ] 10.5.0.1
- [x] 10.5.4.99
- [ ] 10.0.0.98
- [ ] 10.5.100.4

✅ RESPOSTA CORRETA: 10.5.4.1, 10.5.4.99

> O Host A está na rede 10.5.4.0. Portanto, os dispositivos com os endereços IPv4 10.5.4.1 e 10.5.4.99 estão na mesma rede.

---

### Pergunta 4

O Host-A tem endereço IPv4 e máscara de sub-rede 172.16.4.100 255.255.0.0. Quais dos seguintes endereços IPv4 estariam na mesma rede que o Host-A? (Escolha todas que se aplicam)

- [x] 172.16.4.99
- [x] 172.16.0.1
- [ ] 172.17.4.99
- [ ] 172.17.4.1
- [ ] 172.18.4.1

✅ RESPOSTA CORRETA: 172.16.4.99, 172.16.0.1

> O host A está na rede 172.16.0.0. Portanto, os dispositivos com os endereços IPv4 172.16.4.99 e 172.16.0.1 estão na mesma rede.

---

### Pergunta 5

O Host-A tem o endereço IPv4 e a máscara de sub-rede 192.168.1.50 255.255.255.0. Quais dos seguintes endereços IPv4 estariam na mesma rede que o Host-A? (Escolha todas que se aplicam)

- [ ] 192.168.0.1
- [ ] 192.168.0.100
- [x] 192.168.1.1
- [x] 192.168.1.100
- [ ] 192.168.2.1

✅ RESPOSTA CORRETA: 192.168.1.1, 192.168.1.100

> O Host A está na rede 192.168.1.0. Portanto, os dispositivos com os endereços IPv4 192.168.1.1 e 192.168.1.100 estão na mesma rede.


# 23.2 Resumo do Estrutura do endereço IPv4

## 23.2.1 O que eu aprendi neste módulo?

### Estrutura de endereço IPv4

Um endereço IPv4 é um endereço hierárquico de 32 bits composto por uma parte de rede e uma parte de host. Ao determinar a parte da rede versus a parte do host, você deve observar o fluxo de 32 bits. Os bits na parte de rede do endereço devem ser iguais em todos os dispositivos que residem na mesma rede. Os bits na parte de host do endereço devem ser exclusivos para identificar um host específico dentro de uma rede. Se dois hosts tiverem o mesmo padrão de bits na parte de rede especificada do fluxo de 32 bits, esses dois hosts residirão na mesma rede.

A máscara de sub-rede IPv4 é usada para diferenciar a parte da rede da parte do host de um endereço IPv4. Quando um endereço IPv4 é atribuído a um dispositivo, a máscara de sub-rede é usada para determinar o endereço de rede do dispositivo. O endereço de rede representa todos os dispositivos na mesma rede.

Um método alternativo de identificar uma máscara de sub-rede, um método chamado comprimento do prefixo. O comprimento do prefixo é o número de bits definido como 1 na máscara de sub-rede. Está escrito em "notação de barra", que é anotada por uma barra (/) seguida pelo número de bits definido como 1. Por exemplo, `192.168.10.10 255.255.255.0` seria gravado como `192.168.10.10/24`.

A operação AND é usada para determinar o endereço de rede. O AND lógico é a comparação de dois bits. Observe como somente 1 AND 1 produz um 1. Qualquer outra combinação resulta em um 0.

- 1 E 1 = 1
- 0 E 1 = 0
- 1 E 0 = 0
- 0 E 0 = 0

Para identificar o endereço de rede de um host IPv4, é feito um AND lógico, bit a bit, entre o endereço IPv4 e a máscara de sub-rede. Quando se usa AND entre o endereço e a máscara de sub-rede, o resultado é o endereço de rede.

## 23.2.2 Webster - Perguntas para reflexão

Antes de estudar este módulo, eu estava me sentindo como Marcy e Vincent. Eu não tinha uma boa noção de como os números no endereço IPv4 eram importantes. Você conhecia o endereço hierárquico de 32 bits que é composto por uma porção de rede e uma porção de host? Você consegue explorar isso em sua própria rede? E quem sabia sobre ANDing e a máscara de sub-rede?

Estou me sentindo um pouco mais como Bob depois deste módulo e espero que você também esteja.

## 23.2.3 Questionário sobre Estrutura do Endereço IPv4

## Pergunta 1

**Qual afirmação descreve o endereçamento IPv4?**

- [ ] Os roteadores usam o endereço IP completo de 32 bits para determinar a localização de cada host individual.
- [ ] Um endereço IPv4 contém duas partes: uma parte de rede e uma parte de sub-rede.
- [x] A parte de rede de um endereço IP de destino é obtida executando uma operação AND entre um endereço IP do host e uma máscara de sub-rede.
- [ ] Dois hosts com a mesma máscara de sub-rede estão na mesma rede.

**Resposta: A parte de rede de um endereço IP de destino é obtida executando uma operação AND entre um endereço IP do host e uma máscara de sub-rede.**

---

## Pergunta 2

**Qual declaração descreve uma finalidade da configuração da máscara de sub-rede para um host?**

- [ ] É usado para descrever o tipo de sub-rede.
- [ ] É usado para identificar o gateway padrão.
- [x] É usado para determinar a qual rede o host está conectado.
- [ ] É usado para determinar o número máximo de bits em um pacote que pode ser colocado em uma rede específica.

**Resposta: É usado para determinar a qual rede o host está conectado.**

---

## Pergunta 3

**Quantos octetos existem em um endereço IPv4?**

- [ ] 8
- [ ] 16
- [ ] 32
- [x] 4

**Resposta: 4**

---

## Pergunta 4

**Qual faixa completa de valores decimais válida em um octeto de um endereço IPv4?**

- [ ] 0 a 31
- [ ] 1 a 64
- [ ] 0 a 128
- [x] 0 a 255
- [ ] 1 a 256

**Resposta: 0 a 255**

---

## Pergunta 5

**Para qual finalidade os endereços IPv4 são utilizados?**

- [ ] Um endereço IPv4 é usado para identificar o número de redes IP disponíveis.
- [x] Um endereço IPv4 é usado para identificar exclusivamente um dispositivo em uma rede IP.
- [ ] Um endereço IPv4 é gravado na placa de rede para identificar exclusivamente um dispositivo.
- [ ] Um endereço IPv4 é usado para identificar exclusivamente a aplicação que solicitou as informações de um dispositivo remoto.

**Resposta: Um endereço IPv4 é usado para identificar exclusivamente um dispositivo em uma rede IP.**

---

## Pergunta 6

**Qual é a notação de comprimento do prefixo para a máscara de sub-rede 255.255.255.224?**

- [ ] /25
- [ ] /28
- [ ] /26
- [x] /27

**Resposta: /27**

---

## Pergunta 7

**Quais duas partes são componentes de um endereço IPv4? (Escolha duas.)**

- [ ] Parte física
- [ ] Parte de broadcast
- [x] Parte de host
- [x] Parte da rede
- [ ] Parte de sub-rede
- [ ] Parte lógica

**Resposta: Parte de host e Parte da rede**

---

## Pergunta 8

**O que é obtido ao ANDing do endereço 192.168.65.3/18 com sua máscara de sub-rede?**

- [ ] 192.168.0.0
- [ ] 192.168.32.0
- [ ] 192.168.16.0
- [x] 192.168.64.0

**Resposta: 192.168.64.0**

---

## Pergunta 9

**O que os dispositivos na mesma sub-rede IPv4 têm em comum?**

- [ ] Todos eles têm uma máscara de sub-rede de /8, /16 ou /24.
- [ ] Todos eles têm o mesmo último octeto em seus endereços IPv4.
- [x] Todos eles usam o mesmo gateway padrão.
- [ ] Todos eles têm o mesmo número nos três primeiros octetos de seus endereços IPv4.

**Resposta: Todos eles usam o mesmo gateway padrão.**

---

## Pergunta 10

**Quantos endereços exclusivos estão disponíveis para atribuição a hosts na rede de 10.100.16.0 com máscara de sub-rede 255.255.252.0?**

- [ ] 510
- [x] 1022
- [ ] 4094
- [ ] 254

**Resposta: 1022**

---

## Pergunta 11

**Qual é um endereço de gateway padrão válido para um host configurado com o endereço IP 10.25.1.110 e uma máscara de sub-rede de 255.255.255.192?**

- [x] 10.25.1.65
- [ ] 10.25.1.127
- [ ] 10.25.1.1
- [ ] 10.0.0.1

**Resposta: 10.25.1.65**

---

## Pergunta 12

**Quando o endereçamento IPv4 é configurado manualmente em um servidor web, que propriedade da configuração IPv4 identifica as partes de host e de rede de um endereço IPv4?**

- [x] Máscara de sub-rede
- [ ] Endereço do servidor DNS
- [ ] Endereço do servidor DHCP
- [ ] Gateway padrão

**Resposta: Máscara de sub-rede**

