
# 22.0 Introdução

## 22.0.1 Webster - Por que devo fazer este módulo?

Olá novamente! Bob também precisou aprender muito sobre a camada de rede em seus cursos antes de se tornar um especialista em TI. A camada de rede, ou Camada OSI 3, fornece serviços para permitir que dispositivos finais troquem dados entre redes. IPv4 e IPv6 são os principais protocolos de comunicação da camada de rede. Os protocolos da camada de rede realizam quatro operações: endereçamento de dispositivos finais, encapsulamento, roteamento e desencapsulamento.

Isso parece muita informação para pessoas como Marcy e Vincent, que não têm conhecimento de redes! Parece esmagador para você? Este módulo ajudará você a entender a camada da rede.


## 22.0.2 O que vou aprender neste módulo?

**Titulo do Módulo:** Camada de Rede

**Objetivo do Módulo:** Explicar como os roteadores usam protocolos e serviços da camada de rede para habilitar a conectividade de ponta a ponta.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Características de camada de rede|Explicar como a camada de rede usa protocolos IP para comunicações confiáveis.|
|Pacote IPv4|Explicar a função dos principais campos do cabeçalho no pacote IPv4.|
|Pacote IPv6|Explicar a função dos principais campos do cabeçalho no pacote IPv6.|


# 22.1 Características de camada de rede

## 22.1.1 Vídeo - Encapsulamento de Dados

**Selecione o botão Reproduzir para assistir ao vídeo.**

Usando o modelo OSI, vamos dar uma olhada em um exemplo do processo de encapsulamento.

Quando um usuário insere uma URL em um navegador da Web, ela se torna parte dos dados que solicitam a página da Web de um servidor web. Esses dados são então enviados para a camada 7, o protocolo da camada de aplicação — nesse caso, HTTPS. O processo HTTPS encapsula os dados com um cabeçalho HTTPS. A PDU, ou unidade de dados do protocolo, é conhecida como dados.

Em seguida, o cabeçalho HTTPS e os dados originais são enviados para a camada 4, o protocolo da camada de transporte — neste exemplo, TCP. O processo TCP encapsula o cabeçalho HTTPS e os dados originais com um cabeçalho TCP. O cabeçalho e os dados HTTPS anteriores se tornam a porção de dados do segmento da camada de transporte.

Em seguida, o segmento TCP é enviado para a camada 3, o protocolo da camada de rede — neste exemplo, IPv4. O processo IPv4 encapsula o cabeçalho TCP e os dados com um cabeçalho IPv4, que se torna a porção de dados desse pacote da camada de rede.

Em seguida, o pacote IPv4 é enviado para a camada 2, o protocolo da camada de enlace de dados, que normalmente é a Ethernet. O processo Ethernet encapsula o cabeçalho IPv4 e os dados com o cabeçalho Ethernet e o trailer, que se torna a porção de dados desse quadro da camada de enlace de dados.

Por fim, o quadro de enlace de dados é enviado para a NIC, ou placa de interface de rede, como bits físicos na mídia com ou sem fio da rede.

O protocolo e os dados de cada camada se tornam a porção de dados do próximo protocolo. Cada protocolo aceita o cabeçalho do protocolo anterior nos dados e então encapsula essas informações como dados com um cabeçalho de protocolo adicional. A camada de enlace de dados é a única camada que também acrescenta um trailer Ethernet.


## 22.1.2 A Camada de Rede

Protocolos da Camada de Rede

A camada de rede, ou Camada OSI 3, fornece serviços para permitir que dispositivos finais troquem dados entre redes. Como mostrado na figura, IP versão 4 (IPv4) e IP versão 6 (IPv6) são os principais protocolos de comunicação de camada de rede. Outros protocolos de camada de rede incluem protocolos de roteamento, como OSPF (Open Shortest Path First) e protocolos de mensagens, como ICMP (Internet Control Message Protocol).

### Protocolos da Camada de Rede

![[Pasted image 20260617063146.png]]

Para realizar comunicações de ponta a ponta através dos limites da rede, os protocolos de camada de rede executam quatro operações básicas:

