Function that bear the same name as a PHP function, and that are declared. 

This is possible when managing some backward compatibility, like emulating an old function, or preparing for newer PHP version, like emulating new upcoming function.

<?php

if (version_compare(PHP_VERSION, 7.0) > 0) {
    function split($separator, $string) {
        return explode($separator, $string);
    }
}

print_r( split(' ', '2 3'));

?>
