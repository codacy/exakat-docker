Unknown directives names used in the code. 

The following list has directive mentionned in the code, that are not known from PHP or any extension. If this is due to a mistake, the directive must be fixed to be actually useful.

<?php

// non-existing directive
$reporting_error = ini_get('reporting_error');
$error_reporting = ini_get('error_reproting'); // Note the inversion
if (ini_set('dump_globals')) {
    // doSomething()
}

// Correct directives
$error_reporting = ini_get('reporting_error');
if (ini_set('xdebug.dump_globals')) {
    // doSomething()
}

?>
