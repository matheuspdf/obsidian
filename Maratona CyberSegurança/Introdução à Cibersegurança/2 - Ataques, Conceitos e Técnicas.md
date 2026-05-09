## 2.1 Analisando um ataque cibernético
### 2.1.1 Tipos de Malware
Os criminosos digitais usam muitos tipos diferentes de software mal-intencionado, ou malware, para realizar suas atividades. Abreviação de “Malicious Software” (software mal-intencionado), o malware é qualquer código que pode ser usado para roubar dados, ignorar controles de acesso, causar danos  ou comprometer um sistema. Saber quais são os diferentes tipos e como eles se espalham é fundamental para contê-los e removê-los.

## Tipos de Malware

| Tipo                   | Descrição                                                                                                                                                  | Observação                                                                                                                     |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| 🕵️ **Spyware**        | Monitora sua atividade on-line, registra teclas pressionadas e captura dados confidenciais (como dados bancários), modificando configurações de segurança. | Frequentemente se junta a softwares legítimos ou cavalos de Troia.                                                             |
| 📢 **Adware**          | Instalado junto a versões de software, exibe anúncios automaticamente — geralmente pop-ups no navegador.                                                   | É comum vir acompanhado de spyware.                                                                                            |
| 🚪 **Backdoor**        | Obtém acesso não autorizado ignorando autenticação normal, permitindo ao invasor acesso remoto a recursos e comandos do sistema.                           | Funciona em segundo plano e é difícil de detectar.                                                                             |
| 🔒 **Ransomware**      | Mantém o sistema ou dados presos — geralmente via criptografia — até que um pagamento seja feito.                                                          | Frequentemente disseminado por e-mails de phishing com anexos maliciosos.                                                      |
| 😱 **Scareware**       | Usa táticas de medo para induzir o usuário a executar um programa, exibindo alertas falsos de que o sistema está em risco.                                 | Ao concordar em executar o programa indicado, o sistema é infectado.                                                           |
| 🌿 **Rootkit**         | Modifica o sistema operacional para criar um backdoor, escalando privilégios e alterando arquivos de sistema para acesso remoto.                           | Modifica ferramentas de monitoramento, tornando-se muito difícil de detectar. Geralmente exige formatação completa.            |
| 🦠 **Vírus**           | Programa que, ao ser executado, se replica e anexa seu código a outros arquivos. Pode ser ativado em hora/data específica.                                 | Pode ser inofensivo (exibir imagem) ou destrutivo (apagar dados). Espalha-se via USB, discos, rede ou e-mail.                  |
| 🐴 **Cavalo de Troia** | Malware que se disfarça de software legítimo para enganar o usuário, explorando seus privilégios. Comum em imagens, áudios e jogos.                        | Diferente dos vírus, **não se replica** automaticamente — age como engodo.                                                     |
| 🪱 **Worms**           | Se replica e se espalha de computador em computador **sem precisar de um programa host** e sem interação do usuário.                                       | Exploram vulnerabilidades do sistema e causam danos massivos — um worm infectou mais de 300.000 servidores em 19 horas (2001). |

### 2.1.2 Sintomas de Malware
Independentemente do tipo de malware com o qual um sistema foi infectado, existem alguns sintomas comuns a serem observados. Entre eles estão:

- um aumento no uso da unidade de processamento central (CPU), o que torna o dispositivo mais lento
- o computador congela ou trava frequentemente
- Há uma diminuição na velocidade de navegação na Web.
- Existem problemas inexplicáveis com conexões de rede.
- arquivos modificados ou excluídos
- Há presença de arquivos, programas ou ícones de desktop desconhecidos.
- Processos ou serviços desconhecidos em execução
- Programas estão se desligando ou reconfigurando sozinhos.
- E-mails estão sendo enviados sem o conhecimento ou consentimento do usuário.

### 2.1.3 O que você acha?
## Tipos de Malware

| Definição                                                                                                                                           | Tipo           |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- |
| Malware projetado para rastrear sua atividade on-line e capturar seus dados                                                                         | **Spyware**    |
| Software que entrega anúncios automaticamente                                                                                                       | **Adware**     |
| Malware que mantém um sistema de computador cativo até que um pagamento seja feito ao invasor                                                       | **Ransomware** |
| Código mal-intencionado que anexa a programas legítimos e geralmente se espalha por unidades USB, mídia óptica, compartilhamentos de rede ou e-mail | **Vírus**      |
| Código malicioso que se replica de forma independente, explorando vulnerabilidades em redes                                                         | **Worms**      |

