---
title: Anforderungen an das Talent-System
description: In diesem Thema sind die Anforderungen für Dynamics 365 Talent aufgeführt.
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 509827d5736887f56e7754a0760af7dea76277f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461265"
---
# <a name="talent-system-requirements"></a>Anforderungen an das Talent-System

[!include [banner](includes/banner.md)]

In diesem Thema werden die Anforderungen für Microsoft Dynamics 365 Talent, einschließlich Attract und Onboard, beschrieben. Es werden auch die Länder und Regionen beschrieben, in denen Talent verfügbar ist, außerdem werden Informationen zu Sprachen und zur Lokalisierung für Talentdaten bereitgestellt. Zusätzlich bietet dieses Thema die Aktualisierungsrichtlinie für Talent bereit.

## <a name="supported-web-browsers"></a>Unterstützte Webbrowser

Microsoft Dynamics 365 Talent kann in den folgenden Webbrowsern ausgeführt werden, die auf den angegebenen Betriebssysteme ausgeführt werden: 

*   Microsoft Edge (letzte öffentlich verfügbare Version) unter Windows 10
*   Internet Explorer 11 unter Windows 10, Windows 8.1 oder Windows 7
*   Google Chrome (letzte öffentlich verfügbare Version)
*   Apple Safari (letzte öffentlich verfügbare Version)

Um die neueste Version für jeden Webbrowser zu suchen, wechseln Sie zur Website des Softwareherstellers. 

> [!NOTE]
> * Wenn Sie Bilder aufzuzeichnen, die über die Aufgabenaufzeichnung generiert wurden, und diese in Microsoft Word-Dokumente aufnehmen, müssen Sie eine Chrome-Erweiterung installiert haben. 
> * Der Workflow-Editor wird als ClickOnce-Anwendung gestartet. Nur Microsoft Edge und Internet Explorer (auf einer unterstützten Version von Microsoft WindowsClickOnce-Bewerbungen) unterstützen. Die Workflow-Editor-ClickOnce-Anwendung erfordert ein kompatibles 64-Bit-Betriebssystem.
> * Um PDF-Dateien in der Vorschau anzeigen, sollten Sie moderne Browser wie Microsoft Edge verwenden (aktuellste verfügbare Version) unter Windows 10 oder Google Chrome (aktuellste verfügbare Version) unter Windows 10, 8,1, Windows 8, Windows 7 oder Google Nexus-10 Tablet.
>   Netzwerkanforderungen
> * Dynamics 365 Talent wurde für Netzwerke mit eine Latenzzeit von 250-300 Millisekunden (ms) oder weniger entwickelt. Diese Latenzzeit ist die Latenzzeit von einem Browser-Client zum Microsoft Azure-Rechenzentrum, das Talent hostet. Wir empfehlen, die Netzwerklatenz unter [www.azurespeed.com](https://www.azurespeed.com "Azure Latenztest") zu testen.
> * Bandbreitenanforderungen für Talent hängen vom Szenario ab. In den meisten Fällen wird eine Bandbreite von mehr als 50 Kilobytes pro Sekunde (kbps) benötigt.
> 
> [!WARNING]
> Berechnen Sie Bandbreitenanforderungen von einem Clientstandort nicht, indem Sie die Anzahl der Benutzer mit den Mindestbandbreitenanforderungen multiplizieren. Die gleichzeitige Nutzung eines bestimmten Standorts ist schwierig zu berechnen. Kunden, die sich Gedanken machen über die Bandbreitenanforderungen, sollten eine Testversion von Talent verwenden.

## <a name="supported-microsoft-office-applications"></a>Unterstützte Microsoft Office.Anwendungen

* Zum Ausführen von Microsoft Excel- und Word-Add-Ins muss Microsoft Office 2016 für Windows oder Mac installiert sein. Weitere Informationen zu den Versionsanforderungen finden Sie unter [Fehlerbehebung bei der Office-Integration](../dev-itpro/office-integration/office-integration-troubleshooting.md "Fehlerbehebung bei der Office Integration").
* Um Dokumente anzuzeigen, die über die Funktionen für einen Export nach Excel oder einen Export nach Word erzeugt wurden, muss Microsoft Office 2007 oder höher installiert sein.

## <a name="regional-availability-languages-and-localization"></a>Regionale Verfügbarkeit, Sprachen und Lokalisierung

Sie können eine PDF-Datei der Länder, Regionen der und der von Talent unterstützten Sprachen unter [Internationale Verfügbarkeit von Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability) herunterladen. 

> [!NOTE]
> Auch wenn die Benutzeroberfläche in andere Sprachen lokalisiert ist, werden alle Benutzerdaten in der Sprache gespeichert, in der sie eingegeben wurden. Sie können E-Mails und Vorlagen in anderen Sprachen erstellen, aber Daten wie Planungsinformationen sind derzeit nur auf Englisch verfügbar.

Wenn Sie Entwickler sind, der an dem Erstellen länder- oder regionsspezifischer Anpassungen interessiert ist, oder an der Erstellung einer Lösung für ein Land oder eine Region, die derzeit nicht von Microsoft unterstützt wird, finden weitere Informationen unter [Globalisierung](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).



[!INCLUDE[footer-include](../includes/footer-banner.md)]