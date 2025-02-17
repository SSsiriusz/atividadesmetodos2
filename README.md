import java.util.Scanner;

public class MetodoPrincipal {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        
        System.out.println("Insira três números:");
        int num1 = scanner.nextInt();
        int num2 = scanner.nextInt();
        int num3 = scanner.nextInt();
        
        
        Calculadora calculadora = new Calculadora(num1, num2, num3);
        int maiorNumero = calculadora.max();

        
        Exibidor exibidor = new Exibidor(maiorNumero);
        exibidor.exibirResultado();

       
        scanner.close();
    }
}


class Calculadora {
    private int num1;
    private int num2;
    private int num3;

    
    public Calculadora(int num1, int num2, int num3) {
        this.num1 = num1;
        this.num2 = num2;
        this.num3 = num3;
    }

    
    public int max() {
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

    
    @Override
    public String toString() {
        return "Calculadora [num1=" + num1 + ", num2=" + num2 + ", num3=" + num3 + "]";
    }
}

// Classe Exibidor
class Exibidor {
    private int maiorNumero;

    
    public Exibidor(int maiorNumero) {
        this.maiorNumero = maiorNumero;
    }

    
    public void exibirResultado() {
        System.out.println("O maior número é: " + maiorNumero);
    }

    
    @Override
    public String toString() {
        return "Exibidor [maiorNumero=" + maiorNumero + "]";
    }
}

