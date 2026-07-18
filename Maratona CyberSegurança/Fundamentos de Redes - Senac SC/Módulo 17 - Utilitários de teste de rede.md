# 17.0 Introdução

## 17.0.1 Webster - Por que devo fazer este módulo?

Kishori tenta acessar um site usando seu computador desktop em seu posto de enfermagem. Ela recebe uma mensagem de erro ao tentar acessar o site. Ela verifica a conexão com fio, e está tudo bem. Ela usa o laptop para tentar acessar o mesmo site sem sucesso. Na área de trabalho, ela acessa o prompt de comando e envia um ping para um site diferente na Internet. Agora ela percebe que não tem conexão. Ela liga para o departamento de TI. Madhav chega ao posto para investigar o problema. Madhav abre um site pela internet. Kishori explica que já tentou isso. Em seguida, ele envia um ping para o gateway padrão e recebe uma resposta. O roteador está funcionando. É o ISP que está inativo. Madhav está impressionado que Kishori aprendeu muito nos últimos meses. Ele diz a ela que ela deve se candidatar a essa promoção e que ela pode usá-lo como referência!

Você está pronto para aprender alguns comandos para solução de problemas? Continue lendo!

## 17.0.2 O que vou aprender neste módulo?

**Titulo do módulo:** Utilitários de teste de rede

**Objetivo do módulo:** Usar várias ferramentas para testar e solucionar problemas de conectividade de rede.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Comandos para solução de problemas|Solucionar problemas com utilitários de rede.|

# 17.1 Comandos para solução de problemas

## 17.1.1 Visão geral dos comandos de solução de problemas

Existem programas utilitários de software disponíveis que podem ajudar a identificar problemas de rede. A maioria desses utilitários é provida pelo sistema operacional, como comandos de interface da linha de comando (CLI). A sintaxe dos comandos pode variar de acordo com os sistemas operacionais.

Estes são alguns dos utilitários disponíveis:

- **ipconfig** - Exibe informações da configuração IP.
- **ping** - Testa conexões com outros hosts IP.
- **netstat** - Exibe as conexões de rede.
- **tracert** - Exibe a rota percorrida até o destino.
- **nslookup** - consulta diretamente o servidor de nomes para obter informações sobre um domínio de destino.

17.1.2 O comando ipconfig

Quando um dispositivo não tem um endereço IP ou tem uma configuração de IP incorreta, ele não pode se comunicar na rede local nem acessar a Internet. Em dispositivos do Windows, você pode ver informações de configuração de IP com **o comando ipconfigno** prompt de comando. O **comando ipconfig** tem várias opções úteis, incluindo **/all**, **/release**e **/renew**.

**Clique abaixo para ver exemplos do comando ipconfig.**

### ipconfig

O **comando ipconfig** é usado para exibir as informações de configuração de IP atuais de um host. A emissão deste comando a partir do prompt de comando exibirá as informações básicas de configuração, incluindo endereço IP, máscara de sub-rede e gateway padrão.

```
C:\> ipconfig

Windows IP Configuration

Ethernet adapter Ethernet:

   Media State . . . . . . . . . . . : Media disconnected

   Connection-specific DNS Suffix . :

Wireless LAN adapter Wi-Fi:

   Connection-specific DNS Suffix . : lan

   Link-local IPv6 Address . . . . . : fe80 :: a1cc: 4239: d3ab: 2675% 6

   IPv4 Address. . . . . . . . . . . : 10.10.10.130

   Subnet Mask . . . . . . . . . . . : 255.255.255.0

   Default Gateway . . . . . . . . . : 10.10.10.1

C:\>
```


### /all

**ipconfig/all**

O comando **ipconfig /all** exibe informações adicionais que incluem o endereço MAC, os endereços IP do gateway padrão e os servidores DNS. Ele também indica se o DHCP está ativado, o endereço do servidor DHCP e as informações da concessão.

Como esse utilitário ajuda no processo de solução de problemas? Sem uma configuração de IP apropriada, o host não pode participar da comunicação em uma rede. Se o host não souber o local dos servidores DNS, ele não poderá converter nomes em endereços IP.

