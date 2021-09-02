>## __Normal Forms__
> To revisit, Database normalization is the process of structuring a relational database in accordance with a series of so-called normal forms in order to reduce data redundancy and improve data integrity.  Normalization was first proposed by Edgar F. Codd.
>
> **Normal Forms** (NF) are the different stages of normalization.
>- 1 NF (First Normal Form)
>- 2 NF (Second Normal Form)
>- 3 NF (Third Normal Form)
>- BCNF (Boyce -Codd Normal Form)
>___
> ### __First Normal Form: 1 NF__
> A relation R is said to be in 1 NF (First Normal) if and only if:
>- All the attributes of R are atomic in nature
>- There should not be any multi-valued attribute
>
> Table before 1st normal form
>![!](/assets/img/F1Norm.PNG)
>So, we will split the non-atomic attribute, retailoutletlocation into three different attributes- street, city and zipcode all of them being atomic, the resulting relation will be in First Normal Form.
>
> Table after 1st normal form
>![!](/assets/img/Normalizationretailoutlet1.JPG)
>___
> ### __Second Normal Form: 2 NF__
> A relation R is said to be in 2 NF (Second Normal) form if and only if:
>
>- R is already in 1 NF
>- There is no partial dependency in R which exists between non-key attributes and key attributes
>
> To make a table 2 NF compliant, remove all such partial dependencies and decompose the relation.
> 
> Since the description is dependent only on itemcode, we can create a separate table item with itemcode and description as its attributes, so that the partial dependencies are eliminated. Similarly, retail outlet details like retailoutletid, street, city and zipcode attributes must be in a separate table retailoutlet. Also, the attributes qtyavailable, retailunitprice, itemclass are dependent on both itemcode and retailoutletid. Hence, we will have another table retailstockdetails with those attributes.
>
> After removing the partial dependencies, we have three tables item, retailoutlet and retailstockdetails, each of them in 2 NF.
>![!](/assets/img/normalforms1.JPG)
>![!](/assets/img/normalforms2.JPG)
>___
> ### __Third Normal Form: 3 NF__
> A relation R is said to be in 3 NF (Third Normal Form) if and only if:
>
>- R is already in 2 NF
>- There is no transitive dependency which exists between key attributes and non-key attributes through other non-key attributes
>
>A transitive dependency in a database is an indirect relationship between attributes in the same table that causes a functional dependency.
>
>X -> Z is a transitive dependency if the following three functional dependencies hold true:
>
>- X->Y
>- Y does not ->X
>- Y->Z
>
> To make retailstockdetails 3 NF compliant, we must remove all such transitive dependencies by decomposing the relation.
> Here we split retailstockdetails in three.
>
>After
>![!](/assets/img/normalforms2.JPG)
>Before
>![!](/assets/img/3nf1.JPG)
>![!](/assets/img/3nf2.JPG)
> ___
> ### __Diagrammatic Representation__
>![!](/assets/img/summary.JPG)
>___
> ### __Guidelines__
>Depending on the business requirements, the tables can be normalized up to 2nd normal form or 3rd normal form
>
>Tables in 3 NF are preferred in applications with extensive data modifications
>
>Tables in 2 NF are preferred in applications with extensive data retrieval
>
>Reason: retrieving data from multiple tables is a costly operation
>
>Converting the tables from higher normal form to lower normal form is called “Denormalization”

