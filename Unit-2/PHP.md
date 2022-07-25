<div align="center">

[**_``Go Back``_**](../README.md)

# PHP

</div>

## Introduction to Server Side Scripting Language

Server-side scripts are discrete blocks of program code that execute on a web server (as opposed to a web client) computer. They are generally used to create dynamic web pages. This means that the page displayed to the user does not exist as a document on the server in its own right, and is only brought into existence in response to a user request. Often, a server-side script provides the interface between a web-based user interface and a database that resides on a web server.

> Web servers are used to execute server-side scripting. They are basically used to create dynamic pages. It can also access the file system residing at the webserver. A server-side environment that runs on a scripting language is a web server. 

Early server-side scripts were almost always ``C`` programs, ``Perl`` scripts or shell scripts which were accessed via the ``Common Gateway Interface (CGI)``. Today these scripts, together with scripts created in more recent web application programming environments such as ``ASP`` or ``PHP``, can be executed directly by the web server itself, or through the use of server extensions. Direct execution is usually faster, as the involvement of a separate interpreter is not required. The following technologies are currently used to create web applications using server-side scripts:

- ``PHP`` - a widely-used scripting language originally created by ``Rasmus Lerdorf`` in ``1995``, and now maintained by the PHP Group. PHP originally stood for Personal Home Pages, although the acronym is now understood to stand (somewhat recursively) for PHP: Hypertext Preprocessor. PHP is free software released under the PHP License, and is especially suited to web development. As with other server side scripting languages, PHP code can be embedded into HTML or XHTML documents and is executed on the server to generate dynamic web content. The current version of PHP is version 5, with version 6 currently under development. PHP is frequently used together with MySQL, and is one of the key technologies in the WAMP (Windows, Apache, MySQL and PHP) and LAMP (Linux, Apache, MySQL and PHP) web application architectures, although the "P" may also refer to Perl or Python.

- ``Python`` - a general-purpose high-level programming language conceived in the late ``1980s`` by ``Guido van Rossum`` that supports multiple programming paradigms (primarily object-oriented, imperative and functional), and is often used as a scripting language for web applications. The language is now maintained by the Python Software Foundation. The current version (3.0) was released in December 2008. Python is a standard component of several operating systems, including most Linux distributions.

- ``Active Server Pages (ASP)`` - a server-side scripting environment from ``Microsoft``, first released in ``1996``, that is used to create dynamically generated web pages. The files produced are essentially HTML documents with ASP scripts embedded within them, and a file extension of .asp. Scripts are usually written in VBScript (although other scripting languages such as Jscript or JavaScript can also be used), and interpreted by the server at run-time. ASP will normally run only on Microsoft servers, although third party vendors have produced versions that run on other platforms.

- ``JavaServer Pages (JSP)`` - a Java technology similar to ASP that is used to create dynamically generated web pages by embedding Java programming code in HTML or XHTML documents. JSP was ``Sun Microsystems'`` response to ASP. A JavaServerPage is compiled into a Java servlet by an application server, rather than being interpreted like "Classic" ASP (a servlet is a Java program that executes on the server to create dynamic web pages).

## PHP Introduction

The term PHP is an acronym for ``PHP: Hypertext Preprocessor``. PHP is a server-side scripting language designed specifically for web development. It is open-source which means it is free to download and use. It is very simple to learn and use. The files have the extension ``.php``. It was originally created by ``Rasmus Lerdorf`` in ``1995``, and now maintained by the PHP Group.

- PHP code is executed in the server.
- It can be integrated with many databases such as Oracle, Microsoft SQL Server, MySQL, PostgreSQL, Sybase, Informix.
- It is powerful to hold a content management system like WordPress and can be used to control user access.
- It supports main protocols like HTTP Basic, HTTP Digest, IMAP, FTP, and others.
Websites like www.facebook.com, www.yahoo.com are also built on PHP.
- One of the main reasons behind this is that PHP can be easily embedded in HTML files and HTML codes can also be written in a PHP file.
- The thing that differentiates PHP from the client-side language like HTML is, PHP codes are executed on the server whereas HTML codes are directly rendered on the browser. PHP codes are first executed on the server and then the result is returned to the browser.
- The only information that the client or browser knows is the result returned after executing the PHP script on the server and not the actual PHP codes present in the PHP file. Also, PHP files can support other client-side scripting languages like CSS and JavaScript.

