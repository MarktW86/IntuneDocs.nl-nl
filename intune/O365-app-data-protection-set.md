---
title: Basisgegevensbeheer in Office 365-apps instellen in Intune
titleSuffix: Intune on Azure
description: Ondersteunende documentatie voor de wizard Office 365-apps beheren.
keywords: 
author: lindavr
ms.author: lindavr
manager: angrobe
ms.date: 01/09/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 852612ac-f146-4372-a900-3f6fdebd05ad
ROBOTS: NOINDEX,NOFOLLOW
ms.reviewer: ayesham
ms.suite: ems
ms.custom: intune-azure
ms.openlocfilehash: 302f646bfb9ff0ac024687fa0b3926d83158995c
ms.sourcegitcommit: 34cfebfc1d8b81032f4d41869d74dda559e677e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2017
---
# <a name="how-your-users-will-experience-basic-protection-on-managed-office-365-apps"></a>Hoe uw gebruikers basisbeveiliging ervaren in beheerde Office 365-apps

Met de wizard **Office 365-apps beheren** wordt voor elk apparaatplatform een app-beveiligingsbeleid gemaakt.

De wizard schakelt de volgende beleidsregels in:

**iOS**
* App-gegevens versleutelen

**Android**
* App-gegevens versleutelen
* Eenvoudige pincode vereist voor toegang

Deze beleidsregels zorgen ervoor dat u de Office 365-apps kunt beheren en u de mogelijkheid hebt werkgegevens uit de Office-apps te wissen als dit nodig is. Daarnaast zorgen de beleidsregels voor basisbeveiliging voor zoekgeraakte of gestolen apparaten door de werkgegevens te versleutelen en af te dwingen dat een pincode moet worden ingevoerd om de gegevens in de Office 365-apps te kunnen bekijken.


In dit artikel wordt OneDrive voor Bedrijven gebruikt als voorbeeld om de gebruikerservaring te laten zien in een toepassing die met Intune wordt beheerd.


>[!NOTE]
>Op een privé-apparaat downloadt de eindgebruiker doorgaans de app. Als het apparaat wordt beheerd door een MDM-oplossing (Mobile Device Management), kunt u de app op het apparaat implementeren.

## <a name="user-experience-on-an-ios-device"></a>Gebruikerservaring op een iOS-apparaat

1. Start de app OneDrive voor Bedrijven om de aanmeldingspagina te openen.  <br/> ![Afbeelding van het OneDrive-aanmeldingsscherm voor iOS](./media/onedrive-ios-sign-in.png)
2. Voer de gebruikersnaam van uw werkaccount in. U wordt omgeleid naar de pagina Office 365-verificatie, waar u uw werkreferenties kunt invoeren. <br/> ![Afbeelding van de aanmeldingspagina voor Office 365](./media/o365-sign-in-ios.png)
3. Nadat uw referenties door Azure Active Directory zijn geverifieerd, worden de MAM-beleidsregels (Mobile App Management) toegepast en wordt u gevraagd de app OneDrive voor Bedrijven opnieuw te starten.  <br/>![Afbeelding van prompt voor opnieuw starten voor iOS](./media/ios-restart-prompt.png)
>[!NOTE]
>Het bericht voor opnieuw starten wordt alleen weergegeven op apparaten die niet zijn ingeschreven in Intune.


4. Start de app OneDrive voor Bedrijven opnieuw. De app wordt gestart en de MAM-beleidsregels worden ingeschakeld. U wordt gevraagd een pincode voor het apparaat in te stellen (als u nog geen pincode voor het apparaat hebt geconfigureerd). <br/> ![Afbeelding van prompt voor het maken van een pincode](./media/pin-prompt-ios.png)

>[!NOTE]
>Deze prompt wordt voor de meeste gebruikers niet weergegeven. Alleen gebruikers die geen pincode op hun iOS-apparaat hebben ingeschakeld, krijgen deze prompt te zien.


