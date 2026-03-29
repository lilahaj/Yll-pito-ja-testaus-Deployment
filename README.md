<a href='https://coveralls.io/github/lilahaj/Yll-pito-ja-testaus-Deployment?branch=main'><img src='https://coveralls.io/repos/github/lilahaj/Yll-pito-ja-testaus-Deployment/badge.svg?branch=main' alt='Coverage Status' /></a>

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

- **Testatut tiedostot:**

| File                 | % Stmts | % Branch | % Funcs | % Lines |
| -------------------- | ------- | -------- | ------- | ------- |
| add.js               | 100     | 100      | 100     | 100     |
| at.js                | 100     | 100      | 100     | 100     |
| camelCase.js         | 100     | 100      | 100     | 100     |
| capitalize.js        | 100     | 100      | 100     | 100     |
| castArray.js         | 100     | 66.66    | 100     | 100     |
| ceil.js              | 100     | 100      | 100     | 100     |
| clamp.js             | 100     | 33.33    | 100     | 100     |
| countBy.js           | 100     | 100      | 100     | 100     |
| defaultTo.js         | 100     | 100      | 100     | 100     |
| difference.js        | 100     | 66.66    | 100     | 100     |
| divide.js            | 100     | 100      | 100     | 100     |
| drop.js              | 100     | 40       | 100     | 100     |
| endsWith.js          | 89.18   | 40       | 100     | 89.18   |
| eq.js                | 100     | 75       | 100     | 100     |
| every.js             | 100     | 83.33    | 100     | 100     |
| filter.js            | 100     | 80       | 100     | 100     |
| get.js               | 100     | 50       | 100     | 100     |
| isArguments.js       | 100     | 100      | 100     | 100     |
| isArrayLike.js       | 100     | 100      | 100     | 100     |
| isArrayLikeObject.js | 100     | 100      | 100     | 100     |
| isBoolean.js         | 100     | 75       | 100     | 100     |
| isBuffer.js          | 100     | 16.66    | 100     | 100     |
| isDate.js            | 100     | 60       | 100     | 100     |
| isEmpty.js           | 88.4    | 52.94    | 100     | 88.4    |
| isLength.js          | 100     | 100      | 100     | 100     |
| isObject.js          | 100     | 75       | 100     | 100     |
| isObjectLike.js      | 100     | 100      | 100     | 100     |
| isSymbol.js          | 100     | 80       | 100     | 100     |
| isTypedArray.js      | 100     | 60       | 100     | 100     |
| keys.js              | 100     | 100      | 100     | 100     |
| map.js               | 100     | 75       | 100     | 100     |
| memoize.js           | 96.87   | 55.55    | 100     | 96.87   |
| reduce.js            | 100     | 66.66    | 100     | 100     |
| slice.js             | 86.95   | 30       | 100     | 86.95   |
| toFinite.js          | 87.5    | 40       | 100     | 87.5    |
| toInteger.js         | 100     | 66.66    | 100     | 100     |
| toNumber.js          | 81.53   | 40       | 100     | 81.53   |
| toString.js          | 88.09   | 60       | 100     | 88.09   |
| upperFirst.js        | 100     | 100      | 100     | 100     |
| words.js             | 97.36   | 71.42    | 100     | 97.36   |

- **Testaamattomat tiedostot:**  
   `chunk.js`, `compact.js`, `toFinite.js`, `toNumber.js` ja `memoize.js`

### 3. Tuotantovalmiuden arviointi

Kirjasto ei ole missään nimessä valmis tuotantokäyttöön.

Vaikka ohjelmisto saavuttaa lähes täydellisen testikattavuuden lukumäärällisesti, Chai paljasti useita virheitä. Tämä toimii erinomaisena esimerkkinä siitä, että pelkkä kattavuusprosentti ei anna takeita ohjelmiston laadusta.

**Löydetyt bugit:**  
Bugit ovat mainittu **Issues** välilehdessä.

### 4. Käytetyt työkalut ja linkit

- **Coverage Status:** Raportti ja Badge Coverallsiin (linkattu tiedoston yläreunassa).
- CI putken testien raportointi käy selväksi GitHubin **Actions**-välilehdeltä ja vikojen raportointi **Issues**-välilehdeltä.
