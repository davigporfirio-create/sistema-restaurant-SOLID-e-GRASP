# Sistema de Restaurante - SOLID e GRASP

## Sobre o projeto

Este projeto foi desenvolvido para a AV1 da disciplina, com o objetivo de criar a estrutura de um sistema de restaurante utilizando conceitos de Programação Orientada a Objetos.

Durante a criação do diagrama buscamos aplicar os princípios **SOLID** e os padrões **GRASP**, principalmente para organizar melhor as responsabilidades das classes e diminuir a dependência entre elas.

## Funcionalidades

O sistema possui funcionalidades relacionadas ao funcionamento de um restaurante, como:

- Cadastro de funcionários e produtos;
- Controle de estoque;
- Gerenciamento de mesas;
- Criação de pedidos;
- Adição de produtos aos pedidos;
- Pagamentos em dinheiro, cartão ou PIX;
- Geração de relatórios.

## Diagrama de Classes

O diagrama abaixo representa as principais classes do sistema e seus relacionamentos.

![Diagrama de Classes](diagrama.png)

## SOLID

Alguns princípios SOLID utilizados no projeto foram:

**Responsabilidade Única (SRP):**  
As responsabilidades foram divididas entre diferentes classes. Por exemplo, `PedidoService` cuida das operações relacionadas aos pedidos, enquanto os repositórios ficam responsáveis pelo acesso aos dados.

**Aberto/Fechado (OCP):**  
Os métodos de pagamento utilizam a interface `IPagamento`. Dessa forma, é possível adicionar uma nova forma de pagamento sem precisar modificar toda a estrutura existente.

**Inversão de Dependência (DIP):**  
Os Services utilizam interfaces de repositório, como `IPedidoRepository`, em vez de depender diretamente das implementações.

## GRASP

Também utilizamos alguns conceitos GRASP na organização das classes.

**Information Expert:**  
Classes que possuem as informações necessárias também possuem comportamentos relacionados a essas informações. Por exemplo, `PedidoItem` possui o método `subtotal()`.

**Controller:**  
As classes Service, como `PedidoService`, `ProdutoService` e `MesaService`, controlam as principais operações do sistema.

**Low Coupling:**  
O uso das interfaces de repositório diminui a dependência entre as classes.

**High Cohesion:**  
Cada classe procura manter responsabilidades relacionadas a uma função específica do sistema.

**Polymorphism:**  
A interface `IPagamento` permite utilizar diferentes formas de pagamento, como PIX, cartão e dinheiro.

## Estrutura

O projeto foi dividido principalmente em:

- **Entidades:** representam os objetos do sistema, como Pedido, Produto, Mesa e Funcionário.
- **Services:** possuem as operações e regras do sistema.
- **Repositories:** responsáveis pelo acesso e armazenamento dos dados.
- **Pagamentos:** diferentes implementações para as formas de pagamento.

## Integrantes

- Gabriel Martins Feijó
- Davi Bezerra
- Davi Gomes
- Ian Alves

