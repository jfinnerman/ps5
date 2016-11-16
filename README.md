# ps5
# DML continued
---

## INSERT
----
Insert, as the name implies, allows you to add records to a table. You should already be familiar with this command as you have used it to insert
many records into the store database.  The syntax is:

```sql
INSERT INTO table
column_list
VALUES (value1, value 2, ...);
```


## UPDATE
----

The `UPDATE` command is used to __update__ records.  IMPORTANT: Use `WHERE` clause!  The syntax is as follows:

```sql
UPDATE table
SET column='value'
WHERE [condition]
```

You can also update multiple column values by setting multiple columns as:
```sql
UPDATE table
SET column1='value1'
    column2='value2'
WHERE [condition]
```

TRY IT:  Update a customers phone number to: 614-223-2983.  (Pick one customer)

## DELETE 
---
The `DELETE` command removes records.  For example, suppose a customer demands to be removed from the database.  IMPORTANT: Do NOT forget the `WHERE` clause, else all records will be deleted.

```sql
DELETE FROM table
WHERE [condition]
```

What about referential integrity?  




## Exercises (using SQL)
---

1. INSERT 10 new customer into the database that has NOT made orders.
    
    INSERT INTO `unemath_Finnerman`.`Customers` (`customer_id`, `first_name`, `last_name`, `email`, `phone_number`, `zip`, `address`) VALUES ('555999333', 'Levi', 'Ellis', 'Lellis90@gmail.com', '8083244356', '43001', '805 Star Street');

    INSERT INTO `unemath_Finnerman`.`Customers` (`customer_id`, `first_name`, `last_name`, `email`, `phone_number`, `zip`, `address`) VALUES ('123456789', 'Olivia', 'Pope', 'Opope88@whitehouse.net', '2024561111', '20500', '1600 Pennsylvania Ave');

    
2. Update a customer's address as 'they have moved' since you added it.
3. Delete a customer that you recently added.
4. Update a manufacturer's website information.
5. Update one of the unknown categories.
6. Find all customers that have not made any orders (of course they are probably the ones you just added)
7. Select all products that customers from zip code 26034 have ordered.
8. What other queries can you form?  What other queries might be of interest to the owners of the store?  What queries might be of interest to the customers?

## More functions
---

Research the following, determine their functionality and syntax of use:

1. UPPER()
2. LOWER()
3. LTRIM()
4. RTRIM()
5. CONCAT()
6. LENGTH()
7. ISNULL()
8. LPAD()
9. RPAD()

## Triple joins
---

```sql
SELECT column(s)
FROM
    table1 A
        INNER JOIN
    table2 B
        ON A.commonField = B.commonField
        INNER JOIN 
    Table3 C
        ON B.commonField = C.commonField
WHERE (if needed)
```        

Next Time we will look at `VIEWS` and the `ALTER` table command including: 'add column', 'drop column', and 'modify column'.
---

### Assignment (Due One Week - Wednesday before Thanksgiving)

Create a datamodel (database) for the math department.  We need a database that can be used to track and advise students as well as 
aid in scheduling future classes.  The database should include students (include e.g., PIN, graduation year), whether they are major/minor, list of faculty advisors from the math department, and which classes the students have had and in which semester.  What do you recommend for a front-end interface to the database?  Are there  any other details of which you can think?


