
## 29.0.1 Webster - Por que devo fazer este módulo?

Parabéns! Você chegou ao último módulo deste curso! Meu amigo, Diego, configurou a rede e agora precisa verificar se está funcionando corretamente. Felizmente, existem algumas ferramentas que ele e você podem usar para descobrir facilmente se há algo errado com a sua rede. Neste módulo, você aprenderá a usar essas ferramentas para solucionar problemas de sua própria rede. Vai ser divertido!

## 29.0.2 O que vou aprender neste módulo?

**Título do Módulo:** ICMP

**Objetivo do módulo:** Usar várias ferramentas para testar a conectividade de rede.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Mensagens ICMP|Explicar como o protocolo ICMP é usado para testar a conectividade da rede.|
|Teste de ping e traceroute|Usar utilitários ping e traceroute para testar a conectividade da rede.|

# 29.1 Mensagens ICMP

## 29.1.1 Mensagens ICMPv4 e ICMPv6

Neste tópico, você aprenderá sobre os diferentes tipos de ICMPs (Internet Control Message Protocols) e as ferramentas que são usadas para enviá-los.

Embora o IP seja apenas um protocolo de melhor esforço, o pacote TCP/IP fornece mensagens de erro e mensagens informativas ao se comunicar com outro dispositivo IP. Essas mensagens são enviadas com os serviços do ICMP. O objetivo dessas mensagens é dar feedback sobre questões relativas ao processamento de pacotes IP sob certas condições, e não tornar o IP confiável. As mensagens ICMP não são necessárias e muitas vezes não são permitidas por questões de segurança.

O ICMP está disponível tanto para IPv4 como para IPv6. ICMPv4 é o protocolo de mensagens para o IPv4. O ICMPv6 fornece os mesmos serviços para o IPv6, mas inclui funcionalidade adicional. Neste curso, o termo ICMP será usado indistintamente quando falarmos de ICMPv4 e ICMPv6.

Os tipos de mensagens ICMP e os motivos pelos quais são enviadas são extensos. As mensagens ICMP comuns ao ICMPv4 e ICMPv6 e discutidas neste módulo incluem:

- Acessibilidade do host
- Destino ou serviço inalcançável
- Tempo excedido

## 29.1.2 Acessibilidade do Host

Uma mensagem de eco ICMP pode ser usada para testar a capacidade de acesso de um host em uma rede IP. O host local envia uma solicitação de eco ICMP (ICMP Echo Request) para um host. Se o host estiver disponível, o host de destino enviará uma resposta de eco (Echo Reply). Na figura, clique em Reproduzir para ver uma animação de solicitação de eco/resposta de eco ICMP. Esse uso das mensagens de eco ICMP é a base do utilitário **ping**.

![[Pasted image 20260625073736.png]]
![[Pasted image 20260625073811.png]]

## 29.1.3 Destino ou Serviço Inacessível

Quando um host ou um gateway recebe um pacote que não pode entregar, ele pode usar uma mensagem ICMP de destino inalcançável para notificar à origem que o destino ou o serviço está inalcançável. A mensagem conterá um código que indica por que não foi possível entregar o pacote.

Alguns dos códigos de Destino inacessível para o ICMPv4 são os seguintes:

- 0 = rede inalcançável
- 1 = host inalcançável
- 2 = protocolo inalcançável
- 3 = porta inalcançável

Alguns dos códigos de Destino inacessível para o ICMPv6 são os seguintes:

- 0 - Nenhuma rota para o destino
- 1 - A comunicação com o destino é administrativamente proibida (por exemplo, firewall)
- 2 - Além do escopo do endereço de origem
- 3 - Endereço inacessível
- 4 - porta inalcançável

**Observação**: o ICMPv6 possui códigos semelhantes, mas ligeiramente diferentes, para mensagens de destino inacessível.

## 29.1.4 Tempo excedido

Uma mensagem ICMPv4 de tempo excedido é usada por um roteador para indicar que um pacote não pode ser encaminhado porque o campo Vida Útil (TTL) do pacote foi reduzido a 0. Se um roteador recebe um pacote e o campo TTL do pacote IPv4 diminui para zero, ele descarta o pacote e envia uma mensagem de tempo excedido para o host de origem.

O ICMPv6 também enviará uma mensagem de tempo excedido se o roteador não conseguir encaminhar um pacote IPv6 porque o pacote expirou. Em vez do campo TTL do IPv4, o ICMPv6 usa o campo Limite de salto do IPv6 para determinar se o pacote expirou.

**Nota**: As mensagens de tempo excedido são usadas pela ferramenta **traceroute**.

## 29.1.5 Mensagens ICMPv6

