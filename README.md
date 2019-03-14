# DatabaseAssignment7

## Exercise 1

### Normal form 1
There are no violations to the first normal form.
### Normal form 2
There is a second normal form violation.

Specifically, there is a functional dependancy issue because the customer number is used to access all of the information regarding the customer, which means a non-key field is not completly depedant on the entire composite primary key. 

Functional dependency is an issue because if we were to only use the employee name part of the primary key, we would not be able to access the customer information.
### Normal form 3
Because the table does not fulfill the requirements to be in normal form 2, it is naturally not in normal form 3 either.

## Exercise 2
To replace Customer Number as the customer part of the composite primary key, we instead use Customer Name, because it is a unique value since you can only have one customer attached in this table.

In regards to violations, you still end up hitting the same second normal form violation, because you still can't get customer information without the customer part of the primary key.

## Exercise 3

### Statement 1

### Statement 2

## Exercise 4
