
# 14.0 Introdução

## 14.0.1 Webster - Por que devo fazer este módulo?

Kishori deixa o trabalho durante o dia e começa seu caminho de casa. Sua amiga ligou para avisá-la de que há muito congestionamento em sua rota habitual para casa. Ela usou o GPS do telefone para redirecionar para uma estrada menos congestionada. Kishori se pergunta se as redes podem ficar congestionadas. Eles encontram uma rota mais rápida?

Ótima pergunta, Kishori! As redes também podem ter esse problema de congestionamento retardando o desempenho. Em uma rede, o roteador pode determinar o melhor caminho. Como uma rede fica congestionada? O que você pode fazer para limitar esse congestionamento? Você e Kishori vão descobrir neste módulo!

## 14.0.2 O que vou aprender neste módulo?

**Título do módulo:** Roteamento entre redes

**Objetivo do Módulo:** Criar uma LAN totalmente conectada.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|A necessidade do roteamento|Explicar a necessidade do roteamento.|
|A tabela de roteamento|Explicar como os roteadores usam tabelas.|
|Criando uma LAN|Criar uma rede totalmente conectada.|

# 14.1 A necessidade do Roteamento

## 14.1.1 Vídeo - Dividindo a Rede Local

Nesta lição, vamos falar sobre como, conforme as redes crescem, torna-se necessário começar a dividi-las de uma única grande rede local para vários segmentos de rede local menores.

Vamos olhar para uma empresa que consiste em três departamentos principais: Gerenciamento de Rede, Departamento de Contabilidade e Departamento de Vendas.

Algumas das razões pelas quais você pode dividir uma rede em componentes menores:

A primeira é apenas para limitar a quantidade de tráfego de broadcast que atravessa a rede. Sempre que você gerar um broadcast, mesmo que esteja no Gerenciamento de Rede, seu computador e todos os outros dispositivos na rede serão forçados a aceitar esse broadcast e processá-lo. A maioria dos broadcasts não contém informações que cada dispositivo precisa saber. Portanto, há muitos broadcasts que estão sendo processados pelo seu dispositivo e que eventualmente estão sendo jogados fora, porque as informações contidas nessa transmissão realmente não são necessárias para nenhum aplicativo no seu dispositivo.

Essa é uma razão pela qual podemos querer dividir uma rede: conter transmissões, para fazer domínios de broadcast menores. O termo domínio de broadcast refere-se à área que ouve um broadcast. No caso de uma rede onde todos os dispositivos são ligados por switches, todos os broadcasts seriam ouvidos por todos os dispositivos conectados.

Outra razão pela qual podemos desejar dividir nossa rede é para fins de segurança. Podemos não querer que pessoas no Departamento de Vendas sejam capazes de ver os dispositivos e servidores ou usar as impressoras localizadas no Departamento de Contabilidade. Também podemos não querer que o Departamento de Contabilidade possa acessar os mecanismos de controle da rede que estão no Departamento de Gerenciamento de Rede.

Uma das principais razões para querermos dividir a rede é, por exemplo, quando o Departamento de Contabilidade está se mudando para um novo prédio ou um novo escritório em um andar diferente, fora de onde nossa rede local pode realmente atendê-los. Pegar e dividir algo por localização geográfica exige que façamos nossos segmentos de rede muito menores.

Então, basicamente, como fazemos isso? Como dividimos uma rede grande em pedaços menores? Uma das maneiras é com um roteador. Em todas as redes, a rede local — ou seja, a rede que pertence ao negócio, à casa, ou à empresa — essa rede é separada da internet por um roteador. Quando você compra sua conexão de rede doméstica, seu provedor de serviços coloca um roteador em sua casa, para que o tráfego gerado pela sua rede não acabe na internet.

Quando adicionamos um roteador, ele nos permite dividir a rede e também dividir os domínios de broadcast. Ao inserir roteadores no diagrama de rede, pegamos uma rede relativamente grande e a dividimos em três redes separadas. Em um roteador, cada interface conecta e define uma rede separada. Quando falamos de redes separadas, estamos falando de ambos os domínios de broadcast, mas também de diferentes redes IP — diferentes redes com diferentes conjuntos de endereços IP que identificam todas as pessoas dentro da rede como estando na mesma rede IP.

Para recapitular as razões pelas quais dividimos uma rede: dividimos a rede por segurança; dividimos a rede porque queremos manter domínios de broadcast menores; e dividimos a rede porque podemos estar movendo coisas para locais diferentes onde uma única grande rede não pode alcançar.


## 14.1.2 Agora Precisamos de Roteamento

IP Packet Encapsulated in an Ethernet Frame

Na maioria das situações, queremos que os nossos dispositivos possam se conectar além da rede local: a outras residências, a empresas e à Internet. Os dispositivos que estão além do segmento de rede local são conhecidos como hosts remotos. Quando um dispositivo de origem envia um pacote a um dispositivo de destino remoto, é necessária a ajuda de roteadores e do roteamento. O roteamento é o processo de identificação do melhor caminho até um destino.

Um roteador é um dispositivo de rede que conecta várias redes IP de Camada 3. Na camada de distribuição da rede, os roteadores direcionam o tráfego e realizam outras funções essenciais em uma operação de rede eficiente. Os roteadores, como switches, conseguem decodificar e ler as mensagens que são enviadas para eles. Ao contrário dos switches, que tomam uma decisão de encaminhamento com base no endereço MAC da Camada 2, os roteadores fundamentam suas decisões de encaminhamento no endereço IP da Camada 3.

O formato do pacote contém os endereços IP dos hosts de destino e de origem, assim como os dados da mensagem que está sendo enviada entre eles. O roteador lê a porção de rede do endereço IP de destino e a utiliza para descobrir qual das redes conectadas é a melhor forma de encaminhar a mensagem para o destino.

