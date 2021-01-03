# Data Binding

- The Data Binding Library is a support library that allows you to bind UI components in your layouts to data sources in your app using a declarative format 
rather than programmatically.

__Data binding has the following benefits__

- Code is shorter, easier to read, and easier to maintain than code that uses findByView().
- Data and views are clearly separated. This benefit of data binding becomes increasingly important later in this course.
- The Android system only traverses the view hierarchy once to get each view, and it happens during app startup, not at runtime when the user is interacting with the app.
- You get type safety for accessing views. (Type safety means that the compiler validates types while compiling, and it throws an error if you try to assign the wrong type to a variable.)
