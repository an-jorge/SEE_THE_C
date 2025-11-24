---
icon: '2'
---

# Conversão de Temperatura

{% hint style="warning" %}
## ⚡️ Exercício 2: Conversão de Temperatura de Celsius para Fahrenheit&#x20;



**Objectivo**: Neste exercício, você praticará a conversão de temperaturas de Celsius para Fahrenheit, além de trabalhar com o conceito de internacionalização de programas usando a função `setlocale` para configurar a localidade em Português.
{% endhint %}



***

### **Instruções:**

1. **Entendimento do código:**
   * O programa define uma variável `celsius` com o valor 20.
   * A conversão para Fahrenheit é feita usando a fórmula: Fahrenheit=(Celsius×59​)+32
   * NOTA: (2&#x30;**°C** × 9/5) + 32 = 6&#x38;**°F**
   * O valor da temperatura em Celsius e o resultado da conversão em Fahrenheit são exibidos.
   * O código também tenta configurar a localidade para o português utilizando `setlocale(LC_ALL, "Portuguese")` para suportar caracteres específicos e formatação de acordo com o idioma.

### **Tarefa:**

1. Copie o código e execute-o no seu compilador C.
2. Observe a saída com as temperaturas exibidas tanto em Celsius quanto em Fahrenheit.
3. Certifique-se de que a configuração da localidade funcione correctamente. Se a localidade `portuguese` não estiver disponível no sistema, o código exibe uma mensagem de erro.
4. **Perguntas para reflexão:**
   * A fórmula de conversão para Fahrenheit está correta? Se sim, por que a multiplicação por 9/5 é necessária?
   * O que acontece se você alterar o valor da variável `celsius` para outro número? O cálculo se ajusta correctamente?
   * A função `setlocale` funcionou como esperado no seu ambiente de desenvolvimento? Se não, que passos adicionais podem ser necessários para configurar a localidade no seu sistema?



***



### **Desafio extra:**

1. Modifique o programa para permitir que o usuário insira uma temperatura em Celsius através da função `scanf` e exiba a conversão correspondente para Fahrenheit.
2. Adicione uma função para converter Fahrenheit de volta para Celsius.
3. Teste o programa com diferentes valores de temperatura para garantir que as conversões estão corretas.



***

<a href="../../capitulo-1-re/conversao-de-temperatura.md" class="button secondary">RE2</a>
