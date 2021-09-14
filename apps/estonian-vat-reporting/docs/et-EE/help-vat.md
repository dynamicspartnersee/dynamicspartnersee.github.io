---
---
# Eesti käibemaksu aruanne - kasutusjuhend
Antud funktsionaalsus võimaldab teil koguda vajalikke andmeid käibedeklaratsiooni (vorm KMD) ja deklaratsiooni lisa (vorm KMD INF) jaoks ning esitada need XML-failivormingus.

## Käibedeklaratsiooni seadistamine
Lehel **KM väljavõtted** saate seadistada Käibedeklaratsiooni (KMD). Seal peate määratlema seosed KM väljavõtte ja KMD lahtri nr. vahel.

Avage leht **KM väljavõtted** ja muutke väljavõtet mida soovite KMD aruandluseks kasutada.  
KM väljavõtte rea jõudmiseks KMD-sse tuleb sisestada väljale **Lahtri nr.** vastav käibedeklaratsiooni rea number.  
Kui lahkute välja või rea pealt, näete deklaratsiooni rea kirjeldust väljal **Lahtri kirjeldus**.  
Nõuanne: klõpsates väljal **Lahtri kirjeldus** avanevad kõik käibemaksu aruande read mida kasutada saate.
  
  
### Sõiduautode arv
Avage **KM aruande seadistus** ja lisage sõiduautode arvuline info vahekaardi **Eesti KM aruanne** väljadele:  
* Ettevõtluses (100%) kasutatavate sõiduautode arv
* Osaliselt ettevõtluses kasutatavate sõiduautode arv  
  
Kui sõiduautode arv muutub, siis tuleb enne vastava kuu käibedeklaratsiooni XML faili koostamist andmed ülalolevatel väljadel vastavalt muuta.
  
  
## Kuidas koguda andmeid käibemaksuaruande lisa jaoks
Avage **KM aruande seadistus** ja vahekaardil **Eesti KM aruanne** seadistage järgmised väljad:
* Esitatav tehingupartner - valige, milliseid osapooli deklaratsioonis kasutatakse:
    * *Makse saaja hankija/Maksja klient*
    * *Müüja hankija/Ostja klient*
    * *Müüja hankija/Ostja klient (ainult KM reg. nr. olemasolul)* - selle valikuga kasutatakse Müüja hankija/Ostja klient juhul kui neil on **KM reg. nr.**, vastasel juhul kasutatakse Makse saaja hankijat/Maksja klienti.
* Piirmäära summa - sisestage Käibemaksuseaduses sätestatud piirmäär (üldjuhul 1000).   
 
Andmed KM aruande lisa jaoks kogutakse **KM kanded** loendist.  
Õigete andmete kogumiseks vajalike tingimuste seadistamiseks avage **KM konteerimise seadistus**.  
Iga käibemaksu konteeringurühma kombinatsiooni jaoks saate määratleda, kas selle kombinatsiooniga konteeritud tehing tuleb esitada või mitte, ning seadistada vajalikud eripärad.

Deklareeritavate ja mitte deklareeritavate tehingute automaatseks eraldamiseks tuleb tehingud konteerida erineva KM konteeringurühma kombinatsiooniga.  
Tehingud, mida tuleb kirjeldada eranditena, tuleb konteerida ka eraldi KM konteeringurühma kombinatsiooniga (nt Metalli ost-müük või konfidentsiaalsed tehingud).  

Näited:
1. Tehingud ettevõtetega tuleb deklareerida ja tehinguid eraisikutega ei pea deklareerima. Seetõttu peaksid eraisikutest kliendid ja hankijad olema loodud eraldi **KM äri konteeringurühm** väärtusega (näiteks *MITTE KM KOHUSLANE*).  
2. Kui arve(d) esitatakse ametialaste teenuste eest, mida seaduse ees käsitletakse kui konfidentsiaalseid, siis neid tehinguid ei pea deklareerima ja nende teenuste müügi konteerimiseks peaks olema eraldi **KM toote konteeringurühm**.

Märkige linnuke **KMD INF-il ei deklareerida** nendele ridadele **KM konteerimise seadistuses**, mille tehinguid ei pea INF-il deklareerima.  
Ridadele, kus **KM %** on null, ei pea te **KM konteerimise seadistuses** linnukest panema - need tehingud välistatakse automaatselt.

