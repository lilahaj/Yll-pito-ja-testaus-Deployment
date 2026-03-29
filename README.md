<a href='https://coveralls.io/github/lilahaj/Ohjelmistojen-yll-pito-ja-testaus?branch=main'><img src='https://coveralls.io/repos/github/lilahaj/Ohjelmistojen-yll-pito-ja-testaus/badge.svg?branch=main' alt='Coverage Status' /></a>


# Student template

## Purpose of this repository

This is a project template for students participating in Software Testing course
at LAB University of Applied Sciences.

The repository only contains the source code that is under testing, `package.json` skeleton
and LICENSE file.

Source code folder contains a separate license file that must **NOT** be removed under any circumstances!
Removing this license file directly violates terms and conditions of the software under testing.
Individuals who remove or modify the license file will also carry the consequences.

---

## Tehtävän dokumentaatio

### 1. Toiminta ja asennus

Kirjaston testaus toteutettiin Mochalla ja Chailla, koodikattavuuden mittauksessa käytettiin c8:a. CI/CD-putki on luotu GitHub Actions -järjestelmään. Työnkulkuihin kuuluu automaattinen testien ajo useilla eri Node.js-versioilla sekä lähetys Coveralls-palveluun, kun koodia pushataan mainiin.

### 2. Testatut ja testaamattomat tiedostot

- **Testatut tiedostot:** Testit on kirjoitettu yhteensä 31 eri modulin/funktion toiminnalle (kuten esim. `add.js`, `divide.js`, `isEmpty.js`, `filter.js`, `get.js`, `camelCase.js` ja `slice.js`). Nämä testit tutkivat lähinnä "happy path" -toiminnallisuuskia sekä keskeisempiä ominaisuuksia.
- **Testaamattomat tiedostot:** Suoraa, varsinaista yksittäistä testausta eivät sisältäneet moduulit, kuten `chunk.js`, `compact.js`, `toFinite.js`, `toNumber.js` ja `memoize.js`. Ne kuitenkin suoriutuivat osin c8:n mukaisesti ("peittyivät osittain"), sillä testatut funktiot nojasivat näihin sisäisesti.
  Ympäristölle asetetun vaatimuksen 60 % koodikattavuusylitys (excluding `.internal`) toteutui erinomaisesti yli 97 % peitolla.

### 3. Tuotantovalmiuden arviointi (Production Readiness)

Kirjasto **ei ole valmis tuotantokäyttöön** (`NOT ready for production`).
Korkea (>97%) testikattavuus ei todista kirjaston virheettömyyttä: kattavuus todistaa vain, mitkä koodirivit suoritettiin kertaalleen testien aikana, ei sitä ymmärretäänkö säännöt oikein reunaehtojen tai puutteellisten tarkistusten osalta.

Tästä on todisteena kirjaston varsinaisen koodilogiikan käsin tarkastelussa ja testiajoissa havaitut vakavat ohjelmointivirheet (mahdollisesti assignmenttiin tarkoituksella jätettyjä):

1. `divide.js` jakaa jakajan itsellään (palauttaa aina arvon 1).
2. `filter.js` palauttaa alustuksena `[[]]` sisältäen tyhjän arrayn sijasta `[]`, ja suodattaessaan se saattaa ylikirjoittaa osan tiedosta.
3. `chunk.js` tallentaa jatkuvasti kaikki pätkityt (chunked) elementit suoraan taulukon alkuindeksiin ylikirjoittaen kaiken.
4. `compact.js` käyttää väärää alustusarvoa `-1` taulukon sisäisenä indeksinsä.
   Kaikki yllä mainitut loogiset ongelmat ja ohjelmointivirheet on kirjattu GitHub-projektin ohjelmavikoina (`Issues`) issue-trackeriin korjattavaksi. Tässä tilassa ohjelmistoa on hasardi viedä tuotantoympäristöihin.

### 4. Käytetyt työkalut ja linkit

- **Coverage Status (Coveralls):** Raportti ja Badge Coverallsiin (linkattu tiedoston yläreunassa).
- CI putken testien raportointi käy selväksi GitHubin **Actions**-välilehdeltä ja vikojen raportointi **Issues**-välilehdeltä.
