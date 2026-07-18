# 28.0 Introdução

## 28.0.1 Webster - Por que devo fazer este módulo?

Olá, sou eu, Webster. Você e Diego agora têm uma boa noção das funções de linha de comando do Cisco IOS. Isso facilitará muito a próxima tarefa de Diego. No novo local, ele terá que instalar e configurar todos os dispositivos, inclusive dispositivos de host, switches e roteadores, e toda a fiação necessária. Essa nova rede deve ser capaz de se comunicar com a rede da sede, além de poder acessar a internet. Isso é um pouco mais complicado do que minha rede doméstica, mas acho que posso fazê-lo, com uma pequena ajuda. É por isso que vou fazer este módulo. Espero que você se junte a mim!

## 28.0.2 O que vou aprender neste módulo?

**Titulo do Módulo:** Construir uma pequena rede Cisco

**Objetivo do Módulo:** Criar uma rede de computador simples com dispositivos Cisco.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Configuração Básica de Switch|Configurar definições iniciais em um switch Cisco.|
|Configurar definições iniciais em um switch Cisco.|Configurar as definições iniciais de um roteador.|
|Proteção dos Dispositivos|Configurar dispositivos para gerenciamento remoto seguro.|
|Configurar o gateway padrão|Configurar dispositivos para que usem o gateway padrão.|

# 28.1 Configuração Básica de Switch

## 28.1.1 Etapas da Configuração Básica de um Switch

O switch Cisco só precisa receber informações básicas de segurança antes de ser conectado à rede. Elementos que normalmente são configurados em um switch de LAN incluem: nome de host, informações de endereço IP de gerenciamento, senhas e informações descritivas.

O nome de host do switch é o nome configurado para o dispositivo. Como cada computador ou impressora tem um nome atribuído, o equipamento de rede deve ser configurado com um nome descritivo. Isso será útil se o nome do dispositivo incluir o local onde o switch será instalado, como mostrado na figura. Um exemplo seria: SW_Bldg_R-Room_216.

Um endereço IP de gerenciamento será necessário apenas se você configurar e gerenciar o switch através de uma conexão em banda na rede. Um endereço de gerenciamento permite acessar o dispositivo por clientes Telnet, SSH ou HTTP. As informações de endereço IP que devem ser configuradas em um switch são essencialmente as mesmas que você configura em um PC: endereço IP, máscara de sub-rede e gateway padrão.

Para proteger um switch Cisco LAN, é necessário configurar senhas em cada um dos métodos de acesso à linha de comando. Os requisitos mínimos incluem a atribuição de senha a métodos de acesso remoto, como Telnet, SSH e a conexão do console. Você também deve atribuir uma senha ao modo privilegiado no qual as alterações de configuração podem ser feitas.

**Observação:** Telnet envia o nome de usuário e a senha em texto simples e não é considerado seguro. O SSH é um método mais seguro, pois criptografa o nome de usuário e a senha.

**Selecione cada guia para obter mais informações.**

### Tarefas de configuração

Antes de configurar um switch, examine as tarefas iniciais de configuração de switch listadas na Figura:

Configurar o nome do dispositivo.

- **hostname** _nome_

Proteger o modo EXEC usuário.

- **line console 0**
- **senha** _senha_
- **login**

Proteger o acesso remoto Telnet/SSH

- **line vty 0 15**
- **senha** _senha_
- **login**

Proteger o modo EXEC privilegiado.

- **enable secret** _password_

Proteger todas as senhas do arquivo de configuração.

- **service password-encryption**

Apresentar a notificação legal.

- **banner motd** _delimiter mensagem delimiter_

Configurar SVI de gerenciamento.

- **interface vlan 1**
- **ip address** _ip-address subnet-mask_
- **no shutdown**

Salvar a configuração.

- **copy running-config startup-config**


### Exemplo de Configuração de um Switch

```
Switch> enable
Switch# configure terminal
Switch(config)# hostname S1
S1(config)# enable secret class
S1(config)# line console 0
S1(config-line)# password cisco
S1(config-line)# login
S1(config-line)# line vty 0 15
S1(config-line)# password cisco
S1(config-line)# login
S1(config-line)# exit
S1(config)# service password-encryption
S1(config)# banner motd #Nenhum acesso não autorizado permitido!#
S1(config)# interface vlan 1
S1(config-if)# ip address 192.168.1.20 255.255.255.0
S1(config-if)# no shutdown
S1(config-if)# end
S1# copy running-config startup-config
Destination filename [startup-config]?
Building configuration...
[OK]
S1#
```

