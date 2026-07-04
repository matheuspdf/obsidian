# 38.0 Introdução

## 38.0.1 Por que devo fazer este módulo?

É Webster novamente! O help desk da faculdade recebe tíquetes de suporte por vários motivos. O guia de solução de problemas que Lara criou ajudará os técnicos com problemas comuns de computador e rede. Mas, às vezes, esses tíquetes de suporte resultam de malware no computador do usuário. A web tem muito a oferecer, mas os usuários devem ter cuidado porque os malfeitores sempre querem causar estragos ou lucrar com você.

Lara fez um trabalho tão bom criando o guia de solução de problemas de suporte técnico que a faculdade a designou para trabalhar em uma campanha de conscientização sobre segurança cibernética. A campanha deve educar os usuários universitários sobre as ameaças, vulnerabilidades e ataques cibernéticos comuns usados por agentes de ameaças. Também deve incluir informações sobre agentes de ameaças que usam técnicas de engenharia social para enganar os usuários, informações sobre ameaças sem fio comuns e uma explicação das ameaças aos aplicativos.

Educação é a primeira linha de defesa Se os usuários souberem das coisas ruins que podem acontecer, eles ajudarão defender a faculdade contra eles. Então, vamos nos aprofundar e aprender mais sobre essas ameaças, vulnerabilidades e ataques cibernéticos.

## 38.0.2 O que vou aprender neste módulo?

**Titulo do módulo:** Ameaças, Vulnerabilidades e Ataques de Cibersegurança

**Objetivo do módulo:** Explicar as ameaças comuns, vulnerabilidades e ataques em endpoints

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Ameaças comuns|Explicar as ameaças, as vulnerabilidades e os ataques que ocorrem nos vários domínios.|
|Disfarce|Descrever os diferentes métodos de fraude usados pelos invasores para enganar suas vítimas.|
|Ataques cibernéticos|Descrever os tipos comuns de ataques de rede.|
|Ataques a dispositivos móveis e sem fio|Descrever os tipos comuns de ataques a dispositivos móveis e sem fio.|
|Ataques a aplicativos|Descrever os tipos de ataques a aplicações.|

# 38.1 Ameaças Comuns

## 38.1.1 Domínios de Ameaça

Com as empresas enfrentando um número cada vez maior de ameaças digitais, é fundamental que elas tenham soluções de segurança robustas em vigor. Mas, para se protegerem, as empresas precisam saber quais vulnerabilidades existem em seus domínios de ameaça. Um **“domínio de ameaça**” é considerado como uma área de controle, autoridade ou proteção que os invasores podem explorar para obter acesso a um sistema.

Há muitas maneiras pelas quais os invasores podem descobrir vulnerabilidades e explorar sistemas em um domínio.

Os invasores podem explorar sistemas em um domínio com:

- Acesso direto e físico a sistemas e redes.
- Redes sem fio que vão além dos limites de uma empresa.
- Dispositivos Bluetooth ou de comunicação de campo próximo (NFC).
- Anexos de e-mail maliciosos.
- Elementos menos seguros na cadeia de fornecimento de uma empresa.
- As contas de mídia social de uma empresa.
- Mídia removível, como unidades flash.
- Aplicações em nuvem.

## 38.1.2 Tipos de ameaças cibernéticas

As ameaças digitais podem ser classificadas em categorias diferentes. Isso permite que as empresas avaliem a probabilidade de ocorrência de uma ameaça e compreendam o impacto monetário de uma ameaça para que possam priorizar seus esforços de segurança. Esta é a edição de Allan.

**Selecione os títulos para ver exemplos de ameaças digitais em cada uma dessas categorias.**

### Ataques de software

- Um ataque de negação de serviço bem-sucedido (ataque DoS).
- Um vírus de computador.

### Erros de software

- Um bug de software
- Um aplicativo que fica off-line
- um script entre sites (xss) ou compartilhamento ilegal de servidor de arquivos

### Sabotagem

- Um usuário autorizado penetra e compromete com sucesso o banco de dados primário de uma organização.
- A desfiguração do site de uma organização.

### Erro humano

- Erros de entrada de dados inadvertidos.
- Uma configuração incorreta do firewall.

### Roubo

- Laptops ou equipamentos sendo roubados de uma sala destrancada.

### Falhas de hardware

- Falhas de disco rígido

### Interrupção do utilitário

- Interrupções de energia elétrica
- Danos causados pela água resultantes da falha do sprinkler


### Desastres naturais

- Tempestades severas, como furacões ou tornados.
- Terremotos.
- Inundações.
- Incêndios.


