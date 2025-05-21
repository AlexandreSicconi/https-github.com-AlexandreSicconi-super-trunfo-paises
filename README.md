# https-github.com-AlexandreSicconi-super-trunfo-paises
mkdir super-trunfo-paises cd super-trunfo-paises
#include <stdio.h>

int main() {
    const int estados = 8;
    const int cidades_por_estado = 4;

    char codigos[estados * cidades_por_estado][4];
    int populacao[estados * cidades_por_estado];
    float area[estados * cidades_por_estado];
    float pib[estados * cidades_por_estado];
    int pontos_turisticos[estados * cidades_por_estado];

    int contador = 0;
    for (char estado = 'A'; estado <= 'H'; estado++) {
        for (int cidade = 1; cidade <= 4; cidade++) {
            sprintf(codigos[contador], "%c%02d", estado, cidade);
            contador++;
        }
    }

    printf("\n===== Cadastro das Cartas =====\n");
    for (int i = 0; i < estados * cidades_por_estado; i++) {
        printf("\nCarta %s:\n", codigos[i]);

        printf("Digite a populacao: ");
        scanf("%d", &populacao[i]);

        printf("Digite a area (em km²): ");
        scanf("%f", &area[i]);

        printf("Digite o PIB (em bilhões): ");
        scanf("%f", &pib[i]);

        printf("Digite o número de pontos turísticos: ");
        scanf("%d", &pontos_turisticos[i]);
    }

    printf("\n===== Cartas Cadastradas =====\n");
    for (int i = 0; i < estados * cidades_por_estado; i++) {
        printf("\nCarta %s:\n", codigos[i]);
        printf("População: %d habitantes\n", populacao[i]);
        printf("Área: %.2f km²\n", area[i]);
        printf("PIB: %.2f bilhões\n", pib[i]);
        printf("Pontos turísticos: %d\n", pontos_turisticos[i]);
    }

    return 0;
git add .


}

