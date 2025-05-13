import java.util.Scanner;

public class ConversorDeMoedas {

    // Taxas de câmbio simuladas  
    static final double TAXA_USD = 5.10;  // 1 USD = 5.10 BRL
    static final double TAXA_EUR = 5.50;  // 1 EUR = 5.50 BRL

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int opcao;

        do {
            System.out.println("\n=== Conversor de Moedas ===");
            System.out.println("1. Real para Dólar");
            System.out.println("2. Real para Euro");
            System.out.println("3. Dólar para Real");
            System.out.println("4. Euro para Real");
            System.out.println("5. Sair");
            System.out.print("Escolha uma opção: ");
            opcao = scanner.nextInt();

            double valor;
            switch (opcao) {
                case 1:
                    System.out.print("Digite o valor em BRL: ");
                    valor = scanner.nextDouble();
                    System.out.printf("USD: %.2f\n", valor / TAXA_USD);
                    break;
                case 2:
                    System.out.print("Digite o valor em BRL: ");
                    valor = scanner.nextDouble();
                    System.out.printf("EUR: %.2f\n", valor / TAXA_EUR);
                    break;
                case 3:
                    System.out.print("Digite o valor em USD: ");
                    valor = scanner.nextDouble();
                    System.out.printf("BRL: %.2f\n", valor * TAXA_USD);
                    break;
                case 4:
                    System.out.print("Digite o valor em EUR: ");
                    valor = scanner.nextDouble();
                    System.out.printf("BRL: %.2f\n", valor * TAXA_EUR);
                    break;
                case 5:
                    System.out.println("Encerrando o programa...");
                    break;
                default:
                    System.out.println("Opção inválida.");
            }

        } while (opcao != 5);

        scanner.close();
    }
}
