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

|Categoria|Resposta correta|
|---|---|
|ataque backdoor|Este é um tipo de ataque de malware usado por cibercriminosos para obter acesso não autorizado a sistemas, ignorando os procedimentos normais de autenticação, geralmente fazendo com que usuários autorizados executem, sem saber, um programa de ferramenta administrativa remota (RAT) em seus computadores que instala um backdoor.|
|ataque de rootkit|Este é um tipo de ataque de malware projetado para modificar o sistema operacional para criar uma vulnerabilidade que os invasores podem usar para acessar o computador remotamente e obter acesso a recursos que normalmente não deveriam estar acessíveis (escalonamento de privilégios) e modificar arquivos do sistema.|
|ataque de algoritmo|Este é um tipo de ataque de malware que gera informações incorporadas em um software legítimo para gerar comportamentos não intencionais. Esse tipo de ataque de malware pode ser usado para selecionar alvos ou disparar alertas falsos. Eles também podem desabilitar um computador forçando-o a usar toda a sua RAM ou sobrecarregando sua unidade central de processamento (CPU).|
|Ameaças persistentes avançadas|Este é um tipo de ataque de malware que é contínuo e usa táticas de espionagem elaboradas envolvendo vários atores e/ou malware sofisticado para obter acesso à rede do sistema de destino. Normalmente é direcionado a governos e organizações de alto nível e geralmente é bem orquestrado e bem financiado.|
# 38.2 Disfarce

## 38.2.1 Engenharia Social

A engenharia social é uma estratégia não técnica que tenta manipular indivíduos para realizar ações específicas ou divulgar informações confidenciais.

Em vez de vulnerabilidades de software ou hardware, a engenharia social explora a natureza humana, aproveitando a disposição das pessoas em ajudar ou se aproveitando de suas fraquezas, como ganância ou vaidade.

**Selecione as setas para descobrir mais sobre alguns tipos comuns de ataques de engenharia social.**

### **Pretexting (pré-dialogo)**

Esse tipo de ataque ocorre quando um indivíduo mente para obter acesso a dados privilegiados. Por exemplo, um invasor finge precisar de dados pessoais ou financeiros para confirmar a identidade de uma pessoa.

### **Algo por algo (Quid pro quo)**

Os ataques de contrapartida envolvem uma solicitação de informações pessoais em troca de algo, como um presente. Por exemplo, um e-mail mal-intencionado pode solicitar que você forneça seus dados pessoais confidenciais em troca de férias gratuitas.

### **Fraude de identidade**

É o uso da identidade roubada de uma pessoa para obter bens ou serviços por meio de engano. Por exemplo, alguém adquire suas informações pessoais e tenta solicitar um cartão de crédito em seu nome.

## 38.2.2 Táticas de Engenharia Social

Os criminosos digitais dependem de várias táticas de engenharia social para obter acesso a informações confidenciais.

**Selecione os títulos para descobrir o que são.**

### Autoridade

Os invasores atacam o fato de que as pessoas são mais propensas a obedecer quando instruídas por alguém que consideram uma figura de autoridade.

Por exemplo, um executivo abre o que parece ser um anexo de intimação oficial, mas na verdade é um PDF infectado.

### Intimidação

Os criminosos cibernéticos muitas vezes obrigam uma vítima a agir que compromete a segurança.

A secretária de um executivo recebe um telefonema informando que seu chefe está prestes a fazer uma apresentação importante, mas seus arquivos estão corrompidos. O criminoso ao telefone alega que é culpa da secretária e pressiona a secretária a enviar os arquivos imediatamente ou corre o risco de ser demitida.

### Consenso

Frequentemente chamados de "prova social", os ataques de consenso funcionam porque as pessoas tendem a agir da mesma forma que as outras pessoas à sua volta, pensando que algo deve estar certo se os outros estiverem fazendo isso.

Por exemplo, os cibercriminosos podem publicar uma postagem em mídia social sobre uma falsa oportunidade de negócios e fazer com que dezenas de contas legítimas ou ilegítimas comentem sobre sua validade. Isso encoraja vítimas inocentes a fazer uma compra.

### Escassez

Uma tática de marketing bem conhecida, os ataques de escassez funcionam porque os invasores sabem que as pessoas tendem a agir quando acham que há uma quantidade limitada de algo disponível.

Por exemplo, alguém recebe um e-mail sobre um item de luxo que está sendo vendido por muito pouco dinheiro, mas ele afirma que há apenas um punhado disponível a esse preço, em um esforço para estimular a vítima desavisada a agir. Isso pode estimular a vítima desavisada a agir impulsivamente.

### Urgência

Da mesma forma, as pessoas também tendem a agir quando pensam que há um tempo limitado para isso.

Por exemplo, os criminosos digitais promovem uma oferta falsa de envio por tempo limitado para tentar levar as vítimas a agir rapidamente.

### Familiaridade

As pessoas são mais propensas a fazer o que outra pessoa pede se gostarem dela.

Portanto, os invasores geralmente tentam estabelecer um relacionamento com a vítima para estabelecer um relacionamento. Em outros casos, eles podem clonar o perfil de mídia de um amigo seu para que você pense que está falando com ele.


### Confiança

Construir confiança em um relacionamento com a vítima pode exigir mais tempo para se estabelecer.

Por exemplo, um criminoso cibernético disfarçado de especialista em segurança liga para a vítima desavisada para oferecer consultoria. Ao ajudar a vítima, o “especialista em segurança” descobre um “erro grave” que precisa de atenção imediata. A solução oferece ao criminoso digital a oportunidade de violar a segurança da vítima.


## 38.2.3 Item de Prática - Cenário de Engenharia Social

Você está investigando um e-mail suspeito que foi enviado a um funcionário que trabalha remotamente Parece que o e-mail foi enviado pelo administrador, pedindo aos funcionários que cliquem em um link para baixar uma rede privada virtual que protegerá a conexão Wi-Fi durante o trabalho em casa. Embora o e-mail pareça legítimo, clicar no link instala malware no dispositivo do funcionário. Que tipo de ataque de engenharia social está sendo usado aqui?

**Qual engenharia social ocorre quando alguém mente para obter acesso a dados privilegiados?**

- [ ] Fraude de identidade
- [ ] Quid pro quo
- [x] Pretexting (pré-dialogo)
- [ ] Phishing

Está certo.

- O pretexto ocorre quando um indivíduo mente para obter acesso a dados privilegiados.
- Quid pro quo descreve um ataque que envolve uma solicitação de informações em troca de algo, como um presente.
- A fraude de identidade usa a identidade roubada de uma pessoa para obter dados, bens ou serviços por meio de engano.
- Phishing é um cibercrime no qual um alvo ou alvos são contatados por e-mail, telefone ou mensagem de texto por alguém que se faz passar por uma instituição legítima para induzir indivíduos a fornecer dados confidenciais, como informações de identificação pessoal, dados bancários e de cartão de crédito e senhas.

## 38.2.4 Shoulder Surfing e Dumpster Diving (Busca de informações na Lixeira)

  

O **Shoulder Surfing** é um ataque simples que envolve observar ou literalmente olhar por cima do ombro de um alvo para obter informações valiosas, como PINs, códigos de acesso ou detalhes de cartão de crédito. Os criminosos nem sempre precisam estar perto de suas vítimas para escapar da onda - eles podem usar binóculos ou câmeras de segurança para obter essas informações.

Esta é uma razão pela qual uma tela de caixa eletrônico só pode ser vista em determinados ângulos. Esses tipos de proteções dificultam muito o Shoulder Surfing.

Você já deve ter ouvido falar da frase: "O lixo de um homem é o tesouro de outro homem". Em nenhum lugar isso é mais verdadeiro do que no mundo do **dumpster diving (mergulho em lixeiras)** – o processo de examinar o lixo de um alvo para ver quais informações foram descartadas. 

É por isso que os documentos que contêm informações confidenciais devem ser triturados ou armazenados em sacos de queima até que possam ser destruídos.


## 38.2.5 Falsificação de identidade e boatos

Os criminosos digitais têm muitas outras técnicas de dissimulação para ajudá-los a obter sucesso.

**Selecione as imagens para saber mais.**

**Representação**

A personificação é o ato de fingir ser outra pessoa para induzir alguém a fazer algo que normalmente não faria. Por exemplo, um cibercriminoso se passando por um funcionário da Receita recentemente atacou os contribuintes, dizendo às vítimas que eles deviam dinheiro que deveria ser pago imediatamente por meio de transferência eletrônica - ou correria o risco de ser preso.

Os criminosos também usam a representação para atacar os outros. Por exemplo, eles podem se passar por suas vítimas on-line e publicar em sites ou páginas de mídia social para minar a credibilidade da vítima.

**Farsas**

Um hoax é um ato destinado a enganar ou enganar alguém. Os hoaxes podem causar tanta interrupção quanto uma violação de segurança real.

Por exemplo, uma mensagem que avisa sobre uma ameaça de vírus (inexistente) em um dispositivo e pede que o destinatário compartilhe essas informações com todos que eles conhecem. Esse hoax provoca uma reação do usuário, criando medo desnecessário e comportamento irracional que é perpetuado por e-mail e mídias sociais.



## 38.2.6 Pegadinhas (Piggybacking) e utilização não autorizada (Tailgating)

Piggybacking ou Tailgating ocorre quando um criminoso segue uma pessoa autorizada para obter entrada física em um local seguro ou em uma área restrita. Os criminosos podem conseguir isso:

- Dar a impressão de ser escoltado para a instalação por uma pessoa autorizada.
- Juntar-se e fingir ser parte de uma grande multidão que entra na instalação.
- Visar uma pessoa autorizada que não tem cuidado com as regras da instalação.

