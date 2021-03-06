---
title: Intune-apparaatbeperkingsinstellingen voor Windows 10
titleSuffix: Intune on Azure
description: Meer informatie over de Intune-instellingen die u kunt gebruiken voor het beheren van apparaatinstellingen en functionaliteit op Windows 10-apparaten.
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 06/28/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 89f2d806-2e97-430c-a9a1-70688269627f
ms.reviewer: heenamac
ms.suite: ems
ms.custom: intune-azure
ms.openlocfilehash: c3819042d3b6e7236506c288156f98a0e55c15ea
ms.sourcegitcommit: 34cfebfc1d8b81032f4d41869d74dda559e677e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2017
---
# <a name="windows-10-and-later-device-restriction-settings-in-microsoft-intune"></a>Apparaatbeperkingsinstellingen voor Windows 10-apparaten (en hoger) in Microsoft Intune

[!INCLUDE[azure_portal](./includes/azure_portal.md)]

## <a name="general"></a>Algemeen
-   **Schermafbeelding (alleen mobiel)**: hiermee kan de gebruiker het apparaatscherm vastleggen als afbeelding.
-   **Kopiëren en plakken (alleen mobiel)**: hiermee staat u kopieer- en plakbewerkingen tussen apps op het apparaat toe.
-   **Registratie handmatig ongedaan maken**: hiermee kan de gebruiker het werkplekaccount handmatig van het apparaat verwijderen.
-   **Handmatige installatie van het basiscertificaat (alleen mobiel)**: de gebruiker kan niet langer basiscertificaten en tussenliggende CAP-certificaten handmatig installeren.
-   **Verzending van diagnostische gegevens**: mogelijke waarden zijn:
    -       **Geen**: er worden geen gegevens naar Microsoft verzonden
    -       **Basis**: beperkte informatie wordt naar Microsoft verzonden
    -       **Uitgebreid**: uitgebreide diagnostische gegevens worden naar Microsoft verzonden
    -       **Volledig**: hiermee worden dezelfde gegevens verzonden als bij Uitgebreid, aangevuld met gegevens over de apparaatstatus
-   **Camera**: hiermee kunt u het gebruik van de camera op het apparaat toestaan of blokkeren.
-   **Bestandssynchronisatie met OneDrive**: hiermee blokkeert u dat het apparaat bestanden synchroniseert naar OneDrive.
-   **Verwisselbare opslag**: hiermee geeft u op of er met het apparaat externe opslagapparaten, zoals SD-kaarten, kunnen worden gebruikt.
-   **Geolocatie**: hiermee geeft u aan of op het apparaat gegevens van locatieservices kunnen worden gebruikt.
-   **Gedeeld internet**: hiermee staat u het gebruik van een gedeelde internetverbinding op het apparaat toe.
-   **Opnieuw instellen van telefoon**: hiermee bepaalt u of de gebruiker de fabrieksinstellingen van het apparaat kan herstellen.
-   **USB-verbinding (alleen mobiel)**: hiermee bepaalt u of apparaten via een USB-verbinding toegang kunnen krijgen tot externe opslagapparaten.
-   **AntiTheft-modus (alleen mobiel)**: hiermee configureert u of de AntiTheft-modus van Windows is ingeschakeld.
-   **Meldingen van het Actiecentrum (alleen mobiel)**: hiermee schakelt u de meldingen van het actiecentrum op het vergrendelingsscherm van het apparaat in of uit (alleen voor Windows 10 Mobile).
-   **Cortana**: hiermee schakelt u de spraakassistent Cortana in en uit.
-   **Spraakopname (alleen mobiel)**: hiermee kunt u het gebruik van het spraakopnameapparaat van het apparaat toestaan of blokkeren.
-   **Instellingen voor in-/uitschakelen en slaapstand wijzigen (alleen desktop)**: hiermee voorkomt u dat de eindgebruiker de instellingen voor in-/uitschakelen en de slaapstand op het apparaat wijzigt.
-   **Regio-instellingen aanpassen (alleen desktop)**: hiermee voorkomt u dat de eindgebruiker de regionale instellingen op het apparaat wijzigt.
-   **Taalinstellingen wijzigen (alleen bureaublad)**: hiermee voorkomt u dat de eindgebruiker de taalinstellingen op het apparaat wijzigt.
-   **Systeemtijd wijzigen**: hiermee voorkomt u dat de eindgebruiker de datum en tijd van het apparaat wijzigt.
-   **Apparaatnaam wijzigen**: hiermee voorkomt u dat de eindgebruiker de apparaatnaam wijzigt.
-   **Inrichtingspakketten toevoegen**: hiermee blokkeert u de runtime configuratieagent die inrichtingspakketten installeert.
-   **Inrichtingspakketten verwijderen**: hiermee blokkeert u de runtime configuratieagent die inrichtingspakketten verwijdert.
-   **Apparaatdetectie**: hiermee voorkomt u dat een apparaat wordt gedetecteerd door andere apparaten.
-   **Taakwisselaar (alleen mobiel)**: hiermee blokkeert u de taakwisselaar op het apparaat.
-   **Foutberichtvenster voor SIM-kaart (alleen mobiel)**: hiermee voorkomt u dat op het apparaat een foutbericht wordt weergegeven als er geen SIM-kaart wordt gedetecteerd.


