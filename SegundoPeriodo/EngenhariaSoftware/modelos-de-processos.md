# Engenharia de software

## Modelos de processo de software

Exemplos mais comuns de processos de software
- [Modelo Cascata](#modelo-cascata)
- [Engenharia de software baseada em componentes](#engenharia-de-software-baseada-em-componentes)
- [Modelo Incremental](#modelo-incremental)
- [Modelo Evolucionário](#modelo-evolucionário)
- processo unificado


### Modelo cascata

Este modelo, conhecido também como a “abordagem clássica”, percorre as atividades (ou fases) fundamentais e distintas do desenvolvimento de um software, de uma forma bem linear. De início, deve-se planejar e programar  todas as atividades do processo antes de começar a trabalhar nelas. Atividades estas como: definição de requisitos, implementação, manutenção entre outras.

Na abordagem de Pressmann, o modelo cascata compreende os seguintes passos:

- Comunicação, o marco zero do projeto, onde são levantadas todas as necessidades;
- Planejamento, onde são elaboradas e delegadas as tarefas, cronogramas e acompanhamentos;
- Modelagem, que incluem tanto análise desses fatores e o projeto;
- Construção, onde o código é desenvolvido e são aplicados os testes;
- Emprego, quando é realizada a entrega, realizados os feedbacks e prestado suporte.

O modelo em V é considerado uma variação do modelo em cascata. Segundo o autor, à medida que a equipe de software avança, os requisitos básicos do problema são refinados, em representações progressivamente cada vez mais detalhadas e técnicas do problema e de sua solução ao passo de que, conforme o código é gerado, a equipe realiza uma série de testes que validem cada um dos modelos criados. Como Pressmann cita “na realidade, não existe nenhuma diferença fundamental entre o ciclo de vida clássico e o modelo V. Este modelo é uma forma de visualizar como a verificação e as ações de validação são aplicadas ao trabalho de engenharia anterior”.

Já na análise de Sommerville, o modelo em cascata é abordado com os seguintes passos:

- Definição de requisitos;
- Projeto de sistema e software;
- Implementação e teste unitário;
- Integração e teste de sistema;
- Operação e manutenção.

Segundo o autor, cada estágio é sujeito a uma aprovação e o estágio seguinte não deve ser iniciado até que a fase anterior seja concluída. Cada estágio dessa abordagem é  alimentado com informações dos outros estágios, de modo que problemas são identificados em fases distintas e analisados corretamente. O modelo não se restringe somente à linearidade, mas o feedback se torna essencial.

Ressaltando, o modelo cascata é preferencialmente usado quando todos os requisitos são bem compreendidos e dificilmente sofrerão alteração durante o seu desenvolvimento.

### Engenharia de software baseada em componentes

Similarmente chamado de componentização ou modularização, o conceito DRY (Don't Repeat Yourself) pode ser identificado e aplicado a praticamente todo software em desenvolvimento (ou já completado) onde há algum tipo de reúso. Esse reúso ocorre independentemente do processo de desenvolvimento que se use. A principal ideia é a adaptação das ferramentas (funções ou até mesmo classes inteiras) para reutilização em várias partes do projeto (e muitas vezes em até outros projetos). Como afirma Sommerville, "abordagens orientadas a reúso dependem de uma ampla base de componentes reusáveis de software e de um framework de integração para a composição desses".
Esses componentes muitas vezes podem ser sistemas completos, os **COTS** (Commercial Off-The-Shelf) ou conhecido como *Comercial de prateleira*, desenvolvidos por outras empresas ou grupos de empresas que os oferecem como produtos ou serviços, capazes de fornecer uma funcionalidade específica.

De qualquer modo, esse modelo de processo não difere tanto dos outros em vários aspectos: a equipe define requisitos, traça metas e etc. Quando o projeto ou a arquitetura do projeto é elaborada, é onde as coisas diferem. No lugar de planos extensos e detalhados, a equipe deve examinar os requisitos e determinar a construção. Perguntas do tipo "há componentes disponíveis ou frameworks elaborados para implementar os requisitos?" ou "os COTS obtidos são compatíveis dentro da arquitetura do software a ser construído?" irão direcionar o projeto o caminho correto.

A engenharia baseada em componentes pode ter duas perspectivas:
- Criação de novos componentes, passando por especificação, implementação e documentação;
- Desenvolvimento de sistemas completos utilizando um conjunto de componentes interligados.

Pode-se destacar cinco estágios nesse processo todo:
- **Seleção** de componentes, que consiste na identificação de componentes candidatos à reúso;
- **Qualificação**, analisando a compatibilidade do componente no sistema;
- **Adaptação**, visto que dificilmente um componente se adaptará por completa em um sistema;
- **Composição** que vai fazer a integração o componente no sistema e;
- **Atualização**, visto que com a evolução dos sistemas, versões antigas podem ficar obsoletas ou em desuso rapidamente.

### Modelo Incremental

Sendo uma das abordagens mais utilizadas, este modelo consiste na exposição de uma pequena versão funcional do projeto aos usuários e a realização de tarefas simultâneas ao passo em que o feedback é recebido, assim criando novas versões até que um software estável e adequado seja desenvolvido. Pode-se afirmar que o foco deste modelo é voltado para a entrega de um serviço ou produto ao cliente que já possua capacidade de atendê-lo, entregando a cada etapa ou nova versão mais recursos adicionais, até que se atinja o produto final.

O desenvolvimento incremental tem três vantagens importantes quando comparado ao modelo cascata, segundo Sommerville:

- Custo de acomodar as mudanças nos requisitos do cliente é reduzido;
- É mais fácil obter feedback dos clientes sobre o desenvolvimento que foi feito;
- É possível obter a entrega e implementação rápida de um software útil ao cliente, mesmo se toda funcionalidade não for incluída.

### Modelo Evolucionário

É esperado que softwares evoluam e sejam atualizados, assim como qualquer sistema complexo. Ao passo em que o projeto avança, novas especificações ou necessidades irão surgir e regras de negócio podem mudar tornando certas abstrações do projeto inúteis ou incompletas. 

Além disso, fatores externos influentes também interferem no projeto, alterando por exemplo, prazos e metas. Para atender situações dessa natureza, softwares com conjuntos de funcionalidades básicas são criados para atender especificações imediatas mas intencionalmente projetados para que evoluam ao longo do tempo.

Entre os processos evolucionários mais conhecidos, Pressman ressalta a **Prototipação** e o **Modelo Espiral**.

O *paradigma da prototipação* pode ser a melhor escolha quando são especificados muitos objetivos do projeto, porém pouco sobre os requisitos, recursos e funções de implementação, ou seja, como ele deverá ser desenvolvido. Sem esses detalhes, a primeira etapa pode ser vista justamente como a criação de um protótipo, que poderá evoluir ou ser descartado, de acordo com as necessidades e requerimentos.

No início do ciclo, temos a *comunicação*. Reuniões, feedbacks, que levem ao esboço das ideias, esquemas, levantamento de necessidades e afins, justamente para ter uma visão ampla do serviço ou produto e na modelagem do *projeto rápido*.

Este projeto leva na construção do protótipo e consiste na representação dos aspectos do software que serão visíveis ao usuário final. Servindo como primeiro sistema, ele atua como um mecanismo para identificar os requisitos do software. Porém é recomendado que, quando esse software tenha cumprido o seu papel, ele seja descartado, já que, como primeiro protótipo, ele foi feito para isso.

Como afirma Pressman, embora possam ocorrer problemas, este método pode ser efetivo para a engenharia de software. O segredo é definir as regras do jogo logo no início, ou seja, todos os envolvidos terão ciência de que o protótipo foi construído com o propósito de definir os requisitos e portanto, será descartado.

**imagem do paradigma**

Barry Boehm, criador do modelo espiral, o descreve da seguinte forma:

> O modelo espiral de desenvolvimento é um gerador de modelos de processos dirigidos a riscos e é utilizado para guiar a engenharia de sistemas intensivos de software, que ocorre de forma concorrente e tem múltiplos envolvidos.

Este modelo é considerado uma melhoria do **modelo incremental** e possui esse nome por conta da sua abstração, onde uma volta completa no espiral percorre todas as fases do processo do desenvolvimento do software. As repetições deverão ser realizadas quantas vezes sejam necessárias até que o sistema completo seja entregue.

Segundo Sommerville(2011), o modelo em espiral "combina prevenção e tolerância a mudanças, assume que mudanças são um resultado de riscos de projeto e inclui atividades explícitas de gerenciamento de riscos para sua redução".

PRESSMAN (2011) também diz que o modelo é "uma abordagem realista so desenvolvimento de sistemas e software de grande porte ... usando a prototipagem como mecanismo de redução de riscos".

A divisão dos setores do modelo espiral pode ser dada em quatro fases:
- Definição dos objetivos;
- Avaliação e redução dos riscos;
- Implementação e validação;
- Planejamento e especificação.

**imagem do modelo espiral**

Apesar de inúmeras vantagens desse método, vale a ressalva:
- Se um risco importante não for descoberto e gerenciado corretamente, fatalmente ocorrerão problemas;
- A avaliação de riscos exige um profissional experiente;
- Aplica-se melhor em sistemas de grande porte e;
- Segundo PRESSMAN (2011), pode ser difícil convencer os clientes que o processo de evolução é controlável, devido a exigência pela competência na avaliação dos riscos.

Referências Bibliográficas

PRESSMAN, Roger S. Engenharia de Software - Uma abordagem profissional, Sétima Edição. Editora MCGrawHill: Porto Alegre, 2011
SOMMERVILLE, Ian Engenharia de Software, Nona Edição. Editora Pearson Prentice Hall: São Paulo, 2011