# T04: Serveis de directori. LDAP

Cambiem el nostres hostname, i el hosts a server.innovatech15.test

Per establir comunicació amb l’amfitrió, configurem una interfície de tipus Host-Only i també un adaptador en mode pont

Editem el netplan

Fem un `systemctl status slapd`, i per instalar, fem un `sudo apt install slapd`

Comprovacio que el directori s’ha creat amb el nom correcte

S’han de crear dues unitats organitzatives OUs, users i grups

Per crear les OUs finalment executarem la comanda seguent.

Comprovació de que s’han creat correctement OUs

Instal·lació del gestor LDAP.

Entrem en lam, amb contraseña lam

l

Amb tot aixo, crear dos usuaris i dos grups, amb el nom, manager01, i tech01, també canviar, la contrasenya de lam a 1234, per el inici de sessió.

Comprovem els noms

Comprovació de la resolució del servidor domini

Instalem els mòduls d’autenticació de ldap

Comprovar la connectivitat amb el servidor, farem una consulta ldapsearch des del client

Configurar el arxiu nsswitch

Borrar el terme use_authok

Afegir la línia següent per permetre la creació automàtica dels perfils d’usuari:

Podem verificar que el sistema mostra correctament els usuaris provinents del directori LDAP.

Permetre l’inici de sessió gràfica dels usuaris del domini.

