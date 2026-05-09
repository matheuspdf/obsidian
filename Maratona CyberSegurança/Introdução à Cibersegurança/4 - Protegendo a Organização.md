## 4.1 Dispositivos e Tecnologias de segurança cibernética

### 4.1.1 Dispositivos de segurança
Os dispositivos de segurança podem ser dispositivos independentes, como um roteador ou ferramentas de software que são executados em um dispositivo de rede. Eles se enquadram em seis categorias gerais.

**Roteadores**

Embora os roteadores sejam usados principalmente para interconectar vários segmentos de rede, eles geralmente também oferecem recursos básicos de filtragem de tráfego. Essas informações podem ajudá-lo a definir quais computadores de um determinado segmento de rede podem se comunicar com quais segmentos de rede.

**Firewalls**

Os firewalls podem analisar melhor o tráfego de rede e identificar comportamentos mal-intencionados que precisam ser bloqueados. Os firewalls podem ter políticas de segurança sofisticadas aplicadas ao tráfego que passa por eles.

**Sistemas de prevenção de invasão**

Os sistemas IPS usam um conjunto de assinaturas de tráfego que correspondem e bloqueiam tráfego e ataques mal-intencionados.

**Redes Privadas Virtuais (VPN)**

Os sistemas de VPN permitem que os funcionários remotos usem um túnel criptografado seguro em seus computadores móveis e se conectem com segurança à rede da empresa. Os sistemas de VPN também podem interconectar com segurança filiais com a rede da central.

**Antivírus e Antimalware**

Esses sistemas usam assinaturas ou análises comportamentais das aplicações para identificar e bloquear a execução de códigos mal-intencionados.

**Outros dispositivos de segurança**

Outros dispositivos de segurança incluem dispositivos de segurança para web e e-mail, dispositivos de descriptografia, servidores de controle de acesso de clientes e sistemas de gerenciamento de segurança.


### 4.1.2 Qual é?
Isto é interessante! Você se pergunta qual sistema de segurança está sendo implementado na @Apollo.

Você pergunta ao Chief Technology Officer (CTO), que explica que os seguintes dispositivos de segurança estão instalados. Você consegue identificar em qual categoria cada uma delas se encaixa? Você tem a chance de ganhar alguns pontos de defensor, então escolha suas respostas com cuidado.

**O Cisco ISR 4000 oferece roteamento, filtragem e criptografia em uma única plataforma** ✅ **Roteador**

---

**O Cisco Firepower 4100 Series mostra o que está acontecendo na rede para que você possa agir com mais rapidez diante de um ataque cibernético** ✅ **Firewall**

---

**O AnyConnect Secure Mobility Client da Cisco capacita funcionários remotos com acesso altamente seguro à rede de @Apollo de qualquer dispositivo, a qualquer hora e em qualquer local** ✅ **VPN**

---

**O AMP da Cisco oferece proteção de endpoint de próxima geração, varredura e monitoramento constante de arquivos em relação a comportamentos mal-intencionados** ✅ **Antimalware**

**Muito bem, foi complicado!**

Mas você conseguiu identificar corretamente os dispositivos de segurança e garantiu a segurança da @Apollo contra ataques cibernéticos… por enquanto!

Em resumo, os dispositivos de segurança implementados são:

- **Cisco Integrated Services Router (ISR) 4000**. Esses roteadores têm muitos recursos, incluindo filtragem de tráfego, a capacidade de executar um sistema de prevenção de intrusão (IPS), criptografia e recursos de VPN para encapsulamento criptografado seguro.
    
- **Cisco’s Firepower 4100 Series** é um firewall de última geração que possui todos os recursos de um roteador ISR, bem como gerenciamento e análise de rede avançados. Ele pode ajudá-lo a ver o que está acontecendo na rede para que você possa detectar ataques mais cedo.
    
- **Cisco’s AnyConnect Secure Mobility Client** é um sistema de VPN que permite que funcionários remotos usem um túnel criptografado seguro de seu computador móvel para se conectarem de volta à rede da empresa. Todos os dispositivos de segurança da Cisco estão equipados com um servidor VPN e tecnologia de cliente, projetados para tunelamento criptografado seguro.
    
- **Cisco’s Advanced Malware Protection (AMP)** é instalado em roteadores Cisco, firewalls, dispositivos IPS e dispositivos de segurança de e-mail e web de próxima geração. Também pode ser instalado como software em computadores host.

