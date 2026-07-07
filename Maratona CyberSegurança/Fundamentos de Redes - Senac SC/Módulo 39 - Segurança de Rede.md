
# 39.0 Introdução

## 39.0.1 Por que devo fazer este módulo?

Olá de novo! A campanha de conscientização em que Lara trabalhou foi um sucesso. Por causa disso, a faculdade convidou Lara para trabalhar em um comitê para desenvolver a política de segurança da faculdade. A política de segurança é um documento que ajuda os administradores da faculdade, a equipe de TI e os usuários da faculdade a defender a rede e os terminais.

Lara revisará as políticas de segurança atuais neste comitê e ajudará a desenvolver novas. Essas políticas informam à equipe de TI como manter a confidencialidade dos dados, garantir a integridade dos dados e garantir que a rede esteja disponível para todos os usuários. Ele também define como a web pode ser acessada, quais sistemas e dispositivos serão usados para protegê-la e como proteger dispositivos terminais e acesso sem fio. Vamos trabalhar neste módulo para saber mais sobre o que podemos fazer para defender a rede e seus terminais.

## 39.0.2 O que vou aprender neste módulo?

**Título do Módulo**: Segurança de Rede 
**Objetivo do Módulo**: Configurar acesso seguro do usuário à rede.

| Título do Tópico                                  | Objetivo do Tópico                                                                                      |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| Fundamentos de Segurança                          | Explicar os conceitos básicos de segurança.                                                             |
| Controle de acesso                                | Configurar o controle de acesso.                                                                        |
| Defesa de sistemas e dispositivos                 | Explicar processos e procedimentos de cibersegurança que protegem os sistemas.                          |
| Proteção Antimalware                              | Explicar os métodos de mitigação de malware.                                                            |
| Prevenção de Intrusão Baseada em Host e Firewalls | Explicar como os firewalls operam para filtrar o tráfego e recomendar medidas de segurança de endpoint. |
| Acesso sem fio seguro                             | Configurar a segurança básica em um roteador sem fio residencial (WPAx).                                |

# 39.1 Fundamentos de Segurança

## 39.1.1 O Cubo de Cibersegurança

Você já ouviu falar do cubo de segurança digital? Ele fornece uma maneira útil de refletir sobre a proteção de dados. O cubo nos mostra o que a tarefa de proteger dados envolve, incluindo as três dimensões da segurança da informação.

**Role para baixo para explorar cada uma delas.**

### 1. Princípios de segurança

A primeira dimensão do cubo de segurança cibernética identifica os objetivos para proteger o espaço cibernético. Os princípios fundamentais de confidencialidade, integridade e disponibilidade de dados fornecem um foco que permite que o especialista em segurança cibernética priorize ações ao proteger qualquer sistema em rede.

A **confidencialidade** dos dados impede a divulgação de informações a pessoas, recursos ou processos não autorizados.

A **integridade** dos dados refere-se à precisão, consistência e confiabilidade dos dados.

A **disponibilidade** de dados garante que as informações sejam acessíveis por usuários autorizados quando necessário.

Use o acrônimo CIA para se lembrar desses três princípios.


### 2. Estado dos Dados

O domínio do ciberespaço contém uma quantidade considerável de dados extremamente importantes. Mas em que estado?  
A segunda dimensão do cubo de segurança digital representa os três possíveis estados dos dados.

- Dados **em trânsito**.
- Dados **inativos** ou em armazenamento.
- Dados **em processamento**.

A segurança digital eficaz exige a proteção de dados nos três estados. Não podemos nos concentrar apenas na proteção dos dados que estão sendo processados, nem apenas nos dados armazenados.


### 3. Proteção

A terceira dimensão do cubo de segurança digital define os pilares nos quais precisamos basear nossas defesas de segurança digital para proteger dados e infraestrutura.

São contramedidas de proteção: **tecnologia**, **políticas e práticas** e a conscientização de **pessoas**.

Os profissionais de segurança cibernética devem usar uma variedade de diferentes qualificações profissionais e disciplinas disponíveis a eles, ao proteger os dados no espaço cibernético.

## 39.1.2 Confidencialidade, Integridade, and Disponibilidade

É verdade que a lista de tipos de ataque de rede é longa. Mas existem muitas práticas recomendadas que você pode usar para defender sua rede, como você aprenderá neste tópico.

A segurança da rede consiste em proteger informações e sistemas de informações contra acesso não autorizado, uso, divulgação, interrupção, modificação ou destruição.

A maioria das organizações segue a tríade de segurança da informação CIA. Uma vez que constitui a base da prática de segurança cibernética, é importante que você tenha uma compreensão detalhada dos três princípios:

- **Confidencialidade** - Apenas indivíduos, entidades ou processos autorizados podem acessar informações sensíveis. Ele pode exigir o uso de algoritmos de criptografia como AES para criptografar e descriptografar dados.
- **Integridade** - Refere-se à proteção dos dados contra alterações não autorizadas. Requer o uso de algoritmos de hash criptográfico, como o SHA.
- **Disponibilidade** - Os usuários autorizados devem ter acesso contínuo a recursos e dados importantes. Requer a implementação de serviços, gateways e links redundantes.

A figura mostra a Tríade CIA composta por Confidencialidade, Integridade e Disponibilidade.

### Tríade CIA
![[Pasted image 20260706083835.png]]


## 39.1.3 Tríade da CIA - O Princípio da Confidencialidade

Para obter confidencialidade sem usar criptografia, a **tokenização** é uma técnica de substituição que pode isolar os elementos de dados da exposição a outros sistemas de dados. Um valor aleatório sem relacionamento matemático substitui os dados originais. Fora do sistema, um token não tem valor e não faz sentido. A tokenização pode preservar o formato dos dados (tipo e comprimento dos dados), o que os torna úteis para bancos de dados e processamento de pagamento com cartão.

O gerenciamento de direitos abrange o **gerenciamento de direitos digitais (DRM)** e o **gerenciamento de direitos de informação (IRM)**. Ambos protegem os dados contra acesso não autorizado usando criptografia.

O DRM protege materiais protegidos por direitos autorais, como músicas, filmes ou livros. Quando qualquer conteúdo desse tipo aparece em formato digital - por exemplo, em CD, mp3 ou e-book - ele é criptografado e, portanto, a mídia não pode ser copiada sem a chave de descriptografia. A chave de descriptografia está disponível apenas para partes licenciadas.

O IRM é usado com e-mail e outros arquivos que são relevantes para as atividades e comunicações de uma empresa. Quando essas informações são compartilhadas com outras pessoas, o IRM permite que o proprietário do documento, a empresa ou um de seus membros controle e gerencie o acesso ao documento.


## 39.1.4 Item prático – Proteção e privacidade dos dados

Está certo.

Coloque as opções na seguinte ordem:

|Item|Classificação|
|---|---|
|Informações de acesso restrito de uma agência governamental para um novo módulo de treinamento que @Apollo está criando, com base em políticas de alta segurança.|Confidencial|
|Uma nova ferramenta de eLearning, que @Apollo está planejando lançar no mercado no próximo ano.|Negócios|
|Detalhes bancários de um funcionário da @Apollo.|Pessoal|

## 39.1.5 Integridade dos Dados

Integridade é a precisão, consistência e confiabilidade dos dados em todo o seu ciclo de vida.

Os dados passam por várias operações, como captura, armazenamento, recuperação, atualização e transferência. Os dados devem permanecer inalterados por entidades não autorizadas durante todas essas operações.

Os métodos usados para garantir a integridade de dados incluem hashing, verificações de validação de dados, verificações de consistência dos dados e controles de acesso. Os sistemas de integridade de dados podem incluir um ou mais desses métodos.

A integridade de dados é um componente fundamental da segurança da informação. Garantir a integridade dos dados é um desafio constante para a maioria das organizações. A perda da integridade de dados pode tornar recursos de dados inteiros não confiáveis ou inutilizáveis.

No entanto, a importância da integridade dos dados varia com base em como uma organização usa seus dados. Por exemplo, um banco ou organização financeira atribui maior importância à integridade dos dados do que um canal de mídia social.

**Selecione as imagens para saber mais sobre a necessidade de integridade dos dados.**

**Nível crítico de necessidade**

Em uma empresa de serviços de saúde, a integridade de dados pode ser uma questão de vida ou morte. Por exemplo, as informações de prescrição devem ser precisas. Portanto, todos os dados são continuamente validados, testados e verificados.

**Alto nível de necessidade**

Em uma empresa de comércio eletrônico ou baseada em análises, as transações e as contas de clientes devem ser precisas. Todos os dados são validados e verificados em intervalos frequentes.

**Nível médio de necessidade**

Os mecanismos de busca e vendas on-line coletam dados que foram publicados publicamente. Pouca verificação é realizada, e os dados não são totalmente confiáveis.

**Baixo nível de necessidade**

Blogs, fóruns e páginas pessoais nas redes sociais são impulsionados pela opinião pública e contribuição aberta. Os dados podem não ser verificados e o nível de confiança no conteúdo é baixo.


## 39.1.6 Disponibilidade

A disponibilidade refere-se à necessidade de tornar os dados acessíveis a todos os usuários autorizados sempre que eles precisarem. Ataques cibernéticos e falhas do sistema podem impedir o acesso a informações, sistemas e serviços.

**Você consegue identificar as causas mais comuns de falhas no sistema que podem afetar a disponibilidade de dados?**

Ao selecionar 'Iniciar', você verá uma série de opções. Toque em 'Sim' se achar que isso pode causar falhas no sistema que podem afetar a disponibilidade de informações, sistemas e serviços. Caso contrário, toque em 'Não'.

- Desastre natural
- Negação de serviço
- Ataques Maliciosos
- Manutenção de equipamento
- Falha de equipamento
- Backup de sistema

## 39.1.7 Garantia de Disponibilidade

Há muitas medidas que as empresas podem implementar para garantir a disponibilidade de seus serviços e sistemas.

Vamos explorar alguns exemplos.

**Selecione os títulos abaixo para saber mais sobre alguns deles.**

### Manutenção de equipamentos

A manutenção regular do equipamento pode melhorar bastante o tempo de atividade do sistema. A manutenção inclui a substituição, limpeza e alinhamento do componente.

### Sistemas operacionais e atualizações e patches de software

Sistemas operacionais, aplicativos e softwares modernos são atualizados continuamente para corrigir erros e eliminar vulnerabilidades. Em todas as organizações, todos os sistemas, aplicativos e softwares devem ser atualizados regularmente. Os profissionais de segurança cibernética podem se registrar para alertas que anunciam novas versões de atualização.

### Teste de backup

O backup dos dados da organização, dos dados de configuração e dos dados pessoais ajuda a garantir a disponibilidade. Os sistemas de backup e os dados de backup também devem ser testados para garantir que funcionem corretamente e que os dados possam ser recuperados em caso de perda de dados.

### Planejamento contra desastres

O planejamento contra desastres é uma parte crítica da disponibilidade crescente do sistema. Os funcionários e os clientes devem saber como responder a um desastre. A equipe de segurança cibernética deve praticar protocolos de resposta, testar sistemas de backup e estar familiarizada com os procedimentos para restaurar sistemas críticos.

### Implementações de novas tecnologias

A alta disponibilidade requer avaliação contínua e teste de novas tecnologias, para considerar novas ameaças e ataques. Os criminosos cibernéticos utilizam as mais recentes ferramentas e truques, por isso os profissionais de segurança cibernética também são obrigados a se manter atualizados utilizando novas tecnologias, produtos e dispositivos.


### Monitoramento de atividades

O monitoramento do sistema contínuo aumenta a disponibilidade do sistema. Monitorar logs de eventos, alertas do sistema e registros de acesso fornece ao profissional de segurança cibernética informações em tempo real sobre o sistema. Esse monitoramento pode identificar ataques em questão de segundos e permitir que os profissionais de segurança cibernética se defendam contra eles quando ocorrerem.


### Teste de disponibilidade

Todos os sistemas devem ser testados para encontrar vulnerabilidades. O teste pode incluir varreduras de porta, varreduras de vulnerabilidade e testes de penetração.


## 39.1.8 Verifique sua compreensão - Fundamentos de segurança

Combine o cenário, descrevendo o uso de dados, com o respectivo nível de integridade de dados necessária.

|Item|Classificação|
|---|---|
|Blogs, fóruns e páginas pessoais nas redes sociais são impulsionados pela opinião pública e contribuição aberta. Os dados podem não ser verificados e o nível de confiança no conteúdo é baixo.|Baixo nível de necessidade|
|Os mecanismos de busca e vendas on-line coletam dados que foram publicados publicamente. Pouca verificação é realizada, e os dados não são totalmente confiáveis.|Nível médio de necessidade|
|Em uma organização de saúde, a integridade dos dados pode ser uma questão de vida ou morte. As informações de prescrição devem ser precisas. Portanto, todos os dados são continuamente validados, testados e verificados.|Nível crítico de necessidade|
|Em uma organização de comércio eletrônico ou baseada em análise, as transações e as contas dos clientes devem ser precisas. Todos os dados são validados e verificados com frequência.|Alto nível de necessidade|

