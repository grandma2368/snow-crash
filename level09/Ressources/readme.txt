#on trouve level09 et un token dans la ~
#level09 semble haser les chaines de caractere qu'on lui donne

./level09 aaa
abc
./level09 qwerty
qxgux~

#on lui envoie donc une chaine de caracteres qu'il pourra interpreter et executer comme getflag
#chaine de caractere qu'on encode avec un script python en ressource

py /tmp/exploit.py `cat token`
f3iji1ju5yuevaus41q1afiuq

#on recupere le mot de passe pour se connecter au flag09
#de la on recupere le flag du level09 avec getflag