## Basic PHP Syntax

A PHP script can be placed anywhere in the document.

A PHP script starts with ``<?php`` and ends with ``?>``:

```PHP
<?php
// PHP code goes here
?>
```
The default file extension for PHP files is ``.php``.

A PHP file normally contains HTML tags, and some PHP scripting code.

Below, we have an example of a simple PHP file, with a PHP script that uses a built-in PHP function "echo" to output the text "Hello World!" on a web page:

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <?php echo "Hello World!";?>
</body>
</html>
```

## Comments in PHP

A comment in PHP code is a line that is not executed as a part of the program. Its only purpose is to be read by someone who is looking at the code.

Comments can be used to:

- Let others understand your code
- Remind yourself of what you did - Most programmers have experienced coming back to their own work a year or two later and having to re-figure out what they did. Comments can remind you of what you were thinking when you wrote the code

PHP supports several ways of commenting:

**single-line comments:**
```PHP
<?php
// This is a single-line comment
# This is also a single-line comment
?>
```

**multi-line comments:**
```PHP
<?php
/*
This is a multiple-lines comment block
that spans over multiple
lines
*/
?>
```
## Variable

In PHP, a variable starts with the ``$`` sign, followed by the name of the variable:

**Example:**

```PHP
<?php
$txt = "Hello world!";
$x = 5;
$y = 10.5;
?> 
```
> Note: When you assign a text value to a variable, put quotes around the value.

> Note: Unlike other programming languages, PHP has no command for declaring a variable. It is created the moment you first assign a value to it.

**Rules for PHP variables:**

- A variable starts with the ``$`` sign, followed by the name of the variable
- A variable name must start with a letter or the underscore character
- A variable name cannot start with a number
- A variable name can only contain alpha-numeric characters and underscores (``A-z``, ``0-9``, and ``_`` )
- Variable names are case-sensitive (``$age`` and ``$AGE`` are two different variables)

## PHP Control Structure
PHP supports a number of traditional programming constructs for controlling the flow of execution of a program.

Conditional statements, such as if/else and switch, allow a program to execute different pieces of code, or none at all, depending on some condition. Loops, such as while and for, support the repeated execution of particular code.

### PHP Conditional Statements
Very often when you write code, you want to perform different actions for different conditions. You can use conditional statements in your code to do this.

In PHP we have the following conditional statements:

* ``if statement`` - executes some code if one condition is true
* ``if...else statement`` - executes some code if a condition is true and another code if that condition is false
* ``if...elseif...else statement`` - executes different codes for more than two conditions
* ``switch statement`` - selects one of many blocks of code to be executed
 
#### **if statement**
The ``if`` statement executes some code if one condition is true.

Syntax:

```PHP
if (condition) 
{
  Statements;
}
```

#### **if...else statement**
The ``if...else`` statement executes some code if a condition is true and another code if that condition is false.`

Syntax:

```PHP
if (condition) 
{
  Statements;
} 
else 
{
  Statements;
}
```

#### **if...elseif...else statement**
The ``if...elseif...else`` statement executes different codes for more than two conditions.

Syntax:

```PHP
if (condition) 
{
  Statements;
} 
elseif (condition) 
{
  Statements;
} 
else 
{
  Statements;
}
```
Example Program:

```PHP
<?php
$a = 10; 
$b = 45;
if ($a > $b) 
{
  echo "$a is Greater.";
} 
elseif ($b > $a) 
{
  echo "$b is Greater.";
} 
else 
{
  echo "Both are Equal";
}
?>
```

#### **switch statement**

The ``switch`` statement is used to perform different actions based on different conditions.

Syntax:

```PHP
switch (Expression) 
{
  case (value 1):
  {
    Statements;
    break;
  }
  case (value 2):
  {
    Statements;
    break;
  }
    ...
  default:
  {
    Statements;
  }
}
```
Example:

```PHP
<?php
$favcolor = "red";
switch ($favcolor) 
{
  case ("red"):
    echo "Your favorite color is red!";
    break;
  case ("blue"):
    echo "Your favorite color is blue!";
    break;
  case ("green"):
    echo "Your favorite color is green!";
    break;
  default:
    echo "Your favorite color is neither red, blue, nor green!";
}
?> 
```

### PHP Loops:

Loops are used to execute the same block of code again and again, as long as a certain condition is true.

In PHP, we have the following loop types:

