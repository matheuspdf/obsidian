# TEMA 1 – MEDIDAS DE DISPERSÃO

A análise realizada pelas medidas de posição pode ser complementada com a utilização das medidas de dispersão. Segundo Castanheira (2010), as medidas de dispersão servem para verificar com que confiança as medidas de posição resumem as informações fornecidas pelos dados obtidos em uma pesquisa.

As medidas de dispersão indicam se os dados estão afastados da região central, medindo o grau de variação existente entre os valores, e servem também para medir a representatividade da média.

Considere uma pesquisa que represente o preço de dois produtos (A e B) em diferentes pontos de venda:

A: 20, 20, 20

B: 15, 10, 20, 25, 30

Ao calcular a média de preço, obtemos o valor igual a R$ 20,00 para os dois produtos, mas, analisando os valores, temos que no produto A não há variação entre os preços; já no produto B, temos preços diferentes, ou seja, a média é de R$ 20,00, e encontramos o produto por R$10,00 e R$30,00. Logo, para o mesmo produto, encontramos diferenças entre os preços. Assim, os valores apresentam dispersão em torno da média.

Dentre as medidas de dispersão, podemos citar a **amplitude total**, o **desvio médio**, a **variância** e o **desvio padrão**.

A amplitude total é considerada a medida de dispersão mais simples, e é calculada pela diferença entre o maior e o menor valores de uma série de dados:

**A = maior – menor**

Se o resultado encontrado para a amplitude for um número elevado, significa que os valores da série estão afastados uns dos outros. Caso o valor encontrado seja baixo, os valores da série estão próximos uns dos outros. Dessa forma, quanto maior a amplitude, maior a dispersão dos valores.

**Exemplo 1**

Considere os valores 40, 45, 48, 62 e 70. Calcule a amplitude total.

Para encontrar a amplitude, precisamos do maior e do menor valor para depois realizar a diferença:

Maior valor = 70

Menor valor = 40

Amplitude = 70 – 40 = 30

**Exemplo 2**

Qual é a amplitude do preço pago por um equipamento eletrônico nos últimos cinco meses?

| **Mês** | **Valor** |
| ------- | --------- |
| 1       | 500       |
| 2       | 1.500     |
| 3       | 1.800     |
| 4       | 2.200     |
| 5       | 2.500     |

Maior valor = 2.500

Menor valor = 500

Amplitude = 2.500 – 500 = 2.000

Segundo Castanheira (2010), para o caso de os dados estarem agrupados em classes, o cálculo da amplitude total pode ser realizado de duas formas:

1. pelos pontos médios das classes. Nesse caso, a amplitude total é igual ao ponto médio da última classe, menos o ponto médio da primeira classe;

2. pelos limites das classes. Nesse caso, a amplitude total é igual ao limite superior da última classe, menos o limite inferior da primeira classe.

**Exemplo 3**

Qual é a amplitude da seguinte distribuição?

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image002.jpg)

Calcule a amplitude considerando as duas formas citadas anteriormente:

1. pelo ponto médio das classes. Nesse caso, para calcular a amplitude total, precisamos encontrar o ponto médio da última classe e o ponto médio da primeira classe para depois realizar a diferença. Lembre-se de que o ponto médio é calculado pela fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image003.png)

Ponto médio da última classe:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image004.png)

Ponto médio da primeira classe:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image005.png)

Amplitude = 172 – 152 = 20 cm

2. pelos limites das classes. Para calcular a amplitude total, precisamos encontrar o limite superior da última classe e o limite inferior da primeira classe para depois realizar a diferença:

Limite superior da última classe = 174

Limite inferior da primeira classe = 150

Amplitude = 174 – 150 = 24 cm

A amplitude total apresenta algumas restrições, pois considera apenas os valores extremos da série, desprezando os valores intermediários. Segundo Martins (2010, p. 52), a utilização da amplitude total como medida de dispersão é limitada, pois, sendo uma medida que depende apenas dos valores extremos, não capta possíveis variações entre seus limites.

