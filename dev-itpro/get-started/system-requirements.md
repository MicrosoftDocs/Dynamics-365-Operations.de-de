---
title: Systemanforderungen
description: "In diesem Thema werden die Systemanforderungen für die aktuelle Version von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, für Cloud- und On-Premises-Bereitstellungen aufgeführt."
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: de-de
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>Systemanforderungen

[!include[banner](../includes/banner.md)]


In diesem Thema werden die Systemanforderungen für die aktuelle Version von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, für Cloud- und On-Premises-Bereitstellungen aufgeführt. Bevor Sie Finance and Operations, überprüfen Sie, wenn es angemessen ist, dass das System, mit dem Sie arbeiten, die Mindestnetzwerk-, Hardware und Softwareanforderungen erfüllt.


## <a name="supported-microsoft-office-applications"></a>Unterstützte Microsoft Office-Anwendungen
Die folgenden Office-Anwendungen werden in der Cloud und in On-Premises-Bereitsellungen von Finance and Operations unterstützt.
-   Zum Ausführen von Microsoft Excel- und Word-Add-Ins muss Microsoft Office 2016 für Windows oder Mac installiert sein. Genauere Informationen zu Versionsanforderungen erhalten Sie unter [Office-Integration – Problembehebung](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Um Dokumente anzuzeigen, die über die Funktionen für einen Export nach Excel oder einen Export nach Word erzeugt wurden, muss Microsoft Office 2007 oder höher installiert sein.

# <a name="system-requirements-specific-to-cloud-deployments"></a>Systemanforderungen spezifisch für Cloudbereitstellungen
## <a name="network-requirements"></a>Netzwerkanforderungen
-   Finance and Operations wurde für Netzwerke mit eine Latenzzeit von 250-300 Millisekunden (ms) oder weniger entwickelt. Dies ist die Latenzzeit von einem Browser-Client zum Microsoft Azure-Rechenzentrum, das Finance and Operations hostet. Es wird empfohlen, dass Sie die Netzwerkwartezeit unter <http://www.azurespeed.com> testen.
-   Bandbreitenanforderungen für Finance and Operations sind vom Szenario abhängig. In den meisten Fällen wird eine Bandbreite von mehr als 50 Kilobytes pro Sekunde (kbps) benötigt. Bei hohen Nutzlastanforderungen, beispielsweise Arbeitsbereiche oder Szenarien mit umfangreichen Anpassungen, wird eine höhere Bandbreite empfohlen.

Im Allgemeinen ist Finance and Operations für das Internet optimiert. Die Anzahl von Roundtrips von einem Browserclient zum Azure Rechenzentrum ist sehr klein, und die gesamte Nutzlast ist komprimiert. 

> [!WARNING]
> Berechnen Sie Bandbreitenanforderungen von einem Clientstandort nicht, indem Sie die Anzahl der Benutzer mit den Mindestbandbreitenanforderungen multiplizieren. Die gleichzeitige Nutzung eines bestimmten Standorts ist schwierig zu berechnen. Kunden, die sich Gedanken machen über die Bandbreitenanforderungen, sollten eine Vorabversion von Finance and Operations verwenden.

## <a name="net-framework-requirements"></a>.NET Framework-Anforderungen
Finance and Operations erfordert .NET Framework Version 4.6.2 für alle ClickOnce-Anwendungen, beispielsweise dem Dokumentweiterleitungsagenten. Installationsanweisungen erhalten Sie unter [Installieren von .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-web-browsers"></a>Unterstützte Webbrowser
Die Webanwendung kann in den folgenden Webbrowsern ausgeführt werden, die auf den angegebenen Betriebssysteme ausgeführt werden:


-   Microsoft Edge (letzte öffentlich verfügbare Version) unter Windows 10
-   Internet Explorer 11 unter Windows 10, Windows 8.1 oder Windows 7
-   Google Chrome (letzte öffentlich verfügbare Version) unter Windows 10, Windows 8.1, Windows 8, Windows 7 oder Google Nexus 10 Tablet
-   Apple Safari (letzte öffentlich verfügbare Version) auf Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) oder Apple iPad

Um die neueste Version für jeden Webbrowser zu suchen, wechseln Sie zur Website des Softwareherstellers. 

> [!NOTE]
> -   Es muss eine Vorabversion der Chrome-Erweiterung installiert werden, damit Screenshot-Bilder durch die Aufgabenaufzeichnung erfasst und in Microsoft Word-Dokumenten aufgenommen werden können. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   Der Workflow-Editor wird als ClickOnce-Anwendung gestartet. Nur Microsoft Edge and Internet Explorer (auf einer unterstützten Microsoft Windows-Version) unterstützen ClickOnce-Anwendungen. Die Workflow-Editor-ClickOnce-Anwendung erfordert ein kompatibles 64-Bit-Betriebssystem.
> -   Der Berichts-Designer für Finanzberichterstellung wird als ClickOnce-Anwendung gestartet. Er erfordert ein kompatibles 64-Bit-Betriebssystem. Wenn Sie Chrome verwenden, müssen Sie eine ClickOnce-Erweiterung installieren, um den Berichtsdesigner-Client herunterzuladen. Wenn Sie Chrome im unbekannten Modus verwenden, sollten Sie sicherstellen, dass die ClickOnce-Erweiterung auch für den unbekannten Modus aktiviert ist.
> -   Um PDF-Dateien in der Vorschau anzuzeigen, sollten Sie moderne Browser wie Microsoft Edge verwenden (aktuellste verfügbare Version) unter Windows 10 oder Google Chrome (aktuellste verfügbare Version) unter Windows 10, 8,1, Windows 8, Windows 7 oder Google Nexus-10 Tablet.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Unterstützte Webbrowser für Retail Cloud POS

Retail Cloud POS kann in den folgenden Webbrowsern ausgeführt werden, die auf den angegebenen Betriebssysteme ausgeführt werden:

-   Microsoft Edge (letzte öffentlich verfügbare Version) unter Windows 10
-   Internet Explorer 11 unter Windows 10, Windows 8.1 oder Windows 7
-   Chrome (letzte öffentlich verfügbare Version) unter Windows 10, Windows 8.1 oder Windows 7

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS-Anforderungen
### <a name="supported-operating-systems"></a>Unterstützte Betriebssysteme

-   Retail Modern POS ist eine 32-Bit-Anwendung, die sowohl auf x86- als auch auf x64-Architekturen ausgeführt werden kann.
-   Retail Modern POS wird von den Editionen Windows 10 Pro, Enterprise und Enterprise Long Term Servicing Branch (LTSB) unterstützt.

### <a name="minimum-system-requirements"></a>Mindestsystemanforderungen

-   Die unterstützte Mindestauflösung ist 1280 × 1024.
-   Der Computer, auf dem Retail Modern POS ausgeführt wird, muss folgende Anforderungen erfüllen:
    -   Er muss mindestens einen Dual-Core-Prozessor haben, der mit mindestens 2 Gigahertz (GHz) ausgeführt wird.
    -   Er muss einen RAM von mindestens 3 Gigabytes (GB) haben.
    -   Er muss einen Internetzugriff haben.

## <a name="retail-hardware-station-requirements"></a>Retail Hardware station-Anfoderungen
### <a name="supported-operating-systems"></a>Unterstützte Betriebssysteme

-   Retail Hardware station ist eine 32-Bit-Anwendung, die sowohl auf x86- als auch auf x64-Architekturen ausgeführt werden kann.
-   Retail Hardware station wird auf folgenden Betriebssystemen unterstützt:
    -   Windows 7 Professional, Enterprise und Ultimate 
    
    > [!NOTE]
    > Windows 7 wird nur unterstützt, wenn Internet Explorer 11 manuell im System installiert ist.

    -   Windows 8.1, Update 1 Professional, Enterprise und Embedded
    -   Windows 10 Pro, Enterprise und Enterprise LTSB

### <a name="minimum-system-requirements"></a>Mindestsystemanforderungen

Der Computer muss alle Systemanforderungen für das Einrichten und Verwenden der folgenden Elemente erfüllen:

-   Internetinformationsdienste (IIS)
-   Hardware von Drittanbietern

## <a name="retail-store-scale-unit-requirements"></a>Retail Store Scale Unit-Anforderungen
### <a name="supported-operating-systems"></a>Unterstützte Betriebssysteme

-   Retail Store Scale Unit ist eine 32-Bit-Anwendung, die sowohl auf x86- als auch auf x64-Architekturen ausgeführt werden kann.
-   Retail Store Scale Unit wird auf folgenden Betriebssystemen unterstützt:
    -   Windows 7 Professional, Enterprise und Ultimate
    -   Windows 8.1, Update 1 Professional, Enterprise und Embedded
    -   Windows 10 Pro, Enterprise und Enterprise LTSB

### <a name="minimum-system-requirements"></a>Mindestsystemanforderungen

-   4 GB RAM
-   1.6 GHz maximale CPU-Geschwindigkeit pro Kern (mindestens zwei Kerne erforderlich)
-   Mindestens 10 GB freier Speicherplatz (die Kanaldatenbank benötigt viel Speicherplatz)

### <a name="recommended-system-requirements"></a>Empfohlene Systemanforderungen

-   6 GB RAM
-   2.4 GHz i7 (oder vergleichbar) maximale CPU-Geschwindigkeit pro Kern (vier Kerne empfohlen)
-   Mindestens 10 GB freier Speicherplatz (die Kanaldatenbank benötigt viel Speicherplatz)

## <a name="connector-requirements"></a>Konnektoranforderungen
### <a name="supported-operating-systems"></a>Unterstützte Betriebssysteme

-   Der Konnektor für Microsoft Dynamics AX verfügt über zwei unterschiedliche Installationsprogramme, **Async-Server-Konnektor-Service** und **Echtzeit-Service für Dynamics AX 2012 R3**.
-   Beide Komponenten sind 32-Bit-Anwendung, die sowohl auf x86- als auch auf x64-Architekturen ausgeführt werden können.
-   Die Komponenten werden auf den folgenden Betriebssystemen unterstützt:
    -   Windows 7 Professional, Enterprise und Ultimate
    -   Windows 8.1, Update 1 Professional, Enterprise und Embedded
    -   Windows 10 Pro, Enterprise und Enterprise LTSB
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>Mindestsystemanforderungen

-   2 GB RAM von, 4 GB RAM wird empfohlen
-   1.6 GHz maximale CPU-Geschwindigkeit pro Kern (mindestens zwei Kerne erforderlich)
-   Mindestens 10 GB freier Speicherplatz (die Kanaldatenbank benötigt viel Speicherplatz)

## <a name="requirements-for-development-on-local-vms"></a>Anforderungen für Entwicklung auf lokalen VMs
Weitere Informationen zu den Anforderungen für die Entwicklung auf lokalen virtuellen Maschinen (VMs) finden Sie unter [Lokale VM-Ausführung](../dev-tools/access-instances.md).

# <a name="system-requirements-for-on-premises-deployments"></a>Systemanforderungen für On-Premises-Bereitstellungen

## <a name="network-requirements"></a>Netzwerkanforderungen
Finance and Operations (on-premises) kann in Netzwerken eingesetzt werden, die Internetprotokoll, Version 4, (IPv4), oder Internetprotokoll, Version 6, (IPv6), verwenden. Berücksichtigen Sie die Netzwerkumgebung, wenn Sie Ihr System planen und die folgenden Richtlinien verwenden.

### <a name="network-response-time"></a>Netzwerkantwortzeit
In der folgenden Tabelle werden die Mindestnetzwerkanforderungen für die Verbindung zwischen dem Webbrowser und Anwendungsobjektserver (AOS) sowie für die Verbindung zwischen AOS und der Datenbank in einem On-premises-System aufgeführt.

| Wert     | Webbrowser zu AOS | AOS zu Datenbank                                            |
|-----------|--------------------|------------------------------------------------------------|
| Bandbreite | 50 KB/s pro Benutzer   | 100 MB/s                                                   |
| Latenz   | < 250-300 ms       | < 1 ms (nur LAN). AOS und Datenbank müssen zusammengestellt werden. |

- Finance and Operations (on-premises) wurde für Netzwerke mit einer Latenzzeit von 250-300 Millisekunden (ms) oder weniger entwickelt. Diese Latenzzeit ist die Latenzzeit von einem Browser-Client zum Rechenzentrum, das Finance and Operations hostet.
- Bandbreitenanforderungen für Finance and Operations (on-premises) sind vom Szenario abhängig. Typische Szenarien benötigen einer Bandbreite von mehr als 50 Kilobytes pro Sekunde (KB/s) zwischen dem Browser und dem Finance and Operations-Server. Bei hohen Nutzlastanforderungen, beispielsweise Arbeitsbereiche oder Szenarien mit umfangreichen Anpassungen, wird eine höhere Bandbreite empfohlen und ist von der Benutzung abhängig.
Bereitstellungen, bei denen der AOS und die SQL Server-Datenbank in verschiedenen Rechenzentren sind, werden nicht unterstützt. Der AOS und die SQL Server-Datenbank müssen zusammengelegt werden. Im Allgemeinen ist Finance and Operations daraufhin optimiert, die Roundtrips von Browser zu Server zu reduzieren. Die Anzahl von Roundtrips von einem Browser-Client zum Rechenzentrum ist entweder NULL oder einer für jede Benutzerinteraktion, und die Nutzlast ist komprimiert.

> [!WARNING]
> Berechnen Sie keine Bandbreitenanforderungen von einem Clientstandort, indem Sie die Anzahl der Benutzer mit den Mindestbandbreitenanforderungen multiplizieren. Die gleichzeitige Nutzung eines bestimmten Standorts ist schwierig zu berechnen. Wir empfehlen die Verwendung einer Echtzeitsimulation gegenüber einer Nichtproduktionsumgebung von Finance and Operations als besten Maßstab der Leistung für Ihren spezifischen Fall. 

### <a name="lan-environments"></a>LAN-Umgebungen
In den Umgebungen lokaler Netzwerke (LAN) ist es nicht erforderlich, dass Microsoft-Remotedesktop in Microsoft Windows Server eine Verbindung mit Finance and Operations herstellt. Allerdings kann es für Wartungsvorgänge auf virtuellen Computern erforderlich sein, aus denen die Server-Bereitstellungen bestehen.

### <a name="wan-environments"></a>WAN-Umgebungen
In Umgebungen von Fernnetzen (WAN) ist es nicht erforderlich, dass Microsoft-Remotedesktop in Microsoft Windows Server eine Verbindung mit Finance and Operations herstellt.

### <a name="internet-connectivity-requirements"></a>Internetkonnektivitätsanforderungen
Finance and Operations (on-premises) erfordert keine Internetkonnektivität von Endbenutzer-Arbeitsstationen. Einige Funktionen sind jedoch ohne Internetkonnektivität nicht verfügbar.

| Browserclient | Ein Intranetszenario ohne Internetkonnektivität ist ein Designpunkt für die On-Premise-Bereitstellungsoption. Einige Funktionen, die Clouddienste benötigen, sind nicht verfügbar, wie Hilfe und Aufgabenleitfaden-Bibliotheken in LCS. |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Server         | Die AOS- oder Service Fabric-Ebene muss mit LCS kommunizieren können. Der browserbasierte On-Premise-Client benötigt keinen Internetzugriff.                                                                                |
| Telemetrie      | Telemetriedaten gehen möglicherweise verloren, wenn es lange Unterbrechungen bei der Konnektivität gibt. Unterbrechungen in der Konnektivität zu LCS wirken sich nicht auf die On-Premises-Anwendungsfunktionen auf.                                                |
| LCS            | Konnektivität zu LCS ist für die Bereitstellung, die Codebereitstellung sowie Wartungsvorgänge erforderlich.                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>Telemetriedatenübertragung in die Cloud
Die meiste Telemetrie wird lokal gespeichert und auf sie kann mithilfe der Ereignisanzeige in Microsoft Windows zugegriffen werden. Eine kleine Teilmenge von Telemetrieereignissen wird zur Microsoft-Telemetriepipeline in der Cloud zur Diagnose übertragen. Kundendaten und identifizierbare Endbenutzerdaten sind nicht Teil der Telemetrie, die an Microsoft gesendet wird. Namen von virtuellen Computern werden an Microsoft übermittelt, um die Umgebungsverwaltung und die Diagnose vom LCS-Portal zu unterstützen.

## <a name="domain-requirements"></a>Domänenanforderungen
Berücksichtigen Sie die folgenden Domänenanforderungen, wenn Sie Finance and Operations (on-premises) installieren:

- Virtuelle Computer, die Finance and Operations (on-premises)-Komponenten hosten, müssen zu einer Active Directory-Domäne gehören. Active Directory Domain Services (AD DS) müssen im nativen Modus konfiguriert sein.
- Virtuelle Computer, die Finance and Operations (on-premises)-Komponenten ausführen, müssen Zugriff aufeinander haben, der in Active Directory Domain Services konfiguriert ist. 
- Der Domänencontroller muss in Microsoft Windows Server 2016 ausgeführt werden.

## <a name="hardware-requirements"></a>Hardwareanforderungen
Dieser Abschnitt beschreibt die Hardware, die erforderlich ist, um Finance and Operations (on-premises) auszuführen.
Auf Basis der Systemkonfiguration, Datenenanordnung und der Anwendungen und Funktionen, zu deren Benutzung Sie sich entscheiden, können die tatsächlichen Hardwareanforderungen unterschiedlich sein. Nachfolgend sind einige Faktoren, die sich auf die Wahl der geeigneten Hardware für Finance and Operations (on-premises) auswirken könnten:

- Die Anzahl der Transaktionen pro Stunde.
- Die Anzahl der gleichzeitigen Benutzer.

## <a name="minimum-infrastructure-requirements"></a>Minimale Infrastrukturanforderungen
Finance and Operations (on-premises) verwendet Microsoft Azure Service Fabric, um den AOS, die Charge, die Datenverwaltung, den Management Reporter und die Umgebungsorchestratordienste zu hosten. Microsoft SQL Server Reporting Services (SSRS) werden nicht im Service Fabric-Cluster gehostet.
SQL Server muss in einem HADRON-Setup mit hoher Verfügbarkeit eingerichtet sein, das über mindestens zwei Knoten für die Produktionsverwendung verfügt.
Die folgende Abbildung zeigt die empfohlene Mindestanzahl von Knoten in Ihrem Service Fabric-Cluster an.

[![empfohlene Anzahl von Knoten für Service Fabric-Cluster](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Prozessor und RAM-Anforderungen
Die folgende Tabelle führt die Anzahl der Prozessoren und den Umfang des Arbeitsspeichers (RAM) auf, die für jede der Rollen erforderlich sind, die für die Ausführung dieser Bereitstellungsoption benötigt werden. Weitere Informationen finden Sie in den empfohlenen Mindestanforderungen für den eigenständigen Service Fabric-Cluster [Planen und Vorbereiten Ihres Service Fabric-Clusters](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Wenn andere Microsoft-Software auf demselben Computer installiert ist, muss dass System auch die Hardwareanforderungen für jene Software erfüllen. Es wird empfohlen, dass Sie andere Server-Anwendungen auf demselben Computer als AOS auf 1 Gigabyte (GB) RAM beschränken.

**Größenanpassung nach Rolle und Topologietyp**

| Topologie   | Rolle (Knotentyp)              | Empfohlene Prozessorkerne | Empfohlener Arbeitsspeicher (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| Produktion | AOS, Datenverwaltung, Charge   | 8                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |
| Sandbox    | AOS, Datenverwaltung, Charge   | 4                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |

**Minimale Größenanpassungsschätzungen für Produktions- und Sandboxbereitstellungen**\*

| Topologie                                  | Rolle                          | Anzahl der Instanzen |
|-------------------------------------------|-------------------------------|---------------------|
| Produktion                                | AOS (Datenverwaltung, Charge)  | 3                   |
|                                           | Management Reporter           | 2                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Orchestrator\*\*                | 3                   |
| Sandbox                                   | AOS, Datenverwaltung, Charge   | 2                   |
|                                           | Management Reporter           | 1                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Orchestrator                  | 3                   |
| *Zusammenfassende Produktions- und Sandboxtopologien* |                               | 16                  |

\*Diese Zahlen werden von unseren Vorschaudebitoren überprüft und werden möglicherweise nach Bedarf angepasst, basierend auf dem Feedback.

\*\*Orchestrator wird als Primärknotentyp festgelegt und wird auch verwendet, um die Service Fabric-Dienste auszuführen.

**Backend-SQL Server- und AD-Anfangsschätzungen**

[![Backend-SQL Server- und AD-Anfangsschätzungen](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*SQL Server-Größen sind stark von Arbeitsauslastungen abhängig. Weitere Informationen finden Sie im Abschnitt [Hardwaregrößenanpassung für On-Premises-Umgebungen](#Hardware-sizing-for-on-premises-environments).

## <a name="storage"></a>Lager

- **AOS** -– Finance and Operations (on-premises) verwendet eine Server Message Block (SMB) 3.0-Freigabe, um unstrukturierte Daten zu speichern. Weitere Informationen finden Sie unter [Direkte Speicherplätze in Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – Funktionsfähige Optionen:
    - Ein Solid State Drive (SSD)-Setup mit hoher Verfügbarkeit.
    - Ein Storage Area Network (SAN) optimiert für OLTP-Durchsätze.
    - Leistungsstarker direkt zugeordneter Speicher (DAS) 
- **SQL- und Datenverwaltungs-IOPS** – Der Speicher sowohl für die Datenverwaltung als auch für SQL Server sollte mindestens 2.000 input/output-Operationen pro Sekunde aufweisen. Produktions-IOPS hängt von vielen Faktoren ab. Weitere Informationen finden Sie im Abschnitt „Hardwaregrößenanpassung für On-Premises-Umgebungen”. 
- **IOPS des virtuellen Computers** – Jeder virtuelle Computer sollte mindestens 100 Schreibvorgänge in IOPS haben.

## <a name="virtual-host-requirements"></a>Virtuelle Hostanforderungen
Wenn Sie die virtuellen Hosts für eine Finance and Operations (on-premises)-Umgebung einrichten, entnehmen Sie Anleitungen aus den folgenden Richtlinien: [Planen und Vorbereiten Ihres Service Fabric-Clusters](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) und [Beschreibung eines Service Fabric-Clusters](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Jeder virtuelle Host sollte ausreichend Kerne für die Infrastruktur haben, deren Größe angepasst wird. Mehrere erweiterte Konfigurationen sind möglich, bei denen sich SQL Server in der physischen Hardware befindet, aber alles andere virtualisiert ist. Wenn SQL Server virtualisiert ist, sollte das Datenträgersubsystem ein schnelles SAN oder Vergleichbares sein. In allen Fällen sollten Sie sicherstellen, dass die grundlegenden Einstellungen des virtuellen Hosts hochverfügbar und redundant sind. In allen Fällen, wenn Virtualisierung verwendet wird, sollten keine VM-Momentaufnahmen gemacht werden.

## <a name="software-requirements-for-all-server-computers"></a>Softwareanforderungen für alle Servercomputer
Die folgende Software muss auf einem Computer vorhanden sein, bevor irgendwelche Finance and Operations (on-premises)-Komponenten installiert werden können:

- Microsoft .NET Framework 4.5.1 oder höher
- Service Fabric – weitere Informationen finden Sie unter [Planen und Vorbereiten Ihres Service Fabric-Clusters](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Unterstützte Serverbetriebssysteme
In der folgenden Tabelle werden die Serverbetriebssysteme aufgeführt, die für Finance and Operations-Komponenten unterstützt werden.

| Betriebssystem                                     | Hinweise                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 Datacenter oder Standard | Diese Anforderungen gelten für die Datenbank und den Service Fabric-Cluster, der AOS hostet. |

## <a name="software-requirements-for-database-servers"></a>Softwareanforderungen für Datenbankserver

- Nur 64-Bit-Versionen von SQL Server 2016 werden unterstützt.
- In einer Produktionsumgebung empfiehlt es sich, dass Sie das aktuellste kumulative Update (CU) für die von Ihnen verwendete Version von SQL Server installieren.
- Finance and Operations (on-premises) unterstützt Unicode-Sortierungen, bei denen Groß-/Kleinschreibung, Akzente und Kana beachtet werden muss, aber die Breite nicht beachtet werden muss. Die Sortierung muss dem Windows-Gebietsschema der Computer entsprechen, auf denen AOS-Instanzen ausgeführt werden. Wenn Sie eine neue Installation einrichten, wird empfohlen, dass Sie eine Windows-Sortierung anstelle einer SQL Server-Sortierung auswählen. Weitere Informationen zum Auswählen einer Sortierung für eine SQL Server-Datenbank finden Sie in der [SQL Server-Dokumentation](/sql/sql-server/sql-server-technical-documentation).
In der folgenden Tabelle werden die SQL Server-Versionen aufgeführt, die für die Finance and Operations-Datenbanken unterstützt werden. Weitere Informationen finden Sie unter den Mindesthardwareanforderungen für [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016).

| Ausweichressourcenleistung                                                      | Hinweise                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard Edition oder Enterprise Edition | Informationen zu den Hardwareanforderungen für SQL Server 2016 finden Sie unter [Hardware- und Softwareanforderungen zum Einrichten von SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-client-computers"></a>Softwareanforderungen für Clientcomputer
Die Finance and Operations-Webanwendung kann auf jedem beliebigen Gerät mit einem HTML5.0-kompatiblen Webbrowser ausgeführt werden. Spezifische Gerät-/Browserkombinationen, die Microsoft bestätigt hat, umfassen:

- Microsoft Edge (letzte öffentlich verfügbare Version) unter Windows 10
- Internet Explorer 11 unter Windows 10, Windows 8.1 oder Windows 7
- Google Chrome (letzte öffentlich verfügbare Version) unter Windows 10, Windows 8.1, Windows 8, Windows 7 oder Google Nexus 10 Tablet
- Apple Safari (letzte öffentlich verfügbare Version) auf Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) oder Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Softwareanforderungen für Active Directory-Verbunddienste 
Active Directory-Verbunddienste (AD FS) auf Windows Server 2016

Der Domänencontroller muss Windows Server 2012 R2 oder höher sein, mit einer Domänenfunktionsebene von 2012 R2 oder höher

Weitere Informationen zu Domänenfunktionsebenen finden Sie unter: 
- [Was sind Active Directory-Funktionsebenen](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Grundlegendes zu Active Directory Domain Services-Funktionsebenen](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Hardware- und Softwareanforderungen für Retail Komponenten
Finance and Operations (on-premises) umfasst gegenwärtig nicht die Retail Komponenten.

<a name="see-also"></a>Siehe auch
--------

[Eine Evaluationskopie von Dynamics 365 for Finance and Operations, Enterprise-Edition abrufen](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

