# Continue e Break

{% hint style="info" %}
#### **Saiba mais** <a href="#saiba-mais" id="saiba-mais"></a>

**No final desta lição, você será capaz de responder ao como alterar o fluxo de um programa com**:

* `continue` `break`

Diferenças entre as instruçóes `if` `else` e  `switch`e quando utilizar uma delas&#x20;
{% endhint %}

***

### `Continue` e `Break`

Como esclarecido na [página anterior](./#desvios-e-saltos) `continue` e `break` são utilizados para alterar o fluxo de execução dentro de laços de repetição (`for`, `while`, `do-while`) e também no comando `switch-case` em C.

* `break`**:**
  * Interrompe imediatamente o loop de repetição em que está inserido.
  * O programa continua a execução a partir da instrução seguinte ao loop.
* `continue`**:**
  * Interrompe a iteração actual do loop de repetição em que está inserido.
  * O programa pula para a avaliação da condição do loop e, se verdadeira, executa a próxima iteração.

### **O uso de** `break` **e** `continue`**:**

{% code overflow="wrap" %}
```c
#include <stdio.h>

int main() {

  for (int i = 1; i <= 10; i++) {
    if (i == 5) {
      break; // Sai do loop quando i for igual a 5
    }
    if (i % 2 == 0) {
      continue; // Pula para a próxima iteração se i for par
    }
    printf(" repetição ímpar número %d\n", i);
  }

  return 0;
}
```
{% endcode %}

{% hint style="info" %}


* Só será executado se:
  * `i` **não for 5**
  * `i` **não for par**
* Ou seja, só imprime **números ímpares menores que 5**.
{% endhint %}

```
>.
 repetição ímpar número 1
 repetição ímpar número 3

```



## Quando usar `switch` ao invez de `if-else`?

**Use** `switch` **quando**:

* Há muitas comparações com **valores fixos**.
* Você trabalha com **números inteiros ou caracteres**.

**Prefira** `if-else` **quando**:

* As comparações **envolvem intervalos** (`>`, `<`, `>=`, `<=`).
* A condição envolve **números de ponto flutuante** (`float`**,** `double`).
* O `switch` ficaria grande e difícil de ler.

{% hint style="info" %}
## Saiba mais:

### <mark style="color:green;">Quando o "Fall-Through" é Útil?</mark>



Embora muitas vezes indesejado, o "fall-through" pode ser útil em alguns casos, como **casos agrupados**:

***



<pre class="language-c" data-overflow="wrap"><code class="lang-c">#include &#x3C;stdio.h>

int main() { char letra = 'a';

<strong>switch (letra) {
</strong>    case 'a':  
    case 'e':  
    case 'i':  
    case 'o':  
    case 'u':
        printf("É uma vogal!\n");
        break;
    default:
        printf("É uma consoante!\n");
}

return 0;
</code></pre>

}
{% endhint %}

{% code title="TERMINAL" overflow="wrap" %}
```
>.
É uma vogal!
```
{% endcode %}



***
