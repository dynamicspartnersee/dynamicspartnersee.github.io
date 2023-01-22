---
---
# Eesti pakendiaktsiis - Kasutusjuhend

Käesolev äpp lisab Dynamics 365 Business Central-i pakendiaktsiisi funktsionaalsuse.

Ettevõtjad peavad esitama kord kvartalis pakendi aktsiisideklaratsiooni. Antud Eesti lokalisatsiooni funktsionaalsus võimaldab Business Centralis koostada aktsiisideklaratsiooni esitamise jaoks vajaliku andmete komplekti. Funktsionaalsus ei sisalda aktsiisideklaratsiooni aruande väljatrükki.

Viited pakendiseadusele:
- <a href="https://www.riigiteataja.ee/akt/104042012006?leiaKehtiv" target="_blank">Pakendiseadus</a>
- <a href="https://www.riigiteataja.ee/akt/13074692?leiaKehtiv" target="_blank">Pakendiaktsiisi seadus</a>

# Seadistamine

## Üldseadistus

Pakendimaterjalide seadistused leiab sisestades otsingusse **Pakendimaterjalid**

## Pakendiaktsiisi seadistused kaupadel

### Kaubakaart

Kiirkaardil **Varud** valitakse väärtus väljale **Pakendi aktsiisiarvutus**. Välja võimalikud väärtused on järgmised:

**Väärtus** | **Selgitus**
-- | --
Ei arvutata | Kaupa ei kaasata pakendi aktsiisiarvutustesse.
Kasuta kande mõõtühikut | Pakendid peavad olema seadistatud mõõtühikute kohta, mida kasutatakse tehingute tegemisel.
Kasuta alusmõõtühikut | Pakendid peavad olema seadistatud ainult alusmõõtühikule. Teistes mõõtühikutes tehtud tehingud teisendatakse pakendikoguste arvutamiseks alusmõõtühikusse.

### Kauba mõõtühiku sidumine pakkematerjalidega

Pakendiaktsiisi arvutuseks peab kauba mõõtühiku(d) siduma pakkematerjalidega.  
Selleks vajutatakse **Kaubakaardi** lintmenüü **Toimingud** -> **Kaup** all nuppu **Pakendimaterjalid**.  
Avaneval **Kauba pakendimaterjalid** lehel seadistatakse kauba mõõtühikuga (või erinevate mõõtühikutega) seotud pakkematerjalide tähised ja kogus (kg) ehk kaal.  
Samas saab isikupärastamisega tuua nähtavale **Variandi tähis** veeru, et sisestamaks pakendimaterjalid erinevate variantide lõikes (juhul kui erinevatel kauba variantidel on erinevad pakendid).  
NB! Kui mõnel kauba variandil puudub pakend, kuid tühja variandiga kaubal on pakendimaterjal, siis tuleks vastava variandi kauba pakendimaterjali koguseks määrata null.

Lisainfona (nt audiitorile) saab lisada pakendi kaalu saamise meetodi (valikus Ise kaalutud, Hankija andmed, Analoogne kaup).  
Isikupärastamisega saab lehele lisada looja ning muutja informatsiooni veerud.  

# Kasutamine

Pakendiaktsiisi aruande koostamiseks tuleb otsinguga leida leht **Pakendi aktsiisdeklaratsioonid**.  
Uue pakendi aktsiisideklaratsiooni loomiseks tuleb vajutada nupule **Uus** ning määrata deklaratsioonile number.  
Nupp **Redigeeri** võimaldab muuta märgitud ja esitamata pakendi aktsiisideklaratsioone.  

Pakendi aktsiisideklaratsiooni päise osal on järgmised väljad:

**Väli** | **Selgitus**
-- | --
Nr. | Väljale sisestatakse pakendi aktsiisideklaratsiooni number.
Kirjeldus | Pakendi aktsiisideklaratsiooni kirjeldus.
Perioodi algus | Määrab perioodi alguse.
Perioodi lõpp | Määrab perioodi lõpu.
Muudetud | Pakendi aktsiisideklaratsiooni viimase muutmise aeg.
Muutja | Pakendi aktsiisideklaratsiooni viimase muutaja kasutajanimi.
Esitatud | Viitab, et pakendi aktsiisideklaratsioon on esitatud. Muudab väljad (v.a **Esitatud**) mittemuudetavaks.

Pakendi aktsiisideklaratsiooni arvutamise tegevus käivitatakse lehel **Pakendi aktsiisdeklaratsioon** nupust **Arvuta read**.  
Avaneval päringuvormil määratakse filtrid (need on vaikimisi eeltäidetud) ja vajutatakse **OK**.

Süsteem arvutab pakendiaktsiisi kogused filtritega määratud tingimustel.  

Tegevuse **Arvuta read** päringuvormi (_kaubaandmiku kanded_) filter on vaikimisi eeltäidetud järgmiselt:
-   Kande liik = müük
-   Riigi/regiooni tähis = riigi/regiooni tähis ettevõtte andmetest
-   Konteerimiskuupäev = filter deklaratsiooni perioodile lähtuvalt deklaratsiooni päises määratud kuupäevadest  
Juhul kui aruandel on juba ridu, siis tegevuse **Arvuta read** teistkordsel käivitamisel kuvatakse kasutajale hoiatus, mille aktsepteerimisel arvutatakse read uuesti.

Pakendi aktsiisideklaratsioon täidetakse järgmise loogikaga:  
-   Ridadena luuakse kõik kirjed tabelist **Pakendimaterjalid** (ehk kõik seadistatud pakendimaterjalid).
-   Iga filtrisse jääva **Kaubaandmiku kande** puhul lähtutakse vastava kauba kaardil olevast **Pakendi aktsiisiarvutus** määratlusest.
-   Kui kaup on määratud osalema pakendi aktsiisiarvutuses, siis otsitakse vastavale kaubale seadistatud pakendimaterjale.
  -   Kui kaubale on määratud pakendimaterjalid variantide lõikes, siis arvutatakse pakendite kogused vastavalt variantidele.
-   Pakendi aktsiisideklaratsiooni kandeid luuakse iga kaubakande kohta nii palju, kui on erinevaid pakendeid kaubale seadistatud.
  

Valmis genereeritud aruande ridu käsitsi lisada ja kustutada ei saa. Kasutaja saab lisada väärtused järgmistesse veergudesse:
-   **Ümbert. tegelik kogus (KG)** (Ümbertöödeldud pakendimaterjali kogus kilogrammides)
-   **Ringlussev. tegelik kogus (KG)** (Ringlusse võetud pakendimaterjali kogus kilogrammides)
-   **Taask. tegelik kogus (KG)** (Taaskasutusse võetud pakendimaterjali kogus kilogrammides)

Klikkides veeru **Pakendimaterjali kogus (KG)** väärtusele, avatakse leht **Pakendi aktsiisideklaratsiooni kanded**, kus kuvatakse detailsed kanded, millest arvutatud kogus koosneb.

Kui aruanne on esitatud, siis märgitakse selle päises väli **Esitatud**.  
Kui väli on märgitud, siis:
-   ei lubata pakendi aktsiidideklaratsiooni päise välju muuta (v.a väli **Esitatud**, mis võimaldab aruande uuesti avada) ja aruannet kustutada;
-   ei lubata pakendi aktsiidideklaratsiooni ridu muuta ega käivitada uuesti tegevust **Arvuta read**.

----------

Täpsema info saamiseks, palun võtke ühendust ühega partneritest:  
<a href="http://www.dynamicspartners.ee/" target="_blank">www.dynamicspartners.ee</a>
