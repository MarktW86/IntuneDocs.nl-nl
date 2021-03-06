---
title: Netwerktoegangsbeheer integreren met Intune
titleSuffix: Intune on Azure
description: Netwerktoegangsbeheer integreren met Intune
keywords: 
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: aa7ecff7-8579-4009-8fd6-e17074df67de
ms.reviewer: davidra
ms.suite: ems
ms.custom: intune-azure
ms.openlocfilehash: 6037ec4638b487c0bae8fcecf2d9bd010e3bc59a
ms.sourcegitcommit: fd2e8f6f8761fdd65b49f6e4223c2d4a013dd6d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/03/2017
---
# <a name="network-access-control-nac-integration-with-intune"></a>Netwerktoegangsbeheer integreren met Intune

Intune kan worden geïntegreerd met producten van partners voor netwerktoegangsbeheer (ook wel Network Access Control of kortweg NAC genoemd) om de zakelijke gegevens van organisaties te beveiligen wanneer apparaten proberen toegang te krijgen tot on-premises resources.

## <a name="how-do-intune-and-nac-solutions-help-protect-your-organization-resources"></a>De resources van uw organisatie beveiligen met Intune en NAC-oplossingen

NAC-oplossingen zijn verantwoordelijk voor het controleren van de apparaatregistratie en nalevingsstatus bij Intune om op basis hiervan beslissingen over toegangsbeheer te nemen. Als het apparaat niet is geregistreerd, of wel is geregistreerd maar niet voldoet aan het Intune-nalevingsbeleid voor apparaten, moet het apparaat worden omgeleid naar Intune voor registratie en/of een compatibiliteitscontrole.

### <a name="example"></a>Voorbeeld

Als het apparaat is geregistreerd en compatibel is met Intune, moet de NAC-oplossing het apparaat toegang geven tot bedrijfsresources. Als gebruikers bijvoorbeeld via Wi-Fi of een VPN toegang proberen te krijgen tot bedrijfsresources, kan dit worden toegestaan of geweigerd.

## <a name="nac-and-conditional-access"></a>NAC en voorwaardelijke toegang

NAC werkt met voorwaardelijke toegang om beslissingen voor toegangsbeheer mogelijk te maken.

- Zie [Common ways to use conditional access with Intune](conditional-access-intune-common-ways-use.md) (Gebruikelijke manieren om voorwaardelijke toegang met Intune te gebruiken) voor meer informatie.

## <a name="how-the-nac-integration-works"></a>De werking van NAC-integratie

Hier volgt een overzicht van de werking van NAC als een dergelijke oplossing is geïntegreerd met Intune. De eerste drie stappen hebben betrekking op het voorbereidingsproces. Als de NAC-oplossing na die stappen is geïntegreerd met Intune, wordt in stappen 4-9 de werking van de oplossing beschreven.

![De werking van NAC met Intune](./media/ca-intune-common-ways-2.png)

1.  Registreer de NAC-partneroplossing bij Azure Active Directory (AAD) en verleen gedelegeerde machtigingen aan de NAC-API van Intune.

2.  Configureer de NAC-partneroplossing met de juiste instellingen, inclusief de detectie-URL van Intune.

3.  Configureer de NAC-partneroplossing voor certificaatverificatie.

4.  Een gebruiker maakt verbinding met een Wi-Fi-toegangspunt of verstuurt een aanvraag voor een VPN-verbinding.

5.  De NAC-partneroplossing stuurt de gegevens van het apparaat door naar Intune en vraagt bij Intune gegevens op over de apparaatregistratie en nalevingsstatus.

6.  Als het apparaat niet compatibel is of niet is geregistreerd, krijgt de gebruiker instructies van de NAC-partneroplossing om het apparaat te registreren of compatibel te maken.

7.  De compatibiliteit en/of registratiestatus van het apparaat worden opnieuw geverifieerd.

8.  Zodra het apparaat is geregistreerd en compatibel is, vraagt de NAC-partneroplossing de status op bij Intune.

9.  De verbinding wordt tot stand gebracht en het apparaat heeft nu toegang tot de bedrijfsresources.

## <a name="next-steps"></a>Volgende stappen

-   [Cisco ISE integreren met Intune](http://www.cisco.com/c/en/us/td/docs/security/ise/2-1/admin_guide/b_ise_admin_guide_21/b_ise_admin_guide_20_chapter_01000.html)

-   [Citrix NetScaler integreren met Intune](https://docs.citrix.com/netscaler-gateway/11-1/microsoft-intune-integration/configuring-network-access-control-device-check-for-netscaler-gateway-virtual-server-for-single-factor-authentication-deployment.html)

-   [HP Aruba Clear Pass integreren met Intune](https://support.arubanetworks.com/Documentation/tabid/77/DMXModule/512/Command/Core_Download/Default.aspx?EntryId=23757)
