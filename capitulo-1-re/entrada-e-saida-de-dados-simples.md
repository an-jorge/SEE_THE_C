---
icon: '3'
---

# Entrada e Saída de dados Simples

{% code title="main.c" overflow="wrap" %}
```c
#include <stdio.h>
#include <locale.h>
#include <stdlib.h>
#include <unistd.h>



int main() {

    // Tenta usar ANSI escape codes (funciona em Unix, Linux, Mac, e terminais modernos no Windows)
    if (isatty(fileno(stdout))) {
        // ANSI: limpa tela e move cursor para o topo
        printf("\033[2J\033[H");
        fflush(stdout);
    } else {
        // Fallback para sistemas sem suporte ANSI
#ifdef _WIN32
        system("cls");
#else
        system("clear");
#endif
    }

    const char *locales[] = {
        "pt_PT.utf8", "pt_PT.UTF-8",
        "pt_BR.utf8", "pt_BR.UTF-8",
        "pt_PT", "pt_BR",
        "Portuguese",                      // Windows (genérico)
        "Portuguese_Portugal.1252",       // Windows (Portugal)
        "Portuguese_Brazil.1252",         // Windows (Brasil)
        NULL
    };

    const char *locale = NULL;
    for (int i = 0; locales[i]; i++) {
        if (setlocale(LC_ALL, locales[i])) {
            locale = locales[i];
            break;
        }
    }

    if (locale)
        printf("\t Localidade definida: %s\n", locale);
    else {
    printf(" \t Aviso: O idioma do sistema não está configurado como português. \n"
           " \t Por essa razão, a acentuação poderá estar incorreta.\n\n");
}

    /*
     * Resolvendo o Exercício
     */
    printf("Exercício #3 | CAP #1: \n");
    printf("========================================\n");
    printf("|  Entrada e Saída de dados Simples     |\n");
    printf("========================================\n");

    printf("\n");
    int how_old;
    float how_weight;

    printf("Informe a sua idade:\n");
    scanf("%d", &how_old);
    printf("Informe a sua idade:\n");
    scanf("%f", &how_weight);
    printf("Você tem %d anos e pesa %2.f Kg\n", how_old, how_weight);

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
