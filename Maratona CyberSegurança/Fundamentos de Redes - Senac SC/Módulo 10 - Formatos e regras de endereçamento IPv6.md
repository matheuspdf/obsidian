# 10.0 Introdução

## 10.0.1 Webster - Por que devo fazer este módulo?

Kishori encontra Rina para almoçar novamente. Kishori está animada para contar a Rina tudo que ela aprendeu sobre endereços IPv4. Rina a parabeniza e pergunta se ela já ouviu falar sobre IPv6. IPv6? Kishori não tem ideia do que é IPv6! E você? Deixe-me ajudá-lo com isso. Vamos começar com este módulo!


## 10.0.2 O que vou aprender neste módulo?

**Título do Módulo:** Formatos e regras de endereçamento IPv6

**Objetivo do Módulo:** Explicar os recursos do endereçamento IPv6.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Problemas de IPv4|Explicar a necessidade do endereçamento IPv6.|
|Endereçamento IPv6|Explicar como representar endereços IPv6.|

# 10.1 Problemas do IPv4

## 10.1.1 A Necessidade do IPv6

RIR IPv4 Exhaustion Dates

Você já sabe que o IPv4 está ficando sem endereços. É por isso que você precisa aprender sobre IPv6.  
  
Projetado para ser o sucessor do IPv4, O IPv6 tem um espaço de endereço maior, de 128 bits, fornecendo 340 undecilhão (ou seja, 340 seguidos por 36 zeros) de endereços possíveis. No entanto, o IPv6 é mais do que, apenas, endereços maiores.  
  
Quando a IETF começou o desenvolvimento de um sucessor para o IPv4, aproveitou para corrigir as limitações do IPv4 e incluir aprimoramentos. Um exemplo é o ICMPv6 (Internet Control Message Protocol versão 6), que inclui a resolução de endereços e a configuração automática de endereços, não encontradas no ICMP para IPv4 (ICMPv4).  
  
O esgotamento de endereços IPv4 tem sido o fator motivador para a migração para o IPv6. À medida que África, Ásia e outras áreas do mundo ficarem mais conectadas à Internet, não haverá endereços IPv4 suficientes para acomodar esse crescimento. Conforme mostra a figura, quatro dos cinco RIRs estão com endereços IPv4 esgotados.

### **Datas de Esgotamento do IPv4 por RIR**

![[Pasted image 20260530233413.png]]

O IPv4 tem um máximo teórico de 4,3 bilhões de endereços. Os endereços privados em combinação com o Network Address Translation (NAT - tradução de endereços de rede) têm sido fundamentais para retardar o esgotamento do espaço de endereços IPv4. No entanto, o NAT é problemático para muitos aplicativos, cria latência e possui limitações que impedem severamente as comunicações ponto a ponto.

Com o número cada vez maior de dispositivos móveis, os provedores móveis têm liderado o caminho para a transição para o IPv6. Os dois principais provedores de telefonia móvel nos Estados Unidos relatam que mais de 90% de seu tráfego usa IPv6.

A maioria dos principais ISPs e provedores de conteúdo, como YouTube, Facebook e NetFlix, também fizeram a transição. Muitas empresas como Microsoft, Facebook e LinkedIn estão fazendo transição para IPv6 somente internamente. Em 2018, o ISP Comcast de banda larga relatou a implantação de mais de 65% e a British Sky Broadcasting de mais de 86%.

**Internet das Coisas**

A internet de hoje é significativamente diferente da internet das últimas décadas. A internet de hoje é mais do que e-mail, páginas da web e transferências de arquivos entre computadores. A Internet em evolução está se tornando a Internet das Coisas (IoT - Internet of Things). Computadores, tablets e smartphones não serão mais os únicos dispositivos que acessam a internet Os dispositivos equipados com sensor e prontos para a Internet do amanhã incluirão tudo, desde automóveis e dispositivos biomédicos, até eletrodomésticos e ecossistemas naturais.

Com uma população cada vez maior na Internet, espaço de endereços IPv4 limitado, problemas com NAT e a Internet das Coisas, chegou o momento de iniciar a transição para o IPv6.

## 10.1.2 Coexistência entre IPv4 e IPv6

