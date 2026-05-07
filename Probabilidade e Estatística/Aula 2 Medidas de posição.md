# TEMA 1 – MEDIDAS DE POSIÇÃO

Um conjunto de dados pode ser apresentado de forma mais sintética se utilizarmos apenas um valor que represente em termos “médios” todo o conjunto que tende a se localizar no centro em torno do qual os dados se concentram.

As principais medidas de posição – também chamadas de _medidas de tendência central_ – são a média, a mediana e a moda. Essas medidas podem ser aplicadas nos três tipos de dados que já estudamos: **dados não agrupados**, **distribuição de frequência** e **distribuição de frequência por classe ou intervalo**.

- **Dados não agrupados**: dados não apresentados nem agrupados numa distribuição de frequência.

12 13 10 14 16 15 17 14 12 13

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image002.jpg)

- **Dados agrupados numa distribuição de frequência**: tabela que demonstra a frequência de ocorrência de cada resultado.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image003.jpg)

- **Dados agrupados numa distribuição de frequência por classe**: tabela que apresenta os dados em faixas de valores, indicando a frequência com que cada faixa aparece na pesquisa.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image004.png)

Agora vamos estudar a diferença entre **média**, **mediana** e **moda**, e como calcular as medidas para cada tipo de dado apresentado.

# TEMA 2 – MÉDIA

A média aritmética é uma medida estatística que representa o grau de concentração dos valores numa distribuição, ou seja, é nela que a maioria dos valores se posiciona. Segundo Oliveira (1999), é o protótipo das medidas de tendência central definida como o quociente entre a soma de todos os valores da variável e seu número de elementos.

A média (ou média aritmética) é a medida de posição mais comum, representada pelo símbolo ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image005.png). Ela é definida pela soma dos resultados obtidos numa pesquisa dividida pela quantidade de resultados; ou seja, somamos todos os valores e o dividimos pela quantidade de dados que temos na pesquisa.

Quando trabalhamos com dados não agrupados, utilizamos a seguinte fórmula para calcular a média:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image006.png)

Sendo _X_ os dados, e _N_ a quantidade de observações.

**Exemplo 1**: uma indústria pretende determinar a duração de certo equipamento eletrônico medindo 10 aparelhos (em horas), obtendo os seguintes resultados:

123 116 122 110 175 126 125 111 118 117

Com base nos dados coletados, determine a média de vida útil do equipamento.

Para calcular a média, precisamos somar os dados e dividi-los por 10, descobrindo a quantidade de equipamentos avaliados, ou seja:

**![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image007.png)**

**![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image008.png)**

Logo, o equipamento dura em média 124,3 horas.

**Exemplo 2**: uma loja apresentou, durante um ano, o seguinte volume de vendas (R$): 2.500, 2.600, 3.100, 15.100, 4.600, 4.000, 4.100, 3.700, 3.400, 3.600, 3.900 e 4.200. Qual a média mensal de vendas?

Somamos os valores fornecidos e dividimos por 12:

**![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image009.png)**

**![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image010.png)**

Assim, a média mensal de vendas da empresa é R$ 4.566,67.

**Exemplo 3**: as exportações de determinado porto brasileiro registraram o seguinte movimento durante um ano (em bilhões de reais) (Castanheira, 2010). Qual foi a média mensal de exportações (em bilhões de reais)?

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image011.jpg)

Para encontrar a média, devemos somar os valores mensais de exportações segundo a coluna (R$) e depois dividi-los por 12, pois temos 12 meses:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image012.png)

A média mensal de exportações é de 3 bilhões de reais.

A média é a medida de posição mais utilizada, mas tem um ponto negativo, já que é influenciada pelos extremos. Precisamos sempre observar se os dados coletados têm valores baixos e altos, pois influenciarão no cálculo da medida.

# TEMA 3 – MÉDIA PONDERADA

