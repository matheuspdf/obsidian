**Efficiently move large amounts of data** _Mover grandes quantidades de dados eficientemente_ 
– Use a shipping truck _– Use um caminhão de transporte_

**The network topology is the road** _A topologia de rede é a estrada_ 
– Ethernet, DSL, cable system _– Ethernet, DSL, sistema de cabo_

**The truck is the Internet Protocol (IP)** _O caminhão é o Protocolo de Internet (IP)_ 
– We've designed the roads for this truck _– Projetamos as estradas para esse caminhão_

**The boxes hold your data** _As caixas guardam seus dados_ 
– Boxes of TCP and UDP _– Caixas de TCP e UDP_

**Inside the boxes are more things** _Dentro das caixas há mais coisas_ 
– Application information _– Informações de aplicação_


![[Pasted image 20260423212426.png]]

# TCP and UDP

**Transported inside of IP** _Transportado dentro do IP_ 
– Encapsulated by the IP protocol _– Encapsulado pelo protocolo IP_

**Two ways to move data from place to place** _Duas formas de mover dados de um lugar para outro_ – Different features for different applications _– Recursos diferentes para aplicações diferentes_

**OSI Layer 4** _Camada 4 do modelo OSI_ 
– The transport layer _– A camada de transporte_

**Multiplexing** _Multiplexação_ 
– Use many different applications at the same time _– Usar várias aplicações diferentes ao mesmo tempo_ – TCP and UDP _– TCP e UDP_


# TCP – Transmission Control Protocol

**Connection-oriented** _Orientado a conexão_ 
– A formal connection setup and close _– Uma configuração e encerramento formal de conexão_

**"Reliable" delivery** _Entrega "confiável"_ 
– Recovery from errors _– Recuperação de erros_ 
– Can manage out-of-order messages or retransmissions _– Consegue gerenciar mensagens fora de ordem ou retransmissões_

**Flow control** _Controle de fluxo_ 
– The receiver can manage how much data is sent _– O receptor pode gerenciar a quantidade de dados enviada_

# UDP – User Datagram Protocol

**Connectionless** _Sem conexão_ 
– No formal open or close to the connection _– Sem abertura ou encerramento formal de conexão_

**"Unreliable" delivery** _Entrega "não confiável"_ 
– No error recovery _– Sem recuperação de erros_ 
– No reordering of data or retransmissions _– Sem reordenação de dados ou retransmissões_

**No flow control** _Sem controle de fluxo_ 
 – Sender determines the amount of data transmitted _– O remetente determina a quantidade de dados transmitida_

# Why would you ever use UDP?

_Por que você usaria UDP?_

**Real-time communication** _Comunicação em tempo real_ – There's no way to stop and resend the data _– Não há como parar e reenviar os dados_ – Time doesn't stop for your network _– O tempo não para pela sua rede_

**Connectionless protocols** _Protocolos sem conexão_ – DHCP (Dynamic Host Configuration Protocol) _– DHCP (Protocolo de Configuração Dinâmica de Host)_ – TFTP (Trivial File Transfer Protocol) _– TFTP (Protocolo Trivial de Transferência de Arquivos)_

**The data might not get through** _Os dados podem não chegar ao destino_ – The application keeps track and decides what to do _– A aplicação mantém o controle e decide o que fazer_ – It might not do anything _– Pode simplesmente não fazer nada_


# Communication using TCP

_Comunicação usando TCP_

**Connection-oriented protocols prefer a "return receipt"** _Protocolos orientados a conexão preferem um "aviso de recebimento"_ – HTTPS (Hypertext Transfer Protocol Secure) _– HTTPS (Protocolo de Transferência de Hipertexto Seguro)_ – SSH (Secure Shell) _– SSH (Shell Seguro)_

**The application doesn't worry about out of order frames or missing data** _A aplicação não se preocupa com quadros fora de ordem ou dados ausentes_ – TCP handles all of the communication overhead _– O TCP cuida de toda a sobrecarga de comunicação_ – The application has one job _– A aplicação tem apenas uma função_

# Speedy Delivery

_Entrega Rápida_

**The IP delivery truck delivers from one (IP) address to another (IP) address** _O caminhão de entrega IP entrega de um endereço (IP) para outro endereço (IP)_ – Every house has an address, every computer has an IP address _– Toda casa tem um endereço, todo computador tem um endereço IP_

