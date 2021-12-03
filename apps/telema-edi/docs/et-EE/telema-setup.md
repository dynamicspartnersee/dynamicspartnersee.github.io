---
---
# EDI seadistamine

 - [Kuidas seadistada ühendus Telema serveriga](#kuidas-seadistada-ühendus-telema-serveriga)
 - [Kuidas seadistada ühendus Edisofti serveriga](#kuidas-seadistada-ühendus-edisofti-serveriga)
 - [Kuidas seadistada ühendus kahe Business Centrali vahel ilma operaatorita](#kuidas-seadistada-ühendus-kahe-Business-Centrali-vahel-ilma-operaatorita)
 
## Kuidas seadistada ühendus Telema serveriga
Avage **Telema EDI seadistus** ning kiirkaart  **Ühendus.**  
Palun küsige järgnevalt täidetav informatsioon Telemast:

| Väli: |
| - |
| **API URL** |
| **API kanali id** |
| **API võti** |

Peale kiirkaardi **Ühendus**  täitmist kasutage funktsiooni **Testi ühendust** kindlustamaks, et ühendus Telemaga on loodud.

## Kuidas seadistada ühendus Edisofti serveriga
Avage **Telema EDI seadistus** ning kiirkaart  **Ühendus.**  
Palun küsige järgnevalt täidetav informatsioon Edisoftist:

| Väli: |
| - |
| **Edisoft URL** |
| **Edisoft kasutaja** |
| **Edisoft võti** |

Peale kiirkaardi **Ühendus**  täitmist kasutage funktsiooni **Testi Edisoft ühendust** kindlustamaks, et ühendus Edisofti serveriga on loodud.

## Kuidas seadistada ühendus kahe Business Centrali vahel ilma operaatorita

Dokumendivahetuseks kasutatakse Business Central SOAP veebiteenuseid, mis peavad olema vastuvõtja poolel aktiveeritud.
### Dokumentide saatmine
Dokumentide saatmiseks avage **Kliendid** loendist kliendi kaart ning kiirkaardil **Telema EDI** valige **Saatmise viis** *BC e-dokumendi veebiteenus*. 
Palun küsige järgnevalt täidetav informatsioon ettevõttelt kelle Business Central-i soovite dokumente otse saata:

| Väli: |
| - |
| **E-dokument veebiteenuse URL** |
| **E-document veebiteenuse kasutaja** |
| **E-dokument veebiteenuse parool** |

### Dokumentide vastuvõtmine
Dokumentide vastuvõtmiseks peate edastama saatjale järgnevad andmed: veebiteenuse URLi, kasutaja ning parooli.

Avage **Telema EDI seadistus** ning aktiveerige **Avalda e-document veebiteenus**.

Seejärel avage **Veebiteenused** ning valige objekti **TED E-Document Web Service** realt **SOAP URL**. See ongi **E-dokument veebiteenuse URL**.  

Seejärel avage **Kasutajad** ning looge saatja ettevõttele kasutaja. Määrake **Kasutajanimi**, **Veebiteenuse juurdepääsu võti** ning vajalikud õigustekomplektid. 
  
Edastage andmed saatja ettevõttele.


## Kuidas e-dokumente saata ja vastu võtta

Vaata juhendit:  
[Sissetulevad e-dokumendid](inbound-edocuments)  
[Väljaminevad e-dokumendid](outbound-edocuments)
