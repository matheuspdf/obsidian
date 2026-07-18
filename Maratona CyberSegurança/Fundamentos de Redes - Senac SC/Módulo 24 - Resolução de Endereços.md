
# 24.0 Introdução

## 24.0.1 Webster - Por que devo fazer este módulo?

Webster aqui novamente! Eu tenho outra amiga para apresentar a você. O nome dela é Olcay. Olcay é uma profissional de IT em uma empresa de energia na Turquia. Ela está orientando um novo funcionário chamado Abay. Abay vai acompanhar a Olcay durante o próximo mês para se tornar mais eficiente em redes na empresa de energia. Olcay pergunta a Abay o que ele sabe sobre a resolução de endereços. O Abay sabe que para enviar um pacote para outro host na mesma rede IPv4 local, um host deve conhecer o endereço IPv4 e o endereço MAC do dispositivo de destino. Um dispositivo usa ARP para determinar o endereço MAC de destino de um dispositivo local quando conhece seu endereço IPv4.

Se Abay quiser ser bem-sucedido em seu novo emprego, ele precisa aprender um pouco mais e você também! Sugiro fazer este módulo sobre Resolução de Endereços.

## 24.0.2 O que vou aprender neste módulo?

**Titulo do módulo:** Resolução de endereços

**Objetivo do módulo:** Explicar como o ARP permite a comunicação em uma rede local.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|ARP|Descrever a finalidade do ARP.|

# 24.1 ARP

## 24.1.1 Visão geral do ARP

Se sua rede estiver usando o protocolo de comunicações IPv4, o Protocolo de Resolução de Endereços ou ARP é o que você precisa para mapear endereços IPv4 para endereços MAC. Este tópico explica como o ARP funciona.

Cada dispositivo IP em uma rede Ethernet tem um endereço MAC Ethernet exclusivo. Quando um dispositivo envia um quadro Ethernet Layer 2, ele contém estes dois endereços:

- **Endereço MAC de destino** - O endereço MAC Ethernet do dispositivo de destino no mesmo segmento de rede local. Se o host de destino estiver em outra rede, o endereço de destino no quadro será o do gateway padrão (ou seja, roteador).
- **Endereço MAC de origem** - O endereço MAC da Ethernet NIC no host de origem.

A figura ilustra o problema ao enviar um quadro para outro host no mesmo segmento em uma rede IPv4.

![[Pasted image 20260619070332.png]]

Para enviar um pacote para outro host na mesma rede IPv4 local, um host deve saber o endereço IPv4 e o endereço MAC do dispositivo de destino. Os endereços IPv4 de destino do dispositivo são conhecidos ou resolvidos pelo nome do dispositivo. No entanto, os endereços MAC devem ser descobertos.

Um dispositivo utiliza o protocolo ARP (Address Resolution Protocol) para determinar o endereço MAC de destino de um dispositivo local quando conhece o endereço IPv4.

O ARP fornece duas funções básicas:

- Resolução de endereços IPv4 em endereços MAC
- Manter uma tabela de mapeamentos de endereços IPv4 para MAC


## 24.1.2 Funções ARP

Quando um pacote é enviado à camada de enlace de dados para ser encapsulado em um quadro Ethernet, o dispositivo consulta uma tabela em sua memória para encontrar o endereço MAC que é mapeado para o endereço IPv4. Esta tabela é armazenada temporariamente na memória RAM e denominada tabela ARP ou cache ARP.

O dispositivo emissor pesquisará em sua tabela ARP um endereço IPv4 destino correspondente a um endereço MAC.

- Se o endereço IPv4 destino do pacote estiver na mesma rede que o endereço IPv4 origem, o dispositivo pesquisará o endereço IPv4 destino na tabela ARP.
- Se o endereço IPv4 destino do pacote estiver em uma rede diferente do endereço IPv4 origem, o dispositivo pesquisará o endereço IPv4 do gateway padrão na tabela ARP.

Nos dois casos, a pesquisa é por um endereço IPv4 e um endereço MAC correspondente para o dispositivo.

Cada entrada (linha) da tabela ARP vincula um endereço IPv4 a um endereço MAC. Chamamos a relação entre os dois valores de um mapa. Isso significa simplesmente que você pode localizar um endereço IPv4 na tabela e descobrir o endereço MAC correspondente. A tabela ARP salva (armazena em cache) temporariamente o mapeamento dos dispositivos da LAN.

Se o dispositivo localizar o endereço IPv4, seu endereço MAC correspondente será usado como endereço MAC de destino no quadro. Se nenhuma entrada for encontrada, o dispositivo enviará uma requisição ARP.