**Boxes arrive at the house / IP address** _As caixas chegam na casa / endereço IP_ – Where do the boxes go? _– Para onde vão as caixas?_ – Each box has a room name _– Cada caixa tem o nome de um cômodo_

**Port is written on the outside of the box** _A porta está escrita na parte externa da caixa_ – Drop the box into the right room _– Entregar a caixa no cômodo correto_


# Lots of Ports

_Muitas Portas_

**IPv4 sockets** _Sockets IPv4_ – Server IP address, protocol, server application port number _– Endereço IP do servidor, protocolo, número de porta da aplicação do servidor_ – Client IP address, protocol, client port number _– Endereço IP do cliente, protocolo, número de porta do cliente_

**Non-ephemeral ports – permanent port numbers** _Portas não efêmeras – números de porta permanentes_ – Ports 0 through 1,023 _– Portas 0 a 1.023_ – Usually on a server or service _– Geralmente em um servidor ou serviço_

**Ephemeral ports – temporary port numbers** _Portas efêmeras – números de porta temporários_ – Ports 1,024 through 65,535 _– Portas 1.024 a 65.535_ – Determined in real-time by the client _– Determinadas em tempo real pelo cliente_

# Port Numbers

_Números de Porta_

**TCP and UDP ports can be any number between 0 and 65,535** _Portas TCP e UDP podem ser qualquer número entre 0 e 65.535_

**Most servers (services) use non-ephemeral (not-temporary) port numbers** _A maioria dos servidores (serviços) usa números de porta não efêmeros (não temporários)_ – This isn't always the case _– Isso nem sempre é o caso_ • It's just a number. _• É apenas um número._

**Port numbers are for communication, not security** _Números de porta servem para comunicação, não para segurança_

**Service port numbers need to be "well known"** _Números de porta de serviço precisam ser "bem conhecidos"_

**TCP port numbers aren't the same as UDP port numbers** _Números de porta TCP não são os mesmos que números de porta UDP_


# Ports on the Network

_Portas na Rede_

**Web server - tcp/80** _Servidor Web - tcp/80_ **VoIP server - udp/5004** _Servidor VoIP - udp/5004_ **Email server - tcp/143** _Servidor de E-mail - tcp/143_

---

Representação da ilustração:

```
Client (10.0.0.1)                                    Server (10.0.0.2)

┌────────────┬────┬─────┬───────────────┬───────────────────────┐
│ Eth Header │ IP │ TCP │   HTTP data   │  Ethernet Trailer     │
└────────────┴────┴─────┴───────────────┴───────────────────────┘

┌────────────┬────┬─────┬───────────────┬───────────────────────┐
│ Eth Header │ IP │ UDP │   VoIP data   │  Ethernet Trailer     │
└────────────┴────┴─────┴───────────────┴───────────────────────┘

┌────────────┬────┬─────┬───────────────┬───────────────────────┐
│ Eth Header │ IP │ TCP │   Email data  │  Ethernet Trailer     │
└────────────┴────┴─────┴───────────────┴───────────────────────┘
```


# Ports on the Network – Detalhe dos Pacotes

_Detalhamento dos endereços e portas em cada pacote_

```
Client (10.0.0.1)                                          Server (10.0.0.2)

┌──────────────────────┬───────────────────────┬─────────────┐
│ Source IP = 10.0.0.1 │ TCP Source Port = 3000│             │
│ Dest IP   = 10.0.0.2 │ TCP Dest Port   = 80  │  HTTP data  │
└──────────────────────┴───────────────────────┴─────────────┘

┌──────────────────────┬───────────────────────┬─────────────┐
│ Source IP = 10.0.0.1 │ UDP Source Port = 7100│             │
│ Dest IP   = 10.0.0.2 │ UDP Dest Port   = 5004│  VoIP data  │
└──────────────────────┴───────────────────────┴─────────────┘

┌──────────────────────┬───────────────────────┬─────────────┐
│ Source IP = 10.0.0.1 │ TCP Source Port = 4407│             │
│ Dest IP   = 10.0.0.2 │ TCP Dest Port   = 143 │ Email data  │
└──────────────────────┴───────────────────────┴─────────────┘
```

> **Nota:** A porta de origem (source port) é efêmera — gerada pelo cliente. A porta de destino (dest port) é a porta conhecida do serviço no servidor.