5. Zodra u de pincode hebt ingesteld en hebt bevestigd, gaat u terug naar de app OneDrive voor Bedrijven. U ziet een eenmalige kennisgeving dat de werkgegevens in OneDrive op dit moment worden beveiligd door de IT-beheerder. <br/> ![Afbeelding van de eenmalige kennisgeving van uw IT-beheerder](./media/one-time-notice.png)
6. Klik voorbij deze kennisgeving om toegang te krijgen tot de bestanden in uw exemplaar van OneDrive voor Bedrijven. <br/> ![Afbeelding van OneDrive-bestanden op iOS-apparaat](./media/onedrive-files-ios.png) <br/>

>[!NOTE]
>Wanneer u een geïmplementeerde beleid wijzigt, worden de wijzigingen de volgende keer dat u de app opent, toegepast.


## <a name="user-experience-on-an-android-device"></a>Gebruikerservaring op een Android-apparaat

1. Start de app OneDrive voor Bedrijven om de aanmeldingspagina te openen.  <br/> ![Afbeelding van welkomstscherm van de app OneDrive](./media/onedrive-android-welcome.png)
2. Voer de gebruikersnaam van uw werkaccount in. U wordt omgeleid naar de pagina Office 365-verificatie, waar u uw werkreferenties kunt invoeren. <br/> ![Afbeelding van O365-aanmelding op Android](./media/o365-sign-in-android.png)
3. Nadat uw referenties door Azure Active Directory zijn geverifieerd, ziet u een bericht met instructies voor het installeren van de bedrijfsportal-app, als deze niet al op het apparaat is geïnstalleerd. Tik op **Ga naar winkel** om door te gaan. <br/> ![Afbeelding van het bericht voor het downloaden van de bedrijfsportal-app](./media/get-company-portal-android.png) <br/>Als u de bedrijfsportal-app al op uw telefoon hebt geïnstalleerd, wordt de app OneDrive voor Bedrijven automatisch gestart en kunt u doorgaan naar de eindopmerking.
>[!IMPORTANT]
>Als u voor uw Android-apparaat instelt dat Office-apps moeten worden beheerd met een MAM-beleid, **moet** de gebruiker van het apparaat de bedrijfsportal-app installeren om toegang te kunnen krijgen tot zijn of haar e-mails en documenten voor werk, ook al hoeft de eindgebruiker de app niet te openen of zich aan te melden bij de app om e-mails en documenten te kunnen lezen.

4. U bent nu in de Google Play Store waar u de bedrijfsportal-app kunt downloaden en installeren. De app helpt u de gegevens veilig en beschermd te houden. <br/> ![Afbeelding van de app in Google Play Store](./media/google-play-get-app-android.png)
5. Nadat u de app-installatie hebt voltooid, kiest u **Accepteren** om de voorwaarden te accepteren. De app OneDrive voor Bedrijven wordt automatisch gestart.


>[!NOTE]
>De volgende keer dat u OneDrive voor Bedrijven opent, wordt u mogelijk gevraagd een pincode in te stellen als de IT-afdeling dit vereist. Nadat u de pincode hebt ingesteld en bevestigd, kunt u doorgaan naar OneDrive voor Bedrijven.

![Afbeelding van prompt voor pincode](./media/pin-prompt-android.png)


<!--- Original steps: 6. The next time you open OneDrive for Business, you may be asked to set a PIN, if your IT requires one to use the OneDrive for Business app. ART 7. After you set and confirm the PIN, you can continue on to OneDrive for Business. -->

