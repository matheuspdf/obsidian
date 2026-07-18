# 32.0 Introdução

## 32.0.1 Webster - Por que devo fazer este módulo?

Oi, é Webster novamente.

Halimah está tendo uma boa visão da rede na sede e nas outras filiais. Ela entende melhor como essas redes são, na verdade, apenas uma rede conectada.

É na camada de rede que ocorre a conectividade de ponta a ponta. A conectividade permite enviar um e-mail a um amigo, acessar um site, transmitir um podcast e recuperar um documento de um local central. Gosto de saber sobre redes, protocolos e serviços que estão envolvidos.

Você está intrigado? Eu sei que eu estou!

## 32.0.2 O que vou aprender neste módulo?

**Título do Módulo:** Roteamento na camada de rede

**Objetivo do Módulo:** Explicar como os roteadores usam protocolos e serviços da camada de rede para habilitar a conectividade de ponta a ponta.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Como um Host Roteia|Explique como os dispositivos de rede usam tabelas de roteamento para direcionar pacotes para uma rede de destino.|
|Tabela de Roteamento|Explicar a função dos campos na tabela de roteamento de um roteador.|

# 32.1 Como um Host Roteia

## 32.1.1 Decisão de Encaminhamento do Host

Com IPv4 e IPv6, os pacotes são sempre criados no host de origem. O host de origem deve ser capaz de direcionar o pacote para o host de destino. Para fazer isso, os dispositivos finais (host) criam sua própria tabela de roteamento. Este tópico discute como os dispositivos finais usam tabelas de roteamento.

Outra função da camada de rede é direcionar pacotes entre hosts. Um host pode enviar um pacote para o seguinte:

- **Ele mesmo** - Um host pode executar ping em si mesmo enviando um pacote para um endereço IPv4 especial 127.0.0.1 ou um endereço IPv6 :: / 1, conhecido como interface de loopback. O ping na interface de loopback testa a pilha de protocolos do TCP/IP no host.
- **Host local** - este é um host de destino que está na mesma rede local que o host de envio. Os hosts de origem e destino compartilham o mesmo endereço de rede.
- **Host remoto** - este é um host de destino em uma rede remota. Os hosts de origem e destino não compartilham o mesmo endereço de rede.

A figura ilustra a conexão PC1 a um host local na mesma rede e a um host remoto localizado em outra rede.

![[Pasted image 20260629114340.png]]

Se um pacote é destinado a um host local ou a um host remoto é determinado pelo dispositivo final de origem. O dispositivo final de origem determina se o endereço IP de destino está na mesma rede em que o próprio dispositivo de origem está. O método de determinação varia de acordo com a versão IP:

- **Em IPv4** - o dispositivo de origem usa sua própria máscara de sub-rede junto com seu próprio endereço IPv4 e o endereço IPv4 de destino para fazer essa determinação.
- **Em IPv6** - o roteador local anuncia o endereço da rede local (prefixo) para todos os dispositivos da rede.

Em uma rede doméstica ou comercial, você pode ter vários dispositivos com e sem fio interconectados usando um dispositivo intermediário, como um switch LAN ou um ponto de acesso sem fio (WAP). Este dispositivo intermediário fornece interconexões entre hosts locais na rede local. Os hosts locais podem interagir entre si e compartilhar informações sem a necessidade de dispositivos adicionais. Se um host estiver enviando um pacote para um dispositivo configurado com a mesma rede IP que o dispositivo host, o pacote será simplesmente encaminhado para fora da interface do host, através do dispositivo intermediário e diretamente ao dispositivo de destino.

Obviamente, na maioria das situações, queremos que nossos dispositivos possam se conectar além do segmento de rede local, como em outras residências, empresas e na Internet. Os dispositivos que estão além do segmento de rede local são conhecidos como hosts remotos. Quando um dispositivo de origem envia um pacote a um dispositivo de destino remoto, é necessária a ajuda de roteadores e do roteamento. O roteamento é o processo de identificação do melhor caminho até um destino. O roteador conectado ao segmento de rede local é conhecido como gateway padrão.

