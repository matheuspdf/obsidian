# 33.0 Introdução

## 33.0.1 Webster - Por que devo fazer este módulo?

Oi, é Webster novamente! Bem, esse último módulo contém muitas informações novas para mim. E agora há um novo tipo de endereço IP - IPv6! Mas estou confiante de que posso aprender isso.

Halimah sabe muito sobre endereçamento IPv6 e está feliz em ver que ele está incorporado de forma estratégica à rede da empresa. Isso ajudará a rede da empresa a continuar crescendo e mudando.

Aqui está sua chance de atualizar o IPv6 também!

## 33.0.2 O que vou aprender neste módulo?

**Título do Módulo:** Endereçamento IPv6

**Objetivo do Módulo:** Implementar um esquema de endereçamento IPv6.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Tipos de Endereço IPv6|Comparar os tipos de endereços de rede IPv6.|
|Configuração Estática do GUA e do LLA|Explique como configurar endereços de rede IPv6 globais estáticos e unicast.|
|Endereçamento dinâmico para GUAs IPv6|Explicar como configurar endereços unicast globais de forma dinâmica.|
|Endereçamento Dinâmico para LLAs IPv6|Explicar como configurar endereços unicast locais de forma Dinâmica.|
|Endereços IPv6 Multicast|Identificando Endereços IPv6.|

# 33.1 Tipos de Endereço IPv6
## 33.1.1 Unicast, Multicast, Anycast

Tal como acontece com o IPv4, existem diferentes tipos de endereços IPv6. Na verdade, existem três grandes categorias de endereços IPv6:

- **Unicast** – Um endereço IPv6 unicast identifica exclusivamente uma interface em um dispositivo habilitado para IPv6.
- **Multicast** – Um endereço IPv6 multicast é usado para enviar um único pacote IPv6 para vários destinos.
- **Anycast** – Um endereço IPv6 anycast é qualquer endereço IPv6 unicast que possa ser atribuído a vários dispositivos. Um pacote enviado a um endereço de anycast é roteado para o dispositivo mais próximo que tenha esse endereço. Os endereços anycast estão fora do escopo deste curso.

Ao contrário do IPv4, o IPv6 não possui um endereço de broadcast. No entanto, há um endereço multicast para todos os nós IPv6 que fornece basicamente o mesmo resultado.

## 33.1.2 Comprimento do prefixo IPv6

Lembre-se de que o prefixo (a parte de rede) de um endereço IPv4 pode ser identificado pelo comprimento do prefixo (notação em barra) ou por uma máscara de sub-rede decimal com pontos. Por exemplo, o endereço IPv4 192.168.1.10 com máscara de sub-rede decimal com pontos 255.255.255.0 é equivalente a 192.168.1.10/24.

No IPv6 é chamado de comprimento do prefixo. O IPv6 não usa a notação decimal com pontos da máscara de sub-rede. Como o IPv4, o comprimento do prefixo é representado na notação de barra e é usado para indicar a parte da rede de um endereço IPv6.

O comprimento do prefixo pode variar de 0 a 128. O comprimento do prefixo IPv6 recomendado para LANs e a maioria dos outros tipos de redes é /64, conforme mostrado na figura.

### Comprimento do Prefixo IPv6

![[Pasted image 20260630205951.png]]Isso significa que o prefixo ou a parte de rede do endereço é de 64 bits, restando outros 64 bits para a ID da interface (parte de host) do endereço.

É altamente recomendável usar um ID de interface de 64 bits para a maioria das redes. Isso ocorre porque a configuração automática de endereço sem estado (SLAAC) usa 64 bits para o ID de interface. Também facilita a criação e o gerenciamento de sub-redes.

## 33.1.3 Tipos de Endereços IPv6 Unicast

Um endereço IPv6 unicast identifica exclusivamente uma interface em um dispositivo habilitado para IPv6. Um pacote enviado a um endereço unicast é recebido pela interface à qual foi atribuído esse endereço. Semelhante ao IPv4, o endereço IPv6 origem deve ser um endereço unicast. O endereço IPv6 destino pode ser um endereço unicast ou multicast. A figura mostra os diferentes tipos de endereços unicast IPv6.

### Endereços IPv6 unicast

![[Pasted image 20260630210006.png]]

Ao contrário dos dispositivos IPv4 que têm apenas um único endereço, os endereços IPv6 normalmente têm dois endereços unicast:

- **Um endereço unicast global(GUA)** - E semelhante a um endereço IPv4 público. São endereços de Internet roteáveis e globalmente exclusivos. GUAs podem ser configurados estaticamente ou dinamicamente distribuídos
- **Endereço de Link-Local (LLA)** - Isso é necessário para cada dispositivo habilitado para IPv6. Os LLAs são usados para se comunicar com outros dispositivos no mesmo link local. No IPv6, o termo link se refere a uma sub-rede. LLAs são limitados a um único enlace. Sua exclusividade só deve ser confirmada nesse link, porque eles não são roteáveis além do link. Em outras palavras, os roteadores não encaminham pacotes com um endereço de link local origem ou destino.


## 33.1.4 Uma observação sobre o endereço local exclusivo

Endereços locais exclusivos (intervalo fc00::/7 a fdff::/7) ainda não são comumente implementados. Portanto, este módulo abrange apenas a configuração GUA e LLA. No entanto, endereços locais exclusivos podem eventualmente ser usados para endereçar dispositivos que não devem ser acessíveis de fora, como servidores internos e impressoras.

Os endereços IPv6 unique local têm alguma semelhança com endereços privados do RFC 1918 para o IPv4, mas há diferenças significativas:

- Os endereços unique local são utilizados para endereçamento local dentro de um site ou entre um número limitado de sites.
- Os endereços unique local podem ser usados para dispositivos que nunca precisarão ou terão acesso por outra rede.
- Endereços locais exclusivos não são globalmente roteados ou traduzidos para um endereço IPv6 global.

**Nota**: Muitos sites usam a natureza privada dos endereços RFC 1918 para tentar proteger ou ocultar sua rede de possíveis riscos à segurança. No entanto, essa nunca foi a finalidade dessas tecnologias. A IETF sempre recomendou que os sites tomassem as devidas precauções de segurança em seu roteador de Internet.

## 33.1.5 IPv6 GUA

O endereço IPv6 unicast global (GUA) é globalmente exclusivo e roteável na Internet IPv6. Esses endereços são equivalentes aos endereços públicos do IPv4. O Internet Committee for Assigned Names and Numbers (ICANN), o operador de Internet Assigned Numbers Authority (IANA), aloca os blocos de endereço IPv6 para os cinco RIRs. No momento, somente endereços unicast globais com os primeiros três bits de 001 ou 2000::/3 estão sendo atribuídos

A figura mostra o intervalo de valores para o primeiro hextet onde o primeiro dígito hexadecimal para GUAs atualmente disponíveis começa com um 2 ou um 3. Isso é apenas um oitavo do espaço de endereço IPv6 total disponível, excluindo uma parte muito pequena de outros tipos de endereços unicast e multicast.

**Nota**: O endereço 2001:0DB8::/32 foi reservado para fins de documentação, incluindo uso nos exemplos.

![[Pasted image 20260630210052.png]]

A figura seguinte mostra a estrutura e o alcance de um GUA.

### Endereço IPv6 com prefixo de roteamento global /48 e prefixo /64

![[Pasted image 20260630210103.png]]

Um GUA tem três partes:

- Prefixo global de roteamento
- ID da Sub-Rede
- ID da interface


## 33.1.6 Estrutura IPv6 GUA

**Prefixo Global de Roteamento**

