# Lab 02b — Gerenciar Governança via Política do Azure

## Introdução ao lab

Neste lab, você aprende como implementar os planos de governança da sua organização. Você aprende como as políticas do Azure podem garantir que decisões operacionais sejam aplicadas em toda a organização. Você aprende como usar marcação de recursos para melhorar os relatórios.

Este lab requer uma assinatura do Azure. O tipo de assinatura pode afetar a disponibilidade de recursos neste lab. Você pode alterar a região, mas as etapas foram escritas usando o Leste dos EUA.

**Tempo estimado:** 30 minutos

---

## Cenário do lab

O ambiente de nuvem da sua organização cresceu consideravelmente no último ano. Durante uma auditoria recente, você descobriu um número substancial de recursos que não têm um proprietário, projeto ou centro de custo definido. Para melhorar o gerenciamento de recursos do Azure em sua organização, você decide implementar as seguintes funcionalidades:

- Aplicar marcas de recursos para anexar metadados importantes aos recursos do Azure
- Impor o uso de marcas de recursos para novos recursos usando a Política do Azure
- Atualizar recursos existentes com marcas de recursos
- Usar bloqueios de recursos para proteger recursos configurados

---

## Diagrama de arquitetura

![[Pasted image 20260512203218.png]]

---

## Habilidades do trabalho

- Tarefa 1: Criar e atribuir marcas por meio do portal do Azure.
- Tarefa 2: Impor marcação por meio de uma Política do Azure.
- Tarefa 3: Aplicar marcação por meio de uma Política do Azure.
- Tarefa 4: Configurar e testar bloqueios de recursos.

---

## Tarefa 1: Atribuir marcas por meio do portal do Azure

Nesta tarefa, você criará e atribuirá uma marca a um grupo de recursos do Azure por meio do portal do Azure. As marcas são um componente crítico de uma estratégia de governança conforme descrito pelo Microsoft Well-Architected Framework e pelo Cloud Adoption Framework. As marcas permitem que você identifique rapidamente proprietários de recursos, datas de encerramento, contatos de grupo e outros pares de nome/valor que sua organização considera importantes. Para esta tarefa, você atribui uma marca que identifica o Centro de Custo do recurso.

1. Entre no portal do Azure — https://portal.azure.com.
2. Pesquise e selecione **Grupos de recursos**.
3. Em Grupos de recursos, selecione **+ Criar** e use as seguintes configurações:

|Configuração|Valor|
|---|---|
|Nome da assinatura|sua assinatura|
|Nome do grupo de recursos|`az104-rg2`|
|Local|`East US`|

> **Observação:** Para cada lab neste curso, você criará um novo grupo de recursos. Isso permite localizar e gerenciar rapidamente seus recursos de lab.

4. Selecione **Próximo** e vá para a aba **Tags**. Forneça informações para uma nova tag:

|Configuração|Valor|
|---|---|
|Nome|`Cost Center`|
|Valor|`000`|

5. Selecione **Revisar + Criar** e, em seguida, selecione **Criar**.

---

## Tarefa 2: Impor marcação por meio de uma Política do Azure

Nesta tarefa, você atribuirá a política interna **Exigir uma marca e seu valor nos recursos** ao grupo de recursos e avaliará o resultado. A Política do Azure pode ser usada para impor configurações e, neste caso, governança aos seus recursos do Azure.

1. No portal do Azure, pesquise e selecione **Política**.
2. Na folha **Criação**, selecione **Definições**. Reserve um momento para navegar pela lista de definições de política integradas disponíveis. Observe que você também pode pesquisar uma definição.
3. Pesquise a política interna **Exigir uma marca e seu valor nos recursos**. Selecione a política e reserve um minuto para revisar a definição.
4. Selecione **Atribuir política**.
5. Especifique o **Escopo** clicando no botão de reticências e selecionando os seguintes valores. Clique em **Selecionar** quando terminar:

|Configuração|Valor|
|---|---|
|Assinatura|sua assinatura|
|Grupo de recursos|`az104-rg2`|

> **Observação:** Você pode atribuir políticas no nível do grupo de gerenciamento, assinatura ou grupo de recursos. Você também tem a opção de especificar exclusões, como assinaturas, grupos de recursos ou recursos individuais. Neste cenário, queremos a marca em todos os recursos do grupo de recursos.

6. Configure as propriedades de **Básico** da atribuição especificando as seguintes configurações (deixe as demais com seus padrões):

