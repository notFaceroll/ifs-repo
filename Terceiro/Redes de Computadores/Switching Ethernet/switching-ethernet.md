# Switching Ethernet

> A Ethernet é uma das duas tecnologias de LAN usadas atualmente, sendo a outra LANs sem fio (WLANs). A Ethernet utiliza comunicações com fios, incluindo par trançado, ligações de fibra óptica e cabos coaxiais.

## Quadros Ethernet

A Ethernet é uma tecnologia de camada de enlace de dados que permite a comunicação entre dispositivos conectados à mesma rede local. Ela usa um cabo de cobre ou fibra óptica para transmitir dados entre dispositivos e foi padronizada pelo Institute of Electrical and Electronics Engineers (IEEE) como a família de padrões IEEE 802.3.

A Ethernet suporta larguras de banda de dados:

- 10 Mbps
- 100 Mbps
- 1000 Mbps (1 Gbps)
- 10,000 Mbps (10 Gbps)
- 40,000 Mbps (40 Gbps)
- 100,000 Mbps (100 Gbps)

## Subcamadas de Enlace de Dados

A subcamada **LLC** (Logical Link Control) se comunica entre o software de rede nas camadas superiores e o hardware do dispositivo nas camadas inferiores. Ela coloca a informação no quadro que identifica qual protocolo de camada de rede está sendo usado para o quadro.

A subcamada **MAC** (Media Access Control) é responsável pelo encapsulamento de dados e acesso ao meio físico, ou seja, ela controla a maneira como os dispositivos compartilham o meio para transmitir e receber quadros de dados. O MAC define regras para acesso ao meio compartilhado e como os dispositivos resolvem colisões de quadros que ocorrem quando dois ou mais dispositivos tentam transmitir ao mesmo tempo. Ele também fornece endereçamento físico exclusivo para cada dispositivo em uma rede, conhecido como endereço MAC.

O encapsulamento de dados IEEE 802.3 inclui o seguinte:

- Quadro Ethernet - Estrutura interna do quadro Ethernet.
- Endereçamento Ethernet - O quadro Ethernet inclui um endereço MAC de origem e de destino para fornecer o quadro Ethernet da NIC Ethernet para a NIC Ethernet na mesma LAN.
- Detecção de erro Ethernet - O quadro Ethernet inclui um trailer de sequência de verificação de quadros (FCS) usado para detecção de erros.

Ethernet herdada usando uma topologia de barramento ou hubs, é um meio compartilhado e half-duplex. Ethernet sobre um meio half-duplex usa um método de acesso baseado em contenção, detecção de múltiplos acessos/detecção de colisão (CSMA/CD).

As LANs Ethernet de hoje usam switches que operam em full-duplex. As comunicações full-duplex com switches Ethernet não exigem controle de acesso através do CSMA/CD.

### Campos de um quadro Ethernet

O tamanho mínimo de quadro Ethernet é 64 bytes e o máximo é 1518 bytes, incluindo todos os bytes do campo de endereço MAC de destino através do campo FCS (Frame Check Sequence).

O campo de preâmbulo não é incluído no tamanho do quadro.

Quadros com tamanhos maiores ou menores que esses limites são descartados pelos dispositivos receptores dos quadros.

### Detalhes dos campos do quadro Ethernet

- **Preâmbulo (7 bytes) e SFD (1 byte)** - São usados para sincronização entre os dispositivos de envio e recepção
- **Endereço MAC de destino (6 bytes)** - Identificador do destino desejado;
- **Endereço MAC de origem (6 bytes)** - Identifica a NIC ou interface de origem do quadro;
- **Tipo / Comprimento (2 bytes)** - Identifica o protocolo da camada superior encapsulado em o quadro Ethernet;
- **Dados (46 ~ 1500 bytes)** - Contém os dados encapsulados de uma camada superior (PDU de camada 3 genérica ou IPv4 pacote);
- **FCS (4 bytes)** - Detecção de erros no quadro.

## Endereços MAC

### Endereços MAC e Hexadecimal

Um endereço MAC Ethernet consiste em um valor binário de 48 bits. Hexadecimal é usado para identificar um endereço Ethernet porque um único dígito hexadecimal representa quatro bits binários. Portanto, um endereço MAC Ethernet de 48 bits pode ser expresso usando apenas 12 valores hexadecimais.

> Como um byte é igual a 8 bits, também podemos dizer que um endereço MAC tem 6 bytes de comprimento.

