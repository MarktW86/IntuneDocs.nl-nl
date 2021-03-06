---
title: Instellingen voor Intune Endpoint Protection voor Windows 10
titleSuffix: Intune on Azure
description: Lees hier alles over de Intune-instellingen die u kunt gebruiken voor het beheren van instellingen voor eindpuntbeveiliging op Windows 10-apparaten, zoals BitLocker.
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 06/28/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 3af7c91b-8292-4c7e-8d25-8834fcf3517a
ms.reviewer: ilwu
ms.suite: ems
ms.custom: intune-azure
ms.openlocfilehash: 4994656afcf1cdb97fdcd3877f6dabdadfb7d374
ms.sourcegitcommit: 34cfebfc1d8b81032f4d41869d74dda559e677e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2017
---
# <a name="endpoint-protection-settings-for-windows-10-and-later-in-microsoft-intune"></a>Instellingen voor de beveiliging van eindpunten voor Windows 10 en hoger in Microsoft Intune

[!INCLUDE[azure_portal](./includes/azure_portal.md)]

Via het profiel voor eindpuntbeveiliging kunt u beveiligingsfuncties op Windows 10-apparaten beheren, zoals BitLocker.

Gebruik de informatie in dit onderwerp om profielen voor eindpuntbeveiliging te maken.

## <a name="create-an-endpoint-protection-profile"></a>Een profiel voor eindpuntbeveiliging maken

1. Meld u aan bij Azure Portal.
2. Kies **Meer services** > **Bewaking en beheer** > **Intune**.
3. Kies op de blade **Intune** de optie **Apparaatconfiguratie**.
2. Kies **Beheren** > **Profielen** op de blade **Apparaatconfiguratie**.
3. Kies **Profiel maken** op de blade Profielen.
4. Voer op de blade **Profiel maken** een **naam** en **beschrijving** in voor het profiel voor de apparaatfuncties.
5. Selecteer in de vervolgkeuzelijst **Platform** de optie **Windows 10 en hoger**.
6. Kies **Endpoint Protection** in de vervolgkeuzelijst **Profieltype**. 
7. Op de blade **Windows-versleuteling** kunt u de gewenste instellingen configureren. Gebruik de informatie in dit onderwerp om te begrijpen wat elke instelling doet. Als u klaar bent, kiest u **OK**.
8. Ga terug naar de blade **Profiel maken** en kies **Maken**.

Het profiel wordt gemaakt en wordt weergegeven op de blade met de profielenlijst.

## <a name="endpoint-protection-profile-settings-reference"></a>Naslaginformatie voor profiel voor eindpuntbeveiliging

### <a name="windows-settings"></a>Windows-instellingen

- **Vereisen dat apparaten worden versleuteld (alleen desktop)**: als deze instelling is ingeschakeld, krijgen gebruikers opdracht om apparaatversleuteling in te schakelen. Bovendien moeten ze bevestigen dat er geen versleuteling van een andere provider is ingeschakeld. Als Windows-versleuteling is ingeschakeld terwijl een andere versleutelingsmethode actief is, wordt het apparaat mogelijk instabiel.
- **Vereisen dat de opslagkaart wordt versleuteld (alleen mobiel)**: schakel deze instelling in om verwijderbare opslagkaarten die door het apparaat worden gebruikt te versleutelen.


### <a name="bitlocker-base-settings"></a>Basisinstellingen voor BitLocker

- **Versleutelingsmethoden configureren**: schakel deze instelling in om versleutelingsalgoritmen te configureren voor het besturingssysteem, gegevens en verwisselbare stations.
    - **Versleuteling voor stations met besturingssysteem**: kies de versleutelingsmethode stations met een besturingssysteem. Het is raadzaam om het algoritme XTS AES te gebruiken.
    - **Versleuteling voor vaste gegevensschijven**: kies de versleutelingsmethode voor vaste (ingebouwde) schijven, ook wel 'harde schijven' genoemd. Het is raadzaam om het algoritme XTS AES te gebruiken.
    - **Versleuteling voor verwisselbare gegevensstations**: kies de versleutelingsmethode voor verwisselbare gegevensstations. Als het verwisselbare station wordt gebruikt met apparaten waarop Windows 10 niet wordt uitgevoerd, raden we aan om het algoritme AES-CBC te gebruiken.


### <a name="bitlocker-os-drive-settings"></a>BitLocker-instellingen voor station met besturingssysteem

- **Aanvullende verificatie bij opstarten vereisen** - 
    - **BitLocker blokkeren op apparaten zonder een compatibele TPM-chip** - 
    - **TPM opstarten**: configureer of de TPM-chip is toegestaan, niet is toegestaan of is vereist. 
    - **TPM-opstartpincode**: configureer of het gebruiken van een TPM-opstartpincode met de TPM-chip is toegestaan, niet is toegestaan of is vereist. 
    - **TPM-opstartsleutel**: configureer of het gebruiken van een TPM-opstartsleutel met de TPM-chip is toegestaan, niet is toegestaan of is vereist. 
    - **Opstartsleutel en pincode voor TPM**: configureer of het gebruiken van een opstartsleutel en pincode voor TPM met de TPM-chip is toegestaan, niet is toegestaan of is vereist.
- **Minimale lengte pincode**: schakel deze instelling in om een minimale lengte te configureren voor de TPM-opstartpincode.
    - **Minimum aantal tekens**: geef het aantal tekens op dat is vereist voor de opstartpincode, tussen **4**-**20**.
