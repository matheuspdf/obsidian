# 31.0. Introdução

## 31.0.1 Webster - Por que devo fazer este módulo?

Webster, ao seu dispor!

Como a Halimah vai se familiarizar com a rede na sede?

Ela examinará algumas topologias criadas pelo departamento de TI. Isso a ajudará a entender como os vários dispositivos intermediários e finais estão conectados e que mídia é usada para conectá-los. As topologias lógicas a ajudarão a entender o tipo de enquadramento de rede e controle de acesso à mídia que está sendo usado. As topologias físicas servem como uma espécie de mapa que informa a Halimah quais dispositivos são encontrados em quais salas de cada edifício no campus.

Aprender a ler topologias é uma parte muito importante para se tornar um profissional de TI.

Vamos indo!

## 31.0.2 O que vou aprender neste módulo?

**Título do Módulo:** Camada de Enlace de Dados

**Objetivo do Módulo:** Explica como o controle de acesso ao meio na camada de enlace de dados oferece suporte à comunicação entre redes físicas e lógicas.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Topologias|Compare as características das topologias físicas e lógicas.|
|Métodos de Controle de Acesso ao Meio Físico|Explique como os dispositivos acessam uma LAN para enviar quadros.|

# 31.1 Topologias

## 31.1.1 Topologias Físicas e Lógicas

Como você aprendeu no tópico anterior, a camada de enlace de dados prepara os dados da rede para a rede física. Ela deve conhecer a topologia lógica de uma rede para poder determinar o que é necessário para transferir quadros de um dispositivo para outro. Este tópico explica as maneiras pelas quais a camada de enlace de dados funciona com diferentes topologias de rede lógica.

A topologia de uma rede é a organização, ou o relacionamento, dos dispositivos de rede e as interconexões entre eles.

Existem dois tipos de topologias usadas ao descrever redes LAN e WAN:

- **Topologia física** - Identifica as conexões físicas e como os dispositivos finais e intermediários (ou seja, roteadores, switches e pontos de acesso sem fio) são interconectados. A topologia também pode incluir a localização específica do dispositivo, como o número do quarto e a localização no rack do equipamento. As topologias físicas são geralmente ponto a ponto ou estrela.
- **Topologia lógica** - Refere-se ao modo como uma rede transfere quadros de um nó para o seguinte. Esta topologia identifica conexões virtuais usando interfaces de dispositivo e esquemas de endereçamento IP da Camada 3.

A camada de enlace de dados “vê” a topologia lógica da rede quando controla o acesso de dados ao meio físico. É a topologia lógica que influencia o tipo de enquadramento de rede e o controle de acesso ao meio usado.

A figura exibe um exemplo de **topologia física** para uma rede pequena.

### Topologia **Física**

![[Pasted image 20260628233322.png]]

A próxima figura exibe um exemplo de **topologia lógica** para a mesma rede.

### Topologia Lógica

![[Pasted image 20260628233340.png]]


## 31.1.2 Vídeo - A Topologia Lógica

**Selecione o botão Reproduzir para assistir o vídeo.**

