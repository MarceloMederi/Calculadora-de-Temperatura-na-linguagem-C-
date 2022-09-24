# Calculadora-de-Temperatura-na-linguagem-C-

#include <stdio.h>

int escolha;
float Celsius, Fahrenheit, Kelvin;

void Celsius_Fahrenheit() {
  printf("\nDigite a temperatura em Celsius.: ");
  scanf("%f", &Celsius);
  Fahrenheit = ((9*Celsius + 160)/5);
  printf("A temperatura em Fahrenheits = %.1f", Fahrenheit);
  printf(" °F");

}

void Celsius_Kelvin() {
  printf("\nDigite a temperatura em Celsius.: ");
  scanf("%f", &Celsius);
  Kelvin = (Celsius + 273);
  printf("A temperatura em Kelvin = %.1f", Kelvin);
  printf(" °K");

}

void Fahrenheit_Celsius() {
  printf("\nDigite a temperatura em Fahrenheits.: ");
  scanf("%f", &Fahrenheit);
  Celsius = ((5*(Fahrenheit - 32))/9);
  printf("A temperatura em Celsius = %.1f", Celsius);
  printf(" °C");

}

void Fahrenheit_Kelvin() {
  printf("\nDigite a temperatura em Fahrenheits.: ");
  scanf("%f", &Fahrenheit);
  Kelvin = ((5*Fahrenheit + 2297)/9);
  printf("A temperatura em Kelvin = %.1f", Kelvin);
  printf(" °K");

}

void Kelvin_Celsius() {
  printf("\nDigite a temperatura em Kelvin.: ");
  scanf("%f", &Kelvin);
  Celsius = (Kelvin - 273.15);
  printf("A temperatura em Celsius = %.1f", Celsius);
  printf(" °C");

}

void Kelvin_Fahrenheit() {
  printf("\nDigite a temperatura em Kelvin.: ");
  scanf("%f", &Kelvin);
  Fahrenheit = ((Kelvin - 273.15) * 9) / 5 + 32;
  printf("A temperatura em Fahrenheits = %.1f", Fahrenheit);
  printf(" °C");

}

int main() {
  printf("CALCULADORA DE TEMPERATURA");
  printf("\n1-Celsius para Fahrenheits\n2-Celsius para Kelvin\n3-Fahrenheits para Celsius\n4-Fahrenheits para Kelvin\n5-Kelvin para Celsius\n6-Kelvin para Fahrenheits\n7-Sair\n\nOpcao: ");
  scanf("%d", &escolha);
  switch (escolha) {
    case 1:
      Celsius_Fahrenheit();
      break;

    case 2:
      Celsius_Kelvin();
      break;

    case 3:
      Fahrenheit_Celsius();
      break;

    case 4:
      Fahrenheit_Kelvin();
      break;

    case 5:
      Kelvin_Celsius();
      break;

    case 6:
      Kelvin_Fahrenheit();
      break;

    case 7:
      printf("O programa será encerrado");
      break;

    default:
      printf("Opção Invalida! Escolha dentre as opções apresentada.");
      break;

  }

  return(0);

}
