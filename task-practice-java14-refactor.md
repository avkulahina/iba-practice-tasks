# Task \#14: Refactor task7/DataBase.java 

## Requeriments
---------------------------
### Sql Queries
- create Interface IQueries. The interface must have all method to get String SQL queries for each CRUD operation ( like getUpdate(), getInsert(), get(), getList(), getDelete()). Also it must have static method that accepts enum( with values INCIDENT, USER, WORKLOG) and abstract class name ( like SQLiteQueries.class) and returns an instance of corresponding subclass ( IncidentSQLiteQueries etc...).
- create abstarct class DefaultQueries ( implements IQueries)
- create classes IncidentDefaultQueries, UserDefaultQueries, WorkLogDefaultQueries (extends DefaultQueries) - implement all method using already existing code from DataBase.java

### Operations
- create Interface IOperations. The interface must have insert(), update(), get(), getAll() etc. Also it must have static method that returns instance of subclass and accepts enum( with values INCIDENT, USER, WORKLOG) and abstract class name ( like DefaultOperations.class).
- create abstact class DefaultOperations ( implements IOperations)
- create classes IncidentDefaultOperations, UserDefaultOperations, WorkLogDefaultOperations ( extends DefaultOperations) that implements all methods. Note: you should reuse IQueries here. 

### DataBase
- instead of updateIncident, updateUser etc it should be only one method - update() which can accept enum with a type of record ( like INCIDENT, USER, WORKLOG). Note: you do not allow to recursevly update User or WorkLog together to Incident. If there is more than 1 record updated at time - you should return Exception.

## Note
You can have difficulties with Operations/get and getAll methods. Those methods must return Record object. Make abstract class Record, which will extend every of your *Model classes.
