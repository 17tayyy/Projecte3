# 🌍 P04: Documentació del servidor DNS  

Formeu part de l’equip de **sistemes d’EverPia** i us toca preparar un **servidor DNS** com a prova de concepte per al client **Digicore**. Ara mateix tot funciona en una màquina virtual, però l’objectiu és **pujar els fitxers a GitHub** perquè qualsevol pugui tornar a desplegar el servidor d’una manera ràpida i sense complicacions.

---

## 🎯 Objectiu  
Facilitar que, en replicar el servidor DNS, **no calgui reconfigurar-lo des de zero**: només cal descarregar els arxius i **reiniciar el servei** perquè tot quedi operatiu.

---

## 🔧 Fase 1: Connectivitat i Exportació dels Fitxers  

### 🛠️ Pas 1.1: Configuració de la Interfície Host-Only  
1. Afegiu una segona interfície de xarxa a la VM Ubuntu Server i poseu-la en mode **Host-Only**.  
2. Configureu-la i assegureu-vos que queda activa.  
3. Comproveu que hi ha **connectivitat** entre la màquina física i la virtual.

### 🔒 Pas 1.2: Transferència Segura amb SCP  
Amb la connexió Host-Only preparada, utilitzareu **SCP**, inclòs dins SSH, per copiar els fitxers de configuració cap al vostre ordinador.

**Fitxers que heu de copiar:**  
- `/etc/bind/named.conf.options`  
- `/etc/bind/named.conf.local`  
- Fitxers de zona ubicats a `/etc/bind/zones`

---

## 📤 Fase 2: Pujada a GitHub  

### 📄 Pas 2.1: Crear Carpeta i README  
1. Creeu la carpeta `producte04` i afegiu-hi el fitxer `README.md`.  
2. Dins del README, incorporeu-hi el **nom del producte** i una **descripció del contingut**.

### ☁️ Pas 2.2: Pujar els Fitxers  
1. Pugeu tots els fitxers de configuració a la carpeta `producte04`.  
2. Creeu la carpeta `zones` abans de pujar-hi els fitxers de zona.  
3. Si GitHub no permet crear carpetes buides, afegiu un fitxer temporal i elimineu-lo després.

---

## 🟢 Resultat Final  
Un cop finalitzat el procés, disposareu de:

- Un **repositori a GitHub** amb tota la configuració del servidor DNS.  
- Un sistema **replicable fàcilment** en qualsevol servidor Linux.  
- Una **documentació clara i ordenada** per facilitar manteniments futurs.

## 📎 Documents  
Podeu consultar cadascun dels fitxers aquí:

- ![**named.conf.local**](./named.conf.local): definició de zones.  
- ![**named.conf.options**](./named.conf.options): configuració general.  
- ![zones](./zones/): fitxers de configuració de les zones.