- **Endereçamento de dispositivos finais** – Os dispositivos finais devem ser configurados com um endereço IP exclusivo para identificação na rede.
- **Encapsulamento** – A camada de rede encapsula a unidade de dados de protocolo (PDU) da camada de transporte em um pacote. O processo de encapsulamento adiciona informações de cabeçalho IP, como os endereços IP dos hosts origem (emissor) e destino (receptor). O processo de encapsulamento é executado pela origem do pacote IP.
- **Roteamento** – A camada de rede fornece serviços para direcionar os pacotes para um host de destino em outra rede. Para trafegar para outras redes, o pacote deve ser processado por um roteador. A função do roteador é escolher o melhor caminho e direcionar os pacotes para o host de destino em um processo conhecido como roteamento. Um pacote pode atravessar muitos roteadores antes de chegar ao host de destino. Cada roteador que um pacote atravessa para chegar ao host de destino é chamado de salto.
- **Desencapsulamento -** Quando o pacote chega à camada de rede do host de destino, o host verifica o cabeçalho IP do pacote. Se o endereço IP de destino no cabeçalho corresponder ao seu próprio endereço IP, o cabeçalho IP será removido do pacote. Depois que o pacote é desencapsulado pela camada de rede, a PDU resultante da Camada 4 é transferida para o serviço apropriado na camada de transporte. O processo de desencapsulamento é executado pelo host de destino do pacote IP.

Diferentemente da camada de transporte (OSI Layer 4), que gerencia o transporte de dados entre os processos em execução em cada host, os protocolos de comunicação da camada de rede (ou seja, IPv4 e IPv6) especificam a estrutura de pacotes e o processamento usado para transportar os dados de um host para outro hospedeiro. A operação sem levar em consideração os dados contidos em cada pacote permite que a camada de rede transporte pacotes para diversos tipos de comunicações entre vários hosts.

**Clique em Reproduzir na figura para ver uma animação que demonstra a troca de dados.**

![[Pasted image 20260617064822.png]]

![[Pasted image 20260617064840.png]]

![[Pasted image 20260617064859.png]]

![[Pasted image 20260617064925.png]]

![[Pasted image 20260617064946.png]]

![[Pasted image 20260617065016.png]]

![[Pasted image 20260617065046.png]]

## 22.1.3 Encapsulamento IP

O IP encapsula o segmento da camada de transporte (a camada logo acima da camada de rede) ou outros dados adicionando um cabeçalho IP. O cabeçalho IP é usado para entregar o pacote ao host de destino.

A figura ilustra como a PDU da camada de transporte é encapsulada pela PDU da camada de rede para criar um pacote IP.

![[Pasted image 20260617065107.png]]

O processo de encapsulamento camada por camada possibilita o desenvolvimento e a expansão dos serviços nas diferentes camadas sem afetar outras camadas. Isso significa que os segmentos da camada de transporte podem ser imediatamente empacotados por IPv4 , IPv6 ou qualquer protocolo que venha a ser desenvolvido no futuro.

O cabeçalho IP é examinado por dispositivos de Camada 3 (ou seja, roteadores e switches de Camada 3) à medida que viaja através de uma rede até seu destino. É importante notar que as informações de endereçamento IP permanecem as mesmas desde o momento em que o pacote sai do host de origem até chegar ao host de destino, exceto quando traduzidas pelo dispositivo que executa a Tradução de Endereços de Rede (NAT) para IPv4.

**Observação**: O NAT é discutido em módulos posteriores.

Os roteadores implementam protocolos de roteamento para rotear pacotes entre redes. O roteamento realizado por esses dispositivos intermediários examina o endereçamento da camada de rede no cabeçalho do pacote. Em todos os casos, a parte de dados do pacote, ou seja, a PDU da camada de transporte encapsulada ou outros dados, permanece inalterada durante os processos da camada de rede.

## 22.1.4 Características do IP

O IP foi desenvolvido como um protocolo com baixa sobrecarga. Ele fornece apenas as funções necessárias para enviar um pacote de uma origem a um destino por um sistema interconectado de redes. O protocolo não foi projetado para rastrear e gerenciar o fluxo de pacotes. Essas funções, se exigido, são realizadas por outros protocolos em outras camadas, principalmente TCP na Camada 4.

Estas são as características básicas da IP:

- **Sem conexão** - Não há conexão com o destino estabelecido antes do envio de pacotes de dados.
- **Melhor esforço** - o IP é inerentemente não confiável, porque a entrega de pacotes não é garantida.
- **Independente da mídia** - A operação é independente do meio (ou seja, cobre, fibra ótica ou sem fio) que carrega os dados.


