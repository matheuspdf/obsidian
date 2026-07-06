
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