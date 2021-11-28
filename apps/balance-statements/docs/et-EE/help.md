---
---
# Saldoteatised - Kasutusjuhend

Saldoteatise funksionaalsus võimaldab kasutajal saata klientidele/hankijatele saldoteatised vastavalt enda valitud kuupäevale ning jälgida nende kinnitamisi.  
Lisaks on Põhivarade loendis võimalik väljastada **PV Saldo** (inventuuri loend) aruannet.
  
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
Enne, kui hakkad esmakordselt saldoteatiseid välja saatma, palun veendu, et  **Meili stsenaarium** on määratud.  
Saldoteatised saadetakse välja meilikontoga, mille alla on määäratud stsenaarium **Saldoteatis**. Kui viimane on määramata, siis kasutatakse vaike meilikontot. 

Kliki **Protsess -> Saada teatised...**

|**Välja nimi**|**Selgitus**|
|-|-|
|**Meiliaadressid:**||
|Saatja|Määratleb meilisõnumi saatmise konto. Meilikonto määratakse lehel Meili stsenaariumi määramine.|
|Koopia|Määratleb isikute meiliaadressid, kes saavad kirja koopia.|
|Salakoopia|Määratleb isikute meiliaadressid, kes saavad kirja salakoopiana (Bcc). Neid aadresse ei näidata teistele kirja saajatele.|
|Test adressaat|Kui väli on täidetud, siis saadetakse saldoteatis sellele meiliaadressile (Saaja meili asemel). Saab kasutada testimiseks.|
|Ava meilisõnumi koostamine|Määratleb, kas saldoteatis(ed) avatakse enne saatmist Meilisõnumi koostamise lehel. NB! Saldoteatis(ed) märgitakse saadetuks ka juhul, kui meil hüljatakse Meilisõnumi koostamise lehel.|
|**Filtrid:**||
|Nr.|Vaikimisi on filtris saldoteatis(ed), mis oli(d) valitud nupule "Saada teatised..." vajutamise hetkel. Kui soovid saata kõik saltoteatised korraga, siis tühjenda filter.|

Vajuta **OK** ning ning süsteem alustab saldoteatiste välja saatmist.  
Õnnestunult saadetud saldoteatised saavad märke **Saadetud**.  
Saadetud saldoteatised on leitavad ka kliendi/hankija alt avanevast **Saadetud meilisõnumid** lehelt.  

Hiljem, kui äripartnerid on vastanud, saate märkida teatise oleku **töödelduks**.  
Lisaks on võimalik igale saldoteatisele lisada **manuseid** ja **märkmeid**.  

<br>

## PV Saldo (inventuuri loend)
Põhivarade loendis, aruannete sektsioonis (Rohkem suvandeid all) on aruanne **PV Saldo**.  

Aruanne võimaldab väljastada põhivarade loendi teatud kuupäeva seisuga ning kasutada seda näiteks põhivara inventeerimiseks.  

|**Välja nimi**|**Selgitus**|
|-|-|
|**Valikud:**||
|Kulumiraamat|Määratleb kulumiraamatu tähise, mille kohta aruanne väljastatakse.|
|Dokumendi nr.|Määratleb aruandel kuvatava dokumendi numbri|
|Saldo kuupäev|Määratleb kuupäeva, mis seisuga on info aruandel kajastatud.|
|Trüki PV finantsinfo|Määratleb, kas aruandel kuvatakse üldinfo (klass, alamklass jne) asemel finantsinfo (soetusmaksumus, kulum, jääkväärtus).|
|Kaasa jääkväärtuseta PV|Määratleb, kas aruandele kaasatakse ka null jääkväärtusega põhivarad.|
|Rühmitusalus|Määratleb millistel alustel põhivarad aruandele rühmitatakse.|
|Uus lk per rühm|Määratleb, kas iga rühm trükkida eraldi lehele.|
|**Komisjoni liikmed:**|Väljatrükile saab valida töötajate loendist kuni 3 inventuurikomisjoni liiget|


<br>

Lisainformatsiooni saamiseks pöördu partneri poole:  
<a href="http://www.dynamicspartners.ee/" target="_blank">www.dynamicspartners.ee</a>