## <a name="password"></a>Wachtwoord
-   **Wachtwoord**: hiermee geeft u aan dat de eindgebruiker een wachtwoord moet invoeren voor toegang tot het apparaat.
    -   **Vereist wachtwoordtype**: hiermee geeft u aan of het wachtwoord alleen numeriek of alfanumeriek moet zijn.
    -   **Minimale wachtwoordlengte**: alleen van toepassing op Windows 10 Mobile.
    -   **Aantal mislukte aanmeldingen voordat een apparaat wordt gewist**: voor apparaten met Windows 10: als BitLocker is ingeschakeld op het apparaat, wordt het in de herstelmodus van BitLocker gezet nadat het aanmelden het aantal keren dat u opgeeft is mislukt. Als BitLocker niet is ingeschakeld op het apparaat, is deze instelling niet van toepassing.
Voor Windows 10 Mobile-apparaten: nadat het aanmelden het aantal keren dat u opgeeft is mislukt, wordt het apparaat gewist.
    -   **Maximum aantal minuten van inactiviteit voordat het scherm wordt vergrendeld**: hiermee geeft u de hoeveelheid tijd op die een apparaat inactief moet zijn voordat het scherm wordt vergrendeld.
    -   **Wachtwoord verloopt (dagen)**: hiermee geeft u de hoeveelheid tijd op waarna het wachtwoord van een apparaat moet worden gewijzigd.
    -   **Wachtwoorden niet opnieuw gebruiken**: hiermee geeft u het aantal eerder gebruikte wachtwoorden op dat door het apparaat wordt onthouden.
    -   **Wachtwoord vereisen wanneer het apparaat wordt geactiveerd vanuit een niet-actieve status**: hiermee geeft u aan dat de gebruiker een wachtwoord moet opgeven om het apparaat te ontgrendelen (alleen voor Windows 10 Mobile).
    -   **Eenvoudige wachtwoorden**: hiermee kunt u instellen dat eenvoudige wachtwoorden zijn toegestaan, zoals 1111 en 1234. Met deze instelling kunt u ook het gebruik van afbeeldingswachtwoorden toestaan of blokkeren.
-   **Versleuteling**: hiermee schakelt u versleuteling in op bepaalde apparaten (alleen voor Windows 10 Mobile) inschakelen.

## <a name="personalization"></a>Persoonlijke instellingen

-   **URL achtergrondafbeelding Bureaublad (alleen bureaublad)**: geef de URL op naar een afbeelding in PNG-, JPG- of JPEG-indeling die u wilt gebruiken als de achtergrond van het Windows-bureaublad. Gebruikers kunnen dit niet wijzigen.

## <a name="privacy"></a>Privacy

