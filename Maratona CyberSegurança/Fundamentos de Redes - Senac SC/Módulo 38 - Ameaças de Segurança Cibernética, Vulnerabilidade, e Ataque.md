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

