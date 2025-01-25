# OOP

## Concepts
1. `Abstraction` implemented as `Interfaces` and `Abstract classes`
2. `Incapsulation` - `public`, `protected`, `private`
3. `Inheritance` - `extends`
4. `Polymorphism` - `@Override`


## Inner / Nested Classes

```java
public class Outer {
    class Inner {
        Inner() { System.out.println("Inner"); }
    }
    static class Nested {
        Nested() { System.out.println("Nested"); }
    }
}

public class Test {
    public static void main(String[] args) {
        Outer outer = new Outer();
        Outer.Inner inner = outer.new Inner();
        Outer.Nested nested = new Outer.Nested();
    }
}
```

