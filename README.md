# Jeedom_Widget_Json

- Widget managing Json data instead of simple string as done by core widgets.
- Thanks to the Jeedom Community 
  
## Json Input
- The json data is submitted to Jeedom as raw string as the following:
     ```json
      "{'Battery': '90', 'Temperature':'16,5', Humidity':'55'}"
    ```
- if your data is the output of PHP script, make sure the format is OK.
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

![image](https://github.com/sinbrive/Jeedom_Widget_Json/assets/21102151/a7c04c70-a008-4246-ae2b-b9d17a76094a)


![image](https://github.com/sinbrive/Jeedom_Widget_Json/assets/21102151/66849db0-2c67-4d6b-8bc6-2b3bbb699951)


![image](https://github.com/sinbrive/Jeedom_Widget_Json/assets/21102151/80c6e393-5a52-416a-b008-9f3221e5beff)


![image](https://github.com/sinbrive/Jeedom_Widget_Json/assets/21102151/fc4f346f-dd55-4d44-a33b-79eaa0c8236a)


![image](https://github.com/sinbrive/Jeedom_Widget_Json/assets/21102151/206cd010-6932-42ae-aa5a-4bec8c98d581)


![image](https://github.com/sinbrive/Jeedom_Widget_Json/assets/21102151/072a364f-11ad-4a4b-8af3-f7d61027cb8c)


## Virtual Creation

![image](https://github.com/sinbrive/Jeedom_Widget_Json/assets/21102151/d1babb8a-1d63-4f20-b8e2-f8f5bcd4c977)


![image](https://github.com/sinbrive/Jeedom_Widget_Json/assets/21102151/cd568a12-3382-43dd-83bf-1f99901d9550)


![image](https://github.com/sinbrive/Jeedom_Widget_Json/assets/21102151/8ab140f7-cbbe-492c-9e09-d8228842529a)


![image](https://github.com/sinbrive/Jeedom_Widget_Json/assets/21102151/d3d80779-4031-42b9-bf48-9affeaa89342)

## Still Open
  - manage options
