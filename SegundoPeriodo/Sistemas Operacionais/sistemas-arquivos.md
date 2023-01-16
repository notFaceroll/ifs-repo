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

