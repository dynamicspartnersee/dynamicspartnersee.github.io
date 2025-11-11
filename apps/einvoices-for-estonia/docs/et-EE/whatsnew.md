---
---
##### Versioon 26.0.25307.0 _(saadaval al. 04.11.2025)_
- Täiendatud loodava arve XML-i koostamise loogikat nii, et kui maksja-kliendi kaardil on KM registreerimise nr. täidetud, siis lisatakse e-arvele BuyerParty blokki tag VATRegNumber.
  - _Muudatus hõlmab nii arvet, kui kreeditarvet (sh hoolduse arve ja kreeditarve)._
- Lisatud võimalus tagantjärgi küsida e-ostuarvele uuesti manust Finbite-st.
  - Ostuarvelt tuleb avada vastav Sissetulev dokument ning kasutada toimingut "Võta Finbite manus(ed)".
    - _Vajalik kasutada juhul, kui mingil põhjusel pole PDF manus e-ostuarvega koos BC-sse jõudnud._
- Täiendatud Makse saaja hankija pangakonto leidmist ostuarvele olukorras, kus e-arvel olev pangakonto sisaldas tühikuid või sidekriipse.   

##### Versioon 26.0.25272.0 _(saadaval al. 30.09.2025)_
- Lisatud võimalus saata operaatori Finbite kaudu e-müügiarvet nii, et PDF väljatrükki ei lisata.
  - Dokumendi saatmise profiilile, kui valitud "Eesti e-arve operaator" väärtuseks "Finbite dok.vahetusteenuse kaudu", ilmub nähtavale uus väli "Ära lisa PDF-i e-arvele".
  - _Vajalik juhul, kui Finbite ise lisab XML andmete alusel PDF kujunduse ning edastab selle kliendile._
- Täiendatud ostuarve loomisel e-arvelt kaupade tuvastamise loogikat, vältimaks eksliku kauba tuvastamist, kui kaupade numbrid BC-s kattuvad hankija kauba numbriga.
  - Hankija kaardil, kui määratud "Dokumendi rea loomise loogika" väärtuseks "Tuvasta kaubad", siis ilmub nähtavale uus väli "Kauba nr. võib olla SellerProductId".
  - _Seda on vaja sisse lülitada juhul, kui hankija kaubakoode kasutatakse BC-s kaubakoodidena._  

##### Versioon 26.0.25259.0 _(saadaval al. 17.09.2025)_
- Täiendatud ostuarvete pärimist Finbite -st nii, et juhul kui tulemas on nii palju ostuarveid (Finbite praeguse reegli kohaselt 30), siis kuna peab mitu korda neid pärima, siis nö korduva päringu vahel süsteem ootab 15 sekundit.
  - _Vajalik veaolukorra "Request rate too high Error 93" vältimiseks._
- Täiendatud ostuarve loomisel hankija pangakontode salvestamist:
  - _Juhul kui pangal oli pikk nimi (üle 20 tähemärgi), siis enam ei teki sellest tõrget hankija pangakonto lisamisel._
  - _Juhul kui pangal oli pika nimega pangas mitu kontot, siis enam ei teki ka nende lisamisel tõrget._  

##### Versioon 26.0.25252.0 _(saadaval al. 10.09.2025)_
- Täiendatud ostuarve loomisel hankija IBAN pangakonto salvestamist.
  - _XML-is olevast pangakontost eemaldatakse tühikud ning sidekriipsud._
- BC27 ühilduv (2025 wave 2).  

##### Versioon 21.5.25307.0 _(vt kirjeldust ülal versioonile 26.0.25307.0)_  

##### Versioon 21.5.25259.0 _(vt kirjeldust ülal versioonile 26.0.25259.0)_  

##### Versioon 21.5.25252.0 _(vt kirjeldust ülal versioonile 26.0.25252.0)_  

##### Versioon 21.5.25223.0 _(saadaval al. 12.08.2025)_
- Finbite päringute timeout suurendamine 180 sekundi peale, kuna Finbite tõstis ERP SOAP liideses vastuse ehk response andmise ajalise vahemiku selliseks.  

##### Versioon 21.5.25127.1 _(saadaval al. 08.05.2025)_
- Täiendatud ostudokumendi loomise veahaldust.
  - Ebastandardses olukorras, kui e-arvel oli InvoiceSumGroup sektsioonis mitu sama VATRate väärtusega VAT blokki tekkis sissetulevast dokumendist ostudokumendi loomisel veateade "Sama võtmega üksus on juba lisatud".  

##### Versioon 21.5.25064.0 _(saadaval al. 05.03.2025)_
- Kasutusmugavuse täiendused:
  - Ostuarve reale e-arvelt kauba mõõtühiku kirjutamisel kontrollitakse, kas kauba mõõtühikutes on vastav mõõtühik olemas ning kui mitte, siis kuvatakse kasutajale vastavasisuline veateade ühes viitega probleemsele kaubale.
  - Kaubaga ostuarve rele, kus puudub mõõtühik, saab nüüd määrata kauba mõõtühiku nii, et rea finantsandmed (hind, kogus) jäävad alles.  

