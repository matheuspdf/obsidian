
# 8.0 Introdução

## 8.0.1 Webster - Por que devo fazer este módulo?

Kishori está aprendendo muito com Rina! Ela entende que, quando envia ou recebe um pacote pelo correio, há um endereço exclusivo envolvido. Um código postal é essencial no endereço para rotear o pacote para a agência postal correta. Ela pergunta a Rina se os computadores usam algo como um código postal para encaminhar a mensagem para o local correto. Rina explica mais detalhes sobre o processo e explica que, assim como o endereço residencial de Kishori identifica onde ela mora, um endereço IPv4 identifica um host na rede. Um host precisa de um endereço IPv4 para entrar na Internet. Cada pacote enviado pela Internet tem um endereço IPv4 de origem e de destino. Essa informação é necessária para os dispositivos de rede garantirem que os dados cheguem ao destino e que as respostas sejam retornadas à origem.

Minha amiga Kishori nunca pensou que ela estaria tão interessada em todas essas informações de tecnologia, mas ela realmente quer saber mais! E você? Aproveite este módulo para saber mais sobre o protocolo da Internet e a estrutura dos endereços IPv4!


## 8.0.2 O que vou aprender neste módulo?

**Titulo do Módulo:** O IP (Protocolo de Internet)

**Objetivo do Módulo:** Explicar os recursos de um endereço IP.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Finalidade de um endereço IPv4|Explicar a finalidade de um endereço IPv4.|
|A estrutura do endereço IPv4|Explicar como os endereços IPv4 e as sub-redes são usados juntos.|

# 8.1 Finalidade de um endereço IPv4

## 8.1.1 O endereço IPv4

Um host precisa de um endereço IPv4 para entrar na Internet. O endereço IPv4 é um endereço de rede lógico que identifica um host específico. Ele deve ser configurado corretamente e de forma exclusiva dentro da LAN, para fornecer comunicação local. Também deve ser configurado corretamente e de forma exclusiva no mundo, para fornecer comunicação remota. É assim que um host se comunica com outros dispositivos na Internet.

Um endereço IPv4 é atribuído à conexão de interface de rede de um host. Essa conexão geralmente é uma placa de interface de rede (NIC) instalada no dispositivo. Estações de trabalho, servidores, impressoras de rede e telefones IP são exemplos de dispositivos de usuário final com interfaces de rede. Alguns servidores podem ter mais de uma NIC e cada um deles tem seu próprio endereço IPv4. As interfaces de roteador que fornecem conexões a uma rede IP também têm um endereço IPv4.

Cada pacote enviado pela Internet tem um endereço IPv4 de origem e de destino. Essa informação é necessária para os dispositivos de rede garantirem que os dados cheguem ao destino e que as respostas sejam retornadas à origem.

## 8.1.2 Octetos e notação decimal com ponto

Os endereços IPv4 têm 32 bits de comprimento. Aqui está um endereço IPv4 em binário:  
**11010001101001011100100000000001**

Observe como é difícil ler este endereço. Imagine ter que configurar dispositivos com uma série de 32 bits! Por esse motivo, os 32 bits são agrupados em quatro bytes de 8 bits chamado octetos:  
**11010001.10100101.11001000.00000001**

Está melhor, mas ainda assim difícil de ler. É por isso que convertemos cada octeto em seu valor decimal, separados por um ponto decimal ou por um período. O IPv4 binário acima torna-se esta representação decimal com ponto: **209.165.200.1**

**Observação:** por enquanto, você não precisa saber como converter entre sistemas de números binários e decimais.

## 8.1.3 Packet Tracer – Conexão com um servidor da Web

### Objetivos

Observe como os pacotes são enviados pela Internet usando endereços IP.

### Instruções

#### Parte 1: Verificar a conectividade ao servidor da Web

a.  Abra a janela do prompt de comando do host de origem. Selecione **PC0**.

b.  Selecione a guia Desktop > Command Prompt.

