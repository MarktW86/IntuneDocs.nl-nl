---
title: Voorwaardelijke toegang met Intune
titleSuffix: Intune on Azure
description: Gebruikelijke manieren om voorwaardelijke toegang met Intune te gebruiken
keywords: 
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 05/23/2017
ms.topic: get-started-article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: a0b8e55e-c3d8-4599-be25-dc10c1027b62
ms.suite: ems
ms.custom: intune-azure
ms.openlocfilehash: 0ba1f12d762a6288fc2e7a3bfdae637f8ae13a94
ms.sourcegitcommit: 34cfebfc1d8b81032f4d41869d74dda559e677e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2017
---
# <a name="common-ways-to-use-conditional-access-with-intune"></a>Gebruikelijke manieren om voorwaardelijke toegang met Intune te gebruiken

[!INCLUDE[azure_portal](./includes/azure_portal.md)]

U moet Intune-beleid voor de compatibiliteit van mobiele apparaten en de Intune MAM-mogelijkheden (Mobile Application Management) configureren om de naleving van de voorwaardelijke toegang binnen uw organisatie te waarborgen. Laten we het eens hebben over de gebruikelijke manieren om voorwaardelijke toegang met Intune te gebruiken.

## <a name="device-based-conditional-access"></a>Voorwaardelijke toegang op basis van het apparaat

