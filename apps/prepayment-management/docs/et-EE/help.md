---
---
# Ettemaksude haldus - Kasutusjuhend

Kliendipõhise ja/või hankijapõhise ettemaksu funktsionaalsus võimaldab BC-s järgmist:

-   Väljastada ettemaksunõuet ehk ettemaksuarvet.
-   Käibemaksuseadusest tulenevalt käsitleda klientide ettemaksu kui käivet ning arvestada sellelt käibemaksu.
-   Kliendi/Hankija ettemaksude üle arvestust pidada ning neid kasutada (maha arvata) kliendile/hankijale esitatavatel põhiarvetel.
-   Kliendipõhise ettemaksu funktsionaalsus toetab ka standardis olevat ettemaksu realiseerimata käibemaksu lahendust.
-   Siduda ettemakseid projektimooduliga.

## **Seadistamine**

Funktsionaalsuse kasutamiseks on vajalikud standardse ettemaksu seadistused. **Üld. konteeringu seadistuses** peab olema määratud **Müügi ettemaksu konto**/**Ostu ettemaksu konto**.

### _**Ettemaksu realiseerimata käibemaksu seadistus**_

Kui soovitakse, et ettemaksuarvete käibemaks läheks KM deklaratsiooni alles seejärel kui arve on tasutud, siis tuleb teha järgenvad seadistused.

Esimese sammuna tuleb **Pearaamatu seadistuses** märkida linnuke _**Ettem. realiseerimata KM**_.

Teiseks tuleb **KM konteerimise seadistuses** soovitud _**KM äri konteeringurühma**_ ja _**KM toote konteeringurühma**_ kombinatsioonidel ära määrata _**Realiseerimata KM liik**_ (näiteks _Protsent_) ning lisaks tuleb määrata ka _**Real-mata müügi KM konto**_.

## **Kasutamine**

### **Kliendipõhise ettemaksu registreerimine ja ettemaksuarve väljastamine**

BC-s registreeritakse kliendipõhine ettemaks müügiarve kaudu ning hankijapõhine ettemaks ostuarve kaudu. Selleks luuakse kliendile müügiarve või hankijale ostuarve, mille reale valitakse konto, mis esineb üld. konteeringu seadistuses veerus **Müügi ettemaksu konto** või hankija puhul **Ostu ettemaksu konto**.

**Projektiga setoud** etteamksu arve loomine saab, saranselt projekti müügiarvetega, alguse Projekti plaanimisrealt ning sellele rakendub eelpoolmainitu. Projektipõhise etteamksu arve korral lisatakse **Ettemaksuandmikusse** ka **Projekti nr.** ning **Projekti ülesande nr.**

#### **_Tähtis_**
----------
_Ettemaksu arve koostamisel märgitakse taustal väli **Kliendipõhine ettemaksuarve**/**Hankijapõhine ettemaksuarve** konteerimsiel automaatselt (välja väärtus kandub üle konteeritud arvele või konteeritud kreeditarvele)._

_Sellest tulenevalt rakendub järgnev:_

-   _Arvete konteerimisel kasutatakse konteeritud ettemaksu arvete/kreeditarvete numbriseeriaid._
-   _Sellise arvega saab müüa/osta ainult ettemaksu kontodelt, mis on määratud üld. konteeringu seadistuses. Kontroll toimub konteerimisel._

----------

Kui müügiarve reale valitakse müügi ettemaksu konto (_ja ostuarve real vastavalt ostu ettemaksu konto_), siis loob BC automaatselt ettemaksukanded ettemaksuandmikusse ja konteeritud arve välja trükkimisel (kas nupust Konteeri ja prindi või konteeritud arvete loendist) prinditakse välja ettemaksuarve.

### **Kliendipõhiste ja/või hankijapõhiste ettemaksukannete kontrollimine**

Ettemaksukandeid saab kontrollida kahel viisil.

-   Klientide/hankijate loendis või kliendi/hankija kaardil olevas kiirinfoaknas **Ostja-kliendi müügi ajalugu**/**Müüja-hankija ajalugu**, kus avatud ettemaksu kannete arv kuvatakse väljal **Avatud ettemaksude arv**
-   Arve, -tellimuse või kreeditarve lehel olevas kiirinfoaknas **Ostja-kliendi müügi ajalugu**/**Müüja-hankija ajalugu**, kus avatud ettemaksu kannete arv kuvatakse väljal **Avatud ettemaksude arv**

