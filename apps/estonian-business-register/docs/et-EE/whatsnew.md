---
---
##### Versioon 22.1.26128.0 _(saadaval al. 08.05.2026)_
- Lisatud äriregistri päringu lehele väli Staatus, mis kuvab tekstina päritud ettevõtte hetke staatust äriregistris (Registrisse kantud, Likvideerimisel, Pankrotis).
- Lisatud äriregistri päringu lehele kliendipõhise loogika lisamiseks eventid OnAfterSetCustomer, OnAfterGetCustomer, OnAfterSetVendor, OnAfterGetVendor, OnAfterSetContact, OnAfterGetContact.
- Loendis nn mass äriregistri päringuga kliendi/hankija andmeid uuendades, täidetakse nüüd registreerimisnumbri väli ühes valideerimisega.
- Täiendatud koodisisest õiguste haldust objektide vahel.  

##### Versioon 22.1.23234.0 _(saadaval al. 25.09.2023)_
- Lisatud äriregistri päringu lehe koodi eventid _(OnBeforeGetCustomer, OnBeforeGetVendor, OnBeforeGetContact)_, et oleks kliendipõhise arendusega võimalik vastavates protseduurides kasutada kliendipõhist loogikat.
- Värskendatud äpi logo.  


##### Versioon 22.1.23136.0 _(saadaval al. 17.05.2023)_
- Üleminek kontaktide registris standard Registreerimisnr. väljale (_tuli BC22.1 versioonis_).
  - Analoogselt kliendi ja hankija registrile jääb ka kontaktide tabelis senine Registreerimisnr. väli taustal esialgu alles ning täitub paralleelselt standard Registreerimisnr. välja täitumisega.  


##### Versioon 21.5.23074.0 _(saadaval al. 15.03.2023)_
- Üleminek kliendi ja hankija registris standard Registreerimisnr. väljale (_tuli BC21.5 versioonis_).
  - Lahenduse senine Registreerimisnr. väli jääb taustal esialgu alles ning täitub paralleelselt standard Registreerimisnr. välja täitumisega.
    - Lahenduse värskendamisel käesolevale versioonile täidetakse standard Registreerimisnr. väli nii kliendite kui hankijate puhul senise Registreerimisnr. välja väärtusega.
    - _Senist Registreerimisnr. välja hoitakse alles vähemalt kuni BC24 versioonini ilmumiseni (aprill 2024.a.) selleks, et väljaga seotud arendused jõuaksid samuti üle minna standard Registreerimisnr. väljale._
- Parandatud olukord, kus klient/hankija, mis seotud läbi kontakti hankija/kliendiga Registreerimisnr. välja muutmisel ei muutunud seotud registris välja väärtus.
- Lahenduse tehnlilised täiendused tulenevalt BC alusversiooni suurenemisest.  


##### Versioon 15.3.22064.0 _(saadaval al. 05.03.2022)_
- Mittefunktsionaalsed tehnilised täiendused.  


##### Versioon 15.3.21362.0 _(saadaval al. 28.12.2021)_
- Päring tehakse nüüd eelistades äriregistri koodi _(kui kood puudub või ei vasta nõuetele, siis päring endiselt nime alusel)_.
- Nime alusel päringu algatamine korjab nüüd ära enamlevinud õigusliku vormi ees- ning järelliited _(sh nt Korteriühistu)_.
- Täiendatud masspäringu aruande andmestikku _(lisatud nime võrdlus nähtavalt aruandele ning aadressiinfo taustal)_.
- Parandatud olukord, mis avaldus BC19 versioonis ning mille tõttu ei õnnestunud kliendi/hankija kaardil muuta äriregistri koodi.
- Parandatud olukord, mille tõttu ei salvestunud äriregistri kood hankija kaardilt päringut tehes.
- UX täiendused.  


##### Versioon 15.3.21168.0 _(saadaval al. 17.06.2021)_
- Linnaosa salvestamine linna väljale tehtud seadistatavaks.
- Linna/Valla + linnaosa/küla mittemahtumisel salvestatakse ainult Linn/Vald.  


##### Versioon 15.3.21103.1 _(saadaval al. 08.06.2021)_
- Inglise keele puudumise bugfix.  


##### Versioon 15.3.21103.0 _(saadaval al. 13.04.2021)_
- parandatud olukord, kus Dok.saatmise profiil ei jõudnud mestimise lehelt Kliendi kaardile
- parendatud lahendust, et välja Registreerimisnr. manuaalsel uuendamisel jõuaks info kenasti seotud registritesse (Klient-Kontakt-Hankija)