c.  Verificar a conectividade ao servidor da Web. No prompt de comando, pingue o endereço IP do servidor web digitando **ping 172.33.100.50**.

PC> **ping 172.33.100.50**

Pinging 172.33.100.50 with 32 bytes of data:

Reply from 172.33.100.50: bytes=32 time=0ms TTL=127

Reply from 172.33.100.50: bytes=32 time=0ms TTL=127

Reply from 172.33.100.50: bytes=32 time=0ms TTL=127

Reply from 172.33.100.50: bytes=32 time=0ms TTL=127

Ping statistics for 172.33.100.50:

Packets: Sent = 4, Received = 3, Lost = 1 (25% loss),

Approximate round trip times in milli-seconds:

Minimum = 0ms, Maximum = 0ms, Average = 0ms

Uma resposta verifica a conectividade do cliente com o servidor web de destino. A resposta pode atingir o tempo limite enquanto os dispositivos carregam e o ARP é executado.

d.  Feche somente a janela do prompt de comando ao selecionar o x na janela do prompt de comando. Certifique-se de deixar a janela de configurações do PC0 aberta.

#### Parte 2: Conecte-se ao servidor da Web através do cliente da Web.

a.  Na guia Desktop no PC0, escolha **Web Browser.**

b.  Insira **172.33.100.50** na URL e clique em **Go**. O cliente Web será conectado ao servidor Web através do endereço IP e abrirá a página da Web.

Quais mensagens você viu após a página Web ter sido carregada?

**R: Welcome to the Learn IP Web Site**
**You were able to reach this website because you had the IP address of the web server. O PC que conectou também tinha um cliente Web em execução no dispositivo.**


# 8.2 A estrutura do endereço IPv4

