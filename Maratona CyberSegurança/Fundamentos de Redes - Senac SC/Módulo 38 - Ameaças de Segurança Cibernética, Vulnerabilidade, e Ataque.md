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

