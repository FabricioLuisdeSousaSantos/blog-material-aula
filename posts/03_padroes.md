---
icon: edit
date: 2023-03-30
tag:
  - padroes
category:
  - aula
order: 3
---

# Padrões de Projetos 🚧

## Introdução

Os padrões de projeto são soluções comuns para problemas recorrentes no desenvolvimento de software. Eles são como plantas pré-fabricadas que podem ser personalizadas para resolver problemas específicos de projeto de código. No entanto, um padrão não é um pedaço específico de código, mas sim um conceito geral para resolver um problema específico. É importante ressaltar que os padrões não podem ser simplesmente copiados e colados em um programa, mas sim adaptados às necessidades de cada projeto.

## História

A ideia de padrões foi apresentada por Christopher Alexander em 1977 no contexto de Arquitetura (de prédios e cidades):

- Problemas semelhantes com soluções diferentes
- Reinventando a Roda


## Conceito

Também conhecidos como *Padrões de Desenho de Software OO* ou simplesmente como *Padrões.*

::: tip Definição
Cada padrão descreve um problema que ocorre repetidas vezes em nosso ambiente, e então descreve o núcleo da solução para aquele problema, de tal maneira que pode-se usar essa solução milhões de vezes sem nunca fazê-la da mesma forma duas vezes [^Alexander]
:::


::: tip Definição
Os padrões de projeto são descrições de objetos que se comunicam e classes que são customizadas para resolver um problema genérico de design em um contexto específico [^GAMMA]
:::


### Outras definições

- Maneira testada ou documentada de alcançar um objetivo qualquer.
  - Padrões são comuns em várias áreas da engenharia
- Design Patterns, ou Padrões de Projeto
  - Padrões para alcançar objetivos na engenharia de software usando classes e métodos em linguagens orientadas a objeto
  - Inspirado em "A Pattern Language" de Christopher Alexander, sobre padrões de arquitetura de cidades, casas e prédios
  - "Design Patterns" de Erich Gamma, John Vlissides, Ralph Jonhson e Richard Helm, conhecidos como "The Gang of 	Four", ou GoF, descreve 23 padrões de projeto úteis

## Vantagens

Os padrões de projeto são uma coleção de ferramentas que oferecem soluções testadas e aprovadas para problemas recorrentes no desenvolvimento de software. Mesmo que você nunca tenha se deparado com esses problemas antes, o conhecimento dos padrões é extremamente valioso, pois eles ensinam como resolver vários problemas usando princípios de projeto orientado a objetos

- Aprender com a experiência dos outros
  - Identificar problemas comuns em engenharia de software e utilizar soluções testadas e bem documentadas
  - Utilizar soluções que têm um nome: facilita a comunicação, compreensão e documentação
- Aprender a programar bem com orientação a objetos
  - Os 23 padrões de projeto "clássicos" utilizam as melhores práticas em OO para atingir os resultados desejados
- Desenvolver software de melhor qualidade
  - Os padrões utilizam eficientemente polimorfismo, herança, modularidade, composição, abstração para construir código reutilizável, eficiente, de alta coesão e baixo acoplamento
- Vocabulário comum
  - Faz o sistema ficar menos complexo ao permitir que se fale em um nível mais alto de abstração
- Ajuda na documentação e na aprendizagem
  - Conhecendo os padrões de projeto torna mais fácil a compreensão de sistemas existentes
  - "As pessoas que estão aprendendo POO freqüentemente reclamam que os sistemas com os quais trabalham usam herança de forma convoluida e que é difícil de seguir o fluxo de controle. Geralmente a causa disto é que eles não entendem os padrões do sistema" [GoF]
  - Aprender os padrões ajudam um novato a agir mais como um especialista
- Uma prática adjunta aos métodos existentes
  - Mostram como usar práticas primitivas
  - Descrevem mais o porquê do design
  - Ajudam a converter um modelo de análise em um modelo de implementação
- Um alvo para refatoramento
  - Captura as principais estruturas que resultam do refatoramento
  - Uso de patterns desde o início pode diminuir a necessidade de refatoramento			

## Elementos de um padrão

- Nome
- Problema
  - Quando aplicar o padrão, em que condições?