Uma maneira de evitar isso é usar dois conjuntos de portas. Isso às vezes é chamado de mantrap e significa que os indivíduos entram por uma porta externa, que deve fechar antes que eles possam ter acesso através de uma porta interna.


## 38.2.7 Outros métodos de fraude

Esteja ciente de que os invasores têm muito mais truques na manga para enganar suas vítimas.

**Selecione os títulos para saber mais sobre alguns desses métodos.**

### Fraude da fatura

As faturas falsas são enviadas com o objetivo de receber dinheiro de uma vítima solicitando que ela coloque suas credenciais em uma tela de login falsa. A fatura falsa também pode incluir linguagem urgente ou ameaçadora.

### Ataque do regador

Um ataque watering hole (poço de água) descreve uma exploração na qual um invasor observa ou adivinha quais sites uma empresa usa com mais frequência e infecta um ou mais deles com malware.

### Typosquatting

Esse tipo de ataque depende de erros comuns, como erros de digitação cometidos por indivíduos ao inserir um endereço de site em seu navegador. A URL incorreta levará os indivíduos a um site legítimo de propriedade do invasor, cujo objetivo é coletar informações pessoais ou financeiras.


### Adendo

Os invasores podem remover a tag de e-mail “externa” usada pelas empresas para avisar o destinatário de que uma origem externa é originada de um e-mail. Isso leva as pessoas a acreditarem que um e-mail mal-intencionado foi enviado de dentro da empresa.

### Influenciar campanhas

Frequentemente usadas em guerra cibernética, as campanhas de influência são geralmente muito bem coordenadas e combinam vários métodos, como notícias falsas, campanhas de desinformação e publicações em mídias sociais.

## 38.2.8 Verifique sua compreensão - Ataques de engenharia social

Corresponda o termo com a descrição apropriada.

|Categoria|Resposta correta|
|---|---|
|Personificação|Um amigo envia uma mensagem de texto para parabenizá-lo por sua nova posição depois de ver sua atualização de status no seu perfil social. Você ainda precisa atualizar essas informações.|
|Tailgating|Um colega lhe conta que um homem lhes pediu para segurar a porta da frente no caminho para o escritório esta manhã, porque ele havia esquecido sua carteira de identidade. Seu colega nunca tinha visto esse homem antes.|
|Typosquatting|Um cliente relatou que o malware infectou seu computador depois que ele visitou um site. Investigação mais aprofundada revelou que o cliente acidentalmente digitou incorretamente o endereço do site.|

## 38.2.9 Defendendo-se contra fraudes

As organizações precisam promover a conscientização sobre as táticas de engenharia social e educar adequadamente os funcionários sobre as medidas de prevenção. Aqui estão algumas dicas importantes.

- Nunca divulgue informações confidenciais ou credenciais por e-mail, chat, mensagens de texto, pessoalmente ou por telefone para partes desconhecidas.
- Resista ao desejo de clicar em e-mails atraentes e links da web.
- Desconfie de downloads não iniciados ou automáticos.
- Estabelecer e educar os funcionários sobre as principais políticas de segurança.
- Incentive os funcionários a assumirem responsabilidade pelos problemas de segurança.
- Não se submeter à pressão de pessoas desconhecidas.



## 38.2.10 Vídeo - Técnicas de Exploração de Engenharia Social

Pressione o botao Play para assistir o vídeo.

Este vídeo é uma visão geral do laboratório para técnicas de engenharia social. Este laboratório requer um PC ou algum outro dispositivo com acesso à Internet.

Nem todos os ataques de segurança cibernética vêm de algum invasor aleatório que está invadindo uma rede de um computador que está a milhares de quilômetros de distância. Muitas vezes, os invasores roubam informações pessoais ou organizacionais que adquiriram ao fazer com que alguém lhes concedesse acesso sem saber. Isso é chamado de engenharia social, e isso acontece com mais frequência do que você imagina.

Estes são os objetivos deste laboratório. Na primeira parte, você aprenderá sobre os diferentes tipos de técnicas de engenharia social que são usadas para obter acesso a dados pessoais ou organizacionais. Você verá uma lição interativa sobre engenharia social e responderá perguntas.

Na parte dois, você criará um pôster de conscientização sobre segurança cibernética para incentivar os outros a estarem cientes de ataques de engenharia social.

Esperamos que você goste deste laboratório.


## 38.2.11 Laboratório - Técnicas de Exploração de Engenharia Social

Neste laboratório, você completará os seguintes objetivos:

- Parte 1: Técnicas de Exploração de Engenharia Social
- Parte 2: Crie um pôster de conscientização sobre segurança cibernética

# 38.3 Ataques cibernéticos

## 38.3.1 Malware

Os cibercriminosos usam muitos tipos diferentes de software malicioso, ou malware, para realizar ataques. Malware é qualquer código que pode ser usado para roubar dados, contornar o espaço no-break do controle de acesso ou causar danos, ou comprometer um sistema.

**Selecione os ícones de alfinete para saber mais sobre três dos tipos mais comuns de malware.**

### Vírus

Um vírus é um tipo de programa de computador que, quando executado, se replica e se anexa a outros arquivos, como um programa legítimo, inserindo nele seu próprio código. Alguns vírus são inofensivos, mas outros podem ser destrutivos, como aqueles que modificam ou excluem dados. A maioria dos vírus requer interação do usuário final para iniciar a ativação e pode ser escrito para atuar em uma data ou hora específica.

Os vírus podem se espalhar através de mídia removível, como unidades flash USB, downloads da Internet e anexos de e-mail. O simples ato de abrir um arquivo ou executar um programa específico pode desencadear um vírus. Quando um vírus está ativo, ele geralmente infecta outros programas no computador ou outros computadores na rede. Os vírus sofrem mutações para evitar a detecção.

Por exemplo, o vírus Melissa foi lançado em 1999 e disseminado por e-mail, afetando dezenas de milhares de usuários e causando danos estimados em US $1,2 bilhão.

### Worms
Um worm é um programa de software malicioso que se replica explorando independentemente vulnerabilidades nas redes. Ao contrário de um vírus, que requer um programa host para ser executado, os worms podem ser executados por si próprios. Além da infecção inicial do host, eles não exigem a participação do usuário e podem se espalhar muito rapidamente pela rede, geralmente diminuindo a velocidade.

Os worms compartilham padrões semelhantes: Eles exploram vulnerabilidades do sistema, têm uma maneira de se propagar e todos contêm código malicioso (carga útil) para causar danos a sistemas ou redes de computadores.

Os worms são responsáveis por alguns dos ataques mais devastadores da Internet. Em 2001, o worm Code Red infectou mais de 300.000 servidores em apenas 19 horas.


### Cavalo de Troia
Um Trojan (Cavalo de Troia) é um malware que realiza operações maliciosas mascarando sua verdadeira intenção. Pode parecer legítimo, mas é, de fato, muito perigoso. Trojans (Cavalos de Troia) exploram os privilégios do usuário que os executa.

Ao contrário dos vírus, os trojans (Cavalos de Troia) não se replicam automaticamente, mas geralmente se ligam a arquivos não executáveis, como arquivos de imagem, áudio ou vídeo, que atuam como um chamariz para prejudicar os sistemas de usuários desavisados.

## 38.3.2 Bombas Lógicas

Uma bomba lógica é um programa malicioso que espera por um gatilho, como uma data especificada ou entrada de banco de dados, para detonar o código malicioso. Até que este evento de disparo aconteça, a bomba lógica permanecerá inativa.

Uma vez ativada, uma bomba lógica implementa um código malicioso que causa danos a um computador de várias maneiras. Ela pode sabotar registros de banco de dados, apagar arquivos e atacar sistemas operacionais ou aplicativos. 

Especialistas em segurança cibernética descobriram recentemente bombas lógicas que atacam e destroem os componentes de hardware em um dispositivo ou servidor, incluindo ventiladores, unidade central de processamento (CPU), memória, discos rígidos e fontes de alimentação. A bomba lógica sobrecarrega esses componentes até que eles superaqueçam ou falhem.

## 38.3.3 Ransomware

Malware projetado para manter um sistema de computador, ou os dados incluídos nele, presos até que o pagamento seja feito.

O ransomware geralmente funciona criptografando os dados para que você não possa acessá-los. Conforme as reividicações do ransomware, assim que o resgate for pago por meio de um sistema de pagamento não rastreável, o cibercriminoso fornecerá um programa que descriptografa os arquivos ou envia um código de desbloqueio. Na realidade, muitas vítimas não têm acesso aos seus dados mesmo após terem pago. 

Algumas versões de ransomware podem tirar proveito de vulnerabilidades específicas do sistema. O ransomware é frequentemente disseminado por e-mails de phishing que o incentivam a baixar um anexo mal-intencionado ou uma vulnerabilidade de software.

## 38.3.4 Ataques de negação de serviço
Os ataques de negação de serviço (DoS) são um tipo de ataque de rede que é relativamente simples de realizar, mesmo por um invasor não qualificado. Esses ataques são um grande risco, pois geralmente resultam em algum tipo de interrupção dos serviços de rede, causando uma perda significativa de tempo e dinheiro. Mesmo as tecnologias operacionais, que consistem em hardware ou software que controla dispositivos ou processos físicos em edifícios, fábricas ou fornecedores de serviços públicos, são vulneráveis a ataques DoS, que podem causar o desligamento do sistema em circunstâncias extremas.

Selecione as imagens para descobrir mais sobre os dois principais tipos de ataques de DoS.

**Quantidade esmagadora de tráfego**

Quando uma rede, host ou aplicativo recebe uma enorme quantidade de dados a uma taxa que não consegue processar. Isso causa uma desaceleração na transmissão ou resposta ou uma falha em um dispositivo ou serviço.

**Pacotes maliciosamente formatados**

