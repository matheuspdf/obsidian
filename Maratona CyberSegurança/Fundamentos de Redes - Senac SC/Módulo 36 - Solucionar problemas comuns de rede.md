# 36.0 Introdução

## 36.0.1 Webster - Por que devo fazer este módulo?

Olá novamente e parabéns! Você alcançou o módulo final deste curso!

Halimah concluiu sua tarefa de projetar e configurar uma nova rede de filiais. Ela precisará testá-la e, se houver problemas, ela os diagnosticará e corrigirá. Eu também quero saber como testar, diagnosticar e corrigir problemas de rede. Ser capaz de fazer isso é um sinal claro de que você está pronto para se tornar um profissional de rede.

Vamos fazer isso juntos!

## 36.0.2 O que vou aprender neste módulo?

**Titulo do módulo:** Solucionar problemas comuns de rede

**Objetivo do módulo:** Solucionar problemas da conectividade básica de rede.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|O processo de solução de problemas|Descrever algumas das abordagens usadas para solucionar problemas de redes.|
|Problemas de camada física|Descrever o processo de detecção de problemas da camada física.|
|Solução de problemas de conectividade sem fio|Solucionar um problema de rede sem fio.|
|Problemas comuns de conectividade com a Internet|Explicar problemas comuns de conectividade com a Internet.|
|Apoio ao cliente|Explicar como usar fontes externas e recursos da Internet para solução de problemas.|

# 36.1 O Processo de Solução de Problemas

## 36.1.1 Vídeo - Solução de problemas de rede

**Selecione o botão Reproduzir para assistir o vídeo.**

Uma das melhores maneiras de aprender e entender qualquer tópico é solucionar problemas. Para um profissional de rede em qualquer nível, a solução de problemas é uma oportunidade para aprofundar os protocolos e tecnologias envolvidas na tentativa de resolver o problema. As configurações incorretas e os erros de cabeamento acontecem. Mas esses tipos de erros geralmente são detectados logo no início durante a verificação. Encontrar o problema normalmente envolve uma abordagem sistemática para encontrar a origem do problema. Isso inclui descobrir quais dispositivos podem comunicar-se entre si, e quais não podem.

Por exemplo, e se o usuário do PC 1 submeter um tíquete de suporte que ele não consegue mais acessar dispositivos na Internet, como www.example.com. Há várias coisas que podemos fazer para isolar o problema, além de entrar em contato com outros usuários para ver se estão enfrentando problemas semelhantes. Mas vamos ver o que podemos fazer com o PC1.

Usamos o comando IP config no PC 1 para verificar as informações de endereçamento IP é o que esperamos ver. Tudo funciona bem. Em seguida, vamos ver se um PC pode alcançar outros dispositivos no mesmo switch. Do PC um, fazemos ping no endereço IPv4 do PC dois e descobrir que os pings são bem-sucedidos. Em seguida, tentamos fazer o ping do endereço IPv4 para seu default gateway, o roteador, 192.168.1.1, esses pings são malsucedidos. Tentamos fazer o ping para outros dispositivos em nossa rede como os servidores DNS e DHCP e isso também prova ser malsucedido.

Ao fazer alguns testes adicionais, notamos que nenhum dos dispositivos no switch pode alcançar dispositivos no switch 2 ou acesse a Internet. Entretanto, os dispositivos no switch dois podem alcançar Internet, mas não conseguem se comunicar com dispositivos no switch 1. Parece que nosso problema está entre switch um e switch dois.

Fazendo alguma investigação adicional, determinamos que o problema é uma porta com defeito no switch usada para conectar switch 1 ao switch dois. Movendo o cabo para outra porta no switch 1 corrige o problema e a acessibilidade total é restaurada. Marcamos a porta como defeituosa e atualizamos o tíquete de suporte.

## 36.1.2 Visão geral da solução de problemas de rede

A resolução de problemas é o processo de identificar, localizar e corrigir problemas. Os indivíduos experientes confiam no instinto para solucionar problemas. Entretanto, há técnicas estruturadas que podem ser usadas para determinar a causa mais provável e a solução.

Na solução de problemas, a documentação apropriada deve ser mantida. Esta documentação deve incluir o máximo de informações possível sobre o seguinte:

- O problema encontrado
- As etapas seguidas para determinar a causa do problema
- As etapas para corrigir o problema e garantir que ele não ocorra novamente

Documente todas as etapas seguidas na solução de problemas, até mesmo as etapas que não resolveram o problema. Essa documentação torna-se uma referência importante quando o mesmo problema ou um problema semelhante ocorre novamente. Mesmo em uma rede residencial pequena, uma documentação adequada pode ajudar a economizar tempo e lembrar como um problema foi corrigido no passado.

![[Pasted image 20260701205704.png]]


## 36.1.3 Reunir Informações

Quando um problema é detectado pela primeira vez na rede, é importante verificá-lo e determinar a dimensão da rede afetada pelo problema. Quando o problema é confirmado, a primeira etapa na solução de problemas é coletar informações. O checklist a seguir apresenta algumas informações importantes que você deve verificar.

**Natureza do problema**

- Relatórios do usuário final
- Relatório de verificação do problema

**Equipamento**

- Fabricante
- Marca/modelo
- Versão de firmware
- Versão do sistema operacional
- Informações sobre propriedade/garantia

**Configuração e topologia**

- Topologia física e lógica
- Arquivos de configuração
- Arquivos de log

**Solução de problemas anterior**

- Passos dados
- Resultados alcançados

Uma das primeiras formas de coletar informações é fazer perguntas a todos os usuários que reportaram o problema, bem como a outros usuários afetados. As perguntas podem incluir a experiência do usuário final, sintomas observados, mensagens de erro e informações sobre mudanças recentes de configuração em dispositivos ou aplicativos.

Em seguida, reúna informações sobre todos os equipamentos que podem ser afetados. Essas informações podem ser obtidas na documentação. Também são necessárias uma cópia de todos os arquivos de log e uma lista de todas as alterações recentes nas configurações de equipamentos. Os arquivos de log são gerados pelo próprio equipamento e normalmente são fornecidos pelo software de gerenciamento. Outras informações sobre o equipamento incluem o fabricante, a marca e o modelo dos dispositivos afetados, além de informações de propriedade e garantia. A versão do firmware ou software no dispositivo também é importante porque pode haver problemas de compatibilidade com plataformas de hardware específicas.