Não há uma data exata para migrar para o IPv6. Tanto o IPv4 como o IPv6 coexistirão no futuro próximo e a transição levará vários anos. A IETF criou vários protocolos e ferramentas para ajudar os administradores de rede a migrarem as redes para IPv6. As técnicas de migração podem ser divididas em três categorias:

**Clique em cada botão abaixo para obter mais informações.**

### Pilha Dupla

A pilha dupla permite que IPv4 e IPv6 coexistam no mesmo segmento de rede. Os dispositivos de pilha dupla executam os protocolos IPv4 e IPv6 simultaneamente. Conhecido como IPv6 nativo, isso significa que a rede do cliente tem uma conexão IPv6 com seu ISP e é capaz de acessar o conteúdo encontrado na internet através de IPv6.
![[Pasted image 20260530233456.png]]


### Tunelamento

Tunelamento é um método de transporte de pacote IPv6 através de uma rede IPv4. O pacote IPv6 é encapsulado dentro de um pacote IPv4, de forma semelhante a outros tipos de dados.

A topologia de rede física mostra dois PCs IPv6 somente conectados a roteadores de pilha dupla que estão conectados por um túnel através de uma nuvem somente IPv4.

![[Pasted image 20260530233517.png]]

### Conversão

O NAT64 (Network Address Translation 64) permite que os dispositivos habilitados para IPv6 se comuniquem com os dispositivos habilitados para IPv4 usando uma técnica de conversão semelhante ao NAT IPv4. Um pacote IPv6 é traduzido para um pacote IPv4 e um pacote IPv4 é traduzido para um pacote IPv6.

![[Pasted image 20260530233533.png]]

**Observação:** O tunelamento e a tradução são para transição para IPv6 nativo e só devem ser usados quando necessário. O objetivo deve ser as comunicações IPv6 nativas da origem até o destino.

## 10.1.3 Verifique o seu entendimento — Problemas com IPv4

### Pergunta 1

Qual é o fator motivador mais importante para migrar para o IPv6?

- [x] Esgotamento do espaço de endereços IPv4
- [ ] melhor segurança com IPv6
- [ ] Melhor desempenho
- [ ] Endereços IPv6 que são mais fáceis de trabalhar com

✅ RESPOSTA CORRETA: Esgotamento do espaço de endereços IPv4

> O driver principal ou fator mais importante para o IPv6 é o esgotamento do espaço de endereços IPv4.

---

### Pergunta 2

Verdadeiro ou Falso: 4 em cada 5 RIRs não têm mais endereços IPv4 suficientes para alocar regularmente aos clientes.

- [x] Falso
- [ ] Verdadeiro

✅ RESPOSTA CORRETA: Falso

> A resposta correta é Falso. Quatro dos cinco RIRs, ARIN, APNIC, LACNIC e RIPENCC esgotaram seus pools de endereços IPv4.

---

### Pergunta 3

Quais das seguintes técnicas usam conectividade IPv6 nativa?

- [x] pilha dupla
- [ ] tunelamento
- [ ] tradução
- [ ] todos os itens acima

✅ RESPOSTA CORRETA: pilha dupla

> Somente a pilha dupla usa conectividade IPv6 nativa.

# 10.2 Endereçamento IPv6

## 10.2.1 Sistema de numeração hexadecimal

Antes de abordar o endereçamento IPv6, é importante que você saiba que os endereços IPv6 são representados usando números hexadecimais. Este sistema numérico, de base dezesseis, usa os dígitos de 0 a 9 e as letras de A a F:

**0 1 2 3 4 5 6 7 8 9 A B C D E F**

Nos endereços IPv6, esses 16 dígitos são representados por hextetos (discutidos a seguir), permitindo representar esses endereços enormes em um formato muito mais legível.


## 10.2.2 Formatos do endereçamento IPv6

### Segmentos ou Hextets de 16 bits

O primeiro passo para aprender sobre IPv6 em redes é entender a forma como um endereço IPv6 é escrito e formatado. Os endereços IPv6 são muito maiores do que os endereços IPv4, razão pela qual é improvável que fiquemos sem eles.

