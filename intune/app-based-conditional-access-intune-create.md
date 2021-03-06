---
title: Op apps gebaseerd beleid voor voorwaardelijke toegang met Intune
description: In dit onderwerp wordt beschreven hoe u met Intune op apps gebaseerd beleid voor voorwaardelijke toegang kunt configureren.
keywords: 
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 06/28/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: d1693515-de18-4553-91ef-801976cd3ec7
ms.reviewer: chrisgre
ms.suite: ems
ms.custom: intune-azure
ms.openlocfilehash: a7f054868d0bae061f348239614f3a40b96a15b1
ms.sourcegitcommit: fd2e8f6f8761fdd65b49f6e4223c2d4a013dd6d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/03/2017
---
# <a name="set-up-app-based-conditional-access-policies"></a>Op apps gebaseerd beleid voor voorwaardelijke toegang instellen

[!INCLUDE[azure_portal](./includes/azure_portal.md)]

In dit onderwerp vindt u instructies voor het instellen van op apps gebaseerd beleid voor voorwaardelijke toegang voor apps die deel uitmaken van de lijst met goedgekeurde apps. De lijst met goedgekeurde apps bestaat uit apps die zijn getest door Microsoft.

> [!IMPORTANT]
> In dit onderwerp worden de stappen beschreven voor het toevoegen van een op apps gebaseerd beleid voor voorwaardelijke toegang met behulp van Exchange Online. U kunt dezelfde stappen echter gebruiken voor het toevoegen van andere apps uit de lijst met goedgekeurde apps, zoals SharePoint Online en Microsoft Teams.

## <a name="to-create-an-app-based-conditional-access-policy"></a>Op apps gebaseerd beleid voor voorwaardelijke toegang maken
1.  Ga naar [Azure Portal](https://portal.azure.com) en meld u aan met uw referenties.

2.  Kies **Meer services** en typ Intune.

3.  Kies **Intune-app-beveiliging**.

4.  Kies in de blade **Intune Mobile Application Management** de optie **Alle instellingen**.

5.  Kies in de sectie **Voorwaardelijke toegang** de optie **Exchange Online**.

    ![Schermafdruk van de blade Instellingen met de sectie voor voorwaardelijke toegang met de optie Exchange Online gemarkeerd](./media/MAM-conditional-access-1.png)

6. Kies in de blade **Toegestane apps** de optie **Apps met ondersteuning voor Intune-beleid toestaan** als alleen apps met ondersteuning voor Intune beveiligingsbeleid voor apps toegang mogen hebben tot Exchange Online. Wanneer u deze optie selecteert, wordt de lijst met ondersteunde apps weergegeven.

    > [!NOTE]
    > Alle Exchange Active Sync-e-mailclients, met inbegrip van de ingebouwde e-mailclients op iOS en Android die verbinding met Exchange Online maken, kunnen geen e-mail verzenden of ontvangen. In plaats daarvan ontvangen gebruikers één e-mailbericht dat ze de Outlook-e-mail-app moeten gebruiken.

7. Als u dit beleid wilt toepassen op gebruikers, opent u de blade **Beperkte gebruikersgroepen** en kiest u **Gebruikersgroep toevoegen**. Selecteer een of meer gebruikersgroepen waarop u dit beleid wilt toepassen.

    ![Schermafbeelding van de blade Beperkte gebruikersgroepen met de optie Gebruikersgroep toevoegen gemarkeerd](./media/mam-ca-add-user-group.png)

8. Mogelijk wilt u dat dit beleid niet wordt toegepast op bepaalde gebruikers in de gebruikersgroep die u in de vorige stap hebt geselecteerd. In dat geval voegt u die gebruikersgroepen toe aan de lijst met uitgesloten gebruikersgroepen. Kies in de blade **Exchange Online** de optie **Uitgesloten gebruikersgroepen**. Kies **Gebruikersgroep toevoegen** om de lijst met gebruikersgroepen te openen. Selecteer de groepen die u van dit beleid wilt uitsluiten.

## <a name="to-modify-or-delete-user-groups-from-an-existing-app-based-ca-policy"></a>Gebruikersgroepen aanpassen of verwijderen op basis van bestaand CA-beleid op basis van apps

1. Open de blade **Beperkte gebruikersgroepen** en markeer de gebruikersgroep die u wilt verwijderen.
2. Klik op de knop met weglatingstekens om de opties voor verwijderen weer te geven.
3. Kies **Verwijderen** om de gebruikersgroep uit de lijst te verwijderen.

## <a name="next-steps"></a>Volgende stappen
[Apps die geen gebruik maken van moderne verificatie blokkeren](app-modern-authentication-block.md)

### <a name="see-also"></a>Zie tevens

[Beveilig app-gegevens met beveiligingsbeleid voor apps](app-protection-policies.md)
