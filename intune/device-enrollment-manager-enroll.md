---
title: Apparaten inschrijven - apparaatinschrijvingsmanager
titleSuffix: Intune on Azure
description: Gebruik het manageraccount voor apparaatregistratie om apparaten in te registreren. "
keywords: 
author: nathbarn
ms.author: nathbarn
manager: angrobe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 7196b33e-d303-4415-ad0b-2ecdb14230fd
ms.reviewer: damionw
ms.suite: ems
ms.custom: intune-azure
ms.openlocfilehash: 1667470154e5d2485e3a372ab25d36eea12109a7
ms.sourcegitcommit: 34cfebfc1d8b81032f4d41869d74dda559e677e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2017
---
# <a name="enroll-devices-using-device-enrollment-manager"></a>Apparaten inschrijven met de apparaatinschrijvingsmanager

[!INCLUDE[azure_portal](./includes/azure_portal.md)]

Organisaties kunnen Intune gebruiken voor het beheren van een groot aantal mobiele apparaten met één gebruikersaccount. Het account voor de *apparaatinschrijvingsmanager* (DEM-account) is een speciaal gebruikersaccount waarmee maximaal duizend apparaten kunnen worden ingeschreven. U voegt bestaande gebruikers toe aan het DEM-account om ze speciale DEM-mogelijkheden te bieden. Voor elk geregistreerd apparaat is een licentie nodig. Gebruik apparaten die zijn geregistreerd met dit account als gedeelde apparaten in plaats van persoonlijke (BYOD)-apparaten.  

Gebruikers moeten in Azure Portal bestaan om ze te kunnen toevoegen aan apparaatinschrijvingsmanagers. Voor een optimale beveiliging mag de DEM-gebruiker géén Intune-beheerder zijn.

>[!NOTE]
>De DEM-registratiemethode kan niet worden gebruikt met de volgende andere registratiemethoden: [Apple Configurator met Configuratieassistent](apple-configurator-setup-assistant-enroll-ios.md), [Apple Configurator met directe enrollment](apple-configurator-direct-enroll-ios.md), [Apple School Manager (ASM)](apple-school-manager-set-up-ios.md) of [Device Enrollment Program (DEP)](device-enrollment-program-enroll-ios.md).

## <a name="example-of-a-device-enrollment-manager-scenario"></a>Voorbeeld van een scenario voor apparaatinschrijvingsmanager

Een restaurant wil 50 verkooptablets inzetten voor zijn bedienend personeel en bestellingsmonitors voor het keukenpersoneel. De werknemers hebben geen toegang tot bedrijfsgegevens nodig of moeten zich aanmelden als gebruikers. De Intune-beheerder maakt een apparaatinschrijvingsmanageraccount en voegt een restaurantsupervisor toe aan het DEM-account. Daarmee krijgt die supervisor DEM-mogelijkheden. De supervisor kan de 50 tablets nu inschrijven met de DEM-referenties.

Alleen gebruikers in de Intune-console kunnen apparaatinschrijvingsbeheerders zijn. De gebruiker van het account voor apparaatinschrijvingsmanagers mag geen Intune-beheerder zijn.

De DEM-gebruiker kan:

-   Maximaal 1000 apparaten inschrijven in Intune.
-   Aanmelden bij de bedrijfsportal om bedrijfsapps op te halen.
-   Toegang tot bedrijfsgegevens configureren door rolspecifieke apps te implementeren op de tablets.

## <a name="limitations-of-devices-that-are-enrolled-with-a-dem-account"></a>Beperkingen van apparaten die zijn ingeschreven bij een DEM-account

