---
---
##### Versioon 26.0.26116.0 _(saadaval al. 27.04.2026)_
- Viidud lahendus ühilduvaks BC28 versiooniga.
- Täiendatud müügi- ja ostu kreeditarve toimingu "Too kliendipõhine/hankijapõhine ettemaks" kasutajakogemust.
  - _Nupust on võimalik rida lisada ainult siis, kui ühtegi teist liiki rida arvel ei ole (kuna konteerimisel seda kontrollitakse)._
- Täiendatud ettemaksuarve konteerimise kontrolli nii, et enam ei õnnestu konteerida ettemaksuarvet, kui vastaval real on periodiseerimise tähis.
- Täiendatud ettemaksuarve konteerimisel kontrolli nii, et ei tuleks viga olukorras, kus mõnel arvereal on tühja Nr. määranguga rida.
- Koodisisesed funktsionaalsust mittemõjutavad tehnilised täiendused.  

##### Versioon 26.0.25255.0 _(saadaval al. 12.09.2025)_
- Viidud lahendus ühilduvaks BC27 versiooniga.
  - _Lahenduse uus versioon seetõttu nüüd sobilik vaid alates BC26 versioonile._
- Lisatud müügi kreeditarvele toiming "Too kliendipõhine ettemaks", et oleks võimalik mugavamalt luua kliendipõhisele ettemaksuarvele kreeditit.
- Lisatud ostu kreeditarvele toiming "Too hankijapõhine ettemaks", et oleks võimalik mugavamalt luua hankijapõhisele ettemaksuarvele kreeditit.  

##### Versioon 20.0.23335.0 _(saadaval al. 01.12.2023)_
- Lisatud tugi uuele laiendatavale arvesisestusmootorile.
- Lahendatud ettemaksu toomine pöördkäibemaksuga müügireale.  

##### Versioon 17.0.23268.0 _(saadaval al. 26.09.2023)_
- Lisatud eventid _(OnBeforeInsertPrepaymentEntry, OnBeforeSetPrepaymentEntryFilter, OnBeforePrepaymentEntryFindFirst, OnBeforeSetPrice, OnBeforeSalesLineInsert, OnApplyPrepaymentEntries)_, et oleks kliendipõhise arendusega võimalik täiendada ettemaksude käsitlemise ja haldamise loogikat.  

##### Versioon 17.0.23262.0 _(saadaval al. 19.09.2023)_
- Värskendatud äpi logo.  

##### Versioon 17.0.23158.0 _(saadaval al. 09.06.2023)_
- Parandatud olukord "Please chesk VAT base amounts", mis tekkis kliendipõhise ettemaksukande kasutamisel müügidokumendil, kus oli määratud "Hinnad koos KM-ga" ning dokumendil olid erineva KM %-ga read.  

##### Versioon 17.0.23146.0 _(saadaval al. 27.05.2023)_
- Täiendatud kliendipõhise ettemaksu toomist müügitellimusele/müügiarvele nii, et süsteem toob ka "Hinnad koos KM-ga" valiku korral dokumendi reale sellise ettemaksu summa, mis ei ületa arve kogusummat.
- Lisatud kontroll, et konteerimisel kontrollitakse, kas ettemaksu real kasutatud KM toote konteeringurühm vastab ettemaksuandmiku vastaval kandel olevale rühmale.
- Müügitellimuse ja müügirave ridade lehele lisatud vaikimisi peidus väli "Seotud ettemaksukande nr." (et kasutaja saaks vajadusel välja nähtavale tuua ning seeläbi leida rida, millele mõni veateade vihjab.
- Parandatud olukord, kus tekkis viga "Kutse funktsioonile LOCKTABLE pole .... TryFunction".
- Tehnilised täiendused.  

##### Versioon 15.3.22095.1 _(saadaval al. 05.04.2022)_
- Lisandus Hankijapõhine ettemaksude funktsionaalsus (aktiveeritav Ostude ja ostuv. seadistuses).
- Lisandus valuutas ettemaksude ümberhindlus.
- Parandatud olukord, kus "Hinnad koos KM-ga" aktiveerituse puhul tuli konteerimisel veateade "Välja Jääksumma väärtus ei tohi olla -0,01".
- Tehnilised täiendused ühildumaks värskete BC versioonidega.  
