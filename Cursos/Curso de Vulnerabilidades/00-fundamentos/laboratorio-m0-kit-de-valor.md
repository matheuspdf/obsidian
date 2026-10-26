---
status: a-estudar
---
# Laboratório M0: Kit de valor para o negócio

## 🎯 Objetivo

Criar um caso de negócio inicial e um termo de abertura para um processo fictício de gestão de vulnerabilidades. O material deve relacionar riscos técnicos a serviços, responsabilidades e decisões organizacionais.

## Ética e legalidade

> [!warning] Use somente material fictício
> Não inclua informações reais da empresa onde você trabalha. Nunca faça varreduras ou testes em sistemas sem autorização. Este laboratório é documental e não precisa acessar nenhum ambiente corporativo.

## Requisitos mínimos

| Recurso | Mínimo recomendado |
|---|---|
| Processador | 2 núcleos. |
| Memória | 4 gigabytes (GB) de **RAM (Random Access Memory, memória de acesso aleatório)**. |
| Armazenamento | 5 gigabytes (GB) livres para as ferramentas e os arquivos. |
| Máquina virtual | Não é necessária. |
| Conexão com a internet | Necessária somente se você decidir publicar o repositório. |

## Ferramentas gratuitas

- LibreOffice Writer e Calc, software livre e gratuito.
- Um editor de texto para arquivos Markdown.
- Git, caso queira versionar os arquivos localmente.
- Conta gratuita no GitHub e repositório público, caso queira publicar.

O laboratório não depende de serviço de nuvem, plano temporário nem execução de automações.

## Passo a passo

### 1. Crie a pasta do projeto

Crie uma pasta chamada:

```text
kit-gestao-vulnerabilidades-ficticio
```

Dentro dela, crie uma pasta `docs` para os documentos do exercício.

### 2. Defina o cenário fictício

Use um rótulo claramente fictício, como Organização de Exemplo, e registre que a organização é fictícia.

Exemplo de texto:

> A Organização de Exemplo usa serviços de comunicação, acesso remoto e armazenamento de relatórios para apoiar suas atividades. Este projeto é um exercício educacional e não representa uma avaliação de uma empresa real.

Não use nomes de clientes, fornecedores, pessoas ou sistemas reais.

### 3. Liste três serviços de negócio

Escolha três serviços fictícios, por exemplo:

- Comunicação corporativa.
- Acesso remoto para colaboradores.
- Armazenamento e consulta de relatórios.

Para cada serviço, indique o processo de negócio apoiado e uma função responsável, como “responsável pela operação” ou “representante da área de negócio”. Não use nomes de pessoas reais.

### 4. Monte um mapa de impactos

Use uma planilha ou uma tabela Markdown. Considere confidencialidade, integridade e disponibilidade, além das consequências para o negócio.

| Serviço fictício | Confidencialidade | Integridade | Disponibilidade | Consequência possível |
|---|---|---|---|---|
| Repositório de relatórios | Acesso não autorizado a relatórios. | Alteração não autorizada de conteúdo. | Atraso no acesso ou na preparação de relatórios. | Retrabalho, atraso em atividades e possível perda de confiança. |
| Acesso remoto | Acesso indevido a recursos internos. | Alteração de informações acessíveis pela conexão. | Colaboradores sem acesso remoto. | Dificuldade de executar atividades fora do escritório. |

Esses exemplos são qualitativos. Não são uma avaliação de risco nem uma classificação de criticidade. Se mencionar uma consequência financeira, registre a premissa e não invente um valor como se fosse um dado real.

### 5. Faça o mapa de partes interessadas

Inclua grupos que poderiam participar de um processo real:

- Liderança ou patrocinador do processo.
- Segurança da informação.
- Infraestrutura e suporte.
- Responsáveis pelos serviços de negócio.
- Jurídico, privacidade ou compliance, quando aplicável.
- Fornecedores relevantes, conforme contrato e responsabilidade.

Você pode usar uma matriz **RACI (Responsible, Accountable, Consulted and Informed, responsável pela execução, responsável pela aprovação final, consultado e informado)**.

Registre que decisões sobre risco devem ser encaminhadas a pessoas com autoridade adequada. A equipe que identifica uma vulnerabilidade não assume automaticamente a decisão de aceitar o risco do negócio.

### 6. Registre barreiras e ações

Inclua pelo menos quatro barreiras e uma ação inicial para cada uma:

| Barreira no cenário fictício | Sinal observado | Ação inicial proposta |
|---|---|---|
| Falta de apoio da liderança | Não há responsável pelo piloto. | Solicitar patrocinador e uma decisão específica. |
| Falha de comunicação | Os relatórios só contêm termos técnicos. | Acrescentar serviço afetado e consequência possível. |
| Imaturidade do processo | Não há responsáveis pelos serviços. | Definir responsáveis no escopo do piloto. |
| Silos entre equipes | Segurança e infraestrutura planejam sem a área usuária. | Fazer uma revisão conjunta do serviço escolhido. |

As ações são propostas do exercício. Não são garantias de que todos os problemas serão resolvidos imediatamente.

### 7. Escreva um termo de abertura

Prepare um documento de uma página com:

- Objetivo do processo.
- Escopo do piloto fictício.
- Serviços e partes interessadas envolvidos.
- Responsabilidades iniciais.
- Forma de comunicar descobertas e decisões.
- Forma de registrar impedimentos e exceções.
- Frequência de revisão proposta, identificada como premissa do exercício.
- Critério para decidir se o piloto pode ser ampliado.

Não defina ainda prazos de **SLA (Service Level Agreement, acordo de nível de serviço)** nem uma fórmula de priorização. Esses assuntos serão estudados nos módulos [[modulo-1-ciclo-de-vida|Módulo 1]] e [[modulo-2-priorizacao-de-riscos|Módulo 2]].

### 8. Produza um resumo executivo

Escreva uma página dirigida à liderança. Inclua:

1. O serviço ou cenário em foco.
2. Por que vulnerabilidades podem afetar continuidade, informações ou confiança.
3. Qual piloto você propõe.
4. Quais papéis ou recursos são necessários.
5. Qual decisão está sendo solicitada.

Evite jargões sem explicação, promessas de risco zero e valores financeiros fictícios apresentados como fatos.

### 9. Revise o material para publicação

Antes de publicar, confira nomes, textos, propriedades dos documentos e imagens. Remova nomes de usuário, caminhos locais, informações de contato, logotipos e qualquer referência que possa identificar a empresa ou pessoas do seu trabalho.

Se precisar usar um domínio de exemplo, use `.example`. Para endereços de rede em exercícios futuros, use faixas reservadas para documentação, nunca endereços reais.

## ✅ Resultado esperado

Ao concluir, você terá:

- Um cenário empresarial fictício e delimitado.
- Um mapa de serviços e consequências possíveis.
- Um mapa de partes interessadas.
- Uma lista de barreiras organizacionais e ações propostas.
- Um termo de abertura de uma página.
- Um resumo executivo pronto para apresentar como exercício de portfólio.

## Erros comuns

- Descrever o impacto como “risco de segurança” sem explicar qual serviço ou atividade pode ser afetado.
- Apresentar frequência, prioridade ou valor financeiro como universal sem registrar que é uma premissa.
- Afirmar que a organização fictícia está sujeita a uma norma setorial sem analisar seu enquadramento.
- Usar telas, documentos, logotipos ou configurações reais do trabalho.
- Publicar metadados que revelem nome de usuário ou caminho local.
- Escrever o resumo executivo como se fosse um relatório técnico para especialistas.

## Como validar

Confirme os seguintes itens:

- O cenário está marcado como fictício.
- Há pelo menos três serviços e impactos descritos para confidencialidade, integridade e disponibilidade.
- As partes interessadas estão identificadas por função, não por pessoas reais.
- As barreiras têm ações propostas.
- O resumo executivo solicita uma decisão clara.
- Não há nomes, endereços de rede, configurações, capturas de tela, dados ou metadados da empresa real.

## Estrutura sugerida para o repositório de portfólio

```text
kit-gestao-vulnerabilidades-ficticio/
├── README.md
├── docs/
│   ├── 01-cenario-ficticio.md
│   ├── 02-mapa-servicos-impactos.ods
│   ├── 03-partes-interessadas-barreiras.md
│   ├── 04-termo-de-abertura.md
│   └── 05-resumo-executivo.md
└── evidencias/
    └── README.md
```

O arquivo **ODS (OpenDocument Spreadsheet)** é uma planilha suportada pelo LibreOffice.

## Modelo de README para o portfólio

```markdown
# Kit inicial de gestão de vulnerabilidades

## Resumo

Este projeto apresenta um caso de negócio e um termo de abertura para um
processo fictício de gestão de vulnerabilidades.

## English summary

A fictional business case and starter charter for a vulnerability management
process, created as a security portfolio project.

## Cenário

Organização e serviços fictícios. Nenhuma informação de uma empresa real foi usada.

## Objetivo

Relacionar vulnerabilidades a serviços, impactos de negócio, responsabilidades
e decisões de gestão.

## Entregáveis

- Mapa de serviços e impactos.
- Mapa de partes interessadas.
- Registro de barreiras organizacionais e ações iniciais.
- Termo de abertura.
- Resumo executivo.

## Método

Descrever brevemente como o cenário foi criado e como os impactos foram
registrados qualitativamente.

## Premissas e limitações

Listar as premissas do exercício e explicar que o projeto não representa uma
auditoria ou avaliação de uma empresa real.

## Ética e anonimização

Confirmar que nomes, dados, endereços, configurações e documentos são fictícios.
```

## Evidências para mostrar

- Captura do mapa de serviços e impactos, com o cenário fictício visível.
- Termo de abertura em Markdown ou em **PDF (Portable Document Format, formato de documento portátil)**.
- Resumo executivo de uma página.
- Estrutura do repositório e README.

Não publique imagens de ferramentas corporativas, relatórios internos, telas do Microsoft 365, Action1, Entra ID, Sophos ou qualquer outro sistema do trabalho.

## Descrições para currículo e LinkedIn

Currículo:

> Desenvolvi um kit fictício de gestão de vulnerabilidades, relacionando serviços de negócio, impactos potenciais, partes interessadas e barreiras organizacionais. Produzi termo de abertura e resumo executivo para um piloto.

LinkedIn:

> Projeto de portfólio: criei um caso de negócio fictício para gestão de vulnerabilidades, com mapa de impactos, responsabilidades, barreiras organizacionais e proposta de piloto. O material usa somente dados sintéticos.
