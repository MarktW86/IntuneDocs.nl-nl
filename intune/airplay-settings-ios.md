---
title: Intune AirPlay-instellingen voor iOS-apparaten
titleSuffix: Intune on Azure
description: In dit onderwerp leest u hoe u met Intune automatisch iOS-apparaten kunt verbinden met AirPlay- compatibele apparaten.
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 712a79fb-14ef-4f6b-aba5-1dfca900afd2
ms.reviewer: karanda
ms.suite: ems
ms.custom: intune-azure
ms.openlocfilehash: 7e44c1d438fc5782d696cba0b39c3c4d65492096
ms.sourcegitcommit: c9b3a95bf529b6cb2a2bdacbc49127dfa0c233e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/05/2017
---
# <a name="intune-airplay-settings-for-ios-devices"></a>Intune AirPlay-instellingen voor iOS-apparaten

[!INCLUDE[azure_portal](./includes/azure_portal.md)]

Gebruik deze instellingen om iOS-apparaten die u beheert te verbinden met AirPlay-compatibele apparaten (zoals Apple TV's) in uw netwerk.
Met deze functie kunt u het volgende doen:

- **Een lijst met apparaten en wachtwoorden configureren**: hiermee kunnen gebruikers automatisch verbinding maken met AirPlay-apparaten die zich binnen bereik bevinden. Richt ze in met de naam en het wachtwoord van AirPlay-apparaten, zodat deze niet hoeven op te geven wanneer ze verbinding maken.
- **Toegestane bestemmingen configureren**: Een lijst met AirPlay-apparaten configureren (op apparaat-id). Eindgebruikers zien alleen de door u vermelde apparaten en kunnen alleen met deze apparaten verbinding maken (alleen voor apparaten onder supervisie).

## <a name="get-started"></a>Aan de slag

1. Kies op de blade **Apparaatfuncties** het item **AirPlay**.
2. Kies op de blade **AirPlay** een of beide van de volgende acties:

## <a name="configure-a-device-and-password-list"></a>Een apparaat- en een wachtwoordenlijst configureren

1. Voer op de blade **Wachtwoorden** de **Apparaatnaam** en het **Wachtwoord** in van een AirPlay-apparaat, bijvoorbeeld **Contoso Apple TV**.
2. Na het invoeren van de apparaatdetails klikt u op **Toevoegen**. Het apparaat wordt weergegeven in de lijst **Apparaatnaam**.
3. Ga door naar het toevoegen van apparaten. Als u klaar bent, kiest u **OK**.


## <a name="configure-allowed-destinations"></a>Toegestane bestemmingen configureren

1. Voer op de blade **Toegestane doelen (alleen onder supervisie)** de **Apparaat-id** van een AirPlay-apparaat in, bijvoorbeeld 52:46:CD:51:83:4 C.
2. Na het invoeren van de apparaat-ID klikt u op **Toevoegen**. De id wordt weergegeven in de lijst **Apparaat-id**.
3. Ga door naar het toevoegen van apparaten. Als u klaar bent, kiest u **OK**.

U kunt apparaten, wachtwoorden en toegestane bestemmingen ook importeren uit een bestand met door komma's gescheiden waarden (csv).


## <a name="next-steps"></a>Volgende stappen

U kunt het apparaatprofiel nu toewijzen aan de gewenste groepen. Zie [Apparaatprofielen toewijzen](device-profile-assign.md) voor meer informatie.

