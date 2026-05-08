- # Lab 02a — Gerenciar Assinaturas e RBAC
    
    ## Introdução ao lab
    
    Neste lab, você aprende sobre controle de acesso baseado em função. Você aprende como usar permissões e escopos para controlar quais ações as identidades podem e não podem executar. Você também aprende como facilitar o gerenciamento de assinaturas usando grupos de gerenciamento.
    
    Este lab requer uma assinatura do Azure. O tipo de assinatura pode afetar a disponibilidade de recursos neste lab. Você pode alterar a região, mas as etapas foram escritas usando o Leste dos EUA.
    
    **Tempo estimado:** 20 minutos
    
    * * *
    
    ## Cenário do lab
    
    Para simplificar o gerenciamento de recursos do Azure em sua organização, você foi encarregado de implementar as seguintes funcionalidades:
    
    - Criar um grupo de gerenciamento que inclua todas as suas assinaturas do Azure.
    - Conceder permissões para enviar solicitações de suporte para todas as assinaturas no grupo de gerenciamento. As permissões devem ser limitadas apenas a:
        - Criar e gerenciar máquinas virtuais
        - Criar tickets de solicitação de suporte (não incluir a adição de provedores do Azure)
    
    * * *
    
    ## Diagrama de arquitetura
    
    ![56c8392c4738918f9b157428b882c9fd.png](../_resources/56c8392c4738918f9b157428b882c9fd.png)
    
    * * *
    
    ## Habilidades do trabalho
    
    - Tarefa 1: Implementar grupos de gerenciamento.
    - Tarefa 2: Revisar e atribuir uma função integrada do Azure.
    - Tarefa 3: Criar uma função RBAC personalizada.
    - Tarefa 4: Monitorar atribuições de função com o Log de Atividades.
    
    * * *
    
    ## Tarefa 1: Implementar Grupos de Gerenciamento
    
    Nesta tarefa, você criará e configurará grupos de gerenciamento. Os grupos de gerenciamento são usados para organizar e segmentar assinaturas de forma lógica. Eles permitem que o RBAC e a Política do Azure sejam atribuídos e herdados para outros grupos de gerenciamento e assinaturas. Por exemplo, se sua organização tem uma equipe de suporte dedicada para a Europa, você pode organizar as assinaturas europeias em um grupo de gerenciamento para fornecer à equipe de suporte acesso a essas assinaturas (sem fornecer acesso individual a todas as assinaturas). Em nosso cenário, todos no Help Desk precisarão criar uma solicitação de suporte em todas as assinaturas.
    
    1.  Entre no portal do Azure — https://portal.azure.com.
        
    2.  Pesquise e selecione **Microsoft Entra ID**.
        
    3.  Na folha **Gerenciar**, selecione **Propriedades**.
        
    4.  Revise a área **Gerenciamento de acesso para recursos do Azure**. Observe que você pode gerenciar o acesso a todas as assinaturas do Azure e grupos de gerenciamento no locatário.
        
    5.  Pesquise e selecione **Grupos de gerenciamento**. (Pesquisar no Search resources, desatualizado)
        
    6.  Na folha **Grupos de gerenciamento**, clique em **\+ Criar**.
        
    7.  Crie um grupo de gerenciamento com as seguintes configurações. Selecione **Enviar** quando terminar.
        
        | Configuração | Valor |
        | --- | --- |
        | ID do grupo de gerenciamento | `az104-mg161600151` (deve ser único no diretório) |
        | Nome de exibição do grupo de gerenciamento | `az104-mg161600151` |
        
    8.  Atualize a página do grupo de gerenciamento para garantir que o novo grupo de gerenciamento seja exibido. Isso pode levar um minuto.
        
    
    > **Observação:** Você notou o grupo de gerenciamento raiz? O grupo de gerenciamento raiz é integrado à hierarquia para que todos os grupos de gerenciamento e assinaturas se consolidem nele. Esse grupo de gerenciamento raiz permite que políticas globais e atribuições de função do Azure sejam aplicadas no nível do diretório. Após criar um grupo de gerenciamento, você adicionaria quaisquer assinaturas que devem ser incluídas no grupo.
    
    * * *
    
    ## Tarefa 2: Revisar e atribuir uma função integrada do Azure
    
    Nesta tarefa, você revisará as funções integradas e atribuirá a função Colaborador de Máquina Virtual a um membro do Help Desk. O Azure fornece um grande número de funções integradas.
    
    > **Observação:** Nas etapas a seguir, você atribuirá a função ao grupo IT Helpdesk. Se você não tiver um grupo Help Desk, reserve um momento para criá-lo.
    
    1.  Selecione o grupo de gerenciamento `az104-mg161600151`.
        
    2.  Selecione a folha **Controle de acesso (IAM)** e, em seguida, a aba **Funções**.
        
    3.  Role pelas definições de função integradas disponíveis. Visualize uma função para obter informações detalhadas sobre **Permissões**, **JSON** e **Atribuições**. Você frequentemente usará proprietário, colaborador e leitor.
        
    4.  Selecione **\+ Adicionar**, no menu suspenso, selecione **Adicionar atribuição de função**.
        
    5.  Na folha **Adicionar atribuição de função**, pesquise e selecione **Colaborador de Máquina Virtual**. A função Colaborador de máquina virtual permite que você gerencie máquinas virtuais, mas não acesse o sistema operacional delas nem gerencie a rede virtual e a conta de armazenamento às quais estão conectadas. Esta é uma boa função para o Help Desk. Selecione **Próximo**.
        
        > **Você sabia?** O Azure originalmente fornecia apenas o modelo de implantação Clássico. Isso foi substituído pelo modelo de implantação do Azure Resource Manager. Como prática recomendada, não use recursos clássicos.
        
    6.  Na aba **Membros**, selecione **Selecionar membros**.
        
    7.  Pesquise e selecione o grupo **IT Helpdesk**. Clique em **Selecionar**.
        
    8.  Clique em **Revisar + atribuir** duas vezes para criar a atribuição de função.
        
    9.  Continue na folha **Controle de acesso (IAM)**. Na aba **Atribuições de função**, confirme se o grupo IT Helpdesk tem a função **Colaborador de Máquina Virtual**.
        
    
    > **Observação:** Como prática recomendada, sempre atribua funções a grupos, não a indivíduos.
    
    > **Você sabia?** Essa atribuição pode não conceder nenhum privilégio adicional. Se você já tem a função Proprietário, essa função inclui todas as permissões associadas à função Colaborador de VM.
    
    * * *
    
    ## Tarefa 3: Criar uma função RBAC personalizada
    
    Nesta tarefa, você criará uma função RBAC personalizada. As funções personalizadas são uma parte central da implementação do princípio do menor privilégio para um ambiente. As funções integradas podem ter permissões demais para o seu cenário. Também criaremos uma nova função e removeremos permissões que não são necessárias. Você tem um plano para gerenciar permissões sobrepostas?
    
    1.  Continue trabalhando no seu grupo de gerenciamento. Navegue até a folha **Controle de acesso (IAM)**.
        
    2.  Selecione **\+ Adicionar**, no menu suspenso, selecione **Adicionar função personalizada**.
        
    3.  Na aba **Básico**, conclua a configuração.
        
        | Configuração | Valor |
        | --- | --- |
        | Nome da função personalizada | `Custom Support Request61600151` |
        | Descrição | `A custom contributor role for support requests.` |
        
    4.  Em **Permissões de linha de base**, selecione **Clonar uma função**. No menu suspenso **Função a clonar**, selecione **Colaborador de Solicitação de Suporte**.<img src="../_resources/778778f2d784a2778138107a8929e97b.png" alt="778778f2d784a2778138107a8929e97b.png" width="412" height="272" class="jop-noMdConv">
        
    5.  Selecione **Próximo** para ir para a aba **Permissões** e, em seguida, selecione **\+ Excluir permissões**.
        
    6.  No campo de pesquisa do provedor de recursos, insira `.Support` e selecione **Microsoft.Support**.
        
    7.  Na lista de permissões, marque a caixa de seleção ao lado de **Outros: Registra o Provedor de Recursos de Suporte** e selecione **Adicionar**. A função deve ser atualizada para incluir essa permissão como uma NotAction.
        
        > **Observação:** Um provedor de recursos do Azure é um conjunto de operações REST que habilitam a funcionalidade para um serviço específico do Azure. Não queremos que o Help Desk tenha essa capacidade, portanto ela está sendo removida da função clonada.
        
    8.  Na aba **Escopos atribuíveis**, verifique se o seu grupo de gerenciamento está listado e clique em **Próximo**.
        
    9.  Revise o JSON para as **Actions**, **NotActions** e **AssignableScopes** que são personalizadas na função.
        
    10. Selecione **Revisar + Criar** e, em seguida, selecione **Criar**.
        
    
    > **Observação:** Neste ponto, você criou uma função personalizada e a atribuiu ao grupo de gerenciamento.
    
    * * *
    
    ## Tarefa 4: Monitorar atribuições de função com o Log de Atividades
    
    Nesta tarefa, você exibe o log de atividades para determinar se alguém criou uma nova função.
    
    1.  No portal, localize o recurso `az104-mg161600151` e selecione **Log de atividades**. O log de atividades fornece informações sobre eventos no nível da assinatura.
    2.  Revise as atividades para atribuições de função. O log de atividades pode ser filtrado para operações específicas.![0bed7b8627ce66640cb7f4e419b7d563.png](../_resources/0bed7b8627ce66640cb7f4e419b7d563.png)
