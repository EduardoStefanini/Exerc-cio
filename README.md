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