## 28.1.2 Configuração da Interface Virtual de Switch

Para acessar o switch remotamente, um endereço IP e uma máscara de sub-rede devem ser configurados na SVI. Para configurar uma SVI em um switch, use o comando de configuração global **interface vlan 1** . Vlan 1 não é uma interface física real, mas virtual. Em seguida, atribua um endereço IPv4 usando o comando de configuração de interface **ip-address** _subnet-mask_. Por fim, ative a interface virtual com o comando de configuração de interface **no shutdown** .

Depois que o switch é configurado com esses comandos, o switch tem todos os elementos IPv4 prontos para comunicação pela rede local.

**Nota**: Semelhante aos hosts do Windows, os switches configurados com um endereço IPv4 normalmente também precisam ter um gateway padrão atribuído. Isso pode ser feito usando o comando de configuração global **ip default-gateway** _ip-address_ . O parâmetro _ip-address_ deve ser o endereço IPv4 do roteador local na rede, como mostrado no exemplo. No entanto, neste tópico, você configurará apenas uma rede com switches e hosts. Os roteadores serão configurados posteriormente.

```
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# interface vlan 1
Sw-Floor-1(config-if)# ip address 192.168.1.20 255.255.255.0
Sw-Floor-1(config-if)# no shutdown
Sw-Floor-1(config-if)# exit
Sw-Floor-1(config)# ip default-gateway 192.168.1.1
```

## 28.1.3 Verificador de sintaxe - Configurar uma interface virtual do switch

```
Entre no modo de configuração de interface da VLAN 1.

Switch(config)#interface vlan 1

Configure o endereço IPv4 como 192.168.1.20 e a máscara de sub-rede como 255.255.255.0.

Switch(config-if)#ip address 192.168.1.20 255.255.255.0

Habilite a interface.

Switch(config-if)#no shutdown

%LINK-5-CHANGED: Interface Vlan1, changed state to up

Você configurou com êxito a interface virtual do switch para a VLAN 1.
```


## 28.1.4 Packet Tracer - Implementação da conectividade básica

Nesta atividade, você completará os seguintes objetivos:

- Realizar uma configuração básica em S1 e S2
- Configurar os PCs
- Configurar a interface de gerenciamento do switch

> [!example]- 🖧 Recursos do Lab
> - 📄 [[anexos/28.1.4.html|Instruções]]
> - 📥 [[anexos/28.1.4.pka|Abrir no Packet Tracer]]

---
# 28.2 Configurar definições iniciais do roteador

## 28.2.1 Etapas da Configuração Básica de um Roteador

As tarefas a seguir devem ser concluídas ao configurar as configurações iniciais em um roteador.

**Etapa 1.** Configurar o nome do dispositivo.

```
Router(config)# hostname hostname
```

**Etapa 2.** Proteger o modo EXEC privilegiado.

```
Router(config)# enable secret password
```

**Etapa 3.** Proteger o modo EXEC usuário.

```
Router(config)# line console 0
Router(config-line)# password password
Router(config-line)# login
```

**Etapa 4.** Proteger o acesso remoto Telnet/SSH.

```
Router(config-line)# line vty 0 4
Router(config-line)# password password
Router(config-line)# login
Router(config-line)# transport input {ssh | telnet | none | all}
```

**Etapa 5.** Proteger todas as senhas do arquivo de configuração.

```
Router(config-line)# exit
Router(config)# service password-encryption
```

**Etapa 6.** Apresentar a notificação legal.

```
Router(config)# banner motd delimiter message delimiter
```

**Etapa 7.** Salvar a configuração.

```
Router(config)# copy running-config startup-config
```

## 28.2.2 Exemplo de Configuração Básica do Roteador

Neste exemplo, o roteador R1 será configurado com as configurações iniciais. Para configurar o nome do dispositivo para R1, use os seguintes comandos.

```
Router> enable
Router# configure terminal
Enter configuration commands, one per line.
End with CNTL/Z.
Router(config)# hostname R1
R1(config)#
```

**Observação:** Observe como o prompt do roteador agora exibe o nome de host do roteador.

Todo o acesso ao roteador deve ser protegido. O modo EXEC privilegiado fornece ao usuário acesso completo ao dispositivo e sua configuração.