- * * *
    
    ## Limpar seus recursos
    
    Se você estiver trabalhando com sua própria assinatura, reserve um momento para excluir os recursos do lab. Isso garantirá que os recursos sejam liberados e o custo seja minimizado. A maneira mais fácil de excluir os recursos do lab é excluir o grupo de recursos do lab.
    
    - No portal do Azure, selecione o grupo de gerenciamento, selecione **Excluir** e clique em **Sim** para confirmar a exclusão.
    - Usando o Azure PowerShell: `Remove-AzManagementGroup -GroupName az104-mg161600151`
    - Usando a CLI: `az account management-group delete --name az104-mg161600151`
    
    * * *
    
    ## Principais conclusões
    
    Parabéns por concluir o lab. Aqui estão as principais conclusões deste lab.
    
    - Os grupos de gerenciamento são usados para organizar assinaturas de forma lógica.
    - O grupo de gerenciamento raiz integrado inclui todos os grupos de gerenciamento e assinaturas.
    - O Azure tem muitas funções integradas. Você pode atribuir essas funções para controlar o acesso a recursos.
    - Você pode criar novas funções ou personalizar funções existentes.
    - As funções são definidas em um arquivo formatado em JSON e incluem Actions, NotActions e AssignableScopes.
    - Você pode usar o Log de Atividades para monitorar atribuições de função.