As informações sobre a rede também podem ser obtidas com as ferramentas de monitoramento de rede. As ferramentas de monitoramento de rede são aplicativos complexos muito usados em redes grandes para coletar continuamente informações sobre o estado e os dispositivos de rede. Essas ferramentas podem não estar disponíveis para redes menores.

Quando todas as informações necessárias forem coletadas, inicie o processo de solução de problemas.

## 36.1.4 Métodos Estruturados de Solução de Problemas

Existem várias abordagens estruturadas de solução de problemas que podem ser usadas. Qual usar dependerá da situação. Cada abordagem tem suas vantagens e desvantagens. Este tópico descreve métodos e fornece diretrizes para escolher o melhor método para uma situação específica.

**Clique em cada botão para obter uma descrição das diferentes abordagens de solução de problemas que podem ser usadas.**

### **Bottom-Up**

Na solução de problemas de baixo para cima, você começa com os componentes físicos da rede e sobe pelas camadas do modelo OSI até que a causa do problema seja identificada, conforme mostrado na figura.

A identificação e solução de problemas bottom-up é um bom método a ser usado quando há suspeita de que o problema seja físico. A maioria dos problemas de rede reside nos níveis inferiores, portanto, a implementação da abordagem bottom-up é frequentemente eficaz.

A desvantagem da abordagem de identificação e solução de problemas bottom-up é o fato de que ela requer a verificação de todos os dispositivos e interfaces na rede, até encontrar a possível causa do problema. Lembre-se de que todas as conclusões e possibilidades devem ser documentadas, portanto, essa abordagem pode gerar muita papelada. Um desafio ainda maior consiste em determinar quais dispositivos começar a examinar primeiro.

![[Pasted image 20260701205737.png]]

### **Top-Down**

Na figura, a solução de problemas de cima para baixo começa com os aplicativos do usuário final e desce pelas camadas do modelo OSI até que a causa do problema seja identificada.

Os aplicativos de usuário final de um sistema final são testados antes da abordagem das partes de rede mais específicas. Use essa abordagem para problemas mais simples ou quando você achar que o problema está em um componente de software.

A desvantagem da abordagem top-down é que ela requer a verificação de todos os aplicativos de rede até que seja encontrada a causa possível do problema. É necessário documentar todas as conclusões e possibilidades. O desafio é determinar qual aplicativo começar a examinar primeiro.
![[Pasted image 20260701205751.png]]


### **Divide-and-conquer (Dividir para conquistar)**

A figura mostra a abordagem de dividir e conquistar para solucionar um problema de rede.

O administrador de rede seleciona uma camada e testa em ambos os sentidos a partir dessa camada.

Na identificação e solução de problemas divide-and-conquer, você começa com a coleta das experiências do usuário em relação ao problema, documenta os sintomas e depois, de posse dessas informações, faz uma dedução inteligente sobre em qual camada OSI começar a investigação. Após a confirmação do funcionamento correto de uma camada, é possível pressupor que as camadas abaixo estejam funcionando. O administrador pode trabalhar as camadas OSI desse ponto para cima. Se uma camada não estiver funcionando da forma correta, o administrador pode aplicar o modelo de camada OSI.

Por exemplo, se os usuários não puderem acessar o Servidor Web, mas puderem fazer ping no Servidor, o problema está acima da camada 3. Se o ping no Servidor não for bem-sucedido, o problema provavelmente estará em uma camada OSI inferior.
![[Pasted image 20260701205808.png]]


### **Siga o caminho**

Esta é uma das técnicas de solução de problemas mais básicas. A abordagem primeiro descobre o caminho de tráfego real da origem até o destino. O escopo da solução de problemas é reduzido apenas para os links e dispositivos que estão no caminho de encaminhamento. O objetivo é eliminar os links e dispositivos que são irrelevantes para a tarefa de solução de problemas em mãos. Esta abordagem geralmente complementa uma das outras abordagens.


### **Substituição**

Essa abordagem também é chamada de troca do componente porque você troca fisicamente o dispositivo problemático por um conhecido e funcional. Se o problema for resolvido, o problema será com o dispositivo removido. Se o problema continuar, a causa poderá estar em qualquer outro ponto.

Em situações específicas, esse pode ser um método ideal para a rápida resolução de problemas, como em um único ponto crítico de falha. Por exemplo, um roteador de borda desce. Pode ser mais benéfico substituir o dispositivo e restaurar o serviço, em vez de solucionar o problema.

Se o problema estiver em vários dispositivos, talvez não seja possível isolar corretamente o problema.


### **Por Pequenas e Médias Empresas**

Esta abordagem também é chamada de abordagem spot-the-differences e tenta resolver o problema alterando os elementos não operacionais para ser consistente com os que trabalham. Você compara configurações, versões de software, hardware ou outras propriedades de dispositivo, links ou processos entre situações de trabalho e não funcionando e detecta diferenças significativas entre elas.

A fraqueza desse método é que ele pode levar a uma solução funcional, sem revelar claramente a causa raiz do problema.


### **Adivinhe Educado**

Essa abordagem também é chamada de abordagem de solução de problemas de tiroteio do quadril. Este é um método de solução de problemas menos estruturado que usa um palpite educado com base nos sintomas do problema. O sucesso desse método varia de acordo com sua experiência e capacidade de solução de problemas. Técnicos experientes são mais bem-sucedidos porque podem confiar em seu amplo conhecimento e experiência para isolar e resolver decisivamente problemas de rede. Com um administrador de rede menos experiente, esse método de identificação e solução de problemas pode ser mais aleatório.


## 36.1.5 Diretrizes para selecionar um método de solução de problemas

Para resolver rapidamente problemas de rede, selecione o método de identificação e solução de problemas de rede mais eficaz.

A figura ilustra qual método pode ser usado quando um determinado tipo de problema é descoberto.
![[Pasted image 20260701205935.png]]

