
# 16.0 Introdução

## 16.0.1 Webster - Por que devo fazer este módulo?

Kishori precisa ter acesso a um arquivo de paciente. Ela já fez isso muitas vezes, mas só agora está se perguntando como esse processo realmente acontece em uma rede. De onde vem este documento eletrônico? Como ela consegue de acessar a intranet do hospital? Como ela consegue acessar a Internet? Tudo isso é possível devido aos serviços da camada de aplicação.

Kishori tem mais a aprender antes de se candidatar para a posição mencionada por Rina. Existem muitos serviços que funcionam na camada de aplicação, incluindo alguns com os quais você está familiarizado, como FTP, DHCP e DNS. Quando você quiser recuperar algo que ainda não está localizado no seu computador, você será o cliente a solicitar que o servidor apropriado envie esse item. E, é claro, você já sabe que haverá protocolos envolvidos. Continue lendo...

## 16.0.2 O Que Vou Aprender Neste Módulo?

**Título do Módulo:** Serviços da Camada de Aplicação

**Objetivo do Módulo:** Explicar a função dos serviços comuns da camada de aplicação.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|A relação Cliente — Servidor|Explicar a interação entre clientes e servidores.|
|Network Application Services|Descrever as aplicações comuns de rede.|
|Domain Name System (Sistema de Nomes de Domínios).|Descrever o DNS.|
|Clientes e servidores Web|Descrever HTTP e HTML.|
|Clientes e servidores FTP|Descrever o FTP.|
|Terminais virtuais|Descrever o Telnet e o SSH.|
|E-mails e mensagens|Descrever os protocolos de e-mail.|

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

Neste vídeo, vamos usar o Packet Tracer para ilustrar como uma página web é obtida de um servidor web.

Neste caso, temos um PC que está conectado através de uma nuvem de internet simulada para um servidor web. Esse servidor web está em www.learnip.com, também no endereço IP 172.33.100.50.

Vamos ao PC e solicitar uma página web. Para solicitar uma página web, temos que usar um cliente que é apropriado para um servidor web. Começamos escolhendo o cliente web — o cliente apropriado para visualizar uma página web é o navegador web. Vamos abrir o navegador web, iniciar o utilitário de captura e capturar o tráfego do PC0 para o servidor web.

Colocamos a URL learnip.com no navegador e solicitamos o pacote. Você pode ver que os pacotes HTTP estão sendo gerados e estão viajando pela internet simulada para o servidor web. O servidor web irá então responder e entregar a página web de volta ao PC.

Neste ponto vamos parar a captura e dar uma olhada em alguns desses pacotes. Se examinarmos as informações do pacote clicando na caixa ao lado do pacote que queremos investigar, podemos ver que é um pacote HTTP que está gerando uma solicitação web. Ele está usando o TCP como seu protocolo de transporte e está indo para o endereço IP de destino do servidor web. Você pode ver neste pacote que o endereço IP de origem é o endereço IP de PC0. Você também pode ver que, quando for comunicado, é inicialmente formatado como um quadro Ethernet e passa pela conexão Ethernet entre o PC0 e seu primeiro hub para acessar a internet.

Quando o servidor web responde, o servidor recebe a solicitação que recebeu do PC0 e em seguida envia de volta a resposta. Como você pode ver, a resposta é destinada ao PC0 como destino. Este processo continuará à medida que todas as informações relacionadas à página web são transmitidas.






## 16.1.5 Packet Tracer - A interação do cliente
### Packet Tracer - A interação do cliente

### Objetivos

Observar a interação de cliente entre o servidor e o PC.

### Histórico/Cenário

Clientes, como PCs desktops, solicitam serviços dos servidores. O ambiente do laboratório, com PCs e servidores, suporta uma grande variedade de serviços. Em um ambiente simulado, o número de serviços é limitado. O Packet Tracer permite a adição de servidores de rede que suportam DHCP, DNS, HTTP e TFTP. O Packet Tracer também suporta a adição de PCs simulados que podem solicitar esses serviços. Essa atividade usa uma rede simples com um PC conectado diretamente a um servidor configurado para fornecer serviços DNS e hospedar uma página Web através de um servidor HTTP. Essa atividade rastreará o fluxo de tráfego que ocorre quando uma página da Web é solicitada, como o endereço IP da página da Web é resolvido e como a página da Web é disponibilizada.

### Instruções

## Parte 1: Entre no modo de simulação.

Quando o Packet Tracer inicia, ele apresenta uma visão lógica da rede em modo de tempo real.

Clique em **Simulation Mode** para entrar no modo de simulação. O ícone  simulation mode está localizado no canto inferior direito do logical workplace.

## Parte 2: Defina os Filtros da Lista de Eventos.

No simulation mode, o padrão é capturar todos os eventos. Você usará os filtros somente para capturar os eventos de DNS e HTTP.

a.  Na seção **Event List Filters**, clique em **Show All/None** para desmarcar todas as seleções.

b.  Clique em **Edit Filters**. Na guia IPv4, selecione **DNS**. Na guia Misc, selecione **HTTP**. Feche a janela quando terminar. Os **Event List Filters** mostram o DNS e o HTTP como os únicos eventos visíveis.

## Parte 3: Solicite uma página Web em um PC.

Você abrirá um navegador da Web simulado no PC e solicitará uma página Web do servidor.

a.  Clique em **PC**. Clique na guia **Desktop** e no **Web Browser**.

b.  Um navegador da Web simulado será aberto. Digite **www.example.com** na caixa da URL e clique no botão **Go** à direita. Minimize a janela do PC.

## Parte 4: Execute a simulação.

a.  Na seção **Play Controls** do **Simulation Panel**, clique **Play**. A troca entre o PC e o servidor é animada e os eventos são adicionados na **Event List**.

Esses eventos representam a solicitação do PC pela resolução da URL para um endereço IP, o fornecimento do endereço IP pelo servidor, a solicitação do PC pela a página Web, o servidor enviando a página Web em dois segmentos e o reconhecimento do PC sobre a página Web.

b.  Clique em **View Previous Event** (Visualizar Evento Anterior) para continuar quando o buffer estiver completo.

## Parte 5: Acesse uma PDU específica.

a.  Restaure a janela simulada do PC. Observe que há uma página Web em exibição no Navegador da Web. Minimize a janela simulada do navegador.

b.  Na seção **Simulation Panel Event List**, a última coluna contém uma caixa colorida que fornece acesso a informações detalhadas sobre um evento. Clique na caixa colorida na primeira linha para o primeiro evento. A janela **PDU Information** (janela de Informações da PDU) será aberta.

## Parte 6: Examine o conteúdo da janela de Informações da PDU.

A primeira guia na janela de informações da PDU contém informações sobre a PDU de entrada e/ou de saída com base no modelo OSI. Clique em **Next Layer >>** repetidamente para percorrer as camadas de inbound e outbound e leia a descrição na caixa abaixo das camadas para obter uma visão geral de como a troca funciona.

Examine as informações da PDU quanto aos outros eventos para ter um resumo de todo o processo de troca.


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