Os comandos a seguir protegem o modo EXEC privilegiado e o modo EXEC do usuário, habilitam o acesso remoto Telnet e SSH e criptografam todas as senhas de texto simples (ou seja, EXEC do usuário e linha VTY). É muito importante usar uma senha forte ao proteger o modo EXEC privilegiado, pois esse modo permite o acesso à configuração do dispositivo.

```
R1(config)# enable secret class
R1(config)#
R1(config)# line console 0
R1(config-line)# password cisco
R1(config-line)# login
R1(config-line)# exit
R1(config)#
R1(config)# line vty 0 4
R1(config-line)# password cisco
R1(config-line)# login
R1(config-line)# transport input ssh telnet
R1(config-line)# exit
R1(config)#
R1(config)# service password-encryption
R1(config)#
```

A notificação legal avisa os usuários de que o dispositivo só deve ser acessado por usuários permitidos. A notificação legal é configurada da seguinte forma:

```
R1(config)# banner motd #
Enter TEXT message. End with the character '#'.
***********************************************
WARNING: Unauthorized access is prohibited!
***********************************************
R1(config)#
```

Se os comandos anteriores foram configurados e o roteador perdeu energia acidentalmente, todos os comandos configurados serão perdidos. Por esse motivo, é importante salvar a configuração quando as alterações são implementadas. O comando a seguir salva a configuração na NVRAM.

```
R1# copy running-config startup-config
Destination filename [startup-config]?
Building configuration...
[OK]
R1#
```

## 28.2.3 Verificador de sintaxe - Definição das configurações iniciais do roteador

Use este verificador de sintaxe para praticar a configuração das configurações iniciais em um roteador.

- Configurar o nome do dispositivo.
- Proteger o modo EXEC privilegiado.
- Proteja e habilite o acesso SSH e Telnet remoto.
- Proteja todas as senhas de texto sem formatação.
- Apresentar a notificação legal.


```
Entre no modo de configuração global para configurar o nome do roteador como "R1".

Router>enable
Router#configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)#hostname R1
Configure 'class' como a senha secreta.

R1(config)#enable secret class
Configure 'cisco' como a senha da linha do console, exija que os usuários efetuem login e retorne ao modo de configuração global.

R1(config)#line console 0
R1(config-line)#password cisco
R1(config-line)#login
R1(config-line)#exit
Para a linha vty 0 a 4, configure 'cisco' como a senha, exija que os usuários façam login, habilite o acesso SSH e Telnet e retorne ao modo de configuração global.

R1(config)#line vty 0 4
R1(config-line)#password cisco
R1(config-line)#login
R1(config-line)#transport input ssh telnet
R1(config-line)#exit
Criptografe todas as senhas em texto simples.

R1(config)#service password-encryption
Digite o banner "Somente acesso autorizado!" e use # como o caractere delimitante.

R1(config)#banner motd #Authorized Access Only!#
Saia do modo configuração global.

R1(config)#exit
R1#
Você configurou com êxito as configurações iniciais no roteador R1.
```

## 28.2.4 Packet Tracer – Definição das Configurações Iniciais de um Roteador

Nesta atividade, você completará os seguintes objetivos:

- Verificar a Configuração Padrão do Roteador
- Definir e Verificar a Configuração Inicial do Roteador
- Salvar o Arquivo de Configuração Ativa


# 28.3 Proteção dos Dispositivos

## 28.3.1 Recomendações de senha

É importante usar senhas fortes para proteger dispositivos de rede. Estas são as diretrizes padrão a serem seguidas:

- Use uma senha de pelo menos 8 caracteres, preferencialmente 10 ou mais caracteres. Uma senha mais longa é uma senha mais segura.
- Use senhas complexas. Inclua uma combinação de letras maiúsculas e minúsculas, números, símbolos e espaços, se permitido.
- Evite as senhas com base em repetição, palavras comuns de dicionário, sequências de letras ou números, nomes de usuário, nomes de parentes ou de animais de estimação, informações biográficas, como datas de nascimento, números de identificação, nomes de antepassados ou outras informações facilmente identificáveis.
- Deliberadamente, soletre errado uma senha. Por exemplo, Smith = Smyth = 5mYth ou Security = 5ecur1ty.
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

