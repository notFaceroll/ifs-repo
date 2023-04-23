# Camada de Enlace de Dados

> - Função da Camada
> - Características dos métodos de controle de acesso à mídia na WAN e Topologias de LAN.
> - Características e as funções do quadro de link de dados.

## Conceito

A camada de enlace de dados (OSI Camada 2) é responsável por garantir que os dados sejam transmitidos com sucesso entre dois dispositivos conectados diretamente por um meio físico compartilhado, como um cabo ou rede sem fio. A camada de enlace de dados divide os dados em quadros (ou frames) e adiciona informações de controle, como endereços de origem e destino, sequência de quadros e detecção de erros.

A camada:

- Permite que as camadas superiores acessem a mídia. O protocolo de camada superior não está completamente ciente do tipo de mídia que é usado para encaminhar os dados.
- Aceita dados, geralmente pacotes de Camada 3 (ou seja, IPv4 ou IPv6), e os encapsula em quadros da Camada 2.
- Controla como os dados são colocados e recebidos na mídia.
- Troca quadros entre pontos de extremidade através da mídia de rede.
- Recebe dados encapsulados, geralmente pacotes de Camada 3, e os direciona para o protocolo de camada superior apropriado.
- Executa a detecção de erros e rejeita qualquer quadro corrompido.

### IEEE 802 Subcamadas de link de dados de LAN/MAN

A camada de link de dados da LAN/MAN IEEE 802 é dividida em duas subcamadas: a subcamada **LLC (Logical Link Control)** e a subcamada **MAC (Media Access Control)**.

> A subcamada LLC é responsável por fornecer serviços de comunicação confiáveis e independentes do meio para as camadas superiores.

Ela também oferece mecanismos de controle de erros e de fluxo de dados. Ela coloca a informação no quadro que identifica qual protocolo de camada de rede está sendo usado para o quadro.

> Já a subcamada MAC é responsável pelo acesso ao meio e controle de acesso ao meio. Ela define como os dispositivos em uma rede compartilham o meio de transmissão e evitam colisões de dados.

Ela também define o formato dos quadros de dados, que são transmitidos no meio físico e fornece encapsulamento de dados:

- Delimitação de quadros - O processo de enquadramento fornece delimitadores importantes para identificar campos dentro de um quadro. Esses bits de delimitação promovem a sincronização entre os nós de transmissão e de recepção.
- Endereçamento - Fornece endereçamento de origem e destino para transportar o quadro da Camada 2 entre dispositivos na mesma mídia compartilhada.
- Detecção de erro - Inclui um trailer usado para detectar erros de transmissão.

### Padrões da camada de enlace de dados

As organizações de engenharia que definem padrões abertos e protocolos que se aplicam à camada de acesso à rede (ou seja, as camadas físicas e de link de dados OSI) incluem o seguinte:

- Institute of Electrical and Electronics Engineers (IEEE)
- International Telecommunication Union (ITU)
- International Organization for Standardization (ISO)
- Instituto Nacional Americano de Padronização (ANSI)

## Topologias Físicas e Lógicas

> A topologia de uma rede é a organização, ou o relacionamento, dos dispositivos de rede e as interconexões entre eles.

Existem dois tipos de topologias usadas ao descrever redes LAN e WAN:

- **Física**: Conexões físicas e como os dispositivos finais e intermediários (ou seja, roteadores, comutadores e pontos de acesso sem fio) são interconectados. A topologia também pode incluir a localização específica do dispositivo, como o número do quarto e a localização no rack do equipamento.
- **Lógica**: Identifica conexões virtuais usando interfaces de dispositivo e esquemas de endereçamento IP da Camada 3. Refere-se à maneira como uma rede transfere quadros de um nó para o próximo.

### Topologias de WAN

As topologias de rede WAN (Wide Area Network) referem-se à forma como os dispositivos e nós de rede são interconectados em uma área geográfica ampla. Algumas das topologias de WAN mais comuns incluem:

