# Sistemas de Arquivos

## Intro
O **Sistema de Arquivos** é o modo como as informações são armazenadas nos dispositivos físicos de armazenamento, como discos rígidos, ssd, drives externos, etc.

É a parte mais visível de um SO, pois a manipulação de arquivos é uma atividade frequentemente realizada pelos usuários, devendo sempre ocorrer de maneira uniforme, independente dos diferentes dispositivos de armazenamento.

O armazenamento e a recuperação de informação são atividades essenciais para qualquer tipo de aplicação. Um processo deve ser capaz de ler e gravar dados de forma permanente em discos.

## Arquivos

São construídos de informações logicamente relacionadas, podendo conter instruções (programa executável) ou dados (arquivos de texto, banco ded dados, planilha, etc). Arquivos são identificados por um nome (em alguns SOs há distinção entre maiúsculas e minúsculas) e podem conter após o nome uma extensão do arquivo.

### Organização dos Arquivos

A organização dos arquivos consiste no modo como os dados estão internamente armazenados, podendo, sua estrutura, variar em função do tipo de informação contida no arquivo.

A forma mais simples de organização é através de uma sequência não estruturadas de bytes. A aplicação deve definir toda a organização, com vantagem da flexibilidade, porém de inteira responsabilidade da aplicação.

As organizações mais conhecidas e implementadas são a sequencial, relativa e indexada.

### Operações de I/O

Realizadas através de System Calls, que fornecem uma interface simples e uniforme entre a aplicação e os diversos dispositivos, permitindo leitura/gravação, criação/eliminação de arquivos.

- Create
- Open
- Read
- Write
- Close
- Delete

### Atributos

Os atributos são informações de controle dos arquivos que variam dependendo do Sistema Operacional, por exemplo: tamanho, proteção, identificação do criador e data e hora de criação;

Alguns atributos específicos são alterados apenas pelo próprio Sistema Operacional, como data e hora de criação, tamanho e outros podem ser alterados pelo usuário como proteção.

## Diretórios

A organização por diretórios é o modo como o Sistema organiza logicamente os diversos arquivos contidos em um dispositivo físico de armazenamento.

O diretório contém entradas associadas aos arquivos onde são armazenadas informações como localização física, nome, organização e demais atributos.

Ao abrir um arquivo, o Sistema Operacional procura a sua entrada na estrutura de diretórios em uma tabela mantida na memória principal, contendo todos os arquivos. É necessário fechar o arquivo ao término de seu uso.

### Nível Único:

- Organização mais simples de uma estrutura de diretórios.
- Existe apenas um único diretório contendo todos os arquivos do disco.
- O nível único é bastante limitado, não permitindo que usuários criem arquivos com mesmo nome.

### Master File Directory (MFD):

- Existe um nível de diretório adicional para controlar os diretórios individuais dos usuários.
- Indexado pelo nome do usuário e, nele, cada entrada aponta para o diretório (UFD) pessoal.

### Estrutura de diretórios em árvore:

- Existe o diretório MFD que é a raiz, os galhos são os UFD e os arquivos são as folhas.
- Cada subdiretório abaixo do MDF pode conter arquivos e novos subdiretórios e assim por diante.
- Quando se referencia a um arquivo, é necessário especificar seu nome, bem como o diretório onde ele se encontra, referência chamada PATH.
- Mais organizada e adotada pela maioria dos Sistemas Operacionais.
Na maioria dos sistemas, diretórios também são tratados como arquivos, com identificação de atributos, proteção identificação do criador e data da criação.

### Proteção de Acesso

A proteção de acesso aos arquivos visa possibilitar o compartilhamento seguro de arquivos entre usuários, quando desejado. Em geral, existe concessão ou não de acessos como leitura, gravação, execução e eliminação.

Existem diferentes mecanismos de níveis de proteção. Alguns deles são:

### Senha de Acesso:

- O sistema concede acesso a determinados arquivos/diretórios através de uma senha;
- Cada arquivo possui apenas uma senha e o acesso pode ter diversos níveis de acesso;
- Desvantagem de compartilhamento, pois além do dono, todos os demais usuários precisam conhecer a senha de acesso.

### Grupos de Usuários:

- Existente em diversos Sistemas Operacionais;
- Associa cada usuário a um grupo de usuários que compartilham arquivos e diretórios;
- Existe três níveis de proteção: owner (dono), group (grupo) all (todos);
- Necessário associar o tipo do acesso (leitura, escrita, execução e eliminação) aos três níveis de proteção.

