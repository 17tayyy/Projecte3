# 📘 Guia LDAP

## 🖥️ Servidor (Ubuntu Server)

---

### 🔧 Configurem els adaptadors de xarxa amb netplan

![image20](img/image19.png)

---

### 🔧 Configurem el segon adaptador amb DHCP4 activat i apliquem canvis

![image25](img/image22.png)

---

### 🌐 Escribim el domini server.innovatechXX.test (XX és el número de llista)

![image11](img/image12.png)

---

### 🏷️ Posem el hostname

![image1](img/image53.png)

---

### 📦 Instal·lem slapd i ldap-utils

![image3](img/image32.png)
![image2](img/image49.png)

---

### ✔️ Comprovem que el servei slapd funciona

![image2](img/image44.png)

---

### 🔑 Configurem la contrasenya de slapd

![image4](img/image31.png)

---

### ✔️ Verifiquem que la configuració s’ha aplicat correctament

![image2](img/image48.png)

---

### 🗂️ Creem els arxius OU d’usuaris i els afegim a LDAP

![image2](img/image16.png)
![image5](img/image7.png)
![image2](img/image43.png)

---

### 🗂️ Fem el mateix amb els grups

![image2](img/image45.png)
![image2](img/image45.png)

---

### 🔍 Fem una cerca amb ldapsearch per verificar que tot funciona

![image2](img/image34.png)

---

### 📦 Instal·lem LDAP Account Manager

![image2](img/image27.png)

---

### 🌐 Obrim la web del LAM i accedim a /lam/templates/login.php

![image2](img/image29.png)

---

### 🔐 Entrem amb el LAM configurat

![image2](img/image6.png)

---

### ⚙️ Configurem l’account manager

![image2](img/image40.png)
![image2](img/image5.png)
![image2](img/image33.png)

---

### 🔑 Accedim com administrador

![image2](img/image20.png)

---

### ➕ Creem el perfil quan ens aparegui el missatge

![image2](img/image28.png)

---

### 👥 Ara creem els grups i usuaris

![image2](img/image4.png)
![image2](img/image42.png)
![image2](img/image21.png)
![image2](img/image50.png)
![image2](img/image26.png)
![image2](img/image39.png)

---

# 🖥️ Client

---

### 🔄 Actualitzem el sistema

![image2](img/image46.png)

---

### 🏷️ Configurem el hostname i el domini al fitxer /etc/hosts

#### Domini
![image34](img/image14.png)
![image34](img/image56.png)

#### Hostname
![image34](img/image2.png)

---

### ✔️ Comprovem que els canvis s’han aplicat

![image34](img/image18.png)

---

### 🌐 Fem un dig per assegurar que el servidor respon

![image34](img/image52.png)

---

### 📦 Instal·lem les utilitats LDAP al client

![image34](img/image17.png)

---

### ⚙️ Configurem LDAP en finalitzar la instal·lació

![image34](img/image9.png)
![image4](img/image54.png)
![image34](img/image35.png)
![image34](img/image36.png)
![image34](img/image1.png)

---

### 🔍 Fem un ldapsearch des del client

![image34](img/image57.png)

---

# 🔐 Integració PAM i NSS

---

### 🧩 Modifiquem nsswitch per fer servir LDAP

![image7](img/image30.png)
![image7](img/image13.png)

---

### 🔧 Modifiquem /etc/pam.d/common-password (eliminem use_authok)

![image7](img/image51.png)
![image7](img/image37.png)

---

### 🧩 Modifiquem /etc/pam.d/common-session per crear perfils automàticament

![image7](img/image51.png)
![image7](img/image10.png)

---

### 👤 Comprovem que s’han creat els usuaris

![image7](img/image23.png)

---

### 📝 Modifiquem gdm-launch-environment per permetre login amb usuaris LDAP

![image7](img/image41.png)

---

### 🔐 Provem el login amb l’usuari tech01 de LDAP

![image7](img/image38.png)

---

# ✅ Ja ens podem loguejar — Finalitzat!
