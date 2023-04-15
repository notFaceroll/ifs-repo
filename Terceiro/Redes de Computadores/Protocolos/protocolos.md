# Protocolos

## As Regras de Protocolos de rede

### Fundamentos das Comunicações

As redes variam em tamanho, forma e função. Elas podem ser tão complexas quanto os dispositivos conectados pela Internet ou tão simples quanto dois computadores conectados diretamente um ao outro com um único cabo e qualquer outra coisa. No entanto, apenas ter a conexão física com ou sem fio entre os dispositivos finais não é suficiente para permitir a comunicação. Para que ocorra comunicação, os dispositivos devem saber “como” se comunicar.

As pessoas trocam ideias usando vários métodos de comunicação diferentes. No entanto, todos os métodos de comunicação têm os seguintes três elementos em comum:

- **Fonte da Mensagem (remetente)** - As fontes da mensagem são pessoas ou dispositivos eletrônicos que precisam enviar uma mensagem para outras pessoas ou dispositivos.
- **Destino da mensagem (destinatário)** - O destino recebe a mensagem e a interpreta.
- **Canal** - Consiste na mídia que fornece o caminho pelo qual a mensagem viaja da origem ao destino.

### Protocolos de Comunicação

Protocolos de comunicação são conjuntos de regras e procedimentos que permitem a comunicação entre dispositivos em uma rede de computadores. Eles definem o formato, o tempo e o significado das mensagens que são trocadas entre dispositivos, bem como as ações que devem ser tomadas em resposta a essas mensagens.

Os protocolos de comunicação garantem que os dispositivos possam se comunicar de maneira eficiente e confiável, independentemente do tipo de hardware, software ou sistemas operacionais que estão sendo usados. Sem protocolos de comunicação, os dispositivos em uma rede de computadores não seriam capazes de se comunicar uns com os outros.

### Requisitos de Protocolo de Rede

Os protocolos usados nas comunicações de rede compartilham muitas dessas características fundamentais. Além de identificar a origem e o destino, os protocolos de computadores e de redes definem os detalhes sobre como uma mensagem é transmitida por uma rede. Protocolos de computador comuns incluem os seguintes requisitos:

- Codificação de mensagens;
- Formatação e encapsulamento de mensagens;
- Tamanho da mensagem;
- Tempo da mensagem;
- Opções de envio de mensagem.

Codificação de mensagens: Refere-se à forma como os bits são organizados e representados nas mensagens transmitidas entre dispositivos de rede. A codificação é importante para garantir que a mensagem seja transmitida corretamente e possa ser interpretada corretamente pelo dispositivo receptor.

Formatação e encapsulamento de mensagens: Refere-se à estrutura e organização da mensagem, incluindo o cabeçalho, dados e informações de controle necessárias para que a mensagem seja transmitida corretamente na rede. O encapsulamento é importante para garantir que as mensagens possam ser transmitidas de forma confiável e eficiente na rede.

Tamanho da mensagem: Refere-se ao tamanho máximo permitido para uma mensagem, o que é importante para garantir que as mensagens possam ser transmitidas de forma eficiente e sem erros na rede. Um tamanho de mensagem muito grande pode causar problemas de desempenho na rede, enquanto um tamanho muito pequeno pode limitar a quantidade de dados que podem ser transmitidos de uma só vez.

Tempo da mensagem: Refere-se à velocidade de transmissão da mensagem na rede, que é importante para garantir que as mensagens possam ser entregues com a maior rapidez possível. O tempo da mensagem é afetado por fatores como a largura de banda da rede, a distância entre dispositivos e a carga de tráfego na rede.

As opções de envio de mensagem são importantes para permitir diferentes tipos de comunicação e garantir a confiabilidade dos dados: 

- O Unicast é um tipo de comunicação ponto a ponto, em que uma mensagem é enviada de um único emissor para um único receptor. É o método mais comum de comunicação em redes.

- O Multicast é um tipo de comunicação em grupo, em que uma mensagem é enviada de um único emissor para um grupo de receptores. É útil para enviar a mesma mensagem para vários destinatários ao mesmo tempo, reduzindo a carga na rede.

- O Broadcast é um tipo de comunicação em que uma mensagem é enviada de um único emissor para todos os dispositivos em uma rede. É útil para enviar informações gerais ou alertas para todos os dispositivos em uma rede, mas pode causar congestionamento de rede desnecessário se usado em excesso.

## Protocolos

### Visão Geral do Protocolo de Rede

Os protocolos de rede definem um formato comum e um conjunto de regras para a troca de mensagens entre dispositivos. Os protocolos são implementados por dispositivos finais e dispositivos intermediários em software, hardware ou ambos. Cada protocolo de rede tem sua própria função, formato e regras para comunicações.

