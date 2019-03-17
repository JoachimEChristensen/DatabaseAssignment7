# DatabaseAssignment7

## Exercise 1

### Normal form 1
There are no violations to the first normal form.
Customer number is the primary key here, but in order to uniquely associate salesrep's information with salesrep and customer, a composite primary key composed of customerNumber and repName is used.
### Normal form 2
There is a second normal form violation.

Specifically, there is a functional dependancy issue because the customer number is used to access all of the information regarding the customer, which means a non-key field is not completly depedant on the entire composite primary key. 

Functional dependency is an issue like we mentioned above, not all non-key fields are dependent upon the entire primary key.
if we could use repName to access the salesrep's information, not even need a customer number. 

### Normal form 3
Because the table does not fulfill the requirements to be in normal form 2, it is naturally not in normal form 3 either.

## Exercise 2
To replace Customer Number, we instead use Customer Name, because it is a unique value since you can only have one customer attached in this table. So it means a composite primary key composed of customerName and repName is used.

In regards to violations, you still end up hitting the same second normal form violation, because some all non-key fields are still not dependent upon the entire primary key. 

## Exercise 3
***Statement 1*** <br/>
```
UPDATE CustomerOverview
SET repPhone = '+1 512 738 5208'
WHERE customerName = 'Mini Creations Ltd.' AND repName = 'Julie Firrelli';
```
***Statement 2*** <br/>
```
UPDATE CustomerOverview
SET repEmail = 'jrell3333i@classicmodelcars.com'
WHERE custCity = 'Bern';
//OR WHERE custCountry = 'USA';
```
By look into the result from table after update statement 1, we found out that repPhone is not depended on repName but the entire office. When we update the phone number of a specific salesrep, it will end up to also update other salesreps in the same office. We call it *update anomalies*, which means problems that arise when information is inserted, deleted, or updated.
<br/> As same as the result from update statement 1, the update statement 2 got the same problem that the query will also update other redundant data, when one of them is getting update, which means that database is still un-normalized.

## Exercise 4