Muutke **KM konteerimise seadistuses** neid ridasid millele te tahate seada erisusi.  
Valige erisuse kood väljal **KMD erisus müügil** või **KMD erisus ostul**.  
Erisust '03' ei pea, ega saagi lisada - see erisus lisatakse automaatselt, kui müügiarvel on ridu nii käibemaksuga kui ilma.

## Kuidas luua käibedeklaratsiooni
Avage **KM tagastused (KMD)**, looge uus aruanne, määrake **Nr.** ja valige **Versioon** 'EST'.

### Andmete saamine
Andmete saamiseks aruandesse käivitage toiming **Soovita ridu**, valides seejärel kasutatav KM aruanne ja aruande periood.

Funktsioon täidab KM deklaratsiooni aruande ridadel andmed (kui olete seadistanud **Käibedeklaratsiooni seadistamine** jaotistes kirjeldatud seosed) ja INF lisad all väljad **INF-A read** ja **INF-B read**.

**INF-A read** ja **INF-B read** ülevaatamiseks, klõpsake rea väärtusel.

Kui tahate näha mõne müügi- või ostukande detaile (nt algdokumenti), võite kasutada funktsiooni **Navigeeri**.  
Vajadusel saate manuaalselt lisada andmeid.  

### Registreerimisnumbrite kontrollimine ja täitmine
Tehingupartneri nime kasutatakse deklaratsioonil, kui tehingupartneri registreerimisnumber puudub.  
Võimalike tuvastamisprobleemide vältimiseks (nimi BC-s erineb veidi maksuameti andmebaasis olevast nimest) on soovitatav täita registreerimisnumbrid BC-s (kliendi/hankija kaardil).  
Puuduvate registreerimisnumbritega tehingupartnerite loendi vaatamiseks klõpsake vastavalt lehele nupul **Reg.numbrita kliendid** või **Reg.numbrita hankijad**.

Puuduvate registreerimisnumbrite automaatseks täitmiseks võite mõlema lisaga kasutada funktsiooni **Uuenda andmed äriregistrist**.  
Pärast uuenduse käivitamist, sisaldab nimekiri neid tehinguparntereid keda ei leitud äriregistrist.  
Muutke neid kliente/hankijaid ükshaaval kasutades funktsiooni **Päri äriregistrist** ja määrates otsitava ettevõtte nime.

## Deklaratsiooni esitamiseks XML-faili loomine
Märkige linnuke **Esita kõik tehingud**, kui soovite lisada nende tehingupartnerite arveid, kelle tehingute kogusumma jääb alla **KM aruande seadistus** lehel määratud piirmäära (üldjuhul 1000 €).

Aruande XML-faili salvestamiseks klõpsake **Koosta** ja OK nupule vajutades saate faili salvestada.  
Laadige fail üles ja esitage E-maksuametis.

---
## Business Centrali konteeringute nõuded:
1. Konteeritud KM kanded on kohustuslikud kuna KM aruande lisade andmed põhinevad KM kannetel. Nõuet 1 toetab nõuete 2 ja 3 järgimine.
2. Tehingud tuleb konteerida kliendi ja hankija registreid kasutades. Kliendi ja hankija andmed registris peavad vastama nende tehingupartnerite tegelikule ettevõtteteabele.
3. Tehingud tuleb konteerida arve või kreeditarvena või peažurnaali kandena, kui dokumendi tüübiks on määratud arve või kreeditarve.
4. Deklareeritavad / deklareerimata tehingupartnerid tuleb luua erinevate KM äri konteeringurühmadega. See võimaldab teil KM konteerimise seadistuses määratleda käibemaksu konteeringurühmade kombinatsioonid, mis tuleb deklareeritud andmetest välja jätta.
5. Deklareeritavad / deklareerimata kaubad / teenused tuleb seadistada koos erinevate KM toote konteerigurühmadega. See võimaldab teil KM konteerimise seadistuses määratleda käibemaksu konteeringurühmade kombinatsioonid, mis tuleb deklareeritud andmetest välja jätta.
6. Aruandvate isikute esitatud kuludokumendid tuleks sisestada ostuarvetena.
7. Ettemaksude deklareerimiseks peate konteerima ja väljastama ettemaksuarve(d), kuna käibedeklaratsiooni lisa põhineb arvete andmetel, mitte maksetel.
8. Et lisada ettemaksuarve deklaratsiooni alles pärast selle tasumist, peate kasutama Pearaamatu seadistuse määratlust Ettem. realiseerimata KM.
