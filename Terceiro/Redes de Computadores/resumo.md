# Resumo do resumo

## Introdução

### Componentes de rede:

- **Host** é qualquer dispositivo conectado a uma rede que pode ser endereçado e enviar ou receber dados.
- **Peer-to-peer** (P2P) é um modelo de comunicação em rede em que os dispositivos conectados compartilham recursos diretamente entre si, sem a necessidade de um servidor central.
- "**End device**" é um dispositivo final em uma rede de computadores que pode enviar ou receber dados e executar aplicativos ou serviços.
- **Dispositivos intermediários** são componentes que fornecem serviços de rede para dispositivos finais, ajudando a encaminhar pacotes de dados e fornecer conectividade. Eles são essenciais para garantir a eficiência e segurança da rede.
- **Network Media** (ou mídia de rede) são meios por onde as informações são transmitidas: cabos de cobre, fibra ótica, wireless, satélite, etc.


### Representações de rede:

- NIC é um dispositivo de hardware que permite que um computador se conecte a uma rede.
- Uma porta física é uma abertura ou conector na NIC que permite conectar um cabo de rede. 
- Interface são portas especializadas em um dispositivo de rede que se conectam a redes individuais
- Diagramas de Topologia:
  - Física -> Localização física dos dispositivos intermediários e a instalação dos cabos;
  - Lógica -> Dispositivos, portas e o esquema de endereçamento da rede.


### Tipos comuns de rede

- Uma LAN é uma infraestrutura de rede que abrange uma pequena área geográfica.
- Uma WAN é uma infraestrutura de rede que abrange uma ampla área geográfica. As WANs geralmente são gerenciadas por provedores de serviços (SPs) ou provedores de serviços de Internet (ISPs).

### Intranets e Extranets

- Intranet é uma rede privada que usada por uma organização para compartilhar informações internamente, podendo ser acessada somente pelos funcionários ou membros da organização.
- Extranet é uma extensão da Intranet que permite que pessoas ou organizações externas se conectem a ela e acessem informações ou serviços limitados, com permissões controladas pela organização.

### Conexões com a Internet

Para usuários domésticos:

- Linha discada (dial-up): utiliza a rede telefônica para conectar o computador à internet. É uma tecnologia de acesso lenta e obsoleta, que já foi muito utilizada no passado.
- ADSL: utiliza a linha telefônica para transmitir dados de alta velocidade. É uma tecnologia comum em áreas urbanas e subúrbios.
- Cabo: utiliza uma conexão de cabo coaxial para transmitir dados de alta velocidade. É uma tecnologia comum em áreas urbanas e subúrbios.
- Fibra óptica: utiliza cabos de fibra óptica para transmitir dados em alta velocidade. É a tecnologia mais rápida disponível atualmente, mas sua disponibilidade é limitada.
- Satélite: utiliza um satélite para transmitir dados de e para o computador. É uma tecnologia comum em áreas rurais e remotas.
- Wireless: utiliza uma conexão sem fio, como Wi-Fi ou 4G, para se conectar à internet. É uma tecnologia comum em áreas urbanas e subúrbios.


Para corporações:

- Linha alugada dedicada: é uma conexão de alta velocidade ponto a ponto entre dois pontos geograficamente distintos. É uma linha de comunicação exclusiva para uso de uma organização.
- Metro Ethernet: é uma tecnologia de rede de alta velocidade que usa Ethernet para fornecer serviços de conectividade entre edifícios em uma área metropolitana.
- DSL de negócios: é um serviço de internet de alta velocidade projetado especificamente para empresas. 

Redes Covergentes:
- São redes que unificam serviços de voz, vídeo e dados em uma única infraestrutura de rede baseada em IP. Essas redes oferecem maior eficiência, escalabilidade e flexibilidade, permitindo que as organizações reduzam custos e melhorem a colaboração.

### Redes Confiáveis

Características importantes para um arquiteto de software:

- Tolerância a falhas: a capacidade da rede de continuar operando mesmo quando ocorrem falhas em algum dos seus componentes.
- Escalabilidade: a capacidade da rede de suportar um aumento no número de usuários, dispositivos e aplicativos sem comprometer o desempenho ou a segurança da rede.
- Qualidade de serviço (QoS): a capacidade da rede de priorizar o tráfego de dados com base em sua importância para a organização.
- Segurança: a proteção da rede contra ameaças internas e externas, incluindo acesso não autorizado, malware, vírus e outras formas de ataque. 

### Tendências das Redes

Algumas das várias tendências de rede que afetam organizações e consumidores:

- BYOD (Bring Your Own Device): é uma tendência crescente na qual os funcionários trazem seus próprios dispositivos, como laptops, smartphones e tablets, para o ambiente de trabalho e os usam para acessar dados corporativos e aplicativos.

- Colaboração on-line: Equipes separadas trabalham juntas em projetos por meio da Internet.

- Comunicação por vídeo: Tendência cada vez mais popular para comunicações empresariais, incluindo videoconferências, webinars, treinamentos on-line e apresentações virtuais.

- Computação em nuvem: Os recursos de hardware e software são fornecidos como serviços através da Internet, permitindo que as empresas acessem recursos sob demanda e paguem apenas pelo que usam.

- IoT: a conexão de dispositivos eletrônicos à internet para permitir a troca de dados e a interação com outros dispositivos.

- Rede "powerline": tecnologia que usa a rede elétrica existente para transmitir dados e fornecer conexões de internet em residências.

- Banda larga sem fio: tecnologia sem fio que fornece conexões de internet mais rápidas, confiáveis e com melhor cobertura em residências.


### Ameaças à segurança

- Vírus, worms e cavalos de Tróia - Eles contêm software ou código malicioso em execução no dispositivo do usuário.
- Spyware e adware - Estes são tipos de software que são instalados no dispositivo de um usuário. O software, em seguida, coleta secretamente informações sobre o usuário.
- Ataques de dia zero - Também chamados de ataques de hora zero, ocorrem no primeiro dia em que uma vulnerabilidade se torna conhecida.
- Ataques de ator de ameaça - Uma pessoa mal-intencionada ataca dispositivos de usuário ou recursos de rede.
- Ataques de negação de serviço - Esses ataques atrasam ou travam aplicativos e processos em um dispositivo de rede.
- Interceptação de dados e roubo - Esse ataque captura informações privadas da rede de uma organização.
- Roubo de identidade - Esse ataque rouba as credenciais de login de um usuário para acessar informações privadas.

### Possíveis soluções

- Antivirus e antispyware - Esses aplicativos ajudam a proteger os dispositivos finais contra a infecção por software malicioso.
- Filtragem por firewall - A filtragem por firewall bloqueia o acesso não autorizado dentro e fora da rede.
- Sistemas de firewall dedicados - Eles fornecem recursos de firewall mais avançados que podem filtrar grandes quantidades de tráfego com mais granularidade.
- Listas de controle de acesso (ACL) - Eles filtram ainda mais o acesso e o encaminhamento de tráfego com base em endereços e aplicativos IP.
- Sistemas de prevenção de intrusões (IPS) - Identificam ameaças de rápida disseminação, como ataques de dia zero ou hora zero.
Redes privadas virtuais (VPN) - fornecem acesso seguro a uma organização para trabalhadores remotos.


## Protocolos e Modelos

### Fundamentos

- **Fonte da Mensagem (remetente)** - As fontes da mensagem são pessoas ou dispositivos eletrônicos que precisam enviar uma mensagem para outras pessoas ou dispositivos.
- **Destino da mensagem (destinatário)** - O destino recebe a mensagem e a interpreta.
- **Canal** - Consiste na mídia que fornece o caminho pelo qual a mensagem viaja da origem ao destino.

#### Protocolos de comunicação

>Conjuntos de regras e procedimentos que permitem a comunicação entre dispositivos em uma rede de computadores.

- Os protocolos de comunicação garantem que os dispositivos possam se comunicar de maneira eficiente e confiável, independentemente do tipo de hardware, software ou sistemas operacionais que estão sendo usados.

#### Requisitos

