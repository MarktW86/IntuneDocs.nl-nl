---
title: UI-updates voor Intune-apps voor eindgebruikers
description: Ontdek wat is gewijzigd in de gebruikersinterface voor apps op eindgebruikersapparaten met Intune.
keywords: 
author: barlanmsft
ms.author: barlan
manager: angrobe
ms.date: 06/28/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: b782e382-8deb-48a7-a437-d7c5a17163f1
ms.reviewer: priyar
ms.suite: ems
ms.custom: intune-classic
ms.openlocfilehash: 1e2e1eb6da9114c689aae5eb06f7d7c780f35817
ms.sourcegitcommit: 34cfebfc1d8b81032f4d41869d74dda559e677e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2017
---
# <a name="ui-updates-for-intune-end-user-apps"></a>UI-updates voor Intune-apps voor eindgebruikers
Lees welke updates we hebben aangebracht in de gebruikersinterface voor apps die uw eindgebruikers zien in deze versie van Microsoft Intune. Dit kan u helpen bij de communicatie met gebruikers en het bijwerken van eventuele aangepaste documentatie die u hebt gemaakt om uw implementatie te ondersteunen. Zo kunt u beter problemen oplossen wanneer ze de helpdesk bellen voor ondersteuning via de bedrijfsportal.

## <a name="week-of-june-12-2017"></a>Week van 12 juni 2017

### <a name="company-portal-app-for-android-now-has-a-new-end-user-experience-for-app-protection-policies---1305217--"></a>De Intune-bedrijfsportal-app voor Android heeft een nieuwe interface voor app-beveiligingsbeleid <!--1305217-->
Op basis van feedback van klanten hebben we de Intune-bedrijfsportal-app voor Android aangepast en de knop **Toegang verkrijgen tot bedrijfsinhoud** toegevoegd. De reden hiervoor is dat eindgebruikers dan niet onnodig het registratieproces moeten doorlopen wanneer ze alleen toegang nodig hebben tot apps die ondersteuning bieden voor app-beveiligingsbeleid, een functie van Intune Mobile Application Management.

De gebruiker hoeft alleen maar op de knop **Toegang verkrijgen tot bedrijfsinhoud** te tikken in plaats van het apparaat eerst te registreren.

![Een afbeelding van de Intune-bedrijfsportal-app voor Android, met in het midden groot de tekst in Toegang verkrijgen tot bedrijfsinhoud, in plaats van opties voor directe inschrijving, wat de standaardsituatie is.](./media/and_access_company_content_after_1706.png)

De gebruiker wordt omgeleid naar de website met de bedrijfsportal om de app te autoriseren voor gebruik op hun apparaat, waarvoor hun referenties worden geverifieerd door de bedrijfsportal-app.

![Een afbeelding van de website met de bedrijfsportal, waarop de aanmelding wordt bevestigd.](./media/and_iwp_sign_in_auth_page_after_1706.png)

Het apparaat kan nog steeds onder volledig beheer worden geplaatst door op het **actiemenu** te tikken.

![Een afbeelding van de Intune-bedrijfsportal-app voor Android, met het menu in de rechterbovenhoek van het scherm met een optie om het apparaat alsnog te registreren.](./media/and_sign_in_menu_after_app_protection_policy_enrolled_after_1706.png)

### <a name="improvements-to-app-syncing-with-windows-10-creators-update---676505--"></a>Verbeterde synchronisatie van apps met Windows 10-makersupdate <!--676505-->

De bedrijfsportal-app voor Windows 10 voert nu automatisch een synchronisatie uit voor app-installatieaanvragen voor apparaten met Windows 10-makersupdate (versie 1703). Hierdoor is de kans aanzienlijk kleiner dat app-installaties worden gestopt tijdens de status Synchronisatie in behandeling. Daarnaast kunnen gebruikers handmatig een synchronisatie uitvoeren vanuit de app.

