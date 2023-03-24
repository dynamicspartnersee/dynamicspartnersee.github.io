---
---

##### Versioon 17.0.23083.0
- E-dokumendid vajavad üsna palju salvestusruumi ja on tihti baasis ühed suuremad tabelid. Vanad e-dokumendid saab nüüd kustutada läbi "Säilitamise poliitika" funktsionaalsuse.

##### Versioon 17.0.23076.0
- Telema soovil tühistatakse e-dokument, mille saatmisel tekib veakood 0 ehk järgmised tüüpvead:
  - tundmatu saatja 
  - tundmatu saaja 
  - puuduv link saatja ja saaja vahel 
  - valideerimise viga 
  - duplikaat
  
  Tühistamine tähendab, et lõpetatakse dokumendi edasised saatmiskatsed.

##### Versioon 17.0.23072.0
- Lisandus Web Folders funktsionaalsus, mis võimaldab failivahetust on-prem serveritega. Serveris kus asub failikaust, tuleb see välja jagada IIS Virtual Directory-na ning aktiveerida WebDAW Publishing, Directory Browsing ja Basic Authentication.

##### Versioon 17.0.22311.0
- Müügidokumentidele on lisatud OrderParty blokk, lisaks senistele BuyerParty ja DeliveryParty blokkidele. See tähendab, et toetatud on kõigi kolme osapoole: Ostja, Maksja ja Saaja väljastamine.

##### Versioon 17.0.22259.0
- Telema seadistuses saab määrata "Tuvstamata kauba nr". Sel juhul ei lähe sissetulev dokument tõrkesse kui kaupa ei leita, vaid kasutatakse seda.
- E-dokumendid vajavad üsna palju salvestusruumi ja on tihti baasis ühed suuremad tabelid. Mahu vähendamiseks pea poole võrra ei eraldata enam XML-ist PDF-i ja ei salvestata seda eraldi. Kasutuskogemust muudatus ei mõjuta - PDF-i vaatamisel loetakse see sel samal hetkel XML-ist välja ning kuvatakse.

##### Versioon 17.0.22185.0
- Lisandus teavituslahendus. Seadistuses saab määrata e-meili aadressi(d), keda teavitatakse, kui e-dokumendi käsitlemine ebaõnnestub (nii sisse kui välja suunal).  
  
##### Versioon 16.0.22103.0
- Uus dokumendi liik: **Müügitellimuse kinnitus**.
- Uus sündmus **OnBeforeModifySalesHeader** sissetuleva müügitellimuse käsitlemisel.
- Uus sündmus **OnBeforeSalesLineInsert** sissetuleva müügitellimuse käsitlemisel.
- Uus sündmus **OnAfterSaveSalesOrderLine** sissetuleva müügitellimuse käsitlemisel.
- Uus sündmus **OnAfterSaveRecAdv** sissetuleva tarnekinnituse käsitlemisel.
- Uus sündmus **OnAfterModifySalesLineRecAdv** sissetuleva tarnekinnituse käsitlemisel.

##### Versioon 16.0.21361.0
- Litsentsikontroll uuendatud oauth autentimisele

##### Versioon 16.0.21356.0
- Äpi nimi muutus: "Telema & Edisoft EDI"

##### Versioon 16.0.21285.0
- BC19 tugi
- GTIN välja tugi
- Kauba viidete tugi (lisaks ristviidetele)

##### Versioon 15.0.21235.0
- Parendatud tarne sidumist arvega 
  
##### Versioon 15.0.21216.0
- Vastavalt Telema soovitusele on e-arve ReceiverID elemendi väärtus "Maksja-kliendi nr." asemel "Ostja-kliendi nr.".
  
##### Versioon 15.0.21189.0
- Edisoft opertaatori tugi

##### Versioon 15.0.21122.1
- Kliendi kaardil uus valik **Saateleht hindadeta**

##### Versioon 15.0.21122.0
- eFlow dokumendikviitungit ei väljastatud konteerimisel. Parandatud.
- Uus sündmus **OnBeforeSaveSalesOrderLine** sissetuleva müügitellimuse käsitlemisel.
- Uus sündmus **OnBeforeEDocCreateEntry** peale väljamineva müügidokumendi (arve, saateleht, kreeditarve) loomist.

##### Versioon 15.0.20315.0
- Uus väli "Luba kauba nr. kasutamist" kliendi ja hankija kaardil. Juhul kui kaupa ristviite järgi ei tuvastatud, siis kasutatakse e-dokumendil olevat kauba numbrit.

##### Versioon 15.0.20314.0
- Veebiteenustel baseeruv otsekanal dokumendivahetuseks Business Central ettevõtete vahel.
- Uus dokumendi liik: **Ostutellimuse kinnitus**.

##### Versioon 1.0.19161.0
- Ostuarve: kauba mittetuvastamisel kulukonto tuvastamise funktsionaalsus ("Vastenda tekst kontoks" seadete alusel).