Numbrit klõpsates avaneb leht, kus kuvatakse kliendi/hankija ettemaksuandmiku kanded

Tähtsamate väljade selgitused:

|Väli | Selgitus|
|- | -|
Summa | Algne ettemaksu summa.
Jääksumma | Kasutamata ettemaksu summa.
Avatud | Märge väljal viitab, et ettemaksukanne on avatud ja seda saab saab kasutada (sel juhul on **Jääksumma** nullist erinev).
Kliendi/Hankija kande nr. | Viide kliendi/hankija andmikukande numbrile, millega seoses loodi kanne ettemaksuandmikusse.
Arve makstud | Viitab, kas ettemaksukande eest on kliendilt laekumine _(hankijale ülekanne)_ tehtud või mitte. Kui see on **Ei**, siis on kliendi/hankija andmikukanne avatud ehk kliendilt/hankijalt pole veel ettemaksu laekumist BC-s registreeritud. **Jah** puhul on kliendi/hankija andmikukanne suletud, mis viitab registreeritud laekumisele/maksele.
|Projekti nr. / Projekti ülesnde nr.| Lisatakse kannetele kui ettemaks on seotud projektiga ehk kui ettemaksu arve on loodud **Projekti plaanimisrealt**.|

#### **_Tähtis_**

----------

_Arvestama peab sellega, et **Ettemaksuandmikus** kuvatavad read, ei ole kliendi ettemaksu laekumised (hankijale ettemaksu tasumised). Seda, kas ettemaks on kliendilt laekunud (hankijale tasutud), kuvab ettemaksukandel välja **Arve makstud** väärtus. Kui see on **Ei**, siis on kliendi/hankija andmikukanne avatud ehk kliendilt/hankijalt pole veel ettemaksu laekumist/tasumist BC-s registreeritud. **Jah** puhul on kliendi/hankija andmikukanne suletud, mis viitab registreeritud laekumisele/maksele._

----------

Kasutades tegevusnuppu **Navigeeri** saab vaadata märgitud ettemaksukandega seotud arvet ja kandeid.

### **Ettemaksu kasutamine**

Kliendi ettemaksu saab kasutada konteerimata müügitellimusel ja -arvel või projekti plaanimisridadel kasutades selleks nuppu **Too kliendipõhine ettemaks**.  
Hankija ettemaksu saab kasutada konteerimata ostutellimusel ja -arvel, kasutades selleks nuppu **Too hankijapõhine ettemaks**.  
Avaneval lehel kuvatakse avatud ja jääksummadega ettemaksukanded, mille seast märgitakse kanne, mida soovitakse kasutada ja vajutatakse nuppu **OK**.

**OK** vajutamisel toimuvad järgmised kontrollid:

-   Kontrollitakse, et kande valuuta vastab dokumendi või projekti valuutale.
-   Kontrollitakse, et kande ettemaksu liik ei oleks **Tellimusepõhine** ehk, et kanne oleks **Kliendipõhine**.

Kandelt kopeeritakse uuele dokumendi reale või projekti plaanimisreale:

-   konto nr.
-   kirjeldus
-   kõik konteeringurühmad
-   müügireal/ostureal/projekti plaanimisreal täidetakse väli **Seotud ettemaksukande number** seotud ettemaksu kande numbriga. Väli on peidetud ja selle infot saab vaadata ainult zuumi kasutades
-   rea koguseks täidetakse miinus üks (-1).
-   juhul kui arve summa käibemaksuga on väiksem kui avatud ettemaks, siis vähendatakse selle järgi arvele toodavat summat.

#### **_Tähtis_**

----------

