#on voit un fichier level02.pcap dans le ~ du niveau on le telecharge avec scp depuis une autre machine

scp -P 4242 scp://level02@[ip]/level02.pcap level02.pcap

#on nous demande un mot de passe pour telecharger, il faut renseigner le flag du niveau precedent
#on se retrouve avec un fichier level02.pcap sur la machine distante
#on n'a pas les droits dessus, on se les approprie donc

chmod 777 level02.pcap

#on peut maintenant ouvrir le fichier dans wireshark
#on va dans le bandeau Analyse > Follow > TCP Stream et on trouve

..%..%..&..... ..#..'..$..&..... ..#..'..$.. .....#.....'........... .38400,38400....#.SodaCan:0....'..DISPLAY.SodaCan:0......xterm.........."........!........"..".....b........b....	B.
..............................1.......!.."......"......!..........."........"..".............	..
.....................
Linux 2.6.38-8-generic-pae (::ffff:10.1.1.2) (pts/10)

..wwwbugs login: l.le.ev.ve.el.lX.X
..
Password: ft_wandr...NDRel.L0L
.
..
Login incorrect
wwwbugs login: 

#on remarque le "Password: ft_wandr...NDRel.L0L" , on supprime les "." et on obtient

ft_wandrNDRelL0L

#on remanie cette chaine de caractere en supprimant les doublons pour qu'elle ait un sens

ft_waNDReL0L