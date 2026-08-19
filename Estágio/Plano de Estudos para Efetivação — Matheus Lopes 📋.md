> Baseado nos pontos que seu chefe passou. Foco: **ver → entender → praticar**, 1 tópico por dia.

## Como usar este plano

Cada dia segue o mesmo formato:

- 🔎 **O que é** — explicação direta do conceito
- 🛠️ **Pratique hoje** — checklist de ações concretas (marque conforme for fazendo)
- ⏱️ **Tempo estimado**
- 💡 **Conexão com seu trabalho** — onde isso já aparece (ou pode aparecer) no seu dia a dia, quando fizer sentido

Reserve de 30 a 45 minutos por dia, de preferência sempre no mesmo horário. Se pular um dia, não tente compensar tudo de uma vez — só retome no seguinte. Fins de semana são bons pra revisar o que ficou menos claro.

## 🗺️ Visão geral do plano

| Dia | Semana | Código | Tema                                      |
| --- | ------ | ------ | ----------------------------------------- |
| 1   | 1      | 1.3    | Processo de resolução de problemas        |
| 2   | 1      | 2.2    | Ferramentas de diagnóstico do dispositivo |
| 3   | 1      | 2.3    | Portas e cabos                            |
| 4   | 1      | 2.4    | Componentes de desktop                    |
| 5   | 1      | 2.5    | Problemas comuns de hardware              |
| 6   | 2      | 3.1    | Acesso a recursos de rede                 |
| 7   | 2      | 3.2    | Conectividade de periféricos              |
| 8   | 2      | 3.3    | Conectividade básica de rede              |
| 9   | 2      | 4.1    | Problemas do Windows                      |
| 10  | 2      | 4.3    | Problemas em dispositivos móveis          |
| 11  | 3      | 4.4    | Virtualização e cloud                     |
| 12  | 3      | 4.5    | Problemas de aplicações                   |
| 13  | 3      | 5.1    | Ameaças de segurança                      |
| 14  | 3      | 5.2    | Engenharia social                         |
| 15  | 3      | 5.3    | Confidencialidade e políticas             |
| 16  | 4      | 6.1    | Acesso remoto                             |
| 17  | 4      | 6.2    | Pesquisa e documentação                   |
| 18  | 4      | 6.3    | Windows Server                            |
| 19  | 4      | —      | Revisão geral                             |
| 20  | 4      | —      | Preparar conversa com o chefe             |

---

## 📆 Semana 1 — Fundamentos de Diagnóstico e Hardware (Dias 1–5)

### Dia 1 — [1.3] Processo de resolução de problemas

🔎 **O que é:** o ciclo padrão de troubleshooting em TI:

1. Definir o problema
2. Coletar informações detalhadas
3. Identificar uma causa provável
4. Elaborar um plano de ação
5. Implementar as mudanças
6. Observar o resultado
7. Se não resolveu, repetir o ciclo
8. Documentar tudo o que foi feito

É o esqueleto por trás de praticamente todo atendimento que você já faz — a diferença é fazer isso de forma consciente e documentada.

🛠️ **Pratique hoje:**

- [ ] Escolha 1 chamado recente e reescreva-o seguindo os 8 passos acima
- [ ] No próximo chamado real de hoje, siga o processo conscientemente e anote cada etapa
- [ ] Identifique em qual etapa você costuma "pular" (ex: ir direto pra causa provável sem coletar informação suficiente)

⏱️ **Tempo estimado:** 30–40 min

💡 **Conexão com seu trabalho:** seus relatórios de BSOD e o checklist de remediação que você já produziu são exatamente esse processo documentado.

---

### Dia 2 — [2.2] Ferramentas de diagnóstico do dispositivo

🔎 **O que é:** ferramentas nativas do Windows pra levantar dados de um equipamento — hostname, hardware (processador, memória, disco), versão do SO, IPv4/IPv6, MAC address:

- Gerenciador de Tarefas
- Informações do Sistema (msinfo32)
- Visualizador de Eventos
- ipconfig
- WinDBG (análise de arquivos de dump, geralmente ligados a telas azuis/BSOD)

🛠️ **Pratique hoje:**