Quando os dados se agrupam numa distribuição de frequência, calculamos a média aritmética ponderada (ou apenas média ponderada), pois cada grandeza envolvida no cálculo tem uma importância diferente, ou seja, acontece um número diferente de vezes. Para calcular essa medida, usamos a seguinte fórmula e os seguintes passos:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image013.png), sendo N = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image014.png)

1.  Multiplicamos os dados (_X_) pela frequência (_f_) para cada um dos valores da distribuição;

2.  Somamos os valores obtidos no Passo 1, ou seja, os resultados da multiplicação _X.f_;

3.  Encontramos o valor de _N_ somando a coluna de frequências;

4.  Dividimos o valor encontrado no Passo 2 pelo valor de _N._

**Exemplo 1**: uma pesquisa obteve a seguinte distribuição quanto à idade dos integrantes de um grupo. Calcule a idade média na seguinte distribuição de frequências:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image015.png)

1.  Multiplique os valores (_X_), que representam as idades, pela frequência (_f_), representada na segunda coluna, para cada um dos valores da distribuição:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image016.jpg)

2.  Some os valores obtidos na multiplicação _X.f_:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image017.png)

3.  Encontre o valor de _N_ somando a coluna de frequências: _N= 20_.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image018.png)

4.  Divida o valor encontrado na soma de _X.f_ pelo valor de _N_.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image019.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image023.png)

Assim, a idade média desse grupo é de 5,5 anos.

**Exemplo 2**: uma indústria avaliou 30 aparelhos produzidos, apresentando os seguintes números de defeitos por aparelho:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image024.png)

Qual o número médio de defeitos?

Vamos primeiro multiplicar _X.f_ e, depois de somar os valores obtidos, encontrar o valor de _N_; por último, dividimos para encontrar a média:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image025.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image026.png)

A média de defeitos nos aparelhos inspecionados é de 1,1 defeito.

Quando temos uma distribuição de frequências representada em intervalos ou classes, a média ponderada é calculada ao substituirmos os valores de _X,_ na fórmula, pelo ponto médio (_PM_) de cada intervalo, ou seja:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image027.png) = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image028.png)

Para calcular a média numa distribuição de frequência por classe, consideramos os passos a seguir.

1.  Calculamos o ponto médio de cada classe aplicando a seguinte fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image029.png)

2.  Para cada um dos valores da distribuição, multiplicamos o ponto médio (_PM_) pela frequência (_f_);

3.  Somamos os valores obtidos na multiplicação _PM.f_ ;

4.  Somamos a coluna de frequências para encontrar o valor de _N_;

5.  Dividimos o valor encontrado na soma de _PM.f_ pelo valor de _N._

**Exemplo 1**: uma pesquisa indicou a altura dos funcionários de determinada empresa. Com base nos dados obtidos na pesquisa, calcule a média das alturas.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image030.jpg)

Para calcular a média numa distribuição de frequência por classe, aplicamos os seguintes passos:

- **Calculamos o ponto médio de cada classe.**

Primeira classe:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image031.png)

Aplicando o mesmo cálculo para as demais classes, temos:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image032.jpg)

- **Para todas as classes, multiplicamos o ponto médio (_PM_) pela frequência (_f_):**

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image036.jpg)

- **Somamos os valores obtidos na multiplicação _PM.f_:**

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image037.jpg)

- **Somamos a coluna de frequências para encontrar o valor de _N_:**

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image038.jpg)

- **Dividimos o valor da soma de _PM.f_ pelo valor de _N_:**

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image039.jpg)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image045.png)

A média da altura dos funcionários é 161 cm.

**Exemplo 2**: uma empresa inspecionou 50 componentes eletrônicos para determinar seu tempo de vida útil, obtendo a seguinte distribuição.

- **Calculamos o tempo médio de vida desse componente.**

|   |   |
|---|---|
|Tempo (horas)|Frequência|
|1200 \|--- 1300|1|
|1300 \|--- 1400|3|
|1400 \|--- 1500|11|
|1500 \|--- 1600|20|
|1600 \|--- 1700|10|
|1700 \|--- 1800|3|
|1800 \|--- 1900|2|

