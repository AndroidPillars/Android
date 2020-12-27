# Classes and Objects

- A template (blueprint) for creating objects (the real thing).
- For example, we can take a Mic -> Mic is an object.

__classes Anatomy__

- properties or attributes -> color, name, micType
- Methods -> turnOn, turnOff, setVolume(), mute()
- Objects will have those properties and methods tool (i.e.) It is a basic unit of Object Oriented Programming and represents the real life entities.

__MyClass.java__

```ruby
public class MyClass {
    public static void main(String[] args) {
        Microphone mMicrophone = new Microphone();
        mMicrophone.mName = "Gauthy";
        mMicrophone.mColor = "Blue";
        mMicrophone.mModel = 555;

        System.out.println(mMicrophone.mName + ", " + mMicrophone.mColor + ", " + mMicrophone.mModel);

        mMicrophone.turnOn();
        mMicrophone.setVolume();
        mMicrophone.turnOff();
        System.out.println(mMicrophone.showDescription());

    }
}
```

__Microphone.java__

```ruby
public class Microphone {

    //    Instance variables / Properties / Fields
    String mName;
    String mColor;
    int mModel;

    public void turnOn() {
        System.out.println(this.mName + " Turn On");
    }

    public void turnOff() {
        System.out.println(this.mName + " Turn Off");
    }

    public void setVolume() {
        System.out.println(this.mName + " Set Volume");
    }

    public String showDescription() {
        return "Microphone name " + this.mName + " with color: " + this.mColor
                + " and its model " + this.mModel;
    }

}
```

# Constructor

- The Constructor is a method that add to our class which will allow us to construct the object.
- In other words,The constructor is a block of codes similar to the method. 
- It is called when an instance of the class is created. 
- At the time of calling constructor, memory for the object is allocated in the memory.
- It calls a default constructor if there is no constructor available in the class.

__MyClass.java__

```ruby
public class MyClass {
    public static void main(String[] args) {
        Microphone mMicrophone = new Microphone("Gauthy", "Blue", 555);

        System.out.println(mMicrophone.mName + ", " + mMicrophone.mColor + ", " + mMicrophone.mModel);

        mMicrophone.turnOn();
        mMicrophone.setVolume();
        mMicrophone.turnOff();
        System.out.println(mMicrophone.showDescription());

    }
}
```

__Microphone.java__

```ruby
public class Microphone {

    String mName;
    String mColor;
    int mModel;

    public Microphone(String mName, String mColor, int mModel) {
        this.mName = mName;
        this.mColor = mColor;
        this.mModel = mModel;
    }

    public void turnOn() {
        System.out.println(this.mName + " Turn On");
    }

    public void turnOff() {
        System.out.println(this.mName + " Turn Off");
    }

    public void setVolume() {
        System.out.println(this.mName + " Set Volume");
    }

    public String showDescription() {
        return "Microphone name " + this.mName + " with color: " + this.mColor
                + " and its model " + this.mModel;
    }

}
```

# Super Keyword

- The super keyword in Java is a reference variable which is used to refer immediate parent class object.
- Whenever you create the instance of subclass, an instance of parent class is created implicitly which is referred by super reference variable.

__Usage of Java super Keyword__
- super can be used to refer immediate parent class instance variable.
- super can be used to invoke immediate parent class method.
- super() can be used to invoke immediate parent class constructor.

# Inheritance

- When the class is able to inherit the properties and methods from their parents.
- In other words, Inheritance is a mechanism in which one class acquires the property of another class.

__MyClass.java__
```ruby
public class MyClass {
    public static void main(String[] args) {

        Microphone mMicrophone = new Microphone("Gauthy", "Blue", 555);

        mMicrophone.setmName("Gauthy");
        mMicrophone.setmColor("Green");
        mMicrophone.setmModel(987);
        System.out.println(mMicrophone.getmName() + ", " + mMicrophone.getmColor() + ", " + mMicrophone.getmModel());


        MiniMicrophone mMicroPhoneOne = new MiniMicrophone();
        mMicroPhoneOne.setmName("GauthyOne");
        mMicroPhoneOne.setmColor("Red");
        mMicroPhoneOne.setmManufacturingCompany("ReddyDot");
        System.out.println(mMicroPhoneOne.getmName() + ", " + mMicroPhoneOne.getmColor());

    }
}
```