## 8.2.1 Video - Estrutura do Endereço IPv4
![[8.2.1.mp4#subtitle=anexos/8.2.1.vtt]]
Nesta lição vamos falar sobre como o endereçamento IP funciona em um ambiente de várias redes. Originalmente, quando falamos sobre endereçamento IP, todos os dispositivos com os quais estávamos nos comunicando estavam na mesma rede local. Então, como o IP sabe quando um dispositivo está em uma rede diferente?

Basicamente, vamos ver nossa rede dividida aqui. Temos o Departamento de Gestão de Redes, departamento de contabilidade e o Departamento de Vendas. Cada um desses departamentos tem uma estrutura de endereçamento IP que é exclusivo para sua rede local.

Agora, como sabemos qual parte do endereço IP diferencia as redes. Basicamente, todo endereço IP tem uma estrutura para ele e essa estrutura inclui um componente de rede, e vamos pegar um endereço de rede que está aqui. Tem um componente de rede e tem um componente host.

Todos os dispositivos na rede local do Departamento de Vendas terão que ter os mesmos três primeiros octetos do seu endereço IP, porque esta rede é representada pelo 192.168.3. Os números de host individuais, que são o último octeto, terá que ser único. Em outras palavras, seu computador aqui tem o endereço de 192.168.3.10. Nenhum outro dispositivo nessa mesma rede pode ter o mesmo endereço IP, porque cada parte do host deve ser única.

Assim, em uma rede local, a parte da rede tem que ser a mesma e a parte do host deve ser única. Agora, se passarmos para a próxima rede aqui, podemos ver que a parte da rede é diferente. Tínhamos a rede 192.168.3 aqui. Temos a rede 192.168.2 aqui. Se eu for ao Gerenciamento de Rede, onde estou localizado, você verá que estou na rede 192.168.1.

É muito importante lembrar que se o seu endereço IP é tal que sua parte de rede não corresponde ao que sua rede local está atribuída, você não será capaz de se comunicar. Então, se eu acidentalmente peguei um computador daqui e mudei para cá e não alterei o endereço IP, ele não será capaz de se comunicar pela rede IP.

Então, basicamente, para ter uma rede IP, a parte de rede do endereço deve ser a mesma para todos os computadores na rede local.

## 8.2.2 Redes e hosts

O endereço lógico IPv4 de 32 bits é hierárquico e contém duas partes, a rede e o host. Na figura, a porção de rede é azul e a porção de host é vermelha. As duas partes são necessárias em um endereço IPv4. Ambas as redes têm a máscara de sub-rede 255.255.255.0. Máscara de sub-rede é usada para identificar a rede à qual o host está conectado.

Como exemplo, um host com o endereço IPv4 192.168.5.11 e a máscara de sub-rede 255.255.255.0. Os três primeiros octetos (192.168.5) identificam a porção de rede do endereço e o último octeto (11) identifica o host. Isso é conhecido como endereçamento hierárquico porque a porção de rede indica a rede na qual está localizado cada endereço exclusivo de host. Os roteadores precisam saber apenas como alcançar cada rede, em vez de precisar saber a localização de cada host individual.

Com o endereçamento IPv4, poderão existir diversas redes lógicas em uma rede física se a porção de rede dos endereços de hosts de rede lógica for diferente. Por exemplo: três hosts em uma única rede local física têm a mesma porção de rede do endereço IPv4 (192.168.18) e outros três hosts têm porções de rede diferentes de seus endereços IPv4 (192.168.5). Os hosts com o mesmo número de rede em seus endereços IPv4 poderão se comunicar entre si, mas não com os outros hosts sem o uso de roteamento. Neste exemplo, há uma rede física e duas redes IPv4 lógicas.

Outro exemplo de rede hierárquica é o sistema telefônico. Em um número de telefone, o código de país, o código de área e a central telefônica representam o endereço de rede e os dígitos restantes representam um número de telefone local.

![[Pasted image 20260528211752.png]]
## 8.2.3 Verifique o seu entendimento - Estrutura de endereços IPv4

### Pergunta 1

O Host-A tem o endereço IPv4 e a máscara de sub-rede 10.5.4.100 255.255.255.0. Qual é o endereço de rede do Host-A?

- [ ] 10.0.0.0
- [x] 10.5.4.0
- [ ] 10.5.0.0
- [ ] 10.5.4.100

✅ RESPOSTA CORRETA: 10.5.4.0

> O endereço de rede para 10.5.4.100 com uma máscara de sub-rede de 255.255.255.0 é 10.5.4.0.

---

### Pergunta 2

O Host-A tem endereço IPv4 e máscara de sub-rede 172.16.4.100 255.255.0.0. Qual é o endereço de rede do Host-A?

- [ ] 172.16.4.100
- [ ] 172.0.0.0
- [ ] 172.16.4.0
- [x] 172.16.0.0

✅ RESPOSTA CORRETA: 172.16.0.0

> O endereço de rede para 172.16.4.100 com uma máscara de sub-rede de 255.255.0.0 é 172.16.0.0.

---

### Pergunta 3

O Host-A tem o endereço IPv4 e a máscara de sub-rede 10.5.4.100 255.255.255.0. Quais dos seguintes endereços IPv4 estariam na mesma rede que o Host-A? (Escolha todas que se aplicam)

- [x] 10.5.4.99
- [ ] 10.0.0.98
- [x] 10.5.4.1
- [ ] 10.5.100.4
- [ ] 10.5.0.1

✅ RESPOSTAS CORRETAS: 10.5.4.99, 10.5.4.1

> O Host A está na rede 10.5.4.0. Portanto, os dispositivos com os endereços IPv4 10.5.4.1 e 10.5.4.99 estão na mesma rede.

---

### Pergunta 4

O Host-A tem endereço IPv4 e máscara de sub-rede 172.16.4.100 255.255.0.0. Quais dos seguintes endereços IPv4 estariam na mesma rede que o Host-A? (Escolha todas que se aplicam)

- [ ] 172.18.4.1
- [ ] 172.17.4.1
- [x] 172.16.0.1
- [ ] 172.17.4.99
- [x] 172.16.4.99

✅ RESPOSTAS CORRETAS: 172.16.0.1, 172.16.4.99

> O host A está na rede 172.16.0.0. Portanto, os dispositivos com os endereços IPv4 172.16.4.99 e 172.16.0.1 estão na mesma rede.

---

### Pergunta 5

O Host-A tem o endereço IPv4 e a máscara de sub-rede 192.168.1.50 255.255.255.0. Quais dos seguintes endereços IPv4 estariam na mesma rede que o Host-A? (Escolha todas que se aplicam)

- [ ] 192.168.0.100
- [x] 192.168.1.100
- [x] 192.168.1.1
- [ ] 192.168.0.1
- [ ] 192.168.2.1

✅ RESPOSTAS CORRETAS: 192.168.1.100, 192.168.1.1

> O Host A está na rede 192.168.1.0. Portanto, os dispositivos com os endereços IPv4 192.168.1.1 e 192.168.1.100 estão na mesma rede.


# 8.3 Resumo Procotolo IP

## 8.3.1 O que aprendi neste módulo?

### Finalidade do endereço IPv4

O endereço IPv4 é um endereço de rede lógico que identifica um host específico. Ele deve ser configurado corretamente e de forma exclusiva dentro da LAN, para fornecer comunicação local. Também deve ser configurado corretamente e de forma exclusiva no mundo, para fornecer comunicação remota.

Um endereço IPv4 é atribuído à conexão de interface de rede de um host. Essa conexão geralmente é uma placa de interface de rede (NIC) instalada no dispositivo.

Cada pacote enviado pela Internet tem um endereço IPv4 de origem e de destino. Essa informação é necessária para os dispositivos de rede garantirem que os dados cheguem ao destino e que as respostas sejam retornadas à origem.

---

### A estrutura do endereço IPv4

O endereço lógico IPv4 de 32 bits é hierárquico e contém duas partes, a rede e o host. Como exemplo, um host com o endereço IPv4 192.168.5.11 e a máscara de sub-rede 255.255.255.0. Os três primeiros octetos (192.168.5) identificam a porção de rede do endereço e o último octeto (11) identifica o host. Isso é conhecido como endereçamento hierárquico porque a porção de rede indica a rede na qual está localizado cada endereço exclusivo de host.

Os roteadores precisam saber apenas como alcançar cada rede, em vez de precisar saber a localização de cada host individual. Com o endereçamento IPv4, poderão existir diversas redes lógicas em uma rede física se a porção de rede dos endereços de hosts de rede lógica for diferente.

## 8.3.2 Webster – Questões para Reflexão

Faz sentido que cada dispositivo na rede tenha um endereço IP, e os roteadores usam esses endereços para enviar pacotes da origem para o destino. Quando envio uma carta pelo correio, coloco o endereço e o endereço do destinatário no envelope. Mas agora vejo a outra conexão a forma como as redes operam. O código postal e a cidade do meu destinatário são um pouco parecidos com a parte da rede do endereço IP, e o endereço é como a porção host do endereço IP. Você consegue pensar em outras analogias com as operações de rede e endereços IP?

## 8.3.3 Questionário sobre Protocolo Internet

### Pergunta 1

Que critério deve ser seguido no projeto de um esquema de endereçamento IPv4 para dispositivos finais?

- [x] Cada endereço IP deve ser único em uma mesma rede.
- [ ] Cada endereço IP precisa ser compatível com o endereço MAC.
- [ ] Cada endereço IP deve corresponder ao endereço atribuído ao host pelo DNS.
- [ ] Cada host local deve receber um endereço IP com um componente de rede exclusivo.

✅ RESPOSTA CORRETA: Cada endereço IP deve ser único em uma mesma rede.

---

### Pergunta 2

Quantos octetos existem em um endereço IPv4?

- [ ] 32
- [ ] 8
- [x] 4
- [ ] 16

✅ RESPOSTA CORRETA: 4

---

### Pergunta 3

Quais duas partes são componentes de um endereço IPv4? (Escolha duas.)

- [ ] parte física
- [ ] parte de broadcast
- [ ] parte de sub-rede
- [x] parte da rede
- [x] parte de host
- [ ] parte lógica

✅ RESPOSTAS CORRETAS: parte da rede, parte de host

---

### Pergunta 4

Qual é o objetivo de combinar a máscara de sub-rede com um endereço IP?

- [ ] identificar exclusivamente um host em uma rede
- [x] determinar a sub-rede a qual o host pertence
- [ ] identificar se o endereço é público ou privado
- [ ] mascarar o endereço IP para intrusos

✅ RESPOSTA CORRETA: determinar a sub-rede a qual o host pertence

---

### Pergunta 5

Um técnico está configurando o equipamento em uma rede. Quais são os três dispositivos que precisarão de endereços IP? (Escolha três.)

- [x] um servidor com duas placas de rede
- [x] uma impressora com uma placa de rede integrada
- [ ] um PDA conectado a uma estação de trabalho de rede
- [ ] um mouse sem fio
- [x] um telefone IP
- [ ] uma Web câmera conectada diretamente a um host

✅ RESPOSTAS CORRETAS: um servidor com duas placas de rede, uma impressora com uma placa de rede integrada, um telefone IP

---

### Pergunta 6

Qual afirmação descreve o relacionamento de uma rede física e redes endereçadas IPv4 lógicas?

- [ ] Os dispositivos finais em redes lógicas IPv4 diferentes podem se comunicar entre si se todos se conectarem ao mesmo switch.
- [ ] Uma rede física local é compatível com uma rede lógica IPv4.
- [x] Uma rede física pode conectar vários dispositivos de redes lógicas IPv4 diferentes.
- [ ] Todos os dispositivos conectados a uma rede física precisam pertencer à mesma rede lógica IPv4.

✅ RESPOSTA CORRETA: Uma rede física pode conectar vários dispositivos de redes lógicas IPv4 diferentes.

---

### Pergunta 7

Qual o tamanho dos endereços IPv4?

- [ ] 64 bits
- [ ] 8 bits
- [x] 32 bits
- [ ] 128 bits
- [ ] 16 bits

✅ RESPOSTA CORRETA: 32 bits

---

### Pergunta 8

Qual é o número de rede para um endereço IPv4 172.16.34.10 com a máscara de sub-rede de 255.255.255.0?

- [ ] 10
- [ ] 172.16.0.0
- [x] 172.16.34.0
- [ ] 34.10

✅ RESPOSTA CORRETA: 172.16.34.0

---

### Pergunta 9

Quais são os dois recursos dos endereços IPv4? (Escolha duas.)

- [ ] Os endereços IPv4 são usados apenas para comunicações na Internet.
- [x] IPv4 é um esquema de endereçamento lógico.
- [ ] Um endereço IPv4 é vinculado a uma placa de interface de rede para torná-lo único.
- [ ] Um endereço IPv4 contém 8 octetos.
- [x] Um esquema de endereçamento IPv4 é hierárquico.

✅ RESPOSTAS CORRETAS: IPv4 é um esquema de endereçamento lógico. / Um esquema de endereçamento IPv4 é hierárquico.

---

### Pergunta 10

Considere o grupo de cinco endereços IPv4 cada um com a máscara de sub-rede 255.255.255.0. Quais dois endereços IPv4 pertencem à mesma rede local? (Escolha duas.)

- [ ] 193.168.10.16
- [x] 192.168.10.2
- [ ] 192.168.100.62
- [ ] 192.167.10.74
- [x] 192.168.10.56

✅ RESPOSTAS CORRETAS: 192.168.10.2, 192.168.10.56

---

### Pergunta 11

O grupo de TI precisa projetar e implantar a conectividade de rede IPv4 em um novo laboratório de informática do ensino médio. O projeto de rede requer que várias redes lógicas sejam implantadas em uma rede física. Qual tecnologia é necessária para permitir que computadores em redes lógicas diferentes se comuniquem?

- [ ] mapeamento
- [x] roteamento
- [ ] hospedagem
- [ ] comutação

✅ RESPOSTA CORRETA: roteamento