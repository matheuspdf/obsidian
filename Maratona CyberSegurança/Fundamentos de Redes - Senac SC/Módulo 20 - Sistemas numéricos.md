
# 20.0 Introdução

## 20.0.1 Webster - Por que devo fazer este módulo?

O Webster aqui de novo! Bob é bom nesse negócio de redes. Quando ele estava aprendendo redes, ele tinha que entender sistemas numéricos e você também! Você já usa o sistema decimal de base 10, que usa números inteiros de 0 a 9. Você conhece outros sistemas numéricos? Já vi base-12, base-60 e outras. Você sabe sobre o sistema binário que os computadores usam? O sistema binário usa apenas dois números inteiros, 0 e 1. Hosts, servidores e dispositivos de rede usam endereçamento binário. Há também algo chamado sistema de numeração hexadecimal. Ele é usado em rede para representar endereços IP Versão 6 e endereços Ethernet MAC.

Aproveite este módulo para aprender mais sobre esses sistemas numéricos e como convertê-los!

## 20.0.2 O Que Vou Aprender Neste Módulo?

**Titulo do Módulo:** Sistemas Numéricos

**Objetivo do Módulo:** Calcular números entre sistemas decimais, binários e hexadecimais.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Sistema de numeração binário|Calcular números entre sistemas decimal e binário.|
|Sistema de numeração hexadecimal|Calcular números entre sistemas decimal e hexadecimal.|

# 20.1 Sistema de numeração binário

## 20.1.1 Endereços Binários e IPv4

Os endereços IPv4 começam como binários, uma série de apenas 1s e 0s. Eles são difíceis de gerenciar, portanto, os administradores de rede devem convertê-los em decimal. Este tópico mostra algumas maneiras de fazer isso.

Binário é um sistema de numeração que consiste nos dígitos 0 e 1 chamados bits. Em contraste, o sistema de numeração decimal consiste em 10 dígitos que incluem 0 a 9.

É importante compreender o binário porque hosts, servidores e dispositivos de rede usam esse tipo de endereçamento. Especificamente, eles usam endereços IPv4 binários, como mostrado na figura, para se identificar.

![[Pasted image 20260614212432.png]]Cada endereço é composto por uma string de 32 bits dividida em quatro seções, chamadas octetos. Cada octeto tem 8 bits (ou 1 byte) separados por um ponto. Por exemplo, o PC1 na figura recebeu o endereço IPv4 11000000.10101000.00001010.00001010. Seu endereço de gateway padrão seria aquele da interface Ethernet Gigabit do R1, 11000000.10101000.00001010.00000001.

O binário funciona bem com hosts e dispositivos de rede. No entanto, é muito desafiador para os seres humanos trabalharem.

Para facilitar o uso pelas pessoas, os endereços IPv4 são geralmente expressos em notação decimal pontilhada. O PC1 recebe o endereço IPv4 192.168.10.10 e o endereço de gateway padrão é 192.168.10.1, conforme mostrado na figura.

![[Pasted image 20260614212446.png]]

Para ter um conhecimento sólido do endereçamento de rede, é preciso saber lidar com endereçamento binário e ter prática na conversão entre endereços IPv4 binários e decimais com pontos. Esta seção abordará como converter entre os sistemas de numeração de base dois (binário) e base 10 (decimal).

## 20.1.2 Vídeo - Convertendo entre sistemas de numeração binária e decimal

Neste vídeo vamos discutir conversão de binário para decimal. Mas antes de fazer isso, vamos dar uma olhada em notação posicional ou valores de lugar.

Tomando o número 2168 como exemplo, podemos ver que os valores de lugar são: o lugar do um, o lugar dos 10, o lugar dos 100, o lugar dos 1000, 10.000, 100.000 e milhões. Estes são os valores de lugar do sistema de número decimal de base 10. Temos o número dois no lugar dos 1000, então temos dois mil; temos um no lugar dos 100, por 100; temos seis no lugar dos 10, por 60; e temos oito no lugar do um, por oito. Efetivamente, temos dois mil, um cem, seis dezenas e oito unidades.

