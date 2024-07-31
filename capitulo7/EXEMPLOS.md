### Use exceções em vez de retornar códigos

```java

public class Calculator {
    public int divide(int numerator, int denominator) {
        if (denominator == 0) {
            throw new IllegalArgumentException("Denominator cannot be zero");
        }
        return numerator / denominator;
    }
}

```

###  Crie primeiro sua estrutura try-catch-finally

```java

public class FileManager {
    public void readFile(String filePath) {
        try {
            // Código para ler o arquivo
        } catch (IOException e) {
            // Tratamento do erro
        } finally {
            // Código de limpeza
        }
    }
}

```

### Use exceções não verificadas

```java

public class UserService {
    public User findUserById(int id) {
        if (id <= 0) {
            throw new IllegalArgumentException("ID must be positive");
        }
        // Lógica para encontrar o usuário
    }
}

```

### Forneça exceções com contexto

```java

public class OrderService {
    public void processOrder(int orderId) {
        if (orderId <= 0) {
            throw new IllegalArgumentException("Order ID must be positive: " + orderId);
        }
        // Lógica para processar o pedido
    }
}

```
### Defina as classes de exceções segundo as necessidades do chamador

```java

public class DataAccessException extends RuntimeException {
    public DataAccessException(String message, Throwable cause) {
        super(message, cause);
    }
}

public class UserRepository {
    public User findUserById(int id) {
        try {
            // Lógica para encontrar o usuário
        } catch (SQLException e) {
            throw new DataAccessException("Error finding user by ID: " + id, e);
        }
    }
}

```

### Defina o fluxo normal

```java

public class PaymentProcessor {
    public void processPayment(Payment payment) {
        if (payment == null) {
            throw new IllegalArgumentException("Payment cannot be null");
        }
        // Lógica normal de processamento de pagamento
    }
}

```

### Não retorne null

```java

public class UserService {
    public Optional<User> findUserById(int id) {
        // Lógica para encontrar o usuário
        return Optional.ofNullable(user);
    }
}

```

### Não passe null para os métodos

```java

public class UserService {
    public void updateUser(User user) {
        if (user == null) {
            throw new IllegalArgumentException("User cannot be null");
        }
        // Lógica para atualizar o usuário
    }
}

```

Esses exemplos destacam a importância de tratar erros de forma elegante e robusta, garantindo que o código seja fácil de manter e entender. A boa prática de tratamento de erros contribui significativamente para a qualidade geral do software.