```
C:\> ipconfig/all

Windows IP Configuration

   Host Name . . . . . . . . . . . . : your-a9270112e3

   Primary Dns Suffix . . . . . . . :

   Node Type . . . . . . . . . . . . : Hybrid

   IP Routing Enabled. . . . . . . . : Não

   WINS Proxy Enabled. . . . . . . . : Não

   DNS Suffix Search List. . . . . . : lan

Ethernet adapter Ethernet:

   Media State . . . . . . . . . . . : Media disconnected

   Connection-specific DNS Suffix . :

   Description . . . . . . . . . . . : Realtek PCIe GBE Family Controller

   Physical Address. . . . . . . . . : 00-16-D4-02-5A-EC

   DHCP Enabled. . . . . . . . . . . : Yes

   Autoconfiguration Enabled . . . . : Yes

Wireless LAN adapter Wi-Fi:

   Connection-specific DNS Suffix . : lan

   Description . . . . . . . . . . . : Intel (R) banda dupla Wireless-AC 3165

   Physical Address. . . . . . . . . : 00-13-02-47-8C-6A

   DHCP Enabled. . . . . . . . . . . : Yes

   Autoconfiguration Enabled . . . . : Yes

   Link-local IPv6 Address . . . . . : fe80 :: a1cc: 4239: d3ab: 2675% 6 (Preferencial)

   IPv4 Address. . . . . . . . . . . : 10.10.10.130 (preferencial)

   Subnet Mask . . . . . . . . . . . : 255.255.255.0

   Lease Obtained. . . . . . . . . . : Wednesday, September 2, 2020 10:03:43 PM

   Lease Expires . . . . . . . . . . : Friday, September 11, 2020 10:23:36 AM

   Default Gateway . . . . . . . . . : 10.10.10.1

   DHCP Server . . . . . . . . . . . : 10.10.10.1

   DHCPv6 IAID . . . . . . . . . . . : 98604135

   DHCPv6 Client DUID. . . . . . . . : 00-01-00-01-1E-21-A5-84-44-A8-42-FC-0D-6F

   DNS Servers . . . . . . . . . . . : 10.10.10.1

   NetBIOS over Tcpip. . . . . . . . : Enabled

C:\>
```


### /release e /renew

**ipconfig /release** e **ipconfig /renew**

Se as informações de endereçamento IP forem atribuídas dinamicamente, o comando **ipconfig /release** liberará as ligações DHCP atuais. **ipconfig /renew** solicitará novas informações de configuração ao servidor DHCP. Um host pode conter informações de configuração de IP desatualizadas ou com falhas. Com uma simples renovação dessas informações, a conectividade pode ser recuperada.

Se, após a liberação da configuração IP o host não puder obter informações atualizadas do servidor DHCP, talvez não haja conectividade de rede. Verifique se a NIC tem uma luz de link acesa, que indica uma conexão física com a rede. Se isso não resolver, talvez exista um problema no servidor DHCP ou nas conexões de rede com o servidor DHCP.

```
C:\> ipconfig/release

Windows IP Configuration

No operation can be performed on Ethernet while it has its media disconnected.

Ethernet adapter Ethernet:

   Media State . . . . . . . . . . . : Media disconnected

   Connection-specific DNS Suffix . :

Wireless LAN adapter Wi-Fi:

   Connection-specific DNS Suffix . :

   Link-local IPv6 Address . . . . . : fe80 :: a1cc: 4239: d3ab: 2675% 6

   Default Gateway . . . . . . . . . :

C:\> ipconfig/renew

Windows IP Configuration

No operation can be performed on Ethernet while it has its media disconnected.

Ethernet adapter Ethernet:

   Media State . . . . . . . . . . . : Media disconnected

   Connection-specific DNS Suffix . :

Wireless LAN adapter Wi-Fi:

   Connection-specific DNS Suffix . : lan

   Link-local IPv6 Address . . . . . : fe80 :: a1cc: 4239: d3ab: 2675% 6

   IPv4 Address. . . . . . . . . . . : 10.10.10.130

   Subnet Mask . . . . . . . . . . . : 255.255.255.0

   Default Gateway . . . . . . . . . : 10.10.10.1

C:\>
```

## 17.1.3 Packet Tracer - Use o comando ipconfig