Os endereços IPv6 têm 128 bits e são escritos como uma sequência de valores hexadecimais. Cada 4 bits são representados por um único dígito hexadecimal, totalizando 32 valores hexadecimais, como mostra a Figura 1. Os endereços IPv6 não diferenciam maiúsculas e minúsculas e podem ser escritos tanto em minúsculas como em maiúsculas.

### **Segmentos de 16 bits ou Hextets**

![[Pasted image 20260530233826.png]]

**Formato Preferencial**

Como mostrado na Figura 1, o formato preferencial para escrever um endereço IPv6 é x: x: x: x: x: x: x: x, com cada “x” consistindo em quatro algarismos hexadecimais. O termo octeto refere-se aos oito bits em um endereço IPv4. No IPv6, um hexteto é o termo não oficial usado para se referir a um segmento de 16 bits ou quatro algarismos hexadecimais. Cada “x” é um único hexteto de 16 bits ou quatro dígitos hexadecimais.

Formato preferencial significa que o endereço IPv6 é gravado usando todos os 32 dígitos hexadecimais. Isso não significa necessariamente que é o método ideal para representar o endereço IPv6. Existem duas regras que ajudam a reduzir o número de dígitos necessários para representar um endereço IPv6.

A Figura 3 tem exemplos de endereços IPv6 no formato preferencial.

```
2001 : 0db8 : 0000 : 1111 : 0000 : 0000 : 0000: 0200

2001 : 0db8 : 0000 : 00a3 : abcd : 0000 : 0000: 1234

2001 : 0db8 : 000a : 0001 : c012 : 9aff : fe9a: 19ac

2001 : 0db8 : aaaa : 0001 : 0000 : 0000 : 0000: 0000

fe80 : 0000 : 0000 : 0000 : 0123 : 4567 : 89ab: cdef

fe80 : 0000 : 0000 : 0000 : 0000 : 0000 : 0000: 0001

fe80 : 0000 : 0000 : 0000 : c012 : 9aff : fe9a: 19ac

fe80 : 0000 : 0000 : 0000 : 0123 : 4567 : 89ab: cdef

0000 : 0000 : 0000 : 0000 : 0000 : 0000 : 0000: 0001

0000 : 0000 : 0000 : 0000 : 0000 : 0000 : 0000: 0001
```

## 10.2.3 Vídeo - Regras de Formatação IPv6

Os endereços IPv6 têm 128 bits de comprimento e são escritos como uma string de valores hexadecimais. Os endereços IPv6 não diferenciam maiúsculas de minúsculas e podem ser escritos em letras minúsculas ou maiúsculas.

![[Pasted image 20260530234521.png]]
Cada quatro bits é representado por um único dígito hexadecimal, para um total de 32 valores hexadecimais. Por exemplo, o dígito hexadecimal dois é o equivalente em binário aos quatro bits 0010 0010. Conjuntos de quatro dígitos hexadecimais são separados por dois pontos. Cada dígito hexadecimal tem quatro bits, o que facilita a representação do endereço IPv6 de 128 bits.

Cada conjunto de quatro segmentos hexadecimais às vezes é chamado de hexteto. Quando escrito com todos os 32 dígitos hexadecimais, este é conhecido como formato preferencial, o que não significa que seja sempre a forma preferida de exibir o endereço.

Há duas regras que podem ser usadas para reduzir o número de dígitos hexadecimais usado para representar um endereço IPv6.

### Regra 1 — Omitir zeros à esquerda

![[Pasted image 20260530234601.png]]
A primeira regra para ajudar a reduzir a notação de endereços IPv6: omitir qualquer 0s (zeros) à esquerda em qualquer hexteto. Apenas os zeros à esquerda são omitidos, não os zeros à direita. Caso contrário, não saberíamos quais zeros foram omitidos — zeros à esquerda, zeros à direita ou ambos. Usando esta primeira regra, sabemos que apenas zeros à esquerda são omitidos.

### Regra 2 — Dois pontos duplos (`::`)

![[Pasted image 20260530234634.png]]

A segunda regra pode ser usada para reduzir ainda mais a representação de um endereço IPv6. Qualquer sequência única contígua de um ou mais segmentos de 16 bits que consistem todos em zeros podem ser representados com dois pontos duplos (`::`)

Para aplicar as duas regras:

1. Primeiro aplica-se a Regra 1, omitindo os zeros à esquerda.
2. Em seguida aplica-se a Regra 2, substituindo hextetos contíguos zerados por `::`.

Observe que dois pontos duplos podem ocorrer no final de um endereço. Todos os zeros no final de um endereço IPv6 estão associados a um endereço de Rede IPv6.

![[Pasted image 20260530234709.png]]

**Os dois pontos duplos (`::`) podem ser usados apenas uma vez em um endereço IPv6.** Caso contrário, haveria mais de um possível endereço resultante.

![[Pasted image 20260530234735.png]]

Se um endereço tiver mais de uma sequência contígua de hextetos zerados, a melhor prática é usar dois pontos duplos na sequência mais longa e aplicar os zeros iniciais omitidos na sequência mais curta. Se as cadeias de caracteres forem iguais, a primeira cadeia deve usar dois pontos duplos (`::`) . Mas, normalmente, tudo se resume à preferência pessoal.

## 10.2.4 Regra 1 - Omitir zeros à esquerda

A primeira regra para ajudar a reduzir a notação de endereços IPv6 é omitir os 0s (zeros) à esquerda de qualquer seção de 16 bits ou hexteto. Aqui estão quatro exemplos de maneiras de omitir zeros à esquerda:

- `01AB` pode ser representado como `1AB`
- `09f0` pode ser representado como `9f0`
- `0a00` pode ser representado como `a00`
- `00ab` pode ser representado como `ab`

Essa regra se aplica somente aos 0s à esquerda, e NÃO aos 0s à direita. Caso contrário, o endereço ficaria ambíguo. Por exemplo, o hexteto "abc" poderia ser "0abc" ou "abc0", mas essas duas representações não se referem ao mesmo valor.

---

| Tipo | Formato |
|---|---|
| Preferencial | 2001 : 0db8 : 0000 : 1111 : 0000 : 0000 : 0000 : 0200 |
| Sem 0s à esquerda | 2001 : db8 : 0 : 1111 : 0 : 0 : 0 : 200 |
| Preferencial | 2001 : 0db8 : 0000 : 00a3 : ab00 : 0ab0 : 00ab : 1234 |
| Sem 0s à esquerda | 2001 : db8 : 0 : a3 : ab00 : ab0 : ab : 1234 |
| Preferencial | 2001 : 0db8 : 000a : 0001 : c012 : 90ff : fe90 : 0001 |
| Sem 0s à esquerda | 2001 : db8 : a : 1 : c012 : 90ff : fe90 : 1 |
| Preferencial | 2001 : 0db8 : aaaa : 0001 : 0000 : 0000 : 0000 : 0000 |
| Sem 0s à esquerda | 2001 : db8 : aaaa : 1 : 0 : 0 : 0 : 0 |
| Preferencial | fe80 : 0000 : 0000 : 0000 : 0123 : 4567 : 89ab : cdef |
| Sem 0s à esquerda | fe80 : 0 : 0 : 0 : 123 : 4567 : 89ab : cdef |
| Preferencial | fe80 : 0000 : 0000 : 0000 : 0000 : 0000 : 0000 : 0001 |
| Sem 0s à esquerda | fe80 : 0 : 0 : 0 : 0 : 0 : 0 : 1 |
| Preferencial | 0000 : 0000 : 0000 : 0000 : 0000 : 0000 : 0000 : 0001 |
| Sem 0s à esquerda | 0 : 0 : 0 : 0 : 0 : 0 : 0 : 1 |
| Preferencial | 0000 : 0000 : 0000 : 0000 : 0000 : 0000 : 0000 : 0000 |
| Sem 0s à esquerda | 0 : 0 : 0 : 0 : 0 : 0 : 0 : 0 |

## 10.2.5 Regra 2- Dois pontos duplos

A segunda regra para ajudar a reduzir a notação de endereços IPv6 é que dois pontos duplos (::) podem substituir qualquer string única e contígua de um ou mais hextetos de 16 bits consistindo em zeros. Por exemplo, 2001:db8:cafe: 1:0:0:0:1 (0s iniciais omitidos) poderia ser representado como 2001:db8:cafe:1::1. Os dois-pontos duplos (::) são usados no lugar dos três hextetos compostos por zeros (0:0:0).