O prefixo global de roteamento é o prefixo (parte de rede) do endereço que é atribuído pelo provedor (como um ISP) a um cliente ou um site. Por exemplo, é comum que os ISPs atribuam um prefixo de roteamento global /48 a seus clientes. O prefixo de roteamento global geralmente varia dependendo das políticas do ISP.

A figura anterior mostra um GUA usando um prefixo de roteamento global /48. Os prefixos /48 são os prefixos de roteamento global mais comuns atribuídos e serão usados na maioria dos casos ao longo deste curso.

Por exemplo, o endereço IPv6 2001:db8:acad::/ 48 possui um prefixo de roteamento global que indica que os primeiros 48 bits (3 hextets) (2001:db8:acad) são como o ISP conhece esse prefixo (rede). Dois-pontos duplo (::) antes do comprimento de prefixo /48 significa que o restante do endereço contém apenas 0s. O tamanho do prefixo de roteamento global determina o tamanho da ID da sub-rede.

**ID da Sub-Rede**

O campo ID da sub-rede é a área entre o Prefixo de Roteamento Global e o ID da interface. Ao contrário do IPv4, onde você deve pedir bits emprestados da parte do host para criar sub-redes, o IPv6 foi projetado tendo em mente a sub-rede. O ID da sub-rede é usado por uma organização para identificar sub-redes dentro da sua localização. Quanto maior a ID da sub-rede, mais sub-redes disponíveis.

**Nota**: Muitas organizações estão recebendo um prefixo de roteamento global /32. Usando o prefixo /64 recomendado para criar um ID de interface de 64 bits, deixa um ID de sub-rede de 32 bits. Isso significa que uma organização com um prefixo de roteamento global /32 e um ID de sub-rede de 32 bits terá 4,3 bilhões de sub-redes, cada uma com 18 quintilhões de dispositivos por sub-rede. Isso equivale a tantas sub-redes quantos endereços IPv4 públicos

O endereço IPv6 na figura anterior tem um prefixo de roteamento global /48, que é comum entre muitas redes corporativas. Isso torna especialmente fácil examinar as diferentes partes do endereço. Usando um tamanho típico de prefixo / 64, os quatro primeiros hextetos são para a parte da rede do endereço, com o quarto hexteto indicando o ID da sub-rede. Os quatro hextets restantes são para o ID da interface.

**ID da interface**

A ID da interface IPv6 equivale à parte de host de um endereço IPv4. O termo ID da interface é usado porque um único host pode ter várias interfaces, cada uma com um ou mais endereços IPv6. A figura mostra um exemplo da estrutura de um GUA IPv6. É altamente recomendável que as sub-redes /64 sejam usadas na maioria dos casos. Um ID de interface de 64 bits permite 18 quintilhões de dispositivos ou hosts por sub-rede.

Uma sub-rede /64 ou prefixo (Global Routing Prefix + Subnet ID) deixa 64 bits para o ID da interface. Isso é recomendado para permitir que dispositivos habilitados para SLAAC criem seu próprio ID de interface de 64 bits. Também torna o desenvolvimento de um plano de endereçamento IPv6 simples e eficaz.

**Nota**: Ao contrário do IPv4, no IPv6, todos os endereços de host de all-0s e de all-1s podem ser atribuídos a um dispositivo. O endereço todos-1s pode ser usado porque os endereços de broadcast não são usados dentro do IPv6. O endereço de all-0s também pode ser usado, mas é reservado como endereço de anycast de subnet-router, e deve ser atribuído somente aos roteadores.

## 33.1.7 LLA IPv6

Comunicações IPv6 de Link Local

Um endereço IPv6 de link-local permite que um dispositivo se comunique com outros dispositivos habilitados para IPv6 no mesmo link e somente nesse link (sub-rede). Os pacotes com endereço de link local origem ou destino não podem ser roteados além do link de onde o pacote foi originado.

O GUA não é um requisito. No entanto, cada interface de rede habilitada para IPv6 deve ter um LLA.

Se um LLA não estiver configurado manualmente em uma interface, o dispositivo criará automaticamente um próprio, sem se comunicar com um servidor DHCP. Os hosts habilitados para LLA IPv6 criarão um endereço IPv6 mesmo que não tenha sido atribuído um endereço IPv6 unicast global ao dispositivo. Isso permite que dispositivos habilitados para IPv6 se comuniquem com outros dispositivos semelhantes na mesma sub-rede. Isso inclui a comunicação com o gateway padrão (roteador).

Os LLAs IPv6 estão no intervalo fe80: :/10. O /10 Indica que os primeiros 10 bits são 1111 1110 10xx xxxx. O primeiro hextet tem um intervalo de 1111 1110 10 **00 0000** (FE80) a 1111 1110 10 **11 1111** (FEBF).

A Figura mostra um exemplo de comunicação usando endereços LLA IPv6. O PC é capaz de se comunicar diretamente com a impressora usando os LLAs.

### Comunicações IPv6 de Link Local

![[Pasted image 20260630210142.png]]

A figura seguinte mostra alguns dos usos para LLAs IPv6 .

![[Pasted image 20260630210204.png]]

## 33.1.8 Verifique sua compreensão - Tipos de endereços IPv6

**Verifique sua compreensão dos tipos de endereços IPv6 escolhendo a melhor resposta para as seguintes perguntas.**

### Pergunta 1

Qual é o comprimento do prefixo recomendado para a maioria das sub-redes IPv6?

- [x] /64
- [ ] /48
- [ ] /128
- [ ] /32

✅ RESPOSTA CORRETA: /64

> A maioria das sub-redes IPv6 terá um comprimento de prefixo de /64.

---

### Pergunta 2

Qual parte de um GUA é atribuída pelo ISP?

- [x] Prefixo de roteamento global
- [ ] Prefixo de roteamento global e ID de sub-rede
- [ ] Prefixo RIR
- [ ] Prefixo

✅ RESPOSTA CORRETA: Prefixo de roteamento global

> O prefixo de roteamento global é a parte de um GUA atribuída por um ISP.

---

### Pergunta 3

Que tipo de endereço unicast IPv6 não é roteável entre redes?

- [ ] Endereço IPv4 incorporado
- [ ] GUA
- [ ] Endereço local exclusivo
- [x] LLA

✅ RESPOSTA CORRETA: LLA

> Endereços IPv6 de link local são apenas para comunicação de link e não são roteáveis.

---

### Pergunta 4

Verdadeiro ou falso? O campo ID de sub-rede em um GUA deve usar bits emprestados do ID da interface.

- [ ] Verdadeiro
- [x] Falso

✅ RESPOSTA CORRETA: Falso

> GUAs não usam um bit do ID da interface para criar sub-redes.

---

### Pergunta 5

Que tipo de endereço IPv6 começa com fe80?

- [x] LLA
- [ ] Endereço de multicast
- [ ] GUA
- [ ] Nenhum. Um endereço IPv6 deve começar com 2001

✅ RESPOSTA CORRETA: LLA

> Endereços IPv6 de link local começam com o prefixo fe80.


# 33.2 Configuração Estática do GUA e do LLA

## 33.2.1 Configuração de GUA Estático em um Roteador

Como você aprendeu no tópico anterior, as GUAs IPv6 são iguais aos endereços IPv4 públicos. O endereço IPv6 unicast global (GUA) é globalmente exclusivo e roteável na Internet IPv6. Um LLA IPv6 permite que dois dispositivos habilitados para IPv6 se comuniquem uns com os outros no mesmo link (sub-rede). É fácil configurar estaticamente GUAs e LLAs IPv6 em roteadores para ajudá-lo a criar uma rede IPv6. Este tópico ensina como fazer exatamente isso!

