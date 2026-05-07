# 1.0 Introdução

## 1.0.1 Por que devo cursar este módulo?

## 1.0.2 O que vou aprender neste módulo?
| Título do Tópico                        | Objetivo do Tópico                                                                                                         |
| --------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Redes afetam nossas vidas**           | Explicar como as redes afetam nossas vidas diárias.                                                                        |
| **Componentes de rede**                 | Explicar como os dispositivos de host e de rede são usados.                                                                |
| **Representações e topologias de rede** | Explicar representações de rede e como elas são usadas na rede topologias.                                                 |
| **Tipos comuns de redes**               | Comparar as características de tipos comuns de redes.                                                                      |
| **Conexões com a Internet**             | Explicar como LANs e WANs se interconectam com a Internet.                                                                 |
| **Redes confiáveis**                    | Descrever os quatro requisitos básicos de uma rede confiável.                                                              |
| **Tendências das redes**                | Explicar como tendências como BYOD, colaboração on-line, vídeo e nuvem a computação está mudando a forma como interagimos. |
| **Segurança da rede**                   | Identificar algumas ameaças e soluções básicas de segurança para todas as redes.                                           |
| **O profissional de TI**                | Explicar oportunidades de emprego no campo de rede.                                                                        |
## 1.0.3 Baixe e instale o Packet Tracer

## 1.0.4 Vídeo - Introdução ao Cisco Packet Tracer

## 1.0.5 Packet Tracer - Exploração de modo lógico e físico

# 1.1 Redes afetam nossas vidas

## 1.1.1 Redes Conecte-nos
Entre todas as coisas essenciais para a existência humana, a necessidade de interagir com os outros está logo abaixo das nossas necessidades básicas. A comunicação é quase tão importante para nós quanto nossa dependência de ar, água, comida e abrigo.

No mundo de hoje, com o uso de redes, estamos conectados como nunca estivemos. Pessoas que têm ideias podem se comunicar instantaneamente com as demais para torná-las uma realidade. Novos acontecimentos e descobertas são conhecidos no mundo inteiro em questão de segundos. Indivíduos podem até mesmo se conectar e jogar com seus amigos separados por oceanos e continentes.

## 1.1.2 1.1.2 Vídeo - A experiência de aprendizado da Cisco Networking Academy

## 1.1.3 Não Há Limites
Os avanços nas tecnologias de redes são talvez as mudanças mais significativas no mundo hoje. Eles estão ajudando a criar um mundo em que fronteiras nacionais, distâncias geográficas e limitações físicas se tornem menos relevantes, apresentando obstáculos cada vez menores.

A internet mudou a maneira pela qual nossas interações sociais, comerciais, políticas e pessoais ocorrem. A natureza imediata das comunicações pela Internet incentiva a criação de comunidades globais. As comunidades globais permitem a interação social que é independente de localização ou fuso horário.

A criação de comunidades on-line para a troca de ideias e informações tem o potencial de aumentar as oportunidades de produtividade ao redor do mundo.

A criação da nuvem nos permite armazenar documentos e imagens e acessá-los em qualquer lugar, a qualquer hora. Portanto, quer estejamos em um trem, em um parque ou em pé no topo de uma montanha, podemos acessar facilmente nossos dados e aplicativos em qualquer dispositivo.

# 1.2 Componentes de rede
## 1.2.1 Funções do Host
Se você quiser fazer parte de uma comunidade online global, seu computador, tablet ou smartphone deve primeiro estar conectado a uma rede. Essa rede deve estar conectada à internet. Este tópico discute as partes de uma rede.

Todos os computadores que estão conectados a uma rede e participam diretamente da comunicação em rede são classificados como hosts. Os hosts podem ser chamados de dispositivos finais. Alguns hosts também são chamados de clientes. No entanto, o termo hosts refere-se especificamente a dispositivos na rede que recebem um número para fins de comunicação. Este número identifica o host dentro de uma rede específica. Este número é chamado de endereço IP. Um endereço identifica o host e a rede à qual host está conectado.

Servidores são computadores com software que lhes permite fornecer informações, como e-mail ou páginas da Web, para outros dispositivos finais na rede. Cada serviço exige um software de servidor separado. Por exemplo, um computador exige um software de servidor Web, para que possa prover serviços à rede. Um computador com software de servidor pode fornecer serviços simultaneamente a muitos clientes diferentes.

Como mencionado anteriormente, os clientes são um tipo de host. Os clientes têm software para solicitar a exibir as informações obtidas do servidor, conforme mostrado na figura.

![[Pasted image 20260316070109.png]]

Um exemplo de software cliente é um navegador, como Chrome ou FireFox. Um único computador pode também executar vários tipos de software cliente. Por exemplo, um usuário pode verificar o e-mail e visualizar uma página da Web enquanto troca mensagens instantâneas e ouve um fluxo de áudio. A tabela lista três tipos comuns de software de servidor.

| Tipo    | Descrição                                                                                                                                                                                               |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| E-mail  | O servidor que executa o software do servidor de e-mail. Clientes usam cliente de e-mail software, como o Outlook, para acessar o e-mail no servidor.                                                   |
| Web     | O servidor web executa o software do servidor web. Os clientes usam software de navegador, como o Windows Internet Explorer, para acessar páginas da web no servidor.                                   |
| Arquivo | O servidor de arquivos armazena arquivos corporativos e de usuário em um local central. Os dispositivos clientes acessam esses arquivos com software cliente, como o explorados de arquivos do Windows. |
## 1.2.2 Ponto a ponto
O software cliente e o servidor geralmente são executados em computadores separados, mas também é possível que um computador seja usado para ambas as funções ao mesmo tempo. Em pequenas empresas e em casas, muitos computadores funcionam como servidores e clientes na rede. Esse tipo de rede é chamado de rede ponto a ponto.
![[Pasted image 20260316071219.png]]


## 1.2.3 Dispositivos finais

Os dispositivos de rede com os quais as pessoas estão mais familiarizadas são dispositivos finais. Para distinguir um dispositivo final de outro, cada dispositivo final em uma rede tem um endereço. Quando um dispositivo final inicia uma comunicação, ele usa o endereço do dispositivo final de destino para especificar onde entregar a mensagem.

 Um dispositivo final é a origem ou o destino de uma mensagem transmitida pela rede.


## 1.2.4 Dispositivos intermediários
Dispositivos intermediários conectam os dispositivos finais individuais à rede. Eles podem conectar várias redes individuais para formar uma internetwork. Eles oferecem conectividade a asseguram que os dados fluam pela rede.

Esses dispositivos intermediários usam o endereço do dispositivo final de destino, em conjunto com as informações sobre as interconexões de rede, para determinar o caminho que as mensagens devem percorrer na rede. Exemplos dos dispositivos intermediários mais comuns e uma lista de funções são mostrados na figura.
![[Pasted image 20260316072205.png]]

## 1.2.5 Meios de rede
A comunicação transmite através de uma rede na mídia. A mídia fornece o canal pelo qual a mensagem viaja da origem ao destino.

As redes modernas usam principalmente três tipos de mídia para interconectar dispositivos, como mostrados na figura:
- **Fios de metal dentro de cabos** - Os dados são codificados em impulsos elétricos.
- **Fibras de vidro ou plásticos nos cabos (cabo de fibra óptica)** - Os dados são codificados em pulsos de luz.
- **Transmissão sem fio** - Os dados são codificados através da modulação de frequência específicas de ondas eletromagnéticas.
![[Pasted image 20260316072950.png]]

## 1.2.6 Verifique sua compreensão - componentes de rede
