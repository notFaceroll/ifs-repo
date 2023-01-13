# Sistemas Operacionais 2nd Unidade

Table of contents
- [Gerência do Processador](#gerência-do-processador)
  - [Política de Escalonamento](#política-de-escalonamento)
  - [Critérios de Escalonamento](#critérios-de-escalonamento)
  - [Classificação](#classificação)
    - [Não Preemptivo](#não-preemptivo)
    - [Preemptivo](#preemptivo)
  - [Escalonamentos](#escalonamentos)
- [Gerência de Memória](./gerencia-memoria.md)
  - [Funções Básicas](#funções-básicas)
  - [Alocação Contígua Simples](#alocação-contígua-simples)
  - [Técnica de Overlay](#técnica-de-overlay)
  - [Alocação Particionada](#alocação-particionada)
    - [Estática (ou fixa)](#estática-ou-fixa)
    - [Dinâmica (ou variável)](#dinâmica-ou-variável)
  - [Estratégias de alocação de Partição](#estratégias-de-alocação-de-partição)
  - [Swapping](#swapping)

## Gerência do Processador
O Escalonamento (Scheduling) determina qual processo será escolhido para fazer uso do processador. Os critérios utilizados para esta seleção compõem a chamada Politica de Escalonamento.

### Política de Escalonamento
- Manter o processador ocupado na maior parte do tempo;
- Balancear o uso da UCP entre processos;
- Privilegiar a execução de aplicações críticas;
- Maximizar o throughput do sistema;
- Oferecer tempos de resposta razoáveis para usuários interativos;
- Evitar *Starvation*

### Critérios de Escalonamento
- **Utilização do Processador** (%);
  - Em geral, é desejável que o processador permaneça a maior parte do tempo ocupado;
- **Throughput** representa o número de processos executados em um determinado intervalo de tempo;
- **Tempo de Processador** é o tempo que um processo leva no estado de execução durante;
- **Tempo de Espera** é o tempo que um processo permanece na fila de pronto;
- **Tempo de Turnaround** é o tempo que um processo leva desde a sua criação até o seu término;
  - Considera tempo de espera para alocação de memória, espera na fila de processos prontos, processamento e operações de entrada e saída.
  - Em geral, a minimização do tempo de turnaround é desejada.

### Classificação
#### Não Preemptivo
O processo somente sai do estado de execução quando termina seu processamento ou quando executa alguma instrução que ocasione uma mudança para o estado de espera.
- Existente nos primeiros sistemas multiprogramáveis, onde predominava o processamento batch.
- Quando um processo (JOB) ganha o direito de utilizar a CPU, nenhum outro processo pode lhe tirar esse recurso;
#### Preemptivo
O sistema operacional pode interromper um processo em execução e passa-lo para o estado de pronto.
- Permite que o sistema dê atenção imediata a processos mais prioritários, como no caso de sistemas em tempo real.
- Proporciona melhores tempos de resposta em sistemas de tempo compartilhado;
- Compartilhamento do processador de uma maneira mais uniforme entre os processos.
>Preempção - possibilidade do sistema operacional interromper um processo em execução e substituí-lo por um outro.

### Escalonamentos
- **Shortest-Job-First** (SJF):
  - Não preemptivo;
  - Associa cada processo (JOB) ao seu tempo de execução.
  - Quando o processador está livre, o processamento que ocupar menos tempo da CPU para terminar seu processamento é selecionado.
  - Favorece os programas menores.
- **Cooperativo**: O processo pode voluntariamente liberar o processador, retornando à fila de pronto;
  - Permite uma melhor distribuição do processador entre os processos.
  - Não existe intervenção do Sistema Operacional na execução do processo.
- **Round Robin** (Circular);.
  - Preemptivo (time-slice);
  - Implementado por um algoritmo semelhante ao FIFO, porém, quando um processo passa para o estado de execução, existe um tempo-limite (quantum ou time-slice) para sua utilização de forma contínua. Caso a fatia de tempo expire, o sistema operacional interrompe o processo em execução e direciona-o para o fim da fila de pronto;
- **Por Prioridades**:
  - Realizado com base em um valor associado a cada processo denominado prioridade de execução;
  - Processos possuem diferentes prioridades de execução.
  - Processos de maior prioridade são escalonados preferencialmente.
  - Algoritmo Implementado mediante um clock, que interrompe o processador em determinados intervalos de tempo, reavaliando prioridades e, possivelmente, escalonando outro processo.
  - Todos os sistemas de tempo compartilhado implementam algum tipo de prioridade, sendo esta uma característica do contexto de software.
- **Circular com Prioridades**:
  - Preemptivo;
- **Por Múltiplas filas**:
  - Implementa diversas filas de processos no estado pronto, onde cada processo é associado exclusivamente a uma delas.
  - Cada fila possui um mecanismo próprio de escalonamento, em função das características dos processos.
  - Cada fila possui uma prioridade associada.
  - O sistema só pode escalonar processos de uma fila, se todas as outras de prioridade maior estiverem vazias.
- **Por Múltiplas filas com realimentação**:
  - Também Implementa diversas filas onde cada uma tem uma prioridade de execução associada, porém, os processos não permanecem em uma mesma fila até o término do processamento.
  - O sistema identifica dinamicamente o comportamento de cada processo, ajustando assim suas prioridades de execução e mecanismos de escalonamento.
  - Os processos não são previamente associados às filas de pronto, e sim direcionados pelo sistema entre as diversas filas com base em seu comportamento.
  - Execução:
    - Processo criado entra no final da fila de mais alta prioridade.
    - Cada fila implementa o mecanismo de FIFO para escalonamento.
    - Quando o processo em execução deixa a CPU por preempção por prioridade ou por solicitação a um recurso do sistema ele é reescalonado para dentro da mesma fila.
    - Caso o processo esgote seu quantum de tempo, ele é redirecionado para um a fila de menor prioridade (preempção por tempo), e assim por diante.
    - A fila de mais baixa prioridade implementa o mecanismo de escalonamento circular.
    - O quantum em cada fila varia em função da sua prioridade. Quanto maior a prioridade, menor seu quantum de tempo.

  - Atende as necessidades dos diversos tipos de processos.
  - Pode ser implementado em qualquer tipo de Sistema Operacional.

## Gerência de Memória

### Funções Básicas
O sistema operacional transfere os programas da memória secundária para a memória principal antes de serem executados.
Como o tempo de acesso à memória secundária é muito superior ao tempo de acesso à memória principal, o sistema operacional deve buscar reduzir o número de operações de E/S à memória secundária.

A gerência de memória deve tentar manter na memória principal o maior número de processos residentes.
Mesmo na ausência de espaço livre, o sistema deve permitir que novos processos sejam aceitos e executados. (Swapping)
Permitir que a execução de programas que sejam maiores que a memória física disponível. (overlay e memória virtual)
O sistema operacional deve proteger as áreas de memória ocupadas por cada processo, além da área onde reside o próprio sistema operacional.
Oferecer mecanismos de compartilhamento para que diferentes processos possam trocar dados de forma protegida.

### Alocação Contígua Simples
- Em sistemas monoprogramáveis
- Subutilização da memória principal

### Técnica de Overlay
O programa é dividido em módulos. Cada módulo pode ser executado independentemente dos outros.

### Alocação Particionada
#### Estática (ou fixa)
A memória é dividida em pedaços de tamanho fixo, chamados de **partições**.
Conceitos:
- **Código absoluto** - Todas as referências a endereços no programa são posições físicas na memória principal.
- **Código Relocável** - Todas as referências a endereços no programa são relativas ao início do código, e não a endereços físicos de memória.
- **Fragmentação Interna** - Fragmentação dentro da partição.

#### Dinâmica (ou variável)
Eliminando o conceito de partições de tamanho fixo, cada programa utilizaria o espaço necessário, tornando esta área sua partição.
- **Fragmentação Externa** - ??

### Estratégias de alocação de Partição
Determinar em qual área livre um programa será carregado para execução.
O sistema operacional possui uma lista de áreas livres, com o endereço e tamanho de cada área.

- Best-fit: A melhor partição é escolhida;
- Worst-fit: A pior (maior) partição é escolhida;
- First-fit: A primeira partição que couber é a escolhida.

### Swapping
- Contorna o problema da insuficiência de memória principal;
- Programas que esperam por memória livre para serem executados;
- Swap out - transferência da memória principal para a memória secundária;
- Swap in - quando o processo é carregado de volta da memória secundária para a memória principal.
> - Residentes: Estão na memória principal.
> - Não residentes (outswapped): Estão na área de swap.
A escolha do processo a ser retirado deve priorizar o processo que tem menos chances de ser escalonado, geralmente um processo em estado de espera.
O sistema deve oferecer **realocação dinâmica**.



## Memória Virtual 💻

Algoritmos de Substituição de Páginas
Selecionar os frames que tenham as menores chances de serem referenciados em um futuro próximo.
- Aleatório - não utiliza critério algum de seleção.
- FIFO (First-In-First-Out) - seleciona a página que está há mais tempo na memória principal.
- LFU (Least-Frequently-Used) - seleciona a página menos referenciada, ou seja, o frame menos utilizado.
- LRU (Least-Recently-Used) - seleciona a página na memória principal que está há mais tempo sem ser referenciada.