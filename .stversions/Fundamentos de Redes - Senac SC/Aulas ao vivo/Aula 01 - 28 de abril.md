# Redes de Computadores

> Computadores interligados para **compartilhar informações e recursos**.

---

## 1. Componentes de uma Rede

### Hardware

- Equipamento de usuário
- Meio físico de comunicação
- Equipamentos de rede

### Software

- Protocolos de rede
- Aplicações de rede

---

## 2. Equipamentos

### Equipamentos de Usuário (End Points / Hosts)

Originam e recebem tráfego.

**Exemplos:** computadores, laptops, impressoras, celulares, relógios, lâmpadas.

**Clientes vs. Servidores (hardware)**

|Papel|Função|
|---|---|
|Cliente|Usa o recurso|
|Servidor|Gerencia o recurso|

---

### Equipamentos de Rede (Intermediários)

Encaminham o tráfego: **switch**, **access point**, **roteador**.

---

### Meios Físicos

|Meio|Sinal|
|---|---|
|Cabos metálicos|Elétrico|
|Cabos ópticos|Luminoso|
|Wireless|Eletromagnético|

---

## 3. Topologias de Rede

> Forma como os equipamentos estão interligados.

### Anel

|Característica|Detalhe|
|---|---|
|Funcionamento|Dados circulam em um único sentido, passando por cada nó|
|Falha|Um nó com defeito pode derrubar toda a rede|
|Vantagem|Sem colisões de pacotes; fácil diagnóstico de falhas|
|Desvantagem|Baixa tolerância a falhas; expansão difícil|
|Custo|Baixo cabeamento|
|Uso típico|Redes legadas (Token Ring)|

---

### Estrela

|Característica|Detalhe|
|---|---|
|Funcionamento|Todos os dispositivos conectam-se a um hub/switch central|
|Falha|Falha no hub derruba toda a rede|
|Vantagem|Isolamento de falhas simples; fácil adicionar/remover nós|
|Desvantagem|Dependência total do dispositivo central|
|Custo|Médio (mais cabos, mas switch barato)|
|Uso típico|Redes domésticas e LANs corporativas — **topologia mais comum hoje**|

---

### Malha

|Característica|Detalhe|
|---|---|
|Funcionamento|Cada nó conectado diretamente a vários outros|
|Falha|Falha de um nó **não** derruba a rede|
|Vantagem|Alta redundância e resiliência|
|Desvantagem|Custo de cabeamento muito elevado|
|Variações|Parcial (alguns caminhos) ou Total (full mesh)|
|Uso típico|Backbones, roteadores de internet|

---

### Barramento

|Característica|Detalhe|
|---|---|
|Funcionamento|Todos os dispositivos pendurados em um único cabo compartilhado|
|Falha|Falha no cabo derruba toda a rede|
|Vantagem|Simples e barato de implementar|
|Desvantagem|Colisões frequentes; difícil diagnóstico; praticamente obsoleto|
|Custo|Muito baixo|
|Uso típico|Redes antigas (Ethernet 10Base2 / coaxial)|

---

### Hierarquia (Árvore)

|Característica|Detalhe|
|---|---|
|Funcionamento|Organização em camadas pai/filho; combinação de estrelas|
|Falha|Falha num nó intermediário afeta toda a sua subárvore|
|Vantagem|Fácil expansão por galhos; gerenciamento centralizado|
|Desvantagem|Ponto único de falha por nível hierárquico|
|Custo|Médio a alto (conforme escala)|
|Uso típico|Redes corporativas, WAN, infraestrutura de campus|

---

### Comparativo Rápido

|Topologia|Redundância|Custo|Escalabilidade|Uso Atual|
|---|---|---|---|---|
|Anel|Baixa|Baixo|Difícil|Raro|
|Estrela|Média|Médio|Alta|Muito comum|
|Malha|Alta|Alto|Média|Backbones|
|Barramento|Nenhuma|Muito baixo|Baixa|Obsoleto|
|Hierarquia|Média|Médio|Alta|Comum|

---

## 4. Diagramas de Rede

### Diagrama Físico — _"O que está instalado e onde?"_

Mostra a infraestrutura concreta e tangível: equipamentos reais, localização física e como estão interligados por cabos.

**O que aparece:**

- Equipamentos reais (switches, roteadores, patch panels, APs, servidores)
- Tipo e meio de conexão (cabo UTP Cat6, fibra óptica, Wi-Fi)
- Localização física (rack, sala, andar)
- Número de portas, comprimento de cabos, modelo e fabricante

**Público:** técnicos de campo, equipe de cabeamento, facilities.

---

### Diagrama Lógico — _"Como o tráfego flui?"_

Mostra como a rede funciona: endereçamento IP, VLANs, roteamento e protocolos. Equipamentos são representados como ícones genéricos.

