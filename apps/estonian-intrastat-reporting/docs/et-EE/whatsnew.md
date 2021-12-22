---
---

##### Versioon 17.2.21356.1
- XML-i loomisel arvestab lahendus 2022 aastast kehtima hakkavad nõudeid (lisandub tehingupartneri käibemaksukohustuslase number ning eemaldatakse transpordiliik, tarneklausel, koht, statistilise väärtus. Lisaks kontrollitakse, et aruande valuutaks oleks EUR).
- Täiendavate nõuetena ei kontrollita enam Transpordiviisi ega Lahetusviisi tähist dokumendidel, mille konteerimiskuupäev on 2022 aastas (sest seda infot enam XML-i ei panda).

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
