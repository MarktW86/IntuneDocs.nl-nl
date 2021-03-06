---
title: Aan de slag met beleid
titleSuffix: Intune on Azure
description: 
keywords: 
author: barlanmsft
ms.author: barlan
manager: angrobe
ms.date: 06/27/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 1ac74ba5-7441-44ac-98b5-9d8bb8899747
ms.reviewer: 
ms.suite: ems
ms.custom: intune-azure
ms.openlocfilehash: 232ec25c34df5e71f70737ca5f0f8a2ef12a05f0
ms.sourcegitcommit: fd2e8f6f8761fdd65b49f6e4223c2d4a013dd6d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/03/2017
---
# <a name="getting-started-with-policies"></a>Aan de slag met beleid

Eén van de belangrijkste redenen om te kiezen voor Intune is de registratie van apparaten, om ervoor te zorgen dat deze voldoen aan het bedrijfsbeleid. Nalevingsbeleid is niet alleen handig bij het beheren van gespecialiseerde apparaattypen, zoals kiosken in bedrijfseigendom, maar ook van persoonlijke apparaten (BYOD), tablets en apparaten zonder gebruiker.

![Dashboard voor compatibiliteit met erg weinig gegevens](/intune/media/generic-compliance-dashboard.png)

Nalevingsbeleid biedt de volgende beheermogelijkheden voor mobiele apparaten:

* Reguleren van het aantal apparaten dat een gebruiker inschrijft
* Beheren van apparaatinstellingen (zoals versleuteling op apparaatniveau, wachtwoordlengte en cameragebruik)
* Het leveren van apps, e-mailprofielen, VPN-profielen, enzovoort.
* Evalueren van criteria op apparaatniveau op naleving van beveiligingsbeleid

U stelt voor elk platform afzonderlijk nalevingsbeleid op. In dit voorbeeld hebben we gekozen voor iOS. De volgende beleidsregels zijn beschikbaar voor iOS-apparaten:

* Configuratie van de pincode of het wachtwoord
* Apparaatversleuteling
* Jailbreaking van apparaat
* E-mailprofiel
* Minimale versie van het besturingssysteem
* Maximale versie van het besturingssysteem

__Hoe maak ik een beleid?__

1. Meld u aan bij [Azure Portal](https://portal.azure.com).
2. Gebruik **Resources zoeken** om te zoeken naar **Intune**.
3. Selecteer **Apparaatnaleving**.
4. Selecteer **Beleidsregels** op de blade **Apparaatnaleving**.
5. Selecteer **Beleid maken** en geef de details op, zoals waarden voor **Naam** en **Beschrijving**. Kies **iOS** bij **Platform**.
6. Ga naar **Instellingen**, selecteer **Systeembeveiliging** en zet **Wachtwoord vereisen voor het ontgrendelen van mobiele apparaten** op **Vereisen**. U kunt ook andere regels instellen, zoals **Minimale wachtwoordlengte**, **Vereist wachtwoordtype** en **Het minimumaantal niet-alfanumerieke tekens in een wachtwoord**. Als u tevreden bent over het beleid, selecteert u **OK**.
7. Ga terug naar de blade **Beleid maken** en selecteer **Maken**.
8. Als het beleid is gemaakt, selecteert u **Toewijzingen** om het beleid toe te wijzen aan uw testgroep. Selecteer de testgroep (deze moet uw testgebruiker bevatten) en wijs het beleid toe aan die groep door op **Opslaan** te klikken.
9. Als het goed is, verschijnt er na een paar minuten een bericht met het verzoek om een nieuw wachtwoord in te stellen voor het apparaat om te blijven voldoen aan het bedrijfsbeleid. U kunt dit ook handmatig controleren in de **bedrijfsportal-app voor iOS** door op de naam van het apparaat te tikken en vervolgens op de knop **Synchroniseren**.
