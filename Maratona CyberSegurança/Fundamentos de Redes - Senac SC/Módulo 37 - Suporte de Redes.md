# 37.0 Introdução

## 37.0.1 Por que devo fazer este módulo?

Olá! Aqui é o Webster Deixe-me apresentar-lhe a minha amiga Lara! Lara trabalha como técnica de help desk no departamento de TI de uma pequena faculdade comunitária em Brisbane, Austrália, há pouco mais de um ano. O help desk recebe inúmeras solicitações de suporte de TI de administrativos, professores e alunos. Lara provou ser um excelente recurso para a equipe de help desk, pois é muito eficaz na resolução de problemas. Por causa de seu excelente trabalho, Lara foi recentemente promovida e designada para desenvolver um guia de solução de problemas para ajudar novos técnicos a resolver problemas de TI do dia a dia. Que abordagem você usaria ao diagnosticar um problema relatado? Que documentação você precisaria para ajudar a fazer o seu trabalho? Como você acompanha um problema relatado? Quais comandos seriam úteis ao diagnosticar problemas de dispositivos finais e de rede? Continue lendo, pois responderemos a essas perguntas neste módulo.

## 37.0.2 O que vou aprender neste módulo?

**Titulo do módulo:** Suporte de Redes

**Objetivo do módulo:** Demonstrar metodologias eficazes de solução de problemas e práticas recomendadas de Central de Ajuda (Help Desk)

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Diagnóstico e Metodologias para Solução de Problemas|Demonstrar metodologias eficazes de solução de problemas.|
|Documentação da rede|Criar documentação de rede.|
|Centrais de Ajuda (Help Desk)|Explicar as melhores práticas de help desk.|
|Solucionar problemas de conectividade de endpoint|Explicar como verificar a conectividade de rede nos sistemas operacionais de dispositivos Linux, Mac, Android e Apple.|
|Solucionar Problemas de uma rede|Solucionar os problemas de uma rede.|
|Solucionar problemas de Conectividade Remota|Explicar como solucionar problemas de conectividade remotamente.|

## 37.0.3 Baixar o Cisco Packet Tracer

