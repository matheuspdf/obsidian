
# Switch básico e configuração de dispositivo final

**Objetivo do módulo:** Implementar as configurações iniciais, incluindo senhas, endereçamento IP e parâmetros de gateway padrão em um switch de rede e em dispositivos finais.

| Título do Tópico | Objetivo do Tópico |
|---|---|
| **Acesso ao Cisco IOS** | Explicar como acessar um dispositivo Cisco IOS para fins de configuração. |
| **Navegação IOS** | Explicar como navegar no Cisco IOS para configurar os dispositivos de rede. |
| **A estrutura de comandos** | Descrever a estrutura de comandos do software Cisco IOS. |
| **Configuração básica de dispositivos** | Configurar um dispositivo Cisco IOS usando CLI. |
| **Salvar configurações** | Usar os comandos do IOS para salvar a configuração atual. |
| **Portas e endereços** | Explicar como os dispositivos se comunicam no meio físico de rede. |
| **Configurar endereços IP** | Configurar um dispositivo de host com um endereço IP. |
| **Verificar a conectividade** | Verificar a conectividade entre dois dispositivos finais. |

### Sistema operacional:

Shell: a interface de usuário que permite que os usuário solicitem tarefas específicas do computador.

Kernel: comunicação entre software e hardware. Gerencia recursos de hardware para atender a requisitos de software.

Hardware: parte física.

---

**GUI** _Graphical User Interface_ (Interface Gráfica do Usuário): permite que o usuário interaja com o sistema usando um abiente de ícones gráficos, menus e janelas.

**CLI** _Command-Line Interface_ (Interface de Linha de Comando): permite que o usuário execute comandos baseados em texto num shell.

---

## Métodos de acesso (acesso ao Cisco IOS)

- Por padrão, o primeiro acesso a ser realizado num switch cisco é via **Console**, uma porta física de gerenciamento usada para acessar um dispositivo para fornecer manutenção, como executar as configurações inciais.
- Shell segura (SSH) -  estabelece uma conexão CLI segura remota com um dispositivo, por meio de uma interface virtual em uma rede.
- Telnet - estabelece uma conexão CLI remota insegura a um dispositivo através da rede.

### Programa de emulação de terminal
- programas de emulação de terminal são usados para se conectar a um dispositivo de rede por uma porta de console ou por uma conexão SSH/Telnet
- Existem vários programas de emulação de terminal para escolher, como PuTTY, Tera Term e SecureCRT.

## Modos de comando primários

Modo EXEC do usuário
- permite acesso a apenas um número limitado de comandos básicos de monitoramento
- identificao pelo prompt da CLI que termina como símbolo >

Modo EXEC com privilégios:
- permite acesso a todos os comandos e recursos
- identificado pelo prompt da CLI que termina com o símbolo #️

## Modo de configuração de navegação IOS e modos de subconfiguraçào

**Modo de configuração global**
- usado para acessar opções de configuração no dispositivo

**Modo de configuraçào de linhas**
- usado para configurar o acesso ao console, SSH, Telnet ou AUX

**Modo de configuração de interface**
- usado para configurar uma porta de switch ou interface de roteador

26:42