# 39.2 Controle de acesso

## 39.2.1 Controles de Acesso Físico

Controles de acesso físico são barreiras reais implantadas para evitar o contato direto com os sistemas. A meta é prevenir que usuários não autorizados acessem fisicamente as instalações, equipamentos e outros ativos organizacionais.

Por exemplo, o controle de acesso físico determina **quem** pode entrar (ou sair), **onde** podem entrar (ou sair) e **quando** podem entrar (ou sair).

Aqui estão alguns exemplos de controles de acesso físicos:

- Guardas que monitoram a instalação.
- Cercas que protegem o perímetro.
- Detectores de movimento que detectam objetos em movimento.
- Travas de laptop que impedem o roubo de equipamentos portáteis.
- Portas trancadas para impedir o acesso não autorizado.
- Cartões de acesso para permitir o acesso a uma área restrita.
- Cães de guarda para proteger a instalação.
- Câmeras de vídeo para monitorar uma instalação coletando e gravando imagens.
- Sistemas de entrada estilo Mantrap para escalonar o fluxo de pessoas na área protegida e prender visitantes indesejados.
- Alarmes para detectar intrusão.

## 39.2.2 Controles de Acesso Lógico

Controles de acesso lógico são as soluções de hardware e software usadas para gerenciar o acesso aos recursos e sistemas. Essas soluções baseadas em tecnologia incluem ferramentas e protocolos que os sistemas de computador utilizam para identificação, autenticação, autorização e contabilização.

Exemplos de controle de acesso lógico incluem:

- A criptografia é o processo de pegar o texto claro e criar o texto codificado.
- Os cartões inteligentes possuem um microchip integrado.
- As senhas são strings de caracteres protegidos.
- A biometria se refere às características físicas dos usuários.
- As listas de controle de acesso (ACLs) definem o tipo de tráfego permitido em uma rede.
- Os protocolos são conjuntos de regras que regem a troca de dados entre os dispositivos.
- Os firewalls impedem o tráfego de rede indesejado.
- Os roteadores conectam pelo menos duas redes.
- Os sistemas de detecção de invasão monitoram as atividades suspeitas de uma rede.
- Os níveis de corte são determinados pelos limites permitidos para erros antes de acionar uma bandeira vermelha.

## 39.2.3 Controles de Acesso Administrativo

Os controles de acesso administrativo são as políticas e procedimentos definidos pelas empresas para implementar e aplicar todos os aspectos de controle de acesso não autorizado.

Os controles administrativos se concentram nas seguintes práticas de pessoal e negócios.

- **Políticas** são ideias ou ações aprovadas que orientam o comportamento.
- **Procedimentos** são as etapas detalhadas necessárias para realizar uma atividade.
- As **práticas de contratação** definem as etapas que uma organização adota para encontrar funcionários qualificados.
- As **verificações de antecedentes** são um tipo de triagem de funcionários que inclui a verificação de empregos anteriores, histórico de crédito e histórico criminal.
- A **classificação de dados** categoriza os dados com base em sua sensibilidade.
- O **treinamento de segurança** educa os funcionários sobre as políticas de segurança em uma organização.
- As **revisões** avaliam o desempenho no trabalho de um funcionário.
![[Pasted image 20260706204908.png]]


## 39.2.4 Autenticação, autorização e contabilidade (AAA)

Vamos analisar os controles de acesso administrativos com mais detalhes.

O conceito de controles de acesso administrativo envolve três serviços de segurança: autenticação, autorização e contabilidade (AAA).

Esses serviços fornecem a estrutura principal para controlar o acesso, impedindo o acesso não autorizado a um computador, rede, banco de dados ou outro recurso de dados.

**Selecione os títulos abaixo para saber mais sobre alguns deles.**

### Autenticação
O primeiro A no AAA representa a autenticação. A autenticação é a verificação da identidade de cada usuário, para evitar acesso não autorizado. Os usuários provam sua identidade com um nome de usuário ou um ID. Além disso, os usuários precisam verificar sua identidade fornecendo um dos seguintes:

Algo que saibam (como uma senha)
Algo que tenham (como um token ou cartão)
Algo que eles são (como uma impressão digital)
No caso da autenticação de dois fatores, que está se tornando cada vez mais comum, a autenticação requer uma combinação de dois dos elementos mencionados anteriormente em vez de apenas um.

### Autorização
Serviços de autorização determinam quais recursos os usuários podem acessar, juntamente com as operações que os usuários podem realizar.

Alguns sistemas fazem isso usando uma lista de controle de acesso, ou uma ACL. Uma ACL determina se um usuário tem certos privilégios de acesso depois de se autenticar. Só porque você pode fazer logon na rede corporativa não significa que você tenha permissão para usar a impressora colorida de alta velocidade, por exemplo.

A autorização também pode controlar quando um usuário tem acesso a um recurso específico. Por exemplo, os funcionários podem ter acesso a um banco de dados de vendas durante o horário comercial, mas o sistema os bloqueia, depois de horas.

### Accounting
Não relacionado à contabilidade financeira, a contabilidade em AAA (Autenticação, Autorização e Contabilidade) registra o que os usuários fazem - incluindo o que eles acessam, a quantidade de tempo que acessam e quaisquer alterações que façam.

Por exemplo, um banco mantém o controle da conta de cada cliente. Uma auditoria do sistema pode revelar o tempo e o valor de todas as transações e o funcionário ou o sistema que executou as transações. Serviços de accounting de segurança cibernética funcionam da mesma maneira. O sistema controla cada transação de dados e fornece os resultados da auditoria. Os administradores de sistema podem configurar políticas de computador para habilitar a auditoria do sistema.

O conceito do AAA é semelhante ao uso de um cartão de crédito. O cartão de crédito identifica quem pode usá-lo, determina quanto o usuário pode gastar e contabiliza os itens ou serviços que o usuário comprou.

A contabilidade de cibersegurança acompanha e monitora as atividades dos usuários em tempo real.


## 39.2.5 O que é identificação?

A identificação aplica as regras estabelecidas pela política de autorização. Sempre que o acesso a um recurso é solicitado, os controles de acesso determinam se o acesso deve ser concedido ou negado.

Um identificador único assegura a devida associação entre as atividades permitidas e os indivíduos. Um nome de usuário é o método mais comum usado para identificar um usuário. Um nome de usuário pode ser uma combinação alfanumérica, um número de identificação pessoal (PIN), um cartão inteligente ou um recurso biométrico - como uma impressão digital, um escaneamento da retina ou reconhecimento de voz.

Um identificador único assegura que um sistema possa identificar cada usuário individualmente; portanto, permite que um usuário autorizado realize as ações apropriadas em um recurso específico.


## 39.2.6 Gerenciamento de identidade federada

A gestão de identidade federada (FIM) refere-se a várias empresas que permitem que seus usuários usem as mesmas credenciais de identificação para acessar as redes de todas as empresas do grupo. Embora o FIM forneça conveniência para usuários e administradores, se o sistema for explorado por hackers, eles terão acesso a vários sistemas em vez de apenas um.

Em termos gerais, uma identidade federada vincula a identidade eletrônica de um sujeito em sistemas separados de gerenciamento de identidade. Isso pode permitir o acesso a vários sites usando as mesmas credenciais de login social, por exemplo.

O objetivo da gestão de identidade federada é compartilhar informações de identidade automaticamente entre as fronteiras empresariais. Do ponto de vista do usuário individual, isso significa um único login em várias redes.

É imperativo que as organizações examinem as informações de identificação que são compartilhadas com parceiros, mesmo dentro do mesmo grupo corporativo. O compartilhamento de números de CPF, nomes e endereços pode permitir que ladrões de identidade roubem essas informações de um parceiro para cometer fraudes. A maneira mais comum de proteger a identidade federada é vincular a identidade do usuário a dispositivos autorizados, como estações de trabalho e telefones.

## 39.2.7 Métodos de Autenticação

Como mencionamos anteriormente, os usuários comprovam sua identidade com um nome de usuário ou ID. Além disso, os usuários precisam verificar sua identidade fornecendo um dos seguintes:

**Selecione os títulos para obter informações sobre os métodos de autenticação.**

### O que você sabe
Senhas, frases secretas ou PINs são exemplos de algo que o usuário conhece. As senhas são o método mais popular usado para autenticação.

Os termos passphrase, passcode, passkey e PIN são geralmente referidos genericamente como senha. Uma senha é uma string de caracteres protegidos usada para comprovar a identidade de um usuário. Se essa sequência de caracteres estiver relacionada a um usuário (por exemplo, se for seu nome, data de nascimento ou endereço), será mais fácil para os cibercriminosos adivinharem a senha desse usuário.

Várias publicações recomendam que uma senha tenha pelo menos oito caracteres. Os usuários não devem criar uma senha muito grande que seja difícil de memorizar ou, por outro lado, tão pequena que se torne vulnerável à quebra de senha. A complexidade da senha deve incluir uma combinação de letras maiúsculas e minúsculas, números e caracteres especiais.

Os usuários precisam usar senhas diferentes para sistemas diferentes porque, se um criminoso quebrar a senha do usuário uma vez, o criminoso terá acesso a todas as contas do usuário. Um gerenciador de senhas pode ajudá-lo a criar e usar senhas fortes — e torna desnecessário lembrar tantas senhas complexas.


### O que você tem
Os cartões inteligentes e os dispositivos de segurança são exemplos de objetos que os usuários possuem e que podem ser usados para fins de autenticação.

Um cartão inteligente é um pequeno cartão de plástico, do tamanho de um cartão de crédito, com um pequeno chip embutido nele. O chip é um portador de dados inteligente, capaz de processar, armazenar e proteger dados. Os cartões inteligentes contêm informações privadas, como números de contas bancárias, identificação pessoal, registros médicos e assinaturas digitais, usando criptografia para manter os dados seguros e fornecer um meio de autenticação.

Um chaveiro de segurança é um dispositivo pequeno o suficiente para ser anexado a um chaveiro. Na maioria dos casos, as chaves de segurança são usadas para autenticação de dois fatores (2FA), que é muito mais segura do que uma combinação de nome de usuário e senha.

Por exemplo, vamos supor que você queira acessar o seu banco online, que utiliza autenticação em duas etapas. Primeiro, insira seu nome de usuário (identificação). Em seguida, você insere a senha, que é o seu primeiro fator de autenticação. Depois disso, você precisa de um segundo meio de autenticação, pois o sistema usa 2FA. Você insere um PIN no seu dispositivo de segurança, e ele exibe um número. Isso prova que você tem acesso físico a este dispositivo, que foi emitido para você. Este número é o segundo fator. Você o insere para fazer login na conta do e-banking.

### Quem você é
Características físicas únicas, como impressão digital, padrão de retina ou impressão de voz. Essas características biométricas pessoais identificam exclusivamente uma pessoa específica. A segurança biométrica compara as características físicas aos perfis armazenados para autenticar os usuários. Neste caso, um perfil é um arquivo de dados contendo características conhecidas de um indivíduo. O sistema concede ao usuário o acesso se suas características corresponderem às informações salvas em seu perfil. Um leitor de impressão digital é um dispositivo biométrico comum.

Existem dois tipos de identificadores biométricos:

Características físicas — impressões digitais, DNA, rosto, mãos, retina ou características da orelha.
Características comportamentais — padrões de comportamento como gestos, voz, caminhar ou ritmo de digitação.
A biometria está se tornando cada vez mais popular em sistemas de segurança pública, dispositivos eletrônicos do consumidor e aplicações de ponto de venda. Implementar biometria envolve um leitor ou dispositivo de escaneamento, um software que converte as informações escaneadas em formato digital e um banco de dados que armazena os dados biométricos para comparação.

## 39.2.8 Senhas

É importante usar senhas fortes para proteger dispositivos de rede. Estas são as diretrizes padrão a serem seguidas:

- Use uma senha de pelo menos 8 caracteres, preferencialmente 10 ou mais caracteres. Uma senha mais longa é uma senha mais segura.
- Use senhas complexas. Inclua uma combinação de letras maiúsculas e minúsculas, números, símbolos e espaços, se permitido.
- Evite as senhas com base em repetição, palavras comuns de dicionário, sequências de letras ou números, nomes de usuário, nomes de parentes ou de animais de estimação, informações biográficas, como datas de nascimento, números de identificação, nomes de antepassados ou outras informações facilmente identificáveis.
- Deliberadamente, soletre errado uma senha. Por exemplo, Smith = Smyth ou 5mYth ou Security = 5ecur1ty.
- Altere as senhas periodicamente. Se uma senha for inconscientemente comprometida, a janela de oportunidade para o agente de ameaças usar a senha é limitada.
- Não anote as senhas e muito menos as deixe em locais óbvios, como em sua mesa ou no monitor.

As tabelas mostram exemplos de senhas fortes e fracas.

|Senha Fraca|Por que ela é fraca?|
|---|---|
|secret|Senha simples de dicionário|
|smith|Nome de solteira da mãe|
|toyota|Fabricante de um carro|
|bob1967|Nome e data de nascimento do usuário|
|Blueleaf23|Palavras e números simples|

