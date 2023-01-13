# Gerência do Processador

O Escalonamento (Scheduling) determina qual processo será escolhido para fazer uso do processador. Os critérios utilizados para esta seleção compõem a chamada Politica de Escalonamento.

## Política de Escalonamento

- Manter o processador ocupado na maior parte do tempo;
- Balancear o uso da UCP entre processos;
- Privilegiar a execução de aplicações críticas;
- Maximizar o throughput do sistema;
- Oferecer tempos de resposta razoáveis para usuários interativos;
- Evitar *Starvation*

## Critérios de Escalonamento

- **Utilização do Processador** (%);
  - Em geral, é desejável que o processador permaneça a maior parte do tempo ocupado;
- **Throughput** representa o número de processos executados em um determinado intervalo de tempo;
- **Tempo de Processador** é o tempo que um processo leva no estado de execução durante;
- **Tempo de Espera** é o tempo que um processo permanece na fila de pronto;
- **Tempo de Turnaround** é o tempo que um processo leva desde a sua criação até o seu término;
  - Considera tempo de espera para alocação de memória, espera na fila de processos prontos, processamento e operações de entrada e saída.
  - Em geral, a minimização do tempo de turnaround é desejada.

## Classificação

### Não Preemptivo

O processo somente sai do estado de execução quando termina seu processamento ou quando executa alguma instrução que ocasione uma mudança para o estado de espera.
- Existente nos primeiros sistemas multiprogramáveis, onde predominava o processamento batch.
- Quando um processo (JOB) ganha o direito de utilizar a CPU, nenhum outro processo pode lhe tirar esse recurso;

### Preemptivo

O sistema operacional pode interromper um processo em execução e passa-lo para o estado de pronto.
- Permite que o sistema dê atenção imediata a processos mais prioritários, como no caso de sistemas em tempo real.
- Proporciona melhores tempos de resposta em sistemas de tempo compartilhado;
- Compartilhamento do processador de uma maneira mais uniforme entre os processos.
>Preempção - possibilidade do sistema operacional interromper um processo em execução e substituí-lo por um outro.

## Escalonamentos

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