Um pacote é uma coleção de dados que flui entre uma origem e um computador destino ou aplicação através de uma rede, como a Internet. Quando um pacote formatado de forma mal-intencionada é enviado, o receptor não será capaz de tratá-lo.

Por exemplo, se um invasor encaminhar pacotes contendo erros ou pacotes formatados incorretamente que não podem ser identificados por um aplicativo, isso fará com que o dispositivo receptor funcione muito lentamente ou falhe.


## 38.3.5 Sistema de nomes de domínio
Há muitos serviços técnicos essenciais necessários para uma rede operar, como roteamento, endereçamento e nomes de domínio. Esses são os principais alvos de ataques.

Selecione os títulos para descobrir como os criminosos digitais podem aproveitar as vulnerabilidades nesses serviços.

### Reputação de domínio

O sistema de nome de domínio (DNS) é usado por servidores DNS para converter um nome de domínio, como www.cisco.com, em um endereço IP numérico para que os computadores possam entendê-lo. Se um servidor DNS não sabe o endereço IP, ele perguntará a outro servidor DNS.

Uma empresa precisa monitorar sua reputação de domínio, incluindo seu endereço IP, para ajudar a proteger contra domínios externos mal-intencionados. A reputação do domínio é usada para classificar e-mails como spam ou possíveis ameaças à segurança.

### DNS spoofing

A falsificação de DNS ou o envenenamento de cache DNS é um ataque no qual dados falsos são introduzidos em um cache de resolvedor de DNS - o banco de dados temporário no sistema operacional de um computador que registra visitas recentes a sites e outros domínios da Internet.

Esses ataques exploram uma fraqueza no software de cache DNS que faz com que os servidores DNS redirecionem o tráfego de um domínio legítimo para o endereço IP de um servidor ilícito.


### Sequestro de domínio

Quando um invasor obtém, por engano, o controle das informações de DNS de um alvo, ele pode fazer alterações não autorizadas. Isso é conhecido como sequestro de domínio.

A maneira mais comum de sequestrar um nome de domínio é alterar o endereço de e-mail de contato do administrador por meio de engenharia social ou invadir a conta de e-mail do administrador. O endereço de e-mail do administrador pode ser facilmente encontrado pelo registro WHOIS do domínio, que é de registro público.


### Redirecionamento de URL (Localizador Uniforme de Recursos)

Um localizador uniforme de recursos (URL) é um identificador exclusivo para encontrar um recurso específico na Internet. O redirecionamento de uma URL geralmente acontece para fins legítimos.

Por exemplo, você se conectou a um portal de eLearning para iniciar este curso do Cybersecurity Essentials. Se você sair do portal e retornar a ele outra vez, o portal o redirecionará de volta para a página de login. 

É esse tipo de funcionalidade que os invasores podem explorar. Em vez de direcioná-lo para a página de login do eLearning, ele pode redirecioná-lo para um site mal-intencionado. 

## 38.3.6 Ataques de Camada 2

A camada 2 refere-se à camada de link de dados no modelo de comunicação de dados Open Systems Interconnection (OSI).

Essa camada é usada para mover dados por uma rede física vinculada. Os endereços IP são mapeados para cada endereço de dispositivo físico (também conhecido como endereço de controle de acesso de mídia (MAC)) na rede, usando um procedimento chamado protocolo de resolução de endereço (ARP). 

Em seus termos mais simples, o endereço MAC identifica o destinatário de um endereço IP enviado pela rede, e o ARP resolve endereços IP para endereços MAC para transmissão de dados. 

Os invasores geralmente aproveitam as vulnerabilidades nessa segurança de camada 2.

Role para baixo para descobrir alguns exemplos.

### Spoofing
Spoofing é um ataque de representação e tira proveito de uma relação de confiança entre os dois sistemas.

A falsificação de endereço MAC ocorre quando um invasor disfarça seu dispositivo como um dispositivo válido na rede e, portanto, pode ignorar o processo de autenticação. 
O ARP spoofing envia mensagens ARP falsificadas através de uma LAN. Isso vincula o endereço MAC de um invasor ao endereço IP de um dispositivo autorizado na rede.
A falsificação de IP envia pacotes IP de um endereço de origem falsificado para disfarçar a origem do pacote.

### Inundação de MAC
Os dispositivos em uma rede são conectados por um switch de rede usando o switching de pacote para receber e encaminhar dados para o dispositivo de destino. A inundação de MAC compromete os dados transmitidos para um dispositivo. Um invasor inunda a rede com endereços MAC falsos, comprometendo a segurança do switch de rede.


## 38.3.7 Item de prática - Tipo de Ataque
Vários funcionários relataram problemas de desempenho em seus computadores, com aplicativos executando anúncios pop-up lentos e notáveis. Como parte da investigação, uma ferramenta de monitoramento de rede é consultada, revelando tráfego anormal na web. Com base nas descobertas, que tipo de ataque está afetando a corporação?

- [ ] Ataques de DNS
- [ ] ataque de DoS
- [x] Ataque DDoS
- [ ] Ataques da camada 2

Está certo.

Um ataque de DoS causa a interrupção de uma rede conectada à Internet, sobrecarregando-a com dados ou pacotes mal-intencionados. Um ataque de DDoS é semelhante, mas origina-se de um botnet de hosts infectados chamados zumbis. Quando está pronto, o hacker instrui os sistemas controladores para fazer com que o botnet de zumbis execute um ataque de negação de serviço distribuído (DDoS). Os ataques de camada 2 visam a camada de enlace de dados que é usada para mover dados através de uma rede física vinculada ignorando protocolos de autenticação. Os ataques de DNS visam a vulnerabilidades no sistema de nome de domínio que faz com que ele se comporte de forma inesperada.

## 38.3.8 Man-in-the-Middle e Ataques Man-in-the-Mobile
Os invasores podem interceptar ou modificar as comunicações entre dois dispositivos para roubar informações ou se passar por um dos dispositivos.

Selecione as imagens para saber mais sobre esses tipos de ataques.

**Man-in-the-Middle (MitM)**

Um ataque MitM, também conhecido como ataque no caminho, ocorre quando um cibercriminoso assume o controle de um dispositivo intermediário sem o conhecimento do usuário. Com esse nível de acesso, um invasor pode interceptar, manipular e retransmitir informações falsas entre o remetente e o destino pretendido.

**Man-in-the-Mobile (MitMo)**

Uma variação do man-in-the-middle, o MitMo é um tipo de ataque usado para assumir o controle do dispositivo móvel de um usuário. Quando infectado, o dispositivo móvel é instruído a capturar informações confidenciais do usuário e enviá-las aos invasores.

O ZeuS é um exemplo de pacote de malware com recursos MitMo. Ele permite que os invasores capturem silenciosamente as mensagens SMS de verificação em duas etapas enviadas aos usuários.

## 38.3.9 Ataques de dia zero
Um ataque de dia zero ou ameaça de dia zero explora vulnerabilidades de software antes que elas se tornem conhecidas, ou antes de serem divulgadas pelo fornecedor do software.

Uma rede é extremamente vulnerável a ataques entre o momento em que um exploit é descoberto (zero hora) e o tempo que leva para o fornecedor do software desenvolver e lançar um patch que corrija esse exploit.

A defesa contra esses ataques rápidos exige que os profissionais de segurança de rede adotem uma visão mais sofisticada e holística de qualquer arquitetura de rede.

## 38.3.10 Registro de teclado

Como o nome sugere, o registro de teclado ou o registro de teclas refere-se à gravação ou ao registro de cada tecla pressionada no teclado de um computador.

Os cibercriminosos registram as teclas digitadas por meio de software instalado em um sistema de computador ou por meio de dispositivos de hardware conectados fisicamente a um computador. O software keylogger envia o arquivo de log para o criminoso. Por ter registrado todas as teclas pressionadas, esse arquivo de registro pode revelar nomes de usuário, senhas, sites visitados e outras informações confidenciais.

Muitos pacotes anti-spyware podem detectar e remover keyloggers não autorizados.


## 38.3.11 Confirme seus detalhes
Um funcionário acaba de receber um e-mail do departamento de RH solicitando os detalhes da conta bancária do funcionário, clicando em um link no e-mail. Ressalta que isso deve ser concluído até o final do dia para que o empregado seja incluído na folha de pagamento deste mês. Embora o e-mail pareça ter sido enviado internamente, uma inspeção mais detalhada revela uma pequena variação no domínio de e-mail do endereço do remetente. Que tipo de ataque é esse?

- [ ] Cavalo de Troia
- [x] Representação
- [ ] Man-in-the-middle
- [ ] Invasão de domínio

Está certo.

A personificação (Impersonation) é enganar alguém para divulgar suas informações pessoais fingindo ser outra pessoa. Um ataque man-in-the-middle acontece quando um criminoso digital assume o controle de um dispositivo sem o conhecimento do alvo para interceptar, manipular e transmitir informações falsas entre eles e o destino pretendido. O sequestro de domínio (Domain hijacking) descreve um invasor que obtém controle indevidamente e faz alterações não autorizadas nas informações de DNS de um alvo. Um Cavalo de Troia é um malware que se liga a arquivos não executáveis, como arquivos de imagem, áudio ou vídeo, agindo como uma isca para prejudicar os sistemas de usuários desavisados.


## 38.3.12 Defesa contra ataques

As organizações podem tomar várias medidas para se defender contra vários ataques. Estes incluem o seguinte:

Configure firewalls para remover quaisquer pacotes de fora da rede que tenham endereços indicando que eles se originaram de dentro da rede. 
Verifique se as correções e atualizações estão atualizadas.
Distribua cargas de trabalho em vários sistemas de servidor.
Os dispositivos de rede usam pacotes do Internet Control Message Protocol (ICMP) para enviar mensagens de erro e controle, como se um dispositivo pode ou não se comunicar com outro na rede. Para evitar ataques de DoS e DDoS, as empresas podem bloquear pacotes externos de ICMP com seus firewalls.


