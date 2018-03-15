# odmiana-imion

```php
$regexes = json_decode(file_get_contents('regexes.json'));

function replace_name($name) {
   global $regexes;

   foreach ($regexes as $from => $to) {
      if(preg_match('/'.$from.'/i', $name)) {
         return preg_replace('/'.$from.'/i', $to, $name);
      }
   }

   return $name;
}
```
