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

        System.out.println(mMicrophone.mName + ", " + mMicrophone.mColor + ", " + mMicrophone.mModel);

        mMicrophone.turnOn();
        mMicrophone.setVolume();
        mMicrophone.turnOff();
        System.out.println(mMicrophone.showDescription());

        MiniMicrophone mMiniMicrophone = new MiniMicrophone("Gauthy", "Blue", 555, "Honey-Well");
        System.out.println(mMiniMicrophone.mManufacturingCompany);
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

__MiniMicrophone.java__

```ruby
public class MiniMicrophone extends Microphone {

    String mManufacturingCompany;

    public MiniMicrophone(String mName, String mColor, int mModel, String mManufacturingCompany) {
        super(mName, mColor, mModel);
        this.mManufacturingCompany = mManufacturingCompany;
    }
}
```

