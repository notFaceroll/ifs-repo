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