Os dois-pontos duplos (::) só podem ser usados uma vez dentro de um endereço, caso contrário, haveria mais de um endereço resultante possível. Quando associada à técnica de omissão dos 0s à esquerda, a notação do endereço IPv6 pode ficar bastante reduzida. É o chamado formato compactado.

Aqui está um exemplo do uso incorreto dos dois pontos duplos: 2001:db8::abcd::1234.

Os dois pontos duplos são usados duas vezes no exemplo acima. Aqui estão as possíveis expansões possíveis deste endereço de formato compactado incorretamente:

- 2001:db8::abcd:0000:0000:1234
- 2001:db8::abcd:0000:0000:0000:1234
- 2001:db8:0000:abcd::1234
- 2001:db8:0000:0000:abcd::1234

Se um endereço tiver mais de uma string contígua de hextetos com zero, a melhor prática é usar dois pontos duplos (::) na string mais longa. Se as strings forem iguais, a primeira string deve usar dois pontos duplos (::).

---

|Tipo|Formato|
|---|---|
|Preferencial|2001 : 0db8 : 0000 : 1111 : 0000 : 0000 : 0000 : 0200|
|Compactado/espaços|2001 : db8 : 0 : 1111 : : 200|
|Compactado|2001:db8:0:1111::200|
|Preferencial|2001 : 0db8 : 0000 : 0000 : ab00 : 0000 : 0000 : 0000|
|Compactado/espaços|2001 : db8 : 0 : 0 : ab00 ::|
|Compactado|2001:db8:0:0:ab00::|
|Preferencial|2001 : 0db8 : aaaa : 0001 : 0000 : 0000 : 0000 : 0000|
|Compactado/espaços|2001 : db8 : aaaa : 1 ::|
|Compactado|2001:db8:aaaa:1::|
|Preferencial|fe80 : 0000 : 0000 : 0000 : 0123 : 4567 : 89ab : cdef|
|Compactado/espaços|fe80 :: 123 : 4567 : 89ab : cdef|
|Compactado|fe80::123:4567:89ab:cdef|
|Preferencial|fe80 : 0000 : 0000 : 0000 : 0000 : 0000 : 0000 : 0001|
|Compactado/espaços|fe80 :: 1|
|Compactado|fe80::1|
|Preferencial|0000 : 0000 : 0000 : 0000 : 0000 : 0000 : 0000 : 0001|
|Compactado/espaços|:: 1|
|Compactado|::1|
|Preferencial|0000 : 0000 : 0000 : 0000 : 0000 : 0000 : 0000 : 0000|
|Compactado/espaços|::|
|Compactado|::|

## 10.2.6 Atividade - Representações do Endereço IPv6

**Instruções:**

Converta os endereços IPv6 em formatos curtos e compactos (omita os zeros à esquerda). Insira letras em minúsculas. Clique em Avançar para seguir na atividade para o próximo endereço.

| | | | | | | | | |
|---|---|---|---|---|---|---|---|---|
| **Formato preferencial** | 2013 | ef12 | 0123 | 4567 | 89ab | cdef | 0000 | 0001 |
| **Omitir zeros à esquerda** | 2013 | ef12 | 123 | 4567 | 89ab | cdef | 0 | 1 |
| **Formato compactado** | 2013:ef12:123:4567:89ab:cdef::1 | | | | | | | |

---

| | | | | | | | | |
|---|---|---|---|---|---|---|---|---|
| **Formato preferencial** | 2001 | 0db8 | 2233 | 4455 | 6677 | 0000 | 0000 | 0101 |
| **Omitir zeros à esquerda** | 2001 | db8 | 2233 | 4455 | 6677 | 0 | 0 | 101 |
| **Formato compactado** | 2001:db8:2233:4455:6677::101 | | | | | | | |

---

|                             |                              |      |      |      |      |      |      |      |
| --------------------------- | ---------------------------- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| **Formato preferencial**    | 2001                         | 0db8 | 2233 | 4455 | 6677 | 0000 | 0000 | 0101 |
| **Omitir zeros à esquerda** | 2001                         | db8  | 2233 | 4455 | 6677 | 0    | 0    | 101  |
| **Formato compactado**      | 2001:db8:2233:4455:6677::101 |      |      |      |      |      |      |      |


