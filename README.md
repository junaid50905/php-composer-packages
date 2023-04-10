# php-composer-packages


### psr-4 autoloading

#### why use psr-4
<ol>
  <li>Autoloading: PSR-4 provides a standardized way to autoload PHP classes, making it easier to manage dependencies and avoid conflicts between class names.</li>
</ol>

#### how to use psr-4

- create a composer.json file in the project directory
- put the following code in the composer.json file

##### composer.json
```
{
  "autoload": {
      "psr-4": {
          "App\\": "src/"
      }
  }
}

```
- write this command in the project directory terminal: composer dump-autoload . Then we will get a new folder named vendor. In this vendor folder we put all the outside file like bootstrap.
- write namespace App to class like the following

```
<?php
    namespace App;

    class Students{
        public function show_students()
        {
            echo "show all students data";
        }
    }

```
- From where we want to use the class, we have to include the autoload.php file from vendor and use class like the following
```
<?php

//classes
include_once 'vendor/autoload.php';
use App\Students;
use App\Teachers;



$std = new Students;
echo $std->show_students();
echo "<br>";


?>

```