-   **Persoonlijke instellingen invoeren**: hiermee kunt u het gebruik van cloudgebaseerde spraakservices voor Cortana, de dicteerfunctie of Windows Store-apps blokkeren. Als u deze services toestaat, kan Microsoft spraakgegevens verzamelen voor het verbeteren van de service.
-   **Automatische acceptatie van de goedkeuringsvensters voor koppelen en privacy**: hiermee kunt u instellen dat Windows automatisch toestemming mag geven voor bewerkingen met koppelen en privacy bij het uitvoeren van apps.


## <a name="locked-screen-experience"></a>Vergrendeld scherm


-   **Meldingen van het Actiecentrum (alleen mobiel)**: hiermee kunt u meldingen van het actiecentrum op het vergrendelingsscherm van het apparaat weergeven (alleen Windows 10 Mobile).
-   **URL vergrendelde schermafbeelding (alleen bureaublad)**: geef de URL op naar een afbeelding in PNG-, JPG- of JPEG-indeling die wordt gebruikt als achtergrond van het Windows-vergrendelingsscherm. Gebruikers kunnen dit niet wijzigen.
-   **Time-out voor het scherm die door de gebruiker kan worden ingesteld (alleen mobiel)**: hiermee kunnen gebruikers de hoeveelheid tijd configureren 
-   **Cortana op vergrendeld scherm (alleen desktop)**: de gebruiker geen toestemming geven voor interactie met Cortana wanneer het vergrendelingsscherm wordt weergegeven op het apparaat (alleen Windows 10 voor desktops).
-   **Pop-upmeldingen op vergrendeld scherm**: geen waarschuwingsberichten weergeven op het vergrendelingsscherm van het apparaat.
-   **Time-out voor het scherm (alleen mobiel)**: hiermee geeft u de tijd in seconden op waarna het scherm wordt uitgeschakeld nadat het scherm is vergrendeld.



## <a name="app-store"></a>App Store

-   **App Store (alleen mobiel)**: hiermee kunt u het gebruik van de App Store op Windows 10 Mobile-apparaten inschakelen of blokkeren.
-   **Apps automatisch bijwerken vanuit Store**: apps die zijn geïnstalleerd vanuit de Windows Store kunnen automatisch worden bijgewerkt.
-   **Installatie van vertrouwde app**: voor apps die zijn ondertekend met een vertrouwd certificaat is sideloaden mogelijk.
-   **Ontgrendeling voor ontwikkelaars**: de eindgebruiker mag instellingen voor Windows-ontwikkelaars wijzigen, zoals het toestaan van sideloaden van apps.
-   **Gedeelde app-gegevens voor gebruikers**: apps mogen gegevens delen tussen verschillende gebruikers op hetzelfde apparaat.
-   **Alleen persoonlijke store gebruiken**: schakel dit in om toe te staan dat eindgebruikers apps downloaden van uw privé-store.
-   **Uit Store afkomstige app starten**: alle apps uitschakelen die vooraf geïnstalleerd zijn op het apparaat of die zijn gedownload vanuit Windows Store.
-   **Appgegevens installeren op systeemvolume**: apps kunnen geen gegevens opslaan op het systeemvolume van het apparaat.
-   **Apps installeren op systeemstation**: apps kunnen geen gegevens opslaan op het systeemstation van het apparaat.
-   **Game-DVR (alleen desktop)**: hiermee bepaalt u of het opnemen en uitzenden van games is toegestaan.



