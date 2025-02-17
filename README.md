# atividadesmetodos2
import java.util.Scanner;

num1

public class MetodoPrincipal {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Solicita a entrada dos três números
        System.out.println("Insira três números:");
        int num1 = scanner.nextInt();
        int num2 = scanner.nextInt();
        int num3 = scanner.nextInt();

        // Cria a instância da classe Calculadora para fazer o cálculo
        Calculadora calculadora = new Calculadora();
        int maiorNumero = calculadora.max(num1, num2, num3);

        // Cria a instância da classe Exibidor para mostrar o resultado
        Exibidor exibidor = new Exibidor();
        exibidor.exibirResultado(maiorNumero);

        // Fecha o scanner
        scanner.close();
    }
}
class Calculadora {
    // Método para calcular o maior número entre três valores
    public int max(int num1, int num2, int num3) {
        int maxNumber;
        if (num1 > num2 && num1 > num3) {
            maxNumber = num1;
        } else if (num2 > num3) {
            maxNumber = num2;
        } else {
            maxNumber = num3;
        }
        return maxNumber;
    }

}

// Classe para exibir resultados
class Exibidor {
    // Método para exibir o resultado
    public void exibirResultado(int value) {
        System.out.println("O maior número é: " + value);
    }
}

num2