## 2.2. Métodos de infiltração
### 2.2.1 Engenharia social
Engenharia social – manipulação do indivíduo para executar ações ou divulgar informações confidenciais. Os engenheiros sociais frequentemente dependem da boa vontade das pessoas para ajudar, mas também miram nos pontos fracos. Por exemplo, um invasor ligará para um funcionário autorizado com um problema urgente que exija acesso imediato à rede e apelará para a vaidade, ganância ou invocação de autoridade do funcionário usando técnicas de remoção  de nome para obter esse acesso.

> [!example]- Pretexting 
> Isso ocorre quando um invasor liga para um indivíduo e mente para ele na tentativa de obter acesso a dados privilegiados. Por exemplo, fingir que precisa dos dados pessoais ou financeiros de uma pessoa para confirmar sua identidade.

> [!example]- Tailgating
> Isso ocorre quando um invasor segue rapidamente uma pessoa autorizada até um local físico seguro. 

> [!example]-  Algo por algo (Quid pro quo) 
> É quando um hacker solicita informações pessoais de uma pessoa em troca de algo, como um brinde gratuito.

### 2.2.2 Negação de Serviço
Os ataques de negação de serviço (DoS) são um tipo de ataque de rede que é relativamente simples de realizar, mesmo por um invasor não qualificado. Um ataque de negação de serviço (DoS) resulta em algum tipo de interrupção de serviço aos usuários, dispositivos ou aplicações.


> [!example]-  Quantidade esmagadora de tráfego
> Quando uma rede, host ou aplicativo recebe uma enorme quantidade de dados a uma taxa que não consegue processar. Isso causa uma desaceleração na transmissão ou resposta ou uma falha em um dispositivo ou serviço.

> [!example]- Pacotes Maliciosamente Formatados
> Um pacote é uma coleta de dados que flui entre uma fonte e um computador receptor ou aplicativo através de uma rede, como a Internet. Quando um pacote formatado de forma mal-intencionada é enviado, o receptor não será capaz de tratá-lo. 
> 
> Por exemplo, um invasor encaminha pacotes com erros que não podem ser identificados pelo aplicativo ou encaminha pacotes formatados incorretamente.


### 2.2.3 DoS Distribuída
Um ataque de negação de serviço distribuída (DDoS) é semelhante a um  ataque de negação de serviço (DoS), mas é proveniente de várias fontes coordenadas. Por exemplo:

- Um invasor cria uma rede (botnet) de hosts infectados chamados zumbis, que são controlados por sistemas de tratamento.
- Os computadores zumbis examinam e infectam constantemente mais hosts, criando mais zumbis.
- Quando está pronto, o hacker instrui os sistemas controlador para fazer com que o botnet de zumbis execute um ataque de negação de serviço distribuído (DDoS).


### 2.2.4 Botnet
Um computador bot normalmente é infectado por visitar um site, abrir um anexo de e-mail ou abrir um arquivo de mídia infectado. Uma botnet é um grupo de robôs (bots), conectados pela Internet, com a capacidade de ser controlado por um indivíduo ou grupo mal-intencionado. Ela pode ter dezenas de milhares, ou até centenas de milhares, de bots que normalmente são controlados por meio de um servidor de comando e controle.

Esses robôs podem ser ativados para distribuir malware, lançar ataques de DDoS, distribuir e-mail de spam ou executar ataques de senha de força bruta. Os cibercriminosos freqüentemente alugam botnets para terceiros para fins nefastos.

Muitas empresas. como a Cisco, força as atividades de rede por meio de filtros de tráfego de botnet para identificar qualquer local de botnet.

![[Pasted image 20260324203730.png]]
1. Os bots infectados tentam se comunicar com um host de comando e controle na Internet.
2. O filtro de botnet do Cisco Firewall é um recurso que detecta o tráfego proveniente de dispositivos infectados com o código mal-intencionado do botnet.
3. O serviço Cisco Security Intelligence Operations (SIO) na nuvem envia os filtros atualizados para o firewall, que corresponde ao tráfego de novos botnets conhecidos.
4. Os alertas são enviados à equipe de segurança interna da Cisco para notificá-los sobre os dispositivos infectados que estão gerando tráfego mal-intencionado, para que possam evitar, mitigar e corrigir esses problemas.


