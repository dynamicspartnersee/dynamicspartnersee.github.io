---
---
##### Peatselt lisandumas _(kohe kui Unifiedpost oma ühenduse FitekIn keskkonda korda saab)_
- _Hankijate saatmine läbi Unifiedpost-i liidese FitekIn keskkonda_
<br>

##### Versioon 17.3.21364.2
- Põhiandmete (kontod ja dimensioonid) saatmine läbi Unifiedpost-i liidese FitekIn keskkonda

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