## 22.1.5 Sem Conexão

Sem conexão - Analogia

O IP não tem conexão, o que significa que nenhuma conexão ponta a ponta dedicada é criada pelo IP antes que os dados sejam enviados. A comunicação sem conexão é conceitualmente semelhante a enviar uma carta a alguém sem notificar o destinatário com antecedência. A figura resume esse ponto-chave.

### Sem conexão - Analogia

![[Pasted image 20260617065141.png]]

### Sem conexão - Rede

As comunicações de dados sem conexão funcionam com o mesmo princípio. Como mostra a figura, o IP não requer troca inicial de informações de controle para estabelecer uma conexão ponto a ponto antes do encaminhamento dos pacotes.

### Sem conexão - Rede

![[Pasted image 20260617065219.png]]

## 22.1.6 Melhor Esforço

O IP também não requer campos adicionais no cabeçalho para manter uma conexão estabelecida. Esse processo reduz bastante a sobrecarga do IP. No entanto, sem conexão de ponta a ponta pré-estabelecida, os remetentes não sabem se os dispositivos de destino estão presentes e funcionais ao enviar pacotes, nem sabem se o destino recebe o pacote ou se o dispositivo de destino pode acessar e ler o pacote.

O protocolo IP não garante que o pacote enviado seja, de fato, recebido. A figura ilustra a característica de entrega não confiável ou de melhor esforço do protocolo IP.

![[Pasted image 20260617065235.png]]

## 22.1.7 Independente de Mídia

Não confiável significa que o IP não tem a capacidade de gerenciar e recuperar pacotes não entregues ou corrompidos. Isso ocorre porque, embora os pacotes IP sejam enviados com informações sobre o local da entrega, eles não contêm informações que podem ser processadas para informar ao remetente se a entrega foi bem-sucedida. Os pacotes podem chegar ao destino corrompidos, fora de sequência ou simplesmente não chegar. O IP não tem capacidade de retransmitir os pacotes em caso de erros.

Se os pacotes forem entregues fora de ordem ou estiver faltando algum pacote, as aplicações que usam os dados, ou serviços de camada superior, deverão resolver esses problemas. Isso permite que o IP funcione de forma bem eficiente. No conjunto de protocolos TCP / IP, a confiabilidade é o papel do protocolo TCP na camada de transporte.

O IP opera independentemente da mídia que transporta os dados nas camadas inferiores da pilha de protocolos. Conforme mostra a figura, os pacotes IP podem ser comunicados como sinais elétricos por cabo de cobre, sinais ópticos nas fibras ou sinais de rádio em redes sem fio.

![[Pasted image 20260617065249.png]]

A camada de enlace de dados OSI é responsável por pegar um pacote IP e prepará-lo para transmissão pelo meio de comunicação. Isso significa que a entrega de pacotes IP não se limita a nenhum meio específico.

Há, no entanto, uma característica muito importante dos meios físicos que a camada de rede considera: o tamanho máximo da PDU que cada meio consegue transportar. Essa característica é chamada de unidade máxima de transmissão (maximum transmission unit - MTU). Parte das comunicações de controle entre a camada de enlace de dados e a camada de rede é a definição de um tamanho máximo para o pacote. A camada de enlace de dados passa o valor da MTU para a camada de rede. A camada de rede então determina o tamanho que os pacotes podem ter.

Em alguns casos, um dispositivo intermediário, geralmente um roteador, deve dividir um pacote IPv4 ao encaminhá-lo de um meio para outro com uma MTU menor. Esse processo é chamado fragmentação do pacote ou fragmentação. A fragmentação causa latência. Os pacotes IPv6 não podem ser fragmentados pelo roteador.


## 22.1.8 Verifique sua compreensão - Características de IP

**Verifique sua compreensão das características de IP escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Qual camada OSI envia segmentos para serem encapsulados em um pacote IPv4 ou IPv6?

- [ ] camada de enlace de dados
- [ ] camada de rede
- [x] camada de transporte
- [ ] camada de sessão

✅ RESPOSTA CORRETA: camada de transporte

> Camada de Transporte PDUs, chamados de segmentos, são encapsulados na camada de rede por IPv4 e IPv6 em pacotes.

---

### Pergunta 2

