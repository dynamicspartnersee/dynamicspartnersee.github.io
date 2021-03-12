---
---
# Eesti intrastat aruandlus - kasutusjuhend
Laiendus lisab Dynamics 365 Business Central intrastat funktsionaalsusele Eesti nõuded ja failiformaadi.

Business Central'i intrastat funktsionaalsuse üldist juhendit saate lugeda siit:
[https://docs.microsoft.com/en-US/dynamics365/business-central/finance-how-setup-report-intrastat](https://docs.microsoft.com/en-US/dynamics365/business-central/finance-how-setup-report-intrastat)

## Intrastati seadistus
Intrastati aruannete nõutud detailsus on Eestis ettevõteti erinev.

Nõutud detailsusastme määramiseks avage **Intrastati seadistus** ning määrake **Eesti Intrastat** vahelehel vastavalt **Ostu kohustuslikud väljad** ja **Müügi kohustuslikud väljad**:

Väärtus | Kirjeldus
-- | --
Ei ole kasutuses | Intrastati väljade täitmist ei nõuta.
Baasnõuded | "Tehingu liik", "Tariifi nr.", "Päritoluriigi tähis", "Netokaal" on nõutud.
Täiendavad nõuded | Baasnõuded + "Transpordiviis", "Lahetusviisi tähis", "Sisenemis- /väljumispunkt" on nõutud.

## Tariifinumbrite (nomenklatuurinumbrid) seadistus
Lisaks kaalule tuleb Eestis mõnede nomenklatuurinumbrite puhul esitada ka kogus täiendavas mõõtühikus.

Seadistamiseks avage **Nomenklatuurinumbrid** ning täitke **Täiendava mõõtühiku tähis** ning märkige **Täiendavad ühikud**, kui need on nõutud.
  
Kaupadel, mis kuuluvad antud nomenklatuurinumbri alla, peab sama mõõtühik olema seadistatud ka **Kauba mõõtühikute** all.

Selliste kaupade puhul täidetakse aruande koostamisel **Intrastat žurnaali** real lisaveerud **Täiendava mõõtühiku tähis** ja **Täiendava mõõtühiku kogus**.

## Aruande koostamine intrastat žurnaalis
Enne esmakordset aruande koostamist kontrollige, kas Eesti failiformaat on seadistatud. Selleks avage **Intrastati seadistus** ja kontrollige **Eesti Intrastat** vahelehel, et **Formaat seadistatud** väärtus on 'Jah'. Klikkides väljal näete formaadi konfiguratsioonikirjet.

Kui eelnev formaat on seadistatud, siis intrastat žurnaali tegevused **Soovita read** ja **Koosta fail** kasutavad nende Eesti jaoks lokaliseeritud versioone.

XML kujul väljundfaili saab esitada [estat](https://estat.stat.ee/) keskkonnas.

***

Täpsema info saamiseks võtke palun ühendust oma partneriga:  
[http://www.dynamicspartners.ee](http://www.dynamicspartners.ee)
