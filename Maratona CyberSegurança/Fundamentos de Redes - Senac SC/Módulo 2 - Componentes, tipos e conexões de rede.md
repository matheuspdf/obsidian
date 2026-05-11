# 2.1 Clientes e Servidores
## 2.1.1 Vídeo - Clientes e Servidores
### Clientes e Servidores

Em redes modernas, um host pode atuar como **cliente**, **servidor** ou **ambos**. O software instalado no computador determina a sua função.

---

#### Servidores

Servidores são hosts com softwares instalados que lhes permitem **fornecer informações** para outros hosts na rede, como e-mail ou páginas Web. Cada serviço de servidor requer um **software de servidor separado**.

#### Clientes

Clientes são hosts que possuem softwares instalados que permitem **solicitar e exibir** as informações obtidas do servidor.

---

#### Exemplos

**Navegador Web**

- Software cliente: Chrome, Edge, Safari, Firefox
- O cliente solicita a página Web ao servidor
- O servidor Web responde com a página Web

**E-mail**

- Software cliente: Microsoft Outlook
- O cliente acessa o e-mail no servidor
- O cliente pode enviar e receber mensagens do servidor de e-mail


## 2.1.2 Funções de Clientes e Servidores
Todos os computadores conectados a uma rede que participam diretamente na comunicação de rede são classificados como hosts. Os hosts podem enviar e receber mensagens na rede. Nas redes modernas, um host pode atuar como cliente, servidor ou ambos. O software instalado no computador determina qual função o computador desempenha.
![[Pasted image 20260509220151.png]]

**Servidores** são hosts que têm um software instalado que os permite fornecer informações, como e-mail ou páginas Web, a outros hosts na rede. Cada serviço exige um software de servidor separado. Cada destino que você acessa on-line é fornecido por um servidor localizado em algum lugar de uma rede conectada à Internet global.

**Clientes** são computadores host que têm um software instalado que os permite solicitar e exibir as informações obtidas do servidor. Um exemplo de software cliente é um navegador da Web, como Internet Explorer, Safari, Mozilla Firefox ou Chrome.

|Tipo|Descrição|
|---|---|
|**E-mail**|O servidor executa o software do servidor de e-mail. Clientes usam um software de e-mail, como o Microsoft Outlook, para acessar e-mails no servidor.|
|**Web**|O servidor web executa o software do servidor web. Os clientes usam navegadores, como o Windows Internet Explorer, para acessar páginas da Web no servidor.|
|**Arquivo**|O servidor de arquivos armazena arquivos corporativos e de usuário em um local central. Os dispositivos clientes acessam esses arquivos com softwares clientes, como o Windows Explorer.|

## 2.1.3 Redes Ponto-a-Ponto

Os softwares de cliente e de servidor geralmente são executados em computadores separados, mas também é possível que um computador execute as duas funções ao mesmo tempo. Em pequenas empresas e em casas, muitos computadores funcionam como servidores e clientes na rede. Esse tipo de rede é chamado de rede ponto a ponto(P2P).

A rede ponto-a-ponto mais simples consiste em dois computadores diretamente conectados por uma conexão com ou sem fio. Ambos os computadores podem usar essa rede simples para trocar dados e serviços entre si, atuando como cliente ou servidor conforme necessário.

Vários PCs também podem ser conectados para criar uma rede ponto-a-ponto maior, mas isso exige um dispositivo de rede (como um switch) para interconectar os computadores.

A principal desvantagem de um ambiente ponto-a-ponto é que o desempenho de um host pode ser reduzido se ele estiver atuando como cliente e servidor ao mesmo tempo. A figura lista algumas das vantagens e desvantagens das redes ponto-a-ponto.

Em empresas de grande porte, devido ao potencial para quantidades altas de tráfego de rede, geralmente é necessário ter servidores dedicados para suportar o número de solicitações de serviço.