Qual camada é responsável por pegar um pacote IP e prepará-lo para transmissão pelo meio de comunicação?

- [ ] camada física
- [ ] camada de rede
- [x] camada de enlace de dados
- [ ] camada de transporte

✅ RESPOSTA CORRETA: camada de enlace de dados

> A camada de enlace de dados recebe pacotes IP da camada de rede e os encapsula para transmissão pelo meio.

---

### Pergunta 3

Qual é o termo para dividir um pacote IP ao encaminhá-lo de uma mídia para outra mídia com uma MTU menor?

- [ ] encapsulamento
- [x] fragmentação
- [ ] segmentação
- [ ] serialização

✅ RESPOSTA CORRETA: fragmentação

> Fragmentação é o processo de divisão de pacotes IP para trafegar em um meio com um MTU menor.

---

### Pergunta 4

Qual método de entrega não garante que o pacote seja entregue totalmente sem erros?

- [ ] sem conexão
- [x] melhor esforço
- [ ] independe de meios físicos

✅ RESPOSTA CORRETA: melhor esforço

> A entrega de melhor esforço não garante que os pacotes serão entregues ao destino.

# 22.2 Pacote IPv4

## 22.2.1 Cabeçalho do Pacote IPv4

O IPv4 é um dos principais protocolos de comunicação de camada de rede. O cabeçalho do pacote IPv4 é usado para garantir que esse pacote seja entregue para sua próxima parada no caminho para seu dispositivo final de destino.

O cabeçalho de um pacote IPv4 consiste em campos com informações importantes sobre o pacote. Esses campos contêm números binários que são examinados pelo processo da Camada 3.


## 22.2.2 Campos do cabeçalho do pacote IPv4

Os valores binários de cada campo identificam várias configurações do pacote IP. Os diagramas de cabeçalho de protocolo, cuja leitura é feita da esquerda para a direita, de cima para baixo, disponibilizam uma visualização para consultar ao discutir os campos de protocolo. O diagrama de cabeçalho de protocolo IP na figura identifica os campos de um pacote IPv4.

### Campos no cabeçalho do pacote IPv4

![[Pasted image 20260617065526.png]]

Campos significativos no cabeçalho IPv4 incluem o seguinte:

- **Versão** – Contém um valor binário de 4 bits definido como 0100 que identifica que este é um pacote IP versão 4.
- **Serviços diferenciados ou DiffServ (DS)** - Anteriormente chamado de Tipo de Serviço (ToS), o campo DS é um campo de 8 bits usado para determinar a prioridade de cada pacote. Os seis bits mais significativos do campo DiffServ são os bits do ponto de código de serviços diferenciados (DSCP) e os dois últimos são os bits de notificação de congestionamento explícita (ECN).
- **Tempo de vida (TTL)** – TTL contém um valor binário de 8 bits que é usado para limitar a vida útil de um pacote. O dispositivo de origem do pacote IPv4 define o valor TTL inicial. É diminuído em um cada vez que o pacote é processado por um roteador. Se o campo TTL for decrementado até zero, o roteador descartará o pacote e enviará uma mensagem ICMP de tempo excedido para o endereço IP de origem. Como o roteador decrementa o TTL de cada pacote, o roteador também deve recalcular a soma de verificação do cabeçalho.
- **Protocolo** - Este campo é usado para identificar o protocolo de próximo nível. O valor binário de 8 bits indica o tipo de carga de dados que o pacote está carregando, o que permite que a camada de rede transfira os dados para o protocolo apropriado das camadas superiores. Valores comuns incluem ICMP (1), TCP (6) e UDP (17).
- **Checksum de cabeçalho** — Isso é usado para detectar corrupção no cabeçalho IPv4.
- **Endereço IP Origem** – Contém um valor binário de 32 bits que representa o endereço IP origem do pacote. O endereço de origem IPv 4 é sempre um endereço unicast.
- **Endereço IP Destino** – Contém um valor binário de 32 bits que representa o endereço IP destino do pacote. O endereço IPv4 destino é um endereço unicast, multicast, ou broadcast.

Os dois campos mais referenciados são os endereços IP de origem e destino. Esses campos identificam a procedência do pacote e para onde ele vai. Normalmente, esses endereços não mudam durante a viagem da origem ao destino.

Os campos Tamanho do Cabeçalho de Internet (IHL), Tamanho Total e Soma de Verificação do Cabeçalho servem para identificar e validar o pacote.

