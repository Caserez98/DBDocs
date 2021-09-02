## **Database Systems Overview**
### __Data requirements__
>- **Integrity** Data should be accurate
>- **Availability** I should be able to access and see my data at all times
>- **Security** No one else should be able to see my data (Depends on you of course)
>- **Independent of Application** I should be able to access the same data on a wide variety of devices.
>- **Concurrent** Data concurrency allows multiple users to access data all at the same time
***
## __Limitations on Flat Files__
>- Data is stored in flat files and can be accessed using any programming language. The file-based approach suffers following problems:
>- Dependency of program on physical structure of data
>- Complex process to retrieve data
>- Loss of data on concurrent access
>- Inability to give access based on record (Security)
>- Data redundancy
***
### **DBMS**
> A Database is a shared collection of logically related data and description of these data, designed to meet the information needs of an organization.
>
> A Database Management System(DBMS) is a software system that enables users to define, create, maintain, and control access to the database. Database Systems typically __have high cost__ and they __require high-end hardware configurations__.
>
>A database management system is a **Collection of programs to access data**.
>
> Is an interface between the __database application__ and the __database__.

>__Disventages of file system to store data:__
>    - Data redundancy and inconsistancy
>    - Difficulty in accesing data
>   - Data isolation is not present
>

>__Features provided by DBMS:__
>- Maintain accurancy of database
>- Utilities for perfomance analysis and logging
>- Ensure modifications are succesful or not done at all
>- Recovery mechanism for database recovery
>
***
>### **Functions of DBMS**
>Database Management Systems offers several functions that help us overcome problems associated with file-based systems. 
>
>We will focus on Data Management, Integrity, Transaction and Concurrency in this course. Security, Recovery and Utilities are out of scope for this introductory-level course.
>- **Utilities**: Data import/export, user management, backup, performance analysis, logging and audits.
>- __Integrity:__ Maintain accurancy of data.
>- __Security:__ Access to authorised users only.
>- __Data Management:__ Store, retrieve and modify data.
>- __Transaction support:__ Ensure modifications to database must either be successful or not done at all.
>- __Concurrency control:__ Simultaneous data access provided to users.
>- __Recovery:__ Recovery mechanism for data so nothing is lost.
***