### 4.1.3 Firewalls
Em redes de computadores, um firewall é projetado para controlar ou filtrar quais comunicações são permitidas dentro e quais são permitidas fora de um dispositivo ou rede. Um firewall pode ser instalado em um único computador com o objetivo de proteger aquele computador (firewall baseado em host) ou pode ser um dispositivo de rede autônomo que protege uma rede inteira de computadores e todos os dispositivos host nessa rede (firewall baseado em rede).

À medida que os ataques a computadores e redes se tornaram mais sofisticados, novos tipos de firewalls foram desenvolvidos, com finalidades diferentes.

## Tipos de Firewall

**Firewall de camada de rede** Filtra as comunicações com base nos endereços IP de origem e destino.

---

**Firewall da camada de transporte** Filtra as comunicações com base nas portas de dados de origem e destino, bem como nos estados de conexão.

---

**Firewall da camada de aplicação** Filtra as comunicações de acordo com um aplicativo, programa ou serviço.

---

**Firewall sensível ao contexto (Context-aware)** Filtra as comunicações com base no usuário, dispositivo, função, tipo de aplicativo e perfil de ameaça.

---

**Servidor proxy** Filtra solicitações de conteúdo da Web, como URLs, nomes de domínio e tipos de mídia.

---

**Servidor proxy reverso** Colocados na frente de servidores web, os servidores proxy reversos protegem, ocultam, descarregam e distribuem o acesso aos servidores web.

---

**Network address translation (NAT) firewall** Este firewall oculta ou mascara os endereços privados dos hosts da rede.

---

**Firewall baseado em host** Filtra portas e chamadas de serviço do sistema em um único sistema operacional de computador.

### 4.1.4 Qual é?
O CTO esqueceu de mencionar que o @Apollo tem alguns firewalls implementados. Com base nas seguintes afirmações, você consegue identificar qual é a categoria de firewall? Responda corretamente para ganhar pontos de defensor valiosos que ajudarão a proteger @Apollo de ataques.

**Uma pequena rede de área local interna com computadores requer acesso à Internet usando uma única conexão com a Internet** ✅ **NAT firewall**

---

**Por padrão, o Windows tenta bloquear o acesso a aplicativos em execução em computadores Windows de outros computadores na rede** ✅ **Firewall baseado em host**

---

**Os funcionários que usam computadores na rede não têm acesso a URLs específicas, como sites de jogos** ✅ **Servidor proxy**


**Está correto!**

Você identificou corretamente os tipos de firewall e ganhou alguns pontos de defensor! Verifique seu progresso clicando no ícone de escudo no canto superior direito da tela.

Lembre-se:

- Um **NAT firewall** filtra as comunicações de acordo com os endereços IP de origem e destino.
- Um **servidor proxy** filtra solicitações de conteúdo da Web, como URLs, nomes de domínio e tipos de mídia.
- Um **firewall baseado em host** filtra portas e chamadas de serviço do sistema em um único sistema operacional de computador.

### 4.1.5 – Varredura de portas
Na rede, cada aplicativo em execução em um dispositivo recebe um identificador ou número de porta. Esse número da porta é usado em ambas as extremidades da transmissão para que os dados certos sejam passados ao aplicativo correto. A varredura de portas é um processo de sondar um computador, servidor ou outro host de rede em busca de portas abertas. Ele pode ser usado maliciosamente como uma ferramenta de reconhecimento para identificar o sistema operacional e os serviços em execução em um computador ou host, ou pode ser usado sem causar danos por um administrador de rede para verificar as políticas de segurança da rede.