Nesta atividade, você usará o comando ipconfig para identificar a configuração incorreta em um PC.

> [!example]- 🖧 Recursos do Lab
> - 📄 [[anexos/17.1.3.html|Instruções]]
> - 📥 [[anexos/17.1.3.pka|Abrir no Packet Tracer]]

---
## 17.1.4 O comando ping

Provavelmente, o utilitário de rede mais usado é o ping. A maioria dos dispositivos habilitados para IP oferece suporte a **alguma forma do comando ping** para testar se dispositivos de rede podem ou não ser alcançados através da rede IP.

Se a configuração IP estiver correta no host local, teste a conectividade de rede por meio do ping. O comando **ping** pode ser seguido por um endereço IP ou pelo nome de um host de destino. No exemplo, o usuário faz ping para o gateway padrão em 10.10.10.1 e, em seguida, faz ping para ww​w.cisco.com.

```
C:\> ping 10.10.10.1

Pinging 10.10.10.1 with 32 bytes of data:

Reply from 10.10.10.1: bytes=32 time=1ms TTL=64

Reply from 10.10.10.1: bytes=32 time=1ms TTL=64

Reply from 10.10.10.1: bytes=32 time=1ms TTL=64

Reply from 10.10.10.1: bytes=32 time=1ms TTL=64

Ping statistics for 10.10.10.1:

    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),

Approximate round trip times in milli-seconds:

    Minimum = 1ms, Maximum = 1ms, Average = 1ms

C:\> ping www.cisco.com

Pinging e2867.dsca.akamaiedge.net [104.112.72.241] with 32 bytes of data:

Reply from 104.112.72.241: bytes=32 time=25ms TTL=53

Reply from 104.112.72.241: bytes=32 time=25ms TTL=53

Reply from 104.112.72.241: bytes=32 time=27ms TTL=53

Reply from 104.112.72.241: bytes=32 time=24ms TTL=53

Ping statistics for 104.112.72.241:

    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),

Approximate round trip times in milli-seconds:

    Minimum = 24ms, Maximum = 27ms, Average = 25ms

C:\>
```

Quando um ping é enviado para um endereço IP, um pacote conhecido como echo request é enviado através da rede para o endereço IP especificado. Se o host de destino receber o echo request, ele responderá com um pacote conhecido como echo reply. Se a origem receber o echo reply, a conectividade será verificada pela resposta do endereço IP específico. O ping não é bem-sucedido se uma mensagem como request timed out ou general failure for exibida.

Se um **ping** for enviado para um nome, como ww​w.cisco.com, um pacote será enviado primeiro para um servidor DNS para resolver o nome para um endereço IP. Depois que o endereço IP é obtido, o echo request é encaminhado para o endereço IP e o processo continua. Se um ping for bem-sucedido para o endereço IP, mas não for para o nome, talvez exista um problema com o DNS.

## 17.1.5 Resultados do Ping

Se os comandos **ping** para o nome e o endereço IP forem bem-sucedidos, mas o usuário ainda não conseguir acessar a aplicação, o problema provavelmente estará na aplicação no host de destino. Por exemplo, é possível que o serviço solicitado não esteja funcionando.

Se nenhum ping tiver êxito, a conectividade de rede no caminho até o destino será o problema mais provável. Se isso ocorrer, é comum fazer ping no gateway padrão. Se o ping para o gateway padrão for bem-sucedido, o problema não será local. Se o ping para o gateway padrão falhar, o problema estará na rede local.

Em alguns casos, o ping pode falhar, mas a conectividade de rede não é o problema. Um ping pode falhar devido ao firewall no dispositivo de envio ou recebimento ou a um roteador no caminho que bloqueia os pings.

O comando **ping** básico geralmente envia quatro ecos e espera as respostas de cada um. Entretanto, ele pode ser modificado para aumentar sua utilidade. As opções listadas na figura mostram os recursos adicionais disponíveis.