**O que aparece:**

- Endereços IP e máscaras de sub-rede
- VLANs e suas fronteiras
- Gateways e rotas
- Protocolos (OSPF, BGP, STP, DHCP)
- Zonas de segurança (DMZ, LAN, WAN)
- Serviços (DNS, Firewall, NAT)

**Público:** administradores de rede, arquitetos de sistemas, equipe de segurança.

---

### Comparativo: Físico vs. Lógico

|Aspecto|Físico|Lógico|
|---|---|---|
|Pergunta central|Onde está?|Como funciona?|
|Representa|Hardware e cabos|IPs, VLANs, rotas|
|Nível de detalhe|Modelo, porta, rack|Sub-rede, protocolo, gateway|
|Localização importa?|Sim|Não|
|Muda com mudança de IP?|Não|Sim|
|Muda ao trocar um switch?|Sim|Raramente|
|Ferramenta comum|Visio, draw.io|Visio, draw.io, NetBox|

**Exemplo prático:**

- **Físico:** switch Cisco Catalyst 2960 no rack 3 do andar 2, conectado via fibra OM3 ao patch panel do andar 1, porta 24.
- **Lógico:** nó "SW-DIST-02" separando VLAN 10 (192.168.10.0/24) da VLAN 20 (192.168.20.0/24), com gateway apontando para o firewall.

---

## 5. Classificação de Redes

|Característica|LAN|WAN|
|---|---|---|
|Abrangência|Local|Remota|
|Localização|Dentro de uma propriedade|Entre propriedades|
|Infraestrutura|Meios e equipamentos próprios|Meios de provedores (ISPs)|
|Custo do tráfego|Gratuito|Tarifado|
|Velocidade|Maior|Menor|
|Qualidade|Maior|Menor|
|Função|Conecta dispositivos de usuário|Interconecta LANs distantes|

> **Importante:** LAN e WAN **não** se diferenciam pelo tamanho ou quantidade de equipamentos, mas pelo **domínio administrativo**.

### Tecnologias LAN

|Tipo|Tecnologia|Equipamentos|
|---|---|---|
|Cabeada|Ethernet|Switch + cabos|
|Sem fio|Wi-Fi|Roteador / Access Point|

---

## 6. Endereçamento Físico

### MAC Address — _Media Access Control_

Endereço de **48 bits**, dividido em dois blocos de 24 bits.

**Exemplo:** `00:1A:3F:F1:4C:C6`

|Bloco|Octetos|Nome|Descrição|
|---|---|---|---|
|OUI|`00:1A:3F`|Organizationally Unique Identifier|Identifica o **fabricante**|
|NIC|`F1:4C:C6`|Network Interface Controller Specific|Identifica o **dispositivo**|

---

### Frame Ethernet

Tamanho total: **64 – 1518 bytes**

|Campo|Tamanho|Descrição|
|---|---|---|
|Preamble + SFD|8 bytes|Sincronização e delimitador de início|
|Destination MAC|6 bytes|Endereço MAC do destinatário|
|Source MAC|6 bytes|Endereço MAC do remetente|
|Type / Length|2 bytes|Protocolo da camada superior (ex: IPv4, ARP)|
|Data (Payload)|45–1500 bytes|Dados encapsulados|
|FCS|4 bytes|Frame Check Sequence — verificação CRC|

---

## 7. Internet

- Rede de computadores de **alcance global**
- WAN que interconecta todas as LANs do mundo
- Formada pela interligação hierárquica dos **ISPs** (Internet Service Providers)

**Conexão à Internet:**

- Feita através de um provedor (ISP) via _link_
- Tecnologias: linha telefônica, fibra óptica, rádio, satélite, celular (5G)
- **Roteador:** equipamento que interliga redes; pode exercer função de firewall

**Medidas:**

- Taxa de transferência / velocidade → **bits por segundo (bps)**
- Volume de dados → **bytes**

---

## 8. Arquitetura de Rede

- A comunicação é regida por **regras**
- Regras são agrupadas em **protocolos**
- Protocolos são agrupados em **arquiteturas/modelos**
- Definidas de forma estruturada: **modelo de camadas**

> Dois equipamentos se comunicam apenas se possuem a mesma arquitetura.

**Cada camada:**

- Realiza uma parte do trabalho
- Serve à camada superior (interface/serviço)
- Conversa com a mesma camada do outro equipamento (protocolo)

---

### Modelo OSI — Comunicação em Camadas

|Sistema A|↔ Protocolo ↔|Sistema B|
|---|---|---|
|Camada 7 — Aplicação|↔|Camada 7|
|Camada 6 — Apresentação|↔|Camada 6|
|Camada 5 — Sessão|↔|Camada 5|
|Camada 4 — Transporte|↔|Camada 4|
|Camada 3 — Rede|↔|Camada 3|
|Camada 2 — Enlace|↔|Camada 2|
|Camada 1 — Física|↔|Camada 1|

