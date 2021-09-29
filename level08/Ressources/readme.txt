#on retrouve un executable level08 et un fichier token
#level08 renvoie une erreur quand on lui donne token
#on essaye de changer les droits sur token, on ne peut pas, on va donc en faire un lien symbolique

ln -s /home/user/level08/token /tmp/exploit

#puis on redonne le lien symbolique a level08

./level08 /tmp/exploit

#qui nous renvoie quelque chose qui ressemble a un flag mais qui est le mdp
#du flag08 (quif5eloekouj29ke0vouxean) qui lui nous permettra avec un getflag classique
#de recuperer le flag du level09