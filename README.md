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

// Tarefa 4 : Lista 2

Exercicio 1) 
#include <stdio.h>

int main() {
  float temperatura;
  
  printf("Digite a temperatura: ");
  scanf("%f", &temperatura);

  while (temperatura < 20 || temperatura > 25) {
    printf("Alerta! Temperatura fora da faixa (20°C - 25°C).\n");
    printf("Digite a temperatura: ");
    scanf("%f", &temperatura);
  }
  printf("Temperatura dentro da faixa.\n");

  return 0;
}


Exercicio 2)
#include <stdio.h>

int main() {
  int nivelCombustivel;

  printf("Digite o nível de combustível: ");
  scanf("%d", &nivelCombustivel);

  while (nivelCombustivel < 15) {
    printf("O nível de combustível está abaixo de 15%%. Por favor, abasteça!\n");
    printf("Digite o nível de combustível: ");
    scanf("%d", &nivelCombustivel);
  }

  printf("O nível de combustível está acima de 15%%. Seguro para dirigir.\n");

  return 0;
}


Exercicio 3)
#include <stdio.h>

int main() {
  int passos = 0;
  int totalPassos = 0;

  printf("Bem-vindo ao contador de passos!\n");
  printf("Sua meta diária é de 10.000 passos.\n");

  while (totalPassos < 10000) {
    printf("Digite o número de passos dados desde a última atualização: ");
    scanf("%d", &passos);

    totalPassos += passos;

    printf("Total de passos: %d\n", totalPassos);

    if (totalPassos >= 10000) {
      printf("Parabéns! Você atingiu sua meta diária!\n");
    }
  }

  return 0;
}


Exercicio 4)
#include <stdio.h>

int main() {
  float deposito;

  printf("Digite o valor do depósito inicial: R$ ");
  scanf("%f", &deposito);

  while (deposito < 500.00) {
    printf("Erro: O valor mínimo de depósito é R$ 500.00.\n");
    printf("Digite um novo valor de depósito: R$ ");
    scanf("%f", &deposito);
  }

  printf("Depósito aceito!\n");

  return 0;
}


Desafio)
#include <stdio.h>
#include <math.h>

void calcular_media_e_desvio(float precos[], int n, float *media, float *desvio_padrao) {
    float soma = 0, soma_variancia = 0;

    // Calcula a soma para a média
    for (int i = 0; i < n; i++) {
        soma += precos[i];
    }
    *media = soma / n;

    // Calcula a soma das variâncias para o desvio padrão
    for (int i = 0; i < n; i++) {
        soma_variancia += pow(precos[i] - *media, 2);
    }
    *desvio_padrao = sqrt(soma_variancia / n);
}

int main() {
    int dias;
    char opcao;

    do {
        printf("Quantos dias deseja analisar? ");
        scanf("%d", &dias);

        if (dias <= 0) {
            printf("Por favor, insira um número positivo de dias.\n");
            continue;
        }

        float precos[dias];

        // Coletar preços
        for (int i = 0; i < dias; i++) {
            printf("Informe o preço da ação no dia %d: ", i + 1);
            scanf("%f", &precos[i]);
        }

        float media, desvio_padrao;
        calcular_media_e_desvio(precos, dias, &media, &desvio_padrao);

        // Exibe resultados
        printf("\nMédia dos preços: %.2f\n", media);
        printf("Desvio padrão: %.2f\n", desvio_padrao);

        // Verifica estabilidade
        if (desvio_padrao < (0.05 * media)) {
            printf("O desempenho das ações é considerado **estável**.\n");
        } else {
            printf("O desempenho das ações é considerado **volátil**.\n");
        }

        // Pergunta se deseja continuar
        printf("\nDeseja analisar novos dados? (s/n): ");
        scanf(" %c", &opcao);

    } while (opcao == 's' || opcao == 'S');

    printf("Encerrando o programa.\n");
    return 0;
}
Exercicios 2.
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

// Função para o Controle de Movimento
void controleMovimento() {
    int x = 0, y = 0; // Posição inicial
    char comando[10];

    printf("\nRobô no espaço 10x10. Posição inicial: (%d, %d)\n", x, y);

    while (1) {
        printf("Comando (frente, tras, esquerda, direita ou sair): ");
        scanf("%s", comando);

        if (strcmp(comando, "frente") == 0 && y < 9) y++;
        else if (strcmp(comando, "tras") == 0 && y > 0) y--;
        else if (strcmp(comando, "esquerda") == 0 && x > 0) x--;
        else if (strcmp(comando, "direita") == 0 && x < 9) x++;
        else if (strcmp(comando, "sair") == 0) break;
        else printf("Comando inválido ou fora do espaço.\n");

        printf("Posição atual: (%d, %d)\n", x, y);
    }
}

// Função para a Leitura de Sensores
void leituraSensores() {
    float distancia;
    srand(time(0)); // Geração de números aleatórios

    printf("\nIniciando leitura do sensor de distância...\n");
    while (1) {
        distancia = (rand() % 1000) / 10.0; // Gera distância aleatória entre 0 e 100 cm
        printf("Distância medida: %.2f cm\n", distancia);

        if (distancia < 10.0) {
            printf("Distância menor que 10 cm detectada. Encerrando.\n");
            break;
        }

        char opcao;
        printf("Continuar leitura? (s/n): ");
        scanf(" %c", &opcao);
        if (opcao == 'n') break;
    }
}

// Função para o Controle de Atuação
void controleAtuacao() {
    int opcao;

    printf("\nControle de Atuação do Robô:\n");
    while (1) {
        printf("1. Ligar lâmpada\n");
        printf("2. Tocar som\n");
        printf("3. Mover braço\n");
        printf("4. Sair\n");
        printf("Escolha uma ação: ");
        scanf("%d", &opcao);

        switch (opcao) {
            case 1: printf("Lâmpada ligada!\n"); break;
            case 2: printf("Som tocado!\n"); break;
            case 3: printf("Braço movido!\n"); break;
            case 4: return;
            default: printf("Opção inválida.\n");
        }
    }
}