## 38.3.13 Verifique sua compreensão - Ataques cibernéticos

**Pergunta 1**
Combine o termo de segurança cibernética com a respectiva descrição.

|Categoria|Resposta correta|
|---|---|
|Ataques de Cavalo de Troia|Este é um malware que realiza operações maliciosas mascarando sua verdadeira intenção.|
|Ataque de ransomware|Este é um malware projetado para manter um sistema de computador ou os dados que ele contém cativos por meio de criptografia, até que um pagamento seja feito.|
|Ataques de Sequestro de domínio (Domain hijacking)|É quando um invasor obtém indevidamente o controle das informações de DNS de um alvo para que possam fazer alterações não autorizadas nelas.|
|Ataques de dia zero|Esse tipo de ataque explora vulnerabilidades de software antes que elas se tornem conhecidas ou antes de serem divulgadas pelo fornecedor do software.|
|Ataques de Negação de Serviços|Quando uma rede, host ou aplicativo recebe uma enorme quantidade de dados a uma taxa que não consegue processar. Isso causa uma desaceleração na transmissão ou resposta ou uma falha em um dispositivo ou serviço.|
|ataques de bombas lógicas|Uma bomba lógica é um programa malicioso que espera por um gatilho, como uma data especificada ou entrada de banco de dados, para detonar o código malicioso.|

**Pergunta 2**

Verdadeiro ou falso: Ataques DoS e DDoS podem ser mitigados pelas empresas através do bloqueio de pacotes ICMP externos com firewalls.

- [x] Verdadeiro
- [ ] Falso

Está certo.

Os dispositivos de rede usam pacotes do Internet Control Message Protocol (ICMP) para enviar mensagens de erro e controle, como se um dispositivo pode ou não se comunicar com outro na rede. Para prevenir ataques DoS e DDoS, empresas podem bloquear pacotes ICMP externos com firewalls.


# 38.4 Ataques a dispositivos móveis e sem fio

## 38.4.1 Grayware e SMiShing

**Grayware** é qualquer aplicativo indesejado que se comporta de maneira irritante ou indesejável. E, embora o grayware não tenha nenhum malware reconhecível, ele ainda pode representar um risco para o usuário, por exemplo, acompanhando a sua localização ou disponibilizando publicidade indesejável.

Os autores de grayware normalmente mantêm a legitimidade ao incluir esses recursos "cinzas" nas letras pequenas do contrato de licença do software. Esse fator representa uma ameaça crescente à segurança móvel, em particular, já que muitos usuários de smartphones instalam aplicativos móveis sem levar em consideração essas letras pequenas. 

O serviço de mensagem curta phishing ou **SMiShing** é outra tática usada pelos invasores para enganá-lo. Mensagens de texto falsas solicitam que você acesse um site mal-intencionado ou ligue para um número de telefone fraudulento, o que pode resultar no download de malware no dispositivo ou no compartilhamento de informações pessoais.


## 38.4.1 Grayware e SMiShing
Grayware é qualquer aplicativo indesejado que se comporta de maneira irritante ou indesejável. E, embora o grayware não tenha nenhum malware reconhecível, ele ainda pode representar um risco para o usuário, por exemplo, acompanhando a sua localização ou disponibilizando publicidade indesejável.

Os autores de grayware normalmente mantêm a legitimidade ao incluir esses recursos "cinzas" nas letras pequenas do contrato de licença do software. Esse fator representa uma ameaça crescente à segurança móvel, em particular, já que muitos usuários de smartphones instalam aplicativos móveis sem levar em consideração essas letras pequenas. 

O serviço de mensagem curta phishing ou SMiShing é outra tática usada pelos invasores para enganá-lo. Mensagens de texto falsas solicitam que você acesse um site mal-intencionado ou ligue para um número de telefone fraudulento, o que pode resultar no download de malware no dispositivo ou no compartilhamento de informações pessoais.

## 38.4.2 Pontos de acesso não autorizados

Um access point não autorizado é um access point sem fio instalado em uma rede segura sem autorização explícita. Embora possa ser configurado por um funcionário bem-intencionado que procura uma conexão sem fio melhor, ele também apresenta uma oportunidade para os invasores que desejam obter acesso à rede de uma empresa.

Selecione as setas para saber como.

Um invasor geralmente usa táticas de engenharia social para obter acesso físico à infraestrutura de rede de uma empresa e instalar o **access point não autorizado**.

---

Também conhecido como access point de criminosos, o access point pode ser configurado como um dispositivo MitM para capturar suas informações de login.

Isso funciona desconectando o access point não autorizado, que aciona a rede para enviar um quadro de autenticação e desassociar o access point. Esse processo é então explorado falsificando seu endereço MAC e enviando uma transmissão de dados de autenticação para o access point sem fio.

---

Um **ataque evil twinl** descreve uma situação em que o access point do invasor é configurado para parecer uma opção de conexão melhor. Depois de se conectar ao ponto de acesso maligno, o invasor pode analisar o tráfego da rede e executar ataques MitM.


## 38.4.3 Bloqueio de Frequência de Rádio
Os sinais sem fio são suscetíveis a interferência eletromagnética (EMI), interferência de radiofrequência (RFI) e até mesmo a raios ou ruídos de luzes fluorescentes.

Os invasores podem aproveitar esse fato bloqueando deliberadamente a transmissão de uma estação de rádio ou satélite para impedir que um sinal sem fio chegue à estação receptora.

Para bloquear o sinal com sucesso, a frequência, a modulação e a potência do jammer de RF precisam ser iguais às do dispositivo que o invasor está tentando interromper.


## 38.4.4 Bluejacking e Bluesnarfing
O Bluetooth é um protocolo de curto alcance e baixa potência que transmite dados em uma rede de área pessoal (PAN) e usa o emparelhamento para estabelecer uma relação entre dispositivos, como celulares, laptops e impressoras. Os criminosos digitais descobriram maneiras de explorar as vulnerabilidades entre essas conexões.

Devido ao alcance limitado do Bluetooth, o invasor deve estar dentro do alcance do alvo. Aqui estão algumas maneiras pelas quais eles podem explorar o dispositivo de um alvo sem o conhecimento deles.

Selecione as imagens para saber como.

**O Bluejacking usa a tecnologia Bluetooth sem fio para enviar mensagens não autorizadas ou imagens chocantes para outro dispositivo Bluetooth.**

**O bluesnarfing ocorre quando um invasor copia informações, como e-mails e listas de contatos, de um dispositivo de destino usando uma conexão Bluetooth.**


## 38.4.5 Ataques contra protocolos Wi-Fi
Wired Equivalent Privacy (WEP) e Wi-Fi Protected Access (WPA) são protocolos de segurança projetados para proteger redes sem fio.

O WEP foi desenvolvido para fornecer dados transmitidos por uma rede local sem fio (WLAN) com um nível de proteção comparável ao que é normalmente esperado de uma rede com fio tradicional. Ela agregou segurança às redes sem fio ao criptografar os dados.

WEP usou uma chave para criptografia. O problema, no entanto, era que o WEP não dispunha de gerenciamento de chaves e, portanto, o número de pessoas que compartilhavam a mesma chave crescia continuamente, dando aos criminosos acesso a uma grande quantidade de dados de tráfego. Além disso, o vetor de inicialização (IV) do WEP, um dos principais componentes de sua chave de criptografia, era muito pequeno, legível e estático.

Para resolver isso e substituir o WEP, o WPA e o WPA2 foram desenvolvidos como protocolos de segurança aprimorados. Ao contrário do WEP, um invasor não pode recuperar a chave de criptografia do WPA2 observando o tráfego de rede. No entanto, eles ainda podem usar um sniffer de pacotes para analisar os pacotes entre um ponto de acesso e um usuário legítimo.

## 38.4.6 Wi-Fi e defesa móvel
Existem várias medidas que organizações e usuários precisam implementar para se defender contra ataques a dispositivos móveis e sem fio. Estes incluem o seguinte:

Aproveite os recursos básicos de segurança sem fio, como autenticação e criptografia, alterando as configurações padrão.
Restrinja o posicionamento de access point colocando esses dispositivos fora do firewall ou em uma zona desmilitarizada - uma rede de perímetro que protege a LAN de uma empresa contra dispositivos não confiáveis.
Use ferramentas WLAN como NetStumbler para detectar pontos de acesso não autorizados ou estações de trabalho não autorizadas. 
Desenvolva uma política para acesso seguro de convidados à rede Wi-Fi de uma organização.
Os funcionários de uma organização devem usar uma VPN de acesso remoto para acesso WLAN quando estiverem em redes Wi-Fi públicas.


## 38.4.7 Verifique sua compreensão - Ataques a dispositivos móveis e sem fio
Você está tomando um café no café local e decide atualizar seus e-mails enquanto espera que seu amigo chegue. A pessoa tenta se conectar ao Wi-Fi do café, mas a conexão parece fraca Felizmente, há um segundo Wi-Fi com um nome semelhante, então a pessoa faz logon. No entanto, um invasor está sentado por perto, tendo criado um ponto de acesso Wi-Fi em seu celular, que emparelhou com seu laptop Eles estão monitorando a atividade online de todos que se conectam a este Wi-Fi.

Que tipo de ataque é esse?

- [ ] Interferência de Radiofrequência
- [x] Gêmeo do mal
- [ ] Bluejacking
- [ ] Bluesnarfing

Isso mesmo!

Bluejacking e o bluesnarfing usam a tecnologia sem fio Bluetooth para realizar um ataque. Um ataque "evil twin" descreve uma situação em que o ponto de acesso à Internet de um invasor é configurado para parecer uma opção de conexão melhor para um ponto de acesso legítimo. O bloqueio de radiofrequência descreve uma situação em que a transmissão de uma estação de rádio ou satélite é deliberadamente bloqueada para impedir que um sinal sem fio chegue à estação receptora.


