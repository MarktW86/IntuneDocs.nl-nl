---
title: Android-Line-Of-Business-apps toevoegen aan Intune
titleSuffix: Intune on Azure
description: In dit onderwerp vindt u meer informatie over het toevoegen van Android-Line-Of-Business-apps aan Intune."
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 04/12/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 061d793c-c724-4cd9-9240-adb0cbda5661
ms.reviewer: mghadial
ms.suite: ems
ms.custom: intune-azure
ms.openlocfilehash: 52a762e0d8990ab96053f5d3a092b3731ee00ca0
ms.sourcegitcommit: 34cfebfc1d8b81032f4d41869d74dda559e677e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2017
---
# <a name="how-to-add-android-line-of-business-lob-apps-to-microsoft-intune"></a>Android-Line-Of-Business-apps (LOB) toevoegen aan Microsoft Intune

[!INCLUDE[azure_portal](./includes/azure_portal.md)]


## <a name="step-1---specify-the-software-setup-file"></a>Stap 1: de locatie van het software-installatiebestand opgeven

1. Meld u aan bij Azure Portal.
2. Kies **Meer services** > **Bewaking en beheer** > **Intune**.
3. Kies **Apps beheren** op de blade **Intune**.
4. Kies **Beheren** > **Apps** in de workload **Mobiele apps**.
5. Kies **Toevoegen** boven de lijst met apps.
6. Kies **Line-Of-Business-app** in de blade **App toevoegen**.

## <a name="step-2---configure-the-app-package-file"></a>Stap 2: het pakketbestand van de app configureren

1. Kies **Installatiebestand** op de blade **App toevoegen**.
2. Klik op de blade **Installatiebestand** op de bladerknop en selecteer een Android-installatiebestand met de extensie **.apk**.
3. Als u klaar bent, kiest u **OK**.


## <a name="step-3---configure-app-information"></a>Stap 3: de app-gegevens configureren

1. Kies **Installatiebestand** op de blade **App toevoegen**.
2. Configureer de volgende gegevens op de blade **App-gegevens**. Afhankelijk van de app die u hebt gekozen, worden bepaalde waarden op deze blade mogelijk automatisch ingevuld:
    - **Naam**: voer de naam van de app in zoals deze in de bedrijfsportal zal worden weergegeven. Zorg ervoor dat alle app-namen die u gebruikt, uniek zijn. Als dezelfde app-naam twee keer voorkomt, wordt slechts één van de apps weergegeven voor gebruikers in de bedrijfsportal.
    - **Beschrijving**: voer een beschrijving in voor de app. Deze wordt weergegeven voor gebruikers in de bedrijfsportal.
    - **Uitgever**: voer de naam van de uitgever of de app in.
    - **Minimumversie van het besturingssysteem**: selecteer in de lijst de minimumversie van het besturingssysteem waarin de app kan worden geïnstalleerd. Als u de app toewijst aan een apparaat met een lager besturingssysteem, wordt de app niet geïnstalleerd.
    - **Categorie**: selecteer een of meer van de ingebouwde app-categorieën of selecteer een categorie die u hebt gemaakt. Hierdoor kunnen gebruikers de app gemakkelijker vinden wanneer ze door de bedrijfsportal bladeren.
    - **Deze weergeven als aanbevolen app in de bedrijfsportal**: hiermee wordt de app duidelijk zichtbaar op de startpagina van de bedrijfsportal wanneer gebruikers naar apps zoeken.
    - **Informatie-URL**: voer de URL in van een website die informatie over deze app bevat (optioneel). Deze URL wordt weergegeven voor gebruikers in de bedrijfsportal.
    - **Privacy-URL**: voer de URL in van een website die privacyinformatie over deze app bevat (optioneel). Deze URL wordt weergegeven voor gebruikers in de bedrijfsportal.
    - **Ontwikkelaar**: voer de naam in van de app-ontwikkelaar (optioneel).
    - **Eigenaar**: voer een naam in voor de eigenaar van deze app, bijvoorbeeld **HR-afdeling** (optioneel).
    - **Opmerkingen**: voer de opmerkingen in die u aan deze app wilt koppelen.
    - **Logo**: upload een pictogram dat aan de app wordt gekoppeld. Dit is het pictogram dat samen met de app wordt weergegeven wanneer gebruikers door de bedrijfsportal bladeren.
3. Als u klaar bent, kiest u **OK**.

## <a name="step-4---finish-up"></a>Stap 4: afronden

1. Controleer op de blade **App toevoegen** of de gegevens die u hebt geconfigureerd correct zijn.
2. Kies **Toevoegen** om de app te uploaden naar Intune.

De app die u hebt gemaakt, wordt weergegeven in de lijst met apps waar u de app kunt toewijzen aan de groepen die u kiest. Zie [Apps aan groepen toewijzen](apps-deploy.md) voor hulp.
