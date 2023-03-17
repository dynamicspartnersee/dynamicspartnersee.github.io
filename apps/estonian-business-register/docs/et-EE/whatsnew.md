---
---

##### Versioon 21.5.23074.0
- Üleminek kliendi ja hankija registris standard Registreerimisnr. väljale (_tuli BC21.5 versioonis_)
  - Lahenduse senine Registreerimisnr. väli jääb taustal esialgu alles ning täitub paralleelselt standard Registreerimisnr. välja täitumisega
    - Lahenduse värskendamisel käesolevale versioonile täidetakse standard Registreerimisnr. väli nii kliendite kui hankijate puhul senise Registreerimisnr. välja väärtusega
    - _Senist Registreerimisnr. välja hoitakse alles vähemalt kuni BC24 versioonini ilmumiseni (aprill 2024.a.) selleks, et väljaga seotud arendused jõuaksid samuti üle minna standard Registreerimisnr. väljale_
- Parandatud olukord, kus klient/hankija, mis seotud läbi kontakti hankija/kliendiga Registreerimisnr. välja muutmisel ei muutunud seotud registris välja väärtus.
- Lahenduse tehnlilised täiendused tulenevalt BC alusversiooni suurenemisest  


##### Versioon 15.3.22064.0
- Mittefunktsionaalsed tehnilised täiendused


##### Versioon 15.3.21362.0
- Päring tehakse nüüd eelistades äriregistri koodi _(kui kood puudub või ei vasta nõuetele, siis päring endiselt nime alusel)_
- Nime alusel päringu algatamine korjab nüüd ära enamlevinud õigusliku vormi ees- ning järelliited _(sh nt Korteriühistu)_
- Täiendatud masspäringu aruande andmestikku _(lisatud nime võrdlus nähtavalt aruandele ning aadressiinfo taustal)_
- Parandatud olukord, mis avaldus BC19 versioonis ning mille tõttu ei õnnestunud kliendi/hankija kaardil muuta äriregistri koodi
- Parandatud olukord, mille tõttu ei salvestunud äriregistri kood hankija kaardilt päringut tehes
- UX täiendused  


##### Versioon 15.3.21168.0
- Linnaosa salvestamine linna väljale tehtud seadistatavaks
- Linna/Valla + linnaosa/küla mittemahtumisel salvestatakse ainult Linn/Vald  


##### Versioon 15.3.21103.1
- Inglise keele puudumise bugfix  


##### Versioon 15.3.21103.0
- parandatud olukord, kus Dok.saatmise profiil ei jõudnud mestimise lehelt Kliendi kaardile
- parendatud lahendust, et välja Registreerimisnr. manuaalsel uuendamisel jõuaks info kenasti seotud registritesse (Klient-Kontakt-Hankija)
