
# 19.0 Introdução

## 19.0.1 Webster - Por que devo fazer este módulo?

Ao planejar a rede futura, Bob acredita que Marcy e Vincent devem aproveitar os serviços em nuvem e a virtualização. Bob explicou que eles podem alugar serviços de um provedor de nuvem. Marcy e Vincent queriam saber por que deveriam considerar isso. Bob explica que isso consumirá menos energia, exigirá menos equipamento e menos espaço. Também pode ajudar na recuperação de desastres. Ele compara isso com as fotos de Marcy e Vincent em seus telefones celulares sendo copiadas para uma nuvem. Mesmo que o celular seja danificado, as fotos ainda podem ser recuperadas.

Você consegue pensar em como usa a nuvem? Quanto você sabe sobre a nuvem e a virtualização? Deixe-me ajudá-lo a aprender mais. Aproveite este módulo!

## 19.0.2 O Que Vou Aprender Neste Módulo?

**Titulo do Módulo:** Nuvem e virtualização

**Objetivo do Módulo:** Explicar as características da virtualização e dos serviços em nuvem.

| Título do Tópico          | Objetivo do Tópico                                              |
| ------------------------- | --------------------------------------------------------------- |
| Nuvem e Serviços de Nuvem | Explicar as características das nuvens e dos serviços em nuvem. |
| Virtualização             | Explicar o propósito e as características da virtualização.     |

# 19.1 Nuvem e Serviços de Nuvem

## 19.1.1 Vídeo - Nuvem e Virtualização

Em geral, quando falamos de nuvem, estamos falando de três coisas: data centers, computação em nuvem ou serviços em nuvem, e virtualização ou computação virtual.

Embora os data centers possam ser menores, geralmente são grandes instalações que demandam grande quantidade de energia, resfriamento e largura de banda. Apenas organizações muito grandes como Facebook ou Google podem se dar ao luxo de construir seus próprios data centers privados para prestar serviços aos seus usuários. Outras organizações menores alugam espaço em um datacenter. Provedores de serviços em nuvem como Cisco, Amazon Web Services ou Microsoft Azure oferecem seus serviços fora de datacenters.

Existem dois tipos básicos de nuvens: nuvens públicas e nuvens privadas. Nuvens públicas oferecem serviços e aplicativos à população em geral. Já as nuvens privadas destinam-se a organizações ou entidades específicas, como os governos, e são acessadas apenas por essas organizações privadas.

Existem diferentes categorias de serviços em nuvem. SaaS, ou Software como Serviço, refere-se a software sob demanda ou um modelo de assinatura onde a licença e a entrega do software acontece por meio da nuvem. Você verá isso em coisas como o Office 365 ou Adobe Creative Cloud, ou mesmo softwares de jogos de computador em que o acesso ao software acontece normalmente através de um navegador web. O software normalmente não é comprado, mas sim alugado. PaaS, ou Plataforma como Serviço, é onde o provedor de serviços em nuvem fornece a plataforma, como a plataforma Java ou .Net, para um desenvolvedor desenvolver um aplicativo. Isso muitas vezes envolve fornecer bancos de dados e ferramentas para o desenvolvedor para que eles possam desenvolver rapidamente um aplicativo. Infraestrutura como Serviço refere-se à virtualização da computação que pode ser fornecida pela internet sob demanda. Isso inclui computação virtual, como servidores virtuais, bem como armazenamento virtualizado e recursos de rede virtualizados que podem ser provisionados, alocados e fornecidos sob demanda com base nas necessidades.

A virtualização é a capacidade de abstrair ou separar o sistema operacional do hardware físico. Para criar um computador virtual, o hardware físico dedicado precisa ser compartilhado com o computador virtual. Isso é feito através de um hipervisor.