## <a name="edge-browser"></a>Edge-browser
-   **Microsoft Edge-browser (alleen mobiele apparaten)**: hiermee staat u het gebruik van de Edge-webbrowser toe op het apparaat.
-   **Vervolgkeuzelijst van de adresbalk (alleen desktop)**: gebruik deze optie als u in Edge geen lijst met suggesties wilt weergeven wanneer u typt in een vervolgkeuzelijst. Dit helpt bij het beperken van de netwerkbandbreedte die nodig is tussen Edge en Microsoft-services.
-   **Favorieten synchroniseren tussen Microsoft-browsers (alleen desktop)**: hiermee kunnen favorieten worden gesynchroniseerd tussen Internet Explorer en Edge.
-   **SmartScreen**: hiermee schakelt u SmartScreen in of uit, waarmee frauduleuze websites worden geblokkeerd.
-   **Do Not Track-headers verzenden**: hiermee configureert u de Edge-browser zodanig, dat verzoeken om niet gevolgd te worden, worden verzonden naar websites die gebruikers bezoeken.
-   **Cookies**: hiermee kunnen internetcookies in de browser op het apparaat worden opgeslagen.
-   **JavaScript**: hiermee staat u de uitvoering van scripts, zoals JavaScript, toe in de Microsoft Edge-browser.
-   **Pop-ups** pop-upvensters in de browser blokkeren (alleen van toepassing op Windows 10-desktop).
-   **Zoeksuggesties**: hiermee kan de zoekmachine sites voorstellen wanneer er zoektermen worden getypt.
-   **Intranetverkeer naar Internet Explorer sturen**: hiermee kunnen gebruikers intranetwebsites in Internet Explorer openen (alleen Windows 10 Desktop).
-   **Automatisch doorvoeren**: hiermee staat u gebruikers toe instellingen voor automatisch doorvoeren in de browser te wijzigen (alleen Windows 10 Desktop).
-   **Wachtwoordbeheer**: hiermee schakelt u de functie Wachtwoordbeheer van Microsoft Edge in of uit.
-   **Locatie van de lijst met websites van Bedrijfsmodus**: hiermee geeft u de plaats aan van de lijst met websites die in Bedrijfsmodus worden geopend. Gebruikers kunnen deze lijst niet bewerken.<br>(Alleen Windows 10 Desktop.)
-   **Ontwikkelhulpprogramma's**: hiermee voorkomt u dat de eindgebruiker de ontwikkelhulpprogramma's van Edge opent.
-   **Extensies**: toestaan dat de eindgebruiker Edge-extensies installeert op het apparaat.
-   **InPrivate-navigatie**: hiermee voorkomt u dat de eindgebruiker InPrivate-navigatiesessies opent.
-   **Pagina voor eerste keer uitvoeren weergeven**: hiermee wordt de introductiepagina niet weergegeven wanneer Edge de eerste keer wordt uitgevoerd.
    -   **URL voor eerste uitvoering**: hiermee geeft u de URL op van een pagina die wordt weergegeven wanneer een gebruiker de eerste keer Edge uitvoert (alleen Windows 10 Mobile).
-   **Startpagina's**: hiermee kunt u een lijst met sites toevoegen die u wilt gebruiken als startpagina's in Edge (alleen desktop).
-   **Wijzigingen van de startpagina**: hiermee kunnen gebruikers de startpagina's wijzigen die worden weergegeven bij het openen van Edge. Gebruik de instelling Startpagina's om de pagina, of een lijst van pagina's, te maken die u wilt openen bij het starten van Edge.
-   **Toegang tot about-vlaggen blokkeren**: Hiermee voorkomt u dat de eindgebruiker toegang krijgt tot de pagina met about-vlaggen in Edge. Op deze pagina staan instellingen voor ontwikkelaars en experimentele instellingen.
-   **SmartScreen-prompts negeren**: de eindgebruiker mag meldingen van het SmartScreen-filter over mogelijk schadelijke websites negeren.
-   **SmartScreen-prompts negeren voor bestanden**: de eindgebruiker mag meldingen van het SmartScreen-filter over het downloaden van mogelijk schadelijke bestanden negeren.
-   **LocalHost IP-adres voor WebRTC**: hiermee blokkeert u het weergeven van het IP-adres van de localhost van gebruikers tijdens het doen van telefoonoproepen via het WebRTC-protocol.
-   **Standaardzoekmachine**: geef de zoekmachine op die u standaard wilt gebruiken. Eindgebruikers kunnen deze waarde op elk moment wijzigen.
-   **Browsegegevens wissen bij afsluiten**: hiermee worden de geschiedenis en de browsegegevens gewist wanneer de gebruiker Edge afsluit.
-   **Verzamelen van livetegelgegevens**: hiermee geeft u op dat Windows geen gegevens moet verzamelen van de livetegel wanneer gebruikers vanuit Edge een site vastmaken aan het startmenu.