# TEMA 2 – DESVIO MÉDIO

O **desvio médio** é uma medida de dispersão que analisa a média dos desvios em torno da média de cada um dos valores da série e é calculado pela média dos valores absolutos dos desvios. Representa a média das distâncias entre cada elemento da amostra e seu valor médio.

Chamamos _Dm_ o desvio médio e o calculamos pela fórmula:

_Dm_ =![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image006.png)

onde ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image007.png) é o módulo de cada desvio em relação à média e _N_ é igual à soma das frequências. O módulo (| |) utilizado no cálculo do desvio médio possui a função de tornar o número positivo, assim, se a diferença entre o dado e a média resultar em um número positivo, ao se retirar o módulo ele continua positivo, e se for negativo, vira positivo.

Como o desvio médio verifica o afastamento em relação à média, o primeiro passo é calcular a média. Depois, aplicamos a fórmula para encontrar o desvio médio.

**Exemplo 1**

Suponha os seguintes dados que representem a quantidade de anos de vida útil de um equipamento eletrônico e determine o desvio médio desse conjunto de dados:

3  7   8   10   11

Para calcular o desvio médio, calculamos primeiramente a média. Lembre-se de que para calcular a média em dados não agrupados somamos todos os valores e dividimos pelo número de observações:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image008.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image009.png)

O segundo passo é aplicar a fórmula do desvio médio:

_Dm_ =![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image006.png)

Primeiro, calculamos o desvio de cada valor em relação à média, ou seja, cada valor menos a média, que é 7,8. Os valores encontrados, multiplicamos pela frequência, que é o número de vezes que o valor aparece. Por exemplo, se considerarmos o primeiro valor, que é 3, temos |3 – 7,8|.1, ou seja, o número 3 menos a média, que é 7,8 vezes 1, pois o número 3 aparece apenas uma vez. Repetimos esse processo para cada valor da série e, depois, dividimos por 5, que é o número de observações, ou seja, a quantidade de ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image010.png) dados apresentados:

Resolvendo a subtração dentro de cada módulo, temos:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image011.png)

Agora, precisamos retirar os valores do módulo, lembrando que se o número for positivo ele continua positivo e o número negativo torna-se positivo, assim:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image012.png)

Multiplicamos os valores pela frequência, somamos e dividimos por 5:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image013.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image014.png)

Esse resultado indica que, em média, a vida útil desse equipamento eletrônico se desvia em 2,24 anos da média, que é de 7,8 anos.

**Exemplo 2**

Em um determinado dia foi registrado o número de veículos negociados por uma amostra de 10 vendedores de uma agência de automóveis, como mostra a tabela a seguir. Calcule o desvio médio. (Adaptado de Shiguti; Shiguti, 2006.)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image015.jpg)

O primeiro passo é calcular a média. Lembre-se de que, nesse exemplo, temos uma distribuição de frequência e que a média é calculada pela fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image016.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image017.jpg)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image018.png)

Agora, calculamos o desvio em relação à média. Para facilitar, incluimos uma nova coluna na tabela, identificando o cálculo |x – média|, assim para o primeiro valor da tabela, temos: |1 – 2,6| = |-1,6| = 1,6. Seguimos esse mesmo processo para os demais valores da tabela:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image019.jpg)

Encontrados os valores dos desvios, devemos multiplicá-los pelas suas respectivas frequências, incluindo mais uma coluna chamada |x – média|*f. Para o primeiro valor, temos: 1,60 * 1 = 1,60. Seguimos esse processo para os demais valores da tabela e, depois, somamos todos os valores encontrados:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image020.jpg)

Para finalizar, aplicamos a fórmula do desvio médio:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image021.png)_Dm_ =![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image022.png)

