# As redes atualmente

## Index
- [<- Página Inicial](../README.md)
- [Componentes de Rede](#componentes-de-rede)
- [Representações de Rede](#representações-de-rede)
- [Tipos comuns de Redes](#tipos-comuns-de-redes)
- [Conexões com a Internet](#conexões-com-a-internet)
- [Redes Confiáveis](#redes-confiáveis)
- [Tendências das Redes](#tendências-das-redes)

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

- Cabo de cobre: é o meio mais comum e tradicional de transmissão de dados em redes. Os cabos de cobre são usados em várias tecnologias, como Ethernet, DSL e telefonia, e podem transmitir dados a velocidades de até vários Gbps.

- Fibra ótica: é um meio de transmissão de alta velocidade que usa cabos de vidro ou plástico para transmitir dados através de sinais de luz. A fibra ótica é usada em redes de longa distância e pode transmitir dados a velocidades de até vários terabits por segundo.

- Wireless (sem fio): é um meio de transmissão que usa ondas de rádio para enviar dados através do ar. As tecnologias sem fio mais comuns incluem Wi-Fi, Bluetooth e NFC. As redes sem fio são amplamente usadas em ambientes domésticos e empresariais.

- Satélite: é um meio de transmissão que usa satélites de comunicação para transmitir dados. As tecnologias de satélite são usadas em áreas onde as outras formas de transmissão não são práticas ou não estão disponíveis, como em áreas rurais ou remotas.

A escolha do meio de transmissão depende de fatores como distância, velocidade, custo, disponibilidade, segurança e interferência. É importante avaliar cada um desses fatores para determinar qual meio de transmissão é mais adequado para uma determinada rede.

## Representações de Rede

Um diagrama fornece uma maneira fácil de entender como os dispositivos se conectam em uma rede grande. Esse tipo de “fotografia” de uma rede é conhecido como um diagrama de topologia. A capacidade de reconhecer as representações lógicas dos componentes físicos de rede é crucial para se permitir visualizar a organização e a operação de uma rede.

Além dessas representações, é utilizada terminologia especializada para descrever como cada um desses dispositivos e mídias se conectam:

- NIC (Network Interface Card), ou placa de interface de rede em português, é um dispositivo de hardware que permite que um computador se conecte a uma rede. A NIC é geralmente instalada em um slot de expansão na placa-mãe do computador e possui uma ou mais portas físicas para conexão com cabos de rede.

- Uma porta física é uma abertura ou conector na NIC que permite conectar um cabo de rede. As portas físicas podem ter diferentes tipos de conectores, como RJ-45 para cabos Ethernet ou LC/SC para cabos de fibra ótica.

- Uma interface, por outro lado, é uma abstração de software que permite que o computador se comunique com a rede. Uma interface de rede é criada quando a NIC é instalada e configurada no sistema operacional do computador. Cada interface é identificada por um endereço MAC exclusivo e pode ser configurada com endereços IP, máscaras de sub-rede e outros parâmetros de rede.


### Diagramas de Topologia

- Física: Representam a estrutura física de uma rede, mostrando a localização dos dispositivos de rede, cabos, portas, hubs, switches e outros componentes físicos. Esse tipo de diagrama é útil para planejar e configurar a rede, bem como para identificar problemas de conectividade física.

- Lógica: Representa a estrutura lógica da rede, mostrando como os dados fluem pela rede, incluindo o caminho que os pacotes de dados percorrem, os protocolos de rede usados e outras informações relacionadas à comunicação lógica. Esse tipo de diagrama é útil para entender o fluxo de tráfego de rede, bem como para identificar problemas de desempenho e segurança.


## Tipos comuns de Redes

Existem vários tipos de redes de computadores, cada uma com suas próprias características e finalidades. Alguns dos tipos de redes incluem:

- LAN (Local Area Network): uma rede local que abrange uma área geográfica limitada, como um escritório, um edifício ou um campus universitário.

- WAN (Wide Area Network): uma rede de longa distância que abrange uma área geográfica maior, como uma cidade, um país ou até mesmo vários continentes.

- WLAN (Wireless Local Area Network): uma rede local que usa tecnologia sem fio para conectar dispositivos, permitindo que os usuários se conectem à rede sem a necessidade de cabos.

- MAN (Metropolitan Area Network): uma rede de computadores que abrange uma área metropolitana, como uma cidade ou um subúrbio.

- CAN (Campus Area Network): uma rede de computadores que conecta várias redes locais em um campus universitário, por exemplo.

- VPN (Virtual Private Network): uma rede que permite que usuários remotos se conectem a uma rede privada através de uma conexão segura pela internet.

- SAN (Storage Area Network): uma rede usada para conectar dispositivos de armazenamento, como discos rígidos e dispositivos de armazenamento em rede.

- VoIP (Voice over IP) Network: uma rede que permite que usuários realizem chamadas de voz sobre uma rede IP, em vez de usar a rede telefônica tradicional.

Esses são apenas alguns dos tipos mais comuns de redes de computadores. Cada tipo de rede tem suas próprias características e finalidades específicas, dependendo das necessidades do usuário ou organização. 
A internet é a maior rede existente. Na verdade, o termo Internet significa uma “rede de redes”. É uma coleção de redes públicas e privadas interconectadas.

Os dois tipos mais comuns de infraestruturas de rede são as redes locais (LANs) e as redes de longa distância (WANs). 

### LANs e WANs


#### Local Area Network (LAN)
- LANs interconectam dispositivos finais em uma área limitada, como uma casa, uma escola, um edifício de escritórios ou um campus.
- Uma LAN é geralmente administrada por uma única organização ou pessoa. O controle administrativo é imposto no nível da rede e governa as políticas de segurança e controle de acesso.
- As LANs fornecem largura de banda de alta velocidade para dispositivos finais internos e dispositivos intermediários,

#### Wide Area Network (WAN)
- Interconectam as LANs em grandes áreas geográficas, como entre cidades, estados, províncias, países ou continentes.
- São geralmente administradas por vários prestadores de serviço.
- Geralmente fornecem links de velocidade mais lenta entre as LANs.

### Intranets e Extranets

Intranet é uma rede privada que é usada por uma organização para compartilhar informações internamente, como documentos, comunicações, recursos e aplicativos. Pode ser acessada apenas pelos funcionários ou membros da organização e geralmente é protegida por firewall para garantir a segurança e a privacidade dos dados.

Já a Extranet é uma extensão da Intranet que permite que pessoas ou organizações externas se conectem a ela e acessem informações ou serviços limitados, com permissões controladas pela organização. A Extranet é protegida por sistemas de autenticação e criptografia de dados para garantir a segurança das informações compartilhadas entre a organização e os usuários externos.

A principal diferença entre Intranet e Extranet é que a Intranet é uma rede interna privada, enquanto a Extranet é uma rede privada estendida a usuários ou organizações externas autorizadas. Ambas as redes são importantes para facilitar a comunicação e o compartilhamento de informações dentro e fora de uma organização, mantendo a segurança e a privacidade dos dados.


## Conexões com a Internet
### Tecnologia de Acesso à Internet

Usuários domésticos, trabalhadores remotos e pequenos escritórios geralmente exigem uma conexão com um ISP (Internet Service Provider) para acessar a Internet. As opções de conexão variam muito entre os ISPs e as localizações geográficas. No entanto, as opções populares incluem banda larga a cabo, a banda larga via DSL (Digital Subscriber Line), WANs sem fio e serviços de telefonia móvel celular.

As organizações geralmente precisam acessar outros sites corporativos e a Internet. Conexões rápidas são necessárias para dar suporte a serviços comerciais que incluem telefones IP, videoconferência e armazenamento em data center. As controladoras oferecem interconexões de nível empresarial. Os serviços populares de nível empresarial incluem DSL, linhas dedicadas e Metro Ethernet.

Alguns dos tipos mais comuns, dentre diversas tecnologias de acesso à internet disponíveis são:

- Linha discada (dial-up): utiliza a rede telefônica para conectar o computador à internet. É uma tecnologia de acesso lenta e obsoleta, que já foi muito utilizada no passado.

- ADSL: utiliza a linha telefônica para transmitir dados de alta velocidade. É uma tecnologia comum em áreas urbanas e subúrbios.

- Cabo: utiliza uma conexão de cabo coaxial para transmitir dados de alta velocidade. É uma tecnologia comum em áreas urbanas e subúrbios.

- Fibra óptica: utiliza cabos de fibra óptica para transmitir dados em alta velocidade. É a tecnologia mais rápida disponível atualmente, mas sua disponibilidade é limitada.

- Satélite: utiliza um satélite para transmitir dados de e para o computador. É uma tecnologia comum em áreas rurais e remotas.

- Wireless: utiliza uma conexão sem fio, como Wi-Fi ou 4G, para se conectar à internet. É uma tecnologia comum em áreas urbanas e subúrbios.

E para corporações:

- Linhas dedicadas: empresas podem contratar uma linha dedicada de alta velocidade para se conectar à internet. Essas linhas são geralmente caras, mas oferecem alta disponibilidade e garantia de banda larga.

- MPLS: MPLS é uma tecnologia de rede que permite que empresas criem redes privadas virtuais (VPNs) para conectar seus escritórios, data centers e filiais à internet. Essa tecnologia oferece alta segurança e desempenho.

- SD-WAN: Software-defined Wide Area Network (SD-WAN) é uma tecnologia de rede que permite que empresas conectem suas filiais, escritórios e data centers à internet usando conexões de internet públicas. Essa tecnologia oferece alta disponibilidade e desempenho, reduzindo custos em relação a linhas dedicadas.

- Metro Ethernet: é uma tecnologia de rede de alta velocidade que usa Ethernet para fornecer serviços de conectividade entre edifícios em uma área metropolitana. É uma solução escalável e flexível, oferecendo largura de banda ajustável e entrega de pacotes confiável para empresas.

- DSL de negócios: é um serviço de internet de alta velocidade projetado especificamente para empresas. O DSL de negócios oferece maior largura de banda e confiabilidade do que a linha discada tradicional, usando tecnologias de modem DSL para transmitir dados por meio da linha telefônica existente da empresa.

### Redes Covergentes

Redes convergentes são redes que unificam serviços de voz, vídeo e dados em uma única infraestrutura de rede. Essas redes são projetadas para fornecer um ambiente de rede mais eficiente, escalável e flexível, permitindo que as organizações reduzam custos, simplifiquem a manutenção e melhorem a colaboração.

As redes convergentes geralmente utilizam o Protocolo de Internet (IP) como tecnologia central, permitindo que os dados sejam transmitidos de forma mais rápida e eficiente. Além disso, as redes convergentes podem ser usadas para suportar tecnologias de comunicação unificada, como telefonia IP, videoconferência e mensagens instantâneas, proporcionando uma experiência de comunicação mais integrada e eficiente para os usuários.


## Redes Confiáveis

### Arquitetura de redes

Quatro características de extrema importância na arquitetura de software podem ser reconhecidas como:

- Tolerância a falhas: a capacidade da rede de continuar operando mesmo quando ocorrem falhas em algum dos seus componentes. Isso inclui redundância, balanceamento de carga e failover para garantir que a rede continue a funcionar mesmo em caso de problemas.

- Escalabilidade: a capacidade da rede de suportar um aumento no número de usuários, dispositivos e aplicativos sem comprometer o desempenho ou a segurança da rede. Isso pode incluir a adição de hardware e software, como servidores, roteadores e switches, bem como o aumento da largura de banda disponível.

- Qualidade de serviço (QoS): a capacidade da rede de priorizar o tráfego de dados com base em sua importância para a organização. Isso pode incluir a priorização de voz e vídeo sobre tráfego de dados menos críticos, para garantir que essas aplicações tenham desempenho adequado.

- Segurança: a proteção da rede contra ameaças internas e externas, incluindo acesso não autorizado, malware, vírus e outras formas de ataque. Isso pode incluir a autenticação, criptografia e firewalls, bem como políticas de segurança e treinamento de usuários.

## Tendências das Redes

À medida que novas tecnologias e dispositivos do usuário final chegam ao mercado, as empresas e os consumidores devem continuar se ajustando a esse ambiente em constante mudança. Existem várias tendências de rede que afetam organizações e consumidores:

- BYOD (Bring Your Own Device):

BYOD (Bring Your Own Device) é uma tendência crescente na qual os funcionários trazem seus próprios dispositivos, como laptops, smartphones e tablets, para o ambiente de trabalho e os usam para acessar dados corporativos e aplicativos. Isso pode melhorar a produtividade e reduzir os custos de hardware, mas também pode criar desafios de segurança, gerenciamento e compatibilidade.

- Colaboração on-line:

Equipes distribuídas geograficamente trabalham juntas em projetos por meio de ferramentas de comunicação e colaboração on-line, como videoconferência, compartilhamento de arquivos e mensagens instantâneas. Isso permite uma maior flexibilidade e produtividade para as equipes, mas também pode exigir uma infraestrutura de rede robusta e segura.

- Comunicação por vídeo:

Tendência cada vez mais popular para comunicações empresariais, incluindo videoconferências, webinars, treinamentos on-line e apresentações virtuais. Isso pode melhorar a comunicação e colaboração em equipe, permitir a conexão remota com clientes e parceiros e reduzir custos com viagens e deslocamentos.

- Computação em nuvem:

Os recursos de hardware e software são fornecidos como serviços através da Internet, permitindo que as empresas acessem recursos sob demanda e paguem apenas pelo que usam. Isso pode reduzir custos de infraestrutura, melhorar a flexibilidade e a escalabilidade da empresa, e permitir que as equipes acessem e colaborem em dados e aplicativos de qualquer lugar com acesso à internet. No entanto, a computação em nuvem também pode trazer desafios de segurança e privacidade de dados, além de depender da qualidade e disponibilidade da conexão de internet.

### IoT (Internt of Things)

Considerada uma "tendência caseira", a tecnologia de casa inteligente se integra aos aparelhos diários, que podem ser conectados a outros dispositivos para tornar os aparelhos mais “inteligentes” ou automatizados, isso pode incluir termostatos inteligentes, luzes, eletrodomésticos, sistemas de segurança e muito mais.

### Rede Powerline

A rede "powerline" é uma tecnologia que permite que a rede doméstica utilize a rede elétrica existente para transmitir dados. Em outras palavras, em vez de usar cabos de rede ou Wi-Fi, a conexão de internet é transmitida pela rede elétrica da casa. Isso pode ser útil em situações em que o sinal Wi-Fi é fraco ou inexistente em certas partes da casa.

### Banda larga sem fio

A banda larga sem fio é uma tendência em que as redes sem fio são usadas para fornecer conexões de internet mais rápidas e confiáveis ​​para residências. Isso pode incluir tecnologias como 5G, Wi-Fi 6 e Wi-Fi mesh, que oferecem velocidades de download e upload mais rápidas, menor latência e melhor cobertura em comparação com tecnologias sem fio anteriores.