## 32.1.2 Gateway Padrão

O gateway padrão é o dispositivo de rede (ou seja, roteador ou switch da Camada 3) que pode rotear o tráfego para outras redes. Comparando a rede com uma sala, o gateway padrão é a porta. Se você quiser ir para outra sala (rede), vai precisar encontrar essa porta.

Em uma rede, um gateway padrão geralmente é um roteador com esses recursos:

- Ele possui um endereço IP local no mesmo intervalo de endereços que outros hosts na rede local.
- Ele pode aceitar dados na rede local e encaminhar dados para fora da rede local.
- Ele direciona o tráfego para outras redes.

Um gateway padrão é necessário para enviar tráfego fora da rede local. O tráfego não pode ser encaminhado para fora da rede local se não houver gateway padrão, o endereço de gateway padrão não estiver configurado ou o gateway padrão estiver inativo.


## 32.1.3 Um host encaminha para o gateway padrão

Uma tabela de roteamento de host normalmente inclui um gateway padrão. No IPv4, o host recebe o endereço IPv4 do gateway padrão dinamicamente do DHCP (Dynamic Host Configuration Protocol) ou configurado manualmente. No IPv6, o roteador anuncia o endereço de gateway padrão ou o host pode ser configurado manualmente.

Na figura, PC1 e PC2 são configurados com o endereço IPv4 de 192.168.10.1 como o gateway padrão.

![[Pasted image 20260629114409.png]]

A configuração do gateway padrão cria uma rota padrão na tabela de roteamento do computador. Uma rota padrão é a rota ou o caminho que o computador usa quando tenta entrar em contato com uma rede remota.

Tanto PC1 quanto PC2 terão uma rota padrão para enviar todo o tráfego destinado a redes remotas para R1.

## 32.1.4 Tabelas de Roteamento dos Hosts

Em um host do Windows, o comando **route print** ou o comando **netstat-r** pode ser usado para exibir a tabela de roteamento do host. Os dois comandos geram o mesmo resultado. O resultado pode parecer confuso no começo, mas é bastante simples de entender.

A figura exibe uma topologia e a saída gerada pelo comando **netstat –r**.![[Pasted image 20260629114428.png]]

### Tabela de Roteamento IPv4 de PC1

```
C:\Users\PC1> netstat -r
(output omitted)
IPv4 Route Table
===========================================================================
Active Routes:
Network Destination         Netmask       Gateway       Interface    Metric
          0.0.0.0           0.0.0.0   192.168.10.1   192.168.10.10       25
        127.0.0.0         255.0.0.0       On-link        127.0.0.1      306
        127.0.0.1   255.255.255.255       On-link        127.0.0.1      306
  127.255.255.255   255.255.255.255       On-link        127.0.0.1      306
     192.168.10.0     255.255.255.0       On-link    192.168.10.10      281
    192.168.10.10   255.255.255.255       On-link    192.168.10.10      281
   192.168.10.255   255.255.255.255       On-link    192.168.10.10      281
        224.0.0.0         240.0.0.0       On-link        127.0.0.1      306
        224.0.0.0         240.0.0.0       On-link    192.168.10.10      281
  255.255.255.255   255.255.255.255       On-link        127.0.0.1      306
  255.255.255.255   255.255.255.255       On-link    192.168.10.10      281
(output omitted)
```

**Nota:** A saída exibe apenas a tabela de rotas IPv4.

Ao inserir o comando **netstat-r** ou o comando equivalente **route print** três seções relacionadas às conexões de rede TCP/IP atuais são exibidas:

- **Lista de interface** - lista o endereço de controle de acesso à mídia (MAC) e o número de interface atribuído de cada interface com capacidade de rede no host, incluindo adaptadores Ethernet, Wi-Fi e Bluetooth.
- **Tabela de rotas IPv4** - lista todas as rotas IPv4 conhecidas, incluindo conexões diretas, rede local e rotas padrão locais.
- **Tabela de rotas IPv6** - lista todas as rotas IPv6 conhecidas, incluindo conexões diretas, rede local e rotas padrão locais.