A quantidade de veículos negociados por cada vendedor possui um desvio médio de 0,68 em torno dos 2,6 veículos comercializados em média.

Para dados agrupados em classes ou intervalos, substituímos o _X_ na fórmula do desvio médio pelo ponto médio de cada classe (_Pm_).

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image023.png)

Dessa forma, para calcular o desvio médio em uma distribuição de frequência por classe, temos os seguintes passos:

1. calcular o ponto médio de cada classe;

2. ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image028.png) calcular a média;

3. calcular o desvio em relação à média:

4. calcular o desvio médio.

**Exemplo 3**

A tabela a seguir representa as notas obtidas por um grupo de 58 alunos matriculados em uma determinada disciplina. Calcule o desvio médio. (Adaptado de Shiguti; Shiguti, 2006.)

O primeiro passo é calcular o ponto médio de cada classe. Lembre-se de que, para calcular o ponto médio, utilizamos a fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image029.png)

Considerando a primeira classe, temos:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image030.png)

Seguindo o mesmo processo para as demais classes, obtemos:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image031.jpg)

No próximo passo, calculamos a média da distribuição de frequência utilizando a fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image032.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image033.jpg)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image034.png)

Encontrada a média, precisamos calcular os desvios em relação a esse valor:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image035.png)

Para primeira classe, temos:

|40 – 62,24|*5

| -22,24|*5 = 22,24*5 = 111

Seguindo esse cálculo para as demais classes, e após somarmos os valores obtidos, temos:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image036.jpg)

Por fim, aplicamos a fórmula do desvio médio:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image027.png)

A nota de cada aluno possui uma distância de 10,29 pontos do desempenho médio, que foi de 62,24 pontos. 

# TEMA 3 – VARIÂNCIA E DESVIO PADRÃO

A dispersão dos dados também pode ser calculada considerando os quadrados dos desvios médios. Segundo Castanheira, à média aritmética dos quadrados dos desvios damos o nome de variância, que pode ser calculada de duas formas: considerando uma população ou uma amostra. 

População:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image038.png)

No cálculo da variância de uma amostra, o denominador deverá ser (N –1), ou seja:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image039.png)

onde _x_ representa os dados, ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image040.png) é a média do conjunto de dados, _f_ é a frequência com que o dado aparece e _N_ é o número de observações. Como a variância utiliza o quadrado dos desvios médios, o primeiro passo é calcular a média para depois aplicar as fórmulas indicadas.

Ao analisar o resultado da variância, temos que, quanto maior for o seu valor, mais distante da média estarão os dados, e quanto menor, mais próximos os valores estarão da média, ou seja, se os desvios forem baixos, teremos pouca dispersão, e se forem altos, teremos elevada dispersão.

Segundo Martins (2010), para melhor interpretar a dispersão de uma variável, calcula-se a raiz quadrada da variância, obtendo-se o desvio padrão. O desvio padrão também será calculado para uma população ou uma amostra:

- população:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image041.png)

- amostra:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image042.png)

Podemos utilizar as fórmulas anteriores ou calcular a variância e, depois, tirar a raiz quadrada, assim:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image043.png)

**Exemplo 1**

Suponha o conjunto de tempo de serviço de 5 funcionários e determine a variância e o desvio padrão desse conjunto de dados, considerando uma amostra.

3   7   8   10   11

O primeiro passo é calcular a média. Lembre-se de que, para dados não agrupados, somamos os dados e dividimos pela quantidade de observações:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image044.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image045.png)

Depois de encontrada a média, calculamos a variância, verificando que o enunciado solicita a variância considerando uma amostra. Assim, utilizamos a seguinte fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image039.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image046.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image047.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image048.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image049.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image050.png)

Para finalizar, calculamos o desvio padrão tirando a raiz quadrada da variância.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image051.png)

**Exemplo 2**

Considere os seguintes dados e calcule a variância e o desvio padrão considerando uma população.

40  45  48  52  54  62  70

