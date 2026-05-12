## Introdução ao lab

Este é o primeiro de uma série de labs para Administradores do Azure. Neste lab, você aprende sobre usuários e grupos. Usuários e grupos são os blocos de construção básicos para uma solução de identidade.

Este lab requer uma assinatura do Azure. O tipo de assinatura pode afetar a disponibilidade de recursos neste lab. Você pode alterar a região, mas as etapas foram escritas usando o Leste dos EUA.

**Tempo estimado:** 30 minutos

---

## Cenário do lab

Sua organização está construindo um novo ambiente de lab para testes de pré-produção de aplicativos e serviços. Alguns engenheiros estão sendo contratados para gerenciar o ambiente de lab, incluindo as máquinas virtuais. Para permitir que os engenheiros se autentiquem usando o Microsoft Entra ID, você foi encarregado de provisionar usuários e grupos. Para minimizar a sobrecarga administrativa, a associação dos grupos deve ser atualizada automaticamente com base nos cargos.

---

## Diagrama de arquitetura

_Diagrama da arquitetura do lab 01._
![[Pasted image 20260511205504.png]]
---

## Habilidades do trabalho

- Tarefa 1: Criar e configurar contas de usuário.
- Tarefa 2: Criar grupos e adicionar membros.

---

## Tarefa 1: Criar e configurar contas de usuário

Nesta tarefa, você criará e configurará contas de usuário. As contas de usuário armazenarão dados do usuário, como nome, departamento, localização e informações de contato.

1. Entre no portal do Azure — https://portal.azure.com.
    
2. Para prosseguir para o portal, selecione **Cancelar** na tela inicial de boas-vindas do Azure.
    
    > **Observação:** O portal do Azure é usado em todos os labs. Se você é novo no Azure, pesquise e selecione **Centro de início rápido**. Reserve alguns minutos para assistir ao vídeo Introdução ao portal do Azure. Mesmo que você já tenha usado o portal antes, encontrará algumas dicas e truques para navegar e personalizar a interface.
    
3. Pesquise e selecione **Microsoft Entra ID**. O Microsoft Entra ID é a solução de gerenciamento de identidade e acesso baseada em nuvem do Azure. Reserve alguns minutos para se familiarizar com alguns dos recursos listados no painel esquerdo.
    
4. Selecione a folha **Visão geral** e, em seguida, a aba **Gerenciar locatários**.
    
    > **Você sabia?** Um locatário é uma instância específica do Microsoft Entra ID contendo contas e grupos. Dependendo da sua situação, você pode criar mais locatários e alternar entre eles.
    
5. Retorne à página do Entra ID pressionando voltar no navegador ou selecionando a opção no menu de navegação estrutural.
    
6. Se tiver tempo, explore outras opções, como **Licenças** e **Redefinição de senha**.
    

### Criar um novo usuário

1. Na folha **Gerenciar**, selecione **Usuários**; em seguida, no menu suspenso **Novo usuário**, selecione **Criar novo usuário**.
    
2. Crie um novo usuário com as seguintes configurações (deixe as demais com seus padrões). Na aba **Propriedades**, observe todos os diferentes tipos de informações que podem ser incluídas na conta de usuário.
    
|Configuração|Valor|
|---|---|
|Nome principal do usuário|`az104-user1`|
|Nome de exibição|`az104-user1`|
|Gerar senha automaticamente|marcado|
|Conta habilitada|marcado|
|Cargo (aba Propriedades)|`IT Lab Administrator`|
|Departamento (aba Propriedades)|`IT`|
|Local de uso (aba Propriedades)|`United States`|
    
3. Após terminar de revisar, selecione **Revisar + criar** e, em seguida, **Criar**.
    
4. Atualize a página e confirme que o novo usuário foi criado.
    

### Convidar um usuário externo