Iniciamos calculando o ponto médio e depois o multiplicamos pela frequência. Somados os resultados obtidos na multiplicação, dividimos por _N_ para encontrar a média.

|   |   |   |   |
|---|---|---|---|
|Tempo (horas)|Frequência|PM|PM.f|
|1200 \|--- 1300|1|1250|1250|
|1300 \|--- 1400|3|1350|4050|
|1400 \|--- 1500|11|1450|15950|
|1500 \|--- 1600|20|1550|31000|
|1600 \|--- 1700|10|1650|16500|
|1700 \|--- 1800|3|1750|5250|
|1800 \|--- 1900|2|1850|3700|
||50||77700|

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image046.png)

O tempo médio de vida útil dos componentes eletrônicos é 1.554 horas.

# TEMA 4 – MEDIANA

A segunda medida de posição é a mediana, que representamos por _Md_ e indica o elemento que ocupa a posição central. Essa medida divide a distribuição em 50%, ou seja, é o valor que divide o conjunto de dados em duas partes iguais.

Figura 1 – Mediana

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image047.jpg)

Para dados não agrupados, a mediana é o valor que divide a série ordenada em dois conjuntos de igual tamanho, ou seja, com o mesmo número de valores. Segundo Castanheira (2010), é necessário observar que a quantidade de dados pode ser par ou ímpar. Sendo ímpar, o valor da mediana é o valor que está no centro da série; sendo par, a mediana será a média aritmética dos dois valores no centro da série.

Quando temos os dados não agrupados, os passos para calcular a mediana são:

- Colocar os dados em ordem;
- Encontrar o valor de _N_, que é igual ao número de observações, quantidade de dados da série;
- Verificar se _N_ é ímpar ou par;
- Encontrar a posição da mediana pela fórmula: posição = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image048.png);
- Calcular a mediana, considerando se _N_ é par ou ímpar:
    - Ímpar = valor central;
    - Par = média dos valores centrais.

**Exemplo 1**: calcule a mediana da série 2, 5, 6, 8, 10, 13, 15, 16, 18.

- Ordenar a série: nesse exemplo os dados já estão ordenados;
- Encontrar o valor de _N_, contando quantos dados temos na série. Nesse caso, _N_ = 9;
- Verificar se _N_ é ímpar ou par: _N_ = 9 é ímpar;
- Calcular posição.

Posição = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image049.png)

**Observação**: caso a posição apresente um número com vírgula, arredonde para o inteiro mais próximo.

- Procure na série ordenada o número na posição 5. Assim, o número 2 está na primeira posição, o número 5 na segunda etc. Seguindo esse processo, temos o número 10 na quinta posição: 2, 5, 6, 8, **[10]**, 13, 15, 16, 18.

Como _N_ é ímpar, a mediana é o valor central. Assim, a mediana é igual a 10, pois abaixo de 10 temos 4 números (2, 5, 6, 8), e acima de 10 também (13, 15, 16, 18).

**Exemplo 2**: calcule a mediana da série: 1, 6, 3, 10, 9, 8.

**Passos**:

- Ordenar a série: 1, 3, 6, 8, 9, 10;
- Encontrar o valor de _N_, contando quantos dados temos na série. Logo, _N_ = 6;
- Verificar se _N_ é ímpar ou par: N = 6 é par;
- Calcular posição.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image050.png)

- Como _N_ é par, precisamos encontrar dois valores centrais. Logo, vamos procurar na série ordenada o número que está na posição 3 e a próxima posição, que é a 4. Na posição 3 temos o número 6, e na posição 4, o número 8: 1, 3, **[6]**, **[8]**, 9, 10.

Para encontrar a mediana, calculamos a média entre os dois valores centrais, somando-os e dividindo-os por 2:

Md = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image051.png)

A mediana também pode ser calculada numa distribuição de frequências pelos seguintes passos:

1. Encontre o valor de _N_, que é igual à soma das frequências;
2. Determine se _N_ é par ou ímpar;
3. Calcule a frequência acumulada (_fa)_;
4. Calcule a posição _N/2_;
5. Identifique na frequência acumulada a posição calculada no Passo 4. Sempre busque um valor igual ou maior que a posição calculada;
6. Calcule a mediana:
    - Ímpar = valor central;
    - Par = média dos valores centrais.

**Exemplo 3**: uma indústria avaliou 30 aparelhos produzidos, apresentando os seguintes números de defeitos por aparelho:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image052.jpg)

Qual a mediana dessa distribuição?

Para determinar a mediana, seguimos os passos indicados:

1.   Encontre o valor de _N_; para isso, somamos as frequências, e temos _N_ = 30:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image053.jpg)

2.   Determine se _N_ é par ou ímpar; _N_ = 30, então _N_ é par;

3.   Calcule a frequência acumulada; para isso, repetimos a primeira frequência e somamos com a seguinte frequência:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image054.png)

4.   Calcule a posição:

Posição = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image057.png)

5.   Identifique, na frequência acumulada, a posição encontrada no Passo 4. Como _N_ é par, precisamos de dois valores centrais;, ou seja, vamos encontrar o valor que está na posição 15 e na 16. Na coluna da frequência acumulada, procuramos valor igual ou maior que a posição; nesse caso, procuramos valores iguais ou maiores que 15 e 16. Esses números (15 e 16) estão na frequência acumulada igual a 20, que tem dado igual a 1.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image058.png)

Posição 15 = 1;

Posição 16 = 1.

6.   Some os dados encontrados nas posições para calcular a mediana:

Md = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image059.png)

A mediana dessa distribuição é igual a 1, ou seja, 50% dos aparelhos avaliados têm até 1 defeito.

**Exemplo 4**: uma pesquisa foi feita em diferentes lojas para avaliar o preço de determinado produto. Com base na seguinte distribuição, calcule a mediana:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image060.png)

1.  Inicialmente, encontramos o valor de _N_, que é a soma das frequências:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image061.jpg)

2.  Verificamos se o valor de _N_ encontrado no Passo 1 é par ou ímpar; como _N_ é 31, então é ímpar;

3.  Com base na coluna de frequências, calculamos a frequência acumulada:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image063.png)

4.  Calculamos a posição da mediana utilizando a seguinte fórmula:

Posição = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image064.png)

5.  Identificamos a posição na coluna de frequência acumulada, procurando um valor igual ou maior que 16. Esse número está na frequência acumulada igual a 24, que tem dado igual a 77;

6.  Como _N_ é um número ímpar, a mediana será o valor encontrado na posição 16; ou seja, a mediana é igual a 77.

Assim, 50% dos locais comercializam o produto por até R$ 77.

Quando temos uma distribuição de frequência com os dados agrupados por classes, utilizamos os seguintes passos para calcular a mediana:

1.  Some as frequências para encontrar o valor de _N_;

2.  Calcule a posição da mediana pela divisão ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image065.png);

3.  Calcule frequência acumulada (_fa_);

4.  Identifique a posição calculada no Passo 2 na frequência acumulada. Lembre-se que buscamos um valor igual ou maior que a posição calculada no Passo 2;

5.  Calcule a mediana aplicando a seguinte fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image066.png)

Sendo:

- _Li_ = limite inferior da classe que contém a mediana;
- _N_ = número de observações, ou seja, soma das frequências;
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image067.png)= soma das frequências anteriores à classe que contém a mediana;
- _A_ = amplitude das classes: _A = Ls − Li_;
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image068.png)= frequência da classe que contém a mediana.

**Exemplo 5**: uma empresa inspecionou 50 componentes eletrônicos para determinar seu tempo de vida útil, obtendo a distribuição a seguir. Calcule a mediana.

|   |   |
|---|---|
|Tempo (horas)|Frequência|
|1200 \|--- 1300|1|
|1300 \|--- 1400|3|
|1400 \|--- 1500|11|
|1500 \|--- 1600|20|
|1600 \|--- 1700|10|
|1700 \|--- 1800|3|
|1800 \|--- 1900|2|

