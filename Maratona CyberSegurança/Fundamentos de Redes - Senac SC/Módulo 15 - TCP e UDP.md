
# 15.0 Introdução

## 15.0.1 Webster - Por que devo fazer este módulo?

Kishori chega cedo ao trabalho para fazer uma chamada de videoconferência no computador da estação de enfermagem. Ela entra na sessão sobre o protocolo de máscara no hospital. Ao ouvir atentamente o apresentador, ela percebe algumas palavras descartadas. Ela se pergunta se há algum problema com a rede. Isso é semelhante ao tablet perder a conexão por um momento? Mas ela se lembra de que está usando um computador conectado à rede.

Imediatamente após a chamada, ela envia um e-mail para Madhav no departamento de TI. Madhav vem até a mesa de Kishori. Ela está confusa porque todos os dispositivos parecem estar conectados. Madhav explica que UDP e TCP são protocolos de camada de transporte que operam um pouco diferente. Ele diz a ela que o UDP é um sistema de entrega de melhor esforço que não requer confirmação de recebimento. O UDP é preferível para aplicações como a transmissão de áudio e vídeo ao vivo, e Voz sobre IP (VoIP). O UDP é usado para chamadas de videoconferência.

Kishori nunca tinha ouvido falar nisso. E você, já? Neste módulo, você comparará esses protocolos. Continue lendo!

## 15.0.2 O que vou aprender neste módulo?

**Titulo do módulo:** TCP e UDP

**Objetivo do Módulo:** Explicar como os clientes acessam os serviços de Internet.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|TCP e UDP|Comparar as funções da camada de transporte TCP e UDP.|
|Números de porta|Explicar como o TCP e o UDP usam números de porta.|


# 15.1 TCP e UDP

## 15.1.1 Vídeo - Operação do TCP e UDP

Nesta lição vamos falar sobre os dois protocolos da camada de transporte, TCP e UDP.

Vou começar com UDP. UDP é um protocolo usado principalmente em streaming ou comunicações em tempo real. A razão pela qual o UDP funciona melhor nesses tipos de ambientes é que o UDP não está atrelado a um monte de sobrecarga.

Na camada de transporte, o que acontece é que as comunicações — ou seja, dados, que são uma grande sequência de bits — são movidos para baixo, para a camada de transporte. Na camada de transporte, eles são divididos em segmentos. Cada um desses segmentos recebe informações de porta no cabeçalho. Então, é a partir de, digamos, uma porta aleatória 5105 como origem, e vamos dizer que o destino é um servidor DNS, então essa seria a porta 53. Cada um desses segmentos é rotulado com a porta de origem e a porta de destino para que eles se tornem parte da mesma conversa.

Quando estes forem transmitidos através de uma rede, digamos como a internet, eles podem não ir todos exatamente da mesma maneira. Alguns deles podem se perder ao longo do caminho ou podem ficar fora de ordem. Mas em tempo real — por exemplo, ouvindo minha voz em tempo real, se estivéssemos tendo uma conversa por telefone IP — se um pacote é perdido, provavelmente não perceberíamos isso a menos que fosse um longo fluxo de pacotes. Basicamente, em tempo real, apenas deixamos que esses pacotes tomem seu caminho da origem ao destino e que a resposta retorne. Não estamos tão preocupados com alguns pacotes sendo perdidos no caminho ou fora de ordem quando forem recebidos, porque em tempo real isso não vai importar — não vamos voltar para resgatar essas outras coisas, e a demora em esperar seria mais disruptiva para as comunicações do que perder esses poucos pacotes.

Mas definitivamente existem aplicações onde até mesmo perder um único pacote seria catastrófico. Por exemplo, em uma transferência bancária, se estivéssemos enviando milhões de dólares pela internet e perdemos alguns pacotes que continham os números das contas, seria muito chato para as pessoas que perderam suas informações.

