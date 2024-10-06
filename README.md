# PHP-Laravel

#1 foreach loop short-hand

<html>
  <head></head>
  <body>

    <?php 
    
      $books = [
        "times",
        "oldTimes",
        "newTimes"
      ];
    
    ?>

    <ul>

      <?php  foreach ($books as $book) :?>
        <?= "<li>$book</li>"; ?>

      <?php endforeach ;?>
      
    </ul>
        
 </body>
</html>


#2 Associative key values for arrays 

## Keys can be used to loop/access the values of array.

```php
<body>
   <?php 
    
      $books = [
        [
        'name'=>"TheTimes",
        'author'=>"TimesAuthor"
        ],
        [
        'name'=> "OldTimes",
        'author'=>"OldTimesAuthor"
        ]
      
      ];
    
    ?>

    <ul>

      <?php  foreach ($books as $book) :?>
       <li>
         <?= $book['name'] ;?>
       </li>

      <?php endforeach ;?>
      
    </ul>
</body>
