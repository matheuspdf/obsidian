# 25.0 Introdução

## 25.0.1 Webster - Por que devo fazer este módulo?

Oi. Enquanto Olcay e Abay estão trabalhando juntos, Olcay precisa usar o comando nslookup para verificar o status atual dos servidores de nomes. Olcay aproveita a oportunidade para ver o que o Abay sabe sobre serviços DNS e DHCP. Abay explica que o protocolo DNS define um serviço automatizado que combina os nomes dos recursos com o endereço de rede numérico necessário. Ele também explica o DHCP. Em vez de usar endereçamento estático para cada conexão, é mais eficiente ter endereços IPv4 atribuídos automaticamente usando DHCP. Olcay está impressionado com o conhecimento de Abay! Ele realmente tem feito sua lição de casa.

Você consegue explicar como os serviços DNS e DCHP operam? Aposto que este módulo vai ajudar. Continue lendo!


## 25.0.2 O que vou aprender neste módulo?

**Titulo do módulo:** Serviços de Endereçamento IP

**Objetivo do módulo:** Explicar como os serviços DNS e DHCP operam

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Serviços DNS|Explicar como funciona a DNS|
|Serviços DHCP|Explicar como o DHCP opera|

# 25.1 Serviços DNS

## 25.1.1 Vídeo - Serviço de Nome de Domínio
![[25.1.1.mp4#subtitle=anexos/25.1.1.vtt]]
Quando digitamos um nome de domínio como URL, `www.cisco.com`, como nosso cliente sabe o endereço IP com esse nome de domínio? A resposta está no DNS, o sistema de nome de domínio.

O sistema operacional verificará primeiro seu cache de DNS local para ver se ele já tem essas informações, de endereço IP para `www.cisco.com`. Se a informação não estiver presente no cache do DNS, o cliente enviará uma consulta para o endereço IP do servidor DNS local.

O servidor DNS local verificará seu próprio cache DNS para o endereço IP associado a `www.cisco.com`. Se ele já contiver essas informações, ele enviará uma resposta de volta para o cliente. Caso contrário, ele precisará obter a resposta para o cliente.

O servidor DNS local, também conhecido como servidor DNS recursivo, buscará uma resposta enviando uma consulta para o servidor de nome DNS raiz. Existem 13 servidores de nome raiz operados por 12 diferentes empresas, com mais do que 750 instâncias de servidores em todo o mundo.

Servidores de nomes raiz encaminharão solicitações aos servidores de domínio de nível superior apropriados. Um domínio de nível superior, ou TLD, é o que segue o ponto final de um nome de domínio, como `.com` ou `.org`. Existem servidores de domínio de nível superior para cada TLD.

Já que nosso cliente está solicitando o endereço IP para um nome de domínio que termina em `.com`, o servidor de nome raiz fará referência ao servidor DNS local para `.com` — o servidor de nome de domínio de nível superior, ou servidor TLD. O servidor de nome raiz envia o endereço IP de um dos muitos servidores TLD `.com` para o servidor DNS local. O servidor DNS local agora adicionará o endereço IP do servidor de TLD `.com` para o cache DNS.

Normalmente, o servidor DNS local já terá o endereço IP do servidor TLD `.com` em seu cache, portanto, ele não precisa perguntar ao servidor de nome raiz primeiro. O servidor DNS local agora fará a consulta ao servidor TLD `.com`.

Os servidores de domínio de nível superior têm conhecimento dos endereços IP de servidores autoritativos. Um servidor autoritativo DNS é o detentor final do endereço IP do domínio que o cliente procura. Neste exemplo, `cisco.com` é o servidor autoritativo para qualquer domínio que termine em `cisco.com`. Ele pode ser gerenciado pelo proprietário do domínio, como a Cisco Systems, ou por terceiros em nome do proprietário do domínio.

A função do servidor TLD `.com` é oferecer ao servidor DNS local o endereço IP do servidor autoritativo da `cisco.com`.

Estamos finalmente no último servidor da nossa hierarquia, o servidor autoritativo. O servidor DNS local agora tem o endereço IP do servidor autoritativo da `cisco.com`, e envia uma consulta para o servidor `cisco.com`, questionando o endereço IP para `www.cisco.com`, que é o nome de domínio solicitado pelo cliente.

O servidor autoritativo da `cisco.com` contém todos os endereços IP para qualquer domínio que termina em `cisco.com`, inclusive `www.cisco.com`. O servidor autoritativo da `cisco.com` envia o endereço IP que responde por `www.cisco.com` para o servidor DNS local.

O servidor DNS local adiciona essas informações ao cache de DNS e agora tem o que precisa para o cliente. O servidor DNS local agora pode responder à consulta do cliente com o endereço IP de `www.cisco.com`.

O cliente adiciona o endereço IP de `www.cisco.com` no cache DNS, e agora tem o endereço IP necessário para enviar um pacote IP para o servidor da web da `www.cisco.com`.

E aqui está outra visão de quem estava envolvido em resolver nosso nome de domínio `www.cisco.com` para um endereço IP.


## 25.1.2 Serviço de Nomes de Domínio (DNS)

Existem outros protocolos específicos da camada de aplicativo que foram projetados para facilitar a obtenção de endereços para dispositivos de rede. Esses serviços são essenciais porque seria muito demorado lembrar endereços IP em vez de URLs ou configurar manualmente todos os dispositivos em uma rede média a grande. Este tópico entra em mais detalhes sobre os serviços de endereçamento IP, DNS e DHCP.

Em redes de dados, os dispositivos são rotulados com endereços IP numéricos para enviar e receber dados pelas redes. Os nomes de domínio foram criados para converter o endereço numérico em um nome simples e reconhecível.

Na internet, nomes de domínio totalmente qualificados (FQDNs), como ( [http://www.cisco.com](http://www.cisco.com/)), são muito mais fáceis de lembrar do que 198.133.219.25, que é o endereço numérico real para este servidor. Se a Cisco decidir alterar o endereço numérico de [www.cisco.com](http://www.cisco.com/), é transparente para o usuário porque o nome de domínio permanece o mesmo. O novo endereço é simplesmente vinculado ao nome de domínio atual e a conectividade é mantida.

O protocolo DNS define um serviço automatizado que compara nomes de recursos com o endereço de rede numérico requisitado. Ele inclui o formato para consultas, respostas e dados. As comunicações do protocolo DNS utilizam um único formato, chamado de mensagem. Este formato de mensagem é utilizado para todos os tipos de consultas de cliente e respostas de servidor, mensagens de erro e transferência de informações de registro de recursos entre servidores.

**Selecione cada guia para obter mais informações.**

**Etapa 1**

O usuário digita um FQDN em um campo Endereço do aplicativo do navegador.![[Pasted image 20260622062327.png]]

**Etapa 2**

Uma consulta DNS é enviada para o servidor DNS designado para o computador cliente.![[Pasted image 20260622062343.png]]

**Etapa 3**

O servidor DNS corresponde ao FQDN com seu endereço IP.![[Pasted image 20260622062425.png]]

**Etapa 4**

A resposta da consulta DNS é enviada de volta ao cliente com o endereço IP do FQDN.![[Pasted image 20260622062437.png]]

**Etapa 5**

O computador cliente usa o endereço IP para fazer solicitações do servidor.![[Pasted image 20260622062448.png]]

## 25.1.3 Formato de Mensagem DNS

O servidor DNS armazena diferentes tipos de registros de recursos usados para resolver nomes. Esses registros contêm o nome, endereço e tipo de registro. Alguns desses tipos de registro são os seguintes:

- **A** – Um endereço IPv4 do dispositivo final
- **NS** – Um servidor de nomes autoritativo
- **AAAA** – Um endereço IPv6 de dispositivo final (pronuncia-se quad-A)
- **MX** – Um registro de troca de e-mail

Quando um cliente faz uma consulta, o processo DNS do servidor primeiro examina seus próprios registros para resolver o nome. Se não conseguir resolver o nome usando seus registros armazenados, ele entrará em contato com outros servidores para resolver o nome. Quando uma correspondência é encontrada e retornada ao servidor requisitante original, o servidor temporariamente armazena o número do endereço em questão, no caso do mesmo nome ser requisitado outra vez.

O serviço eficiente de DNS nos PCs com Windows também armazena nomes resolvidos anteriormente na memória. O comando `ipconfig /displaydns` exibe todas as entradas DNS em cache.

Conforme mostrado na tabela, o DNS usa o mesmo formato de mensagem entre servidores, consistindo em uma pergunta, resposta, autoridade e informações adicionais para todos os tipos de consultas de cliente e respostas de servidor, mensagens de erro e transferência de informações de registro de recursos.

|Campo|Descrição|
|---|---|
|Pergunta|A pergunta para o servidor de nomes|
|Resposta|Registros de recursos respondendo a pergunta|
|Autoridade|Registros de recursos apontando para uma autoridade|
|Crescimento do|Registros de recursos com informações adicionais|

## 25.1.4 Hierarquia DNS

O protocolo DNS usa um sistema hierárquico para criar um banco de dados para fornecer resolução de nomes, conforme mostrado na figura. O DNS usa os nomes de domínio para formar a hierarquia.

A estrutura de nomenclatura é dividida em zonas pequenas, gerenciáveis. Cada servidor DNS mantém um arquivo de banco de dados específico e só é responsável por gerenciar os mapeamentos de nome para IP para essa pequena parte da estrutura DNS. Quando um servidor DNS recebe uma requisição para a conversão de um nome que não faça parte da sua zona DNS, o servidor DNS a encaminha para outro servidor DNS na zona apropriada para a tradução. O DNS é escalável porque a resolução do nome do host está espalhada por vários servidores.

Os diferentes domínios de nível superior representam o tipo de organização ou país de origem. Exemplos de domínios de nível superior são os seguintes:

- **.com** - uma empresa ou indústria
- **.org** - uma organização sem fins lucrativos
- **.au** - Australia
- **.co** - Colombia
![[Pasted image 20260622062557.png]]

## 25.1.5 O Comando nslookup

Ao configurar um dispositivo de rede, são fornecidos um ou mais endereços de servidor DNS que o cliente DNS pode usar para resolução de nomes. Normalmente, o ISP fornece os endereços a serem usados nos servidores DNS. Quando um aplicativo de usuário solicita a conexão a um dispositivo remoto por nome, o cliente DNS solicitante consulta o servidor de nomes para resolver o nome para um endereço numérico.

Os sistemas operacionais dos computadores também têm um utilitário chamado nslookup que permite que o usuário consulte manualmente os servidores de nome para resolver um nome de host específico. Este utilitário também pode ser usado para corrigir problemas de resolução de nomes e verificar o status atual dos servidores de nomes.

Nesta figura, quando o comando **nslookup** é emitido, o servidor DNS padrão configurado para seu host é exibido. O nome de um host ou domínio pode ser inserido no prompt do **nslookup**. O utilitário nslookup tem muitas opções disponíveis para amplos testes e verificações do processo DNS.

```
C:\Users> nslookup
Default Server:  dns-sj.cisco.com
Address:  171.70.168.183
> www.cisco.com
Server:  dns-sj.cisco.com
Address:  171.70.168.183
Name:    origin-www.cisco.com
Addresses:  2001:420:1101:1::a
          173.37.145.84
Aliases:  www.cisco.com
> cisco.netacad.net
Server:  dns-sj.cisco.com
Address:  171.70.168.183
Name:  cisco.netacad.net
Address:  72.163.6.223
>
```

## 25.1.6 Verificador de Sintaxe - O Comando nslookup

Pratique entrando com o comando nslookup no Windows e Linux

```
No prompt de comando do Windows, digite o **nslookup** comando para iniciar uma consulta manual dos servidores de nomes.

C:\>nslookup

Default Server: Unknown
Address: 10.10.10.1

As saídas listam o nome e o endereço IP do servidor DNS configurado no cliente. Observe que o endereço do servidor DNS pode ser configurado manualmente ou aprendido dinamicamente através do DHCP. Você está agora no modo **nslookup**. Digite o nome de domínio www.cisco.com.

>
```


```
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

## **25.1.7 Verifique sua compreensão - Serviços DNS

**Verifique sua compreensão dos serviços DNS escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Qual dos seguintes tipos de registro DNS é usado para resolver endereços IPv6?

- [ ] A
- [ ] NS
- [x] AAAA
- [ ] MX

✅ RESPOSTA CORRETA: AAAA

> Registros DNS AAAA são usados para resolver nomes para endereços IPv6.

---

### Pergunta 2

Verdadeiro ou falso? Um servidor DNS que recebe uma solicitação para uma resolução de nome que não esteja dentro de sua zona DNS enviará uma mensagem de falha para o cliente solicitante.

- [ ] verdadeiro
- [x] falso

✅ RESPOSTA CORRETA: falso

> A resposta correta é falso. Quando um servidor DNS recebe uma solicitação de resolução de nome para um nome não dentro de sua zona, o serviço encaminhará a solicitação para outro servidor DNS.

---

### Pergunta 3

Qual dos seguintes itens é exibido pelo utilitário nslookup?

- [x] O servidor DNS padrão configurado
- [ ] O endereço IP do dispositivo final
- [ ] Todas as entradas DNS armazenadas em cache

✅ RESPOSTA CORRETA: O servidor DNS padrão configurado

> Emitindo o comando nslookup, o servidor DNS padrão configurado é exibido.

---

### Pergunta 4

Qual dos seguintes tipos de registro de recurso DNS resolve servidores de nomes autoritativos?

- [x] NS
- [ ] A
- [ ] MX
- [ ] AAAA

✅ RESPOSTA CORRETA: NS

> Os registros NS resolvem servidores de nomes autoritativos. Os registros DNS A resolvem endereços IPv4. Os registros AAAA resolvem endereços IPv6 e os registros MX resolvem servidores de troca de e-mail.


## 25.1.8 Laboratório - Observe a resolução do DNS

Nesse laboratório, você completará os seguintes objetivos:

- Parte 1: Observar a conversão DNS de uma URL para um Endereço IP
- Parte 2: Observar a Pesquisa DNS Usando o Comando **nslookup** em um Site
- Parte 3: Observar a Pesquisa DNS Usando o Comando **nslookup** em Servidores de E-mail


# 25.2 Serviços DHCP

## 25.2.1 Protocolo de Configuração Dinâmica de Host (DHCP)

O serviço DHCP para IPv4 torna automática a atribuição de endereços IPv4, máscaras de sub-rede, gateways e outros parâmetros de rede IPv4. Isso é conhecido como o endereçamento dinâmico. A alternativa para o endereçamento dinâmico é o endereçamento estático. Ao usar o endereçamento estático, o administrador de redes insere manualmente informações de endereço IP em hosts.

Quando um host está conectado à Internet, o servidor DHCP é contatado e um endereço é requisitado. O servidor DHCP escolhe um endereço de uma lista configurada de endereços chamada pool e o atribui (aloca) ao host.

Em redes maiores, ou onde a população de usuários muda frequentemente, o DHCP é preferido para atribuição de endereços. Novos usuários podem chegar e precisar de uma conexão; outros podem ter novos computadores que devem ser conectados. Em vez usar endereçamento estático para cada conexão, é mais eficiente ter endereços IPv4 atribuídos automaticamente usando o DHCP.

O DHCP pode alocar endereços IP por um período de tempo configurável, chamado período de concessão. O período de concessão é uma configuração DHCP importante, quando o período de concessão expira ou o servidor DHCP recebe uma mensagem DHCPRELEASE, o endereço é retornado ao pool DHCP para reutilização. Os usuários podem se mover livremente de um local para outro e restabelecer com facilidade conexões de rede com o DHCP.

Como a figura mostra, diversos tipos de dispositivos podem ser servidores DHCP. O servidor DHCP na maioria das redes médias a grandes normalmente é um computador PC com um servidor dedicado. Em redes residenciais, o servidor DHCP é normalmente localizado no roteador local que conecta a rede residencial ao ISP.

![[Pasted image 20260622063014.png]]Muitas redes utilizam DHCP e endereçamento estático. O DHCP é usado para hosts de uso geral, como dispositivos de usuário final. O endereçamento estático é usado para dispositivos de rede, como roteadores de gateway, comutadores, servidores e impressoras.

O DHCP para IPv6 (DHCPv6) fornece serviços semelhantes para clientes IPv6. Uma diferença importante é que o DHCPv6 não fornece o endereço do gateway padrão. Isso só pode ser obtido dinamicamente a partir da mensagem Anúncio do roteador do roteador.

## 25.2.2 Vídeo - Operação do DHCP em um roteador doméstico
![[25.2.2.mp4#subtitle=anexos/25.2.2.vtt]]
DHCP, ou Protocolo de Configuração Dinâmica de Host, é um serviço que permite que os dispositivos recebam automaticamente seu endereço IP e outras informações de endereçamento de um servidor DHCP. O DHCP está disponível para IPv4 e IPv6. Há algumas diferenças entre os dois, no entanto, o resultado final é muito semelhante. Neste vídeo, vamos nos concentrar no DHCP para IPv4, usando um roteador doméstico típico como servidor DHCP.

Em nossa topologia, vocês podem ver que nosso roteador doméstico tem o endereço IPv4 `192.168.1.1`, e também foi habilitado como um servidor DHCP. Em vez de uma única porta para conectar nossos dispositivos locais, a maioria dos roteadores domésticos inclui um switch Ethernet integrado. Dispositivos cliente, como PC 1 e PC 2, receberão normalmente as informações de endereçamento IPv4 de um servidor DHCP. O PC 2 já recebeu suas informações de endereçamento usando o DHCP.

Ao atribuir automaticamente as informações de endereçamento, o DHCP elimina possíveis problemas devido a erros de configuração manual. No entanto, alguns dispositivos, como uma impressora ou um servidor, provavelmente terão suas informações de endereçamento IPv4 configuradas manualmente. Isso é para garantir que esses dispositivos tenham um endereço IPv4 específico.

Um servidor DHCP pode ser um computador separado, mas, na maioria das redes domésticas, o roteador doméstico local atuará como um servidor DHCP. No nosso cenário, usaremos o roteador doméstico como nosso servidor DHCP. O roteador doméstico foi configurado como um servidor DHCP para fornecer informações de endereçamento para os clientes, inclusive o pool ou o escopo dos endereços IPv4 — normalmente endereços IPv4 privados. Cada cliente DHCP receberá um endereço IPv4 exclusivo desse pool.

O servidor DHCP controla qual dispositivo recebe qual endereço IPv4, ao associar o endereço IPv4 atribuído ao endereço MAC Ethernet do cliente. Os endereços do gateway padrão, máscara de sub-rede e o servidor DNS também são distribuídos e serão as mesmas informações para todos os clientes.

Como a maioria dos dispositivos clientes, o PC 1 é habilitado por padrão para obter seu endereço IPv4 automaticamente usando DHCP. O cliente enviará um broadcast Ethernet solicitando informações de endereçamento IPv4 de um servidor DHCP. Após uma breve sequência de mensagens entre o cliente e o servidor DHCP, o servidor atribuirá ao cliente um dos endereços IPv4 disponíveis do pool, junto com a máscara de sub-rede apropriada, endereço de gateway padrão e endereço do servidor DNS. O PC 1 agora tem suas informações de endereçamento IPv4.

Já que o cliente PC 2 já tem o primeiro endereço do pool, o servidor DHCP atribuirá o próximo endereço disponível, `192.168.1.100`. Note que o endereço do gateway padrão é o endereço do roteador doméstico. O cliente agora tem todas as informações de endereçamento de que precisa para se comunicar corretamente com os dispositivos em sua própria rede, bem como outros dispositivos, inclusive a Internet.

Aliás, geralmente é assim que um roteador doméstico recebe informações de endereçamento IPv4 pela interface WAN, a interface que é usada para se conectar ao ISP. Quando o roteador doméstico está ligado, ele atua como um cliente DHCP e recebe seu endereço IPv4 público e outras informações de endereçamento de um servidor DHCP do ISP — assim como vimos com nossos PCs clientes.

## 25.2.3 Mensagens DHCP

Como mostra a figura, quando um dispositivo IPv4 configurado com DHCP inicia ou se conecta à rede, o cliente transmite uma mensagem de descoberta DHCP (DHCPDISCOVER) para identificar qualquer servidor DHCP disponível na rede. Um servidor DHCP responde com uma mensagem de oferta DHCP (DHCPOFFER), que oferece uma locação ao cliente. A mensagem de oferta contém o endereço IPv4 e a máscara de sub-rede a serem atribuídos, o endereço IPv4 do servidor DNS e o endereço IPv4 do gateway padrão. A oferta de locação também inclui a duração da locação.

![[Pasted image 20260622063140.png]]

O cliente pode receber várias mensagens DHCPOFFER, caso exista mais de um servidor DHCP na rede local. Portanto, deve escolher entre eles e transmitir uma mensagem de requisição de DHCP (DHCPREQUEST) que identifique o servidor explícito e a oferta de locação que o cliente está aceitando. Um cliente também pode decidir requisitar um endereço que já havia sido alocado pelo servidor.

Presumindo que o endereço IPv4 requisitado pelo cliente, ou oferecido pelo servidor, ainda seja válido, o servidor retornará uma mensagem de confirmação DHCP (DHCPACK) que confirma para o cliente que a locação foi finalizada. Se a oferta não é mais válida, o servidor selecionado responde com uma mensagem de confirmação negativa DHCP (DHCPNAK). Se uma mensagem DHCPNAK for retornada, o processo de seleção deverá recomeçar com a transmissão de uma nova mensagem DHCPDISCOVER. Quando o cliente tiver a locação, ela deverá ser renovada por outra mensagem DHCPREQUEST antes do vencimento.

O servidor DHCP garante que todos os endereços IP sejam exclusivos (um mesmo endereço IP não pode ser atribuído a dois dispositivos de rede diferentes simultaneamente). A maioria dos ISPs usa o DHCP para alocar endereços para seus clientes.

O DHCPv6 possui um conjunto de mensagens semelhantes às do DHCPv4. As mensagens DHCPv6 são SOLICIT, ADVERTISE, INFORMATION REQUEST, e REPLY.


## 25.2.4 Verifique sua compreensão - Serviços DHCP



### Pergunta 1

Verdadeiro ou falso? Os clientes DHCP iniciam o processo DHCP enviando uma mensagem DHCPREQUEST aos servidores DHCP disponíveis.

- [ ] verdadeiro
- [x] falso

✅ RESPOSTA CORRETA: falso

> A resposta correta é falso. Há quatro mensagens DHCP trocadas entre clientes e servidores. O cliente inicia o processo DHCP com uma mensagem de descoberta DHCP para servidores DHCP disponíveis.

---

### Pergunta 2

Qual das opções a seguir melhor descreve o DHCP?

- [ ] O DHCP automatiza o processo de descoberta do endereço MAC do destino.
- [ ] O DHCP automatiza o processo para descobrir o endereço IP de um nome de domínio.
- [x] O DHCP automatiza a atribuição de endereços IP, máscaras de sub-rede, gateways e outros parâmetros de rede IPv4.
- [ ] O DHCP automatiza a conversão de endereços IP privados e públicos.

✅ RESPOSTA CORRETA: O DHCP automatiza a atribuição de endereços IP, máscaras de sub-rede, gateways e outros parâmetros de rede IPv4.

> O DHCP automatiza a atribuição de endereços IP, máscaras de sub-rede, gateways e outros parâmetros de rede IPv4. O ARP automatiza o processo para descobrir o endereço MAC do destino. O DNS automatiza o processo de descoberta do endereço IP de um nome de domínio. O NAT automatiza a tradução de endereços IP privados e públicos.

---

### Pergunta 3

Qual é a ordem correta das mensagens na operação DHCP?

- [ ] DHCPDISCOVER, DHCPOFFER, DHCPNAK, DHCPREQUEST
- [x] DHCPREQUEST, DHCPOFFER, DHCPDISCOVER, DHCPACK
- [ ] DHCPREQUEST, DHCPOFFER, DHCPDISCOVER, DHCPACK
- [ ] DHCPREQUEST, DHCPOFFER, DHCPDISCOVER, DHCPACK

✅ RESPOSTA CORRETA: DHCPDISCOVER, DHCPOFFER, DHCPREQUEST, DHCPACK

> A ordem correta das mensagens para a operação DHCP é DHCPDISCOVER, DHCPOFFER, DHCPREQUEST, DHCPACK.



# 25.3 Resumo dos serviços de endereçamento IP

## 25.3.1 O que aprendi neste módulo?

### Serviços de endereçamento IP

Em redes de dados, os dispositivos são rotulados com endereços IP numéricos para enviar e receber dados pelas redes. Os nomes de domínio foram criados para converter o endereço numérico em um nome simples e reconhecível. O protocolo DNS define um serviço automatizado que compara nomes de recursos com o endereço de rede numérico requisitado. As comunicações do protocolo DNS utilizam um único formato, chamado de mensagem. Este formato de mensagem é utilizado para todos os tipos de consultas de cliente e respostas de servidor, mensagens de erro e transferência de informações de registro de recursos entre servidores.

O servidor DNS armazena diferentes tipos de registros de recursos usados para resolver nomes. Esses registros contêm o nome, endereço e tipo de registro. O DNS usa o mesmo formato de mensagem entre servidores, consistindo em uma pergunta, resposta, autoridade e informações adicionais para todos os tipos de consultas de clientes e respostas de servidores, mensagens de erro e transferência de informações de registros de recursos.

O DNS usa os nomes de domínio para formar a hierarquia. A estrutura de nomenclatura é dividida em zonas. Cada servidor DNS mantém um arquivo de banco de dados específico e só é responsável por gerenciar os mapeamentos de nome para IP para essa pequena parte da estrutura DNS. Quando um servidor DNS recebe uma requisição para a conversão de um nome que não faça parte da sua zona DNS, o servidor DNS a encaminha para outro servidor DNS na zona apropriada para a tradução. O DNS é escalável porque a resolução do nome do host está espalhada por vários servidores.

Os sistemas operacionais de computador têm um utilitário chamado Nslookup que permite ao usuário consultar manualmente os servidores de nomes usado para resolver um determinado nome de host. Este utilitário também pode ser usado para corrigir problemas de resolução de nomes e verificar o status atual dos servidores de nomes. Quando o comando `nslookup` é emitido, o servidor DNS padrão configurado para seu host é exibido. O nome de um host ou domínio pode ser inserido no prompt do nslookup.

Em redes maiores, o DHCP é preferido para atribuição de endereço. Em vez de usar endereçamento estático para cada conexão, é mais eficiente ter endereços IPv4 atribuídos automaticamente usando o DHCP. O DHCP pode alocar endereços IP por um período de tempo configurável, chamado período de concessão. Quando o período de concessão expira ou o servidor DHCP recebe uma mensagem DHCPRELEASE, o endereço é devolvido ao pool DHCP para reutilização. Os usuários podem se mover livremente de um local para outro e restabelecer com facilidade conexões de rede com o DHCP.

O DHCPv6 fornece serviços semelhantes para clientes IPv6. Uma diferença importante é que o DHCPv6 não fornece o endereço do gateway padrão. Isso só pode ser obtido dinamicamente a partir da mensagem Anúncio do roteador do roteador.

Quando um dispositivo configurado para DHCP IPv4 é inicializado ou conectado à rede, o cliente transmite uma mensagem DHCPDISCOVER para identificar quaisquer servidores DHCP disponíveis na rede.

Um servidor DHCP responde com uma mensagem DHCPOFFER, que oferece uma concessão ao cliente. O cliente envia uma mensagem DHCPREQUEST que identifica o servidor explícito e a oferta de aluguel que o cliente está aceitando.

Supondo que o endereço IPv4 solicitado pelo cliente ou oferecido pelo servidor ainda esteja disponível, o servidor retorna uma mensagem DHCPACK que reconhece ao cliente que a concessão foi finalizada. Se a oferta não for mais válida, o servidor selecionado responde com uma mensagem DHCPNAK. Se uma mensagem DHCPNAK for retornada, o processo de seleção deverá recomeçar com a transmissão de uma nova mensagem DHCPDISCOVER.

O DHCPv6 possui um conjunto de mensagens semelhantes às do DHCPv4. As mensagens DHCPv6 são SOLICIT, ADVERTISE, INFORMATION REQUEST, e REPLY.

## 25.3.2 Webster - Questões para Reflexão

Mais um módulo pronto! O que você aprendeu neste módulo sobre serviços de endereçamento IP? Antes de fazer este módulo, você pensou no protocolo DNS definindo um serviço automatizado que correspondesse aos nomes dos recursos com o endereço de rede numérico necessário? Você sabia a diferença entre o endereçamento estático e o DHCP? Eu realmente aprendi muito e espero que você também!