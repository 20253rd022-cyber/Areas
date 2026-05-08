 java.util.Scanner;

public class Main {

    // Método para calcular el área del círculo
    public static double calcularAreaCirculo(double radio) {
        return Math.PI * radio * radio;
    }

    // Método para calcular el área del triángulo
    public static double calcularAreaTriangulo(double base, double altura) {
        return (base * altura) / 2;
    }

    // Método para calcular el área del rectángulo
    public static double calcularAreaRectangulo(double base, double altura) {
        return base * altura;
    }

    // Método opcional para calcular el área del cuadrado
    public static double calcularAreaCuadrado(double lado) {
        return lado * lado;
    }

    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
        int opcion;

        do {
            // Menú principal
            System.out.println("===== CALCULADORA DE ÁREAS =====");
            System.out.println("1. Área de un círculo");
            System.out.println("2. Área de un triángulo");
            System.out.println("3. Área de un rectángulo");
            System.out.println("4. Área de un cuadrado");
            System.out.println("5. Salir");
            System.out.print("Elige una opción: ");
            opcion = entrada.nextInt();

            switch (opcion) {
                case 1:
                    System.out.print("Ingresa el radio del círculo: ");
                    double radio = entrada.nextDouble();
                    // Llamamos al método correspondiente
                    double areaCirculo = calcularAreaCirculo(radio);
                    System.out.printf("El área del círculo es: %.2f unidades²%n%n", areaCirculo);
                    break;

                case 2:
                    System.out.print("Ingresa la base del triángulo: ");
                    double baseTri = entrada.nextDouble();
                    System.out.print("Ingresa la altura del triángulo: ");
                    double alturaTri = entrada.nextDouble();
                    // Llamamos al método correspondiente
                    double areaTriangulo = calcularAreaTriangulo(baseTri, alturaTri);
                    System.out.printf("El área del triángulo es: %.2f unidades²%n%n", areaTriangulo);
                    break;

                case 3:
                    System.out.print("Ingresa la base del rectángulo: ");
                    double baseRec = entrada.nextDouble();
                    System.out.print("Ingresa la altura del rectángulo: ");
                    double alturaRec = entrada.nextDouble();
                    // Llamamos al método correspondiente
                    double areaRectangulo = calcularAreaRectangulo(baseRec, alturaRec);
                    System.out.printf("El área del rectángulo es: %.2f unidades²%n%n", areaRectangulo);
                    break;

                case 4:
                    System.out.print("Ingresa el lado del cuadrado: ");
                    double lado = entrada.nextDouble();
                    // Llamamos al método correspondiente
                    double areaCuadrado = calcularAreaCuadrado(lado);
                    System.out.printf("El área del cuadrado es: %.2f unidades²%n%n", areaCuadrado);
                    break;

                case 5:
                    System.out.println("Programa finalizado. ¡Adiós!");
                    break;

                default:
                    System.out.println("Opción no válida, intenta de nuevo.\n");
            }

        } while (opcion != 5);

        entrada.close();
    }
}
 Areas
