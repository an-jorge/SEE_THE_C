# Estruturas condicionais

{% hint style="info" %}
#### **Saiba mais** <a href="#saiba-mais" id="saiba-mais"></a>

**No final desta lição, você será capaz de responder ao seguinte**:\
O que são "Estruturas Condicionais"

* `if`, `else`

O que são "Instruções Condicionais"
{% endhint %}



## Introdução às Instruções if e else

***

Na programação as instruções `if` e `else` são usadas para controlar o fluxo do programa com base em condições. Assim como na vida, as condições permitem que você execute diferentes blocos de código dependendo se uma condição é verdadeira ou falsa.

### **Sintaxe do `if else`**

{% code overflow="wrap" %}
```c
if (condição) {
  // bloco de código a ser executado se a condição for verdadeira
} else {
  // bloco de código a ser executado se a condição for falsa (opcional)
}
```
{% endcode %}



{% code title="main.c" overflow="wrap" %}
```c
#include <stdio.h>

int main() {
    int number = 10;

    if (number > 0) {
        printf("O número é positivo.\n");
    } else {
        printf("O número é negativo ou zero.\n");
    }

    return 0;
}
```
{% endcode %}

{% code title="TERMINAL" overflow="wrap" %}
```
>. O número é positivo.
```
{% endcode %}

***

## Instrução `else-if`&#x20;

A instrução `else if` é usada quando você precisa verificar **múltiplas condições** em um programa. Ela é uma extensão da estrutura `if-else` e permite adicionar várias condições intermediárias antes de chegar ao bloco `else`.



{% hint style="info" %}
## Saiba mais

`condição`: Uma expressão booleana que deve ser avaliada como verdadeira (não zero) ou falsa para determinar qual bloco de código será executado.



`bloco de código`: Um conjunto de instruções que serão executadas se a condição for verdadeira (bloco `if`) ou falsa (bloco `else`).
{% endhint %}

{% hint style="info" %}
O programa verifica as condições na ordem em que aparecem.

Assim que uma condição for verdadeira 1, o bloco correspondente será executado e o restante será ignorado. O bloco `else` é opcional e será executado apenas se **nenhuma das condições anteriores for verdadeira**.


{% endhint %}

### **Aqui está um exemplo prático**:

{% code title="main.c" overflow="wrap" %}
```c
#include <stdio.h>

int main()
{
    const int score = 10;

        printf("Sua pontuação %d \n", score);

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

{% code title="TERMINAL" overflow="wrap" %}
```
>. 
Sua pontuação 10 
Você foi reprovado.
```
{% endcode %}



A instrução `else if` é uma ferramenta poderosa para lidar com múltiplas condições em um programa. Ela permite que você crie fluxos de decisão mais complexos e dinâmicos, tornando seu código mais flexível e funcional.



***