## 38.1.3 Ameaças internas x externas

As ameaças podem se originar dentro e fora de uma empresa, com os invasores buscando acesso a informações confidenciais valiosas, como registros pessoais, propriedade intelectual e dados financeiros.

**As Ameaças Internas** são geralmente realizadas por funcionários atuais ou antigos e outros parceiros de contrato que acidentalmente ou intencionalmente manipulam dados confidenciais ou ameaçam as operações de servidores ou dispositivos de infraestrutura de rede ao conectar a mídia infectada ou acessar e-mails ou sites mal-intencionados.

A fonte de uma **ameaça externa** geralmente vem de invasores amadores ou qualificados que podem explorar vulnerabilidades em dispositivos de rede ou podem usar técnicas de engenharia social, como truques, para obter acesso aos recursos internos de uma organização.
![[Pasted image 20260703230607.png]]


## 38.1.4 Item de Prática - Origem da Ameaça

Combine o cenário com o tipo de ameaça.

|Item|Classificação|✅|
|---|---|---|
|Um funcionário conectou, sem saber, um USB infectado ao laptop de trabalho.|Ameaça interna|✅|
|Um funcionário inseriu informações erradas no banco de dados da empresa.|Ameaça interna|✅|
|Um funcionário clicou em um link de e-mail suspeito.|Ameaça interna|✅|
|Um ex-funcionário conseguiu baixar arquivos de clientes acessando remotamente a rede da empresa.|Ameaça interna|✅|

## 38.1.5 Ameaças e vulnerabilidades do usuário

Um **domínio de usuário** inclui qualquer pessoa com acesso ao sistema de informações de uma empresa, incluindo funcionários, clientes e parceiros de contrato. Os usuários são frequentemente considerados o elo mais fraco nos sistemas de segurança da informação, representando uma ameaça significativa à confidencialidade, integridade e disponibilidade dos dados de uma organização.

**Selecione os títulos para revelar mais informações sobre as ameaças de usuário mais comuns encontradas em muitas organizações.**

### Não há conscientização de segurança

Os usuários devem estar cientes e entender os dados confidenciais de uma organização, políticas e procedimentos de segurança, tecnologias e contramedidas que são implementadas para proteger as informações e os sistemas de informação.


### Políticas de segurança aplicadas incorretamente

Todos os usuários devem estar cientes e entender as políticas de segurança de uma empresa, bem como as consequências da não conformidade.


### Roubo de dados

Os dados roubados pelos usuários podem representar uma ameaça financeira significativa para as empresas, tanto em termos dos danos resultantes à sua reputação quanto da responsabilidade legal associada à divulgação de informações confidenciais.


### Downloads e mídias não autorizados

Muitas infecções e ataques de rede e dispositivos podem ser rastreados de usuários que baixaram e-mails, fotos, músicas, jogos, aplicativos e vídeos não autorizados em seus computadores, redes ou dispositivos de armazenamento. O uso de mídia não autorizada, como discos rígidos externos e unidades USB, também representa uma ameaça.


### Redes privadas virtuais não autorizadas (VPNs)

As VPNs podem ocultar o roubo de informações não autorizadas porque a criptografia normalmente usada para proteger a confidencialidade pode impedir um administrador de rede de rastrear a transmissão de dados (a menos que tenha permissão para fazê-lo).

### Sites não autorizados

O acesso a sites não autorizados pode representar um risco para os dados e dispositivos de um usuário, bem como para a própria organização. Muitas vezes, esses sites solicitam que os usuários baixem scripts ou plug-ins que contenham código malicioso ou adware. Alguns desses sites podem até assumir dispositivos de usuários, como câmeras e aplicativos.


### Destruição de sistemas, aplicativos ou dados

A destruição ou sabotagem acidental ou deliberada de sistemas, aplicativos e dados representa um sério risco para todas as organizações. Ativistas, funcionários descontentes e concorrentes do setor podem excluir dados, destruir dispositivos ou tornar dados e sistemas de informação indisponíveis.


Tenha sempre em mente que não existem soluções técnicas, controles ou contramedidas que tornem os sistemas de informação mais seguros do que os comportamentos e processos das pessoas que usam esses sistemas.


## 38.1.6 Ameaças aos Dispositivos

- Quaisquer dispositivos deixados ligados e sem supervisãorepresentam o risco de alguém obter acesso não autorizado aos recursos de rede.
- Baixar arquivos, fotos, músicas ou vídeos de fontes não confiáveis pode levar à execução de códigos maliciosos em dispositivos.
- Os criminosos digitais costumam explorar vulnerabilidades de segurança em softwares instalados nos dispositivos de uma empresa para iniciar um ataque.
- As equipes de segurança da informação de uma empresa devem tentar manter-se atualizadas com a descoberta diária de novos vírus, worms e outros malwares que representam uma ameaça para seus dispositivos.