Quando falamos sobre os valores dos lugares no sistema de numeração decimal, estamos falando sobre as potências de 10. O lugar do um é 10 elevado a zero; o lugar dos 10 é 10 elevado a um; o lugar dos 100 é 10 elevado a dois, ou 10 vezes 10; o lugar dos 1000 é 10 elevado a três, ou 10 vezes 10 vezes 10, e assim por diante. Em formato longo, 2168 é: 2000 mais 100 mais 60 mais oito, totalizando 2168.

O sistema decimal é base 10. É baseado no fato de você ter potências de 10 e, mais importante, você tem 10 caracteres ou 10 numerais neste sistema de contagem, de zero até nove. Isso significa que em cada valor de lugar, você pode ter qualquer número do zero até o nove.

Se considerarmos o binário na mesma perspectiva que o decimal, o binário é um sistema de base 2. Há apenas dois caracteres, ou dois números: zero e um. Portanto, nos valores de lugar, só podemos ter zeros ou uns. Os valores de lugar vão de um (que é dois elevado a zero), para dois (dois elevado a um), quatro (dois elevado a dois), oito (dois elevado a três), 16 (dois elevado a quatro), 32, 64 e 128. A tabela é estendida para oito valores de posição porque oito bits é um agrupamento importante de números — oito bits formam um byte no processamento do computador.

Para escrever o número 168 em binário, basta encontrar os valores de lugar correspondentes e colocar um ou zero em cada posição:

- Preciso de 128 para chegar a 168? Sim. Coloco 1.
- Preciso de 64? 128 mais 64 seria 192, o que ultrapassa 168. Coloco 0.
- Preciso de 32? 128 mais 32 é 160. Sim. Coloco 1. Tenho agora 160.
- Preciso de 16? 160 mais 16 seria 176, o que ultrapassa 168. Coloco 0.
- Preciso de 8? 160 mais 8 é 168. Sim. Coloco 1.
- Os lugares do 4, do 2 e do 1 recebem zero.

Portanto, 168 em binário é **10101000**.

Para fazer o caminho oposto e converter o número binário 01101101 para decimal, basta identificar os valores de lugar onde há um 1 e somá-los:

- 1 no lugar do 64
- 1 no lugar do 32
- 1 no lugar do 8
- 1 no lugar do 4
- 1 no lugar do 1

64 mais 32 é 96, mais 8 é 104, mais 4 é 108, mais 1 é **109**.

Agora vamos ver um endereço IP completo em binário. Um endereço IP de 32 bits é composto por quatro octetos. Para converter o endereço IP binário em decimal, basta calcular cada octeto individualmente:

- Primeiro octeto: 11000000 → 128 mais 64 = **192**
- Segundo octeto: 10101000 → 128 mais 32 mais 8 = **168**
- Terceiro octeto: 00000001 → apenas o 1 no lugar do um = **1**
- Quarto octeto: 01100101 → 64 mais 32 mais 4 mais 1 = **101**

Portanto, a conversão deste endereço IP binário em decimal é **192.168.1.101**.

## 20.1.3 Verifique Sua Compreensão - Sistema de Número Binário

### Pergunta 1

Qual é o binário equivalente ao endereço IP 192.168.11.10?

- [ ] 11000000.11000000.00001011.00001010
- [x] 11000000.10101000.00001011.00001010
- [ ] 11000000.10101000.00001010.00001011
- [ ] 11000000.10101000.00001011.00010010

✅ RESPOSTA CORRETA: 11000000.10101000.00001011.00001010

> 192.168.11.10 é equivalente a 11000000.10101000.00001011.00001010

---

### Pergunta 2

Qual dos seguintes é o binário equivalente ao endereço IP 172.16.31.30?

- [ ] 11000000.00010000.00011111.00011110
- [ ] 10101000.00010000.00011111.00011110
- [ ] 10101100.00010000.00011110.00011110
- [x] 10101100.00010000.00011111.00011110

✅ RESPOSTA CORRETA: 10101100.00010000.00011111.00011110

> 172.16.31.30 é equivalente a 10101100.00010000.00011111.00011110


## 20.1.4 Atividade - Conversões binárias em decimais

**Instruções**

