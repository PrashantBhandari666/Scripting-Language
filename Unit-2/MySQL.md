<div align="center">

[**_``Go Back``_**](../README.md)

# MySQL

</div>

## Introduction To MySQL

With PHP, you can connect to and manipulate databases.

MySQL is the most popular database system used with PHP.

* MySQL is a database system used on the web
* MySQL is a database system that runs on a server
* MySQL is ideal for both small and large applications
* MySQL is very fast, reliable, and easy to use
* MySQL uses standard SQL
* MySQL compiles on a number of platforms
* MySQL is free to download and use
* MySQL is developed, distributed, and supported by Oracle Corporation
* MySQL is named after co-founder Monty Widenius's daughter: My

## PHP MySQL Connect with Database

In PHP you can easily do this using the ``mysqli_connect()`` function. All communication between PHP and the MySQL database server takes place through this connection. Here're the basic syntaxes for connecting to MySQL using MySQLi and PDO extensions:

Syntax: MySQLi, Procedural way
```PHP
$conn = mysqli_connect("hostname", "username", "password", "database");
```

Syntax: MySQLi, Object Oriented way
```PHP
$conn = new mysqli("hostname", "username", "password", "database");
```

Syntax: PHP Data Objects (PDO) way
```PHP
$conn = new PDO("mysql:host=hostname;dbname=database", "username", "password"); 
```
**Example:**
```PHP
<?php
$servername = "localhost";
$database = "mmc";
$username = "root";
$password = "";
// Create connection
$conn = mysqli_connect($servername, $username, $password, $database);
// Check connection
if (!$conn) 
{
    die("Connection failed: " . mysqli_connect_error());
}
echo "Connected successfully";
mysqli_close($conn);
?>
```

## Closing a Connection

The connection will be closed automatically when the script ends. To close the connection before, use the following:

```PHP
mysqli_close($conn); 
```

## MySQL Data Types

Properly defining the fields in a table is important to the overall optimization of your database. You should use only the type and size of field you really need to use. For example, do not define a field 10 characters wide, if you know you are only going to use 2 characters. These type of fields (or columns) are also referred to as data types, after the type of data you will be storing in those fields.

``MySQL`` uses many different data types broken into three categories −

- Numeric
- Date and Time
- String Types.

### **Numeric Data Types**
``MySQL`` uses all the standard ``ANSI`` SQL numeric data types, so if you're coming to ``MySQL`` from a different database system, these definitions will look familiar to you.

The following list shows the common numeric data types and their descriptions −

- ``INT`` − A normal-sized integer that can be signed or unsigned. If signed, the allowable range is from -2147483648 to 2147483647. If unsigned, the allowable range is from 0 to 4294967295. You can specify a width of up to 11 digits.

- ``TINYINT`` − A very small integer that can be signed or unsigned. If signed, the allowable range is from -128 to 127. If unsigned, the allowable range is from 0 to 255. You can specify a width of up to 4 digits.

- ``SMALLINT`` − A small integer that can be signed or unsigned. If signed, the allowable range is from -32768 to 32767. If unsigned, the allowable range is from 0 to 65535. You can specify a width of up to 5 digits.

- ``MEDIUMINT`` − A medium-sized integer that can be signed or unsigned. If signed, the allowable range is from -8388608 to 8388607. If unsigned, the allowable range is from 0 to 16777215. You can specify a width of up to 9 digits.

- ``BIGINT`` − A large integer that can be signed or unsigned. If signed, the allowable range is from -9223372036854775808 to 9223372036854775807. If unsigned, the allowable range is from 0 to 18446744073709551615. You can specify a width of up to 20 digits.

- ``FLOAT(M,D)`` − A floating-point number that cannot be unsigned. You can define the display length (M) and the number of decimals (D). This is not required and will default to 10,2, where 2 is the number of decimals and 10 is the total number of digits (including decimals). Decimal precision can go to 24 places for a FLOAT.

- ``DOUBLE(M,D)`` − A double precision floating-point number that cannot be unsigned. You can define the display length (M) and the number of decimals (D). This is not required and will default to 16,4, where 4 is the number of decimals. Decimal precision can go to 53 places for a DOUBLE. REAL is a synonym for DOUBLE.

- ``DECIMAL(M,D)`` − An unpacked floating-point number that cannot be unsigned. In the unpacked decimals, each decimal corresponds to one byte. Defining the display length (M) and the number of decimals (D) is required. NUMERIC is a synonym for DECIMAL.

### **Date and Time Types**
The MySQL date and time datatypes are as follows −

- ``DATE`` − A date in ``YYYY-MM-DD`` format, between ``1000-01-01`` and ``9999-12-31``. For example, December 30th, 1973 would be stored as ``1973-12-30``.

- ``DATETIME`` − A date and time combination in ``YYYY-MM-DD HH:MM:SS`` format, between ``1000-01-01 00:00:00`` and ``9999-12-31 23:59:59``. For example, 3:30 in the afternoon on December 30th, 1973 would be stored as ``1973-12-30 15:30:00``.

