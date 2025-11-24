---
icon: '1'
---

# Cálculo de Média Aritmética

{% hint style="warning" %}
## ⚡️ Exercício 1: **Cálculo de Média Aritmética**



**Objectivo:** Neste exercício, você praticará como calcular e exibir uma média aritmética simples em C, além de identificar possíveis erros no cálculo de expressões matemáticas envolvendo variáveis inteiras.
{% endhint %}



***

### **Instruções:**

1. **Entendimento do código:**
   * O código define três variáveis inteiras: `first_value`, `second_value` e `third_value`, que representam três notas de um aluno.
   * O valor da variável `sum_of_values` armazena a soma das três notas, e o programa exibe essas notas em sequência.
   * O código tenta calcular a média das notas e exibe o resultado.
2. **Tarefa:**
   1. Execute o código em seu compilador C.
   2. Observe o valor da média exibida. O cálculo parece correto?
3. **Perguntas para reflexão:**
   * O cálculo da média está correto? Se não, por que o resultado da média não é o esperado?
   * Como o operador de divisão (`/`) está sendo aplicado no código e o que deveria ser corrigido?
   * Como você pode garantir que a divisão é realizada de forma adequada para calcular a média correta?
4. **Correcção do código:**
   * A expressão para o cálculo da média está incorrecta. A divisão de `third_value` por 3 ocorre antes da soma dos valores, devido à ordem de precedência dos operadores em C.

***



### **Desafio extra:**

1. Modifique o programa para que o usuário possa inserir as três notas em tempo de execução, usando a função `scanf`.
2. Modifique o código para exibir a média com uma casa decimal, utilizando variáveis do tipo `float` para melhorar a precisão do cálculo da média.

***

<a href="../../capitulo-1-re/calculo-de-media-aritmetica.md" class="button primary">RE1</a>
