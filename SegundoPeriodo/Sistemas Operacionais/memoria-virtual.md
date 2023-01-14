# Memória Virtual 💻

## Conceitos

- Combina memória principal e secundária;
- Impressão da memória ser muito maior do que é;
- Permite também um número maior de processos compartilhando a memória principal, já que apenas partes de cada processo estarão residentes;
- Desvinculação do endereçamento feito pelo programa dos endereços físicos da memória principal;
- Procura minimizar o problema de fragmentação da memória.

## Espaço de Endereçamento Virtual

- Conceito próximo a vetores em linguagens de alto nível;
- O sistema operacional utiliza a memória secundária como extensão da memória principal;
- Referência a um componente do vetor sem preocupação com a posição da memória onde o dado está;
- Programa no ambiente de memória virtual não faz referência a endereços físicos de memória (endereços reais), mas apenas a endereços virtuais;
- Mapeamento – é a tradução do endereço virtual para o físico;
- Espaço de endereçamento virtual – é o conjunto de endereços virtuais que os processos podem endereçar.
- Espaço de endereçamento real – é o conjunto de endereços reais.
- Apenas parte do programa pode estar residente na memória em um determinado instante;
- O Sistema Operacional utiliza a memória secundária como uma extensão da memória principal.

## Mapeamento

>Mecanismo que transforma os endereços virtuais em endereços reais;

- Todo programa precisa estar nos espaços de endereçamento real para poder ser referenciado ou executado;
- Atualmente, o mapeamento é realizado via hardware (Memory Management Unit - MMU) junto com o Sistema Operacional, de forma a não comprometer seu desempenho e torná-lo transparente aos usuários e suas aplicações;
- A maioria das aplicações tende a fazer referência a um reduzido número de páginas, logo, somente uma pequena fração da tabela de páginas é necessária.
- Memória associativa ou Translation Lookside Buffer – Hardware especial para mapear endereços virtuais para endereços físicos sem a necessidade de acesso à tabelas de páginas;
- Quando um programa está em execução, existe uma tabela de mapeamento do processo no qual o programa executa. Se outro programa for executado no contexto de outro processo, o sistema deve passar a referenciar a tabela do novo processo. Toda vez que há mudança de contexto, o registrador é atualizado com o endereço da nova tabela.

## Paginação

>Técnica de gerência de memória onde o espaço de endereçamento virtual e o espaço de endereçamento real são divididos em blocos do mesmo tamanho (páginas);

- Páginas virtuais no espaço virtual e páginas reais ou frames (molduras) no espaço real;
- Todo mapeamento é realizado a nível de página, através de tabelas de páginas, em que cada página virtual do processo possui uma entrada na tabela ETP (entrada na tabela de páginas);
- Cada processo possui sua própria tabela de páginas;
- Cada página virtual do processo possui uma entrada na tabela;

- **Políticas de busca de páginas**:

  - Paginação por demanda é quando as páginas dos processos são transferidas da memória secundária para a principal apenas quando são referenciadas.
  - Paginação Antecipada é o carregamento de páginas na memória antecipadamente, sendo que o sistema tenta prever as páginas que serão necessárias à execução do programa.

- **Políticas de alocação de páginas**:

> Quantos frames cada processo pode manter na memória

- **Alocação física** - Cada processo tem um número máximo de frames que pode ser utilizado durante a execução do programa;
- **Alocação variável** - O número máximo de páginas alocadas ao processo pode variar durante sua execução em função de sua taxa de paginação e da ocupação da memória principal.

### Working Set

> Working Set de um processo é o conjunto de páginas referenciadas por ele durante determinado intervalo de tempo, ou, segundo Denning, é o conjunto de páginas constantemente referenciadas pelo processo, devendo permanecer na memória principal para que execute de forma eficiente, evitando a elevada taxa de paginação (thrashing).

- Sempre que um processo é criado, todas as suas páginas estão na memória secundária.
- O Working Set deve Ter um limite máximo de páginas permitidas.

Problemas:
- Paginações exigem operações de E/S (que deve ser evitado) quando um processo faz referência a uma página que não se encontra na memória;
- O Sistema Operacional deve se preocupar em ter um certo número de páginas na memória que reduza ao máximo a taxa de paginação dos processos e não prejudique os demais processos que desejam acesso a memória.

Observações:
- Quando um programa começa a ser executado, percebe-se uma elevada taxa de page faults (páginas que não se encontram na memória), que se estabiliza com o decorrer de sua execução.

**Localidade** é a tendência que existe em um programa de fazer referências a posições de memória de forma quase uniforme, ou seja, instruções próximas.
- ***Localidade espacial***: tendência de que após uma referência a uma posição de memória sejam realizadas novas referências a endereços próximos;
- ***Localidade temporal***: tendência de que após a referência a uma posição de memória esta mesma posição seja novamente referenciada em um curto intervalo de tempo.