Esta atividade permite praticar a conversão de binário em decimal de 8 bits, tanto quanto necessário. Recomendamos que você trabalhe com esta ferramenta até que você seja capaz de fazer a conversão sem erros. Converta o número binário mostrado no octeto ao seu valor decimal.

**Digite a resposta decimal aqui.**

**Valor Decimal:** 220


**Digite a resposta decimal aqui.**

**Valor Decimal:** 220

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed; word-wrap:break-word;"> <tr> <td><strong>Base</strong></td> <td>2</td> <td>2</td> <td>2</td> <td>2</td> <td>2</td> <td>2</td> <td>2</td> <td>2</td> </tr> <tr> <td><strong>Expoente</strong></td> <td>7</td> <td>6</td> <td>5</td> <td>4</td> <td>3</td> <td>2</td> <td>1</td> <td>0</td> </tr> <tr> <td><strong>Posição</strong></td> <td>128</td> <td>64</td> <td>32</td> <td>16</td> <td>8</td> <td>4</td> <td>2</td> <td>1</td> </tr> <tr> <td><strong>Bit</strong></td> <td><strong>1</strong></td> <td><strong>1</strong></td> <td><strong>0</strong></td> <td><strong>1</strong></td> <td><strong>1</strong></td> <td><strong>1</strong></td> <td><strong>0</strong></td> <td><strong>0</strong></td> </tr> </table>

**Número Binário**


## 20.1.5 Conversão de Decimal para Binário

Também é preciso saber como converter um endereço IPv4 decimal com pontos para binário. Uma ferramenta útil é a tabela de valores posicionais binários.

**Clique em cada posição começando em 128 e trabalhe seu caminho da esquerda para a direita para a posição 1.**

![[Pasted image 20260614213336.png]]

---

**Posição 128**

O número decimal do octeto (n) é igual ou superior ao bit mais significativo (**128**)?

- Se não for, insira o binário **0** no valor posicional **128**.
- Em caso afirmativo, adicione um binário **1** ao valor posicional **128** e subtraia **128** do número decimal.

---

**Posição 64**

O número decimal do octeto (n) é igual ou superior ao próximo bit mais significativo (**64**)?

- Se não, insira o binário **0** no valor de posição **64**.
- Em caso afirmativo, adicione um binário **1** ao valor posicional **64** e subtraia **64** do número decimal.

---

**Posição 32**

O número decimal do octeto (n) é igual ou superior ao próximo bit mais significativo (**32**)?

- Se não, insira o binário **0** no valor de posição **32**.
- Em caso afirmativo, adicione um binário **1** ao valor posicional **32** e subtraia **32** do número decimal.

---

**Posição 16**

O número decimal do octeto (n) é igual ou superior ao próximo bit mais significativo (**16**)?

- Se não for, insira o binário **0** no valor posicional **16**.
- Em caso afirmativo, adicione um binário **1** ao valor posicional **16** e subtraia **16** do número decimal.

---

**Posição 8**

O número decimal do octeto (n) é igual ou superior ao próximo bit mais significativo (**8**)?

- Se não for, insira o binário **0** no valor posicional **8**.
- Em caso afirmativo, adicione um binário **1** ao valor posicional **8** e subtraia **8** do número decimal.

---

**Posição 4**

O número decimal do octeto (n) é igual ou superior ao próximo bit mais significativo (**4**)?

- Se não, insira o binário **0** no valor de posição **4**.
- Em caso afirmativo, adicione um binário **1** ao valor posicional **4** e subtraia **4** do número decimal.

---

**Posição 2**

O número decimal do octeto (n) é igual ou superior ao próximo bit mais significativo (**2**)?

- Se não, insira o binário **0** no valor de posição **2**.
- Em caso afirmativo, adicione um binário **1** ao valor posicional **2** e subtraia **4** do número decimal.

---

**Posição 1**

O número decimal do octeto (n) é igual ou superior ao último bit mais significativo (**1**)?

- Se não for, insira o binário **0** no valor posicional **1**.
- Em caso afirmativo, adicione um binário **1** ao valor posicional **1** e subtraia **1** do número decimal.


## 20.1.6 Exemplos de Conversão de Decimal para Binário

