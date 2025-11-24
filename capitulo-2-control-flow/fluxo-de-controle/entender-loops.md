# Entender loops

## Instrução `for`

&#x20;loop `for` é uma estrutura de controle de fluxo ou repetição que permite executar repetidamente um bloco de código enquanto uma condição for verdadeira. Ele é amplamente utilizado para situações em que o número de iterações é conhecido previamente.

#### **Sintaxe `for`**

{% code overflow="wrap" %}
```c
for (inicialização; condição; incremento) {
  // bloco de código a ser repetido
}
```
{% endcode %}

* **inicialização:** Esta expressão é executada apenas uma vez, no início do loop. É comum usada para inicializar uma variável de controle que será utilizada para contar o número de iterações.
* **condição:** Esta expressão é avaliada antes de cada iteração do loop. Se a condição for verdadeira, o bloco de código é executado. Se a condição for falsa, o loop termina.
* **incremento:** Esta expressão é executada após cada iteração do loop. É comum usada para atualizar a variável de controle para a próxima iteração.

### **Exemplo:**

{% code overflow="wrap" %}
```c
#include <stdio.h>

int main() {
  int item;

  for (item = 1; item <= 5; item++) {
    printf("Contando %d\n", item);
  }

  return 0;
}
```
{% endcode %}

**Saída:**

{% code overflow="wrap" %}
```

Contando  1
Contando  2
Contando  3
Contando  4
Contando  5

```
{% endcode %}

* **Inicialização**: `int i = 0` (a variável `i` começa em 0).
* **Condição**: `i < 5` (o loop continua enquanto `i` for menor que 5).
* **Incremento**: `i++` (a variável `i` é incrementada em 1 a cada iteração).

***



## Instrução `while` <a href="#instrucao-while" id="instrucao-while"></a>



O `while` é uma **instrução de controle de fluxo** que utiliza uma **condição** para determinar se um bloco de código será executado repetidamente. Em poucas palavras podemos dizer que, o `while` é uma **estrutura de repetição** que depende de uma **condição lógica** para continuar ou parar a execução de um loop.

#### **Sintaxe `while`**

{% code overflow="wrap" %}
```c
while (condição) {
    // Bloco de código a ser executado enquanto a condição for verdadeira
}
```
{% endcode %}

### **Exemplo**

{% code overflow="wrap" %}
```c
#include <stdio.h>

int main()
{
    int counter = 0;

    // Loop enquanto a condição (contador < 5) for verdadeira
    while (counter < 5)
    {
        printf("Contando: %d\n", counter);
        counter++; // Incrementa o contador
    }

    return 0;
}
```
{% endcode %}

**Saída:**

{% code overflow="wrap" %}
```

Contando: 0
Contando: 1
Contando: 2
Contando: 3
Contando: 4

```
{% endcode %}

* **Condição**: `contador < 5`
* O loop executa enquanto o valor de `contador` for menor que 5. Quando `contador` atinge 5, o loop é encerrado.

***



## Instrução `do-while` <a href="#instrucao-do-while" id="instrucao-do-while"></a>



O `do-while` é uma estrutura de controle de repetição, assim como o `while` e o `for`. A diferença é que o `do-while` garante que o bloco de código dentro dele seja executado **ao menos uma vez**, mesmo que a condição especificada seja falsa desde o início.

#### **Sintaxe`do-while`**

{% code overflow="wrap" %}
```c
do {
    // Bloco de código a ser executado
} while (condição);

```
{% endcode %}

### Exemplo

{% code overflow="wrap" %}
```c
#include <stdio.h>

int main(void)
{
    int items = 0;

    do
    {
        printf("Contando: %d\n", items);
        items++;

    } while (items < 5);

    return 0;
}
```
{% endcode %}

**Saída:**

{% code overflow="wrap" %}
```

Contando: 0
Contando: 1
Contando: 2
Contando: 3
Contando: 4

```
{% endcode %}

* O bloco de código é executado **antes** de verificar a condição `items < 5`.
* O loop termina quando a condição se torna falsa.