### 2.2.5 Ataques On-Path
Os invasores no caminho interceptam ou modificam as comunicações entre dois dispositivos, como um navegador e um servidor da Web, para coletar informações ou se passar por um dos dispositivos.

Esse tipo de ataque também é chamado de ataque **homem no meio** ou **homem no celular**.

> [!example]- MAN-IN-THE-MIDDLE (MITM)
> Um ataque de MitM acontece quando um criminoso digital assume o controle de um dispositivo sem o conhecimento do usuário. Com esse nível de acesso, o invasor pode interceptar e capturar informações do usuário antes de transmiti-las ao seu destino desejado. Esses tipos de ataques costumam ser usados para roubar informações financeiras.
> 
> Existem muitos tipos de malware que possuem recursos de ataque de MitM.

> [!example]- MAN-IN-THE-MOBILE (MITMO)
> Uma variação do man-in-middle, MitMo é um tipo de ataque usado para assumir o controle do dispositivo móvel de um usuário. Quando infectado, o dispositivo móvel é instruído a capturar informações confidenciais do usuário e enviá-las aos invasores. O ZeuS é um exemplo de pacote de malware com recursos MitMo. Ele permite que os invasores capturem silenciosamente as mensagens SMS de verificação de duas etapas enviadas aos usuários.


### 2.2.6 SEO Poisoning
Você provavelmente já ouviu falar em otimização de mecanismos de pesquisa ou SEO, que, em termos simples, visa melhorar o site de uma empresa para que obtenha maior visibilidade nos resultados dos mecanismos de pesquisa.

Mecanismos de pesquisa como o Google funcionam apresentando uma lista de páginas da Web para usuários com base em suas consultas de pesquisa. Essas páginas da Web são classificadas de acordo com a relevância de seu conteúdo.

Embora muitas empresas legítimas se especializem em otimizar sites para melhor posicioná-los, os invasores tiram proveito de termos de pesquisa populares e usam o SEO para empurrar sites maliciosos para posições mais altas nos resultados de pesquisa. Esta técnica é chamada de envenenamento de SEO.

O objetivo mais comum do envenenamento de SEO é aumentar o tráfego para sites maliciosos que podem hospedar malware ou tentar engenharia social.


### 2.2.7 Quebra de senha de acesso à rede WiFi
Você está aproveitando o almoço na cantina quando um colega se aproxima de você. Eles parecem angustiados.

Eles explicam que parecem não conseguir se conectar ao Wi-Fi público no telefone e perguntam se  você tem a senha de Wi-Fi privada em mãos para que possam verificar se o  telefone está funcionando.

> [!failure]- ❌ "Claro. É Xgff76dB."
> Incorreto — compartilhar a senha da rede privada com desconhecidos é uma falha de segurança grave.

> [!success]- ✅ "Mmm... Não tenho certeza se estamos autorizados a usar a rede Wi-Fi privada. Deixe-me falar com meu gerente primeiro."
> **Correto!** Esse colega pode estar realizando um ataque de engenharia social, manipulando você para fornecer a senha usada para proteger a rede sem fio privada da empresa. Nunca se é demasiadamente prudente - e, para responder corretamente, você ganhou alguns pontos de defensor. Muito bem!
> Os hackers têm outras técnicas nas mangas. Alguns usam **ataques de força bruta**, testando possíveis combinações de senhas para tentar adivinhar uma senha. Outros são capazes de identificar senhas não criptografadas ouvindo e capturando os pacotes enviados na rede. Isso é chamado de **sniffing de rede**. Se a senha for criptografada, o invasor ainda poderá revelá-la usando uma ferramenta de quebra de senha.

> [!failure]- ❌ "Sim, claro. Me dê seu telefone e eu vou colocá-lo para você."
> Incorreto — além de compartilhar a senha, manusear o dispositivo de outra pessoa representa um risco adicional.


### 2.2.8 Ataques de senha
Inserir um nome de usuário e senha é uma das formas mais populares de autenticação em um site. Portanto, descobrir a senha é uma maneira fácil para os criminosos digitais obterem acesso às informações mais importantes.

**Selecione os títulos  para descobrir mais sobre alguns dos ataques de segurança de senha comuns.**

