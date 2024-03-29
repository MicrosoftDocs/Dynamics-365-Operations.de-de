---
title: In früheren Versionen entfernte oder veraltete Funktionen
description: Dieser Artikel beschreibt Funktionen, die aus Dynamics 365 for Finance and Operations und früheren Versionen entfernt wurden oder für die Entfernung geplant waren.
author: sericks007
ms.date: 02/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea9355b040c6431f5ddcccc4aaa0de73e21ad299
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124557"
---
# <a name="removed-or-deprecated-features-in-previous-releases"></a>In früheren Versionen entfernte oder veraltete Funktionen

[!include [banner](../includes/banner.md)]



> [!IMPORTANT]
> Dieser Artikel wird nicht mehr aktualisiert. Um eine aktuelle Liste der Funktionen anzuzeigen, die aus Apps für Finanzen und Betrieb entfernt oder außer Betrieb genommen wurden, suchen Sie nach **„Entfernte oder außer Betrieb genommene Funktionen“**, die sich auf die App beziehen, die Sie verwenden.

Dieser Artikel beschreibt Funktionen, die aus Dynamics 365 for Finance and Operations und früheren Versionen dieses Produkts entfernt wurden oder veraltet sind.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen. 

Ausführliche Informationen über Objekte in Apps für Finanzen und Betrieb finden Sie in den [Technischen Referenzberichten](/dynamics/s-e/global/axtechrefrep_61). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die in den einzelnen Versionen der Apps für Finanzen und Betrieb geändert oder entfernt wurden.

## <a name="finance-1007-with-platform-update-31"></a>Finance 10.0.7 mit Plattformupdate 31

### <a name="chinese-voucher-types-without-account-groups-selection"></a>Chinesische Belegtypen ohne Kontogruppenauswahl
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Geändert in die Funktion mit Kontogruppenauswahl. |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Bewerbung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Wir planen, die chinesischen Belegtypen-Einstellungen ohne Kontogruppenauswahl bis zum 1. Dezember 2020 nicht mehr zu unterstützen. Zusätzliche Details für das neue Funktionsdesign finden Sie in „Neuerungen in 10.0.7“. |

## <a name="finance-and-operations-1006-with-platform-update-30"></a>Finance and Operations 10.0.6 mit Plattformupdate 30


### <a name="dimensionhashgethashstr-_message"></a>DimensionHash.getHash(str _message)

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Verwendung von SHA1 ist in Windows veraltet, wie in [Windows-Durchsetzung von SHA1-Bescheinigungen](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx) dokumentiert.  |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Bewerbung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Bis zum 1. April 2020 müssen Entwickler, die in der Klasse **Hat Funktion** enthaltenen Plattform-APIs verwenden. |

### <a name="hashcomputesha1hashstring-message"></a>Hash.ComputeSHA1Hash(string message)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Verwendung von SHA1 ist in Windows veraltet, wie in [Windows-Durchsetzung von SHA1-Bescheinigungen](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx) dokumentiert.  |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Plattform |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Bis zum 1. April 2020 müssen Entwickler, die in der Klasse **Hat Funktion** enthaltenen Plattform-APIs verwenden. |


### <a name="formdatetimecontrolsetutcstring"></a>FormDateTimeControl.setUtcString()

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Wir deaktivieren die Methode **setUtcString()**, da eine bessere Ersatzmethode verfügbar ist. |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Plattform |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Wir planen, die Methode **setUtcString()** bis zum 1. Oktober 2020 nicht mehr zu unterstützen. Entwickler können stattdessen die Methode **setUtcDateTime()** verwenden. |

### <a name="blocklist-report-it--feature-reference-it-00001"></a>Sperrlistenbericht (IT) – Funktionsreferenz IT-00001

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Nicht rechtlich obligatorisch. |
| **Ersetzt durch eine andere Funktion?**   | Nein |
| **Betroffene Produktbereiche**         | Italienische Lokalisierung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Wir planen, diesen Bericht bis zum 1. Oktober 2020 nicht mehr zu unterstützen. |

### <a name="domestic-tax-report--feature-reference-it-00003"></a>InInlandssteuererklärung – Funktionsreferenz IT-00003

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Nicht rechtlich obligatorisch. |
| **Ersetzt durch eine andere Funktion?**   | Nein |
| **Betroffene Produktbereiche**         | Italienische Lokalisierung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Bis 1. Oktober 2020 planen wir, **Inlandssteuererklärung – Funktionsreferenz IT-00003** nicht mehr zu unterstützen. |

## <a name="october-2019-deprecation-announcement"></a>Ankündigung der Außerbetriebnahme im Oktober 2019

### <a name="flowchart-diagrams-in-business-process-modeler"></a>Flussdiagramme im Geschäftsprozessmodellierer

<table>
<tbody>
<tr>
<td><strong>Grund für veralteten Zustand/Entfernung</strong></td>
<td>Die Flowchart-Diagrammkomponente im Geschäftsprozessmodellierer (BPM) wird nicht mehr empfohlen, da das Legacy-Design zu einer geringen Nutzung geführt hat.</td>
</tr>
<tr>
<td><strong>Ersetzt durch eine andere Funktion?</strong></td>
<td>Nein</td>
</tr>
<tr>
<td><strong>Betroffene Bereiche</strong></td>
<td>Geschäftsprozessmodellierer</td>
</tr>
<tr>
<td><strong>Status</strong></td>
<td>Veraltet: Die Flussdiagrammkomponente in BPM wird voraussichtlich im Jahr 2020 entfernt. Folgende Funktion wird nicht mehr verfügbar sein:
<ul>
<li>Alle Flussdiagramme sind schreibgeschützt und können nicht bearbeitet werden. Die Formeigenschaften, die Flussdiagrammaktivitäten zugeordnet sind, sind ebenfalls nicht verfügbar. Diese Flussdiagramme umfassen sowohl automatisch generierte Standardflussdiagramme als auch benutzerdefinierte Flussdiagramme, die auf der Grundlage dieser Standardflussdiagramme geändert werden.</li>
<li>Die Prozessschritte sind schreibgeschützt und können nicht bearbeitet werden.</li>     
<li>Die Funktion zur Analyse älterer Anpassungen/Lücken ist nicht verfügbar. Daher wird keine Lückenliste automatisch erstellt oder steht für den Export zur Verfügung.
<p><strong>Hinweis:</strong> Diese Funktion war zuvor veraltet und wurde durch Microsoft Azure DevOps-Integrationen ersetzt.</p>
</li>
<li>Der Versionsverlauf des Flussdiagramms ist nicht verfügbar.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="finance-and-operations-1005-with-platform-update-29"></a>Finance and Operations 10.0.5 mit Plattformupdate 29

### <a name="us-payroll-tax-updates"></a>Aktualisierungen der US-Lohnsteuer

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Steueraktualisierungen für die US-Gehaltsabrechnung werden aufgrund der niedrigen Verwendung und aufgrund von erweiterten Funktionen, die nun über strategische Integrationen angeboten werden, eingestellt.  |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Payroll |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Ab 31. Juli 2024 werden Steueraktualisierungen für Kunden der US-Gehaltsabrechnung nicht mehr angeboten. Die Funktionalität bleibt zwar im Produkt bestehen, wird aber nicht mehr durch Erweiterungen auf dem neuesten Stand gehalten. Eventuelle Produktfehler von Fall zu Fall bewertet. |

