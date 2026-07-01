# 34.0 Introdução

## 34.0.1 Webster - Por que devo fazer este módulo?

Webster aqui!

Halimah ainda está investigando a rede de sua empresa. Ela está impressionada com a forma como a equipe de TI o estruturou. Ela sabe sobre descoberta de vizinho (ND) IPv6 e, neste módulo, você aprenderá sobre isso também.

IPv6 ND é como dispositivos endereçados IPv6 resolvem endereços MAC. O IPv6 ND permite que dispositivos com endereços IPv6 se comuniquem com outros dispositivos em uma rede, o que é, convenhamos, todo o motivo de ter uma rede.

Então, dada a importância desse assunto, vamos começar!

## 34.0.2 O que vou aprender neste módulo?

**Título do módulo:** Descoberta de vizinhos IPv6

**Objetivo do Módulo:** Explicar como o ND permite a comunicação em uma rede.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Operação de descoberta de vizinho|Descrever a operação de descoberta de vizinho IPv6.|

# 34.1 Operação de descoberta de vizinho

## 34.1.1 Vídeo - Descoberta de Vizinhos IPv6

Se sua rede estiver usando o protocolo de comunicação IPv6, o protocolo de descoberta de vizinhos, ou ND, é o que você precisa para corresponder endereços IPv6 a endereços MAC. Este tópico explica como o ND funciona.

**Pressione o botão Reproduzir para ver uma demonstração do IPv6 Neighbor Discovery.**

Neste vídeo vamos discutir o processo de como o IPv6 executa a resolução de endereços com mensagens de Solicitação de Vizinho ICMPv6 e mensagens de Anúncio de Vizinho. Isso é semelhante ao processo ARP usado pelo IPv4, mas tem certas vantagens que veremos em um momento.

O Host A tem um pacote para enviar ao Host C. O Host A determinou que o endereço IPv6 de destino está na mesma rede que o Host A. O Host A conhece o endereço IPv6 de destino, mas precisa do endereço MAC de destino associado para que ele possa encapsular o pacote IPv6 em um quadro Ethernet para enviar diretamente para o Host C. O Host A examina seu cache vizinho para ver se existe uma entrada para este endereço IPv6 de destino. Semelhante a uma tabela ARP, o cache vizinho mapeia endereços IPv6 para endereços MAC. Como podemos ver, não há nenhuma entrada MAC associada com este endereço IPv6.

O pacote IPv6 é colocado em espera e o Host A cria uma mensagem de solicitação de vizinho ICMPv6. Isso é semelhante a uma solicitação ARP usado para resolução de endereços IPv4. Uma diferença significativa é que as mensagens ARP são enviadas diretamente através de Ethernet, IPv4 não está envolvido. O processo de resolução de endereços IPv6 usa ICMPv6, que é então encapsulado em um cabeçalho IPv6, e em seguida encapsulado em um cabeçalho Ethernet e trailer.

O cabeçalho de solicitação de vizinho ICMPv6 inclui o endereço IPv6 de destino, que é o mesmo endereço IPv6 de destino no pacote que está em espera. O endereço IPv6 de destino é mapeado para um endereço multicast de nó solicitado IPv6 especial, que é então mapeado para um endereço MAC multicast Ethernet especial. Este processo de mapeamento contém uma parte significativa do endereço IPv6 de destino. Isso permite que as NICs Ethernet em cada dispositivo que recebe esse quadro determinem se deve ou não aceitar e processar o quadro. É aqui que vemos uma vantagem da descoberta de vizinhos ICMPv6 sobre ARP para IPv4. Uma vez que o ARP usa um endereço de broadcast, todos os dispositivos na rede local devem processar pelo menos parcialmente uma solicitação ARP.

