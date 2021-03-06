---
title: Aangepaste Intune-instellingen voor macOS-apparaten
titleSuffix: Intune on Azure
description: Meer informatie over de instellingen die u kunt gebruiken in een aangepast MacOS-profiel.
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 05/04/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 68100ea5-7d9b-4c0b-8df7-b9a24b2442c8
ms.reviewer: heenamac
ms.suite: ems
ms.custom: intune-azure
ms.openlocfilehash: 57c4ec3621ffaef5c1aaffd55c87baac91e50154
ms.sourcegitcommit: 34cfebfc1d8b81032f4d41869d74dda559e677e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2017
---
# <a name="custom-settings-for-macos-devices-in-microsoft-intune"></a>Aangepaste instellingen voor macOS-apparaten in Microsoft Intune

[!INCLUDE[azure_portal](./includes/azure_portal.md)]

Gebruik het aangepaste macOS-profiel van Microsoft Intune om instellingen die u met het hulpprogramma [Apple Configurator](https://itunes.apple.com/app/apple-configurator-2/id1037126344?mt=12) hebt gemaakt, toe te wijzen aan macOS-apparaten. Met dit hulpprogramma kunt u veel instellingen configureren die de werking van deze apparaten regelen, en deze instellingen exporteren naar een configuratieprofiel. U kunt dit configuratieprofiel vervolgens importeren naar een aangepast Intune macOS-profiel en de instellingen toewijzen aan gebruikers en apparaten in uw organisatie.

Op deze manier kunt u macOS-instellingen toewijzen die u niet kunt configureren met andere Intune-profieltypen.


1. Volg de instructies in [Aangepaste apparaatinstellingen configureren in Microsoft Intune](custom-settings-configure.md) om aan de slag te gaan.
2. Geef de volgende informatie op de blade **Profiel maken** op:

- **Aangepaste configuratieprofielnaam**: geef een naam op voor het beleid, zoals het moet worden weergegeven op het apparaat en in de Intune-status.
- **Configuratieprofielbestand**: blader naar het configuratieprofiel dat u hebt gemaakt met Apple Configurator.
Controleer of de instellingen die u vanuit het hulpprogramma Apple Configurator exporteert compatibel zijn met de macOS-versie op de apparaten waarop u het aangepaste macOS-beleid toewijst. Als u meer wilt weten over het oplossen van problemen bij incompatibele instellingen, zoekt u op de [Apple Developer](https://developer.apple.com/)-website naar **Configuration Profile Reference** (naslag voor configuratieprofielen) en **Mobile Device Management Protocol Reference** (naslag voor beheerprotocol voor mobiele apparaten).

Het bestand dat u hebt geïmporteerd, wordt weergegeven in het gebied **Bestandsinhoud** van de blade.
