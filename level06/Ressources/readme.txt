#on arrive au level06 avec deux fichiers, un level06 et un level06.php

#!/usr/bin/php
<?php
function y($m) { $m = preg_replace("/\./", " x ", $m); $m = preg_replace("/@/", " y", $m); return $m; }
function x($y, $z) { $a = file_get_contents($y); $a = preg_replace("/(\[x (.*)\])/e", "y(\"\\2\")", $a); $a = preg_replace("/\[/", "(", $a); $a = preg_replace("/\]/", ")", $a); return $a; }
$r = x($argv[1], $argv[2]); print $r;
?>

#on remarque dans la regexp le 'e' qui va nous permettre d'ajouter du code a executer
#on remplit donc une chaine de caracteres d'elements comblants la regexp pour ensuite lui injecter du code
#le script exploit est en ressource

./level06 /tmp/exploit

#une erreur php est renvoyee precedee par le flag recherche