Para ajudar a entender o processo, considere o endereço IP **192.168.10.11**.

O primeiro número de octeto **192** é convertido em binário usando o processo de notação posicional explicado anteriormente.

É possível ignorar o processo de subtração com números decimais mais fáceis ou menores. Por exemplo, observe que é bastante fácil calcular o terceiro octeto convertido em um número binário sem realmente passar pelo processo de subtração (8 + 2 = 10). O valor binário do terceiro octeto é **00001010**.

O quarto octeto é 11 (8 + 2 + 1). O valor binário do quarto octeto é **00001011**.

A conversão entre binário e decimal pode parecer desafiadora a princípio, mas com a prática fica mais fácil.

Clique em cada etapa para ver a conversão do endereço IP de **192.168.10.11** em binário.

Dá sim, mas com limitações: as tabelas de bits ficam bem em Markdown simples, mas o diagrama de fluxo (setas, "Sim/Não", "Adicionar 0/1") não tem representação fiel em Markdown puro sem virar ilegível. A solução mais fiel e legível no Obsidian é HTML para as tabelas e texto descritivo para o fluxo. Veja como ficaria:

---

Clique em cada etapa para ver a conversão do endereço IP de **192.168.10.11** em binário.

---
**Etapa 1**

O primeiro número do octeto **192** é igual ou maior que o bit de ordem alta **128**?

- Sim, é, portanto, adicione **1** ao valor posicional de ordem superior para representar **128**.
- Subtraia **128** de **192** para produzir um resto de **64**.

**Examplo: 192**.168.10.11 → 192 >= 128 → Sim → Adicionar 1 → 192 − 128 = 64

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <th>Valor Posicional</th><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td> </tr> <tr> <th>Bit</th><td><strong>1</strong></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td> </tr> </table>

---

**Etapa 2**

O resto **64** é igual ou maior que o próximo bit de ordem alta **64**?

- É igual, portanto, adicione **1** ao próximo valor posicional de ordem superior.

**Examplo: 192**.168.10.11 → 64 >= 64 → Sim → Adicionar 1 → 64 − 64 = 0

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <th>Valor Posicional</th><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td> </tr> <tr> <th>Bit</th><td><strong>1</strong></td><td><strong>1</strong></td><td></td><td></td><td></td><td></td><td></td><td></td> </tr> </table>

---

**Etapa 3**

Como não há resto, insira o binário **0** nos valores posicionais restantes.

- O valor binário do primeiro octeto é **11000000**.

**Examplo: 192**.168.10.11

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <th>Valor Posicional</th><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td> </tr> <tr> <th>Bit</th><td><strong>1</strong></td><td><strong>1</strong></td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td> </tr> </table>

`11000000 . ___ . ___ . ___`

---

**Etapa 4**

O segundo octeto número **168** é igual ou maior que o bit de ordem superior **128**?

- Sim, é, portanto, adicione **1** ao valor posicional de ordem superior para representar **128**.
- Em seguida, subtraia **128** de **168** para produzir o valor **40** como resto.

**Exemplo: 192.168**.10.11 → 168 >= 128 → Sim → Adicionar 1 → 168 − 128 = 40

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <th>Valor Posicional</th><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td> </tr> <tr> <th>Bit</th><td><strong>1</strong></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td> </tr> </table>

---

**Etapa 5**

O resto **40** é igual ou maior que o próximo bit de ordem alta **64**?

- Não, não é, portanto, insira um binário **0** no valor posicional.

**Exemplo: 192.168**.10.11 → 40 >= 64 → Não → Adicionar 0

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <th>Valor Posicional</th><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td> </tr> <tr> <th>Bit</th><td><strong>1</strong></td><td>0</td><td></td><td></td><td></td><td></td><td></td><td></td> </tr> </table>

---

**Etapa 6**

O resto **40** é igual ou maior que o próximo bit de ordem alta **32**?

- Sim, é, portanto, adicione **1** ao valor posicional de ordem superior para representar **32**.
- Em seguida, subtraia **32** de **40** para produzir o valor **8** como resto.

