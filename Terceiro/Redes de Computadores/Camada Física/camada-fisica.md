# Camada Física

## Sumário

- [Introdução](#conceitos-introdutórios)
  - [A conexão física](#a-conexão-física)
  - [A Camada Física](#a-camada-física)
  - [Codificação e Sinalização](#codificação-e-sinalização)
  - [Largura de Banda](#largura-de-banda)
  - [Terminologia](#terminologia)
- [Cabeamento de Cobre](#cabeamento-de-cobre)
  - [Tipos de Cabeamento](#tipos-de-cabeamento)
  - [UTP](#utp)
  - [STP](#stp)
  - [Coaxial](#coaxial)
- [Cabeamento de Fibra Óptica](#cabeamento-de-fibra-óptica)
  - [Tipos de fibra](#tipos-de-fibra)
  - [Aplicabilidade](#aplicabilidade)
  - [Conectores e Cabos](#conectores-e-cabos)
  - [Comparação UTP x Fibra](#comparação-utp-x-fibra)
- [Meios Sem Fio](#meios-sem-fio)
  - [Tipos de Meio Físico Sem Fio](#tipos-de-meio-físico-sem-fio)
  - [LAN sem fio](#lan-sem-fio)
  
  

| Título do Tópico                 | Objetivo do Tópico                                                       |
| -------------------------------- | ------------------------------------------------------------------------ |
| Propósito da camada física       | Descrever a finalidade e as funções da camada física na rede.            |
| Características da camada física | Descrever as características da camada física.                           |
| Cabeamento de cobre              | Identificar as características básicas do cabeamento de cobre.           |
| Cabeamento UTP                   | Explicar como o cabo UTP é usado em redes Ethernet.                      |
| Cabeamento de fibra óptica       | Descrição e suas principais vantagens em relação a outros meios físicos. |
| Mídia sem fio                    | Conectar dispositivos usando meio físico com e sem fio.                  |

## Conceitos Introdutórios e Características

### A conexão física

Placas de Interface de Rede

As placas de interface de rede (NICs) conectam um dispositivo à rede. As NICs Ethernet são usadas para uma conexão com fio, enquanto as NICs da rede local sem fio (WLAN) são usadas para a conexão sem fio.

### A Camada Física

A camada física é responsável por transmitir bits brutos de dados entre dispositivos de rede, sem considerar o significado dos dados ou sua estrutura. Ela define as especificações técnicas dos meios de transmissão físicos, como cabos, conectores e sinais elétricos, além de estabelecer regras para a codificação e decodificação dos bits que compõem os dados. A camada física também trata de aspectos como a velocidade da transmissão, a forma como os dados são sincronizados e como as colisões são detectadas e resolvidas em redes que utilizam compartilhamento de meio físico.

> A camada física consiste em circuitos eletrônicos, meios físicos e conectores desenvolvidos pelos engenheiros. Portanto, é aconselhável que os padrões que regem esse hardware sejam definidos pelas organizações de engenharia de comunicações e elétrica relevantes.

Os padrões da camada física abordam três áreas funcionais:

- Componentes Físicos;
- Codificação;
- Sinalização.

Os **componentes físicos** são os dispositivos de hardware eletrônico, mídia e outros conectores que transmitem os sinais que representam os bits.

### Codificação e Sinalização

A **codificação** é um método para converter um fluxo de bits de dados em um agrupamentos de bits predefinido usados para fornecer um padrão previsível que pode ser reconhecido tanto pelo emissor quanto pelo receptor.
Os dados são convertidos em sinais elétricos, ópticos ou de radiofrequência para serem transmitidos pelo meio físico que representem os valores “1” e “0”. Os padrões de camada física devem definir que tipo de sinal representa cada valor. Isso pode ser tão simples quanto uma alteração no nível de um sinal elétrico ou de um pulso óptico.

### Largura de Banda

A largura de banda se refere à quantidade de dados que podem ser transmitidos em uma conexão de rede em um determinado período de tempo. É medida em bits por segundo (bps) ou em múltiplos de bits por segundo, como kilobits por segundo (Kbps), megabits por segundo (Mbps) ou gigabits por segundo (Gbps).

A largura de banda é um fator importante na determinação da velocidade e desempenho de uma rede, pois quanto maior a largura de banda, mais dados podem ser transmitidos em um determinado período de tempo. No entanto, a largura de banda também pode ser limitada por outros fatores, como a qualidade da conexão física ou a capacidade de processamento dos dispositivos de rede envolvidos na transmissão de dados

Uma combinação de fatores determina a largura de banda prática de uma rede:

- As propriedades do meio físico;
- As tecnologias escolhidas para sinalização e detecção de sinais de rede.

#### Terminologia

- **Latência** é o termo se refere ao tempo necessário para os dados viajarem de um ponto a outro, incluindo atrasos.

> Em uma internetwork ou em uma rede com vários segmentos, a taxa de transferência não pode ser mais rápida que o link mais lento no caminho da origem ao destino.

- **Taxa de transferência** é a medida da transferência de bits através da mídia durante um determinado período.

A taxa de transferência geralmente é menor que a largura de banda. Existem muitos fatores que influenciam a taxa de transferência:

- A quantidade de tráfego;
- O tipo de tráfego;
- A latência criada pelo número de dispositivos de rede encontrados entre a origem e o destino.

## Cabeamento de Cobre

É o tipo mais comum de cabeamentos, porém as redes usam mídia de cobre porque é barata, fácil de instalar e tem baixa resistência à corrente elétrica. Entretanto, ela é limitada pela distância e interferência de sinal.

> Os dados são transmitidos por cabos de cobre como pulsos elétricos. No entanto, quanto mais o sinal viaja, mais ele se deteriora. Isso se chama atenuação de sinal. Por isso, todas as mídias de cobre devem seguir limitações de distância rigorosas, conforme especificado nos padrões de orientação.

A temporização e a voltagem dos pulsos elétricos também são suscetíveis à interferência de duas fontes:

- **Interferência eletromagnética (EMI) ou interferência de radiofrequência (RFI)** - Os sinais EMI e RFI podem distorcer e corromper os sinais de dados que estão sendo transportados pela mídia de cobre.

- **Diafonia** é uma perturbação causada pelos campos elétrico ou magnético de um sinal em um fio para o sinal em um fio adjacente. Nos circuitos de telefone, a diafonia pode fazer com que parte de outra conversa de voz de um circuito adjacente seja ouvida (linha cruzada).

### Tipos de Cabeamento

Há três tipos principais de mídias de cobre usadas em redes:

- Cabo de par trançado não-blindado (UTP - Unshielded Twisted Pair);
- Cabo de pares trançados blindados (STP - Shielded Twisted Pair);
- Cabo coaxial;

#### UTP

O **UTP** é o meio físico de rede mais comum. Terminado com conectores RJ-45, é usado para interconectar hosts de rede com dispositivos de rede intermediários, como comutadores e roteadores.

O cabeamento UTP consiste em quatro pares de fios de cobre com código de cores que foram torcidos juntos e depois envoltos em uma bainha de plástico flexível. Seu tamanho reduzido pode ser vantajoso durante a instalação.

Os projetistas de cabos descobriram outras maneiras de limitar o efeito negativo da diafonia:

- **Cancelamento** - os designers agora emparelham os fios em um circuito. Quando dois fios de um circuito elétrico são colocados próximos um do outro, seus campos magnéticos serão opostos. Assim, os dois campos magnéticos cancelam um ao outro e também podem cancelar sinais externos de EMI e RFI.
- **Numero de torções por par de fios** - O cabo UTP deve seguir especificações precisas que orientam quantas tranças são permitidas por metro (3,28 pés) do cabo.

O cabo UTP depende exclusivamente do efeito de cancelamento produzido pelos pares de fios trançados para limitar a degradação de sinal e fornecer efetivamente a autoblindagem para cabos trançados na mídia de rede.

O TIA/EIA-568 estipula os padrões de cabeamento comerciais para instalações de LAN e é o padrão mais usado em ambientes de cabeamento de LAN. Alguns dos elementos definidos são os seguintes:

- Tipos de cabos;
- Comprimentos do cabo;
- Conectores;
- Terminação de cabo;
- Métodos de teste de cabo.

As características elétricas do cabeamento de cobre são definidas pelo Instituto de Engenharia Elétrica e Eletrônica (IEEE).
O IEEE classifica o cabeamento UTP de acordo com o desempenho.

> Os cabos em categorias mais altas são desenvolvidos e construídos para suportar taxas de dados mais elevadas. À medida que novas tecnologias Ethernet de velocidade de gigabit estão sendo desenvolvidas e adotadas, a Categoria 5e é agora o tipo de cabo minimamente aceitável, com a Categoria 6 sendo o tipo recomendado para novas instalações prediais.

- A categoria 3 foi originalmente utilizada para comunicação de voz através de linhas de voz, mas mais tarde utilizada para transmissão de dados.
- As categorias 5 e 5e são utilizadas para a transmissão de dados. Categoria 5 suporta 100Mbps e Categoria 5e suporta 1000 Mbps.
- A categoria 6 tem um separador adicional entre cada par de fios para suportar velocidades mais altas. Categoria 6 suporta até 10 Gbps.
- Categoria 7 também suporta 10 Gbps.
- Categoria 8 suporta 40 Gbps.

Fios individuais do cabo precisam ser conectados em ordem diferente para conjuntos diferentes de pinos nos conectores RJ-45.

- Ethernet direta - O tipo mais comum de cabo de rede. Geralmente é usado para interconectar um host a um switch e um switch a um roteador.
- Ethernet Crossover - Um cabo usado para interconectar dispositivos semelhantes. (Depreciado)

#### STP

O **STP** oferece maior proteção contra ruído do que o UTP. No entanto o cabo STP é significativamente mais caro e difícil instalação. Assim como o cabo UTP, o STP usa um conector RJ-45.
Os cabos STP combinam as técnicas de blindagem para contrabalançar a EMI e a RFI, e são trançados para conter o crosstalk. Se o cabo não estiver devidamente aterrado, a blindagem poderá atuar como uma antena e captar sinais indesejados.

#### Coaxial

O cabo **coaxial**, ou coax para abreviar, recebeu seu nome porque tem dois condutores que compartilham o mesmo eixo e consiste no seguinte:

- Um condutor de cobre é usado para transmitir os sinais eletrônicos.
- Uma camada de isolamento plástico flexível envolve um condutor de cobre.
- O material de isolamento é envolvido em uma malha de cobre com tecido, ou uma folha metálica, que atua como o segundo cabo no circuito e uma proteção para o condutor interno. Essa segunda camada, ou blindagem, também reduz a quantidade de interferência eletromagnética externa.
- Todo o cabo é coberto com um revestimento para evitar danos físicos menores.

## Cabeamento de Fibra Óptica

A fibra óptica é um fio flexível, extremamente fino e transparente de vidro muito puro, não muito maior do que um fio de cabelo humano.

> O cabo de fibra óptica transmite dados por longas distâncias e a larguras de banda mais altas do que qualquer outra mídia de rede.

- Os bits são codificados na fibra como pulsos de luz.
- Sinais com menos atenuação
- Imune à interferência de EMI e RFI.

### Tipos de fibra

- Fibra monomodo (Single Mode Fiber - SMF)
- Fibra multimodo (Multi Mode Fiber - MMF)

> A fibra monomodo é usada em aplicações de longa distância que exigem altas velocidades de transmissão, como em redes de telecomunicações e transmissão de dados de longa distância, enquanto a fibra multimodo é mais adequada para aplicações locais de curta distância, como redes de campus e data centers.

As principais diferenças entre cabos SMF e MMF estão relacionadas à distância de transmissão, velocidade de transmissão e custo:

- Distância de transmissão: A fibra monomodo (SMF) é projetada para longas distâncias de transmissão, com um alcance típico de até 100 km, enquanto a fibra multimodo (MMF) é projetada para curtas distâncias de transmissão, geralmente até 2 km, mas pode chegar a até 550 metros para algumas aplicações.

- Velocidade de transmissão: A fibra monomodo é capaz de transmitir a uma taxa mais alta de dados do que a fibra multimodo, chegando a 100 Gbps ou mais, enquanto a fibra multimodo tem limitações de velocidade e geralmente não ultrapassa os 10 Gbps.

- Custo: O custo da fibra monomodo é geralmente mais alto do que o da fibra multimodo, devido às suas características ópticas superiores e sua fabricação mais precisa.

### Aplicabilidade

- Redes corporativas - Aplicativos de cabeamento de backbone e dispositivos de infraestrutura de interconexão.
- FTTH (Fiber-to-the-Home) - Residências e pequenas empresas.
- Redes de longo curso - Utilizadas por provedores de serviços para conectar países e cidades.
- Redes de cabos submarinos - Utilizadas para fornecer soluções confiáveis de alta velocidade e alta capacidade, capazes de sobreviver em ambientes submarinos adversos até distâncias transoceânicas.

### Conectores e Cabos

- Conector ponta reta (ST)
- Conector SC
- Conectores Lucent (LC) simplex
- Conectores LC duplex multimodo

O uso das cores diferencia entre cabos monomodo e multimodo. A cor amarela indica cabos de fibra monomodo e o laranja é para cabos de fibra multimodo.

### Comparação UTP x Fibra

| Problemas de Implementação                                          | Cabeamento UTP                       | Cabeamento de fibra óptica               |
| ------------------------------------------------------------------- | ------------------------------------ | ---------------------------------------- |
| Largura de banda suportada                                          | 10 Mb/s - 10 Gb/s                    | 10 Mb/s - 100 Gb/s                       |
| Distância                                                           | Relativamente curto (1 a 100 metros) | Relativamente longo (1 - 100.000 metros) |
| Imunidade a interferência eletromagnética e de frequências de rádio | Baixa                                | Alto (totalmente imune)                  |
| Imunidade a perigos elétricos                                       | Baixa                                | Alto (totalmente imune)                  |
| Custos da mídia e dos conectores                                    | Menor                                | Mais alta                                |
| Habilidades necessárias para a instalação                           | Menor                                | Mais alta                                |
| Precauções de segurança                                             | Menor                                | Mais alta                                |


## Meios Sem Fio

O meio físico sem fio transporta sinais eletromagnéticos que representam os dígitos binários de comunicações de dados usando frequências de rádio ou de micro-ondas.

- Vantagens
  - Mobilidade
  - Mais dispositivos conectados ao mesmo tempo
- Limitações
  - Área de cobertura
  - Interferência
  - Segurança

### Tipos de Meio Físico Sem Fio

Padrões sem fio:
- **Wi-Fi (IEEE 802.11**) - A WLAN usa um protocolo baseado em contenção conhecido como acesso múltiplo / detecção de colisão de portadora (CSMA / CA). A NIC sem fio deve ouvir primeiro, antes de transmitir, para determinar se o canal de rádio está limpo. Se houver outro dispositivo sem fio transmitindo, a NIC deverá esperar até o canal estar limpo. Wi-Fi é uma marca comercial registrada da Wi-Fi Alliance.
- **Bluetooth (IEEE 802.15)** - Este é um padrão de rede pessoal sem fio (WPAN), comumente conhecido como “Bluetooth”. Ele usa um processo de emparelhamento de dispositivo para se comunicar em distâncias de 1 a 100 metros.
- **WiMAX (IEEE 802:16)** - Comumente conhecido como Interoperabilidade mundial para acesso por microondas (WiMAX), esse padrão sem fio usa uma topologia ponto a multiponto para fornecer acesso à banda larga sem fio.
- **Zigbee (IEEE 802.15.4)** - Zigbee é uma especificação usada para comunicações de baixa taxa de dados e baixa potência. Destina-se a aplicações que exigem taxas de dados de curto alcance, baixas e longa duração da bateria. (IoT ou Ambientes industriais).

### LAN sem fio

- **Ponto de acesso sem fio (AP)** - Estes concentram os sinais sem fio dos usuários e se conectam à infraestrutura de rede existente baseada em cobre, como Ethernet. 
- **Adaptadores de NIC sem fio** - fornecem recursos de comunicação sem fio para hosts de rede.

