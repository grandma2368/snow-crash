#on se connecte au niveau avec level00:level00 comme donne dans le sujet
#on cherche ce qui pourrait ressembler de pres ou de loin a un flag avec

find / -user 2> / dev/null

#find [chemin] (ici '/') [pattern] (ici en priorite 'user' et 'flag00' ensuite) --- on nettoie notre sortie d'erreur en envoyant tout ca dans /dev/null
#on tombe sur deux fichiers

/rofs/usr/sbin/john
/usr/sbin/john

#contenant tous deux la meme chaine de caracteres

cdiiddwpgswtgt

#cela ne passe pas en mot de passe, on tente donc de decrypter avec dcode.fr
#on dechiffre le cesar et le code le plus coherent donne

nottoohardhere