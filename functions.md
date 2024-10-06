# Creating and calling functions to echo out the desired results.

```php
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Demo</title>
</head>

<body>
    <?php
        $books = [
            [
                'name' => 'Do Androids Dream of Electric Sheep',
                'author' => 'Philip K. Dick',
                'releaseYear' => 1968,
                'purchaseUrl' => 'http://example.com'
            ],
            [
                'name' => 'Project Hail Mary',
                'author' => 'Andy Weir',
                'releaseYear' => 2021,
                'purchaseUrl' => 'http://example.com'
            ],
            [
                'name' => 'The Martian',
                'author' => 'Andy Weir',
                'releaseYear' => 2011,
                'purchaseUrl' => 'http://example.com'
            ],
        ];

        function filterByAuthor($books, $author) {
            $filteredBooks = [];

            foreach ($books as $book) {
                if ($book['author'] === $author) {
                    $filteredBooks[] = $book;
                }
            }

            return $filteredBooks;
        }

        $filteredList = filterByAuthor($books, 'Andy Weir');
    ?>

    <ul>
        <?php foreach ($filteredList as $book): ?>
            <li><?= $book['name'] ?></li>
        <?php endforeach; ?>
    </ul>
</body>
</html>

```

#More generalized approach

```php
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Demo</title>
</head>

<body>
    <?php
        $books = [
            [
                'name' => 'Do Androids Dream of Electric Sheep',
                'author' => 'Philip K. Dick',
                'releaseYear' => 1968,
                'purchaseUrl' => 'http://example.com'
            ],
            [
                'name' => 'Project Hail Mary',
                'author' => 'Andy Weir',
                'releaseYear' => 2021,
                'purchaseUrl' => 'http://example.com'
            ],
            [
                'name' => 'The Martian',
                'author' => 'Andy Weir',
                'releaseYear' => 2011,
                'purchaseUrl' => 'http://example.com'
            ],
        ];


function filter($items, $key, $value){

    $filteredItems = [];

    foreach($items as $item){
        if($item[$key]===$value){
            $filteredItems[]= $item;
        }
    }
    return $filteredItems;
    
    
}
    $filteredList = filter($books, 'author', 'Andy Weir' );
    
    ?>

<ul>
    <?php foreach( $filteredList as $book) :?>

    <li>
        <?= $book['name'] ?>
    </li>

<?php endforeach ;?>
</ul>


    
</body>
</html>

```