- [x] Na sua máquina, levante: hostname, modelo do processador, RAM total, espaço livre em disco, build do Windows, IPv4, MAC address
- [x] Rode `ipconfig /all` no cmd e identifique cada campo retornado
- [x] Abra o Visualizador de Eventos e localize um evento de erro recente
- [x] Se possível, abra um dump antigo no WinDBG só pra reconhecer a interface

⏱️ **Tempo estimado:** 30–45 min

💡 **Conexão com seu trabalho:** é basicamente o que o Action1 faz de forma centralizada e remota no seu `action1-desktop` — entender as ferramentas nativas ajuda a entender os dados que a API te devolve.

---
#### Resumo — Dia 2 [2.2] Ferramentas de diagnóstico do dispositivo

#### A lógica geral

Três ferramentas nativas do Windows respondem três perguntas diferentes sobre uma máquina:

| Ferramenta              | Pergunta que responde                            |
| ----------------------- | ------------------------------------------------ |
| Gerenciador de Tarefas  | "O que está rodando **agora**?"                  |
| `msinfo32`              | "Qual é a **configuração estática** da máquina?" |
| Visualizador de Eventos | "O que **aconteceu** (erros, histórico)?"        |

Juntas, elas formam o mesmo tipo de "perfil de dispositivo" que uma ferramenta de RMM (Remote Monitoring & Management) — como o **Action1** — coleta via agente e te entrega centralizado pela API.

---

#### Gerenciador de Tarefas (`Ctrl+Shift+Esc`)

Mostra o estado **atual** dos processos.

- **Aba Desempenho** → CPU, RAM total/em uso, disco, rede
- **Aba Detalhes** → visão por processo:
    - **PID** (Process ID) — identificador único enquanto o processo roda
    - **Nome de usuário** — quem é "dono" do processo (usuário comum vs `SISTEMA`/`SERVIÇO LOCAL`)
    - **CPU / Delta de memória** — consumo e variação (útil pra achar vazamento de memória)
    - **Plataforma** (32/64 bits)

**Diagnóstico de segurança**: clique direito → _Abrir local do arquivo_ pra conferir se o processo roda de um caminho confiável (`System32`, `Program Files`) ou suspeito (`AppData\Temp`).

**Múltiplas instâncias**: normal ver vários `brave.exe` ou `msedgewebview2.exe` — é arquitetura multiprocesso (cada aba/módulo roda separado).

---

#### `taskkill` — finalizar processo via terminal

```cmd
taskkill /PID <numero> /F
```

- `/PID` → especifica o processo pelo número (não é `/PDI`!)
- `/F` → força o encerramento
- `/IM nome.exe` → mata por nome (mata **todas** as instâncias)
- `/T` → mata o processo + toda a árvore de processos filhos
- `/S ip /U user /P senha` → executa em **máquina remota** (conceito por trás de RMMs)

Cuidado ao forçar encerramento de processos `SISTEMA`/`SERVIÇO LOCAL` — pode travar o Windows.

**Exemplos:**

```cmd
taskkill /PID 23304 /F
```

Mata o processo pelo PID, à força.

```cmd
taskkill /IM notepad.exe /F
```

Mata todas as instâncias do notepad.exe.

```cmd
taskkill /PID 22124 /F /T
```

Mata o processo e toda a árvore de processos filhos.

```cmd
taskkill /S 192.168.0.10 /U administrador /P senha /PID 4521 /F
```

Mata um processo em uma máquina remota (conexão → alvo → modificador).

---

#### Informações do Sistema (`msinfo32`)

Win+R → `msinfo32`

O "cadastro" fixo da máquina, tudo em uma tela:

- Nome do host
- Fabricante/modelo do sistema
- Processador
- RAM instalada
- Versão do BIOS
- Tipo de sistema (x64)

Dá pra exportar (Arquivo → Exportar) pra comparar com dados retornados por uma API de gestão remota.

---

#### Visualizador de Eventos (`eventvwr.msc`)

Win+R → `eventvwr.msc` → **Logs do Windows > Sistema** (ou **Aplicativo**)

- Filtrar por **Nível: Erro** (botão direito → Filtrar Log Atual)
- Anotar: **Event ID**, **Origem (Source)**, **Horário**
- Pesquisar o Event ID pra entender o significado (ex: Event ID 41 = Kernel-Power, geralmente desligamento inesperado)