Vamos falar agora sobre o outro protocolo, TCP. Quando os networkers falam sobre UDP e TCP, eles falam sobre eles em termos de confiabilidade. Por confiabilidade, o que eles querem dizer é que se os pacotes forem perdidos em um fluxo UDP, eles não são retransmitidos e não há nenhuma preocupação acontecendo sobre se eles chegam ou não lá. Mas em TCP, confiabilidade é construída não em se algum pacote é descartado ou não, mas no fato de haver um mecanismo que garante que o menor número de pacotes seja descartado e, em segundo lugar, que se algum for descartado, eles serão retransmitidos automaticamente, sem que o aplicativo do usuário final precise se preocupar com isso.

Nas comunicações TCP, temos uma origem e um destino, assim como nas comunicações UDP. Mas cada segmento TCP tem um número de sequência, em adição aos números de porta de origem e destino. Por exemplo, se estivéssemos buscando uma página web e enviando a solicitação, teríamos como origem nosso número de porta aleatório e o número da porta de destino seria 80, que é a porta TCP atribuída a um servidor web. Então teríamos um número de sequência atribuído a cada um desses segmentos, para que quando forem transmitidos pela internet para o servidor, o servidor possa receber esses pacotes e poder contabilizar cada um. Então, por exemplo, se isso é um, dois e três, e o servidor pegou todos eles, enviaria de volta uma confirmação dizendo que quer que eu comece a próxima sequência com quatro.

A comunicação constante ocorre entre os dois dispositivos finais — a origem e o destino — para determinar quantos pacotes são enviados antes que um reconhecimento retorne. Essa é a sobrecarga da qual eu estava falando. Em uma conexão muito confiável, eventualmente isso pode se realizar com centenas de milhares de pacotes. Em comunicações muito pouco confiáveis — digamos, por exemplo, através de um link de satélite percorrendo todo o mundo, onde há a possibilidade de muitos pacotes serem descartados — a janela de pacotes que será enviada antes de uma confirmação ficará cada vez menor. Isso garante que um menor número de pacotes seja descartado, porque estão sendo confirmados muito mais frequentemente em uma conexão não confiável do que estariam em uma conexão muito confiável.

Então a diferença entre TCP e UDP é que o TCP tem uma confirmação de recebimento dos pacotes, e esses números de sequência também permitem que o host de destino coloque os pacotes de volta na ordem em que foram enviados. No entanto, com UDP, não há confirmações e nem números de sequência.

Cada protocolo, porém, tem seu lugar nas comunicações pela internet, e muitas vezes é a criticidade de cada pacote que está sendo recebido que faz a diferença se a transmissão será enviada via UDP ou TCP.

## 15.1.2 Verifique a sua compreensão - TCP e UDP

**Verifique sua compreensão de TCP e UDP , escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Qual camada do modelo TCP / IP é responsável por garantir que os pacotes sejam enviados de forma confiável e que os pacotes ausentes sejam reenviados?

- [ ] Camada de aplicação
- [x] camada de transporte
- [ ] camada de inter-redes
- [ ] camada de acesso à rede

✅ RESPOSTA CORRETA: camada de transporte

> A camada de transporte nos modelos TCP / IP e OSI é responsável por garantir que os pacotes sejam enviados de forma confiável e que os pacotes ausentes sejam reenviados.

---

### Pergunta 2

Verdadeiro ou falso: O Transport Control Protocol (TCP) não controla os segmentos enviados para o destino.

- [x] falso
- [ ] verdadeiro

✅ RESPOSTA CORRETA: falso

> Falso. O TCP monitora o número de segmentos que foram enviados a um host específico de um aplicativo específico.

---

### Pergunta 3

Verdadeiro ou falso: O User Datagram Protocol (UDP) não usa confirmações para rastrear o recebimento de segmentos.

- [x] verdadeiro
- [ ] falso

✅ RESPOSTA CORRETA: verdadeiro

> Verdadeiro. O UDP é um sistema de entrega de melhor esforço que não requer confirmação de recebimento.


# 15.2 Números de porta

## 15.2.1 Vídeo - Números de porta da camada de transporte