## 32.1.5 Verifique sua compreensão - Como um host roteia

**Verifique sua compreensão de como um host roteia escolhendo a melhor resposta correta para as seguintes perguntas.**
### Pergunta 1

Qual declaração sobre decisões de encaminhamento de host é verdadeira?

- [x] Os hosts locais podem se alcançar sem a necessidade de um roteador.
- [ ] O roteamento é habilitado em switches para descobrir o melhor caminho para um destino.
- [ ] Um host não pode fazer ping em si mesmo.
- [ ] Um host de destino remoto está na mesma rede local que o host de envio.

✅ RESPOSTA CORRETA: Os hosts locais podem se alcançar sem a necessidade de um roteador.

> Não é necessário um roteador para encaminhar pacotes entre hosts locais na rede.

---

### Pergunta 2

Qual instrução de gateway padrão é verdadeira?

- [ ] O endereço de gateway padrão é o endereço IP de um switch em uma rede remota.
- [x] O endereço de gateway padrão é o endereço IP do roteador na rede local.
- [ ] O tráfego só pode ser encaminhado para fora da rede local se não houver gateway padrão.
- [ ] Um gateway padrão é necessário para enviar pacotes para outros hosts na rede local.

✅ RESPOSTA CORRETA: O endereço de gateway padrão é o endereço IP do roteador na rede local.

> O gateway padrão é o endereço IP de um roteador na rede local.

---

### Pergunta 3

Quais dois comandos podem ser inseridos em um host Windows para exibir sua tabela de roteamento IPv4 e IPv6? (Escolha duas.)

- [x] `route`
- [x] `route print`
- [ ] `netstat -r`
- [ ] `print route`
- [ ] `netroute -l`

✅ RESPOSTA CORRETA: `route` / `route print`

> Os comandos `netstat -r` e `route print` exibirá a tabela de roteamento de um host do Windows. 


# 32.2 Tabelas de Roteamento

## 32.2.1 Decisão de Encaminhamento de Pacotes no Roteador

O tópico anterior discutiu tabelas de roteamento de host. A maioria das redes também contém roteadores, que são dispositivos intermediários. Os roteadores também contêm tabelas de roteamento. Este tópico aborda as operações do roteador na camada de rede. Quando um host envia um pacote para outro host, ele consulta sua tabela de roteamento para determinar para onde enviar o pacote. Se o host de destino estiver em uma rede remota, o pacote será encaminhado para o gateway padrão, que geralmente é o roteador local.

O que acontece quando um pacote chega na interface do roteador?

O roteador examina o endereço IP de destino do pacote e pesquisa sua tabela de roteamento para determinar para onde encaminhar o pacote. A tabela de roteamento contém uma lista de todos os endereços de rede conhecidos (prefixos) e para onde encaminhar o pacote. Essas entradas são conhecidas como entradas de rota ou rotas. O roteador encaminhará o pacote usando a melhor (mais longa) entrada de rota correspondente.

![[Pasted image 20260630201653.png]]

A tabela a seguir mostra as informações pertinentes da tabela de roteamento R1.

**Tabela de Roteamento de R1**

|Rota|Próximo salto ou interface de saída|
|---|---|
|192.168.10.0 /24|G0/0/0|
|209.165.200.224/30|G0/0/1|
|**10.1.1.0/24**|**via R2**|
|Rota padrão 0.0.0.0/0|via R2|

## 32.2.2 Tabela de Roteamento do Roteador IP

A tabela de roteamento do roteador contém entradas de rota de rede listando todos os possíveis destinos de rede conhecidos.

A tabela de roteamento armazena três tipos de entradas de rota:

- **Redes conectadas diretamente -** Essas entradas de rota de rede são interfaces de roteador ativas. Os roteadores adicionam uma rota diretamente conectada quando uma interface está configurada com um endereço IP e está ativada. Cada interface do roteador está conectada a um segmento de rede diferente. Na figura, as redes diretamente conectadas na tabela de roteamento IPv4 R1 seriam 192.168.10.0/24 e 209.165.200.224/30.
- **Redes remotas -** Essas entradas de rotas de rede são conectadas a outros roteadores. Os roteadores aprendem sobre redes remotas sendo explicitamente configurados por um administrador ou trocando informações de rota usando um protocolo de roteamento dinâmico. Na figura, a rede remota na tabela de roteamento IPv4 R1 seria 10.1.1.0/24.
- **Rota padrão -** Como um host, a maioria dos roteadores também inclui uma entrada de rota padrão, um gateway de último recurso. A rota padrão é usada quando não há correspondência melhor (mais) na tabela de roteamento IP. Na figura, a tabela de roteamento IPv4 R1 provavelmente incluiria uma rota padrão para encaminhar todos os pacotes para o roteador R2.

A figura identifica as redes remotas e diretamente conectadas ao roteador R1.

![[Pasted image 20260630201948.png]]

Um roteador pode aprender sobre redes remotas de duas maneiras:

- **Manualmente** – As redes remotas são inseridas manualmente na tabela de roteamento usando rotas estáticas.
- **Dinamicamente** - As rotas remotas são aprendidas automaticamente usando um protocolo de roteamento dinâmico.


## 32.2.3 Roteamento estático

Rotas estáticas são entradas de rota configuradas manualmente. A figura mostra um exemplo de uma rota estática configurada manualmente no roteador R1. A rota estática inclui o endereço de rede remota e o endereço IP do roteador de salto seguinte.

![[Pasted image 20260630202030.png]]

O R1 é configurado manualmente com uma rota estática para alcançar a rede 10.1.1.0/24. Se esse caminho mudar, R1 exigirá uma nova rota estática.

Se houver uma alteração na topologia da rede, a rota estática não será atualizada automaticamente e deverá ser reconfigurada manualmente. Por exemplo, na figura R1 tem uma rota estática para alcançar a rede 10.1.1.0/24 via R2. Se esse caminho não estiver mais disponível, R1 precisaria ser reconfigurado com uma nova rota estática para a rede 10.1.1.0/24 via R3. Portanto, o roteador R3 precisaria ter uma entrada de rota em sua tabela de roteamento para enviar pacotes destinados a 10.1.1.0/24 para R2.

![[Pasted image 20260630202039.png]]

Se a rota de R1 via R2 não estiver mais disponível, uma nova rota estática via R3 precisaria ser configurada. Uma rota estática não se ajusta automaticamente para alterações de topologia.

O roteamento estático tem as seguintes características:

- Uma rota estática deve ser configurada manualmente.
- O administrador precisa reconfigurar uma rota estática se houver uma alteração na topologia e a rota estática não for mais viável.
- Uma rota estática é apropriada para uma rede pequena e quando há poucos ou nenhum vínculo redundante.


## 32.2.4 Roteamento dinâmico

Um protocolo de roteamento dinâmico permite que os roteadores aprendam automaticamente sobre redes remotas, incluindo uma rota padrão, de outros roteadores. Os roteadores que usam protocolos de roteamento dinâmico compartilham automaticamente informações de roteamento com outros roteadores e compensam qualquer alteração de topologia sem envolver o administrador da rede. Se houver uma alteração na topologia de rede, os roteadores compartilham essas informações usando o protocolo de roteamento dinâmico e atualizam automaticamente suas tabelas de roteamento.

Os protocolos de roteamento dinâmico incluem OSPF e Enhanced Interior Gateway Routing Protocol (EIGRP). A figura mostra um exemplo de roteadores R1 e R2 compartilhando automaticamente informações de rede usando o protocolo de roteamento OSPF.

![[Pasted image 20260630202054.png]]