> [!note]- Password spraying
> Essa técnica tenta obter acesso a um sistema ao “pulverizar” algumas senhas usadas com frequência em um grande número de contas. Por exemplo, um criminoso digital usa 'Password123' com muitos nomes de usuário antes de tentar novamente com uma segunda senha comumente usada, como 'qwerty'.
> Essa técnica permite que o criminoso não seja detectado ao evitar bloqueios de conta frequentes.

> [!note]- Ataque de dicionário
>Um hacker tenta sistematicamente cada palavra de um dicionário ou uma lista de palavras usadas com frequência como senha, na tentativa de invadir uma conta protegida por senha.

> [!note]- Ataques de força bruta
> A forma mais simples e mais usada de obter acesso a um site protegido por senha, os ataques de força bruta veem um invasor usando todas as combinações possíveis de letras, números e símbolos no espaço de senha até acertar.

> [!note]- Ataques de arco-íris
> As senhas em um sistema de computador não são armazenadas como texto sem formatação, mas como valores de hash (valores numéricos que identificam exclusivamente  os dados). Uma tabela do arco-íris é um grande dicionário de hashes pré-computados e as senhas das quais eles foram calculados.
> Ao contrário de um ataque de força bruta que precisa calcular cada hash, um ataque do arco-íris compara o hash de uma senha com os armazenados na tabela do arco-íris. Quando um invasor encontra uma correspondência, ele identifica a senha usada para criar o hash.

> [!note]- Interceptação de tráfego
> Essa técnica tenta obter acesso a um sistema ao “pulverizar” algumas senhas usadas com frequência em um grande número de contas. Por exemplo, um criminoso digital usa 'Password123' com muitos nomes de usuário antes de tentar novamente com uma segunda senha comumente usada, como 'qwerty'.
> Essa técnica permite que o criminoso não seja detectado ao evitar bloqueios de conta frequentes.


### 2.2.9. Tempos de Cracking
Parece que os hackers estão tentando de tudo para quebrar a senha Wi-Fi privada da Apollo. Precisamos garantir que a senha seja forte o suficiente para suportar o ataque!

Veja as seguintes senhas. Clique nos números para colocá-los  na ordem correta de acordo com quanto tempo você acha que um invasor levaria para quebrar cada um usando força bruta, em que 1 é o menor período de tempo e 4, o maior.




## 🔐 Desafio: Força das Senhas

Parece que os hackers estão tentando de tudo para quebrar a senha Wi-Fi privada da Apollo.
Precisamos garantir que a senha seja forte o suficiente para suportar o ataque!

Ordene as senhas abaixo **do menor para o maior tempo** que um invasor levaria para quebrá-las usando força bruta (1 = mais fácil, 4 = mais difícil).

---

> [!failure]- 1️⃣ — Senha mais fácil de quebrar
> **`Senha`**
> Palavra comum do dicionário, sem números ou símbolos. Quebrada em segundos.

> [!warning]- 2️⃣ — Fácil de quebrar
> **`3trawberry`**
> Palavra do dicionário com substituição simples de letra por número. Ainda vulnerável.

> [!example]- 3️⃣ — Moderadamente difícil
> **`K4km9n2R`**
> Combinação de letras maiúsculas, minúsculas e números. Mais resistente, mas sem símbolos.

> [!success]- 4️⃣ — Mais difícil de quebrar
> **`H $ 1gh # 7iD @ 3`**
> Combina letras maiúsculas e minúsculas, números, símbolos e espaços. Extremamente resistente a ataques de força bruta.

> [!note]
> **Isso mesmo! Você protegeu a senha do Wi-Fi privado da organização e ganhou mais alguns pontos de defensor — ótimo trabalho!**
> Realizar ataques de força bruta envolve o invasor tentando várias combinações possíveis na tentativa de adivinhar a senha. Esses ataques geralmente envolvem um arquivo de lista de palavras — um arquivo de texto contendo uma lista de palavras de um dicionário. Um programa como Ophcrack, L0phtCrack, THC Hydra, RainbowCrack ou Medusa tentará cada palavra e combinações comuns até encontrar uma correspondência. 
> Como os ataques de força bruta levam tempo, as senhas complexas levam muito mais tempo adivinhar.


