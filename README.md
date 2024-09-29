## dto

```php

use Guanhui07\BaseDto;

class MsgGiftDto extends BaseDto
{

    /**
     * 礼物ID
     * @var int
     */
    public $id;

    /**
     * 礼物数量
     * @var int
     */
    public $number;
    
   /**
     * 礼物名
     * @var int
     */
    public $gift_name;

}

```


```php
$giftDto = new MsgGiftDto([
    'id' => 1,
    'number' => 10,
    'gift_name' => 'test123',
])

$obj->send($giftDto);
```