Calcule a média desse conjunto de dados:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image052.png)

Depois de encontrada a média, calculamos a variância, verificando que o enunciado solicita a variância considerando uma população. Assim, utilizamos a seguinte fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image038.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image053.png)![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image054.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image055.png)

Para finalizar, calculamos o desvio padrão tirando a raiz quadrada da variância:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image056.png)

**Exemplo 3**

Em um determinado dia foi registrado o número de veículos negociados por uma amostra de 10 vendedores de uma agência de automóveis, como mostra a tabela a seguir. Calcule a variância e o desvio padrão. (Adaptado de Shiguti; Shiguti, 2006.)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image057.jpg)

Nesse exemplo, temos uma distribuição de frequência e precisamos calcular a variância. Logo, o primeiro passo é o cálculo da média. Lembre-se de que a média em uma distribuição de frequência é calculada pela fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image058.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image059.jpg)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image060.png)

Após o cálculo da média, calculamos o quadrado dos desvios em relação à média e multiplicamos o valor encontrado por sua respectiva frequência. Para o primeiro valor, temos:

(1 – 2,6)². 1 = (-1,6)² . 1 = 2,56 . 1 = 2,56

Seguindo esse cálculo, para os demais valores da distribuição, temos:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image061.jpg)

Somamos o valor encontrado em _(x –_ ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image040.png)_)².f_ e aplicamos a fórmula da variância para uma amostra, encontrando o seguinte valor:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image062.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image063.png)

Tiramos a raiz quadrada da variância para encontrar o desvio padrão:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image064.png)

Para uma distribuição de frequência por classe ou intervalos, substituímos na fórmula da variância o valor de _x_ pelo ponto médio (_Pm_) de cada classe. Dessa forma, o primeiro passo será o cálculo do ponto médio, para depois calcular a média e a variância.

- população:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image065.png)

- amostra:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image066.png)

**Exemplo 4**

A tabela a seguir representa as notas obtidas por um grupo de 58 alunos matriculados em uma determinada disciplina. Calcule a variância e o desvio padrão da amostra. (Adaptado de Shiguti; Shiguti, 2006.)

**![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image067.jpg)**

Nesse exemplo, temos uma distribuição de frequência por classe. Iniciamos calculando o ponto médio (_Pm_) e a média da distribuição:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image068.jpg)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image069.png)![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image070.png)

Agora, calculamos os desvios: (_Pm_– ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image040.png))². O resultado, multiplicamos pela frequência. Para a primeira classe, temos:

(40 – 62,24) ² = (-22,24) ² = 495

495 . 5 = 2.473

Seguindo o mesmo processo para as demais classes e somando os valores obtidos, temos:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image071.jpg)

Agora, calculamos a variância solicitada da amostra:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image066.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image072.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image073.png)

Para calcular o desvio padrão, tiramos a raiz quadrada da variância:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image074.png)

No desvio padrão, obtemos valores altos sempre que ocorrem mudanças consideráveis nos dados analisados e valores baixos quando os dados são mais estáveis. Segundo Martins (2010), quanto maior o desvio padrão, maiores a dispersão e a amplitude total da distribuição.

# TEMA 4 – MEDIDAS DE ASSIMETRIA

De acordo com Castanheira (2010), a média corresponde ao centro de gravidade dos dados; a variância e o desvio padrão medem a variabilidade, mas a distribuição dos pontos sobre um eixo ainda tem outras características que podem ser medidas – uma delas é a assimetria. A assimetria complementa as medidas de posição e dispersão, pois proporciona uma descrição e a compreensão mais completa das distribuições de frequências, já que as distribuições também se diferenciam quanto à sua forma.

Definimos assimetria como o grau de afastamento de uma distribuição da unidade de simetria, pois indica o grau de deformação de uma curva de frequências. Quando uma distribuição é simétrica, temos a igualdade dos valores de média, mediana e moda, conforme figura abaixo:

