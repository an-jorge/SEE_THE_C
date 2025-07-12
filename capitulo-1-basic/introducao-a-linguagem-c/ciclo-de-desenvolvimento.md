# Ciclo de Desenvolvimento

Para desenvolver um aplicativo, um software desktop ou um website começa com o que chamamos de algoritmo expresso em uma linguagem de programação. Tudo que você já viu ou vai ver, desde a máquina de café a foguetes existe uma lógica e um algoritmo. &#x20;

**Linguagem de máquina** é a linguagem dos processadores. Ela é composta de instruções primitivas que correspondem à funcionalidade primitiva de uma CPU. Um algoritmo escrito na linguagem de alto nível que incrementa uma variável pode levar três ou quatro instruções no nível de linguagem de máquina. Portanto, deve haver ferramentas que possam converter de uma linguagem de alto nível, como C, para a linguagem de baixo nível de um processador.

Esse "conversor" é chamado de **compilador**. Um compilador deve analisar um programa, converter a sintaxe e a semântica desse programa em estruturas internas e, em seguida, gerar código de linguagem de máquina com base nessas estruturas internas. Para um programador, a execução do código de linguagem de máquina gerado deve corresponder à semântica do programa de alto nível original.

**Um compilador gera pedaços de código de máquina que precisam ser reunidos em um pacote executável**. Este pacote é normalmente construído por uma ferramenta de linker que coloca os pedaços do programador junto com qualquer código de sistema necessário. O resultado final é um pacote de vários pedaços de código e informações que permitirão que um sistema operacional comece a executar um programa.

***

### **Fluxo de compilação de um programa em C**

<div data-full-width="false"><figure><img src="../../.gitbook/assets/Fluxo do processo.jpg" alt="Compilação de um programa em C "><figcaption><p><strong>Fluxo do processo de compilação de um programa em C</strong></p></figcaption></figure></div>

***



## Etapas do processo de compilação

### **1. Código-fonte (Escrita)**

* O desenvolvedor escreve o programa em **linguagem C** e salva em um arquivo com extensão `.c`.
  * Exemplo: `main.c`.

### **2. Preprocessamento**

* O **preprocessador** (etapa inicial do compilador) executa instruções de diretivas, como `#include` e `#define`.
  * Inclui arquivos de cabeçalho, como `<stdio.h>` ou `<math.h>`.
  * Substitui macros (`#define`) por seus valores.
  * Remove comentários e expande diretivas do tipo `#ifdef`.
* O resultado é um arquivo intermediário com as diretivas processadas.

### **3. Compilação**

* O **compilador** converte o código-fonte preprocessado em **código assembly** (um conjunto de instruções específicas para o processador da máquina).
  * O código assembly é de baixo nível, próximo da linguagem de máquina, mas ainda legível por humanos.
  * Exemplo: Um arquivo `.s` gerado.

### **4. Montagem**

* O **montador** converte o código assembly em **código de máquina** (binário), gerando um arquivo objeto (`.o` ou `.obj`).
  * Esse arquivo contém instruções binárias que o processador pode entender, mas ele ainda não é um programa executável, porque depende de outras partes (bibliotecas, funções, etc.).

### **5. Linkagem**

* O **linker** junta o arquivo objeto gerado com outras bibliotecas e arquivos objeto necessários.
  * Resolve referências entre funções e variáveis (exemplo: `printf()` é ligado à biblioteca padrão `libc`).
  * Gera o programa final, que é um executável.
  * O resultado é o arquivo **executável** (por exemplo, `programa.exe` no Windows ou `programa.out` no Linux).

### **6. Execução**

* Após a linkagem, o programa compilado pode ser executado diretamente pelo sistema operacional.

***

## **Resumo das ferramentas envolvidas**

* **Preprocessador:** Expande macros e inclui cabeçalhos.
* **Compilador:** Converte para código assembly.
* **Montador:** Gera código de máquina.
* **Linker:** Junta tudo e resolve dependências.

Ferramentas como o **GCC (GNU Compiler Collection)** seguem esse processo completo.

***



## **Como funciona a programação?**

\


{% embed url="https://www.blip.ai/blog/wp-content/uploads/2022/08/linguagens_de_programacao_mais_usadas_img1.webp" %}
**como funciona a programação?**
{% endembed %}



## "HELLO WORLD" - Seu Primeiro Programa

***

{% code overflow="wrap" lineNumbers="true" %}
```c
#include <stdio.h>            

int main () 
{                
   printf("Hello World! \n"); 
   return 0;                  
}  

                             
```
{% endcode %}

{% hint style="info" %}
## Compilar o seu código

Dupla barra **//** indica um comentarios são ignorados pelo compilador
{% endhint %}





{% hint style="warning" %}
### ✏️ Actividade de aprendizagem

#### **"Planejamento ou execução: Qual é mais importante?"**

**Perguntas para debate:**

* Um planejamento detalhado reduz problemas futuros?
* É possível planejar demais e nunca começar?

***



#### **"Devemos sempre testar o software?"**

* Até que ponto vale a pena testar um software?
* É possível lançar um software sem testes?
* Qual a diferença entre testes automatizados e manuais?


{% endhint %}



