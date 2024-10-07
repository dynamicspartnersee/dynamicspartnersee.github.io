---
---
# Eesti intrastat aruandlus - kasutusjuhend
Laiendus lisab Dynamics 365 Business Central intrastat funktsionaalsusele täiendavad Eesti nõuded ja aruande XML failiformaadi.

Business Central'i intrastat funktsionaalsuse üldist juhendit saate lugeda siit:  
<a href="https://docs.microsoft.com/en-US/dynamics365/business-central/finance-how-setup-report-intrastat" target="_blank">Set up Intrastat reporting</a>

## Intrastati seadistus
Intrastati aruannete nõutud detailsus on Eestis ettevõteti erinev.

Nõutud detailsusastme määramiseks avage **Intrastati aruande seadistus** ning määrake **Eesti Intrastat** vahelehel vastavalt **Ostu kohustuslikud väljad** ja **Müügi kohustuslikud väljad**:

Väärtus | Kirjeldus
-- | --
Ei ole kasutuses | Intrastati väljade täitmist ei nõuta.
Baasnõuded | "Nomenklatuuri nr.", "Päritoluriigi tähis", "Netokaal" on nõutud kaubakaardil ning "Tehingu liik" dokumendil.
Täiendavad nõuded | Baasnõuded + "Sisenemis- /väljumispunkt" on dokumendil nõutud.<br>_(Kuni 31.12.2021 konteerimiskuupäevaga dokumentidel on nõutud veel "Transpordiviis" ja  "Lahetusviisi tähis)._

Kontrollige, et **Formaat seadistatud** väärtus on 'Jah'.  
Vajutades väljale näete KM aruande konfiguratsioonikirjet liigile "Intrastati aruanne".  
_(Content Codeunit ID peaks olema 24007763 ning Validate Codeunit ID olema 24007762)._  
_See on eelduseks, et oleks võimalik luua Eesti nõuetele vastav Intrastati XML formaadis aruande fail._  

## Nomenklatuurinumbrite (tariifide) ja täiendava mõõtühiku seadistus
Lisaks kaalule tuleb Eestis mõnede nomenklatuurinumbrite puhul esitada ka kogus täiendavas mõõtühikus.

Seadistamiseks avage **Nomenklatuurinumbrid** ning märkige **Täiendavad ühikud**, kui nõutud.
_(Varasemalt (kuni BC24) tuli täita seal veel Täiendava mõõtühiku tähis, mis alates BC25 on leitav kauba kaardilt)._
  
Kaupadel, mis kuuluvad antud nomenklatuurinumbri alla, peab sama mõõtühik olema seadistatud ka **Kauba mõõtühikute** all.

Selliste kaupade puhul täidetakse aruande koostamisel rea lisaveerud **Täiendava mõõtühiku tähis** ja **Täiendava mõõtühiku kogus**.  
NB! Täiendava mõõtühiku tähiseks määratakse XML faili vastav **Rahvusvaheline standardkood** Mõõtühikute tabelist _(kui seal väärtus puudub, siis lisatakse faili real kuvatav väärtus)_.

## Aruande koostamine
Kui intrastati aruandel (_varasemalt Intrastati žurnaali töölehel_) on määratud "Statistika periood" (nt 2024.a. dets. puhul 2412) ning aruanne on Avatud olekus (_varasemalt žurnaalis pidi puuduma linnuke Esitatud_), siis saab Intrastati žurnaalis käivitada tegevuse **Soovita ridu**, mis täidab read toimunud tehingute infoga.  

Tegevus **Loo fail** omakorda käivitab intrastati XML formaadis aruandefaili loomise.
Väljundfaili saab esitada <a href="https://estat.stat.ee/" target="_blank">estat</a> keskkonnas.

***

Lisainformatsiooni saamiseks pöördu partneri poole:  
<a href="https://dynamicspartnersee.github.io/docs/en-us/contacts" target="_blank">Estonian Dynamics Partners</a>