* ``while``-loops through a block of code as long as the specified condition is true
* ``do...while``-loops through a block of code once, and then repeats the loop as long as the specified condition is true
* ``for``-loops through a block of code a specified number of times
* ``foreach``-loops through a block of code for each element in an array

#### **``while`` Loop**

The ``while`` loop executes a block of code as long as the specified condition is true.

Syntax:
```PHP
while (condition) 
{
  Statements;
}
```

Example:
```PHP
<?php
$x = 1;
while($x <= 5) 
{
  echo "The number is: $x <br>";
  $x++;
}
?>
```

#### **``do while`` Loop**

The ``do...while`` loop - Loops through a block of code once, and then repeats the loop as long as the specified condition is true.The ``do...while`` loop will always execute the block of code once, it will then check the condition, and repeat the loop while the specified condition is true.

Syntax:
```PHP
do 
{
  Statements;
} while (condition); 
```

Example:
```PHP
<?php
$x = 1;
do
{
  echo "The number is: $x <br>";
  $x++;
} while ($x <= 5);
?> 
```

#### **``for`` Loop**

The ``for`` loop is used when you know in advance how many times the script should run.

Syntax:
```PHP
for (init counter; test counter; increment counter) 
{
  Statements;
} 
```

Example:
```PHP
<?php
for ($x = 0; $x <= 10; $x++) 
{
  echo "The number is: $x <br>";
}
?> 
```
### PHP Break and Continue

#### **PHP Break**

``break`` statement breaks the execution of the current for, while, do-while, switch, and for-each loop. If you use break inside inner loop, it breaks the execution of inner loop only.

Example:
>This example jumps out of the loop when x is equal to 4:
```PHP
<?php
for ($x = 0; $x < 10; $x++) 
{
  if ($x == 4) 
  {
    break;
  }
  echo "The number is: $x <br>";
}
?> 
```

#### **PHP Continue**

``continue`` statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.

Example:
>This example skips the value of 4
```PHP
<?php
for ($x = 0; $x < 10; $x++) 
{
  if ($x == 4) 
  {
    continue;
  }
  echo "The number is: $x <br>";
}
?> 
```

## PHP Array

An array is a special variable, which can hold more than one value at a time. An array can hold many values under a single name, and you can access the values by referring to an index number.

In PHP, the ``array()`` function is used to create an array:`

```PHP
array();
```

In PHP, there are three types of arrays:

* ``Indexed arrays`` - Arrays with a numeric index

  ```PHP
  <?php
  $cars = array("Volvo", "BMW", "Toyota");
  echo "I like " . $cars[0] . ", " . $cars[1] . " and " . $cars[2] . ".";
  ?> 
  ```

* ``Associative arrays`` - Arrays with named keys

  ```PHP
  <?php
  $age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");
  echo "Peter is " . $age['Peter'] . " years old.";
  ?> 
  ```

* ``Multidimensional arrays`` - Arrays containing one or more arrays

  ```PHP
  <?php
  $cars = array (
    array("Volvo",22,18),
    array("BMW",15,13),
    array("Saab",5,2),
    array("Land Rover",17,15)
  );
  echo $cars[0][0].": In stock: ".$cars[0][1].", sold: ".$cars[0][2].".<br>";
  echo $cars[1][0].": In stock: ".$cars[1][1].", sold: ".$cars[1][2].".<br>";
  echo $cars[2][0].": In stock: ".$cars[2][1].", sold: ".$cars[2][2].".<br>";
  echo $cars[3][0].": In stock: ".$cars[3][1].", sold: ".$cars[3][2].".<br>";
  ?> 
  ```

**Sort Functions For Arrays**

* ``sort()`` - sort arrays in ascending order
* ``rsort()`` - sort arrays in descending order
* ``asort()`` - sort associative arrays in ascending order, according to the value
* ``ksort()`` - sort associative arrays in ascending order, according to the key
* ``arsort()`` - sort associative arrays in descending order, according to the value
* ``krsort()`` - sort associative arrays in descending order, according to the key

## For Each Loop

The ``foreach`` loop works only on arrays, and is used to loop through each key/value pair in an array.

Syntax:
```PHP
foreach ($array as $value) 
{
  Statements;
} 
```

Example:
```PHP
<?php
$colors = array("red", "green", "blue", "yellow");
foreach ($colors as $value) 
{
  echo "$value <br>";
}
?> 
```

## Functions

The real power of ``PHP`` comes from its functions.

PHP has more than 1000 built-in functions, and in addition you can create your own custom functions.

* ``Built-in Functions: ``PHP has over 1000 built-in functions that can be called directly, from within a script, to perform a specific task.
* ``User Defined Functions: ``Besides the built-in PHP functions, it is possible to create your own functions.
  * A function is a block of statements that can be used repeatedly in a program.
  * A function will not execute automatically when a page loads.
  * A function will be executed by a call to the function.

**Create a User Defined Function in PHP**

A user-defined function declaration starts with the word function:

Syntax:

```PHP
function functionName(arguments) 
{
  Statements;
  return(value);
} 
```
Example:

```PHP
<?php
function addNumbers(int $a, int $b) 
{
  return $a + $b;
}
echo addNumbers(5, 5);
?>
```

## Form Handeling

The PHP superglobals ``$_GET`` and ``$_POST`` are used to collect form-data.`