- **Topologia de estrela**: Nesta topologia, todos os dispositivos são conectados a um hub central, que é responsável por encaminhar o tráfego de dados entre os dispositivos.

- **Topologia de malha completa**: Cada dispositivo está conectado diretamente a todos os outros dispositivos da rede. Isso cria uma rede redundante, onde os dados podem ser encaminhados por vários caminhos para chegar ao destino.

- **Topologia em anel**: Cada dispositivo é conectado ao seu vizinho mais próximo em uma configuração em forma de anel. Os dados são transmitidos em um único sentido ao redor do anel, passando por cada dispositivo até chegar ao destino.

- **Topologia em árvore**: Combinação das topologias de estrela e de barramento. Nesta topologia, vários hubs são conectados a um hub central, que é responsável por encaminhar o tráfego de dados entre os dispositivos.

- **Topologia em linha**: Os dispositivos são conectados em uma linha reta, de forma que o dispositivo A esteja conectado ao dispositivo B, o dispositivo B esteja conectado ao dispositivo C, e assim por diante. Essa topologia é usada com menos frequência porque é menos tolerante a falhas do que outras topologias.

### Topologias de LAN

Dentro da topologia física também existem diferentes tipos ou divisões, cada um com suas próprias características e formas de conexão. Alguns exemplos de topologias físicas comuns incluem:

- **Barramento (Bus)**: todos os dispositivos são conectados a um único cabo, em que as informações são transmitidas de um dispositivo para outro. É uma topologia simples, mas pode ser afetada negativamente pela adição de mais dispositivos, o que pode causar congestionamento e diminuir a velocidade de transmissão.

- **Estrela (Star)**: todos os dispositivos são conectados a um concentrador (hub) ou switch central, que recebe e encaminha as informações para o destino apropriado. É uma topologia fácil de gerenciar e que suporta bem o aumento de dispositivos, mas pode ser mais cara devido ao equipamento adicional necessário.

- **Anel (Ring)**: todos os dispositivos são conectados em um circuito fechado, em que as informações são transmitidas de um dispositivo para outro até chegar ao destino apropriado. É uma topologia confiável, mas pode ser difícil de expandir e gerenciar.

- **Malha (Mesh)**: todos os dispositivos são conectados uns aos outros, formando uma rede em que as informações podem ser transmitidas por vários caminhos diferentes. É uma topologia muito redundante e confiável, mas pode ser complexa de configurar e gerenciar.

### Comunicação em half e full duplex

> A comunicação em half duplex e full duplex são duas formas diferentes de comunicação bidirecional em uma rede.

Na comunicação em half duplex, as informações podem ser enviadas e recebidas, mas não ao mesmo tempo. Isso significa que os dispositivos precisam alternar entre transmitir e receber, como se fosse uma conversa em um walkie-talkie, onde apenas uma pessoa pode falar de cada vez.

Já na comunicação em full duplex, os dispositivos podem enviar e receber informações simultaneamente. Isso é possível graças a dois canais de comunicação separados, um para envio e outro para recebimento. É como se fosse uma conversa telefônica, onde as duas pessoas podem falar e ouvir ao mesmo tempo.

> A escolha entre half duplex e full duplex dependerá das necessidades e capacidades dos dispositivos e da rede em questão.

### Métodos de controle de acesso

Na comunicação de rede, existem duas abordagens básicas para o acesso à rede: acesso baseado em contenção e acesso controlado.

O **acesso baseado em contenção** é um método no qual cada nó em uma rede tenta transmitir dados assim que tiver dados para enviar. Se dois ou mais nós tentarem transmitir simultaneamente, ocorre uma colisão e os dados serão retransmitidos posteriormente. O acesso baseado em contenção é comum em redes LAN e WLAN, como o padrão IEEE 802.11.

