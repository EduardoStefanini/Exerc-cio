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
