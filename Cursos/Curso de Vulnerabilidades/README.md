# Curso: Gestão de vulnerabilidades

Curso guiado para estudo individual, do nível introdutório à prática profissional. As notas são compatíveis com Obsidian e os exemplos de laboratório usam dados fictícios.

## Como usar este cofre

- Atualize o campo `status` das notas usando somente `a-estudar`, `estudando` ou `revisado`.
- Leia os módulos na ordem indicada.
- Use os links relativos para abrir as notas no Obsidian ou no GitHub.
- Publique somente materiais fictícios e revisados. Não inclua dados, nomes, endereços de rede ou configurações reais do trabalho.

## Ordem de estudo e progresso

| Ordem | Módulo | Progresso |
|---:|---|---|
| 0 | [Fundamentos](00-fundamentos/modulo-0-fundamentos.md) | a-estudar |
| 1 | [Ciclo de vida de uma vulnerabilidade](01-ciclo-de-vida/modulo-1-ciclo-de-vida.md) | a-estudar |
| 2 | [Identificação e priorização de riscos](02-priorizacao/modulo-2-priorizacao-de-riscos.md) | a-estudar |
| 3 | [Remediação, mitigação e controles compensatórios](03-remediacao/modulo-3-remediacao-e-mitigacao.md) | a-estudar |
| 4 | [Frameworks e compliance](04-frameworks-compliance/modulo-4-frameworks-e-compliance.md) | a-estudar |
| 5 | [DevSecOps e testes de segurança](05-devsecops/modulo-5-devsecops-e-testes.md) | a-estudar |
| 6 | [Relatórios, métricas e automação](06-relatorios-automacao/modulo-6-relatorios-e-automacao.md) | a-estudar |

A carga estimada dos módulos obrigatórios é de 54 a 70 horas, incluindo estudo, exercícios, laboratórios e documentação de portfólio.

## Tópicos extras aprovados

| Código | Tópico | Progresso |
|---|---|---|
| X1 | [Gestão de ativos e inventário](07-topicos-extras-aprovados/x1-gestao-de-ativos.md) | a-estudar |
| X2 | [Superfície de ataque e exposição contínua](07-topicos-extras-aprovados/x2-superficie-e-exposicao.md) | a-estudar |
| X3 | [Inteligência de ameaças e tipos de teste](07-topicos-extras-aprovados/x3-inteligencia-e-testes.md) | a-estudar |
| X4 | [Segurança de aplicações](07-topicos-extras-aprovados/x4-seguranca-de-aplicacoes.md) | a-estudar |
| X5 | [Lista de materiais e cadeia de suprimentos de software](07-topicos-extras-aprovados/x5-sbom-e-cadeia-de-suprimentos.md) | a-estudar |
| X6 | [Vulnerabilidades em nuvem e contêineres](07-topicos-extras-aprovados/x6-nuvem-e-conteineres.md) | a-estudar |
| X7 | [Aplicação ao stack Windows e Microsoft](07-topicos-extras-aprovados/x7-stack-windows-e-microsoft.md) | a-estudar |
| X8 | [Maturidade e roteiro de implantação](07-topicos-extras-aprovados/x8-maturidade-e-roteiro.md) | a-estudar |
| X9 | [Detecção de vulnerabilidades com Wazuh](07-topicos-extras-aprovados/x9-wazuh.md) | a-estudar |

Os tópicos extras acrescentam aproximadamente 32 a 45 horas se forem todos estudados.

## Estrutura do cofre

```text
.
├── .gitignore
├── README.md
├── 00-fundamentos/
│   ├── modulo-0-fundamentos.md
│   └── laboratorio-m0-kit-de-valor.md
├── 01-ciclo-de-vida/
│   └── modulo-1-ciclo-de-vida.md
├── 02-priorizacao/
│   └── modulo-2-priorizacao-de-riscos.md
├── 03-remediacao/
│   └── modulo-3-remediacao-e-mitigacao.md
├── 04-frameworks-compliance/
│   └── modulo-4-frameworks-e-compliance.md
├── 05-devsecops/
│   └── modulo-5-devsecops-e-testes.md
├── 06-relatorios-automacao/
│   └── modulo-6-relatorios-e-automacao.md
└── 07-topicos-extras-aprovados/
    ├── x1-gestao-de-ativos.md
    ├── x2-superficie-e-exposicao.md
    ├── x3-inteligencia-e-testes.md
    ├── x4-seguranca-de-aplicacoes.md
    ├── x5-sbom-e-cadeia-de-suprimentos.md
    ├── x6-nuvem-e-conteineres.md
    ├── x7-stack-windows-e-microsoft.md
    ├── x8-maturidade-e-roteiro.md
    └── x9-wazuh.md
```

## Segurança e publicação

Todos os exemplos e laboratórios devem usar ambientes próprios e intencionalmente vulneráveis. Nunca faça varreduras ou testes sem autorização. Antes de sincronizar com o GitHub, revise arquivos, imagens, metadados e histórico para confirmar que não há informações reais do trabalho.