- **Codificação de mensagens**: Forma como os bits são organizados e representados nas mensagens transmitidas entre dispositivos de rede. 
- **Formatação e encapsulamento de mensagens**: Refere-se à estrutura e organização da mensagem, incluindo o cabeçalho, dados e informações de controle necessárias para que a mensagem seja transmitida corretamente na rede.
- **Tamanho da mensagem**: Importante para garantir que as mensagens possam ser transmitidas de forma eficiente e sem erros na rede.
- **Tempo da mensagem**: velocidade de transmissão da mensagem na rede
- **As opções de envio de mensagem** são importantes para permitir diferentes tipos de comunicação e garantir a confiabilidade dos dados: 

  - O **Unicast** é um tipo de comunicação ponto a ponto, em que uma mensagem é enviada de um único emissor para um único receptor. É o método mais comum de comunicação em redes.

  - O **Multicast** é um tipo de comunicação em grupo, em que uma mensagem é enviada de um único emissor para um grupo de receptores. 

  - O **Broadcast** é um tipo de comunicação em que uma mensagem é enviada de um único emissor para todos os dispositivos em uma rede.

### Protocolos

#### Visão Geral do Protocolo de Rede

>Os protocolos de rede definem um formato comum e um conjunto de regras para a troca de mensagens entre dispositivos.

##### Protocolos de comunicação em rede

Protocolos permitem que dois ou mais dispositivos se comuniquem através de um ou mais redes. A família de tecnologias Ethernet envolve uma variedade de protocolos como IP, Transmission Control Protocol (TCP), HyperText Protocolo de transferência (HTTP) e muito mais.

##### Protocolos de segurança de rede

Protocolos protegem os dados para fornecer autenticação, integridade dos dados e criptografia de dados. Exemplos de protocolos seguros incluem o Secure Shell (SSH), SSL (Secure Sockets Layer) e TLS (Transport Layer Security).

##### Protocolos de roteamento	

Protocolos permitem que os roteadores troquem informações de rota, compare caminho e, em seguida, selecionar o melhor caminho para o destino remota. Exemplos de protocolos de roteamento incluem Open Shortest Path First (OSPF) e Border Gateway Protocol (BGP)

##### Protocolos de descoberta de serviço

Protocolos que são usados para a detecção automática de dispositivos ou serviços. Exemplos de protocolos de detecção de serviços incluem Host dinâmico Protocolo de Configuração (DHCP) que detecta serviços para endereço IP alocação e Sistema de Nomes de Domínio (DNS) que é usado para executar conversão de nome para endereço IP.

#### Funções do Protocolo de Rede

>Os protocolos de comunicação de rede são responsáveis por uma variedade de funções necessárias para comunicações de rede entre dispositivos finais.

- Endereçamento: Identifica o remetente e o destinatário pretendido da mensagem usando um esquema de endereçamento definido. Exemplos de protocolos que fornecem incluem Ethernet, IPv4 e IPv6.
- Confiabilidade:	Fornece mecanismos de entrega garantidos em caso de mensagens são perdidos ou corrompidos em trânsito. O TCP fornece entrega garantida.
- Controle de fluxo:	Garante que os fluxos de dados a uma taxa eficiente entre dois dispositivos de comunicação. O TCP fornece serviços de controle de fluxo.
- Sequenciamento:	Rotula exclusivamente cada segmento de dados transmitido. O TCP fornece serviços de sequenciamento.
- Detecção de erros:	Determina se os dados foram corrompidos durante transmissão. Vários protocolos que fornecem detecção de erros incluem Ethernet, IPv4, IPv6 e TCP.
- Interface de aplicação:	Contém informações usadas para processo a processo comunicações entre aplicações de rede. Por exemplo, ao acessar uma página da Web, protocolos HTTP ou HTTPS são usados para se comunicar entre o processos da Web do cliente e do servidor.

#### Interação de Protocolos

>Uma mensagem enviada através de uma rede de computadores normalmente requer o uso de vários protocolos, cada um com suas próprias funções e formato. 

Para este exemplo:

- **Protocolo de Internet (IP)** - Principal protocolo da camada de rede e é usado para enviar pacotes de dados pela internet. Ele é responsável pelo endereçamento e roteamento dos pacotes, garantindo que eles cheguem ao destino correto. O IP é um protocolo não confiável e sem conexão, o que significa que ele não garante a entrega ou a ordem dos pacotes.

- **Protocolo de Controle de Transmissão (TCP)** -  Responsável por fornecer uma comunicação confiável e orientada à conexão entre aplicativos em sistemas finais.

- **Protocolo de Transferência de Hipertexto (HTTP)** - É o protocolo padrão para transferência de dados na web.

- **Protocolo Ethernet** é um protocolo de rede de camada física que define as características elétricas, mecânicas e de sinalização do cabeamento, bem como o formato dos pacotes de dados transmitidos pela rede. É um dos protocolos mais utilizados em redes locais (LANs) para conectar dispositivos entre si, como computadores, roteadores, switches, entre outros.


### Conjuntos de Protocolos

>Um conjunto de protocolos é um grupo de protocolos inter-relacionados necessários para executar uma função de comunicação.

#### Evolução dos conjuntos de protocolos

O **Internet Protocol Suíte ou TCP/IP** é o conjunto de protocolos mais comum e relevante usado atualmente. Outros conjuntos de protocolos criados anteriormente foram substituídos pelo TCP/IP.
(Incluem OSI, AppleTalk e Novell NetWare).

#### Exemplo de Protocolo TCP/IP

Os protocolos TCP / IP estão disponíveis para as camadas de aplicativo, transporte e Internet. Não há protocolos TCP/IP na camada de acesso à rede. Os protocolos LAN da camada de acesso à rede mais comuns são os protocolos Ethernet e WLAN (LAN sem fio). Os protocolos da camada de acesso à rede são responsáveis por entregar o pacote IP pela mídia física.


#### Conjunto de Protocolos TCP/IP

Além dos protocolos TCP e IP, o conjunto de protocolos TCP/IP inclui vários outros protocolos, como:

| Protocolo  | Descrição |
| ------------- | ------------- |
| Protocolo de Resolução de Endereços (ARP) | Mapeia um endereço IP em um endereço físico (MAC) em uma rede local. |
| Protocolo de Configuração Dinâmica de Host (DHCP) | Atribui endereços IP a dispositivos em uma rede automaticamente. |
| Protocolo de Gateway de Camada de Rede (ICMP) | Fornece informações de controle e mensagens de erro entre dispositivos em uma rede. |
| Protocolo de Sistema de Nomes de Domínio (DNS) | Traduz nomes de domínio em endereços IP. |
| Protocolo de Transferência de Arquivos (FTP) | Transfere arquivos entre dispositivos em uma rede. |
| Protocolo de Correio Simples (SMTP) | Envia e-mails entre servidores de e-mail. |
| Protocolo de Transferência de Hipertexto (HTTP) | Envia e recebe páginas da web na Internet. |
| Protocolo de Gerenciamento de Rede Simples (SNMP) | Gerencia dispositivos em uma rede. |
| Protocolo de Terminal de Rede (Telnet) | Acessa dispositivos remotamente em uma rede. |
| Protocolo de Mensagens de Controle de Rede (NetBIOS) | Compartilha recursos em uma rede local. |

Ou separados por camadas:

##### Camada de aplicação
###### Sistema de nomes

**DNS** - Sistema de nomes de domínio. Converte nomes de domínio em endereços IP.
###### Configuração de hosts

**DHCPv4** - Protocolo de configuração de host dinâmico para IPv4. Um servidor DHCPv4 atribui dinamicamente informações de endereçamento IPv4 aos clientes DHCPv4 na inicialização e permite que os endereços sejam reutilizados quando não forem mais necessários.
**DHCPv6** - Protocolo de Configuração do Host Dinâmico para IPv6. DHCPv6 é semelhante ao DHCPv4. Um servidor DHCPv6 atribui dinamicamente informações de endereçamento IPv6 aos clientes DHCPv6 na inicialização.
**SLAAC** - Configuração automática de endereço sem estado. Um método que permite que um dispositivo obtenha suas informações de endereçamento IPv6 sem usar um servidor DHCPv6.
###### E-mail