Nos roteadores Cisco, os espaços à esquerda são ignorados em senhas, mas os espaços após o primeiro caractere não são ignorados. Portanto, um método para criar uma senha forte é utilizar a barra de espaço e criar uma frase feita de muitas palavras. Isso se chama uma frase secreta. Uma frase secreta é geralmente mais fácil de lembrar do que uma senha simples. Também é maior e mais difícil de ser descoberta.


## 28.3.2 Secure Remote Access

Há várias maneiras de acessar um dispositivo para executar tarefas de configuração. Uma dessas formas é usar um PC conectado à porta de console no dispositivo. Esse tipo de conexão é mais usado na configuração inicial do dispositivo.

A definição de uma senha para o acesso de conexão de console é feita no modo de configurações globais. Esses comandos impedem que usuários não autorizados acessem o modo de usuário na porta do console.

```
Switch(config)# line console 0
Switch(config-line)# password password
Switch(config-line)# login
```

Quando o dispositivo é conectado à rede, pode ser acessado através da conexão de rede com o SSH ou o Telnet. SSH é o método preferido porque é mais seguro. Quando o dispositivo é acessado através da rede, este acesso é considerado uma conexão vty. A senha deve ser configurada na porta vty. A configuração a seguir é usada para habilitar o acesso SSH ao switch.

```
Switch(config)# line vty 0 15
Switch(config-line)# password password
Switch(config-line)# transport input ssh
Switch(config-line)# login
```

Um exemplo de configuração é mostrado na janela de comando.

```
S1(config)# line console 0
S1(config-line)# password cisco
S1(config-line)# login
S1(config-line)# exit
S1(config)#
S1(config)# line vty 0 15
S1(config-line)# password cisco
S1(config-line)# login
S1(config-line)#
```

Muitos switches Cisco são compatíveis com até 16 linhas VTY numeradas de 0 a 15. O número de linhas VTY aceitas varia de acordo com o tipo de dispositivo e a versão do IOS. No entanto, cinco é o número mais comum de linhas vty configuradas em um roteador. Essas linhas são numeradas de 0 a 4 por padrão, embora linhas adicionais possam ser configuradas. Uma senha precisa ser definida para todas as linhas vty disponíveis. A mesma senha pode ser estabelecida para todas as conexões.

Para verificar se as senhas estão definidas corretamente, use o comando **show running-config** . Essas senhas são armazenadas em running-configuration em texto simples. É possível definir a criptografia em todas as senhas armazenadas no roteador de modo que não sejam lidas facilmente por indivíduos não autorizados. O comando de configuração global **service password-encryption** garante que todas as senhas sejam criptografadas.

Com o acesso remoto protegido no switch, você pode configurar o SSH.


## 28.3.3 Ativar SSH

Antes de configurar o SSH, o switch deve ser minimamente configurado com as definições corretas de um nome de host exclusivo e de conectividade de rede.

**Etapa 1. Verifique o suporte a SSH.**

Use o comando **show ip ssh** para verificar se o switch suporta SSH. Se o switch não estiver executando um IOS que ofereça suporte a recursos criptográficos, esse comando não será reconhecido.

**Etapa 2. Configure o domínio IP.**

Configure o nome de domínio IP da rede usando o comando **ip domain-name** _domain-name_ global configuration mode. Na configuração de exemplo abaixo, o valor do _nome de domínio_ é **cisco.com**.

**Etapa 3. Gere pares de chaves RSA.**

Nem todas as versões do IOS padrão para SSH versão 2 e SSH versão 1 tem falhas de segurança conhecidas. Para configurar o SSH versão 2, emita o comando **ip ssh version 2** no modo de configuração global. Gerar um par de chaves RSA habilita automaticamente o SSH. Use o comando **crypto key generate rsa** no modo de configuração global para ativar o servidor SSH no switch e gerar um par de chaves RSA. Ao gerar chaves RSA, o administrador é solicitado a inserir um comprimento de módulo. A configuração de exemplo na figura usa um tamanho de módulo de 1.024 bits. Um comprimento de módulo mais longo é mais seguro, mas leva mais tempo para gerar e usar.

**Observação:** Para excluir o par de chaves RSA, use o comando **crypto key zeroize rsa** no modo de configuração global. Depois que o par de chaves RSA é excluído, o servidor SSH é desabilitado automaticamente.

**Etapa 4. Configure a autenticação do usuário.**

O servidor SSH pode autenticar usuários localmente ou usando um servidor de autenticação. Para usar o método de autenticação local, crie um par de nome de usuário e senha usando o comando **username** _nome do usuário_ **secret** _senha_ no modo de configuração global No exemplo, o usuário **admin** e designado a senha **ccna**.

