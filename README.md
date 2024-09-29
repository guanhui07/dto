## dto

```php 
composer require guanhui07/dto dev-main
```

## 定义dto类

```php
namespace App\Services\Entity;
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

## 使用dto 传参  方式1

```php
$giftDto = new MsgGiftDto([
    'id' => 1,
    'number' => 10,
    'gift_name' => 'test123',
])

$obj->send($giftDto);
```

## 使用dto 传参  方式2

```php
$giftDto = new MsgGiftDto()->fill([
    'id' => 1,
    'number' => 10,
    'gift_name' => 'test123',
]);

$obj->send($giftDto);
```

## 使用dto 传参  方式3

```php
$giftDto = new MsgGiftDto();
$giftDto->id = 1;
$giftDto->number = 10;
$giftDto->gift_name = 'test123';

$obj->send($giftDto);
```