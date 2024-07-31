# Comentários bons

```java

/**
 * © 2024 Nome da Empresa. Todos os direitos reservados.
 * Este código é propriedade exclusiva da Nome da Empresa.
 */
public class LegalExample {
    // Código da classe
}

```

- Comentários de representação legal (como de direitos autorais)

```java

/**
 * Classe responsável por operações de contas bancárias.
 * 
 * @author Autor
 * @version 1.0
 */
public class BankAccount {

    private double balance;

    /**
     * Adiciona uma quantia ao saldo da conta.
     *
     * @param amount A quantia a ser adicionada
     */
    public void deposit(double amount) {
        balance += amount;
    }

    /**
     * Retira uma quantia do saldo da conta.
     *
     * @param amount A quantia a ser retirada
     * @throws IllegalArgumentException se a quantia for maior que o saldo
     */
    public void withdraw(double amount) {
        if (amount > balance) {
            throw new IllegalArgumentException("Saldo insuficiente");
        }
        balance -= amount;
    }

    /**
     * Retorna o saldo atual da conta.
     *
     * @return O saldo atual
     */
    public double getBalance() {
        return balance;
    }
}

```
- Javadocs em API públicas


# Comentários ruins

```java

public class Calculator {

    /**
     * Este método adiciona dois números.
     */
    public int add(int a, int b) {
        return a + b; // Soma a e b
    }

    /**
     * Este método subtrai dois números.
     */
    public int subtract(int a, int b) {
        return a - b; // Subtrai b de a
    }
}

```
- Comentários que explicam o óbvio

```java

public class ComplexCalculation {

    public void performComplexCalculation() {
        int x = 10;
        int y = 20;

        // Se x for maior que y, inverta-os
        if (x > y) {
            int temp = x;
            x = y;
            y = temp;
        }

        // Realiza alguma operação complexa com x e y
        int result = x * y + x - y / x * y;
        System.out.println(result);
    }
}

```
- Comentários que tentam compensar código confuso


## Explicação

#### Comentários bons: 

São aqueles necessários e que agregam valor, como representações legais e documentação de API pública.

#### Comentários ruins: 

São aqueles que explicam o óbvio ou tentam compensar a falta de clareza do código. Eles devem ser evitados, preferindo sempre escrever um código mais claro e autoexplicativo.
