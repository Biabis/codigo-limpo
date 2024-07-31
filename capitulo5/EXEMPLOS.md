## 1. O objetivo da formatação

#### Correto:

```java

// Código bem formatado, fácil de ler e entender
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}


```

#### Errado:

```java

// Código mal formatado, difícil de ler
public class Main{public static void main(String[]args){System.out.println("Hello, World!");}}



```

## 2. Formatação vertical

#### Correto:

```java

public class Main {
    
    private int value;
    
    public Main(int value) {
        this.value = value;
    }

    public void displayValue() {
        System.out.println("Value: " + value);
    }
}

```

#### Errado:

```java

public class Main { private int value; public Main(int value) { this.value = value; } public void displayValue() { System.out.println("Value: " + value); } }


```

## 3. Espaçamento vertical entre conceitos

#### Correto:

```java

public class Main {
    
    private int value;
    
    public Main(int value) {
        this.value = value;
    }
    
    public void displayValue() {
        System.out.println("Value: " + value);
    }
    
    public static void main(String[] args) {
        Main main = new Main(42);
        main.displayValue();
    }
}

```

#### Errado: 

```java

public class Main {
    private int value;
    public Main(int value) {
        this.value = value;
    }
    public void displayValue() {
        System.out.println("Value: " + value);
    }
    public static void main(String[] args) {
        Main main = new Main(42);
        main.displayValue();
    }
}

```

## 4. Continuidade vertical

#### Correto:

```java

public class Main {
    
    private int value;
    private String name;
    
    public Main(int value, String name) {
        this.value = value;
        this.name = name;
    }
}

```

#### Errado:

```java

public class Main {
    private int value;
    public Main(int value, String name) {
        this.value = value;
        this.name = name;
    }
    private String name;
}

```

## 5. Distância vertical

#### Correto:

```java

public class Main {
    
    private int value;
    
    public Main(int value) {
        this.value = value;
    }
    
    public void displayValue() {
        System.out.println("Value: " + value);
    }
}

```

#### Errado:

```java

public class Main {
    private int value;
    public Main(int value) {
        this.value = value;
    }
    public void displayValue() {
        System.out.println("Value: " + value);
    }
}

```

## 6. Declaração de variáveis

##### Correto:

```java

public class Main {
    public static void main(String[] args) {
        int value = 42;
        System.out.println("Value: " + value);
    }
}

```
#### Errado:

```java

public class Main {
    int value;
    public static void main(String[] args) {
        value = 42;
        System.out.println("Value: " + value);
    }
}

```

## 7. Instanciação de variáveis

#### Correto: 

```java

public class Main {
    
    private int value = 42;
    
    public static void main(String[] args) {
        Main main = new Main();
        System.out.println("Value: " + main.value);
    }
}

```

#### Errado:

```java

public class Main {
    
    private int value;
    
    public static void main(String[] args) {
        Main main = new Main();
        main.value = 42;
        System.out.println("Value: " + main.value);
    }
}

```

## 8. Funções dependentes

#### Correto: 

```java

public class Main {
    
    public static void main(String[] args) {
        Main main = new Main();
        main.start();
    }
    
    public void start() {
        printMessage();
    }
    
    private void printMessage() {
        System.out.println("Hello, World!");
    }
}

```

#### Errado:


```java

public class Main {
    
    private void printMessage() {
        System.out.println("Hello, World!");
    }
    
    public void start() {
        printMessage();
    }
    
    public static void main(String[] args) {
        Main main = new Main();
        main.start();
    }
}

```

## 9. Ordenação vertical

#### Correto:

```java

public class Main {
    
    private void printMessage() {
        System.out.println("Hello, World!");
    }
    
    public void start() {
        printMessage();
    }
    
    public static void main(String[] args) {
        Main main = new Main();
        main.start();
    }
}

```

#### Errado:

```java

public class Main {
    
    public static void main(String[] args) {
        Main main = new Main();
        main.start();
    }
    
    public void start() {
        printMessage();
    }
    
    private void printMessage() {
        System.out.println("Hello, World!");
    }
}

```

## 10. Formatação horizontal

#### Certo: 

```java

public class Main {
    public static void main(String[] args) {
        int value = 42;
        System.out.println("Value: " + value);
    }
}

```

#### Errado: 

```java

public class Main {
    public static void main(String[] args) { int value = 42; System.out.println("Value: " + value); }
}

```

## 11. Espaçamento e continuidade horizontal

#### Certo: 

```java

public class Main {
    public static void main(String[] args) {
        int value = 42;
        System.out.println("Value: " + value);
    }
}

```

#### Errado:

```java

public class Main {
    public static void main(String[] args) {
        int value=42;
        System.out.println("Value:"+value);
    }
}

```

Esses exemplos destacam a importância de uma boa formatação para garantir que o código seja legível e fácil de entender. Uma formatação consistente e cuidadosa ajuda a transmitir profissionalismo e atenção aos detalhes.