**Técnica de correlação**: cruzar o horário de um problema (processo travado, app fechou sozinho) com o horário exato de um evento no log — essa é a habilidade central de diagnóstico.

---

#### `ipconfig`

No `cmd`:

```cmd
ipconfig /all
```

Campos principais:

- **Nome do Host**
- **Endereço IPv4 / IPv6**
- **Máscara de Sub-rede**
- **Gateway Padrão**
- **Endereço Físico** (MAC address)
- **Servidores DNS**
- **DHCP Habilitado** (Sim/Não)

Complementos via PowerShell:

```powershell
Get-ComputerInfo | Select WindowsProductName, WindowsVersion
Get-CimInstance Win32_Processor | Select Name
Get-CimInstance Win32_PhysicalMemory | Measure-Object Capacity -Sum
Get-PSDrive C | Select Used,Free
```

---

#### Exercício de fechamento (correlação prática)

1. Abrir o Bloco de Notas e anotar o horário exato
2. Matar via `taskkill /IM notepad.exe /F`
3. Ir ao Visualizador de Eventos → Logs do Windows → Aplicativo
4. Checar se gerou evento no horário — encerramento forçado "de fora" normalmente **não gera erro**; um travamento espontâneo geraria (ex: "Application Hang")

---

#### Conexão com o trabalho (Action1)

O agente do Action1 faz, de forma **remota e centralizada**, o mesmo levantamento que essas ferramentas fazem localmente: inventário de hardware (≈ `msinfo32`), processos/estado atual (≈ Gerenciador de Tarefas), rede (≈ `ipconfig`) e histórico de erros (≈ Visualizador de Eventos) — tudo isso entregue via API.

---

### Dia 3 — [2.3] Portas e cabos

🔎 **O que é:** reconhecer as características de:

- Vídeo: HDMI, USB-C, DVI, DisplayPort, VGA
- USB-A, USB-B, USB-C, Micro USB
- Portas seriais
- RJ-45, UTP, STP (cabos de rede)
- Cabos de força (desktop, notebook, celular)
- Thunderbolt 3/4 (via USB-C)
- Conversores/adaptadores

🛠️ **Pratique hoje:**

- [x] Percorra fisicamente as portas do seu notebook/desktop e nomeie cada uma
- [x] Se tiver acesso a uma gaveta de cabos/adaptadores no help desk, identifique cada item
- [x] Monte uma tabela simples: porta → uso típico → cabo compatível

⏱️ **Tempo estimado:** 25–35 min

💡 **Dica:** esse ponto é bem visual — se quiser, posso te mostrar imagens comparando os conectores lado a lado, é só pedir.

---

### Dia 4 — [2.4] Componentes de desktop (identificação, instalação e upgrade)

🔎 **O que é:**

- Identificar processador e placa-mãe
- Identificar, instalar e fazer upgrade de RAM, periféricos internos (vídeo, wireless, Bluetooth) e armazenamento (SATA, SSD, NVMe, M.2)
- Compatibilidade de interfaces e slots de expansão
- Usar o Gerenciador de Dispositivos pra gerenciar drivers

🛠️ **Pratique hoje:**

- [ ] Abra o Gerenciador de Dispositivos e liste as categorias de hardware da máquina
- [ ] Descubra se o armazenamento é SATA SSD ou NVMe (Gerenciamento de Disco ou Informações do Sistema)
- [ ] Verifique se algum driver está desatualizado ou com erro (ícone de alerta)
- [ ] Se tiver acesso a um desktop físico disponível, abra o gabinete e identifique slots de RAM, conectores de armazenamento e slots de expansão

⏱️ **Tempo estimado:** 35–45 min

---

### Dia 5 — [2.5] Problemas comuns de hardware

🔎 **O que é:**

- Troubleshooting básico: está na tomada? conectado? ligado?
- Requisitos de compatibilidade de aplicações: arquitetura do processador, RAM, GPU, espaço em disco
- Usar o Gerenciador de Dispositivos pra identificar problemas
- Indicadores de status do dispositivo (LEDs)
- Atualizações de firmware (benefícios e riscos)
- Piscadas de diagnóstico da Dell (LED branco e laranja)

🛠️ **Pratique hoje:**

