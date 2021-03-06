---
title: Inleiding tot Intune in Azure Portal
titleSuffix: Intune on Azure
description: Een overzicht van de basisbeginselen van Intune in Azure Portal en hoe u hiermee uw apparaten kunt beheren."
keywords: 
author: robstackmsft
ms.author: robstack
nmanager: angrobe
ms.date: 07/17/2017
ms.topic: get-started-article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 4a085264-232a-4af0-97f1-747496c44517
ms.suite: ems
ms.custom: 
ms.openlocfilehash: a51b3c59d922b0c150073017222dca0c90c5b7a0
ms.sourcegitcommit: 36ae73f59ff5e9fdfe4f930ad0aa4b7795fe11f2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/18/2017
---
# <a name="introduction-to-microsoft-intune-in-the-azure-portal"></a>Inleiding op Microsoft Intune in Azure Portal


[!INCLUDE[azure_portal](./includes/azure_portal.md)]

Microsoft Intune bevindt zich nu in Azure Portal. Dit betekent dat de werkstromen en functionaliteit waarmee u bekend bent, zijn veranderd.
De nieuwe portal biedt u nieuwe en bijgewerkte functionaliteit in Azure Portal waar u de mobiele apparaten, pc's en apps van uw bedrijf kunt beheren.

* In [Waar is de functie die ik zoek gebleven in Azure?](ui-changes.md) kunt u nazoeken welke specifieke werkstromen en gebruiksinterfaces zijn veranderd bij de overgang naar Azure.
* In [Klassieke Intune-groepen in Azure Portal](groups-get-started.md) worden de gevolgen uitgelegd van de overstap naar Azure Active Directory-beveiligingsgroepen voor groepsbeheer.




Informatie over de nieuwe portal vindt u in deze bibliotheek. Deze wordt voortdurend bijgewerkt. Als u suggesties hebt, kunt u feedback geven in de opmerkingen bij onderwerpen. We graag horen van u.

Belangrijke functies van de nieuwe omgeving zijn onder andere:

- Een geïntegreerde console voor al uw Enterprise Mobility + Security-onderdelen (EMS)
- Een console op basis van HTML die is gebouwd op webstandaarden
- Ondersteuning van Microsoft Graph API om veel acties te automatiseren
- Azure Active Directory-groepen (AD) voor compatibiliteit voor al uw Azure-toepassingen
- Ondersteuning voor de meeste moderne webbrowsers

> [!IMPORTANT]
> **Ziet u de nieuwe portal nog niet?**<br>
> Bestaande tenants worden gemigreerd naar de nieuwe ervaring. Voordat uw tenant wordt gemigreerd, wordt in het berichtencentrum Office een melding weergegeven.
>
> Intune-accounts die vóór januari 2017 zijn gemaakt, moeten eenmalig worden gemigreerd om de Apple-registratiewerkstromen in Azure beschikbaar te maken. De planning voor de migratie is nog niet aangekondigd. Als uw bestaande account geen toegang heeft tot Azure Portal, wordt u aangeraden een proefaccount maken.
>
> Bekijk de lijst met potentiële problemen https://blogs.technet.microsoft.com/intunesupport/2017/05/17/intune-migration-blockers-for-grouping-targeting/


## <a name="before-you-start"></a>Voordat u begint

U moet een Intune-beheerder- en tenant-account hebben voor het gebruik van Intune in de Azure Portal. [Meld u aan voor een account](https://portal.office.com/Signup/Signup.aspx?OfferId=40BE278A-DFD1-470a-9EF7-9F2596EA7FF9&dl=INTUNE_A&ali=1#0%20) als u er nog geen hebt.

## <a name="supported-web-browsers-for-the-azure-portal"></a>Ondersteunde webbrowsers voor de Azure Portal

Azure Portal is geschikt voor de meeste moderne pc's, Macs en tablets. Mobiele telefoons worden niet ondersteund.
Momenteel worden de volgende webbrowsers ondersteund:

- Microsoft Edge (meest recente versie)
- Microsoft Internet Explorer 11
- Safari (meest recente versie, alleen Mac)
- Chrome (meest recente versie)
- Firefox (meest recente versie)

Controleer [Azure Portal](https://docs.microsoft.com/azure/azure-preview-portal-supported-browsers-devices) voor de meest recente informatie over ondersteunde browsers.

## <a name="whats-in-this-library"></a>Wat bevat deze bibliotheek?

De documentatie volgt de indeling van de Intune-portal, zodat u snel de gewenste informatie vindt.

![Workloads in de Azure Portal](./media/azure-portal-workloads.png)

### <a name="introduction-and-get-started"></a>Inleiding en aan de slag
Deze sectie bevat [inleidende informatie](introduction-intune.md) die u aan de slag helpt met Intune.
### <a name="plan-and-design"></a>Plannen en ontwerpen
Informatie over het [plannen en ontwerpen](/intune-classic/plan-design/introduction) van uw Intune-omgeving.
### <a name="device-enrollment"></a>Apparaatinschrijving
[Uw apparaten laten beheren door Intune](device-enrollment.md).
### <a name="device-compliance"></a>Apparaatnaleving
[Een nalevingsniveau voor uw apparaten definiëren en vervolgens rapporteren over apparaten die hieraan niet voldoen](device-compliance.md).
### <a name="device-configuration"></a>Apparaatconfiguratie
[Begrijpen welke profielen u kunt gebruiken om instellingen en functies te configureren op apparaten die u beheert](device-profiles.md).
### <a name="devices"></a>Apparaten
[Meer informatie over de apparaten die u met inventaris en rapporten beheert](device-management.md).
### <a name="mobile-apps"></a>Mobiele apps
[Apps publiceren, beheren, configureren en beveiligen](app-management.md).
### <a name="conditional-access"></a>Voorwaardelijke toegang
[De toegang tot Exchange-services beperken op basis van voorwaarden die u hebt opgegeven](conditional-access.md).
### <a name="on-premises-access"></a>Lokale toegang
[Toegang tot Exchange ActiveSync en Exchange on-premises configureren](/intune-classic/deploy-use/mobile-device-management-with-exchange-activesync-and-microsoft-intune)
### <a name="users"></a>Users
[Meer informatie over de gebruikers van apparaten die u beheert en bronnen in groepen sorteren](users-add.md).
### <a name="groups"></a>Groepen
[Meer informatie over het gebruik van Azure Active Directory-groepen met Intune](groups-get-started.md)
### <a name="intune-roles"></a>Intune-rollen
[Bepalen welke personen verschillende Intune-acties kunnen uitvoeren en op welke personen deze acties van toepassing zijn](role-based-access-control.md). U kunt de ingebouwde rollen gebruiken die voorzien in bepaalde algemene Intune-scenario's of u kunt uw eigen rollen maken.
### <a name="software-updates"></a>Software-updates
[Meer informatie over de configuratie van software-updates voor Windows 10-apparaten](windows-update-for-business-configure.md).



## <a name="whats-new"></a>Wat is er nieuw?

[Ontdek wat er nieuw is in Intune](whats-new.md).