A mensagem de solicitação de vizinho ICMPv6 é encaminhada pelo Host A e recebida pelo switch. O switch inundará o quadro multicast Ethernet por todas as portas, exceto a porta de entrada. O Host B recebe o quadro Ethernet. A placa de rede Ethernet do Host B examina o endereço MAC de destino. A NIC Ethernet aceitará quadros cujo endereço MAC de destino corresponde ao endereço MAC na NIC, é um endereço MAC de broadcast ou um endereço MAC multicast que mapeia para um de seus endereços IPv6. Neste caso, o endereço MAC multicast não corresponde a nenhum destes, de modo que a NIC do Host B ignora o restante do quadro sem ter que passá-lo para um processo de nível superior para fazer essa determinação. Novamente, essa é uma vantagem sobre o ARP para IPv4.

O roteador R1 recebe o quadro em sua interface LAN. Um processo semelhante ocorre na interface do R1. A placa de rede Ethernet ignora o quadro porque o multicast de destino para o endereço MAC não mapeia para nenhum dos seus endereços IPv6. Mensagens de solicitação de vizinhos ICMPv6 não são encaminhadas pelo roteador. Isso ocorre porque o endereço multicast do nó solicitado no cabeçalho IPv6 é definido com o escopo local do link, o que diz ao roteador para não encaminhar esses pacotes fora do link ou da rede local.

O Host C recebe o quadro Ethernet. Desta vez, o endereço MAC multicast Ethernet corresponde a um endereço MAC associado ao Host C, especificamente o mapeado para o endereço multicast do nó solicitado IPv6 do Host C. Portanto, o Host C aceita o quadro e o transmite para seu processo IPv6 e, em seguida, seu processo ICMPv6. O endereço IPv6 de destino no cabeçalho ICMPv6 corresponde ao seu próprio endereço unicast global IPv6. Então o Host C sabe que é o alvo desta mensagem de solicitação de vizinho. Antes de responder, o Host C adiciona o endereço IPv6 e endereço MAC do Host A ao seu próprio cache vizinho, para que ele possa retornar uma mensagem de anúncio de vizinho.

O Host C responde com uma mensagem de anúncio do vizinho ICMPv6 enviada como uma mensagem unicast Ethernet diretamente para o Host A. O cabeçalho ICMPv6 inclui o endereço IPv6 do Host C, que o Host A já sabia, e o endereço MAC associado que o Host A estava solicitando. O Host A recebe o quadro Ethernet, examina o endereço IPv6 e o endereço MAC no cabeçalho ICMPv6 e o adiciona ao cache vizinho. O Host A agora pode tirar o pacote IPv6 da espera. O Host A atualiza o endereço MAC de destino com o endereço associado com o endereço IPv6 de destino e encaminha o quadro e o pacote IPv6 para o Host C.

Agora, se o endereço IPv6 de destino estivesse em uma rede diferente, este mesmo processo ocorreria para descobrir o endereço MAC do gateway padrão, que mapearia para o endereço local do link IPv6 do R1 nesta LAN.


## 34.1.2 Mensagens de descoberta de vizinhos IPv6

O protocolo de descoberta de vizinhos IPv6 às vezes é chamado de ND ou NDP. Neste curso, vamos nos referir a ele como ND. O ND fornece serviços de resolução de endereço, descoberta de roteador e redirecionamento para IPv6 usando ICMPv6. O ICMPv6 ND usa cinco mensagens ICMPv6 para executar estes serviços:

- Mensagens de solicitação de vizinho
- Mensagens de anúncio vizinho
- Mensagens de solicitação de roteador
- Mensagens de anúncio do roteador
- Redirecionar mensagem.

As mensagens de solicitação de vizinho e anúncio de vizinho são usadas para mensagens de dispositivo a dispositivo, como resolução de endereço (semelhante ao ARP para IPv4). Os dispositivos incluem computadores host e roteadores.

![[Pasted image 20260630214023.png]]

As mensagens de solicitação de roteador e anúncio de roteador são para mensagens entre dispositivos e roteadores. Normalmente, a descoberta de roteador é usada para alocação de endereços dinâmicos e autoconfiguração de endereço sem estado (SLAAC).

![[Pasted image 20260630214038.png]]

**Nota**: A quinta mensagem ICMPv6 ND é uma mensagem de redirecionamento que é usada para uma melhor seleção do próximo salto. Isso está além do escopo deste curso.

IPv6 ND é definido no IETF RFC 4861.