![[31.1.2.mp4#subtitle=anexos/31.1.2vtt]]

Existem vários tipos de diagramas de rede. Um dos diagramas mais comuns e um dos mais úteis é o diagrama de topologia lógica, que estamos mostrando aqui.

A maioria dos diagramas de rede incluirá muitos dos mesmos dispositivos e algumas das mesmas informações. Um diagrama de topologia lógica se concentra no fluxo de informações, inclusive endereçamento. A topologia aqui está mostrando apenas um exemplo de algumas das informações relevantes que você pode ver neste tipo de diagrama. Estão incluídos neste diagrama os dispositivos de rede tais como switches, roteadores, firewalls. Normalmente, os dispositivos do cliente não estão incluídos. Em vez disso, eles estão representados usando um único switch Ethernet.

Esses diagramas variam em detalhes, mas a intenção é a mesma. Eles são usados para oferecer aos engenheiros e administradores de rede uma melhor compreensão do layout da rede, como os dispositivos se comunicam entre si, e para ilustrar o fluxo de informações através da rede. Isto ajuda a monitorar o tráfego de rede para performance e segurança, dimensionar e aprimorar a rede com dispositivos e recursos adicionais, e, o mais importante, ajudam a solucionar problemas mais rapidamente.

As informações de endereçamento de rede geralmente são incluídas, mostrando várias sub-redes juntamente com os endereços dos principais servidores e outros dispositivos. Algumas das informações de endereçamento também pode estar em outra documentação de rede, como um plano de endereço IP, inclusive endereços de interface específicos de roteadores e firewalls. O plano de endereço também pode incluir políticas relacionados à atribuição dinâmica de endereços IP, endereços de gateway padrão e conversão de endereço de rede. Novamente, tudo isso vai variar dependendo das políticas do departamento de TI e da empresa.

Além do plano de endereçamento IP, outros documentos podem ser incluídos, como políticas de segurança e firewall, inventário de dispositivos de redes, quaisquer estatísticas e análises de rede, informações de backup e recuperação e muito mais.

## 31.1.3 Topologias WAN

As figuras ilustram como as WANs são comumente interligadas usando três topologias WAN físicas comuns.

**Clique em cada botão abaixo para obter mais informações.**

### **Ponto a Ponto**

Esta é a topologia WAN mais simples e comum. Consiste em uma ligação permanente entre dois pontos finais.![[Pasted image 20260628233523.png]]

### **Hub and spoke**

Esta é uma versão WAN da topologia em estrela na qual um site central interconecta sites de filial através do uso de links ponto a ponto. Os sites de filiais não podem trocar dados com outros sites de filiais sem passar pelo site central.
![[Pasted image 20260628233535.png]]


### **Malha**

Essa topologia fornece alta disponibilidade, mas requer que todos os sistemas finais estejam interconectados a todos os outros sistemas. Portanto, os custos administrativos e físicos podem ser significativos. Cada link é essencialmente um link ponto a ponto para outro nó.
![[Pasted image 20260628233548.png]]

Um híbrido é uma variação ou combinação de qualquer topologia. Por exemplo, uma malha parcial é uma topologia híbrida em que alguns dispositivos finais, mas não todos, são interconectados.

## 31.1.4 Topologia de WAN ponto a ponto

As topologias ponto a ponto físicas conectam diretamente dois nós, como mostrado na figura. Nessa organização, dois nós não têm de compartilhar o meio físico com outros hosts. Além disso, ao usar um protocolo de comunicação serial como o protocolo ponto a ponto (PPP), um nó não precisa determinar se um quadro de entrada é destinado a ele ou a outro nó. Portanto, os protocolos de enlace de dados podem ser muito simples, assim como todos os quadros no meio físico podem trafegar apenas para os dois nós ou a partir deles. O nó coloca os quadros na mídia em uma extremidade e esses quadros são retirados da mídia pelo nó na outra extremidade do circuito ponto a ponto.

![[Pasted image 20260629090117.png]]

**Nota:** Uma conexão ponto a ponto via Ethernet requer que o dispositivo determine se o quadro de entrada está destinado a esse nó.

Um nó de origem e destino pode ser indiretamente conectado entre si por alguma distância geográfica, usando vários dispositivos intermediários. No entanto, o uso de dispositivos físicos na rede não afeta a topologia lógica, conforme ilustrado na figura. Na figura, adicionar conexões físicas intermediárias pode não alterar a topologia lógica. A conexão lógica ponto a ponto é a mesma. A imagem mostra um exemplo de rede ponto a ponto que consiste em dois roteadores, rotulados Nó de Origem e Nó de Destino, cada um conectado a uma nuvem de rede através de links WAN. Os dois roteadores são mostrados enviando quadros para a nuvem de rede.

![[Pasted image 20260629090150.png]]


## 31.1.5 Topologias LAN

Em LANs multiacesso, os dispositivos finais (isto é, nós) são interligados usando topologias estrela ou estrela estendida, como mostrado na figura. Neste tipo de topologia, os dispositivos finais são conectados a um dispositivo intermediário central, neste caso, um switch Ethernet. A topologia **estrela estendida** interconecta vários switches Ethernet. As topologias em estrela e estendidas são fáceis de instalar, muito escalonáveis (fáceis de adicionar e remover dispositivos finais) e fáceis de solucionar problemas. As primeiras topologias em estrela interconectavam dispositivos finais usando hubs Ethernet.

Às vezes, pode haver apenas dois dispositivos conectados na LAN Ethernet. Um exemplo são dois roteadores interconectados. Este seria um exemplo de Ethernet usado em uma topologia ponto a ponto.

**Topologias LAN legadas**

As primeiras tecnologias Ethernet e Token Ring LAN legadas incluíam dois outros tipos de topologias:

- **Barramento** - todos os sistemas finais são encadeados entre si e terminados de alguma forma em cada extremidade. Os dispositivos de infraestrutura, como switches, não são necessários para interconectar os dispositivos finais. As redes Ethernet herdadas costumavam ser topologias de barramento usando cabos coaxiais, porque era barato e fácil de configurar.
- **Anel** - os sistemas finais são conectados ao seu respectivo vizinho formando um anel. O anel não precisa ser terminado, ao contrário da topologia de barramento. As redes de interface de dados distribuídos de fibra herdada (FDDI) e Token Ring usavam topologias em anel.

As figuras ilustram como os dispositivos finais são interconectados nas LANs. Nos desenhos de rede, é comum ter uma linha reta representando uma LAN Ethernet, inclusive estrela simples e estrela estendida.

### Topologias Físicas

![[Pasted image 20260629090207.png]]



## 31.1.6 Verifique sua compreensão - Topologias

### Pergunta 1

Qual topologia exibe endereços IP da camada de dispositivo de rede?

- [ ] Topologia física
- [ ] Topologia de endereço IP
- [x] Topologia lógica

✅ RESPOSTA CORRETA: Topologia lógica

> A topologia lógica mostra os endereços IP atribuídos às interfaces de dispositivo.

---

### Pergunta 2

Que tipo de redes físicas são comumente usadas em WANs? (Escolha três.)

- [ ] estrela estendida (extended star)
- [x] hub and spoke
- [x] malha
- [x] ponto a ponto
- [ ] anel
- [ ] barramento (bus)

✅ RESPOSTA CORRETA: hub and spoke / malha / ponto a ponto

> As redes de longa distância (WANs) geralmente incluem topologias físicas ponto a ponto, hub-and-spoke e malha.

---

### Pergunta 3

Qual topologia LAN é uma topologia híbrida?

- [x] Estrela estendida (extended star)
- [ ] Anel
- [ ] Estrela
- [ ] Barramento (bus)

✅ RESPOSTA CORRETA: Estrela estendida (extended star)

> A topologia estrela estendida é considerada uma topologia híbrida porque combina várias topologias em estrelas.

---

### Pergunta 4

Qual topologia de LAN tem todos os sistemas finais interligados e terminados no final?

- [ ] Estrela
- [ ] Estrela estendida (extended star)
- [x] Barramento (bus)
- [ ] Anel

✅ RESPOSTA CORRETA: Barramento (bus)

> Um barramento tem todos os sistemas finais encadeados entre si e terminados no final.


# 31.2 Métodos de Controle de Acesso ao Meio

## 31.2.1 Comunicação Half e Full duplex

Compreender a comunicação duplex é importante ao discutir topologias de LAN porque se refere à direção da transmissão de dados entre dois dispositivos. Existem dois modos comuns de duplex.

### Comunicação meio duplex

Ambos os dispositivos podem transmitir e receber no meio físico, mas não podem fazer isso simultaneamente. WLANs e topologias de barramento herdadas com hubs Ethernet usam o modo meio duplex. O meio duplex permite que apenas um dispositivo envie ou receba por vez na mídia compartilhada. Clique em reproduzir na figura para ver a animação mostrando a comunicação meio duplex.
![[brave_81jJNpK17v.mp4]]
### Comunicação duplex completo

Ambos os dispositivos podem transmitir e receber simultaneamente na mídia compartilhada. A camada de enlace de dados supõe que o meio físico está disponível para transmissão para ambos os nós a qualquer momento. Os comutadores Ethernet operam no modo duplex completo por padrão, mas podem operar no modo meio duplex se estiverem conectados a um dispositivo como um hub Ethernet. Clique em reproduzir na figura para ver a animação mostrando a comunicação duplex completo.

![[brave_UIq2Rb9OaL.mp4]]


Em resumo, as comunicações meio duplex restringem a troca de dados a uma direção de cada vez. O modo duplex completo permite o envio e o recebimento simultâneos de dados.

É importante que duas interfaces interconectadas, como uma NIC de host e uma interface em um comutador Ethernet, operem usando o mesmo modo duplex. Caso contrário, haverá uma incompatibilidade de duplex que criará ineficiência e latência no link.


## 31.2.2 Métodos de controle de acesso

LANs Ethernet e WLANs são exemplos de redes multiacesso. Uma rede multiacesso é uma rede que pode ter dois ou mais dispositivos finais tentando acessar a rede simultaneamente.

Algumas redes multiacesso requerem regras para controlar como os dispositivos compartilham a mídia física. Existem dois métodos básicos de controle de acesso para meio físico compartilhado.

- Acesso baseado em contenção
- Acesso controlado

### Acesso Baseado em Contenção

Em redes multiacesso baseadas em contenção, todos os nós estão operando em meio duplex, competindo pelo uso do meio. No entanto, apenas um dispositivo pode enviar por vez. Portanto, há um processo se mais de um dispositivo transmitir ao mesmo tempo. Exemplos de métodos de acesso baseados em contenção incluem o seguinte:

- Acesso múltiplo com detecção de colisão (CSMA/CD) usado em LANs Ethernet de topologia de barramento herdada
- Acesso múltiplo por operadora com prevenção de colisão (CSMA/CA) usado em LANs sem fio
![[Pasted image 20260629092551.png]]


### Acesso Controlado

Em uma rede multiacesso controlada, cada nó tem seu próprio tempo para usar o meio. Esses tipos determinísticos de redes herdadas são ineficientes porque um dispositivo deve aguardar sua vez para acessar o meio. Exemplos de redes multiacesso que usam acesso controlado incluem o seguinte:

- Token Ring legada
- ARCNET legada
![[Pasted image 20260629093028.png]]

**Nota:** Atualmente, as redes Ethernet operam em duplex completo e não exigem um método de acesso.


## 31.2.3 Acesso baseado em contenção - CSMA/CD

Exemplos de redes de acesso baseadas em contenção incluem o seguinte:

- LAN sem fio (usa CSMA/CA)
- LAN Ethernet de topologia de barramento legado (usa CSMA/CD)
- LAN Ethernet herdada usando um hub (usa CSMA/CD)

Essas redes operam no modo meio duplex, o que significa que apenas um dispositivo pode enviar ou receber de cada vez. Isso requer um processo que determine quando um dispositivo pode enviar e o que acontece quando vários dispositivos enviam ao mesmo tempo.

Se dois dispositivos transmitirem simultaneamente, ocorre uma colisão. Para LANs Ethernet herdadas, ambos os dispositivos detectam a colisão na rede. Esta é a parte de detecção de colisão (CD) do CSMA/CD. A NIC compara os dados transmitidos com os dados recebidos ou reconhecendo que a amplitude do sinal é maior que o normal na mídia. Os dados enviados por ambos os dispositivos serão corrompidos e precisarão ser reenviados.

**Clique em cada botão para obter uma imagem e uma descrição do processo CSMA/CD em LANs Ethernet herdadas que usam um hub.**

### **PC1 envia um quadro**

O PC1 tem um quadro Ethernet para enviar ao PC3. A placa de rede PC1 precisa determinar se algum dispositivo está transmitindo na mídia. Se ele não detectar um sinal de operadora (em outras palavras, não estiver recebendo transmissões de outro dispositivo), ele assumirá que a rede está disponível para envio.

A placa de rede PC1 envia o quadro Ethernet quando a mídia está disponível, conforme mostrado na figura.

![[Pasted image 20260629093111.png]]


### **O hub recebe o quadro**

O hub Ethernet recebe e envia o quadro. Um hub Ethernet também é conhecido como repetidor multiporta. Quaisquer bits recebidos em uma porta de entrada são regenerados e enviados para todas as outras portas, conforme mostrado na figura.

Se outro dispositivo, como o PC2, quiser transmitir, mas estiver recebendo um quadro no momento, deverá aguardar até que o canal esteja limpo, como mostra a figura.

![[Pasted image 20260629093143.png]]

### **O Hub Envia o Quadro**

Todos os outros dispositivos conectados ao hub receberão o quadro. No entanto, como o quadro possui um endereço de link de dados de destino para PC3, somente esse dispositivo aceitará e copiará o quadro inteiro. Todas as outras NICs do dispositivo ignoram o quadro, como mostrado na figura.
![[Pasted image 20260629093156.png]]


## 31.2.4 Acesso Baseado em Contenção – CSMA/CA

Outra forma de CSMA usada pelas WLANs IEEE 802.11 é o acesso múltiplo por detecção de portadora/prevenção de colisão (CSMA/CA).

O CMSA/CA usa um método semelhante ao CSMA/CD para detectar se a mídia está livre. O CMSA/CA usa técnicas adicionais. Em ambientes sem fio pode não ser possível para um dispositivo detectar uma colisão. O CMSA/CA não detecta colisões, mas tenta evitá-las esperando antes de transmitir. Cada dispositivo que transmite inclui o tempo necessário para a transmissão. Todos os outros dispositivos sem fio recebem essas informações e sabem quanto tempo a mídia ficará indisponível.

Na figura, se o host A estiver recebendo um quadro sem fio do ponto de acesso, os hosts B e C também verão o quadro e por quanto tempo a mídia ficará indisponível.

![[Pasted image 20260629093311.png]]

Depois que um dispositivo sem fio enviar um quadro 802.11, o receptor retornará uma confirmação para que o remetente saiba que o quadro chegou.

Quer se trate de uma LAN Ethernet que use hubs, ou uma WLAN, os sistemas baseados em contenção não escalam bem sob uso intenso.

**Nota**: As LANs Ethernet que usam switches não utilizam um sistema baseado em contenção porque o switch e a NIC do host operam no modo duplex completo.


## 31.2.5 Verifique sua compreensão - Métodos de controle de acesso ao meio

**Verifique sua compreensão sobre os métodos de controle de acesso ao meio escolhendo a resposta correta para as seguintes perguntas.**

### Pergunta 1

Qual método de comunicação duplex é usado em WLANs?

- [x] Meio duplex
- [ ] duplex completo
- [ ] Simplex

✅ RESPOSTA CORRETA: Meio duplex

> As LANs sem fio (WLANs) suportam apenas meio duplex porque apenas um dispositivo pode acessar a mídia de cada vez.

---

### Pergunta 2

Quais métodos de controle de acesso à mídia são baseados em contenção? (Escolha duas.)

- [ ] Token Ring
- [ ] ARCNET
- [x] CSMA/CA
- [x] CSMA/CD

✅ RESPOSTA CORRETA: CSMA/CA / CSMA/CD

> O acesso múltiplo com detecção de portadora e detecção de colisão (CSMA/CD) e o acesso múltiplo com detecção portadora com prevenção de colisão (CSMA/CA) são métodos de acesso baseados em contenção.

---

### Pergunta 3

Qual método de controle de acesso requer que o destino envie uma confirmação para que o remetente saiba que o quadro chegou?

- [ ] CSMA/CD
- [x] CSMA/CA
- [ ] Token Ring
- [ ] ARCNET

✅ RESPOSTA CORRETA: CSMA/CA

> O método de acesso CSMA/CA exige que o destinatário retorne uma confirmação para que o remetente saiba que o quadro chegou.


# 31.3 Resumo da Camada de Enlace de dados

## 31.3.1 O que aprendi neste módulo?

### Topologias

Os dois tipos de topologias usados em redes LAN e WAN são físicos e lógicos. A camada de enlace de dados "vê" a topologia lógica da rede quando controla o acesso de dados ao meio físico. A topologia lógica influencia o tipo de enquadramento da rede e controle de acesso à mídia usado. Três tipos comuns de topologias WAN físicas são: ponto a ponto, hub e spoke e malha. As topologias ponto a ponto físicas conectam diretamente dois dispositivos finais (nós). A adição de conexões físicas intermediárias pode não alterar a topologia lógica. Em LANs de acesso múltiplo, os nós são interligados usando topologias em estrela ou estrela estendida. Neste tipo de topologia, os nós são conectados a um dispositivo intermediário central.

As topologias de LAN físicas incluem: estrela, estrela estendida, barramento e anel. As comunicações meio duplex trocam dados em uma direção de cada vez. duplex completo envia e recebe dados simultaneamente. Duas interfaces interconectadas devem usar o mesmo modo duplex ou haverá uma incompatibilidade duplex criando ineficiência e latência no link. LANs Ethernet e WLANs são exemplos de redes multiacesso. Uma rede multiacesso é uma rede que pode ter vários nós acessando a rede simultaneamente.

Algumas redes multiacesso requerem regras para controlar como os dispositivos compartilham a mídia física. Existem dois métodos básicos de controle de acesso para mídia compartilhada: acesso baseado em contenção e acesso controlado. Em redes multiacesso baseadas em contenção, todos os nós estão operando em meio duplex. Existe um processo se mais de um dispositivo transmitir ao mesmo tempo. Exemplos de métodos de acesso baseados em contenção incluem: CSMA/CD para LANs Ethernet de topologia barramento e CSMA/CA para WLANs.

---

## 31.3.2 Webster – Questões para Reflexão

Eu de novo!

Halimah teve que examinar a rede em sua sede na Nigéria. Ela tem muita experiência na criação de topologias. Os dois tipos de topologias usados em redes LAN e WAN são físicos e lógicos. O Halima pode facilmente criar e interpretar topologias.

Você consegue desenhar uma topologia da sua rede doméstica? Isso pode ser um pouco mais simples do que a topologia em seu prédio de escritórios.

Que tipo de topologia você acha que seu prédio tem? Considere perguntar a alguém do seu departamento de TI se você pode analisar a topologia.