__Microphone.java__

```ruby
public class Microphone {

    private String mName;
    private String mColor;
    private int mModel;

    public Microphone() {

    }

    public Microphone(String mName, String mColor, int mModel) {
        this.mName = mName;
        this.mColor = mColor;
        this.mModel = mModel;
    }

    public Microphone(String mName, String mColor) {
        this.mName = mName;
        this.mColor = mColor;
    }

    public String getmName() {
        return mName;
    }

    public void setmName(String mName) {
        this.mName = mName;
    }

    public String getmColor() {
        return mColor;
    }

    public void setmColor(String mColor) {
        this.mColor = mColor;
    }

    public int getmModel() {
        return mModel;
    }

    public void setmModel(int mModel) {
        this.mModel = mModel;
    }
}
```

__MiniMicrophone.java__

```ruby
public class MiniMicrophone extends Microphone {

    private String mManufacturingCompany;

    public String getmManufacturingCompany() {
        return mManufacturingCompany;
    }

    public void setmManufacturingCompany(String mManufacturingCompany) {
        this.mManufacturingCompany = mManufacturingCompany;
    }

}
```

# Access Modifiers

- Java access modifiers are used to provide access control in java.
- An access modifier restricts the access of a class, constructor, data member and method in another class. 
- Java provides access control through __default, private, protected and public__.
- __Private:__ The access level of a private modifier is only within the class. It cannot be accessed from outside the class.
- __Default:__ The access level of a default modifier is only within the package. It cannot be accessed from outside the package. If you do not specify any access level, it will be the default.
- __Protected:__ The access level of a protected modifier is within the package and outside the package through child class. If you do not make the child class, it cannot be accessed from outside the package.
- __Public:__ The access level of a public modifier is everywhere. It can be accessed from within the class, outside the class, within the package and outside the package.
- There are many non-access modifiers, such as static, abstract, synchronized, native, volatile, transient, etc. 

# Encapsulation

- The whole idea behind encapsulation is to hide the implementation details from users. 
- If a data member is private it means it can only be accessed within the same class. 
- No outside class can access private data member (variable) of other class.
- We can use setter and getter methods to set and get the data in it.

__MyClass.java__

```ruby
package com.gowtham.myjava;

public class MyClass {
    public static void main(String[] args) {
    
        Microphone mMicrophone = new Microphone("Gauthy", "Blue", 555);
        mMicrophone.setmName("Gauthy");
        mMicrophone.setmColor("Green");
        mMicrophone.setmModel(987);
        System.out.println(mMicrophone.getmName() + ", " + mMicrophone.getmColor() + ", " + mMicrophone.getmModel());
    }
}
```

__Microphone.java__

```ruby
public class Microphone {

    private String mName;
    private String mColor;
    private int mModel;

    public Microphone(String mName, String mColor, int mModel) {
        this.mName = mName;
        this.mColor = mColor;
        this.mModel = mModel;
    }

    public String getmName() {
        return mName;
    }

    public void setmName(String mName) {
        this.mName = mName;
    }

    public String getmColor() {
        return mColor;
    }

    public void setmColor(String mColor) {
        this.mColor = mColor;
    }

    public int getmModel() {
        return mModel;
    }

    public void setmModel(int mModel) {
        this.mModel = mModel;
    }
}
```

# Method/Constructor Overloading

- If a class has multiple methods having same name but different in parameters, it is known as Method Overloading.
- Constructor overloading in Java is a technique of having more than one constructor with different parameter lists. 
- They are arranged in a way that each constructor performs a different task. 
- They are differentiated by the compiler by the number of parameters in the list and their types.

__MyClass.java__

```ruby
public class MyClass {
    public static void main(String[] args) {
    
        Microphone mMicrophone = new Microphone("Gauthy", "Blue", 555);
        mMicrophone.setmName("Gauthy");
        mMicrophone.setmColor("Green");
        mMicrophone.setmModel(987);
        System.out.println(mMicrophone.getmName() + ", " + mMicrophone.getmColor() + ", " + mMicrophone.getmModel());


        Microphone mMicroPhoneOne = new Microphone();
        mMicroPhoneOne.setmName("GauthyOne");
        mMicroPhoneOne.setmColor("Red");
        System.out.println(mMicroPhoneOne.getmName() + ", " + mMicroPhoneOne.getmColor());

    }
}
```

