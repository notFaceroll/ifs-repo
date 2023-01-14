# Gerência de Memória

- [Funções Básicas](#funções-básicas)
  - [Alocação Contígua Simples](#alocação-contígua-simples)
  - [Técnica de Overlay](#técnica-de-overlay)
  - [Alocação Particionada](#alocação-particionada)
    - [Estática (ou fixa)](#estática-ou-fixa)
    - [Dinâmica (ou variável)](#dinâmica-ou-variável)
  - [Estratégias de alocação de Partição](#estratégias-de-alocação-de-partição)
  - [Swapping](#swapping)

## Funções Básicas

O sistema operacional transfere os programas da memória secundária para a memória principal antes de serem executados.
Como o tempo de acesso à memória secundária é muito superior ao tempo de acesso à memória principal, o sistema operacional deve buscar reduzir o número de operações de E/S à memória secundária.

A gerência de memória deve tentar manter na memória principal o maior número de processos residentes.
Mesmo na ausência de espaço livre, o sistema deve permitir que novos processos sejam aceitos e executados. (Swapping)
Permitir que a execução de programas que sejam maiores que a memória física disponível. (overlay e memória virtual)
O sistema operacional deve proteger as áreas de memória ocupadas por cada processo, além da área onde reside o próprio sistema operacional.
Oferecer mecanismos de compartilhamento para que diferentes processos possam trocar dados de forma protegida.

## Alocação Contígua Simples

- Em sistemas monoprogramáveis
- Subutilização da memória principal

## Técnica de Overlay

O programa é dividido em módulos. Cada módulo pode ser executado independentemente dos outros.

## Alocação Particionada

### Estática (ou fixa)

A memória é dividida em pedaços de tamanho fixo, chamados de **partições**.
Conceitos:
- **Código absoluto** - Todas as referências a endereços no programa são posições físicas na memória principal.
- **Código Relocável** - Todas as referências a endereços no programa são relativas ao início do código, e não a endereços físicos de memória.
- **Fragmentação Interna** - Fragmentação dentro da partição.

### Dinâmica (ou variável)

Eliminando o conceito de partições de tamanho fixo, cada programa utilizaria o espaço necessário, tornando esta área sua partição.
- **Fragmentação Externa** - ??

## Estratégias de alocação de Partição

Determinar em qual área livre um programa será carregado para execução.
O sistema operacional possui uma lista de áreas livres, com o endereço e tamanho de cada área.

- Best-fit: A melhor partição é escolhida;
- Worst-fit: A pior (maior) partição é escolhida;
- First-fit: A primeira partição que couber é a escolhida.

## Swapping

- Contorna o problema da insuficiência de memória principal;
- Programas que esperam por memória livre para serem executados;
- Swap out - transferência da memória principal para a memória secundária;
- Swap in - quando o processo é carregado de volta da memória secundária para a memória principal.
> - Residentes: Estão na memória principal.
> - Não residentes (outswapped): Estão na área de swap.
A escolha do processo a ser retirado deve priorizar o processo que tem menos chances de ser escalonado, geralmente um processo em estado de espera.
O sistema deve oferecer **realocação dinâmica**.
