---
---
##### Infoks seoses Euroopa Keskpanga uute nõuetega ISO faili struktuuris
- _BC maksete XML faili sisu on jätkuvalt tehniliselt nõuetega kooskõlas_
  - _Tuleb vaid jälgida, et **EU väliste maksete puhul** oleks Hankija pangakonto kaardil täidetud Saaja panga aadressiandmed (linn ning riik eelkõige)_
<br>
<br>

##### Versioon 21.5.24135.1
- Eesti pangaformaatide seadistusse lisatud väli "Makse teade töötajale", kuhu saab valida maksežurnaali välja "Teade saajale" sisu koostamise loogika.
- Täiendatud maksežurnaali "Soovita makseid hankijale" protseduuri nii, et nüüd täitub ka kirjeldus seotud arvete infoga.
- Žurnaalides sidumisel jääb nüüd kirjelduse ette osapoole (klient, hankija, töötaja) nimetus, et oleks kande kirjelduse alusel kohe näha, kellega tehing toimus.  

##### Versioon 21.5.24119.0
- Parandatud müügidokumendi konteerimisel välja “Makse viitenr.” mittetäitumine kliendiandmiku kannetes (sh täidetakse tagantjärgi puuduvad viitenumbrid avatud kliendiandmiku kannetel).
- Täiendatud pangaväljavõtte sidumise loogikat, et tehingu viitenumber žurnaalis ei mõjutaks negatiivselt sidumise tulemust.  

##### Versioon 21.5.24080.2
- Lahendatud pangaväljavõtte importimisel tekkinud veaolukord, kus valuutatehingut sisaldanud väljavõtte puhul tuli veateade "Fail, mida püüate importida, sisaldab rohkem kui üht pangaväljavõtet".  

##### Versioon 21.5.24080.1
- BC24 versiooniga ühilduv lahendus.
- Viidud lokaliseeritud pangaväljavõtte sidumisreeglite rakendamine tehniliselt üle uusimatele eventidele.
- Lisatud võimalus aktiveerida Eesti pangaformaatide seadistuses "Seo viitenr. alusel laekumised Kliendiga", mis kliendiandmiku kannete puudumisel seob laekumise viitenumbri alusel otse Kliendiga (kliendipõhiste viitenumbrite korral).
  - Analoogselt kui kasutaja käsitsi määraks Maksete sobitamise žurnaalis Konto liik väärtuseks Klient ja konto nr. väärtuseks kliendi numbri.
    - _Aitab olukordades, kus kliendid tasuvad ilma arveta raha ette ning kiirendab viitenumbri filtri alusel käsitsi sidumist._
- Parandatud olukord, kus "Soovita makseid hankijale" toimingu käivitamisel, kui kasutati Summeeri hankija kohta ja viitenumbri alusel kombinatsiooni, tekkisid kõikide arvete numbrid erinevatele ridadele.
- Lisatud automaatselt genereeritav teisendusreegel "REMOVE_COMPANY_NAME", mida saab vajadusel kasutada andmevahetusmääratluse välja vastendamisel
  - _nt panna teisendusreegel külge ridadele, mille Välja ID = 15, selleks et Maksja/Saaja nimi ei sisaldaks ettevõtte enda nime (LHV XML failist pangaväljavõtte importimisel)_.
- Väiksemad UX täiendused.  

##### Versioon 19.4.23282.0
- Lisatud makse ekspordi formaadi pain.001.001.09 tugi (_valiku nimeks pangakontol "SEPACT-EE-001.001.09"_), mis saab LHV pangas kohustuslikuks 1.nov 2023.a. ning hiljem teistes pankades.
  - Eeldusel, et LHV pangakontol on SWIFT tähiseks LHVBEE22 ning seniseks makse ekspordi formaadiks "SEPACT-EE", siis äpi uuendamise käigus määratakse automaatselt uueks formaadiks pangakonto kaardile "SEPACT-EE-001.001.09"
    - Teiste pankade puhul tuleb kasutajal see valik hiljem ise teha _(sest äpi uuenduse avaldamise hetkel oli ainult LHV võimeline uut maksefaili formaati vastu võtma)_.  

##### Versioon 19.4.23244.0
- Tehtud seadistusega valitavaks, kas mitte-eesti pangakontole mineva makse maksekorraldusele lisatakse viitenumber või makse selgitus (_eeldusel, et tegu on viitenumbriga maksega_).  

##### Versioon 19.4.23187.0
- Lisatud loogika, mis maksete sobitamise žurnaali konteerimisel täidab makse viite (ehk viitenumbri) ka kliendi- ja hankijaandmiku kannetes.
- Maksete sobitamise žurnaalis on nüüd visuaalselt eristatav, kui tehingu Viitenumber ja Seotud kande viitenumber ühtivad (_roheline_) või erinevad (_punane_).
- Parandatud teatud juhtudel peažurnaalis tekkinud veaolukord "Tabelit Klient/Hankija pole olemas".  