### Realocação de Páginas

Problema em decidir quais páginas remover da memória principal.
O Sistema Operacional deve considerar se uma página foi ou não modificada antes de liberá-la para outro processo, caso contrário, possíveis dados armazenados na página serão perdidos.
Sempre que uma página é alterada, um bit de modificação é alterado de 0 para 1, informando que a página foi alterada.
Melhor estratégia de realocação é escolher uma página que não será referenciada num futuro próximo. Tarefa difícil para o Sistema Operacional.

#### Algoritmos de substituição de páginas:

##### Aleatório (random):

- Não utiliza nenhum critério de seleção.
- Consome menos recursos do sistema.
- Raramente é utilizada.

##### First-In-First-Out (FIFO):

- A página que primeiro foi utilizada será a primeira a ser escolhida.
- Implementação bastante simples.
- Necessário apenas uma fila. 

##### Least-Recently-Used (LRU):

- Seleciona a página utilizada menos recentemente, ou seja, a que está há mais tempo sem ser referenciada.
- Estratégia boa, mas pouco implementada;
- Grande overhead causado pela atualização, em cada página referenciada, do momento do último acesso, além do algoritmo de busca dessas páginas. 

##### Not-Recently-Used (NRU):

- Escolha da página que não foi recentemente utilizada (semelhante ao LRU).
- Flag de referência – indica quando a página foi referenciada ou não.
- Inicialmente, todas as páginas estão com o flag = 0, à medida que as páginas são referenciadas, o flag é modificado para 1. 

##### Last-Frequently-Used (LFU):

- Escolhe a página menos referenciada.
- Existe um controle do número de referências feitas às páginas.
- É escolhida a página que o contador tem o menor número de referências.
- Problema – As páginas que entrarem mais recentemente no working set serão as que estarão com o menor número no contador.

##### FIFO com buffer de páginas:

- Combina uma lista de páginas alocadas (LPA) com uma lista de páginas livres(LPL).

##### FIFO Circular (clock):

- As páginas alocadas na memória estão em uma estrutura de lista circular, semelhante a um relógio.

### Tamanho da Página

- Tamanho da página associado ao hardware e varia de sistema para sistema, normalmente entre 512 K e 16 M endereços.
- Tem impacto direto no número de entradas na tabela de páginas, no tamanho da tabela e no espaço ocupado.
- Paginação leva a uma menor fragmentação, pois apenas poderá haver fragmentação na última página.
- A fragmentação é consequência do tamanho da página.
- Páginas pequenas necessitam de tabelas maiores, provocando uma taxa de paginação e número de acesso à memória secundária maior.


### Translation Lookaside Buffer

- A gerência de memória virtual utiliza a técnica de mapeamento para traduzir endereços virtuais em endereços reais.
- Isso implica em 2 acessos à memória: 1 para acessar a tabela de páginas e outro para acessar a própria página.
- Pelo princípio da localidade, somente uma pequena fração da tabela de mapeamento é realmente necessária.
- TLB - mapear endereços virtuais em endereços físicos sem a necessidade do acesso à tabela de páginas.

- Funciona como uma memória cache, com traduções mais recentemente referenciadas.
- Utiliza o esquema de mapeamento associativo, que verifica simultaneamente em todas as entradas a presença do endereço virtual.
- As traduções dos endereços virtuais podem ser armazenadas em qualquer posição da cache.

- Caso o endereço virtual (tag) esteja na cache, o endereço físico é utilizado, eliminando o acesso à tabela de mapeamento (TLB hit).
- Caso o endereço não esteja na cache, a tabela de mapeamento deve ser consultada (TLB miss).
- Se a página estiver na MP, a tradução é colocada no TLB e o endereço é traduzido.
- Caso contrário, ocorre page fault, a página é carregada para MP, a tabela de mapeamento é atualizada e a

- Geralmente, a TLB contém apenas informações do processo em execução.
- Quando há uma mudança de contexto a TLB deve ser reinicializada com informações da tabela de mapeamento do novo processo.
- Caso a TLB possa armazenar endereços de vários processos, deve existir um campo adicional em cada entrada da TLB para a identificação do processo.

- Geralmente, a política de realocação de entradas da TLB é aleatória e, mais raramente, utiliza-se a política NRU.
- A TLB é essencial para reduzir o número de operações de acesso à memória principal em sistemas que implementam memória virtual.
- A taxa de TLB hits é muito alta, reduzindo significativamente o impacto da gerência de memória virtual no desempenho do sistema.

## Segmentação

>Segmentação é um procedimento da gerência de memória, onde os programas são divididos em sub-rotinas e estruturas de dados, e depois são colocados em blocos de informações na memória que possuem tamanhos diferentes com seu próprio espaço de endereçamento.

