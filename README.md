# Jeedom_Widget_Json

- For one of my project I needed a widget managing Json data instead of simple string.
  
## Json Input
- The json data is submitted to Jeedom as raw string as the following
     ```json
      "{'Battery': '90', 'Temperature':'16,5', Humidity':'55'}"
    ```
- if your data is the output of PHP script, make sure the format is in line with it is expected
- Example of PHP code
```php
$json_string="{";
foreach($result as $x => $val) {
  // ....
  $json_string .= "'".$x."':"."'".$val."',"; // add ' instead of " bcse widget remove " ==> see widget script : ' replaced back by "
}
$json_string[strlen($json_string)-1] = "}";  // replace last ',' by '}'
$scenario->setData('JSON', $json_string);
```
## Intallation


## Virtual Creation


## Still on going
  - manage options