Figura 1 – Distribuição simétrica

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image075.jpg)

Uma distribuição assimétrica pode ser assimétrica positiva, também chamada de _assimétrica à direita,_ ou assimétrica negativa, também chamada de _assimétrica à esquerda_.

Em uma distribuição assimétrica positiva a média é maior que a mediana e a moda, ou seja, _![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image076.png)>Md > Mo,_ conforme observamos na figura a seguir:

Figura 2 – Assimetria à direita ou positiva

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image077.jpg)

Na distribuição assimétrica negativa, temos que a média é menor que a mediana e a moda, assim, _![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image076.png)< Md < Mo,_ conforme observamos na figura a seguir:

Figura 3 – Assimetria à esquerda ou negativa

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image078.jpg)

Existem várias fórmulas para o cálculo do coeficiente de assimetria. Dentre eles, estudaremos o coeficiente de assimetria de Pearson. O 1º coeficiente de assimetria de Pearson é calculado por:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image079.png)

Além do 1º coeficiente, podemos calcular o 2º coeficiente de Pearson aplicando a seguinte fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image080.png)

Analisando o valor do coeficiente, temos:

- _AS_ = 0, a distribuição é simétrica;
- _AS_ > 0, a distribuição é assimétrica positiva ou à direita;
- _AS_ < 0, a distribuição é assimétrica negativa ou à esquerda.

**Exemplo 1**

Uma empresa inspecionou 50 componentes eletrônicos para determinar o tempo de vida útil desse componente, obtendo a distribuição que vemos a seguir. Calcule o 1º coeficiente de assimetria de Pearson.

|**Tempo (horas)**|**Frequências**|
|---|---|
|1200 \|--- 1300|1|
|1300 \|--- 1400|3|
|1400 \|--- 1500|11|
|1500 \|--- 1600|20|
|1600 \|--- 1700|10|
|1700 \|--- 1800|3|
|1800 \|--- 1900|2|

Para calcular o 1º coeficiente de Pearson, precisamos dos valores de média, moda e desvio padrão. Na Aula 2, calculamos a média e a moda obtendo os seguintes resultados:

- média:

|Tempo (horas)|Frequências|PM|PM.f|
|---|---|---|---|
|1200 \|--- 1300|1|1250|1250|
|1300 \|--- 1400|3|1350|4050|
|1400 \|--- 1500|11|1450|15950|
|1500 \|--- 1600|20|1550|31000|
|1600 \|--- 1700|10|1650|16500|
|1700 \|--- 1800|3|1750|5250|
|1800 \|--- 1900|2|1850|3700|
||50||77700|

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image081.png)

- moda:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image082.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image083.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image084.png)

Para calcular o desvio padrão, seguimos os passos indicados no Tema 3 desta aula:

- desvio padrão:

|Tempo (horas)|Frequências|_PM_|_(PM – Média)²_|_(PM – Média)².f_|
|---|---|---|---|---|
|1200 \|--- 1300|1|1250|92416|92416|
|1300 \|--- 1400|3|1350|41616|124848|
|1400 \|--- 1500|11|1450|10816|118976|
|1500 \|--- 1600|20|1550|16|320|
|1600 \|--- 1700|10|1650|9216|92160|
|1700 \|--- 1800|3|1750|38416|115248|
|1800 \|--- 1900|2|1850|87616|175232|
||50|||719200|

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image085.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image086.png)

Agora, calculamos o 1º coeficiente de assimetria de Pearson aplicando os valores obtidos na fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image079.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image087.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image088.png)

**Exemplo 2**

Considere uma distribuição de frequência que apresente média igual a 88, mediana igual a 82 e desvio padrão igual a 40. Calcule o 2º coeficiente de Pearson.

Com os valores fornecidos no enunciado, calculamos o coeficiente aplicando a fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image080.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image089.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image090.png)

