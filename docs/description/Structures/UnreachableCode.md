Code may be unreachable, because other instructions prevent its reaching. 
For example, it be located after throw, return, exit(), die(), goto, break or continue : this way, it cannot be reached, as the previous instruction will divert the engine to another part of the code. 

<?php

function foo() {
    $a++;
    return $a;
    $b++;      // $b++ can't be reached;
}

function bar() {
    if ($a) {
        return $a;
    } else {
        return $b;
    }
    $b++;      // $b++ can't be reached;
}

foreach($a as $b) {
    $c += $b;
    if ($c > 10) {
        continue 1;
    } else {
        $c--;
        continue;
    }
    $d += $e;   // this can't be reached
}

$a = 1;
goto B;
class foo {}    // Definitions are accessible, but not functioncalls
B: 
echo $a;


?>

This is dead code, that may be removed.