### 2.2.10 Ameaças persistentes avançadas
Advanced Persistent Threat (APT) – uma operação multi-fase, longo prazo, furtiva e avançada contra um alvo específico. Por essas razões, um invasor geralmente não tem o conjunto de habilidades, os recursos ou a persistência para realizar APTs.

Devido à complexidade e ao nível de habilidade necessários para realizar esse ataque, um APT geralmente é bem financiado e normalmente tem como alvo organizações ou nações por motivos comerciais ou políticos.

Seu principal objetivo é implantar malware personalizado em um ou mais sistemas do alvo e permanecer lá sem ser detectado.

### 2.2.11 Agora é com você...
Ufa! Isso é muito difícil de entender e os hackers certamente têm muitas ferramentas à sua disposição. É importante que você saiba o que é isso para que possa se proteger e à @Apollo.

Você se lembra de algumas das atividades suspeitas que você viu recentemente na empresa. Com base no que você aprendeu neste tópico, que tipo de ataque pode ser cada um desses cenários? Não se apresse com esta. Você tem a chance de ganhar alguns pontos de defensor muito necessários.

**Selecione a resposta correta nas listas suspensas e depois envie.**

## 🧩 Identificação de Ataques

Associe cada situação ao tipo de ataque correto.

---

> [!failure]- ❓ No caminho para o escritório, uma pessoa que você nunca viu antes pede que você feche a porta — ela esqueceu o cartão de acesso.
> ✅ **Engenharia Social**
> O invasor manipula psicologicamente a vítima para obter acesso físico ao ambiente, sem usar nenhum recurso técnico.

> [!failure]- ❓ Você recebeu uma mensagem de erro ao acessar o computador: "Sua conexão foi interrompida. Uma alteração na rede foi detectada."
> ✅ **DoS (Denial of Service)**
> O ataque interrompeu a conexão de rede, impedindo o acesso normal ao sistema.

> [!failure]- ❓ Você pesquisou o site da @ Apollo no Google, mas ao clicar no resultado superior foi redirecionado para uma página que anuncia software antivírus.
> ✅ **Envenenamento de SEO**
> O invasor manipulou os resultados de busca para redirecionar usuários a sites maliciosos.



## # 2.3 Exploits e vulnerabilidade de segurança
### 2.3.1 Vulnerabilidades de Hardware

Vulnerabilidades de hardware são frequentemente introduzidas por falhas de projeto de hardware. Por exemplo, o tipo de memória chamado RAM  consiste basicamente em muitos capacitores (um componente que pode conter uma carga elétrica) instalados muito próximos um do outro. No entanto, logo foi descoberto que, devido à sua proximidade, as mudanças aplicadas a um desses capacitores poderiam influenciar os capacitores vizinhos. Com base nessa falha, foi criado um exploit chamado Rowhammer. Ao acessar (martelar) repetidamente uma linha de memória, a exploração do Rowhammer aciona interferências elétricas que eventualmente corrompem  os dados armazenados na RAM.

Meltdown e Spectre

Os pesquisadores de segurança do Google descobriram Meltdown e Spectre, duas vulnerabilidades de hardware que afetam quase todas as unidades de processamento central (CPUs) lançadas desde 1995 em desktops, laptops, servidores, smartphones,  dispositivos inteligentes e serviços em nuvem.

Os invasores que exploram essas vulnerabilidades podem ler toda a memória de um determinado sistema (Meltdown), bem como os dados manipulados por outras aplicações (Spectre). As explorações de vulnerabilidade Meltdown e Spectre são conhecidas como ataques de canal lateral (as informações são obtidas com a implementação de um sistema de computador). Eles têm a capacidade de comprometer grandes quantidades de dados de memória, porque os ataques podem ser executados várias vezes em um sistema com muito pouca possibilidade de uma falha ou outro erro.

As vulnerabilidades de hardware são específicas para modelos do dispositivo e geralmente não são exploradas por tentativas comprometedoras aleatórias. Embora as explorações de hardware sejam mais comuns em ataques altamente direcionados, a proteção contra malware tradicional e uma boa segurança física são proteção suficiente para o usuário comum.

### 2.3.2 Vulnerabilidades de Software
As vulnerabilidades de software geralmente são introduzidas por erros no sistema operacional ou no código do aplicativo.

**Selecione o logotipo para saber mais sobre a vulnerabilidade de SYNful Knock descoberta no Cisco Internetwork Operating System (IOS) em 2015.**

