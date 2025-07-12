# Fluxo de Controle

Estruturas condicionais na programação são construções que permitem executar diferentes blocos de código com base em condições específicas. Elas avaliam se uma expressão lógica é verdadeira ou falsa e, isso dependendo do resultado, direcionam o fluxo do programa para executar certas instruções.

## **Decisão (condicionais)**

1. Permite **tomar decisões** com base em condições:

* `if`, `else`, `else if`
* `switch`

## **Repetição (laços/loops)**

2. Executa **blocos de código repetidamente**:

* `for`
* `while`
* `do...while`

## **Desvios e saltos**

3. Alteram o fluxo bruscamente (geralmente com cautela):

* `break` – sai de um loop ou `switch`
* `continue` – pula o restante do loop atual
* `return` – sai de uma função
* [`goto`](#user-content-fn-1)[^1] – salto direto (geralmente desaconselhado)

#### Características:

* **Expressões lógicas**: As condições são geralmente expressões que retornam um valor booleano (true ou false), como comparações (==, !=, >, <, etc.).
* **Aninhamento**: Estruturas condicionais podem ser aninhadas, ou seja, um if dentro de outro if.
* **Uso comum**: São usadas para tomar decisões no programa, como validar entradas, controlar fluxos ou executar ações específicas com base em estados.



[^1]: O **`goto`** faz um **salto incondicional** para um **rótulo** dentro da **mesma função**. Ele não sai da função, apenas pula de um ponto para outro no código.
