---
---
##### Versioon 17.0.23268.0
- Lisatud eventid _(OnBeforeInsertPrepaymentEntry, OnBeforeSetPrepaymentEntryFilter, OnBeforePrepaymentEntryFindFirst, OnBeforeSetPrice, OnBeforeSalesLineInsert, OnApplyPrepaymentEntries)_, et oleks kliendipõhise arendusega võimalik täiendada ettemaksude käsitlemise ja haldamise loogikat  

##### Versioon 17.0.23262.0
- Värskendatud äpi logo
  
##### Versioon 17.0.23158.0
- Parandatud olukord "Please chesk VAT base amounts", mis tekkis kliendipõhise ettemaksukande kasutamisel müügidokumendil, kus oli määratud "Hinnad koos KM-ga" ning dokumendil olid erineva KM %-ga read  

##### Versioon 17.0.23146.0
- Täiendatud kliendipõhise ettemaksu toomist müügitellimusele/müügiarvele nii, et süsteem toob ka "Hinnad koos KM-ga" valiku korral dokumendi reale sellise ettemaksu summa, mis ei ületa arve kogusummat
- Lisatud kontroll, et konteerimisel kontrollitakse, kas ettemaksu real kasutatud KM toote konteeringurühm vastab ettemaksuandmiku vastaval kandel olevale rühmale
- Müügitellimuse ja müügirave ridade lehele lisatud vaikimisi peidus väli "Seotud ettemaksukande nr." (et kasutaja saaks vajadusel välja nähtavale tuua ning seeläbi leida rida, millele mõni veateade vihjab
- Parandatud olukord, kus tekkis viga "Kutse funktsioonile LOCKTABLE pole .... TryFunction" 
- Tehnilised täiendused  

##### Versioon 15.3.22095.1
- Lisandus Hankijapõhine ettemaksude funktsionaalsus (aktiveeritav Ostude ja ostuv. seadistuses)
- Lisandus valuutas ettemaksude ümberhindlus
- Parandatud olukord, kus "Hinnad koos KM-ga" aktiveerituse puhul tuli konteerimisel veateade "Välja Jääksumma väärtus ei tohi olla -0,01"
- Tehnilised täiendused ühildumaks värskete BC versioonidega
