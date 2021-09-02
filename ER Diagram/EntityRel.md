> __ER Model__  is a graphical representation of entities and their relationships which helps in understanding data independent of the actual database implementation. Let us understand some key terms used in ER Modelling.
>![!](/assets/img/Page32.png)
>![!](/assets/img/er-model-01.png)
>___
>### __Relationships__
>Relationships are associations of one entity with another entity through a __foreign key__. Each relationship has a name e.g. a Computer is allocated to an Employee.
>![!](/assets/img/relationship-01.png)
>There can be more than one relationship between entities, e.g. an Employee works in a Department while the head of the department (also an employee) manages a Department.
>![!](/assets/img/relationship-02.png)
>A relationship can also exist between instances of the same entity, e.g. an Employee reports to a manager (also an Employee).
>![!](/assets/img/relationship-03.png)
>____
> ### Cardinality of relationships
> Cardinality of relationship is the number of instances in one entity which is associated to the number of instances in another. For the relationship between Employee and Computer, it helps us answer questions like how many computers can be allocated to an employee, can computers be shared between employees, can employees exist without being allocated a computer etc. e.g. if 0 or 1 computer can be allocated to 0 or 1 employee then the cardinality of relationship between these two entities will be 1:1.
>![!](/assets/img/cardinality.png)
> ___
> ### __Crowd Foot Notation__
>Crow foot notation is one of the ways to represent cardinality of relationship in an ER Model. The notation comprises of four symbols and one of them needs to be used for each entity in a relationship.
>![!](/assets/img/crow-feet-notation.png)
>___
> ### __Relationships and Foreign Keys__
>Foreign keys need to be created in tables in order to establish the relationship between entities.
>![!](/assets/img/relationship-04.png)
>![!](/assets/img/relationship-05.png)
>![!](/assets/img/relationship-06.png)
>The table in which foreign key will be created depends upon the cardinality of the relationship. Let us now discuss about the types of cardinalities and how it impacts foreign key creation.
> ___
>### __1:1 Relationship__
>1:1 relationship represents association between single occurrence of one entity and a single occurrence of the second entity. For e.g. consider a company where each employee can be allocated a maximum of 1 computer and computers are not shared between employees.
>![!](/assets/img/cardinality-1-to-1.png)
>The Allot_Dt attribute is not a property of employee or computer. It belongs to the relationship and is hence represented differently in the ER Model.
>___
> ### __1:N Relationship__
>1 : N relationship represents association between single occurrence of one entity and multiple occurrences of second entity. For e.g. consider a company where each employee can be allocated with many computers but still computers cannot be shared between employees.
>![!](/assets/img/cardinality-1-to-n.png)
>In 1 : N relationships, the foreign key and relationship attributes are always added to the many (N) side of the relationship. Hence these attributes are added to computer table. The reverse solution will not work.
>___
> ### __M:N__
>M:N relationship represents association between multiple occurrences of both entities. For e.g. consider a company where each employee can be allocated with many computers and computers can be shared between employees.
>![!](/assets/img/cardinality-m-to-n.png)
>In M : N relationships, the relationship is represented by a completely new table that has a composite primary key. Such a structure requires two foreign keys on the new table linking to the primary keys of each of the parent tables. The attribute of the relationship resides on this new table.
> ### __QUIZ__
>![!](/assets/img/qr1.PNG)
>![!](/assets/img/qr23.PNG)