# 38.5 Ataques a aplicativos

## 38.5.1 Script entre sites (Cross-Site Scripting - CSS)

Os ataques realizados por meio de aplicativos da Web estão se tornando cada vez mais comuns. Atores de ameaças exploram vulnerabilidades na codificação de um aplicativo baseado na Web para obter acesso a um banco de dados ou servidor. 

Cross-site scripting (XSS) é uma ameaça comum encontrada em muitos aplicativos da web. Funciona assim:

1. Os criminosos digitais exploram a vulnerabilidade XSS ao injetar scripts que contêm código mal-intencionado em uma página da Web.
2. A página da Web é acessada pela vítima, e os scripts mal-intencionados passam inadvertidamente para o navegador. 
3. O script malicioso pode acessar cookies, tokens de sessão ou outras informações sensíveis sobre o usuário, que são enviadas de volta para o cibercriminoso.
4. Munido dessas informações, o criminoso digital pode se passar por um usuário.

## 38.5.2 Injeção de Código
A maioria dos sites modernos usa um banco de dados, como um banco de dados de linguagem de consulta estruturada (SQL) ou um XML (Extensible Markup Language), para armazenar e gerenciar dados. Os ataques de injeção buscam explorar os pontos fracos desses bancos de dados.

Selecione os títulos para saber mais sobre alguns tipos comuns de ataques de injeção.


### Ataque de injeção de XML
Um ataque de injeção de XML pode corromper os dados no banco de dados XML e ameaçar a segurança do site.

Ele funciona ao interferir no processamento de dados XML ou na consulta de uma aplicação inserida por um usuário. 

Os criminosos digitais podem manipular essa consulta ao programá-la para atender às suas necessidades. Isso concederá a eles acesso a todas as informações confidenciais armazenadas no banco de dados e permitirá que eles façam qualquer alteração no site.

### Ataque de injeção de SQL
Os criminosos digitais podem realizar um ataque de injeção de SQL em sites ou em qualquer banco de dados SQL inserindo uma instrução SQL mal-intencionada em um campo de entrada.

Esse ataque aproveita uma vulnerabilidade na qual o aplicativo não filtra corretamente os dados inseridos por um usuário por caracteres em uma instrução SQL. 

Como resultado, o criminoso digital pode obter acesso não autorizado a informações armazenadas no banco de dados, das quais pode falsificar uma identidade, modificar dados atuais, destruir dados ou até mesmo se tornar um administrador do próprio servidor de banco de dados.

### Ataque de injeção de DLL
Um arquivo Dynamic Link Library (DLL) é uma biblioteca que contém um conjunto de códigos e dados para realizar uma determinada atividade no Windows. Os aplicativos usam esse tipo de arquivo para adicionar funcionalidades não incorporadas, quando precisam realizar essa atividade.

A injeção de DLL permite que um criminoso digital engane um aplicativo para chamar um arquivo DLL mal-intencionado, que é executado como parte do processo de destino.


### Ataque de injeção de LDAP
O Lightweight Directory Access Protocol (LDAP) é um protocolo aberto para autenticar o acesso do usuário a serviços de diretório.

Um ataque de injeção de LDAP explora vulnerabilidades de validação de entrada ao injetar e executar consultas a servidores LDAP, dando aos criminosos digitais a oportunidade de extrair informações confidenciais do diretório LDAP de uma empresa.


## 38.5.3 Estouro de buffer (Buffer Overflow)
Uma pilha de barras que caindo
Os buffers são áreas de memórias alocadas a um aplicativo. Um estouro de buffer ocorre quando os dados são gravados além dos limites de um buffer. Ao alterar os dados além dos limites de um buffer, o aplicativo pode acessar a memória alocada para outros processos. Isso pode levar a uma falha do sistema ou comprometimento de dados, ou fornecer escalação de privilégios.

Essas falhas de memória também podem oferecer aos invasores controle total sobre o dispositivo de um alvo. Por exemplo, um invasor pode alterar as instruções de uma aplicação vulnerável enquanto o programa está carregando na memória e, como resultado, pode instalar malware e acessar a rede interna do dispositivo infectado.


## 38.5.4 Execuções Remotas de Código
A execução remota de código permite que um cibercriminoso aproveite as vulnerabilidades do aplicativo para executar qualquer comando com os privilégios do usuário que executa o aplicativo no dispositivo de destino.

O escalonamento de privilégios explora um bug, falha de projeto ou configuração incorreta em um sistema operacional, ou aplicativo de software para obter acesso a recursos que normalmente são restritos.

Selecione a imagem para saber mais sobre o Projeto Metasploit e a carga útil do teste de vulnerabilidade de execução remota de código Meterpreter.

O Metasploit Project é um projeto de segurança de computadores que fornece informações sobre vulnerabilidades de segurança e auxilia no teste de penetração. Entre as ferramentas que eles desenvolveram está o Metasploit Framework, que pode ser usado para desenvolver e executar código de exploração em um alvo remoto.

O Meterpreter, em particular, é uma carga útil dentro do Metasploit que permite que os usuários assumam o controle de um dispositivo de destino gravando suas próprias extensões e carregando esses arquivos em um processo em execução no dispositivo. Esses arquivos são carregados e executados a partir da memória, portanto nunca envolvem o disco rígido. Isso significa que esses arquivos voam sob o radar da detecção de antivírus.

O Meterpreter também possui um módulo para controlar a webcam de um sistema remoto. Quando o Meterpreter é instalado em um dispositivo de destino, o usuário Metasploit pode visualizar e capturar imagens da webcam do alvo.


## 38.5.5 Outros ataques a aplicativos
Cada informação que um invasor recebe sobre um sistema ou aplicativo específico pode ser usada como uma arma valiosa para iniciar um ataque perigoso.

Selecione os títulos para descobrir mais sobre outros tipos de ataques a aplicativos.

### Cross-site request forgery (CSRF)

O CSRF descreve a exploração mal-intencionada de um site onde os comandos não autorizados são enviados do navegador de um usuário para um aplicativo da Web confiável.

Um site mal-intencionado pode transmitir esses comandos por meio de marcas de imagem, formulários ocultos ou solicitações de JavaScript especialmente criadas, que podem funcionar sem o conhecimento do usuário.


### Ataque de condição de corrida

Também conhecido como TOC (tempo de verificação) ou tempo de uso (TOU), um ataque de condição de corrida acontece quando um sistema de computação projetado para lidar com tarefas em uma sequência específica é forçado a executar duas ou mais operações simultaneamente.

Por exemplo, os sistemas operacionais são compostos de segmentos, a menor sequência de instruções do programa necessária para realizar um processo. Quando dois ou mais encadeamentos acessam dados compartilhados e tentam alterá-los ao mesmo tempo, ocorre um ataque de condição de corrida.


### Ataque de tratamento de entrada inadequado

Os dados inseridos por um usuário que não é validado corretamente podem afetar o fluxo de dados de um programa e causar vulnerabilidades críticas em sistemas e aplicativos que resultam em estouro de buffer ou ataques de injeção de SQL.


### Ataque de tratamento de erros

Os invasores podem usar mensagens de erro para extrair informações específicas, como nomes de host de sistemas internos e diretórios ou arquivos que existem em um determinado servidor Web, bem como nomes de bancos de dados, tabelas e campos que podem ser usados para criar ataques de injeção de SQL.


### Ataque à interface de programação de aplicativos (API)

Uma API fornece uma resposta do usuário para um sistema e envia a resposta do sistema de volta para o usuário. Um ataque de API ocorre quando um criminoso digital abusa de um endpoint de API.


### ataques de repetição

Isso descreve uma situação em que uma transmissão de dados válida é repetida ou retardada de forma mal-intencionada ou fraudulenta por um invasor, que intercepta, altera e reenvia os dados para que o destinatário faça o que quiser.


### Ataque transversal de diretório

A passagem de diretório ocorre quando um invasor é capaz de ler arquivos no servidor da Web fora do diretório do site. Um invasor pode usar essas informações para baixar arquivos de configuração do servidor que contêm informações confidenciais, expor potencialmente mais vulnerabilidades do servidor ou até mesmo assumir o controle do servidor!


### Ataques de exaustão de recursos

Esses ataques são exploits de segurança de computadores que travam, paralisam ou interferem em um programa ou sistema específico. Em vez de sobrecarregar a largura de banda de rede como um ataque de DoS, os ataques de exaustão de recursos sobrecarregam os recursos de hardware disponíveis no servidor de destino.


## **38.5.6 Item de Prática - Ataques de Código e Memória**

Um invasor identificou uma vulnerabilidade no serviço de mensagens online da corporação, que facilita a comunicação entre funcionários que trabalham em diferentes sites. Quando um funcionário faz uma chamada de voz, ela inunda a memória do aplicativo, dando efetivamente ao invasor controle sobre o dispositivo do funcionário. Que tipo de ataque é esse?

- [ ] Ataque de exaustão de recursos
- [ ] Execução remota de código
- [x] Buffer overflow
- [ ] Script entre sites

Está certo.

- Os ataques de esgotamento de recursos interferem com uma aplicação sobrecarregando os recursos de hardware disponíveis no servidor de destino.
- A execução remota de código ocorre quando os invasores exploram uma vulnerabilidade de aplicativo para executar qualquer comando com os privilégios de destino que executam o aplicativo em seus dispositivos.
- Um buffer overflow ocorre quando os dados são gravados além dos limites de um buffer, permitindo que o aplicativo acesse a memória alocada para outros processos. Isso pode levar à queda do sistema, comprometimento de dados ou fornecer o escalonamento de privilégios.
- Os invasores exploram vulnerabilidades de script entre sites (XSS) injetando scripts contendo código malicioso em uma página da web. Quando a vítima acessa essa página da Web, os scripts mal-intencionados passam sem saber para o navegador, dando aos invasores acesso a informações confidenciais.