Existem dois tipos de hipervisores usados na virtualização. Um hypervisor tipo um, conhecido como hypervisor bare metal, e um hypervisor tipo dois, conhecido como hypervisor hospedado. Um hypervisor bare metal tipo um é um servidor de virtualização onde o hipervisor é um sistema operacional instalado diretamente no hardware. Depois disso, os computadores virtuais podem ser criados. Existem diferentes tipos de hipervisores tipo um: KVM, Red Hat Enterprise Virtualization, Xen, Citrix XenServer, VMware ESXi, VMware vSphere e Microsoft Hyper-V. Um hypervisor tipo dois é conhecido como hypervisor hospedado. Nesta situação, o hypervisor é um aplicativo ou programa instalado no topo do sistema operacional do host. Exemplos incluem Virtualbox, VMware Workstation, Parallels e Virtual PC. Você instala o Virtualbox, por exemplo, no topo do sistema operacional Windows, e então pode criar computadores virtuais.

Além da computação virtual, também é possível virtualizar switching e roteamento. Os computadores virtuais podem ser conectados em rede com um switch virtual, como o Cisco Nexus 1000V, que traz o poder de um switch Cisco para o ambiente de rede virtualizado.

## 19.1.2 Tipos de Nuvens

Existem quatro modelos de nuvem principais:

- **Nuvens públicas** - Os aplicativos e serviços baseados em nuvem oferecidos em uma nuvem pública são disponibilizados à população em geral. Os serviços podem ser gratuitos ou oferecidos em um modelo de pagamento por uso, como o pagamento de armazenamento online. A nuvem pública usa a Internet para fornecer serviços.
- **Nuvens privadas** - Os serviços e aplicativos na nuvem disponibilizados em uma nuvem privada são indicados para entidades ou empresas específicas, como o governo. Uma nuvem privada pode ser configurada usando a rede privada de uma organização, embora isso possa ser caro para construir e manter. Uma nuvem privada também pode ser gerenciada por uma organização externa com segurança de acesso estrita.
- **Nuvens híbridas** - Uma nuvem híbrida é composta de duas ou mais nuvens (exemplo: parte privada, parte pública), onde cada parte permanece um objeto separado, mas ambas são conectadas usando uma única arquitetura. Indivíduos em uma nuvem híbrida podem ter níveis de acesso a vários serviços baseados em direitos de acesso de usuário.
- **Nuvens comunitárias** - Uma nuvem comunitária é criada para uso exclusivo de uma comunidade específica. As diferenças entre nuvens públicas e comunitárias são as necessidades funcionais que foram personalizadas para a comunidade. Por exemplo, organizações de saúde devem manter a conformidade com políticas e leis (por exemplo, HIPAA) que exigem confidencialidade e autenticação especial.

## 19.1.3 Computação em Nuvem e Virtualização

Servidores dedicados

Os termos “computação em nuvem” e “virtualização” normalmente podem ser usados de forma intercambiável, no entanto, podem ter significados diferentes. A virtualização é a base da computação em nuvem. Sem ela, a computação em nuvem, como é mais implantada, não seria possível.

Cerca de uma década atrás, a VMware desenvolveu uma tecnologia de virtualização que permitiu a um sistema operacional servidor suportar um ou mais o sistemas operacionais clientes. A maioria das tecnologias de virtualização são baseadas, agora, nessa tecnologia. A transformação de servidores dedicados em servidores virtualizados foi adotada e está sendo feita rapidamente em data centers e em redes empresariais.

Virtualizar significa criar uma versão virtual, e não física, de um computador. Um exemplo seria a execução de um "computador Linux" no seu PC com Windows, que será feito posteriormente no laboratório.

Para aproveitar totalmente a virtualização, primeiro é necessário entender um pouco do histórico da tecnologia de servidor. Historicamente, os servidores corporativos consistiam em um sistema operacional de servidor, como Windows Server ou Linux Server, instalado em hardware específico, conforme mostrado na figura. Toda a RAM do servidor, poder de processamento e espaço no disco rígido foram dedicados ao serviço fornecido (por exemplo, web, serviços de e-mail, etc.).

![[Pasted image 20260614184042.png]]