>[!NOTE]
> Dies stellt eine Änderung gegenüber dem ursprünglichen Abbruchdatum vom 1. Oktober 2021 dar. Weitere Informationen finden Sie unter [Steueraktualisierungen, die für die US-Gehaltsabrechnung nicht mehr angeboten werden Microsoft Dynamics 365 for Finance and Operations](https://aka.ms/financepayrollfaq).


### <a name="data-management-staging-clean-up"></a>Datenverwaltung – Stagingbereinigung
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Erfüllt nicht die zentralen Voraussetzungen, die für die Planung einer regelmäßigen Bereinigung erforderlich sind. |
| **Ersetzt durch eine andere Funktion?**   | Ja, es wird die Bereinigungsfunktion für den Auftragsverlauf hinzugefügt, um die Anforderungen verschiedener Szenarien ganzheitlich zu erfüllen. |
| **Betroffene Produktbereiche**         | Datenverwaltung |
| **Bereitstellungsoption**              | Alle  |
| **Status**                         | Veraltet: Der anvisierte Zeitrahmen für die Entfernung der Funktionalität ist Dezember 2020. |

## <a name="finance-and-operations-1004-with-platform-update-28"></a>Finance and Operations 10.0.4 mit Plattformupdate 28

### <a name="france-fec-accounting-data-export-in-xml"></a>Frankreich: FEC-Buchhaltungsdatenexport in XML

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch TXT-Format, ist die **Französische FEC-Protokolldatei** über **Hauptbuch** \> **Periodische Aufgaben** \> **Datenexport** verfügbar.
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Hauptbuch |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet. Zielzeitrahmen für die Entfernung der Funktionalität ist Juli 2020. |


### <a name="legacy-navigation-bar"></a>Vorgängernavigationsleiste

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Kopfzeilenausrichtung an anderen Dynamics- und Office-Produkten. Weitere Informationen finden Sie unter [Aktualisierte Navigationsleiste, die an der Office-Kopfzeile ausgerichtet ist](/business-applications-release-notes/April19/dynamics365-finance-operations/updatednavbar).
| **Ersetzt durch eine andere Funktion?**   | Ab Plattformupdate 24 wurde eine neu formatierte Navigationsleiste eingeführt, die eine Suchfunktion enthält. |
| **Betroffene Produktbereiche**         | Webclient |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Ab April 2020 ist die Vorgängernavigationsleiste nicht mehr verfügbar. Bis dahin können Kunden die Vorgängernavigationsleiste über die Seite **Client-Leistungsoptionen** wiederherstellen. |


## <a name="finance-and-operations-1002-with-platform-update-26"></a>Finance and Operations 10.0.2 mit Plattformupdate 26


### <a name="legacy-default-action-behavior"></a>Vorgänger-Standardaktivitätsverhalten

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Vorgängerverhalten für Standardaktivitäten in Rastern führt dazu, dass eine unerwartete Spalte den Standardaktivitätslink hat, nachdem Rasterspalten über die Personalisierung neu geordnet wurden. Die neue Kurzstandardaktivitätsfunktion korrigiert das. Weitere Informationen finden Sie unter [Kurzstandardaktivitäten in Rastern](/business-applications-release-notes/October18/dynamics365-finance-operations/sticky-default-action). |
| **Ersetzt durch eine andere Funktion?**   | Ab Plattformupdate 21 wurde eine Funktion für „Kurzstandardaktivitäten” eingeführt. Diese Funktion kann auf der Seite **Leistungsoptionen des Clients** aktiviert werden. |
| **Betroffene Produktbereiche**         | Raster im Webclient |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Ab April 2020 werden Kurzstandardaktivitäten zum Standardverhalten ohne einen Mechanismus, um zum Vorgängerverhalten zurückzukehren. |

### <a name="legacy-is-one-of-filtering-experience"></a>Vogänger-Filterfunktion „gehört zu“

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Filterfunktion „gehört zu” wurde im Plattformupdate 22 neu konzipiert. Geplant ist, dass dies letztendlich die einzige „gehört zu”-Filterfunktion sein soll. |
| **Ersetzt durch eine andere Funktion?**   | Ab Plattformupdate 22 ist eine verbesserte „gehört zu”-Filterfunktion auf der Seite **Leistungsoptionen des Clients** verfügbar. Weitere Informationen finden Sie unter [Optimierte „gehört zu”-Filterfunktion](/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering). |
| **Betroffene Produktbereiche**         | Webclient |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Ab April 2020 wird die verbesserte „gehört zu”-Funktionalität zum Standardverhalten ohne einen Mechanismus, um zum Vorgängerverhalten zurückzukehren. |

### <a name="parameter-to-enable-sales-orders-with-multiple-project-contract-funding-sources"></a>Parameter, um Aufträge mit mehreren Projektvertrags-Finanzierungsquellen zu aktivieren
Unterstützung für das Erstellen von projektbasierten Aufträgen, bei denen der Projektvertrag mehrere Finanzierungsquellen hat und bei der Einstellung **Projektverwaltungsparameter** die Option **Aufträge für Projekt mit mehreren Finanzierungsquellen zulassen** aktiviert ist. Standardmäßig ist dieser Parameter nicht aktiviert. 

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Diese Funktionalität wird immer aktiviert sein, nachdem der Parameter entfernt wurde. |
| **Ersetzt durch eine andere Funktion?**   | Nein Die Funktionalität, um projektbasierte Aufträge mit mehreren Finanzierungsquellen zu unterstützen, wird immer aktiviert sein.   |
| **Betroffene Produktbereiche**         |Der Parameter **Aufträge für Projekte mit mehreren Finanzierungsquellen zulassen** wird entfernt. Die folgenden Methoden werden geändert, wenn der Parameter entfernt wird: Methode **ctrlSalesOrderTable** in Klasse **ProjStatusType**, Methode **validate** für Feld **ProjId** und Methode **run** im Formular **SalescreateOrder**. Folgende Methoden sind veraltet, wenn der Parameter entfernt wird: **IsSalesOrderAllowedForMultipleFundingSources** in der Tabellendatei **ProjTable**, Methode **IsAllowSalesOrdersForMultipleFundingSourcesParamEnabled** in der Tabellendatei **ProjTable**, Datenfeld **AllowSalesOrdersForMultipleFundingSources** im Formular **ProjParameters** und Dateien **ProjParameterEntity**, private Methode **IsAssociatedToMultipleFundingSourcesContract** in Tabellendatei **ProjTable**. |
| **Bereitstellungsoption**              | Alle  |
| **Status**                         | Veraltung ist für die Versionswelle von April 2020 geplant. |

### <a name="legacy-workflow-reports-for-tracking-and-instance-status"></a>Vorgängerworkflowberichte für die Nachverfolgung und den Instanzstatus

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Vorgängerworkflowberichte für die Nachverfolgung und den Instanzstatus werden als veraltet gekennzeichnet, da auf sie nicht mehr von der Navigation aus verwiesen wird. Die Berichtsnamen sind WorkflowWorkflowInstanceByStatusReport und WorkflowWorkflowTrackingReport. |
| **Ersetzt durch eine andere Funktion?**   | Das Workflowhistorienformular kann stattdessen verwendet werden. |
| **Betroffene Produktbereiche**         | Webclient |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Zielzeitrahmen für die Entfernung der Funktionalität ist April 2020. |

## <a name="finance-and-operations-1001-with-platform-update-25"></a>Finance and Operations 10.0.1 mit Plattformupdate 25

### <a name="deprecated-apis-and-potential-breaking-changes"></a>Veraltete APIs und mögliche wichtige Änderungen


#### <a name="deriving-from-internal-classes-is-deprecated"></a>Das Ableiten von internen Klassen ist veraltet

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Vor Plattformupdate 25 war es möglich, eine Klasse oder Tabelle zu erstellen, die von einer internen Klasse/Tabelle abgeleitet wurde, die in einem anderen Modul/Paket definiert wurde. Dies ist keine sicher Programmierpraxis. Ab Plattformupdate 25 zeigt der Compiler eine Warnung an. |
| **Ersetzt durch eine andere Funktion?**   | Die Compilerwarnung wird durch einen Fehler im Plattformupdate 26 ersetzt. Diese Änderung ist zur Laufzeit abwärtskompatibel. Das bedeutet, dass Plattformupdate 25 oder neuer in einer beliebigen Sandbox oder Produktionsumgebung bereitgestellt werden kann, ohne benutzerdefinierten Code zu ändern. Diese Änderung betrifft nur Entwicklungs- und Kompilierzeit.|
| **Betroffene Produktbereiche**         | Visual Studio-Entwicklungstools |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Die Warnung wird zu einem Kompilierungsfehler im Plattformupdate 26. |

#### <a name="overriding-internal-methods-is-deprecated"></a>Außerkraftsetzen von internen Methoden ist veraltet

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Vor Plattformupdate 25 war es möglich, eine interne Methode in einer abgeleiteten Klasse außer Kraft zu setzen, die in einem anderen Modul/Paket definiert wurde. Dies ist keine sicher Programmierpraxis. Ab Plattformupdate 25 zeigt der Compiler eine Warnung an. |
| **Ersetzt durch eine andere Funktion?**   | Diese Warnung wird durch einen Kompilierungsfehler im Plattformupdate 26 ersetzt. Diese Änderung ist zur Laufzeit abwärtskompatibel. Das bedeutet, dass Plattformupdate 25 oder neuer in einer beliebigen Sandbox oder Produktionsumgebung bereitgestellt werden kann, ohne benutzerdefinierten Code zu ändern. Diese Änderung betrifft nur Entwicklungs- und Kompilierzeit. |
| **Betroffene Produktbereiche**         | Visual Studio-Entwicklungstools |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Die Warnung wird zu einem Kompilierungsfehler im Plattformupdate 26. |

## <a name="finance-and-operations-1000-with-platform-update-24"></a>Finance and Operations 10.0.0 mit Plattformupdate 24

### <a name="renaming-released-products"></a>Freigegebene Produkte umbenennen 
| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Wenn Sie die Funktion **Primärschlüssel umbenennen** verwenden, um das ItemId eines freigegebenen Produkts zu ändern, werden nur direkte Fremdschlüsselreferenzen aktualisiert. Alle anderen Referenzen zum freigegebenen Produkt, wie von Produktionsaufträgen, behalten die alte ItemId bei. Daher kann es inkonsistente Daten geben, die die Geschäftsprozesse letztlich blockieren. |
| **Ersetzt durch eine andere Funktion?**   | Nein |
| **Betroffene Produktbereiche**         | Produktinformationsverwaltung |
| **Bereitstellungsoption**              | Alle  |
| **Status**                         | Entfernt ab Finance and Operations 10.0.0 mit Plattformupdate 24.|


## <a name="finance-and-operations-813-with-platform-update-23"></a>Finance and Operations 8.1.3 mit Plattformupdate 23

### <a name="sql-server-reporting-services-reportviewer-control"></a>SQL Server Reporting Services-ReportViewer-Steuerelement
Debitoren können die Aktivität **Exportieren** verwenden, die vom eingebetteten SQL Server Reporting Services (SSRS)-ReportViewer-Steuerelement bereitgestellt wird, um Dokumente herunterzuladen, die von Finance and Operations-Anwendungen erstellt werden. Diese HTML-basierte Präsentation des Berichts bietet Benutzern eine nicht paganierte Vorschau des Dokuments.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die nicht-paganierte Art der HTML-basierten Vorschauerfahrung ist den letztlich von Finance and Operations erstellten physischen Dokumenten **nicht** treu. Indem PDF vollständig als das Standardformat für Geschäftsdokumente übernommen werden, können Benutzer eine moderne Anzeigefunktionalität mit verbesserter Leistung nutzen, wenn sie Bewerbungsberichte erstellen. |
| **Ersetzt durch eine andere Funktion?**   | Ab jetzt gelten PDF-Dokumente als das Standardformat für Berichte von Finance and Operations.   |
| **Betroffene Produktbereiche**         | Diese Änderung wirkt sich **nicht** auf die Debitorenszenarien aus, in denen Berichte elektronisch verteilt oder direkt an den Druckern gesendet werden.    |
| **Bereitstellungsoption**              | Alle  |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. Die Funktion zur automatischen Vorschau von Bewerbungsberichten mithilfe einer eingebetteten PDF-Anzeige ist für das Plattformupdate im Mai 2019 geplant. |

### <a name="client-kpi-controls"></a>Steuerelemente der Client-KPI
Integrierte Key Performance Indicators (KPIs) können in Visual Studio von einem Entwickler modelliert und vom Endbenutzer weiter angepasst werden.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die nativen Steuerelemente des Clients, die,verwendet werden, um KPIs zu definieren, haben geringe Debitorenaufnahme und sind auf einen Entwickler angewiesen, um nachverfolgbare Metriken hinzuzufügen. |
| **Ersetzt durch eine andere Funktion?**   | PowerBI.com- Service erbringt Weltklasse-Werkzeugbestückung zum Definieren und Verwalten von KPIs, basierend auf Daten aus externen Quellen.  In einer bevorstehenden Version planen wir, Ihnen die Einbettung von Lösungen zu ermöglichen, die auf PowerBI.com in Anwendungsarbeitsbereichen gehostet werden.   |
| **Betroffene Produktbereiche**         | Diese Aktualisierung verhindert, dass Entwickler neue KPI-Seuerelemente in Visual Studio Designer einführen.    |
| **Bereitstellungsoption**              | Alle  |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="deprecated-apis-and-future-breaking-changes"></a>Veraltete APIs und künfige wichtige Änderungen

#### <a name="field-groups-containing-invalid-field-references"></a>Feldgruppen mit ungültigen Feldreferenzen

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Es ist möglich, dass Tabellenmetadatendefinitionen über Feldgruppen verfügen, die ungültige Feldreferenzen enthalten. Bei einer BEreitstellung kann dies dieses zu Laufzeitfehlern bei der Finanzberichterstellung und bei SQL Server Reporting Services (SSRS) führen. Dieses Problem wird derzeit als eine *Compilerwarnung* statt als *Fehler* kategorisiert, d. h., die zur Bereitstellung geeignete Paketerstellung und die Bereitstellung können erfolge, ohne dass, das Problem beheben werden muss. So beheben Sie dieses Problem:<br><br>1. Entfernen Sie die ungültige Feldreferenz aus der Tabellenfeldgruppendefinition.<br><br>2. Neu kompilieren.<br><br>3. Stellen Sie sicher, dass alle Warnungen oder Fehler behoben werden. |
| **Ersetzt durch eine andere Funktion?**   | Diese Warnung wird in Zukunft durch einen Kompelierfehler ersetzt. |
| **Betroffene Produktbereiche**         | Visual Studio-Entwicklungstools |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Außer Betrieb genommen: Bei der Warnung handelt es sich um einen Kompilierungsfehler bei Plattform-Updates für Version 10.0.11 von Apps für Finanzen und Betrieb. |

#### <a name="complete-list"></a>Vollständige Liste
Die vollständige Liste der veralteten APIs finden Sie unter [Veraltete Methoden und Metadatenelemente](deprecation-deletion-apis.md).

## <a name="finance-and-operations-81-with-platform-update-20"></a>Finance and Operations 8.1 mit Plattformupdate 20

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a>Chargenübertragungsregeln für Kontoeinträge in untergeordnetem Sachkonto
Der synchrone Übergangsmodus wird im Hauptbuchparameter nicht mehr weitergeführt.  Dieser Modus wird nur durch asynchrone und geplanten Charge ersetzt, die bereits als Option für die Umlagerung vorhanden sind. Weitere Informationen finden Sie im Blog [Hauptbuchparameter – Stapelübertragungsregeln](https://community.dynamics.com/365/financeandoperations/b/financials/archive/2019/03/15/general-ledger-parameters-batch-transfer-rules).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Wir entfernen die synchrone Option, wegen den Auswirkungen auf die Leistung des Systems. |
| **Ersetzt durch eine andere Funktion?**   | Asynchrone und geplanten Charge sind Optionen, die anstatt Synchron verwendet werden können.   |
| **Betroffene Produktbereiche**         | Hauptbuch, Kreditoren, Debitoren, Beschaffung, Ausgaben    |
| **Bereitstellungsoption**              | Alle  |
| **Status**                         | Veraltet: Zielzeitrahmen für die Entfernung der Funktionalität ist Version 10.0.|

### <a name="electronic-reporting-for-russia"></a>Elektronisches Berichtsformat für Russland
Funktion für das Konfigurieren von .txt und .xml-Datei-Formaten für Meldungen. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt mit elektronischem Bericht. |
| **Ersetzt durch eine andere Funktion?**   | Ja. |
| **Betroffene Produktbereiche**         | Hauptbuch |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Entfernt ab Finance and Operations 8.1 mit Plattformupdate 20. |

### <a name="financial-reports-generator-for-russia"></a>Finanzberichtsgenerator für Russland
Ein Tool, für die Einrichtung der Datenerfassung für Buchhaltungs- und Steuerberichte und um Daten in XLS- und DOC-Berichtsvorlagen zu exportieren. Funktionale Teile: Exportieren von Daten in XLS- und DOC-Berichtsvorlagen, Abfragen, feste Erfordernisse, werden entfernt. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Entfernte Teile werden mit der elektronischen Berichterstattung ersetzt. |
| **Ersetzt durch eine andere Funktion?**   | Ja. Finanzberichtseinstellungsbenutzeroberfläche soll zum Einrichten von Datenerfassungsregeln nach Steuerregister Hauptbuchkonten verwendet werden. Datenexpot in verschiedenen Dateitypen, feste Erfordernisse und Abfrage ähnliche Datenerfassungsregeln sollten in der elektronischen Berichterstellung konfiguriert werden. |
| **Betroffene Produktbereiche**         | Hauptbuch. |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Entfernt ab Finance and Operations 8.1 mit Plattformupdate 20. |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a>Integration mit externen Anbietern zum Senden der elektronischen Berichterstellung nach Kommunikationswegen für Russland
Funktion, die Karteien generierte elektronische Meldungen zum Ordner für das weitere Versenden an offizielle Anbieter von elektronischer Berichterstellung exportiert sowie den Status zurück importiert.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt mit konfigurierbaren Funktion für elektronische Nachrichten. |
| **Ersetzt durch eine andere Funktion?**   | Ja.  |
| **Betroffene Produktbereiche**         | Hauptbuch, Steuer |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Entfernt ab Finance and Operations 8.1 mit Plattformupdate 20. |


### <a name="profit-tax-register-wizard"></a>Gewinnsteuerregister-Assistent
Funktion zum Erstellen von Vorlagen für neue Gewinnsteuerregister. Diese Funktion erstellt X++-Objekte für neue Register, die dann als Vorlagen erstellt werden, bei denen die entsprechende Berechnungslogik hinzugefügt wurde.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Funktion ist nicht mit dem Finance and Operations-Erweiterbarkeitsmodell kompatibel. |
| **Ersetzt durch eine andere Funktion?**   | Nein |
| **Betroffene Produktbereiche**         | Steuern |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Entfernt ab Finance and Operations 8.1 mit Plattformupdate 20. |

### <a name="payroll-and-human-resources-for-russia"></a>Gehaltsabrechnung und Personalverwaltung für Russland
Russisches länderspezifisches Modul zur Verwaltung von Personalverwaltungsinformationen, Arbeitszeittabellendetails für Mitarbeiter, Gehaltsabrechnung und Erstellung von Gehaltsabrechnungen. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Personalabrechnung ist nicht im globalen strategischen Fokus des Dynamics 365-Portfolios enthalten. Partner und ISVs sind am besten positioniert, um Gehaltsabrechnungsfunktionen bereitzustellen, die den lokalen Vorschriften und Steueraktualisierungen entsprechen.|
| **Ersetzt durch eine andere Funktion?**   | Nein|
| **Betroffene Produktbereiche**         | Verwaltung für russische Gehaltsabrechnung und Personalverwaltung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Zielzeitrahmen für die Entfernung der Funktionalität ist eine der künftigen Aktualisierungen von Version 10.0. |

## <a name="finance-and-operations-80-with-platform-update-15"></a>Finance and Operations 8.0 mit Plattformupdate 15
Keine Funktionen sind in dieser Version entfernt oder veraltet worden. Plattformupdate 15 ist kumulativ und enthält neue oder geänderte Funktionen aus Plattformupdate 13, Plattformupdate 14 und Plattformupdate 15.

## <a name="finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>Finance and Operations, Enterprise Edition 7.3 mit Plattformupdate 12

### <a name="personalized-product-recommendations"></a>Personalisierte Produktempfehlungen 
Ab 15. Februar 2018 können Einzelhändler nicht mehr personalisierte Produktempfehlungen in einem Verkaufsstelle (POS)- Gerät anzeigen. Weitere Informationen finden Sie unter [Überblick über die Produktempfehlungen](../../../commerce/product-recommendations.md).  

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Wir entfernen die aktuelle Version des Produktempfehlungs-Service, da wir für diese Funktion einen besseren Algorithmus und neuere Einzelhandels-ausgerichtete Funktionen neu entwerfen.  |
| **Ersetzt durch eine andere Funktion?**   | Nein Ab Frühling 2018 planen wir, diese Funktion zurückzubringen, um einen neuen Empfehlungs-Service zu nutzen.   |
| **Betroffene Produktbereiche**         | Personalisierte Produktempfehlungen in POS.                                                    |
| **Bereitstellungsoption**              | Alle                                                                                      |
| **Status**                         |Entfernt ab 15. Februar 2018. Dies betrifft Kunden mit Dynamics 365 for Operations 1611 und höher.  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Erweiterung der Liste der elektronischen Berichterstellungsfunktionen (ER)
Die Möglichkeit, benutzerdefinierte Funktionen zur Verwendung im ER-Ausdrucks-Generator zu verwenden (weitere Informationen finden Sie unter [Erweitern der Liste elektronischer Berichterstellungsfunktionen (ER, Elektronic Reporting)](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)) wird nicht mehr unterstützt. Aufgrund von Änderungen der ER-APIs, wurde die API zum Aufruf integrierter Funktionen vom ER-Ausrucks-Generator intern und kann nicht mehr erweitert werden.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Codeversiegelungsinitiative  |
| **Ersetzt durch eine andere Funktion?**   | Keiner. Sobald eine neue integrierte Funktion benötigt wird, muss eine neue Erweiterungsanforderung an das ER-Frameworkteam gerichtet werden.<br><br>Als vorübergehende Arbeit während die angeforderte Funktion vom ER-Team entwickelt wird, kann die erforderliche Logik als Methode einer benutzerdefinierten Anwendungsklasse programmiert werden. Auf diese Methode kann in einem ER-Ausdruck als Eigenschaft der hinzugefügten ER-Datenquelle des Typs **Anwendung\Klasse** zugegriffen werden, die sich auf diese benutzerdefinierte Anwendungsklasse bezieht.  |
| **Betroffene Produktbereiche**         | Framework für elektronische Berichterstellung                                                      |
| **Bereitstellungsoption**              | Alle                                                                                      |
| **Status**                         | Entfernt ab Finance and Operations, Enterprise Edition 7.3.    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>Bestand nach Artikelgruppe und Bestand nach Fälligkeitsberichten für Lagerungsdimension

Diese beiden Berichte werden nicht mehr in Finance and Operations unterstützt. Stattdessen kann der Bericht **Bestandsfälligkeit** verwendet werden, um die Benutzerfreundlichkeit zu verbessern.

| &nbsp;  | &nbsp; |
|--------------|-----------------------|
| **Grund für Abschreibung**       | Doppelte Funktionen  |
| **Ersetzt durch eine andere Funktion?** | Ja. Die beiden Berichte wurden durch den Bericht **Bestandsfälligkeit** ersetzt.     |
| **Betroffene Produktbereiche**       | Lagerverwaltung, Kostenmanagement        |
| **Bereitstellungsoption**        | Alle|
| **Status**                       | Veraltet: Die Menüoptionen für die beiden Berichte sind in Version 7.3 entfernt worden. Allerdings bleibt der Code für die Berichte im Produkt bestehen. Es ist geplant, den Code in einer zukünftigen Version zu entfernen. |

### <a name="power-bi-content-packs-available-on-appsource"></a>Power BI-Inhaltspakete verfügbar für AppSource
Die Inhaltspakete **Kostenverwaltung**, **Finanzleistung** und **Retail Channel Performance**, die auf der [Microsoft AppSource](https://appsource.microsoft.com)-Site verfügbar sind, sind infolge von Produktupdates in Microsoft Power BI veraltet. Die Systemverwaltungsformulare, die verwendet werden, um diese Inhaltspakete in PowerBI.com bereitzustellen, werden auch in Finance and Operations veraltet.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Produktupdates in Microsoft Power BI. |
| **Ersetzt durch eine andere Funktion?**   | Die Inhaltspakete **Kostenverwaltung**, **Finanzleistung** und **Retail Channel Performance**, die auf der [AppSource](https://appsource.microsoft.com)-Site zur Verfügung stehen, werden durch Analyseanwendungen ersetzt, die Lösungsintegrationen auf der Datenbankebene zulassen. Weitere Informationen zu Analyseanwendungen finden Sie unter [Eingebettetes Power BI in Arbeitsbereichen](../../dev-itpro/analytics/embed-power-bi-workspaces.md).    |
| **Betroffene Produktbereiche**         | Kostenverwaltung, Finanzen und Einzelhandel                                                                                               |
| **Bereitstellungsoption**              | Nur Cloud (Integration mit PowerBI.com wird in lokalen Bereitstellungen nicht unterstützt.)                                                                                                            |
| **Status**                         | Veraltet: Zielzeitrahmen für die Funktionalitätsentfernung ist das zweite Quartal 2018.    |

### <a name="standard-ui-in-data-management-workspace"></a>Standardbenutzeroberfläche im Datenverwaltungsarbeitsbereich

Die Standardbenutzeroberfläche in der Datenverwaltung ist die ältere Benutzeroberfläche. Sie ist die Standardoberlfäche, die Benutzern angezeigt wird, wenn sie den Datenverwaltungsarbeitsbereich besuchen.

| &nbsp;  | &nbsp; |
|------------------|-------------------------|
| **Grund für veralteten Zustand/Entfernung** | Wir investieren in die Bereitstellung einer neuen Benutzerfreundlichkeit bei der neuen Benutzeroberfläche.             |
| **Ersetzt durch eine andere Funktion?**   | Die neue Benutzeroberfläche *Erweiterte Ansichten* ersetzt die alte Benutzeroberfläche.            |
| **Betroffene Produktbereiche**         | Arbeitsbereich für die Datenverwaltung                                                     |
| **Bereitstellungsoption**              | Alle                                                                           |
| **Status**                         | Veraltet: Zielzeitrahmen für die Entfernung der Funktionalität ist das erste Quartal 2018. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Indirekte Steuern, Umsatzsteuer, Dienstleistungssteuer für Indien

Diese Steuern sind in der indischen GST klassifiziert worden.

|  &nbsp;                                           |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Grund für Entfernung oder veralteten Zustand**       | Diese Steuern sind in der indischen GST klassifiziert worden.                          |
| **Ersetzt durch eine andere Funktion?**            | Indische GST                                                              |
| **Betroffene Produktbereiche**                  | MwSt.                                                                     |
| **Bereitstellungsoption**                       | Alle Module                                                   |
| **Status**                                  | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |    

### <a name="file-validation-utility-fvu-for-india"></a>Hilfsprogramm für die Dateiüberprüfung (FVU) für Indien

|              &nbsp;                               |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Grund für Entfernung oder veralteten Zustand**       | Fehlender Einsatz durch die Kunden.                                                  |
| **Ersetzt durch eine andere Funktion?**            | Nein                                                                      |
| **Betroffene Produktbereiche**                  | Indische Quellensteuer                                                  |
| **Bereitstellungsoption**                       | Alle Module                                                                    |
| **Status**                                  | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.   |        

### <a name="tdstcs-certificate-for-india"></a>TDS/TCS-Zertifikat für Indien

Benutzer können dies vom Behördenportal herunterladen.

|             &nbsp;                                |    &nbsp;                                                                     |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Grund für Entfernung oder veralteten Zustand**       | Fehlender Einsatz durch die Kunden.                                                  |
| **Ersetzt durch eine andere Funktion?**            | Nein                                                                      |
| **Betroffene Produktbereiche**                  | Indische Quellensteuer                                                  |
| **Bereitstellungsoption**                       | Alle Module                                                                   |
| **Status**                                  | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>Export-/Import-(EXIM)-Anreizprogramm für Indien


|              &nbsp;                               |        &nbsp;                                                                 |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Grund für Entfernung oder veralteten Zustand**       | Fehlender Einsatz durch die Kunden.                                                  |
| **Ersetzt durch eine andere Funktion?**            | Nein                                                                      |
| **Betroffene Produktbereiche**                  | Importieren und Exportieren                                                       |
| **Bereitstellungsoption**                       | Alle Module                                                                    |
| **Status**                                  | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.  |    


## <a name="dynamics-365-for-retail-72"></a>Dynamics 365 for Retail 7.2

### <a name="personalized-product-recommendations"></a>Personalisierte Produktempfehlungen 
Ab 15. Februar 2018 können Einzelhändler nicht mehr personalisierte Produktempfehlungen in einem Verkaufsstelle (POS)- Gerät anzeigen. Weitere Informationen finden Sie unter [Überblick über die Produktempfehlungen](../../../commerce/product-recommendations.md).  

|  &nbsp; |  &nbsp;|
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Wir entfernen die aktuelle Version des Produktempfehlungs-Service, da wir für diese Funktion einen besseren Algorithmus und neuere Einzelhandels-ausgerichtete Funktionen neu entwerfen.  |
| **Ersetzt durch eine andere Funktion?**   | Nein Ab Frühling 2018 planen wir, diese Funktion zurückzubringen, um einen neuen Empfehlungs-Service zu nutzen.   |
| **Betroffene Produktbereiche**         | Personalisierte Produktempfehlungen in POS.                                                    |
| **Bereitstellungsoption**              | Alle                                                                                      |
| **Status**                         |Entfernt ab 15. Februar 2018. Dies betrifft Kunden mit Dynamics 365 for Retail 7.2 und höher. |


## <a name="finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Finance and Operations, Enterprise Edition Juli 2017 mit Plattformupdate 8

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a>Währungskonvertierung für Buchhaltungs- und Berichtswährungen

Die Währungskonvertierung für Buchhaltungs- und Berichtswährungen wurde mit der Einführung des Euro eingeführt.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Eingeschränkte Nutzung und Hinzufügen der Juristische Person kopieren-Funktion als Ersatz.      |
| **Ersetzt durch eine andere Funktion?**   | Nein, aber die Juristische Person kopieren-Entität und die Konfigurationsfunktionen wurden hinzugefügt, um den Wechsel zu einem Unternehmen mit sich ändernden Kernanforderungen zu erleichtern. |
| **Betroffene Produktbereiche**         | Finanzverwaltung     |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.   |


### <a name="warehouse-mobile-devices-portal"></a>Portal für mobile Geräte für das Lager

Portal für mobile Geräte für das Lager (Warehouse Mobile Devices Portal – WMDP) war eine eigenständige Komponente, die für lokale Selbstbereitstellung vorgesehen war. Diese Komponente wird nicht mehr in Finance and Operations unterstützt. Eine systemeigener App, die die Benutzererfahrung verbessert, hat die Funktionalität von WMDP ersetzt.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Doppelte Funktionen.       |
| **Ersetzt durch eine andere Funktion?**   | Ja. Diese Funktion wurde von Finance and Operations - Warehousing ersetzt. Weitere Informationen zu Einstellungen und Voraussetzungen finden Sie unter [Installieren und Konfigurieren der Warehousing-App – Übersicht](../../../supply-chain/warehousing/install-configure-warehousing-app.md). |
| **Betroffene Produktbereiche**         | Lagerortverwaltung und Transportverwaltung     |
| **Bereitstellungsoption**              | Portal für mobile Geräte für das Lager (Warehouse Mobile Devices Portal – WMDP) war eine eigenständige Komponente, die für lokale Selbstbereitstellung vorgesehen war.               |
| **Status**                         | Veraltet: Zielzeitrahmen für das Entfernen der Funktion ist Q4 2019.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Erweiterte Abgleichsregel für Bankabstimmung für den manuelle Abgleich

Eine Abgleichsregel, die verwendet wurde, um ein Bankdokument beim manuellen Abgleich von Dokumenten der Auszugsposition im Abstimmungsarbeitsblatt auszuwählen und zu markieren

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Begrenzte Verwendung.                                                                         |
| **Ersetzt durch eine andere Funktion?**   | Nein Funktionen zur Spaltenfilterung sollten verwendet werden, um nach Dokumente für die Abstimmung zu suchen. |
| **Betroffene Produktbereiche**         | Bargeld- und Bankverwaltung                                                               |
| **Bereitstellungsoption**              | Alle                                                                                    |
| **Status**                         | Entfernt ab Juli 2017.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>Dynamics 365 for Operations 1611 mit Plattformupdate 3

### <a name="aeb-payment-formats-for-spain"></a>AEB-Zahlungsformate für Spanien

Die „Consejo Superior Bancario”-Zahlungsformate wurden verwendet, um Rimessedateien an die Bank für Debitoren- und Kreditorenzahlungen zu übermitteln. Der Inhalt dieser Formate wurde von der Asociación Española de Banca bestimmt. Er deckt Cuaderno 19, 32, 58, 34 aus.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Zahlungsformate werden nicht mehr verwendet.                                  |
| **Ersetzt durch eine andere Funktion?**   | Ja, ISO20022 Banküberweisung und Lastschriftverfahren für Spanien |
| **Betroffene Produktbereiche**         | Kreditorenkonten, Debitoren                                    |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Zahlung per Banküberweisung für Litauen

Bankzahlungsüberweisungen wurden mithilfe von des Exportformats der Zahlungsüberweisung (LT) für Litauen erstellt und gedruckt. Der litauische Markt verwendet LITAS, das einheitliche Electronic Banking-System seit dem Jahre 2005.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Zahlungsformate werden nicht mehr verwendet.                        |
| **Ersetzt durch eine andere Funktion?**   | Ja, Kredittransferzahlungsformat ISO20022 für Litauen     |
| **Betroffene Produktbereiche**         | Kreditorenkonten                                               |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>Zahlungsformate BBS Direkte Remittering für Norwegen

Zahlungsformate BBS Direkte Remittering enthalten Debitorenzahlungsinkassoexport (Direktbelastung) und Rückholnachrichtenimport.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Zahlungsformate werden nicht mehr verwendet.  |
| **Ersetzt durch eine andere Funktion?**   | Das AvtaleGiro-Debitorenzahlungsformat für Norwegen kann verwendet werden, um Direktbelastungsnachrichten zu generieren. Rückholnachrichtenimport wird in künftigen Versionen implementiert. |
| **Betroffene Produktbereiche**         | Kreditorenkonten, Debitoren   |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>Kontenplan-Tool für Spanien

Dieses Tool wird verwendet, wenn ein Kontenplan in Spanien größere Änderungen erfordert. Benutzer können einen neuen Kontenplan in Microsoft Excel oder Textformat importieren und können auch Finanzaufstellungen importieren.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Begrenzte Verwendung                                                  |
| **Ersetzt durch eine andere Funktion?**   | Nein                                                             |
| **Betroffene Produktbereiche**         | Hauptbuch                                                 |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="dom80-payment-format-for-belgium"></a>Dom80 Zahlungsformat für Belgien

Ältere Zahlungsformat Belgeien für Zahlungsinkasso (Direktbelastung).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Zahlungsformat wird nicht mehr verwendet.                          |
| **Ersetzt durch eine andere Funktion?**   | Ja; ISO 20022, Lastschriftzahlungsformat für Belgien         |
| **Betroffene Produktbereiche**         | Debitoren                                            |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG Zahlungsformate für die Schweiz

DTA-/EZAG-Formate sind im ESR-System integriert, da sie eine Referenznummer führen können. Da die Referenznummern nicht obligatorisch ist, können diese Formate für die Verarbeitung aller beliebiger Kreditorenzahlungen verwendet werden. Diese Formate werden von Unternehmen verwendet, die ein Bankkonto außerhalb von "Postfinance" haben.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Zahlungsformate werden nicht mehr verwendet.                        |
| **Ersetzt durch eine andere Funktion?**   | Ja, ISO20022 Kredittransferzahlungsformat für die Schweiz   |
| **Betroffene Produktbereiche**         | Kreditorenkonten                                               |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB Zahlungsformat für Österreich

EDIFACT-DIRDEB Zahlungsformat für Zahlungsinkasso (Direktbelastung).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Zahlungsformat wird nicht mehr verwendet.                          |
| **Ersetzt durch eine andere Funktion?**   | Ja; ISO 20022, Lastschriftzahlungsformat für Österreich         |
| **Betroffene Produktbereiche**         | Debitoren                                            |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="edivat-for-belgium"></a>EDIVAT für Belgien

EDIVAT ist ein veralteter belgischer Standard für elektronische Meldungen über sicheren Mailverkehr. Dynamics AX 2012 behält die schreibgeschützte Lösung bei, um auf die historische Daten zuzugreifen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Funktionalität wird nicht mehr verwendet.                           |
| **Ersetzt durch eine andere Funktion?**   | Nein                                                             |
| **Betroffene Produktbereiche**         | Hauptbuch                                                 |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>eGiro EDIFACT CREMUL Zahlungsimportformat für Norwegen

eGiro basiert auf den internationalen UN EDIFACT CREMUL (Mehrere Gutschriftsanzeigen) Standard, der zum automatischen Buchen von Debitorenzahlungen verwendet wird. In Dynamics AX wird eGiro als Debitorenzahlungsimportformat implementiert.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Zahlungsformat wird nicht mehr verwendet.                                                     |
| **Ersetzt durch eine andere Funktion?**   | Ja, der Import der ISO20022 Camt.054 Benachrichtigung. |
| **Betroffene Produktbereiche**         | Debitorenkonten                                                                       |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.                            |

### <a name="external-inventory-for-poland"></a>Externer Bestand für Polen

Nachweis von Waren, die von einem Kreditor für Verkäufe ohne Einkauf verwendet werden. Waren, die im externen Bestand verwaltet werden, haben keinen Einfluss auf den Standardbestand und können verkauft und dann automatisch gekauft werden. Dieser Prozess erstellt echte Bestandumlagerungen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch eine andere Funktion                                    |
| **Ersetzt durch eine andere Funktion?**   | Ja, die zentrale eingehende Lieferungsfunktionalität                |
| **Betroffene Produktbereiche**         | Kreditorenkonto, Lagerverwaltung                         |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Finanzberichtsgenerator für Osteuropa

Ein Tool, um die Datenerfassung für die Berechnung und die Steuererklärungen einzurichten und Daten in XLS- und DOC-Berichtsvorlagen zu exportieren

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Begrenzte Verwendung                                                                            |
| **Ersetzt durch eine andere Funktion?**   | Nein Das Tool wird durch die elektronische Berichterstellungskonfigurationen in künftigen Versionen ersetzt. |
| **Betroffene Produktbereiche**         | Hauptbuch                                                                           |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Import von Buchungen für Debitorenzahlungen für Finnland

Sie können ein Importformat für finnische Zahlungen auswählen, das Debitorenzahlungsbuchungen aus einer externen Datei importiert, die von der Bank bereitgestellten wird.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Zahlungsformat wird nicht mehr verwendet.                                                     |
| **Ersetzt durch eine andere Funktion?**   | Ja, der Import der ISO20022 Camt.054 Benachrichtigung. |
| **Betroffene Produktbereiche**         | Debitorenkonten                                                                       |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Import von Zahlungsbuchungen in eine Hauptbucherfassung für Finnland

Ein Sonderformat für Finnland zum Import von Buchhaltungsbuchungen in das Hauptbuch.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Zahlungsformat wird nicht mehr verwendet.                                                     |
| **Ersetzt durch eine andere Funktion?**   | Ja, der Import des ISO20022 Camt.053 Bankauszugs mit der erweiterten Bankabstimmung. |
| **Betroffene Produktbereiche**         | Debitorenkonten                                                                       |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integration mit Isabel synchronisiert (CIS) für Belgien

Isabel ist das Framework für Electronic Banking in Europa und kein tatsächlicher Standard in Belgien.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Integration mit Isabel-Kunden ist eingestellt.   |
| **Ersetzt durch eine andere Funktion?**   | Nein Die Zahlungsformate, die nicht mehr verwendet werden, werden durch Transferzahlungsformat des Kredits ISO20022 für Belgien ersetzt. |
| **Betroffene Produktbereiche**         | Kreditorenkonten     |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Änderungen im Kontenplan und bei den Buchhaltungsvorschriften für Spanien

Diese Funktion wurde für Änderungen im Kontenplan und bei den Buchhaltungsvorschriften in Spanien verwendet. Führt Konten zusammen, um alte Kontenpläne in die neuen Kontenpläne zu transformieren und das vorherige Geschäftsjahr mit dem neuen Geschäftsjahr zu vergleichen, selbst wenn sie an verschiedene Kontonummern gebucht wurden.

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Begrenzte Verwendung                                                  |
| **Ersetzt durch eine andere Funktion?**   | Nein                                                             |
| **Betroffene Produktbereiche**         | Hauptbuch                                                 |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Kreditorenzahlungsformat Pagamento Fornittori

Veraltetes italienisches Zahlungsformat für Kreditübertragungen.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Zahlungsformat wird nicht mehr verwendet.                          |
| **Ersetzt durch eine andere Funktion?**   | Ja, ISO20022 Kredittransferzahlungsformat für Italien         |
| **Betroffene Produktbereiche**         | Kreditorenkonten                                               |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="payment-export-formats-for-estonia"></a>Zahlungsexportforamte für Estland

Die Formate Telehansa und Teleservide werden für den Bankzahlungsexport verwendet.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Zahlungsformate werden nicht mehr verwendet.                        |
| **Ersetzt durch eine andere Funktion?**   | Ja, ISO20022 Kredittransferzahlungsformat für Estland       |
| **Betroffene Produktbereiche**         | Kreditorenkonten                                               |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="payment-file-archive-for-norway"></a>Zahlungsdateiarchiv für Norwegen

Wenn Zahlungsdateien generiert werden archiviert das Dateiarchiv automatisch alle Dateien, die erstellt werden, auch Dateien, die zuvor gelesen oder geschrieben wurden.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch eine andere Funktion                                        |
| **Ersetzt durch eine andere Funktion?**   | Ja, archivierte Einzelvorgänge für elektronische Berichterstellung                            |
| **Betroffene Produktbereiche**         | Kreditorenkonten, Debitoren, Organisationsverwaltung |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.     |

### <a name="payment-import-formats-for-estonia"></a>Zahlungsimportformate für Estland

Die Formate Telehansa und TeleTeenus werden für den Bankzahlungimport verwendet.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Zahlungsformate werden nicht mehr verwendet.                                                    |
| **Ersetzt durch eine andere Funktion?**   | Ja, der Import der ISO20022 Camt.054 Bankbenachrichtigung. |
| **Betroffene Produktbereiche**         | Debitorenkonten                                                                        |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.                             |

### <a name="payroll-information-in-human-resources"></a>Lohndaten in der Personalverwaltung

Personalverwaltung-Lohndaten

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Diese Funktion wurde durch zentrale Lohn- und Personalverwaltungsseiten ersetzt.  |
| **Ersetzt durch eine andere Funktion?**   | **Vergütungen**, **Einnahmen** und zugehörige Seiten, die zuvor in US-Lohn waren, sind umkonfiguriert worden und sind jetzt Teil der zentralen Personalverwaltungskonfiguration, um die externe Lohnverarbeitung besser zu unterstützen.. Diese Funktionen steht über den Konfigurationsschlüssel **Personalverwaltung 1** \> **Lohnabrechnung** bereit. |
| **Betroffene Produktbereiche**         | Personalverwaltung, Lohnabrechnung   |
| **Status**                         | Entfernt ab Dynamics 365 for Operations Version 1611.    |

### <a name="performance-management-goal-workflow"></a>Leistungsverwaltungsziel-Workflow

Leistungsverwaltung enthält Zielverwaltung und Integration mit Leistungsbeurteilungen.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Leistungsverwaltung wurde neu gestaltet und die Anzahl von Zielseiten wurde verringert, um den Prozess zu vereinfachen.                 |
| **Ersetzt durch eine andere Funktion?**   | Nein Ziele sind für Manager über das Manager-Self-Service-Portal sichtbar und können vom Manager angezeigt und geändert werden. |
| **Betroffene Produktbereiche**         | Human Capital Management       |
| **Status**                         | Entfernt ab Dynamics 365 for Operations Version 1611.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Zahlungsformate Postgirot und Postgirot Utland für Schweden

Zahlungsformate Postgirot und Postgirot Utland für Schweden.

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Zahlungsformate werden nicht mehr verwendet.                        |
| **Ersetzt durch eine andere Funktion?**   | Ja, ISO20022 Kredittransferzahlungsformat für Schweden        |
| **Betroffene Produktbereiche**         | Kreditorenkonten                                               |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="radio-frequency-identifier"></a>Kennung für Funkübertragung

RFID (Radiofrequenz-Identifikation) ist eine Technologie zum Sammeln von Daten. Bei dieser Technologie werden Daten mithilfe elektronischer Markierungen zum Speichern von Identifizierungsdaten sowie mittels eines Lesegeräts erfasst, das ohne direkte Sichtverbindung funktioniert.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Geringe Kundennutzung und ein begrenzter Funktionsumfang.   |
| **Ersetzt durch eine andere Funktion?**   | Nein                                              |
| **Betroffene Produktbereiche**         | Lagerverwaltung                            |
| **Status**                         | Entfernt ab Dynamics 365 for Operations 1611. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Bericht zu Bundeslandrechnungsnummerierung für Lettland

Lettische Gesetzgebung schafft bestimmte Regeln dazu, wie Verkaufsrechnungen nummeriert werden sollen. Mit der Funktionalität können Sie bestimmte Nummern Verkaufsrechnungen zuweisen, basierend auf dem Benutzer oder den Benutzergruppen. Sie können einen Bericht oder eine XML-Datei generieren. Sie können auch einen Bericht zu Rechnungsnummern drucken, die verwendet werden.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Bundeslandrechnungsnummerierung muss nicht mehr verwaltet werden. Der Bericht zu verwendeten Rechnungsnummern wird nicht mehr benötigt. |
| **Ersetzt durch eine andere Funktion?**   | Nein       |
| **Betroffene Produktbereiche**         | Debitoren    |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Richten Sie die Namen vom Manager und dem allgemeinen Buchhalter eines Unternehmens für Litauen ein

Die Namen vom Manager und dem allgemeinen Buchhalter eines Unternehmens können auf den Unternehmensinformationen angegeben werden und in verschiedenen lokalen Berichtsausdrücken verwendet werden.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch eine andere Funktion                                     |
| **Ersetzt durch eine andere Funktion?**   | Ja, das Einrichten von Beamten kann für den selben Zweck verwendet werden.   |
| **Betroffene Produktbereiche**         | Debitorenkonten, Kreditorenkonten, Bargeld- und Bankverwaltung |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.  |

### <a name="shipping-carrier-interface"></a>Versandspediteurschnittstelle

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Doppelte Funktionen   |
| **Ersetzt durch eine andere Funktion?**   | Teilweise ersetzt durch Transportverwaltung |
| **Betroffene Produktbereiche**         | Vertrieb und Marketing, Lagerverwaltung  |
| **Status**                         | Entfernt ab Dynamics 365 for Operations Version 1611.  |

### <a name="telepay-payment-formats-for-norway"></a>Telepay-Zahlungsformate für Norwegen

Telepay-Zahlungsformate enthalten Kreditorenzahlungsexport (Banküberweisung) und Debitorenzahlungsinkasso (Direktbelastung).

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Zahlungsformate werden nicht mehr verwendet.                                                        |
| **Ersetzt durch eine andere Funktion?**   | Ja, das ISO20022 Kredittransferzahlungsformat und das AvtaleGiro-Debitorenzahlungsformat für Norwegen sowie der Import der Rückgabedateien pain.002 und camt.054 der Bankbenachrichtigung. |
| **Betroffene Produktbereiche**         | Kreditorenkonten, Debitoren                                                          |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Exportformate für Kreditorenzahlungen für Finnland

Zwei Formate für den Export von Zahlungen werden für Finnland verfügbar. LM02 (FI) wird für Inlandszahlungen und LUM2 (FI) wird für Auslandszahlungen verwendet.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Zahlungsformate werden nicht mehr verwendet.                        |
| **Ersetzt durch eine andere Funktion?**   | Ja, ISO20022 Kredittransferzahlungsformat für Finnland       |
| **Betroffene Produktbereiche**         | Kreditorenkonten                                               |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="warehouse-management-ii"></a>Lagerortverwaltung II

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Lösung Lagerortverwaltung II (WMS II), die im Modul **Lagerverwaltung** verfügbar war, dupliziert Funktionen im Modul **Lagerortverwaltung**, das in Dynamics AX 2012 R3 veröffentlicht wurde.                                                                         |
| **Ersetzt durch eine andere Funktion?**   | Das Modul **Lagerortverwaltung**, das in AX 2012 R3, Dynamics AX 2012 R3 CU8 und Dynamics AX 2012 R3 CU9 veröffentlicht wurde, ersetzt die Funktionen der Lagerortverwaltung II. Das neue Modul hat fortschrittlichere Funktionen sowie flexiblere Lagerortverwaltungsprozesse als jene, die in den Funktionen der Lagerortverwaltung II angeboten werden. |
| **Betroffene Produktbereiche**         | Lagerverwaltung, Verkauf und Marketing, Beschaffung   |
| **Status**                         | Entfernt ab Dynamics 365 for Operations Version 1611.    |

### <a name="worker-reminders-in-human-resources"></a>Erinnerungen für Arbeitskräfte in der Personalverwaltung

Personalverwaltung-Lohndaten

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Geringe Verwendung                                                           |
| **Ersetzt durch eine andere Funktion?**   | Nein                                                                  |
| **Betroffene Produktbereiche**         | Personalverwaltung                                                     |
| **Status**                         | Entfernt ab Dynamics 365 for Operations Version 1611 |

### <a name="workflow-for-creating-goals"></a>Workflow zum Erstellen der Zielsetzungen

Ein Workflow für das Verwalten der Erstellung der Mitarbeiterziele ist einer von mehreren Workflows, die verfügbar sind, um den Leistungsverwaltungsprozes zu koordinieren.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Leistungsverwaltung wurde in Finance and Operations vollständig neu gestaltet.     |
| **Ersetzt durch eine andere Funktion?**   | Die neu entworfene Leistungsverwaltungsfunktion gibt mehr Kontrolle über den Inhalt der Ziele, die Messungen, die verwendet werden, um den Fortschritt zu verfolgen, und die Zuordnung der Begleitunterlagen. Ziele können als Vorlagen gespeichert werden und anschließend wieder verwendet werden. Diese Funktion kann Ihnen helfen, zusätzliche Ziele für Ihre Mitarbeiter schneller einzurichten. |
| **Betroffene Produktbereiche**         | Human Capital Management                 |
| **Status**                         | Entfernt ab Dynamics 365 for Operations Version 1611. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Möglichkeit zum Abbrechen von Änderungen an einer Kreditorenrechnung

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Leistungsverbesserung        |
| **Ersetzt durch eine andere Funktion?**   | Nein                             |
| **Betroffene Produktbereiche**         | Kreditorenkonten               |
| **Status**                         | Entfernt ab Dynamics AX 7.0. |

### <a name="aif-axd-and-axbc-integrations"></a>Integration mit AIF, AxD und AxBC

In Application Integration Framework (AIF), können Daten mit externen Systemen über Geschäftslogik ausgetauscht werden, die als Dienst verfügbar gemacht wird. Dynamics AX verfügt über Dienste, die auf Dokumenten und .NET Business Connector (AxBC) basieren. Ein Dokument wird über XML erstellt. Das XML umfasst Kopfinformationen, die hinzugefügt werden, um eine *Meldung* zu erstellen, die zu oder aus Dynamics AX übertragen werden kann. Beispiele zu Dokumenten sind Aufträge und Bestellungen. Fast jede Entität, z. B. ein Debitor, kann über Dokument dargestellt werden. Dienste, die auf Dokumenten basieren, verwenden die Klassen **Axd \<Document\>**.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Architektur von AIF und AxDs konnte nicht zu einem Clouddienst skaliert werden. Es gab Leistungsprobleme beim Massenimport.                                        |
| **Ersetzt durch eine andere Funktion?**   | Diese Funktion wird vom Datenimport-/Exportframework ersetzt, das den wiederholten Massenimport/-export unterstützt. Für AxBC wird empfohlen, dass Sie die tatsächlichen Tabellen verwenden. |
| **Betroffene Produktbereiche**         | AxDs, AxBCs und AIF   |
| **Status**                         | Entfernt ab Dynamics AX 7.0.   |

### <a name="billing-code-rate-scripts"></a>Abrechnungscode-Ratenskripts

Abrechnungsskripts wurden verwendet, um Abrechnungsraten für Abrechnungscodes zu berechnen. Diese Skripts erforderten benutzerdefinierte Entwicklung in der Programmiersprache C Sharp oder Visual Basic. In der aktuellen Version von Dynamics AX, werden die **Abrechnungscoderaten-Skripts** nicht unterstützt.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Unterstützung für die benutzerdefinierten C Sharp- oder Visual Basic-Skripts wurden nicht zu Dynamics AX 7.0 hinzugefügt. |
| **Ersetzt durch eine andere Funktion?**   | Nein                                                                                      |
| **Betroffene Produktbereiche**         | Öffentlicher Sektor, Debitoren                                    |
| **Status**                         | Entfernt ab Dynamics AX 7.0.                                                          |

### <a name="boms-without-bom-versions"></a>Stücklisten ohne Stücklistenversionen

Wurde der **Stücklistenversionen**-Konfigurationsschlüssel deaktiviert, so wurden Stücklisteversionen in allen Formularen ausgeblendet, und das System erzwang eine 1:1-Beziehung zwischen freigegebenen Produkten und Stücklisten. Der **Stücklistenversionen**-Konfigurationsschlüssel kann in der aktuellen Version von Dynamics AX nicht deaktiviert werden.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Verwenden eines Konfigurationsschlüssels, um die Skalierung von Stücklistenversionen in einer Cloudumgebung zu verhindern. |
| **Ersetzt durch eine andere Funktion?**   | Nein                                                                                      |
| **Betroffene Produktbereiche**         | Produktinformationsverwaltung, Lagerverwaltung                                    |
| **Status**                         | Entfernt ab Dynamics AX 7.0.                                                          |

### <a name="brazilian-bordero"></a>Brasilianer Bordero

Bestimmte Zahlungsmethode für brasilianische Unternehmen

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Unterstützung für die brasilianische Bordero-Zahlungsmethode wurde in der brasilianischen Version eingestellt. |
| **Ersetzt durch eine andere Funktion?**   | Nein   |
| **Betroffene Produktbereiche**         | Kreditorenkonten   |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="brazilian-sintegra-statement"></a>Brasilianischer Sintegra-Auszug

Bundessteuerauszug für ICMS-Steuer

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Dieser Auszug gilt nicht mehr für einige brasilianische Bundesländer. |
| **Ersetzt durch eine andere Funktion?**   | Nein Benutzer können das generische elektronische Berichtstool verwenden, um sofern erforderlich den Auszug für bestimmten Situationen zu konfigurieren. |
| **Betroffene Produktbereiche**         | Steuerbücher    |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasilianischer SCAN Notfallmodus für NF-e

(SCAN) Notfallumgebung wird verwendet, um den Status einer Nota Fiscal eletrônica (NF-e) zu generieren, zu exportieren und zu importieren, wenn die Umgebung von Secretaria da Fazenda (SEFAZ) nicht verfügbar ist.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Diese Notfallmethode gilt nicht mehr in allen brasilianischen Bundesländern |
| **Ersetzt durch eine andere Funktion?**   | Nein                                                                          |
| **Betroffene Produktbereiche**         | Debitoren                                                         |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.              |

### <a name="business-analyzer"></a>Business Analyzer

Diese mobile Anwendung ermöglicht dem Benutzer die Prüfung von wichtigen Geschäftsmetriken.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Funktion wurde durch eine andere Funktion ersetzt.   |
| **Ersetzt durch eine andere Funktion?**   | Das Inhaltspaket „Finanzielle Leistung überwachen“ für Microsoft Power BI umfasst entscheidende Finanzmetriken, die zuvor im Business Analyzer verfügbar waren. |
| **Betroffene Produktbereiche**         | Hauptbuch      |
| **Status**                         | Veraltet: Die Verwendung des Business Analyzer wurde veraltet.    |

### <a name="business-statistics"></a>Geschäftsstatistik

Die Einrichtung von Geschäftsstatistikabfragen kann das Analysieren der Leistung der Organisation unterstützen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ein veralteter Ansatz für Business Intelligence (BI), geringe Kundennutzung und ein begrenzter Funktionsumfang |
| **Ersetzt durch eine andere Funktion?**   | Neue BI-Lösungen für die aktuelle Version von Dynamics AX                                      |
| **Betroffene Produktbereiche**         | Beschaffung, Kreditorenkonten, Vertrieb und Marketing, Debitorenkonten         |
| **Status**                         | Entfernt ab Dynamics AX 7.0.                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Funktion zum Ändern des Dokumentdatum in der Rechnungsgenehmigungserfassung

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Geringe Verwendung                                                               |
| **Ersetzt durch eine andere Funktion?**   | Ja. Das Dokumentdatum auf der gebuchten Kreditorenbuchung kann geändert werden. |
| **Betroffene Produktbereiche**         | Kreditorenkonten                                                        |
| **Status**                         | Entfernt ab Dynamics AX 7.0.                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>ClieOp03-Zahlungsformat für die Niederlande

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Format ist nicht mehr in den Niederlanden anwendbar, da es durch die SEPA-Funktionen ersetzt wurde. |
| **Ersetzt durch eine andere Funktion?**   | SEPA-Zahlungsexport  |
| **Betroffene Produktbereiche**         | Alle Module     |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.   |

### <a name="compliance-center"></a>Compliance Center

Das Compliance Center war eine Enterprise Portal-Website für die Verwaltung der Dokumentationsanforderungen für Kompatibilitätsinitiativen, die dem Sarbanes-Oxley-Gesetz zugeordnet sind.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Fehlender Einsatz durch die Kunden. Microsoft SharePoint umfasst die gleichen Funktionen, die im Compliance Center verfügbar waren. |
| **Ersetzt durch eine andere Funktion?**   | Nein   |
| **Betroffene Produktbereiche**         | Konformität und interne Kontrollen  |
| **Status**                         | Entfernt ab Dynamics AX 7.0.    |

### <a name="connector-for-microsoft-dynamics"></a>Connector für Microsoft Dynamics

Dieses Tool wurde verwendet, um Schlüsseldaten aus Microsoft Dynamics CRM in Dynamics ERP-Anwendungen zu integrieren.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Funktion wurde durch eine andere Funktion ersetzt. |
| **Ersetzt durch eine andere Funktion?**   | Dataverse                                      |
| **Betroffene Produktbereiche**         | Connector für Dynamics                         |
| **Status**                         | Entfernt ab Dynamics AX 7.0.                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Container-Einheit und mehrere Dimensionen am Lager

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Doppelte Funktionen |
| **Ersetzt durch eine andere Funktion?**   | Ja. Seit AX 2012 ist diese Funktion durch die konsolidierte Chargenauftragsfunktion ersetzt worden. Dieser Funktionsumfang umfasst die konsolidierte verfügbare Ansicht. |
| **Betroffene Produktbereiche**         | Produktinformationsverwaltung, -Produktionssteuerung, Lagerverwaltung, Vertrieb und Marketing  |
| **Status**                         | Entfernt ab Dynamics AX 7.0. |

### <a name="cue-group-metadata"></a>Cue-Group-Metadaten

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Cue-Gruppen wurden verwendet, um eine oder mehrere Cues im Infoboxbereich anzuzeigen. Der Nutzen war beschränkt. Es gab außerdem Leistungsbedenken, da eine Datensatzändern in einem übergeordneten Formular eine Abfrage pro Cue aus der Cue-Gruppe verursacht hat. |
| **Ersetzt durch eine andere Funktion?**   | Nein      |
| **Betroffene Produktbereiche**         | Alle Module    |
| **Status**                         | Entfernt ab Dynamics AX 7.0.  |

### <a name="cue-metadata"></a>Cue-Metadaten

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Cue-Metadaten wurden auf das Zählen oder Summieren von Informationen beschränkt.    |
| **Ersetzt durch eine andere Funktion?**   | Tile-Metadaten wurden für mehr Flexibilität bei der Modellierung eingeführt. So können z. B. aktuelle Nummern, Navigation und Key Performance Indicators (KPIs) modellieren. Count-Tile-Metadaten sind ein direkter Ersatz für Cue-Metadaten. |
| **Betroffene Produktbereiche**         | Alle Module           |
| **Status**                         | Entfernt ab Dynamics AX 7.0      |

### <a name="danish-check-format"></a>Scheckformat Dänemark

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Unterstützung für das dänische Scheckformatlayout ist eingestellt wurden, und der Bericht ist aus der DK-Lokalisierung entfernt worden. |
| **Ersetzt durch eine andere Funktion?**   | Nein    |
| **Betroffene Produktbereiche**         | Alle Module    |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.  |

### <a name="data-partitions"></a>Datenpartitionen

Datenpartitionen enthalten eine logische Trennung von Daten in der Dynamics AX-Datenbank.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Datenpartitionen wurden in Dynamics AX 2012 R2 eingeführt, um Datenisolation zu ermöglichen. In einem häufigen Szenario verfügt ein Unternehmen über Tochtergesellschaften und die Daten einer Tochtergesellschaft sollen einer anderen nicht angezeigt werden, obwohl beide Tochterunternehmen von derselben IT-Abteilung verwaltet werden. Zusätzliche Skripts und Verwaltungsaufwand im gesamten Programm sind jedoch erforderlich, um neue Partitionen zu erstellen und mit Daten zu füllen und Partitionsdaten sichern. In der Cloud, in der wir über Platform-as-a-Service (PaaS)-Datenbankdienste (Microsoft Azure SQL-Datenbank) verfügen, ist es sehr viel effizienter, eine Datenbank als Isolationscontainer zu verwenden, als Isolationen im Programm durchzuführen. Egal, ob eine Datenpartitionierung für Tochterunternehmen, mehrere Mandanten oder nur zur Skalierung benötigt wird, glauben wir, dass die Szenarien besser über mehrere Datenbanken oder mehrere Instanzen von Finance and Operations behandelt werden können. |
| **Ersetzt durch eine andere Funktion?**   | Debitoren, die Datenpartitionen verwenden, müssen mehrere Instanzen von Finance and Operations verwenden, wenn die Datenbankebenentrennung ein kritisches Problem ist.    |
| **Betroffene Produktbereiche**         | Alle Module  |
| **Status**                         | Entfernt ab Dynamics AX 7.0.  |


### <a name="database-and-file-share-storage-for-attachments"></a>Datenbank- und Dateifreigabespeicher für Anhänge

Dynamics AX 2012 erlaubte die Speicherung von Anhängen in der Datenbank und in Dateifreigaben. Beide Optionen werden nicht mehr unterstützt.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Der Dateifreigabespeicher wird nicht mehr unterstützt, weil in der Cloud gehostete Umgebungen nicht mit lokalen Dateifreigaben kommunizieren können. Der Datenbankspeicher wurde zugunsten von Azure Blob-Speicher eingestellt. Azure Blob-Speicher ist äquivalent zur Speicherung in der Datenbank, weil der Zugriff auf Dokumente nur über Finance and Operations-Client-Formulare möglich ist. Auf diese Weise entsteht der zusätzliche Vorteil, dass Speicher bereitgestellt wird, der sich nicht negativ auf die Leistung der Datenbank auswirkt. Blob-Speicher ist der Standardspeichermechanismus für die Dokumentenverwaltung und funktioniert unmittelbar. |
| **Ersetzt durch eine andere Funktion?**   | Der Datenbankspeicher wurde zugunsten von Azure Blob-Speicher eingestellt.   |
| **Betroffene Produktbereiche**         | Alle Module  |
| **Status**                         | Entfernt ab Dynamics AX 7.0.   |

### <a name="delimitation"></a>Trennung

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Kein Verwendung der Funktionen gefunden. |
| **Ersetzt durch eine andere Funktion?**   | Nein                                     |
| **Betroffene Produktbereiche**         | Zeit und Anwesenheit                    |
| **Status**                         | Entfernt ab Dynamics AX 7.0.         |

### <a name="desktop-client"></a>Desktopclient

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Der Dynamics AX-Client wurde neu gestaltet, um die Benutzererfahrung über mehrere Plattformen und Geräte zu verbessern.                      |
| **Ersetzt durch eine andere Funktion?**   | Der neue Webclient basiert auf den Desktop-Formularmetadaten und -Programmiermodell, die geändert wurden, um eine umfangreiche Internet-Plattform bereitzustellen. |
| **Betroffene Produktbereiche**         | Alle Module  |
| **Status**                         | Entfernt ab Dynamics AX 7.0.   |

### <a name="direct-database-connection"></a>Direkte Datenbankverbindung

In Dynamics AX 2012 R3 konnte sich Retail Modern POS direkt mit der Kanal-DB verbinden, ähnlich wie beim Enterprise POS. Dies war zusätzlich zur Standardkommunikationsmethode von Retail Modern POS über den Retail Server.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Direkte Datenbankkonnektivität erforderte ein geringeres Sicherheitsprotokolle und wurde hauptsächlich verwendet, um den höchsten Leistungsstandard zu erreichen. Aufgrund der Leistung und der Sicherheitserweiterungen, die in Finance and Operations aufgetreten sind, führen diese Funktionen nun zu mehr Problemen, als sie lösen. |
| **Ersetzt durch eine andere Funktion?**   | Nein Nur Standard Retail Server Kommunikation wird nun unterstützt.  |
| **Betroffene Produktbereiche**         | Kanal-DB/Retail Modern POS   |
| **Status**                         | Entfernt ab Dynamics AX 7.0.  |

### <a name="dutch-swift-mt940"></a>Niederländisches SWIFT MT940

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Anstelle der lokalisierten Funktionalität wird nun eine generische Funktion verwendet.                    |
| **Ersetzt durch eine andere Funktion?**   | Ja, diese Funktion wurde durch erweiterte Bankabstimmungsfunktionen ersetzt. |
| **Betroffene Produktbereiche**         | Alle Module                                                                              |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL für Deutschland)

Diese Funktionen stellten die eXtensible Business Reporting Language (XBRL)-Ausgabe speziell für die deutsche eBilanz Taxonomie bereit.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Fehlender Einsatz durch die Kunden.  |
| **Ersetzt durch eine andere Funktion?**   | Nicht durch eine andere Funktion ersetzt. Es gibt aber mehrere spezielle XBRL-Pakete, die umfangreiche XBRL-Funktionen für den deutschen Markt bereitstellen. |
| **Betroffene Produktbereiche**         | Management Reporter      |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.  |

### <a name="enterprise-portal-client"></a>Enterprise Portal-Kunde

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Eine einzelne Clientplattform ist bereitgestellt worden.  |
| **Ersetzt durch eine andere Funktion?**   | Der neue Webclient basiert auf den Desktop-Formularmetadaten und -Programmiermodell, die geändert wurden, um eine umfangreiche Internet-Plattform bereitzustellen. |
| **Betroffene Produktbereiche**         | Alle Module  |
| **Status**                         | Entfernt ab Dynamics AX 7.0.   |

### <a name="environmental-sustainability"></a>Umweltverträglichkeit

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Geringe Kundennutzung und ein begrenzter Funktionsumfang.  |
| **Ersetzt durch eine andere Funktion?**   | Nein              |
| **Betroffene Produktbereiche**         | Konformität und interne Kontrollen, Kreditorenkonten  |
| **Status**                         | Entfernt ab Dynamics AX 7.0. |

### <a name="form-activex-and-managed-host-controls"></a>ActiveX- und Managed Host-Steuerelemente in Formularen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | ActiveX und die Managed Host-Steuerelemente basieren auf dem veralteten Desktopclient. |
| **Ersetzt durch eine andere Funktion?**   | Das Framework für erweiterbare Steuerelemente unterstützt die Erstellung neuer Steuerelemente, die auf HTML, CSS und JavaScript basieren, und dient als erstklassiges Steuerelement in der Microsoft Visual Studio-Toolumgebung. |
| **Betroffene Produktbereiche**         | Alle Module     |
| **Status**                         | Entfernt ab Dynamics AX 7.0.       |

### <a name="generate-prenotes-by-using-a-batch"></a>Generieren von Testtransaktionen als Stapelverarbeitung

Testtransaktionsgenerierung kann nicht mithilfe einer Charge verwendet werden. Sie kann jedoch immer noch von einem Benutzer erstellt werden.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Es ist kein Formular vorhanden, um die resultierende Testtransaktionsdatei zu verwalten und anzuzeigen, wenn sie mithilfe einer Charge generiert wurde. |
| **Ersetzt durch eine andere Funktion?**   | Testtransaktionen können weiterhin generiert werden, und der Benutzer hat die Kontrolle über den Speicherort der Datei.   |
| **Betroffene Produktbereiche**         | Debitorenkonten, Kreditorenkonten, Bargeld- und Bankverwaltung  |
| **Status**                         | Entfernt ab AX 7.0.    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Deutscher DTAUS-Zahlungsexport und Kontoauszugsimport (Summen und Buchungen)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Format ist nicht mehr in Deutschland anwendbar, da es durch die SEPA-Funktionen ersetzt wurde.                    |
| **Ersetzt durch eine andere Funktion?**   | Ja, diese Funktionalität wurde durch SEPA-Zahlungsexport und erweiterte Bankabstimmungsfunktionen zum Importieren von Kontoauszügen ersetzt. |
| **Betroffene Produktbereiche**         | Alle Module  |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="german-dtazv-payment-format-in-domestic-currency"></a>Deutsches DTAZV-Zahlungsformat in Landeswährung

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Format ist nicht mehr in Deutschland anwendbar, da es durch die SEPA-Funktionen ersetzt wurde. |
| **Ersetzt durch eine andere Funktion?**   | SEPA-Zahlungsexport    |
| **Betroffene Produktbereiche**         | Kreditorenkonten   |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.    |

### <a name="german-mt940-import"></a>MT940 Import, deutsch

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Anstelle der lokalisierten Funktionalität wird nun eine generische Funktion verwendet.                    |
| **Ersetzt durch eine andere Funktion?**   | Ja, diese Funktion wurde durch erweiterte Bankabstimmungsfunktionen ersetzt. |
| **Betroffene Produktbereiche**         | Alle Module                                                                              |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.                           |

### <a name="german-xml-eu-sales-list"></a>Deutsche XML EU Sales-Liste

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das XML-Format für EU-Umsatzliste für Deutschland wird nicht mehr unterstützt. Nur das Format der Textdatei ELMA5 kann verwendet werden, um den Bericht zur EU-Umsatzliste der deutschen Steuerbehörde zu senden. |
| **Ersetzt durch eine andere Funktion?**   | Nein         |
| **Betroffene Produktbereiche**         | MwSt.        |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.   |

### <a name="gl-ssrs-reports"></a>GL SSRS Berichte

Berichte mit den folgenden Menüoptionen wurden entfernt: **Zusammengefasste Zwischenbilanz**, **Ausführliche Zwischenbilanz**, **Kontenplan**, **Audit-Trail**, **Saldenliste** und **Summen- und Saldenliste**.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Microsoft SQL Server Reporting Services (SSRS)-Finanzberichte wurden durch Management Reporter-Funktionen und -Standardberichte ersetzt. |
| **Ersetzt durch eine andere Funktion?**   | Management Reporter (bezeichnet als **Finanzberichterstellung** in der aktuellen Version von AX)    |
| **Betroffene Produktbereiche**         | Hauptbuch   |
| **Status**                         | Entfernt ab Dynamics AX 7.0.   |

### <a name="infopart-and-formpart-metadata"></a>InfoPart- und FormPart-Metadaten

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | InfoPart- und FormPart-Metadaten ermöglichen die Erstellung von Infoboxen für zwei verschiedene Clients. |
| **Ersetzt durch eine andere Funktion?**   | InfoPart-Metadaten, die einen vereinfachten Formulardefinition darstellen, werden über ein Upgrade zu einem Formular konvertiert. FormPart-Metadaten, die ein Formular referenzieren, wird durch eine direktere Referenz ersetzt, die über ein Upgrade erstellt wird. |
| **Betroffene Produktbereiche**         | Alle Module    |
| **Status**                         | Entfernt ab Dynamics AX 7.0.        |

### <a name="main-account-list-page"></a>Listenseite "Hauptkonten"

Eine Liste der Konten für die juristische Person und die zugeordneten Saldoinformationen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Saldoinformationen sind auf der Listenseite **Zwischenbilanz** nach Konto und Dimension verfügbar.  |
| **Ersetzt durch eine andere Funktion?**   | **Hauptkonten** enthält die gleiche Liste aus Konten, die die **Hauptkonto** Listenseite enthielt. Die Rasteransicht in **Hauptkonten** zeigt auch eine kleinere, rasterähnliche Ansicht. |
| **Betroffene Produktbereiche**         | Hauptbuch      |
| **Status**                         | Entfernt ab Dynamics AX 7.0.    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malaysia- und Singapur-Bankcashflowbericht

Drucken eines Cashflowberichts mit Buchungen und Details des Zu- und Abflusses flüssiger Mittel für einen bestimmten Datumsbereich für die ausgewählten Bankkonten.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die gleichen Informationen können aus der Anfragenbankbuchung eingeholt werden. |
| **Ersetzt durch eine andere Funktion?**   | Die Anfragenbanktransaktion.                                            |
| **Betroffene Produktbereiche**         | Bargeld- und Bankverwaltung                                                |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden.          |

### <a name="mexican-cfd-electronic-invoice"></a>Mexikanische CFD (elektronische Rechnung).

Diese Funktion aktivierte die Generierung der mexikanischen elektronischen Rechnungen, indem die Methode Comprobante Fiscal Digital (CFD) angewendet wird, bei der das Unternehmen die Rechnung signiert, indem es die zugehörige Autorisierung von der Behörde anfordert. Diese Funktion umfasst auch einen monatlichen Bericht, der alle elektronischen Rechnungen umfasst, die in der Periode ausgestellt wurden.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Methode ist nicht mehr verfügbar. Die Generierung elektronischer Rechnungen über die CFD-Methode wurde von den Steuerbehörden als veraltet definiert und durch die Comprobante Fiscal Digital a través de Internet (CFDI)-Methode ersetzt, bei der die Signierung an einen Drittanbieter (PAC) delegiert wird. Der monatliche Bericht ist entfernt wurden. Eine Abfragemöglichkeit ermöglicht Benutzern die Abfrage von historischen Transaktionen. |
| **Ersetzt durch eine andere Funktion?**   | Nein    |
| **Betroffene Produktbereiche**         | Debitoren, Projekt   |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="mexico-realized-and-unrealized-vat"></a>Realisierte und nicht realisierter Mehrwertsteuer in Mexiko

Dynamics AX 2012 verwaltete die nicht realisierte Vorsteuer (MwSt.), indem es eine für Mexiko spezifische Funktionalität für nicht realisierte Steuer verwendete.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Doppelte Funktionen  |
| **Ersetzt durch eine andere Funktion?**   | Ja, diese Funktion wurde durch eine Standardmehrwertsteuerfunktion ersetzt, die von Core bereitgestellt wird. |
| **Betroffene Produktbereiche**         | MwSt.   |
| **Status**                         | Veraltet: Ein Datum für das Entfernen dieser Funktion ist nicht festgelegt worden. |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook-Integration


| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Diese Funktion wurde durch die Microsoft Exchange Server-Integration ersetzt. |
| **Ersetzt durch eine andere Funktion?**   | Ja                                                                            |
| **Betroffene Produktbereiche**         | Vertrieb und Marketing                                                            |
| **Status**                         | Entfernt ab Dynamics AX 7.0.                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Private Sperrung von Lager- und Lagerortverwaltungserfassungen

Die Bestands- und Lagerorterfassungen unterstützen nicht mehr die Möglichkeit, eine Erfassung als privat für einen ausgewählten Benutzer zu markieren. Nur der Prozess der Sperrung von Erfassungen als privat für Benutzergruppen und der Sperrung während der Bearbeitung wird unterstützt.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Kein Verwendung der Funktionen gefunden. |
| **Ersetzt durch eine andere Funktion?**   | Nein                                     |
| **Betroffene Produktbereiche**         | Lagerverwaltung                   |
| **Status**                         | Entfernt ab Dynamics AX 7.0.         |

### <a name="product-builder"></a>Produkt-Generator

Der Produktgenerator wurde zur dynamischen Konfiguration von Artikel aus einem Auftrag, Verkaufsangebot, Produktionsauftrag, Projektangebot oder einem Artikelbedarf verwendet. Basierend auf einem Produktmodell mit Modellvariablen kann der Benutzer Werte auswählen, um die Kundenanforderungen zu erfüllen und eine eindeutige Produktvariante mit einer Stückliste und einem Arbeitsplan zu erhalten.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Der Produktgenerator zeigte X++-Code für die Endbenutzer an und wird in der aktuellen Version von Dynamics AX nicht unterstützt. Es ist entfernt wurden, um doppelten Wartungsaufwand durch Überschneidung einer beträchtlichen Codebases zu vermeiden.  |
| **Ersetzt durch eine andere Funktion?**   | Ja. Die einschränkungsbasierte Konfiguration wurde in Dynamics AX 2012 eingeführt, wo bereits angekündigt wurde, dass der Produkt-Generator in zukünftigen Versionen veraltet sein wird. Die Technologie der einschränkungsbasierten Konfiguration wird bei den Produktmastern ausgewählt, um die Konfiguration zu aktivieren. Weitere Informationen finden Sie unter [Produktkonfiguration – Übersicht](../../../supply-chain/pim/build-product-configuration-model.md). |
| **Betroffene Produktbereiche**         | Produktinformationsverwaltung, Vertrieb und Marketing  |
| **Status**                         | Entfernt ab Dynamics AX 7.0.      |

### <a name="production-floor-app"></a>Produktions-App
Dies ist die App für Tabletgeräte, auf denen Windows 8.1 RT und Windows 8.1 Pro ausgeführt wird.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Mit dem Wechsel zu einem webbasierten Client ist es möglich, ähnliche Funktionen durch den systemeigenen Dynamics AX 7.0-Client bereitzustellen. Das Einzelvorgangslisten-Gerät stellt eine Produktionsbenutzer-Oberfläche bereit, die für Toucheingabe- und Tabletformularfaktoren optimiert ist. |
| **Ersetzt durch eine andere Funktion?**   | Ja. Das Einzelvorgangslisten-Gerät, das ein systemeigener Bestandteil von Dynamics AX 7.0 ist.                                                                           |
| **Betroffene Produktbereiche**         | Produktionssteuerung                                                |
| **Status**                         | Veraltet: Ein Datum für die Entfernung aus dem Microsoft Store ist für diese Funktion noch nicht festgelegt worden.                                                |


### <a name="rename-product-dimension"></a>Produktdimension umbenennen

Mit dieser Funktion können Sie den Namen einer der drei Standardproduktdimensionen (Größe, Farbe oder Stil) auf einen passenderen Namen ändern, der Ihren Geschäftsanforderungen besser entspricht. Das Umbenennen umfasste alle Beschriftungen, in denen der Produktdimensionsname verwendet wurde.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die aktuelle Version von Dynamics AX unterstützt keine Beschriftungsänderungen zur Laufzeit. |
| **Ersetzt durch eine andere Funktion?**   | Nein                                                                            |
| **Betroffene Produktbereiche**         | Produktinformationsverwaltung                                                |
| **Status**                         | Entfernt ab Dynamics AX 7.0.                                                |

### <a name="retail-server-connectivity-using-http"></a>Retail Serververbindung mithilfe von HTTP

In Dynamics AX 2012 R3 konnte der Retail Server mithilfe der HTTP-Kommunikation arbeiten (ungesichert). Dies war zusätzlich zur Standardkommunikation mithilfe HTTPS.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Aufgrund der neuen Sicherheitsanforderungen wird nur noch die gesicherte Kommunikation mit TLS 1.2 (oder höher, wenn verfügbar) unterstützt. Der Self-Service-Installer konfiguriert automatisch den Computer für die Kommunikation. |
| **Ersetzt durch eine andere Funktion?**   | Nein Nur Standard HTTPS-Kommunikation wird nun unterstützt. |
| **Betroffene Produktbereiche**         | Retail Server  |
| **Status**                         | Entfernt ab Dynamics AX 7.0. |

### <a name="role-center-pages"></a>Rollencenterseiten

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Rollencenter-Seiten basierten auf der veralteten Enterprise Portal-Plattform, die durch die neue Webclient-Plattform in der aktuellen Version von Dynamics AX ersetzt wurde. |
| **Ersetzt durch eine andere Funktion?**   | Das neue Arbeitsbereichs-Formularmuster bietet Benutzer ein prozesszentriertes Design, das den einfachen Zugriff auf häufig verwendete Aufgaben innerhalb dieses Prozesses bietet.                       |
| **Betroffene Produktbereiche**         | Alle Module    |
| **Status**                         | Entfernt ab Dynamics AX 7.0   |

### <a name="sales-tax-jurisdictions"></a>Umsatzsteuerzuständigkeiten

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Geringe Kundennutzung und ein begrenzter Funktionsumfang. |
| **Ersetzt durch eine andere Funktion?**   | Nein                                           |
| **Betroffene Produktbereiche**         | US-Mehrwertsteuer                                 |
| **Status**                         | Entfernt ab Dynamics AX 7.0.               |

### <a name="sites-services"></a>Sites Services

Sites Services lassen Sie Websites erstellen, die Ihre Geschäftsprozesse mit dem Internet ohne IT-Support erweitern.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Die Microsoft Azure-Infrastruktur, die von Dynamics AX verwendet wird, hat neue Funktionen, die stattdessen verwendet werden können (beispielsweise Azure-Sites). |
| **Ersetzt durch eine andere Funktion?**   | Nein   |
| **Betroffene Produktbereiche**         | Personalverwaltungs-Pesonalbeschaffung, Anfragenverwaltung, Angebotsanforderungen, Kreditorenerfassung, kooperative Arbeitsbereiche für Verkaufschancen und Kampagnen  |
| **Status**                         | Entfernt ab Dynamics AX 7.0.    |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS Bedarfsplanungsdienste

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Das Design der Funktion kann nicht von der neuen Cloudarchitektur unterstützt werden. |
| **Ersetzt durch eine andere Funktion?**   | Azure Machine Learning Bedarfsplanungsstrategie                           |
| **Betroffene Produktbereiche**         | Produktprogrammplanung                                                              |
| **Status**                         | Entfernt ab Dynamics AX 7.0.                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Kreditorenrechnungspool ohne Buchungsdetails

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Geringe Verwendung. Diese Funktion wurde durch die Rechnungserfassung ersetzt, die Workflowfunktionen hat. |
| **Ersetzt durch eine andere Funktion?**   | Workflowfunktionalitäten der Rechnungserfassung     |
| **Betroffene Produktbereiche**         | Kreditorenkonten |
| **Status**                         | Entfernt ab Dynamics AX 7.0.    |


### <a name="virtual-company-accounts"></a>Virtuelle Unternehmenskonten

Die virtuelle Unternehmensfunktion wird nicht mehr in Dynamics AX unterstützt. Die virtuelle Unternehmensfunktion ermöglicht es Benutzern, Tabellen einzurichten, die für eine Gruppe von Unternehmen freigegeben werden könnten. Eine Beschreibung der Funktion finden Sie unter [Unternehmenskonten und virtuelle Unternehmenskonten](../../fin-ops/get-started/ax4-content-retired.md). Die Funktion arbeitet, indem sie Tabellen in Sammlungen gruppiert die virtuellen Unternehmen zugewiesen werden (Gruppen von "tatsächlichen" Unternehmen). Abfragen werden erstellt, sodass alle Unternehmen im virtuellen Unternehmen auf die Daten in Tabellen der zugeordneten Tabellensammlungen zugreifen können.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | - Virtuelle Unternehmen müssen eingerichtet werden, bevor Daten in Tabellen gespeichert werden. Das nachträgliche Einpassen von virtuellen Unternehmen in eine vorhandene Implementierung ist sehr schwierig.<br><br>- Da in der aktuellen Version von Dynamics AX eine starke Datennormalisierung vorgenommen wurde, ist es sehr schwierig zu wissen, was zu den Tabellensammlungen hinzugefügt werden muss. Beispielsweise ist es schwierig, zu wissen, welche Tabellen freigegeben werden sollen. Alle Tabellen die auf Tabellen verweisen, die in einem virtuellen Unternehmen sind, müssen ebenfalls hinzugefügt werden. Die Tabellennormalisierung bedeutet, dass auch einfache Masterdaten, die auf eine Vielzahl von Tabellen verteilt sind, Teil des virtuellen Unternehmens sein müssen. Jeder Fehler, der hier auftritt, verursacht funktionale Probleme.<br><br>- Wenn eine Tabelle Teil eines virtuellen Unternehmens ist, verliert sie Informationen über den Ursprung der Daten. Nur das virtuelle Unternehmen wird erfasst.   |
| **Ersetzt durch eine andere Funktion?** | Globale Tabellen können verwendet werden, um Tabellen für alle Unternehmen verfügbar zu machen. Zurzeit besteht kein Ersatz. |   
| **Betroffene Produktbereiche**       | Alle Module |   
| **Status**                       | Entfernt ab Dynamics AX 7.0.   |   

### <a name="windows-8-tablet-app"></a>Windows 8-Tablet-App

Die bereitgestellte Funktionen der Windows 8-Tablet-App für Speseneintrag und Genehmigung.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Finance and Operations ist mit Tablets kompatibel. Die Tablet-App wird nicht mehr benötigt.    |
| **Ersetzt durch eine andere Funktion?**   | Nein          |
| **Betroffene Produktbereiche**         | Spesenverwaltung   |
| **Status**                         | Entfernt: Diese Funktionalität ist nur für Dynamics AX 2012 R3 verfügbar. |

### <a name="workplanner"></a>Arbeitsplanung

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Geringe Verwendung |
| **Ersetzt durch eine andere Funktion?**   | Nein, aber die Seite **Profilbeziehung**, die von der Seite **Profilgruppen** geöffnet wird, unterstützt das gleiche Geschäftsszenario wie die veraltete Seite **Arbeitsplanung**. |
| **Betroffene Produktbereiche**         | Zeit und Anwesenheit     |
| **Status**                         | Der Code wurde nicht entfernt. Allerdings wurde das Formular „JmgWorkPlanner” nicht migriert.    |

### <a name="x-financial-statements"></a>X++ Finanzaufstellungen

| &nbsp;  | &nbsp; |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <strong>Grund für veralteten Zustand/Entfernung</strong> |                         Die Funktion wurde durch eine andere Funktion ersetzt.                         |
|  <strong>Ersetzt durch eine andere Funktion?</strong>  | Management Reporter (bezeichnet als <strong>Finanzberichterstellung</strong> in der aktuellen Version von AX) |
|     <strong>Betroffene Produktbereiche</strong>     |                                              Hauptbuch                                              |
|             <strong>Status</strong>             |                                      Entfernt ab Dynamics AX 2012                                      |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

