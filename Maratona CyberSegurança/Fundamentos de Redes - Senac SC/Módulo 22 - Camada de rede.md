
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
![[22.1.1.mp4#subtitle=anexos/22.1.1.vtt]]
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
![[22.2.3.mp4#subtitle=anexos/22.2.3.vtt]]
![](https://www.youtube.com/watch?v=_6-u61V0GGE)

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


## 22.2.4 Verifique sua compreensão - Pacote IPv4

**Verifique sua compreensão do pacote IPv4 escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Quais são os dois campos mais comumente referenciados em um cabeçalho de pacote IPv4 que indicam de onde o pacote está vindo e para onde ele está indo? (Escolha duas.)

- [x] endereço IP de destino
- [ ] protocol
- [ ] Tempo de Vida
- [x] Endereço IP origem
- [ ] Serviços diferenciados (DS)

✅ RESPOSTA CORRETA: endereço IP de destino / Endereço IP origem

> Os campos de cabeçalho IP que identificam a origem do pacote e para onde ele está indo são Endereço IP de Origem e Endereço IP de Destino.

---

### Pergunta 2

Qual instrução está correta sobre campos de cabeçalho de pacote IPv4?

- [x] Os endereços IPv4 de origem e destino permanecem os mesmos durante a viagem da origem para o destino.
- [ ] O campo Time to Live é usado para determinar a prioridade de cada pacote.
- [ ] Os campos Comprimento total e soma de verificação de cabeçalho são usados para reordenar um pacote fragmentado.
- [ ] O campo Versão identifica o protocolo de nível seguinte.

✅ RESPOSTA CORRETA: Os endereços IPv4 de origem e destino permanecem os mesmos durante a viagem da origem para o destino.

> Os endereços IP de origem e de destino no pacote IP não são alterados na rota da origem para o destino.

---

### Pergunta 3

Qual campo é usado para detectar corrupção no cabeçalho IPv4?

- [x] Soma de verificação do cabeçalho
- [ ] Tempo de Vida
- [ ] Protocolo
- [ ] Serviços diferenciados (DS)

✅ RESPOSTA CORRETA: Soma de verificação do cabeçalho

> O campo Checksum de cabeçalho em um cabeçalho IPv4 é usado para detectar pacotes corrompidos.

---
### Pergunta 4

Qual campo inclui valores comuns como ICMP (1), TCP (6) e UDP (17)?

- [ ] Soma de verificação do cabeçalho
- [ ] Tempo de Vida
- [x] Protocolo
- [ ] Serviços diferenciados (DS)

✅ RESPOSTA CORRETA: Protocolo

> O campo protocolo identifica o protocolo da camada superior que é transportado dentro do pacote IP. Protocolos comuns são TCP, UDP e ICMP.


# 22.3 Pacote IPv6

## 22.3.1 Limitações do IPv4

O IPv4 ainda está em uso hoje. Este tópico é sobre IPv6, que eventualmente substituirá o IPv4. Para entender melhor por que você precisa conhecer o protocolo IPv6, ele ajuda a conhecer as limitações do IPv4 e as vantagens do IPv6.

Ao longo dos anos, protocolos e processos adicionais foram desenvolvidos para enfrentar novos desafios. No entanto, mesmo com alterações, ele ainda enfrenta três grandes problemas:

- **Esgotamento do endereço IPv4 -** O IPv4 tem um número limitado de endereços públicos exclusivos disponíveis. Embora haja aproximadamente 4 bilhões de endereços IPv4, o número crescente de novos dispositivos habilitados para IP, conexões sempre ativas e o potencial de crescimento de regiões menos desenvolvidas têm aumentado a necessidade de mais endereços.
- **Falta de conectividade ponto a ponto** - Network Address Translation (NAT) é uma tecnologia comumente implementada em redes IPv4. A NAT é uma forma de vários dispositivos compartilharem um único endereço IPv4 público. No entanto, como o endereço IPv4 público é compartilhado, o endereço IPv4 de um host de rede interna fica oculto. Isso pode ser problemático para tecnologias que exigem conectividade de ponta a ponta.
- **Maior complexidade da rede** - Embora o NAT tenha ampliado a vida útil do IPv4, ele só se destinava a ser um mecanismo de transição para o IPv6. O NAT em suas várias implementações cria complexidade adicional na rede, criando latência e dificultando a solução de problemas.

## 22.3.2 Visão geral do IPv6

No início da década de 90, a Internet Engineering Task Force (IETF) tinha uma preocupação crescente a respeito dos problemas com o IPv4 e começou a procurar um substituto. Isso levou ao desenvolvimento do IP versão 6 (IPv6). O IPv6 supera as limitações do IPv4 e possui recursos que atendem às demandas atuais e previsíveis de rede.

As melhorias que o IPv6 fornece incluem o seguinte:

- **Espaço de endereço aumentado** - Os endereços IPv6 são baseados no endereçamento hierárquico de 128 bits, em oposição ao IPv4 com 32 bits.
- **Manipulação aprimorada de pacotes** - O cabeçalho IPv6 foi simplificado com menos campos.
- **Elimina a necessidade de NAT** - Com um número tão grande de endereços IPv6 públicos, o NAT entre um endereço IPv4 privado e um IPv4 público não é necessário. Isso evita alguns dos problemas induzidos por NAT enfrentados por aplicativos que exigem conectividade de ponta a ponta.

O espaço de 32 bits de um endereço IPv4 fornece aproximadamente 4,294,967,296 endereços exclusivos. O espaço de endereço IPv6 fornece 340,282,366,920,938,463,463,374,607,431,768,211,456, ou 340 undecilhões de endereços. Isto é aproximadamente equivalente a cada grão de areia na Terra.

A figura mostra uma comparação visual do espaço de endereços IPv4 e IPv6.

### Comparação de espaço de endereços IPv4 e IPv6


<table border="1" cellpadding="6" cellspacing="0" style="width:100%; table-layout:fixed; word-wrap:break-word;"> <tr> <th>Nome do Número</th> <th>Notação Científica</th> <th>Número de Zeros</th> </tr> <tr> <td>1 mil</td> <td>10^3</td> <td>1.000</td> </tr> <tr> <td>1 milhão</td> <td>10^6</td> <td>1.000.000</td> </tr> <tr style="background-color:#f4a460;"> <td>1 bilhão</td> <td>10^9</td> <td>1.000.000.000</td> </tr> <tr> <td>1 trilhão</td> <td>10^12</td> <td>1.000.000.000.000</td> </tr> <tr> <td>1 quadrilhão</td> <td>10^15</td> <td>1.000.000.000.000.000</td> </tr> <tr> <td>1 quintilhão</td> <td>10^18</td> <td>1.000.000.000.000.000.000</td> </tr> <tr> <td>1 sextilhão</td> <td>10^21</td> <td>1.000.000.000.000.000.000.000</td> </tr> <tr> <td>1 septilhão</td> <td>10^24</td> <td>1.000.000.000.000.000.000.000.000</td> </tr> <tr> <td>1 octilhão</td> <td>10^27</td> <td>1.000.000.000.000.000.000.000.000.000</td> </tr> <tr> <td>1 nonilhão</td> <td>10^30</td> <td>1.000.000.000.000.000.000.000.000.000.000</td> </tr> <tr> <td>1 decilhão</td> <td>10^33</td> <td>1.000.000.000.000.000.000.000.000.000.000.000</td> </tr> <tr style="background-color:#bfff00;"> <td>1 undecilhão</td> <td>10^36</td> <td>1.000.000.000.000.000.000.000.000.000.000.000.000</td> </tr> </table>

**Legenda:**

- 🟠 Há 4 bilhões de endereços IPv4
- 🟡 Há 340 undecilhões de endereços IPv6


## 22.3.3 Campos do cabeçalho do pacote IPv4 no cabeçalho do pacote IPv6

Uma das principais melhorias de design do IPv6 em relação ao IPv4 é o cabeçalho IPv6 simplificado.

Por exemplo, o cabeçalho IPv4 consiste em um cabeçalho de comprimento variável de 20 octetos (até 60 bytes se o campo Opções for usado) e 12 campos de cabeçalho básicos, sem incluir o campo Opções e o campo Preenchimento.

Para o IPv6, alguns campos permaneceram os mesmos, alguns campos mudaram de nome e posição e alguns campos do IPv4 não são mais necessários, conforme destacado na figura.

### Cabeçalho do Pacote IPv4

![[Pasted image 20260618194350.png]]Por outro lado, o cabeçalho simplificado do IPv6 mostrado na figura a seguir consiste em um cabeçalho de comprimento fixo de 40 octetos (em grande parte devido ao comprimento dos endereços IPv6 de origem e de destino).

O cabeçalho simplificado IPv6 permite um processamento mais eficiente de cabeçalhos IPv6.

### Cabeçalho do Pacote IPv6

![[Pasted image 20260618194428.png]]


## 22.3.4 Cabeçalho do Pacote IPv6

O diagrama de cabeçalho de protocolo IP na figura identifica os campos de um pacote IPv6.

### Campos no cabeçalho do pacote IPv6

![[Pasted image 20260618194450.png]]

Os campos no cabeçalho do pacote IPv6 incluem o seguinte:

- **Versão -** Este campo contém um valor binário de 4 bits definido como 0110 que identifica isso como um pacote IP versão 6.
- **Classe de tráfego -** Este campo de 8 bits é equivalente ao campo DS (Serviços diferenciados de IPv4).
- **Etiqueta de fluxo -** Este campo de 20 bits sugere que todos os pacotes com a mesma etiqueta de fluxo recebam o mesmo tipo de manipulação pelos roteadores.
- **Comprimento da carga útil -** Este campo de 16 bits indica o comprimento da parte dos dados ou da carga útil do pacote IPv6. Isso não inclui o comprimento do cabeçalho IPv6, que é um cabeçalho fixo de 40 bytes.
- **Próximo cabeçalho -** Este campo de 8 bits é equivalente ao campo Protocolo IPv4. Ele exibe o tipo de carga de dados que o pacote está carregando, permitindo que a camada de rede transfira os dados para o protocolo apropriado das camadas superiores.
- **Limite de salto** - Este campo de 8 bits substitui o campo TTL IPv4. Esse valor é subtraído de um por cada roteador que encaminha o pacote. Quando o contador atinge 0, o pacote é descartado e uma mensagem de ICMPv6 com tempo excedido é encaminhada para o host de envio. Isso indica que o pacote não atingiu seu destino porque o limite de salto foi excedido. Ao contrário do IPv4, o IPv6 não inclui uma soma de verificação do cabeçalho IPv6, porque esta função é executada nas camadas inferior e superior. Isso significa que a soma de verificação não precisa ser recalculada por cada roteador quando diminui o campo Limite de Hop, o que também melhora o desempenho da rede.
- **Endereço IPv6 de origem -** Este campo de 128 bits identifica o endereço IPv6 do host de envio.
- **Endereço IPv6 de destino -** Este campo de 128 bits identifica o endereço IPv6 do host de recebimento.

Um pacote IPv6 pode conter também cabeçalhos de extensão (EH), que fornecem informações de camada de rede. Opcionais, os cabeçalhos de extensão ficam posicionados entre o cabeçalho IPv6 e a carga. Eles são usados para fragmentação, segurança, suporte à mobilidade e muito mais.

Ao contrário de IPv4, os roteadores não fragmentam os pacotes IPv6 roteados.

## 22.3.5 Vídeo - Exemplo de cabeçalhos IPv6 no Wireshark

**Selecione o botão Reproduzir para assistir ao vídeo.**
![[22.3.5.mp4#subtitle=anexos/22.3.5.vtt]]
Nesta imagem, podemos ver que o pacote destacado é o pacote número 46 e que o endereço de origem, na área da janela de lista de pacotes, é um endereço IPv6 unicast global. Você pode ver isso começando com o `2001:6f8`. O endereço de destino também é um endereço unicast global `2001:6f8:900e` e assim por diante.

Se observarmos o campo de protocolo, vemos que nas camadas superiores este é um pacote TCP e essa é uma tentativa de estabelecer uma comunicação inicial com um servidor web HTTP.

Se olharmos para baixo na área de informações da camada de rede, você pode ver que as informações IPv6 foram expandidas. Vejamos algumas das informações do campo de protocolo da versão 6 de protocolo da Internet.

Primeiro de tudo, você pode ver que a quantidade de informações é muito menor do que no cabeçalho IPv4.

Aqui estão alguns recursos interessantes:

- **Versão:** o campo versão é o mesmo. Neste caso, diz seis, identificando esse pacote como IPv6. Também podemos ver o binário 6 aqui.
- **Classe de tráfego:** tem a mesma função que o campo de serviços diferenciados em um pacote IPv4. Ele manipula a priorização e o congestionamento de tráfego.
- **Flow Label (Rótulo de fluxo):** é um novo campo para o protocolo IPv6. Seu objetivo é manter os mesmos fluxos de pacote por roteadores e switches, para ajudar as aplicações em tempo real que precisam que os pacotes cheguem na mesma ordem.
- **Tamanho da carga:** é igual ao campo de tamanho total no cabeçalho IPv4. Esse campo informa o tamanho total — nesse caso, 40 bytes.
- **Próximo campo de cabeçalho:** tem o mesmo objetivo que o campo de protocolo para IPv4. Você pode ver que ele está identificando que a parte superior de dados deste pacote é um seis, ou TCP.
- **Limite de saltos:** tem a mesma função que o campo TTL em um pacote IPv4. Você pode ver que o limite de saltos, no momento, está definido em 64 saltos. Uma vez que este decremente para zero, o pacote será descartado.

Em seguida, temos o endereço IPv6 de origem, o endereço IPv6 de destino e, depois, na camada superior, podemos ver que esse é um pacote TCP com informações de cabeçalho TCP.

---

Na próxima imagem, o pacote número 49 está destacado. Agora temos uma conexão com esse servidor da Web. Esse pacote é uma solicitação GET para o servidor da Web. Se olharmos para baixo na janela de detalhes do pacote do protocolo Internet versão 6 expandida, podemos ver que o tamanho da carga é muito maior. Podemos ver abaixo as informações de IPv6, as informações TCP, e que agora há informações do protocolo HTTP também dentro da nossa solicitação GET.

---

A última imagem nos mostra uma mensagem de solicitação de vizinho ICMP versão 6. Se observarmos a janela no pacote destacado, no pacote número 1, veremos que o endereço de origem desta vez não é um endereço IPv6 unicast global, mas sim um endereço de link local. Podemos dizer isso pelo `fe80` aqui. Também podemos ver que esse endereço de link local usou EUI-64 para resolver a parte de identificação da interface do endereço. Podemos dizer isso pelo `ff:fe` no endereço.

O endereço de destino é um endereço IPv6 `ff02`, indicando que esse é um pacote multicast. Se observarmos o protocolo, veremos que é ICMP versão 6, e as informações sobre o pacote nos dizem que é uma mensagem de solicitação de vizinho para o mesmo dispositivo que estávamos contatando nas imagens anteriores.

A função deste pacote é essencialmente similar a uma solicitação ARP no IPv4. Precisamos descobrir o endereço de link local do dispositivo, por isso enviamos uma mensagem ICMP versão 6 multicast e esperamos obter de volta um endereço de link local deste vizinho.

Se olharmos para baixo na janela de detalhes expandida, veremos:

- **Versão:** 6
- **Classe de tráfego**
- **Rótulo de fluxo:** tamanho completo do pacote
- **Próximo campo de cabeçalho:** indicando em 58 que este é uma mensagem ICMP versão 6 na parte de dados do pacote
- **Limite de saltos:** 255 saltos (semelhante ao campo TTL)
- **Endereço de origem:** link local
- **Endereço de destino:** IPv6 multicast

Na parte inferior, abaixo das informações de IPv6, podemos ver que há uma área que pode ser expandida, específica do Internet Control Message Protocol versão 6.

## 22.3.6 Verifique sua compreensão - Pacote IPv6

**Verifique sua compreensão do pacote IPv6 escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Quais três opções são os principais problemas associados ao IPv4? (Escolha três.)

- [x] Redução do número de endereços IP disponíveis
- [x] maior complexidade da rede e expansão da tabela de roteamento da Internet
- [ ] sempre em conexões
- [x] falta de conectividade de ponta a ponta
- [ ] fronteiras globais e políticas
- [ ] muitos endereços IPv4 disponíveis

✅ RESPOSTA CORRETA: Redução do número de endereços IP disponíveis, maior complexidade da rede e expansão da tabela de roteamento da Internet, falta de conectividade de ponta a ponta

> O IPv4 foi padronizado na década de 1980 e tem várias limitações tecnológicas, como a falta de conectividade de ponta a ponta e um espaço de endereços esgotado.

---

### Pergunta 2

Quais duas opções são as melhorias fornecidas pelo IPv6 em comparação com o IPv4? (Escolha duas.)

- [ ] suporta campos adicionais para pacotes complexos
- [x] aumentou o espaço de endereço IP
- [ ] padroniza o uso de NAT
- [ ] suporta redes baseadas em classe
- [x] usa um cabeçalho mais simples para fornecer melhor manipulação de pacotes

✅ RESPOSTA CORRETA: aumentou o espaço de endereço IP, usa um cabeçalho mais simples para fornecer melhor manipulação de pacotes

> Existem várias melhorias técnicas feitas no IPv6, duas das quais são um pool de endereços IP muito maior e um cabeçalho de protocolo simplificado.

---

### Pergunta 3

Qual é o verdadeiro do cabeçalho IPv6? (Escolha duas.)

- [ ] consiste em 20 octetos.
- [x] consiste em 40 octetos.
- [x] contém 8 campos de cabeçalho.
- [ ] contém 12 campos de cabeçalho.

✅ RESPOSTA CORRETA: consiste em 40 octetos, contém 8 campos de cabeçalho

> O cabeçalho IPv6 é um comprimento fixo de 40 octetos e contém 8 campos de cabeçalho.

---

### Pergunta 4

Qual é o verdadeiro do cabeçalho do pacote IPv6?

- [x] O campo Limite de salto substitui o campo Tempo de vida do IPv4.
- [ ] Os endereços IPv6 de origem e destino mudam durante a viagem da origem para o destino.
- [ ] O campo Tempo de vida substitui o campo DiffServ.
- [ ] O campo Versão identifica o próximo cabeçalho.

✅ RESPOSTA CORRETA: O campo Limite de salto substitui o campo Tempo de vida do IPv4.

> Vários campos no cabeçalho IPv6 substituíram campos no cabeçalho IPv4. Por exemplo, o campo Limite de salto substituiu o campo Time to Live do cabeçalho IPv4.


# 22.4 Resumo da camada de rede

## 22.4.1 O que aprendi neste módulo?

### Características de camada de rede

A camada de rede, ou Camada OSI 3, fornece serviços para permitir que dispositivos finais troquem dados entre redes. IPv4 e IPv6 são os principais protocolos de comunicação da camada de rede. Outros protocolos de camada de rede incluem protocolos de roteamento como OSPF e protocolos de mensagens como ICMP.

Os protocolos da camada de rede realizam quatro operações: endereçamento de dispositivos finais, encapsulamento, roteamento e desencapsulamento. IPv4 e IPv6 especificam a estrutura de pacotes e o processamento usado para transportar os dados de um host para outro host. A operação sem levar em consideração os dados contidos em cada pacote permite que a camada de rede transporte pacotes para diversos tipos de comunicações entre vários hosts.

O IP encapsula o segmento da camada de transporte ou outros dados adicionando um cabeçalho IP. O cabeçalho IP é usado para entregar o pacote ao host de destino. O cabeçalho IP é examinado por roteadores e switches de camada 3 à medida que percorre uma rede até seu destino. As informações de endereçamento IP permanecem as mesmas desde o momento em que o pacote deixa o host de origem até chegar ao host de destino, exceto quando traduzido pelo dispositivo executando NAT para IPv4.

As características básicas do IP são: sem conexão, melhor esforço e independente de mídia. O IP não tem conexão, o que significa que nenhuma conexão ponta a ponta é criada pelo IP antes dos dados enviados. O IP também não requer campos adicionais no cabeçalho para manter uma conexão estabelecida. Esse processo reduz bastante a sobrecarga do IP. Os remetentes não sabem se os dispositivos de destino estão presentes e funcionais ao enviar pacotes, nem sabem se o destino recebe o pacote ou se o dispositivo de destino pode acessar e ler o pacote. O IP opera independentemente da mídia que transporta os dados nas camadas inferiores da pilha de protocolos. Os pacotes IP podem ser comunicados como sinais eletrônicos por cabo de cobre, como sinais ópticos por fibra ou sem fio como sinais de rádio. Uma característica do meio que a camada de rede considera é o tamanho máximo da PDU que cada meio pode transportar, ou MTU.

---

### Pacote IPv4

O cabeçalho do pacote IPv4 é usado para garantir que um pacote seja entregue em sua próxima parada no caminho para o dispositivo final de destino. Um cabeçalho de pacote IPv4 consiste em campos contendo números binários que são examinados pelo processo da camada 3. Campos significativos no cabeçalho IPv4 incluem: versão, DS, TTL, protocolo, soma de verificação do cabeçalho, endereço IPv4 de origem e endereço IPv4 de destino.

Os campos Tamanho do Cabeçalho de Internet (IHL), Tamanho Total e Soma de Verificação do Cabeçalho servem para identificar e validar o pacote. O pacote IPv4 usa os campos Identificação, Sinalizadores e Deslocamento de Fragmento para acompanhar os fragmentos. Um roteador pode precisar fragmentar um pacote IPv4 ao encaminhá-lo de um meio para outro com uma MTU menor.

---

### Pacote IPv6

O IPv4 tem limitações, incluindo: esgotamento do endereço IPv4, falta de conectividade de ponta a ponta e maior complexidade da rede. O IPv6 supera as limitações do IPv4. As melhorias que o IPv6 oferece incluem o seguinte: maior espaço de endereçamento, melhor manipulação de pacotes e eliminação da necessidade de NAT.

O espaço de 32 bits de um endereço IPv4 fornece aproximadamente 4.294.967.296 endereços exclusivos. O espaço de endereço IPv6 fornece 340.282.366.920.938.463.463.374.607.431.768.211.456, ou 340 undecilhões de endereços. Isto é aproximadamente equivalente a cada grão de areia na Terra.

Os campos de cabeçalho simplificados do IPv6 incluem: versão, classe de tráfego, rótulo de fluxo, comprimento da carga, próximo cabeçalho, limite de salto, endereço IP de origem e endereço IP de destino. Um pacote IPv6 pode conter também cabeçalhos de extensão (EH), que fornece informações opcionais da camada de rede. Opcionais, os cabeçalhos de extensão ficam posicionados entre o cabeçalho IPv6 e a carga. Eles são usados para fragmentação, segurança, suporte à mobilidade e muito mais. Ao contrário de IPv4, os roteadores não fragmentam os pacotes IPv6 roteados.

## 22.4.2 Webster - Questões para Reflexão

Mais protocolos! Estou começando a entender que houve muito trabalho para criar esses protocolos. Na camada de rede, os protocolos tratam do endereçamento, encapsulando os dados, roteando os pacotes e, em seguida, desencapsulando os pacotes para que possam ser lidos. Marcy e Vincent não são profissionais de TI, então uma rede em funcionamento pode parecer um pouco misteriosa para eles. Mas ajuda saber o que acontece na camada de rede do modelo OSI. Como esse conhecimento pode ajudá-lo a solucionar problemas da sua própria rede?

## 22.4.3 Teste de Camada de Rede

## Pergunta 1

**Qual valor, que está contido em um campo de cabeçalho IPv4, é diminuído por cada roteador que recebe um pacote?**

- [ ] Deslocamento do fragmento
- [ ] Tamanho do cabeçalho
- [x] Vida útil (TTL)
- [ ] Serviços Diferenciados

**Resposta: Vida útil (TTL)**

---

## Pergunta 2

**Qual declaração descreve com precisão uma característica do IPv4?**

- [ ] IPv4 suporta nativamente IPsec.
- [x] O IPv4 tem um espaço de endereço de 32 bits.
- [ ] Um cabeçalho IPv4 tem menos campos do que um cabeçalho IPv6 tem.
- [ ] Todos os endereços IPv4 podem ser atribuídos a hosts.

**Resposta: O IPv4 tem um espaço de endereço de 32 bits.**

---

## Pergunta 3

**Qual tecnologia oferece uma solução para o esgotamento de endereços IPv4, permitindo que vários dispositivos compartilhem um endereço IP público?**

- [ ] HTTP
- [ ] DHCP
- [ ] ARP
- [x] NAT
- [ ] SMB
- [ ] DNS

**Resposta: NAT**

---

## Pergunta 4

**Por que o IPv6 foi projetado para substituir o IPv4?**

- [ ] Para permitir que os computadores endereçem mais memória
- [x] Porque em breve o espaço de endereço IPv4 estará esgotado
- [ ] Para resolver problemas de compatibilidade com dispositivos móveis
- [ ] Porque a maioria dos computadores tem um processador de 64 bits

**Resposta: Porque em breve o espaço de endereço IPv4 estará esgotado**

---

## Pergunta 5

**Qual característica da camada de rede no modelo OSI permite a transferência de pacotes para vários tipos de comunicação entre diversos hosts?**

- [x] A capacidade de operar sem considerar os dados transportados em cada pacote
- [ ] O desencapsulamento dos cabeçalhos das camadas inferiores
- [ ] A capacidade de gerenciar o transporte de dados entre os processos em execução nos hosts
- [ ] A seleção de caminhos para o destino e o direcionamento de pacotes até o destino

**Resposta: A capacidade de operar sem considerar os dados transportados em cada pacote**

---

## Pergunta 6

**Qual afirmação descreve uma característica da camada de rede no modelo OSI?**

- [ ] No processo de encapsulamento, ele adiciona números de porta de origem e destino ao cabeçalho IP.
- [ ] Quando um pacote chega ao host de destino, seu cabeçalho IP é verificado pela camada de rede para determinar para onde o pacote deve ser roteado.
- [ ] Ela gerencia o transporte de dados entre os processos em execução em cada host.
- [x] Seus protocolos especificam a estrutura do pacote e o processamento usado para transportar os dados de um host para outro.

**Resposta: Seus protocolos especificam a estrutura do pacote e o processamento usado para transportar os dados de um host para outro.**

---

## Pergunta 7

**Qual camada do modelo OSI é responsável pelo endereçamento lógico dos pacotes?**

- [ ] Transporte
- [x] Rede
- [ ] Enlace de dados
- [ ] Sessão

**Resposta: Rede**

---

## Pergunta 8

**Qual é a ordem de encapsulamento para as unidades de dados de protocolo que passam da aplicação do usuário para baixo na pilha?**

- [ ] Bits, segmentos, pacotes, quadros, dados
- [x] Dados, segmentos, pacotes, quadros, bits
- [ ] Segmentos, pacotes, quadros, bits, dados
- [ ] Segmentos, dados, pacotes, quadros, bits

**Resposta: Dados, segmentos, pacotes, quadros, bits**

---

## Pergunta 9

**Qual processo envolve colocar uma PDU dentro de outra PDU?**

- [ ] Codificação
- [ ] Segmentação
- [ ] Controle de fluxo
- [x] Encapsulamento

**Resposta: Encapsulamento**

---

## Pergunta 10

**Quais informações são adicionadas à camada 3 do modelo OSI durante o encapsulamento?**

- [ ] Número da porta de origem e destino
- [ ] Protocolo de aplicação origem e destino
- [ ] Endereços MAC origem e destino
- [x] Endereço IP origem e destino

**Resposta: Endereço IP origem e destino**

---

## Pergunta 11

**Como a camada de rede usa o valor de MTU?**

- [ ] A camada de rede depende da camada de link de dados para definir o MTU e ajustará a velocidade da transmissão para acomodá-lo.
- [x] O MTU é transmitido para a camada de rede pela camada de link de dados.
- [ ] Para aumentar a velocidade de entrega, a camada de rede ignora o MTU.
- [ ] A camada de rede depende das camadas de nível superior para determinar o MTU.

**Resposta: O MTU é transmitido para a camada de rede pela camada de link de dados.**

