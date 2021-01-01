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

# Database - SQLite

- Database is a structured way of organising data(rows and coulumns) and also it allows to retrive data quicker and more efficient.
- SQLite is an open-source relational database i.e. used to perform database operations on android devices such as storing, manipulating or retrieving persistent data from the database.
- It is embedded in android bydefault.
- SQLiteOpenHelper class provides the functionality to use the SQLite database.