## 38.5.7 Defesa contra ataques à Aplicação
Um escudo amarelo com um laptop e um smartphone na frente
Existem várias ações que você pode tomar para se defender contra um ataque a aplicativo. Você encontrará alguns deles descritos aqui.

A primeira linha de defesa contra um ataque a aplicativo é escrever um código sólido. 
Prática prudente de programação envolve tratar e validar todas as entradas de fora de uma função como se fosse hostil. 
Use ferramentas de teste de segurança para avaliar o código-fonte e o software binário continuamente durante o ciclo de vida do desenvolvimento do software.
Mantenha todos os softwares atualizados, incluindo os sistemas operacionais e aplicativos, e não ignore os prompts de atualização. Nem todos os programas são atualizados automaticamente.

## 38.5.8 Spam
Spam, também conhecido como lixo eletrônico, é simplesmente um e-mail não solicitado. Na maioria dos casos, é um método de publicidade. No entanto, muito spam é enviado em massa por computadores infectados por vírus ou worms - e muitas vezes contém links mal-intencionados, malware ou conteúdo enganoso que tem como objetivo enganar os destinatários na divulgação de informações confidenciais, como um número de Previdência Social ou informações de conta bancária.

Quase todos os provedores de e-mail filtram spam, mas ainda consomem largura de banda. E mesmo se você tiver recursos de segurança implementados, alguns spams ainda podem chegar até você. Fique atento aos seguintes indicadores de spam:

- O e-mail não tem assunto.
- O e-mail solicita que você atualize os detalhes da sua conta.
- O texto do e-mail contém palavras com erros ortográficos ou pontuação e caracteres estranhos.
- Links no e-mail são longos e/ou incompreensíveis.
- O e-mail parece correspondência de uma empresa legítima, mas há pequenas diferenças - ou contém informações que não parecem relevantes para você.
- O e-mail solicita que você abra um anexo, geralmente com urgência.
- O e-mail se origina de um domínio incomum ou contém links para domínios que provavelmente não pertencem ao remetente identificado.

Se você receber um e-mail que contenha um ou mais desses indicadores, **não** abra o e-mail ou qualquer anexo. Muitas empresas têm uma política de e-mail que exige que os funcionários relatem o recebimento desse tipo de e-mail à equipe de segurança digital para investigação adicional. Em caso de dúvida, sempre informe.


## 38.5.9 Phishing
Phishing é uma forma de atividade fraudulenta frequentemente usada para roubar informações pessoais.

Selecione as imagens para saber mais.

**Phishing**

O phishing ocorre quando um usuário é contatado por e-mail ou mensagem instantânea — ou de qualquer outra forma — por alguém que se disfarça de pessoa ou empresa legítima. A intenção é induzir o destinatário a instalar malware em seu dispositivo ou compartilhar informações confidenciais, como credenciais de login ou informações financeiras.

Por exemplo, você recebe um e-mail parabenizando você por ganhar um prêmio. Parece que ele foi enviado de uma loja conhecida e pede para você clicar em um link para reivindicar o prêmio. Na verdade, esse link pode redirecioná-lo para um site falso que solicita a inserção de seus dados pessoais ou até mesmo instalar um vírus no seu dispositivo.

**Spear phishing**

Um ataque altamente direcionado, o spear phishing envia e-mails personalizados para uma pessoa específica com base em informações que o atacante conhece sobre ela, como seus interesses, preferências, atividades ou projetos de trabalho.

Por exemplo, um criminoso digital descobre através de suas pesquisas que você está procurando um modelo específico de carro. O criminoso digital entra em um fórum de discussão sobre o carro do qual você é membro, cria uma venda de carro e envia um e-mail com um link para ver as fotos do carro. Ao clicar no link, você instala malware sem saber no seu dispositivo.


## 38.5.10 Vishing, Pharming e Whaling
Os criminosos usam uma ampla variedade de técnicas para tentar obter acesso às suas informações pessoais.

Selecione os títulos para descobrir mais sobre alguns dos malware mais comuns.

### Vishing

Muitas vezes chamado de phishing de voz, esse tipo de ataque faz com que os criminosos usem a tecnologia de comunicação por voz para incentivar os usuários a divulgar informações, como detalhes do cartão de crédito.

Os criminosos podem imitar chamadas telefônicas usando o protocolo de voz sobre internet (VoIP) ou deixar mensagens gravadas para dar a impressão de que são chamadas legítimas.


### Pharming

Esse tipo de ataque direciona deliberadamente os usuários para uma versão falsa de um site oficial. Enganados com a crença de que estão conectados a um site legítimo, os usuários inserem suas credenciais no site fraudulento.


### Whaling

Whaling é um ataque de phishing que buscam vítimas de alto perfil em uma empresa, como executivos seniores.


## 38.5.11 Item de Prática - Ataques de Phishing
Combine o cenário descrito com o tipo de ataque.

|Item|Classificação|✅|
|---|---|---|
|Um funcionário recebeu uma mensagem de texto informando que uma das assinaturas de software da @Apollo está expirando e que deve atualizar os detalhes imediatamente.|Smishing|✅|
|Um funcionário recebeu uma chamada telefônica automatizada do banco avisando que a conta da @Apollo tinha sido comprometida e que ele deve ligar para um número específico para redefinir a senha.|Vishing|✅|
|Um funcionário recebeu um e-mail de um fornecedor da @Apollo pedindo que ele clicasse em um link para obter um desconto.|Phishing|✅|

## 38.5.12 Defesa contra ataques a email e browser

Há muitas ações que você pode tomar para se defender contra ataques de e-mail e navegadores. Alguns dos mais importantes estão descritos aqui.

- É difícil parar o spam, mas existem maneiras de reduzir seus efeitos:
    - A maioria dos provedores de serviços de Internet (ISPs) filtra o spam antes que ele chegue à caixa de entrada do usuário.
    - Muitos programas antivírus e de software de e-mail detectam e removem automaticamente spam perigoso de uma caixa de entrada de e-mail.
    - As empresas devem educar os funcionários sobre os perigos dos e-mails não solicitados e conscientizá-los sobre os perigos da abertura de anexos. 
    - Nunca presuma que os anexos de e-mail são seguros, mesmo quando vierem de um contato confiável. Sempre verifique os anexos antes de abri-los.
- Torne-se um membro do Grupo de Trabalho Anti-Phishing (APWG). É uma associação internacional de empresas focada na eliminação de fraudes e roubo de identidade, resultantes de phishing e falsificação de e-mail.
- Todos os softwares devem ser mantidos atualizados, com as correções de segurança mais recentes aplicadas para proteger contra vulnerabilidades de segurança conhecidas.

**Selecione os títulos para revelar mais informações sobre outros ataques comuns que os criminosos digitais podem usar.**

### Ataques físicos

Os ataques físicos são ações intencionais e ofensivas usadas para destruir, expor, alterar, desativar, roubar ou obter acesso não autorizado à infraestrutura ou ao hardware de uma empresa.

Exemplos de ataques físicos incluem:

- Carregamento de malware em uma unidade flash USB que infecta um dispositivo quando conectado.
- Montagem de cabos e plugues, como cabos USB genéricos, cabos de carregamento de dispositivos móveis e adaptadores de energia ou parede com tecnologias avançadas, como um chip sem fio, para permitir que um invasor controle ou forneça instruções a um dispositivo.
- Copiar ou extrair dados de um cartão de crédito ou débito usando um terminal especializado para criar um cartão clonado, que pode ser usado para obter acesso não autorizado às contas da vítima.

### Ataques adversos à inteligência artificial

O aprendizado de máquina é um método de automação que permite que os dispositivos realizem análises e executem tarefas sem serem especificamente programados para isso. Ele funciona com muitos dos aplicativos que usamos hoje, como pesquisa na Web, marcação de fotos, detecção de spam, vigilância por vídeo, detecção de fraude e automação de segurança.

A aprendizagem de máquina usa modelos matemáticos para prever resultados. No entanto, esses modelos dependem dos dados inseridos. Se os dados estiverem infectados, poderão ter um impacto negativo no resultado previsto. Os invasores podem aproveitar isso para realizar ataques contra algoritmos de aprendizagem de máquina. Por exemplo, usar dados corrompidos para enganar um veículo autônomo e interpretar mal as placas de rua.

### Ataques à cadeia de fornecimento

Muitas empresas interagem com terceiros para gerenciar seus sistemas ou comprar componentes e software. As empresas podem até depender de peças ou componentes de fontes estrangeiras.

Os invasores geralmente encontram maneiras de interceptar essas cadeias de fornecimento. Por exemplo, o software pode se basear em contratos de suporte específicos e estar sujeito a uma data de fim de vida útil (EOL). Alterar essa data pode significar que uma empresa não está mais qualificada para obter suporte de serviço e manutenção.


### Ataques na nuvem

Em vez de desenvolver sistemas em suas próprias instalações, mais e mais empresas estão se movendo em direção à computação em nuvem, como discutimos anteriormente neste módulo.

A vantagem é que o provedor de nuvem vai manter o equipamento, mas isso também abre uma empresa para uma série de ameaças potenciais. Os invasores estão constantemente aproveitando formas de explorar dados confidenciais armazenados na nuvem, bem como aplicações, plataformas e infraestrutura baseada em nuvem, como vimos com SaaS, PaaS e IaaS.


## **38.5.13 Verifique sua compreensão - Ataques a aplicativos**

**Pergunta 1**

Qual ataque de aplicativo está ocorrendo quando a vítima acessa uma página da Web e scripts maliciosos são passados inadvertidamente para o navegador?

