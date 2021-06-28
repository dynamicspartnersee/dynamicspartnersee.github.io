---
---
# Käsitletud ostuarve vastuvõtmine (eFlow raamatupidamiskande dokument) 

Võimaldab salvestada Telema ’entrec’ tüüpi e-dokumente kui **Ostuarve** ja väljastada e-dokumendi kinnituse selle vastusena.

Allpool on peamiste andmeüksuste kaardistamise ja kasutamise kirjeldus.

E-dokumendi number salvestatakse **Ostuarve** väljale **E-arve kande nr.** kiirkaardil **Üldine**. Klõpsates väljal **E-arve kande nr.** avaneb  **Sissetulev E-dokument**, 
kus saate vaadata kaasas olevat PDFi toiminguga **Vaata dokumendi PDF-i**.

**Müüja-hankija nr.** tuvastatakse järgnevate e-dokumendi elementide hulgast ja prioritiseeritakse antud järjekorras::
1.  SellerParty/PartyCode
2.  SellerParty/RegNum

**Makse saaja hankija nr.** tuvastatakse järgnevate e-dokumendi elementide hulgast ja prioritiseeritakse antud järjekorras:
1.  FactorParty/PartyCode
2.  FactorParty/RegNum
3.  PayToParty/PartyCode
4.  PayToParty/RegNum

See tähendab, et kui e-dokumendist leitakse faktooringupartner, siis määratakse see kui **Makse saaja hankija nr.**

Kui e-dokumendist ei suudeta tuvastada, kes on **Makse saaja hankija**, määratakse see BC põhiseadistuse alusel.

Lisaks hankijatele tuvastatakse e-dokumendist ka hankija pangakonto. Kui hankija pangakonto antud IBANi kohta on BC-ist puudu, luuakse uus **Hankija pangakonto** ning määratakse see **Hankija kaart** peal kui **Eelistatud pangakonto**. 

Vaata ka:  [Kuidas luua uusi hankijaid automaatselt](#kuidas-luua-uusi-hankijaid-automaatselt)

Lisaks täidetakse **Ostuarve** peal järgmised väljad:

|Ostuarve väli|E-dokumendi element|
|--|--|
|**Konteerimiskuupäev**|TransactionDate|
|**Dokumendi kuupäev**|InvoiceDate|
|**Tähtaeg**|DueDate|
|**Hankija arve nr.**|SourceDocumentNum (type INVOICE)|
|**Sisseostja tähis**|SourceDocumentNum (type ORDER)|
|**Makse viide**|PaymentRefNum|
|**Valuuta tähis**|Currency|

Kui **Ostuarve** e-dokumendi real on ’AccountType’ väärtuseks ’E’ siis (kulu read) salvestatakse ostuarvele. 

Väljad täidetakse järgmiselt:

|Väli Ostuarve read|E-dokumendi element või konstant|
|--|--|
|**Liik**|’PR konto’|
|**Nr.**|AccountID|
|**Kirjeldus**|ItemDescription|
|**Kogus**|’1’ või kui EntryItemType=CRE siis ’-1’|
|**Otsene ühikkulu KM-ga**|Sum|

**Ostuarve**  rida  **Dimensioonid**  uuendatakse vastavalt **e-dokumendis** esitatud dimensioonide teabele.

Pärast **Ostuarve** salvestamist, e-dokumendi lõppsummasid võrreldakse BC dokumendi summadega **Kokku KM-ta** ja **Kokku (KM-ga)**. Vajadusel lisatakse ümarduse rida ja/või korrigeeritakse KM summa BC-is. 

Pärast **Ostuarve** postitamist väljastatakse kinnitus, mis viitab postitatud arvele ja informeerib **Sissetuleva e-dokumendi** edukast käsitlemisest.

Kui **Sissetuleva e-dokumendi** salvestamine **Ostuarvena** ebaõnnestub (näiteks puuduvad või valed andmed dokumendis), saate e-dokumendi edasise töötlemise tühistada toiminguga **Tühista dokument**. Selle tulemusena väljastatakse veateadet sisaldav vastukviitung. Pärast seda saate parandada kandedokumendi Telema eFlows ja saata selle uuesti BC-sse.   


## Kuidas luua uusi hankijaid automaatselt

Puuduvaid hankijaid saab automaatselt luua kui on saadud Ostuarve (raamatupidamise kandedokument või kuluarve). 

Looge  **Konf. mallid** hankija tabeli jaoks ja valiga väljad ja väärtused mida tahaksite, et automaatselt täidetaks uute hankijate loomisel. Vajadusel looge mitu malli (kodumaine, välismaine). Määrake mall(id) **Riigid/regioonid**  loendis väljale **Uue hankija mall**. NAV tuvastab hankija riigi e-dokumendist ja leiab vastava malli mille alusel luua uus hankija.

E-dokumendis sisalduvate andmete põhjal täidetakse järgmised hankijakaardi väljad:

|Hankija väli:|
|--|
|**Nimetus**|
|**Registreerimisnr.**|
|**KM registreerimise nr.**|
|**Telefon**|
|**Meil**|
|**Aaddress**|
|**Linn**|
|**Postiindeks**|
|**Riigi/regiooni tähis**|

Funktsionaalsuse lubamiseks avage **Telema EDI seadistus** ja märkige **Loo uued hankijad**.
