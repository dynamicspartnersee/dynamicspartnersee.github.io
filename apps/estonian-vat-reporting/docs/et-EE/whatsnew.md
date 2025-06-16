---
---
##### Versioon 22.1.25105.0 _(saadaval al. 15.04.2025)_
- Täiendatud vorm KMD 2025 aasta lahendust _(sh KMD XML faili loogika al. 01.07.2025 vastavalt maksuameti avaldatud juhistele)_.
  - Tabelisse "KMD vormi read" lisatud lahter nr. 1 ²', '22% määraga (al. 01.07.25) maksustatavad toimingud ja tehingud'
    - _(Märkuseks, et tuli kasutada ametliku 1² asemel lahtri numbrit 1 ², kuna vormil on juba rida numbriga 12 ning teatud juhtudel SQL tasemel oleks 1² olnud võrdne numbriga 12, põhjustades tõrkeid.)_
- Täiendatud KMD müügiread INF-A täitmist nii, et eraldi read tekivad nii erisuse 01, kui ka erisuse 02 puhul ning järgitakse maksuameti ettenähtud kontrolle.  

##### Versioon 22.1.25025.0 _(saadaval al. 25.01.2025)_
- Täiendatud vorm KMD 2025 aasta lahendust _(sh lisatud eeldatav KMD XML faili loogika al. 01.07.2025)_.
- Väiksemad kasutusmugavuse täiendused.  

##### Versioon 22.1.24324.0 _(saadaval al. 20.11.2024)_
- Lisatud tugi KMD 2025 aasta vormile (sh KMD XML fail).
  - sh tabelisse "KMD vormi read" lisatud lahter nr. 2² (13% määraga (al. 01.01.2025) maksustatavad toimingud ja tehingud), mida läheb vaja majutusettevõtetel.
- Lisatud võimalus välistada INF-A ja/või INF-B lisast tühistatud müügi- ja/või ostuarved.
  - KM aruande seadistuses saab teha vastava(d) määrangu(d).
- Täiendatud tehingute piirmäära ületamise arvutamise loogikat selliselt, et tulemus oleks ootuspärane ka mittemahaarvatava käibemaksuga ostuarvete puhul.
- Lisatud kliendipõhise loogika võimaldamiseks INF-A ja INF-B ridade leidmise koodi eventid OnBeforeVatReportInfLineModifySalesTransactionTaxableAmount, OnBeforeVatReportInfLineModifySalesTransactionInvoiceAmount, OnBeforeVatReportInfLineModifyPurchTransaction.
- Väiksemad UX ja tehnilised täiendused.  

##### Versioon 22.1.24282.0 _(saadaval al. 08.10.2024)_
- Täiendatud KMD müügiread INF-A täitmist nii, et eraldi read tekivad ka erisuse 02 puhul
  - _(varem tekkis ainult erisus 01 puhul)_
- Lisatud event OnSetVatDeclNo, mille abil on võimalik lisada kliendipõhist loogikat Soovita INF read protsessile.  

##### Versioon 22.1.24143.0 _(saadaval al. 22.05.2024)_
- Tehnilised äpi upgrade koodi täiendused seoses "KMD vormi read" tabeli andmete uuendamisega.  

##### Versioon 22.1.24127.0 _(saadaval al. 07.05.2024)_
- Tehnilised täiendused
  - Lisatud KMD XML faili genereerivasse raportisse eventid OnBeforeAddSalesAnnex ja OnBeforeAddPurchaseAnnex, et saaks luua kliendipõhise loogikaga KMD INF-A ja INF-B failide sisu.  

##### Versioon 22.1.23352.1 _(saadaval al. 22.12.2023)_
- Lisatud tugi KMD 2024 aasta vormile (sh KMD XML fail).
  - Tabelisse "KMD vormi read" lisatud lahter nr. 1' (20% määraga (al. 01.01.2024) maksustatavad toimingud ja tehingud) ning nimetatud selguse mõttes ümber lahter nr. 1 (22% määraga (20% kuni 31.12.2023) maksustatavad toimingud ja tehingud)
    - _Lahtrit kahtjuks polnud võimalik nummerdada kui 1¹, sest SQL tasemel tõlgendati see võrdseks juba olemasoleva lahtriga 11._
  - Täiendatud XML-i genereerimise loogikat nii, et kui luuakse KM tagastus (KMD) 2024 aastast alates, siis kasutatakse lahtri nr. 1' 20% jaoks ning lahtri nr. 1 22% jaoks.
    - Vanema perioodi KMD puhul aga tähendab lahtri nr. 1 20%.
