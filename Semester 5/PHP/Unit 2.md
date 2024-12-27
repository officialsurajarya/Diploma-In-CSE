# Unit 2: PHP and MySQL

In this unit, we will learn how to interact with MySQL databases using PHP, which is a popular server-side scripting language. We will cover the basics of MySQL, how to connect to a MySQL database, and perform common operations such as creating a database, inserting data, deleting data, and retrieving data using PHP.

---

#### **2.1 Introduction to MySQL**

**MySQL** is an open-source relational database management system (RDBMS) that uses Structured Query Language (SQL) for accessing, managing, and manipulating data. It is widely used in web development alongside PHP to store and manage data.

**Key features of MySQL**:
- **Data storage**: Stores structured data in tables.
- **SQL queries**: Allows performing operations such as SELECT, INSERT, UPDATE, DELETE on data.
- **Client-server model**: MySQL operates in a client-server architecture, where the client (application) communicates with the MySQL server to access or modify data.
- **Open source**: MySQL is free and open-source software.

---

#### **2.2 Connecting to MySQL using PHP**

To interact with a MySQL database, we need to establish a connection between PHP and MySQL. PHP provides several ways to connect to MySQL, including the `mysqli` extension and the `PDO` extension. The `mysqli` extension is commonly used for MySQL interaction.

Here’s how you can connect to MySQL using the `mysqli` extension:

```php
<?php
$servername = "localhost";  // MySQL server address
$username = "root";         // MySQL username
$password = "";             // MySQL password
$dbname = "test";           // Name of the database

// Create connection
$conn = new mysqli($servername, $username, $password, $dbname);

// Check connection
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
echo "Connected successfully";
?>
```

**Explanation**:
- **$servername**: The address of the MySQL server (usually `localhost` for local development).
- **$username**: The username for MySQL (often `root` by default).
- **$password**: The password associated with the username.
- **$dbname**: The name of the database to connect to.

The `new mysqli()` function establishes a connection. If the connection fails, an error message is displayed.

---

#### **2.3 Creating a Database**

Once connected to MySQL, you can create a database. To create a database using PHP, use the `CREATE DATABASE` SQL query.

```php
<?php
// Create database
$sql = "CREATE DATABASE mydatabase";
if ($conn->query($sql) === TRUE) {
    echo "Database created successfully";
} else {
    echo "Error creating database: " . $conn->error;
}
?>
```

**Explanation**:
- The `CREATE DATABASE` query creates a new database named `mydatabase`.
- If the query is successful, it outputs a success message.

---

#### **2.4 Insertion of Data into MySQL Database**

To insert data into a MySQL database, you need to use the `INSERT INTO` SQL query. Here’s an example of how to insert data into a table:

```php
<?php
$sql = "INSERT INTO users (name, email) VALUES ('John Doe', 'john@example.com')";
if ($conn->query($sql) === TRUE) {
    echo "New record created successfully";
} else {
    echo "Error: " . $sql . "<br>" . $conn->error;
}
?>
```

**Explanation**:
- The `INSERT INTO` query inserts values into the `users` table. 
- In this example, data (name and email) is inserted into the `name` and `email` columns of the table.

---

#### **2.5 Deletion of Data from MySQL Database**

To delete data from a MySQL database, use the `DELETE FROM` SQL query. Here’s how to delete a record:

```php
<?php
$sql = "DELETE FROM users WHERE id = 1";
if ($conn->query($sql) === TRUE) {
    echo "Record deleted successfully";
} else {
    echo "Error deleting record: " . $conn->error;
}
?>
```

**Explanation**:
- The `DELETE FROM` query deletes a record from the `users` table where the `id` is 1.
- You can modify the `WHERE` clause to delete records based on other conditions.

---

#### **2.6 Retrieval of Data from MySQL Database**

To retrieve data from a MySQL database, use the `SELECT` SQL query. Here’s an example of how to fetch and display data:

```php
<?php
$sql = "SELECT id, name, email FROM users";
$result = $conn->query($sql);

if ($result->num_rows > 0) {
    // Output data of each row
    while($row = $result->fetch_assoc()) {
        echo "id: " . $row["id"]. " - Name: " . $row["name"]. " - Email: " . $row["email"]. "<br>";
    }
} else {
    echo "0 results";
}
?>
```

**Explanation**:
- The `SELECT` query retrieves the `id`, `name`, and `email` columns from the `users` table.
- The `num_rows` function checks if any rows are returned. If rows are returned, the `fetch_assoc()` method is used to fetch the data and display it.

---