**Etapa 5. Configure as linhas vty.**

Ative o protocolo SSH nas linhas vty usando o comando **transport input ssh** no modo de configuração de linha. O Catalyst 2960 tem linhas vty variando de 0 a 15. Essa configuração impede conexões não-SSH (como Telnet) e limita o switch para aceitar somente conexões SSH. Use o comando **line vty** no modo de configuração global e, em seguida, o comando **login local** no modo de configuração de linha para exigir autenticação local para conexões SSH do banco de dados de nome de usuário local.

**Etapa 6. Ative a versão 2 do SSH.**

Por padrão, o SSH suporta ambas as versões 1 e 2. Ao suportar ambas as versões, isso é mostrado na saída **show ip ssh** como suportando a versão 1.99. A versão 1 tem vulnerabilidades conhecidas. Por esse motivo, é recomendável habilitar apenas a versão 2. Ative a versão SSH usando o comando de configuração global **ip ssh version 2**.


```
S1# show ip ssh
SSH Disabled - version 1.99
%Please create RSA keys (of at least 768 bits size) to enable SSH v2.
Authentication timeout: 120 secs; Authentication retries: 3
S1# configure terminal
S1(config)# ip domain-name cisco.com
S1(config)# crypto key generate rsa
The name for the keys will be: S1.cisco.com
...
How many bits in the modulus [512]: 1024
...
S1(config)# username admin secret ccna
S1(config-line)# line vty 0 15
S1(config-line)# transport input ssh
S1(config-line)# login local
S1(config-line)# exit
S1(config)# ip ssh version 2
S1(config)# exit
S1#
```

## 28.3.4 Verificador de sintaxe - Configuração SSH

Use este verificador de sintaxe para configurar o SSH no switch S1

```
Set the domain name to cisco.com and generate the 1024 bit rsa key.

S1(config)#ip domain-name cisco.com
S1(config)#crypto key generate rsa
The name for the keys will be: S1.cisco.com  
Choose the size of the key modulus in the range of 360 to 4096 for your General Purpose Keys. Choosing a key modulus greater than 512 may take a few minutes.
How many bits in the modulus [512]:1024
% Generating 1024 bit RSA keys, keys will be non-exportable...  
[OK] (elapsed time was 4 seconds)  
  
S1(config)#  
*Mar 1 02:20:18.529: %SSH-5-ENABLED: SSH 1.99 has been enabled
Create a local user admin with the password ccna. Configure todas as linhas vty para usar o ssh e o login local para conexões remotas. Sair para o modo de configuração global.

S1(config)#username admin secret ccna
S1(config)#line vty 0 15
S1(config-line)#transport input ssh
S1(config-line)#login local
S1(config-line)#exit
S1(config)#  
%SYS-5-CONFIG_I: Configured from console by console
Configure S1 para usar SSH 2.0.

S1(config)#ip ssh version 2
S1(config)#
Você configurou com êxito SSH em todas as linhas VTY.
```


## 28.3.5 Verificar SSH

Em um PC, um cliente SSH, como PuTTY, é usado para se conectar a um servidor SSH. Para os exemplos, o seguinte foi configurado:

- SSH está habilitado no switch S1
- Interface VLAN 99 (SVI) com endereço IPv4 172.17.99.11 no switch S1
- PC1 com endereço IPv4 172.17.99.21

Na figura 1, o técnico inicia uma conexão de SSH com o endereço IPv4 da VLAN na SVI do S1. O software do terminal PuTTY é exibido.

![[Pasted image 20260625072310.png]]

Após clicar em Abrir no PuTTY, o usuário é solicitado a fornecer um nome de usuário e uma senha. Usando a configuração do exemplo anterior, o nome de usuário **admin** e senha **ccna** são inseridos. Depois de inserir a combinação correta, o usuário é conectado via SSH à CLI no switch Catalyst 2960.

Para exibir os dados de versão e configuração de SSH no dispositivo configurado como um servidor SSH, use o comando**show ip ssh.** No exemplo, SSH versão 2 está habilitado. Para verificar as conexões SSH com o dispositivo, use o comando **show ssh.**