A maioria dos comandos de configuração e verificação do IPv6 no Cisco IOS são semelhantes aos seus equivalentes no IPv4. Em muitos casos a única diferença é o uso do **ipv6** em vez do**ip** dentro dos comandos.

Por exemplo, o comando Cisco IOS para configurar um endereço IPv4 em uma interface é **ip address** _endereço-IP máscara-de-subrede._ Em contraste, o comando para configurar um GUA IPv6 em uma interface é **ipv6 address** _endereço-ipv6/comprimento do prefixo._

Observe que não um espaço entre _ipv6-address_ e _prefix-length ._

O exemplo de configuração usa a topologia mostrada na Figura e as seguintes sub-redes IPv6:

- 2001:db8:acad:1::/64
- 2001:db8:acad:2::/64
- 2001:db8:acad:3። /64

### Exemplo de Topologia

![[Pasted image 20260630212248.png]]

O exemplo mostra os comandos necessários para configurar o IPv6 GUA no GigabitEthernet 0/0/0, GigabitEthernet 0/0/1 e na interface Serial 0/1/0 do R1.

### Configuração IPv6 GUA no Roteador R1

```
R1(config)# interface gigabitethernet 0/0/0
R1(config-if)# ipv6 address 2001:db8:acad:1::1/64
R1(config-if)# no shutdown
R1(config-if)# exit
R1(config)# interface gigabitethernet 0/0/1
R1(config-if)# ipv6 address 2001:db8:acad:2::1/64
R1(config-if)# no shutdown
R1(config-if)# exit
R1(config)# interface serial 0/1/0
R1(config-if)# ipv6 address 2001:db8:acad:3::1/64
R1(config-if)# no shutdown
```


## 33.2.2 Configuração de GUA Estático em um Host Windows

Configurar manualmente o endereço IPv6 em um host é semelhante a configurar um endereço IPv4.

Conforme mostrado na figura, o endereço de gateway padrão configurado para PC1 é 2001:db8:acad: 1::1. Essa é a GUA da interface R1 GigabitEthernet na mesma rede. Como alternativa, o endereço de gateway padrão pode ser configurado para corresponder ao endereço LLA da interface Gigabit Ethernet. O uso do LLA do roteador como endereço de gateway padrão é considerado prática recomendada. Qualquer uma das configurações funcionará.

![[Pasted image 20260630212313.png]]

Assim como ocorre no IPv4, a configuração de endereços estáticos em clientes não escala para ambientes maiores. Por esse motivo, a maioria dos administradores de redes IPv6 permite a atribuição dinâmica de endereços IPv6.

Há duas maneiras de um dispositivo obter um endereço IPv6 unicast global automaticamente:

- Configuração automática do endereço sem estado (SLAAC)
- DHCPv6 com estado

O SLAAC e o DHCPv6 são abordados no tópico seguinte.

**Nota**: Quando DHCPv6 ou SLAAC é usado, o LLA do roteador será especificado automaticamente como o endereço de gateway padrão.

## 33.2.3 Configuração estática de um endereço unicast de link-local

A configuração manual do LLA permite criar um endereço reconhecível e fácil de lembrar. Geralmente, só é necessário criar endereços de link local reconhecíveis nos roteadores. Isso é benéfico porque os LLAs do roteador são usados como endereços de gateway padrão e no roteamento de mensagens de anúncio.

Os LLAS podem ser configurados manualmente usando o comando **ipv6 address** _endereço-de-link-local-ipv6_ **link-local** . Quando um endereço começa com esse hextet dentro do intervalo de fe80 a febf, o parâmetro **link-local** deve seguir o endereço.

A figura mostra um exemplo de topologia com LLAs em cada interface.

### Exemplo de Topologia com LLAs

![[Pasted image 20260630212331.png]]

O exemplo mostra a configuração de um LLA no roteador R1.

```
R1(config)# interface gigabitethernet 0/0/0
R1(config-if)# ipv6 address fe80::1:1 link-local
R1(config-if)# exit
R1(config)# interface gigabitethernet 0/0/1
R1(config-if)# ipv6 address fe80::2:1 link-local
R1(config-if)# exit
R1(config)# interface serial 0/1/0
R1(config-if)# ipv6 address fe80::3:1 link-local
R1(config-if)# exit
```

Os LLAs configurados estaticamente são usados para torná-los mais facilmente reconhecíveis como pertencentes ao roteador R1. Neste exemplo, todas as interfaces do roteador R1 foram configuradas com um LLA que começa com **fe80::_n_::1**

**Nota**: O mesmo LLA pode ser configurado em cada link, desde que seja exclusivo nesse link. Isso é possível porque as interfaces de link local só precisam ser exclusivas nesse link. No entanto, a prática comum é criar um LLA diferente em cada interface do roteador para facilitar a identificação do roteador e da interface específica.

## 33.2.4 Verificador de Sintaxe - Configuração Estática GUA e LLA

Atribua GUAs e LLAs IPv6 às interfaces especificadas no roteador R1.

![[Pasted image 20260630212410.png]]

```
Configure e ative o IPv6 na interface Gigabit Ethernet 0/0/0 com os seguintes endereços:

* Use g0/0/0 como o nome da interface * LLA - fe80::1:1 * GUA - 2001:db8:acad:1::1/64 * Ative a interface * Saia do modo de configuração de interface.

R1(config)#interface g0/0/0
R1(config-if)#ipv6 address fe80::1:1 link-local
R1(config-if)#ipv6 address 2001:db8:acad:1::1/64
R1(config-if)#no shutdown
%LINK-3-UPDOWN: Interface GigabitEthernet0/0/0, changed state to up
R1(config-if)#exit
Configure e ative o IPv6 na interface Gigabit Ethernet 0/0/1 com os seguintes endereços:

* Use g0/0/1 como o nome da interface * LLA - fe80::2:1 * GUA - 2001:db8:acad:2: :1/64 * Ative a interface * Saia do modo de configuração de interface.

R1(config)#interface g0/0/1
R1(config-if)#ipv6 address fe80::2:1 link-local
R1(config-if)#ipv6 address 2001:db8:acad:2::1/64
R1(config-if)#no shutdown
%LINK-3-UPDOWN: Interface GigabitEthernet0/0/1, changed state to up
R1(config-if)#exit
Configure e ative o IPv6 na interface serial 0/1/0 com os seguintes endereços:

* Use s0/1/0 como o nome da interface * GUA - 2001:db8:acad:3::1/64 * LLA - fe80::1:3 * Ative a interface * Saia do modo de configuração de interface.

R1(config)#interface s0/1/0
R1(config-if)#ipv6 address fe80::3:1 link-local
R1(config-if)#ipv6 address 2001:db8:acad:3::1/64
R1(config-if)#no shutdown
%LINK-3-UPDOWN: Interface Serial0/1/0, changed state to up
R1(config-if)#exit
R1(config)#
Você configurou com êxito as GUAs IPv6 nas interfaces do roteador R1.
```

# 33.3 Endereçamento dinâmico para GUAs IPv6

## 33.3.1 Vídeo - Mensagens RS e RA

