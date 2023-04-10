# As redes atualmente
## Componentes de Rede
### Host

Em redes de computadores, um "**host**" se refere a qualquer dispositivo que está conectado à rede e pode enviar ou receber dados através dela. Isso inclui computadores, servidores, roteadores, switches, impressoras e outros dispositivos de rede.
Cada host em uma rede é identificado por um endereço IP exclusivo, que é usado para rotear dados entre os dispositivos. Os hosts também podem executar aplicativos e serviços que podem ser acessados por outros dispositivos na rede, como um servidor web ou de correio eletrônico. 


### Peer-to-Peer

Peer-to-peer (P2P) é um modelo de comunicação em rede em que os dispositivos conectados compartilham recursos diretamente entre si. Nesse modelo, cada dispositivo é tanto um cliente quanto um servidor, permitindo que os recursos (como arquivos, dados ou capacidade de processamento) sejam compartilhados de forma descentralizada entre os usuários da rede.

No P2P, não há um único ponto de falha, já que cada dispositivo na rede é independente e pode continuar a funcionar mesmo que outros dispositivos falhem. Além disso, o P2P pode fornecer maior velocidade de transferência de dados, já que os dispositivos podem se comunicar diretamente sem a necessidade de passar por um servidor intermediário.

O P2P é frequentemente utilizado para compartilhar arquivos entre usuários da Internet, como em redes de compartilhamento de arquivos (como BitTorrent) e em sistemas de compartilhamento de arquivos ponto a ponto (como o eMule). No entanto, o P2P também pode ser usado em outras aplicações, como mensagens instantâneas, videoconferência e jogos em rede.

### End Devices (Dispositivos Finais)

Em redes de computadores, um "end device" (dispositivo final, em português) é qualquer dispositivo que esteja no final da conexão de uma rede e que possa enviar ou receber dados através dela. Isso inclui computadores, laptops, smartphones, tablets, impressoras, scanners, câmeras e outros dispositivos que podem se comunicar com outros dispositivos na rede.

Os end devices também podem ser classificados como clientes ou servidores, dependendo da função que desempenham em uma rede. Por exemplo, um computador ou dispositivo móvel pode ser considerado um cliente se estiver solicitando informações ou serviços de um servidor, enquanto um servidor é um dispositivo que fornece informações ou serviços para outros dispositivos na rede.

### Dispositivos Intermediários

Dispositivos intermediários em redes de computadores são aqueles que fornecem serviços de rede para dispositivos finais, ajudando a encaminhar pacotes de dados pela rede e fornecendo conectividade. Esses dispositivos podem incluir roteadores, switches, hubs, firewalls, controladores de acesso sem fio e outros.

Esses dispositivos usam o endereço do dispositivo final de destino, em conjunto com as informações sobre as interconexões de rede, para determinar o caminho que as mensagens devem percorrer na rede.

Cada tipo de dispositivo intermediário tem funções específicas em uma rede. Por exemplo, um roteador é usado para encaminhar pacotes de dados entre diferentes redes, enquanto um switch é usado para fornecer conectividade entre dispositivos na mesma rede. Já um firewall é usado para controlar o acesso à rede, restringindo o tráfego de entrada e saída com base em regras de segurança pré-definidas.

Os dispositivos intermediários são importantes para garantir que os dispositivos finais possam se comunicar uns com os outros de forma eficiente e segura. Eles também ajudam a melhorar o desempenho da rede, reduzindo o tráfego desnecessário e melhorando a qualidade do serviço.

### Network Media

A mídia fornece o canal pelo qual a mensagem viaja da origem ao destino.

As redes modernas utilizam alguns tipos de mídia para interconectar dispositivos, como:

Cabo de cobre: é o meio mais comum e tradicional de transmissão de dados em redes. Os cabos de cobre são usados em várias tecnologias, como Ethernet, DSL e telefonia, e podem transmitir dados a velocidades de até vários Gbps.

Fibra ótica: é um meio de transmissão de alta velocidade que usa cabos de vidro ou plástico para transmitir dados através de sinais de luz. A fibra ótica é usada em redes de longa distância e pode transmitir dados a velocidades de até vários terabits por segundo.

Wireless (sem fio): é um meio de transmissão que usa ondas de rádio para enviar dados através do ar. As tecnologias sem fio mais comuns incluem Wi-Fi, Bluetooth e NFC. As redes sem fio são amplamente usadas em ambientes domésticos e empresariais.

Satélite: é um meio de transmissão que usa satélites de comunicação para transmitir dados. As tecnologias de satélite são usadas em áreas onde as outras formas de transmissão não são práticas ou não estão disponíveis, como em áreas rurais ou remotas.

A escolha do meio de transmissão depende de fatores como distância, velocidade, custo, disponibilidade, segurança e interferência. É importante avaliar cada um desses fatores para determinar qual meio de transmissão é mais adequado para uma determinada rede.

## Representações de Rede

Um diagrama fornece uma maneira fácil de entender como os dispositivos se conectam em uma rede grande. Esse tipo de “fotografia” de uma rede é conhecido como um diagrama de topologia. A capacidade de reconhecer as representações lógicas dos componentes físicos de rede é crucial para se permitir visualizar a organização e a operação de uma rede.

Além dessas representações, é utilizada terminologia especializada para descrever como cada um desses dispositivos e mídias se conectam:

NIC (Network Interface Card), ou placa de interface de rede em português, é um dispositivo de hardware que permite que um computador se conecte a uma rede. A NIC é geralmente instalada em um slot de expansão na placa-mãe do computador e possui uma ou mais portas físicas para conexão com cabos de rede.

Uma porta física é uma abertura ou conector na NIC que permite conectar um cabo de rede. As portas físicas podem ter diferentes tipos de conectores, como RJ-45 para cabos Ethernet ou LC/SC para cabos de fibra ótica.

Uma interface, por outro lado, é uma abstração de software que permite que o computador se comunique com a rede. Uma interface de rede é criada quando a NIC é instalada e configurada no sistema operacional do computador. Cada interface é identificada por um endereço MAC exclusivo e pode ser configurada com endereços IP, máscaras de sub-rede e outros parâmetros de rede.


### Diagramas de Topologia

- Física: Representam a estrutura física de uma rede, mostrando a localização dos dispositivos de rede, cabos, portas, hubs, switches e outros componentes físicos. Esse tipo de diagrama é útil para planejar e configurar a rede, bem como para identificar problemas de conectividade física.

- Lógica: Representa a estrutura lógica da rede, mostrando como os dados fluem pela rede, incluindo o caminho que os pacotes de dados percorrem, os protocolos de rede usados e outras informações relacionadas à comunicação lógica. Esse tipo de diagrama é útil para entender o fluxo de tráfego de rede, bem como para identificar problemas de desempenho e segurança.