|Senha Forte|Por que ela é forte?|
|---|---|
|b67n42d39c|Combina caracteres alfanuméricos|
|12^h u4@1p7|Combina caracteres alfanuméricos, símbolos e inclui um espaço|

Nos roteadores Cisco, os espaços à esquerda são ignorados em senhas, mas os espaços após o primeiro caractere não são ignorados. Portanto, um método para criar uma senha forte é utilizar a barra de espaço e criar uma frase feita de muitas palavras. Isso se chama frase secreta. Uma frase secreta é geralmente mais fácil de lembrar do que uma senha simples. Também é maior e mais difícil de ser descoberta.

**Gerenciadores de senhas**

Use um gerenciador de senhas para proteger as senhas das suas atividades online na internet. Considerada a melhor prática para proteger as senhas, o Gerenciador de Senhas gera automaticamente senhas complexas para você e as inserirá automaticamente quando você acessar esses sites. Você só precisa inserir uma senha principal para ativar esse recurso.

**Autenticação de múltiplos fatores**

Use a autenticação de múltiplos fatores sempre que disponível. Isso significa que a autenticação requer dois ou mais meios independentes de verificação. Por exemplo, quando você insere uma senha, também terá que inserir um código que é enviado para você por meio de e-mail ou mensagem de texto.

## 39.2.9 Autenticação Multifator
Como abordamos anteriormente, a autenticação multifatorial usa pelo menos dois métodos de verificação - como uma senha e algo que você tem, por exemplo, um chaveiro de segurança. Isso pode ser levado um passo adiante adicionando algo que você é, como uma verificação de impressão digital.

A autenticação multifator pode reduzir a incidência de roubo de identidade online porque significa que saber uma senha não dará aos cibercriminosos acesso à conta de um usuário.

Por exemplo, um site de banco on-line pode exigir uma senha e um PIN que o usuário recebe em seu smartphone. Nesse caso, o primeiro fator é a senha e o segundo, o PIN temporário, porque prova que você tem acesso ao que é registrado como seu telefone.

Retirar dinheiro de um caixa eletrônico é outro exemplo simples de autenticação multifatorial, pois o usuário deve ter o cartão do banco e saber o PIN antes de o caixa eletrônico distribuir dinheiro.

Observe que a autenticação de dois fatores (2FA) é um método de autenticação de vários fatores que envolve dois fatores em particular, mas os dois termos são frequentemente usados de forma alternada.

## 39.2.10 Autorização
A autorização controla o que um usuário pode e não pode fazer na rede após a autenticação com sucesso. Depois que um usuário prova sua identidade, o sistema verifica quais recursos de rede o usuário pode acessar e o que pode fazer com os recursos.

Selecione os ícones de alfinete para obter mais informações.

**Quando implementar a autorização**

A autorização utiliza um conjunto de atributos que descreve o acesso do usuário à rede para responder à pergunta 'Quais são os privilégios de leitura, cópia, edição, criação e exclusão que esse usuário tem para cada recurso ao qual ele pode acessar?' Também pode especificar o dia e a hora em que um usuário pode acessar esses recursos.

O sistema compara esses atributos com as informações contidas no banco de dados de autenticação, determina um conjunto de restrições para aquele usuário e o entrega ao dispositivo local onde o usuário está conectado.

A autorização é automática e não exige que os usuários executem etapas adicionais após a autenticação. Os administradores do sistema configuraram a rede para implementar a autorização imediatamente após a autenticação do usuário.

**Como implementar a autorização**

Definir as regras de autorização é a primeira etapa no controle de acesso. Uma política de autorização estabelece essas regras.

Uma política de associação baseada em grupo define a autorização com base nos membros de um grupo específico. Todos os funcionários de uma empresa podem ter um cartão de furto, por exemplo, que fornece acesso às instalações, mas pode não permitir o acesso a uma sala do servidor. Pode ser que apenas funcionários de nível sênior e membros da equipe de TI possam acessar a sala do servidor com seus cartões de furto.

Uma política de nível de autoridade define as permissões de acesso com base na posição de um funcionário na organização.

## 39.2.11. Contabilidade
Siga as setas para descobrir mais sobre o terceiro controle de acesso administrativo, que é a contabilidade.

**O que é contabilidade?**

A Contabilidade rastreia as ações de uma pessoa ou processo. A Contabilidade então coleta essas informações e relata os dados de uso. A empresa pode usar esses dados para determinadas finalidades, como auditoria ou cobrança. Os dados coletados podem incluir a hora de login para um usuário, independentemente de o login de usuário ter sido bem ou malsucedido ou quais recursos de rede o usuário acessou. Isso permite que uma empresa rastreie as ações, erros e erros durante uma auditoria ou investigação.

**Implementar a Contabilidade**

A implementação da contabilidade inclui  tecnologias, políticas, procedimentos e educação. Os arquivos de log fornecem as informações de detalhes com base nos parâmetros escolhidos. Por exemplo, uma empresa pode procurar falhas e sucessos de login. As falhas de login podem indicar que um criminoso tentou invadir uma conta, e os sucessos de login informam à empresa quais usuários estão usando quais recursos e quando.

As políticas e procedimentos da organização especificam quais ações devem ser registradas e como os arquivos de log são gerados, revisados e armazenados.

**Fornecer Contabilidade**

A retenção de dados, o descarte de mídia e os requisitos de conformidade fornecem todos os elementos contábeis. Muitas leis exigem a implementação de medidas para proteger diferentes tipos de dados. Essas leis orientam uma empresa sobre o caminho certo para manusear, armazenar e eliminar dados. A educação e conscientização dos usuários sobre as políticas, procedimentos e leis relacionadas de uma organização também podem contribuir para a contabilidade.

## 39.2.12 Verifique sua Compreensão - Controle de Acesso

Um membro da equipe de contabilidade deixou o token de segurança no trem a caminho do trabalho. A equipe de segurança cibernética deseja garantir que este incidente não leve a uma violação de segurança. Qual é a combinação de autenticação multifator mais segura a ser usada para evitar tal violação de segurança?

- [ ] Um chaveiro de segurança (security key fob) e um cartão inteligente (smart card)
- [ ] Senha e PIN de usuário
- [x] Impressão digital, PIN e chave de segurança FOB
- [ ] Cartão inteligente, PIN e chave de segurança FOB

Está certo.

Impressão digital, PIN e chave de segurança seriam a combinação de autenticação mais segura, pois cada um dos requisitos de segurança requer um método de autenticação diferente - algo que você sabe (PIN), algo que você possui (chave de segurança) e quem você é (impressão digital).

## 39.2.13 Vídeo - Configurar controle de acesso

**Pressione o botao Play para assistir o vídeo.**

**Autenticação e autorização** são processos de segurança distintos no mundo da identidade e gerenciamento de acesso. A autenticação usa senha e outros métodos de identificação para confirmar que os usuários são quem dizem ser. Por outro lado, a autorização atribui permissões de usuário aos recursos que o usuário tem permissão para acessar.

Nessa atividade tutorada do Packet Tracer, **Configure o controle de acesso**, você irá configurar a autenticação e autorização para serviços de rede, inclusive acesso de rede sem fio, e-mail e serviços de FTP.

Esta atividade é aberta e se concentra no modo físico. No entanto, você pode concluí-la no modo lógico. Observe também que a maioria das tarefas nesta atividade é classificada.

---

## Parte 1: Configurar e usar credenciais de autenticação AAA

**Etapa 1.** Configurar as contas de usuário no servidor AAA. Navegue até a HQ e clique no armário, que é o chassi alto e preto do servidor, no canto inferior esquerdo. No rack direito, clique em AAA radius server, guia Serviços e, em seguida, AAA em Serviços. Ative o serviço AAA. Em "User setup," adicione os usuários "User1" e "User2" com a senha especificada nas instruções.

**Etapa 2.** Configurar a autenticação do cliente sem fio em HQ-Laptop-1. Volte para HQ e clique em HQ-Laptop-1 (localizado em duas salas à direita do armário de fiação). Clique na guia Config e, depois, clique na interface, clique em "Wireless0."

```
SSID: HQ-INT
Autenticação: WPA2
User ID: User1
Senha: passuserone!
```

Na seção Configuração de IP, clique em "DHCP". Aguarde alguns instantes até que a oferta de DHCP seja aceita. Verifique que HQ-Laptop-1 recebeu endereçamento e foi atribuído um endereço IP na rede 192.168.50.0/24.

Neste ponto, é importante observar que o rastreamento de pacotes nem sempre converge rapidamente quando estamos configurando o acesso sem fio. Se você estiver tendo problemas, consulte a nota nas instruções para esta etapa.

**Etapa 3.** Configurar a autenticação do cliente sem fio no HQ-Laptop-2. Clique em HQ-Laptop-2, localizado no canto superior direito de HQ. Repita as etapas anteriores para definir as configurações wireless para HQ-Laptop-2, use as credenciais "User2".

Observe que, às vezes, é necessário alternar entre DHCP e estático para forçar a convergência do DHCP. Veja se no HQ-Laptop-2 foi recebido endereçamento e atribuído um endereço na rede 192.168.50.0/24.

---

## Parte 2: Configurar e verificar serviços de e-mail

**Etapa 1.** Ative os serviços de e-mail e configure as contas de usuário de e-mail. Navegue para o armário de fiação. No rack do lado direito, clique em "Servidor de e-mail", guia Serviços, e depois em "E-mail" em "Serviços". Ative os serviços SMTP e POP3.

```
Nome de domínio: mail.cyberhq.com
```

Em Configuração do usuário, digite as combinações de nome de usuário e senha das instruções.

**Etapa 2.** Configure os clientes de e-mail. Navegue de volta para HQ e clique em PC1-1, localizado no canto inferior. Clique na guia "Desktop", "E-mail". As configurações de e-mail devem abrir.

```
Seu nome: Suk-Yi
Seu e-mail: HQuser1@mail.cyberhq.com
Servidor de e-mail de entrada: mail.cyberhq.com
Servidor de e-mail de saída: mail.cyberhq.com
Nome de usuário: HQuser1
Senha: cisco123
```

Clique em "Salvar". Use as informações na tabela em suas instruções para configurar o e-mail nas configurações de PC2-3, HQ-Laptop-1 e Net-Admin.

PC2-3 está no escritório abaixo da sala de conferência. O PC Net-Admin está no armário de distribuição.

**Etapa 3.** Enviar um e-mail como Suk-Yi. No PC1-1, clique em "Escrever". Escreva um email para Ajulo em BRuser1@mail.cyberhq.com. Insira um assunto e uma mensagem de e-mail de sua escolha, clique em "Enviar" quando terminar.

Observe que o Packet Tracer pode levar vários segundos para convergir antes de receber a mensagem "Send Success" localizada na parte inferior da janela. Observe também que o Packet Tracer não classifica esta etapa.

Verifique se você concluiu esta etapa corretamente verificando se o Ajulo recebeu o e-mail. Navegue até o PC2-3. Clique em "Receber" e leia o e-mail de Suk-Yi.

---

## Parte 3: Configurar e usar serviços de FTP

**Etapa 1.** Ative o serviço FTP. Navegue para o armário de fiação. No rack do lado direito, clique em "Servidor FTP", guia "Serviços", e depois em "FTP" em "Serviços". Ative o serviço FTP.

**Etapa 2.** Criar as contas de usuário de FTP. Em Configuração do usuário, digite os nomes de usuário, as senhas, e os privilégios listados nas instruções. Clique em "Adicionar" para adicionar cada usuário.

Observe que o nome de usuário "Malia" não inclui os privilégios de exclusão.

Verifique se cada usuário foi criado corretamente e feche a janela do servidor.

**Etapa 3.** Transferir arquivos entre Net-Admin e o servidor FTP. Clique em "Net-Admin PC", clique na guia Área de trabalho, clique em Command Prompt. Insira o comando:

```
FTP 192.168.75.2
```

para logar no servidor de FTP. E depois autenticar com o nome de usuário `sukyi` e a senha `cisco123`.

Insira o comando para listar os arquivos no servidor FTP:

```
dir
```

Use o comando para baixar o arquivo `amessage.txt`:

```
get amessage.txt
```

Saia da sessão de FTP. Feche o prompt de comando, clique em editor de texto, e, em seguida, em "Abrir arquivo". Abra o arquivo baixado, "amessage.txt": "Saudações. Você conseguiu acesse o servidor de FTP"

Clique em "File-New", digite uma mensagem de sua escolha. Clique em "File-Save" e salve a nova mensagem como "amessage_new.txt". Feche o Text Editor (Editor de Texto) quando terminar.

Clique em Prompt de comando e faça logon novamente no servidor FTP como usuário `sukyi`. Use o comando para subir o arquivo:

```
put amessage_new.txt
```

Saia da sessão de FTP.

**Etapa 4.** Verificar se os privilégios de usuário do FTP estão funcionando como configurado. Volte para a HQ e clique em HQ-Laptop-1. Feche o navegador. Clique em Command Prompt para logar no servidor de FTP:

```
FTP 192.168.75.2
```

