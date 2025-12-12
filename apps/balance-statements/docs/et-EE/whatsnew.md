---
---
##### Versioon 24.0.25345.0 _(saadaval al. 12.12.2025)_
- Lisatud võimalus väljastada saldoteatiseid viitenumbrite lõikes.
  - Vajalik nt. juhul kui erinevate teenuste lõikes on klientide/hankijate arvetel erinevad viitenumbrid.
  - Saldoteatise loomise valikutes, "Kuva rohkem" all, on võimalik sisse lülitada "**Viitenumbrite lõikes**".
    - _Saldoteatised luuakse sellisel juhul viitenumbrite lõikes ning viitenumbrid kuvatakse saldoteatise väljatrükil._
  - Isikupärastamisega on võimalik saldoteatiste loendis (ja Factboxis) välja tuua veerg "Makse viitenr.", et saada viitenumbri põhist ülevaadet loodud saldoteatistest ka loendis.
- Lisatud võimalus väljastada saldoteatiseid ühes infoga teatud perioodi käibest.
  - Vajalik nt. juhul kui audiitor soovib kliendi/hankija kinnitust teatud perioodi (nt aasta esimesed 9 kuud) käibele.
  - Saldoteatise loomise valikutes, "Kuva rohkem" all, on võimalik määrata "**Lisa käive perioodis**" väljale kuupäeva periood (nt kujul 01.01..30.09).
    - _Saldoteatistele lisatakse sellisel juhul eraldi "Käibe" blokk, kus on toodud valuutade lõikes info käivete osas vastavalt siestatud kuupäeva perioodile._
      - _Kui valitakse "Prindi KV-s" (valuutas tehingute puhul nt võiks seda valida), siis lisatakse veel juurde veerud "Summa (KV)" ja "Summa KM-ga (KV), kuvamaks perioodi käivet kohalikus valuutas._
    - _Juhul kui kasutatakse saldoteatise tagasiside osaga kujundust, siis lisatakse rida, kuhu saldoteatise saaja saab kirjutada vastava perioodi käibe summa._
  - Kui kasutatakse määrangut "Viitenumbrite lõikes", siis käibed tulevad samuti vastavate viitenumbrite lõikes.
- Väiksemad tehnilised täiendused (koodi mõningane optimeerimine ja moderniseerimine).  

##### Versioon 24.0.25254.0 _(saadaval al. 12.09.2025)_
- Tehnilised täiendused, et lahendus oleks **BC27** _(2025 wave 2)_ **ühilduv**.  

##### Versioon 20.0.24318.0
- Lisatud "**PV Saldo**" aruande andmestikku Soetuse kuupäev (AcquisitionDate) ning vastav pealdis (AcquisitionDateLbl). Lisaks likvideerimiskuupäeva pealdis (DisposalDateLbl).
- Muudetud "PV Saldo" aruande osad muutujad kättesaadavaks kliendipõhiste laiendustega
- Parandatud olukord, mis tekkis versiooniga 20.0.24268.0, kus ei loodud saldoteatist kliendile/hankijale, kuigi saldo kuupäeval ei olnud saldo nullis _(põhjuseks oli see, et loomise kuupäeval puudusid avatud kanded)_.  

##### Versioon 20.0.24268.0
- Lisatud nii kliendi- kui hankija saldoteatiste loomisel võimalus määrata "**Loo teatis ka null saldo puhul**", mis loob saldoteatise ka juhul, kui saldo kuupäeval puuduvad avatud andmikukanded
  - _Seni loodi saldoteatis null saldo korral ainult siis, kui olid avatud andmikukanded_
- Lisatud AL õiguste komplekt SBS - OBJECTS (Saldoteatised - Koodiobjektid)
- Väiksemad UX täiendused  

##### Versioon 20.0.24071.1
- Täiendatud "**PV Saldo**" aruannet, et oleks võimalik grupeerida aruannet nii Vastutav töötaja kui Vastutav töötaja (palk)
- Väiksemad tehnilised täiendused "PV Saldo" aruandes, võimaldamaks kliendipõhiseid erisusi  

