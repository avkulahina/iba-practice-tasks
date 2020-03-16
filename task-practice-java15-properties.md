# Task \#15 - Use properties file for DataBase configuration

Create `setting.properties` file in your project. The file must contain properties, that will define behaviour of your DataBase class:

- property that set up the target class for each instance of `IOperation`
E.g. your class uses `WorkLogDefaultQueries` class for work logs. Your properties file must contain property that define this behaviour and WorkLog`Default`Queries will be loaded instead of WorkLog`Custom`Queries (you don't have WorkLog`Custom`Queries but imagine like you have).
- property that set up the target class for eqach instance of `IQuery`
- database url, database driver, databse user and password

NOTE: While you developing use only one class e.g. DataBase, do not create clones such as DataBaseRef or DataBase2. Git stores all the history, and in case you can always restore to previous version. Multuple instances of the classes is a bad practice. Now you can copy the code from the resently changed DataBaseRef into DataBase and remove everything related to DataBaseRef.
