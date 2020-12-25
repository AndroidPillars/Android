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

__double__

- Float numbers -> Holds 64 bits

```ruby
public class MyClass {
    public static void main(String[] args) {

         double mAge = 2339483.967888;

        System.out.println("I am " +mAge+ " Years old");
    }
}
```

__Types in Java - int, byte__

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
- char -> Sttring that holds only one character -> Holds 16 bits

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

- Java Source File -> 


# Points to get Remember

- File -> Power Save Mode -> To Disable the auto suggestions methods

# Tools References

- https://www.material-theme.com/docs/getting-started/ [Android Studio Material Theme]
