Usually, comparison are sufficient, and it is rare to have to compare the result of comparison. Check if this two-stage comparison is really needed.

<?php

if ($a === strpos($string, $needle) > 2) {}

// the expression above apply precedence : 
// it is equivalent to : 
if (($a === strpos($string, $needle)) > 2) {}

?>

See also [Operators Precedence](http://php.net/manual/en/language.operators.precedence.php).