- Os usuários que inserem unidades USB, CDs ou DVDs não autorizados correm o risco de introduzir malware ou comprometer os dados armazenados em seus dispositivos.
- As políticas estão em vigor para proteger a infraestrutura de TI de uma organização. Um usuário pode enfrentar graves consequências por violar essas políticas de propósito.
- O uso de hardware ou software desatualizado torna os sistemas e os dados de uma empresa mais vulneráveis a ataques.


## 38.1.7 Ameaças à rede local

A rede de área local (LAN) é um conjunto de dispositivos, normalmente na mesma área geográfica, conectados por cabos (com fio) ou ondas de ar (sem fio).

Como os usuários podem acessar os sistemas, aplicativos e dados de uma organização a partir do **Domínio da LAN,** é fundamental que ela tenha uma segurança forte e controles de acesso rigorosos.

**Exemplos de ameaças à LAN:**

- Acesso não autorizado a armários de cabeamento, data centers e salas de computadores
- Acesso não autorizado a sistemas, aplicações e dados
- Vulnerabilidades do Sistema operacional de rede ou software e atualizações
- Usuários falsos acesso não autorizado a redes sem fio
- Explorações de dados em trânsito
- Ter servidores LAN com hardware ou sistemas operacionais diferentes dificulta o gerenciamento e a solução de problemas
- Detecção de rede não autorizada e varredura de porta
- Firewalls mal configurados

## 38.1.8 Ameaças à nuvem privada

O **domínio da nuvem** privada inclui servidores privados, recursos e infraestrutura de TI disponíveis para membros de uma única organização por meio da Internet. Embora muitas empresas achem que seus dados estão mais seguros em uma nuvem privada, esse domínio ainda apresenta ameaças significativas à segurança, incluindo:

- Detecção de rede não autorizada e varredura de porta
- Acesso não autorizado a recursos
- Vulnerabilidades no sistema operacional ou software de roteadores, firewalls ou dispositivos de rede
- Erros de configuração em roteadores,firewalls ou dispositivos de rede
- Usuários remotos acessando a infraestrutura de uma organização e baixando dados confidenciais

## 38.1.9 Ameaças à nuvem pública

Como um domínio de nuvem privada hospeda recursos de computação para uma única organização, o **domínio de nuvem pública é a** totalidade dos serviços de computação hospedados por uma nuvem, serviço ou provedor de Internet que estão disponíveis ao público e compartilhados entre as organizações.

Existem três modelos de serviços de nuvem pública que as empresas podem optar por usar.

**Selecione as setas para saber mais sobre os serviços de nuvem pública.**

### **Software como Serviço (SaaS)**

Este é um modelo baseado em assinatura que fornece às organizações um software hospedado centralmente e acessado pelos usuários por meio de um navegador da Web, aplicativo ou outro software. Em outras palavras, trata-se de um software que não é armazenado localmente, mas executado na nuvem.

### **Plataforma como um Serviço (PaaS)**

Este modelo baseado em assinatura fornece uma plataforma que permite que uma organização desenvolva, execute e gerencie seus aplicativos no hardware do serviço, usando ferramentas que o serviço fornece. Essa plataforma é acessada pela nuvem pública.

### **Infraestrutura como Serviço (IaaS)**

Esse modelo baseado em assinatura fornece recursos de computação virtual, como hardware, software, servidores, armazenamento e outros componentes de infraestrutura pela Internet. Uma organização comprará acesso a esta infraestrutura e os usará por meio da nuvem pública.

## 38.1.10 Ameaças aos Aplicativos

O **domínio do aplicativo inclui** todos os sistemas, aplicativos e dados críticos usados por uma organização para dar suporte às operações. Cada vez mais, as organizações estão movendo aplicativos como e-mail, monitoramento de segurança e gerenciamento de banco de dados para a nuvem pública.

As ameaças comuns aos aplicativos incluem:

- Alguém obtendo acesso não autorizado a data centers, salas de computadores, armários de fiação ou sistemas
- Tempo de inatividade do servidor durante períodos de manutenção
- Vulnerabilidades de software do sistema operacional de rede
- Perda de dados
- Vulnerabilidades de desenvolvimento de aplicativos cliente-servidor ou web

Faça a correspondência entre a descrição e termo correto.

