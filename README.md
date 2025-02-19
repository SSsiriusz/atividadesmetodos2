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

num2
import java.util.Scanner;

public class met2 {
    public static <Talculadora> void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        System.out.println("Insira um numero");
        int n1 = scanner.nextInt();
        System.out.println("Insira outro numero");
        int n2 = scanner.nextInt();


        talculadora talculadora = new talculadora(n1,n2);


        int resultadoSoma = talculadora.soma(n1,n2);


        exibirValores(resultadoSoma);


        scanner.close();
    }


    public static void exibirValores(int resultadoSoma) {
        System.out.println("A soma é: " + resultadoSoma);
    }
}
class talculadora {
    public int n1;
    public int n2;


    public talculadora(int n1, int n2) {
        this.n1 = n1;
        this.n2 = n2;
    }


    public int soma(int n1, int n2) {
        return n1 * n2;
    }
}

num3

import java.util.Scanner;

public class met3 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);


        System.out.println("Insira as notas do aluno.");
        int nota1 = scanner.nextInt();
        int nota2 = scanner.nextInt();


        Aluno aluno = new Aluno(nota1, nota2);


        aluno.calcularMedia();


        aluno.verificarStatus();


        System.out.println(aluno);


        scanner.close();
    }
}
class Aluno {
    private int nota1;
    private int nota2;
    private int media;
    private String status;


    public Aluno(int nota1, int nota2) {
        this.nota1 = nota1;
        this.nota2 = nota2;
    }


    public void calcularMedia() {
        this.media = (nota1 + nota2) / 2; // Corrigido a fórmula da média
    }


    public void verificarStatus() {
        if (media >= 7) {
            this.status = "Aprovado";
        } else if (media >= 5) {
            this.status = "Recuperação";
        } else {
            this.status = "Reprovado";
        }
    }



    public String toString() {
        return "Notas do Aluno: Nota 1 = " + nota1 + ", Nota 2 = " + nota2 +
                "\nMédia: " + media + "\nStatus: " + status;
    }
}

num4
  import java.util.Scanner;

public class met4 {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Solicita os números ao usuário
        System.out.println("Escreva um numero");
        int num1 = scanner.nextInt();
        System.out.println("Escreva um numero");
        int num2 = scanner.nextInt();
        System.out.println("Escreva um numero");
        int num3 = scanner.nextInt();

        
        Triangulo triangulo = new Triangulo(num1, num2, num3);

        
        int resultado = triangulo.calcularSoma();

        
        System.out.println("A área do triângulo é = " + resultado);

        
        System.out.println(triangulo.toString());

        scanner.close();
    }
}
public class Triangulo {

    private int num1;
    private int num2;
    private int num3;

    
    public Triangulo(int num1, int num2, int num3) {
        this.num1 = num1;
        this.num2 = num2;
        this.num3 = num3;
    }

    
    public int calcularSoma() {
        return num1 + num2 + num3;
    }

    
    @Override
    public String toString() {
        return "Triangulo [num1=" + num1 + ", num2=" + num2 + ", num3=" + num3 + "]";
    }
}

num5

public class met5 {

    public static void main(String[] args) {

        OperacaoMatematica opecacaomatematica = new OperacaoMatematica(100, 2 + 3);


        System.out.println(opecacaomatematica.toString());
    }
}
public class OperacaoMatematica {

    private int numerador;
    private int denominador;


    public OperacaoMatematica(int numerador, int denominador) {
        this.numerador = numerador;
        this.denominador = denominador;
    }


    public double calcularResultado() {
        return (double) numerador / denominador;
    }



    public String toString() {
        return "Cálculo: " + numerador + " / (" + denominador + ") = " + calcularResultado();
    }
}