##### Versioon 19.4.23152.0
- Muudetud avalikuks viitenumbri genereerimise protseduur koodis (et kliendipõhistes laiendustes ei peaks oma viitenumbri genereerimise protseduuri välja mõtlema).  

##### Versioon 19.4.23124.0
- Täiendatud maksežurnaalist maksete faili loomise loogikat nii, et kui real on viitenumber aga saaja pangakonto pole Eesti IBAN (st pole EE algusega), siis ei lisata viitenumbrit vastavale maksele.
  - _Täiendus vajalik selleks, et õnnestuks sellise makse maksefaili import SwedBank internetipanka_  

##### Versioon 19.4.23107.0
- Täiendatud pangaväljavõtte sidumise loogikat nii, et kui kliendilt saadud laekumisel on viitenubmer, siis vastendatakse klient alati esmalt kliendiandmikukannete alusel (vajalik selleks, et kui maksja on ka klient, et siis sobitataks õige kliendi alt tasutud arve)  

##### Versioon 19.4.23082.0
- Parandatud žurnaalides tekkinud veaolukord "Tabelit Klient/Hankija pole olemas."  

##### Versioon 19.4.23081.0
- Parandatud žurnaalides tekkinud veaolukord "Tabelit Eesti pangaformaatide seadistus pole olemas."  

##### Versioon 19.4.23060.0
- Lisatud hooldusmooduli arvetele viitenumbrite automaatne genereerimine (_analoogne loogika, kui müügiarvetel_), kui Eesti pangaformaatide seadisituses on viitenumbrid kasutusele võetud
  - Analoogselt müügiarvetele liigub viitenumber ka kliendiandmiku kannetele, et oleks võimalik hiljem laekumist viitenumbri abil siduda  

##### Versioon 19.4.23037.0
- Maksete sobitamise žurnaali lisatud väli "Seotud kande viitenumber", mis näitab reaga seotud kliendi/hankija/töötajaandmiku kande viitenumbrit, kontrollimaks vastavust tehingu viitenumbrile
- Kliendi pangakonto kaardile lisatud Makse saaja blokk, võimaldamaks makse saaja nime muutmist ka hüvitiste maksmisel kliendil  
  
##### Versioon 19.4.22356.0
- Täiendatud maksete sobitamise žurnaalis viitenumbri alusel müügidokumentide sidumist laekumistega (sh sidumise kiirust)  

##### Versioon 19.4.22350.0
- Lisatud loogika, et laekumisžurnaalis "Seo kanded..." nupust arvete valimisel, täidetakse Laekumisžurnaali real kirjelduse väli seotud arvete numbritega
  - Saab aktiveerida loogika, et kui müügiarvel on täidetud välise dokumendi number, siis tuleb see kirjeldusse
  - Täiendus parandab pangakontoandmikukannete loetavust ning seeläbi ka kassaorderi sisu  

##### Versioon 19.4.22329.0
- Hankijatele maksete loomise täiendus:
  - Üksiku arve puhul määratakse selgituseks senise "Arve 123 makse" asemel lihtsalt "Arve 123" (inglise keeles vastavalt "Payment of Invoice 123" asemel lihtsalt "Invoice 123")  

##### Versioon 19.4.22188.0
- Hankijatele maksete loomise täiendused:
  - Makseid saab filtreerida samasse panka, millelt toimub väljamakse (et teha võimalikult palju nn pangasiseseid makseid, hoidmaks kokku ülekandekulusid)
  - Makseid saab summerida kombinatsioonis hankija ja viitenumber (sama viitenumbriga arved pannakse samale maksele)
  - Summeerimise puhul tulevad makse selgitusse kõik summeeritud arvete numbrid (eeldusel, et välja pikkus seda võimaldab)
  - Maksete selgituse koostamisel arvestatakse Hankija kaardil oleva keele tähisega (eesti ja inglise keel toetatud)
- UX täiendused pangakonto kaardil, hankija pangakonto kaardil ning peažurnaalis  

##### Versioon 15.3.22117.0
- Lahendatud aegluse probleem kassaorderi trükkimisel, kui PR registrites on palju kandeid  

##### Versioon 15.3.21182.0
- Parandatud maksete sobitamisel, pika nimega Hankija/Kliendi puhul, tekkinud Stringi pikkus on suurem kui 50 tähemärki viga  

##### Versioon 15.0.21118.0
- Lisandus Viitenumber kont.kreeditarvele
- Viitenumber kuvatakse Kliendiandmiku kannete sidumise lehel
- Installimise tegevused (Andmevah.määratlus, Panga eks/imp seadistus, Dok.kujundused) käivituvad nüüdsest "Estonian Banking Formats Setup" lehe avamisel
