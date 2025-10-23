# 🔐 Tasca 01: Gestió Segura de Contrasenyes

## ⚠️ Alerta de Seguretat

**EverPia ha estat atacada per ciberdelinqüents.** La consultora on esteu de becaris ha patit una fuita d’informació (_data breach_) que ha exposat dades confidencials d’un projecte en desenvolupament. Els atacants amenacen amb publicar la informació si no es paga un rescat.

Aquesta situació ha generat una gran alarma dins la companyia, que ha activat un **comitè de crisi** per gestionar l'incident. La investigació interna ha revelat que un dels comptes tècnics va ser compromès per l'ús d'una **contrasenya feble o reutilitzada**.

## 🛡️ Directriu de la Direcció Tècnica

Com a resposta a la crisi, la Direcció Tècnica ha emès una directriu clara:

> Tot el personal tècnic ha de començar a utilitzar un **gestor de contrasenyes validat** per garantir l'ús de credencials úniques i robustes.

Se us encarrega la tasca d'avaluar les opcions disponibles i crear la documentació necessària per a la formació del personal.

---

## 📄 Fase 1: Anàlisi i Justificació (`informe.md`)

L'informe ha d'incloure:

### ✅ Introducció i Justificació

- Explicació del risc de contrasenyes febles o reutilitzades (atacs de diccionari, _credential stuffing_, etc.).
- Funció d’un gestor de contrasenyes per mitigar aquests riscos.

### 📊 Comparativa Tècnica

Taula comparativa entre:

| Gestor        | Tipus        | Seguretat            | Accés multiplataforma | Cost / Model |
|---------------|--------------|-----------------------|------------------------|--------------|
| Bitwarden     | Online / Núvol | Xifratge end-to-end   | Sí                     | Freemium     |
| KeePassX/C    | Offline / Escriptori | Arxiu local (KDBX) | Portabilitat manual   | Gratuït / Open Source |

### ⚖️ Avantatges i Inconvenients

- **Online (Bitwarden):**
  - ✅ Sincronització automàtica
  - ✅ Accés des de qualsevol dispositiu
  - ❌ Dependència del núvol

- **Offline (KeePassX/C):**
  - ✅ Control total de les dades
  - ✅ Independència del núvol
  - ❌ Més complexitat en la sincronització

### 📝 Recomanació

Concloure amb l’eina escollida i justificar la decisió segons criteris de seguretat, usabilitat i continuïtat del negoci.

---

## 🧰 Fase 2: Guia d'Ús Tècnica (`guia.md`)

Guia clara amb captures de pantalla (ubicades a la carpeta `img/`) i instruccions pas a pas.

### 🔧 Instal·lació i Configuració Inicial

- Descàrrega i instal·lació de l’eina
- Creació de la base de dades principal o compte mestre

### 🔐 Generació de Contrasenyes Segures

- Ús del generador de contrasenyes
- Paràmetres: longitud, caràcters especials, etc.

### 💾 Exemples d'Ús i Emplenament Automàtic

- Desar credencials d’un compte de correu electrònic
- Desar credencials d’una aplicació o servei web
- Ús de l’extensió del navegador per emplenar automàticament

### 🗂️ Gestió de Còpies de Seguretat

- Com fer una còpia de seguretat (KDBX o exportació)
- Recomanació: clau USB xifrada o emmagatzematge xifrat al núvol

---

## 📁 Estructura del Lliurament


