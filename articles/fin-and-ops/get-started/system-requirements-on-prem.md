---
title: "Systemanforderungen für On-Premises-Bereitstellungen"
description: "In diesem Thema werden die Systemanforderungen für die aktuelle Version von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, für Cloud- und On-Premises-Bereitstellungen aufgeführt."
author: kfend
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 73fefd43c9de917dc6c98b2a6893b36a5c0ccdc5
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a>Systemanforderungen für On-Premises-Bereitstellungen

[!include[banner](../includes/banner.md)]

In diesem Thema werden die Systemanforderungen für die aktuelle Version von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, für Cloud- und On-Premises-Bereitstellungen aufgeführt. Bevor Sie Finance and Operations, überprüfen Sie, wenn es angemessen ist, dass das System, mit dem Sie arbeiten, die Mindestnetzwerk-, Hardware und Softwareanforderungen erfüllt.

## <a name="network-requirements"></a>Netzwerkanforderungen
Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (lokal) kann bei verschiedenen Netzwerken arbeiten, die Internetprotokoll-Version (4) oder IPv4 Internetprotokoll, Version 6 (IPv6) verwenden. Berücksichtigen Sie die Netzwerkumgebung, wenn Sie Ihr System planen und die folgenden Richtlinien verwenden.

### <a name="network-response-time"></a>Netzwerkantwortzeit
In der folgenden Tabelle werden die Mindestnetzwerkanforderungen für die Verbindung zwischen dem Webbrowser und Anwendungsobjektserver (AOS) sowie für die Verbindung zwischen AOS und der Datenbank in einem On-premises-System aufgeführt.

| Wert     | Webbrowser zu AOS                      | AOS zu Datenbank |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| Bandbreite | 50 Kilobytes pro Sekunde (KBit/s) pro Benutzer | 100 (MBit/s Megabytes pro Sekunde) |
| Latenz   | Weniger als 250-300 Millisekunden (ms)     | Weniger als 1 ms (nur lokales Netzwerk [LAN]). AOS und Datenbank müssen zusammengestellt werden. |

- Finance and Operations (on-premises) wurde für Netzwerke mit einer Latenzzeit von 250-300 Millisekunden (ms) oder weniger entwickelt. Diese Latenzzeit ist die Latenzzeit von einem Browser-Client zum Rechenzentrum, das Finance and Operations hostet.
- Bandbreitenanforderungen für Finance and Operations (on-premises) sind vom Szenario abhängig. Typische Szenarien benötigen einer Bandbreite von mehr als 50 Kilobytes pro Sekunde (KB/s) zwischen dem Browser und dem Finance and Operations-Server. Bei hohen Nutzlastanforderungen, beispielsweise Arbeitsbereiche oder Szenarien mit umfangreichen Anpassungen, wird eine höhere Bandbreite empfohlen. Die bestimmte Betrag von Bandbreite hängt von der Verwendung aus.

Bereitstellungen, bei denen der AOS und die Microsoft SQL Server-Datenbank in verschiedenen Rechenzentren sind, werden nicht unterstützt. AOS und SQL Datenbank müssen zusammengestellt werden. 

Im Allgemeinen ist Finance and Operations daraufhin optimiert, die Roundtrips von Browser zu Server zu reduzieren. Die Anzahl von Roundtrips von einem Browser-Client zum Rechenzentrum ist entweder NULL oder einer für jede Benutzerinteraktion, und die Nutzlast ist komprimiert.

> [!WARNING]
> Berechnen Sie keine Bandbreitenanforderungen von einem Clientstandort, indem Sie die Anzahl der Benutzer mit den Mindestbandbreitenanforderungen multiplizieren. Die gleichzeitige Nutzung eines bestimmten Standorts ist schwierig zu berechnen. Wir empfehlen die Verwendung einer Echtzeitsimulation gegenüber einer Nichtproduktionsumgebung von Finance and Operations als besten Maßstab der Leistung für Ihren spezifischen Fall. 

