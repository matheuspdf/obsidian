
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