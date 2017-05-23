![GitHub Logo](https://s3.ap-south-1.amazonaws.com/greyatom-social/GreyAtom-logo.png)

### Using Joins

The SQL Joins clause is used to combine records from two or more tables in a database. A JOIN is a means for combining fields from two tables by using values common to each.

Now, lets join two tables Orders and OrderDetails

        SELECT CustomerID, OrderDate
        FROM Orders, OrderDetails
        WHERE  Orders.OrderID = OrderDetails.OrderID;

This would produce the following result.

| CustomerID | OrderDate |
| ---------- | --------- |
| 51 |	2017-03-20 |
| 71 |	2016-11-21 |
| 71 |	2016-12-29 |
| 71 |	2017-01-04 |
| 71 |	2017-03-28 |

Here, it is noticeable that the join is performed in the WHERE clause. Several operators can be used to join tables, such as =, <, >, <>, <=, >=, !=, BETWEEN, LIKE, and NOT; they can all be used to join tables. However, the most common operator is the equal to symbol.

There are different types of joins available in SQL −

- **INNER JOIN** − returns rows when there is a match in both tables.
- **LEFT JOIN** − returns all rows from the left table, even if there are no matches in the right table.
- **RIGHT JOIN** − returns all rows from the right table, even if there are no matches in the left table.
- **FULL JOIN** − returns rows when there is a match in one of the tables.
- **SELF JOIN** − is used to join a table to itself as if the table were two tables, temporarily renaming at least one table in the SQL statement.
- **CARTESIAN JOIN** − returns the Cartesian product of the sets of records from the two or more joined tables.