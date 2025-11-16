# T04: Serveis de directori LDAP

## 1️⃣ Configuració inicial del servidor

* Canviem el hostname a:

```bash
sudo hostnamectl set-hostname server.innovatech15.test




```
* Modifiquem el fitxer `/etc/hosts` per reflectir el nou hostname.

![ujjuuj](img/captura1.png)

![ujjuuj](img/captura2.png)

![ujjuuj](img/captura3.png)


* Per establir comunicació amb l’amfitrió, configurem:

  * Una interfície de tipus **Host-Only**.
  * Un adaptador en **mode pont**.
    
 ![ujjuuj](img/captura4.png) 

![ujjuuj](img/captura5.png) 

* Editem la configuració de xarxa amb **netplan** segons la nostra topologia.

![ujjuuj](img/captura6.png) 
![ujjuuj](img/captura7.png) 

![ujjuuj](img/captura8.png) 

![ujjuuj](img/captura9.png) 

![ujjuuj](img/captura10.png) 


## 2️⃣ Instal·lació i gestió de LDAP

* Comprovem l’estat del servei LDAP:

```bash
systemctl status slapd
```


* Si no està instal·lat, instal·lem el paquet:

```bash
sudo apt install slapd
```



* Verifiquem que el directori s’ha creat amb el **nom correcte**.

  ![ujjuuj](img/captura11.png) 



## 3️⃣ Creació de les Unitats Organitzatives (OUs)

* Creem dues OUs: `users` i `groups`.

* Comanda per crear les OUs:

```bash
# Exemple de comanda ldapadd amb fitxer LDIF
ldapadd -x -D "cn=admin,dc=innovatech15,dc=test" -W -f ou.ldif
```

* Comprovació que les OUs s’han creat correctament:

```bash
ldapsearch -x -LLL -b "dc=innovatech15,dc=test" ou
```
![ujjuuj](img/captura13.png) 

![ujjuuj](img/captura14.png) 

![ujjuuj](img/captura15.png) 

![ujjuuj](img/captura16.png) 


## 4️⃣ Instal·lació del gestor LDAP (LAM)

  ![ujjuuj](img/captura17.png)

* Entrem al gestor **LAM** amb la contrasenya de l’administrador `lam`.

* Amb el gestor, creem:

  * **2 usuaris:** `manager01` i `tech01`
  * **2 grups** corresponents.

* Canviem la contrasenya de l’administrador `lam` a `1234` per a l’inici de sessió.

* Comprovem que els noms s’han creat correctament i la resolució del servidor de domini funciona.


  ![ujjuuj](img/captura18.png)

  ![ujjuuj](img/captura19.png)

  ![ujjuuj](img/captura20.png)

  ![ujjuuj](img/captura21.png)

  ![ujjuuj](img/captura22.png)

  ![ujjuuj](img/captura23.png)

  ![ujjuuj](img/captura24.png)

  ![ujjuuj](img/captura25.png)

    ![ujjuuj](img/captura26.png)

    ![ujjuuj](img/captura27.png)

    ![ujjuuj](img/captura28.png)

    ![ujjuuj](img/captura29.png) 

## 5️⃣ Configuració del client LDAP

  ![ujjuuj](img/captura30.png) 

  ![ujjuuj](img/captura31.png) 

  ![ujjuuj](img/captura32.png) 

* Instal·lem els mòduls d’autenticació LDAP:


```bash
sudo apt install libpam-ldap libnss-ldap nslcd

```

* Comprovem la connectivitat amb el servidor LDAP des del client:

```bash
ldapsearch -x -LLL -b "dc=innovatech15,dc=test" -H ldap://server.innovatech15.test
```
![ujjuuj](img/captura33.png)

![ujjuuj](img/captura34.png)

![ujjuuj](img/captura35.png)

![ujjuuj](img/captura36.png)

* Configurem `/etc/nsswitch.conf`:

  * Borrem el terme `use_authok`.
  * Afegim la línia següent per permetre la creació automàtica dels perfils d’usuari:
 
  ![ujjuuj](img/captura37.png)

![ujjuuj](img/captura38.png)

![ujjuuj](img/captura39.png)

![ujjuuj](img/captura40.png)

![ujjuuj](img/captura41.png)

![ujjuuj](img/captura42.png)


pam_mkhomedir.so skel=/etc/skel/ umask=0022
```

* Verifiquem que el sistema mostra correctament els usuaris provinents del directori LDAP.



## 6️⃣ Permetre l’inici de sessió gràfica

* Assegurem que els usuaris del domini LDAP poden iniciar sessió gràfica al sistema.
* Prova d’inici de sessió amb `manager01` o `tech01`.