- [x] Script entre sites (XSS)
- [ ] Inserção de SQL
- [ ] Injeção de XML
- [ ] Execução remota de código

Está certo.

Script entre sites ocorre quando a vítima acessa uma página da web e scripts maliciosos são passados inadvertidamente para seu navegador. A execução remota de código permite que um cibercriminoso aproveite as vulnerabilidades do aplicativo para executar qualquer comando com os privilégios do usuário que executa o aplicativo no dispositivo de destino. Um ataque de injeção de XML pode corromper os dados no banco de dados XML e ameaçar a segurança do site. A injeção de SQL é um ataque a sites ou qualquer banco de dados SQL inserindo uma instrução SQL maliciosa em um campo de entrada.

**Pergunta 2**

Qual declaração descreve um ataque de estouro de buffer (buffer overflow)?

- [ ] As vulnerabilidades do aplicativo são exploradas para executar comandos com os privilégios do usuário no dispositivo de destino.
- [ ] Scripts maliciosos em uma página da web são passados inadvertidamente para o navegador da vítima.
- [x] Os dados são gravados além dos limites da área de memória alocada para um aplicativo.
- [ ] Os dados em um banco de dados XML estão corrompidos e ameaçam a segurança de um site.

Está certo.

Um ataque de estouro de buffer faz com que os dados sejam gravados além dos limites da área de memória alocada para um aplicativo. Um ataque de injeção de XML pode corromper os dados no banco de dados XML e ameaçar a segurança do site. Script entre sites ocorre quando a vítima acessa uma página da web e scripts maliciosos são passados inadvertidamente para seu navegador. A execução remota de código permite que um cibercriminoso aproveite as vulnerabilidades do aplicativo para executar qualquer comando com os privilégios do usuário que executa o aplicativo no dispositivo de destino.

**Pergunta 3**

Um cibercriminoso aproveita as vulnerabilidades do aplicativo e executa qualquer comando, no dispositivo de destino, com os privilégios do usuário que está executando o aplicativo. Que tipo de ataque esse cenário descreve?

- [ ] Inserção de SQL
- [ ] Script entre sites
- [x] Execução remota de código
- [ ] Injeção de XML

Está certo.

A execução remota de código permite que um cibercriminoso aproveite as vulnerabilidades do aplicativo para executar qualquer comando com os privilégios do usuário que executa o aplicativo no dispositivo de destino. Script entre sites ocorre quando a vítima acessa uma página da web e scripts maliciosos são passados inadvertidamente para seu navegador. Um ataque de injeção de XML pode corromper os dados no banco de dados XML e ameaçar a segurança do site. A injeção de SQL é um ataque a sites ou qualquer banco de dados SQL realizado pela inserção de uma instrução SQL maliciosa em um campo de entrada.

**Pergunta 4**

Qual prática de programação atenuará um ataque a aplicativo?

- [ ] escanear anexos de e-mail, antes de abri-los
- [ ] educar os usuários a não compartilhar informações confidenciais online
- [x] validar todas as entradas de uma função
- [ ] certifique-se de que o provedor de serviços de internet filtre todas as mensagens de e-mail

Está certo.

Uma prática de programação específica que ajudará a mitigar ataques de aplicativos é tratar e validar todas as entradas de uma função como se fossem hostis. Educar os usuários a não compartilhar informações confidenciais on-line, garantir que os provedores de serviços de Internet filtrem todas as mensagens de e-mail e sempre verificar os anexos de e-mail antes de abri-los são defesas contra ataques de e-mail e phishing.

**Pergunta 5**

Que tipo de ataque é usado para induzir um usuário a compartilhar informações confidenciais, como credenciais de login e números de cartão de crédito?

- [ ] execução remota de código
- [ ] pharming
- [ ] script entre sites
- [x] phishing

Está certo.

O phishing ocorre quando um usuário é contatado por e-mail ou mensagem instantânea e é induzido a instalar malware em seu dispositivo ou a compartilhar informações confidenciais. Pharming (falsificação) redireciona deliberadamente os usuários para uma versão falsa de um site oficial. A execução remota de código permite que um cibercriminoso aproveite as vulnerabilidades do aplicativo para executar qualquer comando com os privilégios do usuário que executa o aplicativo no dispositivo de destino. Script entre sites ocorre quando a vítima acessa uma página da web e scripts maliciosos são passados inadvertidamente para seu navegador.

**Pergunta 6**

Que tipo de ataque desvia deliberadamente os usuários para uma versão falsa de um site real?

- [ ] vishing
- [x] pharming
- [ ] whaling
- [ ] spam

Está certo.

Pharming (falsificação) redireciona deliberadamente os usuários para uma versão falsa de um site oficial. Muitas vezes referido como phishing de voz, o vishing vê os criminosos usarem a tecnologia de comunicação de voz para encorajar os usuários a divulgar informações, como detalhes do cartão de crédito. Whaling é um ataque de phishing que visa indivíduos de alto perfil. Spamming é o envio de e-mail não solicitado, muitas vezes enviado em massa por computadores infectados por vírus ou worms e geralmente contendo links maliciosos, malware ou conteúdo enganoso.


# 38.6 Resumo de Ameaças, Vulnerabilidades e Ataques à Segurança Cibernética

## 38.6.1 O que aprendi neste módulo?

### Ameaças comuns

Um domínio de ameaça é uma área de controle, autoridade ou proteção que os invasores podem explorar para obter acesso a um sistema. Os invasores podem explorar sistemas dentro de um domínio de ameaça obtendo acesso físico a sistemas, invadindo redes sem fio, comprometendo dispositivos Bluetooth e NFC, enviando e-mails maliciosos, examinando contas de mídia social, espalhando software malicioso (malware) por meio de mídia removível ou explorando ambientes de computação em nuvem.

Os ataques podem explorar bugs de software ou erro humano. Os ataques ameaçam os sistemas físicos por meio de sabotagem ou roubo. Além disso, falhas de equipamentos, interrupções de serviços públicos e desastres naturais podem afetar a disponibilidade de sistemas e recursos. As ameaças internas geralmente são de funcionários antigos ou atuais, enquanto as ameaças externas vêm de invasores amadores ou qualificados.

Um domínio de usuário inclui qualquer pessoa com acesso ao sistema de informações de uma empresa, incluindo funcionários, clientes e parceiros de contrato. Os usuários são muitas vezes considerados o elo mais fraco nos sistemas de segurança da informação. As ameaças do usuário vêm da falta de conscientização sobre segurança, políticas de segurança mal aplicadas, roubo de dados, downloads e mídia não autorizados, visitas a sites não autorizados ou destruições intencionais de sistemas, aplicativos e dados.

Ameaças aos dispositivos incluem acesso não autorizado a sistemas autônomos, download de malware e software desatualizado.

As ameaças à LAN incluem acesso não autorizado a instalações e equipamentos, vulnerabilidades do sistema operacional, pontos de acesso não autorizados, interceptação de dados em trânsito e práticas de gerenciamento ineficientes. Dispositivos de segurança mal configurados, como firewalls, também podem ser explorados.

As ameaças à nuvem privada incluem sondagem de rede e verificação de portas não autorizadas, acesso não autorizado a recursos, vulnerabilidades no software do dispositivo, erros de configuração e acesso não autorizado a recursos internos por meio da nuvem.

O domínio de aplicação inclui todos os sistemas críticos, aplicativos e dados usados por uma organização para apoiar suas operações. As ameaças ao domínio do aplicativo incluem acesso não autorizado, tempo de inatividade do servidor ou falha de hardware, vulnerabilidades do sistema operacional de rede, perda de dados e vulnerabilidades em aplicativos da Web ou software cliente-servidor.

Ameaças complexas assumem a forma de ameaças persistentes avançadas (APT) ou ataques de algoritmo. Os APTs ocorrem durante um período prolongado e usam táticas elaboradas e malware. Os ataques de algoritmo exploram processos de software para gerar comportamentos que não foram pretendidos pelos desenvolvedores de software.

Backdoors, como Netbus ou Back Orifice, são usados para obter acesso contínuo não autorizado a sistemas ignorando os procedimentos normais de autenticação. Eles geralmente envolvem o uso de ferramentas administrativas remotas (RAT) para obter acesso aos sistemas. Os rootkits são um tipo de malware que exploram vulnerabilidades para obter acesso não autorizado (escalonamento de privilégios). Os rootkits podem modificar arquivos do sistema e interferir na análise forense do sistema e nas ferramentas de monitoramento. Eles são muito difíceis de detectar e remover.

O United States Computer Emergency Readiness Team (US-CERT) e o Departamento de Segurança Interna dos EUA patrocinam um banco de dados de vulnerabilidades e exposições comuns (CVE). Os identificadores CVE são uma maneira padrão de se referir a vulnerabilidades de segurança conhecidas. A Dark Web é usada por hackers para trocar informações sobre vulnerabilidades e ameaças e dados roubados. Os profissionais de segurança usam CVEs e recursos da Dark Web para pesquisar ameaças à segurança. Indicadores de comprometimento (IOCs) são as características de ataques que podem ser usadas para identificar explorações. O Compartilhamento Automatizado de Indicadores (AIS) fornece uma maneira padrão para os profissionais de segurança trocarem informações de exploração usando a Expressão Estruturada de Informações sobre Ameaças (STIX) e a Troca Automatizada Confiável de Informações de Inteligência (TAXII).

### Disfarce

A engenharia social é uma estratégia não técnica que tenta manipular indivíduos para realizar ações específicas ou divulgar informações confidenciais. Pretexting é um ataque de engenharia social em que alguém mente para obter acesso a dados confidenciais. Um ataque "algo por algo" usa a oferta de um presente para obter informações confidenciais. Fraude de identidade é o uso de informações confidenciais roubadas de uma pessoa para adquirir bens ou serviços.

