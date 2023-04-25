---
---
# Eesti äriregister - Kasutusjuhend

Eesti äriregistri äpp lisab Business Central-i kontakti tabelisse uue välja **Registreerimisnr.** ning võimaldab kasutada **Äriregistri päring** funktsionaalsust kliendi, hankija ja kontakti registris.

## Äriregistri päring

Äriregistri päring võimaldab teha tasuta päringuid e-äriregistri infoteenustest „Ettevõtja rekvisiitide teenus“ ja „E-arve registri teenus“.  

Päringute tegemiseks tuleb sõlmida päringusüsteemide kasutamise leping. Lepingu info: [http://www.rik.ee/et/e-ariregister/lepinguinfo](http://www.rik.ee/et/e-ariregister/lepinguinfo)  

E-äriregistrist päritakse järgmised andmed:

-   Ärinimi
-   Aadress (Tänav, Asula/linn, Maakond, Postiindeks)
-   Registreerimisnumber
-   KM registreerimisnumber
-   Esitatud majandusaasta aruannete viimased kolm aastanumbrit
-   Link ettevõttele äriregistri teabesüsteemis
-   E-arve teenusepakkuja

<br>
<br>

## Kuidas seadistada äriregistri päring

Avage **Äriregistri seadistus** ning seadistage:

-   Äriregistri teenuse URL - sisestage äriregistri veebiteenuse aadress. Näiteks: [https://ariregxmlv6.rik.ee/](https://ariregxmlv6.rik.ee/)
-   Rekvisiitide teenuse kasutajanimi - sisestage oma lepinguline kaustajanimi.
-   Rekvisiitide teenuse parool - sisestage oma lepinguline parool.
-	Vaike riigi/regiooni tähis - valige väärtuseks "EE".
-	Linna info koos linnaosaga - Kui linna info juures ei soovi linnaosa salvestada, siis tuleks mitteaktiivseks muuta.
-   E-arve saatmisprofiil - juhul, kui väljastate e-arveid, valige Dokumendi saatmise profiil, mida soovite määrata neile klientidele, kellel on e-arve vastuvõtu võimekus.


Kui valite **Rakenda vaikeseaded**, siis täidetakse **Äriregistri teenuse URL** Eesti äriregistri leheküljega (https://ariregxmlv6.rik.ee/) ning määratakse automaatselt **Vaike riigi/regiooni tähiseks** Eestile vastav tähis (nt "EE").  
Ühtlasi muudetakse **Riigid/regioonid** tabelis Eesti kirjet nii, et aadressi vorming oleks "Linn+Maakond+Postiindeks". Viimane toob Kliendi/Hankija/Kontakti jms kaartidel nähtavale välja Maakond.  

<br>
<br>

## Kuidas kasutada äriregistri päringut

Äriregistri päringut saab kasutada:

1.  Masspäringu aruandena, mis võrdleb kliendi ja hankija andmeid äriregistriga ning näitab või uuendab allpool nimetatud väljade erinevused. Aruannet saab seadistada ka tööjärjekorra all korduva tööna. Tegevus võrdleb ja uuendab väljad:
    -   Registreerimisnr.
    -   KM reg. nr.
    -   Dokumendi saatmise profiil - võimadab määrata e-arve profiili neile **klientidele**, kes on e-arve registris.
2.  Detailpäringuna uue kliendi/hankija/kontakti loomiseks või olemasoleva kliendi/hankija/kontakti andmete kontrollimiseks ja uuendamiseks.

**Masspäringu** kasutamiseks avage Klientide või Hankijate loend. Soovi korral rakendage filtrid ning käivitage tegevus **Uuenda andmed äriregistrist**.  
Avanevas päriguaknas määrake, kas soovite, et väljund näitab erinevusi või ka uuendab andmed.  
Juhul, kui kliendil või hankijal on Registreerimisnr. täitmata, siis päritakse andmeid nime järgi, millest on eemaldatud enamlevinud õigusliku vormi tähised _(OÜ, AS, UÜ, TÜ, MTÜ, FIE, OSAÜHING, TÄISÜHING, AKTSIASELTS, USALDUSÜHING, KORTERIÜHISTU, TULUNDUSÜHISTU, MITTETULUNDUSÜHING ja FÜÜSILISEST ISIKUST ETTEVÕTJA)_.  
Juhul, kui masspäring mõnda ettevõtet äriregistrist ei leidnud (n. kuna nimekuju erineb) või leidis mitu vastet, siis saate nende puhul kasutada detailpäringut, mis võimaldab otsitavat nime korrigeerida ja tulemuste hulgast õige vaste valida.

**Detailpäringu** kasutamiseks avage Kliendid või Hankijad või Kontaktid, redigeerige mõnda olemasolevat ettevõtet või looge uus, millele määrake **Nr.**.  
Seejärel käivitage tegevus **Päri äriregistrist**, mis avab Äriregistri päringu akna.  
_Juhul kui pärida olemasoleva Kliendi/Hankija/Kontakti infot ja äriregistri kood on kirjel täidetud, siis tehakse päring äriregistri koodi järgi. Selle puudumisel nime järgi._  
NB! Kontaktide puhul saab pärida andmeid äriregistrist vaid juhul kui kontakti **Liik** on "Ettevõte". (Päring ei ole aktiivne kui kontakti liik on "Isik")

## Äriregistri päringu aken

Sisestage ettevõtja **Otsitav nimi** ja/või **Otsitav reg.number**, mille peale teostatakse päring e-äriregistrisse ning kuvatakse leitud tulemused. Vajadusel korrigeerige otsitavat nime või reg.numbrit.

Soovitud tulemuse leidmisel, klikkige ettevõttele.

Akna alumisel paremal osal kuvatakse ettevõtte andmed Business Central-is ning nende kõrval vasakul ettevõtte andmed äriregistris.

Äriregistrist leitud andmete kasutamiseks Business Central-i andmete täitmiseks või uuendamiseks, klikkige soovitud väljade või välja **Vali kõik** järel olevaid nuppe.

Vajadusel saate andmeid redigeerida.  
Andmete salvestamiseks kliendi/hankija/kontakti kaardile klikkige **OK**.

----------

<br>

Lisainformatsiooni saamiseks pöördu partneri poole:  
<a href="https://dynamicspartnersee.github.io/docs/en-us/contacts" target="_blank">Estonian Dynamics Partners</a>