|Categoria|Resposta correta|
|---|---|
|Dentro do escritório corporativo, os funcionários trabalham usando um desktop, laptop, tablet ou smartphone.|Domínio do dispositivo|
|Os clientes da corporação têm acesso a um conjunto de módulos de eLearning fornecidos por uma taxa de assinatura.|Provedor de SaaS|
|A corporação contrata funcionários.|Domínio do usuário|
|No escritório corporativo, os funcionários se conectam à rede.|Domínio da LAN|
|O provedor dos módulos de eLearning usa um serviço de nuvem para hospedar os módulos.|Domínio da nuvem pública|
|Os funcionários obtêm acesso ao escritório corporativo usando um cartão de identificação eletrônico.|Domínio de instalações físicas|

## 38.1.12 Complexidade da Ameaça

  

- **Ameaça persistente avançada (APT)** um ataque contínuo que utiliza táticas elaboradas de espionagem envolvendo múltiplos agentes e malware sofisticado.  
    Os invasores permanecem indetectáveis por um longo período de tempo, com consequências potencialmente devastadoras. Os APTs normalmente visam governos e organizações de alto nível e geralmente são bem orquestrados e bem financiados.

- Como o nome sugere, **os ataques de algoritmos** aproveitam os algoritmos em um software legítimo para gerar comportamentos não desejados. Por exemplo, algoritmos usados para rastrear e relatar quanta energia um computador consome podem ser usados para selecionar alvos ou acionar alertas falsos. Eles também podem desabilitar um computador forçando-o a usar toda a sua RAM ou sobrecarregando sua unidade central de processamento (CPU).


## 38.1.13 Backdoors e Rootkits

Os cibercriminosos também usam muitos tipos diferentes de software malicioso (conhecido como malware) para realizar seus ataques.

Programas de backdoor, como Netbus e Back Orifice, são usados por criminosos digitais para obter acesso não autorizado a um sistema ignorando os procedimentos normais de autenticação.

Os cibercriminosos normalmente têm usuários autorizados, sem que você saiba, executando um programa de ferramenta administrativa remota (RAT) em seu computador que instala um backdoor. O backdoor dá ao criminoso controle administrativo sobre um computador de destino. Backdoors concedem aos cibercriminosos acesso contínuo a um sistema, mesmo que a organização tenha corrigido a vulnerabilidade original usada para atacar o sistema.

Esse malware foi projetado para modificar o sistema operacional para criar um backdoor, que os invasores podem usar para acessar o computador remotamente.

A maioria dos rootkits utiliza as vulnerabilidades do software para escalonar privilégios e modificar arquivos de sistema.

Os Rootkits também podem modificar as ferramentas forenses e de monitoramento do sistema, tornando-os muito difíceis de detectar. Na maioria dos casos, um computador infectado por um rootkit precisa ser apagado e qualquer software necessário reinstalado.


## 38.1.14 Inteligência de ameaças e fontes de pesquisa

O United States Computer Emergency Readiness Team (US-CERT) e o Departamento de Segurança Interna dos EUA patrocinam um banco de dados de **vulnerabilidades e exposições comuns (CVE)**. Esses CVEs foram amplamente adotados como uma forma de descrever e fazer referência a vulnerabilidades conhecidas.

Cada entrada do CVE contém um número de identificador padrão, uma breve descrição da vulnerabilidade de segurança e todas as referências importantes aos relatórios de vulnerabilidade relacionados. A lista CVE é mantida por uma organização sem fins lucrativos, a MITRE Corporation, em seu site público.

**Selecione as setas para saber mais sobre algumas outras fontes de inteligência de ameaças.**

### **a Web obscura**

Isso se refere ao conteúdo da Web criptografado que não é indexado pelos mecanismos de pesquisa convencionais e requer software, autorização ou configurações específicas para acesso. Pesquisadores especialistas monitoram a Web obscura em busca de uma nova inteligência de ameaças.

### **Indicador de comprometimento (IOC)**

IOCs, como assinaturas de malware ou nomes de domínio, fornecem evidências de violações de segurança e detalhes sobre elas.

### **Compartilhamento Automatizado de Indicadores (AIS)**

Compartilhamento Automatizado de Indicadores (AIS): capacidade da Agência de Segurança Cibernética e de Infraestrutura (CISA) que permite a troca em tempo real de indicadores de ameaças cibernéticas usando uma linguagem padronizada e estruturada. Structured Threat Information Expression (STIX) e Trusted Automated Exchange of Intelligence Information (TAXII) são padrões usados em AIS.


## 38.1.15 Verifique sua compreensão - Ameaças comuns

Combine o termo de segurança cibernética com a respectiva descrição.

