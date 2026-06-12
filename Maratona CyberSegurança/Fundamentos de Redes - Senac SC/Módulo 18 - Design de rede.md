
# 18.0 Introdução

## 18.0.1 Webster - Por que devo fazer este módulo?

Deixe-me apresentá-lo ao meu amigo Bob! Bob trabalha na área de TI em Vancouver, no Canadá, e tem alguma experiência em redes. Ele está prestando consultoria para seus amigos, Marcy e Vincent, que compraram uma loja de móveis. Eles querem expandir suas operações físicas e se estabelecer na loja online também. Atualmente, a rede interna da loja lida com transações e estoque na loja. Marcy e Vincent querem adicionar câmeras de segurança, telefones VoIP e também expandi-la para incluir comércio eletrônico e remessa. Bob explica que isso vai ser mais caro do que seus amigos tinham previsto. Ele está pensando em projetar a futura rede para a loja de móveis. Ele explica que deve considerar a tolerância a falhas, a escalabilidade, o QoS e a segurança. Além disso, a rede atualmente é plana, não hierárquica. As redes hierárquicas são bem dimensionadas e acomodarão melhor esse negócio em crescimento.

Uau! Isso é muito para Marcy e Vincent entenderem. Eles não estão familiarizados com esses problemas de rede. E você? Aproveite este módulo para saber mais sobre redes confiáveis e design de rede hierárquica!

## 18.0.2 O que vou aprender neste módulo?

**Titulo do módulo:** Design de rede

**Módulo Objetivo:** Explicar os componentes de um projeto de rede hierárquica.

|Título do Tópico|Objetivo do Tópico|
|---|---|
|Redes confiáveis|Descrever os quatro requisitos básicos de uma rede confiável.|
|Projeto de rede hierárquica|Explicar a função em cada camada do modelo de design de rede de 3 camadas.|

# 18.1 Redes confiáveis

Você já esteve ocupado trabalhando on-line, e achou que "a internet caiu" ? Como você sabe até agora, a internet não caiu, você acabou de perder sua conexão com ela. Isso é muito frustrante. Com tantas pessoas no mundo confiando no acesso à rede para trabalhar e aprender, é imperativo que as redes sejam confiáveis. Nesse contexto, confiabilidade significa mais do que sua conexão à Internet. Este tópico se concentra nos quatro aspectos da confiabilidade da rede.

O papel da rede mudou de uma rede somente de dados para um sistema que permite a conexão de pessoas, dispositivos e informações em um ambiente de rede convergente rico em mídia. Para que as redes funcionem com eficiência e cresçam nesse tipo de ambiente, a rede deve ser construída sobre uma arquitetura de rede padrão.

As redes também suportam uma ampla gama de aplicativos e serviços. Elas devem operar sobre muitos tipos diferentes de cabos e dispositivos, que compõem a infraestrutura física. O termo arquitetura de redes, neste contexto, refere-se às tecnologias que apoiam a infraestrutura e os serviços programados e as regras, ou protocolos, que movimentam os dados na rede.

À medida que as redes evoluem, aprendemos que há quatro características básicas que os arquitetos de rede devem atender para atender às expectativas do usuário:

- Tolerância a falhas
- Escalabilidade
- Qualidade de serviço (QoS)
- Segurança


## 18.1.2 Vídeo - Tolerância a falhas

**Selecione o botão Reproduzir para assistir ao vídeo.**

Neste cenário, temos duas partes em nossa rede. Cada uma com seu próprio caminho para nosso ISP e a Internet. Pacotes originados no PC um são encaminhados para o Roteador A e para o ISP. Enquanto os pacotes provenientes do PC dois são encaminhados para o Roteador B e, em seguida, para o mesmo ISP.

Mas, o que acontece quando há um problema com o Roteador A, ou com um link usado no caminho para o Roteador A? Pacotes que precisam do roteador A para encaminhá-los para a Internet serão descartados, e não podem mais alcançar o destino final.