1. No menu suspenso **Novo usuário**, selecione **Convidar um usuário externo**.
    
    |Configuração|Valor|
    |---|---|
    |Email|seu endereço de email|
    |Nome de exibição|seu nome|
    |Enviar mensagem de convite|marcar a caixa|
    |Mensagem|`Welcome to Azure and our group project`|
    
2. Vá para a aba **Propriedades**. Preencha as informações básicas, incluindo estes campos.
    
    |Configuração|Valor|
    |---|---|
    |Cargo|`IT Lab Administrator`|
    |Departamento|`IT`|
    |Local de uso (aba Propriedades)|`United States`|
    
3. Selecione **Revisar + convidar** e, em seguida, **Convidar**.
    
4. Atualize a página e confirme que o usuário convidado foi criado. Em breve você deverá receber o email de convite.
    

> **Observação:** É improvável que você crie contas de usuário individualmente. Você sabe como sua organização planeja criar e gerenciar contas de usuário?

---

## Tarefa 2: Criar grupos e adicionar membros

Nesta tarefa, você criará uma conta de grupo. As contas de grupo podem incluir contas de usuário ou dispositivos. Estas são duas formas básicas pelas quais os membros são atribuídos a grupos: Estática e Dinamicamente. Grupos estáticos exigem que os administradores adicionem e removam membros manualmente. Grupos dinâmicos são atualizados automaticamente com base nas propriedades de uma conta de usuário ou dispositivo. Por exemplo, o cargo.

1. No portal do Azure, pesquise e selecione **Microsoft Entra ID**. Na folha **Gerenciar**, selecione **Grupos**.
    
2. Reserve um momento para se familiarizar com as configurações de grupo no painel esquerdo.
    
    - **Expiração** permite configurar um tempo de vida do grupo em dias. Após esse período, o grupo deve ser renovado pelo proprietário.
    - **Política de nomenclatura** permite configurar palavras bloqueadas e adicionar um prefixo ou sufixo aos nomes dos grupos.
3. Na folha **Todos os grupos**, selecione **+ Novo grupo** e crie um novo grupo.
    
    |Configuração|Valor|
    |---|---|
    |Tipo de grupo|`Security`|
    |Nome do grupo|`IT Lab Administrators`|
    |Descrição do grupo|`Administrators that manage the IT lab`|
    |Tipo de associação|`Assigned`|
    
    > **Observação:** Uma licença Entra ID Premium P1 ou P2 é necessária para associação dinâmica. Se outros tipos de associação estiverem disponíveis, as opções serão exibidas no menu suspenso.
    
4. Selecione **Nenhum proprietário selecionado**.
    
5. Na página **Adicionar proprietários**, pesquise e selecione você mesmo (exibido no canto superior direito) como proprietário. Observe que você pode ter mais de um proprietário.
    
6. Selecione **Nenhum membro selecionado**.
    
7. No painel **Adicionar membros**, pesquise e selecione o `az104-user1` e o usuário convidado que você convidou. Adicione ambos os usuários ao grupo.
    
8. Selecione **Criar** para implantar o grupo.
    
9. Atualize a página e verifique se o seu grupo foi criado.
    
10. Selecione o novo grupo e revise as informações de **Membros** e **Proprietários**.
    

> **Observação:** Você pode estar gerenciando um grande número de grupos. Sua organização tem um plano para criar grupos e adicionar membros?

---

## Principais conclusões

Parabéns por concluir o lab. Aqui estão algumas das principais conclusões deste lab:

- Um locatário representa sua organização e ajuda você a gerenciar uma instância específica dos serviços de nuvem da Microsoft para seus usuários internos e externos.
- O Microsoft Entra ID tem contas de usuário e de convidado. Cada conta tem um nível de acesso específico ao escopo do trabalho que se espera que seja realizado.
- Os grupos reúnem usuários ou dispositivos relacionados. Existem dois tipos de grupos: Segurança e Microsoft 365.
- A associação ao grupo pode ser atribuída de forma estática ou dinâmica.