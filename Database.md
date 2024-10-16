#connection to mysql

```php
<?php

//PDO: php data objects

//connect to our mysql database

//a string that declares your connection to the database.

$dsn = "mysql:host=localhost;port=3306;dbname=demo;user=root;charset=utf8mb4";
$pdo = new PDO($dsn); //datasource name

$statement = $pdo->prepare("select * from posts");

$statement->execute();

$posts = $statement->fetchAll(PDO::FETCH_ASSOC);


```
