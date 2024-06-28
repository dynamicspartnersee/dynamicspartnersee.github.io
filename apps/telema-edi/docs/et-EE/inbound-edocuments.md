---
---
# Sissetulevad e-dokumendid

## Kuidas vastuvõtta e-dokumente
Avage loend  **Sissetulevad e-dokumendid** ja käivitage toiming  **Võta dokumendid**. Uued dokumendid laetakse alla ja salvestatakse loendisse **Sissetulevad e-dokumendid**.

## Salvestage e-dokument BC dokumendiks
Avage loend **Sissetulevad e-dokumendid**. Näete e-dokumentide loendit, mis pole veel BC dokumendiks salvestatud.

Käivitage toiming  **Salvesta e-dokumendid BC-i**.

Valitud kirjet pakutakse toimingu vaikefiltriks. Kõigi vastuvõetud e-dokumentide salvestamiseks eemaldage filter.

Kui e-dokumendi salvestamine õnnestub, väskendatakse  **Käsitlemise staatus** väärtuseks  **Salvestatud BC-i**  ja e-dokument viiakse **Käsitletud sissetulevad e-dokumendid** juurde.

Kui e-dokumendi salvestamine ebaõnnestub, värskendatakse **Käsitlemise staatus**  olekuks  **Viga** ja **Käsitlemise viga** sisaldab tõrketeadet (esimesed 250 sümbolit).

Kui valite suvandi **Peatu vea korral**, peatatakse toiming esimese tõrke korral ja kuvatakse üksikasjalik tõrketeade.

Tüüpilised vead võivad olla järgmised:
- E-dokument sisaldab tundmatut partnerit
- E-dokument sisaldab tundmatut kaupa

Kui ilmnevad probleemid e-dokumentidega, võite kasutada toimingut  **Vaata dokumendi XML-i** mis võimaldab dokumendi avada (veebibrauseris), salvestada ja kontrollida dokumendi sisu.

Kui e-dokumendi probleemi ei saa lahendada, võite e-dokumendi edasise töötlemise tühistada toiminguga  **Tühista dokument.**

Kui on vaja töödelda (salvestada BC-i dokumenti) käsitsi parandatud XML-failiga, kasutage toimingut **Loo dokument XML-st**. Selle toiminguga luuakse antud XML-faili põhjal uus e-dokument.


## Kuidas automatiseerida e-dokumentide vastuvõtmine ja salvestamine

EDI tööde automatiseerimiseks kasutatakse **Tööjärjekorra** funktsionaalsust.

Avage  **Tööjärjekorra kanded** ning looge tööd:
- **Aruanne 24007801 Võta e-dokumendid kanalilt** e-dokumentide allalaadimisteks operaatori serverist. Määrake operaator töö kaardil aruande päringuaknas.
- **Aruanne 24007803 Salvesta e-dokumendid BC-i**  allalaaditud e-dokumentide automaatseks salvestamiseks BC-i dokumentidesse.

Seadistage tööde ajakava  **Korduvus**  kiirkaardil.

Juhuks kui e-dokumentide töötlemisel esineb tõrkeid, saate seadistada teavituste meiliaadressid **EDI seadistus** lehel väljal **Käsitlemisvigade e-meil**.