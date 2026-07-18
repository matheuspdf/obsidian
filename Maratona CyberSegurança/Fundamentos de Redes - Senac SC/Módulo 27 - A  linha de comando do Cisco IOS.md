# 27.0 Introdução

## 27.0.1 Webster - Por que devo fazer este módulo?

Olá! Tenho outro amigo que quero que conheçam. Diego acabou de ser contratado como membro júnior de um novo departamento de TI de uma pequena empresa de produção em Cusco, Peru. Essa empresa cria peças para equipamentos agrícolas e de moagem. Eles atualizaram e expandiram suas operações recentemente. Eles precisam de uma rede no segundo local que esteja conectada à nova rede na sede. A maioria dos equipamentos é fabricada pela Cisco, então Diego precisa aprender rapidamente as funções de linha de comando do Cisco IOS. Felizmente, há ajuda e Diego estará pronto e funcionando em pouco tempo. E você? Se você quiser saber mais sobre as funções de linha de comando do Cisco IOS, então este módulo é para você!

## 27.0.2 O que vou aprender neste módulo?

**Titulo do módulo:** A linha de comando do Cisco IOS

**Objetivo do módulo:** Use o Cisco IOS.

| Título do Tópico                  | Objetivo do Tópico                                                          |
| --------------------------------- | --------------------------------------------------------------------------- |
| Navegação IOS                     | Use os comandos corretos para navegar nos modos do Cisco IOS.               |
| A estrutura de comandos           | Explicar como navegar no Cisco IOS para configurar os dispositivos de rede. |
| Exibir Informações do dispositivo | Usar os comandos show para monitorar as operações do dispositivo.           |

# 27.1 Navegação IOS

## 27.1.1 Interface de linha de comando do Cisco IOS

A interface da linha de comando (CLI) do Cisco IOS é um programa baseado em texto que permite inserir e executar o comandos do Cisco IOS para configurar, monitorar e administrar dispositivos da Cisco. É possível usar a CLI da Cisco com tarefas de gerenciamento em banda ou fora da banda.

Os comandos da CLI são usados para modificar a configuração de dispositivo e exibir o status atual dos processos no roteador. Para usuários experientes, a CLI oferece muitos recursos de economia de tempo para criar configurações simples e complexas. Quase todos os dispositivos de rede da Cisco usam uma CLI semelhante. Quando o roteador conclui a sequência de inicialização e o prompt **Router>** aparece, a CLI pode ser usada para inserir comandos do Cisco IOS.

```
Router con0 is now available


Press RETURN to get started!



Router> enable
Router# configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)# hostname R1
R1(config)# interface gigabitethernet 0/0/0
R1(config-if)#
```

Os técnicos familiarizados com os comandos IOS e a operação de CLI facilmente monitoram e configuram diferentes dispositivos de rede porque os mesmos comandos básicos são usados configurar um switch e um roteador. A CLI tem um sistema amplo de ajuda que auxilia os usuários na configuração e no monitoramento de dispositivos.


## 27.1.2 Modos de Comando Primários

Todos os dispositivos de rede requerem um SO e podem ser configurados usando a CLI ou uma GUI. O uso da CLI pode fornecer ao administrador de rede controle e flexibilidade mais precisos do que usar a GUI. Este tópico aborda o uso da CLI para navegar pelo Cisco IOS.

Como recurso de segurança, o software Cisco IOS separa o acesso de gerenciamento nestes dois modos de comando:

- **Modo EXEC do usuário** - Este modo tem recursos limitados, mas é útil para operações básicas. Ele permite apenas um número limitado de comandos de monitoramento básicos, mas não permite a execução de nenhum comando que possa alterar a configuração do dispositivo. O modo EXEC usuário é identificado pelo prompt da CLI que termina com o símbolo >.
- **Modo EXEC privilegiado** - Para executar comandos de configuração, um administrador de rede deve acessar o modo EXEC privilegiado. Modos de configuração mais altos, como o modo de configuração global, só podem ser acessados do modo EXEC privilegiado. O modo EXEC privilegiado pode ser identificado pelo prompt que termina com o símbolo #.

A tabela resume os dois modos e exibe os prompts da CLI padrão de um switch e roteador Cisco.

|Modo de comando|Descrição|Prompt padrão do dispositivo|
|---|---|---|
|Modo EXEC do Usuário|O modo permite somente uma quantidade limitada de comandos básicos de monitoramento. Ele é frequentemente denominado modo "Somente visualização".|`Switch>` `Router>`|
|Modo EXEC privilegiado|O modo permite acesso a todos os comandos e recursos. O usuário pode utilizar qualquer comando de monitoramento e executar comandos de configuração e gerenciamento.|`Switch#` `Router#`|