**Exemplo: 192.168**.10.11 → 40 >= 32 → Sim → Adicionar 1 → 40 − 32 = 8

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <th>Valor Posicional</th><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td> </tr> <tr> <th>Bit</th><td><strong>1</strong></td><td>0</td><td><strong>1</strong></td><td></td><td></td><td></td><td></td><td></td> </tr> </table>

---

**Etapa 7**

O resto **8** é igual ou maior que o próximo bit de ordem alta **16**?

- Não, não é, portanto, insira um binário **0** no valor posicional.

**Exemplo: 192.168**.10.11 → 8 >= 16 → Não → Adicionar 0

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <th>Valor Posicional</th><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td> </tr> <tr> <th>Bit</th><td><strong>1</strong></td><td>0</td><td><strong>1</strong></td><td>0</td><td></td><td></td><td></td><td></td> </tr> </table>

---

**Etapa 8**

O resto **8** é igual ou maior que o próximo bit de ordem alta **8**?

- É igual, portanto, adicione **1** ao próximo valor posicional de ordem superior.

**Exemplo: 192.168**.10.11 → 8 >= 8 → Sim → Adicionar 1

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <th>Valor Posicional</th><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td> </tr> <tr> <th>Bit</th><td><strong>1</strong></td><td>0</td><td><strong>1</strong></td><td>0</td><td><strong>1</strong></td><td></td><td></td><td></td> </tr> </table>

---

**Etapa 9**

Como não há resto, insira o binário **0** nos valores posicionais restantes.

- O valor binário do segundo octeto é **10101000**.

**Exemplo: 192.168**.10.11

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <th>Valor Posicional</th><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td> </tr> <tr> <th>Bit</th><td><strong>1</strong></td><td>0</td><td><strong>1</strong></td><td>0</td><td><strong>1</strong></td><td>0</td><td>0</td><td>0</td> </tr> </table>

`11000000 . 10101000 . ___ . ___`

---

**Etapa 10**

O valor binário do terceiro octeto é **00001010**.

**Examplo: 192.168.10**.11

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <th>Valor Posicional</th><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td> </tr> <tr> <th>Bit</th><td>0</td><td>0</td><td>0</td><td>0</td><td><strong>1</strong></td><td>0</td><td><strong>1</strong></td><td>0</td> </tr> </table>

`11000000 . 10101000 . 00001010 . ___`

---

**Etapa 11**

O valor binário do quarto octeto é **00001011**.

**Examplo: 192.168.10.11**

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <th>Valor Posicional</th><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td> </tr> <tr> <th>Bit</th><td>0</td><td>0</td><td>0</td><td>0</td><td><strong>1</strong></td><td>0</td><td><strong>1</strong></td><td><strong>1</strong></td> </tr> </table>

`11000000 . 10101000 . 00001010 . 00001011`


## 20.1.7 Atividade - Conversões Decimal para Binário

Instruções

Esta atividade permite que você pratique a conversão decimal em valores binários de 8 bits. Recomendamos que você trabalhe com esta ferramenta até que você possa fazer uma conversão sem erros. Converta o número decimal mostrado na linha Valor Decimal em seus bits binários.

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <td><strong>Decimal Value</strong></td> <td colspan="8" style="text-align:center;"><strong>43</strong></td> </tr> <tr> <td><strong>Base</strong></td> <td>2</td><td>2</td><td>2</td><td>2</td><td>2</td><td>2</td><td>2</td><td>2</td> </tr> <tr> <td><strong>Exponent</strong></td> <td>7</td><td>6</td><td>5</td><td>4</td><td>3</td><td>2</td><td>1</td><td>0</td> </tr> <tr> <td><strong>Position</strong></td> <td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td> </tr> <tr> <td><strong>Bit</strong></td> <td>0</td><td>0</td><td>1</td><td>0</td><td>1</td><td>0</td><td>1</td><td>1</td> </tr> </table>


## 20.1.8 Atividade – Jogo Binário

Esta é uma maneira divertida de aprender números binários para redes.

