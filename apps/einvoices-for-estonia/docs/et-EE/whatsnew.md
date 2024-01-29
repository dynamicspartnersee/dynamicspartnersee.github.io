---
---
##### Versioon 21.5.24017.1
- Parandatud peale lahenduse installimist Finbite-st ostuarvete pärimisel tekkinud veaolukord "Unknown error has occurred.".
  - Põhjuseks oli mittesobivas formaadis algne kuupäevkellaaeg väljal "Võta arved muudetud alates" (_peab olema formaadis YYYY-MM-DD HH:MM:SS_)
<br>

##### Versioon 21.5.24017.0
- Lisandus Müügi ja müügivõlgade seadistus lehele "E-kreeditarve summad miinusmärgiga", mis määrab, kas kogus ning seeläbi summad e-kreeditarvel (xml) kuvatakse miinusmärgiga.
- Lisatud Run Doc. Exchange koodiblokki event OnBeforeRun, mis võimaldab lisada kliendipõhist loogikat tööjärjekorra kannete käivitamise loogikasse.  
<br>

##### Versioon 21.5.23332.1
- Lisandus "Ära saada null summaga arvet" valik Dokumendi saatmise profiili loomisel kui tehakse "Saada Eesti e-arve automaatselt" valik.
  - Vajalik tühjade arvete saatmise vältimiseks.
- Lisandus lahenduse õiguste komplekt .al objektina.
<br>

##### Versioon 21.5.23237.0
- Lisandus EL e-arve standardi (PEPPOL BIS3 UML) formaadis müügiarvete saatmise ja ostuarvete vastuvõtmise tugi.
  - _Eeldusel, et kasutatav e-arvete operaator vastavat võimalust pakub._
- Lisandus liidestus operaatoriga RIK (Registrite ja Infosüsteemide Keskus), võimaldades e-arvete saatmist ning vastuvõtmist ilma operaatori kuluta.
- Lahendus kasutab nüüd BC standard registrikoodi andmevälju _(senise Eesti lokalisatsiooni Äriregistri äpi väljade asemel)_.
- UX täiendused _(lisandunud paljudele väljadele ja nuppudele seni puudunud selgitavad tooltipid)._  
<br>

##### Versioon 17.3.23251.0
- Lisatud arvete XML-i loomise koodi event OnBeforeCreateItemEntry, et oleks kliendipõhise arendusega võimalik luua oma variant arveridade ehk ItemEntry blokist.
- Parandatud tegevuse logi vaatamisel tõrge "Väli „OEA Request XML Message“ tabelis „Tegevuse logi“ on andmebaasis algse ja JIT-koormuse vahel muutunud".  
<br>

##### Versioon 17.3.23248.0
- Lisatud event OnBeforeFindItem, et oleks kliendipõhise arendusega võimalik luua oma saabunud e-ostuarvelt kaupade tuvastamise loogika.  
<br>

##### Versioon 17.3.23214.0
- Parandatud hooldusarve saatmisel olukord, kus read liigiga Maksumus (Cost) ei jõudnud e-arvele.  
<br>
  
##### Versioon 17.3.23172.0
- Lisandus võimalus lubada kasutajal konteerida ostuarvet ka siis, kui ostuarve summa ei ühti e-arve (sissetuleva dokumendi) summaga.  
<br>

##### Versioon 17.3.23166.0
- Värskendatud äpi logo
- Parandatud ostuarve loomisel kaupade tuvastamise probleem (_tekkis versiooniga 17.3.23088.0_)  
<br>

##### Versioon 17.3.23164.0
- Tehtud täiendus, mis uuendab automaatselt Finbite Teenuse URL-i uuele, alates 16.06.2023.a. kehtima hakkavale kujule (kõikides ettevõtetes):
  - Lisainfo <a href="https://help.finbite.eu/et/articles/7895353-peale-16-juunit-muutuvad-finbite-keskkonna-url-lingid" target="_blank">Finbite lehelt</a>
- Tehtud kasutusmugavuse täiendus nii, et kui kasutaja "Finbite (Omniva) dokumendivahetusteenuse seadistus" lehel vajutab toimingut "Taasta URL-ide vaikeväärtused", siis süsteem kontrollib, kas keskkond asub avalikus pilves (Saas) ning kui tegu on Sandbox liiki keskkonnaga, siis taastatakse vaike URL-iks Finbite testkkeskkonna URL. Kui aga tegu on Production keskkonnaga või asub OnPrem-is, siis, taastatakse vaike URL-iks Finbite Live keskkonna url.  
<br>

##### Versioon 17.3.23108.0
- Parandatud haruldane veaolukord "KM summa ei tohi olla negatiivne", mis tekkis kui arvel olid nii positiivse, kui negatiivse kogusega read ning ühtlasi tekkis automaatse ümardamise vajadus.  
<br>