com o nome de usuário `malia` e a senha `cisco123`.

Use o comando para tentar remover o arquivo novo:

```
delete amessage_new.txt
```

Observe que a permissão é negada. Lembre-se de que o usuário Malia não tem direitos de exclusão. No entanto, ela tem direitos de renomeação. Use o comando para tentar alterar o nome:

```
rename amessage_new.txt amessage_renamed.txt
```

E o arquivo é renomeado com sucesso. Saia da sessão de FTP e feche o HQ-Laptop-1.

Isso termina essa atividade do Packet Tracer, Configure o controle de acesso. Você também pode verificar que você concluiu na atividade ao olhar para "Verificar resultados".


## 39.2.14 Packet Tracer - Configurar Controle de Acesso

Nesta atividade do Packet Tracer, você completará os seguintes objetivos:

- Parte 1: Configurar e usar credenciais de autenticação AAA
- Parte 2: Configurar e Verificar Serviços de E-mail
- Parte 3: Configurar e usar serviços de FTP


# 39.3 Defesa de sistemas e dispositivos

## 39.3.1 Segurança do sistema operacional

O que uma organização precisa fazer para **fortalecer** e manter a segurança de um sistema operacional?

**Selecione as setas para descobrir.**

**Um bom administrador**

Um bom administrador configurará o sistema operacional para proteger contra ameaças externas. Isso significa remover todos os programas e serviços desnecessários e garantir que as correções de segurança e as atualizações sejam instaladas em tempo hábil para corrigir falhas e mitigar riscos.


**Uma abordagem sistemática**

É importante ter uma abordagem sistemática para lidar com as atualizações do sistema. Uma empresa deve:

- estabelecer procedimentos para monitorar informações relacionadas à segurança.
- avaliar atualizações para aplicabilidade.
- planejar a instalação de atualizações e patches de aplicativos.
- instalar atualizações usando um plano documentado.


**Uma linha de base**

Outra maneira crítica de proteger um sistema operacional é identificar possíveis vulnerabilidades. Para fazer isso, estabeleça um parâmetro para comparar o desempenho de um sistema com as expectativas do parâmetro.


## 39.3.2 O que você sabe sobre antimalware?

Combine a descrição com o respectivo tipo de categoria de proteção.

|Item|Classificação|
|---|---|
|Verificações em busca de keyloggers (um programa que registra as teclas digitadas para roubar senhas e outras informações confidenciais) e outros tipos de spyware.|Proteção contra spyware|
|Bloqueia os endereços IP de sites de phishing conhecidos e alerta o usuário sobre emails suspeitos.|Proteção contra phishing|
|Monitora vírus. Avisa o usuário quando um vírus é detectado e o coloca em quarentena ou o exclui.|Proteção antivírus|
|Avisa o usuário sobre programas ou sites inseguros.|Verificação de fontes confiáveis / não confiáveis|
|Procura por programas que exibem anúncios indesejados em janelas popup.|Proteção contra adware|

## 39.3.3 Tipos de Antimalware

Você identificou tipos de antimalware que podem ser usados para proteger dispositivos finais, mas há mais a aprender. Vamos analisar alguns pontos importantes para lembrar sobre antimalware.

**Selecione cada título abaixo para obter algumas sugestões.**

**Cuidado com produtos antivírus invasores**

Tenha cuidado com produtos antivírus nocivos maliciosos que aparecem durante a navegação na Internet. A maioria exibe um anúncio ou pop-up que parece um aviso real do Windows. Eles avisam que o malware está infectando o computador e solicitam que o usuário o limpe. Mas eles não vêm de fontes legítimas, e clicar em qualquer lugar dentro da janela pode baixar e instalar malware.

**Ataques de malware sem arquivo são difíceis de detectar e remover**

O malware sem arquivo usa programas legítimos para infectar um computador. Indo direto para a memória, esse tipo de malware não depende de arquivos, então não deixa pegada. Um ataque sem arquivo termina quando o sistema é reiniciado. Vírus sem arquivo usam linguagens de script como o Windows PowerShell e são difíceis de detectar.


**Os scripts também podem ser malware**

Linguagens de script como Python, Bash (a linguagem de linha de comando para macOS da Apple e a maioria das distribuições Linux) ou Visual Basic for Applications (ou VBA, usado em macros da Microsoft) podem ser usadas para criar scripts que são malware.


**Sempre remova software não aprovado**

Software não aprovado ou não compatível pode ser instalado involuntariamente em um computador. Os usuários também podem instalar intencionalmente programas não autorizados. Embora o software não aprovado possa não ser mal-intencionado, ele ainda pode violar a política de segurança e interferir no software ou nos serviços de rede da empresa. O software não compatível deve ser removido imediatamente.


## 39.3.4 Gerenciamento de patches

Os criminosos digitais trabalham incansavelmente para explorar a fraqueza dos sistemas de computador. Para ficar um passo à frente, mantenha os sistemas seguros e atualizados com a instalação regular de patches.

**Selecione as setas para saber mais sobre o que são as correções e como funcionam.**

**O que são correções?**

Os patches são atualizações de código que os fabricantes fornecem para evitar que um vírus ou um worm recém-descoberto façam um ataque bem-sucedido. Patches e atualizações são frequentemente combinados em um service pack. Muitos ataques de malware poderiam ter sido evitados se os usuários instalassem o service pack mais recente.

Sistemas operacionais como o Windows verificam rotineiramente atualizações que podem proteger um computador contra as ameaças à segurança mais recentes. Isso inclui atualizações de segurança, atualizações críticas e service packs. O Windows pode ser configurado para baixar e instalar automaticamente atualizações de alta prioridade ou para notificar o usuário quando elas estiverem disponíveis.


**O que você precisa fazer?**

Como um profissional de segurança digital, é uma boa prática testar um patch antes de implantá-lo em toda a empresa. Uma ferramenta de gerenciamento de patches pode ser usada para gerenciar patches localmente, em vez de usar o serviço de atualização on-line do fornecedor.

Um serviço de patch automatizado fornece aos administradores um controle maior em vez de esperar pelos patches para download. Vejamos alguns dos benefícios

- Os administradores podem aprovar ou recusar atualizações.
- Os administradores podem forçar a atualização de sistemas para uma data específica.
- Os administradores podem obter relatórios sobre a atualização necessária para cada sistema.
- Cada computador não tem que se conectar ao serviço do fornecedor para baixar os patches. Um sistema obtém a atualização de um servidor local.
- Os usuários não podem desativar ou contornar as atualizações.

**Uma abordagem proativa**

Além de proteger o sistema operacional, é importante atualizar aplicativos de terceiros, como Adobe Acrobat, Java e Google Chrome, para solucionar vulnerabilidades que podem ser exploradas. Uma abordagem proativa ao gerenciamento de patches oferece segurança de rede e ajuda a evitar ransomware e outras ameaças.


## 39.3.5 Segurança de Endpoints

Uma solução de segurança baseada em host é um aplicativo de software executado em um dispositivo local (ou endpoint) para protegê-lo. O software funciona com o sistema operacional para ajudar a evitar ataques.

**Selecione as imagens para conhecer as opções de solução baseada em host.**

### Firewall baseado em host

Um firewall baseado em host é executado em um dispositivo para restringir a atividade de rede de entrada e saída desse dispositivo. Ele pode permitir ou negar tráfego entre o dispositivo e a rede. O firewall de software inspeciona e filtra os pacotes de dados para proteger o dispositivo contra a infecção. O Firewall do Windows, instalado por padrão durante a instalação do Windows, é um exemplo de firewall de software.

O usuário pode controlar o tipo de dados enviados de e para o computador abrindo ou bloqueando as portas selecionadas. Firewalls bloqueiam as conexões de rede de entrada e saída, a menos que exceções sejam definidas para permitir ou negar o tráfego para ou a partir das portas especificadas. Você pode selecionar "regras de entrada" para configurar os tipos de tráfego que têm permissão para passar pelo sistema, o que protegerá o sistema do tráfego indesejado.


### **Sistema de detecção de intrusão em host (HIDS)**

O HIDS é um software instalado em um host para monitorar e analisar atividades suspeitas. Ele monitora as chamadas do sistema e o acesso ao sistema de arquivos para detectar solicitações mal-intencionadas. Ele também pode monitorar informações de configuração sobre o dispositivo mantido no registro do sistema.

O HIDS armazena todos os dados de registro localmente. Ele também pode afetar o desempenho do sistema, pois é intensivo em recursos. Um HIDS não pode monitorar o tráfego de rede que não chega ao sistema hospedeiro, mas pode monitorar os processos do sistema operacional e do sistema crítico específicos desse hospedeiro.


### Sistema de prevenção de intrusão em host (HIPS)

O HIPS é um software que monitora um dispositivo em busca de ataques e anomalias (desvios de largura de banda, protocolos e portas), ou descobre sinais de alerta ao avaliar os protocolos reais em pacotes. Se detectar atividade maliciosa, a ferramenta HIPS pode enviar um alarme, registrar a atividade maliciosa, redefinir a conexão e/ou descartar os pacotes.


### **Detecção e Resposta de Endpoint (EDR)**

O EDR é uma solução de segurança integrada que monitora e coleta dados continuamente de um dispositivo de endpoint. Em seguida, ele analisa os dados e responde a todas as ameaças que detectar. Um antivírus só pode bloquear ameaças, enquanto o EDR pode fazer isso e encontrar ameaças no dispositivo.


### **Prevenção de Perda de Dados (DLP)**

As ferramentas de DLP fornecem uma maneira centralizada de garantir que dados sensíveis não sejam perdidos, utilizados de forma inadequada ou acessados por usuários não autorizados.


### **Firewall de Próxima Geração (NGFW)**

O NGFW é um dispositivo de segurança de rede que combina um firewall tradicional com outras funções de filtragem de dispositivos de rede. Um exemplo é um firewall de aplicação que utiliza inspeção profunda de pacotes (DPI) em linha em um sistema de proteção contra intrusões (IPS).

## 39.3.6 Criptografia do host

O recurso Windows Encrypting File System (EFS) permite que os usuários criptografem arquivos, pastas ou um disco rígido inteiro. A criptografia de disco completo (FDE) criptografa todo o conteúdo de uma unidade (incluindo arquivos temporários e memória). O Microsoft Windows usa o **BitLocker** para FDE.

Para usar o BitLocker, o usuário precisa habilitar um Módulo de Plataforma Confiável (TPM) na BIOS. Um TPM é um chip especializado na placa-mãe que armazena informações sobre o sistema host, como chaves de criptografia, certificados digitais e medições de integridade do sistema. Quando ativado, o BitLocker pode usar o chip do TPM.

Da mesma forma, o **BitLocker To Go** é uma ferramenta que criptografa unidades removíveis. Ele não usa um chip TPM, mas ainda criptografa os dados, exigindo uma senha para descriptografá-los. Unidades de autocriptografia (SEDS) criptografam automaticamente todos os dados na unidade para impedir que invasores acessem os dados por meio de seu sistema operacional. A criptografia SEDS é implementada no hardware da unidade pelo fabricante.

## 39.3.7 Integridade da inicialização

Os invasores podem atacar a qualquer momento, mesmo no curto espaço de tempo que um sistema leva para iniciar. É fundamental garantir que os sistemas e dispositivos permaneçam seguros durante a inicialização.

**Selecione as setas para descobrir como a integridade da inicialização funciona.**

**O que é integridade de inicialização?**

A integridade de inicialização garante que o sistema seja confiável e não tenha sido alterado enquanto o sistema operacional é carregado.

O firmware - instruções de software sobre as funções básicas do computador - é armazenado em um pequeno chip de memória na placa-mãe. O sistema básico de entrada / saída (BIOS) é o primeiro programa executado quando você liga o computador.

A Unified Extensible Firmware Interface (UEFI), uma versão mais recente do BIOS, define uma interface padrão entre o sistema operacional, o firmware e os dispositivos externos. Um sistema que usa UEFI é preferível a um que usa BIOS porque um sistema UEFI pode ser executado no modo de 64 bits.

**Como funciona a inicialização segura?**

A inicialização segura é um padrão de segurança para garantir que um dispositivo inicialize usando software confiável. Quando um sistema de computador é inicializado, o firmware verifica a assinatura de cada parte do software de inicialização, incluindo os drivers de firmware UEFI, aplicativos UEFI e o sistema operacional. Se as assinaturas forem válidas, o sistema inicializará e o firmware dará controle ao sistema operacional.


**O que é a inicialização medida?**

A inicialização medida fornece uma validação mais forte do que a inicialização segura. A inicialização medida mede cada componente, começando pelo firmware até os drivers de inicialização, e armazena as medidas no chip TMP para criar um log. O log pode ser testado remotamente para verificar o estado de inicialização do cliente. A inicialização medida pode identificar aplicativos não confiáveis que tentam carregar e também permite que o antimalware seja carregado mais cedo.


## 39.3.8 Recursos de segurança do sistema Apple

Como sabemos, as distribuições do Windows e Linux incluem recursos de segurança projetados para proteger endpoints. A Apple oferece hardware de sistema e recursos de segurança de macOS que também oferecem proteção avançada para endpoint.