A vulnerabilidade SYNful Knock permitiu que os invasores ganhassem o controle de roteadores de nível empresarial, como os roteadores Cisco ISR antigos, dos quais poderiam monitorar toda a comunicação de rede e infectar outros dispositivos de rede.

Tal vulnerabilidade foi introduzida no sistema quando uma versão alterada do IOS foi instalada nos roteadores. Para evitar isso, sempre verifique a integridade da imagem do IOS baixada e limite o acesso físico do equipamento somente ao pessoal autorizado.


### 2.3.3 Categorizando as vulnerabilidades de software
A maioria das vulnerabilidades de segurança de software se enquadra em várias categorias principais.

> [!example]- Estouro de buffer
> Os buffers são áreas de memórias alocadas a um aplicativo. Uma vulnerabilidade ocorre quando os dados são gravados além dos limites de um buffer. Ao alterar os dados além dos limites de um buffer, o aplicativo pode acessar a memória alocada para outros processos. Isso pode levar a uma falha do sistema ou  comprometimento de dados ou fornecer escalonamento de privilégios.

> [!example]- Entrada não validada
> Os programas geralmente exigem entrada de dados, mas esses dados recebidos podem ter conteúdo malicioso, projetado para forçar o programa a se comportar de maneira não intencional.
> Por exemplo, considere um programa que recebe uma imagem para processamento. Um usuário mal-intencionado pode criar um arquivo de imagem com dimensões de imagem inválidas. As dimensões criadas de forma mal-intencionada podem forçar o programa a alocar buffers de tamanhos incorretos e inesperados.

> [!example]- Condição de corrida
> Esta vulnerabilidade descreve uma situação em que a saída de um evento depende de saídas ordenadas ou cronometradas. Uma condição de corrida se torna uma fonte de vulnerabilidade quando os eventos ordenados ou cronometrados necessários não ocorrem na ordem correta ou na sincronização apropriada.

> [!example]- Fragilidade nas práticas de segurança
> Sistemas e dados confidenciais podem ser protegidos por meio de técnicas como autenticação, autorização e criptografia. Os desenvolvedores devem manter o uso de técnicas de segurança e bibliotecas que já foram criadas, testadas e verificadas e não devem tentar criar seus próprios algoritmos de segurança. É provável que elas introduzam novas vulnerabilidades.

> [!example]- Problemas de controle de acesso
> O controle de acesso é o processo de controlar quem faz o quê e abrange desde o gerenciamento do acesso físico ao equipamento até ditar quem tem acesso a um recurso, como um arquivo, e o que pode ser feito com ele, como ler ou alterar o arquivo. Muitas vulnerabilidades de segurança são criadas com o uso indevido de controles de acesso.
> 
> Quase todos os controles de acesso e as práticas de segurança poderão ser superados se o invasor tiver acesso físico ao equipamento de destino. Por exemplo, não importa as configurações de permissão em um arquivo, um hacker pode ignorar o sistema operacional e ler os dados diretamente do disco. Para proteger a máquina e os dados que ela contém, o acesso físico deve ser restrito e as técnicas de criptografia devem ser usadas para proteger dados contra roubo ou danos.



### 2.3.4 Atualizações de software
O objetivo das atualizações de software é sempre estar atualizado e evitar a exploração de vulnerabilidades. A Microsoft, Apple  e outros fabricantes de sistemas operacionais lançam patches e atualizações quase todos os dias, e aplicativos como navegadores da web, aplicativos móveis e servidores da web são frequentemente atualizados pelas empresas ou organizações responsáveis ​​por eles.

Apesar de as empresas se esforçarem muito para encontrar e corrigir vulnerabilidades de software, novas vulnerabilidades são descobertas regularmente. Enquanto algumas empresas têm equipes de testes de penetração dedicadas para pesquisar, localizar e corrigir vulnerabilidades de software, antes que elas possam ser exploradas, os pesquisadores de segurança de terceiros também são especializados em descobrir essas vulnerabilidades.