## <a name="search"></a>Zoeken
- **Veilig zoeken (alleen mobiel)**: hiermee bepaalt u hoe Cortana inhoud voor volwassenen filtert in de zoekresultaten. U kunt **Strikt** of **Gemiddeld** selecteren, of u kunt toestaan dat eindgebruikers hun eigen instellingen kiezen.

## <a name="cloud-and-storage"></a>Cloud en opslag
-   **Microsoft-account**: hiermee staat u toe dat de gebruiker een Microsoft-account aan het apparaat kan koppelen.
-   **Niet-Microsoft-account**: hiermee staat u toe dat de gebruiker e-mailaccounts aan het apparaat kan toevoegen die niet aan een Microsoft-account zijn gekoppeld.
-   **Synchronisatie van instellingen voor Microsoft-accounts**: hiermee staat u synchronisatie tussen apparaten toe van apparaat- en app-instellingen die aan een Microsoft-account zijn gekoppeld.

## <a name="cellular-and-connectivity"></a>Mobiel en connectiviteit

-   **Mobiel gegevenskanaal**: hiermee voorkomt u dat gebruikers toegang hebben tot gegevens, bijvoorbeeld tijdens het surfen op internet, wanneer ze zijn verbonden met een mobiel netwerk. 
-   **Dataroaming**: hiermee staat u roaming tussen netwerken toe tijdens het ophalen van data.
-   **VPN via het mobiele netwerk**: hiermee bepaalt u of het apparaat toegang kan krijgen tot VPN-verbindingen indien verbonden met een mobiel netwerk.
-   **VPN-roaming via het mobiele netwerk**: hiermee bepaalt u of het apparaat toegang kan krijgen tot VPN-verbindingen tijdens het roamen op een mobiele netwerk.
-   **Bluetooth**: hiermee bepaalt u of de gebruiker Bluetooth op het apparaat kan inschakelen en configureren.
-   **Bluetooth-detectie**: hiermee geeft u aan dat het apparaat kan worden gedetecteerd door andere Bluetooth-apparaten.
-   **Vooraf koppelen van Bluetooth**: hiermee kunt u instellen dat bepaalde Bluetooth-apparaten automatisch worden gekoppeld met een hostapparaat.
-   **Aankondigingen via Bluetooth**: hiermee geeft u aan dat het apparaat aankondigingen via Bluetooth kan ontvangen.
-   **Bluetooth-apparaatnaam**: hiermee kunt u de Bluetooth-naam van een apparaat opgeven. Als u geen naam opgeeft, wordt de standaardradionaam gebruikt.
-   **Service voor verbonden apparaten**: hiermee kunt u opgeven of de service voor verbonden apparaten is toegestaan, waardoor detectie van en verbinding met andere Bluetooth-apparaten mogelijk is.
-   **NFC**: hiermee kan de gebruiker mogelijkheden voor Near Field Communications op het apparaat inschakelen en configureren.
-   **Wi-Fi**: hiermee kan de gebruiker Wi-Fi op het apparaat inschakelen en configureren (alleen voor Windows 10 Mobile).
-   **Automatisch verbinding maken met Wi-Fi-hotspots**: hiermee kunt u het apparaat automatisch verbinding laten maken met gratis Wi-Fi-hotspots en automatisch de voorwaarden voor de verbinding laten accepteren.
-   **Handmatige configuratie van Wi-Fi**: hiermee geeft u aan of de gebruiker zijn of haar eigen Wi-Fi-verbindingen kan instellen, of dat de gebruiker alleen verbindingen kan gebruiken die door een Wi-Fi-profiel zijn geconfigureerd (alleen voor Windows 10 Mobile).
-   **Wi-Fi-scaninterval**: geef op hoe vaak apparaten zoeken naar Wi-Fi-netwerken. Geef een waarde op tussen 1 (zo vaak mogelijk) en 500 (zo min mogelijk).
-   **Services waarvoor Bluetooth is toegestaan**: geef een lijst met toegestane Bluetooth-services en -profielen op, in de vorm van hexadecimale tekenreeksen.