Example
```PHP
<?php
if(isset($_POST["btn"]))
{
    $name=$_POST["name"];
    $email=$_POST["email"];
    echo "Welcome $name <br>" ;
    echo "Your Email is $email" ;
}
?>

<html>
<head>
    <title>form</title>
</head>
<body>
    <form action="#" method="post">
    <label>Name: </label>
    <input type="text" name="name"><br>
    <label>Email: </label>
    <input type="text" name="email"><br>
    <input type="submit" name="btn">
    </form>
</body>
</html>
```
### **PHP ``$_GET``**

PHP ``$_GET`` is a ``PHP`` super global variable which is used to collect form data after submitting an HTML form with ``method="get"``.

``$_GET`` can also collect data sent in the URL.

```
http://www.example.com/index.php?name1=value1&name2=value2
```

> The page and the encoded information are separated by the ``?`` character.


- The ``GET`` method produces a long string that appears in your server logs, in the browser's ``Location: box``.

- The ``GET`` method is restricted to send upto 1024 characters only.

- Never use ``GET`` method if you have password or other sensitive information to be sent to the server.

- ``GET`` can't be used to send binary data, like images or word documents, to the server.

- The data sent by ``GET`` method can be accessed using ``QUERY_STRING`` environment variable.

- The ``PHP`` provides ``$_GET`` associative array to access all the sent information using ``GET`` method.

### **PHP ``$_POST``**

PHP ``$_POST`` is a ``PHP`` super global variable which is used to collect form data after submitting an HTML form with ``method="post"``. $_POST is also widely used to pass variables.

- The ``POST`` method does not have any restriction on data size to be sent.

- The ``POST`` method can be used to send ``ASCII`` as well as binary data.

- The data sent by ``POST`` method goes through ``HTTP header`` so security depends on ``HTTP protocol``. By using Secure ``HTTP`` you can make sure that your information is secure.

- The ``PHP`` provides ``$_POST`` associative array to access all the sent information using POST method.

### **``GET`` vs. ``POST``**

Both ``GET`` and ``POST`` create an array (e.g. array( key1 => value1, key2 => value2, key3 => value3, ...)). This array holds ``key/value`` pairs, where keys are the names of the form controls and values are the input data from the user.

Both GET and POST are treated as ``$_GET`` and ``$_POST``. These are superglobals, which means that they are always accessible, regardless of scope - and you can access them from any function, class or file without having to do anything special.

``$_GET`` is an array of variables passed to the current script via the URL parameters.

``$_POST`` is an array of variables passed to the current script via the HTTP POST method.

### When to use ``GET``?

Information sent from a form with the ``GET`` method is visible to everyone (all variable names and values are displayed in the URL). ``GET`` also has limits on the amount of information to send. The limitation is about 2000 characters. However, because the variables are displayed in the URL, it is possible to bookmark the page. This can be useful in some cases.

``GET`` may be used for sending non-sensitive data.

>Note: ``GET`` should NEVER be used for sending passwords or other sensitive information!

### When to use ``POST``?

Information sent from a form with the ``POST`` method is invisible to others (all names/values are embedded within the body of the ``HTTP`` request) and has no limits on the amount of information to send.

Moreover ``POST`` supports advanced functionality such as support for multi-part binary input while uploading files to server.

However, because the variables are not displayed in the URL, it is not possible to bookmark the page.

>Note: Developers prefer ``POST`` for sending form data.

