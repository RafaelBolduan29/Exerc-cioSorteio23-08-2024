# Exerc-cioSorteio23-08-2024

// Aluno: Rafael Bolduan
// Data: 23/08/2024        Turma: 1º 03

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    int numeroSecreto = (int) (Math.random() * 101);
    Scanner sc = new Scanner(System.in);
    int tentativas = 0;

    while (true) {
      System.out.println("------------------------------------------------------");
      System.out.println("Adivinhe um número que está entre os números 0 e 100:");
      System.out.println("------------------------------------------------------");

      int op = sc.nextInt();
      tentativas++;
      System.out.println("------------------------------------------------------");

      if (op < 0) {
        System.out.println("Erro: O número deve ser maior ou igual a 0.");
      } else if (op > 100) {
        System.out.println("Erro: O número deve ser menor ou igual a 100.");
      } else if (op == numeroSecreto) {
        System.out.println("Acertou o número! Você tentou " + tentativas + " vezes.");
        break;
      } else if (op > numeroSecreto) {
        System.out.println("O número secreto é menor.");
      } else {
        System.out.println("O número secreto é maior.");
      }

      System.out.println("------------------------------------------------------");
    }

    sc.close();
  }
}