Quando um fornecedor atribui um endereço MAC a um dispositivo ou interface Ethernet, o fornecedor deve fazer o seguinte:

- Use sua OUI atribuída como os primeiros 6 dígitos hexadecimais.
- Atribua um valor exclusivo nos últimos 6 dígitos hexadecimais.

### Endereço MAC Unicast

Na Ethernet, são utilizados diferentes endereços MAC para comunicação unicast, broadcast e multicast da Camada 2.

Um endereço MAC de unicast é o endereço exclusivo usado quando um quadro é enviado de um único dispositivo de transmissão para um único dispositivo de destino.

> O endereço MAC de origem deve ser sempre unicast.

O processo de determinar o endereço MAC de destino associado a um endereço IP (tanto IPv4 quanto IPv6) envolve o uso de diferentes protocolos em cada caso.

No caso do IPv4, o processo de resolução do endereço MAC de destino é chamado de ARP (Address Resolution Protocol). O ARP é responsável por mapear endereços IP para endereços MAC em uma rede local. Quando um host de origem precisa enviar um pacote para um endereço IP específico dentro da mesma rede local, ele verifica a tabela ARP local para encontrar o endereço MAC correspondente. Se o endereço MAC não estiver na tabela ARP, o host de origem envia uma solicitação ARP broadcast na rede local, perguntando qual dispositivo possui o endereço IP desejado. O dispositivo com o endereço IP correspondente responde com seu endereço MAC, e então o host de origem atualiza sua tabela ARP com essa informação.

No caso do IPv6, o processo de resolução do endereço MAC de destino é chamado de NDP (Neighbor Discovery Protocol). O NDP é um protocolo usado para várias funções em redes IPv6, incluindo a resolução de endereço. Quando um host de origem precisa determinar o endereço MAC de destino associado a um endereço IPv6, ele usa uma combinação de mensagens ICMPv6 (Internet Control Message Protocol version 6) para realizar a resolução. O NDP emprega mensagens chamadas "Neighbor Solicitation" (Solicitação de Vizinhança) para descobrir o endereço MAC associado a um determinado endereço IPv6 na rede local. O dispositivo de destino responde com uma mensagem "Neighbor Advertisement" (Anúncio de Vizinhança) contendo seu endereço MAC.

Portanto, o processo de determinar o endereço MAC de destino associado a um endereço IPv4 envolve o protocolo ARP, enquanto no caso do IPv6, é o protocolo NDP que desempenha essa função.

### Endereço MAC Broadcast

O endereço MAC de broadcast tem um formato específico e é representado como uma sequência de seis pares de dígitos hexadecimais (por exemplo, FF:FF:FF:FF:FF:FF). Esse endereço é utilizado na camada de enlace de dados para enviar pacotes que devem ser entregues a todos os dispositivos conectados à rede local.

O uso mais comum do endereço MAC de broadcast é para a descoberta de dispositivos na rede, como por exemplo, quando um dispositivo precisa descobrir outros dispositivos disponíveis ou anunciar sua presença na rede. Além disso, protocolos como o ARP (Address Resolution Protocol) e NDP (Neighbor Discovery Protocol) também utilizam o endereço MAC de broadcast para solicitar informações sobre os dispositivos na rede local.

### Endereço MAC Multicast

 Diferentemente do endereço MAC de broadcast, que envia pacotes para todos os dispositivos na rede local, o endereço MAC de multicast é usado para enviar pacotes para um grupo específico de dispositivos interessados em receber esse tipo de tráfego.

Um endereço MAC de multicast também é representado por uma sequência de seis pares de dígitos hexadecimais. Os endereços MAC de multicast começam com um prefixo específico, que indica que se trata de um endereço de multicast. Dessa forma, os dispositivos de rede podem identificar que um pacote é destinado a um grupo de dispositivos em vez de ser um pacote de broadcast.

Quando um dispositivo deseja enviar pacotes para um grupo de dispositivos interessados em receber esse tráfego, ele utiliza o endereço MAC de multicast correspondente a esse grupo. Ao enviar um pacote para esse endereço, o switch ou roteador encaminha o pacote apenas para os dispositivos que estão explicitamente inscritos no grupo de multicast correspondente.

## A Tabela de Endereços MAC

### Noções Básicas sobre Switches

- Toma suas decisões de encaminhamento com base apenas nos endereços MAC Ethernet da camada 2;

- Desconhece completamente os dados (protocolo) que estão sendo transportados na parte de dados do quadro;