**Clique em reproduzir na figura para ver uma animação da função ARP.**
![[brave_MDXJtXsyf0.mp4]]
## 24.1.3 Vídeo - Operação ARP - Solicitação ARP
![[24.1.3.mp4#subtitle=anexos/24.1.3.vtt]]
Uma solicitação ARP é enviada quando um dispositivo precisa determinar o endereço MAC associado a um endereço IPv4 e não possui uma entrada para o endereço IPv4 em sua tabela ARP.

As mensagens do ARP são encapsuladas diretamente em um quadro Ethernet. Não há cabeçalho IPv4. A requisição ARP é encapsulada em um quadro Ethernet usando as seguintes informações de cabeçalho:

- **Endereço MAC de destino** – Este é um endereço de broadcast FF-FF-FF-FF-FF-FF que requer todos os NICs Ethernet na LAN para aceitar e processar a solicitação ARP.
- **Endereço MAC de origem** - Este é o endereço MAC do remetente da solicitação ARP.
- **Tipo** - As mensagens ARP têm um campo de tipo de 0x806. Ele informa à NIC de recebimento que a parte de dados do quadro precisa ser transferida para o processo ARP.

Como as solicitações de ARP são transmissões, elas são inundadas em todas as portas pelo switch, exceto a porta de recebimento. Todas as NICs Ethernet no processo de LAN transmite e devem entregar a solicitação ARP ao seu sistema operacional para processamento. Cada dispositivo deve processar a requisição ARP para ver se o endereço IPv4 destino corresponde ao seu. Um roteador não encaminhará broadcasts pelas outras interfaces.

Somente um dispositivo na LAN terá um endereço IPv4 correspondente ao endereço IPv4 na requisição ARP. Nenhum outro dispositivo responderá.

**Selecione o botão Reproduzir para assistir ao vídeo.**

Neste vídeo, vamos ver o PC A enviando solicitação ARP para o endereço MAC do PC C.

O PC A tem um pacote IP, com o endereço IP de origem de si mesmo, `192.168.1.110`, e o endereço IP de destino do PC C, `192.168.1.50`. Então ele precisa saber qual será o endereço MAC de destino.

Como os endereços IP de origem e destino estão na mesma rede, o endereço MAC de destino será o do dispositivo com o endereço IP de destino do PC C, `192.168.1.50`.

Então o PC A verifica seu cache ARP para o endereço IP `192.168.1.50`. Como não está no cache de ARP, ele vai colocar o pacote em espera e criar uma solicitação ARP.

A solicitação ARP contém o endereço IPv4 de destino. Este é o endereço IPv4 conhecido pelo PC A, e o endereço MAC de destino, que é desconhecido. Isso é o que o PC-A está tentando descobrir.

A solicitação ARP é enviada como broadcast, para que todos na rede precisem examinar se isso está no quadro e processar a solicitação ARP. Então o PC A envia para o switch, porque se houver um broadcast, o switch o enviará por todas as portas, exceto a porta pela qual ele entrou.

O PC B recebe o broadcast, por isso deve processá-lo, e seu processo ARP examina a solicitação ARP. Compara seu próprio endereço IPv4 contra o endereço IPv4 de destino, e percebe que eles não são os mesmos, assim não é preciso enviar uma resposta ARP.

O roteador R1 também recebe essa solicitação ARP. Seu processo ARP examina seu próprio endereço IPv4 e o compara ao endereço IPv4 de destino, e também percebe que esse não é seu endereço IPv4, então ele não precisa enviar a resposta ARP. A propósito, os roteadores não inundarão solicitações ARP por outras portas.

O PC-C recebe a solicitação ARP, compara seu endereço IPv4 em relação ao endereço IPv4 de destino e percebe que é o destino pretendido da solicitação ARP, que o endereço IPv4 de destino corresponde ao seu próprio endereço IPv4. Então o PC-C precisará enviar uma resposta ARP.


## 24.1.4 Vídeo - Operação do ARP - Resposta do ARP
![[24.1.4.mp4#subtitle=anexos/24.1.4.vtt]]
Somente o dispositivo com o endereço IPv4 de destino associado à solicitação ARP responderá com uma resposta ARP. A resposta de ARP é encapsulada em um quadro Ethernet com as seguintes informações de cabeçalho:

- **Endereço MAC de destino** - Este é o endereço MAC do remetente da solicitação ARP.
- **Endereço MAC de origem** - Este é o endereço MAC do remetente da resposta ARP.
- **Tipo** - As mensagens ARP têm um campo de tipo de 0x806. Ele informa à NIC de recebimento que a parte de dados do quadro precisa ser transferida para o processo ARP.

Apenas o dispositivo que enviou originalmente uma requisição ARP receberá a resposta ARP unicast. Depois que a resposta do ARP é recebida, o dispositivo adiciona o endereço IPv4 e o endereço MAC correspondente à sua tabela ARP. Agora os pacotes destinados a esse endereço IPv4 podem ser encapsulados em quadros com o endereço MAC correspondente.

Se nenhum dispositivo responder à requisição ARP, o pacote será descartado porque não será possível criar um quadro.

As entradas na tabela ARP têm carimbo de data/hora (timestamp). Se um dispositivo não receber um quadro de um dispositivo específico antes que o carimbo de data / hora expire, a entrada desse dispositivo será removida da tabela ARP.

Além disso, entradas de mapa estáticas podem ser inseridas em uma tabela ARP, mas isso é raro. As entradas estáticas na tabela ARP não expiram com o tempo e devem ser removidas manualmente.

**Nota**: O IPv6 usa um processo semelhante ao ARP para IPv4, conhecido como ICMPv6 Neighbour Discovery (ND). O IPv6 usa mensagens de requisição e de anúncio de vizinho, semelhantes a solicitações ARP e respostas ARP no IPv4.

**Selecione o botão Reproduzir para assistir ao vídeo.**

No vídeo anterior, vimos uma solicitação de ARP do PC-A procurando o endereço MAC do PC-C. Neste vídeo, veremos a resposta ARP em resposta àquela solicitação ARP.

O PC-C, quando recebeu a solicitação ARP, examinou o endereço IPv4 de destino e comparou com o próprio endereço IPv4, e sabe que era o alvo pretendido. Assim o PC-C vai gerar uma resposta ARP em resposta àquela solicitação ARP.

A resposta do ARP inclui seu próprio endereço IPv4 e seu próprio endereço MAC. É enviado para o PC-A. As respostas do ARP são enviadas como unicast, portanto, o endereço MAC de destino é o do PC-A.

PC-A recebe a resposta do ARP em resposta à sua solicitação ARP anterior. Ele leva as informações, o endereço IPv4 do remetente e o endereço MAC do remetente, e adiciona essas informações ao seu cache ARP.

O PC-A agora pode receber o pacote, o pacote original destinado ao PC-C, tirar esse pacote da espera e ter as informações de que necessita para enviar esse pacote para o PC-C. Então, ele pega as informações do cache do ARP, o endereço MAC, e adiciona isso ao cabeçalho ethernet como o endereço MAC de destino.

PC-A agora pode encaminhar este pacote no quadro ethernet apropriado para PC-C.


## 24.1.5 Vídeo - Função ARP nas comunicações remotas

![[24.1.5.mp4#subtitle=anexos/24.1.5.vtt]]
Quando o endereço IPv4 destino não está na mesma rede que o endereço IPv4 origem, o dispositivo de origem precisa enviar o quadro para o gateway padrão. Essa é a interface do roteador local. Sempre que um dispositivo de origem tiver um pacote com um endereço IPv4 em outra rede, ele encapsulará esse pacote em um quadro usando o endereço MAC de destino do roteador.

O endereço IPv4 do gateway padrão é armazenado na configuração IPv4 dos hosts. Quando um host cria um pacote para um destino, ele compara o endereço IPv4 destino e seu próprio endereço IPv4 para determinar se os dois endereços IPv4 estão localizados na mesma rede de Camada 3. Se o host de destino não estiver na mesma rede, a origem usará a tabela ARP para obter uma entrada com o endereço IPv4 do gateway padrão. Se não houver uma entrada, ela usará o processo de ARP para determinar um endereço MAC do gateway padrão.

**Selecione o botão Reproduzir para assistir ao vídeo.**

Neste vídeo, o PC-A tem um pacote IP, o endereço IP de origem em si, `192.168.1.110`, e o endereço IP de destino `10.1.1.10`, que é um endereço IP em uma rede remota.

O endereço MAC de destino será o do gateway padrão: `192.168.1.1`, o roteador R1, nesse caso.

O PC-A verifica o cache de ARP do endereço IP `192.168.1.1`, e não há entrada com um endereço MAC. Ele coloca o pacote em retenção e cria uma solicitação ARP.

A solicitação ARP tem o endereço IP do roteador `192.168.1.1`, e o endereço MAC é desconhecido. O endereço MAC de destino de uma solicitação ARP é um broadcast, então ele será enviado para o switch, e o switch enviará por todas as portas, exceto pela porta de entrada.

O PC-B compara seu próprio endereço IPv4 em relação ao endereço IPv4 de destino na solicitação ARP, e percebe que não há correspondência, então esse não é o destino pretendido.

O PC-C recebe a solicitação ARP, compara seu próprio endereço IPv4 contra o endereço IPv4 de destino, e também não é o destino pretendido.

O roteador R1 recebe a solicitação ARP, compara seu endereço IPv4 em relação ao endereço IPv4 de destino, e dessa vez é uma correspondência. É o destino da solicitação ARP. Assim o roteador R1 emitirá uma resposta ARP.

Ela incluirá seu próprio endereço MAC, `00-0D`, juntamente com seu endereço IPv4. O endereço MAC de destino da resposta ARP é unicamente direcionado para PC-A. Assim, é um endereço MAC de destino de `00-0A`, e o PC-A recebe a resposta ARP.

PC-A recebe a resposta do ARP em resposta para sua solicitação ARP, vê o endereço IPv4 de destino e o endereço MAC de destino e adiciona-o ao cache ARP. Agora ele tem as informações necessárias para encaminhar o pacote que está em espera.

Assim, o endereço MAC de destino agora será `00-0D`, o do roteador R1, seu endereço MAC. E agora o PC-A pode encaminhar o quadro.


## 24.1.6 Remoção de Entradas de uma Tabela ARP

Em cada dispositivo, um temporizador da cache ARP remove entradas ARP que não tenham sido usadas durante um determinado período. Os horários diferem dependendo do sistema operacional do dispositivo. Por exemplo, os sistemas operacionais Windows mais recentes armazenam entradas da tabela ARP entre 15 e 45 segundos, conforme ilustrado na figura.

![[Pasted image 20260619070757.png]]
Os comandos também podem ser usados para remover manualmente algumas ou todas as entradas na tabela ARP. Após a remoção de uma entrada, o processo de envio de uma requisição ARP e de recebimento de uma resposta ARP deve ocorrer novamente para inserir o mapa na tabela ARP.


## 24.1.7 Tabelas ARP nos dispositivos

Em um roteador Cisco, o comando **show ip arp** é usado para exibir a tabela ARP, conforme mostrado na figura.

```
R1# show ip arp
Protocol  Address           Age (min)  Hardware Addr   Type  Interface
Internet  192.168.10.1      -          a0e0.af0d.e140   ARPA  GigabitEthernet0/0/0
Internet  209.165.200.225   -          a0e0.af0d.e141   ARPA  GigabitEthernet0/0/1
Internet  209.165.200.226   1          a03d.6fe1.9d91   ARPA  GigabitEthernet0/0/1
R1#
```

Em um PC com Windows 10, o comando **arp -a** é usado para exibir a tabela ARP, conforme mostrado na figura.

```
C:\Users\PC> arp -a
Interface: 192.168.1.124 --- 0x10
Internet Address    Physical Address      Type
192.168.1.1          c8-d7-19-cc-a0-86     dynamic
192.168.1.101         08-3e-0c-f5-f7-77     dynamic
192.168.1.110         08-3e-0c-f5-f7-56     dynamic
192.168.1.112         ac-b3-13-4a-bd-d0     dynamic
192.168.1.117         08-3e-0c-f5-f7-5c     dynamic
192.168.1.126         24-77-03-45-5d-c4     dynamic
192.168.1.146         94-57-a5-0c-5b-02     dynamic
192.168.1.255         ff-ff-ff-ff-ff-ff     static
224.0.0.22            01-00-5e-00-00-16     static
224.0.0.251           01-00-5e-00-00-fb     static
239.255.255.250       01-00-5e-7f-ff-fa     static
255.255.255.255       ff-ff-ff-ff-ff-ff     static
C:\Users\PC>
```


## 24.1.8 Problemas de ARP - broadcast de ARP e falsificação de ARP

Como um quadro broadcast, uma requisição ARP é recebida e processada por todos os dispositivos na rede local. Em uma rede corporativa típica, esses broadcasts provavelmente teriam impacto mínimo no desempenho da rede. No entanto, se um grande número de dispositivos precisasse ser ligado e todos começassem a acessar serviços de rede ao mesmo tempo, poderia haver alguma redução no desempenho por um curto período, como mostra a figura. Depois que os dispositivos enviarem os broadcasts ARP iniciais e tiverem reconhecido os endereços MAC necessários, qualquer impacto na rede será minimizado.

![[Pasted image 20260619070857.png]]

Em alguns casos, o uso do ARP pode levar a um risco potencial à segurança. Um ator de ameaça pode usar falsificação ARP para realizar um ataque de envenenamento por ARP. Esta é uma técnica usada por um ator de ameaça para responder a uma solicitação ARP de um endereço IPv4 que pertence a outro dispositivo, como o gateway padrão, conforme mostrado na figura. O agente da ameaça envia uma resposta ARP com seu próprio endereço MAC. O destinatário da resposta ARP adicionará o endereço MAC errado à sua tabela ARP e enviará esses pacotes ao agente de ameaça.  
Switches de nível corporativo incluem técnicas de mitigação conhecidas como inspeção dinâmica ARP (DAI). A DAI não faz parte do escopo deste curso.

![[Pasted image 20260619070913.png]]
## 24.1.9 Packet Tracer – Exame da Tabela ARP

Nesta atividade do Packet Tracer, você atingirá os seguintes objetivos:

- Examinar uma Requisição ARP
- Examinar a Tabela de Endereços MAC de um Switch
- Examinar o Processo ARP em Comunicações Remotas

Esta atividade é otimizada para a visualização de PDUs. Os dispositivos já estão configurados. Você reunirá informações das PDUs no modo de simulação e responderá a uma série de perguntas sobre os dados coletados.

### Packet Tracer – Exame da Tabela ARP

#### Tabela de Endereçamento

<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed; word-wrap:break-word;"> <tr> <th>Dispositivo</th> <th>Interface</th> <th>Endereço MAC</th> <th>Interface do Switch</th> </tr> <tr> <td>Router0</td> <td>Gg0/0</td> <td>0001.6458.2501</td> <td>G0/1</td> </tr> <tr> <td>Router0</td> <td>S0/0/0</td> <td>N/D</td> <td>N/D</td> </tr> <tr> <td>Router1</td> <td>G0/0</td> <td>00E0.F7B1.8901</td> <td>G0/1</td> </tr> <tr> <td>Router1</td> <td>S0/0/0</td> <td>N/D</td> <td>N/D</td> </tr> <tr> <td>10.10.10.2</td> <td>Rede Sem Fio</td> <td>0060.2F84.4AB6</td> <td>F0/2</td> </tr> <tr> <td>10.10.10.3</td> <td>Rede Sem Fio</td> <td>0060.4706.572B</td> <td>F0/2</td> </tr> <tr> <td>172.16.31.2</td> <td>F0</td> <td>000C.85CC.1DA7</td> <td>F0/1</td> </tr> <tr> <td>172.16.31.3</td> <td>F0</td> <td>0060.7036.2849</td> <td>F0/2</td> </tr> <tr> <td>172.16.31.4</td> <td>G0</td> <td>0002.1640.8D75</td> <td>F0/3</td> </tr> </table>

#### Objetivos

Parte 1: Examinar uma Requisição ARP

Parte 2: Examinar a Tabela de Endereços MAC de um Switch

Parte 3: Examinar o Processo ARP em Comunicações Remotas

#### Histórico

Esta atividade é otimizada para a visualização de PDUs. Os dispositivos já estão configurados. Você reunirá informações das PDUs no modo de simulação e responderá a uma série de perguntas sobre os dados coletados.

#### Instruções

##### Parte 1: Examinar uma Requisição ARP

###### Etapa 1: Gere requisições ARP enviando ping para 172.16.31.2 de 172.16.31.3.

a. Clique em 172.16.31.2 e abra o Command Prompt (Prompt de Comando).

b. Digite o comando arp -d para limpar a tabela ARP.

c. Entre no modo Simulation (Simulação) e insira o comando ping 172.16.31.3. Serão geradas duas PDUs. O comando ping não pode completar o pacote ICMP sem saber o endereço MAC de destino. Por isso, o computador envia um quadro broadcast ARP para localizar o endereço MAC destino.

d. Clique uma vez em Capture/Forward (Capturar/Encaminhar). A PDU ARP se moverá para Switch1 quando a PDU do ICMP desaparecer, aguardando a resposta ARP. Abra a PDU e registre o endereço MAC de destino.

**Pergunta:** O endereço está listado na tabela acima?

**Resposta:** Não

e. Clique em Capture/Forward (Capturar/Encaminhar) para mover a PDU para o próximo dispositivo.

**Pergunta:** Quantas cópias da PDU o Switch1 fez?

**Resposta:** 3

**Pergunta:** Qual é o endereço IP do dispositivo que aceitou a PDU?

**Resposta:** 172.16.31.3

f. Abra a PDU e examine a Camada 2.

**Pergunta:** O que aconteceu com os endereços MAC de origem e de destino?

**Resposta:** A origem tornou-se o destino; FFFF.FFFF.FFFF foi transformado no endereço MAC 172.16.31.3

g. Clique em Capture/Forward (Capturar/Encaminhar) até que a PDU retorne para 172.16.31.2.

**Pergunta:** Quantas cópias da PDU o switch fez durante a resposta ARP?

**Resposta:** 1

###### Etapa 2: Examinar a tabela ARP.

a. Observe que o pacote ICMP será exibido novamente. Abra a PDU e examine os endereços MAC.

**Pergunta:** Os endereços MAC origem e destino estão alinhados aos respectivos endereços IP?

**Resposta:** Sim

b. Volte para o modo Realtime (Tempo real) e o ping será concluído.

c. Clique em 172.16.31.2 e insira o comando arp –a.

**Pergunta:** A qual endereço IP corresponde a entrada do endereço MAC?

**Resposta:** 172.16.31.3

**Pergunta:** Em geral, quando um dispositivo final envia uma requisição ARP?

**Resposta:** Quando não sabe o endereço MAC do receptor.

##### Parte 2: Examinar a Tabela de Endereços MAC de um Switch

###### Etapa 1: Gerar tráfego adicional para preencher a tabela de endereços MAC do switch.

a. Em 172.16.31.2, insira o comando ping 172.16.31.4.

b. Clique em 10.10.10.2 e abra o Prompt de Comando.

c. Insira o comando ping 10.10.10.3.

**Pergunta:** Quantas respostas foram enviadas e recebidas?

**Resposta:** 4 enviadas, 4 recebidas.

###### Etapa 2: Examinar a tabela de endereços MAC nos switches.

a. Clique em Switch1 e depois na guia CLI. Insira o comando show mac-address-table.

**Pergunta:** As entradas correspondem às da tabela acima?

**Resposta:** Sim

b. Clique em Switch0 e depois na guia CLI. Insira o comando show mac-address-table.

**Perguntas:** As entradas correspondem às da tabela acima?

**Resposta:** Sim

**Pergunta:** Por que dois endereços MAC estão associados a uma porta?

**Resposta:** Porque ambos os dispositivos estão conectados a uma porta por meio do Access Point.

##### Parte 3: Examinar o Processo ARP em Comunicações Remotas

###### Etapa 1: Gerar tráfego para produzir tráfego ARP.

a. Clique em 172.16.31.2 e abra o Prompt de Comando.

b. Insira o comando ping 10.10.10.1.

c. Digite arp –a.

**Pergunta:** Qual é o endereço IP da nova entrada da tabela ARP?

**Resposta:** 172.16.31.1

d. Insira arp -d para limpar a tabela ARP e mude para o modo Simulation (Simulação).

e. Repita o ping para 10.10.10.1.

**Pergunta:** Quantas PDUs são exibidas?

**Resposta:** 2

f. Clique em Capture/Forward (Capturar/Encaminhar). Clique na PDU que agora está em Switch1.

**Pergunta:** Qual é o endereço IP destino da requisição ARP?

**Resposta:** 172.16.31.1

g. O endereço IP destino não é 10.10.10.1.

**Pergunta:** Por quê?

**Resposta:** O endereço de gateway da interface do roteador é armazenado na configuração IPv4 dos hosts. Se o host de recebimento não estiver na mesma rede, a origem usará o processo de ARP para determinar um endereço MAC para a interface do roteador que serve como gateway.

###### Etapa 2: Examinar a tabela ARP em Router1.

a. Alterne para o modo Realtime (Tempo real). Clique em Router1 e depois na guia CLI.

b. Entre no modo EXEC privilegiado e insira o comando show mac-address-table.

**Pergunta:** Quantos endereços MAC há na tabela? Por quê?

**Resposta:** Zero. Este comando significa algo completamente diferente do que o comando switch show mac address-table.

c. Insira o comando show arp.

**Perguntas:** Existe uma entrada para 172.16.31.2?

**Resposta:** Sim

**Pergunta:** O que acontece com o primeiro ping em uma situação em que o roteador responde à requisição ARP?

**Resposta:** O tempo expirou.


## 24.1.10 Laboratório - Visualizar tráfego ARP no Wireshark

Nesta atividade, você completará os seguintes objetivos:

- Parte 1: Capturar e analisar dados ARP no Wireshark
- Parte 2: Visualizar as entradas do cache ARP no PC

### Laboratório - Visualizar tráfego ARP no Wireshark

#### Objetivos

##### Parte 1: Capturar e analisar dados ARP no Wireshark

- Inicie e interrompa a captura de dados do tráfego de ping para os hosts remotos.
- Localize as informações sobre o endereço IPv4 e MAC em PDUs capturadas.
- Analise o conteúdo das mensagens ARP trocadas entre os dispositivos na LAN.

##### Parte 2: Visualizar as entradas do cache ARP no PC

- Acesse o Prompt de Comando do Windows.
- Use o comando arp do Windows para visualizar o cache da tabela ARP local no PC.

#### Histórico / Cenário

O protocolo ARP é usado pelo TCP/IP para mapear um endereço IPv4 da Camada 3 para um endereço MAC da Camada 2. Quando um quadro Ethernet é transmitido na rede, ele deve ter um endereço MAC de destino. Para encontrar de forma dinâmica o endereço MAC de um destino conhecido, um dispositivo de origem transmite uma solicitação ARP na rede local. O dispositivo configurado com o endereço IPv4 de destino responde para a solicitação com uma resposta ARP e o endereço MAC é registrado no cache ARP.

Todos os dispositivos na LAN mantêm seu próprio cache ARP. O cache ARP é uma pequena área na memória RAM que armazena as respostas ARP. A visualização do cache ARP em um PC exibirá o endereço IPv4 e o endereço MAC de cada dispositivo na LAN com a qual o PC trocou mensagens ARP.

O Wireshark é um software analisador de protocolo, ou "packet sniffer", usado em solução de problemas de rede, análise, desenvolvimento de software e protocolo, e educação. À medida que o fluxo de dados trafega em uma rede, o sniffer "captura" cada unidade de dados de protocolo (PDU) e pode decodificar e analisar seu conteúdo de acordo com as especificações adequadas do protocolo.

O Wireshark é uma ferramenta útil para quem trabalha com redes e pode ser usado, na maioria dos laboratórios dos cursos da Cisco, para análise de dados e solução de problemas. Este laboratório apresenta instruções para baixar e instalar o Wireshark, embora talvez já esteja instalado. Neste laboratório, você usará o Wireshark para capturar trocas de mensagens ARP na rede local.

#### Recursos necessários

- 1 PC (Escolha do sistema operacional com o Wireshark instalado)
- PCs ou dispositivos móveis adicionais em uma rede local (LAN) podem ser usados para responder a solicitações de ping. Caso não haja outros PCs na LAN, o endereço de gateway padrão será usado para responder às solicitações de ping.

#### Instruções

##### Parte 1: Capturar e analisar dados locais ARP no Wireshark

Nesta parte, você efetuará ping para outro computador na LAN e capturará solicitações e respostas ARP no Wireshark. Você também verá quadros capturados para obter informações específicas. Essa análise ajudará a esclarecer como os cabeçalhos dos pacotes são usados para transportar os dados até o destino.

Observação: as instruções foram escritas para PCs que executam o sistema operacional Windows para referência.

###### Etapa 1: Consulte os endereços de interface do PC.

Neste laboratório, você precisará consultar o endereço IPv4 e o endereço MAC do PC. (O comando ifconfig para Linux e MAC OS pode fornecer resultados semelhantes.)

a. Navegue para a janela de prompt de comando, digite `ipconfig /all` at the prompt.

b. Observe qual adaptador de rede o PC está usando para acessar a rede. Anote o endereço IPv4 e o endereço MAC (endereço físico) da interface do PC.

```
C:\Users\Student> ipconfig /all

<output omitted>

Wireless LAN adapter Wireless Network Connection:

   Connection-specific DNS Suffix  . :

   Description . . . . . . . . . . . : Intel(R) Centrino(R) Advanced-N 6205

   Physical Address. . . . . . . . . : A4-AE-31-AD-78-4C

   DHCP Enabled. . . . . . . . . . . : Yes

   Autoconfiguration Enabled . . . . : Yes

   Link-local IPv6 Address . . . . . : fe80::f9e7:e41d:a772:f993%11(Preferred)

   IPv4 Address. . . . . . . . . . . : 192.168.1.8(Preferred)

   Subnet Mask . . . . . . . . . . . : 255.255.255.0

   Lease Obtained. . . . . . . . . . : Thursday, August 04, 2016 05:35:35 PM

   Lease Expires . . . . . . . . . . : Friday, August 05, 2016 05:35:35 PM

   Default Gateway . . . . . . . . . : 192.168.1.1

   DHCP Server . . . . . . . . . . . : 192.168.1.1

   DHCPv6 IAID . . . . . . . . . . . : 245648945

   DHCPv6 Client DUID. . . . . . . . : 00-01-00-01-1B-87-BF-52-A4-4E-31-AD-78-4C

   DNS Servers . . . . . . . . . . . : 192.168.1.1

   NetBIOS over Tcpip. . . . . . . . : Disabled
```

c. No prompt de comando do outro PC, digite o comando `ipconfig`.

**Pergunta:** Registre os endereços IPv4 do gateway padrão e dos outros PCs na LAN.

**Resposta:** As respostas variam. Neste exemplo, o gateway padrão é 192.168.1.1 e o endereço IPv4 para este PC é 192.168.1.8.

Observação: se você estiver usando um dispositivo móvel para responder à solicitação de ping, procure as instruções para encontrar o endereço IP e o endereço MAC Wi-Fi do seu dispositivo móvel.

Observação: se você tiver apenas um dispositivo, o endereço IP do outro PC poderá ser o gateway padrão.

###### Etapa 2: Iniciar o Wireshark e começar a capturar os dados.

a. No seu PC, inicie o Wireshark.

Observação: como alternativa, a instalação do Wireshark também pode fornecer uma opção do Wireshark antigo. Ela mostra o Wireshark na GUI antiga e mais reconhecida. O restante deste laboratório foi concluído usando a GUI mais recente.

b. Após iniciar o Wireshark, selecione a interface de rede que você identificou com o comando `ipconfig`. Insira `arp` na caixa de filtro. Essa seleção configura o Wireshark para exibir somente os pacotes que fazem parte das trocas ARP entre os dispositivos na rede local. Clique com o botão direito do mouse na interface e clique em Iniciar captura para iniciar a captura de dados.

As informações começarão a rolar na seção superior do Wireshark. Cada linha representa uma mensagem sendo enviada entre um dispositivo de origem e destino na rede.

c. Em uma janela do prompt de comando, execute ping no gateway padrão para testar a conectividade para o endereço do gateway padrão que foi identificado na etapa anterior (Para sistemas operacionais Linux e MAC, use o comando `ping -c 4 192.168.1.1` neste exemplo.)

```
C:\Users\Student> ping 192.168.1.1

Pinging 192.168.1.1 with 32 bytes of data:

Reply from 192.168.1.1: bytes=32 time=7ms TTL=64

Reply from 192.168.1.1: bytes=32 time=2ms TTL=64

Reply from 192.168.1.1: bytes=32 time=1ms TTL=64

Reply from 192.168.1.1: bytes=32 time=6ms TTL=64

Ping statistics for 192.168.1.1:

    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),

Approximate round trip times in milli-seconds:

    Minimum = 1ms, Maximum = 7ms, Average = 4ms
```

d. Faça ping nos endereços IPv4 de outros PCs ou dispositivos móveis na LAN que você anotou na etapa anterior.

Observação: se o outro dispositivo não responde aos pings, pode ser que o firewall esteja bloqueando as solicitações. Pesquise na Internet: desbloquear firewall para o seu sistema operacional.

e. Pare de capturar dados clicando em Stop Capture (ícone do quadrado vermelho) na barra de ferramentas.

###### Etapa 3: Examinar os dados capturados.

Nesta etapa, você examinará os dados gerados pelas solicitações de ping do PC de seu membro da equipe. Os dados do Wireshark são exibidos em três seções:

1. A seção superior exibe a lista de quadros PDU capturados com um resumo das informações do pacote IPv4 listadas.
    
2. A seção do meio lista as informações de PDU para o quadro selecionado na parte superior da tela e divide o frame capturado em suas camadas de protocolo.
    
3. A seção inferior mostra os dados brutos de cada camada. Os dados são exibidos em formato hexadecimal e decimal.
    

b. Clique nos quadros ARP na seção superior que têm o endereço MAC do seu PC como o endereço de origem e "broadcast" como o destino do quadro.

c. Com esse quadro de PDU ainda selecionado na seção superior, vá até a seção do meio. Clique na seta à esquerda da linha Ethernet II para ver os endereços MAC de origem e destino.

**Pergunta:** O endereço MAC de origem corresponde à interface do PC?

**Resposta:** Sim.

d. Clique na seta à esquerda da linha Protocolo ARP (solicitação) para visualizar o conteúdo da solicitação ARP.

###### Etapa 4: Localize o quadro da resposta ARP que corresponde à solicitação ARP que você destacou.

a. Com o endereço IPv4 alvo na solicitação ARP, localize o quadro da resposta ARP na seção superior da tela de captura do Wireshark.

**Pergunta:** Qual é o endereço IPv4 do dispositivo alvo na sua solicitação ARP?

**Resposta:** As respostas serão variadas, mas no nosso exemplo será 192.168.1.9.

b. Destaque o quadro de resposta na seção superior da saída do Wireshark. Talvez seja necessário rolar a janela para encontrar o quadro de resposta que corresponde ao endereço IPv4 alvo identificado na etapa anterior. Expanda as linhas Ethernet II e protocolo ARP (resposta) na seção média da tela.

**Pergunta:** O quadro de resposta ARP é um quadro de broadcast?

**Resposta:** Não.

**Pergunta:** Qual é o endereço MAC destino do quadro?

**Resposta:** As respostas variarão, mas o endereço MAC de destino será a4:4e:31:ad:78:4c neste exemplo.

**Pergunta:** Qual é o endereço MAC do seu PC?

**Resposta:** Sim.

**Pergunta:** Qual endereço MAC é a origem do quadro?

**Resposta:** O dispositivo que está respondendo à solicitação de ping.

c. Verifique se o endereço MAC corresponde ao endereço MAC do dispositivo que você selecionou para responder às solicitações de ping.

##### Parte 2: Examine as entradas do cache ARP no PC

Após a resposta ARP ser recebida pelo PC, a associação do endereço MAC para o endereço IPv4 é armazenada na memória do cache no PC. Essas entradas permanecerão na memória por um curto período (de 15 a 45 segundos), e, depois, se não forem usadas nesse período, serão removidas do cache. (Observação: pesquise na Internet para encontrar os comandos relacionados ao ARP para um PC com sistema operacional Linux ou MAC.)

a. Abra uma janela de prompt de comando em um PC. No prompt, entre `arp -a` e pressione enter.

```
C:\Users\Student> arp -a

Interface: 192.168.1.8 --- 0xb

  Internet Address      Physical Address      Type

  192.168.1.1           00-37-73-ea-b1-7a     dynamic

  192.168.1.9           90-4c-e5-be-15-63     dynamic

  192.168.1.13          a4-4e-31-ad-78-4c     dynamic

  224.0.0.5             01-00-5e-00-00-05     static

  224.0.0.6             01-00-5e-00-00-06     static

  224.0.0.22            01-00-5e-00-00-16     static

  224.0.0.252           01-00-5e-00-00-fc     static

  224.0.0.253           01-00-5e-00-00-fd     static

  239.255.255.250       01-00-5e-7f-ff-fa     static

  255.255.255.255       ff-ff-ff-ff-ff-ff     static
```

A saída do comando arp –a exibirá as entradas que estão no cache no PC. No exemplo, o PC tem entradas para o gateway padrão (192.168.1.1) e para dois PCs localizados na mesma LAN (192.168.1.9 e 192.168.1.13).

**Pergunta:** Qual é o resultado da execução do comando arp –a no seu PC?

**Resposta:** O comando lista os mapeamentos conhecidos de endereço MAC para IPv4.

b. O comando arp no PC Windows tem outras funcionalidade. Digite `arp /?` no prompt de comando e pressione enter. As opções do comando arp permitem que você visualize, adicione e remova as entradas da tabela ARP, se necessário.

**Pergunta:** Qual opção exclui uma entrada do cache ARP?

**Resposta:** arp -d

c. Qual seria o resultado da emissão do comando `arp –d *`?

**Resposta:** As associações atuais de endereços no cache ARP seriam excluídas. Este comando requer privilégios administrativos no Windows 10.

#### Reflexão

1. Qual é o benefício de manter as entradas do cache ARP na memória no computador de origem?

**Resposta:** Seu computador sempre verifica o cache local antes de solicitar informações de outros dispositivos na rede. O cache ARP guarda as associações de endereço aprendidas dinamicamente por um curto período. Quando o tráfego é trocado frequentemente entre a origem e o destino, o cache ARP impede que o host transmita solicitações ARP, em broadcast, desnecessariamente.

2. Se o endereço IPv4 de destino não estiver localizado na mesma rede que o host de origem, qual endereço MAC será usado como endereço MAC de destino no quadro?

**Resposta:** O computador usará o endereço MAC do gateway padrão.

## 24.1.11 Verifique seu entendimento - ARP

**Verifique sua compreensão do ARP escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Quais duas funções são fornecidas pelo ARP? (Escolha duas.)

- [ ] Mantém uma tabela de endereços IPv4 para nomes de domínio
- [x] Mantém uma tabela de mapeamentos de endereços IPv4 para MAC
- [ ] Mantém uma tabela de mapeamentos de endereços IPv6 para MAC
- [ ] Resolve endereços IPv4 para nomes de domínio
- [x] Resolve endereços IPv4 para endereços MAC
- [ ] Resolver endereços IPv6 para endereços MAC

✅ RESPOSTA CORRETA: Mantém uma tabela de mapeamentos de endereços IPv4 para MAC, Resolve endereços IPv4 para endereços MAC

> O ARP tem duas funções principais: manter uma tabela de mapeamentos de endereços IPv4 para MAC e determinar os endereços MAC de endereços IPv4 conhecidos.

---

### Pergunta 2

Onde a tabela ARP é armazenada em um dispositivo?

- [ ] ROM
- [ ] flash
- [ ] NVRAM
- [x] RAM

✅ RESPOSTA CORRETA: RAM

> A tabela ARP é armazenada temporariamente em cache na RAM.

---

### Pergunta 3

Qual afirmação é verdadeira sobre o ARP?

- [ ] Um cache ARP não pode ser excluído manualmente.
- [ ] As entradas ARP são armazenadas permanentemente em cache.
- [x] As entradas ARP são armazenadas temporariamente em cache.

✅ RESPOSTA CORRETA: As entradas ARP são armazenadas temporariamente em cache.

> A tabela ARP é armazenada temporariamente em cache na RAM.

---

### Pergunta 4

Qual comando poderia ser usado em um roteador Cisco para exibir sua tabela ARP?

- [ ] arp -a
- [ ] arp - d
- [ ] show arp table
- [x] show ip arp

✅ RESPOSTA CORRETA: show ip arp

> O comando show ip arp é usado em roteadores Cisco para visualizar a tabela ARP.

---

### Pergunta 5

O que é um ataque usando ARP?

- [ ] Transmissões ARP
- [ ] Ataques de salto ARP
- [x] Contaminação de ARP
- [ ] Privação de ARP

✅ RESPOSTA CORRETA: Contaminação de ARP

> Dois problemas de segurança com as Solicitações ARP são que as mensagens ARP são enviadas como transmissões e podem ser falsificadas.


## 24.2.1 O que aprendi neste módulo?

### ARP

Para enviar um pacote para outro host na mesma rede IPv4 local, um host deve conhecer o endereço IPv4 e o endereço MAC do dispositivo de destino. Os endereços IPv4 de destino do dispositivo são conhecidos ou resolvidos pelo nome do dispositivo. No entanto, os endereços MAC devem ser descobertos. Um dispositivo usa ARP para determinar o endereço MAC de destino de um dispositivo local quando conhece seu endereço IPv4. O ARP fornece duas funções básicas: resolver endereços IPv4 para MAC e manter uma tabela de mapeamentos de endereços IPv4 para MAC.

O dispositivo emissor pesquisará em sua tabela ARP um endereço IPv4 destino correspondente a um endereço MAC.

- Se o endereço IPv4 destino do pacote estiver na mesma rede que o endereço IPv4 origem, o dispositivo pesquisará o endereço IPv4 destino na tabela ARP.
- Se o endereço IPv4 destino do pacote estiver em uma rede diferente do endereço IPv4 origem, o dispositivo pesquisará o endereço IPv4 do gateway padrão na tabela ARP.

Cada entrada (linha) da tabela ARP vincula um endereço IPv4 a um endereço MAC. Chamamos a relação entre os dois valores de um mapa. As mensagens do ARP são encapsuladas diretamente em um quadro Ethernet. Não há cabeçalho IPv4. A requisição ARP é encapsulada em um quadro Ethernet usando as seguintes informações de cabeçalho:

- Endereço MAC de destino – Este é um endereço de broadcast FF-FF-FF-FF-FF-FF que requer todos os NICs Ethernet na LAN para aceitar e processar a solicitação ARP.
- Endereço MAC de origem – Este é o endereço MAC do remetente da solicitação ARP.
- Tipo – As mensagens ARP têm um campo de tipo de 0x806. Ele informa à NIC de recebimento que a parte de dados do quadro precisa ser transferida para o processo ARP.

Como as solicitações de ARP são transmissões, elas são inundadas em todas as portas pelo switch, exceto a porta de recebimento. Somente o dispositivo com o endereço IPv4 de destino associado à solicitação ARP responderá com uma resposta ARP. Depois que a resposta do ARP é recebida, o dispositivo adiciona o endereço IPv4 e o endereço MAC correspondente à sua tabela ARP.

Quando o endereço IPv4 destino não está na mesma rede que o endereço IPv4 origem, o dispositivo de origem precisa enviar o quadro para o gateway padrão. Essa é a interface do roteador local. Sempre que um dispositivo de origem tiver um pacote com um endereço IPv4 em outra rede, ele encapsulará esse pacote em um quadro usando o endereço MAC de destino do roteador. O endereço IPv4 do gateway padrão é armazenado na configuração IPv4 dos hosts. Se o host de destino não estiver na mesma rede, a origem usará a tabela ARP para obter uma entrada com o endereço MAC do gateway padrão. Se não houver uma entrada, ela usará o processo de ARP para determinar um endereço MAC do gateway padrão.

Em cada dispositivo, um temporizador da cache ARP remove entradas ARP que não tenham sido usadas durante um determinado período. Os horários diferem dependendo do sistema operacional do dispositivo. Os comandos podem ser usados para remover manualmente algumas ou todas as entradas na tabela ARP.

Em um roteador Cisco, o comando show ip arp é usado para exibir a tabela ARP. Em um PC Windows 10, o comando arp –a é usado para exibir a tabela ARP.

Como um quadro broadcast, uma requisição ARP é recebida e processada por todos os dispositivos na rede local. Se um grande número de dispositivos fosse ligado e todos começassem a acessar os serviços de rede ao mesmo tempo, poderia haver alguma redução no desempenho por um curto período de tempo. Em alguns casos, o uso do ARP pode levar a um risco potencial à segurança.

Um ator de ameaça pode usar falsificação ARP para realizar um ataque de envenenamento por ARP. Essa é uma técnica usada por um agente de ameaças para responder a uma solicitação ARP de um endereço IPv4 que pertence a outro dispositivo, como o gateway padrão. O agente da ameaça envia uma resposta ARP com seu próprio endereço MAC. O destinatário da resposta ARP adicionará o endereço MAC errado à sua tabela ARP e enviará esses pacotes ao agente de ameaça.

---

## 24.2.2 Webster - Questões para Reflexão

Olcay e Abay sabem muito sobre redes, inclusive sobre a resolução de endereços. Antes deste módulo, você entendia ARP e tabelas ARP? Eu nunca tinha pensado em um agente de ameaças usando falsificação de ARP para realizar um ataque de envenenamento de ARP! Você tinha?

## 24.2.3 Teste de Resolução de Endereço

## Pergunta 1

**Qual protocolo é usado para descobrir o endereço de destino que precisa ser adicionado a um quadro Ethernet?**

- [ ] DHCP
- [ ] DNS
- [ ] HTTP
- [x] ARP

**Resposta: ARP**

---

## Pergunta 2

**O que é uma função do protocolo ARP?**

- [ ] Mapeando um nome de domínio para seu endereço IP
- [x] Resolvendo um endereço IPv4 para um endereço MAC
- [ ] Obtendo um endereço IPv4 automaticamente
- [ ] Manutenção de uma tabela de nomes de domínio com seus endereços IP resolvidos

**Resposta: Resolvendo um endereço IPv4 para um endereço MAC**

---

## Pergunta 3

**Consulte a figura. PC1 na VLAN 10 quer se comunicar com PC2 na VLAN 20. PC1 envia uma solicitação de ARP para seu gateway padrão, GW1. Como o GW1 responde?**

![[Pasted image 20260619072525.png]]
_(Topologia: GW1 conectado a SWA, que conecta PC1 — 192.168.10.17, VLAN 10 — e PC2 — 192.168.20.34, VLAN 20)_

- [ ] Ele encaminha a solicitação ARP de PC1 para PC2.
- [ ] Ele envia uma solicitação de ARP para PC1.
- [ ] Ele envia uma resposta ARP para PC2.
- [x] Ele envia uma resposta ARP ao PC1 com seu próprio endereço MAC.

**Resposta: Ele envia uma resposta ARP ao PC1 com seu próprio endereço MAC.**

---

## Pergunta 4

**Que ação o processo ARP executa quando um host precisa criar um quadro, mas o cache ARP não contém um mapeamento de endereço?**

- [ ] O processo ARP envia uma solicitação ARP para o endereço de broadcast IPv4 para descobrir o endereço IPv4 do dispositivo de destino.
- [ ] O processo ARP envia uma solicitação ARP para o endereço de broadcast Ethernet para descobrir o endereço IPv4 do dispositivo de destino.
- [ ] O processo ARP envia uma solicitação ARP para o endereço de broadcast IPv4 para descobrir o endereço MAC do dispositivo de destino.
- [x] O processo ARP envia uma solicitação ARP para o endereço de broadcast Ethernet para descobrir o endereço MAC do dispositivo de destino.

**Resposta: O processo ARP envia uma solicitação ARP para o endereço de broadcast Ethernet para descobrir o endereço MAC do dispositivo de destino.**

---

## Pergunta 5

**Qual afirmativa descreve o tratamento das requisições ARP no link local?**

- [ ] Elas precisam ser encaminhadas por todos os roteadores na rede local.
- [x] Elas são recebidas e processadas por todos os dispositivos na rede local.
- [ ] Elas são recebidas e processadas somente pelo dispositivo destino.
- [ ] Elas são entregues por todos os switches na rede local.

**Resposta: Elas são recebidas e processadas por todos os dispositivos na rede local.**

---

## Pergunta 6

**Qual é o objetivo de um ataque de ARP spoofing?**

- [x] Associar endereços IP aos endereços MAC incorretos
- [ ] Sobrecarregar os hosts de rede com solicitações de ARP
- [ ] Inundar a rede com transmissões de resposta ARP
- [ ] Preencher as tabelas de endereços MAC do switch com endereços falsos

**Resposta: Associar endereços IP aos endereços MAC incorretos**

---

## Pergunta 7

**Um analista de segurança digital acredita que um invasor está anunciando um endereço MAC forjado para os hosts de rede na tentativa de imitar o gateway padrão. Qual comando o analista poderia usar nos hosts de rede para ver qual endereço MAC os hosts estão usando para alcançar o gateway padrão?**

- [ ] route print
- [x] arp -a
- [ ] netstat -r
- [ ] ipconfig /all

**Resposta: arp -a**

---

## Pergunta 8

**O que um host fará primeiro ao preparar uma PDU de Camada 2 para transmissão a um host na mesma rede Ethernet?**

- [x] Ele pesquisará na tabela ARP o endereço MAC do host de destino.
- [ ] Ele enviará a PDU para o roteador diretamente conectado à rede.
- [ ] Ele consultará o servidor DNS local para o nome do host de destino.
- [ ] Ele iniciará uma solicitação ARP para localizar o endereço MAC do host de destino.

**Resposta: Ele pesquisará na tabela ARP o endereço MAC do host de destino.**

---

## Pergunta 9

**Qual endereço de destino é usado em um quadro de solicitação ARP?**

- [ ] 127.0.0.1
- [ ] 0.0.0.0
- [x] FFFF.FFFF.FFFF
- [ ] 01-00-5E-00-AA-23
- [ ] 255.255.255.255

**Resposta: FFFF.FFFF.FFFF**

---

## Pergunta 10

**Qual protocolo é usado por um computador para encontrar o endereço MAC do gateway padrão em uma rede Ethernet?**

- [ ] DHCP
- [x] ARP
- [ ] TCP
- [ ] UDP

**Resposta: ARP**

---

## Pergunta 11

**Consulte a figura. O PC1 tenta se conectar ao File_server1 e envia uma solicitação ARP para obter um endereço MAC de destino. Qual endereço MAC o PC1 receberá na resposta do ARP?**

![[Pasted image 20260619072551.png]]
_(Topologia: PC1 — S1 — R1 [G0/0, S0/0/0] — R2 [S0/0/0, G0/0] — S2 — File_server1)_

- [ ] O endereço MAC de File_server1
- [ ] O endereço MAC da interface G0/0 no R2
- [x] O endereço MAC da interface G0/0 em R1
- [ ] O endereço MAC de S2
- [ ] O endereço MAC de S1

**Resposta: O endereço MAC da interface G0/0 em R1**