> **Meio de Transmissão** — base física compartilhada entre os dois sistemas.

**Vantagens do modelo de camadas:**

- Facilita o projeto e o estudo
- Possibilita interoperabilidade
- Estimula a competição
- Permite engenharia modular (alterar uma camada sem afetar as outras)
- Fornece linguagem comum para descrever a rede

---

### Encapsulamento e Desencapsulamento

|Processo|Descrição|
|---|---|
|**Encapsulamento**|Na transmissão: cada camada **acrescenta** seu cabeçalho e passa à camada inferior|
|**Desencapsulamento**|Na recepção: cada camada **processa e retira** seu cabeçalho e passa à camada superior|

---

### Comparativo: OSI vs. TCP/IP

|OSI|TCP/IP|
|---|---|
|7. Aplicação||
|6. Apresentação|Aplicação|
|5. Sessão||
|4. Transporte|Transporte|
|3. Rede|Internet|
|2. Enlace de Dados|Acesso à Rede|
|1. Física||

---

## 9. Camada de Aplicação

- Não tem função específica pré-definida
- Protocolos e serviços mais utilizados: **HTTP**, **SMTP**, entre outros
- As implementações TCP/IP em cada SO oferecem interfaces com a camada de transporte para que programadores desenvolvam seus próprios aplicativos

### Modelo Cliente/Servidor

|Papel|Função|
|---|---|
|**Servidor**|Oferece serviços|
|**Cliente**|Utiliza serviços|

**Características:**

- São processos (software rodando em hardware)
- Comunicam-se por uma rede, trocando mensagens (cliente solicita, servidor responde)
- Podem estar na mesma sala ou em países diferentes
- Um servidor pode atender **vários clientes simultaneamente**
- O servidor geralmente possui mecanismos de **autenticação**
- Cliente e servidor não precisam se preocupar com detalhes da comunicação

---

### Protocolos por Camada (TCP/IP)

|Camada|Protocolos|
|---|---|
|Aplicação|HTTP, FTP, SMTP, DNS, RIP, SNMP|
|Transporte|TCP, UDP|
|Internet|ARP, IP, IGMP, ICMP|
|Acesso à Rede|Ethernet, Token Ring, Frame Relay, ATM|

---

---

# 📝 Resumo para Anotação em Papel

## Bloco 1 — Estrutura Básica

```
Rede = equipamentos interligados para compartilhar info e recursos

Componentes:
  Hardware → end points (hosts), equipamentos de rede, meio físico
  Software → protocolos, aplicações

Meios físicos:
  Cabo metálico → sinal elétrico
  Cabo óptico   → sinal luminoso
  Wireless      → sinal eletromagnético
```

---

## Bloco 2 — Topologias

```
Anel      → circular, 1 sentido | falha = rede cai | uso: legado
Estrela   → hub/switch central  | falha no hub = rede cai | USO MAIS COMUM
Malha     → todos ligados       | alta redundância | custo alto | backbones
Barramento→ cabo único          | colisões | OBSOLETO
Hierarquia→ árvore (estrelas)   | escalável | ponto de falha por nível
```

---

## Bloco 3 — LAN vs. WAN

```
LAN → dentro da propriedade, infra própria, tráfego grátis, mais rápida
WAN → entre propriedades, infra do ISP, tráfego tarifado, mais lenta
Diferença = domínio administrativo (não tamanho)
```

---

## Bloco 4 — MAC Address e Frame Ethernet

```
MAC = 48 bits = OUI (fabricante) + NIC (dispositivo)
Ex: 00:1A:3F : F1:4C:C6
      OUI          NIC

Frame Ethernet (64–1518 bytes):
  Preamble+SFD | Dest MAC | Src MAC | Type | Data | FCS
     8B            6B        6B       2B   45-1500B  4B
```

---

## Bloco 5 — Modelos de Camadas

```
OSI (7 camadas)       TCP/IP (4 camadas)
7. Aplicação    ┐
8. Apresentação ├──► Aplicação
9. Sessão       ┘
10. Transporte   ────► Transporte
11. Rede         ────► Internet
12. Enlace       ┐
13. Física       ├──► Acesso à Rede

Encapsulamento:   TX → cada camada ADICIONA cabeçalho (desce)
Desencapsulamento: RX → cada camada RETIRA cabeçalho (sobe)
```

---

## Bloco 6 — Camada de Aplicação

```
Modelo Cliente/Servidor:
  Cliente → solicita
  Servidor → responde (autentica, atende vários clientes)

Protocolos:
  Aplicação  → HTTP, FTP, SMTP, DNS
  Transporte → TCP, UDP
  Internet   → IP, ICMP, ARP
  Rede       → Ethernet
```