### <a name="lan-environments"></a>LAN-Umgebungen
In den Umgebungen lokaler Netzwerke (LAN) ist es nicht erforderlich, dass Microsoft-Remotedesktop in Microsoft Windows Server eine Verbindung mit Finance and Operations herstellt. Allerdings kann es für Wartungsvorgänge auf virtuellen Computern erforderlich sein, aus denen die Server-Bereitstellungen bestehen.

### <a name="wan-environments"></a>WAN-Umgebungen
In Umgebungen von Fernnetzen (WAN) ist es nicht erforderlich, dass Microsoft-Remotedesktop in Microsoft Windows Server eine Verbindung mit Finance and Operations herstellt.

### <a name="internet-connectivity-requirements"></a>Internetkonnektivitätsanforderungen
Finance and Operations (lokal) erfordert keine Internetkonnektivität von Endbenutzer-Arbeitsstationen. Einige Funktionen sind jedoch ohne Internetkonnektivität nicht verfügbar.

|                    |   |
|--------------------|---|
| **Browserclient** | Ein Intranetszenario ohne Internetkonnektivität ist ein Designpunkt für die On-Premise-Bereitstellungsoption. Einige Funktionen, die Clouddienste benötigen, sind nicht verfügbar, wie Hilfe und Aufgabenleitfadenbibliotheken in Microsoft Dynamics Lifecycle Services (LCS). |
| **Server**         | Die AOS- oder Microsoft Azure Service Fabric-Ebene muss mit LCS kommunizieren können. Der browserbasierte On-Premise-Client benötigt keinen Internetzugriff. |
| **Telemetrie**      | Telemetriedaten gehen möglicherweise verloren, wenn es lange Unterbrechungen bei der Konnektivität gibt. Unterbrechungen in der Konnektivität zu LCS wirken sich nicht auf die On-Premises-Anwendungsfunktionen auf. |
| **LCS**            | Konnektivität zu LCS ist für die Bereitstellung, die Codebereitstellung sowie Wartungsvorgänge erforderlich. |

## <a name="telemetry-data-transfer-to-the-cloud"></a>Telemetriedatenübertragung in die Cloud
Die meisten Telemetriedaten werden lokal gespeichert und auf sie kann mithilfe der Ereignisanzeige in Microsoft Windows zugegriffen werden. Eine kleine Teilmenge von Telemetrieereignissen wird zur Microsoft-Telemetriepipeline in der Cloud zur Diagnose übertragen. Kundendaten und identifizierbare Endbenutzerdaten sind nicht Teil der Telemetriedaten, die an Microsoft gesendet wird. Namen von virtuellen Computern werden an Microsoft übermittelt, um die Umgebungsverwaltung und die Diagnose vom LCS-Portal zu unterstützen.

## <a name="domain-requirements"></a>Domänenanforderungen
Berücksichtigen Sie die folgenden Domänenanforderungen, wenn Sie Finance and Operations (on-premises) installieren:

- Virtuelle Computer, die Finance and Operations (on-premises)-Komponenten hosten, müssen zu einer Active Directory-Domäne gehören. Active Directory Domain Services (AD DS) müssen im nativen Modus konfiguriert sein.
- WM, die Berichte auf Finance and Operations (lokale) Komponenten ausführen, müssen gegenseitig Zugriff haben. Dieser wird im AD DS Zugriff konfiguriert. 
- Der Domänencontroller muss Microsoft Windows Server 2012 R2 oder höher sein, mit einer Domänenfunktionsebene von 2012 R2 oder höher

## <a name="hardware-requirements"></a>Hardwareanforderungen
Dieser Abschnitt beschreibt die Hardware, die erforderlich ist, um Finance and Operations (on-premises) auszuführen.

