# Vídeo 1 - Download e instalação - Parte

VM up com Windows Server 2025 rodando  - ok

# Vídeo 2 - Configuração base - Parte 2

- Windows Update - ok
- Agent (VMWare tools) - ok
- Hostname - ok
- Rede - ok
- ![[Pasted image 20260806233744.png]]
	![[Pasted image 20260806233806.png]]
- Domínio - ok
- Administrator password - ok
- Firewall - ok
- Configuração de antivírus - ok
- Opções de desempenho - ok
- configuracao de hora e data - ok
- monitoring - ok
- limpeza - ok
- restart - ...

# Vídeo 3 - Como utilizar as funções e recursos - Parte 3

O **Server Manager** é o console central de administração do Windows Server, e uma das suas funções principais é justamente gerenciar **Roles (Funções)** e **Features (Recursos)** — tanto no servidor local quanto em servidores remotos.

## Diferença entre Roles e Features

**Roles (Funções)** são os "papéis" que o servidor desempenha na rede — coisas que definem para que aquele servidor existe. Exemplos:

- **AD DS** (Active Directory Domain Services) — vira um Domain Controller
- **DNS Server**
- **DHCP Server**
- **File and Storage Services**
- **Web Server (IIS)**

**Features (Recursos)** são componentes de suporte que complementam o sistema ou uma role, mas não definem sozinhos o propósito do servidor. Exemplos:

- **.NET Framework**
- **BitLocker Drive Encryption**
- **Windows Backup**
- **Failover Clustering**
- **Telnet Client**

## Como funciona o processo (Add Roles and Features Wizard)

Quando você abre o Server Manager e clica em **"Add roles and features"**, o wizard segue estes passos:

1. **Installation Type** — instalação baseada em role/feature ou instalação de Serviços de Área de Trabalho Remota (RDS)
2. **Server Selection** — escolhe o servidor de destino (pode ser o local ou qualquer servidor remoto já adicionado ao pool do Server Manager)
3. **Server Roles** — marca as roles desejadas (ex: AD DS)
4. **Features** — marca features adicionais
5. **Confirmation** — revisa tudo antes de instalar, com opção de reiniciar automaticamente se necessário
6. **Results** — mostra o progresso e o resultado da instalação

Para remover, o processo é o mesmo, mas via **"Remove Roles and Features"**, que abre um wizard parecido, desmarcando o que não é mais necessário.

## Gerenciamento remoto

Isso é um diferencial importante do Server Manager: ele permite adicionar/remover roles e features em **múltiplos servidores remotos** a partir de um único console, sem precisar logar em cada um via RDP. Você adiciona os servidores ao "Server Pool" (por nome, Active Directory, ou range de IP) e gerencia tudo centralizado — isso é bem alinhado com o que se cobra no AZ-104 sobre administração de VMs no Azure.

## Equivalente em PowerShell

Tudo que o wizard faz também pode ser feito via PowerShell, o que é útil para automação ou Server Core (que não tem GUI):

```powershell
# Listar roles/features disponíveis e instaladas
Get-WindowsFeature

# Instalar uma role (ex: AD DS)
Install-WindowsFeature -Name AD-Domain-Services -IncludeManagementTools

# Remover uma role
Uninstall-WindowsFeature -Name AD-Domain-Services
```


# Conexão de Área de Trabalho Remota – pt 04
# Habilitar Acesso RDP em um Servidor Windows

## 1. Criar o usuário local

**Via GUI (Computer Management):**

1. `Win + R` → `compmgmt.msc`
2. **Local Users and Groups** → **Users** → botão direito → **New User...**
3. Preencher nome, nome completo, descrição e senha → **Create**

**Via PowerShell:**

```powershell
$senha = Read-Host -AsSecureString "Digite a senha"
New-LocalUser -Name "mlopes" -Password $senha -FullName "Matheus Lopes" -Description "Usuário criado para acesso RDP"
```

> ⚠️ **Requisitos de senha** (política padrão do Windows): mínimo 7-8 caracteres, com pelo menos 3 dos 4 tipos — maiúscula, minúscula, número e caractere especial. Senhas fracas geram o erro `InvalidPasswordException`. Verificar política atual: `net accounts` ou `secpol.msc` → Account Policies → Password Policy.

## 2. Adicionar o usuário ao grupo Remote Desktop Users

**Via GUI:** `sysdm.cpl` → aba **Remote** → **Select Users...** → **Add...**

**Via PowerShell:**

```powershell
Add-LocalGroupMember -Group "Remote Desktop Users" -Member "mlopes"
```

## 3. Habilitar RDP no servidor

`Win + R` → `sysdm.cpl` → aba **Remote**:

- Marcar **"Allow remote connections to this computer"**
- (Recomendado) Marcar também **"Allow connections only from computers running Remote Desktop with Network Level Authentication (NLA)"**

## Fluxo completo em PowerShell

```powershell
# 1. Criar o usuário
$senha = Read-Host -AsSecureString "Digite a senha"
New-LocalUser -Name "mlopes" -Password $senha -FullName "Matheus Lopes" -Description "Usuário criado para acesso RDP"

# 2. Adicionar ao grupo de acesso remoto
Add-LocalGroupMember -Group "Remote Desktop Users" -Member "mlopes"
```

## Observações

- A porta **3389** (RDP) já é liberada automaticamente no firewall local ao habilitar RDP via `sysdm.cpl`. Em VM Azure/VMware, confirmar também NSG/regras de rede.
- Se o servidor for um **Domain Controller**, o usuário deve ser criado no **Active Directory** (`New-ADUser` ou ADUC), não como usuário local — DCs não usam contas locais tradicionais.