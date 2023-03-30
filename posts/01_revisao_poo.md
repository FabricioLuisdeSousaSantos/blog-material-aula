---
icon: edit
date: 2023-03-30 20:10:00.00 -3
tag:
  - java
  - objeto
category:
  - aula
order: 1
---
# Revisão POO

## Objeto

- Um objeto é cada uma das entidades identificáveis num dado domínio de aplicação
- Em um sistema Bancário teríamos objetos do tipo: Cliente, Conta, Conta Corrente, Dependente, etc.
- Um objeto também pode ser visto como um agregado de outros objetos (suas partes)

<figure>

```plantuml
@startuml
rectangle "Apartamento"{
    rectangle "Sala" as s
    rectangle "Quarto" as q
    rectangle "Cozinha" as c
    rectangle "Banheiro" as b
s -[hidden]> q
q -[hidden]> c
c -[hidden]> b
}
@enduml  
```

<figcaption> Um objeto como um conjuto de outros objetos.</figcaption>
</figure>


- Um Objeto é uma entidade independente que armazena dados, encapsula serviços, troca mensagens com outros objetos e é modelado para executar as funções do sistema
- Um Objeto pode ser descrito pela identificação de dois elementos básicos: estrutura e comportamento

::: tip Exemplo 
Objeto do tipo **Pessoa**
- **Estrutura** : nome, cpf, idade
- **Comportamento** : trabalhar, descansar
:::

::: tip Exemplo
Objeto do tipo **Conta**
- **Estrutura:** titular, código, saldo
- **Comportamento:** debitarValor, adicionarValor
:::

### Mensagens

- São estímulos enviados aos objetos solicitando que alguma operação seja realizada por um dado objeto
  - Nome da mensagem
  - Parâmetros
- Especifica O QUE deve ser feito
- O comportamento de um objeto é dado pelo conjunto de mensagens que ele pode responder
  
### Características dos Objetos
- Único
- Possui atributos que definem caraterísticas e/ou estado 
- Possuem capacidade de realizar ações que chamamos de métodos ou funções
- Normalmente se diz que um objeto é uma instância de uma Classe.
- O que é uma Classe ?