Sempre que a porção de rede dos endereços IP dos hosts de origem e de destino não coincidir, deverá ser usado um roteador para encaminhar a mensagem. Quando um host localizado na rede 1.1.1.0 precisa enviar uma mensagem para um host na rede 5.5.5.0, ele encaminha a mensagem ao roteador. O roteador recebe a mensagem, desencapsula o quadro Ethernet e lê o endereço IP de destino no pacote IP. Em seguida, ele determina para onde deve encaminhar a mensagem. Ele reencapsula o pacote de volta em um novo quadro e encaminha o quadro para o destino.

**Clique em Play para ver como são usados os endereços MAC e IP.**

### Pacote IP Encapsulado em um Quadro Ethernet

![[Pasted image 20260610065242.png]]
![[Pasted image 20260610065258.png]]
![[Pasted image 20260610065321.png]]


## 14.1.3 Verifique sua compreensão - A necessidade de roteamento

### Pergunta 1

Razões para dividir uma rede em várias redes menores. (Escolha duas.)

- [ ] A solução de problemas é mais difícil em redes grandes.
- [x] Para ter domínios de broadcast menores
- [x] aumentar a segurança de rede
- [ ] Os dispositivos recebem todo o tráfego de rede

✅ RESPOSTA CORRETA: Para ter domínios de broadcast menores, aumentar a segurança de rede

> Você dividiria uma rede em várias redes menores para manter domínios de broadcast menores e aumentar a segurança da rede.

---

### Pergunta 2

Qual dos dispositivos a seguir é usado para dividir uma rede em redes menores?

- [ ] Hubs
- [ ] Switches
- [x] Roteadores
- [ ] Bridges

✅ RESPOSTA CORRETA: Roteadores

> Os roteadores dividem uma rede em redes menores.

---

### Pergunta 3

O que é roteamento?

- [ ] O roteamento transfere dados entre dispositivos.
- [x] O roteamento é um processo para determinar o melhor caminho até um destino.
- [ ] O roteamento é uma forma de conectar dispositivos em uma rede local.

✅ RESPOSTA CORRETA: O roteamento é um processo para determinar o melhor caminho até um destino.

> O roteamento é um processo para determinar o melhor caminho até um destino.


# 14.2 A tabela de roteamento

## 14.2.1 Vídeo - Encaminhamento de pacotes pelo roteador

Neste vídeo, veremos como um roteador encaminha pacotes de uma rede para outra rede.

Neste exemplo, temos o Host em 10.0.0.1 que deseja enviar um pacote para 192.168.1.2, que está em outra rede. Portanto, o endereço IP de origem do pacote será 10.0.0.1 e o endereço IPv4 de destino do pacote será 192.168.1.2.

Então H1 envia o pacote para seu gateway padrão, o roteador. Ele envia para o roteador porque H1 sabe que o destino — H4, seu endereço IPv4 — está em uma rede diferente.

O roteador recebe o pacote e procura o endereço IPv4 de destino do pacote em sua tabela de roteamento. Ele percebe que o endereço IPv4 de destino 192.168.1.2 está na rede 192.168.1.0, e que essa rede está em sua interface Fast Ethernet 02. Assim, o roteador irá encaminhar este pacote para fora de sua Interface Fast Ethernet 02 para o destino final.

Agora, neste caso, H1 tem um pacote para enviar para o endereço IPv4 de destino 255.255.255.255. Como você deve se lembrar, esse é um endereço de broadcast. Assim, uma transmissão será enviada para todos os dispositivos em sua rede. Você notará que o roteador receberá esta transmissão, mas não encaminhará este pacote para outras redes.


## 14.2.2 Vídeo - Mensagens dentro de uma rede e entre redes - Parte 1

Neste vídeo, vamos dar uma olhada em como as mensagens viajam dentro de uma rede e também entre redes.

Nesta primeira parte, temos o host H1 em 192.168.1.10 que vai enviar um pacote para o endereço IPv4 de H2, 192.168.1.20.

H1, a origem do pacote, constrói o pacote IPv4 com seu próprio endereço como fonte, 192.168.1.10, e o endereço IPv4 de destino de 192.168.1.20.

A primeira coisa que H1 precisa determinar é: estamos na mesma rede? Ele percebe que seu próprio endereço de rede é 192.168.1.10 — essa é a rede à qual pertence — e ele usa sua máscara de sub-rede para fazer isso. Em seguida, ele analisa o endereço IPv4 de destino e, usando sua própria máscara de sub-rede, H1 determina que H2, em 192.168.1.20, está na mesma rede, pois ambos começam com 192.168.1.

O que isso significa para H1 é que ele pode enviar este pacote diretamente para H2, sem precisar enviar através do seu gateway padrão, o roteador. Ele pode enviá-lo diretamente.

Então, H1 vai construir o quadro Ethernet com seu próprio endereço MAC de sua NIC Ethernet, AA:AA, como o endereço MAC de origem Ethernet. Para o endereço MAC de destino, ele diz: "Posso enviá-lo diretamente para H2 porque estamos na mesma rede. Eu só preciso saber o endereço MAC associado ao destino, 192.168.1.20."

Nesse caso, H1 verifica sua tabela ARP. Supondo que tem essa informação em sua tabela ARP, ele sabe que 192.168.1.20 tem o endereço MAC BB:BB. Se ele não souber disso, lembre-se de que ele envia uma solicitação ARP, obtém uma resposta ARP e adiciona à tabela.

Agora, H1 pode ir em frente e enviar este quadro Ethernet em direção ao switch, e ele é enviado diretamente para H2.

## 14.2.3 Vídeo - Mensagens dentro de redes e entre redes - Parte 2

Nesta próxima parte, teremos H1 em 192.168.1.10 enviando um pacote IPv4 para 192.168.2.50, host H3.

H1, a origem do pacote, constrói o pacote IPv4. O endereço IPv4 de origem é seu próprio endereço IPv4, 192.168.1.10. O endereço IPv4 de destino é o destino final, o de H3 em 192.168.2.50.

Agora, H1 precisa determinar: o endereço IPv4 de destino, o de H3, está na mesma rede que eu? Ele conhece seu endereço IPv4, 192.168.1.10, que está na rede 192.168.1.0. Ele analisa o endereço IPv4 de destino usando sua própria máscara de sub-rede e determina que o endereço de destino está em outra rede — não está na rede 192.168.1.0, está na 192.168.2.0 talvez. Tudo o que sabe é que não está na sua rede.

