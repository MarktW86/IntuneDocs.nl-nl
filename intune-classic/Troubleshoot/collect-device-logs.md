---
title: Apparaatlogboeken verzamelen
description: Informatie over het verzamelen van logboeken van uw beheerde apparaten.
keywords: 
author: arob98
ms.author: angrobe
manager: angrobe
ms.date: 02/07/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: d97fb610-9d88-40e5-bb06-447eec533630
ms.reviewer: esmich
ms.suite: ems
ms.custom: intune-classic
ms.openlocfilehash: b15e4b7fa0c650a85a080c42d00cd75cb8783c62
ms.sourcegitcommit: 34cfebfc1d8b81032f4d41869d74dda559e677e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2017
---
# <a name="device-logs"></a>Apparaatlogboeken

[!INCLUDE[classic-portal](../includes/classic-portal.md)]

Het is mogelijk dat u in het kader van uw inspanning op het gebied van probleemoplossing ook logboeken van gebruikersapparaten wilt verzamelen. De instructies voor het verzamelen van deze logboeken worden hier beschreven. Normaal gesproken hebt u hiervoor toegang tot het apparaat nodig of moet u de gebruiker vragen de logboeken te verzamelen en naar u te verzenden.

### <a name="android-logs"></a>Android-logboeken
De Android-logboeken bevinden zich in *<Android Device>\Phone\Android\data\com.microsoft.windowsintune.companyportal\files*.

Soms zijn de bestanden niet zichtbaar, met name op nieuwere Android-apparaten. Als dit het geval is, vraagt u uw gebruikers de bedrijfsportal-app voor Android te openen. Vervolgens moeten ze **Instellingen**>**Logboeken kopiëren** kiezen en hun apparaat opnieuw opstarten.

Zie de volgende artikelen voor meer informatie over hoe uw gebruikers u gegevenslogboeken kunnen sturen:

- [Uitgebreide logboekregistratie gebruiken zodat de IT-beheerder problemen met het apparaat kan oplossen](/intune-user-help/use-verbose-logging-to-help-your-it-administrator-fix-device-issues-android): beschrijft hoe gebruikers uitgebreide logboekregistratie kunnen inschakelen, waardoor automatisch al hun gegevenslogboeken naar u worden verzonden. Uitgebreide logboekregistratie is standaard ingeschakeld.

- [Android-logboeken met diagnostische gegevens naar de IT-beheerder verzenden via e-mail](/intune-user-help/send-logs-to-your-it-admin-by-email-android)

- [Logboeken met diagnostische gegevens naar de IT-beheerder verzenden met een USB-kabel](/intune-user-help/send-diagnostic-data-logs-to-your-it-administrator-using-a-usb-cable-android)

### <a name="ios-logs"></a>iOS-logboeken

Gebruikers kunnen u registratiefouten verzenden, zoals wordt beschreven in [iOS-registratiefouten verzenden naar de IT-beheerder](/intune-user-help/send-errors-to-your-it-admin-ios).

Gebruikers kunnen apparaatlogboeken verzenden, zoals beschreven in [Logboeken verzenden naar de bedrijfsportal-ontwikkelaars voor iOS-apparaten](/intune-user-help/send-logs-to-microsoft-ios).

### <a name="mac-os-x-logs"></a>Mac OS X-logboeken

1. Open de app **Console**.
2. Kies bij **BESTANDEN** de optie **system.log**.
3. Kies in de menubalk boven aan het scherm **Bestand** > **Een kopie opslaan als...**. Sla het bestand vervolgens op.

### <a name="windows-phone"></a>Windows Phone

In de bedrijfsportal-app voor Windows Phone kiezen gebruikers de drie puntjes (**...**) om het menu te openen en kiezen vervolgens **Logboeken verzenden**. Deze optie is beschikbaar zowel voor- als nadat u zich bij de bedrijfsportal-app hebt aangemeld.

### <a name="windows"></a>Windows

Voor de Windows-bedrijfsportal bevinden de logboeken zich in *%localappdata%\Packages\Microsoft.CompanyPortal_8wekyb3d8bbwe\LocalState*.