## <a name="what-policies-does-this-wizard-set"></a>Welke beleidsregels worden met deze wizard ingesteld?
|     |       | |
|----|--------|-|
|**Naam**|Office 365-apps beheren| |
| **Beschrijving**|Gemaakt door de wizard Office 365-apps beheren| |
| |  | |
| **Naam van instelling** |**Waarde voor iOS-beleid** | **Waarde voor Android-beleid** |
|Back-ups van de iTunes en iCloud voorkomen| Nee | N.v.t. |
|Back-ups van Android voorkomen |N.v.t. | Nee|
|App mag gegevens overdragen naar ander apps | Alle apps | Alle apps|
|App mag gegevens ontvangen van andere apps| Alle apps | Alle apps|
|'Opslaan als' voorkomen | Nee | Nee|
|Knippen, kopiëren en plakken met andere apps beperken | Elke app | Elke app |
|Webinhoud beperken en weergeven in een bedrijfsbeheerde browser | Nee| Nee|
|App-gegevens versleutelen | Wanneer apparaat is vergrendeld | Yes|
|Synchroniseren van contactpersonen uitschakelen | Nee| Nee|
|Afdrukken uitschakelen | Nee | Nee|
|Pincode is vereist voor toegang | Nee | Yes|
|Aantal pogingen voordat pincode opnieuw wordt ingesteld | N.v.t. |5|
|Eenvoudige pincode toestaan | N.v.t. |Yes|
|Lengte pincode | N.v.t. | 4|
|Vingerafdruk in plaats van pincode toestaan | N.v.t. | Yes |
|Bedrijfsreferenties vereisen voor toegang | Nee | Nee|
|De uitvoering blokkeren van beheerde apps die op gekraakte of geroote apparaten worden uitgevoerd | Nee | Nee|
|Toegangsvereisten opnieuw controleren na (minuten) - Time-out | 30 | 30|
|Toegangsvereisten opnieuw controleren na (minuten) - Offlinerespijtperiode | 720 |720|
|Offline-interval (dagen) voor gegevens van app worden gewist | 90 | 90|
|Schermafbeelding blokkeren (alleen Android-apparaten) | N.v.t. | Nee |

### <a name="why-is-an-app-pin-policy-only-configured-for-android-devices"></a>Waarom wordt alleen een app-pincodebeleid voor Android-apparaten geconfigureerd?
Versleuteling werkt anders voor iOS en Android.

Voor iOS geldt dat voor apps die zijn gekoppeld aan een Intune MAM-beleid, gegevens in rust worden versleuteld met behulp van versleuteling op apparaatniveau die wordt geleverd door het besturingssysteem. Wanneer u het app-versleutelingsbeleid inschakelt, is dus ook vereist dat de gebruiker in het bezit is van een pincode en deze moet invoeren om toegang tot zijn of haar werkgegevens te kunnen krijgen. Gebruikers die nog geen apparaatpincode op het apparaat hebben geconfigureerd, wordt gevraagd een apparaatpincode te maken.

Voor Android geldt dat voor apps die aan een Intune MAM-beleid zijn gekoppeld, de gegevens synchroon worden versleuteld tijdens I/O-taken. Inhoud van de apparaatopslag wordt altijd versleuteld. Voor apparaten die niet met MDM worden beheerd, kan een apparaatpincode niet worden afgedwongen door het MAM-beleid. Om ervoor te zorgen dat gebruikers een pincode invoeren om toegang tot hun werkgegevens te kunnen krijgen, wordt met de wizard het app-pincodebeleid ingeschakeld.

U kunt deze beleidsinstellingen altijd bewerken om aan de behoeften van uw organisatie te voldoen.

### <a name="how-can-i-view-and-edit-the-policies-created-by-the-wizard"></a>Hoe kan ik de beleidsregels bekijken en bewerken die door de wizard zijn gemaakt?
Als u deze beleidsregels, of andere beleidsregels die u in Intune Azure Portal maakt, wilt bekijken of bijwerken, kiest u in het dashboard **Apps beheren** > **App-beveiligingsbeleid**. De lijst met beleidsregels wordt rechts geopend. Kies het beleid dat u wilt bekijken en bewerk de instellingen. <br/>
![Afbeelding van gebruikersinterfacepad voor het weergeven van beleidsregels](./media/image-for-faq.png)

## <a name="next-steps"></a>Volgende stappen
Meer informatie over [app-beveiligingsbeleid](https://docs.microsoft.comapp-protection-policy.md).
