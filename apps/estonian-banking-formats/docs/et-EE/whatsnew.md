---
---
##### Infoks seoses 20.03.2023.a. jõustuvate Euroopa Keskpanga uute nõuetega ISO faili struktuuris
- _BC maksete XML faili sisu on juba täna tehniliselt nõuetega kooskõlas_
  - _Tuleb vaid jälgida, et EU väliste maksete puhul oleks Hankija pangakonto kaardil täidetud Saaja panga aadressiandmed (linn ning riik eelkõige)_
<br>
<br>

##### Versioon 19.4.22350.0
- Lisatud loogika, et laekumisžurnaalis "Seo kanded..." nupust arvete valimisel, täidetakse Laekumisžurnaali real kirjelduse väli seotud arvete numbritega.
  - Saab aktiveerida loogika, et kui müügiarvel on täidetud välise dokumendi number, siis tuleb see kirjeldusse.
  - Täiendus parandab pangakontoandmikukannete loetavust ning seeläbi ka kassaorderi sisu.
<br>

##### Versioon 19.4.22329.0
- Hankijatele maksete loomise täiendus:
  - Üksiku arve puhul määratakse selgituseks senise "Arve 123 makse" asemel lihtsalt "Arve 123" (inglise keeles vastavalt "Payment of Invoice 123" asemel lihtsalt "Invoice 123")
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