## 27.1.3 Vídeo - Modos de Comando Primário da CLI do IOS
![[27.1.3.mp4#subtitle=anexos/27.1.3.vtt]]
Vamos examinar os modos de comando do Cisco IOS. Vou clicar em PC1, clicar no programa de emulação de terminal, clicar em ok e você pode ver que sou apresentado à linha de comando do console. Esse é o Cisco IOS.

Vou pressionar enter no meu teclado para começar. Observem o prompt de comando na parte inferior da tela. Ele indica o modo de comando em que estou.

O Cisco IOS usa diferentes modos de comando para estabelecer vários níveis de privilégio para usuários, e cada modo de comando inclui comandos diferentes. Por exemplo, a palavra `Switch`, que é o nome padrão do switch, com o sinal de maior do que (`>`), indica que estou no modo EXEC do usuário. Esse modo tem poucos privilégios, com acesso a apenas um número limitado de comandos.

Um dos comandos disponíveis neste modo é o comando `enable`. No cursor intermitente, vou digitar o comando `enable` e pressionar enter, e agora estou no modo EXEC privilegiado. Isso fica evidente porque o prompt mudou de um sinal de maior do que para um hash ou um sinal de libra (`#`).

O modo EXEC privilegiado oferece um nível mais privilegiado para o usuário e mais comandos estão disponíveis. Se eu quiser acessar um nível superior, posso entrar no modo de configuração global, ou modo de config global. Posso alcançar o modo de configuração global digitando `configure terminal` e pressionar Enter, e agora você pode ver o prompt de configuração global. Aqui é onde a maioria das configurações de um switch ou roteador são feitas.

Existem também alguns modos de configuração adicionais, como o modo de configuração de interface. Se eu digitar `interface vlan 1` e pressionar Enter, sou apresentado com um prompt que indica que agora estou no modo de configuração da interface.

Muitos comandos só funcionarão de dentro de determinados modos. Um erro comum cometido pelos usuários novos para trabalhar com o Cisco IOS está tentando usar comandos de dentro do modo errado. Se você tiver certeza de que está digitando um comando corretamente, mas continua recebendo uma mensagem de erro, sempre verifique o seu prompt para ter certeza de que você está no modo certo.

## 27.1.4 Vídeo - Navegar entre os modos IOS
![[27.1.4.mp4#subtitle=anexos/27.1.4.vtt]]
Vamos olhar para os comandos que são usados para alternar entre os diferentes modos de comando do IOS. Veremos o comando `enable`, o comando `disable`, `configure terminal`, `exit` e usar `Ctrl+Z` no teclado, mais alguns comandos para inserir diferentes modos de subconfiguração.

Eu tenho uma conexão de console com um switch, então vou clicar no PC 1 e pressionar Enter. Isso me leva ao modo User EXEC. Observe o prompt no canto inferior esquerdo da tela.

Para inserir o modo EXEC privilegiado, digite `enable`. Se eu quiser retornar ao modo EXEC do usuário, posso digitar `disable`. Digitarei `enable` para retornar ao modo EXEC Privilegiado.

Para configurar o switch, eu preciso primeiro acessar o modo de Configuração Global. Vou digitar `configure terminal`. E você pode ver agora que estou no prompt de Configuração Global.

Posso digitar `exit` e pressionar Enter para retornar ao modo EXEC privilegiado. Se eu digitar `exit` novamente, vou deixar a ligação do meu console toda junta. Para entrar novamente no switch e obter uma interface de linha de comando, eu tenho que pressionar Enter no meu teclado, e agora sou trazido de volta para a conexão do console com o switch.

Vou digitar `enable` e pressionar Enter, e, em seguida, `config t` — abreviação de `configure terminal` — e agora estou de volta ao modo de configuração global.

Vamos entrar em um dos modos de subconfiguração. Vou digitar `line console 0` para acessar a interface de gerenciamento da porta do console. Agora que estou em um modo de subconfiguração, se eu digitar `exit`, voltei ao modo de configuração global.

Desta vez, vou digitar `line vty 0 15` para minhas interfaces de gerenciamento de Terminal Virtual. Estas são usadas para acesso administrativo remoto para o switch.

Posso me mover diretamente de um modo de subconfiguração para outro. Observe que se eu digitar `interface vlan 1` e pressionar Enter, meu prompt foi alterado do modo de configuração de linha para o modo de configuração da interface.

A partir daqui, também posso inserir interfaces diferentes, como `interface fastethernet 0/1`, e desde que eu não veja uma mensagem de erro de comando inválido, estou no modo Interface Config para fastethernet 0/1. Eu também posso mover diretamente para `line console 0`.

Comandos que normalmente são executados no modo Configuração Global também podem ser executados de qualquer um dos modos de subconfiguração.

Se eu quiser sair de todos os modos de subconfiguração e retornar ao modo EXEC privilegiado, posso usar o comando `end` ou pressionar `Ctrl+Z` no meu teclado. Vou digitar `end` e pressionar Enter, e você pode ver agora que voltei todo o caminho de volta ao modo Privileged EXEC.

Voltarei ao modo de configuração global e depois na `line console 0`. Desta vez, vou manter pressionada a tecla `Ctrl` e pressionar `Z`. E se eu pressionar Enter, você pode ver que sou trazido todo o caminho de volta ao modo Privileged EXEC.

Se eu estiver no modo de configuração global e digitar `end` e pressionar Enter, também sou levado de volta ao modo EXEC Privilegiado.

Aprender a navegar de forma eficiente entre os diferentes modos de comando irá poupar muito tempo.

## 27.1.5 Uma observação sobre as atividades do verificador de sintaxe

Quando estiver aprendendo a modificar as configurações do dispositivo, convém começar em um ambiente seguro e que não seja de produção antes de experimentá-lo em equipamentos reais. O NetACAD oferece diferentes ferramentas de simulação para ajudar a desenvolver suas habilidades de configuração e solução de problemas. Como estas são ferramentas de simulação, elas geralmente não têm toda a funcionalidade de equipamentos reais. Uma dessas ferramentas é o Verificador de Sintaxe. Em cada Verificador de Sintaxe, você recebe um conjunto de instruções para inserir um conjunto específico de comandos. Você não pode progredir no Verificador de Sintaxe a menos que o comando exato e completo seja inserido conforme especificado. Ferramentas de simulação mais avançadas, como o Packet Tracer, permitem que você insira comandos abreviados, assim como faria em equipamentos reais.

## 27.1.6 Verificador de sintaxe - Navegar entre modos IOS

Use a atividade Verificador de sintaxe para navegar entre as linhas de comando do IOS em um switch.

Entre no modo EXEC privilegiado usando o comando `enable`

```
Switch>enable
```

Retorne ao modo EXEC do usuário usando o comando `disable`

```
Switch#disable
```

Digite novamente o modo EXEC privilegiado.

```
Switch>enable
```

Entre no modo de configuração global usando o comando `configure terminal`

```
Switch#configure terminal
```

Saia do modo de configuração global e retorne ao modo EXEC privilegiado usando o comando `exit`

```
Switch(config)#exit
```

Digite novamente o modo de configuração global.

```
Switch#configure terminal
```

Digite o modo de subconfiguração de linha para a porta do console usando o comando `line console 0`.

```
Switch(config)#line console 0
```

Retorne ao modo de configuração global usando o comando `exit`

```
Switch(config-line)#exit
```

Digite o modo de subconfiguração de linha VTY usando o comando `line vty 0 15`.

```
Switch(config)#line vty 0 15
```

Retorne ao modo de configuração global.

```
Switch(config-line)#exit
```

Entre no modo de subconfiguração da interface da VLAN 1 usando o comando `interface vlan 1`

```
Switch(config)#interface vlan 1
```

No modo de configuração da interface, alterne para o modo de subconfiguração do console de linha usando o comando de configuração `line console 0` global.

```
Switch(config-if)#line console 0
```

Retorne ao modo EXEC privilegiado usando o comando `end`

```
Switch(config-line)#end
```

Você navegou com êxito entre os vários modos de linha de comando do IOS.


## 27.1.7 Verifique sua compreensão - Navegação IOS

**Verifique sua compreensão sobre Navegação IOS escolhendo a melhor resposta para as seguintes perguntas.**

### Pergunta 1

Qual modo IOS permite acesso a todos os comandos e recursos?

- [ ] modo de configuração global
- [ ] Modo de subconfiguração da interface
- [ ] Modo de subconfiguração de console de linha
- [x] modo EXEC privilegiado
- [ ] modo EXEC usuário

✅ RESPOSTA CORRETA: modo EXEC privilegiado

> O modo EXEC privilegiado permite o acesso a todos os comandos. Comandos de nível superior, como o modo de configuração global e os modos de subconfiguração, só podem ser alcançados a partir do modo EXEC privilegiado.

---

### Pergunta 2

Em qual modo IOS você está se o prompt `Switch(config)#` for exibido?

- [x] modo de configuração global
- [ ] Modo de subconfiguração da interface
- [ ] Modo de subconfiguração de console de linha
- [ ] modo EXEC privilegiado
- [ ] modo EXEC usuário

✅ RESPOSTA CORRETA: modo de configuração global

> O modo de configuração global é identificado pelo prompt `(config)#`.

---

### Pergunta 3

Em que modo IOS você está se o prompt `Switch>` for exibido?

- [ ] modo de configuração global
- [ ] Modo de subconfiguração da interface
- [ ] Modo de subconfiguração de console de linha
- [ ] modo EXEC privilegiado
- [x] modo EXEC usuário

✅ RESPOSTA CORRETA: modo EXEC usuário

> O prompt `>` após o nome do dispositivo identifica o modo EXEC do usuário.

---

### Pergunta 4

Quais dois comandos o retornariam ao prompt EXEC privilegiado, independentemente do modo de configuração em que você está? (Escolha duas.)

- [x] Ctrl-Z
- [ ] disable
- [ ] enable
- [x] end
- [ ] exit

✅ RESPOSTA CORRETA: Ctrl-Z, end

> Para retornar de qualquer prompt até o modo EXEC privilegiado, digite o comando `end` ou pressione as teclas `CTRL+Z` simultaneamente no teclado.


# 27.2 A estrutura de comandos

## 27.2.1 Estrutura de Comandos Básicos do IOS

Um administrador de rede deve conhecer a estrutura básica de comandos do IOS para poder usar a CLI para a configuração do dispositivo.

Um dispositivo Cisco IOS é compatível com muitos comandos. Cada comando do IOS possui um formato ou sintaxe específica e pode ser executado apenas no modo apropriado. A sintaxe geral de um comando, mostrada na figura, é o comando seguido por quaisquer palavras-chave e argumentos apropriados.

![[Pasted image 20260623190854.png]]
- **Palavra-chave** - Este é um parâmetro específico definido no sistema operacional (na figura, **protocolos ip**).
- **Argumento** - Não é predefinido; é um valor ou variável definida pelo usuário (na figura, **192.168.10.5**).

Depois de inserir cada comando completo, incluindo palavras-chave e argumentos, pressione a tecla **Enter** para enviar o comando ao interpretador de comandos.

## 27.2.2 Sintaxe de Comandos do IOS

Um comando pode exigir um ou mais argumentos. Para determinar as palavras-chave e os argumentos necessários para um comando, consulte a sintaxe de comando. A sintaxe fornece o padrão, ou formato, que deve ser usado ao inserir um comando.

Conforme identificado na tabela, o texto em negrito indica comandos e palavras-chave inseridas conforme mostrado. O texto em itálico indica um argumento para o qual o usuário fornece o valor.

| Convenção    | Descrição                                                                                                                                                                |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **negrito**  | O texto em negrito indica comandos e palavras-chave que você insere literalmente, como mostradas.                                                                        |
| _itálico_    | O texto em itálico indica argumentos para os quais você fornece valores.                                                                                                 |
| [x]          | Colchetes indicam um elemento opcional (palavra-chave ou argumento).                                                                                                     |
| {x}          | Chaves indicam um elemento necessário (palavra-chave ou argumento).                                                                                                      |
| [x {y \| z}] | Chaves e linhas verticais entre colchetes indicam uma escolha obrigatória dentro de um elemento opcional. Espaços são usados para delinear claramente partes do comando. |

Por exemplo, a sintaxe para usar o comando **description** é **description** _string_. O argumento é um valor _string_ fornecido pelo usuário. O comando **description** é normalmente usado para identificar a finalidade de uma interface. Por exemplo, digitando o comando, **description Connects no switch** principal do escritório da matriz, descreve onde o outro dispositivo está no final da conexão.

Os exemplos a seguir demonstram as convenções usadas para documentar e utilizar comandos do IOS:

- **ping** _ip-address_ - O comando é **ping**, e o argumento definido pelo usuário _ip-address_ é o endereço IP do dispositivo de destino. Por exemplo, **ping 10.10.10.5**.
- **traceroute** _ip-address_ - O comando é **traceroute**, e o argumento definido pelo usuário _ip-address_ é o endereço IP do dispositivo de destino. Por exemplo, **traceroute 192.168.254.254**.

Se um comando é complexo com vários argumentos, você pode vê-lo representado assim:

```
Switch(config-if)# switchport port-security aging { static | time time | type {absolute | inactivity}}
```

O comando normlamente vem seguido de uma descrição detalhada do comando e cada argumento no Referênica de Comando no Cisco IOS.

A Referência de Comandos do Cisco IOS é a fonte definitiva de informações para um determinado comando do IOS.

## 27.2.3 Vídeo - Ajuda Sensível ao Contexto e Verificação da Sintaxe do Comando

![[27.2.3.mp4#subtitle=anexos/27.2.3.vtt]]
O comando de ajuda do Cisco IOS é acessado com um ponto de interrogação (`?`). O comando help é sensível ao contexto, então como e onde usar a interrogação é importante.

Por exemplo, digamos que eu queira uma lista de todos os comandos que estão disponíveis para mim no modo user-exec. Basta digitar uma interrogação e receberei os comandos que estão disponíveis no modo EXEC do usuário. Basta digitar `enable` e entro no modo EXEC privilegiado. Se eu inserir um ponto de interrogação, receberei os comandos que estão disponíveis no modo privileged-exec. Pressionarei a barra de espaço para ir à próxima página dos resultados.

Um conjunto diferente de comandos está disponível no modo de configuração global. Basta acessar o modo de configuração global e inserir um ponto de interrogação para receber um conjunto diferente de comandos disponibilizados nesse modo de comando.

Há outros usos para o comando help também. Digamos que eu não queira uma lista de todos os comandos disponíveis, e eu só quero ajuda para terminar um comando em particular. Por exemplo, digamos que estou colocando o comando `interface`, mas esqueci o nome completo do comando. Digitei `in` e preciso de ajuda para concluir o comando. Posso colocar em parte do comando e inserir um ponto de interrogação para receber ajuda para completá-lo. Eu digitei `in?` e o comando de ajuda retornou que o comando que eu procuro é `interface`.

Também posso usar o comando de ajuda em outro contexto. Agora que sei que o comando é `interface`, digamos que eu não saiba qual é o próximo parâmetro ou argumento que acompanha o comando interface. Nesse caso, devo inserir um espaço e uma interrogação (`interface ?`) e ele vai me dizer o próximo parâmetro ou argumento exigido pelo comando interface. Agora sei que a próxima parte do comando pode ser o nome da interface, como Ethernet, FastEthernet, GigabitEthernet, ou talvez seja vlan ou range.

Um comando relacionado ao de ajuda é o verificador de sintaxe. O comando verificador de sintaxe me avisará quando eu tiver um problema com um comando inserido. Por exemplo, podemos ver que a próxima parte deste comando seria um desses argumentos. Digamos que eu errei e digitei o número `33` em vez de `vlan` ou `range` e pressione Enter. Observe que o verificador de sintaxe de comandos me informou que começando no número três, fiz uma entrada inválida. Isso é extremamente útil porque me ajuda a isolar onde está o problema com o comando específico que eu inseri.

Isso pode funcionar em diferentes contextos também. Por exemplo, digamos que eu insira apenas a letra `i` em vez de `interface` e pressione Enter. O verificador de sintaxe informa que a letra `i` é um comando ambíguo. A razão é que, se eu digitar `i?`, na verdade existem dois comandos que começam com a letra `i` no modo de configuração global: o comando `interface` e o comando `ip`.

O terceiro exemplo do verificador de sintaxe é que, ao digitar `interface` e pressionar Enter, o verificador de sintaxe de comando me informou que o comando está incompleto. Para solucionar esse problema, basta reinserir `interface`, um espaço e um ponto de interrogação e recebo o próximo conjunto de opções que eu preciso para terminar este comando.

Você pode ver como o comando help é muito útil ao aprender os diferentes comandos que estão disponíveis para você, bem como o contexto correto e uso dos diferentes comandos.

## 27.2.4 Teclas de Atalho e Atalhos

A CLI do IOS fornece teclas de atalho e atalhos que facilitam a configuração, o monitoramento e a solução de problemas.

Os comandos e as palavras-chave podem ser abreviados para o número mínimo de caracteres que identifica uma seleção exclusiva. Por exemplo, o comando **configure** pode ser abreviado para **conf** porque **configure** é o único comando que se inicia com **conf**. Uma versão ainda mais curta , **con** não dará certo porque mais de um comando se inicia com **con**. Palavras-chave também podem ser abreviadas.

A tabela lista os pressionamentos de teclas para aprimorar a edição da linha de comando.

|Toque de tecla|Descrição|
|---|---|
|**Tabulação**|Completa um nome de comando parcialmente digitado.|
|**Backspace**|Apaga o caractere à esquerda do cursor.|
|**Ctrl+D**|Apaga o caractere no cursor.|
|**Ctrl+K**|Apaga todos os caracteres do cursor até o final da linha de comando.|
|**Esc D**|Apaga todos os caracteres do cursor até o final da palavra.|
|**Ctrl+U** ou **Ctrl+X**|Apagam todos os caracteres do cursor até o início da linha de comando.|
|**Ctrl+W**|Apaga a palavra à esquerda do cursor.|
|**Ctrl+A**|Move o cursor para o início da linha.|
|**Seta para a esquerda** ou **Ctrl+B**|Movem o cursor um caractere para a esquerda.|
|**Esc B**|Move o cursor uma palavra para a esquerda.|
|**Esc F**|Move o cursor uma palavra para a direita.|
|**Seta para a direita** ou **Ctrl+F**|Movem o cursor um caractere para a direita.|
|**Ctrl+E**|Move o cursor para o final da linha de comando.|
|**Seta para cima** ou **Ctrl+P**|Relembram os comandos no buffer de histórico, a partir dos comandos mais recentes.|
|**Seta para baixo** ou **Ctrl+N**|Vai para a próxima linha no buffer do histórico.|
|**Ctrl+R** ou **Ctrl+I** ou **Ctrl+L**|Reexibem o prompt do sistema e a linha de comando após o uma mensagem ter sido exibida no console.|

**Nota:** Embora a tecla **Delete** normalmente exclua o caractere à direita do prompt, a estrutura de comando do IOS não reconhece a tecla **Delete**.

Quando uma saída de comando produz mais texto do que pode ser exibido em uma janela de terminal, o IOS exibirá um prompt `--More--`. A tabela a seguir descreve os pressionamentos de teclas que podem ser usados quando esse prompt é exibido.

|Toque de tecla|Descrição|
|---|---|
|**Entrar**|Exibe a próxima linha.|
|**Espaço**|Exibe a próxima tela.|
|Qualquer outra chave*|Termina a sequência de exibição, retornando para o prompt anterior. * Exceto "y", que responde "sim" para o prompt `--Mais--` e atua como o **espaço**.|

Esta tabela lista os comandos usados para sair de uma operação.

|Toque de tecla|Descrição|
|---|---|
|**Ctrl-C**|Em qualquer modo de configuração, finaliza o modo de configuração e retorna ao modo EXEC privilegiado. No modo de instalação, volta para o prompt de comando.|
|**Ctrl-Z**|Em qualquer modo de configuração, finaliza o modo de configuração e retorna ao modo EXEC privilegiado.|
|**Ctrl-Shift-6**|Sequência de quebra para todos os fins usada para abortar pesquisas de DNS, traceroutes, pings e interromper um processo de IOS.|

## 27.2.5 Vídeo - Teclas de Atalho e Atalhos

![[27.2.5.mp4#subtitle=anexos/27.2.5.vtt]]
O suporte a teclas de atalho faz o Cisco IOS ser extremamente eficiente. Fazendo uso deles você vai economizar muito tempo quando você está configurando dispositivos.

A primeira tecla de atalho é a tecla **Tab**, ou conclusão de Tab, para completar automaticamente seus comandos. Para chegar ao Modo EXEC Privilegiado, eu normalmente digitaria o comando `enable`. Com o preenchimento Tab, você simplesmente digita as primeiras letras do comando, neste caso `EN`, e pressione a tecla Tab no seu teclado e o comando é concluído automaticamente para você. Isso funcionará se apenas um comando começar com as letras digitadas.

Por exemplo, se eu quiser colocar o comando `configure terminal` e digito `CON` e pressiono Tab, não funciona, pois há mais de um comando começando com as letras `CON` no Modo EXEC Privilegiado. Se eu quiser usar o preenchimento via Tab, vou precisar digitar `CONF` e pressionar a tecla Tab. Para `terminal`, tudo o que preciso fazer é digitar a letra `T` e pressionar a tecla Tab, pois há apenas um argumento ou comando secundário que segue `configure` e começa com a letra `T`.

Ainda melhor do que usar a tecla Tab é a **abreviatura do comando**. Com abreviatura de comandos, em vez de pressionar a tecla Tab para completar o comando, você simplesmente usa as primeiras letras do comando e o IOS aceitará o comando abreviado sem pressionar a tecla Tab. Por exemplo, em vez de digitar o comando `interface fastethernet 0/1`, que é um comando muito longo para digitar, eu posso encurtar o comando para apenas `INT F 0/1` e pressionar Enter. O IOS sabe automaticamente o comando que eu quero e o executa. No entanto, você não verá a exibição do comando completo como você faz com o preenchimento Tab.

Às vezes é necessário repetir comandos. A maneira mais rápida de fazer isso é navegar pelo seu **histórico de comandos** usando as teclas de seta para cima e seta para baixo. Pressionar a tecla de seta para baixo irá levar-me para a frente no meu histórico de comandos. Isso é muito útil para comandos que são usados repetidamente.

Vamos dar uma olhada em algumas teclas de atalho:

- `Ctrl+Z` e `Ctrl+C` terão a função de voltar para o Modo EXEC Privilegiado. `Ctrl+C` também pode ser usado para abortar certos comandos.
- `Ctrl+A` irá levar o cursor para o início de uma linha.
- `Ctrl+E` move o cursor para o final da linha.
- `Ctrl+Shift+6` interromperá a execução de um comando após o comando já ter sido inserido. Por exemplo, se o IOS está tentando traduzir letras digitadas incorretamente em um endereço IP, basta pressionar `Ctrl+Shift+6` e o comando é abortado.
- `Ctrl+R` retorna ao prompt onde o comando parcial será exibido, permitindo que você termine de digitar, caso uma mensagem de evento tenha interrompido o comando que você estava digitando.

Usar teclas de atalho e atalhos é uma ótima maneira para economizar seu tempo ao trabalhar com o Cisco IOS.

## 27.2.6 Packet Tracer - Navegue no IOS

Nesta atividade do Packet Tracer, você atingirá os seguintes objetivos:

- Parte 1: Estabelecer conexões básicas, acesso à CLI e explorar a ajuda
- Parte 2: Explorar modos EXEC
- Parte 3: Ajustar o Relógio

> [!example]- 🖧 Recursos do Lab
> - 📄 [[anexos/27.2.6.html|Instruções]]
> - 📥 [[anexos/27.2.6.pka|Abrir no Packet Tracer]]

---
# 27.3 Exibir Informações do dispositivo

## 27.3.1 Vídeo - Comandos Show Cisco IOS

![[27.3.1.mp4#subtitle=anexos/27.3.1.vtt]]
Neste vídeo, vamos dar uma olhada em alguns dos comandos show básicos em um roteador Cisco IOS.

O primeiro comando é `show running-config`. O que este comando nos mostra é a configuração atual neste roteador — todos os comandos que foram configurados neste roteador. Por exemplo, temos o nome de host `R1`, uma senha do EXEC privilegiado, a configuração da interface para `FastEthernet 0/0` e o endereço IPv4. Rolando para baixo, podemos ver outras configurações, como a configuração da interface para `serial0/0/0`, sua máscara de sub-rede e o endereço IPv4. Também podemos ver que este roteador foi configurado para usar o protocolo de roteamento RIP, que a porta do console foi configurada com uma senha, e que o VTY — Virtual Terminal Telnet Access — foi configurado para este dispositivo.

O comando `show interfaces` nos mostrará informações semelhantes para todas as interfaces neste roteador.

O comando `show arp` mostra a tabela ARP para este roteador. Neste caso, está nos mostrando a tabela ARP para a porta `FastEthernet0/0`. Se este roteador tiver mais de uma porta Ethernet, ele nos mostraria as entradas ARP para cada uma das portas Ethernet que foram conectadas a este roteador.

O comando `show ip route` exibe a tabela de roteamento neste roteador. A informação que irá mostrar é de qualquer interface diretamente conectada — podemos ver isso com um `C`. Estas são as interfaces neste roteador onde o roteador tem um endereço IPv4 e assim estão diretamente conectadas a essa rede. Também vemos `R`, que significa RIP, Routing Information Protocol. RIP é um protocolo de roteamento dinâmico. O roteador aprendeu essa rota dinamicamente, automaticamente de outro roteador.

O comando `show protocols` mostra informações globais e específicas para qualquer uma das interfaces de camada 3.

O comando `show version` exibe informações sobre o sistema operacional e algumas informações de hardware sobre este roteador. Por exemplo, ele exibe a versão do sistema operacional — neste caso `12.4` — informações sobre as interfaces neste roteador, a quantidade de NVRAM, memória e outros tipos de informação.

Esses comandos e muitos outros podem ser usados para ajudar a verificar e solucionar problemas de operações de rede. Existem diferentes variações para cada um desses comandos. À medida que você desenvolve mais habilidades com o uso do sistema operacional, você aprenderá a usar e interpretar a saída desses comandos show.

## 27.3.2 Comandos 'Show'

O Cisco IOS fornece comandos para verificar a operação de interfaces de roteador e switch.

Os comandos **show** da CLI do Cisco IOS exibem informações importantes sobre a configuração e a operação do dispositivo. Os técnicos de rede usam os comandos **show** extensivamente para visualizar arquivos de configuração, verificar o status das interfaces e processos do dispositivo e verificar o status operacional do dispositivo. O status de quase todos os processos ou funções do roteador pode ser exibido por meio de um comando **show**.

Comandos **show** comumente usados e quando usá-los são listados na tabela.

| Comando               | Usado para                                                            |
| --------------------- | --------------------------------------------------------------------- |
| `show running-config` | Verifique as definições e configurações atuais.                       |
| `show interfaces`     | Verifique o status da interface e veja se há alguma mensagem de erro. |
| `show ip interface`   | Verifica informação de camada 3 de uma interface.                     |
| `show arp`            | Verifica a lista de hosts conhecidos nas LANs Ethernet locais.        |
| `show ip route`       | Verifica as informações de roteamento da Camada 3.                    |
| `show protocols`      | Verifica quais protocolos estão operacionais.                         |
| `show version`        | Verifica a memória, as interfaces e as licenças do dispositivo.       |

### **show running-config**

Verifique as definições e configurações correntes.

```
R1# show running-config

(Saída omitida)

!
versão 15.5
service timestamps debug datetime msec
service timestamps log datetime msec
service password-encryption
!
hostname R1
!
interface GigabitEthernet0/0/0
 description Link para R2
 ip address 209.165.200.225 255.255.255.252
 negotiation auto
!
interface GigabitEthernet0/0/1
 description Link para a LAN
 ip address 192.168.10.1 255.255.255.0
 negotiation auto
!
router ospf 10
 network 192.168.10.0 0.0.0.255 area 0
 network 209.165.200.224 0.0.0.3 area 0
!
banner motd ^C Apenas acesso autorizado! ^C
!
line con 0
 password 7 14141B180F0B
 login
line vty 0 4
 password 7 00071A150754
 login
 transport input telnet ssh
!
end
R1#
```

### **show interfaces**

Verifica o status da interface e mostra quaisquer mensagens de erro.

```
R1# show interfaces
GigabitEthernet0/0/0 is up, line protocol is up
  Hardware is ISR4321-2x1GE, address is a0e0.af0d.e140 (bia a0e0.af0d.e140)
  Description: Link para R2
  O endereço da Internet é 209.165.200.225/30
  MTU 1500 bytes, BW 100000 Kbit/sec, DLY 100 usec,
    reliability 255/255, txload 1/255, rxload 1/255
  Encapsulation ARPA, loopback not set
  Keepalive not supported
  Full Duplex, 100Mbps, link type is auto, media type is RJ45
  output flow-control is off, input flow-control is off
  ARP type: ARPA, ARP Timeout 04:00:00
  Last input 00:00:01, output 00:00:21, output hang never
  Last clearing of "show interface" counters never
  Input queue: 0/375/0/0 (size/max/drops/flushes); Total output drops: 0
  Queueing strategy: fifo
  Output queue: 0/40 (size/max)
  5 minute input rate 0 bits/sec, 0 packets/sec
  5 minute output rate 0 bits/sec, 0 packets/sec
    5127 packets input, 590285 bytes, 0 no buffer
    Received 29 broadcasts (0 IP multicasts)
    0 runts, 0 giants, 0 throttles
    0 input errors, 0 CRC, 0 frame, 0 overrun, 0 ignored
    watchdog, 5043 multicast, 0 pausa de entrada
    watchdog, 5043 multicast, 0 pausa de entrada
    0 output errors, 0 collisions, 2 interface resets
    0 unknown protocol drops
    0 babbles, 0 late collision, 0 deferred
    1 lost carrier, 0 no carrier, 0 pause output
    0 output buffer failures, 0 output buffers swapped out
```

### **show ip interface**

Verifica informação de camada 3 de uma interface.

```
R1# show ip interface
GigabitEthernet0/0/0 is up, line protocol is up
  Internet address is 209.165.200.225/30
  Broadcast address is 255.255.255.255
  Address determined by setup command
  MTU is 1500 bytes
  Helper address is not set
  Directed broadcast forwarding is disabled
  Multicast reserved groups joined: 224.0.0.5 224.0.0.6
  Outgoing Common access list is not set
  Outgoing access list is not set
  Inbound Common access list is not set
  Inbound access list is not set
  Proxy ARP is enabled
  Local Proxy ARP is disabled
  Security level is default
  Split horizon is enabled
  ICMP redirects are always sent
  ICMP unreachables are always sent
  ICMP mask replies are never sent
  IP fast switching is enabled
  IP Flow switching is disabled
  IP CEF switching is enabled
  IP CEF switching turbo vector
  IP Null turbo vector
  Associated unicast routing topologies:
        Topology "base", operation state is UP
  IP multicast fast switching is enabled
  IP multicast distributed fast switching is disabled
  IP route-cache flags are Fast, CEF
  Router Discovery is disabled
  IP output packet accounting is disabled
  IP access violation accounting is disabled
  TCP/IP header compression is disabled
  RTP/IP header compression is disabled
  Probe proxy name replies are disabled
  Policy routing is disabled
  Network address translation is disabled
  BGP Policy Mapping is disabled
  Input features: MCI Check
  IPv4 WCCP Redirect outbound is disabled
  IPv4 WCCP Redirect inbound is disabled
  IPv4 WCCP Redirect exclude is disabled
 
(Saída omitida)
```

### **show arp**

Verifica a lista de hosts conhecidos nas LANs Ethernet locais.

```
R1# show arp
Protocol   Address          Age (min) Hardware Addr Type Interface
Internet   192.168.10.1      - a0e0.af0d.e141 ARPA GigabitEthernet0/0/1
Internet   192.168.10.10     95 c07b.bcc4.a9c0 ARPA GigabitEthernet0/0/1
Internet   209.165.200.225   - a0e0.af0d.e140 ARPA GigabitEthernet0/0/0
Internet   209.165.200.226   138 a03d.6fe1.9d90 ARPA GigabitEthernet0/0/0
R1#
```

### **show ip route**

Verifica as informações de roteamento da Camada 3.

```
R1# show ip route
Codes: L - local, C - connected, S - static, R - RIP, M - mobile, B - BGP
   D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
   N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
   E1 - OSPF external type 1, E2 - OSPF external type 2
   i - IS-IS, su - IS-IS summary, L1 - IS-IS level-1, L2 - IS-IS level-2
   ia - IS-IS inter area, * - candidate default, U - per-user static route
   o - ODR, P - periodic downloaded static route, H - NHRP, l - LISP
   a - application route
   + - replicated route, % - next hop override, p - overrides from PfR
O gateway de último recurso é 209.165.200.226 para a rede 0.0.0.0
O*E2 0.0.0.0/0 [110/1] via 209.165.200.226, 02:19:50, Gigabitethernet0/0/0
   10.0.0.0/24 is subnetted, 1 subnets
O   10.1.1.0 [110/3] via 209.165.200.226, 02:05:42, GigabitEthernet0/0/0
   192.168.10.0/24 is variably subnetted, 2 subnets, 2 masks
C   192.168.10.0/24 is directly connected, GigabitEthernet0/0/1
L   192.168.10.1/32 is directly connected, GigabitEthernet0/0/1
   209.165.200.0/24 is variably subnetted, 3 subnets, 2 masks
C   209.165.200.224/30 is directly connected, GigabitEthernet0/0/0
L   209.165.200.225/32 is directly connected, GigabitEthernet0/0/0
O   209.165.200.228/30 [110/2] via 209.165.200.226, 02:07:19, GigabitEthernet0/0/0
R1#
```

### **show protocols**

Verifica quais protocolos estão operacionais.

```
R1# show protocols
Valores globais:
  Internet Protocol routing is enabled
GigabitEthernet0/0/0 is up, line protocol is up
  Internet address is 209.165.200.225/30
GigabitEthernet0/0/1 is up, line protocol is up
  Internet address is 192.168.10.1/24
Serial0/1/0 is down, line protocol is down
Serial0/1/1 is down, line protocol is down
GigabitEthernet0 is administratively down, line protocol is down
R1#
```

### **show version**

Verifica a memória, as interfaces e as licenças do dispositivo.

```
R1# show version
Software Cisco IOS XE, Versão 03.16.08.S - Versão de Suporte Extended
Cisco IOS Software, ISR Software (X86_64_LINUX_IOSD-UNIVERSALK9-M), Version 15.5(3)S8, RELEASE SOFTWARE
(fc2)
Technical Support: http://www.cisco.com/techsupport
Copyright (c) 1986-2018 by Cisco Systems, Inc.
Compilado Qua 08/08/18 10:48 por mcpre

(Saída omitida)

ROM: IOS-XE ROMMON
R1 uptime is 2 hours, 25 minutes
Uptime for this control processor is 2 hours, 27 minutes
System returned to ROM by reload
System image file is "bootflash:/isr4300-universalk9.03.16.08.S.155-3.S8-ext.SPA.bin"
Last reload reason: LocalSoft

(Saída omitida)

Informações sobre a licença do pacote de tecnologia:
-----------------------------------------------------------------
Technology     Technology-package     Technology-package
               Current      Type          Next reboot
------------------------------------------------------------------
appxk9         appxk9       RightToUse    appxk9
uck9           None         None          None
securityk9     securityk9   Permanent     securityk9
ipbase         ipbasek9     Permanent     ipbasek9
cisco ISR4321/K9 (1RU) processor with 1647778K/6147K bytes of memory.
Processor board ID FLM2044W0LT
2 Gigabit Ethernet interfaces
2 Serial interfaces
32768K bytes de memória de configuração não volátil.
4194304K bytes de memória física.
3207167K bytes de memória flash no flash de inicialização:.
978928K bytes de flash USB at usb0 :.
Configuration register is 0x2102
R1#
```

## 27.3.3 Packet Tracer - Usando comandos Show do Cisco IOS

Nesta atividade, explore alguns comandos **show** do Cisco IOS.

> [!example]- 🖧 Recursos do Lab
> - 📄 [[anexos/27.3.3.html|Instruções]]
> - 📥 [[anexos/27.3.3.pka|Abrir no Packet Tracer]]

---
# 27.4 Resumo Linha de Comando do Cisco IOS

## 27.4.1 O que aprendi neste módulo?

### Navegar no IOS

O Cisco IOS CLI é um programa baseado em texto que permite inserir e executar comandos do Cisco IOS para configurar, monitorar e manter dispositivos Cisco. É possível usar a CLI da Cisco com tarefas de gerenciamento em banda ou fora da banda.

Os comandos da CLI são usados para modificar a configuração de dispositivo e exibir o status atual dos processos no roteador. Quando o roteador conclui a sequência de inicialização e o prompt `Router>` aparece, a CLI pode ser usada para inserir comandos do Cisco IOS.

Como recurso de segurança, o software Cisco IOS separa o acesso de gerenciamento nestes dois modos de comando:

- **Modo EXEC do usuário** – Este modo é útil para operações básicas. Ele permite um número limitado de comandos básicos de monitoramento, mas não permite a execução de nenhum comando que possa alterar a configuração do dispositivo. O modo EXEC usuário é identificado pelo prompt da CLI que termina com o símbolo `>`.
- **Modo EXEC privilegiado** – Para executar comandos de configuração, um administrador de rede deve acessar o modo EXEC privilegiado. O modo EXEC privilegiado pode ser identificado pelo prompt que termina com o símbolo `#`. Modos de configuração mais altos, como o modo de configuração global, só podem ser acessados do modo EXEC privilegiado. O modo de configuração global é identificado pelo prompt da CLI que termina com `(config)#`.

Os comandos usados para navegar entre os diferentes modos de comando do IOS são:

- `habilitar`
- `desabilitar`
- `configurar terminal`
- `sair`
- `finalizar`
- `Ctrl+Z`
- `line console 0`
- `line vty 0 15`
- `interface vlan 1`

---

### A estrutura de comandos

Cada comando do IOS possui um formato ou sintaxe específica e pode ser executado apenas no modo apropriado. A sintaxe geral para um comando é o comando seguido por quaisquer palavras-chave e argumentos adequados. A palavra-chave é um parâmetro específico definido no sistema operacional. O argumento não é predefinido; é um valor ou variável definida pelo usuário.

- A sintaxe fornece o padrão, ou formato, que deve ser usado ao inserir um comando. O texto em **negrito** indica comandos e palavras-chave que são inseridos conforme mostrado.
- O texto em itálico indica um argumento para o qual o usuário fornece o valor.
- `[x]` colchetes indicam um elemento opcional (palavra-chave ou argumento).
- `{x}` chaves indicam um elemento obrigatório (palavra-chave ou argumento).

---

## 27.4.2 Webster - Questões para Reflexão

Você já assistiu a um filme ou programa de televisão em que uma pessoa inteligente estava digitando em um computador para burlar uma medida de segurança e obter acesso não autorizado a arquivos? Eles não estavam digitando um romance; eles estavam usando a interface de linha de comando. Embora você possa empregar uma interface de usuário para configurar a maioria dos dispositivos de rede, familiarizar-se e usar comandos é muito mais rápido. Se você precisar solucionar problemas de sua rede, precisará usar comandos. Sim, é um pouco como aprender um novo idioma, mas você sabe imediatamente se o fez corretamente ou não. Depois de começar a usar os comandos, você poderá nunca mais voltar à interface do usuário. O que você gostaria de fazer com os comandos?