##### Versioon 20.0.23348.0
- Tehnilised täiendused, et lahenduses oleks **võimalik kasutada mitut alternatiivset väljatrükki** samale  raportile (alates BC20)
- Lisatud alternatiivsed saldoteatiste kujundused, kus on kuvatud saldoteatise number ning all osas käsitsi täidetav saldoteatise tagasiside sektsioon, mida kasutaja saab valida läbi "Aruande kujunduse valik" lehe:
  - "**Kliendi saldoteatis tagasiside osaga**"
  - "**Hankija saldoteatis tagasiside osaga**"  

##### Versioon 19.3.23251.0
- Tehnilised täiendused, et lahendus oleks **BC23 versiooniga ühilduv**
- Parandatud olukord, kus saldoteatise väljatrükile tekkis punane rist, kui ettevõttel polnud pilti (logo)
- Värskendatud äpi logo vastamaks muutunud Microsoft AppSource tingimustele  

##### Versioon 18.0.23152.0
- Lisandus aruandesse **PV Saldo** uus rühmitusalus "Peavara"  

##### Versioon 18.0.22365.1
- Bugiparandused:
  - Factboxis manuste lisamine ei õnnestunud BC20 või uuemates versioonides
  - Kohandatud saldoteatiste tekstide kaartide vahel liikudes ei muutunud tekstid  

##### Versioon 18.0.22365.0
- Kliendi- ja hankija **saldoteatiste tekste on nüüd võimalik lihtsasti kohandada** läbi Saldoteatiste seadistus lehe
  - Kohandada saab nii eesti-, kui inglisekeelseid tekste  

##### Versioon 18.0.22355.0
- Kliendi- ja hankija teatiste loomisel on nüüd võimalik valida, kas kaasata kannete loetelu, millest saldo moodustub, või mitte
- Kliendi teatiste loomisel on nüüd võimalik valida, kas kasutada **välise dokumendi numbrit arve numbri asemel**  

##### Versioon 18.0.22124.1
- **PV Saldo** aruandes saab nüüd valida, kas aruandesse kaasatakse likvideeritud põhivarad või mitte

##### Versioon 18.0.22005.0
- Mittefunktsionaalsed tehnilised täiendused

##### Versioon 18.0.212331.0
- **Saadetud saldoteatised** on nüüd **leitavad ka kliendi/hankija registrist**, Saadetud meilisõnumid lehelt
- Parandatud bugi, mille tõttu muutus meilisõnumi redigeerimise aknas väljasaatmise meilikonto vaike meilikontoks
- PV Saldo aruande kasutusmugavuse täiendused

##### Versioon 17.1.21327.0
- **Saldoteatiseid saab** nüüd **saata** täiendatud meilivõimaluste (**meilistsenaarium Saldoteatis**) **funktsionaalsusega**
- Lisandus võimalus enne saatmist meilisõnumit redigeerida
- Lisatud Saldo kuupäev veerg saldoteatiste loendisse
- **Lisatud aruanne PV Saldo põhivara loendisse**

##### Versioon 15.3.21243.0
- Saldoteatised luuakse nüüd hoolimata meiliaadressi puudumisest kliendi/hankija kaardil
- Saldoteatiste loetelus on võimalik puuduv aadress lisada (või muuta) ning järgmiseks korraks kliendi/hankija kaardile salvestada
- Teatiste loomise parameetrid nüüdsest salvestuvad
- Saldoteatiste kujundust on täiendatud -sh lisatud infot juurde ning parandatud visuaali
- Palju kasutusmugavuse täiendusi (sh selgemad väljade nimetused, kohtspikrid, manuse faili parem nimetus jne)

##### Versioon 15.3.21148.0
- Täiendatud Kliendi ning Hankija saldoteatise väljatrüki andmestikku nii Kliendi/Hankija, kui Ettevõtte andmete osas:
  - lisandus iga alustabeli osas ca 10-15 välja, mida saab kohandatud kujundusel täiendavalt nüüd kasutada.