```
Login as: admin
Using keyboard-interactive authentication.
Password: <ccna>
 
S1> enable
Password: <class>
S1# show ip ssh
SSH Enabled - version 2.0
Authentication timeout: 90 secs; Authentication retries: 2
Minimum expected Diffie Hellman key size : 1024 bits
IOS Keys in SECSH format(ssh-rsa, base64 encoded):
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAAAgQCdLksVz2QlREsoZt2f2scJHbW3aMDM8 /8jg/srGFNL
i+f+qJWwxt26BWmy694+6ZIQ/j7wUfIVNlQhI8GUOVIuKNqVMOMtLg8Ud4qAiLbGJfAaP3fyrKmViPpO
eOZof6tnKgKKvJz18Mz22XAf2u/7Jq2JnEFXycGMO88OUJQL3Q==
 
S1# show ssh
Connection Version Mode Encryption  Hmac        State        Username
0           2.0     IN   aes256-cbc  hmac-sha1 Session started admin
0           2.0     OUT  aes256-cbc  hmac-sha1 Session started admin
%No SSHv1 server connections running.
S1#
```

## 28.3.6 Packet Tracer - Configuração do SSH

Nesta atividade, você completará os seguintes objetivos:

- Proteger senhas
- Criptografar comunicações
- Verificar a implementação SSH

> [!example]- 🖧 Recursos do Lab
> - 📄 [[anexos/28.3.6.html|Instruções]]
> - 📥 [[anexos/28.3.6.pka|Abrir no Packet Tracer]]

---
# 28.4 Configurar o gateway padrão

## 28.4.1 Gateway padrão em um host

Se sua rede local tiver apenas um roteador, será o roteador gateway e todos os hosts e switches da rede deverão ser configurados com essas informações. Se sua rede local tiver vários roteadores, você deverá selecionar um deles para ser o roteador de gateway padrão. Este tópico explica como configurar o gateway padrão em hosts e switches.

Para que um dispositivo final se comunique pela rede, ele deve ser configurado com as informações de endereço IP, incluindo o endereço de gateway padrão. O gateway padrão só é usado quando o host deseja enviar um pacote a um dispositivo em outra rede. O endereço do gateway padrão geralmente é o endereço da interface do roteador associado à rede local do host. O endereço IP do dispositivo host e o endereço da interface do roteador devem estar na mesma rede.

Por exemplo, suponha que uma topologia de rede IPv4 consista em um roteador que interconecta duas LANs separadas. G0/0/0 está conectado à rede 192.168.10.0, enquanto G0/0/1 está conectado à rede 192.168.11.0. Cada dispositivo host está configurado com o endereço correto do gateway padrão.

Neste exemplo, se PC1 enviar um pacote para PC2, o gateway padrão não será usado. Em vez disso, o PC1 endereça o pacote com o endereço IPv4 do PC2 e encaminha o pacote diretamente para o PC2 através do comutador.

![[Pasted image 20260625072439.png]]

E se o PC1 enviou um pacote para o PC3? O PC1 endereçaria o pacote com o endereço IPv4 do PC3, mas encaminharia o pacote para seu gateway padrão, que é a interface G0/0/0 de R1. O roteador aceita o pacote e acessa sua tabela de roteamento para determinar que G0 / 0/1 é a interface de saída apropriada com base no endereço de destino. Em seguida, o R1 encaminha o pacote para fora da interface apropriada para alcançar o PC3.

![[Pasted image 20260625072451.png]]

O mesmo processo ocorreria em uma rede IPv6, embora isso não seja mostrado na topologia. Os dispositivos usariam o endereço IPv6 do roteador local como gateway padrão.

## 28.4.2 Gateway padrão em um switch

Um comutador que interconecta computadores clientes geralmente é um dispositivo da Camada 2. Como tal, um switch de Camada 2 não precisa de um endereço IP para funcionar corretamente. No entanto, uma configuração IP pode ser configurada em um switch para dar acesso remoto a um administrador ao switch.

Para se conectar e gerenciar um switch em uma rede IP local, ele deve ter uma interface virtual de switch (SVI) configurada. O SVI é configurado com um endereço IPv4 e uma máscara de sub-rede na LAN local. O switch também deve ter um endereço de gateway padrão configurado para gerenciar remotamente o switch de outra rede.

O endereço de gateway padrão geralmente é configurado em todos os dispositivos que se comunicam além da rede local.

Para configurar um gateway padrão IPv4 em um switch, use o comando de configuração global **ip default-gateway** _ip-address_ . O _ip-address_ que está configurado é o endereço IPv4 da interface do roteador local conectada ao switch.