## PHP ``$_REQUEST``

PHP ``$_REQUEST`` is a ``PHP`` super global variable which is used to collect data after submitting an HTML form.

It is an associative array that by default contains the contents of ``$_GET``, ``$_POST`` and ``$_COOKIE``.

**Uses of PHP ``$_REQUEST``**

- The PHP ``$_REQUEST`` is a PHP superglobal variable that is used to collect the data after submitting the HTML forms as the $_REQUEST variable is useful to read the data from the submitted HTML open forms.

- ``$_REQUEST`` is an associative array that by default contains contents of an ``$_GET``,``$_POST``, and ``$_COOKIE``.

- The variables in a ``$_REQUEST`` super variable are obtained to the HTML scripts through ``GET``, ``POST``, and ``COOKIE`` inputs, so it could be changed by the remotely associated user and can’t be trusted again.

- The presence ``$_REQUEST`` variable and the suited orders of ``$_REQUEST`` are variables listed in the array is declared similar to the PHP request_order, and variables_order configuration directives are it.

- PHP ``$_REQUEST`` is the featuring PHP superglobal variable which is used to collect data after submitting the HTML forms in the browser.

- PHP’s ``$_REQUEST`` is widely used to collect information that is after submitting from HTML browsed forms.

- The ``$_REQUEST`` function is used to get the form information sent with its ``POST`` method and the other ``GET`` method.

## PHP ``date()`` function
PHP ``date()`` function is an in-built function that simplify working with date data types. The PHP date function is used to format a date or time into a human readable format. It can be used to display the date of article was published. record the last updated a data in a database.

The ``date()`` function formats a local date and time, and returns the formatted date string.

**Syntax**

```PHP
date($format, $timestamp);
```

**Parameters**

- ``format`` (Mandatory) : This is a format string specifying the format in which you want the output date string to be.

- ``timestamp`` (Optional) : This is an integer value representing the timestamp of the required date.

**Example**

Print current date time:

```PHP
<?php
date_default_timezone_set("Asia/Kathmandu");
$datetime = date('d-m-y h:i:s',time());
echo $datetime
?>
``` 

## PHP include file

The ``include()`` and ``require()`` statement allow you to include the code contained in a PHP file within another PHP file. Including a file produces the same result as copying the script from the file specified and pasted into the location where it is called.

You can save a lot of time and work through including files — Just store a block of code in a separate file and include it wherever you want using the ``include()`` and ``require()`` statements instead of typing the entire block of code multiple times. A typical example is including the header, footer and menu file within all the pages of a website.

> It is possible to insert the content of one PHP file into another PHP file (before the server executes it), with the ``include`` or ``require`` statement.

The include and require statements are identical, except upon failure:

- ``require`` will produce a fatal error ``(E_COMPILE_ERROR)`` and stop the script.

- ``include`` will only produce a warning ``(E_WARNING)`` and the script will continue

The basic syntax of the ``include()`` and ``require()`` statement can be given with:

```PHP
include("path/to/filename");
require("path/to/filename");
```

**Difference Between ``include`` and ``require`` Statements**

You might be thinking if we can include files using the ``include()`` statement then why we need ``require()``. Typically the ``require()`` statement operates like ``include()``.

The only difference is the ``include()`` statement will only generate a PHP warning but allow script execution to continue if the file to be included can't be found, whereas the ``require()`` statement will generate a fatal error and stops the script execution.

## File Handeling

File handling is needed for any application. For some tasks to be done file needs to be processed. File handling in PHP is similar as file handling is done by using any programming language like C. PHP has many functions to work with normal files. Those functions are:

### ``fopen()`` 

PHP ``fopen()`` function is used to open a file. First parameter of ``fopen()`` contains name of the file which is to be opened and second parameter tells about mode in which file needs to be opened, e.g.,

```PHP
<?php
$file = fopen(“file.txt”,'w');
?>
```
Files can be opened in any of the following modes :

* ``w`` – Opens a file for write only. If file not exist then new file is created and if file already exists then contents of file is erased.
* ``r`` – File is opened for read only.
* ``a`` – File is opened for write only. File pointer points to end of file. Existing data in file is preserved.
* ``w+`` – Opens file for read and write. If file not exist then new file is created and if file already exists then contents of file is erased.
* ``r+`` – File is opened for read/write.
* ``a+`` – File is opened for write/read. File pointer points to end of file. Existing data in file is preserved. If file is not there then new file is created.
* ``x`` – New file is created for write only.

