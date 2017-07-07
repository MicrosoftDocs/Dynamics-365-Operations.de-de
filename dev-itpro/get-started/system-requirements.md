---
title: Systemanforderungen
description: "In diesem Thema werden die Systemanforderungen für die aktuelle Version von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, aufgeführt."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 724ee7ec29f8a9c4e8cc0b244193cd6c83c37f03
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017


---

# <a name="system-requirements"></a>Systemanforderungen

[!include[banner](../includes/banner.md)]


In diesem Thema werden die Systemanforderungen für die aktuelle Version von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, aufgeführt.

<a name="supported-web-browsers"></a>Unterstützte Webbrowser
----------------------

Die Webanwendung kann in den folgenden Webbrowsern ausgeführt werden, die auf den angegebenen Betriebssysteme ausgeführt werden:

-   Microsoft Edge (letzte öffentlich verfügbare Version) unter Windows 10
-   Internet Explorer 11 unter Windows 10, Windows 8.1 oder Windows 7
-   Google Chrome (letzte öffentlich verfügbare Version) unter Windows 10, Windows 8.1, Windows 8, Windows 7 oder Google Nexus 10 Tablet
-   Apple Safari (letzte öffentlich verfügbare Version) auf Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) oder Apple iPad

Um die neueste Version für jeden Webbrowser zu suchen, wechseln Sie zur Website des Softwareherstellers. 

**Hinweise:**

-   Es muss eine Vorabversion der Chrome-Erweiterung installiert werden, damit Screenshot-Bilder durch die Aufgabenaufzeichnung erfasst und in Microsoft Word-Dokumenten aufgenommen werden können. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
-   Der Workflow-Editor wird als ClickOnce-Anwendung gestartet. Nur Microsoft Edge and Internet Explorer (auf einer unterstützten Microsoft Windows-Version) unterstützen ClickOnce-Anwendungen. Die Workflow-Editor-ClickOnce-Anwendung erfordert ein kompatibles 64-Bit-Betriebssystem.
-   Der Berichts-Designer für Finanzberichterstellung wird als ClickOnce-Anwendung gestartet. Er erfordert ein kompatibles 64-Bit-Betriebssystem. Wenn Sie Chrome verwenden, müssen Sie eine ClickOnce-Erweiterung installieren, um den Berichtsdesigner-Client herunterzuladen. Wenn Sie Chrome im unbekannten Modus verwenden, sollten Sie sicherstellen, dass die ClickOnce-Erweiterung auch für den unbekannten Modus aktiviert ist.
-   Um PDF-Dateien in der Vorschau anzuzeigen, sollten Sie moderne Browser wie Microsoft Edge verwenden (aktuellste verfügbare Version) unter Windows 10 oder Google Chrome (aktuellste verfügbare Version) unter Windows 10, 8,1, Windows 8, Windows 7 oder Google Nexus-10 Tablet.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Unterstützte Webbrowser für Retail Cloud POS

Retail Cloud POS kann in den folgenden Webbrowsern ausgeführt werden, die auf den angegebenen Betriebssysteme ausgeführt werden:

-   Microsoft Edge (letzte öffentlich verfügbare Version) unter Windows 10
-   Internet Explorer 11 unter Windows 10, Windows 8.1 oder Windows 7
-   Chrome (letzte öffentlich verfügbare Version) unter Windows 10, Windows 8.1 oder Windows 7

## <a name="network-requirements"></a>Netzwerkanforderungen
-   Dynamics 365 for Finance and Operations, Enterprise Edition, wurde für Netzwerke mit eine Latenzzeit von 250-300 Millisekunden (ms) oder weniger entwickelt. Dies ist die Latenzzeit von einem Browser-Client zum Microsoft Azure-Rechenzentrum, das Finance and Operations hostet. Es wird empfohlen, dass Sie die Netzwerkwartezeit unter <http://www.azurespeed.com> testen.
-   Bandbreitenanforderungen hängen vom Szenario ab. In den meisten Fällen wird eine Bandbreite von mehr als 50 Kilobytes pro Sekunde (kbps) benötigt. Bei hohen Nutzlastanforderungen, beispielsweise Arbeitsbereiche oder Szenarien mit umfangreichen Anpassungen, wird eine höhere Bandbreite empfohlen.

Im Allgemeinen ist Finance and Operations für das Internet optimiert. Die Anzahl von Roundtrips von einem Browserclient zum Azure Rechenzentrum ist sehr klein, und die gesamte Nutzlast ist komprimiert. 

**Warnung:** Berechnen Sie Bandbreitenanforderungen von einem Clientstandort nicht, indem Sie die Anzahl der Benutzer mit den Mindestbandbreitenanforderungen multiplizieren. Die gleichzeitige Nutzung eines bestimmten Standorts ist schwierig zu berechnen. Kunden, die sich Gedanken machen über die Bandbreitenanforderungen, sollten eine Vorabversion von Finance and Operations verwenden.

## <a name="net-framework-requirements"></a>.NET Framework-Anforderungen
.NET Framework Version 4.6.2 ist für alle ClickOnce-Anwendungen wie beispielsweise den Dokumentweiterleitungsagenten erforderlich. Installationsanweisungen erhalten Sie unter [Installieren von .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Unterstützte Microsoft Office-Anwendungen
-   Zum Ausführen von Microsoft Excel- und Word-Add-Ins muss Microsoft Office 2016 für Windows oder Mac installiert sein. Genauere Informationen zu Versionsanforderungen erhalten Sie unter [Office-Integration – Problembehebung](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Um Dokumente anzuzeigen, die über die Funktionen für einen Export nach Excel oder einen Export nach Word erzeugt wurden, muss Microsoft Office 2007 oder höher installiert sein.

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
    -   Windows 7 Professional, Enterprise und Ultimate **Hinweis:** Windows 7 wird nur unterstützt, wenn der Internet Explorer 11 manuell auf dem System installiert ist.
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

<a name="see-also"></a>Siehe auch
--------

[Eine Evaluationskopie von Dynamics 365 for Finance and Operations, Enterprise-Edition abrufen](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)