A engenharia social usa várias táticas diferentes para obter informações das vítimas. Os invasores podem fingir ser pessoas com autoridade ou usar a intimidação para obrigar as pessoas a agir de maneira que comprometa a segurança. Eles também podem usar táticas como consenso, escassez, urgência e familiaridade. Os invasores até desenvolverão uma relação de confiança com a vítima para, eventualmente, violar a segurança da vítima.

Shoulder surfing refere-se a olhar por cima do ombro de alguém para obter credenciais como senhas, PINs ou números de cartão de crédito. Dumpster diving (Mergulhar no lixo) significa literalmente vasculhar o lixo de alguém para encontrar informações pessoais confidenciais. Piggybacking e tailgating são maneiras de obter acesso físico não autorizado a áreas restritas.

Outros meios de fraude são o envio de faturas falsas para obter dinheiro ou credenciais, ataques watering hole nos quais sites populares são infectados com malware, "typo squatting" criando URLs que parecem muito próximos de sites populares, anexando ao remover avisos de sites externos por e-mail e campanhas de influência combinadas.

As organizações podem se defender contra o engano ensinando os funcionários a nunca fornecer informações confidenciais a terceiros desconhecidos, detectar e-mails suspeitos e resistir a clicar em links, evitar ou encerrar downloads não iniciados ou automáticos e resistir à pressão de indivíduos desconhecidos.

### Ataques cibernéticos

Malware é um software que pode ser usado para roubar dados, contornar o controle de acesso, ou causar danos ou comprometer um sistema. Os vírus são um tipo de malware que se replica quando executado. Eles podem ser inofensivos ou destrutivos. Worms são programas que se replicam de forma independente nas redes. Cavalos de Troia são malwares que se disfarçam de outros aplicativos de software ou são distribuídos com aplicativos legítimos. As bombas lógicas são acionadas para agir por data e hora ou outros eventos do sistema. Ransomware é um ataque comum que usa software malicioso para criptografar uma unidade de hardware do sistema. Às vezes, mas nem sempre, pagar um resgate reverterá o dano.

Ataques de negação de serviço (DoS) são um tipo de ataque de rede que afeta a disponibilidade de recursos. Em um tipo de ataque DoS, uma rede ou aplicativo é sobrecarregado com uma enorme quantidade de dados. Isso pode tornar os sistemas lentos ou travar. Em outro ataque DoS, pacotes formatados com códigos maliciosos são enviados para interromper a operação do sistema.

O Domain Name System (DNS) é essencial para as operações de rede. Os invasores podem prejudicar a reputação de um domínio criando domínios semelhantes falsos ou por meio de notícias falsas. Na falsificação de domínio, os invasores exploram os pontos fracos do DNS para mapear nomes de domínio legítimos para sites mal-intencionados. Se os invasores obtiverem acesso às informações de registro de DNS de um alvo, eles poderão sequestrar o nome de domínio alterando o nome de domínio para mapeamentos de endereços IP.

Dois tipos comuns de ataques de Camada 2 são spoofing e MAC flooding. A falsificação de endereço MAC ocorre quando um invasor disfarça seu dispositivo como um dispositivo válido na rede e, portanto, pode ignorar o processo de autenticação. O spoofing de ARP envia mensagens falsificadas de ARP através de uma LAN para vincular o endereço MAC do criminoso ao endereço IP do membro não autorizado da rede. O spoofing de IP envia pacotes IP com um endereço de origem falsificado para se disfarçar. No MAC flooding, um invasor inunda a rede com endereços MAC falsos, comprometendo a segurança do switch de rede.

Man-in-the-Middle (MitM), ou ataques no caminho, acontecem quando um cibercriminoso assume o controle de um dispositivo intermediário na rede ou coloca seu próprio dispositivo em um caminho para interceptar dados do usuário. O invasor pode roubar informações, manipular dados ou transmitir informações falsas. Um ataque Man-in-the-Mobile (MitMo) é uma variação de um ataque MitM em que um dispositivo móvel é infectado com malware que rouba dados do dispositivo.

Os ataques de dia zero exploram vulnerabilidades do software antes que elas se tornem conhecidas. Uma visão sofisticada e holística da infraestrutura de segurança é necessária para se defender contra esses ataques.

Os registradores de teclado (keyboard loggers) são tipos de malware que registram cada tecla digitada em um computador. Isso pode revelar informações confidenciais e credenciais de conta.

Várias diretrizes para se defender contra ataques são configurar firewalls para filtrar pacotes de entrada que parecem ter se originado internamente, garantir que todo software tenha as atualizações e patches mais recentes, distribuir cargas de trabalho entre vários sistemas de servidor e bloquear pacotes ICMP na borda da rede.

### Ataques a dispositivos móveis e sem fio

Grayware é um aplicativo indesejado que se comporta de maneira irritante ou indesejável. SMiShing é o uso de mensagens SMS falsas para induzir o usuário a visitar um site malicioso ou ligar para um número de telefone fraudulento.

Pontos de acesso não autorizados são instalados em redes sem autorização. Eles podem se disfarçar como pontos de acesso legítimos para induzir os usuários a se associarem a eles. Eles podem ser usados para conduzir ataques MitM desautenticando usuários ou se passando por pontos de acesso legítimos com conexões mais desejáveis em ataques "evil twin".

Os sinais sem fio são suscetíveis a interferências e bloqueios. Os invasores podem negar o serviço sem fio bloqueando os sinais Wi-Fi. O Bluetooth pode ser usado para enviar mensagens não autorizadas através do Bluejacking. O Bluesnarfing ocorre quando um invasor copia informações de um dispositivo móvel por meio de uma conexão Bluetooth maliciosa.

Wired Equivalent Privacy (WEP) e Wi-Fi Protected Access (WPA) são protocolos de segurança projetados para proteger redes sem fio. O WEP não tinha provisão para gerenciamento de chaves e, portanto, era vulnerável a ataques. Para resolver isso e substituir o WEP, o WPA e o WPA2 foram desenvolvidos como protocolos de segurança aprimorados.

Para aumentar a segurança sem fio, é importante usar pelo menos a criptografia WPA2. Os pontos de acesso devem ser colocados fora do perímetro da rede, se possível. Use ferramentas para detectar access points não autorizados. Permitir apenas acesso Wi-Fi seguro para convidados. Por fim, os funcionários devem sempre usar VPN de acesso remoto ao se conectar à rede da organização em redes Wi-Fi públicas.

### Ataques a aplicativos

Cross-site scripting (XSS) é um ataque de aplicativo da Web comum no qual um código malicioso é inserido em um site legítimo. O navegador da vítima executa o código malicioso que baixa malware, redireciona para um site malicioso ou rouba informações.

Os ataques de injeção envolvem a exploração de sistemas inserindo dados ou comandos malformados nos campos de entrada do usuário. Eles são especialmente comuns contra bancos de dados. Os ataques de injeção de XML e SQL corrompem bancos de dados ou fazem com que informações confidenciais, como credenciais de usuário, sejam reveladas. As bibliotecas de vínculo dinâmico (DLL) são módulos de software usados por aplicativos para interagir com o Windows. Os invasores podem injetar código malicioso em DLLs que serão executados quando a DLL for usada. Os ataques de injeção de LDAP exploram a validação de entrada para executar consultas em servidores LDAP, potencialmente dando aos invasores acesso a informações confidenciais da conta.

A execução remota de código permite que um cibercriminoso aproveite as vulnerabilidades do aplicativo para executar qualquer comando com os privilégios do usuário que executa o aplicativo no dispositivo de destino. Outros ataques a aplicativos são falsificações de solicitação entre sites, ataques de condição de corrida, ataques de entrada imprópria do usuário, ataques de tratamento de erros e ataques de interface de programação de aplicativos (API). Ataques adicionais são ataques de repetição, ataques de travessia de diretório e ataques de esgotamento de recursos.

Para se defender contra ataques a aplicativos, a primeira linha de defesa é escrever um código sólido. Todas as entradas do usuário devem ser validadas. As ferramentas de teste de segurança devem ser usadas para avaliar o código conforme ele é desenvolvido e antes da implantação. Finalmente, todos os softwares, incluindo sistemas operacionais, devem ser mantidos atualizados.

Spam, também conhecido como lixo eletrônico, é simplesmente um e-mail não solicitado. O spam geralmente é um incômodo, mas pode ser malicioso. Embora os filtros de spam sejam amplamente utilizados, é importante que os usuários saibam como identificar o spam.

Phishing e spear phishing são ataques que parecem vir de fontes legítimas, mas querem que você baixe arquivos ou envie informações confidenciais. Os ataques de spear phishing são direcionados diretamente a indivíduos específicos. Vishing usa mensagens de voz para atacar. O pharming direciona os usuários para versões falsas de sites legítimos. Whaling é o phishing direcionado a usuários de alto perfil, como executivos, políticos ou celebridades.

Para se defender contra ataques de e-mail e navegador, as organizações devem usar filtros de spam, implantar software antivírus e educar os usuários sobre segurança de rede.

## 38.6.2 Webster – Perguntas para reflexão

Uau, você sabia sobre todas essas coisas ruins que os agentes de ameaças podem fazer? Eu não sabia, mas estou feliz por saber mais sobre isso agora. A campanha de conscientização deve ajudar os usuários da faculdade a reconhecer as ameaças. Espero que tenha ajudado você também. Mas lembre-se de que os agentes de ameaças tentam constantemente encontrar uma nova maneira de tirar vantagem de você ou de sua empresa. Então, sempre há algo novo para aprender.

Há algo mais que devemos incluir na campanha de conscientização? Você compartilhará algumas dessas informações com familiares ou outros usuários em sua rede? Como você pode proteger a si mesmo, seu computador e sua empresa contra essas ameaças?