Por exemplo, problemas de software geralmente são resolvidos usando uma abordagem de cima para baixo, enquanto problemas baseados em hardware são resolvidos usando a abordagem de baixo para cima. Novos problemas podem ser resolvidos por um técnico experiente usando o método dividir e conquistar. Caso contrário, pode ser utilizada a abordagem ascendente.

Solução de problemas é uma habilidade que é desenvolvida ao fazê-lo. Cada problema de rede que você identifica e resolve aumenta seu conjunto de habilidades


## 36.1.6 Verifique a sua compreensão - O Processo de solução de problemas

**Verifique sua compreensão sobre processo de solução de problemas escolhendo a resposta correta para as seguintes perguntas.**
### Pergunta 1

Medhat não consegue se conectar a um site na internet. Para iniciar a solução de problemas, ele primeiro testa a conectividade de rede. Se isso falhar, ele descerá as camadas até o meio físico. Se os testes de conectividade de rede forem bem-sucedidos, ele trabalhará para solucionar os problemas do software do aplicativo. Qual método de solução de problemas estruturado a Medhat está usando?

- [ ] Bottom-Up
- [ ] Top-Down
- [x] Divide-and-conquer (Dividir para conquistar)
- [ ] Siga o caminho
- [ ] Substituição
- [ ] Por Pequenas e Médias Empresas
- [ ] Adivinhe Educado

✅ RESPOSTA CORRETA: Divide-and-conquer (Dividir para conquistar)

> Está certo. O Medhat está usando o método de solução de problemas de dividir-e-conquistar na camada 3.

### Pergunta 2

Patti está solucionando um problema na rede. Com base em sua experiência anterior com situações semelhantes, ela supõe que o problema é uma configuração de IP incorreta e começa a solução do problema com isso. Qual método de solução de problemas estruturado a Patti está usando?

- [ ] Bottom-Up
- [ ] Top-Down
- [ ] Divide-and-conquer (Dividir para conquistar)
- [ ] Siga o caminho
- [ ] Substituição
- [ ] Por Pequenas e Médias Empresas
- [x] Adivinhe Educado

✅ RESPOSTA CORRETA: Adivinhe Educado

> Está certo. Patti tem experiência anterior com problemas semelhantes; portanto, ela está usando o método de solução de problemas fundamentado.

### Pergunta 3

Allan entra em contato com o provedor de serviços de Internet para reclamar de problemas de conexão. Ele não sabe qual é problema. O provedor de serviços de Internet envia um novo modem pré-configurado para Allan na esperança de resolver a situação. Qual método de solução de problemas estruturado o ISP está usando?

- [ ] Bottom-Up
- [ ] Top-Down
- [ ] Divide-and-conquer (Dividir para conquistar)
- [ ] Siga o caminho
- [x] Substituição
- [ ] Por Pequenas e Médias Empresas
- [ ] Adivinhe Educado

✅ RESPOSTA CORRETA: Substituição

> Está certo. Ao enviar um novo modem e esperar que ele resolva o problema, o ISP está usando o método de solução de problemas de substituição.

### Pergunta 4

Qual método estruturado de solução de problemas deve ser usado quando ocorre um problema orientado por software?

- [ ] Bottom-Up
- [x] Top-Down
- [ ] Divide-and-conquer (Dividir para conquistar)
- [ ] Siga o caminho
- [ ] Substituição
- [ ] Por Pequenas e Médias Empresas
- [ ] Adivinhe Educado

✅ RESPOSTA CORRETA: Top-Down

> Está certo. A abordagem de solução de problemas de cima para baixo deve ser usada quando ocorre um problema orientado por software.

### Pergunta 5

Qual método estruturado de solução de problemas deve ser usado quando um problema de cabeamento é suspeito?

- [x] Bottom-Up
- [ ] Top-Down
- [ ] Divide-and-conquer (Dividir para conquistar)
- [ ] Siga o caminho
- [ ] Substituição
- [ ] Por Pequenas e Médias Empresas
- [ ] Adivinhe Educado

✅ RESPOSTA CORRETA: Bottom-Up

> Está certo. A abordagem ascendente deve ser utilizada quando se suspeita de um problema de cabeamento.

### Pergunta 6

Qual método de solução de problemas estruturado tenta localizar o problema em um dispositivo ou link entre a origem e o destino?

- [ ] Bottom-Up
- [ ] Top-Down
- [ ] Divide-and-conquer (Dividir para conquistar)
- [x] Siga o caminho
- [ ] Substituição
- [ ] Por Pequenas e Médias Empresas
- [ ] Adivinhe Educado

✅ RESPOSTA CORRETA: Siga o caminho

> Está certo. A abordagem de seguir-o-caminho descobre o caminho de tráfego real entre a origem e o destino e, em seguida, tenta eliminar os links e dispositivos que são irrelevantes para a tarefa de solução de problemas em Pergunta.

### Pergunta 7

Qual método estruturado de solução de problemas tenta resolver o problema alterando elementos no dispositivo ou configuração com problema para ser consistente com um em funcionamento?

- [ ] Bottom-Up
- [ ] Top-Down
- [ ] Divide-and-conquer (Dividir para conquistar)
- [ ] Siga o caminho
- [ ] Substituição
- [x] Por Pequenas e Médias Empresas
- [ ] Adivinhe Educado

✅ RESPOSTA CORRETA: Por Pequenas e Médias Empresas

> Está certo. O método de comparação tenta usar um dispositivo ou configuração em funcionamento como modelo para corrigir um problema no dispositivo ou configuração com problema.


# 36.2 Problemas de camada física

## 36.2.1 Problemas Comuns da Camada 1

Grande parte dos problemas de rede está relacionada a problemas ou componentes físicos com a camada física. Os problemas físicos dizem respeito principalmente aos aspectos de hardware de computadores e dispositivos de rede, e aos cabos que os interligam. Os problemas físicos não incluem a configuração lógica (software) dos dispositivos.

Lembre-se, a camada física (Camada 1) lida com a conectividade física dos dispositivos de rede. Alguns dos problemas mais comuns da camada 1 incluem o seguinte:

- Dispositivo desligado
- Dispositivo desconectado
- Conexões de cabo de rede soltas
- Tipo incorreto de cabo
- Falha no cabo de rede
- Falha no access point sem fio

Para solucionar problemas na camada 1, primeiro verifique se todos os dispositivos têm a alimentação adequada e se os dispositivos estão ligados. Pode parecer uma solução óbvia, mas muitas vezes a pessoa que relata o problema pode ignorar um dispositivo que está no caminho de rede da origem para o destino. Verifique se não há erros em qualquer LED que exibe o status de conectividade. Se estiver no local, inspecione visualmente todos os cabos de rede e reconecte-os para garantir uma conexão apropriada. Se houver problemas na conexão sem fio, verifique se o access point sem fio está funcionando e se as configurações sem fio estão corretas.

**Clique abaixo para aprender mais sobre como usar os cinco sentidos na solução de problemas.**


### Visão

A visão é usada para detectar problemas, como cabos conectados incorretamente ou de qualidade inferior:

- Cabos que não estão conectados
- Cabos conectados à porta incorreta
- Conexões de cabo soltas
- Cabos e conectores danificados
- Uso do tipo incorreto de cabo

A visão também permite ver a condição e a função de vários dispositivos de rede com LEDs.

### Os sentidos do olfato e do paladar

O olfato pode alertar os solucionadores de problemas sobre componentes que estão superaquecendo. O cheiro de isolante ou componentes queimados é bastante característico e aponta para um problema muito sério.

O paladar está diretamente relacionado ao olfato, pois ambos usam os mesmos receptores. Você também pode provar a acidez de algo que queima.

### Tato
Com o toque, os solucionadores de problemas podem sentir os componentes superaquecidos e detectar problemas mecânicos em dispositivos, como ventiladores. Geralmente, esses dispositivos criam uma pequena vibração no componente que pode ser detectada pelo toque. A ausência dessa vibração ou a presença de vibração excessiva pode indicar possíveis falhas no ventilador.

### Audição
A audição é usada para detectar problemas sérios, como os de origem elétrica, e a operação adequada de ventiladores e unidades de disco. Todos os dispositivos têm sons característicos. Qualquer mudança no som produzido normalmente indica um tipo de problema.

## 36.2.2 LEDs de Roteadores sem fio

Independentemente da falha estar na rede sem fio ou com fio, uma das primeiras etapas em uma estratégia ascendente de solução de problemas deve ser examinar os LEDs, que indicam o estado ou a atividade atual de um equipamento ou de uma conexão. LEDs podem mudar de cor ou piscar para transmitir informações. A configuração exata e o significado dos LEDs variam entre fabricantes e dispositivos. A figura mostra um roteador sem fio típico com LEDs, incluindo os de energia, sistema, WLAN, portas com fio e Internet (rotulada como WAN na figura), USB e Quick Security Setup (QSS, também conhecido como Configuração de Wi-Fi Protegida [WPS]).

**Nota**: O WPS ou o QSS têm vulnerabilidades conhecidas que permitem que um agente de ameaças obtenha acesso à sua rede. Portanto, é uma prática recomendada de segurança desabilitar esse recurso. Consulte a documentação para saber como desabilitar o WPS ou QSS.

![[Pasted image 20260701210611.png]]

Em alguns dispositivos, um único LED pode transmitir várias informações dependendo do status atual do dispositivo. É importante verificar a documentação do equipamento para o significado exato de todos os indicadores, mas existem alguns pontos em comum.

A maioria dos dispositivos terá LEDs de atividade, que geralmente são chamados de luzes de link. Uma condição normal é que esses LEDs pisquem indicando que o tráfego está fluindo pela porta. Uma luz verde sólida normalmente indica que um dispositivo está conectado à porta, mas nenhum tráfego está fluindo. Nenhuma luz indica normalmente um ou mais dos seguintes itens:

- Nada está conectado à porta.
- Há um problema com a conexão com ou sem fio.
- Um dispositivo ou uma porta falhou.
- Há um problema de cabeamento.
- O roteador sem fio está configurado incorretamente, por exemplo, uma porta foi desligada administrativamente.
- O roteador sem fio tem uma falha de hardware.
- O dispositivo não tem energia.

Se for uma rede com fio ou sem fio, verifique se o dispositivo e as portas estão funcionando para não perder tempo com tentativas de solução de problemas.


## 36.2.3 Problemas de cabeamento

Se o cliente com fio não puder se conectar ao roteador sem fio, será necessário verificar a conectividade física e o cabeamento. O cabeamento é o sistema central de redes com fio e um dos problemas mais comuns quando há inatividade.

Existem diversos problemas relacionados ao cabeamento:

- Utilize o tipo de cabo correto. Dois tipos de cabos UTP são geralmente encontrados em redes: cabos diretos (straight-through) e cabos cruzados. O uso do tipo de cabo incorreto pode impedir a conectividade.
- A terminação de cabo inadequada é um dos principais problemas encontrados em redes. Para evitar isso, os cabos devem ser terminados de acordo com os padrões. Termine cabos com o padrão de terminação T568A ou T568B. Evite destrançar os pares de fios na terminação. Comprima os conectores no cabo de revestimento para fornecer o alívio de tensão.
- Os comprimentos máximos de cabo são definidos pelas características de diferentes cabos. Exceder esses comprimentos pode causar um impacto negativo no desempenho da rede.
- Se há problema na conectividade, verifique se as portas corretas estão sendo usadas entre os dispositivos de rede.
- Proteja cabos e conectores de danos físicos. Use suporte de cabos para evitar a sobrecarga em conectores e coloque os cabos em áreas que não fiquem no caminho.

![[Pasted image 20260701210630.png]]


## 36.2.4 Verifique sua compreensão - Problemas da camada física

**Verifique sua compreensão sobre problemas da camada física escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

O que NÃO é considerado um problema da camada física?

- [ ] energia do dispositivo desligada ou desconectada
- [ ] cabo solto ou incorreto
- [x] configuração Sem Fio
- [ ] falha no cabo de rede
- [ ] falha no access point sem fio

✅ RESPOSTA CORRETA: configuração Sem Fio

