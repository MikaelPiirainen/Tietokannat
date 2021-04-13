# Tietokannat TTC2020 - Harjoitustyö

VIDEON LINKKI

## Suunnitelma


### Vaatimusmäärittely

**Elokuvatietokanta**


* "elokuva_db" -tietokanta
* Työryhmä: Mikael Piirainen AA2799
* Versio 1.0


**1. Johdanto**

Tarkoituksena suunnitella ja luoda tietokanta, joka sisältää tietoa elokuvista, niiden arvosteluista ja näyttelijöistä ja muusta. Tietokanta luodaan harjoitustyönä TTC2020 kurssilla, jota opettaa Ari Rantala.

**2. Yleiskuvaus**

Tietokanta työstetään lokaalisti ja siirretään omalle palvelimelle, kun se on valmis. Tietokantaa varten luodaan  käyttöliittymä, jolla voidaan hakea tietoja verkkosivulle. Toteutus tehdään MySQL Workbench:illä sekä käyttöliittymä tehdään PHP-ohjelmointi kielellä. Dokumentaatio kirjoitetaan GitHubiin ja julkaistaan sivustona hyödyntäen MkDocs:ia.

**3. Toiminnot**

Pakolliset toiminnot:

* Elokuvien tietojen tallennus
* Arvostelujen teko
* Elokuvien haku tietokannasta
* Tietojen ylläpito (komennoilla tai käyttöliittmällä)

---

### Käsiteanalyysi


| **Käsite-ehdokkaat:** | **Taulu** | **Taulu** | **Taulu** | **Taulu** | **Taulu** |
| --- | --- | --- | --- | --- | --- |
| ElokuvaID | ElokuvaID | Ohjaaja | Näyttelijät | Arvostelu | KategoriaID |
| ElokuvaNimi | ElokuvaNimi |  | Näyttelijä | Arvostelija | KategoriaNimi |
| Kuvaus | Kuvaus |
| Vuosi | Vuosi |
| Ohjaaja | Kesto |
| Näyttelijä |
| Arvostelija |
| Arvostelu |
| KategoriaID |
| KategoriaNimi |
| Kesto |
| Näyttelijät |


**Visuaalinen hahmotus ja lisää käsitteitä:**

Hahmotus tehty draw.io sovelluksella.

![](ht_draw.png)


**Perustelut ratkaisuille:**

* Elokuva ja Näyttelijä tauluilla on moni-moneen yhteys ja siihen syntyy liitostaulu Näyttelijät. Isäntätaulujen pääavaimet toimivat liitostaulun viiteavaimina. _Elokuvalla voi olla useita näyttelijöitä ja näyttelijät voivat olla useissa elokuvissa._

* Elokuva ja Arvostelija tauluilla samat perustelut kuin Elokuva - Näyttelijätauluilla, lisäksi liitostauluun lisätään arvosana.

* Elokuva ja Kategoria tauluilla on yksi-moneen yhteys. _Elokuva kuuluu kategoriaa ja kategoriaan voi kuulua useita elokuvia._ (Tiedostan, että useilla elokuvilla saatta olla monia kategorioita, mutta haluan tähän tietokantaan vain "pää kategorian").

* Elokuva ja Ohjaaja tauluilla on yksi-moneen yhteys. _Elokuvalla on yksi ohjaaja ja ohjaaja on voinut tehdä monta elokuvaa._ (Tämä on yleisin elokuvascenessä, vaikkakin poikkeuksiakin löytyy: "Russo Brothers: Avengers: Infinity War & Endgame, The Wachowskis: Matrix 1-3)

---

### ER-kaavio

ER-kaavio tehty MySQL Workbenchi:llä. Luovuin "kansalaisuudesta", koska sille pitäisi olla oma taulunsa, mutta se ei ole niin välttämätön elokuvatietokannassa.

![](ht_er.png)


---

## Tietokannan toteutus

### Tietokannan luonti

Tietokanta luodaan Workbenchin FORWARD ENGINEERING optiolla.

Tietokanta ja taulut onnistuivat.

![](ht_db1.png)

### Tietojen lisäys tauluihin

### SQL-skripti

### SQL-kyselyjä

---

## Käyttöliittymä

Kuvia, tekstiä ja linkki

## Itsearviointi

## Koodit