Então, H1 diz: "Não posso enviar este pacote diretamente ao dispositivo. Preciso enviá-lo para o meu gateway padrão, o roteador." H1 conhece o endereço IPv4 do gateway padrão do roteador, como parte das informações de configuração que todo dispositivo deve ter para alcançar outras redes. Ele sabe que o endereço IPv4 do roteador é 192.168.1.1.

O que ele precisa saber é qual é o endereço MAC desse endereço IPv4 de gateway padrão. Portanto, ele verifica seu cache ARP para esse endereço MAC. Supondo que já tenha essa informação em seu cache ARP, a NIC Ethernet associada a esta interface do roteador é abreviada em 11-11. Se ele não soubesse essa informação, ele enviaria uma solicitação ARP para obter uma resposta ARP do roteador.

Agora este quadro Ethernet é enviado de H1 e é recebido pelo roteador. O roteador recebe e diz: "Sim, esse é o meu endereço MAC de destino, este quadro é para mim." Então, o que ele faz é remover essa informação do cabeçalho Ethernet.

Agora o roteador vai fazer o seu trabalho — o que chamamos de encaminhamento de camada 3, ele vai fazer o roteamento. Ele procura o endereço IPv4 de destino do pacote olhando sua tabela de roteamento. Ele diz: "Este endereço IPv4 de destino, 192.168.2.50, é membro da rede 192.168.2.0 na minha tabela de roteamento. Posso alcançar essa rede enviando o pacote pela Fast-Ethernet 0/2."

Então, ele vai encapsulá-lo em um novo quadro Ethernet. O novo quadro Ethernet terá o endereço MAC de origem desta placa de interface de rede do roteador, que é 22-22. Lembre-se: a camada Ethernet 2 é para comunicações de placa de interface de rede para placa de interface de rede na mesma rede.

A próxima coisa que o roteador precisa fazer é descobrir o endereço MAC associado ao endereço IPv4 de destino, que está na sua rede. Ele verifica seu próprio cache ARP e, supondo que tenha essa informação, sabe que 192.168.2.50 tem o endereço MAC CC-CC. Novamente, isso é abreviado, mas vamos usar CC-CC.

Agora ele pode enviar este quadro Ethernet pela porta Fast Ethernet 0/2, encaminhando para H3. H3 diz: "Sim, o endereço MAC de destino está associado ao endereço MAC da minha placa NIC. Este quadro Ethernet é para mim." Ele recebe o pacote e confirma: "Sim, esse endereço IPv4 é meu endereço IPv4", recebendo o pacote.

E é assim que um pacote é enviado de H1 a H3, em diferentes redes.


## 14.2.4 Entradas da Tabela de Roteamento

Os roteadores movem informações entre redes locais e remotas. Para fazer isso, eles têm que usar tabelas de roteamento para armazenar informações. As tabelas de roteamento não estão relacionadas aos endereços de hosts individuais. Tabelas de roteamento contêm endereços de redes e o melhor caminho para acessar essas redes. As entradas podem ser feitas na tabela de roteamento de duas maneiras: atualizadas dinamicamente por informações recebidas de outros roteadores na rede ou inseridas manualmente por um administrador de rede. Os roteadores usam as tabelas de roteamento para determinar qual interface deve ser usada para encaminhar uma mensagem para o destino desejado.

Se o roteador não conseguir determinar para onde encaminhar uma mensagem, ele a descartará. Os administradores de rede podem configurar uma rota padrão que é inserida na tabela de roteamento para evitar que o pacote não seja descartado pelo fato do caminho para a rede de destino não estar na tabela de roteamento. Uma rota padrão é a interface através da qual o roteador encaminha um pacote contendo um endereço de rede IP de destino que é desconhecido. Essa rota padrão normalmente se conecta a outro roteador que pode encaminhar o pacote para a rede de destino final.


![[Pasted image 20260610065732.png]]

| Tipo | Rede          | Porta           |
| ---- | ------------- | --------------- |
| C    | 10.0.0.0/8    | FastEthernet0/0 |
| C    | 172.16.0.0/16 | FastEthernet0/1 |

- **Tipo** — O tipo de conexão C para diretamente conectado
- **Rede** — O endereço de rede
- **Porta** — Interface usada para encaminhar pacotes para a rede


## 14.2.5 O Gateway Padrão

O método que um host utiliza para enviar mensagens para um destino em uma rede remota difere da forma como um host envia mensagens na mesma rede local. Quando um host precisa enviar uma mensagem para outro host localizado na mesma rede, ele pode encaminhar a mensagem diretamente. Um host usará o ARP para descobrir o endereço MAC do host de destino. O pacote IPv4 contém o endereço IPv4 de destino, encapsula o pacote em um quadro com o endereço MAC de destino e o encaminha para fora.

Quando um host precisa enviar uma mensagem para uma rede remota, ele deve usar o roteador. O host inclui o endereço IP do host de destino dentro do pacote, exatamente como antes. Entretanto, quando ele encapsula o pacote em um quadro, usa o endereço MAC do roteador como destino do quadro. Dessa forma, o roteador receberá e aceitará o quadro baseado no endereço MAC.

Como o host de origem determina o endereço MAC do roteador? Um host conhece o endereço IPv4 do roteador por meio do endereço de gateway padrão configurado em suas configurações de TCP/IP. O endereço do gateway padrão é o endereço da interface do roteador conectada à mesma rede local do host de origem. Todos os hosts na rede local usam o endereço do gateway padrão para enviar mensagens ao roteador. Quando o host conhece o endereço IPv4 do gateway padrão, ele pode usar o ARP para determinar o endereço MAC. O endereço MAC do roteador é colocado no quadro, destinado a outra rede.

É importante que o gateway padrão correto esteja configurado em cada host na rede local. Se não houver um gateway padrão definido nas configurações TCP/IP do host ou se estiver especificado um gateway padrão incorreto, não será possível entregar as mensagens endereçadas aos hosts nas redes remotas.