Nesta lição, vamos falar sobre como os números de porta da camada de transporte são usados para identificar conversas e aplicativos que são o destino e a origem das transmissões.

Vamos falar sobre a configuração de um servidor. Quando configuramos um servidor para fornecer serviços pela rede, carregamos aplicativos nesse servidor. Por exemplo, um aplicativo de servidor web, um aplicativo FTP, ou um aplicativo de transporte de correio. Quando configuramos esses serviços, uma porta é atribuída a eles — uma porta da camada de transporte — ao próprio serviço.

Existem alguns serviços padrão. Números de porta abaixo de 1024 são frequentemente chamados de portas bem conhecidas. A razão pela qual são chamadas de bem conhecidas é porque são as mais comumente usadas. Por exemplo, um servidor web escuta comunicações endereçadas à porta 80. O servidor FTP, à porta 21. O servidor de correio, à porta 25. Estas, e muitas outras portas conhecidas, são automaticamente identificadas pelos clientes. Sempre que abrimos um navegador web e digitamos uma URL, não precisamos dizer qual porta, porque o cliente — neste caso o navegador web — já sabe que os servidores web estão escutando na porta 80 para poder responder a solicitações de páginas web.

Então, quando nosso servidor web está escutando, isso significa que ele tem um buffer configurado que aceitará solicitações endereçadas ao seu endereço IP e também à porta TCP 80. Se espera-se que o servidor FTP responda, as comunicações serão endereçadas à porta 21. Isso nos permite ter muitos serviços diferentes rodando ao mesmo tempo no servidor.

Do lado do host, as portas para TCP e UDP são atribuídas dinamicamente a partir do intervalo acima de 1024, e essas portas são atribuídas aleatoriamente. Basicamente, seu PC escolhe um valor fora do intervalo bem conhecido e o usa como uma porta de origem. Digamos que seu navegador web esteja aberto e você está solicitando uma página web. O navegador web escolherá uma porta TCP. Quando o tráfego vai para a camada de transporte, a porta TCP será a porta de destino 80 e a de origem, uma das portas atribuídas aleatoriamente.

Assim, quando as comunicações saem do host e vão para o servidor web, o servidor web verá a porta de destino como 80 e colocará automaticamente essa solicitação na fila para o servidor web processar. Quando o servidor web formula sua resposta, ele responderá de volta com a porta de destino 5305 e a porta de origem de 80. Então, quando volta para o host, o host saberá que este é o pedido que foi enviado pelo navegador da web, porque a porta 5305 foi atribuída à solicitação do navegador web.

Portas TCP e UDP na camada de transporte são o que permitem que nossos dispositivos tenham muitas aplicações diferentes ao mesmo tempo e que todas essas aplicações estejam se comunicando simultaneamente. Por exemplo, se eu também tivesse um cliente FTP rodando, seria possível enviar solicitações FTP com um número de porta diferente. Neste caso, seria destino 21 e porta de origem 5307. As comunicações voltariam pelo mesmo processo, veria que a porta de destino seria 21 e iria para a fila do servidor FTP. Quando a resposta voltasse, seria endereçada à porta de destino 5307, para que o host saiba que esse foi o pedido do cliente FTP.

## 15.2.2 Números de porta TCP e UDP

São muitos os serviços que acessamos pela Internet ao longo do dia. DNS, Web, E-mail, FTP, Mensagem instantânea e VoIP são apenas alguns desses serviços que são disponibilizados por sistemas cliente/servidor em todo o mundo. Eles podem ser fornecidos por um único servidor ou por vários servidores em grandes datacenters.

Quando uma mensagem é entregue usando o TCP ou o UDP, os protocolos e os serviços são identificados por um número de porta. Uma porta é um identificador numérico dentro de cada segmento que é usado para rastrear conversas específicas entre um cliente e um servidor. Cada mensagem que um host envia contém uma porta origem e destino.

![[Pasted image 20260610200415.png]]

