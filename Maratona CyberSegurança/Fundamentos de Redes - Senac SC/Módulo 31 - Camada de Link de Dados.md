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