- R1 está usando o protocolo de roteamento OSPF para informar R2 sobre a rede 192.168.10.0/24.
- R2 está usando o protocolo de roteamento OSPF para deixar R1 saber sobre a rede 10.1.1.0/24.

A configuração básica requer apenas que o administrador de rede habilite as redes conectadas diretamente dentro do protocolo de roteamento dinâmico. O protocolo de roteamento dinâmico fará automaticamente o seguinte:

- Descobrir redes remotas
- Manter as informações de roteamento atualizadas
- Escolha o melhor caminho para as redes de destino
- Tentar encontrar um novo melhor caminho se o caminho atual não estiver mais disponível

Quando um roteador é configurado manualmente com uma rota estática ou aprende sobre uma rede remota dinamicamente usando um protocolo de roteamento dinâmico, o endereço de rede remota e o endereço de próximo salto são inseridos na tabela de roteamento IP. Conforme mostrado na figura, se houver uma alteração na topologia de rede, os roteadores ajustarão automaticamente e tentarão encontrar um novo melhor caminho.

![[Pasted image 20260630202104.png]]

R1, R2 e R3 estão usando o protocolo de roteamento dinâmico OSPF. Se houver uma alteração na topologia de rede, eles poderão ajustar automaticamente para encontrar um novo caminho melhor.

**Nota:** É comum que alguns roteadores usem uma combinação de rotas estáticas e um protocolo de roteamento dinâmico.

## 32.2.5 Vídeo - Tabela de roteamento do roteador IPv4