A figura mostra um administrador estabelecendo uma conexão remota para o switch S1 em outra rede.

![[Pasted image 20260625072517.png]]

Neste exemplo, o host administrador usaria seu gateway padrão para enviar o pacote para a interface G0/0/1 de R1. R1 encaminharia o pacote para S1 fora de sua interface G0/0/0. Como o endereço IPv4 de origem do pacote veio de outra rede, S1 exigiria um gateway padrão para encaminhar o pacote para a interface G0/0/0 de R1. Portanto, o S1 deve ser configurado com um gateway padrão para poder responder e estabelecer uma conexão SSH com o host administrativo.

**Observação:** Os pacotes provenientes de hosts conectados ao switch já devem ter o endereço do gateway padrão configurado nos sistemas operacionais desses computadores.

Um switch de grupo de trabalho também pode ser configurado com um endereço IPv6 em um SVI. No entanto, o switch não requer que o endereço IPv6 do gateway padrão seja configurado manualmente. O switch receberá automaticamente seu gateway padrão da mensagem de anúncio do roteador ICMPv6 do roteador.

## 28.4.3 Verificador de Sintaxe — Configurar o Gateway Padrão

Use este verificador de sintaxe para praticar a configuração do gateway padrão de um switch da Camada 2.

```
Entre no modo de configuração global.

S1#configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Configure 192.168.10.1 como o gateway padrão para S1.

S1(config)#ip default-gateway 192.168.10.1
S1(config)#
Você configurou com êxito o gateway padrão no comutador S1.
```


## 28.4.4 Atividade Tutorada do Packet Tracer - Construir uma Rede de Switch e Roteador

Esta atividade monitorada do Packet Tracer inclui um sistema de dicas e um tutorial integrado. Você conectará os dispositivos, configurará os PCs, configurará o roteador, configurará o switch e verificará a conectividade de ponta a ponta.

> [!example]- 🖧 Recursos do Lab
> - 📄 [[anexos/28.4.4.html|Instruções]]
> - 📥 [[anexos/28.4.4.pka|Abrir no Packet Tracer]]

---
## 28.4.5 Packet Tracer - Solucionar problemas de gateway padrão

Nesta atividade, você completará os seguintes objetivos:

- Verificar a Documentação de Rede e Isolar Problemas
- Implementar, Verificar e Documentar Soluções

> [!example]- 🖧 Recursos do Lab
> - 📄 [[anexos/28.4.5.html|Instruções]]
> - 📥 [[anexos/28.4.5.pka|Abrir no Packet Tracer]]

---
# 28.5 Resumo de Construindo uma Rede Cisco Pequena

## 28.5.1 O que eu aprendi neste módulo?

### Configuração Básica de Switch

Os elementos a serem configurados em um switch LAN incluem nome do host, informações de endereço IP de gerenciamento, senhas e informações descritivas. Um endereço de gerenciamento permite acessar o dispositivo por clientes Telnet, SSH ou HTTP. As informações de endereço IP que devem ser configuradas em um switch incluem o endereço IP, a máscara de sub-rede e o gateway padrão. Para proteger switch Cisco LAN, configure senhas em cada um dos vários métodos de acesso à linha de comando. Atribua senhas a métodos de acesso remoto, como Telnet, SSH e a conexão do console. Atribua também uma senha ao modo privilegiado no qual as alterações de configuração podem ser feitas.

Para acessar o switch remotamente, configure um endereço IP e uma máscara de sub-rede no SVI. Use o comando de configuração global `interface vlan 1`. Atribua um endereço IPv4 usando o comando `ip address` _ip-address subnet-mask_ de configuração da interface. Por fim, ative a interface virtual com o comando de configuração de interface `no shutdown`. Após a configuração desses comandos, o switch terá todos os elementos IPv4 prontos para comunicação pela rede.

---

### Configurar definições iniciais do roteador

- **Etapa 1.** Configurar o nome do dispositivo.
- **Etapa 2.** Proteger o modo EXEC privilegiado.
- **Etapa 3.** Proteger o modo EXEC usuário.
- **Etapa 4.** Proteger o acesso remoto Telnet/SSH.
- **Etapa 5.** Proteger todas as senhas do arquivo de configuração.
- **Etapa 6.** Apresentar a notificação legal.
- **Etapa 7.** Salvar a configuração.