![[Pasted image 20260610065830.png]]

|PC|Endereço IPv4|Máscara de Sub-Rede|Gateway Padrão|
|---|---|---|---|
|H1|192.168.1.1|255.255.255.0|192.168.1.254|
|H2|192.168.1.2|255.255.255.0|192.168.1.254|
|H3|192.168.1.3|255.255.255.0|192.168.1.254|

## 14.2.6 Verifique a sua compreensão - Selecione o gateway padrão

**Consulte a Figura Selecione o gateway padrão para cada uma das seguintes perguntas.**

![[Pasted image 20260610065901.png]]
### Pergunta 1

Qual é o gateway padrão para H1?

- [ ] 172.16.1.1
- [x] 192.168.1.1
- [ ] 192.0.0.1
- [ ] 172.16.0.50
- [ ] 10.0.0.1
- [ ] 10.168.1.1

✅ RESPOSTA CORRETA: 192.168.1.1

> O gateway padrão para H1 é 192.168.1.1.

---

### Pergunta 2

Qual é o gateway padrão para H2?

- [x] 10.0.0.1
- [ ] 172.16.1.1
- [ ] 10.168.1.1
- [ ] 192.168.1.1
- [ ] 192.0.0.1
- [ ] 172.16.0.50

✅ RESPOSTA CORRETA: 10.0.0.1

> O gateway padrão para H2 é 10.0.0.1.

---

### Pergunta 3

Qual é o gateway padrão para H3?

- [ ] 10.168.1.1
- [ ] 192.168.1.50
- [ ] 10.0.0.1
- [ ] 192.0.0.1
- [ ] 172.16.1.1
- [x] 172.16.0.50

✅ RESPOSTA CORRETA: 172.16.0.50

> O gateway padrão para H3 é 172.16.0.50.


## 14.2.7 Verifique sua compreensão - A tabela de roteamento

**Verifique sua compreensão da tabela de roteamento , escolhendo a melhor resposta para as seguintes perguntas.**

### Pergunta 1

Quais informações no pacote IP o roteador usa para determinar por qual interface encaminhar o pacote?

- [ ] endereço MAC origem
- [ ] endereço MAC de destino
- [ ] endereço IP origem
- [x] endereço IP destino

✅ RESPOSTA CORRETA: endereço IP destino

> O roteador usa o endereço IP de destino para determinar por qual interface encaminhar o pacote.

---

### Pergunta 2

Verdadeiro ou falso? Se o Host-A tiver um pacote IP para enviar ao Host-B, e o Host-A determinar que o Host-B está em uma rede diferente. O Host-A encapsulará o pacote IP em um quadro Ethernet com o endereço MAC de destino do gateway padrão.

- [ ] falso
- [x] verdadeiro

✅ RESPOSTA CORRETA: verdadeiro

> A resposta correta é verdadeira. Um host usará o endereço MAC de destino do gateway padrão para todos os pacotes destinados a redes diferentes.

---

### Pergunta 3

Uma rota padrão é a interface pela qual o roteador encaminha:

- [x] um pacote que contém um endereço de rede IP de destino que não está na tabela de roteamento do roteador
- [ ] qualquer pacote quando um host não receber uma resposta de ARP
- [ ] um pacote que contém um endereço de rede IP de origem que não está na tabela de roteamento do roteador
- [ ] todos os pacotes

✅ RESPOSTA CORRETA: um pacote que contém um endereço de rede IP de destino que não está na tabela de roteamento do roteador

> Se um roteador não tiver uma rota para uma rede de destino, ele usará o roteador padrão.

---

### Pergunta 4

Um host enviará um pacote para o gateway padrão quando:

- [ ] todos os pacotes
- [ ] ele não recebe uma resposta ARP
- [x] o endereço IP de destino está em uma rede diferente
- [ ] o endereço IP de origem está em uma rede diferente

✅ RESPOSTA CORRETA: o endereço IP de destino está em uma rede diferente

> Um host envia pacotes, destinados a uma rede diferente, para o gateway padrão.


# 14.3 Criando uma LAN

## 14.3.1 Redes de Área Local

O termo Rede de Área Local (LAN) se refere a uma rede local ou a um grupo de redes locais interconectadas que estão sob o mesmo controle administrativo. No início das redes de computadores, as LANs eram definidas como pequenas redes que existiam em uma única localização física. Embora as LANs possam ser uma única rede local instalada em uma casa ou pequeno escritório, a definição de LAN evoluiu para incluir redes locais interconectadas, consistindo em muitas centenas de hosts, instalados em vários prédios e locais.

É importante lembrar que todas as redes locais dentro de uma LAN estão sob um controle administrativo. Outras características comuns das LANs são que elas normalmente usam protocolos Ethernet ou Wireless e suportam altas taxas de transmissão de dados.

O termo Intranet geralmente é usado para se referir a uma LAN privada que pertence a uma organização e foi projetada para ser acessada somente por membros da organização, funcionários ou terceiros com autorização.

![[Pasted image 20260610070342.png]]

## 14.3.2 Segmentos de rede local e remota

Dentro de uma LAN, é possível colocar todos os hosts em uma única rede local ou dividi-los entre várias redes conectadas por um dispositivo na camada de distribuição. A forma como esse posicionamento é determinado depende dos resultados desejados.

**Clique abaixo para saber mais sobre os segmentos de rede local e remoto.**

### Todos os hosts em um segmento de rede local

Colocar todos os hosts em uma única rede local permite que eles sejam vistos por todos os outros hosts. Isso ocorre porque existe um domínio da broadcast e os hosts usam o ARP para se localizarem.

Em um projeto de rede simples, pode ser vantajoso manter todos os hosts em uma única rede local. Entretanto, à medida que as redes crescem, o aumento de tráfego diminui a velocidade e o desempenho da rede. Nesse caso, pode valer a pena mover alguns hosts para uma rede remota.

Vantagens de um único segmento local:

