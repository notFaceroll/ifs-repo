# Evolução de Software - (Em progresso)

Tópicos:
- Mudanças são inevitáveis para manter softwares úteis
- Processos de evolução de software
- Diferentes tipos de manutenção de software
- Gerenciamento de sistemas legados


## Importância da evolução

Softwares são investimentos, para manter o valor agregado e retorno viáveis ao negócio, esses softwares precisam de atualizações.

Grande (se não a maior) parte do orçamento dedicado a softwares é em evolução do sistema existente e não no desenvolvimento de um novo.

A evolução, por alto, funciona como uma espiral, revisitando tarefas e etapas anteriores, de modo a refinar e adaptar o sistema ao novo padrão evoluído.

Especificação -> Implementação -> Validação -> Operação -> Especificação -> ...

Evolução x em serviço

- Evolução é quando o sistema evolui a medida que novas implementações são realizadas
- Em serviço, o software continua sendo útil, porém mudanças feitas nele são apenas para mantê-lo útil. Não são acrescentadas novas funcionalidades.
- Interrupção gradual -> O software ainda pode ser usado, mas nenhuma outra alteração é realizada nele.

## Processos de identificação de mudanças e de evolução

Novo sistema -> Processo de identificação de mudanças -> Propostas de mudança -> Processo de evolução -> Novo sistema -> ...

## Processo de evolução

- Solicitação da mudança
- Análise de impacto
- Planejamento de release
  - Correção de defeitos
  - Adaptação da plataforma
  - Aperfeiçoamento do sistema
- Implementação da mudança -> Planejamento de release
- Liberação do sistema -> Solicitação de mudança

### Implementação da mudança

- Mudanças propostas
- Análise de requisitos -> Mudanças propostas
- Atualização de requisitos
- Desenvolvimento de software

> Uma mudança urgente pode precisar ser implementada sem passar por todas essas fases

- Defeito grave deixando o sistema inoperável
- Mudanças ao ambiente do sistema tem efeito inesperado
- Mudanças de negócios que exigem resposta rápida
- etc

### Métodos ágeis e evolução

Como estes são baseados em desenvolvimento incremental, a evolução é imperceptível e pode ser dada simplesmente como a continuação do desenvolvimento baseada em versões frequentes.


## Manutenção de software

É basicamente uma maneira de verificar a integridade de um software, geralmente não envolvendo mudanças importantes na arquitetura. As mudanças são implementadas por meio da modificação de componentes existentes ou pela adição de novos ao sistema.

### Tipos

- Corretiva (correção de deficiências, ex.: erros no código)
- Adaptativa (adaptação do software, ex.: Mudança do OS)
- Perfectiva (adicionar ou modificar funcionalidades)

A maior parte dos esforços de manutenção é na parte perfectiva.

### Custos

Geralmente maiores do que os de desenvolvimento, estes aumentam na medida em que o software é mantido. Softwares velhos podem ter altos custos de suporte.
Custos podem reduzir por conta da familiaridade da equipe com o software.

### Reengenharia de software

A reestruturação ou reescrita de parte ou da totalidade de um sistema legado, sem alterar sua funcionalidade, podendo reduzir riscos e custos.

>Reengenharia nada mais é do que reorganizar e modificar o software com o objetivo de torná-lo mais fácil de manter. 

Atividades do processo:
- Tradução do código fonte
- Engenharia reversa
  - Análise do programa para compreensão
- Melhoria de estrutura de programa
- Modularização
- Reengenharia de dados

#### Fatores de Custo

- Qualidade do software em questão
- Ferramentas de apoio para a execução
- Extensão da conversão de dados
- Disponibilidade de pessoal especializado
  - Pode ser um problema em sistemas legados por conta das techs não mais utilizadas

### Manutenção preventiva por refatoração

> Processo de fazer melhorias em um programa para diminuir a degradação gradual resultante das mudanças (*OPDYKE* e *JOHNSON*, 1990).

Ou seja, modificar um programa para melhorar sua estrutura, para reduzir sua complexidade ou para torná-lo mais compreensível. Ao refatorar, deve-se concentrar na melhoria dele e não acrescentar novas funcionalidades.

Refatoração x Reengenharia

- reengenharia ocorre depois que um sistema é mantido por algum tempo e os custos de manutenção são crescentes
- refatoração é um processo contínuo de melhoria por meio do processo de evolução e desenvolvimento.