> Está certo. A configuração sem fio é normalmente feita em software, o que não é um problema da camada física.

### Pergunta 2

Quais sentidos normalmente alertam os técnicos de que os componentes estão superaquecendo? (Escolha três.)

- [ ] Visão
- [x] Olfato
- [x] Paladar
- [x] Tato
- [ ] Audição

✅ RESPOSTA CORRETA: Olfato; Paladar; Tato

> Está certo. O olfato e tato podem alertar os solucionadores de problemas sobre componentes que estão superaquecendo.

### Pergunta 3

Verdadeiro ou falso? Uma luz de LED que não está acesa em uma porta significa que não há tráfego.

- [x] verdadeiro
- [ ] false

✅ RESPOSTA CORRETA: verdadeiro

> Está certo. A resposta correta é verdadeira. Uma luz de LED que não está acesa pode indicar vários problemas diferentes. Mas em uma porta, isso significa que não há tráfego.


# 36.3 Solucionar problemas de redes sem fio

## 36.3.1 Causas de problemas sem fio

Devido a problemas de conectividade sem fio, o cliente sem fio não pode se conectar ao AP. A comunicação sem fio depende dos sinais de radiofrequência (RF) para transportar dados. Diversos fatores podem afetar nossa capacidade de conexão com hosts que utilizam RF:

- Nem todos os padrões sem fio são compatíveis. O 802.11ac (banda de 5 GHz) não é compatível com os padrões 802.11b/g/n (banda de 2,4 GHz). Na banda de 2,4 GHz, cada padrão usa uma tecnologia diferente. A menos que seja especificamente configurado, o equipamento que está em conformidade com um padrão talvez não funcione com um equipamento que está em conformidade com outro padrão. Na figura, a rede de 2,4 GHz está configurada para oferecer suporte a dispositivos antigos.
- Cada conversação sem fio deve ocorrer em um canal separado sem sobreposição. Alguns dispositivos AP podem ser configurados para selecionar o canal menos congestionado ou o de mais alta produtividade. Embora as configurações automáticas funcionem, a configuração manual do canal AP fornece maior controle e pode ser necessária em alguns ambientes.
- A intensidade de um sinal RF diminui com a distância. Se a intensidade do sinal for muito baixa, os dispositivos não serão capazes de associar e mover dados de maneira confiável. O sinal pode ser removido. O utilitário de cliente NIC pode ser usado para exibir a intensidade do sinal e a qualidade da conexão.
- Os sinais RF são suscetíveis a interferências de fontes externas, inclusive de outros dispositivos que operam na mesma frequência. Uma pesquisa no local deve ser feita para detectar essas interferências.
- APs compartilham a largura de banda disponível entre dispositivos. Quanto mais dispositivos forem associados ao AP, a largura de banda para cada dispositivo individual diminuirá, causando problemas de desempenho de rede. A solução é reduzir o número de clientes sem fio que usa cada canal.
![[Pasted image 20260701213501.png]]

## 36.3.2 Erros de autenticação e associação

As WLANs modernas incorporam várias tecnologias para ajudar a proteger os dados na WLAN. A configuração incorreta de qualquer um deles pode impedir a comunicação. Algumas das configurações mais comuns definidas de forma incorreta incluem: SSID, autenticação e criptografia.

- O SSID é uma string alfanumérica que diferencia maiúsculas e minúsculas até 32 caracteres. Deve corresponder ao AP e ao cliente. Se o SSID for transmitido e detectado, isso não será um problema. Se o SSID não for transmitido, deverá ser inserido manualmente no campo do cliente. Caso o cliente esteja configurado com o SSID incorreto, ele não será associado ao AP. Além disso, quando outro AP está presente e transmite o SSID, o cliente pode se associar automaticamente a esse AP.
- Na maioria dos APs, a autenticação aberta é configurada por padrão, permitindo que todos os dispositivos sejam conectados. Se uma forma mais segura de autenticação for configurada, uma chave será necessária. O cliente e o AP devem ser configurados com a mesma chave. Se as chaves não coincidirem, haverá falha na autenticação e os dispositivos não serão associados.
- Criptografia é o processo que modifica os dados de forma que não sejam usados por qualquer pessoa sem a chave de criptografia adequada. Se a criptografia for ativada, a mesma chave de criptografia deverá ser configurada no AP e no cliente. Caso o cliente seja associado ao AP, mas não puder enviar ou receber dados, a chave de criptografia pode ser o problema.
![[Pasted image 20260701213517.png]]


## 36.3.3 Packet Tracer - Solucionar problemas de uma conexão sem fio

Nesta atividade, você receberá um cenário. Você vai determinar o motivo pelo qual um cliente em rede sem fio não consegue se conectar a um roteador sem fio e não pode corrigir o problema.

# 36.4 Problemas comuns de conectividade com a Internet

## 36.4.1 Erros de configuração do servidor DHCP

Se a conexão física com o host com fio ou sem fio parecer estar se conectando conforme o esperado, mas o host não puder se comunicar em redes remotas ou na Internet, verifique a configuração de IP do cliente.

A configuração de IP pode ter um grande impacto na capacidade de conexão de um host com a rede. Um roteador sem fio atua como um servidor DHCP para clientes locais com e sem fio e fornece configuração de IP, incluindo o endereço IP, máscara de sub-rede, gateway padrão e, geralmente, os endereços IP dos servidores DNS. O servidor DHCP vincula o endereço IP a um endereço MAC do cliente e armazena essas informações em uma tabela de clientes. Geralmente, é possível visualizar essa tabela com a GUI de configuração incluída no roteador.

As informações da tabela do cliente devem corresponder às informações do host local, que você pode ver usando o comando **ipconfig /all**. Além disso, o endereço IP no cliente deve estar na mesma rede que a interface LAN do roteador sem fio. A interface da LAN do roteador sem fio deve ser definida como o gateway padrão. Se as informações de configuração do cliente não estiverem de acordo com as informações da tabela do cliente, o endereço deve ser liberado (**ipconfig /release**) e renovado (**ipconfig /renew**) para formar uma nova ligação.

Na maioria dos casos, o roteador sem fio recebe seu próprio endereço IP pelo DHCP no ISP. Verifique se o roteador tem um endereço IP e tente liberar e renovar o endereço com o utilitário da GUI.

