---
---
# Eesti pakendiaktsiis - Kasutusjuhend

Käesolev äpp lisab Dynamics 365 Business Central-i pakendiaktsiisi funktsionaalsuse.

Ettevõtjad peavad esitama kord kvartalis pakendi aktsiisideklaratsiooni. Antud Eesti lokalisatsiooni funktsionaalsus võimaldab NAV-is koostada aktsiisideklaratsiooni esitamise jaoks vajaliku andmete komplekti. Funktsionaalsus ei sisalda aktsiisideklaratsiooni aruande väljatrükki.

Viited pakendiseadusele:

Pakendiseadus: [https://www.riigiteataja.ee/akt/104042012006?leiaKehtiv](https://www.riigiteataja.ee/akt/104042012006?leiaKehtiv)  
Pakendiaktsiisi seadus: [https://www.riigiteataja.ee/akt/13074692?leiaKehtiv](https://www.riigiteataja.ee/akt/13074692?leiaKehtiv)

# Seadistamine

## Üldseadistus

Pakendimaterjalide seadistused leiab sisestades otsingusse **Pakendimaterjalid**

## Pakendiaktsiisi seadistused kaupadel

### Kaubakaart

Kiirkaardil **Varud** valitakse väärtus väljale **Pakendi aktsiisiarvutus**. Välja võimalikud väärtused on järgmised:

Väärtus | Selgitus
-- | --
Ei arvutata | Kaupa ei kaasata pakendi aktsiisiarvutustesse.
Kasuta kande mõõtühikut | Pakendid peavad olema seadistatud mõõtühikute kohta, mida kasutatakse tehingute tegemisel.
Kasuta alusmõõtühikut | Pakendid peavad olema seadistatud ainult alusmõõtühikule. Teistes mõõtühikutes tehtud tehingud teisendatakse pakendikoguste arvutamiseks alusmõõtühikusse.

### Kauba mõõtühiku sidumine pakkematerjalidega

Pakendiaktsiisi arvutuseks peab kauba mõõtühiku(d) siduma pakkematerjalidega. Selleks vajutatakse **Kaubakaardi** lintmenüü **Toimingud** -> **Kaup** all nuppu **Pakendimaterjalid**. Avaneval lehel seadistatakse kauba mõõtühikuga (või erinevate mõõtühikutega) seotud pakkematerjalide tähised ja kogused.

# Kasutamine

Pakendiaktsiisi aruande koostamise leht **Pakendi aktsiisdeklaratsioonid** käivitatakse sisestades otsingusse **Pakendi aktsiisideklaratsioonid** Tegevused: **Uus** - luuakse uus pakendi aktsiisideklaratsioon. **Redigeeri** - võimaldab muuta märgitud ja esitamata pakendi aktsiisideklaratsiooni. **Vaata** - kuvab märgitud pakendi aktsiisideklaratsiooni. **Kustuta** - kustutab märgitud pakendi aktsiisideklaratsiooni

Uue pakendi aktsiisideklaratsiooni loomisel täidetakse lehel järgmised väljad.

Väli | Selgitus
-- | --
Nr. | Väljale sisestatakse pakendi aktsiisideklaratsiooni number.
Kirjeldus | Pakendi aktsiisideklaratsiooni kirjeldus.
Perioodi algus | Määrab perioodi alguse.
Perioodi lõpp | Määrab perioodi lõpu.
Viimane muutmise aeg | Pakendi aktsiisideklaratsiooni viimase muutmise aeg.
Viimane muutja | Pakendi aktsiisideklaratsiooni viimase muutaja kasutajanimi.
Esitatud | Viitab, et pakendi aktsiisideklaratsioon on esitatud. Muudab väljad (v.a **Esitatud**) mittemuudetavaks.

Pakendi aktsiisideklaratsiooni arvutamise tegevus käivitatakse lehel **Pakendi aktsiisdeklaratsioon** nupust **Arvuta read**. Avaneval päringuvormil määratakse filtrid (need on vaikimisi eeltäidetud) ja vajutatakse **OK**.

Arvutatakse pakendiaktsiisi kogused filtritega määratud tingimustel.

Tegevuse **Arvuta read** päringuvormi filtrid on vaikimisi eeltäidetud järgmiste filtritega.
-   Kande liik = müük
-   Riigi/regiooni tähis = riigi/regiooni tähis ettevõtte andmetest
-   Konteerimiskuupäev = filter aruande päise järgi

Pakendi aktsiisideklaratsioon täidetakse järgmise loogikaga:

-   Tuuakse kõik kirjed pakendite materjalide tabelist **„Pakendimaterjalid”** ehk kõik seadistatud pakendimaterjalid.
-   Kogused vastavalt kauba kaardi väljale **Pakendi aktsiisiarvutus** ja kaubale seadistatud pakendimaterjalidele.
-   Pakendikandeid luuakse kaubakande kohta nii palju, kui on erinevaid pakendeid kauba erinevatele mõõtühikutele seadistatud.
-   Juhul kui aruandel on juba ridu, siis tegevuse **Arvuta read** teistkordsel käivitamisel kuvatakse kasutajale hoiatus, mille aktsepteerimisel arvutatakse read uuesti.

Valmis genereeritud aruande ridu käsitsi lisada ja kustutada ei saa. Kasutaja saab lisada väärtused järgmistesse veergudesse:
-   **Ümbert. tegelik kogus (KG)**
-   **Ringlussev. tegelik kogus (KG)**
-   **Taask. tegelik kogus (KG)**

Klikkides veeru **Pakendimaterjali kogus (KG)** väärtusele, avatakse leht **Pakendi aktsiisideklaratsiooni kanded**, kus kuvatakse detailsed kanded, millest arvutatud kogus koosneb.

Kui aruanne on esitatud, siis märgitakse selle päises väli **Esitatud**. Kui väli on märgitud, siis:
-   ei lubata aruande päise välju muuta (v.a väli **Esitatud**, mis võimaldab aruande uuesti avada) ja aruannet kustutada;
-   ei lubata aruande ridu muuta ja käivitada uuesti tegevust **Arvuta read**.

----------

Täpsema info saamiseks, palun võtke ühendust ühega partneritest:  
[http://www.dynamicspartners.ee](http://www.dynamicspartners.ee/)