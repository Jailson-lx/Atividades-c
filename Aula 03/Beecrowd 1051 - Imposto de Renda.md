#include <stdio.h>

int main() {
  double salario, imposto;

  scanf("%lf", &salario);

  if (salario <= 2000) {
    printf("Isento\n");
  }
  else if (salario <= 3000) {
    imposto = (salario - 2000) * 0.08;
    printf("R$ %.2f\n", imposto);
  }
  else if (salario <= 4500) {
    imposto = 80 + ((salario - 3000) * 0.18);
    printf("R$ %.2f\n", imposto);
  }
  else {
    imposto = 350 + ((salario - 4500) * 0.28);
    printf("R$ %.2f\n", imposto);
  }

  return 0;
}