Intune en Azure Active Directory werken samen om ervoor te zorgen dat alleen beheerde en compatibele apparaten toegang kunnen krijgen tot e-mail, Office 365-services, SaaS-apps (Software as a Service) en [on-premises apps](https://docs.microsoft.com/azure/active-directory/active-directory-application-proxy-get-started). U kunt daarnaast een beleid in Azure Active Directory instellen, zodat alleen computers die zijn toegevoegd aan een domein of mobiele apparaten die zijn ingeschreven in Intune, toegang tot Office 365-services hebben.

Met Intune beschikt u over mogelijkheden voor apparaatnalevingsbeleid waarmee u de nalevingsstatus van het apparaat kunt evalueren. De nalevingsstatus wordt gerapporteerd aan Azure Active Directory om het voorwaardelijke toegangsbeleid af te dwingen dat in Azure Active Directory wordt gemaakt wanneer de gebruiker zich toegang tot uw bedrijfsresources probeert te verschaffen.

Vanaf de nieuwe versie van [Azure Portal](https://docs.microsoft.com/intune-azure/introduction/what-is-microsoft-intune) worden de op apparaten gebaseerde beleidsregels voor voorwaardelijke toegang voor Exchange Online en andere Office 365-producten geconfigureerd via Azure Portal.

-   Meer informatie over [voorwaardelijke toegang in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal).

-   Meer informatie over [Intune-apparaatcompatibiliteit](device-compliance.md).

-   Meer informatie over het [beveiligen van e-mail, Office 365 en andere services middels het gebruik van voorwaardelijke toegang voor Intune](https://docs.microsoft.com/intune-classic/deploy-use/restrict-access-to-email-and-o365-services-with-microsoft-intune).

### <a name="conditional-access-for-exchange-on-premises"></a>Voorwaardelijke toegang voor Exchange On-Premises

Voorwaardelijke toegang kan worden gebruikt de toegang tot **Exchange On-Premises** toe te staan of te blokkeren op basis van de beleidsregels voor apparaatcompatibiliteit en de registratiestatus. Wanneer voorwaardelijke toegang wordt gebruikt in combinatie met een nalevingsbeleid voor apparaten, hebben alleen apparaten die voldoen aan het beleid toegang voor Exchange On-Premises.

U kunt geavanceerde instellingen configureren voor de voorwaardelijke toegang. Zodoende hebt u voor gedetailleerdere controle over onder meer het volgende:

-   Toestaan of blokkeren van bepaalde platforms.

-   Onmiddellijk blokkeren van apparaten die niet worden beheerd door Intune.

Wanneer er beleidsregels voor apparaatcompatibiliteit en voorwaardelijke toegang zijn toegepast, wordt voor elk apparaat dat wordt gebruikt voor toegang tot Exchange On-Premises gecontroleerd of de beleidsregels worden nageleefd.

Wanneer apparaten niet voldoen aan de gestelde voorwaarden, wordt de eindgebruiker door de registratieprocedure voor het apparaat geleid om het probleem te verhelpen dat ervoor zorgt dat het apparaat niet-compatibel is.

#### <a name="how-conditional-access-for-exchange-on-premises-works"></a>Hoe voorwaardelijke toegang voor Exchange On-Premises werkt

Intune Exchange Connector haalt alle EAS-records (Exchange Active Sync) op de Exchange-server op, zodat de EAS-records via Intune kunnen worden gekoppeld aan records Intune-apparaten. Deze records zijn apparaten die zijn geregistreerd bij Intune en door Intune worden herkend. Met dit proces wordt de toegang tot e-mail toegestaan of geblokkeerd.

Als de EAS-record nieuw is en deze niet door Intune wordt herkend, wordt er een cmdlet uitgegeven waarmee de toegang tot e-mail wordt geblokkeerd. Hier volgt meer informatie over de werking van dit proces:

![Exchange on-Premises met CA-stroomdiagram](./media/ca-intune-common-ways-1.png)

1.  De gebruiker probeert toegang te krijgen tot de bedrijfs-e-mail, die wordt gehost op Exchange On-Premises 2010 SP1 of later.

2.  Als het apparaat niet wordt beheerd door Intune, wordt de toegang tot e-mail geblokkeerd. Intune verzendt een blokmelding naar de EAS-client.

3.  EAS ontvangt de blokmelding ontvangt, waarna het apparaat in quarantaine wordt geplaatst. Vervolgens wordt de quarantaine-e-mail verzonden. Deze bevat herstelstappen met koppelingen, zodat de gebruikers hun apparaten kunnen registreren.

4.  Het Workplace Join-proces wordt uitgevoerd. Dit is de eerste stap om een apparaat met Intune te beheren.

5.  Het apparaat wordt geregistreerd bij Intune.

6.  Intune wijst de EAS-record toe aan een apparaatrecord en slaat de nalevingsstatus voor het apparaat op.

7.  De EAS-client-id wordt geregistreerd middels het apparaatregistratieproces van Azure AD, zodat er een relatie tussen de Intune-apparaatrecord en de EAS-client-id wordt gemaakt.

8.  De apparaatregistratie van Azure AD slaat de informatie over de apparaatstatus op.

9.  Als de gebruiker aan de beleidsregels voor voorwaardelijke toegang voldoet, geeft Intune een cmdlet via Intune Exchange Connector uit, zodat het postvak kan worden gesynchroniseerd.

10. De Exchange-server verzendt de melding naar de EAS-client, zodat de gebruiker toegang heeft tot e-mail.

#### <a name="whats-the-intune-role"></a>Wat is de rol van Intune?

Met Intune wordt de apparaatstatus beoordeelt en beheert.

#### <a name="whats-the-exchange-server-role"></a>Wat is de rol van de Exchange-server?

De Exchange-server biedt de API en infrastructuur om apparaten naar in quarantaine te plaatsen.

> [!IMPORTANT] 
> Houd er rekening mee dat er nalevingsbeleid moet worden toegewezen aan de gebruiker van het apparaat, zodat de naleving door het apparaat kan worden beoordeeld. Als er geen nalevingsbeleid wordt geïmplementeerd voor de gebruiker, wordt het apparaat beschouwd als een apparaat dat voldoet aan het beleid en worden er geen toegangsbeperkingen toegepast.

### <a name="conditional-access-based-on-network-access-control"></a>Voorwaardelijke toegang op basis van netwerktoegangsbeheer

Intune kan worden geïntegreerd met partners als Cisco ISE, Aruba Clear Pass en Citrix NetScaler voor toegangsbeheer op basis van de Intune-registratie en de nalevingsstatus van het apparaat.

Gebruikers kan toegang tot het Wi-Fi-netwerk of de VPN-resources worden verleend of geweigerd door te controleren of het apparaat wordt beheerd met en voldoet aan het Intune-nalevingsbeleid voor apparaten.

-   Meer informatie over de [NAC-integratie met Intune](network-access-control-integrate.md).

### <a name="conditional-access-based-on-device-risk"></a>Voorwaardelijk op basis van het apparaatrisico

Intune werkt samen met leveranciers van Mobile Threat Defense, die een beveiligingsoplossing biedt voor het detecteren van malware, Trojaans paarden en andere bedreigingen op mobiele apparaten.

#### <a name="how-the-intune-and-mobile-threat-defense-integration-works"></a>Hoe de integratie van Intune en Mobile Threat Defense werkt

Wanneer de Mobile Threat Defense-agent op een mobiele apparaat is geïnstalleerd, kan de agent berichten over de nalevingsstatus naar Intune sturen om te rapporteren of er in het mobiele apparaat zelf een bedreiging is gevonden.

De integratie van Intune en Mobile Threat Defense speelt een rol bij de beslissingen die op basis van de apparaatrisico's worden genomen voor de voorwaardelijke toegang.

-   Meer informatie over [Intune Mobile Threat Defense](https://docs.microsoft.com/intune-classic/deploy-use/mobile-threat-defense).

### <a name="conditional-access-for-windows-pcs"></a>Voorwaardelijke toegang voor Windows-pc's

Voorwaardelijke toegang voor pc's biedt vergelijkbare mogelijkheden als voor mobiele apparaten. Laten we eens kijken op welke manieren u voorwaardelijke toegang kunt gebruiken wanneer u pc's met Intune beheert.

#### <a name="corporate-owned"></a>In bedrijfseigendom

-   **On-premises AD-domein is toegevoegd:** dit is de meest voorkomende implementatieoptie voor voorwaardelijke toegang voor organisaties waarvan de pc's al worden beheerd met AD-groepsbeleid en/of met System Center Configuration Manager.

-   **Azure AD-domein toegevoegd en het Intune-beheerprogramma:** dit scenario is doorgaans gericht op CYOD-scenario's (Choose Your Own Device) en scenario's met zwervende laptops die maar zelden zijn verbonden met het bedrijfsnetwerk. Het apparaat wordt toegevoegd aan Azure AD en wordt geregistreerd bij Intune, die vervolgens alle afhankelijkheden van on-premises AD en domeincontrollers verwijdert. Dit kan worden gebruikt als een criterium voor voorwaardelijke toegang bij de toegang tot bedrijfsresources.

-   **AD-domein toegevoegd en System Center Configuration Manager:** vanaf de current branch biedt System Center Configuration Manager niet alleen de mogelijkheid om een pc toe te voegen aan een domein, maar beschikt u ook over mogelijkheden voor voorwaardelijke toegang om specifieke nalevingscriteria te evalueren:

    -   Is de pc versleuteld?

    -   Is er schadelijke software geïnstalleerd? Is de pc up-to-date?

    -   Is het apparaat gekraakt of geroot?

#### <a name="bring-your-own-device-byod"></a>BYOD (Bring Your Own Device)

-   **Workplace join en Intune-beheer:** hier kan de gebruiker de eigen persoonlijke apparaten toevoegen voor toegang tot bedrijfsresources en -services. U kunt Workplace Join gebruiken en apparaten bij Intune registreren om beleidsregels op apparaatniveau te ontvangen, wat een andere optie is om de criteria voor voorwaardelijke toegang te evalueren.

## <a name="app-based-conditional-access"></a>Voorwaardelijke toegang op basis van apps

Intune en Azure Active Directory werken samen om ervoor te zorgen dat alleen beheerde apps toegang hebben tot de bedrijfs-e-mail of andere Office 365-services.

-   Meer informatie over [op apps gebaseerde voorwaardelijke toegang met Intune](app-based-conditional-access-intune.md).

## <a name="next-steps"></a>Volgende stappen

[Voorwaardelijke toegang in Azure Active Directory configureren](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)

[De on-premises Exchange-connector installeren met Intune](https://docs.microsoft.com/intune/exchange-connector-install).

[Beleid maken voor voorwaardelijke toegang voor Exchange On-premises](conditional-access-exchange-create.md)
