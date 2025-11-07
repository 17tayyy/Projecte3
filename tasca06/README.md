# Fase Práctica: Diagnosi de Noms (Auditoría amb CLI)

Objectiu: demostrar l'ús de les principals utilitats de diagnosi DNS en els sistemes operatius del client (Linux/macOS i Windows). Per a la demostració s'utilitzarà un equip Zorin amb dues interfícies: NAT i adaptador pont amb IP configurada.

## A. Diagnòstic avançat amb dig (Linux / macOS)

Per a cada comanda, executeu la instrucció indicada i captureu la sortida (pantallazo o text). A continuació, responeu l'anàlisi indicada.

1. Comanda 1 — Consulta bàsica de registre A  
  Comanda:
  ```
  dig xtec.cat A
  ```
  Anàlisi: Identifiqueu la IP de resposta, el valor TTL i el servidor que ha respost a la consulta.

2. Comanda 2 — Consulta de servidors de noms (NS)  
  Comanda:
  ```
  dig tecnocampus.cat NS
  ```
  Anàlisi: Quins són els servidors de noms autoritatius per a aquest domini?

3. Comanda 3 — Consulta detallada SOA  
  Comanda:
  ```
  dig escolapia.cat SOA
  ```
  Anàlisi: Quin és el correu de l'administrador (format SOA) i el número de sèrie del domini?

4. Comanda 4 — Resolució inversa  
  Comanda:
  ```
  dig -x 147.83.2.135
  ```
  Anàlisi: Quina informació de l'enregistrament PTR s'obté? Hi ha aliases (CNAME) o dades addicionals?

## Comprovació amb nslookup (multiplataforma)

nslookup té un mode interactiu (prompt >). Ús bàsic:
- set type=<TIPUS>  (A, AAAA, MX, NS, SOA, TXT, ALL)
- server <IP_o_nom> (canviar servidor de noms)
- exit

5. Comanda 5 — Consulta bàsica no autoritativa  
  Procediment:
  - llançar `nslookup`
  - `set type=A`
  - `tecnocampus.cat`
  Anàlisi: Per què la resposta indica que és no autoritativa? (explicar l'origen de la resposta i el paper del cache/servidor consultat)

6. Comanda 6 — Consulta autoritativa  
  Procediment:
  - dins `nslookup`: `server <IP_del_primer_NS_obtingut_amb_dig>`
  - `set type=A`
  - `tecnocampus.cat`
  Anàlisi: Quines diferències s'observen respecte la comanda 5? (registre autoritatiu, temps de resposta, secció ADDITIONAL, etc.)

## Entrega: ![guia.md](./guia.md)

Crear un fitxer ![`guia.md`](./guia.md) amb:
- Les 6 captures (o sortides textuals) de les comandes anteriors.
- Les respostes d'anàlisi per a cada comanda (concises i tècniques).
- Resultats de les proves de resolució local i conclusions breus sobre el comportament observat.
- Qualsevol comanda addicional emprada per comprovacions (amb la sortida adjunta).

Assegureu-vos d'incloure la data, el sistema operatiu i la configuració de xarxa (NAT / pont i adreces IP) en la capçalera del document.