Para obter e instalar a sua cópia do Cisco Packet Tracer, siga as instruções do link abaixo: [https://www.netacad.com/resources/lab-downloads](https://www.netacad.com/resources/lab-downloads?courseLang=pt-BR)

# 37.1 Metodologias de Diagnóstico e Solução de Problemas

## 37.1.1 Revisão do processo de solução de problemas

A solução de problemas é o processo de identificar, localizar e corrigir problemas. Esse processo envolve a coleta de informações e o uso de um ou mais métodos estruturados de solução de problemas.

Depois que o problema na rede é descoberto pela primeira vez, uma das primeiras etapas é coletar informações. A lista a seguir fornece uma revisão de algumas das informações que você pode querer coletar.

- Determinar a natureza do problema
    - Relatórios do usuário final
    - Relatório de verificação do problema
- Reúna informações relevantes sobre o equipamento
    - Fabricante
    - Marca/modelo
    - Versão de firmware
    - Versão do sistema operacional
    - Informações sobre propriedade/garantia
- Reúna informações de configuração e topologia
    - Topologia física e lógica
    - Arquivos de configuração
    - Arquivos de log
- Determine se houve algum problema semelhante anteriormente
    - Passos dados
    - Resultados alcançados


## 37.1.2 Processo de Solução de Problemas em Sete Etapas

A figura exibe um processo mais detalhado de solução de problemas em sete etapas. Observe como alguns passos se interconectam. Isso ocorre porque, alguns técnicos podem ser capazes de saltar entre etapas com base em seu nível de experiência.

![[Pasted image 20260701215137.png]]

### Definir o Problema

O objetivo deste estágio é verificar se há um problema e, em seguida, definir corretamente qual é o problema. Os problemas geralmente são identificados por um sintoma (por exemplo, a rede está lenta ou parou de funcionar). Os sintomas de rede podem aparecer de várias formas diferentes, incluindo alertas do sistema de gerenciamento de rede, mensagens do console e reclamações de usuários.

Ao reunir os sintomas, é importante fazer perguntas e investigar o problema para localizar o problema em um intervalo menor de possibilidades. Por exemplo, o problema está restrito a um único dispositivo, um grupo de dispositivos ou a toda a sub-rede ou rede de dispositivos?

Em uma organização, os problemas são normalmente atribuídos aos técnicos de rede por meio de tickets de problema. Esses tickets são criados usando softwares de emissão de tickets de problemas que rastreiam o progresso de cada ticket. O software de emissão de tíquetes de problemas também pode incluir um portal de usuário self-service para enviar tickets, acesso a uma base de conhecimento de tickets de problemas pesquisáveis, recursos de controle remoto para resolver problemas do usuário final e muito mais.

### Coletar informações

Nesta etapa, os alvos (ou seja, hosts, dispositivos) a serem investigados devem ser identificados, o acesso aos dispositivos de destino deve ser obtido e as informações coletadas. Durante esta etapa, o técnico pode reunir e documentar mais sintomas, dependendo das características identificadas.

### Analisar as Informações

Possíveis causas devem ser identificadas. As informações coletadas são interpretadas e analisadas usando documentação de rede, linhas de base da rede, busca de bases de conhecimento organizacionais, pesquisa na internet e conversa com outros técnicos.

### Eliminar possíveis causas

Se várias causas são identificadas, então a lista deve ser reduzida eliminando progressivamente possíveis causas para eventualmente identificar a causa mais provável. A experiência em solução de problemas é extremamente valiosa para eliminar rapidamente as causas e identificar a causa mais provável.

### Propor Hipótese

Quando a causa mais provável for identificada, uma solução deve ser formulada. Nesta fase, a experiência em solução de problemas é muito valiosa para propor um plano.

### Testar a Hipótese

Antes de testar a solução, é importante avaliar o impacto e a urgência do problema. Por exemplo, a solução poderia ter um efeito adverso em outros sistemas ou processos? A gravidade do problema deve ser avaliada em relação ao impacto da solução. Por exemplo, se um Servidor ou roteador crítico precisar ficar offline por um período significativo, talvez seja melhor esperar até o fim do dia de trabalho para implementar a correção. Às vezes, é possível criar uma solução alternativa até que o problema real seja resolvido.

### Resolva o problema

Quando o problema for resolvido, informe os usuários e qualquer pessoa envolvida no processo de solução de problemas que o problema foi resolvido. Os outros membros da equipe de TI devem ser informados sobre a solução. É importante documentar adequadamente a causa e a solução, pois isso pode ajudar outros técnicos de suporte a prevenir e resolver problemas semelhantes no futuro.

## 37.1.3 Solução de problemas com modelos de camadas

Os modelos OSI e TCP / IP podem ser aplicados para isolar problemas de rede ao solucionar problemas. Por exemplo, se os sintomas sugerirem um problema de conexão física, o técnico de rede pode se concentrar na solução de problemas dos cabos e suas conexões na camada física.

A figura mostra alguns dispositivos comuns e as camadas OSI que devem ser examinadas durante o processo de solução de problemas para esse dispositivo.
![[Pasted image 20260701215325.png]]


Observe que os roteadores e os switches multicamada são mostrados na camada 4, a camada de transporte. Embora os roteadores e switches multicamada geralmente tomem decisões de encaminhamento na camada 3, as ACLs nesses dispositivos podem usar as informações da camada 4 para tomar decisões de filtragem.


## 37.1.4 Métodos Estruturados de Solução de Problemas

Existem vários métodos estruturados de solução de problemas que podem ser usados para resolver problemas de computador e rede. O método de solução de problemas usado varia dependendo do tipo de problema e da experiência pessoal do técnico.

Um técnico pode escolher um ou mais dos seguintes métodos para resolver um problema:

- **De baixo para cima (Bottom-Up**) - Comece com a camada física e os componentes físicos da rede e suba pelas camadas do modelo OSI até que a causa do problema seja identificada.
- **De cima para baixo (Top-Down**) - Comece com os aplicativos do usuário final e desça pelas camadas do modelo OSI até que a causa do problema seja identificada.
- **Dividir para conquistar (Divide-and-Conquer**) - comece coletando as experiências do usuário sobre o problema, documente os sintomas e, usando essas informações, faça uma estimativa sobre qual camada OSI iniciar sua investigação.
- **Siga o Caminho (Follow-the-Path**) - Descubra o caminho do tráfego desde a origem até o destino. Esta abordagem geralmente complementa uma das outras abordagens.
- **Substituição** - Troque fisicamente o dispositivo ou componente problemático por um que esteja funcionando. Se o problema for corrigido, o problema estará no item removido. Se o problema persistir, a causa está em outro lugar.
- **Comparação** - Compare detalhes como configurações, versões de software, hardware ou outras propriedades de dispositivos, links ou processos entre situações de funcionamento e não funcionamento e identifique diferenças significativas entre eles.
- **Suposição** fundamentada - Um método de solução de problemas menos estruturado que usa uma suposição baseada na experiência do técnico e em sua capacidade de resolver problemas.


## 37.1.5 Diretrizes para Selecionar um Método de Solução de Problemas

Para resolver rapidamente problemas de rede, selecione o método de identificação e solução de problemas de rede mais eficaz.

A figura ilustra qual método pode ser usado quando um determinado tipo de problema é descoberto.

![[Pasted image 20260701215350.png]]

Por exemplo, os problemas de software geralmente são resolvidos usando uma abordagem de cima para baixo, enquanto o problema baseado em hardware é resolvido usando a abordagem de baixo para cima. Novos problemas podem ser resolvidos por um técnico experiente usando o método dividir e conquistar. Caso contrário, pode ser utilizada a abordagem de baixo para cima.

Solução de problemas é uma habilidade que é desenvolvida ao fazê-lo. Cada problema de rede que você identificar e resolver é adicionado ao seu conjunto de habilidades.

## 37.1.6 Documentar Descobertas, Ações e Resultados

Após a resolução de todos os problemas, é importante concluir o processo de solução de problemas documentando todas as informações.

Um técnico deve documentar:

- **Problema** - Inclui o relatório inicial do problema, uma descrição dos sintomas, informações coletadas e qualquer outra informação que ajude a resolver problemas semelhantes.
- **Solução** - Inclui as etapas executadas para resolver o problema.
- **Comandos e Ferramentas Usadas** - Inclui os comandos e ferramentas usadas para diagnosticar o problema e resolvê-lo.

Verifique a solução com o cliente. Se o cliente estiver disponível, demonstre como a solução corrigiu seu problema. Peça ao cliente que teste a solução e tente reproduzir o problema. Quando o cliente puder verificar se o problema foi resolvido, você poderá atualizar a documentação com qualquer nova informação fornecida pelo cliente.


## 37.1.7 Verifique o seu entendimento - Processo de solução de problemas

### Pergunta 1

Em que etapa do processo de solução de problemas de sete etapas, você criaria um plano de reversão identificando como reverter rapidamente uma solução?

- [ ] Propor Hipótese
- [ ] Definir o problema
- [x] Testar hipótese
- [ ] Coletar informações
- [ ] Resolver o problema e documentar a solução
- [ ] Analisar informações
- [ ] Eliminar possíveis causas

✅ RESPOSTA CORRETA: Testar hipótese

> Está certo. Ao testar uma solução para um problema, é uma boa ideia ter um plano de reversão caso a solução não funcione. Isso retorna a rede ao estado inicial para que uma nova solução possa ser tentada ou testada.

### Pergunta 2

Qual é a camada OSI mais alta que deve ser considerada ao solucionar problemas de roteadores e switches de Camada 3?

- [ ] Camada 2
- [x] Camada 4
- [ ] Camada 1
- [ ] Camada 7
- [ ] Camada 3

✅ RESPOSTA CORRETA: Camada 4

> Está certo. Ao solucionar problemas, o modelo OSI pode ser usado para ajudar a isolar problemas de rede. Se os sintomas sugerirem um problema em uma camada específica, um técnico pode se concentrar nos dispositivos que operam nessa camada. Roteadores e switches da Camada 3 tomam decisões de encaminhamento na Camada 3 e também tomam decisões de filtragem usando listas de controle de acesso, com base nas informações da Camada 3 e da Camada 4.

### Pergunta 3

Qual método estruturado de solução de problemas deve ser usado quando um problema de cabeamento é suspeito?

- [ ] de cima para baixo
- [x] de baixo para cima
- [ ] comparação
- [ ] siga o caminho
- [ ] suposição fundamentada
- [ ] dividir para conquistar

✅ RESPOSTA CORRETA: de baixo para cima

> Está certo. Como os cabos operam na Camada 1, a camada física, uma abordagem de solução de problemas de baixo para cima, que começa na Camada 1, é apropriada.

### Pergunta 4

Qual método estruturado de solução de problemas deve ser usado quando ocorre um problema orientado por software?

- [ ] comparação
- [ ] suposição fundamentada
- [ ] dividir para conquistar
- [ ] siga o caminho
- [x] de cima para baixo
- [ ] de baixo para cima

✅ RESPOSTA CORRETA: de cima para baixo

> Está certo. Como o software opera na Camada 7, a camada de aplicativo, uma abordagem de solução de problemas de cima para baixo, que começa na Camada 7, é apropriada.


# 37.2 Documentação da rede

## 37.2.1 Visão geral da Documentação

Como acontece com qualquer atividade complexa, como solução de problemas de rede, você precisará começar com uma boa documentação. Documentação de rede precisa e completa é necessária para monitorar e solucionar problemas de redes com eficiência.

A documentação comum da rede inclui o seguinte:

- Diagramas de topologia de rede física e lógica
- Documentação do dispositivo de rede que registra todas as informações pertinentes do dispositivo
- Documentação da linha de base do desempenho da rede

Toda a documentação da rede deve ser mantida em um único local, como cópia impressa ou na rede em um servidor protegido. O backup da documentação deve ser mantido em um local separado.

## 37.2.2 Topologias e Descrições de Rede

As redes variam em tamanho, dependendo do requisito de rede. Um técnico deve ter conhecimento sobre os diferentes tipos de redes disponíveis para conectar dispositivos finais e sites corporativos.

**Selecione as setas para a esquerda e para a direita para saber mais sobre os diferentes tipos de redes.**

### **PAN**

Uma **rede de área pessoal (PAN)** conecta dispositivos (como mouses, teclados, impressoras, smartphone e tablets) que se encontram dentro do alcance de um indivíduo. Esses dispositivos são, geralmente, conectados com a tecnologia Bluetooth. Bluetooth é uma tecnologia sem fio que permite que os dispositivos se comuniquem em distâncias pequenas.
![[Pasted image 20260701220414.png]]

### **LAN (rede de área local)**

Tradicionalmente, uma **rede de área local ( LAN)** é definida como uma rede que conecta dispositivos usando cabos com fio em uma área geográfica pequena. Entretanto, a característica que distingue as LANs hoje em dia é que normalmente elas são usadas por um indivíduo (em casa ou em uma empresa pequena) ou completamente gerenciadas por um departamento de TI, como em uma escola ou uma corporação.
![[Pasted image 20260701220404.png]]

### **VLAN**

**As LANs virtuais (VLANs)** permitem que um administrador segmente as portas em um único switch, como se fossem vários switches. Isso proporciona um encaminhamento mais eficiente de dados, isolando o tráfego para apenas essas portas, onde é necessário. As VLANs também permitem que os dispositivos finais sejam agrupados em conjunto para fins administrativos. No diagrama, a VLAN 2 cria uma LAN virtual para computadores, mesmo em andares diferentes, e pode ter permissões de rede definidas diferentemente das de outras VLANs.
![[Pasted image 20260701220355.png]]

### **WLAN**

Uma **LAN sem fio (WLAN )** é semelhante a uma LAN mas conecta, via conexão sem fio, usuários e dispositivos em uma área geográfica pequena, ao invés de usar uma conexão com fio.
![[Pasted image 20260701220347.png]]

### **WMN**

Uma **rede de malha sem fio (WMN)** usa vários pontos de acesso para estender a WLAN. A topologia mostra um roteador sem fio. Os dois APs sem fio estendem o alcance da WLAN na casa. Da mesma forma, empresas e municípios podem usar WMNs para adicionar rapidamente novas áreas de cobertura.![[Pasted image 20260701220340.png]]

### **CAN**

Uma rede de área de **campus (CAN)** é um grupo de LANs interconectadas, pertencentes à mesma organização e operando em uma área geográfica limitada. Estes podem ser campi acadêmicos e campi empresariais ou corporativos. As redes da área do campus geralmente consistem em vários prédios interconectados por links Ethernet de alta velocidade usando cabeamento de fibra óptica. A figura mostra três redes de área de campus de tamanhos diferentes.
![[Pasted image 20260701220325.png]]
### **MAN**

Uma **rede de área metropolitana (MAN)** é uma rede que abrange uma cidade ou um grande campus. A rede consiste em vários prédios interconectados por backbones de fibra ótica ou sem fio.
![[Pasted image 20260701220306.png]]
### **WAN**

Uma **rede de longa distância (WAN)** conecta várias redes que estão em locais separados geograficamente. Indivíduos e empresas contratam serviços de WAN. Seu provedor de serviços para sua casa ou dispositivo móvel conecta você à rede de longa distância, Internet. Na figura, as redes de Tóquio e Moscou estão conectadas através da Internet.
![[Pasted image 20260701220259.png]]
### **VPN**

Uma **rede privada virtual (VPN)** é usada para se conectar com segurança a outra rede usando uma rede não segura, como a Internet. O tipo mais comum de VPN é usado pelos trabalhadores remotos para acessar uma rede privada corporativa. Colegas de trabalho são usuários de rede que são externos ou remotos. Na figura, os links entre o Trabalhador Remoto 1 e o roteador na sede da empresa representam uma conexão VPN.
![[Pasted image 20260701220251.png]]


## 37.2.3 Verifique sua Compreensão – Tipos de Redes

Associe o tipo de rede a sua definição.

|Categoria|Resposta correta|
|---|---|
|Uma rede que se estende por uma cidade.|MAN|
|Uma LAN que conecta dispositivos sem fio à rede.|WLAN|
|Conecta os dispositivos próximos ao usuário, geralmente usando Bluetooth.|PAN|
|Os APs sem fio se conectam para estender o acesso de uma rede sem fio.|WMN|
|Conecta redes separadas por grandes distâncias geográficas, como a Internet.|WAN|
|Permite que os usuários se conectem com segurança a outra rede em redes não seguras.|VPN|
|Geralmente usa cabos de cobre para conectar dispositivos a um switch em uma área geográfica pequena.|LAN (Local Area Network)|
|Pode se estender além dos LANs tradicionais e agrupa os usuários com base em limites definidos administrativamente e não físicos|VLAN|

## 37.2.4 Topologias de Rede Corporativa

Dois tipos de topologias de rede que você aprendeu são:

- Topologia de rede física
- Topologia de rede lógica

A figura exibe um exemplo de topologia física para uma rede pequena. A topologia identifica a localização física e a função dos dispositivos.

### Topologia Física
![[Pasted image 20260701220708.png]]

A figura exibe a topologia lógica para a mesma pequena rede do exemplo anterior. Observe que a figura exibe as interfaces de conexão e o esquema de endereçamento de rede da Camada 3.

### Topologia Lógica
![[Pasted image 20260701220726.png]]

As topologias de rede corporativa são semelhantes, mas maiores em escala e complexidade. Eles normalmente também incluem diagramas de topologia de rede adicionais.

Em um curso anterior, você aprendeu sobre design de rede hierárquica, incluindo as camadas de acesso, distribuição e núcleo. Este é um dos vários modelos de arquitetura usados em redes corporativas que podem ajudar a orientá-lo na criação e manutenção de uma estratégia de design eficaz. Esses modelos de arquitetura não são padrões, pois cada rede é diferente em tamanho, complexidade, requisitos e orçamento.

Esta figura mostra uma visão de alto nível de como diferentes partes de uma rede corporativa se conectam ao longo de sua conexão com seu provedor de nuvem.

![[Pasted image 20260701220741.png]]

Para uma rede corporativa, sua documentação de rede geralmente inclui vários diagramas de topologia de rede mostrando diferentes níveis de detalhes e diferentes tipos de informações.

Diferentes diagramas de topologia podem incluir:

- Layout físico e conexões
- Endereço IP e gerenciamento de VLAN
- Políticas de segurança e VPN
- Serviços de nuvem e gerenciamento
- Políticas de roteamento
- Políticas de acesso remoto para trabalhadores remotos e híbridos


## 37.2.5 Serviços e Aplicativos de Rede em Nuvem

Existem três tipos básicos de computação em nuvem:

- SaaS – Software como serviço
- PaaS – plataforma como serviço
- IaaS – Infrastrutura como serviço

Selecione cada guia para obter mais informações sobre cada tipo de computação em nuvem.

### **SaaS (Software as a Service)**

Os aplicativos SaaS são focados no usuário final. Em vez de o aplicativo ser instalado localmente no computador do usuário final, o aplicativo é acessado pela rede, geralmente usando um navegador da web. Em um ambiente de computação tradicional, o usuário acessaria seu software aplicativo de processamento de texto armazenado na unidade de disco rígido local. Usando SaaS, o usuário pode usar um navegador da web para acessar o aplicativo de processamento de texto Google Docs na nuvem do Google. Os documentos do usuário podem ser armazenados na nuvem do Google ou exportados para o computador local.

Outros aplicativos SaaS incluem:

- Planilhas Google
    
- Calendário Google
    
- Google Maps
    

- Office 365
    
- Salesforce


### **PaaS (Platform as a Service)**

PaaS é usado principalmente por desenvolvedores de software. A PaaS permite que os desenvolvedores se concentrem em seu código e não no software e hardware subjacentes necessários para executar seus programas. A nuvem PaaS fornece servidores, armazenamento, segurança, ferramentas, banco de dados e outros serviços para hospedar o aplicativo consumidor. PaaS em sua forma mais simples é onde o desenvolvedor só precisa escrever o código, e a infraestrutura e as operações são tratadas pelo provedor de PaaS

Alguns exemplos de serviços de PaaS são:

- Microsoft Azure
    
- Salesforce Lightning
    
- AWS Lambda
    
- AWS Elastic Beanstalk
    
- Google App Engine


### **IaaS (Infrastructure as a Service)**

IaaS é um serviço em que os recursos de computação são fornecidos por um provedor de serviços em nuvem. A nuvem IaaS fornece as máquinas virtuais (VMs) para armazenamento, rede e outros serviços. O provedor de nuvem é responsável pelos requisitos de tempo de atividade, energia e segurança das VMs.

IaaS é um serviço usado por desenvolvedores de software e administradores de sistema. Como as VMs e os aplicativos são gerenciados pelo provedor de nuvem IaaS, as organizações não precisam hospedar esses sistemas em seu próprio data center.

Alguns exemplos de serviços de IaaS são:

- Cisco Metacloud
    
- Microsoft Azure
    
- Digital Ocean
    
- Google Compute Engine
    
- Rackspace


### XaaS (Qualquer coisa/Tudo como serviço)

outros serviços para hospHoje, uma variedade de soluções e tecnologias podem ser fornecidas como um serviço por provedores de nuvem para seus clientes.edar o aplicativo consumidor. XaaS não é um serviço de nuvem específico, mas é definido como a entrega de tudo e qualquer coisa como um serviço. XaaS inclui Saas, PaaS e IaaS.

Outros exemplos de XaaS incluem:

- Recuperação de desastres como serviço (DRaaS)
- Comunicações como serviço (CaaS)
- Monitoramento como serviço (MaaS)
- Desktop como serviço (DaaS)

### 37.2.6 Padrões Sem Fio

O mundo das comunicações sem fio é vasto No entanto, para habilidades específicas relacionadas ao trabalho, queremos nos concentrar em aspectos específicos do Wi-Fi. O melhor lugar para começar é com os padrões WLAN IEEE 802.11. Esses padrões definem como as frequências de rádio são usadas para links sem fio. A maioria dos padrões especifica que os dispositivos sem fio têm uma antena para transmitir e receber sinais sem fio na frequência de rádio especificada (2,4 GHz, 5 GHz ou 6 GHz). Alguns dos padrões mais recentes que transmitem e recebem em velocidades mais altas exigem que os pontos de acesso (APs) e os clientes sem fio tenham múltiplas antenas usando a tecnologia MIMO (entradas múltiplas e saídas múltiplas). O MIMO usa várias antenas, tanto para transmitir quanto para receber, para melhorar o desempenho da comunicação. Até oito antenas de transmissão e recepção podem ser usadas para aumentar a taxa de transferência.

Várias implementações do padrão IEEE 802.11 foram desenvolvidas ao longo dos anos. A tabela destaca esses padrões.

|Padrão IEEE WLAN|Radiofrequência (RF)|Descrição|
|---|---|---|
|802.11|2.4 GHz|velocidades de até 2 Mbps|
|802.11a|5 GHz|velocidades de até 54 Mbps<br>pequena área de cobertura<br>menos eficaz em penetrar nas estruturas dos edifícios<br>não interoperável com o 802.11be 802.11g|
|802.11b|2.4 GHz|velocidades de até 11 Mbps<br>alcance maior que o 802.11a<br>mais capaz de penetrar em estruturas|
|802.11g|2.4 GHz|velocidades de até 54 Mbps<br>retrocompatível com 802.11b com capacidade de largura de banda reduzida|
|802.11n|2.4 GHz 5 GHz|as taxas de dados variam de 150 Mbps a 600 Mbps com uma faixa de distância de até 70 m (230 pés)<br>APs e clientes sem fio requerem várias antenas usando a tecnologia MIMO<br>retrocompatível com dispositivos 802.11a/b/g com taxas de dados limitadas|
|802.11ac|5 GHz|fornece taxas de dados que variam de 450 Mbps a 1,3 Gbps (1300 Mbps) usando a tecnologia MIMO<br>Até oito antenas podem ser suportadas<br>retrocompatível com dispositivos 802.11a/n com taxas de dados limitadas|
|802.11ax|2.4 GHz 5 GHz|lançado em 2019 - padrão mais recente<br>também conhecido como High-Efficiency Wireless (HEW)<br>Taxas de dados mais altas<br>Capacidade aumentada<br>lida com muitos dispositivos conectados<br>maior eficiência de energia<br>Capacidade de 1 GHz e 7 GHz quando essas frequências se tornam disponíveis<br>Pesquise na Internet o Wi-Fi geração 6 para obter mais informações<br>Wi-Fi 6 – Usa bandas de 2,4 GHz e 5 GHz<br>Wi-Fi 6E – Usa banda de 6 GHz|


### Bandas licenciadas e não licenciadas

Vários canais de comunicação transmitem sinais no espectro eletromagnético. O espectro licenciado refere-se às bandas (faixa de frequência) reservadas para emissoras de rádio, operadoras de celular e emissoras de televisão aberta. As empresas de mídia e celular normalmente pagam pelo direito de transmitir em uma frequência específica dentro do espectro licenciado. Nos Estados Unidos, isso é feito pela Federal Communications Commission (FCC). Outros países têm uma agência reguladora semelhante que licencia bandas específicas para aquele país.

O espectro não licenciado está aberto para qualquer um usar. O espectro não licenciado é onde encontramos as tecnologias Wi-Fi IEEE 802.11 e está disponível gratuitamente ao público. Qualquer pessoa pode transmitir no espectro não licenciado.


## 37.2.7 Packet Tracer - Conectar uma Rede baseada em um Diagrama de Rede

Nesta atividade, você concluirá uma topologia física com base em um diagrama de rede fornecido.


## 37.2.8 Documentação dos Dispositivos de Rede

A documentação dos dispositivos de rede deve conter registros precisos e atualizados do hardware e software da rede. A documentação deve incluir todas as informações pertinentes sobre os dispositivos de rede.

Muitas organizações criam documentos com tabelas ou planilhas para capturar informações relevantes do dispositivo.

**Selecione cada guia para obter exemplos de documentação de roteador, switch e dispositivo final.**

### Documentação do dispositivo roteador

A tabela exibe uma amostra de documentação do dispositivo de rede para dois roteadores interconectados.

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed; word-wrap:break-word;"> <tr style="background:#6b7280; color:white;"> <th>Dispositivo</th><th>Modelo</th><th>Descrição</th><th>Localização</th><th>IOS</th><th>Licença</th> </tr> <tr> <td><strong>Central</strong></td> <td>ISR 4321</td> <td>Roteador de Borda Central</td> <td>Edifício A<br>Rm: 137</td> <td>Cisco IOS XE Software, Version 16.09.04<br><br>flash:isr4300-universalk9_ias.16.09.04.SPA.bin</td> <td>ipbasek9<br>securityk9</td> </tr> <tr style="background:#111827; color:white;"> <th>Interface</th><th>Descrição</th><th>Endereço IPv4</th><th>Endereço IPv6</th><th>Endereço MAC</th><th>Roteamento</th> </tr> <tr> <td>G0/0/0</td> <td>Conecta-se ao SVR-1</td> <td>10.0.0.1/30</td> <td>2001:db8:acad:1::1/64</td> <td>a03d.6fe1.e180</td> <td>OSPF</td> </tr> <tr> <td>G0/0/1</td> <td>Conecta-se ao Branch-1</td> <td>10.1.1.1/30</td> <td>2001:db8:acad:A001::1/64</td> <td>a03d.6fe1.e181</td> <td>OSPFv3</td> </tr> <tr> <td>G0/1/0</td> <td>Conecta-se ao ISP</td> <td>209.165.200.226/30</td> <td>2001:feed:1::2/64</td> <td>a03d.6fc3.a132</td> <td>Padrão</td> </tr> <tr> <td>S0/1/1</td> <td>Connecta-se ao Branch-2</td> <td>10.1.1.2/24</td> <td>2001:db8:acad:2::1/64</td> <td>N/D</td> <td>OSPFv3</td> </tr> <tr><td colspan="6" style="background:#c0c0c0; padding:4px;"></td></tr> <tr style="background:#000000; color:white;"> <th>Dispositivo</th><th>Modelo</th><th>Descrição</th><th>Site</th><th>IOS</th><th>Licença</th> </tr> <tr> <td><strong>Branch-1</strong></td> <td>ISR 4221</td> <td>Roteador de borda Branch-2</td> <td>Edifício B<br>Rm: 107</td> <td>Cisco IOS XE Software, Version 16.09.04<br><br>flash:isr4200-universalk9.16.09.04.SPA.bin</td> <td>ipbasek9<br>securityk9</td> </tr> <tr style="background:#111827; color:white;"> <th>Interface</th><th>Descrição</th><th>Endereço IPv4</th><th>Endereço IPv6</th><th>Endereço MAC</th><th>Roteamento</th> </tr> <tr> <td>G0/0/0</td> <td>Conecta-se ao S1</td> <td>Router-on-a-stick</td> <td>Router-on-a-stick</td> <td>a03d.6fe1.9d90</td> <td>OSPF</td> </tr> <tr> <td>G0/0/1</td> <td>Conecta-se à Central</td> <td>10.1.1.2/30</td> <td>2001:db8:acad:A001::2/64</td> <td>a03d.6fe1.9d91</td> <td>OSPF</td> </tr> </table>



### Documentação do dispositivo de switch LAN

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed; word-wrap:break-word;"> <tr style="background:#000000; color:white;"> <th>Dispositivo</th><th>Modelo</th><th>Descrição</th><th>MGT. Endereço IP</th><th>IOS</th><th colspan="3">VTP</th> </tr> <tr> <td><strong>S1</strong></td> <td>Cisco Catalyst<br><br>WS-C2960-24TC-L</td> <td>Switch Branch-1<br><br>LAN1</td> <td>192.168.77.2/24</td> <td>192.168.77.2/24<br><br>Image: C2960-LANBASEK9-M</td> <td colspan="3">Domínio: CCNA<br><br>Mode: Servidor</td> </tr> <tr style="background:#000000; color:white;"> <th>Porta</th><th>Descrição</th><th>seguro</th><th>VLAN</th><th>Tronco</th><th>EtherChannel</th><th>Nativa</th><th>Habilitado</th> </tr> <tr> <td>Fa0/1</td> <td>Tronco Port Channel 1 ao S2 Fa0/1</td> <td>-</td> <td>-</td> <td>Sim</td> <td>Port-Channel 1</td> <td>99</td> <td>Sim</td> </tr> <tr> <td>Fa0/2</td> <td>Tronco Port Channel 1 ao S2 Fa0/2</td> <td>-</td> <td>-</td> <td>Sim</td> <td>Port-Channel 1</td> <td>99</td> <td>Sim</td> </tr> <tr> <td>Fa0/3</td> <td>*** Fora de uso ***</td> <td>Sim</td> <td>666</td> <td>-</td> <td>-</td> <td></td> <td>Shut</td> </tr> <tr> <td>Fa0/4</td> <td>*** Fora de uso ***</td> <td>Sim</td> <td>666</td> <td>-</td> <td>-</td> <td></td> <td>Shut</td> </tr> <tr> <td>Fa0/5</td> <td>Porta de acesso ao usuário</td> <td>Sim</td> <td>10</td> <td>-</td> <td>-</td> <td></td> <td>Sim</td> </tr> <tr> <td>...</td> <td></td> <td></td> <td>-</td> <td>-</td> <td></td> <td></td> <td>-</td> </tr> <tr> <td>Fa0/24</td> <td>Porta de acesso ao usuário</td> <td>Sim</td> <td>20</td> <td>-</td> <td>-</td> <td></td> <td>Sim</td> </tr> <tr> <td>Fa0/24</td> <td>*** Fora de uso ***</td> <td>Sim</td> <td>666</td> <td>-</td> <td>-</td> <td></td> <td>Shut</td> </tr> <tr> <td>G0/1</td> <td>Link de tronco para Branch-1</td> <td>-</td> <td>-</td> <td>Sim</td> <td>-</td> <td>99</td> <td>Sim</td> </tr> <tr> <td>G0/2</td> <td>*** Fora de uso ***</td> <td>Sim</td> <td>666</td> <td></td> <td>-</td> <td></td> <td></td> </tr> </table>

### Documentação do sistema final

A documentação do sistema final enfoca o hardware e o software usados em servidores, consoles de gerenciamento de rede e estações de trabalho do usuário. Um sistema final configurado incorretamente pode ter um impacto negativo no desempenho geral de uma rede. Por esse motivo, ter acesso à documentação do dispositivo do sistema final pode ser muito útil ao solucionar problemas.

Esta tabela exibe uma amostra de informações que podem ser registradas em um documento de dispositivo do sistema final.

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed; word-wrap:break-word;"> <tr style="background:#000000; color:white;"> <th>Dispositivo</th><th>SO</th><th>Serviços</th><th>Endereço MAC</th><th>Endereços IPv4 / IPv6</th><th>Gateway padrão</th> </tr> <tr> <td rowspan="2"><strong>SRV1</strong></td> <td rowspan="2">Servidor MS 2016</td> <td rowspan="2">SMTP, POP3, Serviços de arquivos, DHCP</td> <td rowspan="2">5475.d08e.9ad8</td> <td>10.0.0.2/30</td> <td>10.0.0.1</td> </tr> <tr> <td>2001:db8:acad:1::2/64</td> <td>2001:db8:acad:1::1</td> </tr> <tr> <td rowspan="2"><strong>SRV2</strong></td> <td rowspan="2">Servidor MS 2016</td> <td rowspan="2">HTTP, HTTPS</td> <td rowspan="2">5475.d07a.5312</td> <td>209,165,201,10</td> <td>209.165.201.1</td> </tr> <tr> <td>2001:feed:1::10/64</td> <td>2001:feed:1::1</td> </tr> <tr> <td rowspan="2"><strong>PC1</strong></td> <td rowspan="2">MS Windows 10</td> <td rowspan="2">HTTP, HTTPS</td> <td rowspan="2">5475.d017.3133</td> <td>192.168.10.10/24</td> <td>192.168.10.1</td> </tr> <tr> <td>2001:db8:acad:1::251/64</td> <td>2001:db8:acad:1::1</td> </tr> <tr> <td>...</td> <td></td> <td></td> <td></td> <td></td> <td></td> </tr> </table>


## 37.2.9 Estabelecer uma Linha de Base de Rede

O objetivo do monitoramento de rede é observar o desempenho da rede em comparação com uma linha de base predefinida. Uma linha de base é usada para estabelecer o desempenho normal da rede ou do sistema para determinar a “personalidade” de uma rede em condições normais.

O estabelecimento de uma linha de base de desempenho de rede requer a coleta de dados de desempenho das portas e dispositivos que são essenciais para a operação da rede.

Uma linha de base de rede deve responder às seguintes perguntas:

- Durante um dia normal ou comum, como é o desempenho da rede? 
- Onde ocorre a maioria dos erros? 
- Qual é a parte da rede usada com mais intensidade? 
- Qual é a parte da rede menos usada? 
- Quais dispositivos devem ser monitorados e quais limites de alerta devem ser definidos? 
- A rede pode cumprir as políticas identificadas? 

A medição do desempenho inicial e da disponibilidade dos links e dispositivos de rede críticos permite que um administrador de rede determine a diferença entre o comportamento anormal e o desempenho de rede apropriado à medida que a rede cresce ou que os padrões de tráfego são alterados. A linha de base também permite prever se o projeto de rede atual atenderá aos requisitos de negócios. Sem a linha de base, não existiria nenhum padrão para medir a natureza ideal dos níveis de tráfego de rede e congestionamento.

A análise após uma linha de base inicial também tende a revelar problemas ocultos. Os dados coletados mostram a verdadeira natureza do congestionamento ou o possível congestionamento em uma rede. Também pode revelar áreas na rede que são subutilizadas e, muitas vezes, podem levar a esforços de redesenho da rede, com base em observações de qualidade e capacidade.

O parâmetro de desempenho de rede inicial define o estágio para medir os efeitos dos esforços de solução de problemas e alterações de rede subsequentes. Portanto, é importante planejar com cuidado.


## 37.2.10 Visão geral do Cisco Discovery Protocol (CDP)

A primeira coisa que você quer saber sobre sua rede é o que está nela? Onde estão esses componentes? Como eles estão conectados? Basicamente, você precisa de um mapa. Este tópico explica como você pode usar o Cisco Discovery Protocol (CDP) para criar um mapa da sua rede.

O CDP é um protocolo de camada 2 proprietário da Cisco usado para coletar informações sobre dispositivos Cisco que compartilham o mesmo link de dados. O CDP é independente de mídias e protocolos. Ele é executado em todos os dispositivos da Cisco, como roteadores, switches e servidores de acesso.

O dispositivo envia anúncios de CDP periódicos aos dispositivos conectados, como mostrado na figura.

![[Pasted image 20260702202432.png]]

Esses anúncios compartilham informações sobre o tipo de dispositivo descoberto, os nomes dos dispositivos e o número e o tipo de interfaces.

Como a maioria dos dispositivos de rede são conectados a outros dispositivos, o CDP pode auxiliar nas decisões de projeto de rede, na solução de problemas e nas alterações que precisam ser feitas no equipamento. O CDP também pode ser usado como uma ferramenta de descoberta de redes para detectar as informações sobre os dispositivos vizinhos. Essas informações coletadas do CDP podem ajudá-lo a criar uma topologia lógica de rede quando a documentação estiver ausente ou com poucos detalhes.


## 37.2.11 Descobrir dispositivos usando CDP

Considere a falta de documentação na topologia mostrada na figura. O administrador da rede sabe apenas que o R1 está conectado a outro dispositivo.

![[Pasted image 20260702202451.png]]

Com o CDP ativado na rede, o **comando show cdp neighbors** pode ser usado para determinar o layout da rede, conforme mostrado na saída.

```
R1# show cdp neighbors
Capability Codes: R - Router, T - Trans Bridge, B - Source Route Bridge
                  S - Switch, H - Host, I - IGMP, r - Repeater, P - Phone,
                  D - Remote, C - CVTA, M - Two-port Mac Relay
  
Device ID        Local Intrfce     Holdtme    Capability  Platform  Port ID
S1               Gig 0/0/1           179         S I      WS-C3560- Fas 0/5
```

Não há informações disponíveis a respeito do resto da rede. O comando **show cdp neighbors** fornece informações úteis sobre cada dispositivo CDP vizinho, inclusive:

- **Identificadores** de dispositivo- Este é o nome do host do dispositivo vizinho (S1).
- **Identificador** de porta- Este é o nome da porta local e remota (G0/0/1 e F0/5, respectivamente).
- **Lista** de recursos- Isso mostra se o dispositivo é um roteador ou um comutador (S para comutador; I para IGMP está além do escopo deste curso) 
- **Platforma** - Esta é a plataforma de hardware do dispositivo (WS-C3560 para switch Cisco Catalyst 3560).

A saída mostra que há outro dispositivo Cisco, S1, conectado à interface G0/0/1 em R1. Além disso, S1 é conectado por meio de sua porta F0/5, conforme mostrado na topologia atualizada.

![[Pasted image 20260702202518.png]]

O administrador de rede usa **show cdp neighbors detail** para descobrir o endereço IP de S1. Conforme exibido na saída, o endereço para S1 é 192.168.1.2.

```
R1# show cdp neighbors
-------------------------
Device ID: S1
Entry address(es):
  IP address: 192.168.1.2
Platform: cisco WS-C3560-24TS, Capabilities: Switch IGMP
Interface: GigabitEthernet0/0/1, Port ID (outgoing port): FastEthernet0/5
Holdtime : 136 sec
  
Version :
Cisco IOS Software, C3560 Software (C3560-LANBASEK9-M), Version 15.0(2)SE7, R
RELEASE SOFTWARE (fc1)
Technical Support: http://www.cisco.com/techsupport
Copyright (c) 1986-2014 by Cisco Systems, Inc.
Compiled Thu 23-Oct-14 14:49 by prod_rel_team
  
advertisement version: 2
Protocol Hello: OUI=0x00000C, Protocol ID=0x0112; payload len=27,
value=00000000FFFFFFFF010221FF000000000000002291210380FF0000
VTP Management Domain: ''
Native VLAN: 1
Duplex: full
Management address(es):
  IP address: 192.168.1.2
  
Total cdp entries displayed : 1
```

Acessando S1 remotamente por meio de SSH ou fisicamente por meio da porta do console, o administrador de rede pode determinar quais outros dispositivos estão conectados a S1, conforme exibido na saída de show **cdp neighbors** na figura.

```
S1# show cdp neighbors
Capability Codes: R - Router, T - Trans Bridge, B - Source Route Bridge
                  S - Switch, H - Host, I - IGMP, r - Repeater, P - Phone,
                  D - Remote, C - CVTA, M - Two-port Mac Relay
Device ID        Local Intrfce     Holdtme    Capability  Platform  Port ID
S2               Fas 0/1           150              S I   WS-C2960- Fas 0/1
R1               Fas 0/5           179             R S I  ISR4331/K Gig 0/0/1
```

A saída exibe as especificações da conexão com R1. Ele também exibe S2, outro switch ao qual S1 está conectado. Especificamente, a saída especifica que S2 é um switch Catalyst 2960 usando F0/1 para se conectar à interface F0/1 em S1.

![[Pasted image 20260702202610.png]]

Novamente, o administrador de rede pode usar **show cdp neighbors detail** para descobrir o endereço IP de S2 e, em seguida, acessá-lo remotamente. Após um login bem-sucedido, o administrador de rede usa o **comando show cdp neighbors** para descobrir se há mais dispositivos.

```
S2# show cdp neighbors
Capability Codes: R - Router, T - Trans Bridge, B - Source Route Bridge
                  S - Switch, H - Host, I - IGMP, r - Repeater, P - Phone,
                  D - Remote, C - CVTA, M - Two-port Mac Relay
Device ID        Local Intrfce     Holdtme    Capability  Platform  Port ID
S1               Fas 0/1           141              S I   WS-C3560- Fas 0/1
```

O único dispositivo conectado a S2 é o S1. Dessa forma, não há mais dispositivos para descobrir na topologia. Agora o administrador de rede pode atualizar a documentação para refletir os dispositivos descobertos.

## 37.2.12 Packet Tracer - Use o CDP para Mapear uma Rede

Um administrador de rede sênior exige que você mapeie a rede da Filial remota e descubra o nome de um switch instalado recentemente e que ainda precisa ter um endereço IPv4 configurado. Sua tarefa é criar um mapa da rede da filial. Para mapear a rede, você usará SSH para acesso remoto e Protocolo de Descoberta da Cisco (Cisco Discovery Protocol ou CDP) para descobrir informações sobre dispositivos de rede vizinhos, como roteadores e switches.

## 37.2.13 Packet Tracer - Desafio de Solução de Problemas - Documentar a Rede

Nesta atividade de Tracer de Pacotes, você documentará uma rede que é desconhecida para você.

- Teste a conectividade de rede.
- Compilar informações de endereçamento do host.
- Acesse remotamente dispositivos de gateway padrão.
- Documentar configurações de dispositivo de gateway padrão.
- Descubra dispositivos na rede.
- Desenhe a topologia de rede.

**Observação**: Certifique-se de guardar sua documentação. Será necessária para uma atividade mais adiante neste módulo.


# 37.3 Central de Ajuda (Help Desk)

## 37.3.1 A Política de Segurança 

As organizações operam com políticas corporativas, de funcionários e de segurança bem definidas.

O documento “Security Policy” contém políticas que informam usuários, equipe de TI e gerentes sobre os requisitos para proteção de ativos de tecnologia e informação. Conforme mostrado na figura, existem políticas para:

- Especificar como os usuários são identificados e autenticados
- Configurar o comprimento, a complexidade e o intervalo de atualização da senha
- Definir qual comportamento é aceitável na rede corporativa
- Especificar requisitos de acesso remoto, etc

![[Pasted image 20260702202710.png]]

O documento de política de segurança é um documento em constante evolução que reage a mudanças no cenário de ameaças, novas vulnerabilidades e requisitos de negócios e funcionários. A Política de Segurança ajuda a equipe de TI a entender o que deve fazer para manter a rede operacional e segura usando:

**Procedimentos operacionais padrão (SOP)** - definem ações passo a passo que devem ser concluídas para que qualquer tarefa esteja em conformidade com uma política. Existem SOPs a serem seguidos ao substituir dispositivos de rede, instalar (ou desinstalar) aplicativos, integrar novos funcionários, demitir funcionários existentes e muito mais.

**Diretrizes** - Abrangem as áreas onde não há SOPs definidos.

Quando os usuários encontram um problema ou precisam de suporte de rede, eles devem entrar em contato com um “help desk”. O help desk auxilia os usuários seguindo os SOPs e diretrizes definidos. O help desk usará um sistema de tickets para gerenciar as etapas dentro do ciclo de vida de solução de problemas mostrado na figura a seguir.

Este tópico se concentrará no uso de um sistema de tickets para concluir as três primeiras etapas mostradas na figura.

![[Pasted image 20260702202722.png]]

## 37.3.2 Help Desks 

Um help desk é uma equipe especializada em um departamento de TI que é o ponto central de contato para funcionários ou clientes.

Quando os usuários precisam de suporte, eles devem entrar em contato com o help desk de TI. Isso pode ser feito usando uma ferramenta de notificação on-line, chat ao vivo, telefone ou e-mail (por exemplo, suporte-de-TI@email.com). As centrais de atendimento costumam usar uma conta de e-mail “compartilhada”. Isso significa que todos os técnicos de helpdesk podem ver as solicitações de e-mail e respondê-las adequadamente.

**Nota**: A ferramenta de notificação on-line pode ser integrada ao sistema de ticketing.

Frequentemente, o técnico de help desk pode ser capaz de responder ou resolver rapidamente os problemas do usuário. Por exemplo, se uma organização teve uma falha na rede de internet, os usuários podem entrar em contato com o suporte técnico perguntando por que não conseguem acessar sites externos. O técnico informaria que a rede estava fora do ar e que deveria estar operacional dentro de um horário específico.

No entanto, se a solicitação de suporte for válida, o técnico criará um “ticket de problema”. Isso é feito usando um software especial de sistema de tickets para gerenciar solicitações, incidentes e problemas relatados. Esses “tickets” podem ser criados pelo usuário usando um painel do sistema de tickets ou por um técnico de help desk. Normalmente, um usuário inicia o ticket e o técnico de help desk o valida.

O técnico de help desk pode ter que coletar informações adicionais sobre a solicitação. Ao questionar os usuários, use técnicas de questionamento eficazes e ouça atentamente as respostas do usuário. Você também pode ter que investigar fisicamente o dispositivo ou conectar-se remotamente para replicar o problema, executar comandos e verificar as configurações.

O técnico então analisaria os dados coletados e:

**Resolver o problema** - Assim que o problema do usuário for resolvido, o técnico atualizará e fechará o ticket de problema. Atualizar a solução de tickets é importante porque pode preencher o banco de dados do sistema de tickets. Portanto, se o mesmo problema for relatado por outro usuário, o técnico respondente pode pesquisar o banco de dados para resolver o problema rapidamente. Além disso, os administradores podem analisar os tickets para identificar problemas comuns e suas causas para eliminar globalmente o problema, se possível.

**Escalar o ticket de problema** - Alguns problemas são mais complexos ou requerem acesso a dispositivos para os quais o técnico não possui credenciais. Nesses casos, o técnico deve escalar (ou seja, encaminhar) o ticket de problema para um técnico mais experiente. É importante que toda a documentação capturada do usuário seja clara, concisa e precisa.

A figura resume um processo típico de ticket de problema que um técnico de help desk teria que executar.

**Nota**: Os processos podem variar dependendo da organização.

![[Pasted image 20260702202747.png]]

## 37.3.3 Sistemas de Ticket 

Os sistemas de tickets de suporte técnico ajudam as organizações a gerenciar problemas ou solicitações de usuários. O software de tickets foi projetado especificamente para garantir que usuários ou clientes corporativos recebam suporte de maneira oportuna e sistemática. Eles também garantem que todos os tickets sejam notados e endereçados.

Uma caixa de correio compartilhada é um método alternativo que pode ser usado por uma organização para dar suporte às solicitações do usuário. Os técnicos de suporte técnico compartilhariam a mesma caixa de correio e responderiam a e-mails para resolver problemas.

Os sistemas de ticketing variam de acordo com a necessidade da organização. Por exemplo, existem sistemas de ticketing projetados para as necessidades de usuários corporativos internos e outros sistemas para dar suporte a provedores de serviços ou clientes externos.

**Observação**: uma rápida pesquisa na Internet por “software de help desk” revela muitos fornecedores de software diferentes, incluindo Zendesk, HaloITSM, Connectwise e muito mais.

A figura mostra um exemplo de ticket projetado para ajudá-lo a entender quais informações um ticket de suporte técnico pode capturar.

![[Pasted image 20260702202807.png]]

A tabela descreve os campos que podem ser usados quando um registro de problema é criado.

|Nome do campo|Campo Contém ...|
|---|---|
|Número do ticket|Um número exclusivo gerado automaticamente pelo sistema de ticketing para acompanhar a solicitação<br>O número do ticket nunca muda|
|Data de criação|Uma lista suspensa que exibe a data em que o ticket foi criado|
|Descrição|Um campo de formato livre que descreve a solicitação|
|Reportado por|Campos de formato livre que identificam quem solicitou o suporte|
|Categoria|Uma lista suspensa para selecionar categorias pré-determinadas<br>Isso é útil para agrupar tickets relacionados<br>Por exemplo, Solicitação de novo dispositivo/aplicativo, Integração/Encerramento de funcionário, Suporte, Relatar um problema e Incidente de segurança|
|Prioridade / Severidade|Uma lista suspensa para selecionar níveis de prioridade pré-determinados<br>Por exemplo, alto, médio, baixo ou crítico, maior e menor|
|Status|Uma lista suspensa para selecionar níveis de status pré-determinados<br>Por exemplo, não iniciado, aberto, em andamento, concluído|
|Criado por, Atribuído a|Campos de formato livre que identificam o técnico que criou o ticket e a quem o ticket foi atribuído se o escalonamento for necessário|
|Detalhes Data e especificidades|Uma lista suspensa que exibe a data em que o ticket foi atualizado<br>Um campo de formato livre para atualizar o ticket|

**Observação**: Outros campos também podem estar disponíveis, como tipo e modelo de plataforma, versão do sistema operacional, conexão de rede utilizada e outros.

Nesse exemplo de ticket, alguns campos são gerados pelo sistema (em laranja), por meio de caixas drop-down (em azul) ou de forma livre (em amarelo). Os campos suspensos facilitam a inserção e a manutenção da consistência. Os campos de formato livre são usados pelo técnico de help desk para adicionar informações descritivas.

Os campos de formato livre serão lidos por outros técnicos e gerentes. Portanto, é importante usar uma comunicação escrita clara e concisa. Use linguagem simples e frases curtas. Sempre preste atenção à sua ortografia, gramática e estilo.

## 37.3.4 Peguntar aos usuários finais 

Ao solicitar suporte de um help desk, os usuários geralmente fornecem informações vagas e às vezes errôneas. Por exemplo, os usuários geralmente relatam problemas como “A rede está inativa.”, “Não consigo acessar meu e-mail.” ou “Meu computador está lento”. Na maioria dos casos, informações adicionais são necessárias para entender completamente o problema.

Ao inserir o ticket de problema, o técnico de help desk deve descobrir “quem”, “o quê” e “quando” do problema.

As seguintes recomendações devem ser empregadas ao se comunicar com um usuário:

Seja sempre atencioso e empatize com os usuários enquanto os deixa saber que você vai ajudá-los a resolver seu problema. Os usuários que relatam um problema podem estar sob estresse e ansiosos para resolver o problema o mais rápido possível. Nunca diminua, menospreze, insulte ou acuse o usuário de causar o problema.

Fale em um nível técnico que eles possam entender. Evite usar terminologia complexa ou jargão da indústria.

Sempre ouvir ou ler atentamente o que o usuário está dizendo. Tomar notas pode ser útil ao documentar um problema complexo.

Boas habilidades interpessoais são um trunfo para o técnico de helpdesk. É importante desenvolver esse conjunto de habilidades para melhor atender e se comunicar com usuários e colegas. Por exemplo, um técnico deve se dirigir a um usuário por seu nome preferido, tentar se relacionar com o usuário e trabalhar para esclarecer exatamente o que ele está solicitando.

### Conhecer, se relacionar e entender

A tabela resume três diretrizes gerais que ajudam a desenvolver o conjunto de habilidades Conhecer, se relacionar e entender.

| Regra         | Sugestão                                                                                                   | Exemplo                                                                                                                                                                                                                                                                                                                                                                |
| ------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Conhecer      | Chame o usuário pelo nome.<br>Você pode perguntar se há algum nome que eles prefiram que você use.         | Se um usuário lhe disser que o nome dela é Sra. Johnson, pergunte se é assim que ela prefere ser chamada por você.<br>Ela pode dizer sim ou pode fornecer seu primeiro nome.<br>Em qualquer caso, use apenas o nome preferencial com seu cliente.                                                                                                                      |
| Se relacionar | Tente criar uma conexão um-para-um com o usuário.                                                          | Tente encontrar algo que vocês possam ter em comum.<br>Se você ouvir um animal de estimação ao fundo, pergunte brevemente sobre isso.<br>Se você teve que ligar para o suporte ao cliente do seu próprio computador, mencione que você entendeu o quanto isso pode ser frustrante e que você fará tudo o que puder para ajudá-los.<br>Não perca o controle da chamada. |
| Entender      | Determine o nível de conhecimento técnico do usuário.<br>Isso ajudará você a se comunicar melhor com eles. | Um cliente que é muito novo em computadores provavelmente não saberá todo o jargão que você usa todos os dias, então você deve usar as palavras mais comuns que você pode pensar para descrever os aspectos de seu computador.<br>Um cliente mais experiente provavelmente sabe um pouco do mesmo jargão que você usa.                                                 |
Ao entrevistar o usuário, oriente a conversa e use técnicas de questionamento eficazes para verificar rapidamente o problema. Dois métodos comuns para fazer isso incluem o uso de:

**Perguntas abertas** – Permitem aos usuários explicar detalhes do problema e são úteis para obter informações gerais.

**Perguntas fechadas** - Estas são respostas simples de sim, não ou de uma única palavra para descobrir fatos sobre o problema.

### Perguntas abertas do usuário final

A tabela fornece algumas diretrizes de questionamento e exemplos de perguntas abertas ao usuário final.

| Diretrizes                                                    | Exemplos de perguntas abertas do usuário final                                                                                             |
| ------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Faça perguntas pertinentes.                                   | O que não funciona?<br>Qual é exatamente o problema?<br>O que você está tentando realizar?                                                 |
| Determine o escopo do problema.                               | Quem esse problema afeta? É só você ou os outros?<br>Em que dispositivo é que isto está a acontecer?                                       |
| Determine quando ocorreu o problema/ocorre.                   | Quando o problema ocorre exatamente?<br>Quando o problema foi observado pela primeira vez?<br>Houve alguma mensagem(s) de erro exibida(s)? |
| Determine se o problema é constante ou intermitente.          | Você pode reproduzir o problema?<br>Você pode me enviar uma captura de tela ou vídeo do problema?                                          |
| Determine se alguma coisa mudou.                              | O que mudou desde a última vez que funcionou?                                                                                              |
| Use perguntas para eliminar ou descobrir possíveis problemas. | O que funciona?<br>O que não funciona?                                                                                                     |

Ao terminar de entrevistar o usuário, repita sua compreensão do problema para o usuário para garantir que ambos concordem com o que está sendo relatado.

## 37.3.5 Verifique sua Compreensão - Perguntas Fechadas e Abertas

### Pergunta 1

Combine a pergunta que um técnico pode fazer ao cliente com o tipo de pergunta.

|Categoria|Resposta correta|
|---|---|
|Que problemas você está tendo com o computador ou a rede?|Pergunta Aberta|
|O que você estava fazendo quando o problema foi identificado?|Pergunta Aberta|
|Qual software foi instalado recentemente no seu computador?|Pergunta Aberta|
|Quais alterações de hardware foram feitas recentemente em seu computador?|Pergunta Aberta|
|Você pode reproduzir o problema?|Pergunta Fechada|
|Você está conectado à rede?|Pergunta Fechada|
|Você mudou a sua senha nos últimos dias?|Pergunta Fechada|
|Seu computador foi usado por outra pessoa?|Pergunta Fechada|
|Você recebeu mensagens de erro no computador?|Pergunta Fechada|

### Pergunta 2

Leia cada pergunta e indique se é aberta ou fechada.

|Categoria|Resposta correta|
|---|---|
|Você pode me dizer o que estava fazendo quando o problema ocorreu pela primeira vez?|Aberta|
|O que você já tentou fazer para corrigir esse problema?|Aberta|
|Seu computador está executando o Windows 10?|Fechada|
|Por quanto tempo você teve esse Notebook?|Fechada|

## 37.3.6 Escuta Ativa 

Para entender melhor o problema relatado pelo usuário, pratique habilidades de escuta ativa. Permita que o cliente conte toda a história. Durante a explicação do cliente sobre o problema, emita de vez em quando qualquer palavra ou frase pequena, como “Entendo”, “Sim”, “Sei” ou “OK”. Esse comportamento permite que o cliente saiba que você continua na linha e está ouvindo.

No entanto, o técnico não deve interromper o cliente para fazer uma pergunta ou se expressar. Além de ser rude e desrespeitoso, isso cria tensão. Muitas vezes, em uma conversa, você pode se pegar pensando no que dizer antes que a outra pessoa termine de falar. Ao fazer isso, você não está ouvindo ativamente. Em vez disso, escute com atenção quando os clientes falarem e deixe que eles completem os pensamentos.

Se você solicitou que o cliente explicasse o problema para você, isso é conhecido como uma pergunta aberta. Uma pergunta aberta raramente tem uma resposta simples. Normalmente, ele envolve informações sobre o que o cliente estava fazendo, o que ele está tentando fazer e por que eles estão frustrados.

Depois de ouvir o cliente explicar todo o problema, resuma o que ele disse. Isso ajuda a convencê-lo que você ouviu e entendeu a situação. Uma boa prática de esclarecimento é parafrasear a explicação do cliente começando com as palavras “deixa eu ver se entendi o que você falou”. Essa é uma ferramenta muito eficaz que demonstra ao cliente que você ouviu e entendeu.

Depois de garantir ao cliente que compreende o problema, é provável que você precise fazer algumas perguntas de acompanhamento. Mas antes certifique-se de que elas são pertinentes. Não faça perguntas que já tenham sido respondidas pelo cliente durante a descrição do problema. Isso irrita o cliente e mostra que você não estava prestando atenção.

As perguntas de acompanhamento devem ser perguntas fechadas e direcionadas, com base nas informações que você obteve. A finalidade das perguntas fechadas é adquirir informação específica. O cliente deve responder com “sim” ou “não”, ou com uma resposta direta, como “Windows 10”.

Use todas as informações coletadas do cliente para preencher o ticket de problema.

Documente as informações fornecidas pelo usuário no ticket do problema. Inclua tudo o que você acha que pode ser importante para você ou outro técnico. Os pequenos detalhes geralmente levam à solução de um problema difícil ou complicado.

Quando o ticket for concluído, o técnico deve repetir sua compreensão do problema para o usuário para garantir que ambos concordem com o problema que está sendo relatado.


## 37.3.7 Demonstração em vídeo - Escuta Ativa e Resumo 

Dicas para usar a escuta ativa com um cliente

- Permita que o cliente conte seu problema.
- Emitir de vez em quando qualquer palavra ou frase pequena, como “Entendo”, “Sim”, “Sei” ou “OK”, para que o cliente saiba que você está ouvindo.
- Resumir o problema do cliente quando ele terminar, para que ambos tenham certeza de que você entendeu.
- Faça perguntas esclarecedoras.
- Não interrompa o cliente no momento em que você perceber que tem uma pergunta.

Selecione **Reproduzir** para ver o vídeo.

**Chamada 1**

- Obrigado por ligar para o suporte ao cliente. Meu nome é Lee. Em que posso ajudar você?
- Eu sou Chris.
- Olá, Chris. Qual parece ser o problema hoje?
- Achei que seria óbvio, mas aparentemente não é, meu computador não está funcionando. Por que eu ligaria para você, caso contrário?
- Oh, aqui vamos nós.
- Com licença?
- Seu arquivo diz que você tem um Dell Latitude.
- Sim, tenho uma atitude Dell e tenho ouvidos e ouvi que você disse 'lá vamos nós'.
- Então, Lee, eu gostaria de ser transferido para Rebecca. Rebecca está disponível agora?
- Eu não sei. Acabou de me colocar em espera?

**Chamada 2**

- Obrigado por ligar para o suporte ao cliente. Meu nome é Lee. Em que posso ajudar você?
- Eu sou Chris.
- Olá, Chris. Qual parece ser o problema hoje?
- Achei que seria óbvio, mas aparentemente não é, meu computador não está funcionando. Por que eu ligaria para você, caso contrário?
- Entendo. Chris, deixe-me fazer o que puder para que sua máquina volte a funcionar. Agora, seu registro mostra que você tem uma Dell Latitude. Executando Windows 10.
- Sim. É um 2 em 1
- e vejo que você já ligou para nós antes em relação a este computador. Você é novo aqui?
- Prefiro falar com Rebecca. Ela já me ajudou com este problema no touchscreen.
- Bem, ela está aqui, mas está numa ligação. Quer que eu descubra quando ela estará disponível? Eu ficaria feliz em fazer isso. Ou posso guiar você pelos passos para resolver o problema.
- Não quero esperar.
- Ok, Chris, vamos resolver este problema o mais rapidamente possível.


## 37.3.8 Coletar informações para tickets relacionados ao host 

O sistema de emissão de tickets geralmente inclui seções para inserir informações relacionadas ao host. Esses campos geralmente são preenchidos durante a etapa "Obter Informações" do ciclo de vida de solução de problemas.

Informações úteis relacionadas ao host incluem:

- Fabricante do host, modelo, número de série
- Versão do sistema operacional
- Ambiente de rede (ou seja, com fio, sem fio, …)
- Resultados do teste de conectividade de rede (ping, tracert, …)

Informações adicionais que podem ser capturadas de um host incluem:

- Códigos de bipe
- Logs do Visualizador de Eventos
- Configurações do Gerenciador de Dispositivos
- Dados do gerenciador de tarefas
- Resultados da ferramenta de diagnóstico

Selecione cada guia para obter mais informações sobre essas ferramentas.

### **Códigos de Bipes**

Cada fabricante de BIOS tem uma sequência única de bipes, uma combinação de bipes curtos e longos, para falhas de hardware. Ao solucionar problemas, ligue o computador e ouça. Enquanto o sistema prossegue com o POST, a maioria dos computadores emite um bipe para indicar que o sistema está sendo inicializado corretamente. Se houver um erro, você poderá ouvir vários bipes. Documente a sequência de bipes e pesquise-a para determinar o problema específico.

**Informações da BIOS**

Se o computador inicializa e para após o POST, investigue as configurações da BIOS. Um dispositivo não pode ter sido detectado ou configurado corretamente. Consulte a documentação da placa-mãe para garantir que as configurações da BIOS estejam corretas.

### **Visualizador de Eventos**

Quando ocorrem erros de sistema, usuário ou software em um computador com Windows, o Visualizador de Eventos (Event Viewer) mostrado na figura é atualizado com informações sobre os erros.

O aplicativo Event Viewer registra as seguintes informações sobre o problema:

- Qual problema ocorreu
- Data e hora do problema
- Gravidade dos problemas
- Origem dos problemas
- Número de ID do evento
- Qual usuário estava conectado quando o problema ocorreu

Embora o Visualizador de Eventos liste detalhes sobre o erro, você precisa pesquisar mais sobre o problema para determinar uma solução.

![[Pasted image 20260702203444.png]]

### **Gerenciador de Dispositivos**

O Gerenciador de Dispositivos, mostrado na figura, exibe todos os dispositivos que estão configurados em um computador.

O sistema operacional sinaliza com um ícone de erro os dispositivos que não estão operando corretamente. Um triângulo amarelo com um ponto de exclamação indica que o dispositivo está em um estado problemático. Um X vermelho significa que o dispositivo está desativado, removido ou o Windows não consegue localizar o dispositivo. Uma seta para baixo significa que o dispositivo foi desativado. Um ponto de interrogação amarelo indica que o sistema não sabe qual driver instalar para o hardware.

![[Pasted image 20260702203455.png]]

### **Gerenciador de Tarefas**

O Gerenciador de Tarefas, mostrado na figura, exibe os aplicativos e processos em segundo plano que estão em execução no momento.

Com o Gerenciador de Tarefas, você pode fechar os aplicativos que pararam de responder. Você também pode monitorar o desempenho da CPU e da memória virtual, visualizar todos os processos em execução no momento e visualizar informações sobre as conexões de rede.

![[Pasted image 20260702203508.png]]

### **Ferramentas de Diagnóstico**

Faça a pesquisa para determinar qual software está disponível para ajudar a diagnosticar e a resolver problemas. Há muitos programas para ajudá-lo a solucionar problemas de hardware. Os fabricantes de hardware normalmente fornecem suas próprias ferramentas de diagnóstico. Por exemplo, um fabricante de disco rígido pode oferecer uma ferramenta para inicializar o computador e para diagnosticar o motivo pelo qual o disco rígido não inicializa o sistema operacional.


### 37.3.9 Coletar informações para tíquetes relacionados a dispositivos Cisco

Para coletar sintomas de um dispositivo de rede suspeito de ter problemas, use os comandos do Cisco IOS e outras ferramentas, como capturas de pacotes e logs de dispositivos.

### Comandos do Cisco IOS para coletar informações

A tabela descreve comandos comuns do Cisco IOS usados para reunir os sintomas de um problema de rede.

| Comando                                                  | Descrição                                                                                                                                                      |
| -------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ping {host \| ip-address}`                              | Envia um pacote echo request a um endereço e espera uma resposta.<br>A variável _host_ ou _ip-address_ é o alias de IP ou o endereço IP do sistema de destino. |
| `traceroute destination`                                 | Identifica o caminho percorrido por um pacote nas redes.<br>A variável _destination_ é o nome de host ou o endereço IP do sistema de destino.                  |
| `telnet {host \| ip-address}`                            | Conecta-se a um endereço IP por meio do aplicativo Telnet.<br>Usar SSH sempre que possível em vez de Telnet.                                                   |
| `ssh -l user-id ip-address`                              | Conecta-se a um endereço IP com SSH.<br>O SSH é mais seguro do que o Telnet.                                                                                   |
| `show ip interface brief`<br>`show ipv6 interface brief` | Exibe um status resumido de todas as interfaces em um dispositivo.<br>Útil para identificar rapidamente o endereçamento IP em todas as interfaces.             |
| `show ip route`<br>`show ipv6 route`                     | Exibe as tabelas de roteamento IPv4 e IPv6 atuais, que contêm as rotas para todos os destinos de rede conhecidos.                                              |
| `show protocols`                                         | Exibe os protocolos configurados e mostra o status global e específico da interface de qualquer protocolo configurado da camada 3.                             |

### 37.3.10 Analisar as Informações 

Agora que o registro de problema foi criado e as informações coletadas, o técnico deve analisar as informações. Para conseguir isso, o técnico conta com sua experiência, bases de conhecimento e outras fontes de informação para decidir se pode resolver o problema. O técnico também pode se comunicar com colegas para obter informações sobre o problema.

As bases de conhecimento que podem ser pesquisadas incluem:

- **Bancos de dados de software de tickets** - A maioria dos sistemas de tickets cria um repositório de tickets anteriores que podem ser pesquisados para ver se outro técnico resolveu um problema idêntico ou semelhante.
- **Recursos do fornecedor** - Os fornecedores mantêm documentos de perguntas frequentes (FAQs) que podem ser pesquisados e também podem oferecer ferramentas on-line para ajudar a resolver problemas. Alguns oferecem chats ao vivo para resolver problemas mais rapidamente.
- **Pesquisas on-line na Internet -** Usando mecanismos de pesquisa para verificar se um problema foi encontrado anteriormente.

Se o problema não puder ser resolvido, o ticket deverá ser escalado para um membro da equipe de TI mais experiente.

