Exercicio 1:

#include <stdio.h>

int main() {
  int visitantes;

  printf("Digite o número de visitantes que entraram hoje: ");
  scanf("%d" , &visitantes);

  printf("Número de visitantes registrados: %d\n", visitantes);
  printf("Obrigado!\n");

  return 0;
}



Exercicio 2:

#include <stdio.h>

int main() {
  float receita, despesa, saldo;

  printf("Digite o valor da receita: ");
  scanf("%f", &receita);

  printf("Digite o valor da despesa: ");
  scanf("%f", &despesa);

  saldo = receita - despesa;

  printf("Saldo final: %.2f\n", saldo);

  return 0;
}



Exercicio 3:

#include <stdio.h>

int main() {
    // Preço médio das ações
    float preco_acao1 = 24.13;
    float preco_acao2 = 11.00;
    float preco_acao3 = 38.65;

    float dividendo_acao1 = 17.00;
    float dividendo_acao2 = 35.00;
    float dividendo_acao3 = 25.00;

    float montante_total = 1000.00;

    int qtd_acao1 = montante_total / preco_acao1;
    int qtd_acao2 = montante_total / preco_acao2;
    int qtd_acao3 = montante_total / preco_acao3;

    float dy_acao1 = (dividendo_acao1 / preco_acao1) * 100;
    float dy_acao2 = (dividendo_acao2 / preco_acao2) * 100;
    float dy_acao3 = (dividendo_acao3 / preco_acao3) * 100;

    printf("Você pode comprar %d ações da Ação 1.\n", qtd_acao1);
    printf("Você pode comprar %d ações da Ação 2.\n", qtd_acao2);
    printf("Você pode comprar %d ações da Ação 3.\n", qtd_acao3);

    printf("Dividend Yield da Ação 1: %.2f%%\n", dy_acao1);
    printf("Dividend Yield da Ação 2: %.2f%%\n", dy_acao2);
    printf("Dividend Yield da Ação 3: %.2f%%\n", dy_acao3);

    return 0;
}

//prova 1 - correção

// questão 1 - C

// questão 2 - B

// questão 3 - alternativa "A" Resultado: F = 369, C = 187,22

#include <stdio.h>

int main() {
    double fahrenheit, celsius;

    // Solicita o valor em Fahrenheit
    printf("Digite a temperatura em Fahrenheit: ");
    scanf("%lf", &fahrenheit);

    // Converte para Celsius usando a fórmula com double
    celsius = (fahrenheit - 32.0) * (5.0 / 9.0);

    // Imprime o resultado
    printf("Temperatura em Celsius: %.2f\n", celsius);

    return 0;
}

// questão 3 - alternativa "B" Resultado: F 369, C = 0

#include <stdio.h>

int main() {
    int fahrenheit, celsius;

    // Solicita o valor em Fahrenheit
    printf("Digite a temperatura em Fahrenheit: ");
    scanf("%d", &fahrenheit);

    // Converte para Celsius usando a fórmula com int (note a perda de precisão)
    celsius = (fahrenheit - 32) * (5 / 9);

    // Imprime o resultado
    printf("Temperatura em Celsius: %d\n", celsius);

    return 0;
}

// questão 4

#include <stdio.h>

int main() {
    int temperatura;

    // Solicita a temperatura atual em graus Celsius
    printf("Digite a temperatura atual em graus Celsius: ");
    scanf("%d", &temperatura);

    // Avalia a temperatura e fornece a previsão
    if (temperatura <= 0) {
        printf("Geleira - Temperatura muito fria!\n");
    } 
    else if (temperatura >= 1 && temperatura <= 15) {
        printf("Frio - Pode precisar de um casaco!\n");
    } 
    else if (temperatura >= 16 && temperatura <= 25) {
        printf("Agradável - Tempo bom para sair!\n");
    } 
    else if (temperatura >= 26 && temperatura <= 35) {
        printf("Quente - Ótimo para um dia de praia!\n");
    } 
    else {
        printf("Muito quente - Mantenha-se hidratado!\n");
    }

    return 0;
}

// questão 5

#include <stdio.h>

int main() {
    int temperatura;

    // Solicita a temperatura atual do depósito
    printf("Digite a temperatura atual do depósito em graus Celsius: ");
    scanf("%d", &temperatura);

    // Classifica o nível de risco com base na temperatura
    if (temperatura < -10) {
        printf("Risco Baixo - Armazenamento ideal para alimentos congelados.\n");
    } 
    else if (temperatura >= -10 && temperatura <= 0) {
        printf("Risco Moderado - Condições aceitáveis para armazenamento refrigerado.\n");
    } 
    else if ((temperatura >= 1 && temperatura <= 10) || temperatura == 15) {
        printf("Risco Elevado - Monitore a temperatura.\n");
    } 
    else if (temperatura > 10 && temperatura != 15) {
        printf("Risco Crítico - Ação Imediata Necessária!\n");
    }

    return 0;
}
