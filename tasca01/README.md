# **Fase 1 – Informe Tècnic: Gestors de Contrasenyes**

## **1. Introducció i Justificació**

L’incident de seguretat recent a **EverPia** ha posat de manifest una de les vulnerabilitats més habituals en entorns corporatius: **l’ús de contrasenyes febles o reutilitzades**. Aquestes pràctiques obren la porta a diversos tipus d’atacs, entre els quals destaquen:

- **Atacs de diccionari o força bruta:** Els atacants proven combinacions comunes o paraules freqüents fins a trobar la contrasenya correcta.  
- **Credential stuffing:** Els delinqüents utilitzen credencials robades d’altres serveis per intentar accedir a sistemes de l’empresa, aprofitant la reutilització de contrasenyes.  
- **Phishing i enginyeria social:** Els empleats poden ser enganyats per revelar credencials que no són gestionades de manera segura.  

Aquesta situació demostra la necessitat urgent de garantir l’ús de **contrasenyes úniques, complexes i emmagatzemades de manera segura**.  
Un **gestor de contrasenyes** resol aquests problemes mitjançant:

- **Generació automàtica de contrasenyes robustes**.  
- **Emmagatzematge segur i xifrat** de totes les credencials.  
- **Sincronització i accés controlat** entre dispositius.  
- **Reducció del risc humà**, evitant la reutilització i facilitant bones pràctiques de seguretat.

Per això, la Direcció Tècnica ha requerit l’ús obligatori d’un gestor de contrasenyes validat per tot el personal tècnic.

---

## **2. Comparativa Tècnica**

| Característica | **Bitwarden** (Online / Núvol) | **KeePassXC** (Offline / Escriptori) |
|----------------|-------------------------------|------------------------------------|
| **Model d’emmagatzematge** | Núvol (servidors Bitwarden o autohospedatge opcional) | Fitxer local KDBX |
| **Xifratge** | AES-256, PBKDF2-SHA256, end-to-end | AES-256, ChaCha20; xifratge local |
| **Codi obert** | Sí (open source, auditat) | Sí (open source) |
| **Accés multi-dispositiu** | Sí (apps mòbils, extensions, web vault) | Sí, però manual (copiant el fitxer) |
| **Sincronització automàtica** | Sí, a través del núvol | No, només mitjançant sincronització manual |
| **Generador de contrasenyes** | Integrat i configurable | Integrat i configurable |
| **Autocompletat en navegadors** | Sí (extensions oficials per Chrome, Firefox, etc.) | Sí, mitjançant plugins externs o integració amb KeePassHTTP |
| **Model de cost** | Freemium (gratuït bàsic; premium 10 €/any) | Gratuït completament |
| **Backup i restauració** | Exportació xifrada i còpies automàtiques | Manual, còpia del fitxer .kdbx |
| **Portabilitat** | Molt alta (web, mòbil, escriptori) | Alta (fitxer transportable) |
| **Dependència del núvol** | Sí (o autohospedat) | No |
| **Complexitat d’ús** | Baixa (interfície intuïtiva) | Mitjana (entorn més tècnic) |

---

## **3. Avantatges i Inconvenients**

### **Bitwarden (Online / Núvol)**

**Avantatges:**
- Sincronització automàtica entre dispositius.  
- Interfície moderna i fàcil d’utilitzar.  
- Accessible des del web sense instal·lacions addicionals.  
- Autenticació multifactor (2FA) integrada.  
- Opció d’autohospedatge per a entorns corporatius.

**Inconvenients:**
- Dependència d’una infraestructura en línia.  
- Exposició teòrica en cas de vulnerabilitat dels servidors del proveïdor (tot i el xifrat end-to-end).  
- Model freemium amb certes funcions de pagament.

---

### **KeePassXC (Offline / Escriptori)**

**Avantatges:**
- Control total de les dades: el fitxer roman localment.  
- Sense dependència de tercers ni connexió a Internet.  
- 100% gratuït i open source.  
- Portable (fitxer .kdbx pot copiar-se en dispositius externs).  

**Inconvenients:**
- Sincronització manual (no apta per a usuaris amb múltiples dispositius).  
- Corba d’aprenentatge més pronunciada.  
- No disposa d’infraestructura per a còpies de seguretat automàtiques.  

---

## **4. Recomanació Final**

Després d’avaluar ambdues opcions, **es recomana adoptar *Bitwarden*** com a gestor corporatiu per al personal tècnic d’EverPia, per les següents raons:

1. **Equilibri entre seguretat i usabilitat:** Ofereix xifratge end-to-end i una interfície senzilla.  
2. **Accés multi-dispositiu i sincronització automàtica:** Imprescindible per a equips tècnics que treballen en diversos entorns.  
3. **Gestió centralitzada i auditable:** Permet futures polítiques corporatives de seguretat (grups, rols, 2FA).  
4. **Codi obert i auditat:** Transparència i confiança en el model de seguretat.  

En entorns crítics o sense connexió, **KeePassXC** pot ser utilitzat com a alternativa de seguretat reforçada local, però la solució principal recomanada és **Bitwarden (versió Enterprise o autohospedada)**.
