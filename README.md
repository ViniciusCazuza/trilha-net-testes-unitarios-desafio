# Projeto - Testes Unitários com C#

Este projeto foi desenvolvido como parte do módulo **"Testes Unitários com C#"** da trilha .NET da DIO. O objetivo principal foi implementar testes unitários para as classes e métodos fornecidos, garantindo maior cobertura de código e segurança no desenvolvimento do software.

## Desafio

Os gestores relataram frequentes problemas no sistema em produção, como bugs e falhas em funcionalidades que antes funcionavam corretamente. Por isso, foi sugerida a implementação de testes unitários para garantir a qualidade do código, prevenir regressões e melhorar a confiabilidade do sistema.

## Objetivo

O objetivo deste projeto foi criar testes unitários utilizando o framework **xUnit** para cobrir as classes e métodos de validação que já existiam no sistema. Os testes foram construídos para validar cenários positivos e negativos, cobrindo as funcionalidades mais críticas.

## Tecnologias Utilizadas

- **C#**
- **.NET 6.0**
- **xUnit** para testes unitários
- **Visual Studio** ou qualquer IDE com suporte a .NET

## Estrutura do Projeto

O projeto está dividido em dois:

1. **Projeto Console**: Contém as classes principais com a lógica de validação.
2. **Projeto de Testes**: Contém as classes de testes unitários para validar o comportamento das classes e métodos do projeto console.

### Classes do Projeto Console

#### 1. `ValidacoesLista`

Esta classe contém métodos para validar listas de números inteiros.

- **RemoverNumerosNegativos**: Remove números negativos de uma lista.
- **ListaContemDeterminadoNumero**: Verifica se um determinado número está presente em uma lista.
- **MultiplicarNumerosLista**: Multiplica todos os elementos de uma lista por um determinado número.
- **RetornarMaiorNumeroLista**: Retorna o maior número de uma lista.
- **RetornarMenorNumeroLista**: Retorna o menor número de uma lista.

#### 2. `ValidacoesString`

Esta classe contém métodos para validar e manipular strings.

- **RetornarQuantidadeCaracteres**: Retorna a quantidade de caracteres em uma string.
- **ContemCaractere**: Verifica se uma string contém um determinado caractere ou trecho.
- **TextoTerminaCom**: Verifica se uma string termina com um determinado trecho.

### Classes do Projeto de Testes

#### 1. `ValidacoesListaTests`

Esta classe contém os testes unitários para os métodos da classe `ValidacoesLista`.

- **DeveRemoverNumerosNegativosDeUmaLista**: Testa se os números negativos são removidos corretamente de uma lista.
- **DeveConterONumero9NaLista**: Verifica se o número 9 está presente na lista.
- **NaoDeveConterONumero10NaLista**: Verifica se o número 10 não está presente na lista.
- **DeveMultiplicarOsElementosDaListaPor2**: Testa se os números da lista são corretamente multiplicados por 2.
- **DeveRetornar9ComoMaiorNumeroDaLista**: Verifica se o maior número da lista é 9.
- **DeveRetornarOitoNegativoComoMenorNumeroDaLista**: Verifica se o menor número da lista é -8.

#### 2. `ValidacoesStringTests`

Esta classe contém os testes unitários para os métodos da classe `ValidacoesString`.

- **DeveRetornar6QuantidadeCaracteresDaPalavraMatrix**: Verifica se a quantidade de caracteres da palavra "Matrix" é 6.
- **DeveContemAPalavraQualquerNoTexto**: Testa se a palavra "qualquer" está presente no texto.
- **NaoDeveConterAPalavraTesteNoTexto**: Verifica se a palavra "teste" não está presente no texto.
- **TextoDeveTerminarComAPalavraProcurado**: Verifica se o texto termina com a palavra "procurado".

## Como Utilizar

1. **Clone o projeto** ou abra diretamente em sua IDE de preferência.
2. **Compile o projeto** e execute os testes unitários para validar as implementações.
3. Para rodar os testes unitários:
    - No Visual Studio, use o Test Explorer para rodar todos os testes.
    - Em outras IDEs, use o terminal para executar `dotnet test` na raiz do projeto.

## Testes

Os testes cobrem cenários críticos, incluindo:

- Remoção de números negativos de uma lista.
- Verificação de números específicos em listas.
- Operações de multiplicação sobre listas.
- Verificação de caracteres e trechos de strings.
- Comparações de maior e menor valor em listas.

## Conclusão

Com a implementação dos testes unitários, foi possível garantir maior confiabilidade e segurança no código, prevenindo a ocorrência de bugs e comportamentos indesejados. A cobertura de testes permite detectar rapidamente qualquer regressão no código, melhorando a qualidade do sistema como um todo.


##

# DIO - Trilha .NET - Testes Unitários com C#
www.dio.me

## Desafio de projeto
Para este desafio, você precisará usar seus conhecimentos adquiridos no módulo de Testes Unitários com C#, da trilha .NET da DIO.

## Contexto
Você está trabalhando em um sistema, e seus gestores relataram que frequentemente há problemas no software: bugs, funcionalidades que estavam funcionando de repente não funcionam mais, problemas de validações, entre outros. Os clientes já começam a duvidar da qualidade do código.

Feito isso, você sugeriu a implementação de testes unitários: escrever testes cobrindo as partes mais críticas do sistema, com cenários positivos e negativos, a fim de ter uma rastreabilidade e controle do código, melhorando assim a qualidade desse sistema.