|Configuração|Valor|
|---|---|
|Nome da atribuição|`Require Cost Center tag and its value on resources`|
|Descrição|`Require Cost Center tag and its value on all resources in the resource group`|
|Imposição de política|Habilitado|

> **Observação:** O Nome da atribuição é preenchido automaticamente com o nome da política selecionada, mas você pode alterá-lo. A Descrição é opcional. Observe que você pode desabilitar a política a qualquer momento.

7. Clique em **Próximo** e defina os **Parâmetros** com os seguintes valores:

|Configuração|Valor|
|---|---|
|Nome da marca|`Cost Center`|
|Valor da marca|`000`|

8. Clique em **Próximo** e revise as abas **Correção** e **Identidade Gerenciada**. Deixe a caixa de seleção **Criar uma Identidade Gerenciada** desmarcada na aba Identidade Gerenciada.
9. Clique em **Revisar + Criar** e, em seguida, clique em **Criar**.

> **Observação:** Agora você verificará se a nova atribuição de política está em vigor tentando criar uma conta de Armazenamento do Azure no grupo de recursos. Você criará a conta de armazenamento sem adicionar a marca necessária.

> **Observação:** Pode levar entre 5 e 10 minutos para que a política entre em vigor.

10. No portal, pesquise e selecione **Contas de Armazenamento** e selecione **+ Criar**.
11. Na aba **Básico** da folha Criar conta de armazenamento, conclua a configuração:

|Configuração|Valor|
|---|---|
|Grupo de recursos|`az104-rg2`|
|Nome da conta de armazenamento|qualquer combinação globalmente exclusiva de 3 a 24 letras minúsculas e dígitos, começando com uma letra|

12. Selecione **Revisar** e, em seguida, clique em **Criar**.
13. Você deverá receber uma mensagem de **Falha na validação**. Visualize a mensagem para identificar o motivo da falha. Verifique se a mensagem de erro indica que a implantação do recurso foi negada pela política.

> **Observação:** Ao clicar na aba **Erro Bruto**, você pode encontrar mais detalhes sobre o erro, incluindo o nome da definição de função **Exigir uma marca e seu valor nos recursos**. A implantação falhou porque a conta de armazenamento que você tentou criar não tinha uma marca chamada `Cost Center` com seu valor definido como `Default`.

---

## Tarefa 3: Aplicar marcação por meio de uma Política do Azure

Nesta tarefa, usaremos a nova definição de política para corrigir quaisquer recursos não conformes. Neste cenário, faremos com que quaisquer recursos filho de um grupo de recursos herdem a marca `Cost Center` que foi definida no grupo de recursos.

1. No portal do Azure, pesquise e selecione **Política**.
2. Na seção **Criação**, clique em **Atribuições**.
3. Na lista de atribuições, clique no ícone de reticências na linha que representa a atribuição de política **Exigir uma marca e seu valor nos recursos** e use o item de menu **Excluir atribuição** para excluir a atribuição.
4. Clique em **Atribuir política** e especifique o **Escopo** clicando no botão de reticências e selecionando os seguintes valores:

|Configuração|Valor|
|---|---|
|Assinatura|sua assinatura do Azure|
|Grupo de recursos|`az104-rg2`|

5. Para especificar a **Definição de política**, clique no botão de reticências e pesquise e selecione **Herdar uma marca do grupo de recursos se ausente**.
6. Selecione **Adicionar** e configure as propriedades restantes de **Básico** da atribuição:

|Configuração|Valor|
|---|---|
|Nome da atribuição|`Inherit the Cost Center tag and its value 000 from the resource group if missing`|
|Descrição|`Inherit the Cost Center tag and its value 000 from the resource group if missing`|
|Imposição de política|Habilitado|

7. Clique em **Próximo** e defina os **Parâmetros** com os seguintes valores:

|Configuração|Valor|
|---|---|
|Nome da marca|`Cost Center`|

8. Clique em **Próximo** e, na aba **Correção**, configure as seguintes configurações (deixe as demais com seus padrões):

|Configuração|Valor|
|---|---|
|Criar uma tarefa de correção|habilitado|
|Política a ser corrigida|`Herdar uma marca do grupo de recursos se ausente`|

> **Observação:** Esta definição de política inclui o efeito **Modify**. Portanto, uma identidade gerenciada é necessária.

9. Clique em **Revisar + Criar** e, em seguida, clique em **Criar**.

