<!-- @format -->

# ContaTerminal

Este programa Java solicita informações sobre uma conta bancária ao usuário e exibe uma mensagem de agradecimento com base nos dados inseridos.

## Atributos da Conta Bancária:

| Atributo     | Tipo    | Exemplo         |
| ------------ | ------- | --------------- |
| Numero       | Inteiro | 1212            |
| Agencia      | Texto   | 321-1           |
| Nome Cliente | Texto   | Jose de Almeida |
| Saldo        | Decimal | 100.48          |

## Funcionamento do Programa:

1. **Entrada de Dados:**
   O programa utiliza a classe `Scanner` para permitir a entrada de dados via terminal. Ele solicita ao usuário que insira o número da agência, o número da conta, o nome do cliente e o saldo da conta.

2. **Método Concatenação:**
   Após a inserção de todas as informações, o programa utiliza o método `concat` para formar uma mensagem de agradecimento personalizada. Os campos entre `[ ]` na mensagem são substituídos pelas informações inseridas pelos usuários.

## Código Java:

```java
import java.util.Scanner;

public class ContaTerminal {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Solicita ao usuário que insira o número da Agência
        System.out.println("Por favor, digite o número da Agência:");
        String agencia = scanner.nextLine();

        // Solicita ao usuário que insira o número da Conta
        System.out.println("Por favor, digite o número da Conta:");
        int numero = scanner.nextInt();
        scanner.nextLine(); // Limpa o buffer do scanner

        // Solicita ao usuário que insira o nome do Cliente
        System.out.println("Por favor, digite o nome do Cliente:");
        String nomeCliente = scanner.nextLine();

        // Solicita ao usuário que insira o saldo
        System.out.println("Por favor, digite o saldo:");
        double saldo = scanner.nextDouble();

        scanner.close(); // Fechar o scanner

        // Exibe a mensagem com os dados fornecidos pelo usuário
        System.out.println("Olá " + nomeCliente + ", obrigado por criar uma conta em nosso banco, sua agência é "
                + agencia + ", conta " + numero + " e seu saldo " + saldo + " já está disponível para saque.");
    }
}
```