![[33.3.1.mp4#subtitle=anexos/33.3.1.vtt]]

Para entender melhor o endereçamento dinâmico para IPv6, vamos dar uma olhada no DHCP para IPv4.

PC1 e PC2 receberam informações de endereçamento IPv4 de um servidor DHCP. A maioria dessas informações, inclusive a máscara de sub-rede, o endereço de gateway padrão e o endereço do servidor DNS não são exclusivos e é a mesma informação enviada a todos os clientes. Esta informação é considerada stateless. Isso significa que um servidor DHCP não está mantendo o estado ou guardando um registro de quem recebe essas informações.

Entretanto, os endereços IPv4 de cada dispositivo são atribuídos a partir de um pool, com cada dispositivo obtendo um endereço IPv4 exclusivo. Essas informações são consideradas stateful. O servidor DHCP está mantendo o estado, está mantendo um registro de qual dispositivo recebe qual endereço IPv4. No caso de DHCP para IPv4, o servidor mantém um registro de qual dispositivo que recebeu o endereço, com base no endereço Ethernet MAC do cliente. Observe que, embora cada endereço IPv4 seja exclusivo, a parte de rede dos endereços é a mesma. É apenas a parte do host que torna cada endereço único.

O endereçamento dinâmico com IPv6 usa uma mensagem ICMPv6 de anúncio de roteador (RA) que informa aos clientes como obter dinamicamente as informações de endereçamento IPv6. Um roteador IPv6 envia mensagens de anúncio de roteador a cada 200 segundos. Uma mensagem RA também pode ser enviada sempre que o roteador recebe uma mensagem de solicitação do roteador (RS) de um dispositivo.

Vamos dar uma olhada na mensagem de RA. Uma mensagem de anúncio do roteador é enviada para todos os dispositivos IPv6 pelo endereço multicast ff02::1. O endereço de origem é o endereço local do link do roteador. A mensagem RA inclui o prefixo de rede e o comprimento do prefixo — esse é o mesmo prefixo de rede do endereço unicast global do roteador nesta interface — um endereço de servidor DNS e um ou mais flags de configuração ativados.

Ambos PC1 e PC2 receberam a mensagem RA. O prefixo da rede e o comprimento do prefixo indicam o endereço de rede. Os dispositivos também usam o endereço local do link do roteador como seus endereços de gateway padrão. O endereço de um ou mais servidores DNS é normalmente incluído na mensagem RA.

Neste exemplo, a mensagem RA tem apenas o flag A ativado. Isso significa que nossos dispositivos usarão SLAAC — Stateless Address Autoconfiguration — para seus endereços IPv6 unicast global. Cada dispositivo usa o prefixo de rede recebido e cria aleatoriamente sua própria ID de interface, que é a parte do host do endereço. A ID de interface está indicada em vermelho. PC2 faz o mesmo.

Observe que todas as informações de endereço obtidas pelo PC1 e PC2 são stateless. Não há servidor algum controlando qual dispositivo recebeu qual endereço. Nesse caso, significando que um servidor DHCP stateful não é obrigatório.


## 33.3.2 Mensagens RS e RA

Se você não quiser configurar as GUAs IPv6 estaticamente, não precisa se preocupar. A maioria dos dispositivos obtém suas GUAs IPv6 dinamicamente. Este tópico explica como esse processo funciona usando mensagens de anúncio de roteador (RA) e solicitação de roteador (RS). Este tópico fica bastante técnico, mas quando você entende a diferença entre os três métodos que um anúncio de roteador pode usar, bem como o processo EUI-64 para criar um ID de interface difere de um processo gerado aleatoriamente, você terá dado um grande salto em sua experiência IPv6!

Para o GUA, um dispositivo obtém o endereço dinamicamente através de mensagens ICMPv6 (Internet Control Message Protocol versão 6). Os roteadores IPv6 enviam mensagens ICMPv6 de RA a cada 200 segundos para todos os dispositivos habilitados para IPv6 na rede. Uma mensagem de RA também é enviada em resposta a um host que envie uma mensagem ICMPv6 de RS (Solicitação de Roteador). Ambas as mensagens são mostradas na figura.

### Mensagens ICMPv6 RS e RA

![[Pasted image 20260630212551.png]]

As mensagens de RA estão em interfaces Ethernet de roteador IPv6. O roteador deve estar habilitado para roteamento IPv6, que não vem habilitado por padrão. Para habilitar um roteador como um roteador IPv6, o comando deconfiguração global **ipv6 unicast-routing** deve ser usado.

A mensagem ICMPv6 de RA é uma sugestão para um dispositivo sobre como obter um endereço IPv6 unicast global. A decisão final é do sistema operacional do dispositivo. A mensagem ICMPv6 de RA inclui:

- **Prefixo de rede e comprimento do prefixo** – Informa ao dispositivo a que rede ele pertence.
- **Endereço do gateway padrão** – É um endereço LLA IPv6, o endereço IPv6 origem da mensagem de RA.
- **Endereços DNS e nome de domínio** – Endereços de servidores DNS e um nome de domínio.

Existem três métodos para mensagens RA:

- **Método 1: SLAAC** - “Eu tenho tudo o que você precisa, incluindo o prefixo, comprimento do prefixo e endereço de gateway padrão.”
- **Método 2: SLAAC com um servidor DHCPv6 sem estado** - "Aqui estão as minhas informações, mas você precisa obter outras informações, como endereços DNS, de um servidor DHCPv6 sem estado".
- **Método 3: DHCPv6 com estado (sem SLAAC)**- “Posso dar-lhe o seu endereço de gateway padrão. Você precisa pedir a um servidor DHCPv6 com estado todas as suas outras informações.”


## 33.3.3 Método 1: SLAAC

SLAAC é um método que permite que um dispositivo crie seu próprio GUA sem os serviços do DHCPv6. Com SLAAC, os dispositivos dependem das mensagens ICMPv6 de RA (Anúncio de Roteador) do roteador local para obter as informações necessárias.

Por padrão, a mensagem de RA sugere que o dispositivo de recebimento use as informações dessa mensagem para criar seu próprio endereço IPv6 unicast global e para todas as demais informações. Os serviços de um servidor DHCPv6 não são obrigatórios.

SLAAC é stateless, o que significa que não existe servidor central (por exemplo, um servidor DHCPv6 stateful) alocando endereços unicast globais e mantendo uma lista de dispositivos e seus endereços. Com SLAAC, o dispositivo cliente usa as informações da mensagem de RA para criar seu próprio endereço unicast global. Como mostrado na Figura , as duas partes do endereço são criadas da seguinte forma:

- **Prefixo** - Isso é anunciado na mensagem RA.
- **ID da Interface** - Isso usa o processo EUI-64 ou gera um número aleatório de 64 bits, dependendo do sistema operacional do dispositivo.

![[Pasted image 20260630212608.png]]


## 33.3.4 Método 2: SLAAC e DHCPv6 sem esstado

Uma interface de roteador pode ser configurada para enviar um anúncio de roteador usando SLAAC e DHCPv6 sem estado.

Como mostrado na figura, com esse método, a mensagem RA sugere que os dispositivos usem o seguinte:

- SLAAC para criar seu próprio IPv6 GUA
- O LLA do roteador, que é o endereço IPv6 de origem RA, como o endereço de gateway padrão.
- Um servidor DHCPv6 sem estado (stateless) para obter outras informações como o endereço de um servidor DNS e um nome de domínio.

**Nota**: Um servidor DHCPv6 sem estado distribui endereços do servidor DNS e nomes de domínio. Não atribui GUAs.

![[Pasted image 20260630212628.png]]

## 33.3.5 Método 3: DHCPv6 com estado

Uma interface de roteador pode ser configurada para enviar um RA usando apenas DHCPv6 com estado.

O DHCPv6 stateful é semelhante ao DHCP para IPv4. Um dispositivo pode receber automaticamente suas informações de endereçamento, incluindo uma GUA, tamanho do prefixo e os endereços dos servidores DNS de um servidor DHCPv6 com monitoração de estado.

Como mostrado na figura, com esse método, a mensagem RA sugere que os dispositivos usam o seguinte:

- O LLA do roteador, que é o endereço IPv6 de origem RA, como o endereço de gateway padrão
- Um servidor DHCPv6 stateful para obter o endereço unicast global, o endereço do servidor DNS, o nome do domínio e todas as demais informações.

![[Pasted image 20260630212641.png]]

Um servidor DHCPv6 com estado aloca e mantém uma lista dos dispositivos que recebem endereços IPv6. DHCP para IPv4 é com estado (stateful).

**Nota**: O endereço de gateway padrão só pode ser obtido dinamicamente da mensagem de RA. O servidor DHCPv6 sem estado ou com estado não fornece o endereço de gateway padrão.

## 33.3.6 Processo EUI-64 ou Gerado Aleatoriamente

Quando a mensagem de RA é SLAAC ou SLAAC com DHCPv6 sem estado, o cliente deve gerar sua própria ID da interface. O cliente conhece a parte de prefixo do endereço da mensagem de RA, mas deve criar sua própria ID da interface. A ID da interface pode ser criada por meio do processo EUI-64 ou de um número de 64 bits gerado aleatoriamente, como mostrado na Figura 1.

### Criando dinamicamente um ID de interface

![[Pasted image 20260630212658.png]]


## 33.3.7 Processo EUI-64

AIEEE definiu o identificador exclusivo estendido (EUI) ou processo EUI-64 modificado. Esse processo usa o endereço MAC Ethernet de 48 bits de um cliente e insere outros 16 bits no meio do endereço MAC de 48 bits para criar uma ID da interface de 64 bits.

Geralmente representados em hexadecimal, os endereços MAC de Ethernet são compostos de duas partes:

- **Organizationally unique identifier (OUI)** – O OUI é um código de fornecedor de 24 bits (6 dígitos hexadecimais) designado pelo IEEE.
- **Identificador de dispositivo** – O identificador do dispositivo é um valor exclusivo de 24 bits (6 dígitos hexadecimais) com um OUI em comum.

Um ID de interface EUI-64 é representado em binário e composto por três partes:

- OUI de 24 bits do endereço MAC do cliente, mas o sétimo bit (o bit universal/local (U/L)) é invertido. Isso significa que, se o sétimo bit for 0, ele se tornará 1, e vice-versa.
- O valor de 16 bits fffe (em hexadecimal) inserido.
- Identificador do dispositivo de 24 bits do endereço MAC do cliente.

O processo EUI-64 está ilustrado na Figura 2, usando o endereço MAC Gigabit Ethernet de R1 fc99:4775:cee0.

![[Pasted image 20260630212712.png]]

**Etapa 1:** Divida o endereço MAC entre o OUI e o identificador do dispositivo.

**Etapa 2:** Insira o valor hexadecimal FFFE, o qual em binário: 1111 1111 1111 1110.

**Etapa 3:** Converta os primeiros 2 valores hexadecimais do OUI em binário e inicie o bit de U/L (7 bits). Neste exemplo, o 0 do bit 7 é alterado para 1.

O resultado é um ID de interface gerado pela EUI-64 de fe99: 47ff: fe75: cee0.

**Observação** : O uso do bit de U/L e os motivos para reverter o valor são discutidos em RFC 5342.

A saída de exemplo para o comando **ipconfig** mostra o GUA IPv6 sendo criado dinamicamente usando o SLAAC e o processo EUI-64. Uma maneira fácil de identificar que um endereço provavelmente foi criado usando o EUI-64 é o **fffe** localizado no meio do ID da interface.

A vantagem do EUI-64 é o endereço MAC Ethernet que pode ser usado para determinar a ID da interface. Ele também permite que os administradores de rede rastreiem facilmente um endereço IPv6 para um dispositivo final usando o endereço MAC exclusivo. No entanto, isso causou preocupações de privacidade entre muitos usuários que se preocupavam que seus pacotes pudessem ser rastreados para o computador físico real. Devido a essas preocupações, poderá ser utilizada uma ID da interface gerada de forma aleatória.

### ID da interface gerada com EUI-64

```
C:\> ipconfig
Windows IP Configuration
Ethernet adapter Local Area Connection:
   Connection-specific DNS Suffix . :
   IPv6 Address. . . . . . . . . . . : 
2001:db8:acad:1:
fc99:47
ff:fe
75:cee0
   Link-local IPv6 Address . . . . . : fe80::fc99:47ff:fe75:cee0
   Default Gateway . . . . . . . . . : fe80::1
C:\>
```


## 33.3.8 IDs da Interface Geradas Aleatoriamente

Dependendo do sistema operacional, um dispositivo pode usar uma ID da interface gerada de forma aleatória em vez de usar o endereço MAC e o processo EUI-64. Por exemplo, do Windows Vista em diante, o Windows usa uma ID da interface gerada de forma aleatória em vez de uma criada com o EUI-64. O Windows XP e os sistemas operacionais Windows anteriores usavam o EUI-64.

Depois que a ID da interface for estabelecida, seja pelo processo de EUI-64 ou por geração aleatória, ela poderá ser combinada a um prefixo IPv6 da mensagem de RA para criar um endereço unicast global, como mostra a Figura 4.

### ID da interface gerada aleatoriamente com 64 bits

```
C:\> ipconfig
Windows IP Configuration
Ethernet adapter Local Area Connection:
   Connection-specific DNS Suffix  . :
   IPv6 Address. . . . . . . . . . . : 
2001:db8:acad:1:
50a5:8a35:a5bb:66e1
   Link-local IPv6 Address . . . . . : fe80::50a5:8a35:a5bb:66e1
   Default Gateway . . . . . . . . . : fe80::1
C:\>
```

**Nota**: Para garantir a exclusividade de qualquer endereço IPv6 unicast, o cliente pode usar um processo conhecido como detecção de endereço duplicado (DAD). Isso equivale a uma solicitação ARP para seu próprio endereço. Se não houver resposta, significa que o endereço é exclusivo.


## 33.3.9 Verifique o seu entendimento - Endereçamento dinâmico para IPv6 GUAs

**Verifique sua compreensão sobre endereçamento dinâmico para GUAs IPv6 escolhendo a melhor resposta para as seguintes perguntas.**

### Pergunta 1

Verdadeiro ou falso? As mensagens de RA são enviadas a todos os roteadores IPv6 por hosts solicitando informações de endereçamento.

- [ ] Verdadeiro
- [x] Falso

✅ RESPOSTA CORRETA: Falso

> As mensagens de anúncio do roteador (RA) são enviadas para todos os nós IPv6. Se o Método 1 (somente SLAAC) for usado, o RA incluirá informações de prefixo de rede, prefixo e gateway padrão.

---

### Pergunta 2

Qual método de endereçamento dinâmico para GUAs é aquele em que os dispositivos dependem exclusivamente do conteúdo da mensagem RA para suas informações de endereçamento?

- [x] Método 1: SLAAC
- [ ] Método 2: SLAAC e DHCPv6 sem estado (stateless)
- [ ] Método 3: DHCPv6 com estado (stateful)

✅ RESPOSTA CORRETA: Método 1: SLAAC

> SLAAC é um método onde os dispositivos criam seu próprio GUA sem os serviços do DHCPv6. Com SLAAC, os dispositivos dependem das mensagens ICMPv6 de RA (Anúncio de Roteador) do roteador local para obter as informações necessárias.

---

### Pergunta 3

Qual método de endereçamento dinâmico para GUAs é aquele em que os dispositivos contam apenas com um servidor DHCPv6 para obter suas informações de endereçamento?

- [ ] Método 1: SLAAC
- [ ] Método 2: SLAAC e DHCPv6 stateless
- [x] Método 3: DHCPv6 com estado

✅ RESPOSTA CORRETA: Método 3: DHCPv6 com estado

> Um dispositivo pode receber automaticamente suas informações de endereçamento, incluindo uma GUA, tamanho do prefixo e os endereços dos servidores DNS de um servidor DHCPv6 com monitoração de estado.

---

### Pergunta 4

Qual método de endereçamento dinâmico para GUAs é aquele em que os dispositivos obtêm sua configuração IPv6 em uma mensagem RA e solicitam informações DNS de um servidor DHCPv6?

- [ ] Método 1: SLAAC
- [x] Método 2: SLAAC e DHCPv6 sem estado
- [ ] Método 3: DHCPv6 com estado

✅ RESPOSTA CORRETA: Método 2: SLAAC e DHCPv6 sem estado

> SLAAC e DHCPv6 sem estado é um método em que os dispositivos usam SLAAC para o GUA e endereço de gateway padrão. Em seguida, os dispositivos usam um servidor DHCPv6 sem estado para servidores DNS e outras informações de endereçamento.

---

### Pergunta 5

Quais são os dois métodos que um dispositivo pode usar para gerar seu próprio ID de interface IPv6? (Selecione dois)

- [x] Gerado Aleatoriamente
- [ ] DHCPv6 sem estado
- [x] EUI-64
- [ ] SLAAC
- [ ] DHCPv6 com estado

✅ RESPOSTA CORRETA: Gerado Aleatoriamente / EUI-64

> Quando a mensagem de RA é SLAAC ou SLAAC com DHCPv6 sem estado, o cliente deve gerar sua própria ID da interface.

# 33.4 Endereçamento Dinâmico para LLAs IPv6

## 33.4.1 LLAs dinâmicos

Todos os dispositivos IPv6 devem ter um IPv6 LLA. Assim como IPv6 GUAs, você também pode criar LLAs dinamicamente. Independentemente de como você cria seus LLAS (e seus GUAs), é importante que você verifique toda a configuração de endereço IPv6. Este tópico explica a verificação de configuração de LLAs e IPv6 gerados dinamicamente.

A Figura 1 mostra que o endereço de link local é criado dinamicamente com o prefixo FE80::/10 e que a ID da interface é criada por meio do processo EUI-64 ou por um número de 64 bits gerado aleatoriamente.

![[Pasted image 20260630213038.png]]

## 33.4.2 LLAs dinâmicos no Windows

Sistemas operacionais, como o Windows, normalmente usarão o mesmo método para um GUA criado pelo SLAAC e um LLA atribuído dinamicamente. Veja as áreas destacadas nos exemplos a seguir que foram mostrados anteriormente.

### ID da interface gerada com EUI-64

```
C:\> ipconfig
Windows IP Configuration
Ethernet adapter Local Area Connection:
Connection-specific DNS Suffix . :
IPv6 Address. . . . . . . . . . . : 2001:db8:acad:1:
fc99:47
ff:fe
75:cee0
Link-local IPv6 Address . . . . . : fe80::
fc99:47
ff:fe
75:cee0
Default Gateway . . . . . . . . . : fe80::1
C:\>
```

### ID da interface gerada aleatoriamente com 64 bits

```
C:\> ipconfig
Windows IP Configuration
Ethernet adapter Local Area Connection:
   Connection-specific DNS Suffix  . :
   IPv6 Address. . . . . . . . . . . : 2001:db8:acad:1:
50a5:8a35:a5bb:66e1
   Link-local IPv6 Address . . . . . : fe80::
50a5:8a35:a5bb:66e1
   Default Gateway . . . . . . . . . : fe80::1
C:\>
```

## 33.4.3 LLAs dinâmicos em Roteadores Cisco

Os roteadores Cisco criam automaticamente um endereço IPv6 de link local sempre que um endereço unicast global é atribuído à interface. Por padrão, os roteadores Cisco IOS usam o EUI-64 para gerar a ID da interface de todos os endereços de link local em interfaces IPv6. Em interfaces seriais, o roteador usará o endereço MAC de uma interface Ethernet. Lembre-se de que um endereço de link local deve ser exclusivo somente nesse link ou rede. No entanto, uma desvantagem ao usar o endereço link local atribuído dinamicamente é sua longa ID de interface, o que faz com que seja um desafio identificar e lembrar os endereços atribuídos. A Figura 3 mostra o endereço MAC da interface Gigabit Ethernet 0/0 de R1. Esse endereço é usado para criar dinamicamente o LLA na mesma interface e também para a interface Serial 0/1/0.

Para tornar mais fácil reconhecer esses endereços em roteadores e lembrar deles, é comum configurar estaticamente endereços IPv6 de link local nos roteadores.

### IPv6 LLA usando EUI-64 no roteador R1

```
R1# show interface gigabitEthernet 0/0/0
GigabitEthernet0/0/0 is up, line protocol is up
  Hardware is ISR4221-2x1GE, address is 
7079.b392.3640
 (bia 7079.b392.3640)
(Output omitted)
R1# show ipv6 interface brief
GigabitEthernet0/0/0   [up/up]
    FE80::
7279:B3
FF:FE
92:3640
    2001:DB8:ACAD:1::1
GigabitEthernet0/0/1   [up/up]
    FE80::
7279:B3
FF:FE
92:3641
    2001:DB8:ACAD:2::1
Serial0/1/0            [up/up]
    FE80::
7279:B3
FF:FE
92:3640
    2001:DB8:ACAD:3::1
Serial0/1/1            [down/down]
    unassigned
R1#
```

## 33.4.4 Verificando a Configuração de Endereço IPv6

A Figura mostra a topologia.

![[Pasted image 20260630213143.png]]

**Clique em cada botão para obter a saída e uma descrição do comando.**

### show ipv6 interface brief

A saída do comando **show ipv6 interface brief** exibe endereços IPv6 configurados nas interface Ethernet. EUI-64 usa esse endereço MAC para gerar a ID da interface para o endereço de link local. Além disso, o comando **show ipv6 interface brief** exibe a saída abreviada para cada uma das interfaces. A saída [up/up] na mesma linha que a interface indica o estado da Camada 1/Camada 2 da interface. Isso equivalente é o mesmo que as colunas de status e de protocolo no comando IPv4 .

Observe que aqui cada interface tem dois endereços IPv6. O segundo endereço para cada interface é o GUA que foi configurado. O primeiro endereço, que começa com FE80, é o endereço de link local unicast da interface. Lembre-se de que o endereço de link local será automaticamente adicionado à interface quando um endereço unicast global for atribuído.

Além disso, observe que o endereço de link local da serial 0/0/0 de R1 é o mesmo da sua interface Gigabit Ethernet 0/0. Como as interfaces seriais não têm endereços MAC Ethernet, o Cisco IOS usa o endereço MAC da primeira interface Ethernet disponível. Isso é possível porque as interfaces de link local só precisam ser exclusivas nesse link.

**O comando show ipv6 interface brief no R1**

```
R1# show ipv6 interface brief
GigabitEthernet0/0/0   [up/up]
    FE80::1:1
    2001:DB8:ACAD:1::1
GigabitEthernet0/0/1   [up/up]
    FE80::1:2
    2001:DB8:ACAD:2::1
Serial0/1/0            [up/up]
    FE80::1:3
    2001:DB8:ACAD:3::1
Serial0/1/1            [down/down]
unassigned
R1#
```

### show ipv6 route

Como mostrado no exemplo, o comando **show ipv6 route** pode ser usado para verificar que redes IPv6 e endereços IPv6 específicos tenham sido instalados tabela de roteamento IPv6. O comando **show ipv6 route** só exibirá redes IPv6, não redes IPv4.

Na tabela de rotas, um **C** próximo a uma rota indica que é uma rede conectada diretamente. Quando a interface de um roteador está configurada com um endereço unicast global e se encontra no estado “up/up”, o prefixo IPv6 e o comprimento do prefixo são adicionados à tabela de roteamento IPv6 como uma rota conectada.

**Nota**: O **L** indica uma rota local, o endereço IPv6 específico atribuído à interface. Isto não é um LLA. Os endereços de link local não são incluídos na tabela de roteamento do roteador, pois não são endereços roteáveis.

O endereço IPv6 unicast global configurado na interface também é instalado na tabela de roteamento como uma rota local. A rota local tem um prefixo /128. As rotas locais são usadas pela tabela de roteamento para processar de forma eficiente pacotes com um endereço destino igual ao endereço da interface do roteador.

**O comando show ipv6 route no R1**

```
R1# show ipv6 route
IPv6 Routing Table - default - 7 entries
Codes: C - Connected, L - Local, S - Static, U - Per-user Static route
 
C   2001:DB8:ACAD:1::/64 [0/0]
     via GigabitEthernet0/0/0, directly connected
L   2001:DB8:ACAD:1::1/128 [0/0]
     via GigabitEthernet0/0/0, receive
C   2001:DB8:ACAD:2::/64 [0/0]
     via GigabitEthernet0/0/1, directly connected
L   2001:DB8:ACAD:2::1/128 [0/0]
     via GigabitEthernet0/0/1, receive
C   2001:DB8:ACAD:3::/64 [0/0]
     via Serial0/1/0, directly connected
L   2001:DB8:ACAD:3::1/128 [0/0]
     via Serial0/1/0, receive
L   FF00::/8 [0/0]
     via Null0, receive
R1#
```


### ping

O comando **ping** para IPv6 é idêntico ao comando usado com IPv4, exceto pelo fato de que um endereço IPv6 é usado. Como mostrado na Figura 3, o comando serve para verificar a conectividade da Camada 3 entre R1 e PC1. Ao fazer ping de um roteador para um endereço de link local, o Cisco IOS solicitará que o usuário escolha a interface de saída. Como o endereço de link local de destino pode estar em um ou mais de seus links ou redes, o roteador precisa saber para qual interface enviar o ping.

**O comando ping no R1**

```
R1# ping 2001:db8:acad:1::10
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 2001:DB8:ACAD:1::10, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/1/1 ms
R1#
```


## 33.4.5 Verificador de sintaxe - Verifique a configuração do endereço IPv6

Use comandos **show** para verificar a configuração do endereço IPv6 nas interfaces do roteador R1.

![[Pasted image 20260630213257.png]]

```
Insira o comando show que exibirá um breve resumo do status das interfaces IPv6.

R1#show ipv6 interface brief
GigabitEthernet0/0/0   [up/up]
    FE80::1:1
    2001:DB8:ACAD:1::1
GigabitEthernet0/0/1   [up/up]
    FE80::2:1
    2001:DB8:ACAD:2::1
Serial0/1/0            [up/up]
    FE80::3:1
    2001:DB8:ACAD:3::1
Serial0/1/1            [down/down]
    unassigned
GigabitEthernet0       [administratively down/down]
    unassigned
Verifique a conectividade de R1 para PC2 em 2001:db8:acad:1: :10.

R1#show ipv6 route
IPv6 Routing Table - default - 7 entries
Codes: C - Connected, L - Local, S - Static, U - Per-user Static route
       B - BGP, HA - Home Agent, MR - Mobile Router, R - RIP
       H - NHRP, I1 - ISIS L1, I2 - ISIS L2, IA - ISIS interarea
       IS - ISIS summary, D - EIGRP, EX - EIGRP external, NM - NEMO
       ND - ND Default, NDp - ND Prefix, DCE - Destination, NDr - Redirect
       O - OSPF Intra, OI - OSPF Inter, OE1 - OSPF ext 1, OE2 - OSPF ext 2
       ON1 - OSPF NSSA ext 1, ON2 - OSPF NSSA ext 2, la - LISP alt
       lr - LISP site-registrations, ld - LISP dyn-eid, a - Application
C   2001:DB8:ACAD:1::/64 [0/0]
     via GigabitEthernet0/0, directly connected
L   2001:DB8:ACAD:1::1/128 [0/0]
     via GigabitEthernet0/0, receive
C   2001:DB8:ACAD:2::/64 [0/0]
     via GigabitEthernet0/1, directly connected
L   2001:DB8:ACAD:2::1/128 [0/0]
     via GigabitEthernet0/1, receive
C   2001:DB8:ACAD:3::/64 [0/0]
     via Serial0/0/1, directly connected
L   2001:DB8:ACAD:3::1/128 [0/0]
     via Serial0/0/1, receive
L   FF00::/8 [0/0]
     via Null0, receive
R1#ping 2001:db8:acad:1::10
Type escape sequence to abort.
Sending 5, 100-byte ICMP Echos to 2001:DB8:ACAD:1::10, timeout is 2 seconds:
!!!!!
Success rate is 100 percent (5/5), round-trip min/avg/max = 1/1/1 ms
Você verificou com êxito a configuração de endereço IPv6.
```

## 33.4.6 Packet Tracer – Configurando Endereçamento IPv6

Nesta atividade, você vai praticar a configuração de endereços IPv6 em servidores, clientes e um roteador. Também vai praticar a verificação da implementação de endereçamento IPv6.

# 33.5 Endereços IPv6 Multicast

## 33.5.1 Endereços multicast IPv6 atribuídos

Anteriormente neste módulo, você aprendeu que existem três grandes categorias de endereços IPv6: unicast, anycast e multicast. Este tópico entra em mais detalhes sobre endereços multicast.

Os endereços IPv6 multicast são semelhantes aos endereços IPv4 multicast. Lembre-se de que um endereço multicast é usado para enviar um único pacote a um ou mais destinos (grupo multicast). Os endereços multicast IPv6 têm o prefixo ff00::/8.

**Nota**: Os endereços multicast só podem ser endereços destino e não endereços origem.

Há dois tipos de endereços IPv6 multicast:

- Endereços multicast conhecidos
- Endereços multicast de nó solicitado.


## 33.5.2 Endereços Multicast IPv6 bem conhecidos

Endereços multicast IPv6 bem conhecidos são atribuídos. Os endereços multicast atribuídos são endereços multicast reservados para grupos predefinidos de dispositivos. Um endereço multicast atribuído é um único endereço usado para acessar um grupo de dispositivos que executam um serviço ou um protocolo comum. Os endereços multicast atribuídos são usados no contexto com protocolos específicos, como o DHCPv6.

Estes são dois grupos multicast atribuídos ao IPv6 comuns:

- **ff02::1 Grupo multicast de todos os nós** – Esse é um grupo de multicast que todos os dispositivos com IPv6 habilitado participam. Um pacote enviado para esse grupo é recebido e processado por todas as interfaces IPv6 no link ou rede. Isso tem o mesmo efeito que um endereço de broadcast em IPv4. A figura mostra um exemplo de comunicação usando o endereço multicast all-nodes. Um roteador IPv6 envia mensagens RA ICMPv6 ao grupo multicast de todos os nós.
- **ff02::2 Grupo multicast de todos os roteadores** – Esse é um grupo multicast que todos os roteadores IPv6 participam. Um roteador se torna um membro desse grupo quando é habilitado com um roteador IPv6 com o comando de configuração global **ipv6 unicast-routing** . Um pacote enviado para esse grupo é recebido e processado por todos os roteadores IPv6 no link ou rede.

### IPv6 All-Nodes Multicast: RA Message

![[Pasted image 20260630213401.png]]

Os dispositivos habilitados para IPv6 enviam mensagens ICMPv6 RS para o endereço multicast de todos os roteadores. A mensagem de RS solicita uma mensagem de RA do roteador IPv6 para ajudar o dispositivo em sua configuração de endereço. O roteador IPv6 responde com uma mensagem RA, conforme mostrado.

## 33.5.3 Endereços multicast IPv6 de nó solicitado

Um endereço multicast de nó solicitado é semelhante ao endereço multicast all-nodes(todos os nós). A vantagem do endereço multicast nó solicitado é que ele é mapeado para um endereço multicast Ethernet especial. Isso permite que a placa de rede Ethernet filtre o quadro, examinando o endereço MAC de destino sem enviá-lo ao processo IPv6 para ver se o dispositivo é o alvo pretendido do pacote IPv6.

![[Pasted image 20260630213420.png]]

## **33.5.4 Laboratório – Identificando Endereços IPv6

Neste laboratório, você completará os seguintes objetivos:

- Parte 1: Prática com diferentes tipos de endereços IPv6
- Parte 2: Examinar o Endereço e a Interface de Rede de um Host IPv6


# 33.6 Resumo de Endereçamento IPv6

## 33.6.1 O que aprendi neste módulo?

### Tipos de Endereço IPv6

Há três tipos de endereços IPv6: unicast, multicast e anycast. O IPv6 não usa a notação decimal com pontos da máscara de sub-rede. Como o IPv4, o comprimento do prefixo é representado na notação de barra e é usado para indicar a parte da rede de um endereço IPv6. Um endereço IPv6 unicast identifica exclusivamente uma interface em um dispositivo habilitado para IPv6. Os endereços IPv6 normalmente têm dois endereços unicast: GUA e LLA. Os endereços locais exclusivos IPv6 têm os seguintes usos: eles são usados para endereçamento local dentro de um site ou entre um número limitado de sites, eles podem ser usados para dispositivos que nunca precisarão acessar outra rede e não são globalmente roteados ou traduzidos para um endereço IPv6 global. O endereço IPv6 unicast global (GUA) é globalmente exclusivo e roteável na Internet IPv6. Esses endereços são equivalentes aos endereços públicos do IPv4. Um GUA tem três partes: um prefixo de roteamento global, um ID de sub-rede e um ID de interface. Um endereço IPv6 de link-local permite que um dispositivo se comunique com outros dispositivos habilitados para IPv6 no mesmo link e somente nesse link (sub-rede). Os dispositivos podem obter um LLA estaticamente ou dinamicamente.

---

### Configuração Estática do GUA e do LLA

O comando Cisco IOS para configurar um endereço IPv4 em uma interface é `ip address` _endereço-IP máscara-de-subrede_. Em contraste, o comando para configurar um GUA IPv6 em uma interface é `ipv6 address` _endereço-ipv6/comprimento do prefixo_. Assim como ocorre no IPv4, a configuração de endereços estáticos em clientes não escala para ambientes maiores. Por esse motivo, a maioria dos administradores de redes IPv6 permite a atribuição dinâmica de endereços IPv6. A configuração manual do LLA permite criar um endereço reconhecível e fácil de lembrar. Geralmente, só é necessário criar endereços de link local reconhecíveis nos roteadores. Os LLAs podem ser configurados manualmente usando o comando `ipv6 address` _endereço-de-link-local-ipv6_ `link-local`.

---

### Endereçamento dinâmico para GUAs IPv6

Um dispositivo obtém um GUA dinamicamente através de mensagens ICMPv6. Os roteadores IPv6 enviam mensagens ICMPv6 de RA a cada 200 segundos para todos os dispositivos habilitados para IPv6 na rede. Uma mensagem de RA também é enviada em resposta a um host que envie uma mensagem ICMPv6 de RS (Solicitação de Roteador). A mensagem de RA ICMPv6 inclui: prefixo de rede e comprimento do prefixo, endereço de gateway padrão e endereços DNS e nome de domínio. As mensagens de RA têm três métodos: SLAAC, SLAAC com um servidor DHCPv6 sem estado e DHCPv6 com estado (sem SLAAC). Com o SLAAC, o dispositivo cliente usa as informações na mensagem RA para criar seu próprio GUA porque a mensagem contém o prefixo e o ID da interface. Com o SLAAC com DHCPv6 sem estado, a mensagem RA sugere que os dispositivos usam SLAAC para criar seu próprio IPv6 GUA, usar o roteador LLA como o endereço de gateway padrão e usar um servidor DHCPv6 sem estado para obter outras informações necessárias.

Com o DHCPv6 com estado, o RA sugere que os dispositivos usam o roteador LLA como o endereço de gateway padrão e o servidor DHCPv6 com estado para obter um GUA, um endereço de servidor DNS, nome de domínio e todas as outras informações necessárias. A ID da interface pode ser criada por meio do processo EUI-64 ou de um número de 64 bits gerado aleatoriamente. Esse processo usa o endereço MAC Ethernet de 48 bits de um cliente e insere outros 16 bits no meio do endereço MAC de 48 bits para criar uma ID da interface de 64 bits. Dependendo do sistema operacional, um dispositivo pode usar uma solicitação de ID de interface gerada aleatoriamente.

---

### Endereçamento Dinâmico para LLAs IPv6

Todos os dispositivos IPv6 devem ter um LLA IPv6. Um LLA pode ser configurado manualmente ou criado dinamicamente. Sistemas operacionais, como o Windows, normalmente usarão o mesmo método para um GUA criado pelo SLAAC e um LLA atribuído dinamicamente. Os roteadores Cisco criam automaticamente um endereço IPv6 de link local sempre que um endereço unicast global é atribuído à interface. Por padrão, os roteadores Cisco IOS usam o EUI-64 para gerar a ID da interface de todos os endereços de link local em interfaces IPv6. Em interfaces seriais, o roteador usará o endereço MAC de uma interface Ethernet. Para tornar mais fácil reconhecer esses endereços em roteadores e lembrar deles, é comum configurar estaticamente endereços IPv6 de link local nos roteadores. Para verificar a configuração do endereço IPv6, use os três comandos a seguir: `show ipv6 interface brief`, `show ipv6 route` e `ping`.

---

### Endereços IPv6 Multicast

Existem dois tipos de endereços multicast IPv6: endereços multicast bem conhecidos e endereços multicast de nós solicitados. Os endereços multicast atribuídos são endereços multicast reservados para grupos predefinidos de dispositivos. Endereços multicast bem conhecidos são atribuídos. Dois grupos de multicast atribuídos comuns são: ff02::1 Grupo de multicast de todos os nós e ff02::2 Grupo de multicast de todos os roteadores. Um endereço multicast nó solicitado é semelhante ao endereço multicast all-nodes. A vantagem do endereço multicast nó solicitado é que ele é mapeado para um endereço multicast Ethernet especial.

---

## 33.6.2 Webster – Questões para Reflexão

Webster está ao seu serviço novamente!

Este módulo tinha muitas informações sobre IPv6. Você aprendeu que há três tipos de mensagens IPv6: unicast, multicast e anycast. O IPv6 não usa a notação decimal com pontos na máscara de sub-rede.

O que você aprendeu sobre o endereçamento estático de LLA e GUA?

Qual é a vantagem do endereçamento estático?

No seu escritório ou universidade, qual seria a desvantagem do endereçamento estático?