Uma rede tolerante a falhas é aquela que pode continuar suas operações, sem interrupção, quando um ou mais componentes da rede falham. Agora instalamos links adicionais em nossa rede, oferecendo múltiplos caminhos para alcançar nosso ISP e a Internet. Ter vários caminhos para um destino é conhecido como redundância, que é uma das formas de tornar a rede tolerante a falhas. Se um caminho falhar, os pacotes são automaticamente encaminhados usando um link diferente. Quanto mais redundância em uma rede, mais tolerante a falhas a rede se torna.


## 18.1.3 Tolerância a Falhas

Uma rede tolerante a falhas é aquela que limita o número de dispositivos afetados durante uma falha. Ela foi desenvolvida para permitir uma recuperação rápida quando ocorre uma falha. Essas redes dependem de vários caminhos entre a origem e o destino de uma mensagem. Se um caminho falhar, as mensagens serão instantaneamente enviadas por um link diferente. Ter vários caminhos para um destino é conhecido como redundância.

A implementação de uma rede comutada por pacotes é uma das maneiras pelas quais redes confiáveis fornecem redundância. A comutação de pacotes divide os dados do tráfego em pacotes que são roteados por uma rede compartilhada. Uma única mensagem, como um e-mail ou stream de vídeo, é dividido em vários blocos, chamados pacotes. Cada pacote tem as informações de endereço necessárias da origem e do destino da mensagem. Os roteadores na rede alternam os pacotes com base na condição da rede no momento. Isso significa que todos os pacotes em uma única mensagem podem seguir caminhos muito diferentes para o mesmo destino. Na figura, o usuário desconhece e não é afetado pelo roteador que está alterando dinamicamente a rota quando um link falha.

![[Pasted image 20260612185348.png]]

## 18.1.4 Escalabilidade

Uma rede escalável se expande rapidamente para oferecer suporte a novos usuários e aplicativos. Ela faz isso sem degradar o desempenho dos serviços que estão sendo acessados por usuários existentes. A figura mostra como uma nova rede é facilmente adicionada a uma rede existente. Essas redes são escaláveis porque os projetistas seguem padrões e protocolos aceitos. Isso permite que os fornecedores de software e hardware se concentrem em melhorar produtos e serviços sem precisar criar um novo conjunto de regras para operar na rede.

![[Pasted image 20260612185406.png]]

## 18.1.5 Qualidade de Serviço

A qualidade do serviço (QoS) é um requisito crescente das redes atualmente. Novos aplicativos disponíveis para usuários em redes, como transmissões de voz e vídeo ao vivo, criam expectativas mais altas em relação à qualidade dos serviços entregues. Você já tentou assistir a um vídeo com intervalos e pausas constantes? Conforme o conteúdo de vídeo, voz e dados convergem na mesma rede, o QoS se torna um mecanismo essencial para gerenciar os congestionamentos e garantir a entrega confiável do conteúdo para todos os usuários.

O congestionamento acontece quando a demanda por largura de banda excede a quantidade disponível. A largura de banda é medida pelo número de bits que podem ser transmitidos em um único segundo, ou bits por segundo (bps). Ao tentar uma comunicação simultânea pela rede, a demanda pela largura de banda pode exceder sua disponibilidade, criando um congestionamento na rede.

Quando o volume de tráfego é maior do que o que pode ser transportado pela rede, os dispositivos retêm os pacotes na memória até que os recursos estejam disponíveis para transmiti-los. Na figura, um usuário está solicitando uma página da Web e outro está em uma ligação. Com uma política de QoS configurada, o roteador é capaz de gerenciar o fluxo do tráfego de voz e de dados, priorizando as comunicações por voz se a rede ficar congestionada. O foco do QoS é priorizar o tráfego sensível ao tempo. O tipo de tráfego, e não o conteúdo, é o que é importante.

![[Pasted image 20260612185420.png]]

## 18.1.6 Segurança de rede

A infraestrutura da rede, os serviços e os dados contidos nos dispositivos conectados à rede são recursos pessoais e comerciais críticos. Os administradores de rede devem abordar dois tipos de preocupações de segurança de rede: segurança da infraestrutura de rede e segurança da informação.

Proteger a infraestrutura de rede inclui proteger fisicamente os dispositivos que fornecem conectividade de rede e impedir o acesso não autorizado ao software de gerenciamento que reside neles, conforme mostrado na figura.

![[Pasted image 20260612185431.png]]