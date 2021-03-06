---
title: Op apps gebaseerde voorwaardelijke toegang met Intune
description: Een overzicht van de concepten over de werking van op apps gebaseerde voorwaardelijke toegang met Intune.
keywords: 
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 05/31/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: b399fba0-5dd4-4777-bc9b-856af038ec41
ms.reviewer: chrisgre
ms.suite: ems
ms.custom: intune-azure
ms.openlocfilehash: 0893d511c73e4154c61063d96e26937ea2825467
ms.sourcegitcommit: 34cfebfc1d8b81032f4d41869d74dda559e677e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2017
---
# <a name="app-based-conditional-access-with-intune"></a>Op apps gebaseerde voorwaardelijke toegang met Intune

[!INCLUDE[azure_portal](./includes/azure_portal.md)]

U kunt [beveiligingsbeleid voor apps in Intune](app-protection-policy.md) gebruiken om te helpen bij het beveiligen van uw bedrijfsgegevens op apparaten die zijn geregistreerd in Intune. U kunt ook beveiligingsbeleid voor apps gebruiken op apparaten die in het bezit zijn van werknemers en die niet zijn geregistreerd voor beheer in Intune. In dit geval moet u, zelfs als u het apparaat niet beheert, er nog steeds voor zorgen dat uw bedrijfsgegevens en -bronnen zijn beveiligd.

Met op apps gebaseerde voorwaardelijke toegang en beheer van mobiele toepassingen voegt u een beveiligingslaag toe door er voor te zorgen dat alleen mobiele aps die app-beveiligingsbeleid van Intune ondersteunen toegang hebben tot Exchange Online en andere Office 365-services.

> [!NOTE]
> Een beheerde app is een app waarop app-beveiligingsbeleid is toegepast en die door Intune kan worden beheerd.

U kunt de ingebouwde e-mailapps op iOS en Android blokkeren wanneer u alleen toegang van de Microsoft Outlook-app tot Exchange Online toestaat. Bovendien kunt u de toegang tot SharePoint Online blokkeren voor apps waarvoor geen app-beveiligingsbeleid in Intune is ingesteld.

## <a name="prerequisites"></a>Vereisten
Als u een op apps gebaseerd beleid voor voorwaardelijke toegang wilt maken, moet u over het volgende beschikken:

- Een **abonnement voor Enterprise Mobility + Security of Azure Active Directory Premium** en gebruikers moeten een licentie hebben voor EMS of Azure AD hebben.
    - Zie de [Enterprise Mobility-pagina met prijzen](https://www.microsoft.com/cloud-platform/enterprise-mobility-pricing) of de [Azure Active Directory-pagina met prijzen](https://azure.microsoft.com/pricing/details/active-directory/) voor meer informatie.

## <a name="supported-apps"></a>Ondersteunde apps

- **Exchange Online**:
    - Microsoft Outlook voor Android en iOS.
<br></br>
- **SharePoint Online**
    - Microsoft Word voor iOS en Android
    - Microsoft Excel voor iOS en Android
    - Microsoft PowerPoint voor iOS en Android
    - Microsoft OneDrive voor Bedrijven voor iOS en Android
    - Microsoft OneNote voor iOS
<br></br>
- **Microsoft Teams**

    > [!NOTE] 
    > Op apps gebaseerde voorwaardelijke toegang [biedt ook ondersteuning voor LOB-apps](https://docs.microsoft.com/intune-classic/deploy-use/block-apps-with-no-modern-authentication), maar als u deze apps wilt gebruiken, moet u gebruikmaken van [moderne verificatie van Office 365](https://support.office.com/article/Using-Office-365-modern-authentication-with-Office-clients-776c0036-66fd-41cb-8928-5495c0f9168a).

## <a name="how-app-based-conditional-access-works"></a>Hoe werkt op apps gebaseerde voorwaardelijke toegang?

In dit voorbeeld heeft de beheerder beveiligingsbeleid voor de Outlook-app toegepast, gevolgd door een regel voor voorwaardelijke toegang waarmee de Outlook-app wordt toegevoegd aan een lijst met goedgekeurde apps die kunnen worden gebruikt bij het openen van bedrijfs-e-mail.

> [!NOTE] 
> De onderstaande stroomdiagramstructuur kan worden gebruikt voor andere beheerde apps.

![Stroomdiagram van op apps gebaseerde voorwaardelijke toegang met Intune](./media/ca-intune-common-ways-3.png)

1.  De gebruiker probeert te verifiëren met Azure AD vanuit de Outlook-app.

2.  De gebruiker wordt omgeleid naar de app store om een broker-app te installeren bij de eerste verificatiepoging. De broker-app kan de Microsoft-Authenticator voor iOS of de Microsoft-bedrijfsportal voor Android-apparaten zijn.

    > [!NOTE]
    > In dit scenario, als gebruikers een native e-mail-app willen gebruiken, worden ze omgeleid naar de app store, waar ze de Outlook-app kunnen installeren.

3.  De broker-app wordt op het apparaat geïnstalleerd.

4.  De broker-app start het registratieproces van Azure AD om een apparaatrecord te maken in Azure AD. Dit is niet hetzelfde zijn als het inschrijvingsproces voor Mobile Device Management (MDM), maar deze record is nodig om het beleid voor voorwaardelijke toegang te kunnen afdwingen op het apparaat.

5.  De broker-app verifieert de identiteit van de app. Er is een beveiligingslaag zodat de broker-app kan valideren of de app gemachtigd is voor gebruik.

6.  De broker-app verzendt de client-id van de app naar Azure AD als onderdeel van het verificatieproces voor de gebruiker om te controleren of de app voorkomt in de lijst met goedgekeurde beleidsregels.

7.  Met Azure AD kan de gebruiker worden geverifieerd en wordt de app op de lijst met goedkeurde beleidsregels gebruikt. Als de app niet op deze lijst voorkomt, weigert Azure AD de toegang aan de app.

8.  De Outlook-app communiceert met de Outlook-cloudservice voor communicatie met Exchange Online.

9.  De Outlook-cloudservice communiceert met Azure AD om de Exchange Online-toegangstoken voor de gebruiker op te halen.

10.  De Outlook-app communiceert met Exchange Online om het bedrijfs-e-mailadres van de gebruiker op te halen.

11.  Bedrijfs-e-mail wordt bezorgd in het postvak van de gebruiker.

## <a name="next-steps"></a>Volgende stappen
[Op apps gebaseerd beleid voor voorwaardelijke toegang maken](app-based-conditional-access-intune-create.md)

[Apps die geen gebruik maken van moderne verificatie blokkeren](app-modern-authentication-block.md)
