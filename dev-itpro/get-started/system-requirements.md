---
title: Systemanforderungen
description: "Dieses Thema werden die Systemanforderungen für die aktuelle Version von Microsoft Dynamics 365 für Arbeitsgänge auf."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>Systemanforderungen

Dieses Thema werden die Systemanforderungen für die aktuelle Version von Microsoft Dynamics 365 für Arbeitsgänge auf.

<a name="supported-web-browsers"></a>Unterstützte Webbrowser
----------------------

Das Microsoft Dynamics 365 für Arbeitsgangswebanwendung kann in folgende Webbrowser ausgeführt werden, die für die angegebenen Betriebssysteme ausgeführt werden:

-   Microsoft umranden spät öffentlich - verfügbare (Version) unter Windows 10
-   Internet Explorer 11 unter Windows 10, Windows 8.1 oder Windows 7
-   Google Chrome (zu spät öffentlich - verfügbare Version) unter Windows 10 - 8,1 -, Windows, Windows, Windows 8 - 7 - oder- Google Nexus-10 Tablet
-   Apple Safari spät öffentlich - verfügbare (Version) auf Mac OS X 10,10 (Yosemite), 10,11 (EL Capitan) oder 10,12 (Sierra) oder APPLE-iPad

Um die neueste Version für jeden Webbrowser zu suchen, wechseln Sie zur Website des Softwareherstellers. **Hinweise:**

-   Wenn Sie Bilder aufzuzeichnen die von der Aufgabenaufzeichnung und in den Microsoft Word-Dokumenten einzubeziehen generiert werden, muss eine Chrome-Erweiterung installierte haben. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Der Workflow-Editor wird als ClickOnce-Bewerbung gestartet. Nur umranden und Microsoft Internet Explorers (auf einer unterstützten Version von Microsoft Windows Unterstützungs-ClickOnce-Bewerbungen). Die Workflow-Editor-ClickOnce-Bewerbung erforderlich kompatibles 64-Bit-Betriebssystem ein.
-   Der für Berichts-Designer Finanzberichterstellung wird als ClickOnce-Bewerbung gestartet. Sie müssen ein kompatibles 64-Bit-Betriebssystem. Wenn Sie Chrome verwenden, müssen Sie eine ClickOnce-Erweiterung einrichten, um den Berichts-Designer-Kunden herunterzuladen. Wenn Sie dem Chrome unbekannten Modus verwenden, sollten Sie sicherstellen, dass die ClickOnce-Erweiterung auch für unbekannten Modus aktiviert ist.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Unterstützte Webbrowser für Retail Cloud POS

Kleincloud POS für Dynamics 365 für Arbeitsgänge kann in folgende Webbrowser ausgeführt werden, die für die angegebenen Betriebssysteme ausgeführt werden:

-   Microsoft umranden spät öffentlich - verfügbare (Version) unter Windows 10
-   Internet Explorer 11 unter Windows 10, Windows 8.1 oder Windows 7
-   Chrome (zu spät öffentlich - verfügbare Version) 10 unter Windows, Windows 8,1 oder Windows 7

## <a name="network-requirements"></a>Netzwerkanforderungen
-   Dynamics 365 für Arbeitsgänge ist für Wartezeit Netzwerke mit von weniger als 150 Millisekunden (ms) entwickelt. Dies ist die Wartezeit von einem Browserclienten auf Microsoft Dynamics Azure-Rechenzentrum, das 365 hostet für Arbeitsgänge. Es wird empfohlen, dass Sie Netzwerkwartezeit unter http://www.azurespeed.com < testen.>
-   Bandbreitenanforderungen für Dynamics 365 für Arbeitsgänge sind von dem Szenario ab. Die meisten typischen Szenarien benötigen einer Bandbreite von mehr als 50 Kilobytes pro Sekunde (KBit/s). Für Szenarien, die hohe Ladungsanforderungen haben, z oder Arbeitsbereiche Szenarien, die Ihr Anpassung umfassen, wird empfohlen Bandbreite mehr.

Im Allgemeinen wird Dynamics 365 für Arbeitsgänge für das Internet finden. Die Anzahl von Roundtrips von einem Browserclienten dem Azure Rechenzentrum ist sehr klein, und die gesamte Hierbei wird zusammengefasst. ** Warnend: ** Berechnen Sie Bandbreitenanforderungen von einem Kundenlagerplatz nicht, indem Sie die Anzahl der Benutzer durch die Mindestbandbreitenanforderungen multiplizieren. Die Verwendung eines bestimmten Lagerplatzes gleichzeitige ist sehr schwierig zu berechnen. Für Debitoren, die über Bandbreitenanforderungen Planungsreihenfolge, verwenden Sie eine Vorschauversion von Microsoft Dynamics 365 für Arbeitsgänge.

