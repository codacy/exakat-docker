Those properties are declared public, but are never used publicly. They may be made protected. 

<?php

class foo {
    // Public, and used publicly
    public $publicProperty;
    // Public, but never used outside the class or its children
    public $protectedProperty;
    
    function bar() {
        $this->protectedProperty = 1;
    }
}

$foo = new Foo();
$foo->publicProperty = 3;

?>

This property may even be made private.

