## Objetos e Estrutura de Dados

### Métodos de Acesso

#### Correto: 

```java

public class Person {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public void celebrateBirthday() {
        this.age++;
    }

    public String getName() {
        return name;
    }
}

```

#### Errado:

```java

public class Person {
    public String name;
    public int age;

    public void celebrateBirthday() {
        this.age++;
    }
}

```

## A lei de Demeter

#### Correto: 

```java

public class Engine {
    public void start() {
        // código para iniciar o motor
    }
}

public class Car {
    private Engine engine;

    public Car() {
        this.engine = new Engine();
    }

    public void startCar() {
        engine.start();
    }
}

public class Driver {
    public void drive() {
        Car car = new Car();
        car.startCar();
    }
}

```

#### Errado:

```java

public class Engine {
    public void start() {
        // código para iniciar o motor
    }
}

public class Car {
    public Engine engine;

    public Car() {
        this.engine = new Engine();
    }
}

public class Driver {
    public void drive() {
        Car car = new Car();
        car.engine.start();
    }
}

```

## Carrinho de trem

#### Correto: 

```java

public class Address {
    private String street;

    public String getStreet() {
        return street;
    }
}

public class Customer {
    private Address address;

    public Address getAddress() {
        return address;
    }
}

public class Order {
    private Customer customer;

    public Customer getCustomer() {
        return customer;
    }
}

public class Main {
    public static void main(String[] args) {
        Order order = new Order();
        Address address = order.getCustomer().getAddress();
        String street = address.getStreet();
    }
}

```

#### Errado:

```java

public class Main {
    public static void main(String[] args) {
        Order order = new Order();
        String street = order.getCustomer().getAddress().getStreet();
    }
}

```

## Híbridos

#### Correto:

```java

public class Rectangle {
    private int width;
    private int height;

    public Rectangle(int width, int height) {
        this.width = width;
        this.height = height;
    }

    public int getWidth() {
        return width;
    }

    public int getHeight() {
        return height;
    }

    public int calculateArea() {
        return width * height;
    }
}

```

#### Errado:

```java

public class Rectangle {
    public int width;
    public int height;

    public int calculateArea() {
        return width * height;
    }
}

```

## Escolha entre Objetos e Estruturas de Dados

#### Objetos:

```java

public class Circle {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    public double calculateArea() {
        return Math.PI * radius * radius;
    }
}

```

#### Estruturas de Dados:

```java

public class Circle {
    public double radius;
}

public class CircleOperations {
    public double calculateArea(Circle circle) {
        return Math.PI * circle.radius * circle.radius;
    }
}

```


A escolha entre usar objetos ou estruturas de dados depende da necessidade do momento. Objetos encapsulam dados e comportamentos, facilitando a adição de novos tipos de dados. Estruturas de dados expõem dados e facilitam a adição de novas operações.

Esses exemplos ilustram a importância de entender e aplicar corretamente os conceitos de objetos e estruturas de dados para manter o código limpo, legível e fácil de manter.