**Link do jogo:** [https://learningnetwork.cisco.com/docs/DOC-1803](https://learningnetwork.cisco.com/s/binary-game)

Você precisará fazer login no cisco.com para usar este link. Será necessário criar uma conta se você ainda não tiver uma.

Há também uma variedade de jogos binários gratuitos para dispostivos mobiles. Pesquise "Binary Games" na sua loja de aplicativos.


## 20.1.9 Endereços IPv4

Como mencionado no início deste tópico, roteadores e computadores só entendem binários, enquanto humanos trabalham em decimal. É importante que você obtenha uma compreensão completa desses dois sistemas de numeração e como eles são usados na rede.

**Clique em cada botão para contrastar o endereço decimal com pontos e o endereço de 32 bits.**

**Endereço decimal com pontos**

192.168.10.10 é um endereço IP atribuído a um computador.

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <td style="text-align:center;"><strong>192</strong></td> <td style="text-align:center;">·</td> <td style="text-align:center;"><strong>168</strong></td> <td style="text-align:center;">·</td> <td style="text-align:center;"><strong>10</strong></td> <td style="text-align:center;">·</td> <td style="text-align:center;"><strong>10</strong></td> </tr> <tr> <td style="text-align:center;">11000000</td> <td style="text-align:center;"></td> <td style="text-align:center;">10101000</td> <td style="text-align:center;"></td> <td style="text-align:center;">00001010</td> <td style="text-align:center;"></td> <td style="text-align:center;">00001010</td> </tr> </table>

---

**Octetos**

Esse endereço é composto por quatro octetos diferentes.

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <td style="text-align:center;">192</td> <td style="text-align:center;">·</td> <td style="text-align:center;">168</td> <td style="text-align:center;">·</td> <td style="text-align:center;">10</td> <td style="text-align:center;">·</td> <td style="text-align:center;">10</td> </tr> <tr> <td style="text-align:center;"><strong>11000000</strong></td> <td style="text-align:center;"></td> <td style="text-align:center;"><strong>10101000</strong></td> <td style="text-align:center;"></td> <td style="text-align:center;"><strong>00001010</strong></td> <td style="text-align:center;"></td> <td style="text-align:center;"><strong>00001010</strong></td> </tr> </table>

---

**Endereço de 32 bits**

O computador armazena o endereço como o fluxo de dados inteiro de 32 bits.

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed;"> <tr> <td style="text-align:center;">192</td> <td style="text-align:center;">·</td> <td style="text-align:center;">168</td> <td style="text-align:center;">·</td> <td style="text-align:center;">10</td> <td style="text-align:center;">·</td> <td style="text-align:center;">10</td> </tr> <tr> <td style="text-align:center;"><strong>11000000</strong></td> <td style="text-align:center;"></td> <td style="text-align:center;"><strong>10101000</strong></td> <td style="text-align:center;"></td> <td style="text-align:center;"><strong>00001010</strong></td> <td style="text-align:center;"></td> <td style="text-align:center;"><strong>00001010</strong></td> </tr> </table>


# 20.2 Sistema de numeração hexadecimal

## 20.2.1 Endereços hexadecimais e IPv6

Agora você sabe como converter binário para decimal e decimal para binário. Você precisa dessa habilidade para entender o endereçamento IPv4 em sua rede. Mas é igualmente provável que esteja utilizando endereços IPv6 na sua rede. Para entender endereços IPv6, você deve ser capaz de converter hexadecimal para decimal e vice-versa.

Assim como decimal é um sistema numérico de base dez, hexadecimal é um sistema de base dezesseis. O sistema numérico de base dezesseis usa os dígitos 0 a 9 e as letras A a F. A figura mostra os valores decimais e hexadecimais equivalentes para os binários 0000 a 1111.

|Decimal|Binário|Hexadecimal|
|---|---|---|
|0|0000|0|
|1|0001|1|
|2|0010|2|
|3|0011|3|
|4|0100|4|
|5|0101|5|
|6|0110|6|
|7|0111|7|
|8|1000|8|
|9|1001|9|
|10|1010|A|
|11|1011|B|
|12|1100|C|
|13|1101|D|
|14|1110|E|
|15|1111|F|

Binário e hexadecimal funcionam bem juntos, porque é mais fácil expressar um valor como um único dígito de hexadecimal do que como quatro bits binários.

O sistema de numeração hexadecimal é usado em rede para representar endereços IP versão 6 e endereços MAC Ethernet.

Os endereços IPv6 têm 128 bits de comprimento e a cada 4 bits é representado por um único dígito hexadecimal; para um total de 32 valores hexadecimais. Os endereços IPv6 não diferenciam maiúsculas e minúsculas e podem ser escritos tanto em minúsculas como em maiúsculas.

Conforme mostrado na figura, o formato preferido para escrever um endereço IPv6 é x:x:x:x:x:x:x:x, com cada "x" consistindo em quatro valores hexadecimais. Quando falamos de 8 bits de um endereço IPv4, usamos o termo octeto. No IPv6, um _hexteto_ é o termo não oficial usado para se referir a um segmento de 16 bits ou quatro valores hexadecimais. Cada "x" é um único hextet, 16 bits ou quatro dígitos hexadecimais.

![[Pasted image 20260614215502.png]]

A topologia de exemplo na figura exibe endereços hexadecimais IPv6.

![[Pasted image 20260614215516.png]]


## 20.2.2 Vídeo — Conversão entre sistemas de numeração hexadecimal e decimal

Hexadecimal, ou hex para abreviação, é um sistema numérico de base 16. Ele usa 16 símbolos: os números de zero a nove, bem como as letras A a F. Baseia-se em potências de 16.

Se seguirmos o mesmo procedimento usado para converter binário em decimal, podemos escrever os valores de lugar ou notação posicional para o sistema de números hexadecimal também. Considerando os primeiros quatro valores de lugar: 16 elevado a zero é igual a 1; 16 elevado a um é igual a 16; 16 elevado a dois é igual a 256 (16 vezes 16); e 16 elevado a três é igual a 4.096 (16 vezes 16 vezes 16).

Os equivalentes decimais e binários de cada símbolo hexadecimal são os seguintes. O símbolo hexadecimal A é igual a 10 decimal, hex B é igual a 11 decimal, e assim por diante, até hexadecimal F que é igual a 15 decimal. Cada símbolo hexadecimal pode ser usado para representar um número binário de 4 bits. Dado que 8 bits é um grupo binário comum, podemos representar um número binário de 8 bits usando apenas dois símbolos hexadecimais.

**Exemplo 1: converter hexadecimal 2A em decimal**

Primeiro, escrevemos a notação posicional para as duas primeiras potências de 16 e inserimos os símbolos hexadecimais abaixo dos valores de lugar correspondentes: 2 abaixo de 16 e A abaixo de 1. Em seguida, multiplicamos cada símbolo hexadecimal pelo valor do lugar e somamos os resultados:

2 × 16 + A × 1 = 32 + 10 = **42 em decimal**

**Exemplo 2: converter 197 decimal para hexadecimal**

Multiplicar ou dividir por 16 nem sempre é fácil ao fazer conversões hexadecimais para decimais. Normalmente, é mais fácil converter o valor decimal para binário primeiro e depois converter esse número binário para hexadecimal.

Primeiro, convertemos 197 para um número binário de 8 bits, usando os primeiros oito valores de lugar do sistema de numeração binário:

- 197 >= 128 → colocar 1, restar 69
- 69 >= 64 → colocar 1, restar 5
- 5 < 32 → colocar 0
- 5 < 16 → colocar 0
- 5 < 8 → colocar 0
- 5 >= 4 → colocar 1, restar 1
- 1 < 2 → colocar 0
- 1 >= 1 → colocar 1, restar 0

Portanto, decimal 197 = **11000101** em binário.

Em seguida, dividimos o número binário de 8 bits em dois grupos de 4 bits e reescrevemos os valores de lugar binário (1, 2, 4, 8) acima de cada metade:

- Metade esquerda: **1100** → 8 + 4 = 12 decimal = **C** em hexadecimal
- Metade direita: **0101** → 4 + 1 = 5 decimal = **5** em hexadecimal

Portanto, 197 em decimal é **C5 em hexadecimal**, ou também pode ser escrito como **0xC5** — o prefixo 0x indica que o que se segue está escrito em hexadecimal.

**Exemplo 3: converter hexadecimal 9F para decimal via binário**

Primeiro, convertemos cada símbolo hexadecimal para seu equivalente binário:

- 9 hexadecimal = 9 decimal = **1001** em binário
- F hexadecimal = 15 decimal = **1111** em binário

Em seguida, combinamos os dois grupos em um número binário de 8 bits: **10011111**

Convertendo para decimal usando os oito valores de lugar:

128 + 16 + 8 + 4 + 2 + 1 = **159 em decimal**

Muitas vezes, existem várias maneiras de abordar a conversão entre sistemas numéricos. Você deve usar o que funciona melhor para você.

## 20.2.3 Verifique sua compreensão - Converter entre sistemas numéricos decimais para hexadecimais

### Pergunta 1

Qual é o equivalente hexadecimal de 202?

- [ ] B10
- [ ] BA
- [ ] C10
- [x] CA

✅ RESPOSTA CORRETA: CA

> O equivalente hexadecimal de 202 é CA.

---

### Pergunta 2

Qual é o equivalente hexadecimal de 254?

- [ ] EA
- [ ] ED
- [ ] FA
- [x] FE

✅ RESPOSTA CORRETA: FE

> O equivalente hexadecimal de 254 é FE.

---

### Pergunta 3

Qual é o equivalente decimal de A9?

- [ ] 168
- [x] 169
- [ ] 170
- [ ] 171

✅ RESPOSTA CORRETA: 169

> O equivalente decimal de A9 é 169.

---

### Pergunta 4

Qual dos seguintes é o equivalente decimal de 7D?

- [ ] 124
- [x] 125
- [ ] 126
- [ ] 127

✅ RESPOSTA CORRETA: 125

> O equivalente decimal de 7D é 125.


# 20.3 Resumo dos sistemas numéricos

## 20.3.1 O Que Eu Aprendi Neste Módulo?

### Sistemas de números binários

Binário é um sistema de numeração que consiste nos dígitos 0 e 1 chamados bits. Por outro lado, o sistema de numeração decimal consiste em 10 dígitos, compreendendo os dígitos de 0 a 9. Hosts, servidores e dispositivos de rede usam endereçamento binário. Especificamente, eles usam endereços IPv4 binários. Para facilitar o uso pelas pessoas, os endereços IPv4 são geralmente expressos em notação decimal com pontos.

Este sistema decimal usa as potências de dez, ou base 10. Por exemplo, o número 2.146 tem 2 na casa dos milhares, ou dois mil. Tem um 1 na casa das centenas, ou cem. Tem um 4 no lugar das dezenas, ou 40. Tem um 6 no lugar das unidades, ou seis.

O sistema binário é um sistema numérico de base 2. Cada valor local pode ter um 0 ou um 1. Uma ferramenta útil é a tabela de valores posicionais binários. É comum usar uma tabela com oito espaços reservados. 8 bits equivalem a um byte.

---

### Sistema de numeração hexadecimal

O sistema de numeração hexadecimal é usado em rede para representar endereços IP versão 6 e endereços MAC Ethernet. Esse sistema numérico de base dezesseis usa os dígitos de 0 a 9 e as letras A a F. Binário e hexadecimal funcionam bem juntos porque é mais fácil expressar um valor como um único dígito hexadecimal do que como quatro bits binários.

Os endereços IPv6 têm 128 bits de comprimento e a cada 4 bits é representado por um único dígito hexadecimal; para um total de 32 valores hexadecimais. Os endereços IPv6 não diferenciam maiúsculas e minúsculas e podem ser escritos tanto em minúsculas como em maiúsculas.

---

## 20.3.2 Webster - Questões para Reflexão

Eu não esperava fazer matemática no meio do meu curso de rede, mas fiquei surpreso com o quão divertido é converter números decimais em seus equivalentes binários e hexadecimais. Eu tenho uma melhor compreensão de por que os endereços IP são representados da maneira que os vemos. Antes de fazer este módulo, o que você sabia sobre sistemas de numeração binários e hexadecimais? Dê uma olhada no endereço MAC da NIC do seu computador. O que você reconhece sobre esse endereço que talvez não tenha antes?