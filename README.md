# Calculadora
import java.util.Scanner;

public class CalculadoraSimples {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        System.out.println("Calculadora Simples");
        System.out.print("Digite o primeiro número: ");
        double num1 = input.nextDouble();
        
        System.out.print("Digite o operador (+, -, *, /): ");
        char operador = input.next().charAt(0);
        
        System.out.print("Digite o segundo número: ");
        double num2 = input.nextDouble();
        
        double resultado = 0.0;
        
        switch (operador) {
            case '+':
                resultado = num1 + num2;
                break;
            case '-':
                resultado = num1 - num2;
                break;
            case '*':
                resultado = num1 * num2;
                break;
            case '/':
                if (num2 != 0) {
                    resultado = num1 / num2;
                } else {
                    System.out.println("Erro: Divisão por zero!");
                    System.exit(1);
                }
                break;
            default:
                System.out.println("Operador inválido!");
                System.exit(1);
        }
        
        System.out.println("Resultado: " + resultado);
    }
}