Os recursos de segurança da Apple incluem o seguinte:

### Hardware com foco em segurança

A plataforma de hardware possui recursos avançados de segurança, como um processador de segurança especial, integridade de inicialização e um mecanismo dedicado de criptografia AES. Esses recursos estão incluídos em um sistema especial em um chip chamado Secure Enclave.

### Armazenamento criptografado

A criptografia de armazenamento de dados Apple Data Protection e FileVault é compatível com o mecanismo de criptografia AES de hardware. Isso permite a criptografia e a descriptografia de arquivos à medida que eles são gravados ou lidos, sem expor as chaves de criptografia para a CPU principal, sistema operacional ou aplicativos em execução.

### Inicialização segura

A ROM de inicialização protege o hardware de nível inferior e só permite a execução de software Apple OS genuíno e inalterado.

### Proteção a dados biométricos

Os dados de autenticação biométrica são processados no sistema de hardware de segurança. Isso o mantém separado do SO e da execução de software de aplicativo, incluindo malware.

### Find My Mac

O Find My Mac ajuda a encontrar dispositivos macOS perdidos ou roubados por meio da função de rastreamento de localização. Ele também permite o bloqueio remoto do dispositivo e o apagamento do armazenamento se dados essenciais estiverem em risco.

### XProtect

A tecnologia antimalware XProtect impede a execução de malware através da detecção de malware por assinatura. Ele também alerta os usuários sobre a existência de malware e oferece a opção de remover os arquivos de malware detectados.

### Ferramenta de remoção de malware (MRT)

A Ferramenta de Remoção de Malware (MRT) detecta e remove as infecções de malware atuais quando as regras de detecção são atualizadas automaticamente pela Apple. Ele também monitora infecções por malware na reinicialização do sistema e no login de usuários.

### Gatekeeper (Guardião)

O Gatekeeper garante que apenas o software autêntico, assinado digitalmente, criado por um desenvolvedor de software autenticado pela Apple, tenha permissão para ser instalado.

## 39.3.9 Proteção Física de Dispositivos

Você aprendeu muito sobre ameaças de software e hardware. Mas e quanto às potenciais ameaças físicas aos dispositivos e instalações?

**Selecione as setas para saber mais sobre as medidas de segurança que podem ser tomadas.**

**Equipamento de Informática**

Para proteger fisicamente os equipamento de informática:

- Utilize travas de cabo para proteger os dispositivos.
- Mantenha as salas de telecomunicações trancadas.
- Use gaiolas de segurança (gaiolas de Faraday) ao redor do equipamento para bloquear campos eletromagnéticos.

**Travas de portas**

O tipo mais comum de trava da porta é uma trava de entrada com uma chave padrão. Eles geralmente são fáceis de abrir. Uma trava de bloqueio pode ser adicionada para aumentar a segurança. Qualquer fechadura que requer uma chave é vulnerável se as chaves forem perdidas, roubadas ou duplicadas.

Uma fechadura cifrada usa botões que são pressionados em uma determinada sequência para abrir a porta. Pode ser programado para que o código de um usuário funcione apenas em determinados dias ou horários. Ele também pode manter um registro de quando a porta foi aberta e o código usado para abri-la.


**Sistemas de identificação por radiofrequência (RFID)**

A RFID (Radio Frequency Identification, Identificação por radiofrequência) usa ondas de rádio para identificar e rastrear objetos. Os sistemas de inventário de RFID usam tags fixadas em todos os itens que uma empresa quer rastrear. Os identificadores contêm um circuito integrado que se conecta a uma antena. As etiquetas RFID são pequenas e requerem muito pouca energia, por isso não precisam de uma bateria para trocar informações com um leitor. A tecnologia RFID pode ajudar a automatizar o rastreamento de ativos ou bloquear, desbloquear ou configurar dispositivos eletrônicos de forma wireless. Os cartões de crédito sem contato usam a tecnologia RFID.

## 39.3.10 Verifique sua compreensão - Sistemas e dispositivos de defesa

**Pergunta 1**

Qual característica descreve o malware sem arquivo?

- [ ] Ele registra as teclas pressionadas para acessar senhas, informações confidenciais e spyware.
- [ ] Ele usa os endereços IP de sites de phishing conhecidos.
- [x] Ele usa programas legítimos para infectar um computador.
- [ ] Ele exibe um anúncio ou pop-up que se parece com um aviso real do Windows.

Está certo.

O malware sem arquivo usa programas legítimos para infectar um computador. Indo direto para a memória, esse tipo de malware não depende de arquivos, então não deixa pegada.

**Pergunta 2**

Verdadeiro ou falso: Um sistema de detecção de invasão de host não pode monitorar o tráfego de rede que não atinge o sistema host.

- [x] Verdadeiro
- [ ] Falso

Está certo.

Um sistema de detecção de invasão do host (HIDS) não pode monitorar nenhum tráfego de rede que não chegue ao sistema do host, mas monitora o sistema operacional e processos críticos do sistema específicos desse host.

**Pergunta 3**

Qual dispositivo de segurança de rede baseado em host combina um firewall tradicional com outras funções de filtragem de dispositivos de rede, como DPI?

- [ ] HIPS
- [ ] EDR
- [x] NGFW
- [ ] HIDS

Está certo.

NGFW (Next-Generation Firewall) é um dispositivo de segurança de rede que combina um firewall tradicional com outras funções de filtragem de dispositivos de rede, como Inspeção Profunda de Pacotes (DPI).

**Pergunta 4**

Qual ferramenta da Microsoft pode ser usada para criptografar unidades removíveis sem o uso de um chip TPM?

- [ ] MRT
- [x] BitLocker To Go
- [ ] XProtect
- [ ] BitLocker

Está certo.

BitLocker To Go é uma ferramenta da Microsoft que criptografa unidades removíveis. Ele não utiliza um chip TPM, mas ainda assim criptografa os dados. Requer uma senha para descriptografar os dados.

**Pergunta 5**

Qual é a finalidade do chip TPM na placa-mãe?

- [ ] Ele é usado para verificar malware de keylogging instalado no sistema.
- [ ] É usado para criptografar todo o conteúdo de uma unidade (incluindo arquivos temporários e memória).
- [ ] É usado para detectar vírus sem arquivos usando linguagens de script como o Windows PowerShell.
- [x] Ele armazena informações sobre o sistema hospedeiro, como chaves de criptografia, certificados digitais e senhas.

Está certo.

TPM é um chip específico na placa-mãe que armazena informações específicas do sistema computacional como chaves de criptografia, certificados digitais e senhas.

**Pergunta 6**

Qual recurso de segurança da Apple protege o hardware de baixo nível e permite apenas a execução de software genuíno e não alterado do sistema operacional Apple?

- [ ] XProtect
- [ ] Gatekeeper (Guardião)
- [ ] MRT
- [x] Secure Boot

Está certo.

Secure Boot - O Boot ROM protege o hardware em nível baixo e permite apenas a execução de software genuíno e não adulterado do sistema operacional da Apple.


# 39.4 Proteção Antimalware

## 39.4.1 Ameaças a Endpoints

O termo “endpoint” é definido de várias maneiras. Para fins deste curso, podemos definir endpoints como hosts na rede que podem acessar ou ser acessados por outros hosts na rede. Isso obviamente inclui computadores e servidores, no entanto muitos outros dispositivos também podem acessar a rede. Com o rápido crescimento da Internet das Coisas (IoT), outros tipos de dispositivos são agora endpoints na rede. Isso inclui câmeras de segurança em rede, controladores e até mesmo lâmpadas e aparelhos. Cada ponto de extremidade é potencialmente uma forma de software malicioso obter acesso a uma rede. Além disso, as novas tecnologias, como a nuvem, expandem os limites das redes empresariais para incluir locais na Internet pelos quais as empresas não são responsáveis.

Uma pesquisa recente com profissionais de segurança cibernética perguntou aos participantes quais são os desafios de segurança com os quais eles mais se deparam. Conforme mostrado na figura, os três principais estão relacionados a ameaças de endpoint. O ransomware (53%) está no topo da lista, seguindo o recente aumento de ataques de ransomware. O próximo maior desafio de segurança é a mudança para o trabalho remoto e os riscos resultantes (47%), introduzidos após a pandemia de Covid-19. A visibilidade limitada das ameaças cibernéticas (41%) completa os três principais desafios de segurança enfrentados pelos profissionais de segurança cibernética.

![[Pasted image 20260706211026.png]]
## 39.4.2 Segurança de Endpoints

A mídia de notícias geralmente cobre ataques de rede externa em redes corporativas. Estes são alguns exemplos de tais ataques:

- Ataques de negação de serviço (DoS) em uma rede de uma organização têm como objetivo degradar ou até mesmo interromper o acesso público a ela.
- Violando o servidor web de uma organização para desfigurar sua presença na web.
- Violando os servidores de dados e hosts de uma organização para roubar informações confidenciais.

Vários dispositivos de segurança de rede são necessários para proteger o perímetro da rede contra acesso externo. Como mostrado na figura, esses dispositivos podem incluir um roteador reforçado que está fornecendo serviços VPN, um firewall de próxima geração (ASA, na figura), um appliance IPS e um servidor de serviços de autenticação, autorização e contabilidade (AAA) (Servidor AAA, na figura).

![[Pasted image 20260706211040.png]]

No entanto, muitos ataques se originam de dentro da rede. Portanto, proteger uma LAN interna é quase tão importante quanto proteger o perímetro externo da rede. Sem uma LAN segura, os usuários de uma organização ainda são suscetíveis a ameaças de rede e paralisações que podem afetar diretamente a produtividade e a margem de lucro de uma organização. Depois que um host interno é infiltrado, ele pode se tornar um ponto de partida para um invasor obter acesso a dispositivos críticos do sistema, como servidores e informações confidenciais.

Especificamente, há dois elementos LAN internos para proteger:

- **Endpoints -** Os hosts comumente consistem em laptops, desktops, impressoras, servidores e telefones IP, todos os quais são suscetíveis a ataques relacionados a malware.
- **Infraestrutura de rede -** Os dispositivos de infraestrutura de LAN interconectam os endpoints e geralmente incluem switches, dispositivos sem fio e dispositivos de telefonia IP. A maioria desses dispositivos é suscetível a ataques relacionados à LAN, incluindo ataques de estouro de tabela de endereços MAC, ataques de falsificação, ataques relacionados a DHCP, ataques de tempestade de LAN, ataques de manipulação de STP e ataques de VLAN.


## 39.4.3 Proteção contra malware baseada em host

O perímetro da rede está sempre se expandindo. As pessoas acessam recursos de rede corporativa com dispositivos móveis que usam tecnologias de acesso remoto, como VPN. Esses mesmos dispositivos também são usados em redes públicas e domésticas não seguras ou minimamente protegidas. Software antimalware/antivírus baseado em host e firewalls baseados em host são usados para proteger esses dispositivos.

**Software antivírus/antimalware**

Este é um software instalado em um host para detectar e mitigar vírus e malware. Exemplos são o Windows Defender Virus & Threat Protection, Cisco AMP for Endpoints, Norton Security, McAfee, Trend Micro e outros. Programas antimalware podem detectar vírus usando três abordagens diferentes:

- **Baseado em assinaturas -** Esta abordagem reconhece várias características de arquivos de malware conhecidos.
- **Baseado em heurísticas -** Esta abordagem reconhece características gerais compartilhadas por vários tipos de malware.
- **Baseado em comportamento -** Esta abordagem emprega a análise de comportamentos suspeitos.

Muitos programas antivírus são capazes de fornecer proteção em tempo real analisando dados conforme eles são usados pelo endpoint. Esses programas também verificam se há malware existente que pode ter entrado no sistema antes de ser reconhecível em tempo real.

A proteção antivírus baseada em host também é conhecida como baseada em agentes. O antivírus baseado em agente é executado em todas as máquinas protegidas. A proteção antivírus sem agente executa verificações em hosts a partir de um sistema centralizado. Os sistemas sem agente tornaram-se populares para ambientes virtualizados nos quais várias instâncias de SO estão sendo executadas em um host simultaneamente. Antivírus baseado em agente executado em cada sistema virtualizado pode ser um sério desperdício de recursos do sistema. O antivírus sem agente para hosts virtuais envolve o uso de um appliance virtual de segurança especial que executa tarefas de varredura otimizadas nos hosts virtuais. Um exemplo disso é o vShield da VMware.

**Firewall de host**

Este software está instalado em um host. Restringe conexões de entrada e saída a conexões iniciadas somente por esse host. Alguns softwares de firewall também podem impedir que um host se infecte e impedir que hosts infectados espalhem malware para outros hosts. Esta função está incluída em alguns sistemas operacionais. Por exemplo, o Windows inclui o Firewall do Windows Defender com Segurança Avançada, conforme mostrado na figura.

Outras soluções são produzidas por outras empresas ou organizações. As ferramentas Linux iptables e TCP Wrappers são exemplos. Os firewalls baseados em host são discutidos com mais detalhes posteriormente neste módulo.