Quando uma mensagem é recebida por um servidor, é necessário que o servidor consiga determinar qual serviço está sendo solicitado pelo cliente. Os clientes são pré-configurados para usar uma porta de destino que foi registrada na Internet para cada serviço. Um exemplo disso são os clientes de navegador da Web, que são configurados previamente para enviar solicitações para servidores da Web pela porta 80, a porta usada normalmente para serviços da Web em HTTP.

As portas são atribuídas e gerenciadas por uma organização conhecida como ICANN (Internet Corporation for Assigned Names and Numbers, Corporação da Internet para Atribuição de Nomes e Números). As portas foram divididas em três categorias e variam em número de 1 a 65.535.

- **Portas bem conhecidas** — As portas de destino que estão associadas a aplicativos de rede comuns são identificadas como portas bem conhecidas. Elas estão no intervalo de 1 a 1.023.
- **Portas registradas** — As portas 1.024 a 49.151 podem ser usadas como portas de destino ou de origem. Elas podem ser usadas por empresas para registrar aplicativos específicos, como os de mensagem instantânea.
- **Portas privadas** — As portas de 49.152 a 65.535 são geralmente utilizadas como portas de origem. Elas podem ser usadas por qualquer aplicativo.

A tabela exibe alguns números de porta conhecidos comuns e seus aplicativos associados.

|Número da Porta|Transporte|Protocolo de aplicação|
|---|---|---|
|20|TCP|Protocolo de Transferência de Arquivos (FTP) — Dados|
|21|TCP|FTP — Controle|
|22|TCP|Secure Shell (Shell seguro) — SSH|
|23|TCP|Telnet|
|25|TCP|Protocolo SMTP|
|53|UDP, TCP|Protocolo DNS|
|67|UDP|Dynamic Host Configuration Protocol (DHCP) — Servidor|
|68|UDP|Cliente DHCP|
|69|UDP|Protocolo de Transferência Trivial de Arquivo (TFTP)|
|80|TCP|Protocolo HTTP|
|110|TCP|Protocolo POP3 (Post Office Protocol — Protocolo dos Correios)|
|143|TCP|Protocolo IMAP|
|161|UDP|Protocolo de Gerenciamento Simples de Rede (SNMP)|
|443|TCP|HTTPS (Secure Hypertext Transfer Protocol — Protocolo de Transferência de Hipertexto Seguro)|

Algumas aplicações podem usar tanto TCP quanto UDP. Por exemplo, o DNS usa o protocolo UDP quando os clientes enviam requisições a um servidor DNS. Contudo, a comunicação entre dois servidores DNS sempre usa TCP.

Pesquise no site da IANA o registro de portas para visualizar a lista completa de números de portas e aplicativos associados.



## 15.2.3 Pares de Soquetes

As portas origem e destino são colocadas no segmento. Os segmentos são encapsulados em um pacote IP. O pacote IP contém o endereço IP de origem e destino. A combinação do endereço IP de origem e o número de porta de origem, ou do endereço IP de destino e o número de porta de destino é conhecida como um socket.

No exemplo na figura, o PC está solicitando simultaneamente serviços FTP e Web do servidor de destino.

![[Pasted image 20260610200542.png]]

No exemplo, a solicitação FTP gerada pelo PC inclui os endereços MAC da Camada 2 e os endereços IP da Camada 3. A solicitação também identifica o número da porta de origem 1305 (ou seja, gerado dinamicamente pelo host) e a porta de destino, identificando os serviços de FTP na porta 21. O host também solicitou uma página da Web do servidor usando os mesmos endereços de Camada 2 e Camada 3. No entanto, ele está usando o número da porta de origem 1099 (ou seja, gerado dinamicamente pelo host) e a porta de destino identificando o serviço Web na porta 80.

O socket é usado para identificar o servidor e o serviço que está sendo solicitado pelo cliente. Um socket do cliente pode ser assim, com 1099 representando o número da porta de origem: 192.168.1.5:1099

O soquete em um servidor da web pode ser 192.168.1.7:80