As mensagens informativas e de erro encontradas no ICMPv6 são muito semelhantes às mensagens de controle e de erros implementadas pelo ICMPv4. No entanto, o ICMPv6 tem funcionalidade aprimorada e novos recursos que não são encontrados no ICMPv4. As mensagens ICMPv6 são encapsuladas no IPv6.

O ICMPv6 inclui quatro novos protocolos como parte do protocolo ND ou NDP (Neighbor Discovery Protocol):

As mensagens entre um roteador IPv6 e um dispositivo IPv6, incluindo alocação de endereços dinâmicos, são as seguintes:

- Mensagem de Solicitação de Roteador (RS)
- Mensagem de Anúncio de Roteador (RA)

As mensagens entre dispositivos IPv6, incluindo detecção de endereço duplicado e resolução de endereço são as seguintes:

- Mensagem de solicitação de vizinhos (NS)
- Mensagem de anúncio de vizinhos (NA)

**Nota**: O ICMPv6 ND também inclui a mensagem de redirecionamento, que tem uma função semelhante à mensagem de redirecionamento usada no ICMPv4.


### Mensagem RA

As mensagens de RA são enviadas por roteadores habilitados para IPv6 a cada 200 segundos para fornecer informações de endereçamento para hosts habilitados para IPv6. A mensagem RA pode incluir informações de endereçamento para o host, como prefixo, comprimento do prefixo, endereço DNS e nome de domínio. Um host que usa a Configuração Automática de Endereço sem Estado (SLAAC) definirá seu gateway padrão para o endereço local do link do roteador que enviou o RA.
![[Pasted image 20260625074003.png]]
---

### Mensagem RS

Um roteador habilitado para IPv6 também enviará uma mensagem RA em resposta a uma mensagem RS. Na figura, PC1 envia uma mensagem RS para determinar como receber suas informações de endereço IPv6 dinamicamente.
![[Pasted image 20260625074021.png]]
---

### Mensagem NS

Quando um dispositivo recebe um endereço IP unicast global ou unicast local de link, um dispositivo pode receber DAD (detecção de endereço duplicado) para garantir que o endereço IPv6 seja exclusivo. Para verificar a exclusividade de um endereço, o dispositivo enviará uma mensagem NS com seu próprio endereço IPv6 como o endereço IPv6 de destino, conforme mostrado na figura.

Se outro dispositivo na rede tiver esse endereço, ele responderá com uma mensagem de NA. Essa mensagem de NA notificará o dispositivo emissor de que o endereço está em uso. Se uma mensagem de NA correspondente não for retornada dentro de um certo período de tempo, o endereço unicast será exclusivo e aceitável para uso.

**Nota:** O DAD não é necessário, mas o RFC 4861 recomenda que o DAD seja executado em endereços unicast.
![[Pasted image 20260625074033.png]]
---

### Mensagem NA

É usada quando um dispositivo na LAN sabe o endereço IPv6 unicast de um destino, mas não seu endereço MAC Ethernet. Para determinar o endereço MAC destino, o dispositivo enviará uma mensagem de NS para o endereço do nó solicitado. A mensagem incluirá o endereço IPv6 (destino) conhecido. O dispositivo que tem o endereço IPv6 alvo responderá com uma mensagem de NA contendo seu endereço MAC Ethernet.

Na figura, R1 envia uma mensagem NS para 2001:db8:acad:1::10 pedindo seu endereço MAC.

![[Pasted image 20260625074044.png]]

## 29.1.6 Verifique sua compreensão - Mensagens ICMP

**Verifique sua compreensão das mensagens ICMP escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Quais dois tipos de mensagens ICMP são comuns ao ICMPv4 e ICMPv6? (Escolha duas.)

- [x] Destino ou serviço inalcançável
- [ ] Resolução de nome de host
- [ ] Configuração de IP
- [ ] Origem Inacessível
- [x] Tempo excedido

✅ RESPOSTA CORRETA: Destino ou serviço inalcançável / Tempo excedido

> As mensagens ICMP comuns ao ICMPv4 e ICMPv6 incluem confirmação do host, destino ou serviço inalcançável e tempo excedido.

---

### Pergunta 2

Que tipo de mensagem ICMPv6 um host enviaria para adquirir uma configuração IPv6 ao inicializar?

- [ ] Mensagem de anúncio de vizinhos (NA)
- [ ] Mensagem de solicitação de vizinhos (NS)
- [ ] Mensagem de Anúncio de Roteador (RA)
- [x] Mensagem de Solicitação de Roteador (RS)

✅ RESPOSTA CORRETA: Mensagem de Solicitação de Roteador (RS)

> Um host habilitado para IPv6 inicializando enviaria uma mensagem de solicitação de roteador ICMPv6. Um roteador habilitado para IPv6 responderia com uma mensagem de anúncio do roteador.