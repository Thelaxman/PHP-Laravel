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
