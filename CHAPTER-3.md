# Android

- Android is an open source and Linux-based Operating System for mobile devices such as smartphones and tablet computers.

# Android Architecture

- It is categorized into five parts:  
     __linux kernel__  
     - Linux kernel is responsible for device drivers, power management, memory management, device management and resource access. 
     
     __native libraries (middleware)__  
     - The WebKit library is responsible for browser support, SQLite is for database, Media for playing and recording audio and video formats.  
     
     __Android Runtime__  
    - In android runtime, there are core libraries and DVM (Dalvik Virtual Machine) which is responsible to run android application. 
    - DVM is like JVM but it is optimized for mobile devices. 
    - It consumes less memory and provides fast performance.   
    
     __Application Framework__  
    - Android framework includes Android API's such as UI (User Interface), telephony, resources, locations, Content Providers (data) and package managers. 
    - It provides a lot of classes and interfaces for android application development.  
    
     __Applications__  
    - All applications such as home, contact, settings, games, browsers are using android framework that uses android runtime and libraries. 
    - Android runtime and native libraries are using linux kernal.  
- Image Link: https://developer.android.com/guide/platform/images/android-stack_2x.png

# Android Widgets

__Toast__

- The toast contains message to be displayed quickly and disappears after sometime.
- Toast class is used to show notification for a particular interval of time. 
- After sometime it disappears. 
- It doesn't block the user interaction.

```ruby
Toast.makeText(getApplicationContext(),"Hello AndroidPillars",Toast.LENGTH_SHORT).show();  
```

__Button__

```ruby
buttonSum.setOnClickListener(new View.OnClickListener() {  
            @Override  
            public void onClick(View view) {  
                Toast.makeText(getApplicationContext(),"Button Clicked!!!", Toast.LENGTH_LONG).show();  
            }  
        });  
```

```ruby
<Button  android:onClick="methodName"/>  
````