##### Versioon 17.3.23105.0
- Parandatud veateadet "Väljal Kogus peab olema tabelis Osturida väärtus" tekitanud olukord, mis ilmnes kui real puudus kogus ning kui "Ostude ja ostuv. seadisuses", Eesti e-arvete seadete sektsioonis välja "Säilita kirjeldus ning ühiku hind" väärtuseks oli "kõikidel ridadel" ja kui muudeti ostuarve real PR Kontot/kaupa või kasutati "Kopeeri dokument" funktsionaalsust.
- Parandatud olukord, kus uue hankija esitatud e-ostuarve väljastaja ettevõtte riigiks ei olnud mitte kahetäheline kood vaid pikem riigi nimetus ning seetõttu automaatne hankija loomine ebaõnnestus.
<br> 

##### Versioon 17.3.23088.0
- BC22 ühilduvaks
  - Kuna kadus Kauba ristviited tabel, siis selle alusel enam e-arvest ostuarvet luues kauba vastet ei otsita.
- Lisatud event OnBeforeCreatePurchaseDocument  
<br>

##### Versioon 17.3.23059.0
- Lisandus võimalus saata e-arvena konteeritud hooldusarvet ja konteeritud hoolduse kreeditarvet.  
<br>

##### Versioon 17.3.22357.0
- Lisandus võimalus valida, kas e-arve/e-kreeditarve kuupäevana kasutatakse vastava arve/kreeditarve konteerimiskuupäeva või dokumendi kuupäeva
  - Valikut saab teha müügi ja müügivõlgade seadistuses, linnukesega "Konteerimiskuupäev e-arve kuupäevana"  
<br>

##### Versioon 17.3.22294.0
- Lisandus võimalus saata uuesti juba korra saadetud e-arvet
  - Selleks tuleb Konteeritud dokumendil nupule "Saada" avanevas aknas valida "Saada juba saadetud e-arve uuesti"  
<br>

##### Versioon 17.3.22285.0
- Arve XML-i loomise koodi lisatud event 'OnAfterCreateSellerProductIdAndBeforeDescription', võimaldamaks kliendipõhise arendusena e-arverea tag-ide lisamist
- Täiendatud e-arve XML-i loomise koodi nii, et ka null-summaga arve puhul tekiks arve VAT blokk _(Muudatus oli vajalik seetõttu, et osad e-arve vastuvõtjad lükkavad vastasel juhul arve automaatselt tagasi)_
- Parandatud olukord, kus Finbite arvekeskusest tulnud ostuarve lisamanustesse salvestus iga järgmise manusele lisaks juurde kõikide eelmiste manuste info
- Muudetud tehnilist andmevahetusmääratluse algandandmete laadimise loogikat _(Muudatus oli vajalik selleks, et lahenduse installeerimisel ei tekiks tõrget teatud andmetega uuemates BC versioonides)_  
<br>

##### Versioon 17.3.22257.0
<!--Release was here-->
- Lisandus automaatne ostuarvete ümardamise funktsionaalsus (et ei peaks käsitsi BC arve summat klapitama e-arve XML-is oleva summaga)
- Eemaldatud kaupade otsingu funktsionaalsuses, kaubaviidete tabelis kasutatud välja "Lõpeta vöötkoodi kasutamine" mittetäidetuse kontroll. _(Muudatus oli vajalik selleks, et lahendus oleks ühilduv BC21 versiooniga)_  
<br>

##### Versioon 17.3.22187.0
- Täiendatud XML-ist ostuarve loomise veakindlust tulenevalt mittekorrektsetest andmetest:
  - Kaupade tuvastamisel kontrollitakse XML-is oleva EAN andmestiku pikkust
  - Hankija loomisel kontrollitakse XML-is oleva meiliaadressi õigsust  
<br>

##### Versioon 17.3.22179.0
- Täiendatud valuutas ostuarve haldust (kui arve on kohalikus valuutas siis alati kustutatakse valuuta tähis ostuarvelt, sest muidu võib sinna sattuda väärtus hankija kaardilt)  
<br>

##### Versioon 17.3.22158.0
- Lisatud tugi müügiarve ja müügi kreeditarve ridadele liigiga "Kulu (kaup)"  
<br>

##### Versioon 17.3.22151.0
- Lisatud saatja registrikood Invoice tag-i parameetritesse, et e-arved jõuaks saajani, kes kasutavad operaatorina Registrite- ja infosüsteemide keskust (RIK)  
<br>