##### Versioon 21.5.25027.0 _(saadaval al. 27.01.2025)_
- Lisatud võimalus Finbite (Omniva) dokumendivahetusteenuse seadistus lehel määrata põhiandmete Finbite Arvekeskusesse saatmise töötlemist:
  - Ära asenda PR kontosid
  - Ära asenda dimensioone
  - Ära asenda hankijaid ja kliente
- Parandatud uue hankija ostuarve loomisel tekkinud veaolukord, mis avaldus kui süsteem otsis vastavat hankijat KM reg. koodi alusel ning e-arve XML-is oli tühi tag VATRegNumber.  

##### Versioon 21.5.25007.0 _(saadaval al. 07.01.2025)_
- Täiendatud ostuarve rea loomisel PR konto leidmist "Vastenda tekst kontoks" funktsionaalsusega.
  - nüüd süsteem esmalt otsib vastava hankija numbriga vastenda tekst kontoks määranguid (_eeldab täpset vastendamise teksti st ilma tärnideta_) ning seejärel hankija numbrita määrangute hulgast (_nagu seni sh tärnidega vastendamise teksti otsing_).
  - enam ei teki tõrget _"Filtri tõlgendamisel ilmnes tõrge: ei oodatud üksust „(“."_, kui vastenda tekst kontoks vastendamise tekstis on kasutatud sulgusid vms süsteemseid sümboleid.  

##### Versioon 21.5.25003.0 _(saadaval al. 03.01.2025)_
- Suurendatud kaupade loomise ning tuvastamise tõrkekindlust:
  - Täiendatud uute kaupade loomise loogikat nii, et kui e-arvel on kaubal mõõtühik, mida BC mõõtühikute tabelis ei ole, siis ostuarve loomisel ei teki enam tõrget vaid ostuarve luuakse ära, kusjuures vastava kaubaga rida jääb ilma mõõtühikuta ning sissetuleva dokumendi peale kuvatakse vastavasisuline teade.
  - Täiendatud kaupade tuvastamist nii, et kaup määratakse ostuarve reale ka siis, kui kauba viidetest leitakse sama EAN koodi või Hankija kauba koodi rohkem, kui ühel korral.
- Täiendatud e-arve XML faili lisatava PDF kujunduse leidmise loogikat selliselt, mis järgib BC standard kujunduse leidmise loogikat.
  - st nüüd süsteem esmalt vaatab Kliendi kaardi kaudu Dokumendi kujunduse määrangut ning alles seejärel üldist Aruandevalikud - Müük määrangut ehk e-arve XML faili lisatava PDF-i kujundus tuleb nüüd sama, mis BC-s arve printimisel.
- Lahendusesisesed tehnilised täiendused (_lisatud koodisisesed õigused võimalike kasutajaõiguste probleemide ennetamiseks_).  

##### Versioon 21.5.24323.0 _(saadaval al. 18.11.2024)_
- Parandatud regionaalformaadi probleem, mis avaldus sissetulevast dokumendist ostuarve loomisel ja mille tõttu ei tekkinud korrektsed komakohad ühiku hinnale.
- Lisatud event OnBeforeFindVendor() võimaldamaks kliendipõhise loogika lisamist hankija leidmisel/lisamisel.  

##### Versioon 21.5.24277.0 _(saadaval al. 03.10.2024)_
- Kui arvele on valitud ettevõtte pangakonto info, siis see kajastub nüüd ka e-arvel _(sektsioonis/tag-is SellerParty/AccountInfo ning PaymentInfo/PayToAccount)._
  - Kui on määramata, siis (nagu seni) võetakse pangakonto info ettevõtte andmed tabelist.
- Kui e-arve on valitul liikuma Finbite kaudu kliendi internetipanka, siis nüüd lisatakse ka kreeditarvele kliendi pangakonto nr. _(channelAddress parameetrina nagu müügiarvete puhul)._
  - _Seni oli see lisatud ainult müügiarvete puhul, eeldades et kreeditarvet polegi vaja internetipanka saata_
- Lahendusesisesed tehnilised täiendused.  

##### Versioon 21.5.24239.0 _(saadaval al. 26.08.2024)_
- Tehnilised täiendused
  - _Lisatud Finbite koodiblokki eventid, et saaks luua kliendipõhise arenduse, mille kaudu saata e-arvetena konteerimata arveid._  

##### Versioon 21.5.24187.0
- Lisandus võimalus luua automaatselt e-arve alusel kaupasid.
  - Hankija kaardil saab määrata kauba malli "Loo uus kaup malliga" väljale ning kui kaupa ei leita, siis luuakse uus kaup vastava kauba malli ning e-arves oleva info (_Kirjeldus, Mõõtühik, EAN, Hankija kood_) alusel.
    - "Loo uus kaup malliga" saab määrata ainult siis, kui "Dokumendi rea loomise loogika" valikuks on "Tuvasta kaubad".
    - "Loo uus kaup malliga" määrangu saab lisada ka hankija mallile.