As vantagens e desvantagens das redes P2P são resumidas na figura.
![[Pasted image 20260509221000.png]]

## 2.1.4 Aplicações Ponto-a-ponto

Um aplicação P2P permite que um dispositivo atue como cliente e servidor na mesma comunicação, como mostra a figura. Nesse modelo, todo cliente é um servidor e todo servidor é um cliente. Aplicações P2P exigem que cada dispositivo final forneça uma interface de usuário e execute um serviço em segundo plano.

Algumas aplicações P2P utilizam um sistema híbrido no qual o compartilhamento de recursos é descentralizado, mas os índices que apontam para as localizações de recursos são armazenados em um diretório centralizado. Em um sistema híbrido, cada peer acessa um servidor de índice para obter a localização de um recurso armazenado em outro peer.

![[Pasted image 20260509221203.png]]

## 2.1.5. Múltiplas Funções na Rede

Um computador com software de servidor pode fornecer serviços simultaneamente a um ou vários clientes, como mostrado na figura.

Além disso, um único computador pode executar vários tipos de software de servidor. Em casa ou em uma empresa pequena, pode ser necessário que um computador atue como um servidor de arquivos, um servidor Web e um servidor de e-mail.

Um único computador pode também executar vários tipos de software cliente. Deve haver um software cliente para cada serviço necessário. Com vários softwares cliente instalados, um cliente pode se conectar a vários servidores ao mesmo tempo. Por exemplo, um usuário pode verificar e-mails e exibir uma página Web enquanto envia mensagens instantâneas e ouve rádio pela Internet.
![[Pasted image 20260509221244.png]]

## 2.1.6 Verifique sua compreensão - Clientes e Servidores

**Verifique sua compreensão sobre Clientes e Servidores escolhendo a resposta correta para as seguintes perguntas.**

#### Quiz — Clientes e Servidores

**P1** Um computador com software instalado para fornecer informações como e-mail ou páginas da Web para outros dispositivos é conhecido como:

- [x] **servidor**
- [ ] smartphone
- [ ] host inteligente
- [ ] cliente

> Servidores são hosts que têm um software instalado que os permite fornecer informações, como e-mail ou páginas Web, a outros hosts na rede.

---

**P2** Um smartphone usa um software de navegador da Web para solicitar e exibir uma página da Web. O smartphone é considerado que tipo de computador?

- [ ] host inteligente
- [ ] solicitante
- [ ] servidor
- [x] **cliente**

> Clientes são computadores host que têm um software instalado que os permite solicitar e exibir as informações obtidas do servidor.

---

**P3** Uma rede em que dois computadores estão se comunicando como cliente e como servidor é conhecida como:

- [ ] rede cliente-cliente
- [ ] rede cliente-servidor
- [ ] rede servidor-servidor
- [x] **rede ponto-a-ponto**

> Uma rede ponto-a-ponto consiste de dois computadores diretamente conectados onde ambos são capazes de trocar dados e serviços com o outro, agindo como cliente ou servidor quando necessário.

## 2.2 Componentes de rede

## 2.2.1 Vídeo - Símbolos de infraestrutura de rede

### Dispositivos Intermediários

|Símbolo|Dispositivo|
|---|---|
|🔀|Roteador|
|📡|Roteador sem fio|
|🔲|Switch|
|📶|Ponto de acesso sem fio|

### Dispositivos Finais

|Símbolo|Dispositivo|
|---|---|
|💻|Laptop|
|🖨️|Impressora|
|📱|Smartphone|
|☎️|Telefone IP|

### Mídias de Rede

|Mídia|Descrição|
|---|---|
|**LAN**|Rede local — mais comumente uma LAN Ethernet|
|**WAN**|Rede de longa distância — usada para comunicações de provedores de serviços de Internet (ISP)|
|**Sem fio**|Mídia de transmissão wireless|
|**Nuvem**|Representa outra rede ou a Internet|