- ``TIMESTAMP`` − A timestamp between midnight, January 1st, 1970 and sometime in 2037. This looks like the previous DATETIME format, only without the hyphens between numbers; 3:30 in the afternoon on December 30th, 1973 would be stored as ``19731230153000`` ( ``YYYYMMDDHHMMSS`` ).

- ``TIME`` − Stores the time in a ``HH:MM:SS`` format.

- ``YEAR(M)`` − Stores a year in a 2-digit or a 4-digit format. If the length is specified as 2 (for example YEAR(2)), YEAR can be between ``1970`` to ``2069`` (70 to 69). If the length is specified as 4, then YEAR can be ``1901`` to ``2155``. The default length is 4.

### **String Types**
Although the numeric and date types are fun, most data you'll store will be in a string format. This list describes the common string datatypes in ``MySQL``.

- ``CHAR(M)`` − A fixed-length string between 1 and 255 characters in length (for example ``CHAR(5)``), right-padded with spaces to the specified length when stored. Defining a length is not required, but the default is 1.

- ``VARCHAR(M)`` − A variable-length string between 1 and 255 characters in length. For example, ``VARCHAR(25)``. You must define a length when creating a VARCHAR field.

- ``BLOB`` or ``TEXT`` − A field with a maximum length of 65535 characters. BLOBs are "Binary Large Objects" and are used to store large amounts of binary data, such as images or other types of files. Fields defined as TEXT also hold large amounts of data. The difference between the two is that the sorts and comparisons on the stored data are case sensitive on BLOBs and are not case sensitive in TEXT fields. You do not specify a length with BLOB or TEXT.

- ``TINYBLOB`` or ``TINYTEXT`` − A BLOB or TEXT column with a maximum length of 255 characters. You do not specify a length with TINYBLOB or TINYTEXT.

- ``MEDIUMBLOB`` or ``MEDIUMTEXT`` − A BLOB or TEXT column with a maximum length of 16777215 characters. You do not specify a length with MEDIUMBLOB or MEDIUMTEXT.

- ``LONGBLOB`` or ``LONGTEXT`` − A BLOB or TEXT column with a maximum length of 4294967295 characters. You do not specify a length with LONGBLOB or LONGTEXT.

- ``ENUM`` − An enumeration, which is a fancy term for list. When defining an ENUM, you are creating a list of items from which the value must be selected (or it can be NULL). For example, if you wanted your field to contain "A" or "B" or "C", you would define your ENUM as ``ENUM ('A', 'B', 'C')`` and only those values (or NULL) could ever populate that field.

## MySQL Insert

The ``INSERT INTO`` statement is used to add new records to a MySQL table:

Syntax:
```SQL
INSERT INTO table_name (column1, column2,...) VALUES (value1, value3,...);
```

Example:
```SQL
INSERT INTO student (StudentID, FirstName, LastName, RollNo, City) 
VALUES (1, 'Prashant', 'Bhandari', 39, 'Birtamode');
```
```SQL
INSERT INTO student VALUES (4, 'Ram', 'Dahal', 67, 'Chandragadi');
```

Data can be entered into MySQL tables by executing SQL ``INSERT`` statement through PHP function ``mysql_query()``.

Example program:
```PHP
<?php
$servername = "localhost";
$database = "mmc";
$username = "root";
$password = "";
// Create connection
$conn = mysqli_connect($servername, $username, $password, $database);
// Check connection
if (!$conn) 
{
    die("Connection failed: " . mysqli_connect_error());
}
// Attempt insert query execution
$sql = "INSERT INTO student VALUES (4, 'Ram', 'Dahal', 67, 'Chandragadi');";
if(mysqli_query($conn, $sql))
{
    echo "Records inserted successfully.";
} 
else
{
    echo "ERROR: Could not able to execute $sql. " . mysqli_error($conn);
}
mysqli_close($conn);
?>
```

## MySQL Select

The ``SELECT`` statement is used to select data from one or more tables:

Syntax:
```SQL
SELECT column_name(s) FROM table_name
```

or we can use the ``*`` character to select ALL columns from a table:

```SQL
SELECT * FROM table_name 
```

Example Program:
```PHP
<?php
$servername = "localhost";
$database = "mmc";
$username = "root";
$password = "";
// Create connection
$conn = mysqli_connect($servername, $username, $password, $database);
// Check connection
if (!$conn) 
{
    die("Connection failed: " . mysqli_connect_error());
}
// Attempt select query execution
$sql = "SELECT * FROM student";
$result = mysqli_query($conn, $sql);

if (mysqli_num_rows($result) > 0) 
{
  // output data of each row
  while($row = mysqli_fetch_assoc($result))
  {
    $id = $row['StudentID'];
    $fn = $row['FirstName'];
    $ln = $row['LastName'];
    $rn = $row['RollNo'];
    $city = $row['City'];
    echo "ID = $id Name  = $fn $ln Rollno = $rn City = $city";
    echo "<br>";
  }
} 
else 
{
  echo "0 results";
}
mysqli_close($conn);
?>
```
the function ``mysqli_num_rows()`` checks if there are more than zero rows returned.