Die tatsächlichen Hardware-Anforderungen sind unterschiedlich, basierend auf der Systemkonfiguration, der Datenenanordnung und der Anwendungen und Funktionen, zu deren Benutzung Sie sich entscheiden, können die tatsächlichen Hardwareanforderungen unterschiedlich sein. Nachfolgend sind einige Faktoren, die sich auf die Wahl der geeigneten Hardware für Finance and Operations (on-premises) auswirken könnten:

- Die Anzahl der Transaktionen pro Stunde.
- Die Anzahl der gleichzeitigen Benutzer.

## <a name="minimum-infrastructure-requirements"></a>Minimale Infrastrukturanforderungen
Finance and Operations (lokal) verwendet Service Fabric, um den AOS, die Charge, die Datenverwaltung, den Management Reporter und die Umgebungsorchestratordienste zu hosten. 

SQL Server muss in einem HADRON-Setup mit hoher Verfügbarkeit eingerichtet sein, das über mindestens zwei Knoten für die Produktionsverwendung verfügt.

Die folgende Abbildung zeigt die empfohlene Mindestanzahl von Knoten in Ihrem Service Fabric-Cluster an.

[![Empfohlene Anzahl von Knoten für Service Fabric-Cluster](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Prozessor und RAM-Anforderungen
Die folgende Tabelle führt die Anzahl der Prozessoren und den Umfang des Arbeitsspeichers (RAM) auf, die für jede der Rollen erforderlich sind, die für die Ausführung dieser Bereitstellungsoption benötigt werden. Weitere Informationen finden Sie in den empfohlenen Mindestanforderungen für den eigenständigen Service Fabric-Cluster [Planen und Vorbereiten Ihres Service Fabric-Clusters](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Wenn andere Microsoft-Software auf demselben Computer installiert ist, muss dass System auch die Hardwareanforderungen für jene Software erfüllen. Wenn andere Anwendungen auf demselben Computer als AOS empfohlen sind, empfehlen wir, dass Sie jene Serveranwendung auf 1 Gigabyte (GB) RAM beschränken.

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

**Minimale Größenanpassungsschätzungen für Produktions- und Sandboxbereitstellungen\***

| Topologie                                        | Rolle                          | Anzahl der Instanzen |
|-------------------------------------------------|-------------------------------|---------------------|
| Produktion                                      | AOS (Datenverwaltung, Charge)  | 3                   |
|                                                 | Management Reporter           | 2                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | Orchestrator\*\*              | 3                   |
| Sandbox                                         | AOS, Datenverwaltung, Charge   | 2                   |
|                                                 | Management Reporter           | 1                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | Orchestrator                  | 3                   |
| *Zusammenfassende Produktions- und Sandboxtopologien* |                               | *16*                |

\* Die Nummern in dieser Tabelle werden von unseren Vorschaukunden geprüft und möglicherweise auf Basis der Feedbacks jener Debitoren angepasst werden.

\*\* Orchestrator wird als Primärknotentyp festgelegt und wird auch verwendet, um die Service Fabric-Dienste auszuführen.

**Anfangsschätzungen für den Backend-SQL-Servver und AD DS**

<table>
<thead>
<tr>
<th></th>
<th>Rolle</th>
<th>VMs/Instanzen</th>
<th>Kerne</th>
<th>Gesamte Kerne</th>
<th>Speicher pro Instanz (GB)</th>
<th>Gesamter Arbeitsspeicher GB</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>Freigegebene Infrastruktur</strong></td>
<td>SQL-Server*</td>
<td>2</td>
<td>8</td>
<td>16</td>
<td>32</td>
<td>64</td>
</tr>
<tr>
<td>Dateiserver/Storage Area Network/ausdrücklich verfügbarer Speicher</td>
<td colspan="5"><p>Die Backend-Speicherung muss auf einem Festkörperlaufwerke (SSDs) auf einem Ablaufstorage Area Network (SAN) sein.</p>
<p>Größen- und Eingabe/Ausgabe-Arbeitsgänge pro Sekunde (IOPS)- Durchsatz basiert auf den Größen der Arbeitsauslastung.</p></td>
</tr>
<tr>
<td>Active Directory</td>
<td>3</td>
<td>4</td>
<td>12</td>
<td>16</td>
<td>48</td>
</tr>
<tr>
<td><em>Zusammenfassung für freigegebene Infrastruktur</em></td>
<td></td>
<td><em>5</em></td>
<td></td>
<td><em>28</em></td>
<td></td>
<td><em>112</em></td>
</tr>
</tbody>
</table>

\* SQL Server-Größen sind stark von Arbeitsauslastungen abhängig. Weitere Informationen finden Sie im Abschnitt [Hardwaregrößenanpassung für lokale-Umgebungen](hardware-sizing-on-premises-environments.md).

## <a name="storage"></a>Lager

- **AOS** -– Finance and Operations (lokal) verwendet eine Server Message Block (SMB) 3.0-Freigabe, um unstrukturierte Daten zu speichern. Weitere Informationen finden Sie unter [Direkte Speicherplätze in Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – Die folgenden Optionen sind verfügbar:

    - Eine ausdrücklich verfügbare SSD-Einstellung
    - Ein SAN, das für Online Transaction Processing (OKTP) optimiert ist
    - Leistungsstarker direkt zugeordneter Speicher (DAS) 

- **SQL-Server und Datenverwaltungs-IOPS** – Der Speicher sowohl für die Datenverwaltung als auch für SQL Server sollte mindestens 2.000 input/output-Operationen pro Sekunde aufweisen. Produktions-IOPS hängt von vielen Faktoren ab. Weitere Informationen finden Sie im Abschnitt [Hardwaregrößenanpassung für lokale-Umgebungen](hardware-sizing-on-premises-environments.md).
- Jedes –**VM-IOPS** VM sollte mindestens 100 IOPS schreiben können.

## <a name="virtual-host-requirements"></a>Virtuelle Hostanforderungen
Wenn Sie die virtuellen Hosts für eine Finance and Operations (lokal)-Umgebung einrichten, entnehmen Sie Anleitungen aus den folgenden Richtlinien: [Planen und Vorbereiten Ihres Service Fabric-Clusters](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) und [Beschreibung eines Service Fabric-Clusters](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Jeder virtuelle Host sollte ausreichend Kerne für die Infrastruktur haben, deren Größe angepasst wird. Mehrere erweiterte Konfigurationen sind möglich, bei denen sich SQL Server in der physischen Hardware befindet, aber alles andere virtualisiert ist. Wenn SQL Server virtualisiert ist, sollte das Datenträgersubsystem ein schnelles SAN oder Vergleichbares sein. In allen Fällen sollten Sie sicherstellen, dass die grundlegenden Einstellungen des virtuellen Hosts hochverfügbar und redundant sind. In allen Fällen, wenn Virtualisierung verwendet wird, sollten keine VM-Momentaufnahmen gemacht werden.

## <a name="software-requirements-for-all-server-computers"></a>Softwareanforderungen für alle Servercomputer
Die folgende Software muss auf einem Computer vorhanden sein, bevor irgendwelche Finance and Operations (on-premises)-Komponenten installiert werden können:

- Die Microsoft .NET Framework-Version 4.5.1 oder später
- Service-Gewebe

Weitere Informationen finden Sie unter [Planen und Vorbereiten Ihres Service Fabric-Clusters](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Unterstützte Serverbetriebssysteme
In der folgenden Tabelle werden die Serverbetriebssysteme aufgeführt, die für Finance and Operations-Komponenten unterstützt werden.

| Betriebssystem                                     | Hinweise |
|------------------------------------------------------|-------|
| Microsoft Windows Server 2016 Datacenter oder Standard | Diese Anforderungen gelten für die Datenbank und den Service Fabric-Cluster, der AOS hostet. |

## <a name="software-requirements-for-database-servers"></a>Softwareanforderungen für Datenbankserver

- Nur 64-Bit-Versionen von SQL Server 2016 werden unterstützt.
- In einer Produktionsumgebung empfiehlt es sich, dass Sie das aktuellste kumulative Update (CU) für die von Ihnen verwendete Version von SQL Server installieren.
- Finance and Operations (on-premises) unterstützt Unicode-Sortierungen, bei denen Groß-/Kleinschreibung, Akzente und Kana beachtet werden muss, aber die Breite nicht beachtet werden muss. Die Sortierung muss dem Windows-Gebietsschema der Computer entsprechen, auf denen AOS-Instanzen ausgeführt werden. Wenn Sie eine neue Installation einrichten, wird empfohlen, dass Sie eine Windows-Sortierung anstelle einer SQL Server-Sortierung auswählen. Weitere Informationen zum Auswählen einer Sortierung für eine SQL Server-Datenbank finden Sie in der [SQL Server-Dokumentation](/sql/sql-server/sql-server-technical-documentation).

In der folgenden Tabelle werden die SQL Server-Versionen aufgeführt, die für die Finance and Operations-Datenbanken unterstützt werden. Weitere Informationen finden Sie unter den Mindesthardwareanforderungen für [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016).

| Ausweichressourcenleistung                                                      | Hinweise |
|------------------------------------------------------------------|-------|
| Microsoft SQL Server 2016 Standard Edition oder Enterprise Edition | Informationen zu den Hardwareanforderungen für SQL Server 2016 finden Sie unter [Hardware- und Softwareanforderungen zum Einrichten von SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-application-object-server-aos"></a>Softwareanforderungen für Application Object Server (AOS) 
- SQL Server Integration Services (SSIS)

## <a name="software-requirements-for-reporting-server-bi"></a>Softwareanforderungen für Berichtsserver (BI)
- SQL Server Reporting Services (SSRS)

## <a name="software-requirements-for-client-computers"></a>Softwareanforderungen für Clientcomputer
Die Finance and Operations-Webanwendung kann auf jedem beliebigen Gerät mit einem HTML 5.0-kompatiblen Webbrowser ausgeführt werden. Spezifische Gerät-/Browserkombinationen, die Microsoft bestätigt hat, umfassen:

- Microsoft Edge (letzte öffentlich verfügbare Version) unter Windows 10
- Internet Explorer 11 unter Windows 10, Windows 8.1 oder Windows 7
- Google Chrome (letzte öffentlich verfügbare Version) unter Windows 10, Windows 8.1, Windows 8, Windows 7 oder Google Nexus 10 Tablet
- Apple Safari (letzte öffentlich verfügbare Version) auf Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) oder Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Softwareanforderungen für Active Directory-Verbunddienste 
Active Directory-Verbunddienste (AD FS) auf Windows Server 2016 ist erforderlich.

Der Domänencontroller muss Microsoft Windows Server 2012 R2 oder höher sein, mit einer Domänenfunktionsebene von 2012 R2 oder höher. Weitere Informationen zu Domänenfunktionsebenen finden Sie unter:

- [Was sind Active Directory-Funktionsebenen](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Grundlegendes zu Active Directory Domain Services-Funktionsebenen](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="supported-microsoft-office-applications"></a>Unterstützte Microsoft Office-Anwendungen
Die folgenden Microsoft Office-Anwendungen werden in der Cloud und in On-Premises-Bereitstellungen von Finance and Operations unterstützt.

-   Zum Ausführen von Microsoft Excel- und Microsoft Word-Add-Ins muss Microsoft Office 2016 für Windows oder Mac installiert sein. Genauere Informationen zu Versionsanforderungen erhalten Sie unter [Office-Integration – Problembehebung](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Um Dokumente anzuzeigen, die über die Funktionen für einen Export nach Excel oder einen Export nach Word erzeugt wurden, muss Microsoft Office 2007 oder höher installiert sein.
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Hardware- und Softwareanforderungen für Retail Komponenten
Finance and Operations (lokal) umfasst gegenwärtig nicht die Retail Komponenten.

