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

## 37.3.11 Verifique sua compreensão – Help Desks

### Pergunta 1

Quais são as duas abordagens de comunicação eficazes para solucionar um problema para um usuário final? (Escolha duas.)

- [x] Ouça atentamente enquanto o usuário explica o problema.
- [x] Fale no nível técnico do usuário.
- [ ] Use o jargão mais atual do setor ao discutir o problema com o usuário.
- [ ] Espere até que a conversa termine antes de fazer anotações.
- [ ] Coloque o usuário em espera enquanto você tenta resolver o problema.

✅ RESPOSTA CORRETA: Ouça atentamente enquanto o usuário explica o problema.; Fale no nível técnico do usuário.

> Está certo. Ao se comunicar com um usuário final para resolver um problema, você deve falar em um nível técnico que ele possa entender, ouvir atentamente sem interromper quando ele estiver falando e fazer anotações para documentar a conversa. Você também deve evitar o uso de jargões técnicos e da indústria. Não coloque o usuário em espera para resolver o problema. Em vez disso, informe-os de que resolver o problema é importante e que você os acompanhará assim que uma solução for encontrada.

### Pergunta 2

Que tipo de informação pode ser coletada emitindo o **comando show ip interface brief** do IOS?

- [x] um resumo do status e endereços IP atribuídos de todas as interfaces
- [ ] uma lista de protocolos configurados e status específico da interface de protocolos habilitados da camada 3
- [ ] uma lista de versões de software instaladas para todos ou componentes específicos
- [ ] uma lista de todas as rotas IPv4 e IPv6 atuais

✅ RESPOSTA CORRETA: um resumo do status e endereços IP atribuídos de todas as interfaces

> Está certo. O comando show ip interface brief exibirá um resumo do status e dos endereços IP de todas as interfaces do dispositivo.

### Pergunta 3

Durante a etapa de coleta de informações, qual comando exibirá os protocolos configurados e o status global e específico da interface de qualquer protocolo da Camada 3 configurado?

- [x] show protocols
- [ ] show ip route
- [ ] show ip interface brief
- [ ] debug

✅ RESPOSTA CORRETA: show protocols

> Está certo. O comando show protocols exibe os protocolos configurados no dispositivo e o status específico da interface de quaisquer protocolos da Camada 3 habilitados.

### Pergunta 4

Como as bases de conhecimento baseadas em fornecedores são usadas para auxiliar na solução de problemas?

- [ ] Elas podem ajudar com tarefas de documentação comuns, como desenhar diagramas de rede, manter software de rede e documentação de hardware atualizados e medir a linha de base de uso de largura de banda de rede.
- [ ] Elas podem ser usadas para investigar e corrigir problemas de rede e permitir que os administradores de rede monitorem dispositivos remotos de forma contínua e automática.
- [x] Elas podem ser combinadas com mecanismos de busca na Internet para fornecer ao administrador de rede acesso a um vasto conjunto de informações baseadas em experiência.
- [ ] Elas podem fornecer software de gerenciamento de dispositivo para mostrar o status dinâmico de dispositivos, estatísticas e informações de configuração para os principais dispositivos de rede.

✅ RESPOSTA CORRETA: Elas podem ser combinadas com mecanismos de busca na Internet para fornecer ao administrador de rede acesso a um vasto conjunto de informações baseadas em experiência.

> Está certo. As bases de conhecimento de fornecedores de dispositivos de rede on-line são fontes importantes de informações para administradores de rede. Quando essas bases de conhecimento são combinadas com os mecanismos de pesquisa da Internet, elas fornecem ao administrador um grande conjunto de informações baseadas na experiência.


# 37.4 Solucionar problemas de conectividade de endpoint

## 37.4.1 Configuração de rede do Windows

Se você usou alguma das ferramentas para verificar a conectividade e descobriu que alguma parte da sua rede não está funcionando como deveria, agora é a hora de usar alguns comandos para solucionar problemas de seus dispositivos. Comandos de host e de IOS podem ajudá-lo a determinar se o problema está no endereço IP de seus dispositivos, o que é um problema de comum em redes.

Verificar o endereçamento IP em dispositivos host é uma prática comum em rede para verificar e solucionar problemas de conectividade de ponta a ponta. No Windows 10, você pode acessar os detalhes do endereço **IP em Centro** de Rede e Compartilhamento > _interface_ > **Detalhes**. Conforme mostrado na figura, os detalhes da interface revelam o endereço IP do host, a máscara de sub-rede, o gateway padrão e os servidores DNS conhecidos.

![[Pasted image 20260702213434.png]]

O método preferencial usado pelos técnicos para visualizar as informações de endereçamento IP em um host Windows é usar o **comando ipconfig** do Windows, conforme mostrado na saída de amostra.

```
C:\Users\PC-A> ipconfig
Windows IP Configuration
(Output omitted)
Wireless LAN adapter Wi-Fi:
   Connection-specific DNS Suffix   . :
   Link-local IPv6 Address . . . . . :
fe80::a4aa:2dd1:ae2d:a75e%16
   IPv4 Address. . . . . . . . . . . : 192.168.10.10
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : 192.168.10.1
(Output omitted)
```

O **comando ipconfig /all** é usado para exibir detalhes de endereçamento adicionais, conforme mostrado na saída de exemplo.

```
C:\Users\PC-A> ipconfig /all
Windows IP Configuration
   Host Name . . . . . . . . . . . . : PC-A-00H20
   Primary Dns Suffix . . . . . . . : cisco.com
   Node Type . . . . . . . . . . . . : Hybrid
   IP Routing Enabled. . . . . . . . : No
   WINS Proxy Enabled. . . . . . . . : No
   DNS Suffix Search List. . . . . . : cisco.com
(Output omitted)
Wireless LAN adapter Wi-Fi:
   Connection-specific DNS Suffix   . :
   Description . . . . . . . . . . . : Intel(R) Dual Band Wireless-AC 8265
   Physical Address. . . . . . . . . : F8-94-C2-E4-C5-0A
   DHCP Enabled. . . . . . . . . . . : Yes
   Autoconfiguration Enabled . . . . : Yes
   Link-local IPv6 Address . . . . . :
fe80::a4aa:2dd1:ae2d:a75e%16(Preferred)
   IPv4 Address. . . . . . . . . . . : 192.168.10.10(Preferred)
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Lease Obtained. . . . . . . . . . : August 17, 2019 1:20:17 PM
   Lease Expires . . . . . . . . . . : August 18, 2019 1:20:18 PM
   Default Gateway . . . . . . . . . : 192.168.10.1
   DHCP Server . . . . . . . . . . . : 192.168.10.1
   DHCPv6 IAID . . . . . . . . . . . : 100177090
   DHCPv6 Client DUID. . . . . . . . : 00-01-00-01-21-F3-76-75-54-E1-AD-DE-DA-9A
   DNS Servers . . . . . . . . . . . : 192.168.10.1
   NetBIOS over Tcpip. . . . . . . . : Enabled
```

## 37.4.2 Verificação da conectividade no Windows

O comando **ping é** uma maneira eficaz de testar rapidamente a conectividade de Camada 3 entre um endereço IP de origem e de destino. Este comando também exibe várias estatísticas de tempo de ida e volta.

```
 C:\Users\PC-A> ping 10.1.1.10
 Pinging 10.1.1.10 with 32 bytes of data:
 Reply from 10.1.1.10: bytes=32 time=47ms TTL=51
 Reply from 10.1.1.10: bytes=32 time=60ms TTL=51
 Reply from 10.1.1.10: bytes=32 time=53ms TTL=51
 Reply from 10.1.1.10: bytes=32 time=50ms TTL=51
 Ping statistics for 10.1.1.10:
     Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
 Approximate round trip times in milli-seconds:
     Minimum = 47ms, Maximum = 60ms, Average = 52ms
 C:\Users\PC-A>
```

Conforme mostrado no exemplo acima, a saída valida a conectividade da Camada 3 entre o PC A e o dispositivo com o endereço IPv4 10.1.1.10.

O **traceroute** ou o comando **tracert** do Windows pode ajudar a localizar áreas problemáticas da Camada 3 em uma rede. O tracert retorna uma lista dos saltos no roteamento de um pacote pela rede. Ele pode ser usado para identificar o ponto ao longo do caminho onde o problema pode ser encontrado.

Alguns firewalls, como o Firewall do Windows, bloqueiam pings por padrão. É importante que isso faça parte da documentação da sua rede e esteja ciente dessas configurações ao testar e verificar a conectividade da rede.

![[Pasted image 20260702213823.png]]

Os técnicos geralmente preferem usar o comando **ifconfig** na janela de terminal para exibir o status

