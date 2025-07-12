# Operadores relacionais e lógicos

Os operadores de relacionais são usados para comparar valores e produzir um resultado booleano (verdadeiro ou falso) com base na comparação. Aqui estão os operadores de comparação mais comuns em C:

1. **Igual a:** `==`
   * Verifica se dois valores são iguais.
2. **Diferente de:** `!=`
   * Verifica se dois valores são diferentes.
3. **Maior que:** `>`
   * Verifica se o valor à esquerda é maior que o valor à direita.
4. **Maior ou igual a:** `>=`
   * Verifica se o valor à esquerda é maior ou igual ao valor à direita.
5. **Menor que:** `<`
   * Verifica se o valor à esquerda é menor que o valor à direita.
6. **Menor ou igual a:** `<=`
   * Verifica se o valor à esquerda é menor ou igual ao valor à direita.

Estes operadores geralmente são usados em expressões condicionais, como em **estruturas de controle de fluxo** (por exemplo, `if`, `else`, `while`, `for`) ou em expressões lógicas mais complexas.

***



**Operadores relacionais** comparam dois valores e retornam um resultado **verdadeiro (1)** ou **falso (0)**.

| Operador | Significado          | Exemplo  | Resultado          |
| -------- | -------------------- | -------- | ------------------ |
| `==`     | **Igual a**          | `5 == 5` | **Verdadeiro (1)** |
| `!=`     | **Diferente de**     | `5 != 3` | **Verdadeiro (1)** |
| `>`      | **Maior que**        | `5 > 3`  | **Verdadeiro (1)** |
| `<`      | **Menor que**        | `5 < 3`  | **Falso (0)**      |
| `>=`     | **Maior ou igual a** | `5 >= 5` | **Verdadeiro (1)** |
| `<=`     | **Menor ou igual a** | `5 <= 3` | **Falso (0)**      |

***

## **Operadores Lógicos**

Os **operadores lógicos** são usados para combinar expressões relacionais e tomar decisões mais complexas.

| Operador | Nome             | Descrição                                                                                                                                   | Exemplo                  |
| -------- | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------ |
| `&&`     | E lógico (AND)   | Verdadeiro se **ambas** as condições forem verdadeiras                                                                                      | `(5 > 3) && (2 < 4)` → 1 |
| \|\|     | (OU lógico)      | **Verdadeiro (1)** se **pelo menos uma** das condições for verdadeira. Ele só retorna **falso (0)** se **todas as condições** forem falsas. | OU lógico (OR)           |
| `!`      | NÃO lógico (NOT) | Inverte o valor lógico                                                                                                                      | `!(5 > 3)` → 0           |



***



### O símbolo do **operador E lógico (AND)** em C é:

**Como funciona?**

O operador `&&` retorna **verdadeiro (1)** **apenas se ambas as condições forem verdadeiras**.

* Se **uma ou ambas** forem falsas, o resultado será **falso (0)**.

{% code overflow="wrap" %}
```c
#include <stdio.h>

int main()
{
    int age = 20;
    int drive_license = 1; // 1 = verdadeiro (tem carteira), 0 = falso

    // Verifica se a pessoa tem 18 anos ou mais E tem carteira de motorista
    if (age >= 18 && drive_license)
    {
        printf("Você pode conduzir!\n");
    }
    else
    {
        printf("Você não pode conduzir.\n");
    }
    return 0;
}
```
{% endcode %}

***



### O símbolo do **operador OU lógico (OR)** em C é:

**Como funciona?**

O operador `||` retorna **verdadeiro (1)** se **pelo menos uma** das condições for verdadeira. Ele só retorna **falso (0)** se **todas as condições** forem falsas.

{% code overflow="wrap" %}
```c
#include <stdio.h>

int main() {
  int a = 5, b = 10;

  // Verifica se pelo menos uma das condições é verdadeira
  if (a > 0 || b < 0) {
    printf("Pelo menos uma das condições é verdadeira.\n");
  } else {
    printf("Nenhuma das condições é verdadeira.\n");
  }
  return 0;
}
```
{% endcode %}



***



## O símbolo do **operador NÃO lógico (NOT)** em C é:

#### &#x20;**Como funciona?**

O operador `!` **inverte** o valor lógico de uma expressão:

* Se a condição for **verdadeira (1)**, o operador retorna **falso (0)**.
* Se a condição for **falsa (0)**, o operador retorna **verdadeiro (1)**.

{% code overflow="wrap" %}
```c
#include <stdio.h>

int main() 
{
    int x = 0;

    if (!x) { // x é 0 (falso), mas o operador NOT inverte para verdadeiro
        printf("A condição é verdadeira após a negação.\n");
    } else {
        printf("A condição permanece falsa.\n");
    }

    return 0;
}
```
{% endcode %}



***



{% hint style="warning" %}
### ⚡️ **Lightning Round 2**: <a href="#actividades-de-aprendizagem" id="actividades-de-aprendizagem"></a>

Qual será o valor de `resultado` após a execução do código abaixo?

{% code overflow="wrap" %}
```c
#include <stdio.h>

int main()
{
    int a = 3, b = 7, c = 0;
    int resultado = (a > 2 && b < 10) || !c;

    printf("%d\n", resultado);
    return 0;
}
```
{% endcode %}
{% endhint %}

{% hint style="warning" %}
### ⚡️ Lightning Round 1:&#x20;

O que será impresso pelo seguinte código?

{% code overflow="wrap" %}
```c
#include <stdio.h>

int main()
{
    int x = 5, y = 10, z = 0;

    if (x > 0 && y > 5) {
        printf("A\n");
    }
    if (x < 0 || z) {
        printf("B\n");
    }
    if (!(y == 10)) {
        printf("C\n");
    }

    return 0;
}
```
{% endcode %}


{% endhint %}