- Examina a tabela de endereços MAC para tomar uma decisão de encaminhamento para cada quadro, ao contrário dos hubs Ethernet herdados que repetem bits em todas as portas, exceto a porta de entrada.

### Aprendizado de endereços MAC

Um switch cria a tabela de endereços MAC, também conhecida como tabela de comutação (switching table), por meio de um processo chamado aprendizado de endereços MAC (MAC learning). O switch monitora o tráfego de rede em todas as suas portas para determinar quais dispositivos estão conectados a cada porta e qual endereço MAC pertence a cada dispositivo.

Quando um pacote de dados é recebido em uma porta específica do switch, ele verifica o endereço MAC de origem do pacote. O switch registra esse endereço MAC juntamente com o número da porta em sua tabela de comutação. Ele associa o endereço MAC do dispositivo que enviou o pacote à porta física pela qual o pacote foi recebido. Isso é feito para cada pacote recebido em todas as portas do switch.

Dessa forma, à medida que o switch continua recebendo pacotes de diferentes dispositivos, ele atualiza sua tabela de comutação, adicionando novos endereços MAC e suas respectivas portas de origem. Se o switch já tiver registrado um endereço MAC em sua tabela, ele atualiza a entrada da tabela com a nova porta de origem.

Quando o switch precisa encaminhar um pacote para um endereço MAC de destino, ele consulta sua tabela de comutação para encontrar o endereço MAC na tabela e identificar a porta associada a esse endereço. Se o endereço MAC de destino estiver na tabela, o switch encaminha o pacote apenas para a porta associada a esse endereço MAC, permitindo que o pacote alcance diretamente o dispositivo de destino.

No entanto, se o endereço MAC de destino não estiver presente na tabela de comutação do switch, ele trata o pacote como um pacote de broadcast. Nesse caso, o switch encaminha o pacote para todas as suas portas, exceto a porta pela qual o pacote foi recebido. Isso permite que o pacote alcance todos os dispositivos conectados ao switch, incluindo o dispositivo de destino correto, que, por sua vez, responde ao pacote.

É importante destacar que a tabela de comutação do switch é dinâmica e pode ser atualizada à medida que novos dispositivos são conectados ou desconectados da rede. Isso permite que o switch acompanhe as mudanças na rede e encaminhe corretamente os pacotes para os dispositivos conectados.

### Métodos de encaminhamento e velocidades

Os switches usam um dos seguintes métodos de encaminhamento para o switching (comutação) de dados entre suas interfaces de rede:

- Switching store-and-forward - Este método de encaminhamento de quadros recebe o quadro inteiro e calcula o CRC. Se o CRC é válido, o switch procura o endereço de destino, que determina a interface de saída. Em seguida, o quadro é encaminhado para fora da porta correta. Quando um erro é detectado em um quadro, o switch o descarta. O descarte de quadros com erros reduz o consumo de largura de banda por dados corrompidos.

- Switching cut-through - Esse método de encaminhamento de quadros encaminha o quadro antes de ser totalmente recebido. Pelo menos o endereço de destino do quadro deve ser lido para que o quadro possa ser encaminhado. O switch armazena em buffer apenas o quadro suficiente para ler o endereço MAC de destino, para que possa determinar para qual porta deve encaminhar os dados. Não realiza nenhuma verificação de erros no quadro.
  - Fast-forward - Oferece o menor nível de latência. e encaminha imediatamente um pacote depois de ler o endereço de destino. Como o switching fast-forward começa o encaminhamento antes de receber todo o pacote, alguns pacotes podem ser retransmitidos com erros. Isso ocorre com pouca frequência e a NIC de destino descarta o pacote com defeito após o recebimento.
  - Fragment-free - O switch armazena os primeiros 64 bytes do quadro antes de encaminhar. O motivo dele armazenar somente os primeiros 64 bytes do quadro é que a maioria dos erros e das colisões de rede ocorre durante esses bytes. Ele executa uma pequena verificação de erros nos primeiros 64 bytes do quadro para garantir que não ocorra uma colisão antes de encaminhar o quadro. 

> Alguns switches são configurados para executar o switching cut-through por porta até que um limite de erro definido pelo usuário seja atingido e, depois, mudam automaticamente para store-and-forward. Quando a taxa de erros fica abaixo do limite, a porta retorna automaticamente para o switching cut-through.

### Buffers de Memória em Switches

- Memória por porta
- Memória compartilhada