# Persistence in Android

- Saving Data on Device.
- Device Disk -> TextFile, Shared Preferences and DataBase

# Shared Preferences

- Shared Preferences allow you to save and retrieve data in the form of key,value pair.
- In order to use shared preferences, you have to call a method getSharedPreferences() that returns a SharedPreference instance pointing to the file that contains the values of preferences.

__Saving the Value__

```ruby
private static final String MESSAGE_ID = "messages_prefs" ;

SharedPreferences sharedPreferences = getSharedPreferences(MESSAGE_ID, MODE_PRIVATE);
SharedPreferences.Editor editor = sharedPreferences.edit();
editor.putString("message", message);
editor.apply();
```
__Getting the Value__

```ruby
SharedPreferences getSharedPrefs = getSharedPreferences(MESSAGE_ID, MODE_PRIVATE);
String value = getSharedPrefs.getString("message", "nothing");
```

# SQLite VS Shared Preferences

__SQLite__

- Large amounts of same structured data should be stored in a SQLite database as databases are designed for this kind of data.
- If you plan to do join, sort, and other DB operations on your data then go for Sqlite.

__Shared Preferences__

- If you want to map simple values (like int, boolean, String) then use Preferences. 
- DB operations won't work here and needless to say you need to have all the keys. 

# Database - SQLite

- Database is a structured way of organising data(rows and coulumns) and also it allows to retrive data quicker and more efficient.
- SQLite is an open-source relational database i.e. used to perform database operations on android devices such as storing, manipulating or retrieving persistent data from the database.
- It is embedded in android bydefault.
- SQLiteOpenHelper class provides the functionality to use the SQLite database.

# Major problems with SQLite

- There is no compile-time verification of raw SQL queries. For example, if you write a SQL query with a wrong column name that does not exist in real database then it will give exception during run time and you can not capture this issue during compile time.
- As your schema changes, you need to update the affected SQL queries manually. This process can be time-consuming and error-prone.
- You need to use lots of boilerplate code to convert between SQL queries and Java data objects (POJO).

# Room Database

- Room is a persistence library, part of the Android Jetpack.
- Android Jetpack is a collection of Android software components to make it easier for you to develop great Android apps.
- Room provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite.
- Room is now considered as a better approach for data persistence than SQLiteDatabase. 
- It makes it easier to work with SQLiteDatabase objects in your app, decreasing the amount of boilerplate code and verifying SQL queries at compile time.

# Why Room

- Room is built to work with LiveData and RxJava for data observation, while SQLite does not.
- In the case of SQLite, There is no compile-time verification of raw SQLite queries. But in Room, there is SQL validation at compile time.
- You need to use lots of boilerplate code to convert between SQL queries and Java data objects. But, Room maps our database objects to Java Object without boilerplate code.