Todo o acesso ao roteador deve ser protegido. O modo EXEC privilegiado fornece ao usuário acesso completo ao dispositivo e sua configuração. É muito importante usar uma senha forte ao proteger o modo EXEC privilegiado, pois esse modo permite o acesso à configuração do dispositivo. A notificação legal avisa os usuários de que o dispositivo só deve ser acessado por usuários permitidos. A configuração do roteador seria perdida se o roteador perdesse energia. Por esse motivo, é importante salvar a configuração quando as alterações são implementadas.

---

### Proteção dos Dispositivos

É importante usar senhas fortes para proteger dispositivos de rede. Uma senha forte combina caracteres alfanuméricos e, se permitido, inclui símbolos e um espaço. Outro método para criar uma senha forte é usar a barra de espaço e criar uma frase feita de muitas palavras, chamada de passphrase. Uma passphrase geralmente é mais fácil de lembrar do que uma senha forte. Também é maior e mais difícil de ser descoberta.

A definição de uma senha para o acesso de conexão de console é feita no modo de configurações globais. Isso impede que usuários não autorizados acessem o modo de usuário da porta do console. Quando o dispositivo é conectado à rede, pode ser acessado através da conexão de rede com o SSH ou o Telnet. SSH é o método preferido porque é mais seguro. Quando o dispositivo é acessado através da rede, este acesso é considerado uma conexão vty. A senha deve ser configurada na porta vty. Cinco é o número mais comum de linhas vty configuradas em um roteador. Essas linhas são numeradas de 0 a 4 por padrão, embora linhas adicionais possam ser configuradas. Uma senha precisa ser definida para todas as linhas vty disponíveis. A mesma senha pode ser estabelecida para todas as conexões.

Para verificar se as senhas estão definidas corretamente, use o comando `show running-config`. Essas senhas são armazenadas em running-configuration em texto simples. É possível definir a criptografia em todas as senhas armazenadas no roteador. O comando de configuração global `service password-encryption` garante que todas as senhas sejam criptografadas.

---

### Para habilitar o SSH

- **Etapa 1.** Verifique o suporte SSH – `show ip ssh`
- **Etapa 2.** Configure o domínio IP – `ip domain-name` _domain-name_
- **Etapa 3.** Gerar pares de chaves RSA – `crypto key generate rsa`
- **Etapa 4.** Configurar autenticação de usuário – `username` _username_ `secret` _password_
- **Etapa 5.** Configurar as linhas vty – `line vty`
- **Etapa 6.** Ativar SSH versão 2 – `ip ssh version 2`

Para exibir os dados de versão e configuração de SSH no dispositivo configurado como um servidor SSH, use o comando `show ip ssh`. No exemplo, SSH versão 2 está habilitado. Para verificar as conexões SSH com o dispositivo, use o comando `show ssh`.

---
### Configurar o gateway padrão

Se sua rede local tiver apenas um roteador, será o roteador gateway e todos os hosts e switches da rede deverão ser configurados com essas informações. Se sua rede local tiver vários roteadores, você deverá selecionar um deles para ser o roteador de gateway padrão. O gateway padrão só é usado quando o host deseja enviar um pacote a um dispositivo em outra rede. O endereço IP do gateway padrão geralmente é o endereço da interface do roteador associado à rede local do host. O endereço IP do dispositivo host e o endereço da interface do roteador devem estar na mesma rede.

Para conectar e gerenciar um switch em uma rede IP local, ele deve ter um SVI configurado. O SVI é configurado com um endereço IPv4 e uma máscara de sub-rede na LAN local. O switch também deve ter um endereço de gateway padrão configurado para gerenciar remotamente o switch de outra rede. Para configurar um gateway padrão IPv4 em um switch, use o comando de configuração global `ip default-gateway` _ip-address_. O _ip-address_ que é configurado é o endereço IPv4 da interface do roteador local conectada ao switch.

---

## 28.5.2 Webster – Questões para Reflexão

É bom ter ajuda quando você tem um grande projeto, como Diego tem. Este módulo tem quase tudo o que preciso saber para configurar uma rede de filial. Com base no que você aprendeu neste curso até agora, aposto que você poderia ter ajudado o Diego. Você tem acesso a uma rede grande o suficiente para conter switches e mais de um roteador? Se sim, pergunte ao departamento de TI se você pode fazer um tour. Você pode se surpreender com o quanto você já entende!