```
C:\> ping

Usage: ping [-t] [-a] [-n count] [-l size] [-f] [-i TTL] [-v TOS]

            [-r count] [-s count] [[-j host-list] | [-k host-list]]

            [-w timeout] [-R] [-S srcaddr] [-c compartment] [-p]

            [-4] [-6] target_name

Options:

    -t             Ping the specified host until stopped.

                   To see statistics and continue - type Control-Break;

                   To stop - type Control-C.

    -a             Resolve addresses to hostnames.

    -n count       Number of echo requests to send.

    -l size        Send buffer size.

    -f             Set Don't Fragment flag in packet (IPv4-only).

    -i TTL         Time To Live.

    -v TOS         Type Of Service (IPv4-only. This setting has been deprecated

                   and has no effect on the type of service field in the IP

                   Header).

    -r count       Record route for count hops (IPv4-only).

    -s count       Timestamp for count hops (IPv4-only).

    -j host-list   Loose source route along host-list (IPv4-only).

    -k host-list   Strict source route along host-list (IPv4-only).

    -w timeout     Timeout in milliseconds to wait for each reply.

    -R             Use routing header to test reverse route also (IPv6-only).

                   Per RFC 5095 the use of this routing header has been

                   deprecated. Some systems may drop echo requests if

                   deprecated. Some systems may drop echo requests if

    -S srcaddr     Source address to use.

    -c compartment Routing compartment identifier.

    -p             Ping a Hyper-V Network Virtualization provider address.

    -4             Force using IPv4.

    -6             Force using IPv6.

C:\>
```

## 17.1.6 Packet Tracer – Uso do comando ping

Nesta atividade, você usará o comando **ping** para identificar uma configuração incorreta em um PC.

> [!example]- 🖧 Recursos do Lab
> - 📄 [[anexos/17.1.6.html|Instruções]]
> - 📥 [[anexos/17.1.6.pka|Abrir no Packet Tracer]]

---
# 17.2. Resumo das Network Testing Utilities

## 17.2.1 O que aprendi neste módulo?

### Comandos para solução de problemas

Vários softwares utilitários estão disponíveis para ajudar a identificar problemas de rede. A maioria desses utilitários é fornecida pelo sistema operacional como comandos da CLI.

Estes são alguns dos utilitários disponíveis:

- **ipconfig** - Exibe informações da configuração IP.
- **ping** - Testa conexões com outros hosts IP.
- **netstat** - Exibe as conexões de rede.
- **tracert** - Exibe a rota percorrida até o destino.
- **nslookup** - consulta diretamente o servidor de nomes para obter informações sobre um domínio de destino.

O **comando ipconfig** é usado para exibir as informações de configuração de IP atuais de um host. A emissão deste comando a partir do prompt de comando exibirá as informações básicas de configuração, incluindo endereço IP, máscara de sub-rede e gateway padrão.

O comando **ipconfig /all** exibe informações adicionais que incluem o endereço MAC, os endereços IP do gateway padrão e os servidores DNS. Ele também indica se o DHCP está ativado, o endereço do servidor DHCP e as informações da concessão.

Se as informações de endereçamento IP forem atribuídas dinamicamente, o comando **ipconfig /release** liberará as ligações DHCP atuais. **ipconfig /renew** solicitará novas informações de configuração ao servidor DHCP. Um host pode conter informações de configuração de IP desatualizadas ou com falhas. Com uma simples renovação dessas informações, a conectividade pode ser recuperada.

Provavelmente, o utilitário de rede mais usado é o ping. A maioria dos dispositivos habilitados para IP oferece suporte a **alguma forma do comando ping** para testar se dispositivos de rede podem ou não ser alcançados através da rede IP. Quando um ping é enviado para um endereço IP, um pacote conhecido como echo request é enviado através da rede para o endereço IP especificado. Se o host de destino receber o echo request, ele responderá com um pacote conhecido como echo reply. Se a origem receber o echo reply, a conectividade será verificada pela resposta do endereço IP específico.


## 17.2.2 Webster - Perguntas para reflexão

Parabéns! Você fez todo o caminho através deste curso! No primeiro módulo deste curso, mencionei que posso solucionar problemas e consertar minha web. Na verdade, posso até torná-la mais sólida e mais segura. Ser capaz de fazer isso é muito gratificante. Você aprendeu sobre os muitos comandos que pode usar para solucionar problemas e corrigir sua própria rede. Você pode usar esses comandos para investigar sua rede, mesmo se ela estiver funcionando como deveria. Com quais comandos você começaria?