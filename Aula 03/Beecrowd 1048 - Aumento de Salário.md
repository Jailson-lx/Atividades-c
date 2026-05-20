%%writefile atividade.c
#include <stdio.h>

int main() {
  double salario, ajuste, Nsalario;
  int porcentagem;

  scanf("%lf", &salario);

  if (salario <= 400.00) {
    porcentagem = 15;
  }
  else if (salario <= 800.00) {
    porcentagem = 12;
  }
  else if (salario <= 1200.00) {
    porcentagem = 10;
  }
  else if (salario <= 2000.00) {
    porcentagem = 7;
  }
  else {
    porcentagem = 4;
  }

  ajuste = salario * (porcentagem / 100.0);
  Nsalario = salario + ajuste;

  printf("Novo salario: %.2f\n", Nsalario);
  printf("Reajuste ganho: %.2f\n", ajuste);
  printf("Em percentual: %d %%\n", porcentagem);

  return 0;
  }