```
ubuntu@ubuntu2004:~$ ifconfig
enp0s3    Link encap:Ethernet HWaddr 08:00:27:b5:d6:cb
          inet addr: 10.0.2.15  Bcast:10.0.2.255  Mask: 255.255.255.0
          inet6 addr: fe80::57c6:ed95:b3c9:2951/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500 Metric:1
          RX packets:1332239 errors:0 dropped:0 overruns:0 frame:0
          TX packets:105910 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:1855455014 (1.8 GB)  TX bytes:13140139 (13.1 MB)
lo: flags=73 mtu 65536
          inet 127.0.0.1  netmask 255.0.0.0
          inet6 ::1  prefixlen 128  scopeid 0x10
          loop  txqueuelen 1000  (Local Loopback)
          RX packets 0  bytes 0 (0.0 B)
          RX errors 0  dropped 0  overruns 0  frame 0
          TX packets 0  bytes 0 (0.0 B)
          TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

O comando **ip address** do Linux é usado para exibir endereços e suas propriedades. Ele também pode ser usado para adicionar ou excluir endereços IP.

**Observação:** A saída exibida pode variar dependendo da distribuição Linux.

## 37.4.4 Verificar conectividade no Linux

O Linux oferece as mesmas ferramentas de ping traceroute que o Windows para verificar a conectividade de rede.

Existem várias outras ferramentas de linha de comando do Linux disponíveis para a maioria das distribuições do Linux, incluindo:

- **speedtest** - Esta é uma ferramenta que testa a largura de banda de sua conectividade com seu provedor de internet.
    
- **ncat** - Ncat é um utilitário de rede que faz parte do conjunto nmap de ferramentas de rede. Ncat ou nc, tem muitos usos, incluindo a verificação da conectividade com um dispositivo usando uma porta específica. Veja a seguir um exemplo de conectividade HTTPS (porta 443) de teste ncat para dois dispositivos diferentes.

```
ubuntu@ubuntu2004:~$ nc -z -v www.google.com 443
 Connection to www.google.com (142.250.138.105) 443 port [tcp/https] succeeded!
 ubuntu@ubuntu2004:~$
 ubuntu@ubuntu2004:~$ nc -z -v 10.0.0.122 443
 nc: connect to 10.0.0.122 port 443 (tcp) failed: Connection refused
 ubuntu@ubuntu2004:~$ 
```

## 37.4.5 Configuração de rede MacOS

Na GUI de um host Mac, abra **Network Preferences > Advanced** para obter as informações de endereço IP, conforme mostrado na figura.

![[Pasted image 20260702213914.png]]

No entanto, o **comando ifconfig** também pode ser usado para verificar a configuração de IP da interface mostrada na saída.

```
MacBook-Air:~ Admin$ ifconfig en0
en0: flags=8863 mtu 1500
        ether c4:b3:01:a0:64:98
        inet6 fe80::c0f:1bf4:60b1:3adb%en0 prefixlen 64 secured scopeid 0x5
        inet 10.10.10.113 netmask 0xffffff00 broadcast 10.10.10.255
        nd6 options=201
        media: autoselect
        status: active
MacBook-Air:~ Admin$
```

Outros comandos úteis do macOS para verificar as configurações de IP do host incluem **networksetup -listallnetworkservices** e networksetup **-getinfo <**_network service_**>,** conforme mostrado na saída a seguir.

```
MacBook-Air:~ Admin$ networksetup -listallnetworkservices
An asterisk (*) denotes that a network service is disabled.
iPhone USB
Wi-Fi
Bluetooth PAN
Thunderbolt Bridge
MacBook-Air:~ Admin$
MacBook-Air:~ Admin$ networksetup -getinfo Wi-Fi
DHCP Configuration
IP address: 10.10.10.113
Subnet mask: 255.255.255.0
Router: 10.10.10.1
Client ID:
IPv6: Automatic
IPv6 IP address: none
IPv6 Router: none
Wi-Fi ID: c4:b3:01:a0:64:98
MacBook-Air:~ Admin$
```

## 37.4.6 Verificar conectividade no MacOS 

Os **comandos ping** e **traceroute** para verificar a conectividade de rede também estão disponíveis no MacOS. Como o Linux, o MacOS é baseado no sistema operacional UNIX e, portanto, compartilha muitos dos mesmos comandos de conectividade de rede, incluindo **ncat** e **speedtest**.

Informações adicionais de verificação de rede podem ser obtidas usando a ferramenta MacOS **System Information**, conforme mostrado na figura. O exemplo exibe informações de Wi-Fi, incluindo protocolos de Wi-Fi compatíveis, como IEEE 802.11ac.

![[Pasted image 20260702214002.png]]

O aplicativo MacOS **Wireless Diagnostics** pode ser usado para solucionar problemas e monitorar a conectividade Wi-Fi. Ao selecionar a opção de monitorar a rede, o aplicativo irá gerar um relatório de diagnóstico.

![[Pasted image 20260702214010.png]]


## 37.4.7 Configurar e verificar a rede no iOS 

A conectividade de rede em um dispositivo Apple iOS pode ser facilmente verificada ao tentar acessar um site ou aplicativo online.

Você também pode verificar as informações de endereçamento IPv4 e IPv6, incluindo o gateway padrão (roteador) em um dispositivo Apple IOS, conforme mostrado na figura. Para fazer isso, vá para **Configurações** > **Wi-Fi** > Selecione o ícone de informações (i) à direita do nome da rede Wi-Fi ativa (SSID).

![[Pasted image 20260702214021.png]]

## 37.4.8 Configurar e verificar a rede no Android 

Como o Apple iOS, a conectividade de rede em um dispositivo Android pode ser verificada ao tentar acessar um site ou aplicativo online.

Se a conexão falhar, verifique se você tem uma conexão confiável com seu provedor de dados de celular. Se você estiver tentando se conectar por Wi-Fi, certifique-se de estar conectado a uma rede Wi-Fi e de ter se autenticado com sucesso nessa rede. Às vezes, é necessária autenticação adicional por meio de um método de autenticação alternativo que pode exigir a concordância com os termos de uso ou o fornecimento de informações de login adicionais.

Em algumas versões do Android, um ícone pode aparecer ao lado do indicador de intensidade do sinal Wi-Fi na barra de status do dispositivo, indicando um problema com a conexão com a Internet. A conectividade Wi-Fi pode ser estabelecida sem acesso à Internet. Isso pode indicar um problema com o gateway de Internet da rede à qual você está conectado ou pode indicar que outras medidas são necessárias para obter acesso à rede.

A interface do Android pode variar significativamente dependendo da versão do Android e do fabricante do dispositivo. Portanto, o processo de verificação das conexões de rede pode diferir ligeiramente entre os dispositivos.

Para acessar suas configurações de rede, abra o aplicativo de configurações em seu telefone e toque **em** Conexões ou **Rede e Internet**. Faça o seguinte:

1. Se estiver usando Wi-Fi, verifique se o Wi-Fi está ativo em seu telefone.
2. Toque em Wi-Fi e verifique se você está conectado a uma rede na qual possa se autenticar. Verifique as redes disponíveis para ver se outras redes podem ser mais adequadas. Pode ser necessário determinar a senha de rede para as várias redes que você verá. Verifique também se a força do sinal é adequada.
3. Se estiver usando uma rede de dados móveis de celular, verifique se você tem conectividade com essa rede na barra de status do dispositivo. Verifique o menu de configurações deslizante para garantir que os dados móveis estejam ativos em seu dispositivo.


As informações de endereçamento IPv4 e IPv6, incluindo o gateway padrão (roteador), podem ser verificadas em Configurações > ****Sobre** o telefone** > **Status**, conforme mostrado na figura.

![[Pasted image 20260702214037.png]]

Aplicativos de análise de rede de terceiros com várias funções estão disponíveis para Android. Eles podem fornecer informações mais detalhadas sobre as configurações de rede do dispositivo, permitir testes de rede com **ping** e **trace** e até mesmo realizar varreduras de portas e dispositivos de rede, conforme mostrado na figura.![[Pasted image 20260702214046.png]]


## 37.4.9 Laboratório - Verificar endereço com uma calculadora de sub-rede

Nesta atividade, você determinará o endereço IPv4 e a máscara de sub-rede de seu dispositivo e usará uma calculadora de sub-rede on-line para determinar o endereço de rede IPv4.

## 37.4.10 Verifique sua compreensão - Solução de problemas de conectividade de endpoint

### Pergunta 1

Quais são as duas informações que podem ser verificadas emitindo o **comando ipconfig/all** em uma máquina Windows? (Escolha duas.)

- [ ] todas as sessões TCP/IP estabelecidas com o host local
- [ ] todos os endereços IP associados a um nome de domínio de destino
- [ ] o número de dispositivos da Camada 3 ao longo do caminho entre o host local e um servidor de destino
- [x] o endereço IP do adaptador de rede
- [x] o gateway padrão

✅ RESPOSTA CORRETA: o endereço IP do adaptador de rede; o gateway padrão

> Está certo. O comando ipconfig/all, quando emitido em uma máquina Windows, exibirá muitas configurações de IP, como o endereço IP de todos os adaptadores de rede ativos, a máscara de sub-rede, o endereço do servidor DNS e o gateway padrão. Use o comando nslookup para determinar o endereço IP associado a um nome de domínio de destino. Use o comando netstat para visualizar todas as sessões TCP/IP estabelecidas para o host local. Use o comando tracert para visualizar os dispositivos da Camada 3 entre o host local e um servidor de destino.

### Pergunta 2

Qual comando um administrador pode usar para verificar a configuração de IP das interfaces em um host Linux?

- [ ] ipconfig/all
- [x] ifconfig
- [ ] arp -a
- [ ] networksetup -getinfo

✅ RESPOSTA CORRETA: ifconfig

> Está certo. Usando a linha de comando do Linux, o administrador de rede pode exibir o status e a configuração de IP das interfaces usando o comando ifconfig.


# 37.5 Solucionar Problemas de uma rede

### 37.5.1 Dispositivos de rede como fontes de informações de rede

Ao documentar ou diagnosticar um problema de rede, geralmente é necessário coletar informações diretamente de roteadores e switches. Comandos de rede úteis óbvios incluem ping, traceroute e telnet. Há também muitos comandos show disponíveis para ajudar a verificar a operação de um dispositivo.

A tabela lista alguns dos comandos show mais comuns do Cisco IOS usados para coleta de dados.

|Comando|Descrição|
|---|---|
|`show version`|Exibe tempo de atividade, informações de versão e informações de licenciamento para o software e hardware do dispositivo.|
|`show ip interface [brief]`<br>`show ipv6 interface [brief]`|Exibe todas as opções de configuração definidas em uma interface.<br>Use a palavra-chave **brief** para exibir apenas o status e o endereço IP das interfaces IP.|
|`show interfaces`|Exibe saída detalhada para cada interface.<br>Para exibir a saída detalhada para apenas uma única interface, inclua o tipo e o número da interface no comando (por exemplo, Gigabit Ethernet 0/0/0).|
|`show ip route`<br>`show ipv6 route`|Exibe o conteúdo da tabela de roteamento, listando redes diretamente conectadas e redes remotas aprendidas.|
|`show cdp neighbors detail`|Exibe informações detalhadas sobre dispositivos vizinhos Cisco conectados diretamente.<br>Útil para validar se as camadas 1 e 2 estão operacionais.|
|`show arp`<br>`show ipv6 neighbors`|Exibe o conteúdo da tabela ARP (IPv4) e da Tabela de vizinhos (IPv6).|
|`show running-config`|Exibe a configuração atual do dispositivo.|
|`show vlan`|Exibe o status das VLANs em um switch.|
|`show port`|Exibe o status das portas em um switch.|
|`show mac-address table`|Exibe o conteúdo da tabela de endereços MAC do switch.|
|`show interface status`|Exibe estatísticas e informações de status para interfaces de rede.|
|`show inventory`|Exibe informações de inventário sobre os componentes específicos em um dispositivo Cisco.|
|`show switch`|Exibe o status da pilha de switches quando os switches são agrupados usando o Cisco Stackwise.|
|`show tech-support`|Esse comando é útil para coletar grande quantidade de informações sobre o dispositivo em caso de identificação e solução de problemas.<br>Ele executa vários comandos show que podem ser fornecidos aos representantes de suporte técnico ao relatar um problema.|

Alguns desses comandos **show** podem exigir acesso ao modo EXEC privilegiado.

Como um recurso de segurança, o software Cisco IOS separa o acesso de gerenciamento em dois níveis de privilégio:

- **Modo EXEC do usuário** - Este é o nível de privilégio 1 e indicado por um prompt de dispositivo que termina com um símbolo maior que **(**>) (por exemplo, Router> ou Switch>). Ele fornece acesso limitado a comandos úteis para um técnico ao verificar a operação básica de um dispositivo.
- **Modo EXEC Privilegiado** – Este é o nível de privilégio 15 e indicado por um prompt que termina com um símbolo de jogo da velha (#) (por exemplo, Router# ou Switch#). É o nível mais alto disponível e só deve ser acessado por um administrador de rede. Nesse modo, todos os comandos do dispositivo estão disponíveis, incluindo a capacidade de configurar ou alterar as as configurações do dispositivo. Use o **comando enable** para entrar no modo EXEC privilegiado.

O Cisco IOS também fornece verificação de sintaxe de comando e ajuda contextual. Se você inserir um comando incorretamente, o IOS identificará onde você cometeu um erro de entrada.

A ajuda contextual permite que o usuário encontre rapidamente as respostas para estas perguntas:

- Quais comandos estão disponíveis em cada modo de comando?
- Quais comandos começam com caracteres específicos ou grupo de caracteres?
- Quais argumentos e palavras-chave estão disponíveis para comandos específicos?

Para acessar a ajuda sensível ao contexto, basta inserir um ponto de interrogação (**?**) ao digitar um comando.

O Cisco IOS também não exige que todo o comando, argumento ou palavra-chave seja digitado. A entrada de comando parcial deve ser longa o suficiente para identificar exclusivamente o comando completo. Por exemplo, você pode usar **en** em vez de inserir o comando completo enable.

Para ter certeza de que o comando correto está sendo digitado, a tecla tab também pode ser usada para completar a entrada parcial de um comando, argumento ou palavra-chave.

## 37.5.2 Captura de Pacotes e Análise de Protocolo

Os analisadores de protocolo podem investigar o conteúdo dos pacotes enquanto fluem pela rede. Um analisador de protocolo decodifica as várias camadas de protocolo em um quadro registrado e apresenta essas informações em um formato relativamente fácil de usar.

Como técnico, você pode receber a tarefa de capturar o tráfego de um host específico. Portanto, é importante que você se familiarize com o software para concluir a tarefa atribuída.

A figura mostra uma captura de tela do analisador de protocolo Wireshark.

![[Pasted image 20260702214603.png]]

As informações exibidas por um analisador de protocolo incluem dados de bits da camada física, informações da camada de enlace, protocolos e descrições para cada quadro. A maioria dos analisadores de protocolo pode filtrar o tráfego que atenda a certos critérios, para que todo o tráfego de e para um dispositivo possa ser capturado. Os analisadores de protocolo, como o Wireshark, podem ajudar a identificar e solucionar problemas de desempenho de rede. É importante ter um bom entendimento de TCP/IP e saber como usar um analisador de protocolo para inspecionar informações em cada camada de TCP/IP.

## 37.5.3 Laboratório - Instalar o Wireshark

O Wireshark é um software analisador de protocolo, ou uma aplicação "packet sniffer", usado para solução de problemas de rede, análise, desenvolvimento de software e protocolo, e educação. O Wireshark é usado neste curso para demonstrar conceitos de rede. Neste laboratório, você vai baixar e instalar o Wireshark.

## 37.5.4 Laboratório - Use ferramentas de rede para aprender sobre uma rede

O Wireshark é um software analisador de protocolo, ou "packet sniffer", usado em solução de problemas de rede, análise, desenvolvimento de software e protocolo, e educação. O Wireshark é usado neste curso para demonstrar conceitos de rede. O Nmap é uma ferramenta popular de varredura e mapeamento de rede. Neste laboratório, você usará o Nmap para descobrir hosts em sua rede e, em seguida, usará o Wireshark para capturar o tráfego entre seu computador e outros hosts.

## 37.5.5 Medindo a Taxa de Transferência (Throughput) da rede

Largura de banda e Taxa de Transferência são dois termos comumente usados para descrever a quantidade de tráfego que flui entre dois dispositivos.

Largura de banda é a quantidade teórica de dados que podem ser transmitidos de um dispositivo para outro em um período de tempo. A largura de banda é normalmente medida em número de **bits por segundo**.

Taxa de transferência é a medida do número real de bits por segundo que estão sendo transmitidos pela mídia. A taxa de transferência é sempre menor do que a largura de banda especificada porque o tráfego pode encontrar latência ou atraso durante a transmissão.

A latência pode ser causada por vários problemas, especificamente a distância física entre a origem e o destino. Existem outros fatores também, incluindo o número de dispositivos de rede encontrados entre a origem e o destino. Como os dados atravessam várias redes, eles devem ser processados e encaminhados por switches e roteadores.

Um técnico pode precisar verificar a taxa de transferência de um link para verificar sua operação. Existem muitos sites na internet que podemos usar para fazer isso. Uma pesquisa usando **internet speed test** como palavras chave fornecerá vários sites que medirão a "velocidade" da conexão e o desempenho do seu dispositivo conectado à Internet. Esses sites geralmente usam servidores pré-selecionados e relatam suas "velocidades" de download e upload.

**O iPerf** é uma ferramenta do Windows que pode ser baixada para medir a taxa de transferência entre um cliente e um servidor. O iPerf deve estar em execução em ambos os dispositivos finais. O exemplo a seguir mostra a taxa de transferência entre um cliente e um servidor iPerf público, speedtest.masnet.ec.

```
37.5.5 Medindo a Taxa de Transferência (Throughput) da rede
Largura de banda e Taxa de Transferência são dois termos comumente usados para descrever a quantidade de tráfego que flui entre dois dispositivos.