-   _Müügidokumendile/ostudokumendile/projekti plaanimisreale valitakse ettemaksuridu ükshaaval, st et korraga mitut rida valida ei saa._
-   _Kui ettemaksukandel olevat jääksummat ei soovita korraga kasutada, siis vähendatakse ettemaksurea summat veerus **Ühiku hind KM-ta** / **Ühiku hind**. Sel juhul jääb ettemaksukanne pärast dokumendi konteerimist jääksummaga avatuks._
-   _**NB!**Projektipõhise ettemaksu puhul tuleb seejärel projekti plaanimisrealt luua müügiarve._
-   _Ettemaksureaga müügidokumendi/ostudokumendi konteerimisel kontrollib BC, kas ettemaksuga müügirida/osturida ei ületa ettemaksukande jääksummat. Vea korral kuvatakse kasutajale veateade._
-   _Kui kogu ettemaksusumma kasutati ära, siis pärast müügidokumendi/ostudokumendi konteerimist märgitakse ettemaksukanne suletuks ja seda ei saa enam dokumendile valida._
-   _Kui ettemaksusummast kasutati ainult osa, siis jääb ettemaksukanne avatuks ning kande jääki saab kasutada mõne teise dokumendiga._

----------

### **Ettemaksuarve tühistamine**

Juba konteeritud kliendi- ja/või hankijapõhise ettemaksuarve tühistamine käib läbi kreeditarve. Arve saab luua nullist või kasutada funktsionaalsust **Kopeeri dokument**, samuti võib **Konteeritud arvete** loendis kasutada funktsiooni **Loo parandav kreeditarve**.

Ettemaksu kreeditarve koostamisel märgitakse taustal väli **Kliendipõhine ettemaksuarve**/**Hankijapõhine ettemaksuarve** konteerimisel automaatselt. See määrab, et konteeritud kreeditarve number võetakse seadistusega määratud ettemaksu kreeditarve numbriseeriast.

Kreeditarve reale valitakse üld. konteeringu seadistuses esinev müügi ettemaksu konto (hankijapõhise ettemaksu puhul ostu ettemaksu konto), kogus 1, summa ning väljale **Seotud ettemaksukande nr.** ettemaksukande number, mida soovitakse tühistada.

#### **_Tähtis_**

----------

-   Kreeditarve konteerimisel kontrollitakse, kas väljale **Seotud ettemaksukande nr.** on ettemaksukande number valitud. Kui seda pole tehtud, siis kuvatakse kasutajale konteerimisel veateade.
-   Kui ei soovita kogu ettemaksukannet tühistada, siis vähendatakse kreeditarvel ettemaksurea summat veerus **Ühiku hind KM-ta**. Sel juhul jääb ettemaksukanne pärast dokumendi konteerimist jääksummaga avatuks (jääksummat vähendatakse kreeditsumma võrra).
-   Ettemaksureaga kreeditarve konteerimisel kontrollib BC, kas ettemaksuga rida ei ületa ettemaksukande jääksummat. Vea korral kuvatakse kasutajale veateade.
-   Kui kogu ettemaksusumma tühistati, siis pärast kreeditdokumendi konteerimist märgitakse ettemaksukanne suletuks ja seda ei saa enam dokumendile valida.
-   Kui ettemaksusummast tühistati ainult osa, siis jääb ettemaksukanne avatuks ja kande jääki saab kasutada mõne teise dokumendiga.

----------

### **Kuidas tühistada arvet, millel on kasutatud ettemaksu**

Tühistamine toimub läbi kreeditarve või tagastuskorralduse. Dokumendi saab luua nullist, kasutades funktsionaalsust **Kopeeri dokument** või tagastuskorraldusel tegevust **Too konteeritud dokumendiread ümberpööramiseks**.

Dokumendireale valitakse (kopeeritakse) üld. konteeringurühmade seadistuses määratud müügi ettemaksu konto (hankijapõhise ettemaksu puhul ostu ettemaksu konto) number, kogus -1, summa. Väli **Seotud ettemaksukande nr.** jäetakse tühjaks.

#### **_Märkus_**

----------

-   _Pärast konteerimist luuakse kliendile/hankijale uus ettemaksuandmiku kanne, mida uue dokumendi puhul kasutada._

----------

Täpsema info saamiseks, palun võtke ühendust ühega partneritest:  
<a href="https://dynamicspartnersee.github.io/docs/en-us/contacts" target="_blank">Estonian Dynamics Partners</a>