![[Pasted image 20260701213637.png]]


## 36.4.2 Verifique a Configuração da Internet

Se os hosts na rede local com e sem fio puderem se conectar ao roteador sem fio e a outros hosts na rede local, mas não à Internet, talvez o problema esteja na conexão entre o roteador e o ISP.

```
C:∖> ping 10.18.32.12
Pinging 10.18.32.12 with 32 bytes of data:
Request timed out.
Request timed out.
Request timed out.
Request timed out.

Ping statistics for 10.18.32.12:
     Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
```

![[Pasted image 20260701213708.png]]

Há muitas maneiras de verificar a conectividade entre o roteador e o ISP. Usando a GUI, uma forma de verificar a conectividade é examinar a página de status do roteador. Como mostrado na figura, ele deve mostrar o endereço IP atribuído pelo ISP (64.100.0.11 neste exemplo).

![[Pasted image 20260701213718.png]]

Se esta página mostrar a ausência de conexão, o roteador sem fio não poderá ser conectado. Verifique todas as conexões físicas e os indicadores LED. Se o DSL ou o modem a cabo for um dispositivo separado, verifique também as conexões e os indicadores. Caso o ISP solicite um nome de login ou uma senha, verifique se coincidem com os dados fornecidos pelo ISP. Usando a GUI, as configurações de senha podem aparecer na página de configuração. Em seguida, tente restabelecer a conectividade ao clicar no botão para conectar ou renovar o endereço IP na página de status. Se o roteador sem fio ainda não estiver conectado, entre em contato com o ISP para saber se o problema é do próprio ISP.


## 36.4.3 Verifique as configurações do Firewall

Se as Camadas 1 a 3 estiverem funcionando normalmente e você puder fazer ping com êxito no endereço IP do servidor remoto, verifique as camadas superiores. Por exemplo, caso um firewall de rede seja usado ao longo do caminho, é importante verificar se a porta TCP ou UDP do aplicativo está aberta e nenhuma lista de filtros está bloqueando o tráfego nessa porta.

Quando todos os clientes têm a configuração de IP correta e podem se conectar ao roteador sem fio, mas não conseguem fazer ping entre eles nem acessar um servidor remoto ou aplicativo, talvez exista um problema nas regras do roteador. Verifique todas as configurações no roteador para garantir que nenhuma restrição de segurança está causando o problema. Verifique se os firewalls locais nos dispositivos clientes não estão impedindo a funcionalidade de rede.

![[Pasted image 20260701213739.png]]

## 36.4.4 Verifique sua compreensão - Problemas comuns de conectividade com a Internet

**Verifique sua compreensão sobre problemas comuns de conectividade com a Internet escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Se sua conexão física estiver funcionando conforme o esperado, mas ainda houver um problema, qual seria o próximo passo?

- [x] Verifique a configuração de IP.
- [ ] Ligue para seu ISP.
- [ ] Reinicie todos os dispositivos na rede.
- [ ] Desconecte os cabos e conecte-os novamente.

✅ RESPOSTA CORRETA: Verifique a configuração de IP.

> Está certo. Caso a conexão física com o host (com fio ou sem fio) seja estabelecida conforme o esperado, verifique a configuração de IP do cliente.

### Pergunta 2

Qual comando você pode usar para pedir ao servidor DHCP para atualizar sua configuração de endereçamento IP?

- [ ] ping
- [ ] netstat
- [x] ipconfig /renew
- [ ] tracert
- [ ] nslookup

✅ RESPOSTA CORRETA: ipconfig /renew

> Está certo. Use os comandos ipconfig /release e ipconfig /renew para liberar e atualizar sua configuração de endereçamento IP.

### Pergunta 3

Qual é a causa mais provável se você conseguir fazer ping em vários sites na Internet, mas não conseguir abrir páginas da Web?

- [ ] Configuração do DHCP
- [ ] Configuração de endereçamento IP
- [ ] Configuração do servidor da Web
- [x] Configuração do firewall

✅ RESPOSTA CORRETA: Configuração do firewall

> Está certo. Se todas as Camadas 1 a 3 parecem estar operando normalmente e você pode executar ping com sucesso no endereço IP do servidor remoto, verifique a configuração do firewall. Também pode haver um problema de DNS.


## 36.4.5 Dividir-e-Conquistar com ping

Os problemas de conectividade ocorrem em redes sem fio, em redes com fio e em redes que usam ambas as conexões. Na solução de problemas de uma rede que tem conexões com e sem fio, é melhor usar uma técnica dividir-para-conquistar para isolar o problema na rede cabeada ou na rede sem fio. A maneira mais fácil de determinar se o problema está na rede com fio ou sem fio é a seguinte:

- Faça um ping do cliente sem fio para o gateway padrão. Isso verifica se o cliente sem fio está se conectando conforme o esperado.
- Faça um ping do cliente com fio para o gateway padrão. Isso verifica se o cliente com fio está se conectando conforme o esperado.
- Faça ping do cliente sem fio para um cliente com fio. Isso verifica se o roteador sem fio está funcionando conforme o esperado.

Depois de isolado, o problema pode ser corrigido.

![[Pasted image 20260701213905.png]]


## 36.4.6 O comando tracert

Embora o **ping** seja o comando de solução de problemas de rede mais usado, existem outros comandos úteis disponíveis em dispositivos Windows.

O comando **ping** pode verificar a conectividade de ponta a ponta. No entanto, se houver um problema e o dispositivo não conseguir executar ping no destino, o comando **ping** não indicará onde a conexão foi realmente interrompida. Para fazer isso, outro comando conhecido como **traceroute** ou **tracert** deve ser usado. O Microsoft Windows usa o comando **tracert**, enquanto outros sistemas operacionais geralmente usam o comando **traceroute**.

O utilitário **tracert** fornece informações de conectividade sobre o caminho que um pacote percorre para chegar ao destino e sobre cada roteador (salto) ao longo do caminho. Indica o tempo que um pacote leva da origem até cada salto e retorno (tempo de ida e volta). O utilitário **tracert** pode ajudar a identificar onde um pacote pode ter sido perdido ou atrasado devido a gargalos ou lentidão na rede.

