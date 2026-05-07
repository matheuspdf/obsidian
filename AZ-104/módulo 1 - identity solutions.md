# Configurar o Microsoft Entra ID

## Descrever os benefícios e recursos do Microsoft Entra ID

![[Pasted image 20260416202301.png]]

Um conjunto de recursos de gerenciamento de identidades baseado em nuvem que permite gerenciar com segurança o acesso aos serviços e recursos do Azure para seus usuários.

Fornece gerenciamento de aplicação, autenticação, gerenciamento de dispositivos e identidade híbrida

O EntraID possui protocolos diferentes dos usados pelo AD.

AD -> Kerberos e NTLM
EntraID -> SAML, Oauth, Open ID e WS-Federation

O EntraID possui protocolos mais modernos de autenticação.
Ao adquirir licenças do MS365, automaticamente você possui autenticação pelo EntraID usando seus protocolos modernos.

Modelo de identidade híbrida: é quando o usuário existe no AD local e é replicado para a nuvem (ENTRAID). Se eu crio o usuário na nuvem, ele não é replicado local.
- AD local → Nuvem: **sim (sincroniza)**
- Nuvem → AD local: **não (por padrão)**


## Descrever os conceitos do Microsoft Entra ID
EntraID -> serviço de diretório que gerencia identidade, assim como o AD. A identidade não é um usuário, ela é um objeto que pode ser autenticado, que eu posso conceder uma permissão a ele.

| Conceito                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Identidade**                  | Um objeto que pode ser autenticado                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Conta**                       | Uma identidade que tem dados associados a ela                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Conta do Microsoft Entra ID** | Uma identidade criada por meio do Microsoft Entra ID ou outro serviço de nuvem da Microsoft                                                                                                                                                                                                                                                                                                                                                                                        |
| **Tenant/Diretório**            | Uma instância dedicada e confiável. Um Tenant é criado automaticamente quando sua organização cria uma subscription (assinatura) de serviço de nuvem da Microsoft. <br><br> • Instâncias adicionais podem ser criadas <br> • O Microsoft Entra ID é o produto subjacente que fornece o serviço de identidade <br> • O termo Tenant significa uma única instância que representa uma única organização <br> • Os termos Tenant e Diretório são frequentemente usados alternadamente |
| **Azure Subscription**          | Usado para pagar por serviços de nuvem do Azure                                                                                                                                                                                                                                                                                                                                                                                                                                    |
## Comparar o Microsoft Entra ID com o ADDS (Active Directory Domain Services)
- O MS Entra ID é principalmente uma solução de identidade
- Consultando usando a API REST sobre HTTP e HTTPS
- Usa protocolos HTTP e HTTPS, como SAML, WS-Federation e OpenID Connect para autenticação (OAuth para autorização)
- Inclui serviços de federação e muitos serviços de terceiros (como o Facebook)
- Os usuários e grupos do MS EntraID são criados em uma estrutura simples e não há Unidades Organizacionais (OUs) ou GPOs (Objetos de Diretiva de Grupo)
## Microsoft Entra ID – Feature Comparison

| Feature                                                     | Free | P1  | P2  | Governance |
| ----------------------------------------------------------- | :--: | :-: | :-: | :--------: |
| **Single Sign-On (unlimited)**                              |  ✓   |  ✓  |  ✓  |            |
| **Cloud and Federated authentication**                      |  ✓   |  ✓  |  ✓  |            |
| **Advanced group management**                               |      |  ✓  |  ✓  |            |
| **Self-service account management portal**                  |  ✓   |  ✓  |  ✓  |            |
| **Multifactor authentication (MFA)**                        |  ✓   |  ✓  |  ✓  |            |
| **Conditional access**                                      |      |  ✓  |  ✓  |            |
| **Risk-based Conditional Access (sign-in risk, user risk)** |      |     |  ✓  |            |
| **Automated user and group provisioning to apps**           |      |  ✓  |  ✓  |     ✓      |
| **Privileged identity management (PIM)**                    |      |     |  ✓  |     ✓      |

