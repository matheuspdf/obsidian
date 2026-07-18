
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
![[14.1.1.mp4#subtitle=anexos/14.1.1.vtt]]
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
![[brave_HcYmVzuVFp.mp4]]


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

![[14.2.1.mp4#subtitle=anexos/14.2.1.vtt]]
Neste vídeo, veremos como um roteador encaminha pacotes de uma rede para outra rede.

Neste exemplo, temos o Host em 10.0.0.1 que deseja enviar um pacote para 192.168.1.2, que está em outra rede. Portanto, o endereço IP de origem do pacote será 10.0.0.1 e o endereço IPv4 de destino do pacote será 192.168.1.2.

Então H1 envia o pacote para seu gateway padrão, o roteador. Ele envia para o roteador porque H1 sabe que o destino — H4, seu endereço IPv4 — está em uma rede diferente.

O roteador recebe o pacote e procura o endereço IPv4 de destino do pacote em sua tabela de roteamento. Ele percebe que o endereço IPv4 de destino 192.168.1.2 está na rede 192.168.1.0, e que essa rede está em sua interface Fast Ethernet 02. Assim, o roteador irá encaminhar este pacote para fora de sua Interface Fast Ethernet 02 para o destino final.

Agora, neste caso, H1 tem um pacote para enviar para o endereço IPv4 de destino 255.255.255.255. Como você deve se lembrar, esse é um endereço de broadcast. Assim, uma transmissão será enviada para todos os dispositivos em sua rede. Você notará que o roteador receberá esta transmissão, mas não encaminhará este pacote para outras redes.


## 14.2.2 Vídeo - Mensagens dentro de uma rede e entre redes - Parte 1
![[14.2.2.mp4#subtitle=anexos/14.2.2.vtt]]
Neste vídeo, vamos dar uma olhada em como as mensagens viajam dentro de uma rede e também entre redes.

Nesta primeira parte, temos o host H1 em 192.168.1.10 que vai enviar um pacote para o endereço IPv4 de H2, 192.168.1.20.

H1, a origem do pacote, constrói o pacote IPv4 com seu próprio endereço como fonte, 192.168.1.10, e o endereço IPv4 de destino de 192.168.1.20.

A primeira coisa que H1 precisa determinar é: estamos na mesma rede? Ele percebe que seu próprio endereço de rede é 192.168.1.10 — essa é a rede à qual pertence — e ele usa sua máscara de sub-rede para fazer isso. Em seguida, ele analisa o endereço IPv4 de destino e, usando sua própria máscara de sub-rede, H1 determina que H2, em 192.168.1.20, está na mesma rede, pois ambos começam com 192.168.1.

O que isso significa para H1 é que ele pode enviar este pacote diretamente para H2, sem precisar enviar através do seu gateway padrão, o roteador. Ele pode enviá-lo diretamente.

Então, H1 vai construir o quadro Ethernet com seu próprio endereço MAC de sua NIC Ethernet, AA:AA, como o endereço MAC de origem Ethernet. Para o endereço MAC de destino, ele diz: "Posso enviá-lo diretamente para H2 porque estamos na mesma rede. Eu só preciso saber o endereço MAC associado ao destino, 192.168.1.20."

Nesse caso, H1 verifica sua tabela ARP. Supondo que tem essa informação em sua tabela ARP, ele sabe que 192.168.1.20 tem o endereço MAC BB:BB. Se ele não souber disso, lembre-se de que ele envia uma solicitação ARP, obtém uma resposta ARP e adiciona à tabela.

Agora, H1 pode ir em frente e enviar este quadro Ethernet em direção ao switch, e ele é enviado diretamente para H2.

## 14.2.3 Vídeo - Mensagens dentro de redes e entre redes - Parte 2
![[14.2.3.mp4#subtitle=anexos/14.2.3.vtt]]
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

> [!example]- 🖧 Recursos do Lab
> - 📄 [[anexos/14.3.3.html|Instruções]]
> - 📥 [[anexos/14.3.3.pka|Abrir no Packet Tracer]]

---
## 14.3.4 Packet Tracer - Criar uma LAN

Nesta atividade do Packet Tracer, você atingirá os seguintes objetivos:

- Conecte hosts e dispositivos de rede
- Configurar dispositivos com endereçamento IPv4
- Verificar a configuração do dispositivo final e a conectividade
- Usar os comandos de rede para exibir informações do host

Packet Tracer - Criaando uma LAN


> [!example]- 🖧 Recursos do Lab
> - 📄 [[anexos/14.3.4.html|Instruções]]
> - 📥 [[anexos/14.3.4.pka|Abrir no Packet Tracer]]

---
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