<div align="center">

[**_``Go Back``_**](../README.md)

# AJAX (Asynchronous JavaScript and XML)

</div>

``AJAX`` stands for ``Asynchronous JavaScript And XML``. In a nutshell, it is the use of the ``XMLHttpRequest`` object to communicate with servers. It can send and receive information in various formats, including ``JSON``, ``XML``, ``HTML``, and text files. ``AJAX's`` most appealing characteristic is its ``asynchronous`` nature, which means it can communicate with the server, exchange data, and update the page without having to refresh the page.

The two major features of AJAX allow you to do the following:

- Make requests to the server without reloading the page
- Receive and work with data from the server

## ``XMLHttpRequest`` Object

The ``XMLHttpRequest`` object can be used to exchange data with a server behind the scenes. This means that it is possible to update parts of a web page, without reloading the whole page.

Syntax:
```JS
variable = new XMLHttpRequest();
```
**``XMLHttpRequest`` Object Methods**

- ``XMLHttpRequest()``:Creates a new ``XMLHttpRequest`` object
- ``abort()``:Cancels the current request
- ``getAllResponseHeaders()``:Returns header information
- ``getResponseHeader()``:Returns specific header information
- ``open(method,url,async,user,psw)``:Specifies the request
    - method: the request type ``GET`` or ``POST``
    - url: the file location
    - async: true (asynchronous) or false (synchronous)
    - user: optional user name
    - psw: optional password
- ``send()``:Sends the request to the server . Used for ``GET`` requests
- ``send(string)``:Sends the request to the server. Used for ``POST`` requests
- ``setRequestHeader()``:Adds a label/value pair to the header to be sent

**``XMLHttpRequest`` Object Properties**

- ``onreadystatechange``:Defines a function to be called when the readyState property changes
- ``readyState`` : Holds the status of the ``XMLHttpRequest``.
    - 0: request not initialized
    - 1: server connection established
    - 2: request received
    - 3: processing request
    - 4: request finished and response is ready
- ``responseText``:Returns the response data as a string
- ``responseXML``:Returns the response data as XML data
- ``status``:Returns the status-number of a request
    - 200: "OK"
    - 403: "Forbidden"
    - 404: "Not Found"

- ``statusText``:Returns the status-text (e.g. "OK" or "Not Found")

Example:
```JS
function run() 
{
    // Creating Our XMLHttpRequest object 
    const xhr = new XMLHttpRequest();
    // Making our connection  
    let url = 'https://jsonplaceholder.typicode.com/posts';
    xhr.open("GET", url, true);  
    // function execute after request is successful 
    xhr.onreadystatechange = function () 
    {
        if (this.readyState == 4 && this.status == 200) 
        {
            console.log(this.responseText);
        }
    }
    // Sending our request 
    xhr.send();
}
run();
```

## Using PHP & MySQL

**Example:**

Content of ``index.html``:

```HTML
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ajax</title>
</head>

<body>
    <script>
        function run() 
        {
            let id = document.getElementById("Id").value;
            // Creating Our XMLHttpRequest object 
            const xhr = new XMLHttpRequest();
            // Making our connection  
            let url = 'request.php?id='+id;
            xhr.open("GET", url, true);
            // function execute after request is successful 
            xhr.onreadystatechange = function () 
            {
                if (this.readyState == 4 && this.status == 200) 
                {
                    let data = JSON.parse(this.responseText);
                    let result = document.getElementById("result").innerHTML = "Name: " + data[0][1] +"<br>"+ "Roll: "+data[0][2];
                    console.table(data);
                }
            }
            // Sending our request 
            xhr.send();
        }
    </script>
    <label>Enter Id</label>
    <input type="text" id="Id">
    <br>
    <input type="button" value="Fetch" onclick="run()">
    <div id="result"></div>
</body>

</html>
```

Content of ``request.php``:

```PHP
<?php
$id = $_GET["id"];
$servername = "localhost";
$database = "mmc";
$username = "root";
$password = "prashant1234";
// Create connection
$conn = mysqli_connect($servername, $username, $password, $database);
// Check connection
if (!$conn) 
{
    die("Connection failed: " . mysqli_connect_error());
}
// Attempt select query execution
$sql = "SELECT * FROM student WHERE id = $id";
$result = mysqli_query($conn, $sql);

if (mysqli_num_rows($result) > 0) 
{
  // output data of each row
  $rows = mysqli_fetch_all($result);
  $JSON = json_encode($rows);
  echo $JSON;
}
else 
{
  echo "0 results";
}
mysqli_close($conn);
?>
```