# TEMA 5 – MEDIDAS DE CURTOSE

Segundo Castanheira (2010), a curtose indica o quanto uma distribuição de frequências é mais achatada ou mais afilada do que uma curva padrão, a qual é denominada de curva normal. A **curva normal** ou **distribuição normal** será estudada na Aula 5.

Ao realizar a análise em relação ao achatamento, temos que a distribuição normal é chamada de _mesocúrtica_, em que os dados estão uniformemente distribuídos. As distribuições mais achatadas que a normal são as _platicúrticas_, em que os dados estão bem dispersos em relação à média. Às distribuições menos achatadas ou mais alongadas que a normal chamamos de _leptocúrticas_, em que os dados estão concentrados em torno da média. Analisaremos cada distribuição nos gráficos seguintes:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image091.jpg)

Para determinar a curtose, aplicamos a seguinte fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image092.png)![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image093.png)

onde:

_K_ = coeficiente percentílico de curtose

_Q1=_ primeiro quartil

_Q3_= terceiro quartil

_p10_= décimo percentil

_p90_= nonagésimo percentil

Analisando o valor de _K_, temos a seguinte classificação:

- K = 0,263 – curva normal, distribuição mesocúrtica;
- K > 0,263 – curva mais achatada, distribuição platicúrtica;
- K < 0,263 – curva mais alongada, distribuição leptocúrtica.

Para o cálculo do coeficiente, precisamos encontrar o quartil e o percentil. O quartil divide uma distribuição em quatro partes iguais e é representado por _Qi_, onde _i_ representa a ordem do quartil. No diagrama a seguir, temos que o 1º quartil representa 25% dos dados, o 2º quartil representa 50% e o terceiro representa 75% dos dados. Isso ocorre porque dividimos 100% dos dados por 4, obtendo 25%. Assim, a cada quartil, acumulamos 25%.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image094.jpg)

Para calcular o quartil em uma distribuição de frequência por classe e intervalos, seguimos alguns passos que são muito próximos ao cálculo realizado na mediana por classe. A diferença está no cálculo da posição que dividimos por 4, e em precisarmos indicar o quartil a ser calculado. Para calcular o quartil, aplicamos os passos seguintes: 

1. encontramos o valor de _N_ que é igual a soma das frequências;

2. calculamos a posição = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image095.png), onde i representa o quartil a ser calculado, assim i = 1, 2 ou 3;

3. calculamos a frequência acumulada (_fa_);

4. identificamos na frequência acumulada a posição calculada no passo 2 (sempre devemos buscar um valor igual ou maior que a posição calculada).

5. calculamos o quartil, utilizando a fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image096.png)

Já o percentil permite dividir a distribuição em cem partes iguais e é representado por _Pi,_ onde _i_ representa a ordem do percentil (1, 2, 3,...., 99). No diagrama a seguir, verificamos que cada percentil corresponde a 1% do conjunto de dados, pois dividimos 100% dos dados por 100, assim, a cada percentil, acumulamos 1%.

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image097.jpg)

A estrutura de cálculo para o percentil é exatamente igual ao do quartil, porém, temos uma modificação no cálculo da posição, pois estamos falando de 100 partes iguais:

- posição:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image098.png), onde i representa o percentil a ser calculado, assim _i_ = 1, 2,..., 99.

- fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image099.png)

**Exemplo 1**

Considere a seguinte distribuição que indica as faixas salariais, em salários mínimos, dos funcionários de uma determinada empresa. Calcule o coeficiente percentílico de curtose e interprete o resultado obtido indicando qual o tipo de curva de frequência temos nessa distribuição.

|**Salários**|**Nº de Funcionários**|
|---|---|
|02 \|--- 04|3|
|04 \|--- 06|6|
|06 \|--- 08|12|
|08 \|--- 10|6|
|10 \|---\| 12|3|

