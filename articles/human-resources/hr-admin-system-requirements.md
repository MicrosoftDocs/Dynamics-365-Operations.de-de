---
title: Systemanforderungen
description: In diesem Thema werden die Systemanforderungen für Microsoft Dynamics 365 Human Resources aufgeführt.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e88006ebf174f1a416fa6d8572d439a0395f0e44
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690861"
---
# <a name="system-requirements"></a>Systemanforderungen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema werden die Systemanforderungen für Microsoft Dynamics 365 Human Resources aufgeführt. Es werden auch die Länder und Regionen beschrieben, in denen Human Resources verfügbar ist, außerdem werden Informationen zu Sprachen und zur Lokalisierung für Human Resourcessdaten bereitgestellt.

## <a name="supported-web-browsers"></a>Unterstützte Webbrowser

Benutzer können auf Microsoft Dynamics 365 Human Resources mit jedem der folgenden Webbrowser zugreifen, die auf den angegebenen Betriebssystemen ausgeführt werden: 

*   Microsoft Edge (letzte öffentlich verfügbare Version) unter Windows 10
*   Internet Explorer 11 unter Windows 10, Windows 8.1 oder Windows 7
*   Google Chrome (letzte öffentlich verfügbare Version)
*   Apple Safari (letzte öffentlich verfügbare Version)

Um die neueste Version für jeden Webbrowser zu suchen, wechseln Sie zur Website des Softwareherstellers. 

## <a name="special-considerations"></a>Besondere Überlegungen

* Damit Task Recorder Screenshots erfassen und in erzeugte Microsoft Word-Dokumente einfügen kann, müssen Sie eine Vorabversion der Chrome-Erweiterung installieren
* Der Workflow-Editor wird als ClickOnce-Anwendung gestartet. Nur Microsoft Edge und Internet Explorer (auf einer unterstützten Version von Microsoft WindowsClickOnce-Bewerbungen) unterstützen. Die Workflow-Editor-ClickOnce-Anwendung erfordert ein kompatibles 64-Bit-Betriebssystem.
* Um PDF-Dateien in der Vorschau anzeigen, sollten Sie moderne Browser wie Microsoft Edge verwenden (aktuellste verfügbare Version) unter Windows 10 oder Google Chrome (aktuellste verfügbare Version) unter Windows 10, 8,1, Windows 8, Windows 7 oder Google Nexus-10 Tablet.

## <a name="network-requirements"></a>Netzwerkanforderungen

* Human Resources wurde für Netzwerke mit eine Latenzzeit von 250-300 Millisekunden (ms) oder weniger entwickelt. Diese Latenzzeit ist die Latenzzeit von einem Browser-Client zum Microsoft Azure-Rechenzentrum, das Human Resources hostet. Wir empfehlen, die Netzwerklatenz unter [www.azurespeed.com](https://www.azurespeed.com "Azure Latenztest") zu testen.
* Bandbreitenanforderungen für Human Resources hängen vom Szenario ab. Typische Szenarien erfordern eine Bandbreite von mehr als 50 Kilobytes pro Sekunde (KBps).
 
> [!WARNING]
> Berechnen Sie Bandbreitenanforderungen von einem Clientstandort nicht, indem Sie die Anzahl der Benutzer mit den Mindestbandbreitenanforderungen multiplizieren. Die gleichzeitige Nutzung eines bestimmten Standorts ist schwierig zu berechnen. Kunden, die sich Gedanken machen über die Bandbreitenanforderungen, sollten eine Testversion von Human Resources verwenden.

## <a name="supported-microsoft-office-applications"></a>Unterstützte Microsoft Office.Anwendungen

* Zum Ausführen von Microsoft Excel- und Word-Add-Ins muss Microsoft Office 2016 für Windows oder Mac installiert sein. Weitere Informationen zu den Versionsanforderungen finden Sie unter [Fehlerbehebung bei der Office-Integration](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Fehlerbehebung bei der Office Integration").
* Um Dokumente anzuzeigen, die über die Funktionen für einen Export nach Excel oder einen Export nach Word erzeugt wurden, muss Microsoft Office 2007 oder höher installiert sein.

## <a name="regional-availability-languages-and-localization"></a>Regionale Verfügbarkeit, Sprachen und Lokalisierung

Sie können eine PDF-Datei der Länder, Regionen der und der von Human Resources unterstützten Sprachen unter [Internationale Verfügbarkeit von Microsoft Dynamics 365](/dynamics365/get-started/availability) herunterladen. 

> [!NOTE]
> Auch wenn die Benutzeroberfläche in andere Sprachen lokalisiert ist, werden alle Benutzerdaten in der Sprache gespeichert, in der sie eingegeben wurden. Sie können E-Mails und Vorlagen in anderen Sprachen erstellen, aber Daten wie Planungsinformationen sind derzeit nur auf Englisch verfügbar.

Wenn Sie Entwickler sind, der an dem Erstellen länder- oder regionsspezifischer Anpassungen interessiert ist, oder an der Erstellung einer Lösung für ein Land oder eine Region, die derzeit nicht von Microsoft unterstützt wird, finden weitere Informationen unter [Globalisierung](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
