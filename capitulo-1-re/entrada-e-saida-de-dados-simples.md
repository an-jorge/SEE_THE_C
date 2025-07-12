---
icon: '3'
---

# Entrada e Saída de dados Simples

{% code title="main.c" overflow="wrap" %}
```c
#include <stdio.h>
#include <stdlib.h>

int main()
{

#ifdef _WIN32
    system(cls); // Limpa o terminal no Windows
#else
    system("clear"); // Limpa o terminal no Linux e macOS
    #endif

if (setlocale(LC_ALL, "pt_PT.utf8") == NULL)
{
    printf(" \t Idioma PT indisponível.\n");
    printf(" \t Aviso: O idioma do sistema não está configurado como português. \n"
           " \t Por essa razão, a acentuação pode estar incorreta.\n\n");
}
    printf("Exercício #3 | CAP #1: \n");
    printf("========================================\n");
    printf("|  Entrada e Saída de dados Simples     |\n");
    printf("========================================\n")

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

<a href="../capitulo-1-basic/capitulo-1-exercicios/entrada-e-saida-de-dados-simples.md" class="button secondary">E3</a>
