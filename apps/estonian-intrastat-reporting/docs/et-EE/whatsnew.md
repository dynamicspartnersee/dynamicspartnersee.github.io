---
---
##### Versioon 25.0.24280.2
- BC25 versiooniga ühilduv lahendus, mis täiendab uut Intrastat Core lahendust.
  - _Intrastat žurnaali asemel on nüüd Intrastat aruanded, kus saab luua **XML faili** statistikaametile esitamiseks._
  - Nomenklatuurinumbrites olnud Täiendava mõõtühiku tähised määratakse äpi uuendamise käigus automaatselt vastavatele kaupadele _(al BC25 on määrang Kauba kaardil)_.
  - Lahendusesisesed tehnilised täiendused.   

##### Versioon 17.2.21356.4
- Mittefunktsionaalsed tehnilised täiendused.  

##### Versioon 17.2.21356.3
- XML-i loomisel arvestab lahendus 2022 aastast kehtima hakkavad nõudeid (eemaldatakse transpordiliik, tarneklausel, koht, statistiline väärtus ning lähetuste puhul lisandub tehingupartneri käibemaksukohustuslase number. Lisaks kontrollitakse, et aruande valuutaks oleks EUR).
- Perioodist 2022.a. jaanuar alates kontrollitakse, et Intrastati žurnaalis oleks Lähetus liigiga ridadel täidetud Partneri KM ID.
- Täiendavate nõuetena ei kontrollita enam Transpordiviisi ega Lahetusviisi tähist dokumendidel, mille konteerimiskuupäev on 2022 aastas (sest seda infot enam XML-i ei panda).
- 2022 aastast kehtima hakkavate muudatuste (sh muudatused andmetes) kohta täpsemalt:
  - Palume lugeda <a href="https://www.stat.ee/et/intrastat" target="_blank">Statistikaameti Intrastat lehte</a>
  - Palume vaadata <a href="https://www.youtube.com/watch?v=cbNvK0wDxAM" target="_blank">Statistikaameti infotundi</a>

##### Versioon 17.0.21337.0
- Parandatud viga, mis ei lubanud muuta lähetusviiside tähist.  

##### Versioon 17.0.21312.0
- Lisatud loogika, et kui nomenklatuurinumbrites on kasutusel täiendavad mõõtühikud, siis Intrastati žurnaali võetakse Täiendava mõõtühiku tähisele vastav Rahvusvaheline standardkood Mõõtühikute tabelist (nt PCE).  

##### Versioon 17.0.21225.0
- XML failis ajaformaadi parandus
- Tehnilised täiendused (sh Intrastati žurnaalis toiming Soovita ridu kasutab nüüdsest BC standardit)  

##### Versioon 15.3.21133.0
- Netokaalu ei ümardata enam nulliks (täisarvuks):
  - Lisandus Intrastati žurnaali uus arvutatav väli Täpne kogukaal, kus kuvatakse kogukaal 3 komakohaga.  
  - XML-i loomisel leitakse netokaal <netMass> samuti arvutades, et komadega numbrid säiliksid