- [x] Procure a documentação oficial da Dell sobre os códigos de LED (branco/laranja) do modelo mais comum na empresa
- [x] Revise 2-3 códigos de erro comuns no Gerenciador de Dispositivos
- [x] Liste os riscos de um firmware/BIOS update sem necessidade (ex: travar o equipamento se faltar energia no meio)

⏱️ **Tempo estimado:** 30–40 min

💡 **Conexão com seu trabalho:** seu relatório do BSOD 0x0000003B no notebook Dell é um ótimo case pra revisar hoje.

---

## 📆 Semana 2 — Redes, Periféricos e Sistema Operacional (Dias 6–10)

### Dia 6 — [3.1] Acesso a recursos de rede

🔎 **O que é:**

- Serviços de diretório: Active Directory e Entra ID
- Autenticação multifator (MFA)
- Mapear unidade compartilhada (SMB e OneDrive)
- `gpupdate /force` no Windows (ou `adgpupdate` em máquinas Linux integradas ao AD)
- Reset de senha
- Verificar associação a grupos de segurança/distribuição
- Verificar permissões

🛠️ **Pratique hoje:**

- [x] No Entra ID, abra um usuário de teste e confira a quais grupos ele pertence e o que isso libera
- [x] Rode `gpupdate /force` na sua máquina e observe o log
- [x] Mapeie manualmente uma unidade via caminho UNC (`\\servidor\pasta`)
- [x] Revise os métodos de MFA disponíveis no tenant

⏱️ **Tempo estimado:** 35–45 min

💡 **Conexão com seu trabalho:** você já mexe com Entra ID no dia a dia — esse é um dos pontos onde você já tem bagagem prática, só falta formalizar.

---

### Dia 7 — [3.2] Conectividade de periféricos

🔎 **O que é:** resolver conectividade em impressoras (fila de impressão, toner, papel), fones, microfones, HDs externos, scanners, webcams, teclado/mouse (com e sem fio), telas touch e dispositivos de teleconferência (Webex Desk Pro).

🛠️ **Pratique hoje:**

- [x] Reinicie o serviço de spooler de impressão (`services.msc` → Print Spooler) e veja o efeito na fila
- [x] Revise o passo a passo oficial de troubleshooting do Webex Desk Pro (câmera, áudio, conexão)
- [x] Simule a limpeza de uma fila de impressão travada

⏱️ **Tempo estimado:** 30 min

💡 **Conexão com seu trabalho:** Webex já está no seu dia a dia — vale revisar a documentação oficial da Cisco pros cenários de tela Desk Pro.

---

### Dia 8 — [3.3] Conectividade básica de rede

🔎 **O que é:**

- LAN (cabo) vs. WLAN (wireless)
- Função do DNS e do DHCP (e o que é IP autoatribuído / APIPA)
- Faixas de IP (sub-rede certa, público x privado)
- Gateway padrão e SSID
- Comandos: ipconfig/ifconfig, tracert/traceroute, ping, nslookup, netstat, ping6, traceroute6, iproute2 (`ip add`, `ss`)
- Função do firewall e como ele afeta a conectividade

🛠️ **Pratique hoje:**

- [ ] Rode na sua máquina: `ipconfig /all`, `ping`, `tracert`, `nslookup`, `netstat -ano`
- [ ] Identifique: seu IP (público x privado), sua sub-rede, seu gateway padrão, seus servidores DNS
- [ ] Explique em voz alta a diferença entre DNS e DHCP como se estivesse ensinando alguém

⏱️ **Tempo estimado:** 30–40 min

💡 **Conexão com seu trabalho:** isso conversa direto com o que você já estudou no NetAcad (CCNA) — hoje é mais consolidar do que aprender do zero.

---
# 📓 Caderno de Estudos — Infraestrutura

**Tema:** [3.3] Conectividade Básica de Rede  
**Data:** 18/08/2026  
**Aluno:** Matheus Lopes

### 1. Análise do ipconfig /all e a dúvida do DNS == Gateway

Na saída do meu comando, o DNS e o Gateway são os mesmo porque o meu roteador doméstico atua como Proxy e encaminhador de DNS. Quando meu computador quer resolver um nome, ele manda a pergunta para o gateway. O roteador recebe, pega essa requisição e repassa para um DNS externo, recebe a resposta e entrega de volta.