Vamos aplicar os passos para calcular a mediana dessa distribuição:

- Encontre o valor de _N_, que é igual à soma das frequências:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image069.png)

- Calcule a posição:

Posição = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image071.png)

- Calcule a frequência acumulada (_fa_):

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image072.jpg)

- Identifique a posição calculada no Passo 2, na frequência acumulada. Temos que a posição é 25, então buscamos um valor igual ou maior na coluna de frequência acumulada:

Posição = 25, identificada na quarta classe.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image076.png)

- Aplique a fórmula para obter a mediana:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image077.png)

Identificamos no Passo 4 a posição na quarta classe. Assim, essa classe será utilizada como base para os cálculos, sendo:

- _Li_ = 1500;
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image078.png);
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image079.png)= soma das frequências anteriores à classe que contém a mediana.

Consideramos o valor anterior à classe na coluna de frequência acumulada. Assim, o valor procurado é igual a 15.

- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image080.png)= frequência da classe que contém a mediana = 20.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image081.png)

Com os valores descritos, aplicamos a fórmula para encontrar o valor da mediana:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image085.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image086.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image087.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image088.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image089.png)

A mediana é igual a 1.550, ou seja, 50% dos componentes têm tempo de vida útil de até 1.550 horas.

**Exemplo 6**: A tabela a seguir representa as notas obtidas por um grupo de 58 alunos matriculados em determinada disciplina. Calcule a mediana.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image090.jpg)

Fonte: Purgote, 2020, com base em Shiguti; Shiguti, 2006.

Para calcular a mediana, seguimos os passos já mencionados:

- Encontre o valor de _N_, que é igual à soma das frequências:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image093.jpg)

- Calcule a posição:

Posição = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image094.png)

- Calcule a frequência acumulada (_fa_):

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image095.png)

- Identifique na frequência acumulada a posição calculada no Passo 2.

Posição = 29, identificada na terceira classe.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image096.png)

- Calcule a mediana utilizando a fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image099.png)

Como a posição foi identificada na terceira classe, essa classe será utilizada como base para os cálculos, sendo:

- _Li_ = 55;
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image100.png);
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image079.png)= soma das frequências anteriores à classe que contém a mediana = 17;
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image101.png)= frequência da classe que contém a mediana = 18;
- _A = Ls − Li = 65 − 55 = 10_.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image102.png)

Com todos os dados necessários, aplicamos a fórmula para encontrar a mediana:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image105.jpg)

Temos que a mediana é igual a 61,67, ou seja, 50% dos alunos obtiveram nota de até 61,67 pontos.

No Tema 2 vimos que a média tem um ponto negativo, já que é influenciada pelos extremos. Na mediana isso não ocorre, pois ela reflete a tendência central, de modo que não é influenciada por valores extremos ou discrepantes.

# TEMA 5 – MODA

Nos demais temas vimos a diferença entre média e mediana; agora vamos trabalhar com a moda. Representada por _Mo,_ a moda indica o valor que ocorre o maior número de vezes, ou seja, que mais se repete. É aquele valor que tem a maior frequência.

Quando calculamos a moda, podemos ter três situações:

1.  **Distribuição modal**: quando temos apenas uma moda, ou seja, ao calcular a moda, temos apenas um valor;

2.  **Distribuição bimodal**: quando temos dois ou mais valores para moda;

3.  **Distribuição amodal**: não há repetição de valores, logo, não temos moda.

Para obter a moda numa série de dados formada por dados não agrupados, verificamos o valor que mais se repete.

**Exemplo 1**: vamos observar a seguinte série: 7, 10, 9, 8, 12, 10, 11, 10. Verificamos que o número 10 aparece 3 vezes; portanto a moda é igual a **10**.

**Exemplo 2**: encontre a moda da seguinte série: 3, 5, 8, 10, 12. Observando a série, percebemos que todos os valores aparecem uma única vez. Logo, a série não apresenta moda, isto é, a série é amodal.

