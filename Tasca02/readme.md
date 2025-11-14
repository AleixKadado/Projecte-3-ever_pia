# 🛡️ Tasca 01 – Gestió de Contrasenyes Segures

## 📌 README.md

Benvingut a la tasca sobre gestió de contrasenyes.  
L’objectiu és garantir la seguretat de les credencials tècniques després del recent incident de fuita de dades a EverPia.  
A continuació es detallen els arxius i enllaços del lliurament:

- **informe.md** → Fase 1: Anàlisi i justificació tècnica de l’eina escollida.  
- **guia.md** → Fase 2: Guia d’ús tècnica pas a pas per a l’equip.  
- **img/** → Carpeta amb captures de pantalla per a la guia.  

---

## 📄 Fase 1: Informe Tècnic – informe.md

### Introducció i Justificació

Recentment, EverPia ha estat víctima d’un atac cibernètic. Un compte tècnic amb contrasenya feble o reutilitzada va ser compromès, provocant una fuga de dades de projectes en desenvolupament.  

Els riscos principals de contrasenyes febles o repetides inclouen:  
- **Atacs de diccionari i força bruta**.  
- **Credential stuffing**: ús de combinacions filtrades d’altres serveis.  
- **Pèrdua de confidencialitat i reputació** de l’empresa.  

Un **gestor de contrasenyes** permet:  
- Generar contrasenyes fortes i úniques.  
- Emmagatzemar-les de manera xifrada end-to-end.  
- Facilitar l’accés segur i la sincronització entre dispositius.  

### Comparativa Tècnica

| Característica           | **Bitwarden (Online/Núvol)**                                | **KeePassX/KeePassXC (Offline/Escriptori)**            |
|---------------------------|-------------------------------------------------------------|--------------------------------------------------------|
| **Emmagatzematge**        | Núvol amb sincronització automàtica                         | Local (arxiu KDBX)                                   |
| **Seguretat**             | Xifratge end-to-end, autenticació multifactor               | Xifratge local AES/Rijndael, sense dependència del núvol |
| **Accés multi-dispositiu**| Sí, mòbil, escriptori, navegador                             | Només dispositiu local o via arxiu portable           |
| **Cost / Model**          | Freemium, opcions premium                                   | Totalment gratuït, open source                        |
| **Portabilitat**          | Sí, des de qualsevol dispositiu amb Internet                | Arxiu portable en USB o núvol xifrat                  |

### Avantatges i Inconvenients

**Bitwarden (Online)**  
- ✅ Avantatges: sincronització automàtica, fàcil d’usar, multi-dispositiu.  
- ❌ Inconvenients: dependència del núvol, necessita connexió a Internet.  

**KeePassX/KeePassXC (Offline)**  
- ✅ Avantatges: total control local, open source, sense dependència d’Internet.  
- ❌ Inconvenients: gestió manual de sincronització, menys amigable per a usuaris novells.  

### Recomanació

Per al **personal tècnic de EverPia**, recomanem **Bitwarden**: permet gestionar contrasenyes robustes i úniques amb mínim esforç, amb suport multi-dispositiu i autenticació multifactor, garantint continuïtat i seguretat en el treball diari.

---

## 🛠️ Fase 2: Guia d’Ús Tècnica – guia.md

### 1️⃣ Instal·lació i Configuració Inicial

1. Visiteu la pàgina oficial: [Bitwarden](https://bitwarden.com/)  
2. Descarregueu la versió corresponent: escriptori, mòbil o extensió de navegador.  
3. Creeu un compte mestre amb contrasenya forta i única.  

> 💡 Consell: utilitzeu autenticació multifactor per reforçar la seguretat del compte mestre.

---

### 2️⃣ Generació de Contrasenyes Segures

1. Obriu Bitwarden i seleccioneu "Generador de contrasenyes".  
2. Configureu els paràmetres:  
   - Longitud: mínim 16 caràcters.  
   - Incloure majúscules, minúscules, números i símbols.  
3. Copieu la contrasenya generada i deseu-la directament al vostre arxiu de Bitwarden.  

---

### 3️⃣ Emplenament Automàtic i Exemples

#### Desar un compte de correu
1. Afegiu un nou ítem.  
2. Introduïu el nom, usuari i contrasenya generada.  
3. Deseu-lo.  

#### Desar un compte d’aplicació web
1. Afegiu un nou ítem amb URL, usuari i contrasenya.  
2. Activeu l’opció "emplenar automàticament".  

#### Extensió del navegador
1. Instal·leu l’extensió oficial.  
2. Inicieu sessió amb el compte mestre.  
3. Activant “emplenar automàticament” podreu iniciar sessió amb un clic.  

---

### 4️⃣ Gestió de Còpies de Seguretat

#### Exportació
1. Obriu Bitwarden → Configuració → Exportar.  
2. Introduïu la contrasenya mestre per xifrar l’exportació.  
3. Deseu el fitxer `.json` en un lloc segur.

#### Millor pràctica
- Guardar la còpia en un **USB xifrat** o núvol xifrat amb accés limitat.  
- No deixar còpies en ordinadors compartits.  

---

### 📸 Captures i Recursos Addicionals

Les imatges i captures de pantalla s’han de guardar dins la carpeta `img/` i enllaçar-les a la guia com:
```markdown
![Descripció de la imatge](img/nom_de_la_imatge.png)