### 2. Anatomia do tracert 8.8.8.8 (passo a passo de cada salto)

O comando tracert descobre o caminho que um pacote faz da sua máquina até o destino. Cada linha é um roteador no meio do caminho:
```text
  1    <1 ms    <1 ms    <1 ms  192.168.18.1
```
- No salto 1, meu roteador local/gateway (192.168.18.1) responde instantaneamente porque está na minha sala.

```text
  2     6 ms     2 ms     2 ms  100.64.0.1
  3     4 ms     1 ms     1 ms  172.22.0.6
  4     2 ms     2 ms     2 ms  172.22.0.1
  5     4 ms     2 ms     4 ms  0.0.23.45
  6     5 ms     2 ms     2 ms  172.16.172.1
```
- Saltos 2 a 6 são roteadores internos da operadora da internet (ISP). Possui faixas de IPs privados (`10.x.x.x`, `172.x.x.x`, `100.x.x.x` - CGNAT).

```text
  7     2 ms     2 ms     2 ms  142.250.167.18
  8     4 ms     2 ms     3 ms  142.251.69.139
  9     5 ms     2 ms     2 ms  108.170.235.139
 10     5 ms     2 ms     2 ms  dns.google [8.8.8.8]
```
- Saltos de 7 a 10. Entrou na rede backbone pública da internet e na infraestrutura global do Google até chegar ao ip final 8.8.8.8.

### 3. `nslookup` na Prática (Dia a Dia do Estagiário de Infra)
Ele consulta o servidor DNS para traduzir nomes legíveis em endereços IP.

Como usar no suporte:
1. Usuário reclama: "Não consigo acessar o sistema da empresa"
2. Teste com nslookup:
	1. Se retornar erro (`Server failure` ou `Non-existent domain`), o problema é de DNS (o servidor de nomes não sabe quem é essa intranet, ou o registro A/CNAME sumiu no AD/DNS Server).
	2. Se retornar o IP certinho, mas o usuário não consegue abrir a página, o problema não é DNS. O cabo está ok, a rede resolveu o nome, mas a aplicação caiu, a porta está bloqueada pelo firewall ou o serviço web parou.

### Análise Linha por Linha:

#### 1. Cabeçalho do Servidor DNS

```text
Servidor:  UnKnown
Address:  192.168.18.1
```
Ao rodar o comando, ele se questiona de para quem deve perguntar. O windows olha no ipconfig e vê que o servidor DNS configurado é o 192.168.18.1 (roteador).

O Unknown significa que o próprio roteador não tem a informação do nome do DNS reverso nele. Então o Windows usa o IP.

#### 2. O Aviso de Resposta

```text
Não é resposta autoritativa:
```

Significa que a resposta não veio direto da fonte, o Windows usou o que tinha em cache. Para o dia a dia, **isso é perfeitamente normal e desejado**, pois acelera a navegação.

#### 3. O Alvo Resolvido

```text
Nome:    youtube.com
Addresses:  2800:3f0:4001:81c::200e
          142.251.133.78
```
O DNS cumpriu o seu papel com sucesso. Ele traduziu o nome legível para os endereços IP reais onde o serviço está hospedado:
- O primeiro (`2800:3f0:...`) é o endereço **IPv6** do YouTube.
- O segundo (`142.251.133.78`) é o endereço **IPv4** do YouTube.

### Como usar isso no seu dia a dia de Infra/Suporte:

Se um usuário rodar `nslookup` para um sistema da empresa (ex: `erp.suaempresa.local`) e a resposta for algo como:

- `*** O Servidor Desconhecido não pode encontrar erp.suaempresa.local: Non-existent domain` (ou falha no servidor DNS)

Significa que **o servidor DNS não sabe quem é esse nome**. Ou o nome foi digitado errado, ou o registro DNS desse sistema sumiu do servidor Active Directory / DNS da empresa, ou a máquina do usuário está sem comunicação com o DNS corporativo.

### 4. desvendando o netstat -ano
Ele mostra todas as conexões de rede ativas e portas escutando na sua máquina. A flag -a mostra tudo, -n mostra números (em vez de tentar resolver nomes de domínio) e -o mostra o PID (Process ID).

### Para que serve no dia a dia?

