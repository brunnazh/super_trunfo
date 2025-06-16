#include <stdio.h>
#include <stdlib.h>
#include <locale.h> // Para setar o idioma no Windows

int main(void) {
    setlocale(LC_ALL, "Portuguese"); // Suporte a acentuação

    char estado[100];
    char carta[50];
    char cidade[50];
    int populacao1 = 0, populacao2 = 0;
    float area1 = 0, area2 = 0;
    float pib1 = 0, pib2 = 0;
    int pontos_turisticos1 = 0, pontos_turisticos2 = 0;
    float densidade1 = 0, densidade2 = 0;
    float per_capita1 = 0, per_capita2 = 0;
    float SuperPoder1 = 0, SuperPoder2 = 0;

    printf("*** Jogo Super Trunfo ***\n");

    // ===== CARTA 1 =====
    printf("\nCarta 1\n");

    printf("Digite o estado: ");
    scanf("%s", estado);
    fflush(stdin);

    printf("Digite o código da carta (ex: A01): ");
    scanf("%s", carta);
    fflush(stdin);

    printf("Digite o nome da cidade: ");
    scanf("%s", cidade);
    fflush(stdin);

    printf("Digite a população: ");
    scanf("%d", &populacao1);
    fflush(stdin);

    printf("Digite a área (em km²): ");
    scanf("%f", &area1);
    fflush(stdin);

    printf("Digite o PIB: ");
    scanf("%f", &pib1);
    fflush(stdin);

    printf("Digite o número de pontos turísticos: ");
    scanf("%d", &pontos_turisticos1);
    fflush(stdin);

    if (area1 != 0)
        densidade1 = populacao1 / area1;
    if (populacao1 != 0)
        per_capita1 = pib1 / populacao1;

    printf("\n--- Carta 1 ---\n");
    printf("Estado: %s\n", estado);
    printf("Carta: %s\n", carta);
    printf("Cidade: %s\n", cidade);
    printf("População: %d\n", populacao1);
    printf("Área: %.2f km²\n", area1);
    printf("PIB: %.2f\n", pib1);
    printf("Pontos turísticos: %d\n", pontos_turisticos1);
    printf("Densidade populacional: %.2f hab/km²\n", densidade1);
    printf("PIB per capita: %.2f reais\n", per_capita1);

    if (densidade1 != 0)
        SuperPoder1 = populacao1 + area1 + pib1 + pontos_turisticos1 + per_capita1 + (1 / densidade1);

    // ===== CARTA 2 =====
    printf("\nCarta 2\n");

    printf("Digite o estado: ");
    scanf("%s", estado);
    fflush(stdin);

    printf("Digite o código da carta (ex: A01): ");
    scanf("%s", carta);
    fflush(stdin);

    printf("Digite o nome da cidade: ");
    scanf("%s", cidade);
    fflush(stdin);

    printf("Digite a população: ");
    scanf("%d", &populacao2);
    fflush(stdin);

    printf("Digite a área (em km²): ");
    scanf("%f", &area2);
    fflush(stdin);

    printf("Digite o PIB: ");
    scanf("%f", &pib2);
    fflush(stdin);

    printf("Digite o número de pontos turísticos: ");
    scanf("%d", &pontos_turisticos2);
    fflush(stdin);

    if (area2 != 0)
        densidade2 = populacao2 / area2;
    if (populacao2 != 0)
        per_capita2 = pib2 / populacao2;

    printf("\n--- Carta 2 ---\n");
    printf("Estado: %s\n", estado);
    printf("Carta: %s\n", carta);
    printf("Cidade: %s\n", cidade);
    printf("População: %d\n", populacao2);
    printf("Área: %.2f km²\n", area2);
    printf("PIB: %.2f\n", pib2);
    printf("Pontos turísticos: %d\n", pontos_turisticos2);
    printf("Densidade populacional: %.2f hab/km²\n", densidade2);
    printf("PIB per capita: %.2f reais\n", per_capita2);

    if (densidade2 != 0)
        SuperPoder2 = populacao2 + area2 + pib2 + pontos_turisticos2 + per_capita2 + (1 / densidade2);

    // ===== COMPARAÇÃO =====
    printf("\n--- Comparação das Cartas ---\n");
    printf("População: %s\n", (populacao1 > populacao2) ? "Carta 1 vence" : "Carta 2 vence");
    printf("Área: %s\n", (area1 > area2) ? "Carta 1 vence" : "Carta 2 vence");
    printf("PIB: %s\n", (pib1 > pib2) ? "Carta 1 vence" : "Carta 2 vence");
    printf("Pontos turísticos: %s\n", (pontos_turisticos1 > pontos_turisticos2) ? "Carta 1 vence" : "Carta 2 vence");
    printf("Densidade Populacional: %s\n", (densidade1 > densidade2) ? "Carta 1 vence" : "Carta 2 vence");
    printf("PIB per capita: %s\n", (per_capita1 > per_capita2) ? "Carta 1 vence" : "Carta 2 vence");
    printf("Super Poder: %s\n", (SuperPoder1 > SuperPoder2) ? "Carta 1 vence" : "Carta 2 vence");

    return 0;
}

