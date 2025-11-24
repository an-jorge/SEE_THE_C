---
icon: '3'
---

# Dias da Semana

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

    int number;
    printf("Digite o número da semana de 1 a 7:\n");
    scanf("%d", &number);
    switch (number) {
        case 1:
            printf("%d - O dia correspondente é Segunda-feira\n", number);
            break;
            case 2:
            printf("%d - O dia correspondente é Terça-feira\n", number);
            break;
            case 3:
            printf("%d - O dia correspondente é Quarta-feira\n", number);
            break;
            case 4:
            printf("%d - O dia correspondente é Quinta-feira\n", number);
            break;
            case 5:
            printf("%d - O dia correspondente é Sexta-feira\n", number);
            break;
            case 6:
            printf("%d - O dia correspondente é Sábado\n", number);
            break;
            case 7:
            printf("%d - O dia correspondente é Domingo\n");
            break;
            default:
            printf("Entrada invalida");
    }

        return 0;
}
```

{% code title="TERMINAL" overflow="wrap" %}
```

>.
Digite o número da semana de (1 a 7): 3
O dia correspondente é Quarta-feira

```
{% endcode %}

<a href="../capitulo-2-exercicios/dias-da-semana.md" class="button secondary">E3</a>