- **Cenário 1 (Conflito de Porta):** Você vai rodar um serviço (ex: um container Docker, IIS, aplicação Node.js) e recebe o erro: _"Porta 80 / 443 / 8080 já está em uso"_.
    - Você roda: `netstat -ano | findstr 8080`
    - Ele te dá o PID (ex: `4736`).
    - Você vai no _Gerenciador de Tarefas_ (aba Detalhes) e descobre qual programa/serviço está travando aquela porta.
- **Cenário 2 (Auditoria/Segurança):** Investigar se há conexões externas suspeitas saindo da máquina de um usuário para IPs desconhecidos.
### Colunas explicadas:

- **Proto:** Protocolo (TCP ou UDP).
- **Endereço Local:** O IP da sua máquina e a porta que está aberta/conversando (`192.168.18.32:53185`). `0.0.0.0` significa "escutando em todas as placas de rede".
- **Endereço Externo:** Com quem o seu computador está falando na internet (`8.8.8.8:443`).
- **Estado:**
    - `LISTENING`: A porta está aberta, "esperando" alguém se conectar (ex: servidor web).
    - `ESTABLISHED`: Conversa ativa neste exato segundo (ex: aba do navegador aberta consumindo dados).
    - `TIME_WAIT` / `CLOSE_WAIT`: Conexão recém-encerrada, limpando os recursos.
- **PID:** O número de identificação do processo no Windows. É a ponte entre a rede e o Gerenciador de Tarefas.
### 💡 Como usar isso na prática no Help Desk / Infra?

Imagine que um usuário te liga: _"O sistema em nuvem da empresa está fora do ar!"_

1. Você roda um `tracert` para o endereço do sistema da empresa.
2. Se o rastreio parar no **Salto 2 ou 3** (dentro da rede da empresa ou da operadora de vocês) e ficar dando `* * *` (timeout), o problema é **local ou da operadora** (sua internet caiu ou a operadora rompeu fibra).
3. Se o rastreio chegar até a porta da nuvem (ex: AWS ou Azure) mas a aplicação não abrir, o problema **não é de rede/internet** — a rota está perfeita, o que significa que o servidor da aplicação em nuvem travou ou o serviço caiu.

---

### Dia 9 — [4.1] Problemas do Windows

🔎 **O que é:**

- Configurações de tela, múltiplos monitores, brilho
- Chaves de recuperação do BitLocker
- Atualizações do Windows e de aplicativos
- Limpeza de cache do navegador
- Encerrar processos pelo Gerenciador de Tarefas
- Backup/restauração via OneDrive
- Sequência de boot e Modo de Segurança
- Gerenciamento de energia e recursos de acessibilidade

🛠️ **Pratique hoje:**

- [x] Localize como recuperar uma chave do BitLocker via Entra ID/AD
- [x] Limpe o cache do navegador no Edge e no Chrome
- [x] Explore os recursos de acessibilidade em Configurações (Narrador, alto contraste, etc.)
- [ ] Se tiver uma VM de teste, pratique iniciar em Modo de Segurança (evite numa máquina de produção)

⏱️ **Tempo estimado:** 35–45 min

💡 **Conexão com seu trabalho:** o caso da KB5094126 (travamento do Explorer, quebra do OneDrive) que você investigou via Action1 é um exemplo real desse tópico.

---

### Dia 10 — [4.3] Problemas em dispositivos móveis

🔎 **O que é:** reiniciar o aparelho, conectividade, configuração de e-mail, apps corporativos e de colaboração, noção básica de MDM; diferenças entre iOS e Android.

🛠️ **Pratique hoje:**

- [ ] Configure (ou revise) uma conta corporativa no Outlook mobile
- [ ] Se a empresa usa Intune ou outro MDM, revise as políticas de compliance de dispositivo
- [ ] Liste as 3 causas mais comuns de "e-mail não sincroniza no celular"

⏱️ **Tempo estimado:** 25–35 min

---

## 📆 Semana 3 — Cloud, Aplicações e Segurança (Dias 11–15)

### Dia 11 — [4.4] Virtualização e cloud

🔎 **O que é:** provedores de nuvem (Microsoft Azure); máquinas virtuais e hipervisores — Tipo 1 (bare-metal, ex: Hyper-V) x Tipo 2 (hospedado, ex: VirtualBox).

