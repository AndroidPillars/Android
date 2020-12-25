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
