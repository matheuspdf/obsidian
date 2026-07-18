
# 16.0 Introdução

## 16.0.1 Webster - Por que devo fazer este módulo?

Kishori precisa ter acesso a um arquivo de paciente. Ela já fez isso muitas vezes, mas só agora está se perguntando como esse processo realmente acontece em uma rede. De onde vem este documento eletrônico? Como ela consegue de acessar a intranet do hospital? Como ela consegue acessar a Internet? Tudo isso é possível devido aos serviços da camada de aplicação.

Kishori tem mais a aprender antes de se candidatar para a posição mencionada por Rina. Existem muitos serviços que funcionam na camada de aplicação, incluindo alguns com os quais você está familiarizado, como FTP, DHCP e DNS. Quando você quiser recuperar algo que ainda não está localizado no seu computador, você será o cliente a solicitar que o servidor apropriado envie esse item. E, é claro, você já sabe que haverá protocolos envolvidos. Continue lendo...

## 16.0.2 O Que Vou Aprender Neste Módulo?

**Título do Módulo:** Serviços da Camada de Aplicação

**Objetivo do Módulo:** Explicar a função dos serviços comuns da camada de aplicação.

| Título do Tópico                                   | Objetivo do Tópico                                |
| -------------------------------------------------- | ------------------------------------------------- |
| A relação Cliente — Servidor                       | Explicar a interação entre clientes e servidores. |
| Network Application Services                       | Descrever as aplicações comuns de rede.           |
| Domain Name System (Sistema de Nomes de Domínios). | Descrever o DNS.                                  |
| Clientes e servidores Web                          | Descrever HTTP e HTML.                            |
| Clientes e servidores FTP                          | Descrever o FTP.                                  |
| Terminais virtuais                                 | Descrever o Telnet e o SSH.                       |
| E-mails e mensagens                                | Descrever os protocolos de e-mail.                |

# 16.1 A relação Cliente - Servidor

## 16.1.1 Interação Cliente e Servidor

Todos os dias usamos os serviços disponíveis nas redes e na Internet para nos comunicar com outras pessoas e executar tarefas de rotina. Raramente pensamos nos servidores, clientes e dispositivos de rede que são necessários para receber um e-mail, atualizar o status em mídias sociais ou comprar as melhores ofertas em uma loja on-line. A maioria dos aplicativos de Internet mais usados depende de interações complicadas entre diferentes clientes e servidores.

O termo servidor refere-se a um host que executa um aplicativo que disponibiliza informações ou serviços para outros hosts conectados à rede. Um exemplo bem conhecido de aplicativo é um servidor Web. Há milhões de servidores conectados à Internet oferecendo serviços como sites, e-mails, transações financeiras, downloads de música, etc. Um fator que é essencial para possibilitar o funcionamento dessas interações complexas é o uso conjunto de padrões e protocolos.

![[Pasted image 20260610205038.png]]

Um exemplo de software cliente é um navegador, como Chrome ou FireFox. Um único computador pode também executar vários tipos de software cliente. Por exemplo, um usuário pode verificar o e-mail e visualizar uma página Web enquanto troca mensagens instantâneas e ouve um fluxo de áudio. A tabela lista três tipos comuns de software de servidor.

|Tipo|Descrição|
|---|---|
|E-mail|O servidor de executa o software do servidor de e-mail. Clientes usam um software de e-mail, como o Microsoft Outlook, para acessar e-mails no servidor.|
|Web|O servidor web executa o software do servidor web. Os clientes usam software navegador, como Chrome ou Firefox, para acessar páginas web do servidor.|
|Arquivo|O servidor de arquivos armazena arquivos corporativos e de usuário em um local central. Os dispositivos clientes acessam esses arquivos com softwares clientes, como o Windows Explorer.|


## 16.1.2 Vídeo - Servidor Web e interações do cliente IP

