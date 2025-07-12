---
icon: '5'
---

# Cálculo de Novo Salário com Reajuste

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
    printf(" \t Idioma PT indisponível.\n");
    printf(" \t Aviso: O idioma do sistema não está configurado como português.\n"
           " \t Por essa razão, a acentuação pode estar incorreta.\n\n");
}

    /*
     * Resolvendo o Exercício
     */

printf("Exercício #5 CAP #1:\n");
printf("================================================================\n");
printf("|  Cálculo de Novo Salário com Reajuste     |\n");
printf("===============================================================\n");


    float salary;
    float readjustment_per;

    printf("Digite o salário atual do funcionário:\n");
    scanf("%f", &salary);
    printf("Digite o percentual de reajuste:\n");
    scanf("%f", &readjustment_per);

    const float new_salary = salary + (salary * readjustment_per / 100);

    printf("O novo salário é: %.2f ", new_salary);

    return 0;
}
```
{% endcode %}

{% code title="TERMINAL" overflow="wrap" %}
```
Exercício #5 CAP #1:
================================================================
|  Cálculo de Novo Salário com Reajuste     |
===============================================================
Digite o salário atual do funcionário:
3000
Digite o percentual de reajuste:
5
O novo salário é: 3150.00 
```
{% endcode %}

<a href="../capitulo-1-basic/capitulo-1-exercicios/calculo-de-novo-salario-com-reajuste.md" class="button secondary">E5</a>