O maior problema com essa configuração é que quando um componente falha, o serviço que é fornecido por esse servidor se torna indisponível. Isso é conhecido como um único ponto de falha. Outro problema era que os servidores dedicados eram subutilizados. Os servidores dedicados geralmente ficavam ociosos por longos períodos, aguardando até que houvesse uma necessidade do serviço específico que eles forneciam. Esses servidores desperdiçavam energia e ocupavam mais espaço do que o garantido pela quantidade de serviço prestado. Isso é conhecido como expansão de servidores.

## 19.1.4 Verifique sua compreensão - Nuvem e Serviços em Nuvem

### Pergunta 1

Qual modelo de nuvem representa duas ou mais nuvens em que cada parte permanece um objeto distinto, mas ambas são conectadas usando uma única arquitetura?

- [ ] nuvem pública
- [ ] nuvem privada
- [x] nuvem híbrida
- [ ] nuvem comunitária

✅ RESPOSTA CORRETA: nuvem híbrida

> O modelo de nuvem híbrida representa duas ou mais nuvens em que cada parte permanece um objeto distinto, mas ambas são conectadas usando uma única arquitetura.

---

### Pergunta 2

Nuvens criadas para atender às necessidades de uma indústria específica, como saúde ou mídia

- [ ] nuvem pública
- [ ] nuvem privada
- [ ] nuvem híbrida
- [x] nuvem comunitária

✅ RESPOSTA CORRETA: nuvem comunitária

> O modelo de nuvem da comunidade é usado para atender às necessidades de um setor específico, como assistência médica ou mídia.

---

### Pergunta 3

Qual dispositivo usa toda a RAM, a potência de processamento e o espaço no disco rígido dedicado a um serviço?

- [x] servidor dedicado
- [ ] dispositivo móvel
- [ ] máquina virtual
- [ ] servidor virtual

✅ RESPOSTA CORRETA: servidor dedicado

> Um servidor dedicado usa toda a RAM, poder de processamento e espaço em disco rígido dedicado a um serviço.


# 19.2 Virtualização

## 19.2.1 Vantagens da virtualização

Uma das principais vantagens da virtualização é o menor custo geral:

- **É necessário menos equipamento** - A virtualização permite a consolidação do servidor, o que requer menos dispositivos físicos e reduz os custos de manutenção.
- **Menos energia é consumida** - A consolidação de servidores reduz os custos mensais de energia e refrigeração.
- **Menos espaço é necessário** - A consolidação do servidor reduz a quantidade de espaço necessário.

São benefícios adicionais da virtualização:

- **Prototipagem mais fácil -** Laboratórios independentes, operando em redes isoladas, podem ser criados rapidamente para testes e implementações de prototipagem de rede.
- **Provisionamento de servidor mais rápido** - Criar um servidor virtual é muito mais rápido do que provisionar um servidor físico.
- **Maior tempo de atividade do servidor** - A maioria das plataformas de virtualização de servidor agora oferece recursos avançados de tolerância a falhas redundantes.
- **Recuperação de desastres aprimorada** - A maioria das plataformas de virtualização de servidores corporativos possui software que pode ajudar a testar e automatizar o failover antes que ocorra um desastre.
- **Suporte legado** - A virtualização pode estender a vida útil dos sistemas operacionais e aplicativos, proporcionando mais tempo para as organizações migrarem para soluções mais recentes.

## 19.2.2 Hipervisores
O hypervisor é um programa, firmware ou hardware que adiciona uma camada de abstração ao hardware físico. A camada de abstração é usada para criar máquinas virtuais que têm acesso a todo o hardware da máquina física, como CPUs, memória, controladores de disco e NICs. Cada uma dessas máquinas virtuais executa um sistema operacional completo e separado. Com a virtualização, não é incomum que 100 servidores físicos sejam consolidados como máquinas virtuais sobre 10 servidores físicos que usam hipervisores.


### **Hipervisor do Tipo 1 - Abordagem “Bare Metal”**

Os hypervisors Tipo 1, também são chamados de abordagem "bare-metal", pois o hypervisor é instalado diretamente no hardware. Os hypervisors Tipo 1 são geralmente usados em servidores corporativos e em dispositivos de rede de data center.