**SMTP** -Protocolo de transferência de correio simples. Permite que os clientes enviem e-mails para um servidor de e-mail e permite que os servidores enviem e-mails para outros servidores.
**POP3** - Post Office Protocol versão 3. Permite que os clientes recuperem e-mails de um servidor de e-mail e baixem o e-mail para o aplicativo de e-mail local do cliente.
**IMAP** - Protocolo de Acesso à Mensagem na Internet. Permite que os clientes acessem o e-mail armazenado em um servidor de e-mail e também mantenham o e-mail no servidor.
###### Transferência de arquivos

**FTP** - Protocolo de transferência de arquivos. Define as regras que permitem que um usuário em um host acesse e transfira arquivos para e de outro host em uma rede. O FTP é um protocolo de entrega de arquivos confiável, orientado a conexão e reconhecido.
**SFTP** - Protocolo de transferência de arquivos SSH. Como uma extensão do protocolo Secure Shell (SSH), o SFTP pode ser usado para estabelecer uma sessão segura de transferência de arquivos na qual a transferência é criptografada. SSH é um método para login remoto seguro que normalmente é usado para acessar a linha de comando de um dispositivo.
**TFTP** - Protocolo de Transferência de Arquivos Trivial. Um protocolo de transferência de arquivos simples e sem conexão com entrega de arquivos não confirmada e de melhor esforço. Ele usa menos sobrecarga que o FTP.
###### Web e serviço Web

**HTTP** - Protocolo de transferência de hipertexto. Um conjunto de regras para a troca de texto, imagens gráficas, som, vídeo e outros arquivos multimídia na World Wide Web.
**HTTPS** - HTTP seguro. Uma forma segura de HTTP que criptografa os dados que são trocados pela World Wide Web.
**REST** - Representational State Transfer. Um serviço Web que utiliza interfaces de programação de aplicações (APIs) e pedidos HTTP para criar aplicações Web.

##### Camada de transporte
###### Conexão orientada

**TCP** - Protocolo de controle de transmissão. Permite a comunicação confiável entre processos executados em hosts separados e fornece transmissões confiáveis e reconhecidas que confirmam a entrega bem-sucedida.
###### Sem Conexão

**UDP** - Protocolo de datagrama do usuário. Permite que um processo em execução em um host envie pacotes para um processo em execução em outro host. No entanto, o UDP não confirma a transmissão bem-sucedida do datagrama.

##### Camada de Internet
###### Protocolo IP (Internet Protocol)

**IPv4** - Protocolo da Internet versão 4. Recebe segmentos de mensagem da camada de transporte, empacota mensagens em pacotes e endereça pacotes para entrega de ponta a ponta através de uma rede. O IPv4 usa um endereço de 32 bits.
**IPv6** - IP versão 6. Semelhante ao IPv4, mas usa um endereço de 128 bits.
**NAT** - Tradução de endereços de rede. Converte endereços IPv4 de uma rede privada em endereços IPv4 públicos globalmente exclusivos.
###### Mensagens

**ICMPv4** - Protocolo de mensagens de controle da Internet para IPv4. Fornece feedback de um host de destino para um host de origem sobre erros na entrega de pacotes.
**ICMPv6** - ICMP para IPv6. Funcionalidade semelhante ao ICMPv4, mas é usada para pacotes IPv6.
**ICMPv6 ND** - descoberta de vizinho ICMPv6. Inclui quatro mensagens de protocolo que são usadas para resolução de endereço e detecção de endereço duplicado.
###### Protocolos de roteamento

**OSPF** - Abrir o caminho mais curto primeiro. Protocolo de roteamento de estado de link que usa um experimento hierárquico baseado em áreas. OSPF é um protocolo de roteamento interno padrão aberto.
**EIGRP** - Protocolo de roteamento de gateway interno aprimorado. Um protocolo de roteamento de padrão aberto desenvolvido pela Cisco que usa uma métrica composta com base na largura de banda, atraso, carga e confiabilidade.
**BGP** - Protocolo de gateway de fronteira. Um protocolo de roteamento de gateway externo padrão aberto usado entre os Internet Service Providers (ISPs). O BGP também é comumente usado entre os ISPs e seus grandes clientes particulares para trocar informações de roteamento.

