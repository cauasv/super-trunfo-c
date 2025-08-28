# super-trunfo-c
Linha de códigos simples criando o esquema básico do jogo "Super trunfo"

//versão 2.0 corrigida pelo Chat GPT
#include <stdio.h>
#include <string.h>

int main () {
    char Estado1[50];
    char codigo1[20];
    char nomeCidade1[50];
    unsigned long int populacao1;
    float Area1;
    float Pib1;
    int pontostour1;

    char Estado2[50];
    char codigo2[20];
    char nomeCidade2[50];
    unsigned long int populacao2;
    float Area2;
    float Pib2;
    int pontostour2;

    printf("Digite seu Estado: \n");
    fgets(Estado1, sizeof(Estado1), stdin);
    Estado1[strcspn(Estado1, "\n")] = 0;

    printf("Digite seu código:\n");
    fgets(codigo1, sizeof(codigo1), stdin);
    codigo1[strcspn(codigo1, "\n")] = 0;

    printf("Nome da cidade:\n");
    fgets(nomeCidade1, sizeof(nomeCidade1), stdin);
    nomeCidade1[strcspn(nomeCidade1, "\n")] = 0;

    printf("Digite o número de habitantes:\n");
    scanf("%d", &populacao1);

    printf("Digite a área do país (km²): \n");
    scanf("%f", &Area1);

    printf("Digite o PIB aproximado do país (em trilhões):\n");
    scanf("%f", &Pib1);

    printf("Digite o total de pontos turísticos do país:\n");
    scanf("%d", &pontostour1);

    while (getchar() != '\n'); // limpar buffer antes de usar fgets de novo

    // ---- SEGUNDA CARTA ----
    printf("\nAGORA VAMOS CRIAR A SEGUNDA CARTA:\n");

    printf("Digite seu Estado: \n");
    fgets(Estado2, sizeof(Estado2), stdin);
    Estado2[strcspn(Estado2, "\n")] = 0;

    printf("Digite seu código:\n");
    fgets(codigo2, sizeof(codigo2), stdin);
    codigo2[strcspn(codigo2, "\n")] = 0;

    printf("Nome da cidade:\n");
    fgets(nomeCidade2, sizeof(nomeCidade2), stdin);
    nomeCidade2[strcspn(nomeCidade2, "\n")] = 0;

    printf("Digite o número de habitantes:\n");
    scanf("%d", &populacao2);

    printf("Digite a área do país (km²): \n");
    scanf("%f", &Area2);

    printf("Digite o PIB aproximado do país (em trilhões):\n");
    scanf("%f", &Pib2);

    printf("Digite o total de pontos turísticos do país:\n");
    scanf("%d", &pontostour2);

    // ---- CÁLCULOS ----
    float densidade1 = populacao1 / Area1;
    float pibpc1 = (Pib1 * 1000000000000) / populacao1; // se PIB for em trilhões

    float densidade2 = populacao2 / Area2;
    float pibpc2 = (Pib2 * 1000000000000) / populacao2;

    float Superpoder1 =populacao1+pibpc1+Area1+Pib1+pontostour1+densidade1;
    float Superpoder2=populacao2+pibpc2+Area2+Pib2+pontostour2+densidade2;

    // ---- EXIBIR RESULTADOS ----
    printf("\n--- Dados Informados Carta 1 ---\n");
    printf("Estado: %s\n", Estado1);
    printf("Código: %s\n", codigo1);
    printf("Cidade: %s\n", nomeCidade1);
    printf("População: %d\n", populacao1);
    printf("Área: %.2f km²\n", Area1);
    printf("PIB: %.2f trilhões\n", Pib1);
    printf("Pontos Turísticos: %d\n", pontostour1);
    printf("Densidade Populacional: %.2f hab/km²\n", densidade1);
    printf("PIB per capita: %.2f\n", pibpc1);

    printf("\n--- Dados Informados Carta 2 ---\n");
    printf("Estado: %s\n", Estado2);
    printf("Código: %s\n", codigo2);
    printf("Cidade: %s\n", nomeCidade2);
    printf("População: %d\n", populacao2);
    printf("Área: %.2f km²\n", Area2);
    printf("PIB: %.2f trilhões\n", Pib2);
    printf("Pontos Turísticos: %d\n", pontostour2);
    printf("Densidade Populacional: %.2f hab/km²\n", densidade2);
    printf("PIB per capita: %.2f\n", pibpc2);

    //-------------------------Comparação das carta----------------------------------------
    printf("Hora de comparar as cartas\n");
    if (populacao1>populacao2){
        printf("A população da carta 1 é maior que a carta 2\n");
    }else{
        printf("A população da carta 2 é maior que a carta 1\n");
    }

     if (Area1>Area2){
        printf("A area da carta 1 é maior que a carta 2\n");
    }else{
        printf("A area da carta 2 é maior que a carta 1\n");
    }

    if(Pib1>Pib2){
        printf("O Pib da carta 1 supera da carta 2\n");
    }else{
        printf("O PIb da carta 1 é menor que o da carta 2\n");
    }

if(pontostour1>pontostour1){
    printf("A quantidade de pontos turisticos da carta 1 supera a da carta 2\n");
}else{
printf("A quantidade de pontos turisticos da carta 1 é menor do que a carta 2\n");
}

if(densidade1>densidade2){
    printf("A densidade da carta 2 é melhor do que a carta 1\n");

}else{
printf("A densidade da carta 1 é melhor do que a carta 1\n");
}

if(pibpc1>pibpc2){
    printf("A carta 1 ganhou sobre o pib per capita\n");
}else{
    printf("A carta 2 ganhou sobre o pib per capita\n");
}


    return 0;
}
