---
# required metadata

title: Nalevingsbeleid implementeren en bewaken in Microsoft Intune | Microsoft Intune
description:
keywords:
author: karthikaraman
manager: jeffgilb
ms.date: 04/28/2016
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: d8f246d4-0d86-4c8b-a1bf-9977985506d8

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: jeffgilb
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Nalevingsbeleid voor apparaten implementeren en bewaken in Microsoft Intune
## Een nalevingsbeleid implementeren
Implementeer het nalevingsbeleid dat u hebt [gemaakt](create-a-device-compliance-policy-in-microsoft-intune.md) voor een of meer groepen van gebruikers of apparaten in uw organisatie.

1.  Selecteer het beleid dat u wilt implementeren in de werkruimte **Beleid** en kies vervolgens **Implementatie beheren**..
![Schermafbeelding van de pagina voor het nalevingsbeleid waarin boven de menuoptie Implementatie beheren wordt weergegeven](./media/intune-sa-3c-deploy-compliance-policy2.png)

2.  Kies in het dialoogvenster **Implementatie beheren** een of meer groepen waarvoor u het beleid wilt implementeren en kies vervolgens **Toevoegen > OK**.
![Schermafbeelding van het dialoogvenster Implementatie beheren](./media/intune-sa-3d-deploy-compliance-policy3-Manage.png)
U kunt nalevingsbeleid implementeren voor gebruikers en/of apparaten. Gebruik Active Directory-groepen die u al hebt gemaakt en met Intune hebt gesynchroniseerd, of maak deze groepen handmatig in de Intune-console. Zie [Configuratiebeleid implementeren](manage-settings-and-features-on-your-devices-with-microsoft-intune-policies.md) voor meer informatie over het implementeren van beleid.

Gebruik het statusoverzicht en de waarschuwingen op de pagina **Overzicht** van de werkruimte **Beleid** om beleidsproblemen te identificeren die uw aandacht vereisen. Bovendien wordt er een statusoverzicht weergegeven in de werkruimte **Dashboard** .

> [!IMPORTANT]Als u geen nalevingsbeleid hebt geïmplementeerd en daarna een Exchange-beleid voorwaardelijke toegang inschakelt, krijgen alle apparaten uit de doelgroep toegang.

## Oplossen van Intune-beleidsconflicten
Conflicterende beleidsinstellingen kunnen zich voordoen wanneer er meerdere Intune-beleidsregels op een apparaat worden toegepast. Als de beleidsinstellingen elkaar overlappen, lost Intune de conflicten aan de hand van de volgende regels op:

-   Als de conflicterende instellingen uit een Intune-configuratiebeleid en een nalevingsbeleid voortkomen, hebben de instellingen in het nalevingsbeleid prioriteit boven de instellingen in het configuratiebeleid, zelfs als de instellingen in het configuratiebeleid veiliger zijn.

-   Als u meerdere nalevingsbeleidsregels hebt geïmplementeerd, wordt de veiligste beleidsregel gebruikt.

## Het nalevingsbeleid bewaken

#### Apparaten weergeven die niet voldoen aan een nalevingsbeleid

1.  Kies in de [Microsoft Intune-beheerconsole](https://manage.microsoft.com) achtereenvolgens **Groepen > Alle apparaten**.

2.  Dubbelklik op de naam van een apparaat in de lijst met apparaten.

3.  Kies het tabblad **Beleid** om een lijst met de beleidsregels voor dat apparaat weer te geven.

4.  Selecteer in de vervolgkeuzelijst **Filters** de optie **Voldoet niet aan nalevingsbeleid**.
![Schermafbeelding van de lijst met opties in de lijst met filters](./media/intune-sa-3e-view-device-noncompliance.png)

#### Health Attestation-rapporten weergeven

1.  Kies in de [Microsoft Intune-beheerconsole](https://manage.microsoft.com) de optie **Rapporten**.

2.  Op de pagina **Health Attestation-rapporten - een nieuw rapport maken** kunt u een rapport bekijken met alle Health Attestation-gegevens van Windows 10 die door Intune zijn verzameld. Met de filters kunt u ook een rapport maken met een subset van de gegevens. De filters kunnen worden gebaseerd op het type apparaat, op het besturingssysteem of op een subset van gegevenspunten.


## Volgende stappen
U kunt het nalevingsbeleid nu gebruiken met beleidsregels voor voorwaardelijke toegang om zo de toegang tot services in uw organisatie te beheren.

[De toegang tot e-mail en O365-services beperken](restrict-access-to-email-and-o365-services-with-microsoft-intune.md)


### Zie tevens
[Inleiding in nalevingsbeleid voor apparaten in Intune](introduction-to-device-compliance-policies-in-microsoft-intune.md)


<!--HONumber=May16_HO1-->