## <a name="control-panel-and-settings"></a>Configuratiescherm en instellingen

-   **App Instellingen**: hiermee blokkeert u toegang tot de app Instellingen van Windows.
    -   **Systeem**: hiermee blokkeert u de toegang tot het systeemgebied van de app Instellingen.
    -   **Apparaten**: hiermee blokkeert u de toegang tot het apparatengebied van de instellingen-app.
    -   **Netwerk en internet**: hiermee blokkeert u de toegang tot het gebied voor netwerk en internet van de instellingen-app.
    -   **Persoonlijke instellingen**: hiermee blokkeert u de toegang tot het gebied voor persoonlijke instellingen van de instellingen-app.
    -   **Accounts**: hiermee blokkeert u de toegang tot het accountsgebied van de instellingen-app.
    -   **Tijd en taal**: hiermee blokkeert u de toegang tot het gebied voor tijd en taal van de instellingen-app.
    -   **Betere toegankelijkheid**: hiermee blokkeert u de toegang tot het gebied voor betere toegankelijkheid van de instellingen-app.
    -   **Privacy**: hiermee blokkeert u de toegang tot het privacygebied van de instellingen-app.
    -   **Bijwerken en beveiliging**: hiermee blokkeert u de toegang tot het gebied voor updates en beveiliging van de instellingen-app.

## <a name="defender"></a>Defender