# 10.3 Resumo de Formatos e regras de endereçamento IPv6

---

## 10.3.1 O que aprendi neste módulo?

### Problemas de IPv4

O esgotamento de endereços IPv4 tem sido o fator motivador para a migração para o IPv6. O IPv6 tem um espaço de endereços maior, de 128 bits, fornecendo 340 undecilhões de endereços possíveis. Quando a IETF começou o desenvolvimento de um sucessor para o IPv4, aproveitou para corrigir as limitações do IPv4 e incluir aprimoramentos. Um exemplo é o ICMPv6, que inclui resolução de endereços e configuração automática de endereços não encontrados no ICMPv4.

Ambos IPv4 e IPv6 coexistem e a transição para apenas IPv6 levará vários anos. A IETF criou vários protocolos e ferramentas para ajudar os administradores de rede a migrarem as redes para IPv6. As técnicas de migração podem ser divididas em três categorias: pilha dupla, encapsulamento e tradução. Os dispositivos de pilha dupla executam os protocolos IPv4 e IPv6 simultaneamente. Tunelamento é um método de transporte de pacote IPv6 através de uma rede IPv4. O pacote IPv6 é encapsulado dentro de um pacote IPv4, de forma semelhante a outros tipos de dados. O NAT64 permite que dispositivos habilitados para IPv6 se comuniquem com dispositivos habilitados para IPv4 usando uma técnica de tradução semelhante ao NAT para IPv4. Um pacote IPv6 é traduzido para um pacote IPv4 e um pacote IPv4 é traduzido para um pacote IPv6.

---

### Endereçamento IPv6

Os endereços IPv6 têm 128 bits e são escritos como uma sequência de valores hexadecimais. Cada quatro bits são representados por um único dígito hexadecimal, perfazendo um total de 32 dígitos hexadecimais. Os endereços IPv6 não diferenciam maiúsculas e minúsculas e podem ser escritos tanto em minúsculas como em maiúsculas. No IPv6, um hexteto se refere a um segmento de 16 bits, ou quatro dígitos hexadecimais. Cada "x" é um único hexteto, que tem 16 bits ou quatro dígitos hexadecimais. Formato preferencial significa que o endereço IPv6 é gravado usando todos os 32 dígitos hexadecimais. Aqui está um exemplo - fe80:0000:0000:0000:0123:4567:89ab:cdef.

Existem duas regras que ajudam a reduzir o número de dígitos necessários para representar um endereço IPv6.

**Regra 1** - omitir zeros à esquerda. Você só pode omitir zeros à esquerda, não zeros à direita.

- 01AB pode ser representado como 1AB
- 09f0 pode ser representado como 9f0
- 0a00 pode ser representado como a00
- 00ab pode ser representado como ab

**Regra 2** - dois pontos duplos. Dois-pontos duplos (::) podem substituir qualquer sequência única e contígua de um ou mais hextetos de 16 bits que consistam em zeros. Por exemplo, 2001:db8:cafe: 1:0:0:0:1 (0s iniciais omitidos) poderia ser representado como 2001:db8:cafe:1::1. Os dois-pontos duplos (::) são usados no lugar dos três hextetos compostos por zeros (0:0:0). Os dois-pontos duplos (::) só podem ser usados uma vez dentro de um endereço, caso contrário, haveria mais de um endereço resultante possível. Se um endereço tiver mais de uma string contígua de hextetos com zero, a melhor prática é usar dois pontos duplos (::) na string mais longa. Se as strings forem iguais, a primeira string deve usar dois pontos duplos (::).

---

## 10.3.2 Webster — Questões para Reflexão

Quando eu estava começando a entender os endereços IPv4, aprendi sobre os endereços IPv6! Mas, como parece que a maioria das redes usa os dois tipos de endereços, estou feliz por saber um pouco sobre cada tipo. Acho que é como carros na estrada. Alguns são antigos, mas ainda funcionam. Os carros mais novos têm muito mais recursos e opções do que os carros mais antigos. E os carros mais antigos e mais novos estão todos andando na mesma estrada. Qual é uma vantagem óbvia de usar endereços IPv6 em vez de usar endereços IPv4?