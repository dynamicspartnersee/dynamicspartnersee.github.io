
---
---
# Väljaminevad e-dokumendid

## Kuidas luua BC-dokumendist e-dokument 
Üldiselt ei ole vaja e-dokumente käsitsi luua. Soovitame seadistada e-dokumentide konteerimisel loomise **Telema EDI seadustus** all.

E-dokumentide käsitsi loomiseks avage **Väljaminevad e-dokumendid** ja valige **Toimingud** vahekaardil **Loo dokument BC-st** sobiv toiming.

Filtreerige dokumendid, mille soovite e-dokumentideks teisendada, ja vajutage **OK.** E-dokumendid luuakse ainult neile klientidele, kelle seadistus võimaldab neile e-dokumentide saatmist.

Kui mõne valitud BC dokumendi jaoks on olemas tühistamata e-dokument, küsitakse uue e-dokumendi loomise kinnitust.

## Kuidas e-dokumente Telemale saata
Avage  **Väljaminevad e-dokumendid**. Seal on nimekiri e-dokumentidest mis on BC dokumentidest loodud aga mida ei ole veel Telemasse saadetud.

Käivita toiming **Saada dokument Telemasse**. Vaikimisi on valitud rida filtris. Et saata välja kõik e-dokumendid, eemalda filter.

Kui e-dokumendi saatmine on edukas, muudetakse **Käsitlemise staatus** välja väärtuseks **Saadetud Telemasse** ja e-dokument liigub lehele **Käsitletud väljaminevad e-dokumendid**.


Kui e-dokumendi saatmine ebaõnnestub, värskendatakse **Käsitlemise staatus** olekuks **Viga** ja **Käsitlemise viga** sisaldab tõrketeadet (esimesed 250 sümbolit).

Kui valite suvandi **Peatu vea korral**, peatatakse toiming esimese tõrke korral ja kuvatakse üksikasjalik tõrketeade.

Tüüpilised vea põhjused võivad olla järgmised:
- E-dokument ei vasta formaadinõuetele
- E-dokument ei vasta vastuvõtja seatud nõuetele

Kui ilmnevad probleemid e-dokumentidega, võite kasutada toimingut **Vaata dokumendi XML-i**, mis võimaldab dokumendi avada (veebibrauseris), salvestada ja kontrollida dokumendi sisu.

Kui e-dokumendi probleemi ei saa lahendada, võite e-dokumendi edasise töötlemise tühistada toiminguga **Tühista dokument.**

Kui on vajadus töödelda (saata Telemasse) käsitsi parandatud XML-failiga, kasutage toimingut **Loo dokument XML-st**. Selle toiminguga luuakse antud XML-faili põhjal uus e-dokument.

**Väljaminev e-dokument** võidakse tagasilükata Telema serveri poolt kui ta on duplikaat. Antud vea põhjuseid võib olla kaks:

- See on tõesti duplikaat (sama saatja dokument, sama dokumendi tüübi- ja numbriga samal aastal). See võib juhtuda kui kasutaja loob dokumendi käsitsi.
- Dokument saadeti Telema serverisse, aga vastuvõtu kinnitus ei jõudnud tagasi BC-i ja dokumendi **Käsitlemise staatus** ei ole **Saadetud Telemasse**.

Mõlemal juhul peaks kasutaja tühistama edasised käsitlemise katsed, kasutades toimingut **Tühista dokument.**

## Kuidas automatiseerida e-dokumentide saatmist BC-ga
Telema EDI-tööde automatiseerimiseks tuleb BC-i rakendusserver seadistada ja käivitada funktsioon **Tööjärjekord**.

Avage  **Tööjärjekorra kanded**. Looge uus tööjärjekorra kanne **Aruanne 24007802 Saada e-dokumendid**. 

Pange paika tööde ajakava  **Korduvus**  kiirkaardil.