**Suites de segurança baseadas em host**

Recomenda-se instalar um conjunto de produtos de segurança baseado em host em redes domésticas e também em redes comerciais. Esses pacotes de segurança baseados em host incluem antivírus, anti-phishing, navegação segura, sistema de prevenção de intrusões baseado em host e recursos de firewall. Essas várias medidas de segurança fornecem uma defesa em camadas que protegerá contra as ameaças mais comuns.

Além da funcionalidade de proteção fornecida pelos produtos de segurança baseados em host é a função de telemetria. A maioria dos softwares de segurança baseados em host inclui funcionalidade de registro robusta que é essencial para operações de segurança cibernética. Alguns programas de segurança baseados em host enviarão logs para um local central para análise.

Há muitos programas e pacotes de segurança baseados em host disponíveis para usuários e empresas. O laboratório de testes independente AV-TEST fornece análises de alta qualidade de proteções baseadas em host, bem como informações sobre muitos outros produtos de segurança.

Pesquise na Internet a organização AVTest para saber mais sobre o AV-TEST.


## 39.4.4 Proteção contra malware baseada em rede

![[Pasted image 20260706211235.png]]

As novas arquiteturas de segurança para a rede sem fronteiras enfrentam os desafios de segurança fazendo com que os endpoints usem elementos de varredura de rede. Esses dispositivos fornecem muito mais camadas de varredura do que um único ponto de extremidade possivelmente poderia. Dispositivos de prevenção de malware baseados em rede também são capazes de compartilhar informações entre si para tomar decisões melhor informadas.

A proteção de endpoints em uma rede sem fronteiras pode ser realizada usando técnicas baseadas em rede, bem como baseadas em host, como mostrado na figura acima. Veja a seguir exemplos de dispositivos e técnicas que implementam proteções de host no nível da rede.

- **Cisco Secure Endpoint -** É uma solução que fornece proteção para endpoints contra vírus e malware.
- **Cisco Secure Email -** É uma solução que oferece filtragem de SPAM e emails potencialmente maliciosos antes que eles cheguem ao endpoint. Um exemplo é o Cisco ESA.
- **Cisco Umbrella -** É uma solução que utiliza solicitações DNS para fornecer filtragem de websites e listas de bloqueio para evitar que hosts acessem locais perigosos na web. O Cisco Umbrella fornece controle sobre como os usuários acessam a internet e pode fazer cumprir políticas de uso aceitáveis, controlar o acesso a sites e serviços específicos e realizar varreduras em busca de malware.
- **Network Admission Control (NAC) -** Permite apenas sistemas autorizados e em conformidade se conectarem à rede.

## 39.4.5 Verifique sua compreensão - Proteção antimalware

**Pergunta 1**

Verdadeiro ou Falso: Endpoints são hosts ou dispositivos na rede que podem acessar ou serem acessados por outros hosts na rede.

- [x] Verdadeiro
- [ ] Falso

Está certo.

Os "endpoints" são quaisquer dispositivos que estão conectados à rede e podem ser acessados por outros dispositivos da rede.

**Pergunta 2**

Que tipo de software antimalware reconhece várias características de arquivos de malware conhecidos?

- [x] baseado em assinatura
- [ ] baseado em auto-navegação
- [ ] baseado no comportamento
- [ ] baseado em heurística

Está certo.

O software antivírus/antimalware baseado em assinaturas detecta vírus com base em detalhes específicos de arquivos de vírus.

**Pergunta 3**

Qual tipo de proteção de endpoint inclui iptables e TCP Wrappers?

- [ ] admissão e controle de rede
- [ ] software antivírus/antimalware
- [x] firewall baseado em host
- [ ] aparelho de segurança web

Está certo.

IPTABLES e TCP Wrappers são exemplos de software de firewall baseado em host baseado em Linux.

**Pergunta 4**

Quais dispositivos e técnicas fornecem filtragem de sites e listas de bloqueio para impedir que os endpoints acessem páginas da web maliciosas?

- [ ] Contra malware totalmente integrada
- [ ] Appliance de segurança de e-mail
- [ ] Admissão e controle de rede
- [x] Appliance de segurança web

Está certo.

Um appliance de segurança da Web filtra solicitações para a Internet e usa a lista negra para impedir que endpoints acessem sites mal-intencionados.

**Pergunta 5**

Que tipo de proteção de endpoint permite que apenas dispositivos autorizados e compatíveis se conectem à rede?

- [ ] Segurança baseada no host
- [ ] Firewall baseado em host
- [ ] Software antimalware
- [x] Admissão e Controle de Rede (NAC)

Está certo.

O Network Admission and Control (NAC) permite que apenas dispositivos autorizados e compatíveis acessem a rede.

# 39.5 Prevenção de Intrusão Baseada em Host e Firewalls

## 39.5.1 Firewalls

Operação de firewall

Um firewall é um sistema ou grupo de sistemas que aplica uma política de controle de acesso entre redes.

Reproduza a animação na figura para visualizar um firewall em operação.

# Operação de firewall
![[brave_aQl4pBua23.mp4]]

Clique em cada botão para saber mais sobre firewalls.

### **Propriedades comuns do Firewall**

Todos os firewalls compartilham algumas propriedades comuns:

- Os firewalls são resistentes a ataques de rede.
- Firewalls são o único ponto de trânsito entre redes corporativas internas e redes externas porque todo o tráfego flui através do firewall.
- Firewalls reforçam a política de controle de acesso.

### **Benefícios do firewall**

Existem vários benefícios do uso de um firewall em uma rede:

- Eles impedem a exposição de hosts, recursos e aplicações sensíveis a usuários não confiáveis.
- Eles sanitizam o fluxo do protocolo, o que impede a exploração de falhas no protocolo.
- Eles bloqueiam dados maliciosos de servidores e clientes.
- Eles reduzem a complexidade do gerenciamento de segurança descarregando a maior parte do controle de acesso à rede para alguns firewalls na rede.

### **Limitações do Firewall**

Os firewalls também têm algumas limitações:

- Um firewall mal configurado pode ter sérias conseqüências para a rede, como se tornar um único ponto de falha.
- Os dados de muitos aplicativos não podem ser transmitidos por firewalls com segurança.
- Os usuários podem procurar proativamente maneiras de contornar o firewall para receber material bloqueado, o que expõe a rede a possíveis ataques.
- O desempenho da rede pode diminuir.
- O tráfego não autorizado pode ser encapsulado ou escondido como tráfego legítimo através do firewall.

## 39.5.2 Tipos de Firewall

É importante entender os diferentes tipos de firewalls e suas capacidades específicas para que o firewall correto seja usado para cada situação.

### **Firewall de filtragem de pacotes (sem estado)**

Os firewalls de filtragem de pacotes geralmente fazem parte de um firewall de roteador, que permite ou nega tráfego com base nas informações da Camada 3 e da Camada 4. Eles são firewalls sem estado que usam uma simples pesquisa de tabela de políticas que filtra o tráfego com base em critérios específicos.

Por exemplo, os servidores SMTP escutam a porta 25 por padrão. Um administrador pode configurar o firewall de filtragem de pacotes para bloquear a porta 25 de uma estação de trabalho específica para evitar que ela transmita um vírus de e-mail.

![[Pasted image 20260706212123.png]]

### **Firewall com monitoração de estado**

Firewalls com estado são as tecnologias de firewall mais versáteis e mais comuns em uso. Os firewalls stateful fornecem filtragem de pacotes stateful usando informações de conexão mantidas em uma tabela de estado. Filtragem com estado é uma arquitetura de firewall classificada na camada de rede. Ele também analisa o tráfego na camada 4 da OSI e na camada 5.![[Pasted image 20260706212139.png]]

### **Firewall de gateway de aplicativo**

Um firewall de gateway de aplicação (firewall proxy), conforme mostrado na figura, filtra as informações nas camadas 3, 4, 5 e 7 do modelo de referência OSI. A maior parte do controle e filtragem do firewall é feita em software. Quando um cliente precisa acessar um servidor remoto, ele se conecta a um servidor proxy. O servidor proxy se conecta ao servidor remoto em nome do cliente. Portanto, o servidor só vê uma conexão do servidor proxy.![[Pasted image 20260706212153.png]]

### **Firewall de próxima geração**

Os firewalls de última geração (NGFW) vão além dos firewalls de estado, fornecendo:

- Prevenção de intrusão integrada
- Reconhecimento e controle de aplicativos para ver e bloquear aplicativos arriscados
- Caminhos de atualização para incluir futuros feeds de informações
- Técnicas para lidar com ameaças de segurança em evolução
![[Pasted image 20260706212206.png]]

Outros métodos de implementação de firewalls incluem:

- **Firewall baseado em host (servidor e pessoal) -**Um PC ou servidor com software de firewall em execução.
- **Firewall transparente -** Filtra o tráfego IP entre um par de interfaces em modo bridge.
- **Firewall híbrido -** Uma combinação dos vários tipos de firewalls. Por exemplo, um firewall de inspeção de aplicações combina um firewall com estado com um firewall de gateway de aplicativo.


## 39.5.3 Verifique sua compreensão - Identifique o tipo de Firewall

Verifique sua compreensão dos tipos de firewalls escolhendo a MELHOR resposta para as seguintes perguntas.

**Pergunta 1**

Que tipo de firewall filtra informações nas Camadas 3, 4, 5 e 7 do modelo de referência OSI?

- [ ] Baseado em host
- [ ] Híbrido
- [x] Gateway de Aplicativo
- [ ] Filtragem de pacotes
- [ ] Com estado

Está certo.

Um firewall de gateway de aplicativo filtra informações nas Camadas 3, 4, 5 e 7 do modelo de referência OSI.

**Pergunta 2**

Que tipo de firewall é uma combinação de vários tipos de firewall?

- [x] Híbrido
- [ ] Filtragem de pacotes
- [ ] NGFW (Última geração)
- [ ] Proxy
- [ ] Baseado em host
- [ ] Com estado
- [ ] Transparent (Transparente)

Está certo.

Um firewall híbrido é uma combinação dos vários tipos de firewall.

**Pergunta 3**

Que tipo de firewall faz parte de um firewall de roteador, permitindo ou negando tráfego com base nas informações da Camada 3 e da Camada 4?

- [ ] Baseado em host
- [ ] Híbrido
- [ ] NGFW (Última geração)
- [x] Filtragem de pacotes
- [ ] Transparent (Transparente)
- [ ] Proxy

Está certo.

Um firewall de filtragem de pacotes faz parte de um firewall de roteador que permite ou nega tráfego com base nas informações da Camada 3 e da Camada 4.

**Pergunta 4**

Que tipo de firewall é um PC ou servidor com software de firewall em execução?

- [ ] Proxy
- [ ] Híbrido
- [ ] Filtragem de pacotes
- [ ] Transparent (Transparente)
- [ ] Com estado
- [ ] NGFW (Última geração)
- [x] Baseado em host

Está certo.

Firewalls baseados em host é um PC ou servidor com software de firewall em execução nele.

**Pergunta 5**

Que tipo de firewall filtra o tráfego IP entre um par de interfaces em ponte?

- [ ] Baseado em host
- [ ] Proxy
- [ ] NGFW (Última geração)
- [ ] Com estado
- [ ] Filtragem de pacotes
- [x] Transparent (Transparente)
- [ ] Híbrido

Está certo.

Um firewall transparente filtra o tráfego IP entre um par de interfaces em ponte.

## 39.5.4 Benefícios e Limitações do firewall de Filtragem de Pacotes

Os firewalls de filtragem de pacotes geralmente fazem parte de um firewall de roteador, que permite ou nega tráfego com base nas informações da Camada 3 e da Camada 4. Eles são firewalls sem estado que usam uma consulta de tabela de política simples que filtra o tráfego com base em critérios específicos, conforme mostrado na figura. Por exemplo, os servidores SMTP escutam a porta 25 por padrão. Um administrador pode configurar o firewall de filtragem de pacotes para bloquear a porta 25 de uma estação de trabalho específica para evitar que ela transmita um vírus de e-mail.
![[Pasted image 20260706212416.png]]

Existem várias vantagens de usar um firewall de filtragem de pacotes:

- Os filtros de pacote implementam conjuntos de regras de permissão simples ou negam.
- Os filtros de pacotes têm um baixo impacto no desempenho da rede.
- Os filtros de pacotes são fáceis de implementar e são suportados pela maioria dos roteadores.
- Os filtros de pacote fornecem um grau inicial de segurança na camada de rede.
- Os filtros de pacotes executam quase todas as tarefas de um firewall high-end a um custo muito menor.

Os filtros de pacotes não representam uma solução de firewall completa, mas são um elemento importante de uma política de segurança de firewall. Existem várias desvantagens de usar um firewall de filtragem de pacotes:

- Os filtros de pacote de informação são suscetíveis à falsificação de IP. Os atores de ameaça podem enviar pacotes arbitrários que atendem aos critérios ACL e passam pelo filtro.
- Os filtros de pacotes não filtram de forma confiável pacotes fragmentados. Como os pacotes IP fragmentados carregam o cabeçalho TCP no primeiro fragmento e filtro de filtros de pacote na informação de cabeçalho TCP, todos os fragmentos após o primeiro fragmento são passados incondicionalmente. As decisões de usar filtros de pacote supõem que o filtro do primeiro fragmento impõe com precisão a política.
- Os filtros de pacotes usam ACLs complexas, que podem ser difíceis de implementar e manter.
- Os filtros de pacotes não podem filtrar dinamicamente determinados serviços. Por exemplo, as sessões que usam negociações de porta dinâmica são difíceis de filtrar sem abrir o acesso a toda uma variedade de portas.

Os filtros de pacotes são sem estado. Eles examinam cada pacote individualmente ao invés de verificar o contexto do estado de uma conexão.


## 39.5.5 Vantagens e Limitações do Firewall de Estado

Existem vários benefícios em usar um firewall com estado em uma rede:

- Firewalls com estado são frequentemente usados como um meio primário de defesa, filtrando tráfego indesejado ou desnecessário.
- Firewalls com estado fortalecem a filtragem de pacotes fornecendo um controle mais rigoroso sobre a segurança.
- Firewalls com estado melhoram o desempenho em relação aos filtros de pacotes ou servidores proxy.
- Firewalls com estado se defendem contra ataques de falsificação e DoS, determinando se os pacotes pertencem a uma conexão existente ou são de uma origem não autorizada.
- Firewalls com estado fornecem mais informações de log do que um firewall de filtragem de pacotes.

Os firewalls com estado também apresentam algumas limitações:

- Firewalls com estado não podem evitar ataques à camada de aplicativo porque não examinam o conteúdo real da conexão HTTP.
- Nem todos os protocolos são stateful. Por exemplo, o UDP e o ICMP não geram informações de conexão para uma tabela de estado e, portanto, não conseguem tanto suporte para filtragem.
- É difícil rastrear conexões que usam negociação de porta dinâmica. Algumas aplicações abrem várias conexões. Isso requer uma nova gama de portas que devem ser abertas para permitir esta segunda conexão.
- Firewalls com estado não suportam autenticação de usuário.

|Vantagens|Limitações|
|---|---|
|Meios primários de defesa|Sem inspeção de camada de aplicativo|
|Filtragem forte de pacotes|Rastreamento limitado de protocolos sem estado|
|Melhor desempenho em relação a filtros de pacotes|Difícil de defender contra a negociação com portas dinâmicas|
|Defende-se contra ataques de falsificação e DoS|Sem suporte de autenticação|
|Registro de dados mais rico||

## 39.5.6 Firewalls baseados em host

Firewalls pessoais baseados em host são programas de software autônomos que controlam o tráfego que entra ou sai de um computador. Aplicativos de firewall também estão disponíveis para telefones e tablets Android.

Firewalls baseados em host podem usar um conjunto de políticas predefinidas, ou perfis, para controlar pacotes que entram e saem de um computador. Eles também podem ter regras que podem ser diretamente modificadas ou criadas para controlar o acesso com base em endereços, protocolos e portas. Aplicativos de firewall baseados em host também podem ser configurados para emitir alertas aos usuários se um comportamento suspeito for detectado. Eles podem então oferecer ao usuário a capacidade de permitir que um aplicativo ofensivo seja executado ou ser impedido de ser executado no futuro.

O registro varia dependendo do aplicativo de firewall. Normalmente, inclui a data e a hora do evento, se a conexão foi permitida ou negada, informações sobre os endereços IP de origem ou destino dos pacotes e as portas de origem e destino dos segmentos encapsulados. Além disso, atividades comuns, como pesquisas de DNS e outros eventos de rotina, podem aparecer em logs de firewall baseados em host, portanto, filtragem e outras técnicas de análise são úteis para inspecionar grandes quantidades de dados de log.

Uma abordagem para a prevenção de intrusões é o uso de firewalls distribuídos. Os firewalls distribuídos combinam recursos de firewalls baseados em host com gerenciamento centralizado. A função de gerenciamento envia regras para os hosts e também pode aceitar arquivos de log dos hosts.

Independentemente de serem instalados completamente no host ou distribuídos, os firewalls baseados em host são uma camada importante de segurança de rede, juntamente com firewalls baseados em rede. Aqui estão alguns exemplos de firewalls baseados em host:

### Firewall do Windows Defender

Incluído pela primeira vez no Windows XP, o Firewall do Windows (agora Windows Defender Firewall) usa uma abordagem baseada em perfil para a funcionalidade do firewall. O acesso a redes públicas é atribuído ao perfil restritivo do firewall Público. O perfil Privado é para computadores que estão isolados da Internet por outros dispositivos de segurança, como um roteador doméstico com funcionalidade de firewall. O perfil Domínio é o terceiro perfil disponível. Ele é escolhido para conexões com uma rede confiável, como uma rede de negócios que se supõe ter uma infra-estrutura de segurança adequada. O Firewall do Windows tem funcionalidade de registo e pode ser gerido centralmente com políticas de segurança de grupo personalizadas a partir de um servidor de gestão, como o System Center 2012 Configuration Manager.

### iptables

Este é um aplicativo que permite aos administradores do sistema Linux configurar regras de acesso à rede que fazem parte dos módulos Netfilter do kernel Linux.


### nftables

O sucessor do iptables, o nftables é um aplicativo de firewall do Linux que usa uma máquina virtual simples no kernel do Linux. O código é executado dentro da máquina virtual que inspeciona pacotes de rede e implementa regras de decisão relativas à aceitação e encaminhamento de pacotes.

### Wrappers TCP

Este é um sistema de registro e controle de acesso baseado em regras para Linux. A filtragem de pacotes é baseada em endereços IP e serviços de rede.


## 39.5.7 Programas Antimalware

Malware inclui vírus, worms, cavalos de Troia, keyloggers, spyware, e adware. Eles são projetados para invadir a privacidade, roubar informações, danificar o computador ou corromper dados. É importante que você proteja os computadores e dispositivos móveis com software antimalware de qualidade. Os seguintes tipos de programas antimalware estão disponíveis:

### Proteção antivírus

Este programa monitora continuamente a presença de vírus. Quando um vírus é detectado, o usuário é avisado e o programa tenta colocar o vírus em quarentena ou excluí-lo.

### Proteção contra adware

Este programa procura continuamente por programas que exibam publicidade em seu computador.

### Proteção contra phishing

Este programa bloqueia os endereços IP de sites de phishing conhecidos e avisa o usuário sobre sites suspeitos.

### Proteção contra spyware

Este programa verifica keyloggers e outros spywares.

### Fontes confiáveis / não confiáveis

Este programa avisa sobre programas inseguros prestes a serem instalados ou sites inseguros antes de serem visitados.


## 39.5.8 Windows Defender Firewall

Um firewall nega, seletivamente, o tráfego a um computador ou a um segmento de rede. Os firewalls trabalham, geralmente, abrindo e fechando as portas usadas por vários aplicativos. Ao abrir apenas as portas necessárias em um firewall, você está implementando uma política de segurança restritiva. Qualquer pacote não explicitamente permitido é negado. Ao contrário, uma política de segurança permissiva permite acesso por todas as portas, exceto aquelas explicitamente negadas. Antigamente, software e hardware eram enviados com configurações permissivas. Como os usuários negligenciavam a configuração do equipamento, as configurações permissivas padrão deixavam muitos dispositivos expostos a invasores. Agora, a maioria dos dispositivos é enviada com configurações o mais restritivas possível, mesmo que permitindo ainda uma configuração fácil.

Para permitir o acesso de programas através do Firewall do Windows Defender, pesquise por **Painéis de Controle** e em seguida localize e clique em **Firewall do Windows Defender** para abri-lo. Clique em **Permitir um aplicativo ou recurso por meio do Firewall do Windows Defender**, conforme mostrado na figura.

![[Pasted image 20260706212644.png]]

Se desejar usar um firewall por software diferente, você precisará desativar o firewall do Windows. Para desativar o Firewall do Windows, clique em **Ativar ou desativar o Firewall do Windows**, como mostrado na figura.

![[Pasted image 20260706212658.png]]

O Windows Defender Firewall inclui muitos recursos adicionais. Clique em **Configurações avançadas** para abri-las, conforme mostrado na figura.![[Pasted image 20260706212711.png]]

Aqui você pode criar regras de tráfego de entrada ou saída com base em critérios diferentes. Você também pode importar e exportar políticas ou monitorar diferentes aspectos do firewall, como mostrado na figura.![[Pasted image 20260706212721.png]]


## 39.5.9 Verifique sua compreensão - Firewall e prevenção de intrusão baseada em host

**Pergunta 1**

Qual é uma característica de um firewall de filtragem de pacotes?

- [ ] Eles são um Firewall Stateful.
- [ ] Eles não filtram pacotes fragmentados de forma confiável.
- [x] Eles implementam conjuntos de regras simples de permissão ou negação.
- [ ] Eles são suscetíveis ao spoofing IP.

Está certo.

Existem várias vantagens de usar um firewall de filtragem de pacotes:

- Os filtros de pacote implementam conjuntos de regras de permissão simples ou negam.
- Os filtros de pacotes têm um baixo impacto no desempenho da rede.
- Os filtros de pacotes são fáceis de implementar e são suportados pela maioria dos roteadores.
- Os filtros de pacote fornecem um grau inicial de segurança na camada de rede.
- Os filtros de pacotes executam quase todas as tarefas de um firewall high-end a um custo muito menor.

**Pergunta 2**

Verdadeiro ou Falso: Os filtros de pacotes não podem filtrar dinamicamente determinados serviços.

- [x] Verdadeiro
- [ ] Falso

Está certo.

Os filtros de pacotes não podem filtrar dinamicamente determinados serviços. Por exemplo, as sessões que usam negociações de porta dinâmica são difíceis de filtrar sem abrir o acesso a toda uma variedade de portas.

**Pergunta 3**

Qual perfil do Windows Defender é adequado para um ambiente doméstico?

- [x] Privado
- [ ] Domínio
- [ ] Pública

Está certo.

O acesso a redes públicas é atribuído ao perfil restritivo do firewall Público. O perfil Privado é para computadores que estão isolados da Internet por outros dispositivos de segurança, como um roteador doméstico com funcionalidade de firewall. O perfil de Domínio é escolhido para conexões a uma rede confiável, como uma rede empresarial que se presume ter uma infraestrutura de segurança adequada.

**Pergunta 4**

Um firewall baseado em host usa uma máquina virtual dentro da qual o código é executado. O código inspeciona pacotes de rede e implementa regras de decisão relacionadas à aceitação e encaminhamento dos pacotes. Qual firewall baseado em host isso descreve?

- [ ] Firewall de gateway de aplicativo
- [ ] Firewall transparente
- [x] nftables
- [ ] Windows Defender

Está certo.

O nftables é um aplicativo de firewall do Linux que usa uma máquina virtual simples no kernel do Linux. O código é executado dentro da máquina virtual que inspeciona pacotes de rede e implementa regras de decisão relativas à aceitação e encaminhamento de pacotes.

**Pergunta 5**

Qual ferramenta do Windows 10 é a proteção interna contra vírus e spyware?

- [x] Windows Defender
- [ ] Firewall transparente
- [ ] Firewall de próxima geração
- [ ] Firewall de gateway de aplicativo

Está certo.

O Windows tem proteção interna contra vírus e spyware chamada Windows Defender. O Windows Defender está ativado por padrão para fornecer proteção em tempo real contra infecções.

**Pergunta 6**

Está certo.

Coloque as opções na seguinte ordem:

|Categoria|Resposta correta|
|---|---|
|Proteção contra spyware|Este programa faz a verificação de keyloggers.|
|Fontes confiáveis/não confiáveis|Este programa avisa sobre programas inseguros prestes a serem instalados e sobre sites inseguros antes de serem visitados.|
|Proteção antivírus|Este programa monitora continuamente a presença de vírus. Quando um vírus é detectado, o usuário é avisado e o programa tenta colocar o vírus em quarentena ou excluí-lo.|
|Proteção contra phishing|Este programa bloqueia os endereços IP de sites de phishing conhecidos e avisa o usuário sobre sites suspeitos.|
|Proteção contra adware|Este programa busca continuamente por programas que exibem anúncios comerciais em seu computador.|

# 39.6 Acesso sem fio seguro

## 39.6.1 Vídeo - Ameaças WLAN

As redes sem fio estão crescendo rapidamente. É importante entender as vulnerabilidades, ameaças e explorações da rede sem fio.

**Clique em Reproduzir para ver um vídeo sobre ameaças às WLANs.**

À medida que mergulhamos nas redes locais sem fio, precisamos descrever as ameaças às nossas LANs sem fio. E, para começar, uma LAN sem fio é praticamente aberta para qualquer pessoa dentro da área de um ponto de acesso. E se eles tiverem as credenciais apropriadas para associar com esse ponto de acesso, eles estão na rede.

Agora, esses ataques podem ser gerados por pessoas de fora, funcionários descontentes, mesmo sem querer por funcionários dentro da sua empresa, e eles nem precisam entrar fisicamente no local de trabalho para obter acesso à rede local sem fio.

