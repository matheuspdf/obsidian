
# Quiz — Fundamentos de Segurança Cibernética (Cisco NetAcad)

### Gabarito comentado — 24 questões

---

## Pergunta 1

**Os funcionários de uma empresa recebem um e-mail informando que a senha da conta irá expirar imediatamente, e que é necessário redefinir uma senha dentro de 5 minutos. Qual declaração classificaria esse e-mail?**

✅ **É um hoax.**

Esse cenário é o exemplo clássico de **hoax** (farsa/boato): um e-mail que cria falsa urgência para induzir o usuário a agir por impulso, sem verificar a veracidade da informação.

---

## Pergunta 2

**Que tipo de ataque é direcionado a um banco de dados SQL usando o campo de entrada de um usuário?**

✅ **Inserção de SQL (SQL Injection)**

Explora campos de entrada de formulários web para inserir comandos SQL maliciosos, manipulando diretamente o banco de dados por trás da aplicação.

---

## Pergunta 3

**Um criminoso virtual envia uma série de pacotes formatados maliciosamente para o servidor de banco de dados. O servidor não consegue analisar os pacotes e o evento causa a falha do servidor. Qual tipo de ataque o criminoso virtual lançou?**

✅ **DoS (Denial of Service)**

O envio de pacotes malformados para travar/derrubar um servidor visa interromper a disponibilidade do serviço.

---

## Pergunta 4

**O que o termo vulnerabilidade significa?**

✅ **Uma fraqueza que torna um alvo suscetível a um ataque.**

---

## Pergunta 5

**Qual é a primeira linha de defesa para proteger um dispositivo contra controle de acesso inadequado?**

✅ **Senhas**

Senhas controlam quem consegue efetivamente acessar o dispositivo em primeiro lugar.

---

## Pergunta 6

**Que termo de vetor de perda de dados ou ataque seria usado para descrever o fornecimento de acesso a dados corporativos ao obter acesso a senhas fracas ou roubadas?**

✅ **Controle de acesso impróprio**

---

## Pergunta 7

**Combine o tipo de ciberataque à descrição.**

|Categoria|Descrição|
|---|---|
|**Hacktivistas**|Fazer declarações políticas a fim de criar consciência de questões importantes para eles|
|**Atacantes patrocinados pelo estado**|Coletar informações ou cometer sabotagem em objetivos específicos em nome de seu governo|
|**Corretores de vulnerabilidade**|Descobrir falhas e reportá-las aos fornecedores|

---

## Pergunta 8

**Um site de mídia social está descrevendo uma violação de segurança em uma agência confidencial de um banco nacional. Na publicação, ela se refere a uma vulnerabilidade. Que afirmação descreve esse termo?**

✅ **Uma fraqueza em um sistema ou em seu design que pode ser explorada por uma ameaça.**

---

## Pergunta 9

**Qual termo descreve um campo no cabeçalho do pacote IPv4 usado para detectar corrupção no cabeçalho IPv4?**

✅ **Soma de verificação do cabeçalho (header checksum)**

---

## Pergunta 10

**Quais três campos de cabeçalho IPv4 não têm equivalente em um cabeçalho IPv6? (Escolha três.)**

✅ **Sinalização** ✅ **Deslocamento de fragmento** ✅ **Identificação**

Esses três campos estão relacionados ao processo de **fragmentação** do IPv4, eliminado no cabeçalho base do IPv6.

> _TTL → equivale a Hop Limit | Protocolo → equivale a Next Header | Versão → também existe no IPv6._

---

## Pergunta 11

**Um funcionário insatisfeito está usando o Wireshark para descobrir nomes de usuário e senhas administrativos do Telnet. Que tipo de ataque de rede isso descreve?**

✅ **Reconhecimento**

Coleta de informações (credenciais) através de sniffing, antes de um ataque mais direto.

---

## Pergunta 12

**Que tipo de ataque de rede envolve a abertura aleatória de várias solicitações Telnet a um roteador e faz com que um administrador de rede válido não consiga acessar o dispositivo?**

✅ **Inundação de SYN (SYN flood)**

---

## Pergunta 13

**Combine o ataque com a definição.**

|Categoria|Definição|
|---|---|
|**Ataque de utilização de recursos**|O invasor envia vários pacotes que consomem recursos do servidor|
|**Envenenamento de cache**|O invasor envia informações falsificadas para redirecionar usuários para sites maliciosos|
|**Amplificação e reflexão**|O invasor usa resolvedores abertos para aumentar o volume de ataques e mascarar a verdadeira fonte do ataque|

---

## Pergunta 14