![Een afbeelding van de Intune-bedrijfsportal-app voor Windows 10, waarbij Microsoft Word wordt gedownload in de App Store van de bedrijfsportal.](./media/w10_download_pending_after_1706.png)

![Een afbeelding van de Intune-bedrijfsportal-app voor Windows 10, met de nieuwe automatische synchronisatiestatus die aangeeft dat het apparaat wordt gesynchroniseerd en probeert de app te downloaden.](./media/w10_download_pending_syncing_after_1706.png)

### <a name="new-guided-experience-for-windows-10-company-portal----1058938---"></a>Nieuwe begeleide ervaring voor Windows 10-bedrijfsportal<!---1058938--->
De bedrijfsportal-app voor Windows 10 bevat een begeleiding voor Intune voor apparaten die nog niet zijn geïdentificeerd of geregistreerd. Deze nieuwe ervaring biedt stapsgewijze instructies die gebruikers begeleidt bij de registratie bij Azure Active Directory (vereist voor de voorwaardelijke toegangsfuncties) en MDM-registratie (vereist voor apparaatbeheerfuncties). De stapsgewijze instructies zijn toegankelijk via de startpagina van de bedrijfsportal. Als gebruikers de registratie en inschrijving niet voltooien, kunnen ze de app gewoon blijven gebruiken, maar is de functionaliteit beperkt.

Deze update is alleen zichtbaar op apparaten met Windows 10 Jubileumupdate (build 1607) of hoger.

![Een afbeelding van de landingspagina van de Intune-bedrijfsportal-app voor Windows 10, met een statusbericht in het midden dat aangeeft dat het apparaat nog niet is ingesteld voor zakelijk gebruik en dat de gebruiker het bericht moet selecteren om hiermee te beginnen.](./media/win10_guided_enroll_select_setup_after_1706.png)

![Een afbeelding van de configuratiepagina van de Intune-bedrijfsportal-app voor Windows 10, met een waarschuwing dat de gebruiker een bedrijfsaccount moet toevoegen aan dit apparaat en dat het apparaat dan kan worden ingeschreven voor beheer.](./media/win10_guided_enroll_we_help_setup_after_1706.png)

![Een afbeelding van de Intune-bedrijfsportal-app voor Windows 10, met de instructie om een bedrijfsaccount toe te voegen, wat kan door in de app Instellingen de optie Verbinding maken te selecteren. Als dat is gebeurd, wordt op het scherm uitgelegd dat ze terug moeten gaan naar de Intune-bedrijfsportal-app om het inschrijven te voltooien.](./media/win10_guided_enroll_leaving_for_iwp_after_1706.png)

![Afbeelding van de Intune-bedrijfsportal-app voor Windows 10 met het scherm Registreren voor beheer, met een bericht dat het inschrijven is voltooid en dat de gebruiker nu op de knop Volgende moet tikken om door te gaan.](./media/win10_guided_enroll_youre_now_enrolled_after_1706.png)

![Een afbeelding van de Intune-bedrijfsportal-app voor Windows 10 met het scherm dat alles klaar is en dat het apparaat is ingeschreven met een bedrijfsaccount.](./media/win10_guided_enroll_youre_all_set_after_1706.png)

### <a name="new-menu-action-to-easily-remove-company-portal---1164569--"></a>Nieuwe menu-actie voor het eenvoudig verwijderen van de bedrijfsportal <!--1164569-->
Op basis van feedback van gebruikers is aan de bedrijfsportal-app voor Android een nieuwe menu-actie toegevoegd om het verwijderen van de bedrijfsportal van uw apparaat te starten. Met deze actie verwijdert u het apparaat uit Intune-beheer, zodat de app door de gebruiker van het apparaat kan worden verwijderd.

![Een afbeelding van de Android-bedrijfsportal-app met in de rechterbovenhoek het geopende actiemenu. De nieuwe optie Bedrijfsportal verwijderen is als derde optie beschikbaar, onder Mijn profiel en Instellingen, en boven Voorwaarden en bepalingen, Help en feedback en Over.](./media/android_remove_cp_menu_action_after_1705.png)