Com os hypervisors Tipo 1, o hypervisor é instalado diretamente no servidor ou no hardware de rede. Depois, as instâncias de um SO são instaladas no hypervisor, conforme mostrado na figura. Os hypervisors Tipo 1 têm acesso direto aos recursos de hardware e, portanto, são mais eficientes do que as arquiteturas hospedadas. Os hypervisors Tipo 1 melhoram a escalabilidade, o desempenho e a robustez.

![[Pasted image 20260614184338.png]]
### **Hipervisor do Tipo 2 - Abordagem “hospedada”**

Um hipervisor Tipo 2 é um software que cria e executa instâncias VM. O computador, em que um hypervisor oferece suporte a uma ou mais VMs, é um computador host. Os hypervisors Tipo 2 são também chamados hypervisors hospedados. Isso acontece porque o hypervisor está instalado no topo do SO atual, como Mac OS X, Windows ou Linux. Em seguida, uma ou mais instâncias de SO adicionais são instaladas no topo do hypervisor, conforme mostrado na figura. Uma grande vantagem dos hipervisores Tipo 2 é que o software do console de gerenciamento não é necessário.

**Observação**: É importante ter certeza de que a máquina de host seja robusta o suficiente para instalar e executar as VMs para que elas não fiquem sem recursos

![[Pasted image 20260614184350.png]]


## 19.2.3 Laboratório - Instale o Linux em uma máquina virtual e explore a GUI

Neste laboratório, você vai instalar um sistema operacional Linux em uma máquina virtual usando um aplicativo de virtualização de desktop, como o VirtualBox. Depois de concluir a instalação, você explorará a interface gráfica de usuário (GUI).

### Laboratório - Instalar o Linux em uma Máquina Virtual e Explorar a GUI

#### Objetivos

- Parte 1: Preparação de um computador para virtualização
- Parte 2: Instalar um sistema operacional Linux na máquina virtual
- Parte 3: Explorando a GUI

#### Histórico / Cenário

Os recursos e a capacidade de computação foram ampliados extraordinariamente nos últimos 10 anos. Um benefício dos processadores de vários núcleos e da grande quantidade de RAM é a capacidade de usar virtualização ou instalar diversos sistemas operacionais em um único computador.

Com a virtualização, um ou vários computadores virtuais podem funcionar em um computador físico. Os computadores virtuais executados dentro de computadores físicos são chamados de máquinas virtuais. As máquinas virtuais são chamadas normalmente de convidadas (guests), e os computadores físicos costumam ser chamados de hosts. Qualquer pessoa com um computador e um sistema operacional modernos pode executar máquinas virtuais.

Neste laboratório, você vai instalar um sistema operacional Linux em uma máquina virtual usando um aplicativo de virtualização de desktop, como o VirtualBox. Depois de concluir a instalação, você explorará a interface gráfica de usuário (GUI). Também vai explorar a interface de linha de comando usando esta máquina virtual em um laboratório posterior neste curso.

#### Recursos Necessários

- Computador com um mínimo de 2 GB de RAM e 10 GB de espaço livre em disco
- Acesso à Internet de alta velocidade para fazer download do Oracle VirtualBox e da imagem do sistema operacional Linux, como o Ubuntu Desktop

#### Instruções

##### Parte 1: Preparar um computador para a virtualização

Na Parte 1, você fará download e instalação do software de virtualização de desktop e de uma imagem do sistema operacional Linux. Essa imagem pode ser fornecida pelo instrutor.

###### Etapa 1: Download e Instalação do VirtualBox.

VMware Player e Oracle VirtualBox são dois programas de virtualização que você pode baixar e instalar para executar o arquivo de imagem do sistema operacional. Neste laboratório, você usará o aplicativo VirtualBox.

a. Navegue até https://www.VirtualBox.org/. Clique no link download nesta página.

b. Escolha e baixe o arquivo de instalação apropriado para o seu sistema operacional.

c. Depois que o arquivo de instalação do VirtualBox for baixado, execute o instalador e aceite as configurações padrão de instalação.

###### Etapa 2: Download de uma Imagem do Linux.

