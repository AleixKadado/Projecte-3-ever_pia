# ⚠️ Alerta de Seguretat: Ciberatac a EverPia

**Alerta!!** EverPia ha estat atacada per ciberdelinqüents. La consultora on esteu de becaris ha patit una **fuita d’informació (data breach)** i informació confidencial sobre un projecte que està en fase de desenvolupament està ara en mans de delinqüents que amenacen amb publicar-la si no es paga un rescat.

Òbviament, això ha causat una gran alarma dins la companyia i s’ha creat un **comitè de crisi** per gestionar la situació. La investigació interna ha revelat que un dels comptes tècnics va ser compromès a causa de l'ús d'una **contrasenya feble o reutilitzada**.

![ujjuuj](img.png)

---

## 🛡️ Directriu de la Direcció Tècnica

Com a resposta a aquesta crisi, la Direcció Tècnica ha emès una directriu:

> Tot el personal tècnic ha de començar a utilitzar un **gestor de contrasenyes validat** per garantir l'ús de credencials úniques i robustes.

Se us encarrega la tasca d'avaluar les opcions i crear la documentació necessària per a la formació del personal.

---

## 📄 Fase 1: Anàlisi i Justificació (Document d'Informe)

Heu de redactar un informe que justifiqui tècnicament la decisió de la Direcció i compari les opcions. Aquest informe ha d'incloure:

### ✅ Introducció i Justificació

- Explicació de per què les contrasenyes febles o reutilitzades són un risc crític per a l'empresa (atac de diccionari, credential stuffing, etc.).
- La funció crucial d'un gestor de contrasenyes per mitigar aquests riscos.

### 📊 Comparativa Tècnica

Realitzeu una taula comparativa detallada entre:

- **Bitwarden (Alternativa Online / Núvol):**
  - Sincronització
  - Model de seguretat (xifratge end-to-end)
  - Facilitat d'accés des de múltiples dispositius
  - Cost / model freemium

- **KeePassX / KeePassXC (Alternativa Offline / Escriptori):**
  - Emmagatzematge local de l'arxiu (KDBX)
  - Independència del núvol
  - Model open source
  - Portabilitat de l'arxiu

### ⚖️ Avantatges i Inconvenients

Resumiu els principals pros i contres de cada model (online vs. offline) des del punt de vista de:

- Seguretat
- Usabilitat
- Continuïtat del negoci

### 📝 Recomanació

Concloeu l'informe escollint l'eina que considereu més adequada per al personal tècnic de l'empresa i justifiqueu la vostra elecció.

---

## 🧰 Fase 2: Guia d'Ús Tècnica (Manual Operatiu)

Utilitzant l'eina que heu seleccionat a la Fase 1 (Bitwarden, KeePassX, o similar), heu de crear una Guia d'Ús per a l'Equip Tècnic. Aquesta guia ha de ser clara i basada en captures de pantalla i instruccions pas a pas.

### 🔧 La guia ha de cobrir els següents punts obligatoris:

- **Instal·lació i Configuració Inicial:**
  - Descàrrega
  - Instal·lació
  - Creació de la BBDD principal o compte mestre

- **Generació de Contrasenyes Segures:**
  - Explicació de com utilitzar el generador de contrasenyes de l'eina
  - Paràmetres, longitud, caràcters especials

- **Exemples d'Ús i Emplenament Automàtic:**
  - Com desar una credencial d'un compte de correu electrònic
  - Com desar una credencial d'una aplicació o servei web
  - Com fer servir l’extensió del navegador per emplenar automàticament les dades

- **Gestió de Còpies de Seguretat (Backup):**
  - Explicació detallada de com fer una còpia de seguretat de l'arxiu de contrasenyes (KDBX en KeePass o Exportació en Bitwarden)
  - Recomanació de la millor pràctica per emmagatzemar aquesta còpia de seguretat de forma segura (clau USB xifrada o emmagatzematge xifrat al núvol)

---

## 📁 Lliurament

Es tracta d’una tasca individual. Què caldrà lliurar?

Dins el repositori del `projecte-3` heu de crear una carpeta anomenada `tasca01`, dins d’ella heu de tenir:

- `README.md` amb la descripció de la tasca i enllaços als arxius de l’informe i la guia
- `informe.md` → Informe corresponent a la Fase 1
- `guia.md` → Guia d’ús tècnica
- Carpeta d’imatges (`img`, `pics`, etc.) amb les captures de pantalla

---

## 📚 Materials i Links de Suport

- [INCIBE: Gestión de contraseñas seguras](https://www.incibe.es/protege-tu-empresa/blog/gestion-contrasenas-seguras)
- [Bitwarden - Pàgina oficial](https://bitwarden.com)
- [KeePassXC - Pàgina oficial](https://keepassxc.org)
- [INCIBE: Gestores de contraseñas](https://www.incibe.es/protege-tu-empresa/blog/gestores-contrasenas)
