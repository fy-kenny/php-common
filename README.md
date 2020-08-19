# php-common
* First of all, thank you very much for reading this document. 
* I am a PHP newbie
* I imitated Java and wrote an parent `Enum` class. 
* This parent class can make it more convenient and simple for everyone to write enumeration classes, 
* and it is more like Java enumeration usage habits. 
* Because PHP does not have symbol `enum` and I also donot want to use SplEnum.

## How
* define `public static variables` as enum definitions
* scan `enum definitions` of sub enum class and make enum instances in the parent `Enum` class
* `protected static $__values = []` holding enum instances
* `instance sub enum class` after loading

## Declaration
```php
class SampleEnum extends Enum {
    protected static $__values = [];
    
    public static $ENUM1;
    public static $ENUM2;
}
new SampleEnum();
```

## Usage
```php
$sampleEnum = SampleEnum::$ENUM1;
```

## You
* Try it
* Tell me issues if any