Baixe e inicie uma ferramenta de varredura de portas como [Zenmap](https://nmap.org/zenmap/). Digite o endereço IP do seu computador, escolha um perfil de varredura padrão e pressione “scan”.

A varredura irá relatar todos os serviços em execução, como serviços da Web ou de e-mail e seus números de porta.

A verificação também irá relatar uma das seguintes respostas:

1. “Aberto” ou “Aceito” significa que a porta ou o serviço em execução no computador pode ser acessado por outros dispositivos de rede.
2. “Fechado”, “Negado” ou “Não atende” significa que a porta ou o serviço não está sendo executado no computador e, portanto, não pode ser explorado.
3. “Filtrado”, “Descartado” ou “Bloqueado” significa que o acesso à porta ou ao serviço é bloqueado por um firewall e, portanto, não pode ser explorado.

Para executar uma verificação de porta de fora da rede, você precisará executá-la no firewall ou no endereço IP público do roteador.

Insira a pergunta "qual é o meu endereço IP?" em um mecanismo de pesquisa como o Google para descobrir essas informações.

Acesse o [Nmap Online Port Scanner](https://hackertarget.com/nmap-online-port-scanner/), digite seu endereço IP público na caixa de entrada e pressione “Quick Nmap Scan”. Se a resposta estiver aberta para as portas 21, 22, 25, 80, 443 ou 3389, provavelmente o encaminhamento de porta foi habilitado em seu roteador ou firewall e você está executando servidores em sua rede privada.


### 4.1.6 O que isso significa?

Seu gerente pede que você avalie o firewall da rede de computadores da @Apollo e a segurança de porta. Você executa uma varredura de porta, que retorna uma resposta de estado "aberto".

**Complete a frase:**

> The port scan reported an 'open' state response. This means that the service running on the network **[pode ser acessado]** by other network devices. Therefore, if the service contains a vulnerability, it **[pode ser explorado]** by an attacker.

✅ **Lacuna 1:** pode ser acessado ✅ **Lacuna 2:** pode ser explorado

**É isso mesmo.**

Uma resposta de estado "aberto" significa que o serviço em execução na rede **pode ser acessado** por outras redes e, se o serviço contiver uma vulnerabilidade, **ele poderá ser explorado por um invasor**que pode, potencialmente, obter acesso a computadores na rede.

É importante observar que a varredura de portas deve ser vista como um precursor de um ataque à rede e, portanto, **nunca**deve ser realizada em servidores públicos na Internet ou na rede de uma organização sem permissão.

### 4.1.7 Sistemas de detecção e prevenção de intrusos.
Sistemas de detecção de intrusão (IDSs) e sistemas de prevenção de intrusão (IPSs) são medidas de segurança implantadas em uma rede para detectar e prevenir atividades maliciosas.


Um IDS pode ser um dispositivo de rede dedicado ou uma das várias ferramentas em um servidor, firewall ou até mesmo um sistema operacional de computador host, como Windows ou Linux, que faz a varredura de dados em um banco de dados de regras ou assinaturas de ataque, em busca de tráfego malicioso.

Se uma correspondência for detectada, o IDS registrará a detecção de registro e criará um alerta para um administrador de rede. Ela não tomará nenhuma ação e, portanto, não impedirá que os ataques aconteçam. O trabalho do IDS é detectar, registrar e relatar.

A varredura realizada pelo IDS deixa a rede mais lenta (conhecido como latência). Para se prevenir o atraso de rede, um IDS é geralmente colocado off-line, separado do tráfego de rede regular. Dados são copiados ou espelhados por um switch e então encaminhados para o IDS para a detecção off-line.
![[Pasted image 20260328201213.png]]

Um IPS pode bloquear ou negar tráfego com base em uma regra positiva ou correspondência de assinatura. Um dos sistemas mais conhecidos de IPS/IDS é o Snort. A versão comercial do Snort é o Sourcefire da Cisco. A Sourcefire pode realizar análise de tráfego e porta em tempo real, registrar, pesquisar e correspondência de conteúdo, bem como detectar sondas, ataques e executar varreduras de porta. Ele também se integra com outras ferramentas de terceiros para relatórios, desempenho e análise de log.
![[Pasted image 20260328201323.png]]


### 4.1.8 Detecção em tempo real
Muitas organizações hoje são incapazes de detectar ataques dias ou até meses após sua ocorrência.

A detecção de ataques em tempo real requer a verificação ativa de ataques usando firewall e dispositivos de rede IDS/IPS. A detecção de malware de cliente e servidor de próxima geração com conexões a centros de ameaças globais online também deve ser usada. Atualmente, os softwares e dispositivos de varredura ativos devem detectar anomalias de rede usando a detecção de comportamento e análise baseada em contexto.

DDoS é uma das maiores ameaças de ataque que requer detecção e resposta em tempo real. Para muitas organizações, ataques DDoS que ocorrem regularmente prejudicam os servidores da Internet e a disponibilidade da rede. Esses ataques são extremamente difíceis de se defender porque os ataques se originam de centenas, até mesmo milhares, de hosts zumbis, e os ataques aparecem como tráfego legítimo.

### 4.1.9 Proteção contra Malware
Uma forma de se defender contra ataques de dia zero e ameaças persistentes avançadas (APTs) é usar uma solução empresarial de detecção de malware, como o **Advanced Malware Protection (AMP) Threat Grid da Cisco.**

AMP é um software cliente/servidor que pode ser implantado em host endpoints, como um servidor autônomo ou em outros dispositivos de segurança de rede. Ele analisa milhões de arquivos e os correlaciona com centenas de milhões de outros artefatos de malware analisados para comportamentos que revelam um APT. Isso proporciona uma visão geral de ataques, de campanhas e de distribuição de malware.

**Equipe do SOC (centro de operações de segurança)** O Threat Grid permite que a equipe do Cisco Secure Operations Center colete dados mais precisos e úteis.

---

**Equipe de resposta a incidentes** A equipe de resposta a incidentes, portanto, tem acesso a informações forenses confiáveis que permitem analisar e entender comportamentos suspeitos com mais rapidez.

---

**Equipe de inteligência de ameaças** Usando essa análise, a equipe de inteligência de ameaças pode melhorar proativamente a infraestrutura de segurança da empresa.

---

**Equipe de engenharia da infraestrutura de segurança** No geral, a equipe de engenharia de infraestrutura de segurança é capaz de consumir e agir com base nas informações de ameaças com mais rapidez, geralmente de forma automatizada.


### 4.1.10 Práticas recomendadas de segurança

Muitas empresas e profissionais publicaram listas das melhores práticas de segurança. Algumas das diretrizes mais úteis são encontradas em repositórios organizacionais, como o Centro de Recursos de Segurança de Computadores do Instituto Nacional de Padrões e Tecnologia (NIST).

#### Boas Práticas de Segurança Organizacional

---

##### Executar avaliação de risco

> Saber o valor do que você está protegendo ajudará a justificar os gastos com segurança.

---

##### Criar uma política de segurança

> Criar uma política que descreva com clareza as regras da empresa, os cargos, as responsabilidades e expectativas dos funcionários.

---

##### Medidas de segurança física

> Restrinja o acesso a armários de rede e locais de servidor, bem como supressão de incêndio.

---

##### Medidas de segurança para recursos humanos

> As verificações de antecedentes devem ser concluídas para todos os funcionários.

---

##### Realizar e testar backups

> Faça backup das informações regularmente e teste a recuperação de dados dos backups.

---

##### Manter patches e atualizações de segurança

> Atualize regularmente os sistemas operacionais e programas de servidores, clientes e dispositivos de rede.

---

##### Empregar controles de acesso

> Configure funções e níveis de privilégio do usuário, bem como autenticação forte de usuário.

---

##### Testar regularmente a resposta a incidentes

> Empregue uma equipe de resposta a incidentes e teste cenários de resposta a emergências.

---

##### Implementar ferramenta de monitoramento, análise e gerenciamento de rede

> Escolha uma solução de monitoramento de segurança que se integre com outras tecnologias.

---

##### Implementar dispositivos de segurança de rede

> Use roteadores, firewalls e outros aparelhos de segurança de última geração.

---

##### Implementar solução de segurança de endpoints abrangente

> Use antimalware e software antivírus de nível empresarial.

---

##### Educar os usuários

> Fornecer treinamento aos funcionários em procedimentos de segurança. Uma das empresas mais conhecidas e respeitadas para o treinamento de segurança cibernética é o **Instituto SANS**.

---

##### Criptografar dados

> Criptografe todos os dados confidenciais da organização, incluindo o e-mail.




##  4.2 Abordagem comportamental à segurança cibernética
### 4.2.1 – Segurança baseada em comportamento

A segurança baseada em comportamento é uma forma de detecção de ameaças que envolve a captura e análise do fluxo de comunicação entre um usuário na rede local e um destino local ou remoto. Quaisquer alterações nos padrões normais de comportamento são consideradas anomalias e podem indicar um ataque.

### Honeypots

> Um honeypot é uma ferramenta de detecção baseada em comportamento que atrai o invasor apelando para seu padrão previsto de comportamento malicioso. Quando o invasor estiver dentro do honeypot, o administrador de rede poderá capturar, registrar e analisar o comportamento dele para que possa construir uma defesa melhor.
> 
![[Pasted image 20260328205404.png]]



### Arquitetura da Solução Cisco Cyber Threat Defense

> Esta arquitetura de segurança usa detecção e indicadores baseados em comportamento para fornecer maior visibilidade, contexto e controle. O objetivo é saber quem está realizando o ataque, que tipo de ataque ele está realizando e onde, quando e como o ataque está ocorrendo. Essa arquitetura de segurança usa muitas tecnologias de segurança para atingir esse objetivo.
![[Pasted image 20260328205432.png]]


### 4.2.2. NetFlow
A tecnologia NetFlow é usada para coletar informações sobre os dados que fluem através de uma rede, incluindo quem e quais dispositivos estão na rede, e quando e como os usuários e dispositivos acessam a rede.

O NetFlow é um componente importante na análise e detecção baseada em comportamento. Switches, roteadores e firewalls equipados com NetFlow podem relatar informações sobre a entrada, saída e passagem de dados pela rede. 

Essas informações são enviadas para coletores do NetFlow que coletam, armazenam e analisam dados do NetFlow, que podem ser usados para estabelecer comportamentos de linha de base em mais de 90 atributos, como endereço IP de origem e destino.

![[Pasted image 20260328205526.png]]

### 4.2.3 Teste de penetração
O teste de penetração, conhecido como pen testing, é o ato de avaliar um sistema de computador, uma rede ou uma empresa em busca de vulnerabilidades de segurança. Um pen test procura violar sistemas, pessoas, processos e códigos para descobrir vulnerabilidades que podem ser exploradas. Essas informações são usadas para melhorar as defesas do sistema e garantir que ele possa suportar ataques cibernéticos no futuro.

#### Etapas do Teste de Penetração (Pen Test)

---

##### Etapa 1: Planejamento

> O pen tester coleta o máximo de informações possível sobre um sistema ou rede de destino, suas vulnerabilidades e exploits potenciais para usar contra ele. Isso envolve a realização de pesquisas de vulnerabilidade e reconhecimento passivo ou ativo (footprinting).

---

##### Etapa 2: Varredura

> O pen tester realiza o reconhecimento ativo para investigar um sistema ou rede de destino e identificar possíveis pontos fracos que, se explorados, podem dar acesso ao invasor. O reconhecimento ativo pode incluir:

- Varredura de porta para identificar possíveis pontos de acesso em um sistema de destino
- Verificação de vulnerabilidades para identificar possíveis vulnerabilidades exploráveis de um determinado alvo
- Estabelecer uma conexão ativa com um destino (enumeração) para identificar a conta de usuário, de sistema e de administrador

---

##### Etapa 3: Obter acesso

> O pen tester tentará obter acesso a um sistema de destino e detectar o tráfego de rede, usando vários métodos para explorar o sistema, incluindo:

- Lançar um exploit com um payload no sistema
- Violar barreiras físicas a ativos
- Engenharia social
- Explorando vulnerabilidades de sites
- Explorando vulnerabilidades ou configurações incorretas de software e hardware
- Violar a segurança dos controles de acesso
- Quebrar Wi-Fi com criptografia fraca

---

##### Etapa 4: Manter o acesso

> O pen tester manterá o acesso ao alvo para descobrir quais dados e sistemas estão vulneráveis à exploração. É importante que não sejam detectados, normalmente usando backdoors, cavalos de Troia, rootkits e outros canais encobertos para ocultar sua presença.

> Quando essa infraestrutura estiver em vigor, o pen tester prosseguirá para coletar os dados que eles consideram valiosos.

---

##### Etapa 5: Análise e geração de relatórios

> O pen tester fornecerá feedback por meio de um relatório que recomenda atualizações de produtos, políticas e treinamento para melhorar a segurança de uma empresa.



### 4.2.4 Sua vez de

Você foi encarregado de realizar um teste interno para verificar a rede de computadores da @Apollo em busca de vulnerabilidades. Como você conduzirá o teste?

**Coloque as etapas a seguir na ordem correta:**

---

|Ordem|Etapa|
|---|---|
|**1**|Reúna o máximo de informações possível sem ser detectado|
|**2**|Investigue a rede para encontrar maneiras de invadir|
|**3**|Identifique possíveis vulnerabilidades exploráveis|
|**4**|Explore todas as vulnerabilidades identificadas na rede simulando um ataque|
|**5**|Relate suas descobertas para a equipe|

**Ótimo trabalho! Você identificou corretamente como realizar um teste de penetração:**

1. O impacto na rede para encontrar maneiras de invadir a oportunidade de coletar as informações necessárias para **planejar** um ataque simulado.
2. **A varredura** de um alvo permite identificar possíveis pontos fracos que podem ser explorados.
3. Você precisará **obter acesso** a uma rede para explorar quaisquer vulnerabilidades e simular um ataque.
4. **Manter o acesso**, sem ser detectado, significa que você pode coletar mais informações sobre as vulnerabilidades de um alvo.
5. Suas descobertas serão **relatadas** à empresa para que melhorias de segurança possam ser feitas.

### 4.2.5 Redução do impacto
Embora a maioria das empresas hoje esteja ciente das ameaças de segurança comuns e se esforce consideravelmente para evitá-las, nenhum conjunto de práticas de segurança é infalível. Portanto, as empresas devem estar preparadas para conter os danos caso ocorra uma violação de segurança. E devem agir rápido!

**Como Responder a uma Violação de Segurança**

---
Comunicar o problema

> A comunicação cria transparência, o que é fundamental neste tipo de situação. Internamente, todos os funcionários devem ser informados e um plano de ação claro deve ser comunicado. Externamente, todos os clientes devem ser informados através de comunicação direta e anúncios oficiais.

---

Ser sincero e responsável

> Responda à violação de forma honesta e genuína, assumindo a responsabilidade onde a empresa é culpada.

---

Forneça os detalhes

> Esteja aberto e explique por que a violação ocorreu e quais informações foram comprometidas. Em geral, espera-se que as organizações cuidem de todos os custos do cliente associados aos serviços de roubo de identidade necessários como resultado de uma violação de segurança.

---

Encontre a causa

> Tome medidas para entender o que causou e facilitou a violação. Isso pode envolver a contratação de especialistas forenses para pesquisar e descobrir os detalhes.

---

Aplicar lições aprendidas

> Certifique-se de que todas as lições aprendidas em investigações forenses sejam aplicadas para evitar violações semelhantes no futuro.

---

Verificar, e verificar novamente

> Os invasores, muitas vezes, tentarão deixar um backdoor para facilitar futuras violações. Para evitar que isso aconteça, certifique-se de que todos os sistemas estejam limpos, não haja backdoors instalados e nada mais tenha sido comprometido.

---

Eduque!

> Conscientizar, treinar e educar funcionários, parceiros e clientes sobre como prevenir violações futuras.


### 4.2.6 O que é gerenciamento de risco?
O gerenciamento de riscos é o processo formal de identificação e avaliação contínuas dos riscos para reduzir o impacto das ameaças e vulnerabilidades. Você não pode eliminar completamente o risco, mas pode determinar níveis aceitáveis ponderando o impacto de uma ameaça com o custo de implementação de controles para mitigá-la. O custo de um controle nunca deve ser maior que o valor do ativo que você está protegendo.


Avaliação de Risco

---

1. Defina o risco

> Identifique as ameaças que aumentam o risco. As ameaças podem incluir processos, produtos, ataques, possível falha ou interrupção de serviços, percepção negativa da reputação de uma empresa, possível responsabilidade legal ou perda de propriedade intelectual.

---

2. Classifique o risco

> Determine a gravidade que cada ameaça representa. Por exemplo, algumas ameaças podem paralisar toda uma empresa, enquanto outras podem ser apenas pequenos inconvenientes. O risco pode ser priorizado ao avaliar o impacto financeiro _(análise quantitativa)_ ou o impacto escalado na operação de uma organização _(análise qualitativa)_.

---

3. Responda ao risco

> Desenvolver um plano de ação para reduzir a exposição geral aos riscos da empresa, detalhando onde os riscos podem ser eliminados, mitigados, transferidos ou aceitos.

---

4. Monitore o risco

> Analise continuamente qualquer risco reduzido por meio de ações de eliminação, mitigação ou transferência. Lembre-se, nem todos os riscos podem ser eliminados, então você precisará monitorar atentamente todas as ameaças que foram aceitas.


## 4.3 Abordagem da Cisco para segurança cibernética
### 4.3.1 O CSIRT da Cisco
Muitas empresas de grande porte têm uma equipe de resposta a incidentes de segurança computacional (CSIRT-Computer Security Incident Response Team) para recepção, análise e resposta de incidentes de segurança de computador. O Cisco CSIRT vai um passo além e fornece avaliação proativa de ameaças, planejamento de mitigação, análise de tendências de incidentes e revisão da arquitetura de segurança em um esforço para prevenir a ocorrência de incidentes de segurança.

O CSIRT da Cisco tem uma abordagem proativa, colaborando com o Forum of Incident Response and Security Teams (FIRST), National Safety Information Exchange (NSIE), Defense Security Information Exchange (DSIE) e o DNS Operations Analysis and Research Center (DNS-OARC ) para garantir que estejamos atualizados com os novos desenvolvimentos.

Existem várias organizações CSIRT nacionais e públicas, como a Divisão CERT do Software Engineering Institute da Carnegie Mellon University, que estão disponíveis para ajudar as organizações e CSIRTs nacionais a desenvolver, operar e melhorar suas capacidades de gerenciamento de incidentes.

### 4.3.2 – Cartilha de segurança
Uma das melhores maneiras de se preparar para uma violação de segurança é evitá-la. As empresas devem fornecer orientação sobre:

- como identificar os riscos de segurança digital para sistemas, ativos, dados e recursos
- a implementação de proteções e treinamento de pessoal
- um plano de resposta flexível que minimiza o impacto e os danos em caso de violação de segurança
- as medidas e os processos de segurança que precisam ser implementados após uma violação de segurança.

Todas estas informações devem ser compiladas em um manual de segurança.

#### Manual de Segurança

> Um manual de segurança é um conjunto de consultas ou relatórios que descrevem um processo padronizado de detecção e resposta a incidentes.

Idealmente, um manual de segurança deve:

- Destacar como identificar e automatizar a resposta a ameaças comuns, como a detecção de máquinas infectadas por malware, atividade de rede suspeita ou tentativas de autenticação irregular
- Descrever e definir claramente o tráfego de entrada e saída
- Fornecer informações resumidas, incluindo tendências, estatísticas e contagens
- Fornecer acesso utilizável e rápido às principais estatísticas e métricas
- Correlacionar eventos em todas as fontes de dados relevantes

### 4.3.3 – Ferramentas para prevenção e detecção de incidentes
Estas são algumas das ferramentas usadas para detectar e prevenir incidentes de segurança:

#### SIEM — Security Information and Event Management

> Um sistema SIEM coleta e analisa alertas de segurança, logs e outros dados históricos e em tempo real de dispositivos de segurança na rede para facilitar a detecção precoce de ataques cibernéticos.

---

#### DLP — Data Loss Prevention

> Um sistema DLP é projetado para impedir que dados confidenciais sejam roubados ou escapem de uma rede. Ele monitora e protege os dados em três estados diferentes:

- **Dados em uso** — dados sendo acessados por um usuário
- **Dados em movimento** — dados que viajam pela rede
- **Dados inativos** — dados armazenados em uma rede ou dispositivo de computador

### 4.3.4 Cisco ISE e TrustSec
O Cisco Identity Services Engine (ISE) e o TrustSec reforçam o acesso do usuário aos recursos de rede ao criar políticas de controle de acesso por função.

#### Cisco Network Visibility e Segmentação (NVS)

> As redes atuais estão sob mais pressão do que nunca — para lidar com mais usuários, mais dispositivos, acesso móvel, nuvem, e um volume crescente de ataques digitais. À medida que a rede cresce, torna-se mais difícil ver quem está participando e detectar quando ela foi violada.

Hoje, é necessário um nível totalmente novo de visibilidade para identificar o tráfego mal-intencionado e detê-lo imediatamente. Esse é o poder do **NVS**, que usa soluções avançadas de segurança de rede da Cisco trabalhando em conjunto para identificar e conter ameaças.

---

#### Componentes do NVS

**StealthWatch**

> Usa aprendizado de máquina para analisar o tráfego de rede e detectar ameaças de forma eficaz, mesmo quando criptografadas.

**Cisco Identity Services Engine (ISE)**

> Aprofunda a visibilidade com mais detalhes sobre usuários e dispositivos, atuando como um gerenciador de políticas central.

**Cisco TrustSec**

> Funciona em conjunto com o ISE para simplificar o controle de acesso e aplicar automaticamente a política de segmentação em toda a rede para quarentena de ameaças.

---

> Juntos, **StealthWatch, ISE e TrustSec** oferecem a visibilidade, o controle e a automação necessários para proteger sua rede em tempo real — transformando-a para a nova era digital, para que você possa crescer na velocidade da empresa.


### 4.3.5 Conheça a linguagem
Este módulo contém muitas informações técnicas e jargões que você precisa saber para desenvolver sua carreira em segurança digital. Então, antes de prosseguir, vamos verificar sua compreensão de alguns desses termos-chave. É a sua última chance de ganhar pontos de defensor, então pense bem antes de fazer suas escolhas.

**Bloqueia ou nega o tráfego com base em uma correspondência de regra ou assinatura positiva** ✅ **IPS**

---

**Um sistema projetado para impedir que dados confidenciais sejam roubados ou escapem de uma rede** ✅ **DLP**

---

**Um sistema que coleta e analisa alertas de segurança, registros e outros dados históricos e em tempo real de dispositivos de segurança na rede** ✅ **SIEM**

---

**Verifica os dados em um banco de dados de regras ou assinaturas de ataque, registra quaisquer detecções e cria um alerta para o administrador da rede** ✅ **IDS**


**Está correto!**

Você correspondeu com sucesso cada termo à sua descrição e ganhou alguns pontos que ajudarão a proteger @Apollo de um ataque cibernético.

Lembre-se:

- Um **IPS** pode bloquear ou negar o tráfego com base em uma regra positiva ou correspondência de assinatura.
- Um **IDS** verifica os dados em um banco de dados de regras ou assinaturas de ataque, em busca de tráfego malicioso.
- Um **DLP** é projetado para impedir que dados confidenciais sejam roubados ou escapem de uma rede 
- Um **SIEM** coleta e analisa alertas de segurança, logs e outros dados históricos e em tempo real de dispositivos de segurança na rede.

## 4.4 Questionário

Quiz de Segurança de Redes — Gabarito

---

Pergunta 1

**Qual das seguintes ferramentas pode ser usada para fornecer uma lista de portas abertas em dispositivos de rede?**

- Whois
- ✅ **Nmap**
- Ping
- Tracert

---

Pergunta 2

**"Hoje, existem dispositivos de segurança únicos que irão resolver todas as necessidades de segurança de rede de uma organização." — Esta afirmação é verdadeira ou falsa?**

- ✅ **Falso**
- Verdadeiro

---

Pergunta 3

**Qual das seguintes ferramentas pode realizar análise de tráfego e porta em tempo real, e também pode detectar varreduras de porta, impressão digital e ataques de estouro de buffer?**

- SIEM
- NetFlow
- Nmap
- ✅ **Snort**

---

Pergunta 4

**Qual é a definição correta de gerenciamento de riscos?**

- ✅ **O processo de identificação e avaliação de riscos para reduzir o impacto de ameaças e vulnerabilidades**
- O processo de aceitação de riscos que não podem ser eliminados, mitigados ou transferidos
- O processo de transferência de riscos que não podem ser eliminados ou mitigados
- O processo de identificação e avaliação de riscos para determinar a gravidade das ameaças

---

Pergunta 5

**Qual é a última fase de um teste de penetração?**

- Coletar informações do alvo
- Manutenção do acesso
- ✅ **Análise e relatórios**
- Scanning

---

Pergunta 6

**A análise baseada em comportamento envolve o uso de informações básicas para detectar o quê?**

- ✅ **Anomalias**
- Vulnerabilidades
- Backdoors
- Risco

---

Pergunta 7

**Quais das seguintes ações uma empresa deve realizar no caso de uma violação de segurança? _(Duas respostas corretas)_**

- ✅ **Comunicar um plano de ação a todos os funcionários**
- ✅ **Realizar pesquisas para descobrir o que causou a violação**
- Conter as informações para que não sejam públicas
- Supor que esse tipo de violação não ocorra novamente
- Aconselhe os funcionários a serem mais cuidadosos

---

Pergunta 8

**O que é um manual de segurança?**

- ✅ **Uma coleção de consultas ou relatórios que descrevem um processo padronizado para detecção e resposta a incidentes**
- Uma coleção de alertas de segurança, logs e dados históricos da rede
- Um guia passo a passo sobre como realizar procedimentos relacionados à TI

A tecnologia está em constante mudança, o que significa que o crime digital também está evoluindo. Novas vulnerabilidades e métodos de ataque são descobertos o tempo todo. A segurança está se tornando uma grande preocupação, à medida que mais e mais empresas terão que lidar com as consequências financeiras, legais e de reputação quando ocorrer uma violação de segurança.

No entanto, muitas empresas ainda não estão preparadas para impedir, detectar ou responder a um ataque digital. É apenas uma questão de tempo até que os invasores tentem explorar seus pontos fracos. Portanto, não é surpreendente que a demanda por profissionais de segurança digital continue a crescer.

Basta dar uma olhada nos pontos de defensor que você ganhou ao clicar no ícone de escudo no canto superior direito da tela. Suas ações ajudaram o @Apollo a se manter segura, e você demonstrou que tem as habilidades necessárias para uma carreira em segurança cibernética. Então, o que está impedindo você? Vá para o módulo final e descubra como dar o próximo passo.