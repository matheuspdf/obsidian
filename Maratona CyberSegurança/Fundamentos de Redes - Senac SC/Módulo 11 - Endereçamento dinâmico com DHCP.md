
# 11.0 Introdução

## 11.0.1 Webster - Por que devo fazer este módulo?

A estação de enfermagem de Kishori acabou de receber um novo laptop do departamento de TI. O especialista de TI, Madhav, está preparando a mesa e tentando se conectar à rede. Ele pede a Kishori para fazer login no computador. Ela digita o nome de usuário e a senha e tenta acessar o prontuário do paciente. Ela explica que deve haver um erro de conexão. Madhav senta para investigar. Madhav verifica o cabo e ele está conectado. Em seu tablet, ele exibe a lista de endereços IPv4 de todos os computadores neste andar nessa rede. Ele encontrou o problema! Há um erro no endereço IPv4. Madhav explica que o estagiário em seu departamento pode ter configurado manualmente as informações de rede neste host, em vez de usar o DHCP (Dynamic Host Configuration Protocol). Kishori nunca ouviu falar sobre DHCP. Ela vai ler sobre esse assunto.

Você está pronto para aprender sobre DHCP? Estou aqui para ajudar! Vamos começar este módulo!

## 11.0.2 O que vou aprender neste módulo?

**Título do Módulo:** Endereçamento dinâmico com DHCP

**Objetivo do Módulo:** Configurar um servidor DHCP.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Endereçamento estático e dinâmico|Comparar o endereçamento IPv4 estático e dinâmico.|
|Configuração do DHCPv4|Configurar um servidor DHCPv4 para atribuir endereços IPv4 de forma dinâmica.|

# 11.1 Endereçamento estático e dinâmico

## 11.1.1 Atribuição de endereço IPv4 estático

Os endereços IPv4 podem ser atribuídos estática ou dinamicamente.

Com uma atribuição estática, o administrador de rede deve configurar manualmente as informações da rede para um host. No mínimo, isso inclui o seguinte:

- **Endereço IP**– Identifica o computador na rede.
- **Máscara de Sub-rede** - Identifica a rede à qual o host está conectado
- **Gateway padrão** – Identifica o dispositivo de rede que o host usa para acessar a Internet ou outra rede remota.

Os endereços estáticos têm algumas vantagens. Por exemplo, são úteis para impressoras, servidores e outros dispositivos de rede que precisam estar acessíveis para clientes na rede. Se os hosts normalmente acessam um servidor em um determinado endereço IPv4, não seria bom que esse endereço mudasse.

Embora a atribuição estática de informações de endereçamento possa proporcionar um controle maior dos recursos de rede, a digitação de informações em cada host pode ficar demorada. Quando os endereços IPv4 são inseridos estaticamente, o host executa apenas verificações básicas de erro no endereço IPv4. Isso aumenta a probabilidade de que ocorram erros.

Ao usar endereçamento IPv4 estático, é importante manter uma lista precisa de quais endereços IPv4 estão atribuídos a quais dispositivos. Além disso, como são endereços permanentes, normalmente eles não são reutilizados.

![[Pasted image 20260606223023.png]]

## 11.1.2 Atribuição dinâmica de endereço IPv4

Nas redes locais, geralmente, a população de usuários muda com frequência. Novos usuários chegam com notebooks e precisam de uma conexão. Outros têm novas estações de trabalho que precisam ser conectadas. Em vez de fazer com que o administrador de rede atribua endereços IPv4 em cada estação de trabalho, é mais eficiente ter endereços IPv4 atribuídos automaticamente. Isso é feito com um protocolo conhecido como Dynamic Host Configuration Protocol (DHCP).

O DHCP fornece um mecanismo para atribuição automática de informações de endereçamento, como endereço IPv4, máscara de sub-rede, gateway padrão e outras informações de configuração, como mostrado na figura.

O DHCP em geral é o método preferido de designação de endereços IPv4 para hosts em redes grandes porque reduz a carga sobre a equipe de suporte da rede e praticamente elimina erros de entrada.