## <a name="net-framework-requirements"></a>.NET Framework-Anforderungen
Dynamics 365 für Arbeitsgänge erfordert .NET Framework Version 4.6.2 für alle Klick-sobald Bewerbungen, wie der Dokumentroutingagent. Für Installationsanweisungen finden Sie [] (https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx) .NET Framework werden müssen.

## <a name="supported-microsoft-office-applications"></a>Unterstützte Microsoft Office-Bewerbungen
-   Für die Microsoft Excel- und Word-Add-Ins ausführen möchten, müssen Sie Microsoft Office 2016 für Windows oder Mac haben, die eingerichtet wurden. Genauere Informationen zu Versionsanforderungen, finden Sie Office-Integrationsproblembehandlung [] (/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting ).
-   Um Dokumente anzuzeigen die vom Export in Excel erzeugt oder in Word-Funktionen exportieren, müssen Sie Microsoft Office 2007 oder später installiert haben.

## <a name="retail-modern-pos-requirements"></a>Moderne POS-KleinAnforderungen
### <a name="supported-operating-systems"></a>Unterstützte Betriebssysteme

-   Modernes KleinPOS ist eine 32-Bit-Anwendung, doch es wird auf x86- und x64-Architekturen ausgeführt.
-   Modernes wird nur auf KleinPOS Zweigstelle Windows 10s Pro, Enterprises und Verwalten Enterprises langfristige (LTSB)- Editionen unterstützt.

### <a name="minimum-system-requirements"></a>Systemanforderungen

-   Die Höchst- unterstützte Lösung × 1280 1024.
-   Der Computer, modernes den KleinPOS ausgeführt wird, muss diese Anforderungen erfüllen:
    -   Er muss mindestens einen Dual-Core-Prozessor haben, der an kein weniger als 2 Gigahertz (GHz) ausgeführt wird.
    -   Er muss mindestens 3 Gigabytes (GB) von RAM haben.
    -   Er muss Internetzugriff haben.

## <a name="retail-hardware-station-requirements"></a>Kleinhardwarestationsanforderungen
### <a name="supported-operating-systems"></a>Unterstützte Betriebssysteme

-   Kleinhardwarestation ist eine 32-Bit-Anwendung, diese werden jedoch auf x86- und x64-Architekturen ausgeführt.
-   Kleinhardwarestation wird auf folgende Betriebssysteme unterstützt:
    -   Windows 7, Enterprise Professional und die wichtigsten Editionen ** Hinweis: ** Windows 7 wird unterstützt, wenn Internet Explorer 11 manuell im System eingerichtet ist.
    -   Windows 8,1, Enterprise Professional Update 1 und Embedded Editionen
    -   Editionen Windows 10s Pro, Enterprises und Enterprises LTSB

### <a name="minimum-system-requirements"></a>Systemanforderungen

Der Computer muss alle Systemanforderungen für das Einrichten und Verwenden der folgenden Artikel entsprechen:

-   Internetinformationsdienste (IIS)
-   Hardware von Drittanbietern

## <a name="retail-store-scale-unit-requirements"></a>Ladengeschäfts-Maßeinheitsanforderungen
### <a name="supported-operating-systems"></a>Unterstützte Betriebssysteme

-   Ladengeschäfts-Maßeinheit ist eine 32-Bit-Anwendung, diese werden jedoch auf x86- und x64-Architekturen ausgeführt.
-   Ladengeschäfts-Maßeinheit wird auf folgende Betriebssysteme unterstützt:
    -   Windows 7, Enterprise Professional und Editionen entscheidende
    -   Windows 8,1, Enterprise Professional Update 1 und Embedded Editionen
    -   Editionen Windows 10s Pro, Enterprises und Enterprises LTSB

### <a name="minimum-system-requirements"></a>Systemanforderungen

-   4 GB RAM von
-   1.6 GHz-Spitze pro CPU-Geschwindigkeit Kernsatz (zwei Kerne sind die Mindestsystemanforderungen.)
-   Mindestens 10 GB von freiem Speicherplatz (die Kanaldatenbank kann einen großen Platz benötigt.)

### <a name="recommended-system-requirements"></a>Empfohlene Systemanforderungen

-   6 GB RAM von
-   2.4 Anfang GHzs (nicht i7 oder) pro CPU-Geschwindigkeit Kernsatz (vier Kerne empfohlen werden.)
-   Mindestens 10 GB von freiem Speicherplatz (die Kanaldatenbank kann einen großen Platz benötigt.)

## <a name="requirements-for-development-on-local-vms"></a>Anforderungen für Entwicklung in lokaler Variable WM
Weitere Informationen zu den Anforderungen für Entwicklung auf lokalen virtuellen Computern (VMs), finden Sie VM-Ausführen lokal [] (/dynamics365/operations/dev-itpro/dev-tools/access-instances #vm-that-is-running-in-premises).

<a name="see-also"></a>Siehe auch
--------

[Erhalten einer Bewertungskopie von Microsoft Dynamics 365 für Arbeitsgänge ab]( /dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