##### Camada de acesso à rede
###### Resolução de endereços

**ARP** - Protocolo de Resolução de Endereço. Fornece mapeamento de endereço dinâmico entre um endereço **IPv4** e um endereço de hardware.

Observação: Também pode ser operado na Camada da Internet (Camada OSI 3).
###### Protocolos de link de dados

**Ethernet** - define as regras para os padrões de fiação e sinalização da camada de acesso à rede.
**WLAN** - Rede local sem fio. Define as regras para sinalização sem fio nas frequências de rádio de 2,4 GHz e 5 GHz.

### Empresas de Padrões

#### Padrões Abertos

Como existem muitos fabricantes diferentes de componentes de rede, todos eles devem usar os mesmos padrões. Em redes, os padrões são desenvolvidos por organizações internacionais de padrões.

Os padrões abertos incentivam a interoperabilidade, a concorrência e a inovação. Eles também garantem que o produto de nenhuma empresa possa monopolizar o mercado ou ter uma vantagem injusta sobre a concorrência.

As organizações padronizadoras geralmente são organizações sem fins lucrativos e independentes de fornecedores estabelecidas para desenvolver e promover o conceito de padrões abertos.

Essas organizações são importantes na manutenção de uma Internet aberta, com especificações e protocolos acessíveis gratuitamente, que podem ser implementados por qualquer fornecedor.

#### Padrões da internet

Várias organizações têm responsabilidades diferentes para promover e criar padrões para a Internet 
e o protocolo TCP / IP.

| Empresa  | Responsabilidade |
| ------------- | ------------- |
|Internet Engineering Task Force (IETF) | Desenvolve padrões técnicos para a Internet, incluindo protocolos TCP/IP e aplicativos relacionados.|
|World Wide Web Consortium (W3C)|Desenvolve padrões para a World Wide Web, incluindo HTML, XML, CSS e outras tecnologias da Web.|
|Internet Corporation for Assigned Names and Numbers (ICANN)| Coordena o sistema de nomes de domínio (DNS) da Internet, atribuindo endereços IP e gerenciando os nomes de domínio de primeiro nível (TLDs).|
|Institute of Electrical and Electronics Engineers (IEEE)| Desenvolve padrões para redes de computadores e comunicação, incluindo Ethernet e Wi-Fi.|
|International Organization for Standardization (ISO)| Desenvolve padrões internacionais em muitas áreas, incluindo tecnologia da informação e comunicação.|
|Telecommunication Standardization Sector of the International Telecommunication Union (ITU-T)| Desenvolve padrões para telecomunicações, incluindo protocolos de rede e outras tecnologias relacionadas.|
|ISOC (Internet Society)| Promove o desenvolvimento aberto da Internet e a sua utilização em todo o mundo. |
|A IRTF (Internet Research Task Force)| Grupo de pesquisa que trabalha em temas de longo prazo relacionados com a Internet, como a arquitetura, os protocolos e as aplicações. |
|A IAB (Internet Architecture Board)| Fornece orientação técnica sobre o desenvolvimento da arquitetura da Internet e a evolução de seus protocolos.|
| IANA (Internet Assigned Numbers Authority) | Responsável por coordenar e gerenciar os recursos de numeração da internet, como endereços IP, identificadores de protocolos e números de porta, entre outros. |


#### Padrões eletrônicos e de comunicações

Outras organizações de padrões têm responsabilidades em promover e criar os padrões eletrônicos e de comunicação usados para entregar os pacotes IP como sinais eletrônicos em um meio com ou sem fio.

- Institute of Electrical and Electronics Engineers (IEEE) – Organização padronizadora de engenharia elétrica e eletrônica;
- Aliança das Indústrias Eletrônicas (EIA);
- Associação da Indústria de Telecomunicações (TIA);
- Setor de Normalização das Telecomunicações da União Internacional de Telecomunicações (ITU-T);