Outro benefício do DHCP é que o endereço não é permanentemente atribuído a um host, mas é só “alugado” por um período. Se o host é desligado ou retirado da rede, o endereço retorna ao pool para ser reutilizado. Isso é especialmente útil com usuários móveis que vêm e vão em uma rede.

![[Pasted image 20260606223037.png]]

## 11.1.3 Servidores DHCP

Se você inserir um hotspot sem fio em um aeroporto ou uma lanchonete, o DHCP possibilitará o acesso à Internet. Ao entrar na área, o cliente DHCP de seu laptop entra em contato com o servidor DHCP local via conexão sem fio. O servidor DHCP atribui um endereço IPv4 ao seu notebook.

Vários tipos de dispositivos podem ser servidores DHCP, desde que executem software de serviço DHCP. Na maioria das redes médias a grandes, o servidor DHCP normalmente é um servidor local dedicado baseado em PC.

Nas redes residenciais, é provável que o servidor DHCP esteja localizado no ISP. Um host na rede residencial recebe a configuração IPv4 diretamente do ISP, como mostrado na figura.

![[Pasted image 20260606223057.png]]

Muitas redes de residências e pequenas empresas usam um modem e um roteador sem fio. Nesse caso, o roteador sem fio é tanto servidor como cliente DHCP. O roteador sem fio atua como cliente para receber a configuração de IPv4 do ISP e atua como servidor DHCP para hosts internos na rede local. O roteador recebe o endereço IPv4 público do ISP e, em sua função como servidor DHCP, distribui endereços privados para os hosts internos.

Além de servidores baseados em PC e roteadores sem fio, outros tipos de dispositivos de rede (como roteadores dedicados) podem fornecer serviços DHCP aos clientes, embora isso não seja tão comum.

## 11.1.4 Verifique sua compreensão - Endereçamento dinâmico e estático

**Verifique sua compreensão de endereçamento estático e dinâmico, escolhendo a melhor resposta para as seguintes perguntas.**


### Pergunta 1

Quem é responsável por atribuir estaticamente as informações de endereçamento IP?

- [ ] o usuário do dispositivo
- [x] o administrador de redes
- [ ] o sistema operacional instalado no dispositivo
- [ ] o fabricante do dispositivo

✅ RESPOSTA CORRETA: o administrador de redes

> Embora um usuário possa atribuir informações de endereçamento IP, isso geralmente é de responsabilidade do administrador de rede.

---

### Pergunta 2

Qual protocolo é responsável pela atribuição automática de informações de endereçamento IP?

- [ ] IETF
- [ ] NAT
- [ ] IPv4
- [x] DHCP

✅ RESPOSTA CORRETA: DHCP

> DHCP (Protocolo de Configuração Dinâmica de Host) é responsável pela atribuição automática de informações de endereçamento IP.


# 11.2 Configuração do DHCPv4