Os gestores aceitaram a sua ideia, e com isso, você precisa implementar testes unitários no sistema.

## Premissas
O sistema hoje possui dois projetos: um do tipo console, e um do tipo testes com **xUnit**. O projeto do tipo console possui duas classes em que são realizadas as lógicas principais: **ValidacoesLista** e **ValidacoesString**. Essas classes contém métodos em comum que são usados para realizar diversas validações em determinados cenários.

O projeto de testes possui as classes de teste **ValidacoesListaTests** e **ValidacoesStringTests**, assim como seus métodos para validar o projeto do tipo console, porém estão incompletos. 

O seu objetivo é implementar os métodos de testes contidos no projeto.

## Projeto Console, suas classes e métodos

Essas são as classes do projeto console, onde fica a principal lógica do sistema.

**Classe ValidaçõesLista**

Classe responsável por realizar diversas validações envolvendo listas.

| Classe          | Método                       | Objetivo                                                                                                                |
|---------------- |------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ValidacoesLista | RemoverNumerosNegativos      | Recebe uma lista de números inteiros e retorna uma nova lista, apenas com os números positivos                          |
| ValidacoesLista | ListaContemDeterminadoNumero | Recebe uma lista de números inteiros e verifica se um determinado número está presente dentro dessa lista               |
| ValidacoesLista | MultiplicarNumerosLista      | Recebe uma lista de números inteiros e retorna uma nova lista, com seus valores múltiplicados por um determinado número |
| ValidacoesLista | RetornarMaiorNumeroLista     | Recebe uma lista de números inteiros e retorna o maior número entre eles                                                |
| ValidacoesLista | RetornarMenorNumeroLista     | Recebe uma lista de números inteiros e retorna o menor número entre eles                                                |

**Classe ValidacoesString**

Classe responsável por realizar diversas validações envolvendo strings.

| Classe           | Método                       | Objetivo                                                                                                                
|------------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ValidacoesString | RetornarQuantidadeCaracteres | Recebe um texto qualquer e retorna a quantidade de caracteres presentes no texto                                                                           |
| ValidacoesString | ContemCaractere              | Recebe um texto qualquer e um texto a ser procurado, retorna verdadeiro ou falso se um determinado trecho procurado está presente no texto                 |
| ValidacoesString | TextoTerminaCom              | Recebe um texto qualquer e um trecho a ser procurado, retorna verdadeiro ou falso se um determinado trecho procurado está presente no final do texto apenas |

## Projeto do tipo teste, suas classes e métodos

**Classe ValidacoesListaTests**

Classe responsável por realizar os testes da classe ValidacoesLista.

| Classe               | Método de teste                               | Resultado esperado do teste
|----------------------|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ValidacoesListaTests | DeveRemoverNumerosNegativosDeUmaLista         | Ao passar uma lista com diversos números, incluindo positivos e negativos, deve ser retornado uma nova lista apenas com números positivos  |
| ValidacoesListaTests | DeveConterONumero9NaLista                     | Ao passar uma lista com diversos números, incluindo o número 9, deve retornar verdadeiro, pois encontrou o 9 na lista                      |
| ValidacoesListaTests | NaoDeveConterONumero10NaLista                 | Ao passar uma lista com diversos números, mas sem o número 10, deve retornar falso, pois não encontrou o 10 na lista                       |
| ValidacoesListaTests | DeveMultiplicarOsElementosDaListaPor2         | Ao passar uma lista de inteiros, deve retornar uma nova lista, com todos os elementos da lista multiplicados por 2                         |
| ValidacoesListaTests | DeveRetornar9ComoMaiorNumeroDaLista           | Ao passar uma lista de números inteiros, sendo o maior deles 9, deve retornar o 9 como maior elemento dentro dessa lista                   |
| ValidacoesListaTests | DeveRetornarOitoNegativoComoMenorNumeroDaList | Ao passar uma lista de números inteiros, sendo o menor deles -8, deve retornar o -8 como menor elemento dentro dessa lista                 |

**Classe ValidacoesStringTests**

Classe responsável por realizar os testes da classe ValidacoesString.

| Classe                | Método de teste                                  | Resultado esperado do teste
|---------------------- |--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ValidacoesStringTests | DeveRetornar6QuantidadeCaracteresDaPalavraMatrix | Ao passar um texto escrito a palavra "Matrix", deve retornar o número 6, representando 6 caracteres presentes na palavra                                                                         |
| ValidacoesStringTests | DeveContemAPalavraQualquerNoTexto                | Ao passar um texto escrito "Esse é um texto qualquer" e procurar pela palavra "qualquer", deve retornar verdadeiro pois a palavra existe no texto                                                |
| ValidacoesStringTests | NaoDeveConterAPalavraTesteNoTexto                | Ao passar um texto escrito "Esse é um texto qualquer" e procurar pela palavra "teste", deve retornar falso pois a palavra não existe no texto                                                    |
| ValidacoesStringTests | TextoDeveTerminarComAPalavraProcurado            | Ao passar um texto escrito "Começo, meio e fim do texto procurado" e procurar pela palavra "procurado", deve retornar verdadeiro pois a palavra existe no texto e está inclusa no final do texto |

## Estrutura do projeto

O projeto está estruturado da seguinte maneira:

![Métodos Swagger](Imagens/projeto.png)


## Solução
O código de testes está pela metade, e você deverá dar continuidade implementando os testes descritos acima, para que no final, tenhamos um programa de testes funcional. Procure pela palavra comentada "TODO" no código, em seguida, implemente conforme as regras acima.