A diferença entre a paginação e a segmentação é que, o primeiro divide o programa em partes de tamanho fixo, sem qualquer ligação com a estrutura do programa, já o segundo permite uma relação entre a lógica do programa e sua divisão na memória. O mecanismo de mapeamento é muito semelhante ao da paginação, com o uso de tabelas de segmentos. Além do endereço do segmento na memória física, cada entrada na tabela possui informações sobre o tamanho do segmento e se ele está ou não na memória.

O sistema operacional mantém uma tabela com as áreas livres e ocupadas da memória. Quando um novo processo é carregado para a memória, o sistema localiza um espaço livre que o acomode. Apenas os segmentos referenciados são transferidos para a memória real.

- Técnica de gerência de memória, onde os programas são divididos logicamente e em sub-rotinas e estruturas de dados e colocados em blocos de informações na memória
- Segmentos são blocos de tamanhos diferentes com seu próprio espaço de endereçamento.

- A escolha da área livre a ser ocupada por um processo a ser carregado na memória pode ser a mesma utilizada no item Alocação Particionada Dinâmica (best-fit, worst-fit ou first-fit).

- Os programas devem ser bem modularizados para uma maior eficiência.
- Existe também o problema da fragmentação e o problema da complexibilidade.

### Segmentação com Paginação

Permite a divisão lógica dos programas e segmentos e, cada segmento é dividido fisicamente em páginas.

Um endereço é formado pelo número do segmento, pelo número de página, contida nesse segmento, e pelo deslocamento dentro dessa página.

O endereço físico é obtido somando-se a posição inicial do frame e o deslocamento.

## Proteção

- Necessária para impedir que um processo, ao acessar uma página/segmento do sistema, a modifique ou mesmo tenha acesso a ela.
- No esquema de memória virtual, cada processo tem sua própria tabela de mapeamento e a tradução dos endereços é realizada pelo sistema, impedindo assim, que um processo tenha acesso a áreas de memória de outros processos, a não ser que tenham compartilhamento explícito.
- A proteção deve ser realizada em nível de cada página/segmento na memória, utilizando-se as entradas da tabela de mapeamento, com alguns bits especificando permissões a cada uma das páginas/segmentos.

## Compartilhamento de Memória

- Bastante útil para programas de código reentrante.
- Bastante simples implementação do compartilhamento de código e dados entre vários processos, bastando que as entradas das tabelas de páginas/segmentos apontem para as mesmas páginas/segmentos na memória principal.
- Reduz o número de programas na memória principal e aumenta o número de usuários compartilhando o mesmo recurso.
- Segmentação X Paginação em relação ao compartilhamento:
- O compartilhamento de segmentos é mais simples que o de páginas, pois as tabelas de segmentos mapeiam estruturas lógicas, como sub-rotinas e estruturas de dados.
- Enquanto o mapeamento de um vetor necessita de várias entradas na tabela de páginas, na tabela de segmentos é necessária apenas uma única entrada.
- O segmento pode variar seu tamanho durante a execução com o crescimento de um vetor, por exemplo, na paginação, isso implica na alocação de novas páginas.

## Swapping em Memória Virtual

- Quando existem novos processos que desejam ser processados e não existe memória real suficiente, o sistema seleciona um ou mais processos que deverão sair da memória para ceder espaço aos novos processos.
- Os critérios mais utilizados para a escolha são a prioridade,  escolhendo processos de melhor prioridade, e o estado do processo, selecionando os processos que estão no estado de espera.

## Thrashing

>É a excessiva transferência de páginas/segmentos entre a memória principal e a memória secundária. Problema existente tanto em paginação quanto a segmentação.

Na **Paginação**:
- A nível de processo:

O working set de um processo pode ser pequeno demais para acomodar as páginas constantemente acomodadas referenciadas por ele, a solução é aumentar o tamanho do working set.
O thrashing também pode ocorrer pela não obediência do conceito da localidade, ou seja, o programa faz referência a comandos/dados localizados em páginas fora do working set do processo e a solução para isso é reescrever a aplicação.

- A nível de sistema:

O trashing ocorre quando existem mais processos competindo por memória que espaço disponível.
O primeiro passo é a redução do tamanho dos working set dos processos, mas isso pode levar o thrashing a nível de processo.
<hr>

Na **Segmentação**:
- Em nível de processo, quando a transferência de segmentos é excessiva devido a modularização extrema do programa não seguindo o conceito da modularidade.
- Em nível de sistema é semelhante ao caso da paginação.

Em qualquer caso, se existem mais processos para serem executados que a memória real disponível, a única solução é expandir a memória principal. Este problema ocorre em todos os sistemas que possuem um mecanismo de gerência de memória.