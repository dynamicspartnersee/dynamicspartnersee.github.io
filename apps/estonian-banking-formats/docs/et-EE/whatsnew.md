---
---
##### Infoks seoses 21.11.2022.a. jõustuvate Euroopa Keskpanga uute nõuetega ISO faili struktuuris
- _BC maksete XML faili sisu on juba täna tehniliselt nõuetega kooskõlas_
  - _Tuleb vaid jälgida, et EU väliste maksete puhul oleks Hankija pangakonto kaardil täidetud Saaja panga aadressiandmed (linn ning riik eelkõige)_
<br>
<br>

##### Versioon 19.4.22188.0
- Hankijatele maksete loomise täiendused:
  - Makseid saab filtreerida samasse panka, millelt toimub väljamakse (et teha võimalikult palju nn pangasiseseid makseid, hoidmaks kokku ülekandekulusid)
  - Makseid saab summerida kombinatsioonis hankija ja viitenumber (sama viitenumbriga arved pannakse samale maksele)
  - Summeerimise puhul tulevad makse selgitusse kõik summeeritud arvete numbrid (eeldusel, et välja pikkus seda võimaldab)
  - Maksete selgituse koostamisel arvestatakse Hankija kaardil oleva keele tähisega (eesti ja inglise keel toetatud)
- UX täiendused pangakonto kaardil, hankija pangakonto kaardil ning peažurnaalis
<br>

##### Versioon 15.3.22117.0
- Lahendatud aegluse probleem kassaorderi trükkimisel, kui PR registrites on palju kandeid
<br>

##### Versioon 15.3.21182.0
- Parandatud maksete sobitamisel, pika nimega Hankija/Kliendi puhul, tekkinud Stringi pikkus on suurem kui 50 tähemärki viga
<br>

##### Versioon 15.0.21118.0
- Lisandus Viitenumber kont.kreeditarvele
- Viitenumber kuvatakse Kliendiandmiku kannete sidumise lehel
- Installimise tegevused (Andmevah.määratlus, Panga eks/imp seadistus, Dok.kujundused) käivituvad nüüdsest "Estonian Banking Formats Setup" lehe avamisel
