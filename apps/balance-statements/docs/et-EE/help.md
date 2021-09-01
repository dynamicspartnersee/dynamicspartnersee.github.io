---
---
# Saldoteatised - Kasutusjuhend

Saldoteatise funksionaalsus võimaldab kasutajal saata klientidele/hankijatele saldoteatised vastavalt enda valitud kuupäevale ning jälgida nende kinnitamisi.
  
<br>

## Saldoteatise laienduse olemasolu kontroll
Ava **Laiendused** ja veendu, et laiendus ‘Balance Statements’ on installitud. Kui pole, võid selle leida <a href="https://appsource.microsoft.com/et-ee/product/dynamics-365-business-central/PUBID.estonian_dynamics_partners%7CAID.balance-statements%7CPAPPID.2c6e9797-3574-4828-b075-ef340322f94c" target="_blank">AppSourcest</a> või võta ühendust oma partneriga.  

<br>

## Seadistused
**Ava otsingust Saldoteatiste seadistused**

|**Välja nimi**|**Selgitus**|
|-|-|
|Saldoteatiste numbrid|Seadista endale soovitud saldoteatise numbriseeria.|
|Kliendi meilisõnumi kujunduse tähis|CUST-EMAIL- sisse ehitatud aruanne, võimalik modifitseerida vastavalt enda vajadustele.|
|Hankija meilisõnumi kujunduse tähis|VEND-EMAIL  sisse ehitatud aruanne, võimalik modifitseerida vastavalt enda vajadustele.|

<br>

## Saldoteatised
Ava otsingust **Saldoteatised**.
  
  
### Kuidas luua kliendi/hankija saldoteatiseid
Saldoteatiste loomise protsess kliendidele ja hankijatele on analoogne.

Kliki **Protsess -> Loo kliendi/hankija teatised**

|**Välja nimi**|**Selgitus**|
|-|-|
|Saldo kuupäev|Määrab ära, mis seisuga saldo kuvatakse.|
|Tagastamise kuupäev|Kuupäev, mis ajaks oodatakse vastust.|
|Prindi KV-s|Määratleb kas võlgnevuse summa näidatakse konverteerituna kokku kohalikus valuutas või iga valuuta kohta eraldi.|
|Väljastaja |Valitud Töötaja nimi ning info (telefon, meil, ametinimetus) lisatakse saldoteatisele.|
 
Loo sobiv filter ja vajuta **OK** ning süsteem alustab saldoteatiste loomist.

![CustomerStatementList](CustomerStatementList.png)

Punaselt kuvatakse saldoteatised, millel puudub Saaja meiliaadress (või on mõni muu saatmise tõrge).  
**Saaja meiliadressi saab muuta/lisada toiminguga "Muuda saaja meil..."** ning järgmiseks korraks kliendi kaardile salvestada (_va olekuga Töödeldud teatised_).

<br>

Saldoteatise PDF faili leiad kiirinfo väljalt, kus vajadusel saad selle ka avada:

![CustomerStatementFactbox](CustomerStatementFactBox.png)

<br>

PDF faili kujundust ning meilisõnumi sisu saab kohandada lehel **Aruande kujunduse valik**:

|**Aruande ID**|**Aruande nimetus**|
|-|-|
|24012100|Klient - Saldoteatis|
|24012101|Hankija - Saldoteatis|

<br>

## Kuidas saata Saldoteatiseid
Enne, kui hakkad saldoteatiseid välja saatma, palun veendu, et  **SMTP-posti seadistused** on tehtud.

Kliki **Protsess -> Saada teatised...**

|**Välja nimi**|**Selgitus**|
|-|-|
|**Meiliaadressid:**||
|Saatja meil|Siia sisesta emaili aadress, mille pealt saldoteatised välja saadetakse. Sõltub **SMTP seadistusest**, kas saab saata ainult sinna määratud aadressilt või saab kasutada erinevaid aadresse.|
|Saatja nimi|Määratleb saajale kuvatava saatja nime (va juhul, kui viimane tuleb meilikontolt).|
|Koopia|Määratleb isikute meiliaadressid, kes saavad kirja koopia.|
|Salakoopia|Määratleb isikute meiliaadressid, kes saavad kirja salakoopiana (Bcc). Neid aadresse ei näidata teistele kirja saajatele.|
|Test adressaat|Kui väli on täidetud, siis saadetakse saldoteatis sellele meiliaadressile (Saaja meili asemel). Saab kasutada testimiseks.|
|**Filtrid:**||
|Nr.|Vaikimisi on filtris see saldoteatis, mille peal olles "Saada teatised..." toimingu käivitasid. Kui soovid saata kõik saltoteatised korraga, tühjenda filter.|

Vajuta **OK** ning ning süsteem alustab saldoteatiste välja saatmist.
Õnnestunult saadetud saldoteatised saavad märke **Saadetud**.

Hiljem, kui äripartnerid on vastanud, on võimalik igale saldoteatisele lisada **manuseid** ja **märkmeid** ning märkida teatise olek **töödelduks**. 


Lisainformatsiooni saamiseks pöördu partneri poole:  
<a href="http://www.dynamicspartners.ee/" target="_blank">www.dynamicspartners.ee</a>