![[16.1.2.mp4#subtitle=anexos/16.1.2.vtt]]
**Selecione o botão Reproduzir para assistir o vídeo.**

Nesta lição, vamos discutir como um cliente web e um servidor web usam protocolos IP para interagir.

Começaremos com o lado do cliente web. O cliente web deseja recuperar uma página web do servidor web. O servidor web está localizado em um local diferente e foi configurado de maneira padrão, estando escutando as solicitações web na porta 80 TCP, neste endereço IP e neste nome de domínio — ou URL, neste caso.

O cliente vai colocar a URL www.learnip.com na linha URL. Como aprendemos até agora, a URL deve ser traduzida para um endereço IP antes que a transmissão possa ser enviada, porque a internet — ou qualquer outra rede — não processa os nomes de domínio, elas processam os endereços IP quando estão encaminhando e transmitindo pacotes.

Então, quando usa a URL www.learnip.com, a primeira coisa que tem que acontecer é que uma pesquisa DNS deve ocorrer. Uma pesquisa DNS está enviando uma solicitação ao servidor DNS para recuperar o endereço IP que foi associado a www.learnip.com. Neste caso, será devolvido o endereço IP 172.16.10.50. Agora, o endereço IP é para onde o pacote será endereçado, que vai conter em sua parte de dados a solicitação para a página web específica. Então é feita a pesquisa de DNS e, uma vez concluída, a mensagem vai ser enviada para o servidor web.

A segunda coisa que tem que acontecer é que deve haver uma conexão TCP criada entre o servidor web e o cliente web. A conexão TCP vai usar o endereço IP do cliente web e o número da porta TCP atribuído ao cliente web. Neste caso, o cliente web terá o endereço IP 192.168.10.15 e será atribuída uma porta aleatória acima de 1024, que será 5507.

Então a conexão TCP se estabelecerá entre a fonte — 192.168.10.15, porta 5507 — e o destino — 172.16.10.50, porta 80. Nas comunicações, isso é chamado de soquete. Basicamente, é o identificador de todos os componentes que pertencem a esta conversa — a conversa entre o cliente web e o servidor web.

Quando o servidor web recebe este pacote que vem chegando, o que ele vai fazer é colocá-lo no buffer atribuído à porta 80, para que o serviço web veja que há uma solicitação deste dispositivo e então formule a resposta com as informações invertidas, onde a fonte da resposta é o 172.16.10.50 porta 80, e o destino é o 192.168.10.15 porta 5507.

Todos os pacotes incluídos nesta conversa — todas as solicitações da web e todas as respostas da web — vão ter essa mesma informação, para que esta conversa possa ser identificada. Mesmo viajando pela internet, vários elementos como roteadores, firewalls e outros dispositivos poderão ler que esses pacotes fazem parte da mesma conversa.

## 16.1.3 URI, URN e URL

### Parts of a URI

Recursos e serviços da Web, como APIs RESTful, são identificados usando uma URI (Identificador de recurso uniforme) Um URI é uma sequência de caracteres que identifica um recurso de rede específico. Conforme mostrado na figura, uma URI tem duas especializações:

- **Nome do Recurso Uniforme (URN)** -identifica apenas o espaço para nome do recurso (página da web, documento, imagem etc.) sem referência ao protocolo.
- **URL (Localizador de Recurso Uniforme)** - define o local da rede de um recurso específico na rede. URLs de HTTP ou HTTPS são normalmente usados por navegadores web. Outros protocolos como FTP, SFTP, SSH e outros podem ser usados por meio de uma URL. Uma URL usando SFTP pode estar no formato: sftp://sftp.example.com.

Estas são as partes de uma URI, como mostrado na figura:

- **Protocolo/esquema** –HTTPS ou outros protocolos como FTP, SFTP, mailto e NNTP
- **Nome do host** - www.example.com
- **Caminho e nome do arquivo** - /author/book.html
- **Fragmento** - # page155

#### Partes de uma URI

![[Pasted image 20260610205215.png]]


## 16.1.4 Vídeo - Tráfego da Web no Packet Tracer

![[16.1.4.mp4#subtitle=anexos/16.1.4.vtt]]
Neste vídeo, vamos usar o Packet Tracer para ilustrar como uma página web é obtida de um servidor web.

Neste caso, temos um PC que está conectado através de uma nuvem de internet simulada para um servidor web. Esse servidor web está em www.learnip.com, também no endereço IP 172.33.100.50.

Vamos ao PC e solicitar uma página web. Para solicitar uma página web, temos que usar um cliente que é apropriado para um servidor web. Começamos escolhendo o cliente web — o cliente apropriado para visualizar uma página web é o navegador web. Vamos abrir o navegador web, iniciar o utilitário de captura e capturar o tráfego do PC0 para o servidor web.

Colocamos a URL learnip.com no navegador e solicitamos o pacote. Você pode ver que os pacotes HTTP estão sendo gerados e estão viajando pela internet simulada para o servidor web. O servidor web irá então responder e entregar a página web de volta ao PC.

Neste ponto vamos parar a captura e dar uma olhada em alguns desses pacotes. Se examinarmos as informações do pacote clicando na caixa ao lado do pacote que queremos investigar, podemos ver que é um pacote HTTP que está gerando uma solicitação web. Ele está usando o TCP como seu protocolo de transporte e está indo para o endereço IP de destino do servidor web. Você pode ver neste pacote que o endereço IP de origem é o endereço IP de PC0. Você também pode ver que, quando for comunicado, é inicialmente formatado como um quadro Ethernet e passa pela conexão Ethernet entre o PC0 e seu primeiro hub para acessar a internet.

Quando o servidor web responde, o servidor recebe a solicitação que recebeu do PC0 e em seguida envia de volta a resposta. Como você pode ver, a resposta é destinada ao PC0 como destino. Este processo continuará à medida que todas as informações relacionadas à página web são transmitidas.






## 16.1.5 Packet Tracer - A interação do cliente

Nesta atividade, você observará a interação de cliente entre o servidor e o PC.

> [!example]- 🖧 Recursos do Lab
> - 📄 [[anexos/16.1.5.html|Instruções]]
> - 📥 [[anexos/16.1.5.pka|Abrir no Packet Tracer]]

---
# 16.2 Serviços de Aplicação de Rede

Quais são os serviços de internet mais comuns que você usa regularmente? Para a maioria das pessoas, a lista inclui serviços como pesquisas na Internet, sites de mídia social, transmissão de áudio e vídeo, sites de lojas on-line, e-mail e mensagens. Cada um desses serviços depende de protocolos, do conjunto de protocolos TCP/IP, para comunicar de forma confiável as informações entre os clientes e os servidores.

Alguns dos servidores mais comuns que fornecem esses serviços são mostrados na figura. Uma breve descrição de cada serviço é mostrada na tabela.

![[Pasted image 20260610213229.png]]

|Protocolo|Descrição|
|---|---|
|**Domain Name System (DNS)**|Resolve nomes de internet para endereços IP.|
|**Secure Shell (Shell seguro) — SSH**|Usado para fornecer acesso remoto a servidores e dispositivos de rede.|
|**Protocolo SMTP**|Envia mensagens de e-mail e anexos de clientes para servidores e de servidores para outros servidores de e-mail.|
|**Protocolo POP**|Usado por clientes de email para recuperar emails e anexos de um servidor remoto.|
|**Protocolo IMAP**|Usado por clientes de email para recuperar emails e anexos de um servidor remoto.|
|**Protocolo de Configuração Dinâmica de Host (DHCP)**|Usado para configurar automaticamente dispositivos com endereçamento IP e outras informações necessárias para permitir que eles se comuniquem pela Internet.|
|**Protocolo HTTP**|Usado por navegadores Web para solicitar páginas Web e por servidores Web para transferir os arquivos que compõem as páginas da World Wide Web.|
|**File Transfer Protocol (FTP)**|Usado para transferência interativa de arquivos entre sistemas.|

## 16.2.2 Verifique sua compreensão - Aplicações de Redes Comuns

**Verifique sua compreensão sobre serviços de aplicação de redes escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Qual protocolo de aplicação é usado para configurar automaticamente as informações de endereçamento IP?

- [ ] FTP
- [ ] IMAP
- [ ] DNS
- [x] DHCP

✅ RESPOSTA CORRETA: DHCP

> O Dynamic Host Configuration Protocol (DHCP) é usado para configurar automaticamente os dispositivos com endereçamento IP e outras informações necessárias.

---

### Pergunta 2

Quais protocolos de aplicação são usados pelos clientes para recuperar mensagens de e-mail? (Escolha duas.)

- [ ] SMTP
- [ ] FTP
- [x] POP
- [ ] HTTP
- [x] IMAP
- [ ] DNS

✅ RESPOSTA CORRETA: POP, IMAP

> O Post Office Protocol (POP) e o Internet Message Access Protocol (IMAP) são usados por clientes de e-mail para recuperar mensagens de e-mail.

---

### Pergunta 3

Qual protocolo de aplicação é usado para resolver endereços Web para um endereço IP?

- [ ] SSH
- [ ] DHCP
- [ ] HTTP
- [x] DNS

✅ RESPOSTA CORRETA: DNS

> O Domain Name System (DNS) resolve nomes da Internet para endereços IP.



# 16.3 Domain Name System (Sistema de Nomes de Domínios).

## 16.3.1 Vídeo - Servidores DNS
![[16.3.1.mp4#subtitle=anexos/16.3.1.vtt]]
**Selecione o botão Reproduzir para assistir o vídeo.**

Neste vídeo, vamos apresentar o servidor DNS. DNS significa servidor de Domain Name System. O servidor DNS é usado para associar um nome de domínio, ou um nome de host, a um endereço IP.

Aqui temos um usuário que acessa o site www.cisco.com. No entanto, a rede — a internet — não entende nomes de domínio como cisco.com. Ela só entende endereços IP. Portanto, o sistema precisa associar um endereço IP a este nome de domínio e, neste caso, ele irá perguntar a um servidor DNS.

O sistema vai entrar em contato com o servidor DNS e pedir o endereço IP associado a www.cisco.com. A consulta — a pergunta — sobre este nome de domínio vai para o servidor DNS. O servidor DNS procura www.cisco.com, encontra o endereço IP e, em seguida, retorna esse endereço IP para o host.

O host agora pode usar este endereço IP para entrar em contato com o servidor web www.cisco.com e, neste caso, baixar as informações apropriadas para exibir a página web.


## 16.3.2 Uma observação sobre as atividades do verificador de sintaxe

Quando estiver aprendendo a modificar as configurações do dispositivo, convém começar em um ambiente seguro e que não seja de produção antes de experimentá-lo em equipamentos reais. O NetACAD oferece diferentes ferramentas de simulação para ajudar a desenvolver suas habilidades de configuração e solução de problemas. Como estas são ferramentas de simulação, elas geralmente não têm toda a funcionalidade de equipamentos reais. Uma dessas ferramentas é o Verificador de Sintaxe. Em cada Verificador de Sintaxe, você recebe um conjunto de instruções para inserir um conjunto específico de comandos. Você não pode progredir no Verificador de Sintaxe a menos que o comando exato e completo seja inserido conforme especificado. Ferramentas de simulação mais avançadas, como o Packet Tracer, permitem que você insira comandos abreviados, assim como faria em equipamentos reais.

## 16.3.3 Verificador de Sintaxe - O Comando nslookup

Ao configurar manualmente um dispositivo para conectividade de rede, lembre-se de incluir também um endereço de servidor DNS. Para redes domésticas, essa configuração é normalmente tratada pelo DHCP em execução no roteador doméstico. Seu ISP fornece o endereço do servidor DNS para o roteador doméstico e, em seguida, ele usa DHCP para enviar a configuração para todos os dispositivos conectados à rede. Quando você digita o nome de um site, [como www.cisco.com](http://www.cisco.com/), o cliente DNS em execução no dispositivo primeiro pede ao servidor DNS o endereço IP, como 172 **.230.155.162**, antes de enviar sua solicitação HTTP.

Você pode usar o comando **nslookup** para descobrir os endereços IP de qualquer nome de domínio. Nesta atividade do Verificador de Sintaxe, pratique a inserção do comando nslookup no Windows e no Linux.

```
No prompt de comando do Windows, digite o **nslookup** comando para iniciar uma consulta manual dos servidores de nomes.

C:\>nslookup

Default Server: Unknown
Address: 10.10.10.1

As saídas listam o nome e o endereço IP do servidor DNS configurado no cliente. Observe que o endereço do servidor DNS pode ser configurado manualmente ou aprendido dinamicamente através do DHCP. Você está agora no modo **nslookup**. Digite o nome de domínio www.cisco.com.

>www.cisco.com

Server:  UnKnown
Address:  10.10.10.1
Non-authoritative answer:
Name:    e2867.dsca.akamaiedge.net
Addresses:  2600:1404:a:395::b33
          2600:1404:a:38e::b33
          172.230.155.162
Aliases:  www.cisco.com
          www.cisco.com.akadns.net
          wwwds.cisco.com.edgekey.net
          wwwds.cisco.com.edgekey.net.globalredir.akadns.net

As saídas listam os endereços IP relacionados com ‘w​ww.cisco.com’ que o servidor ‘e2867’ tem em seu banco de dados atualmente. Observe que endereços IPv6 também estão listados. Além disso, vários aliases são exibidos e que também serão resolvidos para ‘w​ww.cisco.com’.

Digite o comando **exit**para sair do modo nslookup e retornar à linha de comando do Windows.

>exit

Você pode consultar diretamente os servidores DNS simplesmente adicionando o nome de domínio ao comando **nslookup** .

Entrar **nslookup w​ww.google.com**.

C:\>nslookup www.google.com

Server:  UnKnown
Address:  10.10.10.1
Non-authoritative answer:
Name:    www.google.com
Addresses:  2607:f8b0:4000:80f::2004
          172.217.12.36
 
 
=========================================

Você agora está trabalhando no prompt de comando do Linux. O comando nslookup é o mesmo.

* Enter the **nslookup** comando para iniciar uma consulta manual dos servidores de nomes. * Enter **www.cisco[]().com** at the \> prompt. * Enter the **exit** para sair do modo nslookup e retornar à linha de comandos do Linux.

user@cisconetacad$nslookup

Server: 127.0.1.1
Address: 127.0.1.1#53

>www.cisco.com

Non-authoritative answer:
www.cisco.com canonical name = www.cisco.com.akadns.net.
www.cisco.com.akadns.net canonical name = wwwds.cisco.com.edgekey.net.
wwwds.cisco.com.edgekey.net canonical name = wwwds.cisco.com.edgekey.net.globalredir.akadns.net.
wwwds.cisco.com.edgekey.net.globalredir.akadns.net canonical name = e144.dscb.akamaiedge.net.
Name: e144.dscb.akamaiedge.net
Address: 23.60.112.170

>exit

Como no Windows, você pode consultar diretamente os servidores DNS simplesmente adicionando o nome de domínio ao comando **nslookup** . Entrar **nslookup w​ww.google.com**.

user@cisconetacad$nslookup www.google.com

Server:		127.0.0.53
Address:	127.0.0.53#53

Non-authoritative answer:
Name:	www.google.com
Address: 172.217.6.164
Name:	www.google.com
Address: 2607:f8b0:4000:812::2004

Você usou corretamente o comando nslookup para verificar o status dos nomes de domínio.
```

# 16.4 Clientes e servidores Web

## 16.4.1 Vídeo - HTTP e HTML
![[16.4.1.mp4#subtitle=anexos/16.4.1.vtt]]
**Selecione o botão Reproduzir para assistir o vídeo.**

Neste vídeo, vamos dar uma olhada em HTTP e HTML.

HTTP significa Hypertext Transfer Protocol. Estas são as regras que regem a forma como as informações são transmitidas entre o cliente — o dispositivo solicitando a página da web — e o servidor web que envia a página web de volta para o cliente.

HTML significa Hypertext Markup Language. Esta é a codificação, a informação, que na verdade é usada para exibir a própria página web.

Começamos com o cliente solicitando o site www.cisco.com. Mas como dissemos anteriormente, a rede — a internet — não entende nomes, não entende nomes de domínio. Ela precisa do endereço IP associado com www.cisco.com. Assim, o usuário, o sistema, vai entrar em contato com o servidor DNS. O servidor DNS vai associar o nome de domínio www.cisco.com com um endereço IP e devolverá esse endereço IP ao usuário, ao sistema.

Agora o sistema poderá entrar em contato com o servidor web www.cisco.com usando este endereço IP. Esta solicitação usa HTTP para solicitar a página web. Ele é enviado para o servidor web www.cisco.com, que usa HTTP para retornar as informações — o código HTML — de volta ao usuário. Agora o usuário poderá exibir a página web www.cisco.com em seu navegador.

Aqui podemos ver a página da web www.cisco.com. Para dar uma olhada no código HTML, vamos ao menu Desenvolvedor e clicamos em fonte da página. Este page source é o código HTML atual. Este código HTML foi baixado do servidor web www.cisco.com ao sistema do cliente e exibido em seu navegador. O navegador então pega esse código, exibe, e assim vemos a página web www.cisco.com.

## 16.4.2 HTTP e HTML

Quando um cliente Web recebe o endereço IP de um servidor Web, o navegador do cliente usa esse endereço IP e a porta 80 para solicitar serviços da Web. Essa solicitação é enviada para o servidor com o Hypertext Transfer Protocol (HTTP).

Quando um cliente Web recebe o endereço IP de um servidor Web, o navegador do cliente usa esse endereço IP e a porta 80 para solicitar serviços da Web. O conteúdo de informações de uma página Web é codificado por meio de linguagens de marcação especializadas. A codificação HyperText Markup Language (HTML) informa ao navegador o modo de formatação da página Web, além de gráficos e fontes a serem usados. HTML é a linguagem mais usada.

Clique em Play na figura para ver uma solicitação de cliente para uma página Web.
![[brave_LbHlD6koxy.mp4]]

O protocolo HTTP não é um protocolo seguro; as informações podem ser facilmente interceptadas por outros usuários à medida que os dados são enviados pela rede. Para oferecer segurança aos dados, o HTTP pode ser usado com protocolos de transporte seguros. As solicitações de HTTP seguro são enviadas para a porta 443. Essas solicitações usam **https** no endereço do site no navegador, em vez de **http.**

Existem muitos servidores web e clientes web diferentes disponíveis. Os padrões de HTML e do protocolo HTTP fazem com que esses servidores e clientes de diversos fabricantes trabalhem em conjunto sem dificuldades.

## 16.4.3 Packet Tracer - Observar solicitações Web

Nesta atividade, você observará as solicitações Web que ocorrem quando um navegador solicita páginas Web de um servidor.

> [!example]- 🖧 Recursos do Lab
> - 📄 [[anexos/16.4.3.html|Instruções]]
> - 📥 [[anexos/16.4.3.pka|Abrir no Packet Tracer]]

---
# 16.5 Clientes e servidores FTP

## 16.5.1 Protocolo FTP

Além de serviços da Web, outro serviço comum utilizado na Internet é o que permite que os usuários transfiram arquivos.

O File Transfer Protocol (FTP) disponibiliza um método fácil para transferir arquivos de um computador para outro. Um host com software de cliente FTP pode acessar um servidor FTP para executar várias funções de gerenciamento de arquivos, como uploads e downloads.

O servidor FTP permite que o cliente troque arquivos entre dispositivos. Ele também possibilita que os clientes gerenciem arquivos remotamente enviando comandos de gerenciamento de arquivos, como delete ou rename. Para conseguir isso, o serviço FTP usa duas portas diferentes para a comunicação entre cliente e servidor.

O exemplo na figura ilustra como funciona o FTP. Para iniciar uma sessão de FTP, as solicitações de conexão de controle são enviadas para o servidor usando a porta TCP de destino 21. Quando a sessão é aberta, o servidor usa a porta TCP 20 para transferir os arquivos de dados.

O software de cliente FTP vem incorporado em sistemas operacionais de computador e na maioria dos navegadores Web. Os clientes FTP independentes oferecem muitas opções em uma interface fácil de usar, baseada em GUI.

![[Pasted image 20260611064509.png]]
## 16.5.2 Vídeo - Software Cliente FTP

**Selecione o botão Reproduzir para assistir o vídeo.**
![[16.5.2.mp4#subtitle=anexos/16.5.2.vtt]]
Aqui vamos demonstrar como usar um software cliente FTP. FTP significa File Transfer Protocol. Ele nos permite copiar arquivos facilmente de um dispositivo para outro — de um dispositivo cliente para um servidor ou do servidor de volta para o cliente. Isso é usado muitas vezes para fazer upload das informações da sua página web para um servidor web.

Aqui no FileZilla, onde diz Host, vou digitar ftp.cdc.gov. Este é um servidor FTP disponível que qualquer um pode usar. O nome de usuário será anonymous e não há senha associada a este site. Normalmente, você terá um nome de usuário e senha associados ao servidor web para que você possa enviar e baixar as informações com segurança. Clicando em Quick Connect, agora estamos conectados a este servidor FTP.

À esquerda está minha área de trabalho, ou os arquivos do meu computador. À direita está o site remoto. Vou mostrar como é fácil transferir um arquivo, neste caso, do site remoto — o servidor ftp.cdc.gov — para meu host local. Descendo aqui, temos uma mensagem de boas-vindas, e vou arrastar isso para a minha área de trabalho — e isso é tudo o que tenho que fazer. Ele copiou do servidor remoto para minha área de trabalho local.

Podemos realmente ver essa mensagem de boas-vindas aqui. Aí está o arquivo que acabamos de baixar de ftp.cdc.gov.

## 16.5.3 Packet Tracer - Usando serviços FTP

Nesta atividade, você vai colocar um arquivo em um servidor FTP e obter um arquivo de um servidor FTP

Packet Tracer - Usando serviços FTP

## Tabela de Endereçamento

|Dispositivo|Interface|Endereço IP|Máscara de Sub-Rede|
|---|---|---|---|
|Servidor FTP (ftp.pka)|NIC|209.165.200.226|255.255.255.224|

### Objetivos

- Carregamento (upload) de um arquivo para um servidor FTP.
- Baixar (download de) um arquivo de um servidor FTP.

### Histórico/Cenário

O File Transfer Protocol (FTP) é um aplicativo comumente usado para transferir arquivos entre clientes e servidores na rede. O servidor está configurado para executar o serviço no qual os clientes se conectam, fazem login e transferem arquivos. O FTP usa a porta 21 como a porta de comando do servidor para criar a conexão. O FTP usa a porta 20 para transferência de dados.

Nesta atividade, você vai carregar um arquivo para um servidor FTP. Você também vai baixar um arquivo de um servidor FTP.

### Instruções

### Parte 1: Carregamento (upload) de um arquivo para um servidor FTP.

Nesta parte, você localizará o arquivo **sampleFile.txt** e o carregará em um servidor FTP.

#### Etapa 1: Localize o arquivo.

a. Clique em **PC-A**

b. Clique em **Desktop**.

c. Clique em **Command Prompt**.

d. No prompt, clique em **?** para listar os comandos disponíveis.

e. Insira dir para ver os arquivos no PC. Observe que há um arquivo **sampleFile.txt** no diretório C:.

```
C:> dir
Volume in drive C has no label.
Volume Serial Number is 5E12-4AF3
Directory of C:
12/31/1969 17:00 PM 26 sampleFile.txt
26 bytes 1 File(s)
```

#### Etapa 2: Conecte o servidor FTP.

a. Efetue FTP para o servidor FTP em **209.165.200.226** ou **ftp.pka**.

```
C:> ftp 209.165.200.226
Trying to connect...209.165.200.226
Connected to 209.165.200.226
```

b. Entre com username **student** e password **class** para obter accesso.

```
220- Welcome to PT Ftp server
Username:student
331- Username ok, need password
Password:
230- Logged in
(passive mode On)
```

#### Etapa 3: Carregamento (upload) de um arquivo para um servidor FTP.

a. Digite **?** para ver os comandos disponíveis no cliente ftp.

```
ftp> ?
        ?
        cd
        delete
        dir
        get
        help
        passive
        put
        pwd
        quit
        rename
ftp>
```

b. Insira **dir** para ver os arquivos disponíveis no servidor.

```
ftp> dir
Listing /ftp directory from 192.168.1.3:
0 : asa842-k8.bin 5571584
1 : asa923-k8.bin 30468096
2 : c1841-advipservicesk9-mz.124-15.T1.bin 33591768
3 : c1841-ipbase-mz.123-14.T7.bin 13832032
<output omitted>
```

c. Digite **put sampleFile.txt** para enviar o arquivo para o servidor.

```
ftp> put sampleFile.txt
Writing file sampleFile.txt to 209.165.200.226:
File transfer in progress...
[Transfer complete – 26 bytes]
26 bytes copied in 0.08 secs (325 bytes/sec)
ftp>
```

d. Use o comando **dir** novamente para listar o conteúdo do servidor FTP e verificar se o arquivo foi carregado para o servidor FTP.

---

### Parte 2: Baixar (download de) um arquivo de um servidor FTP.

Você também pode baixar um arquivo de um servidor FTP. Nesta parte, você vai renomear o arquivo **sampleFile.txt** e baixá-lo do servidor FTP.

#### Etapa 1: Renomeie o arquivo no servidor FTP.

a. No prompt **ftp>**, renomeie o arquivo **sampleFile.txt** para **sampleFile_FTP.txt**.

```
ftp> rename sampleFile.txt sampleFile_FTP.txt
Renaming sampleFile.txt
ftp>
[OK Renamed file successfully from sampleFile.txt to sampleFile_FTP.txt]
ftp>
```

b. No prompt **ftp>**, digite **dir** para verificar se o arquivo foi renomeado.

#### Etapa 2: Baixe o arquivo do servidor FTP.

a. Insira o comando **get sampleFile_FTP.txt** para recuperar o arquivo do servidor.

```
ftp> get sampleFile_FTP.txt
Reading file sampleFile_FTP.txt from 209.165.200.226:
File transfer in progress...
[Transfer complete – 26 bytes]
26 bytes copied in 0.013 secs (2000 bytes/sec)
ftp>
```

b. Digite **quit** para sair do cliente FTP quando terminar.

c. Exiba o conteúdo do diretório no PC novamente para ver o arquivo de imagem do servidor FTP.

#### Etapa 3: Excluindo o arquivo do servidor FTP.

a. Faça login no servidor FTP novamente para excluir o arquivo **sampleFile_FTP.txt**.

b. Insira o comando para excluir o arquivo **sampleFile_FTP.txt** do servidor.

Qual comando você usou para remover o arquivo do servidor FTP?

```
ftp> delete sampleFile_FTP.txt
```

c. Digite **quit** para sair do cliente FTP quando terminar.


# 16.6 Terminais virtuais

## 16.6.1 Vídeo - Acesso Remoto com Telnet ou SSH
![[16.6.1.mp4#subtitle=anexos/16.6.1.vtt]]
Neste vídeo vamos demonstrar como acessar um servidor remotamente usando Telnet ou SSH.

Aqui trouxe um software conhecido como Tera Term, que me permite usar Telnet ou SSH. Telnet e SSH me permitem acessar remotamente um servidor — outro dispositivo — como se eu estivesse realmente sentado em frente àquele dispositivo.

Vou usar SSH, que é uma versão mais segura do Telnet. No nome de host, tenho oslab.cis.cabrillo.edu. Isso pode ser um nome de host ou um endereço IP. Este é o nome de um servidor que tenho na escola, Cabrillo College, onde leciono.

Neste ponto, seleciono o SSH e clico em OK. Ele me pede um nome de usuário e senha. Coloco meu nome de usuário, rick, e coloco a senha. Clico em OK.

Como você pode ver, me conectei remotamente ao servidor Opus, que é um dos servidores que temos na minha escola, Cabrillo College. É como se eu estivesse sentado naquele computador, digitando os comandos. Mas, em vez disso, estou a quilômetros de distância, acessando-o remotamente.


## 16.6.2 Telnet

Muito antes dos computadores desktop com interfaces gráficas sofisticadas, as pessoas utilizavam sistemas com base em texto que frequentemente eram apenas terminas de exibição fisicamente acoplados a um computador central. Depois que as redes se tornaram disponíveis, as pessoas precisavam de uma maneira para acessar remotamente os sistemas de computador da mesma maneira que faziam com os terminais conectados diretamente.

O Telnet foi desenvolvido para atender a essa necessidade. O Telnet data do início da década de 70 e está entre um dos protocolos e serviços da camada de Aplicação mais antigos da suite TCP/IP. O Telnet fornece um método padrão de emulação de dispositivos terminais baseados em texto na rede de dados. O protocolo e o software cliente que implementa o protocolo são comumente chamados de Telnet. Os servidores Telnet escutam solicitações de clientes na porta TCP 23.

Apropriadamente, uma conexão usando Telnet é chamada de sessão ou conexão de terminal virtual (vty) Em vez de usar um dispositivo físico para se conectar ao servidor, o Telnet utiliza software para criar um dispositivo virtual que fornece os mesmos recursos de uma sessão de terminal com acesso à interface de linha de comando (CLI) do servidor.

Na figura, o cliente se conectou remotamente ao servidor via Telnet. Agora o cliente pode executar comandos como se estivesse conectado localmente ao servidor.

**Observação:** o Telnet não é considerado um protocolo seguro. O SSH deve ser usado na maioria dos ambientes, no lugar do Telnet. O Telnet é utilizado em vários exemplos neste curso pela simplicidade de sua configuração.

![[Pasted image 20260611065326.png]]

## 16.6.3 Problemas de segurança com Telnet

Quando uma conexão Telnet é estabelecida, os usuários podem executar qualquer função autorizada no servidor, como se estivessem usando uma sessão de linha de comando no próprio servidor. Se autorizados, podem iniciar e parar processos, configurar o dispositivo e até mesmo desligar o sistema.

Embora o protocolo Telnet possa exigir o login de um usuário, ele não suporta o transporte de dados criptografados. Todos os dados trocados durante as sessões Telnet são transportados como texto simples pela rede. Isso significa que os dados podem ser facilmente interceptados e compreendidos.

O protocolo Secure Shell (SSH) oferece um método alternativo e seguro para acesso ao servidor. O SSH fornece a estrutura para proteger login remoto e outros serviços de rede segura. Ele também fornece autenticação mais forte do que o Telnet e suporta o transporte de dados de sessão usando criptografia. Como melhor prática, os profissionais de rede sempre devem utilizar o SSH em vez do Telnet, quando possível.

A figura ilustra como o SSH é mais seguro que o Telnet. Observe como são claramente legíveis os dados capturados pelo hacker quando o Telnet é usado, enquanto que os dados, capturados quando o SSH está em uso, estão criptografados, tornando assim a comunicação mais segura.

![[Pasted image 20260611065339.png]]

## 16.6.4 Packet Tracer - Uso do Telnet e SSH

Nesta atividade, você estabelecerá uma sessão remota para um roteador usando Telnet e SSH.

Packet Tracer- Uso do Telnet e SSH

## Tabela de Endereçamento

|Dispositivo|Interface|Endereço IP|Máscara de Sub-Rede|
|---|---|---|---|
|HQ|G0/0/1|64.100.1.1|255.255.255.0|
|PC0|NIC|DHCP||
|PC1|NIC|DHCP||

## Objetivos

Nesta atividade, você estabelecerá uma conexão remota com um roteador usando Telnet e SSH.

=  Verifique a conectividade

=  Acessar um dispositivo remoto

## Instruções

## Parte 1: Verificar a conectividade

Nesta parte, você verificará se o PC tem endereçamento IP e pode pingar o roteador remoto.

### Etapa 1: Verifique o endereço IP em um PC.

a.  Em um PC, clique em **Desktop**. Clique em **Command Prompt**.

b.  No prompt, verifique se o PC possui um endereço IP do DHCP.

#### Pergunta:

Qual comando você usou para verificar se o endereço IP foi obtido por DHCP?

Área de Resposta

ftp> ipconfig

Ocultar resposta

### Etapa 2: Verificar a conectividade com HQ.

Verifique se você consegue pingar o roteador HQ usando o endereço IP listado na tabela de endereçamento.

## Parte 2: Acessar um dispositivo remoto

Nesta parte, você tentará estabelecer uma conexão remota usando Telnet e SSH.

### Etapa 1: Telnet para HQ.

No prompt, digite o comando **telnet 64.100.1.1**.

#### Pergunta:

Deu certo? Qual foi a saída?

Área de Resposta

Não.  
C:\> telnet 64.100.1.1  
Trying 64.100.1.1 ...Open  
  
[Connection to 64.100.1.1 closed by foreign host]

Ocultar resposta

### Etapa 2: SSH para HQ.

O roteador está configurado corretamente para não permitir acesso não seguro ao Telnet. Você tem que usar o SSH.

No prompt, digite o comando **ssh -l admin 64.100.1.1**. Entre com a senha **class** quando solicitado.

C:> **ssh -l admin 64.100.1.1**

Password:

#### Pergunta:

Qual o prompt após acessar o roteador com sucesso via SSH?

Área de Resposta

HQ#

---

# 16.7 E-mail e mensagens

## 16.7.1 Clientes e Servidores de e-mail

O e-mail é um dos mais populares aplicativos cliente/servidor na Internet. Os servidores de e-mail executam um software de servidor que permite interagir com clientes e outros servidores de e-mail pela rede.

Cada servidor de e-mail recebe e armazena e-mails de usuários que têm caixas de correio configuradas no servidor de e-mail. Cada usuário com uma caixa de correio deve usar um cliente de e-mail para acessar o servidor de e-mail e ler essas mensagens. Muitos sistemas de mensagens da Internet usam um cliente baseado na Web para acessar e-mails. Alguns exemplos desse tipo de cliente são Microsoft 365, Yahoo e Gmail.

As caixas de correio são identificadas pelo formato: **usuário@empresa.domínio**

Vários protocolos de aplicativos usados no processamento de e-mail incluem SMTP, POP3 e IMAP4.

![[Pasted image 20260611065605.png]]

## 16.7.2 Protocolos de e-mail

**Protocolo SMTP**

O SMTP é usado por um cliente de e-mail para enviar mensagens para o servidor de e-mail local. O servidor local então decide se a mensagem é destinada a uma caixa de correio local ou se é endereçada a uma caixa de correio em outro servidor.

Se o servidor tiver que enviar a mensagem para um servidor diferente, o SMTP também será usado entre esses dois servidores. As solicitações SMTP são enviadas para a porta 25.

Clique em Play na figura para ver como o SMTP é usado para enviar e-mail.

![[brave_0jvYQjSSuJ.mp4]]

**Protocolo POP (POP3)**

Um servidor compatível com clientes POP recebe e armazena as mensagens endereçadas a seus usuários. Quando o cliente se conecta ao servidor de e-mail, as mensagens são baixadas no cliente. Por padrão, as mensagens não são mantidas no servidor após serem acessadas pelo cliente. Os clientes contatam os servidores POP3 na porta 110.

**Protocolo IMAP4**

Um servidor compatível com clientes IMAP também recebe e armazena as mensagens endereçadas a seus usuários. Entretanto, ao contrário do POP, o IMAP mantém as mensagens nas caixas de correio no servidor, a menos que elas sejam excluídas pelo usuário. A versão mais recente de IMAP é o IMAP4, que ouve solicitações do cliente na porta 143.

Existem muitos servidores de e-mail diferentes para as diversas plataformas de sistema operacional de rede.

## 16.7.3 Mensagens de texto

As mensagens de texto, mostradas na figura, são uma das ferramentas de comunicação mais populares em uso atualmente. Além disso, o software de mensagens de texto é integrado a muitos aplicativos online, aplicativos de smartphones e sites de mídia social.

![[Pasted image 20260611065848.png]]

As mensagens de texto também podem ser chamadas de mensagens instantâneas, mensagens diretas, mensagens privadas e mensagens de bate-papo. As mensagens de texto permitem que os usuários se comuniquem ou conversem pela Internet em tempo real. Os serviços de mensagens de texto em um computador geralmente são acessados por meio de um cliente baseado na Web integrado a uma mídia social ou site de compartilhamento de informações. Esses clientes geralmente se conectam apenas a outros usuários do mesmo site.

Há também vários clientes de mensagens de texto autônomos, como Cisco Webex Teams, Microsoft Teams, WhatsApp, Facebook Messenger e muitos outros. Esses aplicativos estão disponíveis para uma ampla variedade de sistemas operacionais e dispositivos. Uma versão móvel é normalmente oferecida. Além de mensagens de texto, esses clientes suportam a transferência de documentos, vídeos, músicas e arquivos de áudio.

## 16.7.4 Chamadas telefônicas pela Internet

Fazer chamadas telefônicas pela Internet está se tornando cada vez mais popular. Os clientes de Telefonia de Internet usam a tecnologia peer-to-peer, semelhante àquela utilizada pelas mensagens instantâneas, como mostrado na figura. A telefonia IP usa a tecnologia Voice over IP (VoIP) que converte os sinais de voz analógicos em dados digitais. Os dados de voz são encapsulados em pacotes IP, que transportam a chamada telefônica pela rede.

Uma vez instalado o software de telefone IP, basta o usuário selecionar um nome exclusivo. Isso ocorre para que as chamadas de outros usuários possam ser recebidas. É necessário ter alto-falantes e um microfone, integrados ou separados. É comum conectar um headset ao computador para servir de telefone.

As chamadas são feitas para outros usuários do mesmo serviço na Internet selecionando o nome de usuário em uma lista. Uma chamada para um telefone comum (fixo ou celular) requer o uso de um gateway para acessar a Rede Telefônica Pública Comutada (PSTN). Dependendo do serviço, pode haver taxas associadas a esse tipo de chamada. As portas de destino e os protocolos usados por aplicativos de Telefonia de Internet podem variar de acordo com o software.

![[Pasted image 20260611065908.png]]

## 16.7.5 Verifique a sua compreensão - e-mail e Mensagens

**Verifique sua compreensão sobre e-mail e mensagens , escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Este protocolo é utilizado por um cliente para enviar correio eletrônico para um servidor de correio.

- [ ] POP
- [x] SMTP
- [ ] IMAP
- [ ] HTTP

✅ RESPOSTA CORRETA: SMTP

> Os clientes de e-mail se conectam a servidores SMTP pela porta 25 para enviar e-mail. POP e IMAP são usados pelos clientes para receber e-mails. HTTP é usado entre navegadores web e servidores web.

---

### Pergunta 2

Qual é uma característica do IMAP?

- [ ] Ele faz o upload de mensagens de e-mail para um servidor.
- [x] Ele baixa uma cópia das mensagens de e-mail deixando as originais no servidor.
- [ ] Ele escuta passivamente na porta 110 por solicitações de clientes.

✅ RESPOSTA CORRETA: Ele baixa uma cópia das mensagens de e-mail deixando as originais no servidor.

> IMAP é um protocolo para os clientes recuperarem cópias de mensagens de e-mail de um servidor IMAP. As mensagens originais permanecem no servidor até serem excluídas manualmente.

---

### Pergunta 3

Verdadeiro ou falso? A mensagem de texto está disponível apenas em um smartphone?

- [x] falso
- [ ] verdadeiro

✅ RESPOSTA CORRETA: falso

> Falso. Os aplicativos de mensagens de texto estão disponíveis para uma ampla variedade de sistemas operacionais e dispositivos.


## 16.8.1 O que aprendi neste módulo?

### A relação Cliente - Servidor

O termo servidor refere-se a um host executando um aplicativo de software que fornece informações ou serviços para outros hosts conectados à rede, como um servidor web. Um exemplo de software cliente é um navegador, como Chrome ou FireFox. Um único computador pode também executar vários tipos de software cliente. Um fator crucial para permitir que essas interações complexas funcionem é que todas elas usam padrões e protocolos acordados.

A principal característica de sistemas cliente/servidor é que o cliente envia uma solicitação para o servidor, o qual responde ao executar uma função, como o envio de um documento solicitado de volta para o cliente. A combinação de navegador Web e servidor Web é provavelmente a instância mais usada de um sistema cliente/servidor.

Um URI é uma sequência de caracteres que identifica um recurso de rede específico. As partes de uma URI são protocolo/esquema, nome do host, caminho e nome do arquivo e fragmento. Uma URI tem duas especializações:

- **URN** - Identifica apenas o namespace do recurso sem referência ao protocolo.
- **URL** - Isso define o localização de rede de um recurso específico na rede. URLs de HTTP ou HTTPS são normalmente usados por navegadores web. Outros protocolos como FTP, SFTP, SSH e outros podem ser usados por meio de uma URL.

---

### Network Application Services

Para a maioria das pessoas, os serviços de Internet mais comuns que eles usam incluem pesquisas na Internet, sites de mídia social, streaming de vídeo e áudio, sites de compras on-line, e-mail e mensagens. Cada um desses serviços depende de protocolos, do conjunto de protocolos TCP/IP, para comunicar de forma confiável as informações entre os clientes e os servidores. Os serviços comuns incluem: DNS, SSH, SMTP, POP, IMAP, DHCP, HTTP e FTP.

---

### Domain Name System (Sistema de Nomes de Domínios).

O DNS fornece uma maneira para os hosts solicitarem o endereço IP de um servidor específico. Os nomes DNS são registrados e organizados na Internet em grupos ou domínios específicos de alto nível. Alguns dos domínios de alto nível mais comuns na Internet são .com, .edu e .net.

Quando o servidor DNS recebe a solicitação de um host, ele verifica sua tabela para determinar o endereço IP associado a esse servidor web. Se o servidor DNS local não tiver uma entrada para o nome solicitado, ele consultará outro servidor DNS no domínio. Quando o servidor DNS aprende o endereço IP, essa informação é enviada de volta ao host.

---

### Clientes e servidores Web

Quando um cliente Web recebe o endereço IP de um servidor Web, o navegador do cliente usa esse endereço IP e a porta 80 para solicitar serviços da Web. Essa solicitação é enviada para o servidor usando HTTP. O protocolo HTTP não é um protocolo seguro; as informações podem ser facilmente interceptadas por outros usuários à medida que os dados são enviados pela rede. Para fornecer segurança aos dados, o HTTP pode ser usado com protocolos de transporte seguros. As solicitações de HTTP seguro são enviadas para a porta 443. Essas solicitações usam https no endereço do site no navegador, em vez de http.

Quando um cliente Web recebe o endereço IP de um servidor Web, o navegador do cliente usa esse endereço IP e a porta 80 para solicitar serviços da Web. O conteúdo de informação de uma página web é codificado usando HTML. A codificação HTML informa ao navegador como formatar a página Web e quais gráficos e fontes usar.

Existem muitos servidores web e clientes web diferentes. Os padrões de HTML e do protocolo HTTP fazem com que esses servidores e clientes de diversos fabricantes trabalhem em conjunto sem dificuldades.

---

### Clientes e servidores FTP

O FTP fornece um método fácil de transferir arquivos de um computador para outro. Um host com software de cliente FTP pode acessar um servidor FTP para executar várias funções de gerenciamento de arquivos, como uploads e downloads. O servidor FTP permite que o cliente troque arquivos entre dispositivos. Ele também possibilita que os clientes gerenciem arquivos remotamente enviando comandos de gerenciamento de arquivos, como delete ou rename. Para conseguir isso, o serviço FTP usa duas portas diferentes para a comunicação entre cliente e servidor. Para iniciar uma sessão de FTP, as solicitações de conexão de controle são enviadas para o servidor usando a porta TCP de destino 21. Quando a sessão é aberta, o servidor usa a porta TCP 20 para transferir os arquivos de dados.

A maioria dos sistemas operacionais de cliente (como Windows, Mac OS e Linux) inclui uma interface de linha para o FTP. Há também um software cliente FTP baseado em GUI que fornece uma interface simples de arrastar e soltar para FTP.

---

### Terminais virtuais

O Telnet fornece um método padrão de emulação de dispositivos terminais baseados em texto na rede de dados. O protocolo e o software cliente que implementa o protocolo são comumente chamados de Telnet. Os servidores Telnet escutam solicitações de clientes na porta TCP 23. Uma conexão usando Telnet é chamada de sessão vty, ou conexão. Em vez de usar um dispositivo físico para se conectar ao servidor, o Telnet usa software para criar um dispositivo virtual que fornece os mesmos recursos de uma sessão de terminal com acesso à CLI do servidor.

O Telnet não é considerado um protocolo seguro. Embora o protocolo Telnet possa exigir o login de um usuário, ele não suporta o transporte de dados criptografados. Todos os dados trocados durante as sessões Telnet são transportados como texto simples pela rede. Isso significa que os dados podem ser facilmente interceptados e compreendidos.

O SSH fornece a estrutura para proteger login remoto e outros serviços de rede segura. Ele também fornece autenticação mais forte do que o Telnet e suporta o transporte de dados de sessão usando criptografia. Os profissionais de rede devem procurar usar SSH no lugar de Telnet, sempre que possível.

---

### E-mails e mensagens

Cada servidor de e-mail recebe e armazena e-mails de usuários que têm caixas de correio configuradas no servidor de e-mail. Cada usuário com uma caixa de correio deve usar um cliente de e-mail para acessar o servidor de e-mail e ler essas mensagens. Muitos sistemas de mensagens da Internet usam um cliente baseado na Web para acessar emails, incluindo Microsoft 365, Yahoo e Gmail. Os protocolos de aplicação usados no processamento de e-mail incluem SMTP, POP3 e IMAP4.

O SMTP é usado por um cliente de e-mail para enviar mensagens para o servidor de e-mail local. O servidor local então decide se a mensagem é destinada a uma caixa de correio local ou se é endereçada a uma caixa de correio em outro servidor. Se o servidor precisar enviar uma mensagem para um servidor diferente, o SMTP será usado entre esses dois servidores. As solicitações SMTP são enviadas para a porta 25. Um servidor compatível com clientes POP recebe e armazena as mensagens endereçadas a seus usuários. Quando o cliente se conecta ao servidor de e-mail, as mensagens são baixadas no cliente. Por padrão, as mensagens não são mantidas no servidor após serem acessadas pelo cliente. Os clientes contatam os servidores POP3 na porta 110.

Um servidor compatível com clientes IMAP também recebe e armazena as mensagens endereçadas a seus usuários. Entretanto, ao contrário do POP, o IMAP mantém as mensagens nas caixas de correio no servidor, a menos que elas sejam excluídas pelo usuário. A versão mais recente de IMAP é o IMAP4, que ouve solicitações do cliente na porta 143.

As mensagens de texto podem ser chamadas de mensagens instantâneas, mensagens diretas, mensagens privadas e mensagens de bate-papo. As mensagens de texto permitem que os usuários conversem pela Internet em tempo real. Os serviços de mensagens de texto em um computador geralmente são acessados por meio de um cliente baseado na Web integrado a uma mídia social ou site de compartilhamento de informações. Esses clientes geralmente se conectam apenas a outros usuários do mesmo site.

Um cliente de telefonia pela Internet usa tecnologia peer-to-peer semelhante à usada por mensagens instantâneas. A telefonia IP usa VoIP, que converte sinais de voz analógicos em dados digitais. Os dados de voz são encapsulados em pacotes IP, que transportam a chamada telefônica pela rede.

## 16.8.2 Webster - Questões para Reflexão

Como você já sabe, quando você deseja acessar um arquivo ou site que não está localizado no seu computador, ele se torna o "cliente" que está enviando uma solicitação para um "servidor". Talvez você esteja apenas observando o arquivo. E se você precisar baixar uma cópia para o seu computador? Talvez você esteja apenas visitando um site. Tudo isso ocorre na camada de aplicação da rede. O que mais você pode fazer on-line devido aos protocolos e serviços encontrados na camada de aplicação?