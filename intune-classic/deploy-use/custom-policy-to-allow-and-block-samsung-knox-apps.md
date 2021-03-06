﻿---
title: Lijst van toegestane en geblokkeerde apps voor KNOX
description: Aangepast profiel voor het maken van een lijst met toegestane en geblokkeerde apps voor KNOX.
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 11/02/2016
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: bbc8e0df-7bf3-494e-8bc4-dac59a98ab41
ms.reviewer: chrisbal
ms.suite: ems
ms.custom: intune-classic
ms.openlocfilehash: b215425534e833db7e92e3f60fc507a168ef576f
ms.sourcegitcommit: 34cfebfc1d8b81032f4d41869d74dda559e677e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2017
---
# <a name="use-custom-policies-to-allow-and-block-apps-for-samsung-knox-standard-devices"></a>Aangepast beleid gebruiken om apps toe te staan of te blokkeren voor Samsung KNOX Standard-apparaten

[!INCLUDE[classic-portal](../includes/classic-portal.md)]

Gebruik de procedures in dit onderwerp om een aangepast Microsoft Intune-beleid op te stellen voor het maken van een van de volgende lijsten:

- Een lijst met apps die niet kunnen worden uitgevoerd op het apparaat. Apps in deze lijst worden geblokkeerd, wat betekent dat ze niet worden uitgevoerd, ook niet al ze al waren geïnstalleerd toen het beleid werd toegepast.
- Een lijst met apps die gebruikers van het apparaat kunnen installeren uit de Google Play Store. Alleen de apps die u in de lijst opneemt, kunnen worden geïnstalleerd. Geen andere apps kunnen worden geïnstalleerd uit de Store.

Deze instellingen kunnen alleen worden gebruikt door apparaten met Samsung KNOX Standard.

## <a name="to-create-an-allowed-or-blocked-app-list"></a>En lijst met toegestane of geblokkeerde apps maken

1. Kies in de [Microsoft Intune-beheerconsole](https://manage.microsoft.com/) de optie **Beleid** &gt; **Configuratiebeleid** &gt; **Toevoegen**.
2. Vouw in het dialoogvenster **Een nieuw beleid maken** de optie **Android** uit, kies **Aangepaste configuratie** en kies vervolgens **Beleid maken**.
3. Geef een naam op en voer eventueel een beschrijving in voor het beleid en kies vervolgens in de sectie **OMA-URI-instellingen** de optie **Toevoegen**.
4. Geef in het dialoogvenster **OMA-URI-instelling toevoegen of bewerken** het volgende op: Voor een lijst met apps die zijn geblokkeerd en dus niet kunnen worden uitgevoerd op het apparaat:
    
    - **Naam van instelling.** Voer **PreventStartPackages** in.
    - **Beschrijving van instelling.** Voer eventueel een beschrijving in, zoals 'Lijst met apps die zijn geblokkeerd'.
    -   **Gegevenstype.** Kies **Tekenreeks** in de vervolgkeuzelijst.
    -   **OMA-URI.** Voer **./Vendor/MSFT/PolicyManager/My/ApplicationManagement/PreventStartPackages** in.
    -   **Waarde.** Voer een lijst in van de app-pakketnamen die u wilt blokkeren. U kunt **; : ,** of **|** gebruiken als scheidingsteken. (Voorbeeld: pakket1; pakket2;)

    Voor een lijst met apps die gebruikers mogen installeren vanuit de Google Play Store, terwijl alle andere apps worden uitgesloten:

    - **Naam van instelling.** Voer **AllowInstallPackages** in.
    - **Beschrijving van instelling.** Voer eventueel een beschrijving in, zoals 'Lijst met apps die gebruikers kunnen installeren vanuit Google Play'.
    - **Gegevenstype.** Kies **Tekenreeks** in de vervolgkeuzelijst.
    - **OMA-URI.** Voer **./Vendor/MSFT/PolicyManager/My/ApplicationManagement/AllowInstallPackages** in.
    - **Waarde.** Voer een lijst in van de app-pakketnamen die u wilt toestaan. U kunt **; : ,** of **|** gebruiken als scheidingsteken. (Voorbeeld: pakket1; pakket2;)

4. Klik op **OK** en vervolgens op **Beleid opslaan**. 

>[!TIP]
> U kunt de pakket-id van een app vinden door te bladeren naar de app in de Google Play-store. De pakket-id is opgenomen in de URL van de pagina van de app. De pakket-id van de Microsoft Word-app is bijvoorbeeld **com.microsoft.office.word**.

De volgende keer dat een doelapparaat incheckt, worden de app-instellingen toegepast.


## <a name="deploy-the-policy"></a>Het beleid implementeren

1.  Selecteer het beleid dat u wilt implementeren in de werkruimte **Beleid** en klik vervolgens op **Implementatie beheren**.

2.  Selecteer in het dialoogvenster **Implementatie beheren** een of meer groepen waarvoor u het beleid wilt implementeren en klik vervolgens op **Toevoegen** &gt; **OK**.

 
Wanneer u een geïmplementeerde beleid selecteert, kunt u meer informatie over de implementatie weergeven onder in de lijst met beleidsregels.

### <a name="see-also"></a>Zie tevens
[Instellingen voor het Android- en Samsung KNOX-beleid in Microsoft Intune](android-policy-settings-in-microsoft-intune.md)