Existem muitos tipos diferentes de ataques sem fio que podem acontecer, sendo um deles a interceptação de dados. Seus dados sem fio devem ser criptografados o tempo todo para impedir que sejam lidos pelos bisbilhoteiros, pessoas que não deveriam ter acesso a esses dados.

Intrusos sem fio são usuários não autorizados que estão tentando acessar recursos de rede, e sabe de uma coisa? Eles podem ser dissuadidos usando a autenticação.

O ataque de negação de serviço é um pouco mais difícil. Eles tentam acessar serviços de rede local sem fio, depois comprometê-los acidentalmente ou de propósito.

Também temos nossos APs desonestos, que são pontos de acesso não autorizados que são instalados por um usuário bem-intencionado — alguém que só queria ter uma rede sem fio extra por perto — ou instalados para fins maliciosos, e eles querem poder interceptar o tráfego das pessoas. Usando software de gerenciamento, devemos ser capazes de detectar esses pontos de acesso não autorizados.

Como os ataques de negação de serviço acontecem sem fio? Bem, eles podem acontecer por causa de coisas como dispositivos configurados incorretamente. Erros de configuração podem desativar uma rede sem fio. Por exemplo, um administrador poderia acidentalmente desabilitar isso sobre o botão desativar. Ou mesmo um invasor com privilégios administrativos pode intencionalmente desativar a rede local sem fio.

Agora, outro ataque de DoS é onde um usuário mal-intencionado interfere intencionalmente na comunicação sem fio. O que isso significa é que um usuário mal-intencionado tem uma meta, e seu objetivo é sobrecarregar o ponto de acesso sem fio a um ponto em que nenhum dispositivo legítimo possa acessá-lo. Existem ferramentas para dispositivos móveis para isso, bem como ferramentas específicas de bloqueio de radiofrequência.

Interferência acidental, todos sabemos que isso pode acontecer. Nossas redes locais sem fio são propensas a interferências de outros dispositivos sem fio. Esses dispositivos podem ser coisas como fornos de micro-ondas, monitores de bebê, telefones sem fio e muito mais. A frequência de rádio de 2.4 gigahertz é a banda sem fio mais propensa a interferências.

Então, como minimizamos esse risco de negação de serviço? Bem, vamos fortalecer nossos dispositivos e manter nossas senhas seguras. Nós vamos usar backups para voltar a ficar online o mais rápido possível. E também quaisquer alterações que estavam sendo implementadas em nossa rede sempre devem ser feitas fora do horário comercial, não durante o período de nosso ambiente de produção. Muita dessa interferência que pode acontecer, como mencionado, está na banda de 2.4 gigahertz, então vamos mudar nossos dispositivos para a banda de cinco gigahertz, se for possível.

Pontos de acesso não autorizados são prejudiciais à segurança da rede com fio. Um ponto de acesso não autorizado é um ponto de acesso ou um roteador sem fio que foi conectado a uma rede corporativa sem a autorização explícita da empresa. Isso é totalmente contrário à política da empresa. Qualquer pessoa com acesso às instalações físicas pode instalar um roteador sem fio muito barato ou ponto de acesso e permitir-se acessar ao recurso de rede com fio seguro.

Uma vez conectados, esses APs não autorizados podem ser usados por um invasor para capturar endereços MAC, para capturar pacotes de dados, e até mesmo obter acesso a recursos de rede com fio. Eles poderiam ser usados para lançar ataques man-in-the-middle também. Para impedir a instalação desses pontos de acesso não autorizados, as organizações precisam configurar controladores de LAN sem fio com políticas de AP não autorizadas; elas também devem usar software de monitoramento para monitorar ativamente o espectro de rádio em busca de pontos de acesso não autorizados.

Com um ataque man-in-the-middle, um hacker está em uma posição entre duas entidades legítimas para ler ou modificar os dados que passam entre essas duas entidades. Agora há muitas maneiras que um ataque man-in-the-middle pode ser criado. Uma maneira popular é usar o ataque "gêmeo do mal" (evil twin) de pontos de acesso. E é aqui que um invasor irá introduzir um ponto de acesso não autorizado. Ele vai configurar o ponto de acesso não autorizado com o mesmo SSID sem fio de um ponto de acesso real legítimo nas proximidades.

Locais que oferecem Wi-Fi gratuito, como algumas cafeterias, aeroportos e restaurantes, são locais populares para que esse tipo de ataque ocorra, porque eles geralmente têm autenticação aberta. Com autenticação aberta, uma senha não é necessária quando você vai acessar a rede sem fio.

Agora, conectando-se a redes sem fio, veria dois pontos de acesso oferecendo acesso sem fio. As pessoas perto do ponto de acesso não autorizado encontrariam o sinal mais forte e provavelmente se conectariam a ele. Depois que o tráfego do usuário é enviado através do ponto de acesso não autorizado, esses dados são capturados e geralmente são encaminhados ao ponto de acesso legítimo. O tráfego retornando desse ponto de acesso legítimo será enviado de volta ao ponto de acesso não autorizado, será capturado pelo usuário mal-intencionado e encaminhado para esse usuário pobre e inocente. Isso permite que os invasores roubem senhas de usuários, peguem informações pessoais, e até obtenham acesso ao dispositivo do usuário.

Defender-se desses ataques man-in-the-middle depende da sofisticação da sua infraestrutura de rede local sem fio e também da vigilância que você usa para monitorar a atividade nessas redes locais sem fio. Tudo começa com a identificação de dispositivos legítimos na rede, e depois de ter esses dispositivos legítimos conhecidos, a rede pode ser monitorada para qualquer coisa que pareça anormal.


## 39.6.2 Visão geral da segurança sem fio

Uma WLAN está aberta a qualquer pessoa dentro do alcance de um ponto de acesso sem fio (AP) e com as credenciais apropriadas para se associar a ele. Com uma placa de rede sem fio (NIC) e conhecimento de técnicas de quebra de segurança, um invasor pode não precisar entrar fisicamente no local de trabalho para obter acesso à sua rede por meio de uma WLAN.

Ataques podem ser gerados por pessoas externas, funcionários insatisfeitos e até mesmo acidentalmente. Redes sem fio são especialmente suscetíveis a uma série de ameaças, incluindo:

- **Interceptação de dados -** Os dados sem fio devem ser criptografados para evitar que sejam lidos por pessoas que estejam bisbilhotando.
- **Intrusos sem fio -** Usuários não autorizados que tentam acessar recursos de rede podem ser impedidos por meio de técnicas eficazes de autenticação.
- **Ataques de Negação de Serviço (DoS) -** O acesso aos serviços WLAN pode ser comprometido tanto acidentalmente quanto de forma maliciosa. Existem várias soluções, dependendo da origem do ataque DoS.
- **Rogue APs -** Pontos de acesso não autorizados instalados por um usuário bem-intencionado ou com propósitos maliciosos podem ser detectados usando software de gerenciamento de rede sem fio.


## 39.6.3 Ataques DoS

Os ataques de DoS sem fio podem ser o resultado de:

- **Dispositivos configurados incorretamente -** Erros de configuração podem desabilitar a WLAN. Por exemplo, um administrador pode alterar acidentalmente uma configuração e desativar a rede, ou um invasor com privilégios de administrador pode desativar intencionalmente uma WLAN.
- **Um usuário malicioso interfere intencionalmente na comunicação sem fio -** Seu objetivo é desabilitar completamente a rede sem fio ou a ponto de nenhum dispositivo legítimo poder acessar o meio.
- **Interferência acidental -** WLANs são suscetíveis a interferência de outros dispositivos sem fio, incluindo fornos de micro-ondas, telefones sem fio, babás eletrônicas e outros, como mostrado na figura. A banda de 2,4 GHz é mais propensa a interferências do que a banda de 5 GHz.
![[Pasted image 20260706213215.png]]Para minimizar o risco de um ataque de negação de serviço devido a dispositivos mal configurados e ataques maliciosos, proteja todos os dispositivos, mantenha as senhas seguras, crie backups e garanta que todas as alterações na configuração sejam incorporadas fora do horário comercial.

Monitore a WLAN quanto a problemas de interferência acidental e resolva-os assim que aparecerem. Como a banda de 2,4 GHz é usada por outros tipos de dispositivos, os 5 GHz devem ser usados em áreas propensas a interferências.

## 39.6.4 Pontos de acesso não autorizados

Um ponto de acesso não autorizado é um ponto de acesso ou roteador sem fio que foi conectado a uma rede corporativa sem autorização explícita e contra a política corporativa. Qualquer pessoa com acesso às instalações pode instalar (de forma maliciosa ou não maliciosa) um roteador sem fio barato que possa permitir o acesso a um recurso de rede seguro.

Uma vez conectado, o ponto de acesso não autorizado pode ser usado por um invasor para capturar endereços MAC, capturar pacotes de dados, obter acesso a recursos de rede ou iniciar um ataque intermediário.

Um hotspot de rede pessoal também pode ser usado como um ponto de acesso não autorizado. Por exemplo, um usuário com acesso seguro à rede permite que seu host autorizado do Windows se torne um ponto de acesso Wi-Fi. Isso evita as medidas de segurança e outros dispositivos não autorizados agora podem acessar os recursos de rede como um dispositivo compartilhado.

Para evitar a instalação de pontos de acesso não autorizados, as organizações devem configurar controladores de LAN sem fio (WLCs) com políticas de pontos de acesso não autorizados, conforme mostrado na figura, e utilizar software de monitoramento para monitorar ativamente o espectro de rádio em busca de pontos de acesso não autorizados.
![[Pasted image 20260706213234.png]]


## 39.6.5 Ataque Man-in-the-Middle

Em um ataque de "man-in-the-middle" (MITM), o hacker se posiciona entre duas entidades legítimas para ler ou modificar os dados que passam entre as duas partes. Existem várias maneiras de criar um ataque MITM.

Um ataque MITM sem fio popular é chamado de ataque de "AP gêmeo do mal", (“evil twin AP”) em que um invasor introduz um ponto de acesso não autorizado e o configura com o mesmo SSID que um ponto de acesso legítimo, como mostra a figura. Locais que oferecem Wi-Fi gratuito, como aeroportos, cafés e restaurantes, são locais particularmente populares para esse tipo de ataque devido à autenticação aberta.

Os ataques MITM e suas variações são freqüentemente chamados de ataques no caminho.
![[Pasted image 20260706213248.png]]

Os clientes sem fio que tentam se conectar a uma WLAN verão dois APs com o mesmo SSID oferecendo acesso sem fio. Aqueles perto do ponto de acesso não autorizado encontram o sinal mais forte e provavelmente se associam a ele. O tráfego do usuário agora é enviado ao ponto de acesso não autorizado, que por sua vez captura os dados e os encaminha ao ponto de acesso legítimo, como mostra a figura. O tráfego de retorno do ponto de acesso legítimo é enviado ao ponto de acesso não autorizado, capturado e depois encaminhado ao usuário inocente. O invasor pode roubar as senhas e informações pessoais do usuário, obter acesso ao dispositivo e comprometer o sistema.![[Pasted image 20260706213302.png]]

Impedir um ataque como um ataque Man in the middle (MITM) depende da sofisticação da infraestrutura da WLAN e da vigilância no monitoramento da atividade na rede. O processo começa com a identificação de dispositivos legítimos na WLAN. Para fazer isso, os usuários devem ser autenticados. Depois que todos os dispositivos legítimos são conhecidos, a rede pode ser monitorada quanto a dispositivos ou tráfego anormais. Para isso, os usuários devem ser autenticados.

## 39.6.6 Verifique sua Compreensão - Ameaças WLAN
**Pergunta 1**

Qual ameaça WLAN normalmente NÃO é a fonte de um ataque DoS sem fio?

- [ ] dispositivos configurados incorretamente
- [ ] usuário malicioso
- [x] AP não autorizado
- [ ] interferência de rádio

Está certo.

Dispositivos configurados incorretamente, usuários mal-intencionados e interferências acidentais são fontes prováveis de um ataque de DoS sem fio.

**Pergunta 2**

Verdadeiro ou falso: Um AP não autorizado é um AP mal configurado conectado à rede e uma possível fonte de ataques DoS.

- [x] Falso
- [ ] Verdadeiro

Está certo.

Um ponto de acesso não autorizado é um ponto de acesso ou roteador sem fio que foi conectado a uma rede corporativa sem autorização explícita e contra a política corporativa.

**Pergunta 3**

Que tipo de ataque é chamado de ataque "evil twin AP"?

- [ ] Interferência de Rádio
- [ ] Intruso sem fio
- [x] MITM
- [ ] DoS

Está certo.

Um ataque de "AP gêmeo do mal" é um ataque MITM sem fio popular, em que um invasor introduz um AP não autorizado e o configura com o mesmo SSID que um ponto de acesso legítimo.


## 39.6.7 Vídeo - WLANs seguras

O tópico anterior explicou as ameaças da WLAN. O que você pode fazer para proteger a WLAN?

**Clique em Reproduzir para ver um vídeo sobre técnicas para proteger WLANs.**

