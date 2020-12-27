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

# Java Compiler

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

# Java For-Loop

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

# Java Else if

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

# Java Do/While

- This loop will execute the code block once, before checking if the condition is true, then it will repeat the loop as long as the condition is true.

```ruby
public class MyClass {
    public static void main(String[] args) {

        int i = 0;
        do {
            System.out.println("The Condition is printed" + i);
            i++;
        } while (i < 10);
    }
}
```

# Java Methods & Parameters

- A method is a block of code which only runs when it is called.
- You can pass data, known as parameters, into a method.
- Methods are used to perform certain actions, and they are also known as functions.

```ruby
public class MyClass {
    public static void main(String[] args) {
        init("Hello World");
    }

    private static void init(String mValue) {
        System.out.println(mValue);
    }
}
```

# Java Return Types in Methods

- If you want the method to return a value, you can use a primitive data type (such as int, char, etc.) instead of void, and use the return keyword inside the method

```ruby
public class MyClass {
    public static void main(String[] args) {
        int mResult = init(4,5);
        System.out.println(mResult);
    }

    private static int init(int mValue1, int mValue2) {
        int mFinalValue = mValue1 + mValue2;
       return mFinalValue;
    }
}
```

# Arrays

- Ordered group of values or objects in an organized manner.
- Everything starts with INDEX 0.
- Array cannot have multiple different data types of List.

```ruby
public class MyClass {
    public static void main(String[] args) {
        int[] mArray = {123, 456, 789};
        System.out.println(mArray[0]);

        String[] mStringArray = {"abc", "def", "ghi"};
        for (int i = 0; i < mStringArray.length; i++) {
            System.out.println(mStringArray[i]);
        }
    }
}
```

__Pre-Setting Array's Length__

```ruby
public class MyClass {
    public static void main(String[] args) {
        int[] mArray = new int[3];
        mArray[0] = 1;
        mArray[1] = 2;
        mArray[2] = 3;

        for (int i = 0; i < mArray.length; i++) {
            System.out.println(mArray[i]);
        }
    }
}
```

__ArrayLists__

```ruby
public class MyClass {
    public static void main(String[] args) {

        // ArrayList<String> mArrayList = new ArrayList<>();

        ArrayList mArrayList = new ArrayList();
        mArrayList.add(1);
        mArrayList.add("Hello");
        for (int i = 0; i < mArrayList.size(); i++) {
            System.out.println(mArrayList.get(i));
        }
    }
}
```

__Looping through ArrayList__

```ruby
public class MyClass {
    public static void main(String[] args) {

        ArrayList mArrayList = new ArrayList();
        mArrayList.add("a");
        mArrayList.add("b");
        mArrayList.add("c");
        mArrayList.add("d");
        mArrayList.add("f");
        for (int i = 0; i < mArrayList.size(); i++) {
            System.out.println(mArrayList.get(i));
        }

        ArrayList<String> mArrayListTwo = new ArrayList<>();
        mArrayListTwo.add("ab");
        mArrayListTwo.add("bb");
        mArrayListTwo.add("cb");
        mArrayListTwo.add("db");
        mArrayListTwo.add("fb");
        for (String mArrayListValues : mArrayListTwo) {
            System.out.println(mArrayListValues);
        }
    }
}
```

# Passing Arrays as Method Parameter

```ruby
public class MyClass {
    public static void main(String[] args) {
        int[] mArrList = {1, 2, 3, 4, 5, 6, 7, 8, 9};
        multipliesOfThree(mArrList);
    }

    private static void multipliesOfThree(int[] mArrayList) {
        if (mArrayList.length > 0) {
            for (int mArray : mArrayList) {
                if (mArray % 3 == 0) {
                    System.out.println("Multiples of Three: " + mArray);
                } else {
                    System.out.println(mArray);
                }
            }
        } else {
            System.out.println("Array List is Empty");
        }
    }
}
```

# Points to get Remember

- File -> Power Save Mode -> To Disable the auto suggestions methods

# Tools References

- https://www.material-theme.com/docs/getting-started/ [Android Studio Material Theme]
- https://github.com/twitter-archive/commons/blob/master/src/java/com/twitter/common/styleguide.md#formatting [Java Style Guide]