## 34.1.3 Descoberta de Vizinhos IPv6 - Resolução de Endereço

Assim como ARP para IPv4, os dispositivos IPv6 usam IPv6 ND para determinar o endereço MAC de um dispositivo que tem um endereço IPv6 conhecido.

As mensagens de solicitação de vizinho ICMPv6 e de anúncio de vizinho são usadas para resolução de endereço MAC. Isso é semelhante às Solicitações ARP e Respostas ARP usadas pelo ARP para IPv4. Por exemplo, suponha que PC1 queira fazer ping em PC2 no endereço IPv6 2001:db8:acad: :11. Para determinar o endereço MAC para o endereço IPv6 conhecido, o PC1 envia uma mensagem de solicitação de vizinho ICMPv6 conforme ilustrado na figura.

![[Pasted image 20260630214105.png]]

As mensagens de solicitação de vizinho ICMPv6 são enviadas usando endereços multicast Ethernet e IPv6 especiais. Isso permite que o NIC Ethernet do dispositivo receptor determine se a mensagem de solicitação de vizinho é para si mesmo sem precisar enviá-la ao sistema operacional para processamento.

O PC2 responde à solicitação com uma mensagem de anúncio de vizinho ICMPv6 que inclui seu endereço MAC.

## 34.1.4 Packet Tracer - Descoberta de Vizinhos IPv6

Nesta atividade, você completará os seguintes objetivos:

- Parte 1: Rede local de descoberta de vizinhos IPv6
- Parte 2: Rede remota de descoberta de vizinhos IPv6

## 34.1.5 Verifique o seu entendimento - Descoberta de Vizinhos

**Verifique sua compreensão sobre Descoberta de Vizinhos escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Quais duas mensagens ICMPv6 são usadas no SLAAC?

- [x] anúncio de roteador
- [ ] anúncio de vizinho
- [ ] solicitação de vizinho
- [x] solicitação de roteador

✅ RESPOSTA CORRETA: anúncio de roteador / solicitação de roteador

> As duas mensagens ICMPv6 usadas no SLAAC são a solicitação do roteador e o anúncio do roteador.

---

### Pergunta 2

Em quais duas mensagens ICMPv6 são usadas para determinar o endereço MAC de um endereço IPv6 conhecido?

- [ ] solicitação de roteador
- [ ] anúncio de roteador
- [x] anúncio de vizinho
- [x] solicitação de vizinho

✅ RESPOSTA CORRETA: anúncio de vizinho / solicitação de vizinho

> As duas mensagens ICMPv6 usadas na determinação do endereço MAC de um endereço IPv6 conhecido são a solicitação de vizinho e o anúncio de vizinho.

---

### Pergunta 3

Para que tipo de endereço são enviadas mensagens de solicitação de vizinho ICMPv6?

- [ ] broadcast
- [ ] unicast
- [x] multicast

✅ RESPOSTA CORRETA: multicast

> As mensagens de solicitação de vizinho ICMPv6 são enviadas como um multicast.


# 34.2 Resumo da descoberta de vizinhos IPv6

## 34.2.1 O que eu aprendi neste módulo?

### A operação de descoberta de vizinhos

IPv6 não usa ARP, usa o protocolo ND para resolver endereços MAC. O ND fornece serviços de resolução de endereço, descoberta de roteador e redirecionamento para IPv6 usando ICMPv6. O ICMPv6 ND usa cinco mensagens ICMPv6 para executar esses serviços: solicitação de vizinhos, propaganda de vizinhos, solicitação de roteador, anúncio de roteador e redirecionamento. Assim como ARP para IPv4, os dispositivos IPv6 usam IPv6 ND para resolver o endereço MAC de um dispositivo para um endereço IPv6 conhecido.

---

## 34.2.2 Webster – Questões para Reflexão

Webster aqui!

Eu não sabia que o IPv6 não usa ARP. Você sabia disso? Bem, você sabe agora! Neste módulo, eu aprendi sobre a descoberta de vizinhos e espero que você também.

Qual é o objetivo do ND?

Você pode listar as cinco mensagens de ICMPv6 que o ND usa?