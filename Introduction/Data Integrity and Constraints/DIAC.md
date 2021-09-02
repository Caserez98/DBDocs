>## __Data Integrity and Cnstraints__
> ____
>Data integrity refers to maintaining and assuring the accuracy and consistency of data over its entire life-cycle. Database Systems ensure data integrity through constraints which are used to restrict data that can be entered or modified in the database. Database Systems offer three types of integrity constraints:
> ___
>### __Candidate Key__
>A Candidate Key is a minimal set of columns/attributes that can be used to uniquely identify a single row/tuple in a relation. Candidate Keys are determined during database design, based on the underlying business rules of the database.  The Primary key should be selected from the candidate keys. Every table must have at least a __single candidate key__. A table can have multiple candidate keys but only a single primary key.
> **Properties of Candidate Key:**
>- It must contain unique values
>- Candidate key in SQL may have multiple attributes
>- Must no contain null values
>- It should contain a minimum fields to ensure uniqueness
>- Uniquely identify each record in a table
> ___
>### __Primary Key__
>__A Primary Key__ is the candidate key that is selected to uniquely __identify a tuple__ in a **relation**. 
>The mandatory and desired attributes for a primary key are:
>![!](/assets/img/Page-22a.png)

> ___
>### __Foreign Key__
>A Foreign Key is a set of one or more columns in the child table whose values are required to match with corresponding columns in the parent table. Foreign key __establishes a relationship between these two tables__. Foreign key columns identified in child tables must refer to the primary key or unique of the parent table. The child table can contain NULL values. 
>
> Sometimes Foreign Key of a table references back to the primary key of the same table. In that case, the Foreign Key is said to be self-referencing.
>
>Self Referencing Foreign Key is also known as Recursive Foreign Key.
>
>It defines the relationship between the same entity or table.

