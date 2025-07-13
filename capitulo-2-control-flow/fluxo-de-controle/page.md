# Page

## Instrução `switch`

`switch` é usada para realizar uma seleção entre várias alternativas com base no valor de uma expressão. É uma forma mais organizada e eficiente de lidar com múltiplas opções do que uma série de instruções `if` e `else if`.&#x20;

**A estrutura básica do** `switch` **é a seguinte:**

{% code overflow="wrap" %}
```c

#include <stdio.h>

int main()
{
    int option = 1;

    printf("Escolha uma opção:\n");
    printf("1 - Iniciar\n");
    printf("2 - Configurações\n");
    printf("3 - Sair\n");

    switch (option)
    {
    case 1:
        printf("Iniciando...\n");
        break;
    case 2:
        printf("Abrindo configurações...\n");
        break;
    case 3:
        printf("Saindo...\n");
        break;
    default:
        printf("Opção inválida!\n");
    }

    return 0;
}

```
{% endcode %}



{% hint style="danger" %}
## **Atenção:**

### <mark style="color:red;">Evitar "Fall-Through" Indesejado</mark>

`break` impede que os próximos `case` sejam executados.

Se esquecermos o `break`, os `case` seguintes serão executados **mesmo sem correspondência**, causando o que é chamado de efeito chamado **"fall-through"**.



***



{% code overflow="wrap" %}
```c
#include <stdio.h>

int main()
{
    int num = 2;

    switch (num)
    {
    case 1:
        printf("Caso 1\n");
    case 2:
        printf("Caso 2\n");
    case 3:
        printf("Caso 3\n");
    default:
        printf("Padrão\n");
    }

    return 0;
}

```
{% endcode %}

* `break` impede que os próximos `case` sejam executados.


{% endhint %}

{% code title="TERMINAL" overflow="wrap" %}
```

 Caso 2  
 Caso 3
 Padrão   
```
{% endcode %}