If there are more than zero rows returned, the function ``mysqli_fetch_assoc()`` puts all the results into an associative array that we can loop through. The ``while()`` loop loops through the result set and outputs the data.

## MySQL Where Clause

The ``WHERE`` clause is used to filter records.

It is used to extract only those records that fulfill a specified condition.

**Syntax**

```SQL
SELECT (column1, column2, ...)FROM table_name
WHERE condition;
```

>Note: The WHERE clause is not only used in ``SELECT`` statements, it is also used in ``UPDATE``, ``DELETE``, etc.!

## MySQL Delete

The ``DELETE`` statement is used to delete records from a table:

Syntax:
```SQL
DELETE FROM table_name WHERE some_column = some_value 
```

Example:
```SQL
DELETE FROM student WHERE StudentID=3;
```

Example Program:

```PHP
<?php
$servername = "localhost";
$database = "mmc";
$username = "root";
$password = "";
// Create connection
$conn = mysqli_connect($servername, $username, $password, $database);
// Check connection
if (!$conn) 
{
    die("Connection failed: " . mysqli_connect_error());
}
// Attempt delete query execution
$sql = "DELETE FROM student WHERE StudentID=3;";
if(mysqli_query($conn, $sql))
{
    echo "Records deleted successfully.";
} else
{
    echo "ERROR: Could not able to execute $sql. " . mysqli_error($conn);
}
mysqli_close($conn);
?> 
```

## MySQL Update

The ``UPDATE`` statement is used to update existing records in a table:

Syntax:
```SQL
UPDATE table_name SET column1=value1, column2=value2,... 
WHERE some_column=some_value  
```

```SQL
UPDATE student SET FirstName="Yugesh" 
WHERE StudentID=2;
```

Example Program:

```PHP
<?php
$servername = "localhost";
$database = "mmc";
$username = "root";
$password = "";
// Create connection
$conn = mysqli_connect($servername, $username, $password, $database);
// Check connection
if (!$conn) 
{
    die("Connection failed: " . mysqli_connect_error());
}
// Attempt update query execution
$sql = "UPDATE student SET FirstName='Ram Bhadadur' WHERE StudentID=2;";
if(mysqli_query($conn, $sql))
{
    echo "Records updated successfully.";
}
else
{
    echo "ERROR: Could not able to execute $sql. " . mysqli_error($conn);
}
mysqli_close($conn);
?>
```

## MySQL Aggregate Function(Sum, Avg, Count etc)

### **Sum**

The ``SUM()`` function returns the total sum of a numeric column.

Syntax:

```SQL
SELECT SUM(column_name) FROM table_name
WHERE condition;
```

### **Avg**

The ``AVG()`` function returns the average value of a numeric column. 

Syntax:

```SQL
SELECT AVG(column_name) FROM table_name
WHERE condition;
```

### **Count**

The ``COUNT()`` function returns the number of rows that matches a specified criterion.

Syntax:

```SQL
SELECT COUNT(column_name) FROM table_name
WHERE condition;
```

**Others**

|       Funtions       |                Description                     |
|----------------------|------------------------------------------------|
| ``MIN()``            |It returns the minimum (lowest) value in a set. |
| ``MAX()``            |It returns the maximum (highest) value in a set.|
| ``GROUP_CONCAT()``   |It returns a concatenated string.               |

## MySQL Order By & Group By

### **MySQL Order By**

The ``ORDER BY`` keyword is used to sort the result-set in ascending or descending order.

The ``ORDER BY`` keyword sorts the records in ascending order by default. To sort the records in descending order, use the ``DESC`` keyword.

**Syntax**

```SQL
SELECT column1, column2, ... FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```
**Example**

```SQL
SELECT * FROM Customers
ORDER BY Country;
```

### **MySQL Group By**

The ``GROUP BY`` statement groups rows that have the same values into summary rows, like "find the number of customers in each country".

The GROUP BY statement is often used with aggregate functions (``COUNT()``, ``MAX()``, ``MIN()``, ``SUM()``, ``AVG()``) to group the result-set by one or more columns.

**Syntax**

```SQL
SELECT column1, column2, ... FROM table_name
GROUP BY column1, column2,...;
```

```SQL
SELECT * FROM Customers
GROUP BY Country;
```

## MySQL Subqueries

A MySQL subquery is a query nested within another query such as ``SELECT``, ``INSERT``, ``UPDATE`` or ``DELETE``. Also, a subquery can be nested within another subquery.

For example, the following query uses a subquery to return the employees who work in the offices located in the USA.

```SQL
SELECT lastName, firstName FROM employees
WHERE officeCode IN (SELECT officeCode FROM offices WHEREcountry = 'USA');
```

## MySQL Join

A ``JOIN`` clause is used to combine rows from two or more tables, based on a related column between them.

- ``INNER JOIN``: Returns records that have matching values in both tables
- ``LEFT JOIN``: Returns all records from the left table, and the matched records from the right table
- ``RIGHT JOIN``: Returns all records from the right table, and the matched records from the left table
- ``CROSS JOIN``: Returns all records from both tables