- Parandatud ostudokumendi loomisel tekkinud veaolukord, kui hankija kaardil oli valitud “Koonda KM ja arveridade grupi id lõikes” ning e-arve XML-is sisaldusid tühikud grupi id-s.  

##### Versioon 21.5.24161.0
- Lisandus võimalus hankijapõhiselt (Hankija kaardil) määrata, kas e-arvelt loetakse hankija arvelduskontod sisse automaatselt, peale kasutaja kinnitust või üldse mitte.
- Lisandus võimalus ostuarvel määrata, millisele makse saaja hankija pangakontole peaks arve eest makse (ülekanne) minema.
  - Vaikimisi väärtust saab seadistata hankijapõhiselt (Hankija kaardil).
  - Ostuarvel määratud Saaja pangakonto jõuab hankijaandmiku kandele
    - NB! Selleks, et määrang sealt edasi Maksežurnaali kanduks _(Soovita makseid hankijale toiminguga)_, tuleb kontrollida, et kasutatakse Eesti Pangaformaatide äpist vähemalt versiooni 21.5.24161.0
- Hankija malli lehele lisatud hankija kaardil olevad eesti e-arvete lahenduste väljad.
- Väiksemad UX täiendused.  

##### Versioon 21.5.24149.0
- Lisandus võimalus hankijapõhiselt (Hankija kaardil) määrata "Dokumendi rea loomise loogika":
  - Vaikimisi - st. kõik read nii nagu nad e-arvel on
  - Tuvasta kaubad - st. e-arve rida lisatakse ostudokumendi reale liigiga kaup (kui kaup tuvastati)
  - Koonda KM lõikes - st. e-arve read koondatakse XML-is sisalduva VATRate tag-i alusel _(nt 100 reaga telefoniarve puhul jääb järgi ainult 2 rida: 22% ja 0%)_
  - Koonda KM ja arveridade grupi id lõikes - st. kui hankija on saatnud e-arve, kus ridadel küljes grupeerimise tunnus groupId, siis grupeeritakse read vastava tunnuse alusel _(nt telefoniarve puhul iga telefoninumbri ja KM määra kohta üks rida)_
  - Koonda KM ja toote/teenuse kirjelduse lõikes - st. e-arve read lisatakse ostudokumendi reale grupeerituna e-arve kirjelduste järgi _(nt telefoniarve puhul kõik SMS-id ühel real ja kuutasud teisel real jne)_
- Seoses tuvasta kaubad funktsionaalsuse hankijapõhiseks muutumisega, teisaldus ka "Kasuta kauba ostu mõõtühikut" hankijapõhiseks seadistuseks _(kuna määratav ainult siis, kui "Tuvasta kaubad" valik aktiveeritud)_.  

##### Versioon 21.5.24110.1
- Lisandus võimalus aktiveerida "Ostude ja ostuv. seadistus" lehel määrang "Kasuta kauba ostu mõõtühikut", mis määrab, kas e-arvest loodud ostudokumendil kasutatakse kauba kaardil määratud ostu mõõtühikut, e-arvel oleva mõõtühiku asemel.  

##### Versioon 21.5.24085.0
- Lisatud Ostude ja ostuv. seadistusse määrang "Kontrolli duplikaat dokumenti".
  - Kui valik aktiveeritakse, siis sissetulevast dokumentist ostudokumendi loomisel tehakse duplikaat dokumendi kontroll (avastamaks juba olemasolevat dokumenti nii konteeritud kui konteerimata ostudokumentide hulgast).
    - _Mõistlik kasutada juhul, kui duplikaat dokument kipub selguma alles konteerimisel (peale kinnitusringide jms läbimist)_
- Lisatud Ostude ja ostuv. seadistusse määrang "Ära otsi e-arvelt KM koodi"
  - Määrab kas süsteem peaks vältima e-arvel sisalduva KM toote konteeringurühma kasutamist. Määrangu võiks aktiveerida, kui eelnevalt e-arvet arvehalduskeskkonnas ei töödelda.
- Parandatud ostudokumendi loomisel tekkinud veaolukord, mille põhjustas liialt pikk mõõtühiku nimetus e-arves  
<br>

##### Versioon 21.5.24053.0
- Lisatud Ostude ja ostuv. seadistus lehele valik "Leia Makse saaja hankija PayToName alusel", mille abil saab määrata kas ja mis tingimustel leitakse e-ostuarvele Makse saaja hankija kasutades e-arve tag-i PayToName.
  _- Vajalik kasutada juhul kui samale hankija võib erinevate arvete maksmist soovida erinevatele makse saaja hankijatele, kuid hankija kaardile saab teadupärast valida vaid ühe._  
<br>

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