Juntos, esses dois sockets se combinam para formar um par de sockets: 192.168.1.5:1099, 192.168.1.7:80

Os sockets permitem que vários processos em execução em um cliente se diferenciem uns dos outros, e várias conexões com um processo no servidor sejam diferentes umas das outras.

Este número de porta age como um endereço de retorno para a aplicação que faz a solicitação. A camada de transporte rastreia essa porta e a aplicação que iniciou a solicitação, de modo que quando uma resposta é retornada, ela pode ser encaminhada para a aplicação correta.


## 15.2.4 O Comando netstat

Conexões TCP desconhecidas podem representar uma grande ameaça à segurança. Elas podem indicar que algo ou alguém está conectado ao host local. Às vezes é necessário conhecer quais conexões TCP ativas estão abertas e sendo executadas em um host de rede. O netstat é um utilitário de rede importante que pode ser usado para verificar essas conexões. Como mostrado abaixo, digite o comando **netstat** para listar os protocolos em uso, o endereço local e os números de porta, o endereço externo e os números de porta e o estado da conexão.

```
C:\> netstat

Active Connections

  Proto  Local Address          Foreign Address            State
  TCP    192.168.1.124:3126     192.168.0.2:netbios-ssn    ESTABLISHED
  TCP    192.168.1.124:3158     207.138.126.152:http       ESTABLISHED
  TCP    192.168.1.124:3159     207.138.126.169:http       ESTABLISHED
  TCP    192.168.1.124:3161     sc.msn.com:http            ESTABLISHED
  TCP    192.168.1.124:3166     www.cisco.com:http         ESTABLISHED
(output omitted)
C:\> netstat
```


Por padrão, o comando **netstat** tentará resolver os endereços IP para os nomes de domínio e os números de porta para aplicações bem conhecidas. A opção **n** pode ser usada para exibir endereços IP e números de porta em sua forma numérica.


## 15.2.5 Verifique sua compreensão - Números de Porta

**Verifique sua compreensão sobre números de porta, escolhendo a melhor resposta para as seguintes perguntas.**

### Pergunta 1

Suponha que um host com endereço IP 10.1.1.10 deseja solicitar serviços Web de um servidor em 10.1.1.254. Qual das opções a seguir exibe o par de soquetes correto?

- [x] 10.1.1. 10:1099, 10.1.1. 254:80
- [ ] 1099:10 .1.1.10, 80:10 .1.1.254
- [ ] 10.1.1. 10:80, 10.1.1. 254:1099
- [ ] 80:10 .1.1.10, 1099:10 .1.1.254

✅ RESPOSTA CORRETA: 10.1.1. 10:1099, 10.1.1. 254:80

> O par de soquetes para um host com endereço IP 10.1.1.10 solicitando serviços Web de um servidor em 10.1.1.254 seria 10.1.1. 10:1099, 10.1.1. 254:80.

---

### Pergunta 2

Qual grupo de portas inclui números de porta para aplicativos FTP, HTTP e TFTP?

- [ ] portas registradas
- [ ] portas dinâmicas
- [ ] portas privadas
- [x] portas bem conhecidas

✅ RESPOSTA CORRETA: portas bem conhecidas

> Os números de porta de aplicativos FTP, HTTP e TFTP são definidos no grupo de números de porta bem conhecido.

---

### Pergunta 3

Qual comando do Windows exibirá os protocolos em uso, o endereço local e os números de porta, o endereço externo e os números de porta e o estado da conexão?

- [ ] traceroute
- [x] netstat
- [ ] ping
- [ ] ipconfig/all

✅ RESPOSTA CORRETA: netstat

> O comando netstat do Windows exibe protocolos em uso, o endereço local e os números de porta, o endereço externo e os números de porta e o estado da conexão.


# 15.3 Resumo da TCP e UDP

## 15.3.1 O que aprendi neste módulo?

### TCP e UDP