![Een afbeelding van het bevestigingsdialoogvenster dat beschikbaar is nadat u de nieuwe optie Bedrijfsportal verwijderen hebt geselecteerd in het actiemenu. Via het dialoogvenster wordt de gebruiker geïnformeerd dat 'door het verwijderen van de bedrijfsportal uw apparaat niet meer wordt beheerd door uw IT-beheerder en u mogelijk geen toegang meer hebt tot bedrijfsgegevens, bedrijfs-apps en bedrijfse-mail.' Vervolgens wordt de gebruiker gevraagd om het verwijderen van de bedrijfsportal-app te bevestigen met Ja.](./media/android_remove_cp_menu_confirmation_after_1705.png)

## <a name="week-of-june-5-2017"></a>Week van 5 juni 2017

### <a name="improvements-to-the-app-tiles-in-the-company-portal-app-for-ios"></a>Verbeteringen in de app-tegels in de bedrijfsportal-app voor iOS
Het ontwerp van de app-tegels op de startpagina is bijgewerkt in overeenstemming met de huisstijlkleur die u voor de bedrijfsportal instelt.

**Voor**

![Een afbeelding van de bedrijfsportal-app voor iOS voor de update, met vooraf ingestelde opvullende afbeeldingen voor Alle apps, Aanbevolen apps en Categorieën.](./media/cp_ios_homepage_before_1705.png)

**Na**

![Een afbeelding van de bedrijfsportal-app voor iOS na de update, waarin u nu de mogelijkheid hebt de voor uw organisatie relevante kleuren te selecteren .](./media/cp_ios_homepage_after_1705.png)

### <a name="account-picker-now-available-for-the-company-portal-app-for-ios"></a>Account objectkiezer nu beschikbaar voor de bedrijfsportal-app voor iOS
Als gebruikers op hun iOS-apparaat hun werk- of schoolaccount hebben gebruikt om zich aan te melden bij andere Microsoft-apps, zien zij mogelijk de nieuwe accountkiezer wanneer zij zich voor het eerst bij de bedrijfsportal aanmelden.

![Een afbeelding van de accountkiezer waarin een testgebruiker 'Robin Swanson' kiest tussen een van de twee e-mailadressen. Onder de twee adressen bevindt zich een knop waarmee de gebruiker zich kan aanmelden met een ander account.](./media/cp_ios_multi-account-selector-after-1705.png)

## <a name="april-2017"></a>April 2017

### <a name="new-icons-for-the-managed-browser-and-the-company-portal---918433-918431--"></a>Nieuwe pictogrammen voor Managed Browser en de bedrijfsportal <!--918433, 918431-->

Zowel de Android- als iOS-versie van de Managed Browser heeft een nieuw pictogram. Het nieuwe pictogram bevat het bijgewerkte Intune-logo om het consistenter te maken met de andere apps in Enterprise Mobility + Security (EM+S).

<html>
<body>
   <table id="wrapper">
      <tr>
         <td>
            <img src="/intune/media/cp_manbro_before_042017.png" alt="The previous version of the Managed Browser app icon." width=200 height=366 align=center>
          </td>
          <td>
             <img src="/intune/media/cp_manbro_after_042017.png" alt="The updated version of the Managed Browser app icon." width=200 height=366 align=center>
           </td>
      </tr>
   </table>
</body>
</html>

De pictogrammen voor de Android-, iOS- en Windows-versies van de app in de bedrijfsportal worden ook vernieuwd voor meer consistentie met de andere apps in EM+S. Deze pictogrammen worden in de periode van april tot eind mei geleidelijk in gebruik genomen op de verschillende platforms.

### <a name="sign-in-progress-indicator-in-android-company-portal---953374--"></a>Voortgangsindicator voor aanmelden bij Android-bedrijfsportal <!--953374-->

