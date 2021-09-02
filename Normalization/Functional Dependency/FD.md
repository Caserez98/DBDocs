>## __Normalization__
>Is  the process of reorganizing data in a database to ensure that there is no redundancy of data and data dependencies are logical (all related data items are stored together).
>
>The different stages of normalization are known as “normal forms”. To accomplish normalization, we need to understand the concept of Functional Dependencies.
>___
> ### **Functional Dependency**
>
> Functional Dependencies in DBMS is a relation between two or more attributes. It can be categorized as:
>- Fully Functional Dependency
>- Partial Dependency
>- Transitive Dependency
>___
> ### __Dependency in a Relation__
> An attribute of a relation can be determined by knowing one/more attributes of the same relation.
> 
>The attribute which determines the value of other attributes is known as “Determinant”.
>Let us consider the retailoutletstock relation.
>
> __retailoutletstock__ (retailoutletid, itemcode, description, retailoutletlocation(street, city, zipcode), qtyavailable, retailunitprice, itemclass)
>
>The following are the functional dependencies in the relation:
>![!](/assets/img/Functiondependency.JPG)
>- In a relation R, A and B are attributes
>- Attribute B is functionally dependent on attribute A if each value of A determines EXACTLY ONE value of B, which is represented as A -> B (A can be composite in nature)
>- A is called determinant and B is called dependent.
>
>  __{retailoutletid, itemcode}__ is the candidate key of the above relation.
>
> The three types of dependencies are illustrated below.
>![!](/assets/img/F01Norm.PNG)
> In retailoutletstock, we have identified **{retailoutletid, itemcode}** as the candidate key. The attribute, qtyavailable is fully dependent on **{retailoutletid, itemcode}**. The attribute, description is dependent on itemcode(a part of candidate key). Hence description is partially dependent on **{retailoutletid, itemcode}**. The attribute, retailunitprice is dependent on __{retailoutletid, itemcode}__, itemclass is dependent on retailunitprice, which creates a transitive dependency among them.
>
> If functional dependencies are not properly defined, the databases may suffer from the following anomalies.
>- Update/Modification anomalies – if data is inconsistently stored, it can lead to update anomalies
>- Deletion anomalies – when a row is deleted that may contain attributes that shouldn't be deleted
>- Insert anomalies – when a data is inserted that does not exist at all
>
> Normalization is a method to remove all these anomalies and bring the database to a consistent state.
> Let us see these anomalies in detail with an example from the above case study.
> ___
> An anomaly is an unexpected side effect from trying to insert, update, or delete a row. Essentially more data must be provided to accomplish an operation than would be expected.
 >![!](/assets/img/F1Norm.PNG)
> What will happen if we try to insert(add) the details of a new retail outlet that currently has no items in its stock?
>- NULL values would be inserted into the itemdetails columns, which is not preferable.
>
> What will happen if we try to delete the item of an itemcode I1005?
>- The details of the retail outlet R1003 will also be deleted from the database.
>
>How many rows will be updated if the retail outlet location of R1002 is changed from Victoria Street to Saint John Street?
>- 3 Rows will be updated
>
> What are the details we need to insert when new items are supplied to a retail outlet?
>-Apart from all necessary details, retailoutletlocation will also be inserted which is redundant
>
>We have seen insert, delete, update anomalies and data redundancy in the above given example. Functional dependencies may lead to anomalies. To minimize anomalies there is a need to refine functional dependencies using Normalization.

 