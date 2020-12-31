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

Or

```ruby
<Button  android:onClick="searchClose"/>  
````

```ruby
public void searchClose(View view) {
     Toast.makeText(getApplicationContext(),"Button Clicked!!!", Toast.LENGTH_LONG).show();  
    }
```

# Android Manifest

- The AndroidManifest.xml file contains information of your package, including components of the application such as activities, services, broadcast receivers, content providers etc.
- It is responsible to protect the application to access any protected parts by providing the permissions.

# Android Activity LifeCycle

- An activity represents a single screen with a user interface just like window or frame of Java.
- Android activity is the subclass of ContextThemeWrapper class.
     - onCreate -> 	called when activity is first created.
     - onStart -> called when activity is becoming visible to the user.
     - onResume -> 	called when activity will start interacting with the user.
     - onPause -> called when activity is not visible to the user.
     - onStop -> called when activity is no longer visible to the user.
     - onRestart -> called after your activity is stopped, prior to start.
     - onDestroy -> called before the activity is destroyed.
- Image Link: https://developer.android.com/images/activity_lifecycle.png

# Intents

- Android Intent is the message that is passed between components such as activities, content providers, broadcast receivers, services etc.
- It is generally used with startActivity() method to invoke activity, broadcast receivers etc.
- Two Types -> implicit and explicit.

__Implicit Intent__

- Implicit Intent doesn't specifiy the component.
- In such case, intent provides information of available components provided by the system that is to be invoked.

```ruby
Intent intent=new Intent(Intent.ACTION_VIEW);  
intent.setData(Uri.parse("http://www.google.com"));  
startActivity(intent);  
```

__Explicit Intent__

- Explicit Intent specifies the component. 
- In such case, intent provides the external class to be invoked.

```ruby
Intent i = new Intent(getApplicationContext(), ActivityTwo.class);  
startActivity(i);  
```

__or__

```ruby
startActivity(new Intent(getApplicationContext(), ActivityTwo.class));
```

__Passing the Values in Intent__

```ruby
Intent i = new Intent(getApplicationContext(), ActivityTwo.class);
i.putExtra("keyValue", "Hello World");
startActivity(i); 
```

__Getting the Values in Intent__

```ruby
String mStringValue = getIntent().getStringExtra("keyValue");
```

__or__

```ruby
Bundle extras = getIntent().getExtras();
        
if(extras != null){
   String mStringValue = extras.getString("keyValue");
}
```

__Using onActivityResult__

```ruby
private final int REQUEST_CODE = 2;

Intent intent = new Intent(getApplicationContext(), ActivityTwo.class);
intent.putExtra("keyValue", "Hello World");
startActivityForResult(intent, REQUEST_CODE);

@Override
protected void onActivityResult(int requestCode, int resultCode, @Nullable Intent data) {
   super.onActivityResult(requestCode, resultCode, data);

   if (requestCode == REQUEST_CODE) {
        if (resultCode == RESULT_OK) {
           assert data != null;
            String message = data.getStringExtra("message_back");

             Toast.makeText(MainActivity.this, message,
                        Toast.LENGTH_LONG)
                        .show();
       }
    }
 }
```

```ruby
@Override
public void onBackPressed() {
  super.onBackPressed();
  Intent intent = getIntent();
  intent.putExtra("message_back", "From Second Activity");
  setResult(RESULT_OK, intent);
  finish();
}
```

# API (Application Programming Interface)

- It is a software interface that allows two applications to interact with each other without any user intervention.

__Example__

- When you use an application on your mobile phone, the application connects to the Internet and sends data to a server.
- The server then retrieves that data, interprets it, performs the necessary actions and sends it back to your phone. 
- The application then interprets that data and presents you with the information you wanted in a readable way.

# Singleton

- Ensures a class has only one instance, and provide a global point of access it.
- Some times we need only one instances of an Object.

__Advantages__

- Saves memory because object is not created at each request. Only single instance is reused again and again.

__Usage of Singleton design pattern__

- Singleton pattern is mostly used in multi-threaded and database applications. It is used in logging, caching, thread pools, configuration settings etc.
