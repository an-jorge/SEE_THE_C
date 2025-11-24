---
icon: '2'
---

# Conversor de Temperatura Inteligente



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
    printf("| Conversor de Temperatura Inteligente |\n");
    printf("================================================================\n\n");

    float temperature;
    printf("Digite a temperatura atual:\n");
    scanf("%f", &temperature);
    if (temperature <= 15) {
        printf("%2.f°C Está frio!\n", temperature);
    } else if (temperature > 15 && temperature <= 30) {
        printf("%f.2°C Temperatura agradável", temperature);
    } else if (temperature > 30) {
        printf("%f.2°C Está quente!", temperature);
    }

        return 0;

}
```
{% endcode %}

{% code title="TERMINAL" overflow="wrap" %}
```

>.
Exercício #2 CAP #2:
================================================================
| Conversor de Temperatura Inteligente |
================================================================

Digite a temperatura atual:
30
30.000000.2°C Temperatura agradável


```
{% endcode %}

<a href="../capitulo-2-exercicios/conversor-de-temperatura-inteligente.md" class="button secondary">E2</a>
