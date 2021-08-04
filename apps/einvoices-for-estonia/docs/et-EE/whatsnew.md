---
---
##### Versioon 17.3.21215.0.
- Operaatorite kaubamärgi muudatused (Omniva -> Finbite ja Fitek -> Unifiedpost)
- Võimalus säilitada ostuarve rea kirjeldus ning ühiku hind peale PRkonto (või kaubakoodi) muutmist
- Võimalus säilitada ostuarve rea dimensioonid peale PRkonto (või kaubakoodi) muutmist (st kasutada e-arvega kaasa tulnud dimensioone ehk mitte kasutada PR Konto või kauba vaikedimensioone)
- Dimensioonina ei käsitleta enam FitekIn-is määratud kommentaari tagi "Description"
- Ostuarve loomisel ei tekita enam tõrget liiga pikk info väljadel Telefon, Faks, Meiliaadress
- Arve väljastaja postiaadressit ei lisata müügiarve XML-i, kui vastav sisu puudub
- Müügiarve XML-i lisatakse nüüd arve väljastanud ettevõtte meiliaadress ning URL (ettevõtte andmetest)
- Väiksemad bugfixid ja täiendused


##### Versioon 17.3.21140.0
- Allahindluse arvestamine ostuarvel on tehtud seadistusega aktiveeritavaks
- FitekIn-is määratud KM koodi arvestamine
- Liiga pika mõõtühiku bugfix
- Kreeditarve luuakse nüüd ka siis, kui tüüp DEB aga arve kogusumma negatiivne