- Adequado para redes mais simples
- Menos complexidade e menor custo de rede
- Permite que os dispositivos sejam “vistos” por outros dispositivos
- Transferência de dados mais rápida - comunicação mais direta
- Facilidade de acesso ao dispositivo

Desvantagens de um único segmento local:

- Todos os hosts estão em um domínio de broadcast que causa mais tráfego no segmento e pode retardar o desempenho da rede
- Mais difícil de implementar QoS
- Mais difícil de implementar segurança
![[Pasted image 20260610070417.png]]

### Hosts em um segmento remoto

Colocando hosts adicionais em uma rede remota diminuirá o impacto em demandas de tráfego. No entanto, os hosts em uma rede não poderão se comunicar com hosts na outra rede sem o uso de roteamento. Os roteadores aumentam a complexidade da configuração de rede e podem introduzir latência (ou seja, atraso) nos pacotes enviados de uma rede local para outra.

Vantagens:

- Mais adequado para redes maiores e mais complexas
- Divide domínios de transmissão e reduz o tráfego
- Pode melhorar o desempenho em cada segmento
- Deixa as máquinas invisíveis para as pessoas em outros segmentos de rede local
- Pode fornecer segurança avançada
- Pode melhorar a organização de rede

Desvantagens:

- Exige o uso de roteamento (camada de distribuição)
- O roteador pode retardar o tráfego entre segmentos
- Mais complexidade e custos (exige roteador)

![[Pasted image 20260610070434.png]]

## 14.3.3 Packet Tracer - Observar o fluxo de tráfego em uma rede roteada

Nesta atividade do Packet Tracer, você atingirá os seguintes objetivos:

- Parte 1: Observar o fluxo de tráfego em uma LAN não roteada
- Parte 2: Reconfigurar a rede para rotear entre LANs
- Parte 3: Observar o fluxo de tráfego na rede roteada

### Packet Tracer - Observar o fluxo de tráfego em uma rede roteada

#### Objetivos

Parte 1: Observar o fluxo de tráfego em uma LAN não roteada

Parte 2: Reconfigurar a Rede para Roteamento entre LANs

Parte 3: Observar o fluxo de tráfego na Rede Roteada

#### Histórico/Cenário

Foi pedido à empresa na qual você trabalha que propusesse um novo design de rede para a XYZ LLC. A empresa XYZ é uma startup que recentemente obteve sucesso ofertando seus produtos. Eles estão se expandindo e sua rede precisa crescer junto com eles. Atualmente, a rede está configurada com uma única rede IP para hosts em todos os departamentos. Esse design tornou-se ineficiente e os atrasos de rede estão se tornando cada vez mais perceptíveis. Você foi indicado para ajudar a equipe de vendas a preparar a proposta. A equipe de vendas proporá uma solução na qual a eficiência da rede é aprimorada pela implementação de roteamento entre redes separadas para diferentes departamentos. Você está trabalhando uma demonstração de como ter várias redes roteadas em uma empresa pode melhorar a eficiência da rede. Siga as instruções para passar a demonstração que ajudará a propor uma nova rede à XYZ LLC.

#### Instruções

#### Parte 1: Observar o fluxo de tráfego em uma LAN não roteada

A rede XYZ consiste em cerca de 150 dispositivos conectados a uma LAN. A LAN é configurada em uma única rede IPv4. Hosts em diferentes departamentos são conectados a switches que são conectados ao roteador **Edge** (roteador de borda). O roteador apenas roteia o tráfego entre a LAN e a internet, representada pela nuvem **ISP**. Como apenas uma rede IP é usada na LAN, todos os departamentos estão na mesma rede.

A topologia do Packet Tracer está simplificada. Ele mostra apenas alguns dos departamentos e hots. Considere que o comportamento que você irá demonstrar está acontecendo em uma escala muito maior do que o que é mostrado na rede PT.

Nesta parte, você usará o modo de simulação do Packet Tracer para observar como o tráfego flui através de LANs não roteadas.

#### Etapa 1: Limpe o cache do ARP do host Sales 1.

Passe o mouse sobre o host **Sales 1** para ver seu endereço IP. Tome nota disso.

a.  Clique em **Sales 1** > guia **Desktop**> **Command** **Prompt** e insira o comando **arp** **-a** Não deverá haver endereços MAC no cache ARP. Se houver entradas no cache ARP, use o comando **arp -d** para excluí-las.

#### Etapa 2: Observe o fluxo de tráfego na rede.

a.  Clique no botão **Simulation** mode no canto inferior direito da janela do PT para alternar do modo em **Realtime** (Tempo Real) para o modo **Simulation** (Simulação).

b.  Abra o **Command Prompt** para o **Sales 2** e, em seguida, insira o comando **ping** seguido pelo endereço IP de **Sales 1**.

c.  Use o botão **Capture then Forward** (o triângulo apontando para a direita com uma barra vertical anexada) nos **Play Controls** do **Simulation Panel** para que o comando **ping** comece a ser executado. Você verá um ícone de envelope colorido ao lado de Sales 2. Isso representa uma PDU. Clique no botão **Capture then Forward** para mover a PDU para o primeiro dispositivo do caminho rumo ao dispositivo de destino. Clique no envelope da PDU para inspecionar o conteúdo.

#### Perguntas:

Quais são os endereços MAC e IP de origem e destino do quadro e do pacote?

Área de Resposta

O endereço MAC de origem do quadro é o endereço MAC de Sales 1. O endereço MAC de destino é o endereço MAC de broadcast FFFF.FFFF.FFFF. O endereço IP de origem do pacote é o endereço IP de Sales 1. O endereço IP de destino é o de Sales 2, que é o destino.

Ocultar resposta

Por que o endereço MAC de destino é o endereço de broadcast?

Área de Resposta

Como o cache ARP do host está vazio, o host deve primeiro realizar uma solicitação ARP, para obter o endereço MAC de destino, de modo que o quadro possa ser endereçado ao Sales 1.

Ocultar resposta

d.  Avance as PDUs pela rede até que uma nova PDU (cor diferente) seja criada em **Sales 2**.

#### Perguntas:

Quais hosts e outros tipos de dispositivos precisam processar os pacotes de solicitação ARP?

Área de Resposta

Todos os hosts e a interface do roteador

Ocultar resposta

Qual é o impacto disso na eficiência de operação da rede, do modo que está configurada atualmente?

Área de Resposta

Mesmo que o destino do ping solicitações podem ser adjacentes à fonte solicitante, se o host tiver um ARP vazio cache, é enviada uma solicitação ARP que deve ser processada por cada host no rede. As entradas de cache ARP são removidas após um período predefinido. Com muitos hosts em uma rede, As transmissões ARP serão emitidas com mais frequência. Isso requer recursos de rede ser retirado para o tráfego relacionado ao trabalho.

Ocultar resposta

e.  Uma nova PDU com uma cor diferente apareceu em Sales 2. Clique na nova PDU e inspecione seu conteúdo. Veja o Outbound PDU Details

#### Pergunta:

Que tipo de PDU é essa?

Área de Resposta

É o primeiro pacote de solicitação de eco ICMP que é emitido pelo ping do host Sales 2.

Ocultar resposta

f.   Volte ao modo **Realtime**.

#### Parte 2: Reconfigure a rede para rotear entre LANs.

Nesta parte, você demonstrará os benefícios do roteamento entre redes de departamentos. Primeiro, você irá cabear cada switch da rede para conectar-se diretamente a uma interface do roteador. Em seguida, você reconfigurará os hosts para receber endereços em duas novas redes IPv4 criadas pelo roteador.

#### Etapa 1: Alterar as conexões dos dispositivos.

Os três switches são conectados entre si com cabos diretos de cobre (straight through).

a.  Para o cabo que conecta o switch **Accounting** ao switch **Finance**, clique no triângulo verde mais próximo do switch **Accounting**.

b.  Arraste essa extremidade do cabo para o roteador **Edge** e conecte o cabo à porta **GigabitEthernet 1/0**.

c.  Repita esta etapa para o link entre **Finance** e **Sales**. Conecte à porta GigabitEthernet disponível.

#### Etapa 2: Configure os hosts com endereços nas novas LANs.

Cada interface do roteador **Edge** foi previamente configurada para colocar cada departamento em sua própria rede IPv4. Os hosts receberão do roteador seus novos endereços IP. No entanto, levará algum tempo para que os hosts nas redes **Finance** e **Sales** recebam seus novos endereços IP. (Os hosts na rede Accounting permanecerão em 192.168.1.0/24.)

a.  Para acelerar o processo de obtenção de novos endereços IP, abra um **Command Prompt** em cada um dos quatro dispositivos nas redes **Finance** e **Sales**.

b.  Digite o comando **ipconfig /renew**. Isso forçará o host a solicitar um novo endereço IP ao servidor DHCP que está sendo executado no roteador **Edge**. Você deverá ver a confirmação do novo endereçamento IP.

Qual rede IPv4 está atribuída à rede **Finance**?

Área de Resposta

192.168.2.0/24

Ocultar resposta

Qual rede IPv4 está atribuída à rede **Sales**?

Área de Resposta

192.168.3.0/24

Ocultar resposta

#### Parte 3: Observe o fluxo de tráfego na rede roteada.

Nesta parte, você observará como o tráfego agora flui através de uma rede roteada.

#### Etapa 1: Ping Sales 1 a partir de Sales 2

a.  Retorne ao **Command Prompt** de **Sales 2** e verifique se o cache ARP está vazio. Se não estiver, exclua todas as entradas.

b.  Mude para o modo **Simulation**.

c.  Ping **Sales 1** a partir de **Sales 2**

d.  Use o botão **Capture then Forward** para que as PDUs percorram a rede. Observe como a mensagem de solicitação ARP flui pela rede desta vez.

#### Pergunta:

Quais dispositivos recebem os broadcasts  ARP desta vez?

Área de Resposta

Somente o Sales 1 e a interface do roteador conectada à rede do departamento Sales processam a PDU.

Ocultar resposta

#### Etapa 2: Pingue outros hosts.

Repita esta demonstração pingando outros hosts e o internet server. Observe o fluxo das PDUs de ARP request.

#### Pergunta:

Qual é o benefício em usar várias redes IPv4, ou sub-redes, em uma empresa?

Área de Resposta

Um dos principais benefícios do uso de várias redes IP é a contenção de tráfego em partes relevantes da rede sem afetar o desempenho em partes irrelevantes da rede.

Ocultar resposta

**Observação:** a topologia de rede usada na atividade é apenas para fins de demonstração. Embora seja possível que uma rede corporativa real possa usar um roteador dessa maneira, existem topologias mais adequadas para atingir esses resultados. Você aprenderá sobre outras abordagens de design em cursos de rede posteriores.


## 14.3.4 Packet Tracer - Criar uma LAN

Nesta atividade do Packet Tracer, você atingirá os seguintes objetivos:

- Conecte hosts e dispositivos de rede
- Configurar dispositivos com endereçamento IPv4
- Verificar a configuração do dispositivo final e a conectividade
- Usar os comandos de rede para exibir informações do host

Packet Tracer - Criaando uma LAN

#### Tabela de Endereçamento

| Dispositivo  | Interface/Porta | Endereço IPv4   | Máscara de sub-rede |
| ------------ | --------------- | --------------- | ------------------- |
| Admin PC     | NIC             | DHCP            | N/D                 |
| Manager PC   | NIC             | DHCP            | N/D                 |
| Printer      | NIC             | 192.168.1.100   | 255.255.255.0       |
| www.cisco.pt | NIC             | 209.165.200.225 | N/D                 |
#### Objetivos

=  Conectar hosts e dispositivos de rede

=  Configurar dispositivos com endereçamento IPv4

=  Verificar a configuração do dispositivo final e a conectividade

=  Usar os comandos de rede para exibir informações de host

## Histórico/Cenário

Uma nova filial está sendo aberta e pediram para você configurar a LAN. Os dispositivos de rede já estão configurados, mas você precisa conectá-los aos hosts. Você também precisa configurar o endereçamento IPv4 dos dispositivos finais e verificar se eles podem alcançar recursos locais e remotos.

