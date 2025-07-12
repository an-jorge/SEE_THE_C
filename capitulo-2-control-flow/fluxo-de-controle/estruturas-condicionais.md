# Estruturas condicionais

{% hint style="info" %}
#### **Saiba mais** <a href="#saiba-mais" id="saiba-mais"></a>

**No final desta lição, você será capaz de responder ao seguinte**:\
O que são "Estruturas Condicionais"

* `if`, `else`, `switch`

O que são "Instruções Condicionais"
{% endhint %}

## Introdução às Instruções if e else

***

Na programação as instruções `if` e `else` são usadas para controlar o fluxo do programa com base em condições. Assim como na vida, as condições permitem que você execute diferentes blocos de código dependendo se uma condição é verdadeira ou falsa.

#### **Sintaxe do `if else`**

{% code overflow="wrap" %}
```c
if (condição) {
  // bloco de código a ser executado se a condição for verdadeira
} else {
  // bloco de código a ser executado se a condição for falsa (opcional)
}
```
{% endcode %}

{% hint style="info" %}
### Saiba mais

`condição`: Uma expressão booleana que deve ser avaliada como verdadeira (não zero) ou falsa para determinar qual bloco de código será executado.

`bloco de código`: Um conjunto de instruções que serão executadas se a condição for verdadeira (bloco `if`) ou falsa (bloco `else`).
{% endhint %}



{% code overflow="wrap" %}
```c
#include <stdio.h>

int main() {
    int numero = 10;

    if (numero > 0) {
        printf("O número é positivo.\n");
    } else {
        printf("O número é negativo ou zero.\n");
    }

    return 0;
}
```
{% endcode %}



***

## Introdução à Instrução `else-if`&#x20;

A instrução `else if` é usada quando você precisa verificar **múltiplas condições** em um programa. Ela é uma extensão da estrutura `if-else` e permite adicionar várias condições intermediárias antes de chegar ao bloco `else`.



{% hint style="info" %}
## Saiba mais

O programa verifica as condições na ordem em que aparecem.

Assim que uma condição for verdadeira 1, o bloco correspondente será executado e o restante será ignorado. O bloco `else` é opcional e será executado apenas se **nenhuma das condições anteriores for verdadeira**.


{% endhint %}



**Aqui está um exemplo prático**:

{% code overflow="wrap" %}
```c
#include <stdio.h>

int main()
{
    int score = 10;

    printf("Sua pontuacao %d", score);

    if (score >= 90)
    {
        printf("Você tirou A.\n");
    }
    else if (score >= 80)
    {
        printf("Você tirou B.\n");
    }
    else if (score >= 70)
    {
        printf("Você tirou C.\n");
    }
    else if (score >= 60)
    {
        printf("Você tirou D.\n");
    }
    else
    {
        printf("Você foi reprovado.\n");
    }

    return 0;
}
```
{% endcode %}



A instrução `else if` é uma ferramenta poderosa para lidar com múltiplas condições em um programa. Ela permite que você crie fluxos de decisão mais complexos e dinâmicos, tornando seu código mais flexível e funcional.



***

## Instrução `switch`

`switch` é usada para realizar uma seleção entre várias alternativas com base no valor de uma expressão. É uma forma mais organizada e eficiente de lidar com múltiplas opções do que uma série de instruções `if` e `else if`.&#x20;

**A estrutura básica do** `switch` **é a seguinte:**

{% code overflow="wrap" %}
```c

#include <stdio.h>

int main()
{
    int option = 1;

    printf("Escolha uma opção:\n");
    printf("1 - Iniciar\n");
    printf("2 - Configurações\n");
    printf("3 - Sair\n");

    switch (option)
    {
    case 1:
        printf("Iniciando...\n");
        break;
    case 2:
        printf("Abrindo configurações...\n");
        break;
    case 3:
        printf("Saindo...\n");
        break;
    default:
        printf("Opção inválida!\n");
    }

    return 0;
}

```
{% endcode %}



{% hint style="danger" %}
## **Atenção:**

### <mark style="color:red;">Evitar "Fall-Through" Indesejado</mark>

`break` impede que os próximos `case` sejam executados.

Se esquecermos o `break`, os `case` seguintes serão executados **mesmo sem correspondência**, causando o que é chamado de efeito chamado **"fall-through"**.



***



{% code overflow="wrap" %}
```c
#include <stdio.h>

int main()
{
    int num = 2;

    switch (num)
    {
    case 1:
        printf("Caso 1\n");
    case 2:
        printf("Caso 2\n");
    case 3:
        printf("Caso 3\n");
    default:
        printf("Padrão\n");
    }

    return 0;
}

```
{% endcode %}

* `break` impede que os próximos `case` sejam executados.


{% endhint %}

{% code title="TERMINAL" overflow="wrap" %}
```

 Caso 2  
 Caso 3
 Padrão   
```
{% endcode %}

### Instrução `continue` e `break`

***



`continue` e `break` são utilizados para alterar o fluxo de execução dentro de laços de repetição (`for`, `while`, `do-while`) e também no comando `switch-case` em C.

* `break`**:**
  * Interrompe imediatamente o loop de repetição em que está inserido.
  * O programa continua a execução a partir da instrução seguinte ao loop.
* `continue`**:**
  * Interrompe a iteração actual do loop de repetição em que está inserido.
  * O programa pula para a avaliação da condição do loop e, se verdadeira, executa a próxima iteração.

**Exemplo demonstrando o uso de** `break` **e** `continue`**:**

{% code overflow="wrap" %}
```c
#include <stdio.h>

int main() {

  for (int i = 1; i <= 10; i++) {
    if (i == 5) {
      break; // Sai do loop quando i for igual a 5
    }
    if (i % 2 == 0) {
      continue; // Pula para a próxima iteração se i for par
    }
    printf(" repetição ímpar número %d\n", i);
  }

  return 0;
}
```
{% endcode %}



### Quando usar `switch` ao invez de `if-else`?

**Use** `switch` **quando**:

* Há muitas comparações com **valores fixos**.
* Você trabalha com **números inteiros ou caracteres**.

**Prefira** `if-else` **quando**:

* As comparações **envolvem intervalos** (`>`, `<`, `>=`, `<=`).
* A condição envolve **números de ponto flutuante** (`float`**,** `double`).
* O `switch` ficaria grande e difícil de ler.

{% hint style="info" %}
## Saiba mais:

### <mark style="color:green;">Quando o "Fall-Through" é Útil?</mark>



Embora muitas vezes indesejado, o "fall-through" pode ser útil em alguns casos, como **casos agrupados**:

***



<pre class="language-c" data-overflow="wrap"><code class="lang-c">#include &#x3C;stdio.h>

int main() { char letra = 'a';

<strong>switch (letra) {
</strong>    case 'a':  
    case 'e':  
    case 'i':  
    case 'o':  
    case 'u':
        printf("É uma vogal!\n");
        break;
    default:
        printf("É uma consoante!\n");
}

return 0;
</code></pre>

}
{% endhint %}





