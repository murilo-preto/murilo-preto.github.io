---
title: Ponteiros, memória e alocação dinâmica
date: 2023-12-05 14:00 -300
categories: [UFABC, Programação Estruturada]
tags: [programming,c,pointer]
---

## Ponteiros
São estruturas de dados que armazenam um endereço de memória. Em sua declaraçãom devem receber o tipo que será endereçado (int, float), assim como o prefixo \*, indicando que se trata de um ponteiro.

```c
int num = 5;
int *ponteiroNum;

// & passa o endereço de memória da variável
ponteiroNum = &num;

// As duas funções a seguir são equivalentes:
printf("%d",*ponteiroNum); // * acessa o conteúdo do endereço
printf("%d", num);
```

### Passagem por referência
Ponteiros são muito úteis para alterar valores diretamente em uma variável dentro de uma função, sem que seja necessário retorná-la explicitamente:

```c
#include <stdio.h>

// Declaração explícita da função
void somaInt(int *soma, int a, int b);

void somaInt(int *soma, int a, int b){
    // Insere a soma de dois int por referência em outro int
    *soma = a+b;
}

int main(){
    int soma=0,a=5,b=3;
    
    // &soma é o endereço de memória da variável (ponteiro)
    somaInt(&soma,a,b);
    printf("%d",soma);

    return 0;
}

// -> É printado na tela '8'.
```
## Alocação dinâmica
Para alocar dinamicamente vetores durante o tempo de execução, podem ser usadas as funções **malloc** e **calloc**. A diferença entre elas é que a função **calloc** irá zerar os valores alocados, enquanto **malloc** deixa o lixo de memória na alocação, mas sendo por sua vez mais rápida.

> Para usar as funções **malloc** e **calloc**, deve-se lembrar de incluir a biblioteca **stdlib.h**!
{: .prompt-warning }

### Malloc
```c
#include <stdlib.h>

int main(){
    int *p,i;
    p = malloc(100*sizeof(int));

    for (i=0;i<100;i++){
        p[i]=i;
    }

    free(p); // Libera memória alocada
    return 0;
}

```

> Usar a função **free** é uma prática importante para liberar a memória alocada dinamicamente, que caso contrário, permanecerá alocada até que o computador seja reiniciado.
{: .prompt-tip }


### Calloc
```c
#include <stdlib.h>

int main(){
    int *p,i;
    p = calloc(100, sizeof(int));

    for (i=0;i<100;i++){
        p[i]=i;
    }

    free(p); // Libera memória alocada
    return 0;
}

```

> Nota-se que a sintaxe de **malloc** e **calloc** é um pouco diferente. Em um são especificados os **bytes**, e em outra os **blocos de memória** e o **tamanho**!
{: .prompt-info }