__Microphone.java__

```ruby
public class Microphone {

    private String mName;
    private String mColor;
    private int mModel;

    public Microphone() {

    }

    public Microphone(String mName, String mColor, int mModel) {
        this.mName = mName;
        this.mColor = mColor;
        this.mModel = mModel;
    }

    public Microphone(String mName, String mColor) {
        this.mName = mName;
        this.mColor = mColor;
    }

    public String getmName() {
        return mName;
    }

    public void setmName(String mName) {
        this.mName = mName;
    }

    public String getmColor() {
        return mColor;
    }

    public void setmColor(String mColor) {
        this.mColor = mColor;
    }

    public int getmModel() {
        return mModel;
    }

    public void setmModel(int mModel) {
        this.mModel = mModel;
    }
}
```

# Method Overriding

- If subclass (child class) has the same method as declared in the parent class, it is known as method overriding in Java.

__MyClass.java__

```ruby
public class MyClass {
    public static void main(String[] args) {

        Microphone mMicrophone = new Microphone("Gauthy", "Blue", 555);
        mMicrophone.setmName("Gauthy");
        mMicrophone.setmColor("Green");
        mMicrophone.setmModel(987);
        System.out.println(mMicrophone.getmName() + ", " + mMicrophone.getmColor() + ", " + mMicrophone.getmModel());


        MiniMicrophone mMicroPhoneOne = new MiniMicrophone();
        mMicroPhoneOne.setmName("GauthyOne");
        mMicroPhoneOne.setmColor("Red");
        mMicroPhoneOne.setmManufacturingCompany("ReddyDot");
        System.out.println(mMicroPhoneOne.getmName() + ", " + mMicroPhoneOne.getmColor());

        HeadPhone mHeadPhone = new HeadPhone();
        mHeadPhone.setmManufacturingCompany("ReddyDot");
        System.out.println(mHeadPhone.getmManufacturingCompany());

    }
}
```

__Microphone.java__

```ruby
public class Microphone {

    private String mName;
    private String mColor;
    private int mModel;

    public Microphone() {

    }

    public Microphone(String mName, String mColor, int mModel) {
        this.mName = mName;
        this.mColor = mColor;
        this.mModel = mModel;
    }

    public Microphone(String mName, String mColor) {
        this.mName = mName;
        this.mColor = mColor;
    }

    public String getmName() {
        return mName;
    }

    public void setmName(String mName) {
        this.mName = mName;
    }

    public String getmColor() {
        return mColor;
    }

    public void setmColor(String mColor) {
        this.mColor = mColor;
    }

    public int getmModel() {
        return mModel;
    }

    public void setmModel(int mModel) {
        this.mModel = mModel;
    }
}
```

__MiniMicrophone.java__

```ruby
public class MiniMicrophone extends Microphone {

    private String mManufacturingCompany;

    public String getmManufacturingCompany() {
        return mManufacturingCompany;
    }

    public void setmManufacturingCompany(String mManufacturingCompany) {
        this.mManufacturingCompany = mManufacturingCompany;
    }

}
```

__HeadPhone.java__

```ruby
public class HeadPhone extends MiniMicrophone {

    @Override
    public String getmManufacturingCompany() {
        return super.getmManufacturingCompany() + "Hedge";
    }
}
```

# String Override Method

- A string representation of an object can be obtained using the toString() method in Java. 
- This method is overridden so that the object values can be returned.

__MyClass.java__

```ruby
public class MyClass {
    public static void main(String[] args) {
        Student mStudent = new Student(101, "Gauthy");
        System.out.println(mStudent);
    }

```

__Student.java__

```ruby
class Student {
    private int mRNo;
    private String mName;
    public Student(int rNo, String name) {
        mRNo = rNo;
        mName = name;
    }
    public String toString() {
        return mRNo + " " + mName;
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
