# Estratégias de testes de software (Em progresso)

## Panorama

O que é?
- testado para revelar erros cometidos quando o projeto é construído

Quem realiza?
- Gerente de projeto, engenheiros de software e especialistas em testes

Porque é importante (o projeto de testes)?
- Requer esforço e trabalho, obviamente. Logo, é necessário estabelecer uma estratégia sistemática para teste de software.

Quais etapas?
- Várias
- Testes em componentes -> integração entre componentes -> testes em sistemas maiores -> etc.

Como garantir que foi feito corretamente?
- Revisando previamente a especificação do teste antes de realizá-lo. Planos e procedimentos eficazes levarão a uma construção ordenada do software e à descoberta de erros em cada estágio do processo de construção.


> Características genéricas
> - Para executar um teste eficaz, proceder a revisões técnicas eficazes. Fazendo isso, muitos erros serão eliminados antes do começo do teste.
> - O teste começa no nível de componente e progride em direção à integração do sistema computacional como um todo.
> - Diferentes técnicas de teste são apropriadas para diferentes abordagens de engenharia de software e em diferentes pontos no tempo.
> - O teste é feito pelo desenvolvedor do software e (para grandes projetos) por um grupo independente de teste.
> - O teste e a depuração são atividades diferentes, mas a depuração deve ser associada com alguma estratégia de teste.

## Abordagem estratégica

### Verificação e validação

Verificação refere-se ao conjunto de tarefas que garantem que o software implementa corretamente uma função específica. Validação refere-se a um conjunto de tarefas que o software foi criado e pode ser rastreado segundo os requisitos do cliente. Segundo *Boehm*:

- Verificação: "Estamos criando o produto corretamente?"
- Validação: "Estamos criando o produto certo?"

Falha causada por um erro gerado por um defeito
Defeito -gera-> Erro -causa-> Falha no sistema 

Inspeções x Testes

- Na inspeção não há execução do sistema
- Versões incompletas podem ser inspecionadas sem problemas
- Ideal para identificar ineficácia em algoritmos e código ilegível (QA)
- Inspeções são melhores para descobertas de defeitos
- Testes encontram defeitos ocorridos entre interações inesperadas de sistemas

Testes manuais x Testes automatizados

### Modelo de processo
Projetar casos -> Preparar dados -> Executar programa com os dados -> Comparar resultados para os casos -> Relatório


### Estágios / Fases de teste

Testes de:
- Desenvolvimento
  - Unitários
  - Componentes
  - Sistema
- Lançamento (release)
- Usuário

#### Desenvolvimento

- Descoberta de defeitos
- Intercalado com depuração (localização de problemas no código e reparo)
- Incremental

#### Release

- Versão específica para uso fora do desenvolvimento
- Propósito de convencer a eficácia do sistema ao cliente
- Realizado por uma equipe sem envolvimento com o desenvolvimento
- Verifica propriedades emergentes como desempenho e confiabilidade

#### Usuário

- Alfa
  - Usuários trabalham com a equipe de desenvolvimento para testar no local do desenvolvedor
- Beta
  - Uma versão do software é disponibilizada para os usuários usarem e levantarem os problemas descobertos com os devs
- Testes de aceitação
  - Clientes testam o sistema para decidir se está pronto para ser aceito e implantado no ambiente do cliente.