Outros campos são usados para reorganizar um pacote fragmentado. O pacote IPv4 usa especificamente os campos Identificação, Flags e Deslocamento do Fragmento para organizar os fragmentos. Um roteador pode precisar fragmentar um pacote IPv4 ao encaminhá-lo de um meio para outro com uma MTU menor.

Os campos Opções e Preenchimento raramente são usados e estão além do escopo deste módulo.

## 22.2.3 Vídeo - Exemplo de cabeçalhos IPv4 no Wireshark

**Selecione o botão Reproduzir para assistir ao vídeo.**

Eu tenho uma captura de tela do Wireshark e você pode ver que o segundo pacote capturado foi destacado. Na janela de detalhes do pacote, a informação da camada de rede foi expandida para nos mostrar todas as coisas que acontecem na camada de rede.

Vamos ver o que está acontecendo neste pacote específico que estamos examinando. Podemos ver que o protocolo de camada de rede com que estamos lidando era o Protocolo de Internet versão 4 — IPv4. Também podemos ver que o endereço IP de origem era 192.168.1.109 e o endereço IP de destino era 192.168.1.1. Podemos ver que na camada superior este é um pacote de protocolo TCP.

Se limitarmos nossa análise apenas aos campos IPv4, podemos ver os diferentes tipos de informações de controle contidos em todos os pacotes IPv4:

- **Versão:** o número da versão, que é 4, identificando isso como um IPv4, em oposição a um pacote IPv6.
- **Comprimento do cabeçalho:** o tamanho mínimo de um cabeçalho IPv4.
- **Campo de serviços diferenciados:** usado para priorização de pacote, útil para aplicativos como Voice-over IP.
- **Comprimento total:** o comprimento total do pacote.
- **Número de identificação:** usado para fragmentação.
- **Sinalizadores:** o bit DF foi definido, o que significa "não fragmentar". Este pacote não é grande o suficiente ou não é identificado para fragmentação.
- **Deslocamento de fragmento.**
- **TTL (tempo de vida):** definido como 128. Toda vez que um pacote é roteado de um salto para o próximo, o número TTL é reduzido. Quando o número TTL atinge zero, o pacote é descartado, garantindo que os pacotes não circulem na internet para sempre em um loop sem fim. O valor TTL também é usado em rotas de rastreamento ICMP e pings.
- **Campo de protocolo:** nos permite saber o tipo de informação esperado na porção de dados do pacote. O valor seis identifica a parte de dados deste pacote como sendo um pacote TCP.
- **Checksum do cabeçalho:** permite aos roteadores verificar se há algum erro ou inconsistência no cabeçalho IP. Se houver, o pacote será descartado.
- **Endereços IP de origem e destino:** a parte mais importante do pacote IPv4.

Vamos dar uma olhada em mais duas capturas de pacotes do Wireshark para ver algumas semelhanças e diferenças.

A próxima captura nos mostra o oitavo pacote capturado. O endereço IP de origem também é 192.168.1.109 e o endereço IP de destino é 192.168.1.1, exceto que esse pacote é uma solicitação HTTP GET — ou seja, uma solicitação a um servidor da Web localizado em 192.168.1.1. As informações da camada de rede também são protocolo IP versão 4 e temos informações similares nos diferentes campos. Observe no campo comprimento total que este pacote tem 411 bytes, comparado ao pacote anterior que tinha apenas 52 bytes — este pacote tem muito mais informações. Abaixo das informações do IPv4 podemos ver as informações de TCP e, abaixo disso, que existe um protocolo de transferência de hipertexto (HTTP) neste pacote também.

O próximo pacote é o décimo sexto pacote capturado. Também é do host 192.168.1.109 para o host 192.168.1.1, exceto que esse é o protocolo ICMP — especificamente uma solicitação de eco, ou ping. Se procurarmos nas informações do IPv4 na área de detalhes, podemos ver algumas pequenas diferenças: a versão ainda é quatro, o tamanho do cabeçalho ainda é de 20 bytes, mas as flags são um pouco diferentes e o campo de protocolo está agora definido como um, indicando que a porção de dados deste pacote é uma mensagem de protocolo ICMP. Na janela de detalhes na parte inferior há uma área expandida para examinar as informações de cabeçalho específicas para ICMP.