> **Observação:** Para verificar se a nova atribuição de política está em vigor, você criará outra conta de armazenamento do Azure no mesmo grupo de recursos sem adicionar explicitamente a marca necessária.

> **Observação:** Pode levar entre 5 e 10 minutos para que a política entre em vigor.

10. Pesquise e selecione **Conta de Armazenamento** e clique em **+ Criar**.
11. Na aba **Básico** da folha Criar conta de armazenamento, verifique se você está usando o Grupo de Recursos ao qual a Política foi aplicada e especifique as seguintes configurações (deixe as demais com seus padrões) e clique em **Revisar**:

|Configuração|Valor|
|---|---|
|Nome da conta de armazenamento|qualquer combinação globalmente exclusiva de 3 a 24 letras minúsculas e dígitos, começando com uma letra|

12. Verifique se desta vez a validação foi aprovada e clique em **Criar**.
13. Após o provisionamento da nova conta de armazenamento, clique em **Ir para o recurso**.
14. Na folha **Marcas**, observe que a marca `Cost Center` com o valor `000` foi atribuída automaticamente ao recurso.

> **Você sabia?** Se você pesquisar e selecionar **Marcas** no portal, poderá visualizar os recursos com uma marca específica.

---

## Tarefa 4: Configurar e testar bloqueios de recursos

Nesta tarefa, você configura e testa um bloqueio de recurso. Os bloqueios impedem exclusões ou modificações de um recurso.

1. Pesquise e selecione seu grupo de recursos.
2. Na folha **Configurações**, selecione **Bloqueios**.
3. Selecione **Adicionar** e preencha as informações do bloqueio de recurso. Quando terminar, selecione **Ok**:

|Configuração|Valor|
|---|---|
|Nome do bloqueio|`rg-lock`|
|Tipo de bloqueio|`delete` (observe a seleção para somente leitura)|

4. Navegue até a folha **Visão geral** do grupo de recursos e selecione **Excluir grupo de recursos**.
5. Na caixa de texto **Inserir o nome do grupo de recursos para confirmar a exclusão**, forneça o nome do grupo de recursos, `az104-rg2`. Observe que você pode copiar e colar o nome do grupo de recursos.
6. Observe o aviso: _Excluir este grupo de recursos e seus recursos dependentes é uma ação permanente e não pode ser desfeita._ Selecione **Excluir**.
7. Você deverá receber uma notificação negando a exclusão.

> **Observação:** Você precisará remover o bloqueio se pretender excluir o grupo de recursos.

---

## Limpar seus recursos

Se você estiver trabalhando com sua própria assinatura, reserve um momento para excluir os recursos do lab. Isso garantirá que os recursos sejam liberados e o custo seja minimizado. A maneira mais fácil de excluir os recursos do lab é excluir o grupo de recursos do lab.

- No portal do Azure, selecione o grupo de recursos, selecione **Excluir o grupo de recursos**, insira o nome do grupo de recursos e clique em **Excluir**.
- Usando o Azure PowerShell: `Remove-AzResourceGroup -Name resourceGroupName`
- Usando a CLI: `az group delete --name resourceGroupName`

---

## Principais conclusões

Parabéns por concluir o lab. Aqui estão as principais conclusões deste lab.

- As marcas do Azure são metadados que consistem em um par chave-valor. As marcas descrevem um recurso específico em seu ambiente. Em particular, a marcação no Azure permite que você rotule seus recursos de forma lógica.
- A Política do Azure estabelece convenções para os recursos. As definições de política descrevem as condições de conformidade dos recursos e o efeito a ser aplicado se uma condição for atendida. Uma condição compara um campo de propriedade do recurso ou um valor a um valor necessário. Existem muitas definições de política integradas e você pode personalizar as políticas.
- O recurso de tarefa de correção da Política do Azure é usado para trazer recursos à conformidade com base em uma definição e atribuição. Os recursos que não estão em conformidade com uma atribuição de definição de modificação ou deployIfNotExist podem ser trazidos à conformidade usando uma tarefa de correção.
- Você pode configurar um bloqueio de recurso em uma assinatura, grupo de recursos ou recurso. O bloqueio pode proteger um recurso contra exclusões e modificações acidentais por usuários. O bloqueio substitui quaisquer permissões de usuário.
- A Política do Azure é uma prática de segurança pré-implantação. O RBAC e os bloqueios de recursos são práticas de segurança pós-implantação.