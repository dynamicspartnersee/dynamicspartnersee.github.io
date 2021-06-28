---
---
# Eesti pangaformaadid - kasutajajuhend
Laiendus lokaliseerib Dynamics 365 Business Central pangafunktsionaalsuse Eesti nõuetele vastavaks.

Eesti lokalisatsioon sisaldab:
- Kliendi- või arvepõhised viitenumbrid müügiarvetel
- Pangarekvisiitide täiendused müügidokumendite kujundustel (tellimus, arve, kreeditarve)
- Eesti SEPA makseformaat
- Eesti SEPA väljavõtteformaat
- Viitenumbrit ja registreerimisnumbrit arvestavad maksete sidumisreeglid

## Viitenumbrid müügis
Müügiarvetel viitenumbrite kasutamine aitab hiljem väljavõtte töötlemisel laekumisi käsitleda.

Müügis viitenumbrite kasutamiseks avage **Eesti pangaformaatide seadistus** ja määrake **Müügi viitenr.** ühena alljärgnevast:

Väärtus | Selgitus
-- | --
Loo kliendi numbrist | **Makse viitenr.** genereeritakse uue kliendi loomisel ja kantakse edaspidi kliendi pealt kaasa tema arvetele.
Loo arve numbrist | **Makse viitenr.** genereeritakse konteerimise käigus müügiarve numbrist. Seda juhul, kui **Makse viitenr.** puudus enne konteerimist.

## Müügidokumentide kujundused
Lisatud on kolm uut dokumendi kujundust, millel on toodud Eestis üldlevinud kujul ettevõtte- ja pangarekvisiidid:
-  *1305 - Estonian Order Confirmation*
-  *1306 - Estonian Sales Invoice*
-  *1307 - Estonian Sales Credit Memo*

## SEPA makseformaat
Business Central'is koostatud maksete panka edastamiseks on lisatud Eesti SEPA makseformaadi tugi.

Kas formaat on installitud, saate kontrollida **Eesti pangaformaatide seadistuses**. Kui ei ole, võtke ühendust oma partneriga.

Formaadi seadistamiseks pangakontole avage **Pangakontod** ja redigeerige soovitud kontot. Määrake *SEPACT-EE* väljal **Makse ekspordi vorming**.

## SEPA väljavõtteformaat
Pangaväljavõtete importimiseks Business Central'isse on lisatud Eesti SEPA väljavõtteformaadi tugi.

Kas formaat on installitud, saate kontrollida **Eesti pangaformaatide seadistuses**. Kui ei ole, võtke ühendust oma partneriga.

Formaadi seadistamiseks pangakontole avage **Pangakontod** ja redigeerige soovitud kontot. Määrake *SEPACAMT-EE* väljal **Panga väljavõtte impordi vorming**.

## Maksete sidumise reeglid
Business Central'i makse sidumisreegleid on täiendatud järgnevate komponentidega: 
-  *Viitenumber* - aitab dokumendi vastendamisel.
-  *Registreerimisnumber* - aitab kliendi/hankija vastendamisel.

Täiendavad reeglid ei vaja seadistamist ja ei ole nähtavad **Maksete sidumisreeglites**.

Täiendatud reegleid kasutatakse **Maksete sobitamise žurnaali** tegevusel  **Seo automaatselt**.

## Makse saaja
Kui makse saaja on erinev hankijast (näiteks on saajaks faktooring või Rahandusministeerium), lisage andmed **Hankija pangakonto kaart** kiirkaardil **Saaja**.  
Kui **Saaja nimi** väli on täidetud, kasutatakse antud nime ka maksefailis. 

***

Täpsema info saamiseks võtke palun ühendust oma partneriga:  
[http://www.dynamicspartners.ee](http://www.dynamicspartners.ee)