🛠️ **Pratique hoje:**

- [ ] Revise suas próprias anotações dos Labs 01/02a/02b no Obsidian
- [ ] Explique a diferença entre hipervisor Tipo 1 e Tipo 2 com suas palavras
- [ ] Relacione isso com o que você já estudou pro AZ-104

⏱️ **Tempo estimado:** 25–30 min

💡 Esse é um dia "de graça" — você já vem estudando isso pro AZ-104, então hoje é mais revisão do que aprendizado novo.

---

### Dia 12 — [4.5] Problemas de aplicações

🔎 **O que é:** instalação de apps via loja/fonte aprovada; riscos de fontes desconhecidas; problemas em apps de e-mail, colaboração e produtividade.

🛠️ **Pratique hoje:**

- [ ] Verifique se existe uma política formal de fontes aprovadas de software na empresa
- [ ] Pratique diagnosticar o cenário "add-in não carrega no Outlook/Teams"
- [ ] Explique como checar se um instalador tem assinatura digital válida

⏱️ **Tempo estimado:** 30 min

---

### Dia 13 — [5.1] Ameaças de segurança

🔎 **O que é:** phishing, malware, spam, tentativas de acesso não autorizado, spoofing; como ajudar o usuário a rodar um scan de malware; boas práticas de senha.

🛠️ **Pratique hoje:**

- [ ] Rode um scan completo do Windows Defender e analise o relatório
- [ ] Revise o módulo correspondente das suas notas de cibersegurança do NetAcad no Obsidian
- [ ] Rascunhe uma "folha de dicas" anti-phishing de 5 pontos pros usuários da empresa

⏱️ **Tempo estimado:** 30–40 min

💡 **Conexão com seu trabalho:** suas notas de "Fundamentos de segurança cibernética" já cobrem boa parte disso — ótimo dia pra reaproveitar esse material.

---

### Dia 14 — [5.2] Engenharia social

🔎 **O que é:** o técnico de help desk é um alvo preferencial de ataques de engenharia social — phishing, personificação (impersonation), etc.

🛠️ **Pratique hoje:**

- [ ] Pesquise 2-3 táticas reais recentes de engenharia social contra help desks (ex: ligação urgente pedindo reset de senha)
- [ ] Rascunhe um checklist de sinais de alerta antes de resetar senha ou liberar acesso por telefone/chat
- [ ] Reflita: numa multi-family office, executivos e famílias atendidas são alvos de alto valor — o que isso muda na sua postura?

⏱️ **Tempo estimado:** 30 min

---

### Dia 15 — [5.3] Confidencialidade e políticas

🔎 **O que é:** identificar dados confidenciais, proprietários e PII (informação pessoal identificável).

🛠️ **Pratique hoje:**

- [ ] Verifique se existe uma política de classificação de dados na empresa (pergunte se não souber)
- [ ] Liste os tipos de dado que você acessa como estagiário de TI que seriam PII/confidenciais (ex: durante um reset de senha, uma sessão remota)
- [ ] Escreva 2-3 práticas que você já segue (ou deveria seguir) pra proteger esse tipo de dado

⏱️ **Tempo estimado:** 25–35 min

💡 Esse ponto pesa mais numa multi-family office como a TUrim — vocês lidam com dados financeiros e pessoais de famílias de alto patrimônio, então "sigilo" aqui é praticamente um requisito de negócio, não só de TI.

---

## 📆 Semana 4 — Suporte Remoto, Documentação e Fechamento (Dias 16–20)

### Dia 16 — [6.1] Acesso remoto

🔎 **O que é:** Remote Desktop, Assistência Remota, Cisco Webex, gerenciamento remoto (Action1), TeamViewer, VNC, PC Anywhere.

🛠️ **Pratique hoje:**

- [ ] Compare as ferramentas que você já usa (Action1, Webex) com as demais: vantagens, riscos, necessidade de consentimento do usuário
- [ ] Documente isso como um mini guia de referência

⏱️ **Tempo estimado:** 25–35 min

---

### Dia 17 — [6.2] Pesquisa e documentação

🔎 **O que é:** usar IA pra pesquisar um problema (limitações, ética, riscos de privacidade/segurança, diferença entre IA preditiva e generativa); motores de busca; fóruns técnicos; artigos de base de conhecimento (do mercado e internos).

