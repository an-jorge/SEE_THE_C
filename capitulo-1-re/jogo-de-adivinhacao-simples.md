---
icon: '6'
---

# Jogo de Adivinhação Simples

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
     * SOLUÇÃO DO EXERCÍCIO **
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