### ``fread()``

After file is opened using ``fopen()`` the contents of data are read using ``fread()``. It takes two arguments. One is ``file pointer`` and another is ``file size`` in bytes, e.g.,

```PHP
<?php
$filename = "file.txt";
$file = fopen( $filename, 'r' );
$size = filesize( $filename );
$filedata = fread( $file, $size );
?>
```

### ``fwrite()``

New file can be created or text can be appended to an existing file using ``fwrite()`` function. Arguments for ``fwrite()`` function are ``file pointer`` and ``text`` that is to written to file. It can contain optional third argument where ``length of text`` to written is specified, e.g.,

```PHP
<?php
$filename = "file.txt";
$file = fopen( $filename, 'w');
$text = "I am Prashant Bhandari\n";
fwrite($file, $text);
?>
```

### ``fclose()``

file is closed using ``fclose()`` function. Its argument is file which needs to be closed, e.g.,

```PHP
<?php
$file = fopen("file.txt", 'r');
//some code to be executed
fclose($file);
?>
```


## File Uploading

``PHP`` allows you to upload single and multiple files through few lines of code only.

``PHP`` file upload features allows you to upload binary and text files both. Moreover, you can have the full control over the file to be uploaded through ``PHP`` authentication and file operation functions.

**PHP File Upload Example**

Content of ``upload.html``:

```HTML
<form action="action.php" method="post" enctype="multipart/form-data">  
    Select File:  
    <input type="file" name="file"/>  
    <input type="submit" value="Upload Image" name="submit"/>  
</form>  
```
Content of ``action.php``:

```PHP
<?php  
$target_path = "uploads/";  
$target_path = $target_path.basename( $_FILES['file']['name']);   
if(move_uploaded_file($_FILES['file']['tmp_name'], $target_path)) 
{  
    ecsho "File uploaded successfully!";  
} 
else
{  
    echo "Sorry, file not uploaded, please try again!";  
}  
?>  
```

### PHP ``$_FILES``

The PHP global ``$_FILES`` contains all the information of file. By the help of ``$_FILES`` global, we can get file name, file type, file size, temp file name and errors associated with file.

Here, we are assuming that file name is ``filename``.

- ``$_FILES['filename']['name']``: returns file name.

- ``$_FILES['filename']['type']``: returns MIME type of the file.

- ``$_FILES['filename']['size']``: returns size of the file (in bytes).

- ``$_FILES['filename']['tmp_name']``: returns temporary file name of the file which was stored on the server.

- ``$_FILES['filename']['error']``: returns error code associated with this file.

**``move_uploaded_file()`` function**

The ``move_uploaded_file()`` function moves the uploaded file to a new location. The ``move_uploaded_file()`` function checks internally if the file is uploaded thorough the ``POST`` request. It moves the file if it is uploaded through the ``POST`` request.

Syntax:

```PHP
bool move_uploaded_file ( string $filename , string $destination )  
```

## PHP Session

When you work with an application, you open it, do some changes, and then you close it. This is much like a Session. The computer knows who you are. It knows when you start the application and when you end. But on the internet there is one problem: the web server does not know who you are or what you do, because the HTTP address doesn't maintain state.

Session variables solve this problem by storing user information to be used across multiple pages (e.g. username, favorite color, etc). By default, session variables last until the user closes the browser.

So; Session variables hold information about one single user, and are available to all pages in one application.

**Start a Session:**

A session is started with the ``session_start()`` function.

Session variables are set with the PHP global variable: ``$_SESSION``.

```PHP
<?php
// Start the session
session_start();
?>
<!DOCTYPE html>
<html>
  <body>
    <?php
    // Set session variables
    $_SESSION["favcolor"] = "green";
    $_SESSION["favanimal"] = "cat";
    echo "Session variables are set.";
    ?>
  </body>
</html> 
```

>The ``session_start()`` function must be the very first thing in your document. Before any HTML tags.

**Destroy a PHP Session**

To remove all global session variables and destroy the session, use ``session_unset()`` and ``session_destroy()``

Here is the example to unset a single variable −

```PHP
<?php
  unset($_SESSION['counter']);
?>
```

Here is the call which will destroy all the session variables −

```PHP
<?php
  session_destroy();
?>
```


## Sending Email