a. Acesse o site do Ubuntu em http://www.Ubuntu.com. Clique no link download nesta página para baixar e salvar uma imagem do Ubuntu Desktop.

###### Etapa 3: Crie uma Nova Máquina Virtual.

a. Clique em Start (Iniciar) e procure Virtualbox. Clique em Oracle VM VirtualBox para abrir o gerenciador. Quando ele estiver aberto, clique em New (Novo) para iniciar a instalação do Ubuntu.

b. Na tela Name and operating system (Nome e sistema operacional), digite Ubuntu no campo Name (Nome). No campo Type (Tipo), selecione Linux. No campo Version (versão), selecione a versão de download correspondente. Clique em Avançar para continuar.

c. Na tela Memory size (Tamanho da memória), aumente a quantidade de RAM da máquina virtual, se desejar, desde que ela permaneça na área verde. Ultrapassar esse limite afetaria negativamente o desempenho do host. Clique em Next (Avançar) para continuar.

d. Na tela Hard disk (Disco rígido), clique em Create a virtual hard disk now (Criar um disco rígido virtual agora).

e. Na tela Hard disk file type (Tipo de arquivo de disco rígido), use as configurações padrão de tipo de arquivo VDI (VirtualBox Disk Image). Clique em Avançar para continuar.

f. Na tela Storage on physical hard disk (Armazenamento em disco rígido físico), use as configurações padrão de armazenamento Dynamically allocated (Alocado dinamicamente). Clique em Avançar para continuar.

g. Na tela File location and size (Tamanho e local de arquivo), é possível ajustar o disco rígido e alterar o nome e o local do disco rígido virtual. Clique em Create (Criar) para usar as configurações padrão.

h. Quando a criação do disco rígido for concluída, a nova máquina virtual será listada na janela Oracle VM VirtualBox Manager (Gerenciador do Oracle VM VirtualBox). Selecione Ubuntu e clique em Start (Iniciar) no menu superior.

##### Parte 2: Instale o Ubuntu na Máquina Virtual.

###### Etapa 1: Monte a imagem.

a. Na janela Oracle VM Virtualbox Manager, clique com o botão direito em Ubuntu e selecione Settings (Configurações). Na janela Ubuntu – Settings (Ubuntu – Configurações), clique em Storage (Armazenamento) no painel esquerdo. Clique em Empty (Vazio) no painel intermediário. No painel direito, clique no símbolo do CD e selecione o local do arquivo da imagem do Ubuntu. Clique em OK para continuar.

b. Na janela do Oracle VM VirtualBox Manager, clique em Start (Iniciar) no menu superior.

###### Etapa 2: Instale o S.O.

a. Na tela Welcome (Bem-vindo), você deverá escolher entre experimentar ou instalar o Ubuntu. A opção try não instala o S.O., ele executa o S.O. diretamente da imagem. Neste laboratório, você instalará o SO do Ubuntu nesta máquina virtual. Clique em Install Ubuntu (Instalar Ubuntu).

b. Siga as instruções na tela e forneça as informações necessárias quando solicitado.

> **Nota:** se você não estiver conectado à Internet, poderá continuar a instalar e ativar a rede mais tarde.

c. Como essa instalação do Ubuntu está em uma máquina virtual, é seguro apagar o disco e instalar o Ubuntu sem afetar o computador host. Selecione Erase disk and install Ubuntu (Apagar disco e instalar Ubuntu). A instalação do Ubuntu em um computador físico apagaria todos os dados no disco e substituiria o sistema operacional atual pelo Ubuntu. Clique em Install Now (Instalar agora) para iniciar a instalação.

d. Clique em Continue (Continuar) para apagar o disco e instalar o Ubuntu.

e. Na tela Quem é você?, forneça seu nome e escolha uma senha. Você pode usar o nome de usuário gerado ou digitar um nome diferente. Insira seu nome de usuário e senha. Se desejar, altere as outras configurações. Clique em Continuar.