## Instruções

## Parte 1: Conectar dispositivos de rede e hosts

### Etapa 1: Ligue os dispositivos finais e o Office Router.

a.  Clique em cada dispositivo e abra a guia Physical. **Nota**: Não há chave de alimentação no modelo de switch usado nesta atividade.

b.  Localize o  botão liga / desliga de cada dispositivo na janela de exibição de dispositivos físicos.

c.  Clique no botão liga / desliga para ligar o dispositivo. Você deverá ver uma luz verde perto do botão liga/desliga indicando que o dispositivo está ligado.

### Etapa 2: Conecte os dispositivos finais.

Use a tabela e as instruções para conectar os dispositivos de rede e hosts para criar a rede física.

Tabela de conexões

|||||
|---|---|---|---|
|||||
|||||
|||||
|||||
|||||

**Nota:** Na tabela acima, as interfaces designadas com **G** são interfaces GigabitEthernet. As interfaces designadas com **F** são interfaces FastEthernet.

a.  Conecte os dispositivos de rede de acordo com as informações na **Tabela de conexões** usando cabos Ethernet copper straight-through . Para a conexão da Internet com o Office Router, selecione o dispositivo e a porta nos menus suspensos que aparecem quando você clica na nuvem com a ferramenta de conexões selecionada.

b.  Conecte os dois PCs e a impressora ao switch do escritório de acordo com as informações na tabela de conexões. Use cabos copper straight-through (diretos)

c.  Você verá luzes de link verdes em todas as conexões após um breve intervalo de tempo.

## Parte 2: Configurar dispositivos com endereçamento IPv4

### Etapa 1: Configure os hosts com as informações de endereçamento.

a.  Os PCs Admin e Manager devem receber as informações de endereçamento IP via DHCP. O Office Router foi configurado para fornecer endereços IP aos hosts na LAN da filial. Clique nos PCs e vá para as guias Desktop em cada PC. Abra o aplicativo IP Configuration e configure os PCs para receberem seus endereços IP dinamicamente.

b.  Impressoras e servidores geralmente são configurados manualmente com endereçamento porque outros dispositivos na rede são configurados para acessá-los usando endereços IP. A configuração manual com um endereço estático garantirá que os endereços IP desses dispositivos não sejam alterados.

1)  Clique na impressora e abra a guia Config.

2)  Clique na interface FastEthernet0 no painel esquerdo.

3)  Insira as informações de endereçamento da tabela de endereçamento.

c.  Como os dois computadores estão na mesma rede, seus endereços IPv4 serão semelhantes, suas máscaras de sub-rede e gateways padrão serão idênticos.

#### Perguntas:

Por que você acha que os endereços IPv4 são diferentes, mas as máscaras de sub-rede e os gateways padrão são os mesmos?

Área de Resposta

As respostas vão variar. Cada dispositivo na rede deve ter um identificador exclusivo. O endereço IPv4 é uma maneira de identificar exclusivamente cada host ou dispositivo de rede. O gateway padrão representa a forma de comunicação com dispositivos que NÃO estão na rede local.

Ocultar resposta

A impressora não requer um gateway padrão porque só será acessada por hosts na rede local. No entanto, se você precisar configurá-la com um gateway padrão, qual valor a impressora usará? Como você pode determinar isso dos outros dispositivos na rede?

Área de Resposta

Você pode determinar o valor de gateway padrão a ser usado observando os valores com os quais os PCs foram configurados pelo DHCP ou determinando o endereço IP da interface Ethernet do Office Router que está conectada à LAN da filial.

Ocultar resposta

## Parte 3: Verificar a configuração do dispositivo final e a conectividade

### Etapa 1: Verifique a conectividade entre os dois PCs.

a.  Acesse os desktops dos PCs e verifique a configuração de endereçamento IP. Você deverá ver que os PCs receberam endereços IP dinamicamente na rede 192.168.1.0 255.255.255.0. Você também deverá ver que eles receberam endereços para configurar o Gateway padrão e o servidor DNS.

b.  No prompt de comando do Admin PC, pingue o endereço IP da impressora. Repita este processo para o Manager PC. Você deverá ver pings bem-sucedidos para cada um. Isso verifica se os PCs e a impressora estão ligados e conectados e endereçados corretamente.

### Etapa 2: Verifique a conectividade com a internet.

No Desktop dos PCs, abra o navegador Web. Digite o endereço IP do servidor de internet para exibir a página web. Repita o processo, mas conecte usando a URL do servidor.

#### Pergunta:

Se você pode conectar pelo endereço IP, mas não pela URL, qual você acha que é a causa desse problema?

Área de Resposta

Como o DNS é usado para resolver URLs para endereços IP, você pode afirmar com segurança que o servidor DNS não está acessível. Isso pode ser devido a um problema de conectividade de rede ou porque o endereço do servidor DNS configurado nos hosts está ausente ou está incorreto

Ocultar resposta

## Parte 4: Use os comandos de rede para exibir informações de host

Os comandos de rede disponíveis no prompt de comando em PCs são muito semelhantes aos disponíveis no Windows. Nesta parte da atividade, você usará **ipconfig** e **tracert** conhecer melhor a LAN.

### Etapa 1: Use o comando ipconfig.

O comando ipconfig exibe detalhes sobre o endereçamento configurado em um host.

#### Pergunta:

Abra um prompt de comando em um dos PCs e digite o comando **ipconfig** e anote as informações retornadas. Agora digite o comando **ipconfig /all**. Quais informações adicionais são exibidas?

Área de Resposta

O ipconfig /all exibe informações sobre o endereço físico (MAC) da NIC. Ele também exibe os endereços dos servidores DHCP e DNS. No Windows, muitos detalhes adicionais são exibidos. Digite ipconfig /all no prompt de comando de um PC para exibir todas as informações que o Windows exibe com este comando.

Ocultar resposta

### Etapa 2: Use o comando tracert

O comando tracert usa o ICMP para retornar informações sobre os roteadores que são passadas à medida que os pacotes vão do PC de origem para o destino.

