﻿---
title: Uw iOS-apparaat registreren bij Intune | Microsoft Docs
description: Informatie over hoe u een iOS-apparaat bij Intune kunt inschrijven
keywords: 
author: barlanmsft
ms.author: barlan
manager: angrobe
ms.date: 07/06/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 6eeec7aa-1b07-4ce3-894c-13e09b89bdd4
searchScope: User help
ROBOTS: 
ms.reviewer: esmich
ms.suite: ems
ms.custom: intune-enduser
ms.openlocfilehash: 4d7ad138a8aa59ceeff00866469e59e2e1d19520
ms.sourcegitcommit: 2a6ad3c233d15a9fb441362105f64b2bdd550c34
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/13/2017
---
# <a name="enroll-your-ios-device-in-intune"></a>Uw iOS-apparaat inschrijven bij Intune

Als uw bedrijf of school gebruikmaakt van Microsoft Intune, kunt u uw iOS-apparaat registreren voor toegang tot zakelijke e-mail, bestanden en andere bronnen. Door uw apparaten te registreren, kan uw IT-afdeling deze werk- of schoolbronnen beheren en veilig houden, en beschikt u over de vrijheid om het apparaat van uw voorkeur te gebruiken voor uw werk. Zie [Wat gebeurt er wanneer ik de bedrijfsportal-app installeer en mijn apparaat inschrijf bij Intune?](what-happens-if-you-install-the-company-portal-app-and-enroll-your-device-in-intune-ios.md) voor meer informatie over inschrijving.

> [!VIDEO https://channel9.msdn.com/Series/IntuneEnrollment/iOS-Enrollment/player]

> [!NOTE]
> Als u een macOS-apparaat probeert te registreren, zoals een MacBook Pro of iMac, [volgt u in plaats daarvan deze instructies](enroll-your-device-in-intune-macos.md).

**Voordat u begint:**

- Zorg ervoor dat u de registratie voltooit nadat u de stappen hebt gestart. Het proces stopt gewoonlijk wanneer het meer dan enkele minuten wordt onderbroken, waarna u het opnieuw moet starten.
- Als uw registratie om welke reden dan ook mislukt, keert u terug naar de bedrijfsportal-app en probeert u het opnieuw.
- Zorg ervoor dat uw Wi-Fi werkt. Anders mislukt de registratie.
- Als u Safari op het apparaat hebt geblokkeerd, moet u Safari weer deblokkeren. Safari wordt gebruikt als onderdeel van het registratieproces van het apparaat.


**Ga als volgt te werk om uw iOS-apparaat te registreren:**

1.  Volg de stappen in [De Intune-bedrijfsportal-app installeren en u hierbij aanmelden](install-and-sign-in-to-the-intune-company-portal-app-ios.md).

2. Tik op de pagina **Instellen van bedrijfstoegang** op **Starten**.

    ![IOS-registreren-bedrijfstoegang-instellen](./media/ios-enroll-1a-comp-access-setup.png)

3. Lees op het scherm **Waarom moet u uw apparaat registreren?** informatie over wat u kunt doen wanneer u uw apparaat registreert en tik vervolgens op **DOORGAAN**.

    ![IOS-registreren-waarom-registreren](./media/ios-enroll-1b-why-enroll.png)

  > [!NOTE]
  > De gele driehoeken betekenen niet dat er al een fout is opgetreden. Deze pictogrammen geven aan dat er nog stappen moeten worden voltooid in het inschrijvingsproces.

4. Bekijk een lijst met zaken die de IT-beheerder wel en niet kan zien als u het apparaat registreert, en tik vervolgens op **Doorgaan**.

    ![IOS-registreren-wat-IT-kan-zien](./media/ios-enroll-1c-we-care-privacy.png)

5.  Lees op het scherm **De volgende stap** wat er gebeurt tijdens het registreren en tik vervolgens op **Registreren**.

    ![IOS-registreren-de-volgende-stap](./media/ios-enroll-1d-what-comes-next.png)

6.  Tik in het scherm **Profiel installeren** op **Installeren** en voer de wachtwoordcode in als daarom wordt gevraagd.

    ![IOS-registreren-installatie-profiel](./media/ios-enroll-2-mgt-profile-install.png)

7.  Tik op **INSTALLEREN**.

    ![ios-registreren-tik-op-installeren](./media/ios-enroll-3-mgt-profile-install-2.png)    

8.  Tik op **Installeren** om aan te geven dat u de waarschuwing hebt gelezen.

    ![IOS-registreren-tik-op-installeren-na-waarschuwing](./media/ios-enroll-4-warning.png)

9.  Tik op **Vertrouwen**.

    ![IOS-registreren-tik-op-vertrouwen](./media/ios-enroll-5-trust.png)

10.  Wanneer het scherm verandert om weer te geven dat het profiel is geïnstalleerd, tikt u op **Gereed**.

    ![ios-registreren-tik-op-gereed](./media/ios-enroll-6-done.png)

    Het bericht 'Apparaat registreren' wordt weergegeven op het scherm.

11.  Wanneer u in een bericht wordt gevraagd of u de pagina in de bedrijfsportal wilt openen, tikt u op **Openen**.

    ![IOS-registreren-open-bedrijfsportal](./media/ios-enroll-7-open-cp.png)

12. Tik in het scherm **Instellen van bedrijfstoegang** op **Doorgaan**. Op dit scherm ziet u aan welke andere vereisten u wellicht moet voldoen om ervoor zorgen dat uw apparaat compatibel is, zoals het instellen van een wachtwoord. Volg de aanwijzingen op het scherm totdat u voldoet aan alle nalevingsvereisten. Wanneer u klaar bent, keert u terug naar het scherm Instellen van bedrijfstoegang. Tik op **Doorgaan**.

    ![IOS-registreren-bedrijfstoegang-tik-op-doorgaan](./media/ios-enroll-8-comp-access-setup-compliance.png)

13. Tik op **Gereed**.

    ![ios-registreren-tik-op-gereed](./media/ios-enroll-9-comp-access-setup-complete.png)

Uw apparaat is nu geregistreerd bij Intune en u gaat terug naar de bedrijfsportal-app.

> [!Note]
> U moet nog enkele extra stappen uitvoeren voordat het apparaat volledig is geregistreerd. Meer informatie over het [registreren van uw apparaat met Telecom-onkostenbeheer](enroll-your-device-with-telecom-expense-management-ios.md). Als uw organisatie Apple Device Enrollment Program gebruikt, meer, vindt u [hier](enroll-your-device-dep-ios.md) meer informatie.

Nog hulp nodig? Neem contact op met uw IT-beheerder. Ga naar de [bedrijfsportalwebsite](http://portal.manage.microsoft.com) voor de betreffende contactgegevens.
