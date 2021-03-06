---
title: iOS-apps met beveiligingsbeleid voor apps
description: In dit onderwerp wordt beschreven wat u kunt verwachten wanneer uw iOS-app wordt beheerd door een app-beveiligingsbeleid.
keywords: 
author: barlanmsft
ms.author: barlan
manager: angrobe
ms.date: 05/05/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: b57e6525-b57c-4cb4-a84c-9f70ba1e8e19
ms.reviewer: andcerat
ms.suite: ems
ms.custom: intune-classic
ms.openlocfilehash: e66042e5198b76ec484fe0218127acb653394cce
ms.sourcegitcommit: f100c943a635f5a08254ba7cf30f1aaebb7e810e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/13/2017
---
# Wat u kunt verwachten wanneer uw iOS-app wordt beheerd door een app-beveiligingsbeleid
<a id="what-to-expect-when-your-ios-app-is-managed-by-app-protection-policies" class="xliff"></a>

[!INCLUDE[both-portals](./includes/note-for-both-portals.md)]

 In dit onderwerp wordt de gebruikerservaring beschreven voor het gebruik van apps waarop app-beveiligingsbeleid is toegepast. App-beveiligingsbeleid wordt alleen toegepast wanneer apps worden gebruikt in een werkcontext, bijvoorbeeld wanneer de gebruiker apps gebruikt met een werkaccount of bestanden opent die zijn opgeslagen in de OneDrive voor Bedrijven-locatie van uw bedrijf.

##  Toegang tot apps
<a id="access-apps" class="xliff"></a>

Als het apparaat **niet is geregistreerd bij Intune**, wordt de gebruiker gevraagd de app opnieuw te starten wanneer deze voor het eerst wordt gebruikt. Er moet opnieuw worden opgestart zodat het app-beveiligingsbeleid kan worden toegepast op de app.

<!--- The following screenshot from the Skype app illustrates this restart request: --->


<!---  ![Screenshot of the iOS device showing PIN prompt](../media/appmanagement/iOS_AppPINPrompt.png) --->

Op apparaten die zijn **ingeschreven voor beheer in Intune**, wordt een bericht aan de gebruiker weergegeven dat de app nu wordt beheerd.

##  Apps met ondersteuning voor meerdere identiteiten gebruiken
<a id="use-apps-with-multi-identity-support" class="xliff"></a>

Met apps die ondersteuning bieden voor meerdere identiteiten, kunt u verschillende accounts (zakelijk en persoonlijk) gebruiken voor toegang tot dezelfde apps, terwijl beveiligingsbeleid voor apps wordt toegepast wanneer de apps worden gebruikt in zakelijke context.  

De gebruiker moet bijvoorbeeld een pincode invoeren bij het openen van werkgegevens. Voor de **Outlook-app** wordt de gebruiker gevraagd een pincode in te voeren bij het starten van de app. Voor de **OneDrive app** wordt de gebruiker om een pincode gevraagd wanneer deze het werkaccount typt.  Bij Microsoft **Word**, **PowerPoint** en **Excel** wordt de gebruiker om een pincode gevraagd wanneer deze documenten opent die zijn opgeslagen op de OneDrive voor Bedrijven-locatie van het bedrijf.

- Meer informatie over de apps die ondersteuning bieden voor [MAM en meerdere identiteiten](https://www.microsoft.com/cloud-platform/microsoft-intune-apps) met Intune.

App-beveiligingsbeleid wordt alleen toegepast in een werkcontext. Daarom is het mogelijk dat de app zich anders gedraagt, afhankelijk of het om een persoonlijke of werkcontext gaat.

##  Gebruikersaccounts op het apparaat beheren
<a id="manage-user-accounts-on-the-device" class="xliff"></a>

Intune biedt ondersteuning voor de implementatie van app-beveiligingsbeleid voor slechts één gebruikersaccount per apparaat.

* Afhankelijk van de app die u gebruikt, kan het zijn dat de tweede gebruiker op het apparaat wordt geblokkeerd. In alle gevallen wordt echter alleen de eerste gebruiker die het app-beveiligingsbeleid ontvangt, door het beleid beïnvloed.
  * **Microsoft Word**, **Excel** en **PowerPoint** blokkeren een tweede gebruikersaccount niet, maar het tweede gebruikersaccount wordt niet beïnvloed door het app-beveiligingsbeleid.  

  * Voor de apps **OneDrive** en **Outlook** kunt u slechts één werkaccount gebruiken. Het is niet mogelijk om meerdere werkaccounts voor deze apps toe te voegen. U kunt wel een gebruiker verwijderen en een andere gebruiker op het apparaat toevoegen.

* Als een apparaat meerdere gebruikersaccounts heeft voordat het app-beveiligingsbeleid wordt geïmplementeerd, wordt het account waarop het app-beveiligingsbeleid als eerste wordt geïmplementeerd, door het app-beveiligingsbeleid van Intune beheerd.


Lees het volgende voorbeeldscenario om meer inzicht te krijgen in hoe meerdere gebruikersaccounts worden behandeld.

Gebruiker A werkt voor twee bedrijven: **bedrijf X** en **bedrijf Y**. Gebruiker A heeft voor elk bedrijf een werkaccount en voor beide accounts wordt gebruikgemaakt van Intune om app-beveiligingsbeleid te implementeren. **Bedrijf X** implementeert app-beveiligingsbeleid **voordat** **bedrijf Y** dat doet. Het app-beveiligingsbeleid wordt toegepast op het account dat is gekoppeld aan **bedrijf X**, niet op het account dat is gekoppeld aan bedrijf Y. Als u wilt dat het gebruikersaccount dat is gekoppeld aan bedrijf Y, door het app-beveiligingsbeleid wordt beheerd, moet u het gebruikersaccount dat is gekoppeld aan bedrijf X, verwijderen.

### Een tweede account toevoegen
<a id="add-a-second-account" class="xliff"></a>

Als u een iOS-apparaat gebruikt en u een tweede werkaccount op dat apparaat probeert toe te voegen, ziet u mogelijk een blokkeringsbericht. De accounts worden weergegeven en vervolgens u kunt kiezen welk account u wilt verwijderen.

## Volgende stappen
<a id="next-steps" class="xliff"></a>
[Wat u kunt verwachten wanneer uw Android-app wordt beheerd door een app-beveiligingsbeleid](end-user-mam-apps-android.md)