f. O sistema operacional Ubuntu será instalado na máquina virtual. Isso levará alguns minutos. Quando a mensagem Installation is complete (instalação concluída) for exibida, retorne para a janela Oracle VM VirtualBox Manager. Clique com o botão direito em Ubuntu e selecione Settings (Configurações). Na janela Ubuntu – Settings (Ubuntu – Configurações), clique em Storage (Armazenamento) no painel esquerdo. Clique na imagem do Ubuntu montada no painel do meio. No painel direito, clique no símbolo de CD e clique em Remover Disco da Unidade Virtual. Clique em OK para continuar.

g. Na VM do Ubuntu, clique em Reiniciar Agora.

##### Parte 3: Explore a GUI

Nesta parte, você vai instalar as adições de convidado do VirtualBox e explorar a GUI do Ubuntu.

###### Etapa 1: Instale Adições de Convidado.

a. Faça login na máquina virtual do Ubuntu usando as credenciais de usuário criadas na fase anterior.

b. A janela do Ubuntu Desktop poderá ser menor do que o esperado. Isso acontece principalmente em vídeos de alta resolução. Clique em Device > Insert Guest Additions CD image… (Dispositivo > Inserir imagem do CD de Adições de Convidado) para instalar as Adições de Convidado. Isso permite mais funções, como alterar a resolução de tela na máquina virtual.

c. Clique em Run (Executar) para instalar as adições. Quando for solicitada uma senha, use a mesma senha usada para fazer logon. Clique em autenticar para continuar.

d. Se o computador não tiver sido conectado à Internet durante a instalação, clique em Devices > Network Settings (Dispositivos > Configurações de Rede) no menu do Oracle VirtualBox. Ative os adaptadores de rede e defina a configuração apropriada para conexões de rede conforme necessário. Clique em OK.

e. Quando a instalação das adições estiver concluída, reinicie a máquina virtual novamente. Clique no menu no canto superior direito e clique em Desligar. Clique em Restart (Reiniciar) para reiniciar o Ubuntu.

###### Etapa 2: Abra um navegador web.

a. Faça login no Ubuntu mais uma vez. Quando estiver conectado novamente, você poderá redimensionar a janela da máquina virtual.

b. Abra um navegador web. Dependendo da distribuição Linux, talvez seja necessário pesquisar um navegador da Web ou há um link para um navegador da Web que já está na área de trabalho.

c. Localize um emulador de terminal para acessar a interface de linha de comando. Você usará um emulador de terminal nos laboratórios posteriores.

d. Explore a distribuição Linux instalada e localize alguns aplicativos que você pode usar.

#### Perguntas para reflexão

Quais são as vantagens e as desvantagens de usar uma máquina virtual?

**Resposta:** Com uma máquina virtual, você pode testar novos aplicativos ou sistemas operacionais sem afetar o computador host. Também pode salvar o estado atual da máquina quando fechar a máquina virtual. Caso haja algum problema, você terá a opção de reverter a máquina virtual a um estado salvo anteriormente. Por outro lado, uma máquina virtual exige recursos de hardware do computador host, como espaço em disco rígido, RAM e capacidade de processamento.

# 19.3 Resumo de Nuvem e Virtualização

## 19.3.1 O que aprendi neste módulo?

### Nuvem e Serviços de Nuvem

Em geral, quando falamos sobre a nuvem, estamos falando sobre três coisas: data centers, computação ou serviços em nuvem e virtualização ou computação virtual. Os data centers geralmente são grandes instalações que fornecem grandes quantidades de energia, refrigeração e largura de banda. Somente empresas muito grandes podem arcar com seus próprios data centers. A maioria das empresas menores aluga os serviços de um provedor de nuvem.

Os serviços em nuvem incluem o seguinte:

- **SaaS** – Software como serviço
- **PaaS** – Plataforma como serviço
- **IaaS** – Infraestrutura como serviço

Existem quatro modelos primários de nuvem, conforme mostrado na figura:

- **Nuvens públicas** – As aplicações e os serviços em nuvem oferecidos em uma nuvem pública são disponibilizados à população em geral.
- **Nuvens privadas** – os serviços e aplicativos na nuvem disponibilizados em uma nuvem privada são indicados para entidades ou empresas específicas, como o governo.
- **Nuvens híbridas** – Uma nuvem híbrida é composta de duas ou mais nuvens, onde cada parte permanece um objeto separado, mas ambas são conectadas usando uma única arquitetura.
- **Nuvens Comunitárias** – Uma nuvem da comunidade é criada para uso exclusivo por uma comunidade específica. As diferenças entre nuvens públicas e comunitárias são as necessidades funcionais que foram personalizadas para a comunidade.

A virtualização é a base da computação em nuvem. Sem ela, a computação em nuvem, como é mais implantada, não seria possível. Virtualizar significa criar uma versão virtual, e não física, de um computador. Um exemplo seria executar um "computador Linux" no seu PC Windows.

---

### Virtualização

Uma das principais vantagens da virtualização é o menor custo geral:

- **Menos equipamentos são requeridos** – A virtualização permite a consolidação do servidor, o que requer menos dispositivos físicos e reduz os custos de manutenção.
- **Menor consumo de energia** – A consolidação de servidores diminui o consumo mensal de energia e os custos de refrigeração.
- **Menos espaço requerido** – A consolidação do servidor reduz a quantidade de espaço necessário.

São benefícios adicionais da virtualização:

- **Prototipagem mais simples** – Laboratórios independentes, que operam em redes isoladas, podem ser criados rapidamente para implantações de testes e prototipagem de rede.
- **Provisionamento de servidor mais rápido** – Criar um servidor virtual é muito mais rápido que provisionar um servidor físico.
- **Maior tempo de atividade de servidor** – A maioria das plataformas de virtualização de servidor agora oferece recursos avançados de tolerância a falhas e redundância.
- **Recuperação de desastres aprimorada** – A maioria das plataformas de virtualização de servidores corporativos possui software que pode ajudar a testar e automatizar o failover antes que ocorra um desastre.
- **Suporte legado** – A virtualização pode estender a vida útil dos sistemas operacionais e aplicativos, proporcionando mais tempo para as organizações migrarem para soluções mais recentes.

O hypervisor é um programa, firmware ou hardware que adiciona uma camada de abstração ao hardware físico. A camada de abstração é usada para criar máquinas virtuais que têm acesso a todo o hardware da máquina física, como CPUs, memória, controladores de disco e NICs. Cada uma dessas máquinas virtuais executa um sistema operacional completo e separado.

Os hypervisors Tipo 1, também são chamados de abordagem "bare-metal", pois o hypervisor é instalado diretamente no hardware. Os hypervisors Tipo 1 são geralmente usados em servidores corporativos e em dispositivos de rede de data center.

Um hipervisor Tipo 2 é um software que cria e executa instâncias VM. O computador, em que um hypervisor oferece suporte a uma ou mais VMs, é um computador host. Os hypervisors Tipo 2 são também chamados hypervisors hospedados. Isso acontece porque o hypervisor está instalado no topo do SO atual, como Mac OS X, Windows ou Linux. Em seguida, uma ou mais instâncias de SO adicionais são instaladas sobre o hypervisor. Uma grande vantagem dos hipervisores Tipo 2 é que o software do console de gerenciamento não é necessário.

## 19.3.2 Webster - Questões para Reflexão

Por enquanto, Bob está sugerindo que Marcy e Vincent usem a nuvem para armazenamento de dados. Eles entendem que é um serviço de assinatura, mas permitirá que eles mantenham seus dados com mais segurança e será mais barato do que comprar seu próprio armazenamento de dados e servidor. Como você já sabe, há muitos outros serviços fornecidos pela nuvem. Marcy e Vincent podem, eventualmente, desejar alguns desses serviços também. Você já teve o disco rígido inativo e não conseguiu recuperar todos os arquivos? E se isso acontecesse com um computador ou até mesmo com um servidor na sua escola ou no seu trabalho? A sua escola ou rede de trabalho usa outros serviços em nuvem? Em caso afirmativo, você sabe quais são e por que foram selecionados? Se você estivesse na situação de Marcy e Vincent, quais serviços em nuvem você consideraria usar, além do armazenamento de dados?