-   **Realtime-controle**: hiermee schakelt u het realtime scannen op malware, spyware en andere ongewenste software in.
-   **Gedragscontrole**: hiermee kunt u Defender laten controleren op de aanwezigheid van bepaalde bekende patronen van verdachte activiteiten op apparaten.
-   **Netwerkinspectiesysteem (NIS)**: NIS helpt bij de bescherming van apparaten tegen aanvallen vanaf het netwerk. NIS maakt gebruik van handtekeningen van bekende beveiligingsproblemen uit het Microsoft Endpoint Protection Center om schadelijk netwerkverkeer te detecteren en blokkeren.
-   **Alle downloads scannen**: hiermee bepaalt u of Windows Defender alle bestanden moet scannen die van internet worden gedownload.
-   **Scripts scannen die in webbrowsers van Microsoft worden geladen**: hiermee geeft u aan dat Defender scripts moet scannen die worden gebruikt in Internet Explorer.
-   **Toegang van eindgebruikers tot Defender**: hiermee geeft u aan of de gebruikersinterface van Windows Defender voor eindgebruikers wordt verborgen.
Als deze instelling wordt gewijzigd, gaat de wijziging in wanneer de pc van de eindgebruiker de volgende keer opnieuw wordt opgestart.
-   **Interval voor handtekeningupdates (in uren)**: hiermee geeft u het interval op waarmee Defender op nieuwe handtekeningbestanden controleert.
-   **Activiteiten van bestanden en programma's bewaken**: hiermee staat u Defender toe activiteiten van bestanden en programma's op apparaten te bewaken.
-   **Het aantal dagen voordat in quarantaine geplaatste malware wordt verwijderd**: hiermee kunt u Defender gedurende het aantal dagen dat u opgeeft, opgeloste malware laten bijhouden, zodat u handmatig eerder aangevallen apparaten kunt controleren. Als u het aantal dagen instelt op **0**, blijft malware in de map Quarantaine staan en wordt malware niet automatisch verwijderd.
-   **Limiet voor het CPU-gebruik tijdens het scannen**: hiermee kunt u de hoeveelheid CPU beperken die scans mogen gebruiken (tussen **1** en **100**).
-   **Archiefbestanden scannen**: hiermee kunt u toestaan dat Defender gearchiveerde bestanden scant, zoals ZIP- of CAB-bestanden.
-   **Inkomende e-mailberichten scannen**: hiermee kunt u toestaan dat Defender e-mailberichten scant wanneer deze op het apparaat binnenkomen.
-   **Verwisselbare stations scannen tijdens een volledige scan**: hiermee kunt u toestaan dat Defender verwisselbare stations, zoals USB-sticks, scant.
-   **Toegewezen netwerkschijven scannen tijdens een volledige scan**: hiermee kunt u Defender op toegewezen netwerkstations laten scannen.<br>Als de bestanden op de schijf het kenmerk Alleen-lezen hebben, kan Defender eventueel gevonden malware niet verwijderen.
-   **Bestanden die zijn geopend vanuit mappen op het netwerk scannen**: hiermee kunt u Defender bestanden op gedeelde stations laten scannen (bijvoorbeeld bestanden die via een UNC-pad toegankelijk zijn).
Als de bestanden op de schijf het kenmerk Alleen-lezen hebben, kan Defender eventueel gevonden malware niet verwijderen.
-   **Cloudbeveiliging**: hiermee kunt u toestaan of blokkeren dat de Microsoft Active Protection-service informatie ontvangt over malware-activiteit op apparaten die u beheert. Deze informatie wordt gebruikt om de service in de toekomst te verbeteren.
-   **Gebruikers vragen voordat een voorbeeld wordt verzonden**: hiermee bepaalt u of potentieel schadelijke bestanden waarvoor verdere analyse nodig is, automatisch naar Microsoft worden verzonden.
-   **Tijd waarop een dagelijkse snelle scan moet worden uitgevoerd**: hiermee kunt u een snelle scan plannen die dagelijks wordt uitgevoerd op het moment dat u selecteert.
-   **Type systeemscan dat moet worden uitgevoerd**: hiermee kunt u het niveau opgeven waarop moet worden gescand tijdens een geplande systeemscan.
-   **Mogelijk ongewenste toepassingen detecteren**: kies het niveau van beveiliging dat moet worden ingesteld als Windows toepassingen detecteert die mogelijk ongewenst zijn:
        - **Blokkeren**
        - **Controle**. Zie [dit onderwerp](https://docs.microsoft.com/windows/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus) voor meer informatie over mogelijk ongewenste apps.
-   **Acties voor gedetecteerde bedreiging van malware**: schakel deze optie in om de acties op te geven die Defender moet uitvoeren voor de verschillende bedreigingsniveaus (Laag, Gemiddeld, Hoog en Ernstig). U kunt kiezen uit deze acties:
    -   **Reinigen**
    -   **Quarantaine**
    -   **Verwijderen**
    -   **Toestaan**
    -   **Door de gebruiker gedefinieerd**
    -   **Blokkeren**



## <a name="defender-exclusions"></a>Defender-uitsluitingen

-   **Bestanden en mappen die moeten worden uitgesloten van scans en de realtime-beveiliging**: hiermee voegt u een of meer bestanden aan de uitsluitingslijst toe, zoals **C:\pad** of **%ProgramFiles%\pad\bestandsnaam.exe**. Deze bestanden en mappen worden niet opgenomen in real-timescans of geplande scans.
-   **Bestandsextensies die moeten worden uitgesloten van scans en de realtime-beveiliging**: hiermee voegt u een of meer bestandsextensies zoals **jpg** of **txt** aan de uitsluitingslijst toe. Bestanden met deze extensies worden niet opgenomen in realtime-scans of geplande scans.
-   **Processen die moeten worden uitgesloten van scans en de realtime-beveiliging**: hiermee voegt u een of meer processen van het type **.exe**, **.com** of **.scr** aan de uitsluitingslijst toe. Deze processen worden niet opgenomen in real-timescans of geplande scans.


## <a name="network-proxy"></a>Netwerkproxy

-   **Proxy-instellingen automatisch detecteren**: wanneer deze optie is ingeschakeld, probeert het apparaat het pad naar een PAC-script te vinden.
-   **Proxyscript gebruiken**: selecteer deze optie als u een pad naar een PAC-script wilt opgeven om de proxyserver te configureren.
    -   **URL voor het installatiescriptadres**: geef de URL op van een PAC-script dat u wilt gebruiken om de proxyserver te configureren.
-   **Handmatige proxyserver gebruiken**: selecteer deze optie als u de proxyservergegevens handmatig wilt opgeven.
    -   **Adres**: voer de naam of het IP-adres van de proxyserver in.
    -   **Poortnummer**: voer het poortnummer van uw proxyserver in.
    -   **Proxy-uitzonderingen**: voer URL's in die geen gebruik mogen maken van de proxyserver. Scheid de items van elkaar met een puntkomma.
    -   **Proxyserver niet gebruiken voor lokale adressen**: schakel deze optie in als u de proxyserver niet wilt gebruiken voor lokale adressen in uw intranet.


## <a name="windows-spotlight"></a>Windows Spotlight


- Windows Spotlight: gebruik deze instelling om alle functionaliteit van Windows Spotlight te blokkeren op Windows 10-apparaten. In dat geval zijn de volgende instellingen niet beschikbaar.
    - **Windows-spotlight in het vergrendelingsscherm**: instellen dat Windows Spotlight geen informatie weergeeft op het vergrendelingsscherm van het apparaat.
    - **Suggesties van derden in Windows-spotlight**: instellen dat Windows Spotlight geen inhoud mag voorstellen die niet is gepubliceerd door Microsoft.
    - **Windows Tips**: hiermee kunt u de weergave van pop-uptips in Windows blokkeren.
    - **Consumentenfuncties**: hiermee kunt u functies voor consumenten blokkeren, zoals suggesties in het menu Start lidmaatschapsmeldingen.
    - **Windows-spotlight in het Onderhoudscentrum**: suggesties van Windows Spotlight blokkeren, zodat bijvoorbeeld nieuwe apps of beveiligingsinhoud niet wordt vermeld in het actiecentrum van Windows.
    - **Persoonlijke instellingen voor Windows-spotlight**: instellen dat Windows Spotlight de weergave van resultaten aanpast op basis van het gebruik van een apparaat.
    - **Welkomstbericht van Windows**: geen informatie weergeven over nieuwe of bijgewerkte functies.


## <a name="display"></a>Weergave

- **Gebruikersinvoer van ontvangers van draadloze schermen**: hiermee blokkeert u gebruikersinvoer van draadloze beeldschermen.
- **Projectie naar deze PC**: andere apparaten kunnen de pc niet meer detecteren voor projectie.
- **Een pincode vereisen voor koppelen**: er is een pincode vereist voor het verbinden met een projectieapparaat.

## <a name="start"></a>start

- **Apps losmaken van de taakbalk**: de gebruiker kan geen apps meer losmaken vanuit het menu Start.
- **Documenten op het startscherm**: de map Documenten in het menu Start van Windows weergeven of verbergen.
- **Downloads op het startscherm**: de map Downloads in het menu Start van Windows weergeven of verbergen.
- **Bestandenverkenner op het startscherm**: de app Bestandsverkenner in het menu Start van Windows weergeven of verbergen.
- **Thuisgroep op het startscherm**: de map Thuisgroep in het menu Start van Windows weergeven of verbergen.
- **Muziek op het startscherm**: de map Muziek in het menu Start van Windows weergeven of verbergen.
- **Netwerk op het startscherm**: de map Netwerk in het menu Start van Windows weergeven of verbergen.
- **Persoonlijke instellingen op het startscherm**: de map met persoonlijke instellingen in het menu Start van Windows weergeven of verbergen.
- **Afbeeldingen op het startscherm**: de map Afbeeldingen in het menu Start van Windows weergeven of verbergen.
- **Instellingen op het startscherm**: de app Instellingen in het menu Start van Windows weergeven of verbergen.
- **Video's op het startscherm**: de map voor video's in het menu Start van Windows weergeven of verbergen.