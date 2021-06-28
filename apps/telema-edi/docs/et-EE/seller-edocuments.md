---
---
# E-dokumendid müüjale

## Sisukord
 - [Müügitellimuse või müügi tag.korralduse vastuvõtmine](#müügitellimuse-või-müügi-tag.korralduse-vastuvõtmine)
 - [Müügilähetuse väljastamine](#müügilähetuse-väljastamine)
 - [Tarnekinnituse vastuvõtmine](#tarnekinnituse-vastuvõtmine)
 - [Müügi- või kreeditarve väljastamine](#müügi--või-kreeditarve-väljastamine)


## Müügitellimuse või müügi tag.korralduse vastuvõtmine

Võimaldab Telema "tellimus" tüüpi e-dokumente salvestada kui **Müügitellimused** ja "tagastus" tüüpi e-dokumente kui **Müügi tag.korraldus**.

Nende partnerite jaoks, kes kasutavad 4 dokumendi süsteemi, peaks märkeruut **Nõua e-tarnekinnitust** olema valitud ostja-kliendi kaardil. Sellisel juhul kasutatakse müügitellimuse välja **E-tarnekinnituse olek**.
See näitab tellimuse käsitlemise staatust. Müügitellimuse loomisel muutub välja väärtuseks ‘**Nõutud**’, mis annab laole märku, et müügitellimuse kohta ei saa arvet esitada enne kui tarnekinnitus on kliendilt saabunud.

Allpool on peamiste üksuste kaardistamise kirjeldus.

Kliendi tellimuse number salvestatakse väljale **E-tellimuse nr.**. Väli on nähtav ka tellimuste loendis, mis annab ülevaate elektrooniliste kanalite kaudu saabunud tellimustest.

Kõik e-dokumendi väljal ‘AdditionalInfo’ asuvad kirjed salvestatakse **Kommentaarid** väljale. 

**Ostja kliendi nr.** määratletakse järgnevas prioriteedijärjestuses:
1.  OrderParty/PartyCode
2.  OrderParty/GLN
3.  DeliveryParty/PartyCode
4.  DeliveryParty/GLN
5.  BuyerParty/PartyCode
6.  BuyerParty/GLN

**Maksja-kliendi nr.** ei võeta failist, kasutusele jääb BC vaikimisi väärtus.

**Seotud dokumendi liik** ja **Seotud dokumendi nr.** täidetakse müügi tagastuskorraldusel kui on olemas viide originaalarvele.

**Kauba nr.** määratakse järgnevas prioriteedijärjestuses ja **Kauba varianti** ei käsitleta:

1.  'GTIN' otsimine tabelist **Kauba ristviited**
2.  'SellerItemCode' otsimine tabelist  **Kauba ristviited**
3.  ‘BuyerItemCode’ otsimine tabelist **Kauba ristviited**

**Kogus** määratakse järgnevalt:

1. Kui 'BaseUnit' vastab BC vaikimisi mõõtühikule ostu tellimusel, siis võetakse kasutusele 'AmountOrdered'.
2. Kui 'BaseUnit' ei vasta ostutellimuse vaikimisi mõõtühikule, siis 'AmountOrdered' jagatakse väärtusega **Kogus mõõtühiku kohta**. Eeldatakse, et kogus failis on alusmõõtühik.

Ühiku hind võetakse elemendilt ‘ItemPrice’ kui kliendikaardil on märkeruut  **Võta hind e-tellimuselt** valitud. See on lõpphind ja allahindlusi ei rakendata.
Kui märkeruutu **Võta hind e-tellimuselt** ei ole valitud, siis võetakse hind ja allahindlus vastavalt BC hinnastruktuurile.

Kui e-tagastuskorraldus viitab originaalarvele, siis võetakse hinnad ning allahindlused müügi tagastuskorraldusele originaalarvelt.
Täpse maksumusega storno taotlusi ei esitata.

**Partiinumbri** informatsiooni ei käsitleta.

## Müügilähetuse väljastamine
Võimaldab luua saatelehe konteeritud e-tarnest.

Et saata e-tarneid klientidele, tuleb kõigepealt seadistada **Kliendi kaart.** See seadistus on vajalik **Ostja klient** (mitte **Maksja klient**) kaardil.  

Avage kliendi kaart ja tehke järgnev seadistus **Telema EDI** kiirkaardil:

|Väli|Kasutamine|
|--|--|
|**Väljasta e-saateleht**|Märkige ruut kui soovite välja saata müügilähetusi.|
|**GLN**|Kui kliendil on globaalne asukohakood, siis selle saate sisestada antud väljale.|

Lisaks on vajalik lõpetada **Telema EDI Seadistus** leht.
Avage **Telema EDI seadistus** ja täitke kiirkaart **Müügidokumendid** järgnevalt:

|Väli|Kasutamine|
|--|--|
|**Loo e-saatelehed konteerimisel**|Märkige ruut, kui soovite luua e-saatelehed konteerimise ajal. ** See on soovitatav seadistus! **|
|**Ainult kauba read e-arvetel**|Märkige ruut kui soovite e-tarnetel saata ainult kauba read.|
|**GLN**|Kui ettevõttel on globaalne asukohakood, siis selle saab sisestada antud väljale. Saate taodelda oma ettevõttele GLN numbri läbi GS1 Estonia (www.gs1.ee)|

Allpool on peamiste andmeüksuste kaardistamise kirjeldus.

|BC üksus|Telema e-dokumendi üksus|Selgitus|
|--|--|--|
|**Päis**|
|Maksja klient|BuyerParty|
|Ostja klient|DeliveryParty|
|Ettevõtte andmed|SellerParty|
|E-tellimuse nr.|SourceDocument|Viide tellimusele.|
|**Read**||Kui  **Ainult kauba read e-arvetel** märkeruut **Telema EDI seadistus** kaardil on valitud, siis kuvatakse ainult kauba read.|
|Nr.|SellerItemCode|
|Variandi tähis||Variandi informatsiooni ei saadeta.|
|Ristiviite vöötkoodi liik|GTIN|
|Ristviite kliendi liik|BuyerItemCode|
|Kogus (alusmõõtühik)|AmountDespatched|Kogus alusmõõtühikus.|
|Summa / Kogus (alus)|ItemPrice|Võetakse tellimuse realt. Vajalik Bauhofile. Lõpphind, mis sisaldab allahindlusi. Teave saadetakse kliendikaardi väljal **Hinna ümardamistäpsus e-arvel** määratud väärtuse alusel.|
||SourceDocument|Viide e-tellimusele ja e-tellimuse rea number.|
|**Kauba jälgimine**|ItemReserve|Saadetakse partiinumbrid, seerianumbrid ja aegumise info.|

Kasutades konteeritud dokumendis toimingut **Navigeeri**, saate vaadata dokumendist loodud e-dokumenti. Koos teiste kirjetega leiab see funktsioon ka kirje **Väljaminev e-dokument**.

## Tarnekinnituse vastuvõtmine

Tarnekinnitus võimaldab ostjal kinnitada kauba kättetoimetamise. 
Erinevuste ilmnemisel saata teha vajalikud parandused (**Konteeritud müügilähetused** kiirkaardil read **Funktsioonid->Võta lähetus tagasi** )ja konteerida uue(d) rea(d).

**NB!** Parandusdokumendi konteerimisel valige **Ära saada e-dokumendina.**

Et salvestada e-tarnekinnitusel olevad andmed, seotud **Müügitellimus** otsitakse ja uuendatakse järgnev informatsioon: 
- Müügirea **E-tarnekinnituse kogus** uuendatakse
- (Müügirea **E-tarnekinnituse hinnaalandiga hind** uuendatakse)
- Müügitellimuse päises **E-tarnekinnituse** **Olek** uuendatakse)

 **E-tarnekinnituse** **Olek** muutub väärtuseks 'Kinnitatud' kui erinevusi ei ole ja 'Erinevused' kui mõned ridadest sisaldavad ühte järgnevatest erinevustest:
 - **E-tarnekinnituse kogus** väärtus erineb **Lähetatud kogus** väärtusest.
 - **E-tarnekinnituse hinnaalandiga hind** on täidetud (Bauhofi puhul) ja see erineb väärtusest mis on järgnevalt arvutatud: **Rea summa KM-ta** jagatud **Kogus** väärtusega.  Hinnaalandiga hindu võrreldakse kahe kümnendkoha täpsusega.

Kui ilmnesid erinevused ja olete parandused teinud, värskendage **E-tarnekinnituse** **olek** väärtuseks 'Kinnitatud'. Vastasel juhul ei saa arvet väljastada.

Allpool on peamiste andmeüksuste kaardistamise ja kasutamise kirjeldus.

Kõik väljal ‘AdditionalInfo’ asuvad kirjed salvestatakse **Kommentaarid** väljale. 

**Kauba nr.** tuvastamine toimub samal põhimõttel kui **Müügitellimus** puhul ja **Kauba varianti** ei käsitleta.

Müügitellimuse rida, mis on seotud e-tarnekinnituse reaga leitakse kauba numbri põhjal. Seetõttu ei toetata tellimusi millel on sama kauba number mitmel real. 

Kui e-tarnekinnitus sisaldab viidet tellimuse relae, siis kasutatakse seda viidet ridade sobitamiseks. Vastasel juhul sobitatakse müügitellimuse rida e-tarnekinnituse reaga Kauba nr. alusel. Viimasel juhul ei toetata dokumente, millel on sama kauba nr. mitmel real.  

Et salvestada **e-tarnekinnituse kogus** kasutatakse e-dokumendi elementi 'AmountAccepted'. Kui seda elementi ei leta, siis kasutatakse elementi 'AmountActual'. 
Kui **e-tarnekinnituse kogus** on juba täidetud, eelmist väärtust ei kustutata ja lisatakse uus väärtus.

Et salvestada **e-tarnekinnituse hinnaalandiga hind** kasutatakse e-dokumendi elementi 'ItemPrice'.

Vajadusel teisendatakse väärtused õigeks mõõtühikuks samal põhimõttel nagu **müügitellimus** puhul.

**Partiinumbri** informatsiooni ei käsitleta.

## Müügi- või kreeditarve väljastamine

Võimaldab konteeritud müügiarvest ja kreeditarvest e-arve koostada.

Et saata e-arveid klientidele, tuleb kõigepealt seadistada **Kliendi kaart.** See seadistus on vajalik **Ostja klient** (mitte **Maksja klient**) kaardil.

Avage kliendi kaart ja tehke järgnev seadistus **Telema EDI** kiirkaardil:

|Väli|Kasutamine|
|--|--|
|**Väljasta e-arve**|Märkige ruut kui tahate välja saata müügiarveid (ning kreeditarveid).|
|**GLN**|Kui kliendil on globaalne asukohakood, siis selle saate sisestada antud väljale.|
|**Hinna ümardamistäpsus e-arvel**|Näites kui soovite, et arvel oleks 5kohta peale koma, sisestage 0,00001. Ümardamist võib vaja minna, sest lõpphind arvutatakse jagades rea summa (€) kogusega. Allahindluseid ei lisata e-arvetele.

Lisaks on vajalik lõpetada **Telema EDI Seadistus** leht.

Avage **Telema EDI seadistus** ja täitke kiirkaart **Müügidokumendid** järgnevalt:

|Väli|Kasutamine|
|--|--|
|**Loo e-arved konteerimisel**|Märkige ruut, kui soovite luua e-arved (ka kreeditavred) konteerimise ajal. ** See on soovitatav seadistus! **|
|**Ainult kauba read e-arvetel**|Märkige ruut kui soovite e-arvetel saata ainult kauba read.|
|**GLN**|Kui ettevõttel on globaalne asukohakood, siis selle saab sisestada antud väljale. Saate taodelda oma ettevõttele GLN numbri läbi GS1 Estonia (www.gs1.ee)|


Allpool on peamiste andmeüksuste kaardistamise ja kasutamise kirjeldus.

|BC üksus|Telema e-dokumendi üksus|Selgitus|
|--|--|--|
|**Päis**|
|Maksja klient|BuyerParty|
|Ostja klient|DeliveryParty|
|Ettevõtte andmed|SellerParty|
||SourceDocument|Arve pouhul on viide tellimusele, lähetusele ja tarnekinnitusele. Kreeditarve puhul on viide tagastuskorraldusele ja originaalarvele kui väli **seotud dokumendi nr.** on täidetud.|
|Line Amount|DocumentSum|
|Line Amount incl. VAT|TotalSum|
|**Read**||Kui  **Ainult kauba read e-arvetel** märkeruut **Telema EDI seadistus** kaardil on valitud, siis kuvatakse ainult kauba read.|
|Nr.|SellerItemCode|
|Variandi tähis||Variandi informatsiooni ei saadeta.|
|Ristiviite vöötkoodi liik|GTIN|
|Ristviite kliendi liik|BuyerItemCode|
|Kogus (alusmõõtühik)|AmountInvoiced|Kogus alusmõõtühikus.|
|Summa / Kogus (alus)|ItemPrice|Lõpphind koos allahindlustega. Teave saadetakse kliendikaardi väljal **Hinna ümardamistäpsus e-arvel** määratud väärtuse alusel.|
|Summa|ItemSum|ItemSum sisaldab kõiki allahindlusi.|
||SourceDocument|Viide e-tellimusele ja e-tellimuse rea number.|
|**Kauba jälgimine**|ItemReserve|Saadetakse partiinumbrid, seerianumbrid ja aegumise info.|

Kasutades konteeritud dokumendis toimingut **Navigeeri**, saate vaadata dokumendist loodud e-dokumenti. Koos teiste kirjetega leiab see funktsioon ka kirje **Väljaminev e-dokument**.