Rastreie o caminho para um destino remoto abrindo um dos PCs e digitando **tracert** seguido da URL do servidor web.

#### Perguntas:

Quantos roteadores são atravessados no caminho para o destino? Como esses roteadores são identificados?

Área de Resposta

Dois. Eles são identificados pelos endereços IP das interfaces de entrada dos roteadores.

Ocultar resposta

Onde está localizado o segundo roteador?

Área de Resposta

Está na nuvem da internet.

Ocultar resposta

## Reflexão

Considere um pequeno escritório que tenha uma LAN semelhante à que você criou aqui. Qual é o maior desafio das instalações ao configurar a rede em um novo local?

Área de Resposta

A infraestrutura de cabeamento físico. O escritório precisa estar conectado e ter tomadas de comunicação para todos os dispositivos. Além disso, as tomadas precisam estar em locais convenientes. Além disso, as tomadas devem ser conectadas a um local central onde o switch e o roteador estão localizados. O cabeamento físico pode apresentar muitos problemas quando criado em um novo local, no escritório.


# 14.4 Resumo de roteamento entre redes

### A necessidade do roteamento

À medida que as redes crescem, geralmente é necessário dividir uma rede de camada de acesso em várias redes de camada de acesso. As diversas formas de divisão de redes são definidas por critérios diferentes.

- **Contenção** de broadcast — Roteadores na camada de distribuição podem limitar broadcasts somente para a rede local onde devam ser escutados.
- **Requisitos de** segurança — Os roteadores na camada de distribuição podem separar e proteger determinados grupos de computadores onde residem informações confidenciais.
- **Localização físicos** — Os roteadores na camada de distribuição podem ser usados para interconectar redes locais em vários locais de uma organização que estão separados geograficamente.
- **Agrupamento** lógico — Os roteadores na camada de distribuição podem ser usados para agrupar logicamente usuários, como departamentos de uma empresa, que tenham necessidades comuns ou acesso a recursos.

A camada de distribuição conecta estas redes locais independentes e controla o fluxo do tráfego entre elas. Ela é responsável por garantir que o tráfego entre hosts na rede local permaneça local.

Um roteador é um dispositivo de rede que conecta várias redes IP de Camada 3. Na camada de distribuição da rede, os roteadores direcionam o tráfego e realizam outras funções essenciais em uma operação de rede eficiente. Os roteadores, como switches, conseguem decodificar e ler as mensagens que são enviadas para eles. Ao contrário dos switches, que tomam uma decisão de encaminhamento com base no endereço MAC da Camada 2, os roteadores fundamentam suas decisões de encaminhamento no endereço IP da Camada 3.

Sempre que a porção de rede dos endereços IP dos hosts de origem e de destino não coincidir, deverá ser usado um roteador para encaminhar a mensagem.

---

### A tabela de roteamento

Cada porta ou interface em um roteador conecta-se a uma rede local diferente. Cada roteador contém uma tabela de todas as redes localmente conectadas e as interfaces que se conectam a essas redes.

Quando um roteador recebe um quadro, ele decodifica o quadro para obter o pacote que contém o endereço IP de destino. Ele combina a porção de rede do endereço IP de destino com as redes listadas na tabela de roteamento. Se o endereço de rede de destino estiver na tabela, o roteador encapsulará o pacote em um novo quadro para enviá-lo. Ele encaminha o novo quadro para a rede de destino, fora da interface associada ao caminho. O processo de encaminhamento de pacotes para a rede destino é chamado de roteamento.

Um roteador encaminha um pacote para um destes dois locais: a) uma rede diretamente conectada que contém o host de destino real ou b) outro roteador no caminho para o host de destino. Quando um roteador encapsula o quadro para encaminhá-lo para uma interface roteada, ele deve incluir um endereço MAC de destino. Se o roteador precisar encaminhar o pacote para outro roteador por meio de uma interface roteada, ele usará o endereço MAC do roteador conectado. Os roteadores obtêm esses endereços MAC nas tabelas ARP.

Um host conhece o endereço IPv4 do roteador por meio do endereço de gateway padrão configurado em suas configurações de TCP/IP. O endereço do gateway padrão é o endereço da interface do roteador conectada à mesma rede local do host de origem. Todos os hosts na rede local usam o endereço do gateway padrão para enviar mensagens ao roteador.

Tabelas de roteamento contêm endereços de redes e o melhor caminho para acessar essas redes. As entradas podem ser feitas na tabela de roteamento de duas maneiras: atualizadas dinamicamente por informações recebidas de outros roteadores na rede ou inseridas manualmente por um administrador de rede.

---

### Criando uma LAN

LAN refere-se a uma rede local ou a um grupo de redes locais interconectadas que estão sob o mesmo controle administrativo. Todas as redes locais dentro de uma LAN estão sob um controle administrativo. Outras características comuns das LANs são que elas normalmente usam protocolos Ethernet ou Wireless e suportam altas taxas de transmissão de dados.

Dentro de uma LAN, é possível colocar todos os hosts em uma única rede local ou dividi-los entre várias redes conectadas por um dispositivo na camada de distribuição.

Colocar todos os hosts em uma única rede local permite que eles sejam vistos por todos os outros hosts. Isso ocorre porque existe um domínio da broadcast e os hosts usam o ARP para se localizarem.

Colocando hosts adicionais em uma rede remota diminuirá o impacto em demandas de tráfego. No entanto, os hosts em uma rede não poderão se comunicar com hosts na outra rede sem o uso de roteamento. Os roteadores aumentam a complexidade da configuração de rede e podem introduzir latência (ou seja, atraso) nos pacotes enviados de uma rede local para outra.


## 14.4.2 Webster — Questões para Reflexão

Na minha rede doméstica (LAN), geralmente não tenho tráfego de rede suficiente para que haja congestionamento, embora isso possa acontecer quando todos os meus filhos estiverem transmitindo filmes diferentes e eu estiver tentando enviar um documento para o meu trabalho. Você consegue pensar em uma maneira de dividir minha LAN em várias redes?