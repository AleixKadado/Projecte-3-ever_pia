# 🚀 T04 – Implantació d’un Servei d’Autenticació Centralitzada amb OpenLDAP

Innovatech, una start-up tecnològica emergent, està experimentant un ràpid creixement i pateix un caos en la gestió dels seus usuaris i accessos.

Actualment, cada servei intern (servidor de fitxers, wiki de documentació, etc.) utilitza la seva pròpia base de dades d'usuaris i contrasenyes i a més als ordinadors clients s’usa autentificació local. Això genera diversos problemes crítics:

- ⚙️ **Ineficiència Operativa:** Cada cop que s'incorpora o marxa un empleat, l'equip tècnic ha de crear o eliminar el compte en múltiples sistemes.  
- 🔐 **Risc de Seguretat:** Els usuaris sovint acaben reutilitzant contrasenyes entre serveis per evitar l'oblit.  
- 📉 **Manca d'Escalabilitat:** A mesura que Innovatech afegeix nous serveis, el problema es fa insostenible.

---

El CEO d’Innovatech ha contactat amb **EverPia** per tal d’implementar una solució d’autenticació centralitzada.  
La solució proposada és utilitzar **OpenLDAP** (Lightweight Directory Access Protocol) per ser una solució robusta i de codi obert, que s’alinea amb l’esperit d’Innovatech, ja que tots els ordinadors de l’empresa usen GNU-Linux. 🐧

La vostra missió serà:

- 🏗️ Instal·lar el servei **OpenLDAP** en un servidor Linux  
- 🧱 Configurar el domini base  
- 🌳 Crear la jerarquia d'unitats organitzatives  
- 👥 Integrar usuaris i grups que després s’utilitzaran als serveis de xarxa  
- 💻 Configurar un equip client perquè utilitzi el directori per autenticar els usuaris

---

S’ha redactat un document on s’especifica clarament la feina que s’ha de desenvolupar; el teniu disponible en el **plec de condicions tècniques** (també disponible al Moodle de l’assignatura).

## 📚 Material de classe (Moodle)
- 📘 **UD04.AA1** – Serveis de Directori  
- 📙 **UD04.AA2** – Instal·lació OpenLDAP  
- 📗 **UD04.AA3** – Configuració del directori  
- 📕 **UD04.AA5** – Agregar client al directori