![[32.2.5.mp4#subtitle=anexos/32.2.5.vtt]]

Ao contrário de uma tabela de roteamento de computadores host, não há títulos de coluna que identifiquem as informações contidas na tabela de roteamento de um roteador. É importante compreender o significado dos diferentes itens incluídos em cada entrada da tabela de roteamento.

**Clique em Reproduzir para ver uma introdução à tabela de roteamento IPv4.**

Um roteador usa informações em sua tabela de roteamento para encaminhar pacotes. Uma tabela de roteamento exibe entradas listando todas as redes que um roteador está ciente e o melhor caminho para alcançá-los. É muito importante poder ler e compreender as entradas em uma tabela de roteamento.

Nesta demonstração, vamos dar uma olhada em nossa tabela de roteadores IPv4 em detalhes. Mas primeiro, vamos examinar a topologia da rede. Ela realmente consiste em cinco redes separadas, ou sub-redes. Existem quatro LANs para conectá-la a cada roteador e uma conexão WAN entre os dois roteadores.

Se olharmos para R1, ele tem três redes diretamente conectadas: network 192.168.1.0 conectado à interface G0/0/0, network 192.168.2.0 conectado à interface G0/0/1, e à rede 209.165.200.224 conectado à interface S0/1/0. As LANs de R2 não estão diretamente conectadas ao R1, portanto, elas são consideradas redes remotas no que diz respeito a R1. A fim de encaminhar dados para redes remotas, um roteador precisa aprender sobre elas primeiro por meio do uso de roteamento estático ou dinâmico. Neste exemplo, R1 aprendeu sobre elas por meio do protocolo de roteamento dinâmico OSPF que foi configurado em ambos os roteadores.

Para visualizar a tabela de roteamento IPv4, clicamos no roteador R1 e na guia CLI, pressionamos ENTER para conectar-se à linha de comando. A partir daqui, digitamos `enable` e pressionamos enter para entrar no modo exec privilegiado. E daqui em diante, emitimos o comando `show ip route` para visualizar a tabela de roteamento. Pressionando a barra de espaço, vemos a saída completa.

Na parte superior da saída estão os códigos de letra que indicam como cada rota, AKA de rede, foi aprendida. Isso é referido como a origem da rota. Por baixo disso, podemos ver as entradas da tabela de roteamento. Estas representam todas as redes que R1 conhece e a melhor maneira de alcançá-los.

Vamos examinar ainda mais algumas entradas individuais. Primeiro vamos olhar para a entrada para a rede 192.168.1.0. A letra `C` na frente da entrada é a origem da rota e indica que a fonte desta rota é uma rede diretamente conectada. GigabitEthernet0/0/0 é a interface à qual essa rede está conectada.

Agora vamos olhar para a entrada para a rede 10.1.1.0. Esta entrada tem uma origem de rota de `O`, que indica que ela foi aprendida via roteamento OSPF. Após o endereço de rede, você pode ver dois números entre parênteses que são usados pelo roteador para ajudar a determinar o melhor caminho para a rede. O primeiro número é a distância administrativa, que indica a confiabilidade ou classificação de preferência de uma rota sobre outra. Em seguida é a métrica, outro valor usado pelo roteador para ajudar a determinar o melhor caminho. A métrica pode ser calculada usando hopcount, largura de banda, ou algum outro fator. Esta rede pode ser acessada através do próximo endereço de salto, que representa uma interface no roteador R2. Há também um carimbo de data/hora que nos diz há quanto tempo este roteador recebeu pela última vez uma atualização nesta rota. E Serial0/1/0 é a interface de saída em R1 através da qual enviar os pacotes.

Para efeitos desta demonstração, você pode ignorar quaisquer entradas que não listam uma fonte de rota no início. Estas são basicamente títulos. Observe também que, para cada rede diretamente conectada, você tem uma entrada abaixo dela com uma fonte de rota de `L`. `L` refere-se a uma rota local e basicamente este é o endereço IP da interface à qual essa rede está conectada.

Esta tabela de roteamento mostra que R1 está ciente de todas as cinco redes presentes na topologia. Possui três redes diretamente conectadas. Ele tem duas redes que são remotas e foram aprendidas por meio de roteamento OSPF. E por último, se você olhar para a última entrada na tabela, você verá uma rota padrão configurada estaticamente. Esta rota configurada manualmente pode ser usada para encaminhar quaisquer pacotes que não tenham uma entrada específica na tabela de roteamento. A finalidade de uma rota estática padrão é para que o roteador não descarte nenhum pacote. Estes são apenas alguns dos conceitos básicos de uma tabela de roteamento IPv4.


## 32.2.6 Introdução a uma tabela de roteamento IPv4

Observe na figura que R2 está conectado à internet. Portanto, o administrador configurou R1 com uma rota estática padrão enviando pacotes para R2 quando não há nenhuma entrada específica na tabela de roteamento que corresponda ao endereço IP de destino. R1 e R2 também estão usando roteamento OSPF para anunciar redes conectadas diretamente.

![[Pasted image 20260630204545.png]]

```
R1# show ip route
Codes: L - local, C - connected,
       S - static
, R - RIP, M - mobile, B - BGP
       D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
       N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
       E1 - OSPF external type 1, E2 - OSPF external type 2
       i - IS-IS, su - IS-IS summary, L1 - IS-IS level-1, L2 - IS-IS level-2
       ia - IS-IS inter area,
       * - candidate default
, U - per-user static route
       o - ODR, P - periodic downloaded static route, H - NHRP, l - LISP
       a - application route
       + - replicated route, % - next hop override, p - overrides from PfR

Gateway of last resort is 209.165.200.226 to network 0.0.0.0

S*    0.0.0.0/0 [1/0] via 209.165.200.226, GigabitEthernet0/0/1
      10.0.0.0/24 is subnetted, 1 subnets
O       10.1.1.0/24 [110/2] via 209.165.200.226, 00:02:45, GigabitEthernet0/0/1
      192.168.10.0/24 is variably subnetted, 2 subnets, 2 masks
C       192.168.10.1/24 is directly connected, GigabitEthernet0/0/0
L       192.168.10.1/32 is directly connected, GigabitEthernet0/0/0
      209.165.200.0/24 is variably subnetted, 2 subnets, 2 masks
C       209.165.200.224/30 is directly connected, GigabitEthernet0/0/1
L       209.165.200.225/32 is directly connected, GigabitEthernet0/0/1
R1#
```


O comando de modo EXEC privilegiado **show ip route** é usado para exibir a tabela de roteamento IPv4 em um roteador Cisco IOS O exemplo mostra a tabela de roteamento IPv4 do roteador R1. No início de cada entrada de tabela de roteamento é um código que é usado para identificar o tipo de rota ou como a rota foi aprendida. As fontes comuns de rotas (códigos) incluem:

- **L** - Endereço IP da interface local diretamente conectado
- **C** - Rede diretamente conectada
- **S** - A rota estática foi configurada manualmente por um administrador
- **O** - OSPF
- **D** - EIGRP

A tabela de roteamento exibe todas as rotas de destino IPv4 conhecidas para R1.

Uma rota diretamente conectada é criada automaticamente quando uma interface do roteador é configurada com informações de endereço IP e é ativada. O roteador adiciona duas entradas de rota com os códigos **C** (ou seja, a rede conectada) e **L** (ou seja, o endereço IP da interface local da rede conectada). As entradas de rota também identificam a interface de saída a ser usada para alcançar a rede. As duas redes diretamente conectadas neste exemplo são 192.168.10.0/24 e 209.165.200.224/30.

Os roteadores R1 e R2 também estão usando o protocolo de roteamento dinâmico OSPF para trocar informações do roteador. Na tabela de roteamento de exemplo, R1 tem uma entrada de rota para a rede 10.1.1.0/24 que aprendeu dinamicamente do roteador R2 por meio do protocolo de roteamento OSPF.

Uma rota padrão tem um endereço de rede de todos os zeros. Por exemplo, o endereço de rede IPv4 é 0.0.0.0. Uma entrada de rota estática padrão na tabela de roteamento começa com um código de **S***, conforme destacado no exemplo.

## 32.2.7 Verifique sua compreensão - Introdução ao roteamento

**Verifique sua compreensão da introdução ao roteamento escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Qual é o comando usado em um roteador Cisco IOS para exibir a tabela de roteamento?

- [ ] `show routing table`
- [x] `show ip route`
- [ ] `netstart -r`
- [ ] `route print`

✅ RESPOSTA CORRETA: `show ip route`

> O comando `show ip route` é usado para exibir a tabela de roteamento em um roteador Cisco IOS.

---

### Pergunta 2

O que um código de "O" indica ao lado de uma rota na tabela de roteamento?

- [ ] uma rota com uma distância administrativa de 0
- [x] uma rota aprendida dinamicamente do OSPF
- [ ] uma rota diretamente conectada
- [ ] um portal de último recurso

✅ RESPOSTA CORRETA: uma rota aprendida dinamicamente do OSPF

> Os códigos no início de cada entrada da tabela de roteamento são usados para identificar o tipo de rota ou como a rota foi aprendida. Um código "O" indica que a rota foi aprendida no OSPF.

---

### Pergunta 3

Esse tipo de rota também é conhecido como gateway de último recurso.

- [ ] rota diretamente conectada
- [ ] rota estática
- [x] rota padrão
- [ ] rota remota

✅ RESPOSTA CORRETA: rota padrão

> Uma rota padrão também é conhecida como gateway de último recurso.

---

### Pergunta 4

Qual é uma característica das rotas estáticas?

- [ ] Eles são anunciados para vizinhos diretamente conectados.
- [x] Eles são configurados manualmente.
- [ ] Eles são apropriados quando há muitos links redundantes.
- [ ] Eles se ajustam automaticamente a uma alteração na topologia de rede.

✅ RESPOSTA CORRETA: Eles são configurados manualmente.

> As rotas estáticas são configuradas manualmente e não se ajustam às alterações na topologia da rede e não são anunciadas para roteadores vizinhos.

---

### Pergunta 5

Verdadeiro ou falso? Um roteador pode ser configurado com uma combinação de rotas estáticas e um protocolo de roteamento dinâmico.

- [x] Verdadeiro
- [ ] Falso

✅ RESPOSTA CORRETA: Verdadeiro

> Os roteadores podem ser configurados com rotas estáticas e com um protocolo de roteamento dinâmico.

# 32.2 Resumo de Roteamento na camada de rede

## 32.3.1 O que eu aprendi neste módulo?

### Como um host roteia

Um host pode enviar um pacote para si mesmo, outro host local e um host remoto. No IPv4, o dispositivo de origem usa sua própria máscara de sub-rede juntamente com seu próprio endereço IPv4 e o endereço IPv4 de destino para determinar se o host de destino está na mesma rede. No IPv6, o roteador local anuncia o endereço de rede local (prefixo) para todos os dispositivos na rede, para fazer essa determinação. O gateway padrão é o dispositivo de rede (ou seja, roteador) que pode rotear o tráfego para outras redes. Em uma rede, um gateway padrão geralmente é um roteador que tem um endereço IP local no mesmo intervalo de endereços que outros hosts na rede local, pode aceitar dados na rede local e encaminhar dados para fora da rede local e rotear o tráfego para outras redes. Uma tabela de roteamento do host normalmente inclui um gateway padrão. No IPv4, o host recebe o endereço IPv4 do gateway padrão dinamicamente via DHCP ou é configurado manualmente. No IPv6, o roteador anuncia o endereço de gateway padrão ou o host pode ser configurado manualmente. Em um host do Windows, o comando `route print` ou o comando `netstat -r` pode ser usado para exibir a tabela de roteamento do host.

### Tabela de Roteamento

Quando um host envia um pacote para outro host, ele consulta sua tabela de roteamento para determinar para onde enviar o pacote. Se o host de destino estiver em uma rede remota, o pacote será encaminhado para o gateway padrão, que geralmente é o roteador local. O que acontece quando um pacote chega na interface do roteador? O roteador examina o endereço IP de destino do pacote e pesquisa sua tabela de roteamento para determinar para onde encaminhar o pacote. A tabela de roteamento contém uma lista de todos os endereços de rede conhecidos (prefixos) e para onde encaminhar o pacote. Essas entradas são conhecidas como entradas de rota ou rotas. O roteador encaminhará o pacote usando a melhor (mais longa) entrada de rota correspondente.

A tabela de roteamento de um roteador armazena três tipos de entradas de rota: redes conectadas diretamente, redes remotas e uma rota padrão. Os roteadores aprendem sobre redes remotas manualmente ou dinamicamente usando um protocolo de roteamento dinâmico. Rotas estáticas são entradas de rota configuradas manualmente. As rotas estáticas incluem o endereço de rede remota e o endereço IP do roteador de salto seguinte. OSPF e EIGRP são dois protocolos de roteamento dinâmico. O comando de modo EXEC privilegiado `show ip route` é usado para exibir a tabela de roteamento IPv4 em um roteador Cisco IOS. No início de uma tabela de roteamento IPv4 há um código que é usado para identificar o tipo de rota ou como a rota foi aprendida. As fontes comuns de rotas (códigos) incluem:

- **L** – Endereço IP da interface local diretamente conectada
- **C** – Rede conectada diretamente
- **S** – A rota estática foi configurada manualmente por um administrador
- **O** – Abra o caminho mais curto primeiro (OSPF)
- **D** – Protocolo de roteamento de gateway interior aprimorado (EIGRP)

## 32.3.2 Webster – Questões para Reflexão

Talvez você não trabalhe em um hospital, mas se você está aqui agora é porque, como Kishori, você usa computadores e quer saber mais sobre redes.

Você sabia que a Internet é uma enorme rede de redes que são conectadas, direta ou indiretamente, entre si? É como a Rede na qual eu vivo. Uma parte pode ser quebrada, mas a minha Rede não se desfaz; Posso corrigi-la e até fortalecê-la.

Você gostaria de fazer isso pela sua rede?