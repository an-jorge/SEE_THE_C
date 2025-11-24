---
icon: '2'
---

# Conversão de Temperatura

{% code title="main.c" overflow="wrap" %}
```c
#include <stdio.h>

int main()
{

    printf("Exercício 2: Conversão de Temperatura de Celsius para Fahrenheit \n");

    printf("\n");
    int celsius = 20;
    int fahrenheit = (celsius * 9 / 5) + 32;
    printf("%dºC correspondem a %dºF\n", celsius, fahrenheit);

    return 0;
}
```
{% endcode %}

{% code title="TERMINAL" overflow="wrap" %}
```

> 20ºC correspondem a 68ºF

```
{% endcode %}

<a href="../capitulo-1-basic/capitulo-1-exercicios/conversao-de-temperatura.md" class="button secondary">E1</a>