🛠️ **Pratique hoje:**

- [ ] Escreva 2-3 limitações/riscos reais de usar IA em troubleshooting (ex: alucinação, não compartilhar dado sensível com IA pública) e como você já mitiga isso
- [ ] Revise sua própria KB de M365/EAC e veja se falta algum cenário comum

⏱️ **Tempo estimado:** 25–30 min

💡 Esse você praticamente já domina na prática — hoje é sobre colocar em palavras o que você já faz bem.

---

### Dia 18 — [6.3] Windows Server e ferramentas administrativas

🔎 **O que é:** AD, DHCP, File Server, Print Server, entre outras funções administrativas do Windows Server.

🛠️ **Pratique hoje:**

- [ ] Se a empresa tiver servidor on-premises, peça pra acompanhar alguém sênior mexendo no AD/DHCP
- [ ] Se não for possível, suba uma VM de teste (Azure free tier ou Hyper-V/VirtualBox local) e instale as roles de AD DS e DHCP
- [ ] Explore o Gerenciador do Servidor e identifique as roles instaladas

⏱️ **Tempo estimado:** 45–60 min (provavelmente o ponto que mais exige tempo — vale dividir em 2 sessões se precisar)

---

### Dia 19 (bônus) — Revisão geral

🎯 **Objetivo:** consolidar o que ficou menos claro.

🛠️ **Hoje:**

- [ ] Releia os 18 tópicos e marque os 2-3 que você sentiu menos confiança
- [ ] Explique cada um em voz alta, em 1-2 frases, como se estivesse ensinando um novo estagiário
- [ ] Ajuste suas anotações do Obsidian com o que ficou mais claro

⏱️ **Tempo estimado:** 30–40 min

---

### Dia 20 (bônus) — Preparar a conversa com seu chefe

🎯 **Objetivo:** chegar na conversa de efetivação com evidência concreta, não só "eu estudei".

🛠️ **Hoje:**

- [ ] Monte um resumo de 1 página com os 18 pontos e o que você estudou/praticou em cada um
- [ ] Junte evidências que você já tem: sua KB de M365/EAC, o relatório de BSOD, o `action1-desktop`, o fluxo de migração do Planner no Power Automate
- [ ] Agende proativamente uma conversa curta com seu chefe pra apresentar esse resumo — não espere ser cobrado

⏱️ **Tempo estimado:** 30–45 min

---

## 🚀 Dicas extras para aumentar suas chances de efetivação

1. **Centralize tudo em um só lugar.** Você já usa Obsidian — crie uma nota "Checklist de Efetivação" linkando cada um dos 18 pontos ao que você estudou e praticou. Vira prova concreta, não só uma promessa.
    
2. **Transforme chamados reais em estudo de caso.** Toda vez que um ticket tocar em um desses tópicos, anote: o que era → como resolveu → qual ponto isso comprova.
    
3. **Faça check-ins curtos e regulares com seu chefe** (5-10 min por semana) mostrando o que avançou. Proatividade pesa mais que perfeição, e evita a sensação de "sumiço" até o prazo final.
    
4. **Consolide o que você já entregou.** O `action1-desktop`, a migração de tarefas do Planner, a KB de M365/EAC, o relatório e checklist de BSOD — reúna isso num documento ou apresentação simples. É munição forte na hora da decisão.
    
5. **Peça feedback continuamente**, não só no fim. "Como estou indo? O que posso melhorar?" mostra maturidade, não insegurança.
    
6. **Reforce a postura de confidencialidade sempre que possível.** Numa multi-family office, a confiança das famílias atendidas é o ativo mais valioso da empresa — um estagiário com senso de sigilo natural se destaca rápido.
    
7. **Treine explicar tecnologia em termos simples.** Você lida com usuários não técnicos o tempo todo — "traduzir" TI pra quem não é da área vale tanto quanto o conhecimento técnico puro.
    
8. **Pergunte ao seu chefe se existe um formato de avaliação** (prova, entrevista, checklist assinado). Ajuda a calibrar a profundidade certa em cada tópico e mostra que você está levando isso a sério.
    

---

Boa sorte com os estudos — e com o que você já vem entregando, esse plano é mais sobre deixar isso visível do que sobre começar do zero.