// Função para o Monitoramento de Bateria
void monitoramentoBateria() {
    int bateria;

    printf("\nMonitoramento da Bateria:\n");
    while (1) {
        printf("Informe o nível atual da bateria (0-100): ");
        scanf("%d", &bateria);

        if (bateria < 0 || bateria > 100) {
            printf("Nível de bateria inválido.\n");
            continue;
        }

        if (bateria <= 20) {
            printf("Alerta: Bateria baixa! Conecte o robô ao carregador.\n");
        } else {
            printf("Bateria OK.\n");
            break;
        }
    }
}

// Função para a Navegação Autônoma
void navegacaoAutonoma() {
    int x = 0, y = 0;
    char comando[10];

    printf("\nRobô no grid 5x5. Posição inicial: (%d, %d)\n", x, y);

    while (1) {
        printf("Comando (cima, baixo, esquerda, direita ou sair): ");
        scanf("%s", comando);

        if (strcmp(comando, "cima") == 0 && y < 4) y++;
        else if (strcmp(comando, "baixo") == 0 && y > 0) y--;
        else if (strcmp(comando, "esquerda") == 0 && x > 0) x--;
        else if (strcmp(comando, "direita") == 0 && x < 4) x++;
        else if (strcmp(comando, "sair") == 0) break;
        else printf("Comando inválido ou fora do grid.\n");

        printf("Posição atual: (%d, %d)\n", x, y);
    }
}

// Função principal com menu
int main() {
    int opcao;

    do {
        printf("\nMenu Principal:\n");
        printf("1. Controle de Movimento\n");
        printf("2. Leitura de Sensores de Distância\n");
        printf("3. Controle de Atuação\n");
        printf("4. Monitoramento de Bateria\n");
        printf("5. Navegação Autônoma\n");
        printf("6. Sair\n");
        printf("Escolha uma funcionalidade: ");
        scanf("%d", &opcao);

        switch (opcao) {
            case 1: controleMovimento(); break;
            case 2: leituraSensores(); break;
            case 3: controleAtuacao(); break;
            case 4: monitoramentoBateria(); break;
            case 5: navegacaoAutonoma(); break;
            case 6: printf("Encerrando o programa.\n"); break;
            default: printf("Opção inválida.\n");
        }
    } while (opcao != 6);

    return 0;
}


Exercicios 3.
1) int cameraData[10];



2) Lê um valor analógico do pino A1 usando a função analogRead(). Esse valor estará entre 0 e 1023 (valores padrão para leitura analógica no Arduino). Armazena o valor lido no índice 3 do vetor cameraData. Assim, o quarto elemento do vetor (índice começa em 0) conterá o valor analógico lido do pino A1.

3) float temperaturas[ ] = {25.5, 26.0, 24.8, 27.3, 26.5};

4) for (int i = 0; i < 4; i++) {
    Serial.println(ledPins[i]);
}

5) int ledPins[] = {2, 3, 4, 5}; // Vetor de pinos
void setup() {
    Serial.begin(9600); // Inicializa o monitor serial
}

void loop() {
    for (int i = 0; i < 4; i++) {
        Serial.println(ledPins[i]); // Imprime os valores do vetor
    }
    delay(1000); // Aguarda 1 segundo
}

6) int randomValues[5];

void setup() {
    randomSeed(analogRead(0)); // Inicializa o gerador de números aleatórios
    for (int i = 0; i < 5; i++) {
        randomValues[i] = random(1, 101); // Gera valores aleatórios entre 1 e 100
    }
}

void loop() {
    // Opcional: exibir os valores no monitor serial
}

7) for (int i = 0; i < tamanhoVetor; i++) {
    if (sensorReadings[i] == 150) {
        break;
    }
}

8) int sensorData[] = {10, 20, 30, 40, 50};
int tamanho = sizeof(sensorData) / sizeof(sensorData[0]);

Serial.println(tamanho); // Exibe: 5


Exercicio 4
a)A primeira linha da matriz, {22, 25, 23, 21, 24}, representa as temperaturas medidas em graus Celsius em cinco momentos diferentes no primeiro local de monitoramento.
b)Os valores de umidade do solo no segundo local são: {45, 38, 42, 40, 37}. A média é calculada assim: media = soma valores/ numero de valores. Portanto, a média da umidade do solo é 40.4%.
c)Os valores de CO2 no terceiro local são: {400, 380, 420, 410, 390}. O maior valor é 420 ppm, que ocorre no 3º momento (índice 2).
d)int ambientData[3][5] = {
    {22, 25, 23, 21, 24},  // Temperaturas (em °C)
    {45, 38, 42, 40, 37},  // Umidade do solo (em %)
    {400, 380, 420, 410, 390} // Concentração de CO2 (em ppm)
};

void setup() {
    Serial.begin(9600); // Inicializa a comunicação serial

    int totalLocais = 3;
    int totalLeituras = 5;
    int somaTemperaturas = 0;

    for (int i = 0; i < totalLocais; i++) {
        for (int j = 0; j < totalLeituras; j++) {
            somaTemperaturas += ambientData[0][j]; // Considera apenas a linha de temperatura (linha 0)
        }
    }

    // Calcula a média
    float mediaTemperaturas = somaTemperaturas / float(totalLeituras);
    Serial.print("Média de temperatura: ");
    Serial.println(mediaTemperaturas); // Exibe a média
}

void loop() {
    // Não é necessário repetir o cálculo, então loop vazio
}