The ``mail()`` function allows you to send emails directly from a script.

**Syntax:**

```PHP
mail(to,subject,message,headers,parameters);
```

**Parameters**

- ``to``: Required. Specifies the receiver / receivers of the email

- ``subject``: Required. Specifies the subject of the email. This parameter cannot contain any newline characters

- ``message``: Required. Defines the message to be sent. Each line should be separated with a LF (\n). Lines should not exceed 70 characters

- ``headers``: Optional. Specifies additional headers, like From, Cc, and Bcc. The additional headers should be separated with a CRLF (\r\n)

- ``parameters``: Optional. Specifies an additional parameter to the send mail program

As soon as the ``mail`` function is called PHP will attempt to send the email then it will return ``true`` if successful or ``false`` if it is failed.

Multiple recipients can be specified as the first argument to the ``mail()`` function in a comma separated list.

**Example**
```PHP
<?php
$to = "somebody@example.com";
$message = "My subject";
$txt = "Hello world!";
$headers = "From: webmaster@example.com" . "\r\n" .
"CC: somebodyelse@example.com";
$mailstatus = mail ($to,$subject,$message,$header);         
if( $mailstatus == true )
{
    echo "Message sent successfully...";
}
else 
{
    echo "Message could not be sent...";
}
?>
```

## PHP cookie

A cookie is created with the ``setcookie()`` function.

Syntax:

```PHP
setcookie(name, value, expire, path, domain, secure, httponly);
```
>Only the ``name`` parameter is required. All other parameters are optional.

**PHP Create/Retrieve a Cookie**

The following example creates a cookie named ``"user"`` with the value ``"Prashant Bhandari"``. The cookie will expire after 30 days (86400 * 30). The ``"/"`` means that the cookie is available in entire website (otherwise, select the directory you prefer).

We then retrieve the value of the cookie ``"user"`` (using the global variable ``$_COOKIE``). We also use the ``isset()`` function to find out if the cookie is set:

```PHP
<?php
$cookie_name = "user";
$cookie_value = "Prashant Bhandari";
setcookie($cookie_name, $cookie_value, time() + (86400 * 30), "/"); // 86400 = 1 day
?>
<html>
    <body>
    <?php
    if(!isset($_COOKIE[$cookie_name]))
    {
        echo "Cookie named '" . $cookie_name . "' is not set!";
    } 
    else 
    {
        echo "Cookie '" . $cookie_name . "' is set!<br>";
        echo "Value is: " . $_COOKIE[$cookie_name];
    }
    ?>
    </body>
</html> 
```
>**Note:** The ``setcookie()`` function must appear BEFORE the ``<html>`` tag.

>**Note:** The value of the cookie is automatically URLencoded when sending the cookie, and automatically decoded when received (to prevent URLencoding, use ``setrawcookie()`` instead).

**Modify a Cookie Value**

To modify a cookie, just set (again) the cookie using the ``setcookie()`` function:

Example:
```PHP
<?php
$cookie_name = "user";
$cookie_value = "Sachin Khadka";
setcookie($cookie_name, $cookie_value, time() + (86400 * 30), "/"); // 86400 = 1 day
?>
<html>
    <body>
    <?php
    if(!isset($_COOKIE[$cookie_name]))
    {
        echo "Cookie named '" . $cookie_name . "' is not set!";
    } 
    else 
    {
        echo "Cookie '" . $cookie_name . "' is set!<br>";
        echo "Value is: " . $_COOKIE[$cookie_name];
    }
    ?>
    </body>
</html> 
```

**Delete a Cookie**

To delete a cookie, use the ``setcookie()`` function with an expiration date in the past:

```PHP
<?php
// set the expiration date to one hour ago
setcookie("user", "", time() - 3600);
?>
<html>
    <body>
    <?php
    echo "Cookie 'user' is deleted.";
    ?>
    </body>
</html> 
```

**Check if Cookies are Enabled**

The following example creates a small script that checks whether cookies are enabled. First, try to create a test cookie with the ``setcookie()`` function, then count the ``$_COOKIE`` array variable:

```PHP
<?php
setcookie("test_cookie", "test", time() + 3600, '/');
?>
<html>
    <body>
    <?php
    if(count($_COOKIE) > 0) 
    {
        echo "Cookies are enabled.";
    } 
    else
    {
        echo "Cookies are disabled.";
    }
    ?>
    </body>
</html> 
```