**Exemplo 3**: qual a moda da seguinte série? 4, 3, 2, 4, 5, 7, 6, 4, 7, 9, 8, 7.

Tanto o número 4 quanto o número 7 aparecem 3 vezes; assim, temos duas modas _(Mo_ = 4 e _Mo_ = 7_)_; logo, a série é bimodal.

De acordo com Martins (2010), para distribuições simples, sem agrupamento em classes, a identificação da moda é facilitada pela simples observação do elemento que apresenta maior frequência. Assim, verificamos na coluna de frequência o maior valor, e a moda será o valor de _X_, que está na primeira coluna.

**Exemplo 4**: uma indústria avaliou 30 aparelhos produzidos, apresentando os seguintes números de defeitos por aparelho. Com base nos dados obtidos, calcule a moda.

|   |   |
|---|---|
|**Número de defeitos**|**F**|
|0|12|
|1|8|
|2|7|
|3|1|
|4|2|

Como temos uma distribuição de frequência, vamos verificar na coluna de frequência o maior valor. assim, temos que a maior frequência é 12. A moda é identificada pelo dado da primeira coluna; ou seja, a moda é igual a zero (_Mo_ = 0).

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image106.png)

Para calcular a moda numa distribuição de frequências com dados agrupados em classes, aplicamos os seguintes passos:

1.  Identificamos em que classe se encontra a moda;

2.  Determinamos o valor da moda utilizando a seguinte fórmula:

Mo = Li + ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image107.png)

Sendo:

- _Li =_ limite inferior da classe que contém a moda;
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image108.png)= frequência da classe posterior à classe que contém a moda;
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image109.png) = frequência da classe anterior à classe que contém a moda;
- _A_ = amplitude das classes: _A = Ls – Li._

**Exemplo 5**: a tabela a seguir representa as notas obtidas por um grupo de 58 alunos matriculados numa determinada disciplina. Calcule a moda.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image110.jpg)

Fonte: Purgote, 2020, com base em Shiguti; Shiguti, 2006.

Passos para determinar a moda:

1.  Identificamos a classe que apresenta a maior frequência de ocorrência. A maior frequência é 18, assim, a moda se localiza na classe: 55|---- 65.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image111.png)

2.  Considerando a classe identificada no Passo 1 (_55|----65_)_,_ determinamos o valor da moda utilizando a fórmula, sendo:

- _Li =_ 55
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image108.png)= frequência da classe posterior à classe que contém a moda = 14
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image109.png) = frequência da classe anterior à classe que contém a moda = 12

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image112.jpg)

- _A = Ls − Li = 65 − 55 = 10_
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image117.png)
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image118.png)
- ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image119.png)

A nota que aparece com mais frequência (ou que mais se repete) é 60,38; ou seja, a moda é igual a 60,38.

**Exemplo 6**: uma empresa inspecionou 50 componentes eletrônicos para determinar seu tempo de vida útil, obtendo a distribuição a seguir. Calcule a moda.

|   |   |
|---|---|
|Tempo (horas)|Frequências|
|1200 \|--- 1300|1|
|1300 \|--- 1400|3|
|1400 \|--- 1500|11|
|1500 \|--- 1600|20|
|1600 \|--- 1700|10|
|1700 \|--- 1800|3|
|1800 \|--- 1900|2|

- Identifique em que classe se encontra a moda. A maior frequência é 20; assim, a moda está localizada na classe: 1500 |--- 1600;
- Determine o valor da moda utilizando a fórmula, sendo:
    - _Li =_ 1500
    - ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image108.png)= frequência da classe posterior à classe que contém a moda = 10
    - ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image120.png) = frequência da classe anterior à classe que contém a moda = 11
    - _A = Ls − Li = 1600 − 1500 = 100_

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image121.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image122.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a2/includes/html/impressao_arquivos/image123.png)

# FINALIZANDO

Nesta aula, verificamos a diferença entre cada medida de posição (média, mediana e moda), seus cálculos, aplicações e interpretações dos resultados para dados não agrupados, distribuição de frequência e distribuição de frequência por classe.