# Java Basics Intro

- Java is a cross-platform object-oriented programming language that was released by Sun Microsystems in the year 1995.
- It is an object-oriented language similar to C++, but with advanced and simplified features.
- This language is free to access and can run on all platforms.

# How Java Works

- Java Souce File -> Compiler -> Bytecode (machine instructions) -> Device (with JVM)

# JVM

- JVM (Java Virtual Machine) is an abstract machine. 
- It is a specification that provides runtime environment in which java bytecode can be executed.
- JVMs are available for many hardware and software platforms (i.e. JVM is platform dependent).

# Code Structure

```ruby
public class MyClass {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

# Java Variables and Concatenation

- A variable allow us to store a piece of data.
- It is a container/Bucket in memory.

__Strings__

```ruby
public class MyClass {
    public static void main(String[] args) {
        String mName = "Hello World";
        
        System.out.println("My Name is " +mName+ ".");
    }
}
```

__Integer__

- Integer is a type that hold whole numbers.
- int has a certain capacity to hold the numbers.
- int -> Holds 32 bits

```ruby
public class MyClass {
    public static void main(String[] args) {
         int mAge = 23;

        System.out.println("I am " +mAge+ " Years old");
    }
}
```

__Long__

- long -> Holds 64 bits

```ruby
public class MyClass {
    public static void main(String[] args) {

         long mAge = 2339483967888L;

        System.out.println("I am " +mAge+ " Years old");
    }
}
```

__Double__

- Float numbers -> Holds 64 bits

```ruby
public class MyClass {
    public static void main(String[] args) {

         double mAge = 2339483.967888;

        System.out.println("I am " +mAge+ " Years old");
    }
}
```

__Float__

- Decimal numbers -> Holds 32 bits

```ruby
public class MyClass {
    public static void main(String[] args) {

         float mAge = 2339483.967888f;

        System.out.println("I am " +mAge+ " Years old");
    }
}
```

__Boolean__

- A boolean will holds only one state at a time.

```ruby
public class MyClass {
    public static void main(String[] args) {

        boolean isTall = false;

        System.out.println("I am " +isTall);
    }
}
```

# Types in Java - int, byte

- int -> A whole number holds 32 bits
- byte -> Holds 8 bits -> We can set up to the maximum value only up to 127 and regarding negative value up to -128

```ruby
public class MyClass {
    public static void main(String[] args) {

         byte mAge = 127;

        System.out.println("I am " +mAge+ " Years old");
    }
}
```
- short -> Holds 16 bits

```ruby
public class MyClass {
    public static void main(String[] args) {

         short mAge = 289;

        System.out.println("I am " +mAge+ " Years old");
    }
}
```
- char -> String that holds only one character -> Holds 16 bits

```ruby
public class MyClass {
    public static void main(String[] args) {

        char mName = 'G';

        System.out.println("I am " +mName);
    }
}
```

# Compiler

- Compiler is a internal java tool that checks for for errors, syntax.

# Java Operators

__Arithmetic Operators__

-  + -> add , - -> Subtract , * -> Multiply , / -> Divide, % -> Remainder (or) Modular.

```ruby
public class MyClass {
    public static void main(String[] args) {

        int a = 20;
        int b = 5;
        double c = 21;
        double d = 5;

        int mSum = a + b;
        int mSub = a - b;
        int mMul = (int) (c * d);
        double mDiv = c / d;
        double mRemainder = c % d;

        System.out.println(mSum);
        System.out.println(mSub);
        System.out.println(mMul);
        System.out.println(mDiv);
        System.out.println(mRemainder);

    }
}
```

__Relational Operators__

- Relational Operators are operators that relates two variables (i.e.) It is used to check the relationship between two operands
- ==, !=, <, >, <=, >=

```ruby
public class MyClass {
    public static void main(String[] args) {

        int a = 20;
        int b = 5;

        if(a == b) {
            System.out.println(true);
        }else {
            System.out.println(false);
        }
    }
}
```

__Logical Operators__

- Logical operators are used to check whether an expression is true or false.
- AND(&&), OR(||), NOT(!)

```ruby
public class MyClass {
    public static void main(String[] args) {

        int age = 20;
        boolean mCitizen = true;

        if((age >= 20) && (mCitizen)) {
            System.out.println(true);
        }else {
            System.out.println(false);
        }
    }
}
```

# For-Loop

- The Java for loop is used to iterate a part of the program several times.
- where, int i= 0; is the Initialization,  i < 10; is the Condition and i++ increments the values

```ruby
public class MyClass {
    public static void main(String[] args) {

        for (int i = 0; i < 10; i++) {
            if (i % 4 == 0) {
                System.out.println(i);
            }
        }
    }
}
```

# Else if

- The else if statement to specify a new condition if the first condition is false.

```ruby
public class MyClass {
    public static void main(String[] args) {

        int time = 22;
        if (time < 10) {
            System.out.println("Good morning.");
        } else if (time < 20) {
            System.out.println("Good day.");
        } else {
            System.out.println("Good evening.");
        }
    }
}
```

# Java Switch

- The switch statement to select one of many code blocks to be executed.

```ruby
public class MyClass {
    public static void main(String[] args) {

        String command = "Deposit";
        int balance = 1000;
        int amount = 100;

        switch (command) {
            case "Deposit":
                balance = balance + amount;
                break;
            case "WithDraw":
                balance = balance - amount;
                break;
            default:
                System.out.println(balance);
                break;
        }
        System.out.println(balance);
    }
}
```


# Points to get Remember

- File -> Power Save Mode -> To Disable the auto suggestions methods

# Tools References

- https://www.material-theme.com/docs/getting-started/ [Android Studio Material Theme]
