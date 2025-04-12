# esafio-sobre-la-os-de-repeti-o-05

public class ReajusteSalarial {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        System.out.println("=== Reajuste Salarial ===");
        System.out.print("Informe o salário atual do colaborador: R$ ");
        double salarioAtual = scanner.nextDouble();

        double percentual = 0;

        if (salarioAtual <= 280.00) {
            percentual = 20;
        } else if (salarioAtual <= 700.00) {
            percentual = 15;
        } else if (salarioAtual <= 1500.00) {
            percentual = 10;
        } else {
            percentual = 5;
        }

        double aumento = salarioAtual * (percentual / 100);
        double novoSalario = salarioAtual + aumento;

        double inflacao = 3.8;
        double aumentoReal = aumento - (salarioAtual * (inflacao / 100));

        System.out.println("\n=== Resultado do Reajuste ===");
        System.out.printf("1. Salário antes do reajuste: R$ %.2f\n", salarioAtual);
        System.out.printf("2. Percentual de aumento aplicado: %.0f%%\n", percentual);
        System.out.printf("3. Valor do aumento: R$ %.2f\n", aumento);
        System.out.printf("4. Novo salário: R$ %.2f\n", novoSalario);
        System.out.printf("5. Aumento real (descontando inflação): R$ %.2f\n", aumentoReal);

        scanner.close();
    }
}
