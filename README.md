# super-trunfo-c
Linha de códigos simples criando o esquema básico do jogo "Super trunfo"

/* VERSÃO CORRIGIDA CHAT GPT

#include <stdio.h>
#include <string.h>

int main () {
    char Estado[50];
    char codigo[20];
    char nomeCidade[50];
    int populacao;
    float Area;
    float Pib;
    int pontostour;

    printf("Digite seu Estado: \n");
    fgets(Estado, sizeof(Estado), stdin);
    Estado[strcspn(Estado, "\n")] = 0; // remove \n

    printf("Digite seu código:\n");
    fgets(codigo, sizeof(codigo), stdin);
    codigo[strcspn(codigo, "\n")] = 0;

    printf("Nome da cidade:\n");
    fgets(nomeCidade, sizeof(nomeCidade), stdin);
    nomeCidade[strcspn(nomeCidade, "\n")] = 0;

    printf("Digite o número de habitantes:\n");
    scanf("%d", &populacao);

    printf("Digite a área do país: \n");
    scanf("%f", &Area);

    printf("Digite o PIB aproximado do país:\n");
    scanf("%f", &Pib);

    printf("Digite o total de pontos turísticos do país:\n");
    scanf("%d", &pontostour);

    printf("\n--- Dados Informados ---\n");
    printf("Estado: %s\n", Estado);
    printf("Código: %s\n", codigo);
    printf("Cidade: %s\n", nomeCidade);
    printf("População: %d\n", populacao);
    printf("Área: %.2f metros quadrados\n", Area);
    printf("PIB: %.2f-em trilões\n", Pib);
    printf("Pontos Turísticos: %d\n", pontostour);

    return 0;
}
