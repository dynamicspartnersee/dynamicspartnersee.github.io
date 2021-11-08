---
---
# Eesti intrastat aruandlus - kasutusjuhend
Laiendus lisab Dynamics 365 Business Central intrastat funktsionaalsusele Eesti nõuded ja failiformaadi.

Business Central'i intrastat funktsionaalsuse üldist juhendit saate lugeda siit:  
<a href="https://docs.microsoft.com/en-US/dynamics365/business-central/finance-how-setup-report-intrastat" target="_blank">Set Up and Report Intrastat</a>

## Intrastati seadistus
Intrastati aruannete nõutud detailsus on Eestis ettevõteti erinev.

Nõutud detailsusastme määramiseks avage **Intrastati seadistus** ning määrake **Eesti Intrastat** vahelehel vastavalt **Ostu kohustuslikud väljad** ja **Müügi kohustuslikud väljad**:

Väärtus | Kirjeldus
-- | --
Ei ole kasutuses | Intrastati väljade täitmist ei nõuta.
Baasnõuded | "Tehingu liik", "Nomenklatuuri nr.", "Päritoluriigi tähis", "Netokaal" on nõutud.
Täiendavad nõuded | Baasnõuded + "Transpordiviis", "Lahetusviisi tähis", "Sisenemis- /väljumispunkt" on nõutud.

Kontrollige, et **Formaat seadistatud** väärtus on 'Jah'. Klikkides väljal näete formaadi konfiguratsioonikirjet.  
_See võimaldab luua Eesti nõuetele vastava Intrastati faili._  

## Nomenklatuurinumbrite (tariifide) ja täiendava mõõtühiku seadistus
Lisaks kaalule tuleb Eestis mõnede nomenklatuurinumbrite puhul esitada ka kogus täiendavas mõõtühikus.

Seadistamiseks avage **Nomenklatuurinumbrid** ning täitke **Täiendava mõõtühiku tähis** ning märkige **Täiendavad ühikud**, kui need on nõutud.
  
Kaupadel, mis kuuluvad antud nomenklatuurinumbri alla, peab sama mõõtühik olema seadistatud ka **Kauba mõõtühikute** all.

Selliste kaupade puhul täidetakse aruande koostamisel **Intrastat žurnaali** real lisaveerud **Täiendava mõõtühiku tähis** ja **Täiendava mõõtühiku kogus**, kusjuures Täiendava mõõtühiku tähiseks määratakse vastav Rahvusvaheline standardkood Mõõtühikute tabelist.

## Aruande koostamine intrastat žurnaalis
Kui intrastati žurnaali töölehel on määratud "Statistika periood" (nt 2021.a. dets. puhul 2112) ning puudub linnuke Esitatud, siis saab Intrastati žurnaalis käivitada tegevuse **Soovita ridu**, mis täidab žurnaali toimunud tehingute infoga.  

Tegevus **Loo fail** omakorda käivitab intrastati XML formaadis aruandefaili loomise.
Väljundfaili saab esitada <a href="https://estat.stat.ee/" target="_blank">estat</a> keskkonnas.

***

Lisainformatsiooni saamiseks pöördu partneri poole:   
<a href="http://www.dynamicspartners.ee/" target="_blank">www.dynamicspartners.ee</a>