De Android-bedrijfsportal-app is bijgewerkt met een voortgangsindicator voor het aanmelden wanneer de gebruiker de app opent of hervat. De indicator geeft de verschillende statussen weer, beginnend bij 'Verbinden...', gevolgd door 'Aanmelden...' en 'Beveiligingseisen controleren...', voordat de gebruiker de app kan gebruiken.

<html>
<body>
   <table id="wrapper">
      <tr>
         <td>
            <img src="/intune/media/cp_android_connecting_042017.png" alt="The Company Portal app for Android sign in screen that shows a partially filled loading bar with the phrase 'Connecting' underneath it." width=200 height=366 align=center>
          </td>
          <td>
             <img src="/intune/media/cp_android_signing_in_042017.png" alt="The Company Portal app for Android sign in screen that shows a partially filled loading bar with the phrase 'Signing in' underneath it." width=200 height=366 align=center>
           </td>
           <td>
              <img src="/intune/media/cp_android_checking_security_reqs_042017.png" alt="The Company Portal app for Android sign in screen that shows a partially filled loading bar with the phrase 'Checking for security requirements' underneath it." width=200 height=366 align=center>
           </td>
      </tr>
   </table>
</body>
</html>

### <a name="improved-app-install-status-for-the-windows-10-company-portal-app---676495--"></a>Verbeterde app-installatiestatus voor de Windows 10-bedrijfsportal-app <!--676495-->
De Windows 10-bedrijfsportal-app heeft op de app-detailpagina nu een voortgangsbalk voor installatie. Dit wordt ondersteund voor moderne apps op apparaten met Windows 10 Jubileumupdate en hoger.

__Voor__ ![Een afbeelding van de vorige versie van het laadscherm, waarbij voor de status alleen Installeren werd vermeld.](./media/cp_win10_install_status_before_1704.png)

__Na__ ![Een afbeelding van de bijgewerkte versie van het laadscherm, waarbij nu een voortgangsbalk voor de installatie wordt weergegeven.](./media/cp_win10_install_status_after_1704.png)

## <a name="february-2017"></a>Februari 2017