## 11.2.1 Vídeo - Operação do DHCPv4
![[11.2.1.mp4#subtitle=anexos/11.2.1.vtt]]
Nesta aula vamos conversar sobre como o DHCP funciona.

Anteriormente, você aprendeu que as atribuições de endereço IP podem ser distribuídas de duas maneiras: estaticamente, significando que alguém realmente se senta e configura o endereço IP, ou dinamicamente, onde o dispositivo obtém seu endereço de um servidor DHCP.

DHCP significa protocolo de configuração de host dinâmico. Então, como funciona esse protocolo? O protocolo descreve um conjunto de mensagens que vão entre o host que deseja um endereço IP e o servidor DHCP que fornece o endereço IP.

Basicamente, o que temos é um host que envia um pacote chamado **descoberta de DHCP**. O que este pacote está fazendo é procurar por um servidor DHCP. O pacote é um pacote de broadcast, e contém o endereço MAC do dispositivo solicitando o endereço IP, e é destinado para qualquer dispositivo na rede que esteja configurado para ser um servidor DHCP.

Que tipo de dispositivos podem ser servidores DHCP? Normalmente, em uma rede doméstica, o roteador doméstico — o roteador sem fio ou o roteador com fio — está configurado para fornecer DHCP. Em ambientes maiores, muitas vezes é um servidor que estaria fazendo outras funções, como o controle de domínio da Microsoft, ou pode ser um servidor Linux que também funciona como um servidor web. Então, basicamente, o servidor DHCP pode ser um número de diferentes tipos de dispositivos.

Quando a descoberta DHCP sai, uma vez que é um broadcast, qualquer servidor DHCP conectado à rede vai ouvir isso. O servidor DHCP então responde com uma **oferta DHCP**.

O pacote de oferta DHCP contém um endereço IP que o host, o dispositivo individual, poderá usar, se aceitar. Quando o host recebe o pacote de oferta DHCP do servidor DHCP, este contém o endereço IP que foi enviado, a máscara de sub-rede, bem como o endereço de gateway padrão.

Uma vez que o host recebe isso, ele envia de volta um pacote de **solicitação DHCP** para aceitar a oferta, e solicitará o endereço IP que o servidor enviou, 192.168.1.15. O dispositivo irá então pegar esta informação e inseri-la em suas configurações de endereço IP.

E nesse momento, uma vez que o servidor recebe a solicitação DHCP, o servidor enviará de volta uma **confirmação de DHCP** que indicará ao host que o servidor está colocando este endereço IP em sua tabela associada ao endereço MAC que foi enviado pelo host.

## 11.2.2 Vídeo - Configuração do Serviço DHCP
![[11.2.2.mp4#subtitle=anexos/11.2.2.vtt]]
Existem duas maneiras de obter um endereço IP em um dispositivo. Uma maneira é configurá-lo manualmente, ou configurá-lo estaticamente, como é chamado no Microsoft Windows. A outra maneira é obtê-lo automaticamente de um dispositivo que fornece DHCP.

Na pequena rede mostrada no Packet Tracer, temos três PCs conectados a um roteador habilitado para DHCP. Basicamente, este é um dispositivo muito semelhante ao que você deve ter em casa. O dispositivo tem uma porta de switch, uma antena para wireless e uma conexão com a internet. Este tipo de configuração está disponível em quase todos os roteadores sem fio domésticos.

O que vamos fazer é entrar e verificar como o DHCP está configurado neste dispositivo. A maioria dos dispositivos domésticos, dispositivos de rede doméstica, têm uma interface GUI para facilitar a configuração. Neste roteador, vamos habilitar o DHCP e, como você pode ver, por padrão normalmente está habilitado. Você pode ver que um endereço IP já foi atribuído para a interface do roteador voltada para a LAN. Quando a configuração automática é recebida pelos PCs, eles verão esse endereço como seu gateway padrão.

A maneira como o DHCP está configurado é um grupo de endereços reservados em uma determinada rede para ser entregue aos hosts, um por um. Se você olhar nas configurações, ele dirá que o intervalo DHCP começará em 172.16.0.100.

Então, salvando essa configuração, vamos para os PCs e habilitamos cada PC para obter seu endereço IP via DHCP, em vez da configuração estática. Vamos para a área de trabalho, vemos a configuração de IP, e então mudamos da configuração estática para obter o endereço IP via DHCP. Você notará que imediatamente o dispositivo enviou uma solicitação para um endereço DHCP e recebeu um do servidor DHCP. Como este é o primeiro PC a ser configurado para DHCP, ele obteve o primeiro endereço disponível.

Quando olhamos para os outros PCs e vemos suas configurações de IP, se os mudarmos para DHCP, eles também receberão endereços, mas não será o mesmo endereço. Será o próximo número acima.

Com os endereços IP definidos, agora podemos testar a conectividade de rede. Estando no PC zero, vamos fazer ping em um dos outros PCs. Sabemos que como temos o endereço 100, os outros dois dispositivos possuem os endereços 101 e 102. Fazendo ping nesses dois computadores, podemos alcançar o computador 101, que é PC1 no diagrama. Fazendo ping no PC2, podemos alcançá-lo também. Então as informações que estavam na configuração do roteador para DHCP determinaram quais endereços IP seriam atribuídos a todos os PCs na rede.

## 11.2.3 Packet Tracer – Configuração do DHCP em um Roteador Wireless (sem fio)

Nesta atividade, você completará os seguintes objetivos:

- Conectar 3 PCs a um roteador wireless (sem fio)
- Alterar a configuração do DHCP para uma faixa de rede específica
- Configurar os clientes para obter seus endereços por DHCP


### Configuração do DHCP em um Roteador Wireless (sem fio)

## Objetivos

- Conectar 3 PCs a um roteador sem fio
- Alterar a configuração do DHCP para uma faixa de rede específica
- Configurar os clientes para obter seus endereços por DHCP

## Histórico/Cenário

Um usuário doméstico quer usar um roteador sem fio para conectar 3 PCs. Todos os 3 PCs devem obter seus endereços automaticamente a partir do roteador sem fio.

## Instruções

## Parte 1: Configurar a topologia de rede

a.  Adicione três PCs genéricos.

b.  Conecte cada PC a uma porta Ethernet a um roteador sem fio com cabos diretos.

## Parte 2: Observar as configurações DHCP padrão

a.  Após as luzes amarelas ficarem verdes, clique em **PC0**. Clique na guia **Desktop**. Selecione **IP Configuration**. Selecione **DHCP** para receber um endereço IP do roteador **habilitado para DHCP.**

#### Pergunta:

Anote o endereço IP do gateway padrão.

Área de Resposta

192.168.0.1

Ocultar resposta

b.  Feche a janela **IP Configuration**.

c.  Abra um Navegador Web.

d.  Digite o endereço IP do gateway padrão registrado anteriormente no campo URL. Quando solicitado, insira o nome de usuário **admin** e a senha **admin**.

e.  Role pela página Configuração Básica para visualizar as configurações padrão, incluindo o endereço IP padrão do roteador sem fio.

f.   Observe que o DHCP está ativado, o endereço inicial da faixa DHCP e a faixa dos endereços disponíveis aos clientes.

## Parte 3: Altere os endereços IP padrão do roteador sem fio.

a.  Na seção Configurações do IP do Roteador, altere o endereço IP para: **192.168.5.1**.

b.   Vá até o final da página e clique em **Save Settings** (Salvar Configurações).

c.  Se tudo for feito corretamente, a página Web exibirá uma mensagem de erro. Feche o navegador Web.

d.  Clique em **IP Configuration** para renovar o endereço IP atribuído. Clique em **Static (Estático)**. Clique em **DHCP** para receber novas informações de endereço IP do roteador sem fio.

e.  Abra o Navegador Web, digite o endereço IP **192.168.5.1** no campo URL. Quando solicitado, insira o nome de usuário **admin** e a senha **admin**.

## Parte 4: Altere o intervalo de endereços DHCP padrão.

a.  Observe que o endereço IP inicial do servidor DHCP é atualizado para a mesma rede do IP do roteador.

b.  Altere o endereço IP inicial de 192.168.5.100 para **192.168.5.126**.

c.  Altere o Número Máximo de Usuários para **75**.

d.   Vá até o final da página e clique em **Save Settings** (Salvar Configurações). Feche o Navegador Web.

e.  Clique **em IP Configuration** para renovar o endereço IP atribuído. Clique em  **Static (Estático)**. Clique em **DHCP** para receber novas informações de endereço IP do roteador sem fio.

f.   Selecione **Command Prompt**. Insira **ipconfig**.

#### Pergunta:

Anote o endereço IP do PC0:

Área de Resposta

192.168.5.126

Ocultar resposta

## Parte 5: Ative o DHCP nos outros PCs.

a.  Clique em **PC1**.

b.  Selecione a guia **Desktop**.

c.  Selecione Configuração de IP.

d.  Clique em **DHCP**.

#### Pergunta:

Anote o endereço IP do PC1:

Área de Resposta

192.168.5.127

Ocultar resposta

e.  Feche a janela de configuração de

f.   Ative o DHCP no **PC2** seguindo as etapas para o PC1.

## Parte 6: Verifique a conectividade

a.  Clique no **PC2** e selecione a guia **Desktop**.

b.  Selecione Command Prompt.

c.  Digite **ipconfig** no prompt para visualizar a configuração de IP.

d.   No prompt, digite **ping 192.168.5.1** para pingar o roteador wireless.

e.  Execute o comando **ping 192.168.5.126** para fazer ping em PC0.

f.   No prompt, digite **ping 192.168.5.127** para fazer ping em PC1.

g.  Os pings para todos os dispositivos devem ser bem-sucedidos.


# 11.13 Resumo Endereçamento Dinâmico com DHCP

## 11.3.1 O que aprendi neste módulo?

### Endereçamento estático e dinâmico

Com uma atribuição estática, o administrador de rede deve configurar manualmente as informações da rede para um host. No mínimo, isso inclui o endereço IPv4, a máscara de sub-rede e o gateway padrão do host. Embora a atribuição estática de informações de endereçamento possa proporcionar um controle maior dos recursos de rede, a digitação de informações em cada host pode ficar demorada. Ao usar endereçamento IPv4 estático, é importante manter uma lista precisa de quais endereços IPv4 estão atribuídos a quais dispositivos.

Os endereços IPv4 podem ser atribuídos automaticamente usando um protocolo conhecido como DHCP. O DHCP em geral é o método preferido de designação de endereços IPv4 para hosts em redes grandes porque reduz a carga sobre a equipe de suporte da rede e praticamente elimina erros de entrada. Outro benefício do DHCP é que o endereço não é permanentemente atribuído a um host, mas é só "alugado" por um período. Se o host é desligado ou retirado da rede, o endereço retorna ao pool para ser reutilizado.

Assim que você entra na área com um ponto de acesso sem fio, o cliente DHCP do seu notebook entra em contato com o servidor DHCP local por meio de uma conexão sem fio. O servidor DHCP atribui um endereço IPv4 ao seu notebook. Nas redes residenciais, é provável que o servidor DHCP esteja localizado no ISP e um host na rede residencial recebe a configuração IPv4 diretamente do ISP. Muitas redes de residências e pequenas empresas usam um modem e um roteador sem fio. Nesse caso, o roteador sem fio é tanto servidor como cliente DHCP.

---

### Configuração do DHCPv4

O servidor DHCP é configurado com um intervalo (ou pool) de endereços IPv4 que podem ser atribuídos a clientes DHCP. Um cliente que precise de um endereço IPv4 enviará uma mensagem de descoberta DHCP que é um broadcast com o endereço IPv4 de destino 255.255.255.255 (32 uns) e o endereço MAC de destino FF-FF-FF-FF-FF-FF (48 uns). Todos os hosts na rede receberão esse quadro DHCP de broadcast, mas apenas um servidor DHCP responderá. O servidor responderá com uma oferta DHCP, sugerindo um endereço IPv4 para o cliente. O host então envia uma solicitação DHCP pedindo para usar o endereço IPv4 sugerido. O servidor responde com um DHCP Acknowledgment.

Na maioria das redes de residências e pequenas empresas, um roteador sem fio fornece serviços DHCP aos clientes de rede local. Para configurar um roteador sem fio residencial, acesse a interface gráfica Web abrindo o navegador e inserindo o endereço IPv4 padrão do roteador. O endereço IPv4 192.168.0.1 e a máscara de sub-rede 255.255.255.0 são os padrões para a interface interna do roteador. Este é o gateway padrão para todos os hosts na rede local e também o endereço IPv4 interno do servidor DHCP. A maioria dos roteadores sem fio residenciais têm o servidor DHCP ativado por padrão.

## 11.3.2 Webster — Questões para Reflexão

Você inseriu manualmente um endereço IPv4 para todos os dispositivos em sua rede doméstica? Eles são chamados de endereços estáticos. Fiz isso na minha rede doméstica e cometi um erro ao inserir o endereço do tablet. Eu tive que refazê-lo. Você pode imaginar ter que fazer isso em uma grande rede corporativa com centenas ou até milhares de dispositivos? Quais são as outras vantagens de usar o DHCP para endereçamento de dispositivos?