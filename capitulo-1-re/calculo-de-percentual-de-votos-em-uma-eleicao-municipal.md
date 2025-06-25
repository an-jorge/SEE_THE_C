---
icon: '4'
---

# Cálculo de Percentual de Votos em uma Eleição Municipal

{% code title="main.c" overflow="wrap" %}
```c
#include <stdio.h>
#include <stdlib.h>

int main()
{

#ifdef _WIN32
    system("cls"); // Para Windows
#else
    system("clear"); // Para Linux/macOS
#endif

    printf("Exercício #3 | CAP #1: \n");
    printf("========================================\n");
    printf("|  Entrada e Saída de dados Simples     |\n");
    printf("========================================\n");

    // Resolvendo o Exercício

    printf("\n");
    int how_old;
    float how_weight;

    printf("Informe a sua idade:\n");
    scanf("%d", &how_old);
    printf("Informe a sua idade:\n");
    scanf("%f", &how_weight);
    printf("Você tem %d anos e pesa %f.2 Kg\n", how_old, how_weight);

    return 0;
}
```
{% endcode %}

{% code title="TERMINAL" overflow="wrap" %}
```

Exercício #3 | CAP #1: 
========================================
|  Entrada e Saída de dados Simples     |
========================================

Informe a sua idade:
12
Informe a sua idade:
30
Você tem 2 anos e pesa 30.000000.2 Kg


```
{% endcode %}

<a href="../capitulo-1-basic/capitulo-1-exercicios/calculo-de-percentual-de-votos-em-uma-eleicao-municipal.md" class="button secondary">E4</a>
