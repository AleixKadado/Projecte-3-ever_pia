# Fase 1: Anàlisi i Justificació (Document d'Informe)

**Aleix Kadado Sole**  
21/10/2025  

---

## **Índex**
1. [Introducció i Justificació](#introducció-i-justificació)  
2. [Comparativa Tècnica](#comparativa-tècnica)  
3. [Avantatges i Inconvenients](#avantatges-i-inconvenients)  
4. [Recomanació](#recomanació)  

---

## **Informe: Avaluació de gestors de contrasenyes per a EverPia**

### **Introducció i justificació**

Fa poc, a EverPia hi va haver un atac bastant greu i s’ha descobert que tot va començar per culpa d’una contrasenya fluixa o repetida. O sigui, algú va fer servir una contrasenya massa simple i els hackers van poder entrar. Això passa molt més sovint del que sembla, perquè la gent acostuma a posar contrasenyes com “hola123” o “qwerty” o directament les mateixes a tot arreu.

El problema d’això és que hi ha atacs com els de **diccionari** (on proven contrasenyes típiques) o el **credential stuffing**, que bàsicament agafen contrasenyes filtrades d’altres llocs i les proven fins que alguna cola.

Per evitar tot aquest merder, s’ha decidit fer servir un **gestor de contrasenyes**, que és com una aplicació on pots guardar totes les contrasenyes de manera segura i només n’has de recordar una. A més, aquests programes també poden crear contrasenyes fortes automàticament, cosa que està molt bé perquè així no cal trencar-se el cap.

---

### **Comparativa tècnica**

| Aspecte | **Bitwarden (Online / Núvol)** | **KeePassXC (Offline / Escriptori)** |
|----------|--------------------------------|------------------------------------|
| **Seguretat** | Tot està xifrat d’extrem a extrem. Només tu pots veure les teves contrasenyes. | També xifra les dades, però les guarda al teu ordinador o USB. |
| **Accés** | Pots entrar des del mòbil, l’ordinador o el navegador, i tot se sincronitza sol. | Només pots accedir des d’on tinguis guardat l’arxiu. |
| **Emmagatzematge** | Es guarda al núvol (Bitwarden o servidors propis). | Tot queda guardat localment. |
| **Codi obert** | Sí. | Sí, també. |
| **Preu** | Té versió gratis i una de pagament molt barata. | Totalment gratuït. |
| **Facilitat d’ús** | Bastant fàcil i moderna. | Una mica més tècnica, menys “bonica”. |
| **Internet** | Necessita connexió per sincronitzar. | No necessita Internet. |

---

### **Avantatges i inconvenients**

#### **Bitwarden**
**Avantatges:**
- Sincronitza tot sol entre dispositius.  
- Fàcil d’usar i bon disseny.  
- Molt segur, amb xifratge end-to-end.  

**Inconvenients:**
- Necessita Internet.  
- Alguna gent no es refia del núvol.  

#### **KeePassXC**
**Avantatges:**
- No depèn d’Internet.  
- És 100% gratuït i obert.  
- Tot queda sota control de l’usuari.  

**Inconvenients:**
- No sincronitza sol.  
- Si perds l’arxiu o t’oblides la contrasenya, adéu.  
- Interfície una mica lletja i tècnica.  

---

### **Recomanació**

Jo recomanaria **Bitwarden**, perquè per a la gent d’EverPia que treballa amb diferents dispositius o projectes és molt més còmode. És segur, fàcil d’usar i, com que és *open source*, no depens d’una empresa “tancada”.

**KeePassXC** també està bé, però és més per a gent que li agrada controlar-ho tot manualment i no necessita sincronitzar. Per un equip tècnic que ha d’anar ràpid i segur, Bitwarden és més pràctic.

**En resum:** *Bitwarden és segur, ràpid i senzill. Perfecte per evitar que torni a passar un desastre com aquest.*

---