- Solução
  - Descrição abstrata de um problema e como usar os elementos disponíveis (classes e objetos) para solucioná-lo
- Consequências
  - Custos e benefícios de se aplicar o padrão
  - Impacto na flexibilidade, extensibilidade, portabilidade e eficiência do sistema

<table>
<caption>Tabela de padrões do Gof </caption>
<thead>
  <tr>
    <th colspan="2"></th>
    <th colspan="3">Propósito</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td colspan="2"></td>
    <td>De criação</td>
    <td>Estrutural</td>
    <td>Comportamental</td>
  </tr>
  <tr>
    <td rowspan="2">Escopo</td>
    <td>Classe</td>
    <td>
      <ul>
        <li>Factory Method</li>
      </ul>
    </td>
    <td>
        <ul>
            <li>Adapter(class)</li>
        </ul>
    </td>
    <td>
      <ul>
        <li>Interperter</li>
        <li>Template Method</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>Objeto</td>
    <td>
        <ul>
            <li>Abstract Factory</li>
            <li>Builder</li>
            <li>Prototype</li>
            <li>Singleton</li>
        </ul>
    </td>
    <td>
        <ul>
            <li>Adapter (object)</li>
            <li>Bridge</li>
            <li>Composite</li>
            <li>Decorator</li>
            <li>Facade</li>
            <li>Flyweight</li>
            <li>Proxy</li>
        </ul>
    </td>
    <td>
        <ul>
            <li>Chain of Responsibility</li>
            <li>Command</li>
            <li>Interator</li>
            <li>Mediator</li>
            <li>Memento</li>
            <li>Observer</li>
            <li>State</li>
            <li>Strategy</li>
            <li>Visitor</li>
        </ul>
    </td>
  </tr>
</tbody>
</table>

<figure>

```plantuml

@startuml
'skinparam linetype polyline

class "Factory Method" as FactoryMethod
class Interperter
class "Template Method" as TemplateMethod
class "Abstract Factory" as AbstractFactory
class Builder
class Prototype
class Singleton
class Adapter
class Bridge
class Composite
class Decorator
class Facade
class Flyweight
class Proxy
class "Chain of Responsibility" as ChainofResponsibility
class Command
class Iterator
class Mediator
class Memento
class Observer
class State
class Strategy
class Visitor

ChainofResponsibility ---> Composite : Definindo \na cadeia
Command ---> Composite : Usando \ncomposto
Command ---> Memento : Evitando \nhisterese
Iterator ---> Memento : Salvando o \nestado da iteração
Composite ---> Iterator : Enumerando \nfilhos
Visitor ---> Iterator : Definindo\percussos
Composite ---> Visitor : Adicionando\nOperações
Interperter ---> Visitor : Adicionando\nOperações
Interperter ---> Composite : Definindo\na gramática
Interperter ---> Flyweight : Compartilhando\nsímbolos terminais
Composite ---> Flyweight : Compartilhando\ncompostos
Flyweight <--- State : Compartilhando\nestados
Strategy ---> Flyweight : Compartilhando\nestrategias
TemplateMethod ---> Strategy : Definindo os\npasso do\nalgoritmo
Decorator ---> Strategy : Mudando o \nexterior x\ninterior
Strategy ---> Decorator : Mudando o \nexterior x\ninterior
Composite ---> Decorator : Acrescentando\nresponsabilidade\na objetos
Composite ---> Builder : Criando\ncompostos
FactoryMethod <--- TemplateMethod  : usos frequentes
FactoryMethod <--- AbstractFactory  : implementa usando
Prototype <--- AbstractFactory : Configurar\na fabrica\ndinamicamente
Singleton <--- AbstractFactory : instância\núnica
Facade ---> Singleton : instância\núnica
Observer --> Mediator : administração\nde dependências\ncomplexas


Decorator -[hidden]-> Observer


Adapter -[hidden]-> Bridge
Bridge -[hidden]-> Proxy
Adapter -[hidden]> AbstractFactory


hide empty attributes
hide empty methods
hide circle

@enduml
```

<figcaption>Relação entre os padrões do Gof.</figcaption>
</figure>


## Referências

@include(../bib/bib.md)