##### Versioon 17.3.22147.0
- Lisandus tugi välismaiste (ehk äriregistrikoodi mitte omavate) hankijate tuvastamisele, automaatsele hankija loomisele ning vastavate XML ostuarvete käsitlemisele 
- Täiendatud olemasoleva hankija otsimist (lisandus otsimine KM Koodi ning täpse nime alusel)  
<br>

##### Versioon 17.3.22096.0
<!--Unreleased
- Lisandus automaatne ostuarvete ümardamise funktsionaalsus (et ei peaks käsitsi BC arve summat klapitama e-arve XML-is oleva summaga)
-->
- Peppoli saatmisel Finbite-i lisatakse nüüd ka eakInvPartyCountry extension tag, mille puudumine võis saada takistuseks Finbite poolsel arve edastusel Peppol süsteemi
- Parandatud turvalisust päringute salvestamisel XML faili
- Lisatud kontroll välistamaks sama registrikoodiga teise hankija märkimist "Saada Finbite/FitekIn"
- UX täiendused (sh klientide ning hankijate loendis tuleb nüüdsest automaatselt "Saada Finbite/FitekIn" linnuke nähtavale jms)  
<br>

##### Versioon 17.3.22062.1
- Parandatud olukord, kus Finbite-ist tulnud e-ostuarve manuse nimes olnud mitteootuspäraste sümbolite tõttu e-ostuarve vastuvõtmine ebaõnnestus  
<br>

##### Versioon 17.3.22062.0
- Tehnilised täiendused, et saaks kliendipõhiste arendustena lisada valikusse täiendavaid E-arve operaatoreid
- UX täiendused (arve saatmisvalikute juurde lisatud selgitavad tooltipid)  
<br>

##### Versioon 17.3.22034.0
- Täiendatud XML-ist ostuarve loomist, et oleks hallatud juhtumid, kui XML-is puudub arverea netosumma "SumBeforeVAT" tag-i näol, kuid seda on võimalik tuletada alternatiivse info põhjal
- Muudetud installeerimise loogikat, et vältida vahest tekkinud "session is in the kill state" viga  
<br>

##### Versioon 17.3.21364.2
- Põhiandmete (kontod, dimensioonid ning hankijad) saatmine läbi Unifiedpost-i liidese FitekIn keskkonda  
<br>

##### Versioon 17.3.21364.1
- Konteeritud ostuarve numbri saatmine läbi Unifiedpost-i liidese FitekIn keskkonda (sh tööjärjekorra kandega)
- Rahvusvaheliste müügiarvete saatmise tugi (sh Finbite kaudu Peppol ja Unifiedpost kaudu nii Peppol kui muud roaming kanalid)
- Müügiarve kliendile määratud kanaliga Finbite PANK saatmise täiendused (saadetakse serviceId-na kont.arvelt makse viitenr. ning channelId-na maksja kliendikaardilt eelistatud pangakonto IBAN)
- E-arve standardi kohased parendused (et tühjasid tage veelgi paremini vältida)
- FitekIn-is määratud konteerimiskuupäeva haldus ostuarve loomisel
- Peale PRKonto/Kauba koodi muutmist kirjelduste ja dimensioonide mittekadumine nüüd ka ostu-kreeditarvetel
- UX täiendused (dok.saatmise staatused on nüüd jälle värvilised, PRKontode loendis on nüüd saatmise linnuke jms)  
<br>

##### Versioon 17.3.21215.0
- Operaatorite kaubamärgi muudatused (Omniva -> Finbite ja Fitek -> Unifiedpost)
- Võimalus säilitada ostuarve rea kirjeldus ning ühiku hind peale PRkonto (või kaubakoodi) muutmist
- Võimalus säilitada ostuarve rea dimensioonid peale PRkonto (või kaubakoodi) muutmist (st kasutada e-arvega kaasa tulnud dimensioone ehk mitte kasutada PR Konto või kauba vaikedimensioone)
- Dimensioonina ei käsitleta enam FitekIn-is määratud kommentaari tagi "Description"
- Ostuarve loomisel ei tekita enam tõrget liiga pikk info väljadel Telefon, Faks, Meiliaadress
- Arve väljastaja postiaadressit ei lisata müügiarve XML-i, kui vastav sisu puudub
- Müügiarve XML-i lisatakse nüüd arve väljastanud ettevõtte meiliaadress ning URL (ettevõtte andmetest)
- Väiksemad bugfixid ja täiendused  
<br>

##### Versioon 17.3.21140.0
- Allahindluse arvestamine ostuarvel on tehtud seadistusega aktiveeritavaks
- FitekIn-is määratud KM koodi arvestamine
- Liiga pika mõõtühiku bugfix
- Kreeditarve luuakse nüüd ka siis, kui tüüp DEB aga arve kogusumma negatiivne  
