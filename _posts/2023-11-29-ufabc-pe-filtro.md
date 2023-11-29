---
title: Algoritmo para aplicar filtro em imagem com convolução
date: 2023-11-29 19:21 -300
categories: [UFABC, Programação Estruturada]
tags: [programming,c,image,processing]
---

# Código em C
Segue abaixo o código em C:

```c
#include <stdio.h>
#include <stdlib.h>

int main(int arc, char *argv[]){
    char aux, tipoArquivo[3];
    int i, j, linhas, colunas, cmax;
    int k, l, linhasFiltro, colunasFiltro;
    int somaPonderada, x, y;
    
    FILE *pImagem;
    pImagem = fopen(argv[1], "r");
    fscanf(pImagem, "%s", tipoArquivo);
    printf("%s\n",tipoArquivo);
    
    fscanf(pImagem, "%d %d %d", &colunas, &linhas, &cmax);
    printf("%d %d\n%d\n", colunas, linhas, cmax);
    
    int matriz[linhas][colunas];
    int imagemFiltrada[linhas][colunas];
    
    for (i=0;i<linhas;i++){
        for (j=0;j<colunas;j++){
            fscanf(pImagem, "%d", &matriz[i][j]);
        }
    }
    
    // for (i=0;i<linhas;i++){
    //     for (j=0;j<colunas;j++){
    //         printf("%d ", matriz[i][j]);
    //     }
    //     printf("\n");
    // }
    
    FILE *pFiltro;
    pFiltro = fopen(argv[2], "r");
    fscanf(pFiltro, "%d %d", &colunasFiltro, &linhasFiltro);
    int matrizFiltro[linhasFiltro][colunasFiltro];
    
    for (k=0;k<linhasFiltro;k++){
        for (l=0;l<colunasFiltro;l++){
            fscanf(pFiltro, "%d", &matrizFiltro[k][l]);
        }
    }
    
    // printf("\n");
    // for (k=0;k<linhasFiltro;k++){
    //     for (l=0;l<colunasFiltro;l++){
    //         printf("%d ", matrizFiltro[k][l]);
    //     }
    //     printf("\n");
    // }
    
    
    
    printf("\n");
    for (i=0;i<linhas;i++){
        for (j=0;j<colunas;j++){
            // if (i>0&&i<linhas-1&&j>0&&j<colunas-1){
            //     printf("%d ", matriz[i][j]);
            // }
            
            somaPonderada=0;
            for (k=0;k<linhasFiltro;k++){
                for (l=0;l<colunasFiltro;l++){
                    x = i-(linhasFiltro/2)+k;
                    y = j-(colunasFiltro/2)+l;
                    
                    if (x>-1&&x<linhas&&y>-1&&y<colunas){
                        // printf("[%d][%d] ", x, y);
                        somaPonderada += matriz[x][y]*matrizFiltro[k][l];
                    }
                }
            }
            // printf("\n");
            if (somaPonderada<0){
                somaPonderada=0;
            }
            if (somaPonderada>cmax){
                somaPonderada=cmax;
            }
            
            imagemFiltrada[i][j] = somaPonderada;
            printf("%d ", somaPonderada);
        }
        printf("\n");
    }
    
    
    return 0;
}
```