<table>
  <tr>
    <th>Tipo de Protocolo</th>
    <th>Descrição</th>
  </tr>
  <tr>
    <td>
      Protocolos de comunicação em rede
    </td>
    <td>
      Protocolos permitem que dois ou mais dispositivos se comuniquem através de um ou mais redes. A família de tecnologias Ethernet envolve uma variedade de protocolos como IP, Transmission Control Protocol (TCP), HyperText Protocolo de transferência (HTTP) e muito mais.
    </td>
  </tr>
  <tr>
    <td>
      Protocolos de segurança de rede
    </td>
    <td>
      Protocolos protegem os dados para fornecer autenticação, integridade dos dados e criptografia de dados. Exemplos de protocolos seguros incluem o Secure Shell (SSH), SSL (Secure Sockets Layer) e TLS (Transport Layer Security).
    </td>
  </tr>
  <tr>
    <td>
      Protocolos de roteamento	
    </td>
    <td>
      Protocolos permitem que os roteadores troquem informações de rota, compare caminho e, em seguida, selecionar o melhor caminho para o destino remota. Exemplos de protocolos de roteamento incluem Open Shortest Path First (OSPF) e Border Gateway Protocol (BGP)
    </td>
  </tr>
  <tr>
    <td>
      Protocolos de descoberta de serviço
    </td>
    <td>
      Protocolos são usados para a detecção automática de dispositivos ou serviços. Exemplos de protocolos de detecção de serviços incluem Host dinâmico Protocolo de Configuração (DHCP) que detecta serviços para endereço IP alocação e Sistema de Nomes de Domínio (DNS) que é usado para executar conversão de nome para endereço IP.
    </td>
  </tr>
</table>

### Funções do Protocolo de Rede

Os protocolos de comunicação de rede são responsáveis por uma variedade de funções necessárias para comunicações de rede entre dispositivos finais:

- Endereçamento: Identifica o remetente e o destinatário pretendido da mensagem usando um esquema de endereçamento definido. Exemplos de protocolos que fornecem incluem Ethernet, IPv4 e IPv6.
- Confiabilidade:	Fornece mecanismos de entrega garantidos em caso de mensagens são perdidos ou corrompidos em trânsito. O TCP fornece entrega garantida.
- Controle de fluxo:	Garante que os fluxos de dados a uma taxa eficiente entre dois dispositivos de comunicação. O TCP fornece serviços de controle de fluxo.
- Sequenciamento:	Rotula exclusivamente cada segmento de dados transmitido. O TCP fornece serviços de sequenciamento.
- Detecção de erros:	Determina se os dados foram corrompidos durante transmissão. Vários protocolos que fornecem detecção de erros incluem Ethernet, IPv4, IPv6 e TCP.
- Interface de aplicação:	Contém informações usadas para processo a processo comunicações entre aplicações de rede. Por exemplo, ao acessar uma página da Web, protocolos HTTP ou HTTPS são usados para se comunicar entre o processos da Web do cliente e do servidor.

### Interação de Protocolos

Aqui estão os mais comuns dentre os vários protocolos de rede:

- Protocolo de Internet (IP) - Principal protocolo da camada de rede e é usado para enviar pacotes de dados pela internet. Ele é responsável pelo endereçamento e roteamento dos pacotes, garantindo que eles cheguem ao destino correto. O IP é um protocolo não confiável e sem conexão, o que significa que ele não garante a entrega ou a ordem dos pacotes.

- Protocolo de Controle de Transmissão (TCP) -  responsável por fornecer uma comunicação confiável e orientada à conexão entre aplicativos em sistemas finais. Ele estabelece uma conexão de transporte confiável, garantindo que as informações sejam transmitidas sem erros e duplicações, e retransmitindo pacotes perdidos.

- Protocolo de Datagrama de Usuário (UDP) - usado para transmissão de dados em tempo real, como transmissão de vídeo ou voz.

- Protocolo de Transferência de Arquivos (FTP) - É um protocolo usado para transferir arquivos entre sistemas conectados em rede. Ele é amplamente utilizado para transferir arquivos grandes, como imagens e vídeos, de servidores web para computadores locais.

- Protocolo de Correio Simples (SMTP) - É o protocolo padrão para envio de e-mails pela internet. Ele permite que os usuários enviem e-mails de um servidor de e-mail para outro, garantindo que as mensagens sejam entregues corretamente.

- Protocolo de Transferência de Hipertexto (HTTP) - É o protocolo padrão para transferência de dados na web. Ele permite que os navegadores obtenham informações de servidores web e exibam conteúdo para os usuários, como páginas da web, imagens e arquivos de vídeo.

- Protocolo de Sistema de Nomes de Domínio (DNS) - É um protocolo que traduz nomes de domínio em endereços IP. Ele permite que os usuários acessem sites da web digitando nomes em vez de números de IP, tornando a navegação mais fácil e intuitiva.

- Protocolo de Gerenciamento de Rede Simples (SNMP) - É um protocolo usado para monitorar e gerenciar dispositivos de rede. Ele permite que os administradores de rede monitorem o desempenho da rede, detectem falhas e implementem soluções rapidamente.

- Protocolo de Configuração Dinâmica de Host (DHCP) - É um protocolo usado para atribuir endereços IP a dispositivos em uma rede. Ele permite que os dispositivos sejam automaticamente configurados para se conectar à rede sem a necessidade de intervenção manual.

- Protocolo de Acesso Remoto (RDP) - usado para acessar remotamente computadores e servidores em uma rede.

- Protocolo Ethernet é um protocolo de rede de camada física que define as características elétricas, mecânicas e de sinalização do cabeamento, bem como o formato dos pacotes de dados transmitidos pela rede. É um dos protocolos mais utilizados em redes locais (LANs) para conectar dispositivos entre si, como computadores, roteadores, switches, entre outros.