O Project Zero do Google é um grande exemplo de tal prática. Depois de descobrir uma série de vulnerabilidades em vários softwares usados por usuários finais, o Google formou uma equipe permanente dedicada a encontrar vulnerabilidades de software. Você pode descobrir mais sobre a pesquisa de segurança do Google [aqui](https://bugs.chromium.org/p/project-zero/issues/list?can=1&redir=1).


### 2.3.5 O que você acha?
Isso fez você pensar sobre algumas das vulnerabilidades que podem existir no @Apollo. Após algumas investigações, você observou alguns possíveis problemas.

Você consegue identificar em qual categoria cada uma dessas vulnerabilidades se encaixa? Você tem  a chance de ganhar alguns pontos de defensor aqui e proteger ainda mais @Apollo , então tome seu tempo.

**Escolha a resposta correta em cada uma das opções e clique em Enviar.**

> [!failure]- ❓ Ao iniciar no @Apollo, sua senha de rede foi enviada para você em texto sem formatação e você não foi solicitado a alterá-la.
> ✅ **Fragilidade nas práticas de segurança**
> Senhas enviadas em texto puro e sem exigência de troca representam uma falha grave nas políticas de segurança da organização.

> [!failure]- ❓ Os funcionários antigos ainda têm acesso ao banco de dados de clientes da @Apollo.
> ✅ **Problemas de controle de acesso**
> Credenciais de ex-funcionários deveriam ser revogadas imediatamente após o desligamento para evitar acessos não autorizados.

> [!failure]- ❓ Novos usuários podem fazer login na conta @Apollo, mesmo que tenham se inscrito com um endereço de e-mail formatado incorretamente.
> ✅ **Entrada não validada**
> O sistema não verifica se os dados inseridos estão no formato correto, permitindo cadastros inválidos ou potencialmente maliciosos.

**Está correto! Ótimo trabalho!**

Você identificou corretamente os possíveis problemas de segurança e deu um passo mais perto de proteger @Apollo  de ataques. Lembre-se:

- Enviar informações confidenciais por e-mail, como senhas, em texto sem formatação é extremamente arriscado e é uma fraqueza na prática de segurança. Essas informações devem, no mínimo, ser criptografadas.
- Os funcionários antigos não deveriam ter acesso às informações do cliente ao deixarem uma empresa. Esse é um problema sério de controle de acesso.
- Novos usuários precisam ser validados antes que qualquer outra coisa possa ser feita com seus dados. Usar um endereço de e-mail formatado incorretamente para fazer logon é um erro de entrada não validado.

##  2.4 O Cenário da Cibersegurança
### 2.4.1 Criptomoeda
A criptomoeda é o dinheiro digital que pode ser usado para comprar produtos e serviços, usando técnicas de criptografia fortes para proteger transações on-line. Bancos, governos  e até mesmo empresas como a Microsoft e a AT&T estão muito cientes de sua importância e estão entrando na onda das criptomoedas!


## 💰 Como Funciona a Criptomoeda

---

> [!example]- 1️⃣ Carteiras e Transações
> Os proprietários de moedas criptografadas guardam seu dinheiro em **"carteiras" virtuais e criptografadas**. Quando uma transação ocorre entre os proprietários de duas carteiras digitais, os detalhes são registrados em um sistema de contabilidade descentralizado ou **blockchain**.
>
> Isso significa que é realizado com certo grau de anonimato e é autogerenciado, **sem interferência de terceiros**, como bancos centrais ou entidades governamentais.

> [!example]- 2️⃣ Mineração
> Aproximadamente a cada dez minutos, computadores especiais coletam dados sobre as últimas transações de criptomoeda, transformando-os em **quebra-cabeças matemáticos** para manter a confidencialidade.
>
> Essas transações são então verificadas através de um processo técnico e altamente complexo conhecido como **"mineração"**. Essa etapa normalmente envolve um exército de "mineradores" trabalhando em PCs avançados para resolver quebra-cabeças matemáticos e autenticar transações.

> [!example]- 3️⃣ Conclusão da Transação
> Uma vez verificado, o razão é atualizado e copiado e **disseminado eletronicamente em todo o mundo** para qualquer pessoa que pertence à rede blockchain, concluindo com eficiência uma transação. ✅

### 2.4.2 Cryptojacking
O cryptojacking é uma ameaça emergente que se esconde no computador, telefone celular, tablet, laptop ou servidor do usuário, usando os recursos dessa máquina para "extrair" moedas criptografadas sem o consentimento ou conhecimento do usuário .

Muitas vítimas de cryptojacking nem sabiam que tinham sido invadidas até que fosse tarde demais!

## 2.5. Questionário
