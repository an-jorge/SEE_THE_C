---
icon: '4'
---

# Cálculo de Percentual de Votos em uma Eleição Municipal

{% code title="main.c" overflow="wrap" %}
```c
#include <stdio.h>
#include <stdlib.h>
#include <locale.h> // Para setlocale()

int main() {
#ifdef _WIN32
    system("cls"); // Para Windows
#else
    system("clear"); // Para Linux/macOS
#endif

    if (setlocale(LC_ALL, "pt_PT.utf8") == NULL)
    {
        printf("Localização pt_PT indispónivel\n");
        printf(
            "acentuação poderá não ser a correta significa que a forma como as palavras foram acentuadas na frase pode estar errada. "
            "Isso pode acontecer devido à aplicação incorreta das regras de acentuação gráfica da língua portuguesa. \n");
    }

    printf("Exercício #4 | CAP #1:\n");
    printf("================================================================\n");
    printf("|  Cálculo de Percentual de Votos em uma Eleição Municipal     |\n");
    printf("===============================================================\n");

    // Resolvendo o Exercício

    float total_votes;
    float blank_votes;
    float spoiled_votes;
    float valid_votes;

    printf("Digite o número total de eleitores:\n");
    scanf("%f", &total_votes);
    printf("Digite o número de votos brancos:\n");
    scanf("%f", &blank_votes);
    printf("Digite o número de votos nulos:");
    scanf("%f", &spoiled_votes);
    printf("Digite o número de votos válidos:\n");
    scanf("%f", &valid_votes);

    const float blank_votes_perc = (blank_votes / total_votes) * 100;
    const float spoiled_votes_per = (spoiled_votes / total_votes) * 100;
    const float valid_votes_per = (valid_votes / total_votes) * 100;

    printf("O percentual de votos brancos: %.1f%% \n", blank_votes_perc);
    printf("O percentual de votos nulos: %.1f%% \n", spoiled_votes_per);
    printf("O percentual de votos válidos: %.1f%% \n", valid_votes_per);

    return 0;
}
```
{% endcode %}

{% code title="TERMINAL" overflow="wrap" %}
```
Exercício #4 | CAP #1:

O percentual de votos brancos: 10.0% 
O percentual de votos nulos: 5.0% 
O percentual de votos válidos: 85.0% 

```
{% endcode %}

<a href="../capitulo-1-basic/capitulo-1-exercicios/calculo-de-percentual-de-votos-em-uma-eleicao-municipal.md" class="button secondary">E4</a>