Já o **acesso controlado** é um método no qual um nó deve solicitar permissão para transmitir antes de enviar dados. O acesso controlado é comum em redes WAN e é usado em tecnologias como Frame Relay e ATM. O acesso controlado pode garantir que cada nó tenha tempo de transmissão garantido e que não haja colisões de dados.

---

> Existem métodos para prever e prevenir colisões no acesso baseado em contenção. Alguns desses métodos incluem:

- **CSMA/CD (Carrier Sense Multiple Access with Collision Detection)**: Usado em redes Ethernet com fio e é projetado para detectar colisões que ocorrem quando dois ou mais dispositivos tentam enviar dados ao mesmo tempo. Se uma colisão for detectada, os dispositivos aguardam um período aleatório antes de tentar enviar novamente.

- **CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance)**: Método usado em redes sem fio e é projetado para evitar colisões antes que elas ocorram. Os dispositivos sem fio escutam o canal antes de enviar dados e aguardam um breve período de tempo para garantir que nenhum outro dispositivo esteja transmitindo antes de enviar seus próprios dados.

- **Token Passing**: Os dispositivos passam um "token" ao redor da rede, permitindo que apenas o dispositivo que possui o token transmita dados. Isso garante que apenas um dispositivo transmita dados por vez, evitando colisões.

- **Polling**: Neste método, um dispositivo de controle central envia um sinal para cada dispositivo na rede, solicitando que envie dados em vez de deixar os dispositivos transmitirem sempre que estiverem prontos. Isso ajuda a evitar colisões, pois apenas um dispositivo é autorizado a transmitir dados a qualquer momento.

## Quadro de Enlace de Dados

Embora existam muitos protocolos de camada de enlace de dados diferentes que descrevem os quadros de camada de enlace de dados, cada tipo de quadro tem três partes básicas:

- Cabeçalho;
  - Início;
  - Endereçamento;
  - Tipo;
  - Controle;
- Dados;
  - Dados;
- Trailer;
  - Detecção de erros;
  - Fim.

> A camada de link de dados acrescenta informações na forma de um **trailer** no final do quadro.

Todos os protocolos da camada de enlace de dados encapsulam os dados dentro do campo de dados do quadro. No entanto, a estrutura do quadro e os campos contidos no cabeçalho e trailer variam de acordo com o protocolo.

### Campos do quadro

O **cabeçalho** contém informações sobre a origem e o destino do quadro, além de outros campos de controle, como o tipo de protocolo que está sendo transmitido.

- O endereçamento indica os nós de origem e destino;
- O tipo identifica o protocolo da camada 3 no campo de dados;
- O controle identifica serviços especiais no campo de fluxo;

Já os **dados** referem-se ao próprio pacote de informação a ser transmitido, que pode ser um pacote de IP, por exemplo.

O campo de **trailer** contém um código de detecção de erros chamado FCS (Frame Check Sequence), que é usado para verificar se o quadro foi recebido sem erros. O FCS é um valor de verificação de redundância cíclica (CRC) calculado com base nos bits de dados do quadro e é verificado pelo receptor após receber o quadro.

### Quadros de LAN e WAN

Protocolos Ethernet são usados por LANs com fio. As comunicações sem fio se enquadram nos protocolos WLAN (IEEE 802.11). Esses protocolos foram projetados para redes multiacesso.

As WANs tradicionalmente usavam outros tipos de protocolos para vários tipos de topologias ponto a ponto, hub-spoke e malha completa. Alguns dos protocolos WAN comuns ao longo dos anos incluíram:

- Protocolo ponto a ponto (PPP);
- Controle de Enlace de Dados de Alto Nível (HDLC);
- Frame Relay;
- Modo de Transferência Assíncrona (ATM);
- X.25;

Esses protocolos de Camada 2 agora estão sendo substituídos na WAN por Ethernet.

> A diferença na largura de banda resulta normalmente no uso de diferentes protocolos para LANs e WANs.
