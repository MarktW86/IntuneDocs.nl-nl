---
title: De werking van een normale Intune-migratiecyclus
description: In dit artikel wordt uitgelegd hoe een Intune-migratiecyclus werkt en worden voorbeelden gegeven van de wijze waarop u de migratiecycli kunt uitvoeren.
keywords: 
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 07/12/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 3688b724-9521-4210-bf4d-bcf47d8d4ca0
ms.reviewer: dagerrit
ms.suite: ems
ms.openlocfilehash: 34e748e16449a99bad4c1f3e96c22dda6d8f3018
ms.sourcegitcommit: 388c5f59bc992375ac63968fd7330af5d84a1348
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/12/2017
---
# <a name="typical-migration-cycle"></a>Normale migratiecyclus

Het is gebruikelijk voor een organisatie om de Intune-migratie te starten met een korte testfase onder een aantal gebruikers op de IT-afdeling. Bovendien moet uw organisatie mogelijk thema’s bespreken als de welwillendheid van medewerkers ten aanzien van de wijziging, het aantal gebruikers, de complexiteit, de vereisten, de locatie en het bedrijfsrisico zodat u het tijdskader voor de migratie kunt bepalen.

Hier volgt een voorbeeld van de wijze waarop u uw doelgroepen kunt plannen:

  | **Doelgroepen van de migratie** | **Periode 1** | **Periode 2** | **Periode 3** | **Periode 4** | **...**
|:---:|:---:|:---:|:---:|:---:|:---:|
| Beperkte testfase voor de IT-organisatie (50 gebruikers) | Plan aankondigen | Opdracht geven tot deelname | Opgeven van de deadline | De voorwaardelijke toegang toepassen |  |                                                        
| Uitgebreide testfase voor de IT-organisatie (200 gebruikers) |  | Plan aankondigen | Opdracht geven tot deelname | Opgeven van de deadline | De voorwaardelijke toegang toepassen |
| Fase 1 van de migratie met technisch onderlegde gebruikers (2000) |  |  | Plan aankondigen | Opdracht geven tot deelname | Opgeven van de deadline |
| Fase 2 van de migratie (oostelijk deel van de V.S.) |  |  |  | Plan aankondigen | Opdracht geven tot deelname |
| Alle regio 's |  |  |  |  | Plan aankondigen |

## <a name="customer-migration-case-study"></a>Casestudy van de klantmigratie

### <a name="adatum-corporation"></a>Adatum Corporation

Bekijk [hoe Adatum Corporation een migratie heeft doorgevoerd van een externe MDM-provider naar Intune](https://gallery.technet.microsoft.com/Intune-migration-guide-893a95e3?redir=0).

## <a name="monitoring-migration"></a>Migratiebewaking

Intune biedt verschillende methoden om de migratie te bewaken:

* Groepsweergaven van Intune-gebruikers

* Een reeks ingebouwde rapporten

* Waarschuwingen in de Intune-beheerconsole

Houd bij hoeveel gebruikers apparaten hebben geregistreerd na elke fase zodat u het volgende kunt doen:

-   De effectiviteit van uw communicatieplan beoordelen.

-   De gevolgen van het doorvoeren van de voorwaardelijke toegang beoordelen.


## <a name="post-migration"></a>Na migratie

Stel de voorgaande MDM-provider buiten gebruik en meld u af voor de service nadat de migratie naar Intune is uitgevoerd. Daarnaast moet u eventuele overbodige infrastructuurvereisten verwijderen door de instructies van de MDM-provider te volgen.
