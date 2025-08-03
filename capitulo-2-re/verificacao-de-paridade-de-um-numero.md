---
icon: '1'
---

# Verificação de Paridade de um Número



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




    printf("Exercício #2 CAP #2:\n");
    printf("================================================================\n");
    printf("|  Verificação de Paridade de um Número |\n");
    printf("================================================================\n\n");


    int number = 6;
    if (number % 2 == 0) {
        printf("O número PAR");
    } else {
        printf("O número IMPAR");
    }

    return 0;

}
```
{% endcode %}

{% code title="TERMINAL" overflow="wrap" %}
```

>.
Exercício #1 CAP #2:
================================================================
|  Verificação de Paridade de um Número |
================================================================

O número PAR


```
{% endcode %}

<a href="../capitulo-2-exercicios/verificacao-de-paridade-de-um-numero.md" class="button secondary">E1</a>
