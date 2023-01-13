# Sistemas Operacionais 2nd Unidade

Table of contents
- [Gerência do Processador](#gerência-do-processador)


## Gerência do Processador
O Escalonamento (Scheduling) determina qual processo será escolhido para fazer uso do processador. Os critérios utilizados para esta seleção compõem a chamada Politica de Escalonamento.

### Política de Escalonamento
- Manter o processador ocupado na maior parte do tempo;
- Balancear o uso da UCP entre processos;
- Privilegiar a execução de aplicações críticas;
- Maximizar o throughput do sistema;
- Oferecer tempos de resposta razoáveis para usuários interativos.

### Critérios de Escalonamento
- Utilização do Processador (%);
- Throughput representa o número de processos executados em um determinado intervalo de tempo;
- Tempo de Processador é o tempo que um processo leva no estado de execução durante;
- Tempo de Espera é o tempo que um processo permanece na fila de pronto;
- Tempo de Turnaround é o tempo que um processo leva desde a sua criação até o seu término;

### Classificação
#### Não Preemptivos
O processo somente sai do estado de execução quando termina seu processamento ou quando executa alguma instrução que ocasione uma mudança para o estado de espera.
#### Preemptivo
O sistema operacional pode interromper um processo em execução e passa-lo para o estado de pronto.
>Preempção - possibilidade do sistema operacional interromper um processo em execução e substituí-lo por um outro.

### Escalonamentos
- Shortest-Job-First (SJF):
  - Não preemptivo;
- Cooperativo: O processo pode voluntariamente liberar o processador, retornando à fila de pronto;
- Round Robin (Circular);.
  - Preemptivo (time-slice);
  - Caso a fatia de tempo expire, o sistema operacional interrompe o processo em execução e direciona-o para o fim da fila de pronto;
- Por Prioridades:
  - Realizado com base em um valor associado a cada processo denominado prioridade de execução;
- Circular com Prioridades:
  - Preemptivo;
- Por Múltiplas filas;
- Por Múltiplas filas com realimentação.