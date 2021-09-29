#on peut acceder au fichier /etc/password
#je copie colle la ligne du flag01 qui m'interesse et l'enregistre dans un fichier password.txt

flag01:42hDRfypTqqnw:3001:3001::/home/flag/flag01:/bin/bash

#je lance john the ripper dessus pour qu'il decrypte le code

john password.txt

#il sort

Created directory: /Users/camilleduverger/.john
Loaded 1 password hash (descrypt, traditional crypt(3) [DES 128/128 SSE2])
Press 'q' or Ctrl-C to abort, almost any other key for status
abcdefg          (flag01)
1g 0:00:00:00 100% 2/3 100.0g/s 150600p/s 150600c/s 150600C/s raquel..bigman
Use the "--show" option to display all of the cracked passwords reliably
Session completed

#le mot de passe est donc 'abcdefg'