Para o cálculo, precisamos encontrar o quartil 1 e o 3, além do percentil 10 e do 90. Para calcular o quartil, seguimos os passos:

- quartil 1 (_Q1_):

1. encontramos o valor de _N_ que é igual à soma das frequências:

N = 30

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image100.png)

2.  calculamos a posição = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image095.png), onde _i_ representa o quartil a ser calculado, assim _i_ = 1, 2 ou 3. Como queremos calcular o 1º quartil, vamos substituir _i_ por 1:

Posição =![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image095.png)

Posição =![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image102.png)

3. calculamos frequência acumulada (_fa_):

|**Salários**|**Nº de Funcionários**|**_fa_**|
|---|---|---|
|02 \|--- 04|3|3|
|04 \|--- 06|6|9|
|06 \|--- 08|12|21|
|08 \|--- 10|6|27|
|10 \|---\| 12|3|30|
|Total|30||

4.  identificamos na frequência acumulada a posição calculada no passo 2. Sempre devemos buscar um valor igual ou maior que a posição calculada. Nesse caso, temos posição igual a 7,5 que identificamos na classe 2:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image103.png)

5. calculamos o quartil, utilizando a fórmula:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image096.png)

Classe: 04 |--- 06

Li = 04

A = 6 – 4 = 2

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image104.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image105.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image106.png)

Aplicando os mesmos passos encontramos o 3º quartil (Q3):

- quartil 3 (_Q3_):

1.   encontramos o valor de _N_, que é igual à soma das frequências:

N = 30

2.  calculamos a posição = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image095.png), onde _i_ representa o quartil a ser calculado, assim _i_ = 1, 2 ou 3. Como queremos calcular o 3º quartil, substituímos _i_ por 3:

Posição =![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image095.png)

Posição =![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image107.png)

3. calculamos a frequência acumulada (_fa_).

4.  identificamos na frequência acumulada a posição calculada no passo 2. Sempre devemos buscar um valor igual ou maior que a posição calculada. Nesse caso, temos posição igual a 22,5, que identificamos na classe 4:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image101-1.png)

5. calculamos o quartil, utilizando a fórmula:

Li = 08

A = 10 – 08 = 2

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image108.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image109.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image110.png)

Agora, precisamos calcular o percentil 10 e o 90 aplicando os mesmos passos do quartil. A única modificação está no cálculo da posição e na aplicação da fórmula:

- percentil 10 (_P10_):

Posição = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image098.png), onde _i_ representa o percentil a ser calculado. No nosso exemplo, usaremos _i = 10_:

Posição =![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image111.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image101.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image099.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image112.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image113.png)

- percentil 90 (_P90):_

Posição = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image098.png), onde _i_ é igual a 90:

Posição = ![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image114.png) 

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image101-1.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image099.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image115.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image116.png)

Com os valores do quartil e do percentil, aplicamos a fórmula para encontrar o coeficiente:

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image092.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image117.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image118.png)

Obtemos um coeficiente igual a 0,25. Assim, temos uma curva leptocúrtica.

**Exemplo 2**

Considere uma distribuição que apresente as medidas a seguir. Calcule o coeficiente percentílico de curtose e interprete o resultado obtido indicando o tipo de curva de frequência que temos nessa distribuição.

_Q1_ = 24,4 cm

_Q3_ = 41,2 cm

_P10_ = 20,2 cm

_P90_ = 49,5 cm

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image092.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image119.png)

![](https://conteudosdigitais.uninter.com/materiais/aulas//gradNova/2020/engComputacaoBach/probabilidadeEstatistica/a3/includes/html/impressao_arquivos/image120.png)

Obtivemos um coeficiente igual a 0,2867. Assim, temos uma distribuição platicúrtica.

# FINALIZANDO

Nesta aula, apresentamos as principais medidas de **dispersão**, seus cálculos, aplicações e interpretações dos resultados obtidos. Estudamos também as medidas de assimetria e a curtose.