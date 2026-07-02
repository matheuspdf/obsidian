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