Largura de banda é a quantidade teórica de dados que podem ser transmitidos de um dispositivo para outro em um período de tempo. A largura de banda é normalmente medida em número de bits por segundo.

Taxa de transferência é a medida do número real de bits por segundo que estão sendo transmitidos pela mídia. A taxa de transferência é sempre menor do que a largura de banda especificada porque o tráfego pode encontrar latência ou atraso durante a transmissão.

A latência pode ser causada por vários problemas, especificamente a distância física entre a origem e o destino. Existem outros fatores também, incluindo o número de dispositivos de rede encontrados entre a origem e o destino. Como os dados atravessam várias redes, eles devem ser processados e encaminhados por switches e roteadores.

Um técnico pode precisar verificar a taxa de transferência de um link para verificar sua operação. Existem muitos sites na internet que podemos usar para fazer isso. Uma pesquisa usando internet speed test como palavras chave fornecerá vários sites que medirão a "velocidade" da conexão e o desempenho do seu dispositivo conectado à Internet. Esses sites geralmente usam servidores pré-selecionados e relatam suas "velocidades" de download e upload.

O iPerf é uma ferramenta do Windows que pode ser baixada para medir a taxa de transferência entre um cliente e um servidor. O iPerf deve estar em execução em ambos os dispositivos finais. O exemplo a seguir mostra a taxa de transferência entre um cliente e um servidor iPerf público, speedtest.masnet.ec.
```

A saída relevante é:

- **Interval**: O intervalo de tempo que o iPerf relata periodicamente a taxa de transferência. Por padrão, o intervalo de tempo é de 1 segundo.
- **Transfer**: A quantidade de dados transferidos durante cada intervalo de tempo.
- **Bitrate**: a taxa de transferência medida em cada intervalo de tempo.


## 37.5.6 Packet Tracer - Desafio de solução de problemas - Use a documentação para resolver problemas

Nesta atividade do Packet Tracer, você usa a documentação de rede para identificar e corrigir problemas de comunicação de rede.

- Usar várias técnicas e ferramentas para identificar problemas de conectividade.
- Usar a documentação para orientar os esforços para solução de problemas.
- Identificar problemas específicos de rede.
- Implementar soluções para problemas de comunicação em rede.
- Verificar a operação da rede.


# 37.6 Solucionar problemas de Conectividade Remotamente

## 37.6.1 Suporte a usuários remotos

Ao auxiliar usuários remotos, muitas vezes não é eficiente conduzir verbalmente um usuário através de procedimentos complicados. As tecnologias de acesso remoto permitem que os técnicos de suporte assumam o controle da área de trabalho de um usuário para visualizar e definir configurações no computador do usuário. Durante uma sessão de área de trabalho remota, o usuário geralmente não consegue controlar seu PC. No entanto, eles podem assistir tudo o que o técnico faz.

Por exemplo, um usuário pode estar tendo problemas para acessar o site corporativo. Como esse acesso pode depender de várias condições de configuração do computador, um técnico de suporte solicita acesso remoto ao sistema. Depois que o usuário autoriza o acesso, o técnico pode verificar várias configurações de segurança e acesso no sistema para identificar e corrigir o problema.

Os aplicativos de área de trabalho remota apresentam possíveis vulnerabilidades de segurança porque oferecem controle total dos computadores por alguém que não seja o usuário autorizado. Por exemplo, os agentes de ameaças podem explorar portas abertas de aplicativos de área de trabalho remota ou usar técnicas de engenharia social para induzir um usuário a fornecer acesso à área de trabalho remota. É importante que os usuários entendam que apenas técnicos de suporte autorizados devem ter acesso remoto aos sistemas.

**Observação**: muitas organizações desativam o acesso remoto a computadores que possuem ou administram. Por esse motivo, pode ser necessário solicitar que o usuário o ative. Outras organizações usam aplicativos de desktop remoto proprietários ou alternativos para atenuar as vulnerabilidades de segurança associadas ao acesso remoto ao sistema.

Os aplicativos de área de trabalho remota usam um modelo cliente-servidor. O cliente de área de trabalho remota é usado para conectar-se ao sistema remoto, que atua como um servidor. Os aplicativos de acesso remoto podem recuperar dados do sistema, transferir arquivos para sistemas e iniciar sessões de bate-papo seguras com os usuários. Alguns aplicativos de acesso remoto exigem que o usuário esteja presente para autorizar o acesso ou podem acessar sistemas sem a participação do usuário. Outros sistemas de acesso remoto podem acessar o sistema se ele estiver desacompanhado.

**Selecione as setas para a direita e para a esquerda para obter exemplos de aplicativos comuns de área de trabalho remota.**

**Área de Trabalho Remota da Microsoft**

- Instalado em todos os computadores Windows.
- Permite o acesso a partir de PCs, dispositivos Android ou iOS.
- Requer uma edição Pro do Windows.


## 37.6.2 Acesso remoto com Telnet, SSH e RDP

Muito antes dos computadores desktop com interfaces gráficas sofisticadas, as pessoas utilizavam sistemas com base em texto que frequentemente eram apenas terminais de exibição fisicamente acoplados a um computador central. Quando as redes foram disponibilizadas, as pessoas precisaram de uma maneira de acessar remotamente os sistemas de computador da mesma forma que faziam com os terminais diretamente conectados.

O protocolo Telnet foi desenvolvido para atender a essa necessidade. O Telnet data do início da década de 70 e está entre um dos protocolos e serviços da camada de Aplicação mais antigos da suite TCP/IP. O Telnet fornece um método padrão de emulação de dispositivos terminais baseados em texto na rede de dados. O protocolo e o software cliente que implementa o protocolo são comumente chamados de Telnet. Os servidores Telnet escutam solicitações de clientes na porta TCP 23.

Uma conexão Telnet é chamada de sessão de terminal virtual (virtual terminal - vty). Em vez de usar um dispositivo físico para se conectar ao servidor, o Telnet usa software para criar um dispositivo virtual que fornece recursos de uma sessão de terminal com acesso à interface de linha de comando (CLI) do servidor.  
Na figura, o cliente se conectou remotamente ao servidor via Telnet. O cliente agora pode executar comandos como se estivesse conectado localmente à linha de comando do servidor. Da mesma forma, o Telnet pode fornecer acesso à interface de linha de comando (CLI), ou console, de um dispositivo de rede para que o dispositivo possa ser configurado e monitorado.

![[Pasted image 20260702215001.png]]

Quando uma conexão Telnet é estabelecida, os usuários podem executar qualquer função autorizada no servidor, como se estivessem usando uma sessão de linha de comando no próprio servidor. Se autorizados, podem iniciar e parar processos, configurar o dispositivo e até mesmo desligar o sistema.

Embora o protocolo Telnet possa exigir o login de um usuário, ele não suporta o transporte de dados criptografados. Todos os dados trocados durante as sessões Telnet são transportados como texto simples pela rede. Isso significa que os dados podem ser facilmente interceptados e compreendidos. Isso inclui nomes de usuário e senhas.

O protocolo Secure Shell (SSH) oferece um método alternativo e seguro para acesso ao servidor. O SSH fornece a estrutura para proteger login remoto e outros serviços de rede segura. Ele também fornece autenticação mais forte do que o Telnet e suporta o transporte de dados de sessão usando criptografia. Os servidores SSH atendem às solicitações do cliente na porta TCP 22.

Como prática recomendada, os profissionais de rede devem sempre usar SSH no lugar de Telnet, se possível.

A figura ilustra como o SSH é mais seguro que o Telnet. No lado esquerdo da figura, o técnico de rede está usando Telnet e faz login no servidor usando as credenciais indicadas. O agente da ameaça capturou o tráfego Telnet e pode ver facilmente as credenciais usadas. No lado direito da figura, o técnico está usando SSH para se conectar a um servidor diferente. O agente da ameaça ainda pode capturar o tráfego. No entanto, eles não seriam capazes de decifrá-lo porque o SSH criptografa o tráfego do usuário.

![[Pasted image 20260702215204.png]]

Conectar-se a outros dispositivos usando Telnet ou SSH usando uma janela de terminal é comum em alguns sistemas operacionais. Existem também pacotes de emulador de terminal de software comercial disponíveis. PuTTY é um popular programa emulador de terminal gratuito e de código aberto. Este aplicativo cliente suporta SSH, Telnet e rlogin. O Terra Term é outro emulador de terminal gratuito e de código aberto que inclui uma linguagem de script de macro e plug-ins. PuTTY e Tera Term podem usar o protocolo SSH para conexões. Ambos assumem que um servidor SSH, como o disponível com OpenSSH, está sendo executado no dispositivo de destino. O OpenSSH é distribuído com uma ampla gama de sistemas operacionais, incluindo várias distribuições Linux, Windows e MacOS.

O Remote Desktop Protocol (RDP) foi criado pela Microsoft. Ele usa um modelo cliente-servidor no qual o cliente pode se conectar a um servidor RDP executado em um sistema remoto para exibir a interface gráfica do usuário do dispositivo remoto. Os servidores e clientes RDP estão incluídos no Windows e estão disponíveis para OS X, Linux e Unix via xrdp, que é uma implementação gratuita e de código aberto do servidor Microsoft RDP. Outros sistemas operacionais também podem executar essas funções. Por exemplo, no macOS, a funcionalidade de acesso remoto é fornecida pelo recurso de compartilhamento de tela, que é baseado no Virtual Network Computing (VNC). Qualquer cliente VNC pode se conectar a um servidor de compartilhamento de tela. O VNC é um produto freeware que é semelhante em funcionalidade ao RDP e funciona na porta 5900.


## 37.6.3 Demonstração em Vídeo - Área de Trabalho Remota e Assistência Remota

Outros sistemas operacionais também podem executar essas funções. Por exemplo, no macOS, a funcionalidade de acesso remoto é fornecida pelo recurso de compartilhamento de tela, que é baseado no Virtual Network Computing (VNC). Qualquer cliente VNC pode se conectar a um servidor de compartilhamento de tela. O VNC é um produto freeware que é semelhante em funcionalidade ao RDP e funciona na porta 5900.

Selecione **Play** para ver o vídeo.

Você já desejou você poderia ter um segundo par de olhos dê uma olhada em algo que você vê na tela? Bem, é esse vídeo, estamos aqui para conversar sobre desktop remoto e assistência remota aqui no Windows 10, então isso vai ser divertido, porque vamos realmente fazer isso e não apenas falar sobre isso, então para começar, uma das primeiras coisas que queremos fazer é ir para a área de trabalho remota.

E isso vai estar dentro do nosso, clique com o botão direito em nosso botão iniciar, e vamos direto para as configurações. Nós vamos expandir, bem aí. Poderíamos ter clicado em iniciar e digitado as configurações e descobri dessa forma, mas estamos fazendo clique com o botão direito em iniciar e o botão esquerdo em configurações. Agora, dentro das configurações, o que vamos abordar é o sistema, e dentro do sistema, é aqui que vamos rolar até o final no lado esquerdo, e aqui encontramos a área de trabalho remota.

Vou prosseguir e clicar em área de trabalho remota, e o que vemos aqui é que, por padrão, a área de trabalho remota está desativada no Windows 10. Agora, com a área de trabalho remota desligada, isso significa que usuários remotos não podem acessar nosso sistema. Agora, se quisermos permitir que um usuário remoto se conecte ao nosso computador através da rede, e obter acesso ao nosso sistema e ser literalmente nós no sistema, podemos utilizar este controle deslizante à direita e diz tem certeza? Você e os usuários selecionados nas contas de usuário será capaz de se conectar a esta máquina remotamente. E vou clicar em confirmar.

Agora deixe-me conversar um pouco mais sobre isso. Quando você liga a área de trabalho remota, alguém agora pode se conectar remotamente à sua máquina, e quando eles se conectarem a ele, eles vão autenticar utilizando sua combinação de nome de usuário e senha. Bem, e se eu não quiser divulgar meu nome de usuário e senha? Então um usuário remoto teria que ter seu próprio nome de usuário e senha em sua máquina. O que significa que você teria que criar uma conta de usuário para eles em sua máquina. Então, se você quiser cinco usuários diferentes ser capaz de acessar remotamente sua caixa usando seu próprio nome de usuário e senha, eles precisariam de cinco contas, é o que isso significa. Caso contrário, você está compartilhando seu nome de usuário e senha para que eles tenham acesso.

Portanto, esta é uma área de trabalho remota, e há algumas configurações que podemos modificar aqui, por exemplo, há configurações de energia que podemos ver, que é apenas mostrar as configurações, fala sobre energia e modo suspenso, não queremos que nosso PC durma e não poder acessá-lo remotamente. Além disso, tornar nossa máquina detectável em nossa rede para que as pessoas possam ver, temos configurações aqui que vimos anteriormente em nossas configurações de rede, e é aqui que encontramos coisas para compartilhamento de arquivos de rede, bem como a ideia de compartilhamento protegido por senha. Portanto, esses são atendidos por padrão.

Agora vamos rolar para baixo aqui para configurações de área de trabalho remota, e o que podemos ver aqui é o nome que as pessoas vão almejar quando eles usam a área de trabalho remota como uma ferramenta no computador deles, será o nome do PC de StudentPC_1, esse é o nome do meu computador que estamos no momento, que nós apenas permitiu que as pessoas se conectassem.

Lá embaixo, contas de usuários, eu estava falando sobre isso, por padrão, o usuário que pode acessá-lo é o nome de usuário do aluno, com o senha para a conta do aluno. Agora, se você quiser adicionar outras pessoas para poder acessá-lo, clicaríamos em adicionar, e agora aqui dentro, poderíamos digitar os diferentes nomes de usuário ou grupo de usuários que seriam capazes de acessar remotamente nossa máquina. Você os coloca aqui, e então selecionaremos OK.

Agora, continuando em frente, na parte inferior, além de contas de usuário que podem ter acesso remoto, se você não sabe nem como usar a área de trabalho remota de uma máquina remota e usá-la como uma ferramenta, há muitos links aqui para obter ajuda. E o Windows faz um ótimo trabalho para isso.

Então, o que queremos tentar agora, é que queremos tentar acessar remotamente este computador. Mas tenho que fazer algo primeiro. Para acessar remotamente, as pessoas vão precisar de um nome de usuário e senha, e se eu verificar minha conta de estudante aqui, alterar as configurações da conta na minha máquina, o que poderemos ver é que não tenho uma senha. Portanto, as opções de login da conta de estudante, minha conta não tem uma senha, vou adicionar uma senha para que possamos realmente acessar remotamente esta máquina usando uma área de trabalho remota. 123, porque isso é incrível, e a dica vai ser você sabe disso. 123, vamos utilizar isso com a conta de usuário do aluno, para acessar remotamente esta máquina.

Então, vamos tentar, vou carregar um sistema operacional diferente. Então, aqui estamos no Windows 7, vou seguir em frente e clicar em iniciar, e vamos usar a área de trabalho remota, e aqui está a conexão de área de trabalho remota, e então o que farei é digitar o nome do computador que desejo acessar, StudentPC_1 e clicarei em conectar. Agora, quando clico em conectar, diz ooh, você quer se conectar, tudo bem, você vai usar a conta do usuário de aluno, mas qual é a senha para essa conta na outra máquina? E isso é Cisco123, e eu irei em frente e clicarei em OK.

E o que vai acontecer aqui é que minha máquina Windows 7 vai se conectar remotamente à outra máquina de StudentPC_1, e terei controle total e absoluto dessa máquina usando essa conta de usuário. Diz que você deseja verificar, sim, vamos verificar com um certificado, está apenas falando sobre autenticação de certificado e autoridade, e agora a conexão será realizada.

Então, aqui estamos nós com acesso remoto na outra máquina neste momento. Estamos remotos e deixe-me mudar de vista para que você possa ver o topo da minha janela. E no topo da minha janela, você pode ver aqui que na minha máquina Windows 7, estamos conectados à StudentPC_1, e com o que foi dito Eu posso apenas minimizar, e estou de volta minha máquina cliente Windows, ou Windows 7, e eu poderia trazê-lo de volta, e estou de volta na conexão de área de trabalho remota para o StudentPC_1.

Vou mudar minha janela novamente e continuar. Então, na máquina Windows 7, Eu literalmente assumi a caixa do Windows 10, e o que é realmente importante observar sobre isso, se eu for dar uma olhada no Windows 10 sistema novamente, como é? Na máquina Windows 10, ele está desconectado. Quando o usuário remoto conectado à nossa máquina com a conta de estudante, nossa conta corrente que estávamos usando, que era a conta do aluno foi desconectada, e se eu entrar do meu lado na minha conta aqui na caixa do Windows 10, vamos dar uma olhada no que aconteceu a sessão remota na caixa do Windows 7.

Dê uma olhada, uma vez que o usuário no computador Windows 10 se logou novamente no lado deles, fomos desconectados de nossa sessão remota. Vá em frente e clique em OK, e estamos de volta aqui no Windows 7.

Então essa é a área de trabalho remota, e agora temos mais um item para discutir, e isso vai ser assistência remota. Então, estamos de volta ao nosso cliente Windows 10, e agora vamos falar de assistência remota. Agora primeiro, para entrar nas configurações de assistência remota o que vamos fazer é ir em frente e clicar em iniciar, e vamos para o PC. E com o PC, vamos passar para nossas propriedades. Agora, quando clicamos nas propriedades deste PC, isso vai abrir uma nova janela para nós. Queremos ir, fica do lado esquerdo aqui, e é chamado de configurações remotas.

Entramos no nosso link de configurações remotas, o que veremos quando eu redimensionar minha janela, é que temos a assistência remota aqui, que está definido para permitir assistência remota conexões a este computador, isso é ótimo. Incrível, então isso significa que as pessoas que oferecemos um arquivo especial conhecido como convite, pode usar esse arquivo e uma senha para se conectar a nós.

Isso é diferente da área de trabalho remota, porque desktop remoto, estamos literalmente ativando um serviço que qualquer pessoa a qualquer momento podem por conta própria iniciar uma conexão e assumir nosso computador e usá-lo. Apenas remotamente, o que é ótimo. Com a área de trabalho remota, as pessoas podem iniciar por conta própria. Com assistência remota, temos que fornecê-los um arquivo e uma senha para acessar nossa máquina.

Então, como vamos fazer isso? Bem, não é nem um pouco difícil. Agora que temos conexões de assistência remota sendo selecionado, posso ir em frente e clicar em avançar aqui, e o que podemos dar uma olhada é uma de nossas configurações reais para isso. Sim, nosso computador pode ser controlado remotamente. Além disso, por quanto tempo podemos criar um convite e fornecer alguém para ficar aberto? Bem, o padrão aqui é de seis horas, então vamos deixá-lo no padrão de seis horas, e o que queremos fazer agora é criar um convite de assistência remota.

Para fazer isso, clico no meu botão iniciar, e vamos digitar assistência remota aqui. E quando digitamos assistência remota, o que teremos é permitir convites de assistência remota a ser enviado deste computador. Ok, e nas configurações, convide alguém para se conectar ao seu PC e te ajudar, vou clicar nisso.

Quando clico nele, obtemos esta janela de assistência remota. E aqui podemos ir em frente e ajudar outra pessoa quem nos convidou com um arquivo, ou podemos usar convidar alguém, então clicarei no primeiro, Quero convidar outra pessoa para me ajudar remotamente. Quando eu clico nisso, há três opções aqui. Dois deles estão esmaecidos, a primeira opção é que posso salvar o convite como um arquivo na minha máquina. Então terei que enviar esse arquivo para outra pessoa. Por meio de um anexo de e-mail, unidade flash, compartilhamento de arquivos, o que quiser. As outras opções estão esmaecidas, porque não posso selecioná-los neste momento, mas se eu tivesse um programa de e-mail instalado na minha máquina, poderia enviá-lo automaticamente para um alvo remoto ou com um aplicativo Easy Connect da loja do Windows, eu poderia usar isso também.

Vou fazer a opção padrão de salvar o convite como um arquivo. Quando eu clicar nele, ele me perguntará onde colocá-lo, Vou apenas jogá-lo no meu desktop, e agora meu arquivo de convite será salvo para a minha área de trabalho da minha máquina Windows 10. O arquivo salvo na minha máquina, também tenho uma nova janela que aparece, diz por favor certifique-se você dá esta senha para o outro usuário para acessar sua máquina junto com esse arquivo de convite.

Então, vamos para a máquina Windows 7, e vamos usar este arquivo e esta senha para assistir remotamente a caixa do Windows 10. Então estamos na caixa do Windows 7, Eu mudei aquele arquivo de convite para a área de trabalho, e o que posso fazer posso clicar duas vezes no arquivo de convite, diz, ah, qual é a senha para conectar? Bem, essa senha vai ser aquela grande e musculosa que vimos originalmente, que é 92252M92W2MXD5M2X, que é uma loucura, mas é bom, é uma boa segurança. Vá em frente e clique em OK.

A partir daí, o que veremos está de volta no Windows 10, deixe-me voltar novamente. Aqui estamos nós, minha caixa do Windows 10, diz, você permitiria que o aluno se conectasse à sua máquina? Eu vou dizer sim, vá em frente, e você tipo, ei eu não fui desconectado desta vez como a área de trabalho remota, nós desconectamos, mas agora diz que a pessoa a lhe ajudar agora pode ver sua área de trabalho.

Bem, isso é legal, posso pausar a habilidade para o meu ajudante ver, ha, eles não podem ver mais, ou continue, agora meu ajudante pode ver a área de trabalho novamente, Eu posso abrir uma janela de bate-papo onde podemos bater um papo para a frente e para trás, eu e meu ajudante, então, mesmo na área de configurações aqui, temos algumas opções que podemos dar uma olhada, como uso de largura de banda, salvando um registro, você tem informações aqui que você pode personalizar, o que é ótimo.

Nós vamos voltar na máquina Windows 7 para ver o que estão vendo e continuaremos. Ok, isso é legal, então na máquina Windows 7, temos esta janela de assistência remota que está aberta, e diz que estamos ajudando a conta do aluno na outra máquina, e o que podemos fazer é personalizar nosso tamanho aqui, e como vimos na outra máquina, o Windows 10, temos coisas como chat e também configurações.

Não consigo clicar em nada, esta não é uma área de trabalho remota. Eu não tenho acesso ao controle. Se eu quiser solicitar o controle, posso ir em frente e clique em solicitar controle, e ele aparecerá na máquina Windows 10, ainda não consigo clicar, e na máquina Windows 10 diz você quer dar a essa pessoa o controle de sua máquina? porque agora eles podem apenas visualizar, e se eu fosse para o cliente Windows 10, Eu seria capaz de permitir que este usuário do Windows 7 controlasse remotamente minha máquina.

Então essa é a diferença entre assistência remota e desktop remoto, ambos usam um protocolo criptografado em toda a rede para permitir esse tipo de acesso e controle. Obrigado por ver, personalizar, praticar e brincar com seus próprios desktops remotos e remotos Configurações de assistência do Windows e divirta-se e se tornar esse profissional de TI.

## 37.6.4 Entendendo as VPNs

Para se comunicar e compartilhar recursos com segurança em uma rede não segura, como a Internet, é usada uma rede privada virtual (VPN). Os tipos mais comuns de VPN são usados para acessar uma rede privada corporativa por usuários remotos ou sites corporativos remotos.

Uma VPN usa conexões seguras dedicadas, roteadas pela Internet, da rede privada corporativa para o usuário remoto. Quando conectados à rede privada corporativa, os usuários de VPN de acesso remoto passam a fazer parte dessa rede e têm acesso a todos os serviços e recursos como se estivessem fisicamente conectados a ela. As VPNs também são usadas para conectar filiais e outras instalações à rede corporativa.

As VPNs geralmente são implantadas em uma das seguintes configurações: acesso site a site ou acesso remoto.

**Clique nas setas à direita e à esquerda para visualizar informações sobre cada tipo de VLAN.**

### **VPN de site para site**

Uma VPN site a site é criada quando os dispositivos de terminação da VPN, também chamados de gateways VPN, são pré-configurados com informações para estabelecer um túnel seguro. O tráfego da VPN é criptografado apenas entre esses dispositivos. Os hosts internos não sabem que uma VPN está sendo usada.
![[Pasted image 20260702215837.png]]

### **VPNs de acesso remoto**

Uma VPN de acesso remoto é criada dinamicamente para estabelecer uma conexão segura entre um cliente e um dispositivo de terminação da VPN. Por exemplo, uma VPN SSL de acesso remoto é usada quando você verifica suas informações bancárias online.
![[Pasted image 20260702215847.png]]


Os usuários de acesso remoto devem instalar um cliente VPN em seus computadores para formar uma conexão segura com a rede privada corporativa. Roteadores especiais também podem ser usados ​​para conectar computadores à rede privada corporativa. O software VPN criptografa os dados antes de enviá-los pela Internet para o gateway VPN na rede privada corporativa. Os gateways VPN estabelecem, gerenciam e controlam conexões VPN, também conhecidas como túneis VPN. O Windows suporta vários tipos de VPN, no entanto, para algumas VPNs, pode ser necessário um software de terceiros. O cliente Cisco AnyConnect VPN é mostrado na figura.

![[Pasted image 20260702215757.png]]

Uma VPN no Windows 10 pode ser configurada nas configurações de Rede e Internet, conforme mostrado na figura.
![[Pasted image 20260702215806.png]]

Além de proteger o compartilhamento de área de trabalho remota para fins de suporte técnico, os usuários podem usar a área de trabalho remota para acessar remotamente computadores dentro da rede corporativa para realizar suas tarefas normais de trabalho. Isso significa que um usuário pode acessar a área de trabalho de seu computador de trabalho a partir de seu computador doméstico. Isso permite que os funcionários acessem os recursos de trabalho de seus próprios dispositivos e acessem remotamente arquivos e programas hospedados em seu PC de trabalho. Além disso, a computação com desktops virtuais baseados em nuvem está se tornando popular. As organizações podem economizar dinheiro e aumentar a eficiência terceirizando o gerenciamento de estações de trabalho para a nuvem. Nesse caso, as estações de trabalho do usuário são máquinas virtuais hospedadas na nuvem. Isso permite que os usuários acessem seus recursos de computador de praticamente qualquer dispositivo que suporte um cliente de desktop remoto compatível.

No entanto, isso pode criar desafios de segurança. Muitos clientes de área de trabalho remota não são seguros. O uso de VPNs para acessar estações de trabalho de computadores virtuais remotos e baseados em nuvem garante maior segurança quando esta solução está em uso. Microsoft Azure e Amazon Web Services fornecem soluções de espaço de trabalho remoto. A equipe de suporte de TI será necessária para ajudar os funcionários a acessar e operar esses recursos virtuais.

## 37.6.5 Sistemas de gerenciamento de rede

O gerenciamento de rede refere-se a dois conceitos relacionados. O primeiro é o processo de configuração, monitoramento e gerenciamento do desempenho de uma rede. O segundo é a plataforma que as equipes de TI e operações de rede usam para concluir essas tarefas. As plataformas modernas de gerenciamento de rede fornecem análises avançadas, aprendizado de máquina e automação inteligente para otimizar continuamente o desempenho da rede. À medida que as organizações se adaptam a uma força de trabalho mais distribuída, esses sistemas de gerenciamento de rede são cada vez mais implantados em ambientes de nuvem e hospedados.

Os sistemas de gerenciamento de rede coletam dados de dispositivos de rede conectados, como switches, roteadores, pontos de acesso e dispositivos clientes. Eles também fornecem aos administradores de rede controle sobre como esses dispositivos operam e interagem uns com os outros. Os dados capturados desses dispositivos são usados para identificar proativamente problemas de desempenho, monitorar segurança e segmentação e acelerar a solução de problemas.

Os sistemas de gerenciamento de rede geralmente usam o Simple Network Management Protocol (SNMP) e o Remote Network Monitoring (RMON) para coletar informações de dispositivos de rede. Os sistemas operacionais host possuem plataformas de gerenciamento que permitem o monitoramento e a configuração de muitos computadores host.

Os sistemas de gerenciamento de rede são implantados usando dois modelos operacionais, conforme mostrado na tabela.

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed; word-wrap:break-word;"> <tr style="background:#6b7280; color:white;"> <th>Baseado em Nuvem</th><th>No local (on-premises)</th> </tr> <tr> <td> <ul> <li>Os sistemas baseados em nuvem são projetados para fornecer flexibilidade e acesso amplo a redes geograficamente dispersas.</li> <li>Essas plataformas oferecem fácil acesso e monitoramento em redes altamente distribuídas e simplificam o provisionamento de sites remotos.</li> <li>Eles também fornecem um alto nível de configuração e personalização por meio de APIs abertas e ecossistemas de aplicativos robustos.</li> <li>Essas plataformas também oferecem suporte a análises avançadas, automação e casos de uso de otimização, por meio de grandes data lakes e o poder da computação em nuvem para oferecer suporte a aplicativos sofisticados de aprendizado de máquina.</li> </ul> </td> <td> <ul> <li>Os sistemas de gerenciamento de rede no local podem ser usados para grandes redes de campus que exigem maior desempenho e escalabilidade.</li> <li>Eles também fornecem recursos avançados, como análise, garantia e inteligência artificial (IA) e aprendizado de máquina (ML).</li> <li>Algumas organizações devem manter um controle rígido sobre seus ativos de dados e são proibidas de armazenar dados em locais dispersos.</li> <li>Os servidores de gerenciamento de rede on-premises (no local) evitam tais problemas de conformidade porque todos os dados podem ser armazenados no local.</li> <li>Como grandes redes podem gerar muitos dados de gerenciamento, os sistemas locais geralmente são servidores maiores que têm poder suficiente para processar os dados para que possam ser usados para fornecer os insights de que a TI precisa para gerenciar a rede.</li> <li>Esse é um dos motivos pelos quais um servidor local geralmente está localizado no núcleo da rede.</li> <li>Embora possa ser acessado pela internet, o acesso remoto requer uma conexão VPN.</li> </ul> </td> </tr> </table>

Cisco Meraki é uma plataforma líder de gerenciamento de rede baseada em nuvem que fornece recursos de gerenciamento de rede poderosos sem consumir largura de banda do usuário. É seguro, flexível e fácil de implantar. Com ele, as redes podem ser gerenciadas de qualquer lugar. Ele pode gerenciar uma ampla variedade de dispositivos de rede Meraki e não Meraki com segurança. Ele fornece visualizações detalhadas de redes grandes, dispersas e complexas até o computador desktop ou telefone individuais. A figura fornece uma visão de um aspecto de um painel Meraki.

![[Pasted image 20260702220729.png]]

## 37.6.6 Vídeo - O que é gerenciamento de rede?

Este vídeo explora brevemente o gerenciamento de rede, incluindo o gerenciamento de rede em nuvem e o Cisco Nexus Dashboard.

Selecione **Play** para ver o vídeo.

O que é gerenciamento de rede e como ele pode ajudá-lo a alcançar seus objetivos de negócios corporativos?

O gerenciamento de rede é um conjunto de ferramentas projetado para ajudar os gerentes de TI do sistema de rede a implantar, manter, otimizar, e atualizar uma rede de qualquer tamanho. Essas ferramentas ajudam as organizações a avaliar dados rapidamente e fazer mudanças rápidas para dar suporte a novas metas de negócios como trabalhar em casa ou fazer compras online.

Quer sejam no local ou baseados na nuvem e acessado por meio de um navegador, sistemas de gerenciamento de rede gerencia elementos de rede, como switches, roteadores, access points e controladores sem fio. E com a crescente complexidade atual, eles também gerenciam sensores, câmeras e dispositivos industriais.

Eles fazem isso coletando dados como dados de telemetria em tempo real de elementos de rede para fornecer informações sobre a integridade de uma rede em uma GUI fácil de ler. Com estatísticas sobre dispositivos endpoint como telefones celulares, laptops e desktops, os operadores podem solucionar e resolver problemas muito mais facilmente. Além disso, os sistemas de gerenciamento de rede também impulsionam novas atualizações de software e arquivos de configuração atualizados que ajudam a melhorar o desempenho, a confiabilidade e a segurança.

Aqui estão mais duas ferramentas que a TI pode usar para obter melhores insights ao monitorar a integridade da rede. Automação de Rede, onde tarefas repetitivas, como configuração e as atualizações de software são feitas automaticamente. E garantia de rede, que aproveita a inteligência artificial e aprendizado de máquina para melhorar o desempenho, escalabilidade, experiência do usuário e segurança da rede.

Agora que você sabe o que são sistemas de gerenciamento de rede e como eles funcionam, você pode estar se perguntando se deve optar por um sistema local ou baseado em nuvem. Ambos têm suas vantagens.

Sistemas locais, como o Cisco DNA Center são projetados para grandes implementações de rede onde recursos avançados que usam automação, inteligência artificial e aprendizado de máquina são necessários. Com grandes quantidades de dados para processar e armazenar, o servidor de gerenciamento de rede geralmente precisa estar no local, mas ainda terá acesso à toda a rede. E a TI também pode acessar o sistema de gerenciamento de rede via VPN remota. On-premises oferece maior segurança e governança de dados, já que todos os dados da rede são armazenados no local.

No entanto, o gerenciamento de nuvem ajuda a TI a acessar a rede de qualquer lugar a qualquer hora. Sistemas de gerenciamento de rede baseados em nuvem, como Cisco Meraki, fornece tempo quase imediato para o mercado com provisionamento zero touch. Você também pode gerenciar SD-WAN e redes de data center da nuvem. Cisco vManage para SD-WAN permite que operadoras de rede implantem, gerenciem e monitorem dispositivos de rede rapidamente em toda a malha SD-WAN de forma altamente visualizada. O painel do Cisco Nexus é um híbrido, baseado em nuvem, plataforma de rede altamente ágil, e pode configurar a escala, monitorar e simplificar as operações e automação em sites locais e na nuvem pública.

No panorama geral, as redes modernas estão crescendo exponencialmente e tornando-se mais complexo. Os sistemas de gerenciamento de rede ajudarão sua escala de rede tão rápido como você.

Veja o que o Cisco Network Management pode fazer por você. Visite cisco.com/go/networking e saiba mais sobre as plataformas para controlar sua rede.

## 37.6.7 Scripts, Automação e Programabilidade

Redes grandes e complexas são extremamente difíceis e demoradas de gerenciar. É trabalhoso e requer muitos funcionários altamente treinados. Uma única organização pode ter milhares de dispositivos de rede em centenas de locais. Claramente não é praticável monitorar e configurar manualmente este grande número de dispositivos.

A automação envolve a criação de sistemas que operam por conta própria. Automação de rede é o processo de automatizar a configuração, gerenciamento, teste, implantação e operação de dispositivos físicos e virtuais em uma rede. Ao automatizar tarefas diárias de rede, funções e processos repetitivos, a disponibilidade do serviço de rede e a eficiência operacional melhoram.

## 37.6.8 Verifique sua compreensão - Solucione problemas de conectividade remota

### Pergunta 1

Um administrador de rede júnior precisa de uma solução para permitir que os técnicos de help-desk acessem dispositivos remotos para fornecer suporte técnico. A solução precisa ser segura e fornecer uma interface gráfica. Qual tecnologia fornecerá a solução necessária?

- [ ] Telnet
- [x] RDP
- [ ] SSH
- [ ] VPN

✅ RESPOSTA CORRETA: RDP

> Está certo. O Remote Desktop Protocol (RDP) é uma tecnologia que permite uma experiência de desktop completa com gráficos de alta resolução para os usuários acessarem um dispositivo remoto. As sessões RPD operam em um canal criptografado para impedir a espionagem da sessão. A segurança pode ser aprimorada com senhas fortes e autenticação de dois fatores.

### Pergunta 2

Qual tecnologia de tunelamento permite que um usuário se conecte a uma rede privada e acesse remotamente os serviços e recursos da rede?

- [x] VPN de acesso remoto
- [ ] RDP
- [ ] VPN site-to-site
- [ ] GRE tunnel

✅ RESPOSTA CORRETA: VPN de acesso remoto

> Está certo. Uma VPN de acesso remoto cria um túnel virtual entre um dispositivo de usuário e uma rede remota por meio da Internet pública. Através deste túnel VPN o usuário se conecta à rede privada e tem acesso remoto aos serviços e recursos permitidos. Uma VPN site a site é criada quando os dispositivos de terminação da VPN, também chamados de gateways VPN, são pré-configurados com informações para estabelecer um túnel seguro.

### Pergunta 3

O que é usado pelos administradores para controlar, interagir e coletar dados da rede e dos dispositivos clientes?

- [ ] Ferramentas da linha de base de rede
- [ ] Analisadores de protocolo
- [x] Sistemas de monitoramento de rede
- [ ] Bases de conhecimento do fornecedor de rede

✅ RESPOSTA CORRETA: Sistemas de monitoramento de rede

> Está certo. Os sistemas de gerenciamento de rede (NMS) são usados para coletar dados de dispositivos de rede, como switches, roteadores, pontos de acesso e dispositivos clientes. Os dados coletados são usados para fornecer informações sobre a saúde da rede. Um NMS também dá ao administrador de rede a capacidade de controlar a operação desses dispositivos e interação uns com os outros.


# 37.7 Resumo do suporte de rede

## 37.7.1 O que aprendi neste módulo?

### Metodologias de diagnóstico e solução de problemas

A solução de problemas é um processo que deve ser aplicado sistematicamente. Uma abordagem usa um processo de sete etapas em que o técnico define o problema, reúne informações relevantes, analisa as informações, elimina possíveis causas, propõe uma hipótese sobre a causa mais provável do problema e, em seguida, testa a hipótese e resolve o problema. Outra abordagem é seguir as camadas do modelo OSI.

A solução de problemas estruturada pode incluir o uso de sete métodos diferentes, de baixo para cima, de cima para baixo, dividir para conquistar, seguir o caminho, substituição, comparação, suposição fundamentada.

A escolha do método às vezes depende do tipo de problema que está sendo tratado e da experiência do técnico. É importante sempre documentar o problema de acordo com os procedimentos da empresa, inclusive fornecendo informações sobre a eventual resolução do problema.

### Documentação da rede

A documentação da rede é essencial para manter, proteger e solucionar problemas de redes. A documentação pode consistir em diagramas de rede físicos e lógicos, documentos escritos e linhas de base de desempenho de rede.

Existem nove topologias de rede que podem ser documentadas. Isso inclui redes de área pessoal (PAN), redes de área local (LAN), LANs virtuais (VLANS), LANs sem fio (WLAN), redes de malha sem fio (WMN), redes de área de campus (CAN), redes de área metropolitana (MAN), ampla redes de área (WAN) e redes privadas virtuais (VPN).

Os diagramas de topologia física incluem as localizações físicas dos dispositivos e documentam suas conexões. Os diagramas de topologia lógica incluem endereços IP e detalhes do dispositivo de rede, como portas conectadas. Outras informações, como serviços de nuvem, políticas de roteamento e políticas de segurança e acesso remoto, podem aparecer nos diagramas de topologia.

Os serviços em nuvem podem ser Software as a Service (SaaS), Platform as a Service (PaaS), ou Infrastructure as a Service (IaaS). XaaS significa qualquer coisa/tudo como serviço, incluindo desktop como serviço (DaaS), recuperação de desastre como serviço (DRaaS), comunicações como serviço (CaaS) e monitoramento como serviço (MaaS).

Os padrões sem fio definem as características operacionais das operações sem fio, incluindo especificações de sinalização, taxas de dados e eficiência de energia. Os padrões sem fio formam a família de padrões Ethernet sem fio IEEE 802.11, como 802.11b, n, ge ac. Esses padrões existem no espectro sem fio não licenciado. As frequências sem fio licenciadas são controladas pela Federal Communications Commission (FCC) e as licenças são concedidas a estações de rádio, empresas de celular e estações de televisão.

A documentação do dispositivo difere dependendo do tipo de dispositivo. Geralmente inclui sistema operacional e software do dispositivo, informações de licenciamento, status da interface, endereçamento e protocolos de roteamento, etc.

As linhas de base da rede são uma série de medições do desempenho da rede feitas durante diferentes tipos de uso da rede. As linhas de base ajudam a entender os parâmetros de uma rede funcionando adequadamente, de modo que o desempenho da rede ou os problemas de segurança possam ser identificados quando o desempenho se desvia significativamente das medições de linha de base anteriores.

O Cisco Discovery Protocol (CDP) é um protocolo Cisco executado em dispositivos de rede Cisco. Ele envia anúncios CDP para dispositivos vizinhos conectados diretamente. As informações enviadas nesses anúncios incluem o nome do dispositivo configurado, um identificador de porta, a plataforma de hardware e versões de software e endereços IP. Essas informações são exibidas com os comandos IOS show cdp neighbors e show cdp neighbors detail. O CDP pode ser usado para revelar informações sobre topologias de rede.

### Help Desks

As políticas de segurança especificam o que os funcionários precisam fazer para garantir a segurança da rede. Isso inclui políticas relacionadas à identificação e autenticação do usuário, tamanho da senha, complexidade e intervalo de atualização, comportamento aceitável e requisitos de acesso remoto. Os Procedimentos Operacionais Padrão (SOP) definem os procedimentos que devem ser seguidos para substituição de dispositivos de rede, instalação ou remoção de aplicativos de software, integração de novos funcionários e rescisão de funcionários. As diretrizes são sugestões de procedimentos adequados que existem quando nenhum POP é definido.

Um help desk é uma equipe especializada de profissionais de TI que são o ponto central de contato para funcionários e clientes que precisam de assistência técnica. Os help desks usam ferramentas de comunicação como bate-papo, telefone ou e-mail para receber problemas dos clientes e facilitar o processo de solução de problemas. Um sistema de tickets é usado para gerenciar "tickets de problemas" que consistem em detalhes dos problemas relatados pelos usuários. Os usuários iniciam os tickets e os técnicos validam os problemas, trabalham com os usuários para resolver os problemas e encaminham os tickets se um grau mais alto de especialização for necessário para resolver os problemas.

Um técnico de suporte deve ser sempre atencioso e deve simpatizar com os usuários, que podem estar estressados e ansiosos para resolver um problema rapidamente. Os técnicos nunca devem menosprezar, insultar, falar mal ou acusar os usuários de causar o problema.

O conjunto de habilidades Conhecer, se relacionar e entender é uma maneira útil de se relacionar com os clientes. Para conhecer o cliente, chame-o pelo nome ou pergunte se há outro nome que você possa usar. Para se relacionar melhor com o cliente, tente criar uma conexão individual. E para entender o cliente, determine seu nível de conhecimento técnico como forma de falar com ele em um nível adequado. O questionamento é importante usando perguntas abertas ou fechadas. A escuta ativa envolve o uso de respostas compreensivas enquanto os usuários falam e resumem o que eles dizem para verificar sua compreensão.

Ao resolver um problema com hosts, reúna informações sobre o dispositivo, sistema operacional, ambiente de rede e os resultados dos testes de conectividade, como ping e tracert. Outras fontes de informação são códigos de bipe, logs do visualizador de eventos, configurações do gerenciador de dispositivos, dados do gerenciador de tarefas e resultados de ferramentas de diagnóstico.

Para tickets relacionados a dispositivos Cisco, use comandos IOS, capturas de pacotes e logs de dispositivos para coletar informações. Os comandos IOS para teste de conectividade, como ping e traceroute, são úteis. O Secure Shell (SSH) é a maneira preferida de se conectar à CLI do IOS remotamente porque o Telnet não é seguro. Os comandos IOS show, como show ip interface brief, show ip route e show protocols também são úteis.

A próxima etapa no processo de solução de problemas é analisar as informações coletadas e resolver o problema. Você pode consultar o software do sistema de tickets para localizar problemas semelhantes, acessar recursos de informações do fornecedor e perguntas frequentes e pesquisar na Internet informações relevantes. Se você não conseguir resolver o problema, deverá encaminhá-lo para um técnico de nível superior para resolução.

### Solucionar problemas de conectividade de endpoint

Para verificar a configuração de rede de um host Windows, verifique o status das conexões na Central de Rede e Compartilhamento. Você também pode usar ipconfig /all para exibir essas informações. Use ping e traceroute ou tracert para testar a conectividade.

Em um host Linux, você pode visualizar as conexões ativas na GUI ou usar o comando ifconfig em um terminal. Além de ping e traceroute, outras ferramentas de linha de comando, como speedtest e ncat (nc), estão disponíveis para teste de rede.

No MacOS, abra Network Preferences > Advanced para obter informações de endereçamento IP. O comando ifconfig também pode ser emitido de um terminal. Outros comandos úteis são networksetup -listallnetworkservices e networksetup -getinfo <network service>. Os comandos do Linux mencionados acima também estão disponíveis no MacOS. A ferramenta de diagnóstico sem fio do MacOS também pode ajudar a resolver problemas de conectividade.

A rede Apple iOS pode ser verificada acessando as configurações de Wi-Fi. No Android, as informações sobre o endereçamento e as conexões do dispositivo podem ser acessadas em About phone > Status settings. Estão disponíveis aplicativos de terceiros que aprimoram o diagnóstico de redes para Android.

### Solucionar Problemas de uma rede

Para coletar informações para solucionar um problema de rede, os dispositivos Cisco IOS têm muitos comandos show que podem fornecer informações detalhadas. O software Cisco IOS separa o acesso de gerenciamento em dois níveis de privilégio: User EXEC, que é de nível inferior, e Privileged EXEC, que possui privilégios totais. Use o comando enable para entrar no modo Cisco EXEC privilegiado A ajuda sensível ao contexto do IOS pode ser usada para localizar comandos e obter informações sobre seu uso. A ajuda contextual está disponível inserindo um "?" em um prompt vazio ou após um comando.

Os aplicativos de captura de pacotes e análise de protocolo permitem que você investigue o conteúdo do pacote à medida que ele flui pela rede. O software decodifica as camadas de protocolo alojadas em um pacote. O Wireshark é um exemplo de aplicativo popular de análise de protocolo/captura de pacotes de código aberto.

Largura de banda e taxa de transferência são características do fluxo de dados da rede. Largura de banda é a quantidade teórica de dados que podem ser transmitidos de um dispositivo para outro em um período de tempo. A largura de banda é normalmente medida em número de bits por segundo. Taxa de transferência é a medida do número real de bits por segundo que estão sendo transmitidos pela mídia. A taxa de transferência é sempre menor que a largura de banda devido à latência e ao atraso. As ferramentas de teste de velocidade da Internet on-line e a ferramenta iPerf Windows permitem a medição da taxa de transferência.

### Solucionar problemas de Conectividade Remotamente

Ao auxiliar usuários remotos, pode ser mais eficiente usar aplicativos de área de trabalho remota. Esses aplicativos permitem que um técnico assuma o controle de uma área de trabalho remota para investigar problemas e fazer alterações na configuração. Os aplicativos de área de trabalho remota podem criar vulnerabilidades de segurança e muitas organizações têm o compartilhamento de área de trabalho desativado nos computadores. O Microsoft Remote Desktop está incluído em todas as versões profissionais do Windows. O Apple Remote Desktop e o TeamViewer são exemplos de outros softwares de desktop remoto.

Telnet, SSH e Remote Desktop Protocol (RDP) são protocolos para acesso remoto a sistemas. Telnet é um antigo aplicativo de terminal virtual usado para acessar a linha de comando de um sistema remoto. Ele usa a porta TCP 23. O Telnet não possui nenhum mecanismo para criptografar os dados transmitidos e, portanto, não deve ser usado. O SSH, assim como o Telnet, permite sessões de terminal virtual, mas inclui criptografia e deve ser usado no lugar do Telnet. Clientes de terminais virtuais, como PuTTY e Tera Term, estão disponíveis para conexão com servidores Telnet e SSH.

O RDP foi criado pela Microsoft. Ele também usa um modelo cliente-servidor no qual o cliente acessa uma GUI do sistema operacional em um computador remoto. O software RDP está disponível com Windows, OS X, Linux e Unix via xrdp. Para macOS, a funcionalidade de área de trabalho remota é fornecida pelo software Virtual Network Computing (VNC).

As Redes Privadas Virtuais (VPN) permitem o acesso remoto seguro à rede em redes não seguras, como a Internet. Uma VPN usa conexões seguras dedicadas que criptografam o tráfego de rede. VPNs site a site conectam instalações remotas inteiras. As VPNs de acesso remoto conectam usuários individuais à rede corporativa. Os usuários de VPN de acesso remoto se conectam a um gateway de VPN de rede corporativa usando um cliente de software como o Cisco AnyConnect. O Microsoft Windows tem seu próprio cliente VPN.

O gerenciamento de rede refere-se ao processo de configuração, monitoramento e gerenciamento do desempenho de uma rede. As plataformas modernas de gerenciamento de rede fornecem análises avançadas, aprendizado de máquina e automação inteligente para otimizar continuamente o desempenho da rede. Os sistemas de gerenciamento de rede geralmente usam o Simple Network Management Protocol (SNMP) e o Remote Network Monitoring (RMON) para coletar informações. Os sistemas de gerenciamento de rede podem ser implantados em modelos locais ou baseados em nuvem. As implantações baseadas em nuvem são boas para ambientes distribuídos geograficamente dispersos. Os sistemas locais exigem muito poder de computação e armazenamento, mas são bons para situações em que a conformidade com os regulamentos de soberania de dados é necessária. Cisco Meraki é uma plataforma líder de gerenciamento de rede baseada em nuvem que fornece recursos de gerenciamento de rede poderosos sem consumir largura de banda do usuário.

Automação de rede é o processo de automatizar a configuração, gerenciamento, teste, implantação e operação de dispositivos físicos e virtuais em uma rede. Tarefas comuns de trabalho intensivo podem ser automatizadas usando scripts e programação de rede. Python é uma linguagem de script popular para automação de rede.

## 37.7.2 Webster - Questões para reflexão

Lara fez um ótimo trabalho criando um guia de solução de problemas para técnicos de help desk. Compartilhar sua experiência de help desk ajudará os novos técnicos a se tornarem mais eficazes rapidamente. A informação foi prática neste módulo? Como estão suas habilidades de diagnóstico? Qual abordagem de solução de problemas funcionaria melhor se um problema estiver relacionado ao cabeamento? Qual abordagem de solução de problemas funcionaria melhor se o problema estivesse relacionado a um aplicativo?