Na figura, o usuário está seguindo o caminho para a Cisco. O caminho é exclusivo para este usuário. Seu caminho terá uma lista diferente de saltos e pode ser mais curto ou mais longo (número de saltos).

**Observação**: observe na saída que o segundo salto falhou. Isso provavelmente se deve a uma configuração de firewall nesse dispositivo que não permite responder a pacotes do comando **tracert**. No entanto, o dispositivo encaminha os pacotes para o próximo salto.

```
C:∖> tracert www.cisco.com

Tracing route to e2867.dsca.someispedge.net [104.95.63.78]
over a maximum of 30 hops:

   1     1 ms     1 ms       <1 ms      10.10.10.1
   2     *        *           *         Request timed out.
   3     8 ms     8 ms        8 ms      24-155-250-94.dyn.yourisp.net [172.30.250.94]
   4     22 ms    23 ms      23 ms      24-155-121-218.static.yourisp.net [172.30.121.218]
   5     23 ms    24 ms      25 ms      dls-b22-link.anotherisp.net [64.0.70.170]
   6     25 ms    24 ms      25 ms      dls-b23-link.anotherisp.net [192.168.137.106]
   7     24 ms    23 ms      21 ms      someisp-ic-341035-dls-b1.c.anotherisp.net [192.168.169.47]
   8     25 ms    24 ms      23 ms      ae3.databank-dfw5.netarch.someisp.com [10.250.230.195]
   9     25 ms    24 ms      24 ms      a104-95-63-78.deploy.static.someisptechnologies.com [104.95.63.78]

Trace complete.

C:">
```

O utilitário **tracert** básico só permite até 30 saltos entre um dispositivo de origem e de destino antes de assumir que o destino é inacessível. Esse número é ajustável usando o parâmetro **-h**. Outros modificadores, exibidos como opções na figura, também estão disponíveis.

```
C:∖> tracert

Usage: tracert [-d] [-h maximum_hops] [-j host-list] [-w timeout]
               [-R] [-S srcaddr] [-4] [-6] target_name

Options:
    -d                    Do not resolve addresses to hostnames.
    -h maximum_hops       Maximum number of hops to search for target.
    -j host-list          Loose source route along host-list (IPv4-only).
    -w timeout            Wait timeout milliseconds for each reply.
    -R                    Trace round-trip path (IPv6-only).
    -S srcaddr            Source address to use (IPv6-only).
    -4                    Force using IPv4.
    -6                    Force using IPv6.

C:∖>
```

## 36.4.7 O Comando netstat

Às vezes é necessário conhecer quais conexões TCP ativas estão abertas e sendo executadas em um host de rede. O comando **netstat** é um importante utilitário de rede que pode ser usado para verificar essas conexões. Conforme mostrado no exemplo, o comando **netstat** lista o protocolo em uso, o endereço local e o número da porta, o endereço externo e o número da porta e o estado da conexão.

```
C:∖> netstat

Active Connections

   Proto     Local Address          Foreign Address          State
   TCP       10.10.10.130:58520     dfw28s01-in-f14:https    ESTABLISHED
   TCP       10.10.10.130:58522     dfw25s25-in-f14:https    ESTABLISHED
   TCP       10.10.10.130:58523     dfw25s25-in-f14:https    ESTABLISHED
   TCP       10.10.10.130:58525     ec2-3-13-132-189:https   ESTABLISHED
   TCP       10.10.10.130:58579     203.104.160.12:https     ESTABLISHED
   TCP       10.10.10.130:58580     104.16.249.249:https     ESTABLISHED
   TCP       10.10.10.130:58624     52.242.211.89:https      ESTABLISHED
   TCP       10.10.10.130:58628     24-155-92-110:https      ESTABLISHED
   TCP       10.10.10.130:58651     ec2-18-211-133-65:https  ESTABLISHED
   TCP       10.10.10.130:58686     do-33:https              ESTABLISHED
   TCP       10.10.10.130:58720     172.253.119.189:https    ESTABLISHED
   TCP       10.10.10.130:58751     ec2-35-170-0-145:https   ESTABLISHED
   TCP       10.10.10.130:58753     ec2-44-224-80-214:https  ESTABLISHED
   TCP       10.10.10.130:58755     a23-65-237-228:https     ESTABLISHED

C:∖>
```

Conexões TCP desconhecidas podem ser uma ameaça de segurança maior. Isto é porque elas podem indicar que algo ou alguém está conectado ao host local. Além disso, conexões TCP desnecessárias podem consumir recursos valiosos do sistema, diminuindo assim o desempenho do host. O Netstat deve ser usado para examinar as conexões abertas em um host quando o desempenho parecer estar comprometido.

Muitas opções úteis estão disponíveis para o comando **netstat**. Essas opções podem ser visualizadas digitando **netstat /?** no prompt de comando, conforme mostrado no exemplo.

```
C:∖> netstat /?
Displays protocol statistics and current TCP/IP network connections.

NETSTAT [-a] [-b] [-e] [-f] [-n] [-o] [-p proto] [-r] [-s] [-t] [-x] [-y] [interval]

   -a            Displays all connections and listening ports.
   -b            Displays the executable involved in creating each connection or
                 listening port. In some cases well-known executables host
                 multiple independent components, and in these cases the
                 sequence of components involved in creating the connection
                 or listening port is displayed. In this case the executable
                 name is in [] at the bottom, on top is the component it called,
                 and so forth until TCP/IP was reached. Note that this option
                 can be time-consuming and will fail unless you have sufficient
                 permissions.
   -e            Displays Ethernet statistics. This may be combined with the -s
                 option.
   -f            Displays Fully Qualified Domain Names (FQDN) for foreign
                 addresses.
   -n            Displays addresses and port numbers in numerical form.
   -o            Displays the owning process ID associated with each connection.
   -p proto      Shows connections for the protocol specified by proto; proto
                 may be any of: TCP, UDP, TCPv6, or UDPv6. If used with the -s
                 option to display per-protocol statistics, proto may be any of:
                 IP, IPv6, ICMP, ICMPv6, TCP, TCPv6, UDP, or UDPv6.
   -q            Displays all connections, listening ports, and bound
                 nonlistening TCP ports. Bound nonlistening ports may or may not
                 be associated with an active connection.
   -r            Displays the routing table.
   -s            Displays per-protocol statistics. By default, statistics are
                 shown for IP, IPv6, ICMP, ICMPv6, TCP, TCPv6, UDP, and UDPv6;
                 the -p option may be used to specify a subset of the default.
   -t            Displays the current connection offload state.
   -x            Displays NetworkDirect connections, listeners, and shared
                 endpoints.
   -y            Displays the TCP connection template for all connections.
                 Cannot be combined with the other options.
   interval      Redisplays selected statistics, pausing interval seconds
                 between each display. Press CTRL+C to stop redisplaying
                 statistics. If omitted, netstat will print the current
                 configuration information once.


C:∖>
```