O UDP é um sistema de entrega de melhor esforço que não requer confirmação de recebimento. O UDP é preferível para aplicações como a transmissão de áudio e vídeo ao vivo, e Voz sobre IP (VoIP). Confirmações retardariam a entrega e retransmissões são indesejáveis. Os pacotes seguem um caminho da origem até um destino. Alguns pacotes podem ser perdidos, mas isso geralmente não é percebido.

Os pacotes TCP seguem um caminho da origem até o destino. No entanto, cada um dos pacotes tem um número de sequência. O TCP divide uma mensagem em pequenos pedaços conhecidos como segmentos. Os segmentos são numerados em sequência e passados para o processo IP para montagem em pacotes. O TCP monitora o número de segmentos que foram enviados a um host específico de um aplicativo específico. Quando o remetente não recebe uma confirmação dentro de um certo período, ele supõe que os segmentos foram perdidos e transmite-os novamente. Somente a parte da mensagem perdida é reenviada, e não toda a mensagem.

---

### Números de porta

Quando uma mensagem é entregue usando o TCP ou o UDP, os protocolos e os serviços são identificados por um número de porta. Uma porta é um identificador numérico dentro de cada segmento que é usado para rastrear conversas específicas entre um cliente e um servidor. Cada mensagem que um host envia contém uma porta origem e destino.

Quando uma mensagem é recebida por um servidor, é necessário que o servidor consiga determinar qual serviço está sendo solicitado pelo cliente. Os clientes são pré-configurados para usar uma porta de destino que foi registrada na Internet para cada serviço.

As portas são atribuídas e gerenciadas por uma organização conhecida como ICANN (Corporação da Internet para Atribuição de Nomes e Números). As portas foram divididas em três categorias e variam em número de 1 a 65.535.

- **Portas bem conhecidas** — As portas de destino que estão associadas a aplicativos de rede comuns são identificadas como portas bem conhecidas. Elas estão no intervalo de 1 a 1.023.
- **Portas registradas** — As portas 1.024 a 49.151 podem ser usadas como portas de destino ou de origem. Elas podem ser usadas por empresas para registrar aplicativos específicos, como os de mensagem instantânea.
- **Portas privadas** — As portas de 49.152 a 65.535 são geralmente utilizadas como portas de origem. Elas podem ser usadas por qualquer aplicativo.

O número da porta de origem é gerado dinamicamente pelo dispositivo de envio para identificar uma conversa entre dois dispositivos. Este processo permite que várias conversações ocorram simultaneamente. É comum que um dispositivo envie várias solicitações de serviço HTTP para um servidor Web ao mesmo tempo. Cada conversa HTTP separada é rastreada com base em portas origem.

O cliente preenche um número de porta destino no segmento para informar o servidor destino qual serviço está sendo solicitado. Um servidor pode oferecer mais de um serviço simultaneamente como serviços Web na porta 80, ao mesmo tempo que oferece o estabelecimento de uma conexão FTP na porta 21.

Conexões TCP desconhecidas podem representar uma grande ameaça à segurança. Elas podem indicar que algo ou alguém está conectado ao host local. Às vezes é necessário conhecer quais conexões TCP ativas estão abertas e sendo executadas em um host de rede. O netstat é um utilitário de rede importante que pode ser usado para verificar essas conexões. O comando netstat é usado para listar os protocolos em uso, o endereço e os números de porta locais, o endereço e os números de porta externos, e o estado da conexão.

## 15.3.2 Webster — Questões para Reflexão

Uma vez, pedi móveis de uma dessas lojas online. Foi enviado para mim em três caixas diferentes, ao longo de duas semanas. Não estava preocupado com a falta de algo, pois recebi atualizações por e-mail que detalhavam a localização de cada caixa ao longo de sua rota desde a loja até minha casa. Esse exemplo é como o TCP. Durante todo o percurso, há verificações integradas para garantir que o que precisa ser entregue seja entregue e na ordem certa.

Ainda há uma necessidade de UDP na rede. Eu não gostaria de transmitir um filme onde ele para por minutos a fio, esperando que a rede envie a próxima cena. Você consegue pensar em uma boa analogia para o UDP?