**Qual opção é uma vulnerabilidade que permite que criminosos injetem scripts em páginas da Web vistas por usuários?**

✅ **Script entre sites (XSS — Cross-Site Scripting)**

---

## Pergunta 15

**Qual medida de segurança é melhor usada para limitar o sucesso de um ataque de reconhecimento de dentro de uma rede de área do campus?**

✅ **Implemente criptografia para tráfego confidencial.**

Mesmo que o invasor capture os pacotes (sniffing), não conseguirá extrair informações úteis se o tráfego estiver criptografado.

---

## Pergunta 16

**Como os cibercriminosos fazem uso de um iFrame malicioso?**

✅ **O iFrame permite que o navegador carregue uma página da Web de outra fonte.**

---

## Pergunta 17

**Quais são os dois métodos que uma NIC sem fio pode usar para descobrir um AP? (Escolha duas.)**

✅ **Transmitindo uma solicitação de teste** (modo ativo — probe request) ✅ **Receber um quadro de beacon de transmissão** (modo passivo)

---

## Pergunta 18

**Um usuário liga para o suporte técnico reclamando que a senha para acessar a rede sem fio foi alterada sem aviso prévio. O usuário tem permissão para alterar a senha, mas, uma hora depois, a mesma coisa ocorre. O que pode estar acontecendo nessa situação?**

✅ **Access point invasor (rogue AP)**

---

## Pergunta 19

**Um administrador de rede de uma pequena empresa de publicidade está configurando a segurança da WLAN usando o método WPA2 PSK. Que credencial os usuários do escritório precisam para conectar seus laptops à WLAN?**

✅ **Uma chave que corresponde à chave no AP.**

No modo PSK (Pre-Shared Key), todos compartilham a mesma chave configurada no AP — sem autenticação individual por usuário.

---

## Pergunta 20

**O que é uma característica do modo de descoberta passiva de WLAN?**

✅ **O AP envia periodicamente quadros de beacon contendo o SSID.**

---

## Pergunta 21

**Qual declaração descreve uma VPN?**

✅ **As VPNs usam conexões virtuais para criar uma rede privada por meio de uma rede pública.**

---

## Pergunta 22

**Quais são as duas desvantagens para usar o HIPS? (Escolha duas.)**

✅ **O HIPS tem dificuldade em construir uma imagem precisa da rede ou coordenar eventos que ocorrem em toda a rede.** ✅ **Com o HIPS, o administrador da rede deve verificar o suporte para todos os diferentes sistemas operacionais usados na rede.**

> _Vantagem do HIPS (não desvantagem): consegue acessar tráfego já descriptografado no host, diferente de soluções baseadas em rede._

---

## Pergunta 23

**Qual é a função do SNMP?**

✅ **Fornece um formato de mensagem para comunicação entre gestores de dispositivos de rede e agentes.**

---

## Pergunta 24

**O que é uma assinatura IPS?**

✅ **É um conjunto de regras usadas para detectar atividades intrusivas típicas.**

---

## 📋 Resumo rápido do gabarito

| #   | Resposta                                                                    |
| --- | --------------------------------------------------------------------------- |
| 1   | Hoax                                                                        |
| 2   | Inserção de SQL                                                             |
| 3   | DoS                                                                         |
| 4   | Fraqueza que torna alvo suscetível a ataque                                 |
| 5   | Senhas                                                                      |
| 6   | Controle de acesso impróprio                                                |
| 7   | Hacktivistas→C, Estado→B, Corretores→A                                      |
| 8   | Fraqueza em sistema/design explorável                                       |
| 9   | Soma de verificação do cabeçalho                                            |
| 10  | Sinalização, Deslocamento de fragmento, Identificação                       |
| 11  | Reconhecimento                                                              |
| 12  | Inundação de SYN                                                            |
| 13  | Utilização de recursos→B, Envenenamento de cache→C, Amplificação/reflexão→A |
| 14  | Script entre sites (XSS)                                                    |
| 15  | Criptografia para tráfego confidencial                                      |
| 16  | iFrame carrega página de outra fonte                                        |
| 17  | Solicitação de teste + Beacon                                               |
| 18  | Access point invasor                                                        |
| 19  | Chave que corresponde à do AP                                               |
| 20  | AP envia beacons periodicamente                                             |
| 21  | Conexões virtuais → rede privada sobre rede pública                         |
| 22  | Dificuldade de visão de rede + suporte a múltiplos SOs                      |
| 23  | Formato de mensagem gestor↔agente                                           |
| 24  | Conjunto de regras para detectar atividades intrusivas                      |