Apparaten die zijn geregistreerd met een account voor apparaatinschrijvingsmanagers, hebben de volgende beperkingen:

  - Geen toegang per gebruiker. Omdat apparaten geen toegewezen gebruiker hebben, heeft het apparaat geen toegang tot e-mail of bedrijfsgegevens. VPN-configuraties kunnen echter nog wel worden gebruikt om apps op apparaten te leveren met toegang tot gegevens.
  - Er is geen voorwaardelijke toegang mogelijk omdat deze scenario's per gebruiker moet worden opgegeven.
  - De DEM-gebruiker kan bij DEM ingeschreven apparaten niet via de bedrijfsportal uitschrijven op het apparaat zelf. De Intune-beheerder kan dit wel doen, maar de DEM-gebruiker niet.
  - Alleen het lokale apparaat wordt weergegeven in de bedrijfsportal-app of op de website.
  - Gebruikers kunnen geen Apple VPP-apps (Volume Purchase Program) gebruiken vanwege de Apple ID-vereisten per gebruiker voor het beheer van apps.
  - (alleen iOS) Als u DEM gebruikt om iOS-apparaten in te schrijven, kunt u de Apple Configurator of het Apple Device Enrollment Program (DEP) of Apple School Manager (ASM) niet gebruiken om apparaten te registreren.
  - Voor elk apparaat is een apparaatlicentie vereist. Meer informatie over [gebruikers- en apparaatlicenties](licenses-assign.md#how-user-and-device-licenses-affect-access-to-services).


> [!NOTE]
> Om bedrijfsapps te implementeren op apparaten die worden beheerd met de apparaatinschrijvingsmanager, moet u de bedrijfsportal-app als een **Vereiste installatie** implementeren naar het gebruikersaccount voor de apparaatinschrijvingsmanager.
> Om prestaties te verbeteren wordt bij het weergeven van de bedrijfsportal-app op een DEM-apparaat alleen het lokale apparaat weergegeven. Extern beheer van andere DEM-apparaten is alleen mogelijk via de Intune-beheerconsole.


## <a name="add-a-device-enrollment-manager"></a>Een apparaatinschrijvingsmanager toevoegen

1.  Kies in Azure Portal **Meer services** > **Bewaking en beheer** > **Intune**.

2.  Kies **Apparaten inschrijven** op de blade Intune en kies vervolgens **Apparaatinschrijvingsmanagers**.

3.  Selecteer **Toevoegen**.

4.  Voer op de blade **Gebruiker toevoegen** een UPN-naam (User Principal Name) in voor de DEM-gebruiker en selecteer **Toevoegen**. De DEM-gebruiker wordt toegevoegd aan de lijst met DEM-gebruikers.

## <a name="permissions-for-dem"></a>Machtigingen voor DEM

Als u DEM-registratietaken wilt uitvoeren, moet u beschikken over de Azure AD-rollen Globale beheerde of Intune-servicebeheerder. Deze rollen zijn vereist om alle DEM-gebruikers weer te geven, ondanks dat er RBAC-machtigingen worden vermeld en beschikbaar zijn onder de aangepaste gebruikersrol. Een gebruiker zonder de rol van globale beheerder of Intune-servicebeheerder maar met leesmachtigingen voor de DEM-rol, kan alleen de DEM-gebruikers weergeven die door de gebruiker zijn gemaakt. RBAC-rolondersteuning voor deze functies wordt in de toekomst aangekondigd.

Als een gebruiker niet over rol van globale beheerder of Intune-servicebeheerder beschikt maar wel leesmachtigingen voor de toegewezen DEM-rol heeft, kan de gebruiker alleen de zelfgemaakt DEM-gebruikers weergeven.

## <a name="remove-a-device-enrollment-manager"></a>Een apparaatinschrijvingsmanager verwijderen

Het verwijderen van een apparaatinschrijvingsmanager is niet van invloed op ingeschreven apparaten. Het volgende is van toepassing wanneer een apparaatinschrijvingsmanager wordt verwijderd:

-   Dit is niet van invloed op geregistreerde apparaten. Deze blijven volledig beheerd.
-   De accountreferenties van de verwijderde apparaatinschrijvingsmanager blijven geldig.
-   Apparaten kunnen nog steeds niet worden gewist of buiten gebruik worden gesteld met de verwijderde apparaatinschrijvingsmanager.
-   De verwijderde apparaatinschrijvingsmanager kan slechts een bepaald aantal apparaten registreren, overeenkomstig de gebruikerslimiet die door de Intune-beheerder is geconfigureerd.

**Een apparaatinschrijvingsmanager verwijderen**

1. Kies in Azure Portal **Meer services** > **Bewaking en beheer** > **Intune**.
2. Kies **Apparaten inschrijven** op de blade Intune en kies vervolgens **Apparaatinschrijvingsmanagers**.
3. Klik op de blade **Apparaatinschrijvingsmanagers** met de rechtermuisknop op de DEM-gebruiker en selecteer **Verwijderen**.

## <a name="view-the-properties-of-a-device-enrollment-manager"></a>De eigenschappen van een apparaatinschrijvingsmanager weergeven

1. Kies in de Intune-portal de optie **Apparaatinschrijving** en kies vervolgens **Apparaatinschrijvingsmanagers**.
2. Klik op de blade **Apparaatinschrijvingsmanagers** met de rechtermuisknop op de DEM-gebruiker en selecteer **Eigenschappen**.
