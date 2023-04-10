# php-composer-packages


### psr-4 autoloading
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