| Feature                                    | O que faz                                                                                                                                                |
| ------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Single Sign-On (SSO)**                   | Permite que o usuário faça login uma única vez e acesse múltiplos aplicativos sem precisar autenticar novamente                                          |
| **Cloud and Federated Authentication**     | Autentica usuários tanto em serviços na nuvem quanto em sistemas on-premises, integrando identidades externas (ex: AD local)                             |
| **Advanced Group Management**              | Gerenciamento avançado de grupos, incluindo grupos dinâmicos (associação automática por regras) e delegação de administração                             |
| **Self-service Account Management Portal** | Portal onde o próprio usuário pode redefinir senha, gerenciar grupos e atualizar informações sem precisar chamar o suporte de TI                         |
| **Multifactor Authentication (MFA)**       | Exige um segundo fator de verificação no login (app autenticador, SMS, etc.) além da senha, aumentando a segurança                                       |
| **Conditional Access**                     | Define políticas de acesso baseadas em condições (ex: bloquear acesso fora da rede corporativa, exigir MFA em certos apps)                               |
| **Risk-based Conditional Access**          | Versão avançada do Conditional Access que avalia o risco em tempo real do login (localização suspeita, credencial vazada, etc.) e toma ações automáticas |
| **Automated User and Group Provisioning**  | Cria, atualiza e remove automaticamente contas de usuários em aplicativos SaaS (ex: Salesforce, ServiceNow) com base no diretório                        |
| **Privileged Identity Management (PIM)**   | Gerencia, controla e monitora acessos privilegiados (ex: Global Admin), permitindo acesso just-in-time com aprovação e auditoria                         |
## Configurar identidades de dispositivos
![[Pasted image 20260418212123.png]]

## Implement Self-Service Password Reset (SSPR)
- Determine como utilizar o self-service password reset (SSPR)
- Escolha o número de métodos de autenticação necessários e os métodos disponíveis (e-mail, telefone, perguntas)
- Você pode exigir que os usuários se registrem no SSPR (mesmo processo do MFA)
![[Pasted image 20260418212957.png]]

# Configurar contas de usuário e grupo
Objetivos de aprendizagem - Contas de usuário e grupo

	• Criar contas de usuário 
	• Gerenciar contas de usuário 
	• Criar contas em massa 
	• Criar contas de grupo 
	• Atribuir licenças a usuários e grupos 
	• Criar unidades administrativas

Gerenciar identidades e governança do Azure (20–25%): 
- gerenciar usuários e grupos do Microsoft Entra ID 
- Criar usuários e grupos 
- Gerenciar propriedades de usuário e grupo 
- Gerenciar usuários externos 
- Gerenciar licenças

## Criar contas de usuário

![[Pasted image 20260421193136.png]]

- Todos os usuários devem ter uma conta
- A conta é usada para autenticação e autorização
- Cada conta de usuário tem propriedades adicionais

![[Pasted image 20260421193311.png]]

## Gerenciamento de Usuários no Microsoft 365

- Necessário ser **Global Administrator** ou **User Administrator** para gerenciar usuários
- Perfil do usuário (imagem, trabalho, informações de contato) é opcional
- Usuários excluídos podem ser restaurados por **30 dias**
- Disponível informações sobre **auditoria de logins**


## Executar atualizações de conta em massa (bulk)
![[Pasted image 20260421193435.png]]

## Operações em Massa de Usuários

- Necessário ser **Global Administrator** ou **User Administrator** para gerenciar usuários
- Suporta atualizações de usuários e membros de grupo em **massa**
- Crie o modelo de valores separados por vírgulas (**CSV**) que você pode baixar do Portal

## Criar contas de grupo

![[Pasted image 20260421193811.png]]

## Tipos de Grupos

**Group Types**
- Security Groups
- Microsoft 365 Groups

**Assignment Types**
- Assigned (associar manualmente um user)
- Dynamic User (criar uma query para que ela busque algum dado no Entra e adicione ao user)
- Dynamic Device *(Security groups only)*

## Atribuir licenças a usuários e grupos

O Azure é um serviço de nuvem que fornece muitos serviços internos gratuitamente
- O **Microsoft Entra ID** vem como um serviço gratuito
- Funcionalidades adicionais disponíveis com licença **P1** ou **P2**

Serviços adicionais (como o **O365**) são serviços de nuvem pagos
- Os serviços de nuvem pagos da Microsoft exigem licenças
- As licenças são atribuídas a quem precisa de acesso aos serviços
- Cada usuário ou grupo requer uma **licença paga separada**
- Os administradores usam portais de gerenciamento e cmdlets do **PowerShell** para gerenciar licenças

## Criar unidades administrativas
![[Pasted image 20260421194408.png]]
1. Criar uma **unidade administrativa**
2. Preencher a unidade administrativa com **usuários ou grupos**
3. Criar uma **função** com permissões apropriadas com escopo para a unidade administrativa
4. Adicionar **membros de TI** à função