- **Herstellen van OS-station inschakelen**: schakel deze instelling in om te bepalen hoe met BitLocker beveiligde besturingssysteemstations worden hersteld als de vereiste opstartgegevens niet beschikbaar zijn.
    - **Agent voor herstel van gegevens op basis van een certificaat toestaan**: schakel deze instelling in als agenten voor gegevensherstel mogen worden gebruikt met besturingssysteemstations die met BitLocker zijn beveiligd.
    - **Herstelwachtwoord maken door gebruiker**: hiermee configureert u of gebruikers verplicht of optioneel een herstelwachtwoord van 48 cijfers mogen genereren, of dat dit niet is toegestaan.
    - **Herstelsleutel maken door gebruiker**: hiermee configureert u of gebruikers verplicht of optioneel een herstelsleutel van 256 bits mogen genereren, of dat dit niet is toegestaan.
    - **Herstelopties verbergen in de BitLocker-installatiewizard**: schakel deze instelling in om te voorkomen dat gebruikers herstelopties zien of deze kunnen wijzigen wanneer ze BitLocker inschakelen.
    - **BitLocker-herstelgegevens naar AD DS opslaan**: hiermee schakelt u de opslag van BitLocker-herstelgegevens in Active Directory in.
    - **Opslag van BitLocker-herstelgegevens naar AD DS configureren**: hiermee bepaalt u welke onderdelen van BitLocker-herstelgegevens worden opgeslagen in Active Directory. U kunt kiezen uit:
        - **Back-up maken van herstelwachtwoorden en sleutelpakketten**
        - **Alleen een back-up maken van herstelwachtwoorden**
    - **Vereisen dat herstelgegevens worden opgeslagen in AD DS voordat BitLocker wordt ingeschakeld**: schakel deze instelling in om te voorkomen dat gebruikers BitLocker inschakelen, tenzij het apparaat lid is van een domein en BitLocker-herstelgegevens met succes zijn opgeslagen in Active Directory.
- **Preboot-herstelbericht en -URL inschakelen**: schakel deze instelling in om het bericht en de URL te configureren die worden weergegeven op het preboot-scherm voor sleutelherstel.
    - **Preboot-herstelbericht**: configureer hoe preboot-herstelbericht wordt weergegeven aan gebruikers. U kunt kiezen uit:
        - **Standaardherstelbericht en URL gebruiken**
        - **Leeg herstelbericht en -URL gebruiken**
        - **Aangepaste herstelbericht gebruiken**
        - **Aangepaste herstel-URL gebruiken**


### <a name="bitlocker-fixed-data-drive-settings"></a>BitLocker-instellingen voor vaste-gegevensstations

- **Toegang voor schrijven naar vaste-gegevensstations weigeren wanneer deze niet door BitLocker zijn beveiligd**: als deze instelling is ingeschakeld, moet BitLocker-beveiliging zijn ingeschakeld voor alle vaste of ingebouwde gegevensstations om gegevens te kunnen wegschrijven naar die stations.
- **Vast-stationherstel inschakelen**: schakel deze instelling in om te bepalen hoe met BitLocker beveiligde vaste schijven worden hersteld als de vereiste opstartgegevens niet beschikbaar zijn.
    - **Agent voor gegevensherstel toestaan**: schakel deze instelling in als agenten voor gegevensherstel mogen worden gebruikt met vaste schijven die met BitLocker zijn beveiligd.
    - **Herstelwachtwoord maken door gebruiker**: hiermee configureert u of gebruikers verplicht of optioneel een herstelwachtwoord van 48 cijfers mogen genereren, of dat dit niet is toegestaan.  
    - **Herstelsleutel maken door gebruiker**: hiermee configureert u of gebruikers verplicht of optioneel een herstelsleutel van 256 bits mogen genereren, of dat dit niet is toegestaan.
    - **Herstelopties verbergen in de BitLocker-installatiewizard**: schakel deze instelling in om te voorkomen dat gebruikers herstelopties zien of deze kunnen wijzigen wanneer ze BitLocker inschakelen.
    - **BitLocker-herstelgegevens naar AD DS opslaan**: hiermee schakelt u de opslag van BitLocker-herstelgegevens in Active Directory in.
    - **Opslag van BitLocker-herstelgegevens naar AD DS configureren**: hiermee bepaalt u welke onderdelen van BitLocker-herstelgegevens worden opgeslagen in Active Directory. U kunt kiezen uit:
        - **Back-up maken van herstelwachtwoorden en sleutelpakketten**
        - **Alleen een back-up maken van herstelwachtwoorden**
    - **Vereisen dat herstelgegevens worden opgeslagen in AD DS voordat BitLocker wordt ingeschakeld**: schakel deze instelling in om te voorkomen dat gebruikers BitLocker inschakelen, tenzij het apparaat lid is van een domein en BitLocker-herstelgegevens met succes zijn opgeslagen in Active Directory.


### <a name="bitlocker-removable-data-drive-settings"></a>BitLocker-instellingen voor verwisselbare gegevensstations

- **Schrijftoegang weigeren voor een verwisselbaar gegevensstation dat niet door BitLocker is beveiligd**: geef op of BitLocker-versleuteling is vereist voor verwijderbare opslagstations.
    - **Schrijftoegang blokkeren voor apparaten die in een andere organisatie zijn geconfigureerd**: geef op of gegevens mogen worden weggeschreven naar verwisselbare gegevensstations die deel uitmaken van een andere organisatie.



## <a name="next-steps"></a>Volgende stappen

Zie [How to assign device profiles](device-profile-assign.md) (Apparaatprofielen toewijzen) als u wilt doorgaan en dit profiel wilt toewijzen aan groepen.