- Täiendatud KMD loomisel "Soovita ridu" funktsionaalsust nii, et INF-B rea väljale "KM summa" ei lisata nn Impordi käibemaksu KM kannet (eeldusel, et rea KM arvestusviisiks on "Täielik käibemaks" ning "KM konteerimise seadistus" tabelis on vastav rida märkega "KMD INF-il ei deklareerita".
  - Muudatus tehtud lähtuvalt Maksuameti selgitusest "Tollimaaklerilt saadud arvelt vormi KMD lisal INF osas B lahtris 6 näidatakse koguarve summa ja lahtris 8 ainult tollimaakleri oma teenuste eest kajastataud sisendkäibemaks".
- Mõned vähetähtsamad bugiparandused.  

##### Versioon 22.1.23262.0
- Lisatud tugi KM kuupäeva kasutamisele KMD loomisel.
  - KM aruande seadistus lehel on võimalik valida, kas KMD loomisel "Soovita ridu" võtab aluseks KM kannetes oleva KM kuupäeva või konteerimiskuupäeva.
    - Valik on võimalik ainult juhul, kui Pearaamatu seadistuses pole KM kuupäeva kasutamine keelatud.
  - INF ridade lehele lisatud väljad KM kuupäev ja konteerimiskuupäev (vaikimisi peidus).
- Väiksemad UX täiendused.
- Värskendatud äpi logo.  

##### Versioon 22.1.23120.0
- Lisatud loogika võtmaks kasutusele BC22.1 standardisse lisandunud mittemahaarvatava KM lahenduse funktsionaalsuse Eesti lokalisatsiooni mittemahaarvatava KM funktsionaalsuse asemel.
  - Esmalt tuleb deaktiveerida Eesti lokalisatsiooni vastav funktsionaalsus, eemaldades "KM konteerimise seadistus" lehelt kõik "Luba mittemahaarvatav KM" linnukesed.
  - Seejärel saab standardi mittemahaarvatava käibemaksu lahenduse aktiveerida lehel "KM Seadistus". 
- Eemaldatud sõltuvuslik Äriregistri äpi seos, võttes kasutusele kliendi ja hankija registrisse BC19.5 versioonis lisandunud standard Registreerimisnr. välja.
- Tehnilised täiendused tulenevalt värskeimale baasversioonile üleminekust.  

##### Versioon 16.0.25105.0
- Täiendatud vorm KMD 2025 aasta lahendust _(sh KMD XML faili loogika al. 01.07.2025 vastavalt maksuameti avaldatud juhistele)_.
  - Tabelisse "KMD vormi read" lisatud lahter nr. 1 ²', '22% määraga (al. 01.07.25) maksustatavad toimingud ja tehingud'
    - _(Märkuseks, et tuli kasutada ametliku 1² asemel lahtri numbrit 1 ², kuna vormil on juba rida numbriga 12 ning teatud juhtudel SQL tasemel oleks 1² olnud võrdne numbriga 12, põhjustades tõrkeid.)_  

##### Versioon 16.0.23352.1
- Lisatud tugi KMD 2024 aasta vormile (sh KMD XML fail).
- Täiendatud KMD loomisel "Soovita ridu" funktsionaalsust nii, et INF-B rea väljale "KM summa" ei lisata nn Impordi käibemaksu KM kannet (eeldusel, et rea KM arvestusviisiks on "Täielik käibemaks" ning "KM konteerimise seadistus" tabelis on vastav rida märkega "KMD INF-il ei deklareerita".  

##### Versioon 16.0.23081.0
- Parandatud olukord, kus kasutades ostuarvel korraga mittemahaarvatavat käibemaksu ja periodiseerimist ning saates arve kinnitusringile, kuvati kinnitajale konteeringu eelvaates valede summadega kanded.

##### Versioon 16.0.23037.0
- Lisatud loogika, et KMD nn põhiosa XML faili tulevad tag-id ainult siis, kui seal on väärtus _(vältimaks olukorda, kus raamatupidaja maksuametis igaks-juhuks neid nulle igakuiselt kustutamas käis)._
- Tehniline täiendus (lisatud event OnBeforeUpdateamountswithNDV protseduuri OnBeforePostGenJnlLine).
  
##### Versioon 16.0.22244.0
- Parandatud olukord, kus peažurnaalist käsitsi muudetud KM summat (nn KM erinevust) ei võetud mittemahaarvatava KM arvutamisel arvesse.

##### Versioon 16.0.22225.0
- KMD INF-A peal on võimalik kasutada välise dokumendi numbrit müügiarve numbri asemel.
  
##### Versioon 16.0.22179.0
- Lisandus 5% käibemaksu tugi
  - KM väljavõtted (KMD seadistus) tabeli väljale "Lahtri nr." saab nüüd sisestada väärtuse 2¹, mis tähistab 5% KM puhul KMD vormi rea numbrit).
  - KMD XML faili loomisel lisatud loogika, et kui KMD luuakse aasta 2022 kuu 8 või hilisem perioodi kohta, siis lisatakse XML faili tag "transactions5".
  
##### Versioon 16.0.21320.2
- Lahendus ühilduvaks BC20-ga.
  
##### Versioon 16.0.21320.1
- Parandatud olukord, kus väga paljude (sajad tuhanded) KM kannete korral tekkis KMD loomise protsessi "Soovita ridu..." käigus viga "Arithmetic operation resulted in an overflow".
  
##### Versioon 16.0.21320.0
- Parandatud olukord, kus ei õnnestunud kasutada üle 10 märgiseid väärtusi väljadel "KM äri konteeringurühm" ning "KM toote konteeringurühm".
  
##### Versioon 16.0.21132.0
- Parandatud CONSISTENT viga, kui ostuarvel oli kombinatsioon PV + Mittemahaarvatav KM + Pöörd KM.
  
##### Versioon 16.0.21113.0
- parandatud olukord ostuarvel, kus mittemahaarvatava KM + periodiseerimise + arve kinnitamisele saatmise kombinatsiooni puhul muutus periodiseerimise graafik peale kinnituse saamist.
