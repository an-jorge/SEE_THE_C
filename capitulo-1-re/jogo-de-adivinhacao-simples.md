---
icon: '6'
---

# Jogo de Adivinhação Simples

{% code title="main.c" overflow="wrap" %}
```c
#include <stdio.h>
#include <locale.h>
#include <stdlib.h>

int main() {

#ifdef _WIN32
    system(cls); // Limpa o terminal no Windows
#else
    system("clear"); // Limpa o terminal no Linux e macOS
    #endif

if (setlocale(LC_ALL, "pt_PT.utf8") == NULL)
{
    printf(" \t ⚠️ Idioma PT indisponível.\n");
    printf(" \t Aviso: O idioma do sistema não está configurado como português. \n"
           " \t Por essa razão, a acentuação pode estar incorreta.\n\n");
}

    /*
     * Resolvendo o Exercício
     */

printf("Exercício #6 CAP #1:\n");
printf("================================================================\n");
printf("|  Jogo de Adivinhação Simples |\n");
printf("===============================================================\n");

    int shot;
    printf("Diga um número:");
    scanf("%d", &shot);
    if (shot == 4) {
        printf("Acertou!");
    } else {
        printf("Errou!");
    }

    return 0;
}
```
{% endcode %}

{% code title="TERMINAL" overflow="wrap" %}
```

Exercício #6 CAP #1:
================================================================
|  Jogo de Adivinhação Simples |
===============================================================
Diga um número:4

Acertou

```
{% endcode %}

<a href="../capitulo-1-basic/capitulo-1-exercicios/jogo-de-adivinhacao-simples.md" class="button secondary">E6</a>