### Lista de Controle de Acesso (Access Control List - ACL):

- Consiste em uma lista associada a cada arquivos, especificando usuários e tipos de acesso permitido;
- O Sistema Operacional verifica se a lista de controle autoriza a operação desejada pelo usuário;
- A estrutura pode ter um tamanho bastante extenso considerando que um arquivo pode ter seu acesso compartilhado por diversos usuários;
- A pesquisa sequencial na lista pode causar overhead.


## Alocação de Espaço em Disco

O Sistema Operacional possui uma estrutura de dados que armazena informações que possibilitam ao sistema de arquivos gerenciar as áreas ou blocos livres.

Nessa estrutura, geralmente uma lista ou tabela, é possível identificar blocos livres que poderão ser alocados por um novo arquivo.

Quando um arquivo é eliminado, todos os seus blocos são liberados para a estrutura de espaços livres.

- Mapa de Bits:
  - Forma mais simples de implementar uma estrutura de espaços livres;
  - Cada entrada da tabela é associada a um bloco do disco representado por um bit que pode ser 0 (livre) ou 1 (ocupado).
- Lista encadeada:
  - Existe uma lista encadeada de todos os blocos livres do disco;
  - Cada bloco possui uma área reservada para armazenamento do endereço do próximo bloco;
  - A partir do primeiro bloco livre pode-se ter acesso sequencial aos demais de forma encadeada;
  - Problema: para se achar espaço livre, o algoritmo deve sempre realizar uma pesquisa sequencial na lista.
- Blocos Contíguos:
  - Blocos contíguos são geralmente alocados ou liberados simultaneamente;
  - Enxerga o disco como um conjunto de segmentos de blocos livres;
  - Possível manter uma tabela com o endereço do primeiro bloco de cada segmento e o número de blocos livres contíguos que se seguem.

### Alocação Contígua

A alocação contígua consiste em armazenar um arquivo em blocos sequencialmente dispostos, permitindo ao sistema localizar um arquivo através do endereço do primeiro bloco e da sua extensão em blocos. O aceso é feito de maneira simples, tanto para a forma sequencial quanto para a direta.

Um problema desse tipo de alocação é que quando um arquivo é criado com n blocos, é necessário que exista uma cadeia de n blocos livres disposto sequencialmente. Nesse tipo de alocação, o disco é visto como um grande vetor, com segmentos ocupados e livres.

A alocação em um novo segmento livre consiste técnicas para escolha, algumas das principais são:

- First-fit: Seleciona o primeiro segmento livre com o tamanho suficiente para alocar o arquivo e a busca é feita sequencialmente, interrompendo ao achar um segmento livre do tamanho adequado.
- Best-fit: Seleciona o menor segmento livre disponível com o tamanho suficiente para armazenar o arquivo e é necessária a busca em toda a lista, caso esta não esteja ordenada por tamanho.
- Worst-fit: Seleciona o maior segmento livre e a busca funciona como no caso anterior.

>Um problema na alocação contígua é a fragmentação dos espaços livres causado pela criação e eliminação constante de arquivos é que com o tempo surgem espaços vagos sem o tamanho suficiente para se alocar novos arquivos.

A desfragmentação busca solucionar o problema da fragmentação, reorganizando os arquivos no disco de maneira que só exista um único segmento de blocos. A desfragmentação é lenta e deve ser realizada periodicamente.

### Alocação Encadeada

>Na alocação encadeada um arquivo pode ser organizado como um conjunto de blocos ligados logicamente no disco, independente da sua localização física, sendo que cada bloco possui um ponteiro para o bloco seguinte do arquivo e assim sucessivamente.

Neste tipo de alocação, ocorre grande fragmentação dos arquivos devido aos blocos livres dos arquivos não precisarem ser contíguos, existe a quebra do arquivo em diversos pedaços, denominados extents. Essa fragmentação aumenta o tempo de acesso aos arquivos, pois exige que o mecanismo de leitura/gravação se desloque diversas vezes sob sua superfície. Dessa forma se torna necessário a execução da operação de desfragmentação periodicamente

Um problema na alocação encadeada é que ela só permite o acesso sequencial aos blocos dos arquivos, não possuindo acesso direto aos blocos e desperdiça espaço nos blocos com o armazenamento de ponteiros.

### Alocação Indexada

A alocação indexada soluciona o problema da alocação encadeada referente ao acesso direto aos blocos dos arquivos pois mantém os ponteiros de todos os blocos do arquivo em uma única estrutura denominada bloco de índice.