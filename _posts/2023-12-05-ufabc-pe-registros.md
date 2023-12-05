---
title: Registros
date: 2023-12-05 14:40 -300
categories: [UFABC, Programação Estruturada]
tags: [programming,c,registro]
---

## Registros
Um Registro, ou estrutura, permite que várias variáveis sejam armazenadas dentro de um objeto, facilitando relacionar diferentes variáveis. Isso pode ser feito a partir do método **struct**, que funciona na seguinte sintaxe:

```c
#include <stdio.h>
#include <string.h>

// define classe documento
struct documento{
    char nome[128];
    char cpf[128];
    int idade;
    float peso;
};

int main(){
    // define o objetos a,b
    struct documento a, b;
    strcpy(a.nome, "Tobias");
    strcpy(a.cpf, "111.222.333/44");
    a.idade=28;
    a.peso=67.9;

    printf("A idade de %s é %d",a.nome,a.idade);

    return 0;
}
```

## Typedef
O comando **typedef** permite definir novos tipos de variáveis, como por exemplo: int, float, double. Ele pode ser utilizado para simplificar a sintaxe na definição de objetos de uma classe. Por exemplo:

```c
#include <stdio.h>
#include <string.h>

// define classe documento
struct documento{
    char nome[128];
    char cpf[128];
    int idade;
    float peso;
};

// define um tipo para a classe
typedef struct documento doc;

int main(){
    // struct documento a, b = doc a,b
    doc a,b;
    strcpy(a.nome, "Tobias");
    strcpy(a.cpf, "111.222.333/44");
    a.idade=28;
    a.peso=67.9;

    printf("A idade de %s é %d",a.nome,a.idade);

    return 0;
}
```

## Enum
Similarmente ao **typedef**, o método enum