### <a name="new-user-experience-for-the-company-portal-app-for-android---621622-announced-1702--"></a>Nieuwe gebruikerservaring voor de bedrijfsportal-app voor Android <!--621622, announced 1702-->
Vanaf maart volgt de bedrijfsportal-app voor Android [richtlijnen voor het ontwerpen van materiaal](https://material.io/guidelines/material-design/introduction.html) voor een moderne vormgeving. Deze verbeterde gebruikerservaring omvat het volgende:

* __Kleuren__: tabbladkoppen kunnen worden gekleurd volgens uw aangepaste kleurenpalet.

![De afbeelding links toont de bedrijfsportal-app voor Android vóór de update. De afbeelding rechts toont de bedrijfsportal-app voor Android na de update. In beide afbeeldingen is het tabblad Apparaten geselecteerd uit de drie beschikbare tabbladen Apps, Apparaten en Contact opnemen met IT.](./media/CP_Android_DevicesTab_BeforeAfter.png)

* __Interface__: de knoppen __Aanbevolen apps__ en __Alle apps__ op het tabblad __Apps__ zijn bijgewerkt. De knop __Zoeken__ is nu een zwevende actieknop.

![De afbeelding links toont de bedrijfsportal-app voor Android vóór de update. De afbeelding rechts toont de bedrijfsportal-app voor Android na de update. In beide afbeeldingen is het tabblad Apps geselecteerd uit de drie beschikbare tabbladen Apps, Apparaten en Contact opnemen met IT.](./media/CP_Android_AppsTab_BeforeAfter.png)

* __Navigatie__: Alle apps biedt een tabbladweergave van de opties __Aanbevolen__, __Alle__ en __Categorieën__ om de navigatie te vereenvoudigen. __Contact opnemen met IT__ is gestroomlijnd voor een betere leesbaarheid.

<html>
<body>
   <table id="wrapper">
      <tr>
         <td>
            <img src="/intune/media/cp_android_contactit_after.png" alt="The Company Portal app for Android displaying an updated version of the Contact IT tab. The tab shows available contact information for IT, including phone number, email address, IT website, and IT contact information." width=200 height=366 align=center>
          </td>
      </tr>
   </table>
</body>
</html>

## <a name="january-2017"></a>Januari 2017

### <a name="modernizing-the-company-portal-website---753980-announced-1701--"></a>De bedrijfsportalwebsite moderniseren <!--753980, announced 1701-->
Te beginnen in februari ondersteunt de bedrijfsportalwebsite apps die zijn gericht op gebruikers die geen beheerde apparaten hebben. De website wordt in overeenstemming gebracht met andere Microsoft-producten en -services met een nieuw contrasterend kleurenschema, dynamische illustraties en een 'hamburgermenu', ![Kleine afbeelding van het hamburgermenu dat nu is toegevoegd in de linkerbovenhoek van de bedrijfsportalwebsite](./media/CP_hamburger_menu.png) dat contactgegevens van de helpdesk bevat, alsmede informatie over bestaande beheerde apparaten. De landingspagina wordt opnieuw ingedeeld om de nadruk te leggen op apps die beschikbaar zijn voor gebruikers, met carrousels voor uitgelichte en recent bijgewerkte apps.

![Aan de linkerkant een afbeelding van de huidige versie van de bedrijfsportal-website met de vorige versie van Apps, mijn apparaten en speciale en categorieënweergaven. Aan de rechterkant een afbeelding van de bijgewerkte versie van de bedrijfsportal-website met een vernieuwde app-carrousel, een lijst met onlangs gepubliceerde apps en bijgewerkte categorieën-weergave.](./media/CP_Website_BeforeAfter_Feb2016.png)

## <a name="coming-soon-in-the-ui"></a>Binnenkort beschikbaar in de gebruikersinterface
Dit zijn de plannen voor manieren waarop we de gebruikerservaring gaan verbeteren door onze gebruikersinterface bij te werken.

> [!Note]
> De onderstaande afbeeldingen zijn voorbeelden en het aangekondigde product kan verschillen van de weergegeven versies.

### <a name="improved-sign-in-experience-across-company-portal-apps-for-all-platforms---user-story-1132123--"></a>Verbeterde aanmeldervaring in de bedrijfsportal-apps voor alle platformen <!--User Story 1132123-->

Dit is de aankondiging van een wijziging die in de komende maanden wordt geïntroduceerd en waarmee de aanmeldervaring wordt verbeterd voor apps in de Intune-bedrijfsportal voor Android, iOS en Windows. De nieuwe gebruikerservaring wordt automatisch toegepast op alle platformen voor de bedrijfsportal-app wanneer deze wijziging wordt doorgevoerd in Azure AD. Bovendien kunnen gebruikers nu zich aanmelden bij de bedrijfsportal vanaf een ander apparaat met een gegenereerde code voor eenmalig gebruik. Dit is vooral nuttig in gevallen wanneer gebruikers zich moeten aanmelden zonder referenties.  

Hieronder ziet u de vorige aanmeldingservaring, de nieuwe aanmeldingservaring met referenties en de nieuwe aanmeldingservaring vanaf een ander apparaat.

__Vorige aanmeldingservaring__

![De aanmeldingspagina van de bedrijfsportal met een pictogram van een persoon voor een grafische weergave van een website. Hieronder staat de knop Aanmelden. Een koppeling onder aan de pagina leidt naar informatie over privacy en cookies van Microsoft.](./media/cp_ios_aad_signin_before_1704_001.png)

![Nadat de gebruiker op Aanmelden heeft getikt, vult de gebruiker de referenties in op deze pagina waarop wordt gevraagd om het e-mailadres en wachtwoord van de gebruiker. Ook worden verschillende manieren gegeven om problemen met wachtwoorden op te lossen.](./media/cp_ios_aad_signin_before_1704_002.png)

![Na het invoeren van het wachtwoord, wordt de gebruiker aangemeld met de bedrijfsportal-app. Hierbij wordt een laadbalk weergegeven.](./media/cp_ios_aad_signin_before_1704_003.png)

__Nieuwe aanmeldingservaring__

![De aanmeldingspagina van de bedrijfsportal met een pictogram van een persoon voor een grafische weergave van een website. Hieronder staat de knop Aanmelden. Een koppeling onder aan de pagina leidt naar informatie over privacy en cookies van Microsoft.](./media/cp_ios_aad_signin_after_1704_001.png)

![De gebruiker wordt gevraagd alleen een e-mailadres in te voeren in plaats van het e-mailadres en wachtwoord op hetzelfde scherm.](./media/cp_ios_aad_signin_after_1704_002.png)

![De gebruiker wordt gevraagd om het wachtwoord nadat het e-mailadres is geaccepteerd.](./media/cp_ios_aad_signin_after_1704_003.png)

![Nadat het verificatieproces is doorlopen, wordt er aangemeld met de bedrijfsportal-app. Hierbij wordt een laadbalk weergegeven.](./media/cp_ios_aad_signin_from_another_device_after_1704_007.png)

__Nieuwe aanmeldingservaring bij aanmelding vanaf een ander apparaat__

![De aanmeldingspagina van de bedrijfsportal met een pictogram van een persoon voor een grafische weergave van een website. Hieronder staat de knop Aanmelden. Een koppeling onder aan de pagina leidt naar informatie over privacy en cookies van Microsoft.](./media/cp_ios_aad_signin_from_another_device_after_1704_001.png)

Tik op de koppeling __Aanmelding vanaf een ander apparaat__.

![U vindt hier instructies om naar de pagina aka.ms/devicelogin te gaan met een unieke wachtwoordcode vanaf uw werkcomputer en de code te gebruiken om u aan te melden.](./media/cp_ios_aad_signin_from_another_device_after_1704_003.png)

Open een browser en ga naar [https://aka.ms/devicelogin](https://aka.ms/devicelogin).

![Een afbeelding van de browser van de gebruiker op de werkcomputer in plaats van de bedrijfsportal-app. Op de weergegeven pagina Apparaataanmelding wordt de gebruiker gevraagd om de code in de bedrijfsportal-app is ontvangen.](./media/cp_ios_aad_signin_from_another_device_after_1704_004.png)

Voer de code die werd weergegeven in de bedrijfsportal-app. Wanneer u __Doorgaan__ selecteert, kunt u zich verifiëren op alle manieren die worden ondersteund door uw bedrijf, zoals een smartcard.

![De gebruiker heeft de unieke code ingevoerd in het veld en op de site Apparaataanmelding is gevraagd om te bevestigen dat de Intune bedrijfsportal-app de juiste app is om autorisatie te ontvangen voor aanmelding.](./media/cp_ios_aad_signin_from_another_device_after_1704_005.png)

![Een bevestigingspagina met de mededeling dat de gebruiker nu is aangemeld bij de bedrijfsportal-app op hun apparaat en dat deze pagina kan worden gesloten.](./media/cp_ios_aad_signin_from_another_device_after_1704_006.png)

De bedrijfsportal-app begint met aanmelden.

![Nadat het verificatieproces is doorlopen, wordt er aangemeld met de bedrijfsportal-app. Hierbij wordt een laadbalk weergegeven.](./media/cp_ios_aad_signin_from_another_device_after_1704_007.png)
### <a name="see-also"></a>Zie tevens
* [Microsoft Intune-blog](http://go.microsoft.com/fwlink/?LinkID=273882)
* [Roadmap voor cloudplatform](https://www.microsoft.com/server-cloud/roadmap/Indevelopment.aspx?TabIndex=0&dropValue=Intune)
* [Wat is er nieuw in Intune?](https://docs.microsoft.com/intune/whats-new)