## 36.4.8 O Comando nslookup

Quando um dispositivo de rede está sendo configurado, um ou mais endereços de servidor DNS são fornecidos para que o cliente DNS possa usar para resolução de nomes. Normalmente, o ISP fornece os endereços a serem usados nos servidores DNS. Quando um aplicativo de usuário solicita a conexão a um dispositivo remoto por nome, o cliente DNS solicitante consulta o servidor de nomes para resolver o nome para um endereço numérico.

Os sistemas operacionais dos computadores também têm um utilitário chamado nslookup que permite que o usuário consulte manualmente os servidores de nome para resolver um nome de host específico. Este utilitário também pode ser usado para corrigir problemas de resolução de nomes e verificar o status atual dos servidores de nomes.

Nesta figura, quando o comando **nslookup** é emitido, o servidor DNS padrão configurado para seu host é exibido. O nome de um host ou domínio pode ser inserido no prompt do **nslookup**. O utilitário nslookup tem muitas opções disponíveis para amplos testes e verificações do processo DNS.

```
C:∖Users> nslookup
Default Server:  dns-sj.cisco.com
Address:  171.70.168.183
> www.cisco.com
Server:   dns-sj.cisco.com
Address:  171.70.168.183
Name:    origin-www.cisco.com
Addresses:  2001:420:1101:1::a
          173.37.145.84
Aliases:  www.cisco.com
> cisco.netacad.net
Server:  dns-sj.cisco.com
Address:  171.70.168.183
Name:    cisco.netacad.net
Address:  72.163.6.223
>
```


## 36.4.9 Verificador de Sintaxe - O Comando nslookup

Pratique entrando com o comando nslookup no Windows e Linux


```
No prompt de comando do Windows, digite o nslookup comando para iniciar uma consulta manual dos servidores de nomes.

C:\>nslookup
Default Server: Unknown
Address: 10.10.10.1
As saídas listam o nome e o endereço IP do servidor DNS configurado no cliente. Observe que o endereço do servidor DNS pode ser configurado manualmente ou aprendido dinamicamente através do DHCP. Você está agora no modo nslookup. Digite o nome de domínio www.cisco.com.

>www.cisco.com
Server:  UnKnown
Address:  10.10.10.1
Non-authoritative answer:
Name:    e2867.dsca.akamaiedge.net
Addresses:  2600:1404:a:395::b33
          2600:1404:a:38e::b33
          172.230.155.162
Aliases:  www.cisco.com
          www.cisco.com.akadns.net
          wwwds.cisco.com.edgekey.net
          wwwds.cisco.com.edgekey.net.globalredir.akadns.net
As saídas listam os endereços IP relacionados com ‘w​ww.cisco.com’ que o servidor ‘e2867’ tem em seu banco de dados atualmente. Observe que endereços IPv6 também estão listados. Além disso, vários aliases são exibidos e que também serão resolvidos para ‘w​ww.cisco.com’.

Digite o comando exitpara sair do modo nslookup e retornar à linha de comando do Windows.

>exit
Você pode consultar diretamente os servidores DNS simplesmente adicionando o nome de domínio ao comando nslookup .

Entrar nslookup w​ww.google.com.

C:\>nslookup www.google.com
Server:  UnKnown
Address:  10.10.10.1
Non-authoritative answer:
Name:    www.google.com
Addresses:  2607:f8b0:4000:80f::2004
          172.217.12.36
 
 
=========================================
Você agora está trabalhando no prompt de comando do Linux. O comando nslookup é o mesmo.

* Enter the nslookup comando para iniciar uma consulta manual dos servidores de nomes. * Enter www.cisco[]().com at the \> prompt. * Enter the exit para sair do modo nslookup e retornar à linha de comandos do Linux.

user@cisconetacad$nslookup
Server: 127.0.1.1
Address: 127.0.1.1#53
>www.cisco.com
Non-authoritative answer:
www.cisco.com canonical name = www.cisco.com.akadns.net.
www.cisco.com.akadns.net canonical name = wwwds.cisco.com.edgekey.net.
wwwds.cisco.com.edgekey.net canonical name = wwwds.cisco.com.edgekey.net.globalredir.akadns.net.
wwwds.cisco.com.edgekey.net.globalredir.akadns.net canonical name = e144.dscb.akamaiedge.net.
Name: e144.dscb.akamaiedge.net
Address: 23.60.112.170
>exit
Como no Windows, você pode consultar diretamente os servidores DNS simplesmente adicionando o nome de domínio ao comando nslookup . Entrar nslookup w​ww.google.com.

user@cisconetacad$nslookup www.google.com
Server:		127.0.0.53
Address:	127.0.0.53#53

Non-authoritative answer:
Name:	www.google.com
Address: 172.217.6.164
Name:	www.google.com
Address: 2607:f8b0:4000:812::2004
Você usou corretamente o comando nslookup para verificar o status dos nomes de domínio.
```


## 36.4.10 Laboratório - Solucionar problemas usando utilitários de rede

Neste laboratório, você completará os seguintes objetivos:

- Interprete a saída dos utilitários da linha de comando mais usados na rede.
- Determine o utilitário de rede que pode fornecer as informações necessárias para realizar atividades de solução de problemas em uma estratégia bottom-up.














