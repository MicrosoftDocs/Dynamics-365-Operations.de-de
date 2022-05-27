---
title: Neuheiten und Änderungen in Dynamics AX 7.0 (Februar 2016)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics AX 7.0 entweder neu oder geändert sind. Diese Version enthält beide Plattform- und Anwendungsfunktionen, die im Februar 2016 veröffentlicht wurden.
author: sericks007
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 91243
ms.assetid: 515bc6e7-a85d-4995-95c6-6cab6c8aa0f9
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d81d20045c7b06de01a023d1a34ee653dd696ff1
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711319"
---
# <a name="whats-new-or-changed-in-dynamics-ax-70-february-2016"></a>Neuheiten und Änderungen in Dynamics AX 7.0 (Februar 2016)

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics AX 7.0 entweder neu oder geändert sind. Diese Version enthält beide Plattform- und Anwendungsfunktionen, die im Februar 2016 veröffentlicht wurden.

## <a name="cost-management"></a>Kostenverwaltung

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ein kurzer Überblick zum Lagersaldo, Ressource in Fertigung (RIF) und zum Lagerzufluss und -abfluss während des ausgewählten Geschäftsjahres.</td>
<td>Nicht zutreffend</td>
<td>Der Arbeitsbereich <strong>Kostenverwaltung</strong> enthält einen Abschnitt, in dem die Lageraufstellung oder die RIF-Lageraufstellung während des ausgewählten Finanzzeitraums dargestellt wird. Der Aufstellung basiert auf einem Datensatz-Cache, der standardmäßig alle 24 Stunden aktualisiert wird. Daten-Cache kann so konfiguriert werden, das Benutzer ihn manuell für Berichte in Echtzeit aktualisieren können. Die <strong>Datenaktualisierungsstatuskarte</strong> im <strong>Kostenadministration</strong>-Arbeitsbereich zeigt, wann der Cache zuletzt aktualisiert wurde.</td>
<td>Kostencontroller interessieren sich dafür, ob sich der Lageraufstellungs- oder RIF-Lageraufstellungsaldo mit der Zeit erhöht oder verringert. Durch die Klassifizierung betrieblicher Ereignisse im Auszug kann der Kostencontroller einen Überblick über den Bestandsfluss abrufen. Wenn das Lager oder das RIF-Lager nach Standardkosten evaluiert wird, kann auch die gesamte erfasste Abweichung betrachtet werden.</td>
</tr>
<tr>
<td>Verwenden Sie das <strong>Kostenmanagement</strong>-Modul.</td>
<td>Nicht zutreffend</td>
<td>Die Kostenverwaltung wird als Domänenbereich eingeführt. Kostenabhängige Konfiguration und Informationen auf die Lagerverwaltung, die Produktionssteuerung und die Kreditoren verteilt.</td>
<td>Da alle Aufgaben, die zum Kostenmanagement gehören, in einem Modul zentralisiert werden, ist es für Kostencontroller leichter, das System zu verwalten.</td>
</tr>
<tr>
<td>Die Buchungstypen, die zur Bestandsbuchhaltung und zur Produktionskalkulation gehören, wurden aktualisiert.</td>
<td>Die Beschriftungen in den Formularen <strong>InventPosting</strong>, <strong>Ressource</strong>, <strong>ResourceGroup</strong>, und <strong>ProductionGroup</strong> sind nicht immer an den tatsächlichen <strong>LedgerPostingType</strong>-Beschriftungen ausgerichtet. Es ist nicht einfach, die Terminologie zu verstehen, die in die Bezeichnungen verwendet wird.</td>
<td>Die Beschriftungen wurden aktualisiert. Auf den Seiten <strong>InventPosting</strong>, <strong>Ressource</strong>, <strong>ResourceGroup</strong>, und <strong>ProductionGroup</strong> passen Sie nun zu den tatsächlichen <strong>LedgerPostingType</strong>-Beschriftungen. Alle Beschriftungen wurden umbenannt. Sie passen nun zu den betrieblichen Ereignisse. Beachten Sie, dass die tatsächliche Buchungslogik nicht geändert wurde.</td>
<td>So ist es einfacher, das System zu konfigurieren, da die neuen Beschriftungen zu betrieblichen Ereignissen zugeordnet werden, die die Buchungsart verwenden sollen.</td>
</tr>
<tr>
<td>Importieren/exportieren des Einkaufspreises, der Kosten oder des Verkaufspreises aus Microsoft Excel in oder aus einer Nachkalkulationsversion.</td>
<td>Sie können Importpreise oder Kosten nicht ordnungsgemäß in eine Nachkalkulationsversion importieren, da das Datenmodell eine InventDim-ID erfordert.</td>
<td>Die Hinzufügen von Datenentitäten ermöglicht die Implementierung einer Import-/Exportfunktion. Mit dieser Funktion kann ein Benutzer Preise oder Kosten in eine Nachkalkulationsversion importieren/exportieren.
<ul>
<li>Importieren Sie eine vollständige Liste der Einkaufspreise des nächsten Jahrs, die Sie von der Einkaufsabteilung erhalten.</li>
<li>Übertragen Sie Kosten- und Standardverkaufspreise aus den Hauptsitzen an eine oder mehrere Vertriebsunternehmen in einem Arbeitsgang.</li>
</ul></td>
<td>Die Kostencontroller können viel Zeit sparen, wenn sie das System verwalten. Besonders, wenn sie Normalkosten für das nächste Geschäftsjahr verwalten müssen.</td>
</tr>
<tr>
<td>Abrufen eines kurzen Überblicks zum Bestandssaldo und der durchschnittlichen Einheitenkosten eines Kostenträgers.</td>
<td>Der Benutzer muss das Formular öffnen und die Lagerungsdimensionen auswählen, die den Kostenträger widerspiegeln. Daher muss der Benutzer wissen, welche Lagerungsdimensionen für den wertmäßigen Bestand für das jeweilige Produkt markiert wurden.</td>
<td>Eine neue <strong>Kostenträger</strong> Seite wird eingeführt. Standardmäßig zeigt diese Seite alle Kostenträger an, die dem Produkt zugeordnet werden. Auf der Seite werden die aktuelle Bestandsmenge, der Wert und die durchschnittlichen Einheitenkosten pro Kostenträger angezeigt.</td>
<td>Sie verringert die Komplexität und vereinfacht die Arbeit der Kostencontroller.</td>
</tr>
<tr>
<td>Verwenden Sie die neue <strong>Kosteneinträge</strong>- Seite während Lagerverwaltung.</td>
<td>Es kann schwieriger werden, die Lagersteuerung für registrierte Lagerbuchungen und zugeordnete Ausgleiche auszuführen, da die gleichen Buchungen physisch oder wertmäßig sein können.</td>
<td>Die <strong>Kosteneinträge</strong>-Seite bietet eine neue Methode, Lagerbuchungen anzuzeigen.
<ul>
<li>Die Buchungen werden in chronologischer Reihenfolge anzeigen</li>
<li>Nur Buchungen, die zu den Kosten beitragen, werden einbezogen.</li>
<li>Es Physische Kosten oder Finanzkosten werden nicht angezeigt.</li>
<li>Es physische Menge und die wertmäßige Menge werden nicht angezeigt.</li>
<li>Die Kosten werden inkrementell hinzugefügt.</li>
</ul></td>
<td>Kostencontroller können bei der Lagersteuerung auf der Buchungsebene viel Zeit sparen.</td>
</tr>
<tr>
<td>Verwenden Sie das neue <strong>Produktions-RIF-Aufstellung</strong>-Dialogfeld, um eine zusammengefasste Ansicht von kumulierten Kosten für ein bestimmtes Produkt zu sehen.</td>
<td>Nicht zutreffend</td>
<td>Die RIF-Aufstellung zeigt einen zusammengefassten RIF-Saldo des jeweiligen Produktionsauftrags an, gruppiert in entsprechende Aufteilungen der Kosten nach Kostenarten. Ein Diagramm zeigt in chronologischer Reihenfolge, wie sich betriebliche Buchungen auf den RIF-Saldo auswirken.</td>
<td>Kostencontroller können viel Zeit sparen, wenn sie wissen müssen, was der Saldo des aktuellen RIF für einen bestimmten Produktionsauftrag ist oder wie viel Material im Auftrag verbraucht wurde.</td>
</tr>
<tr>
<td>Verwenden Sie die Vergleichsfunktion "Kosten anzeigen", die für Produktionsaufträge eingeführt wurde. Die Funktion vereinfacht den Vergleich von Kosten, die einem Produktionsauftrag zugeordnet sind.</td>
<td>Der Benutzer kann nur vorkalkulierte Kosten und realisierte Kosten vergleichen. Der Vergleich kann auf der niedrigsten Ebene ausgeführt werden.</td>
<td>Die Kostenvergleichsfunktion ermöglicht Kostencontrollern den vergleichen der folgenden Daten:
<ul>
<li>Aktive Kosten vs. vorkalkulierte Kosten = der Planungsabweichung</li>
<li>Vorkalkulierte Kosten vs. realisierte Kosten = Produktionsabweichung</li>
<li>Planungsabweichung + Produktionsabweichungs- = Gesamtabweichung</li>
</ul>
Diese Funktion funktioniert unabhängig von den Nachkalkulationsmethoden, die dem produzierten Artikel zugewiesene werden. Standardmäßig zeigt ein Diagramm den Kostenvergleich nach Kostengruppentyp. Das Diagramm ermöglicht Benutzern die Anzeige von Details.</td>
<td>Kostencontroller oder Produktions-Manager können analysieren, wo die Produktionsabweichungen auftritt und was sie verursacht.</td>
</tr>
</tbody>
</table>

## <a name="developer"></a>Entwickler

| Wie können Sie vorgehen? | Dynamics AX 2012 | Dynamics AX 7.0 | Warum ist dieses wichtig? |
|------------------|------------------|-----------------|------------------------|
| Erstellen Sie webbasierte Lösungen in der Cloud, auf die über eine Vielzahl von Geräten zugegriffen werden kann. | Nicht verfügbar | Die aktuelle Version von Dynamics AX basiert auf einem neuen webbasierten Client und einem Client-Framework. | Sie können Ihre Endbenutzern Lösungen der nächsten Generation bereitstellen. |
| Entwickeln Sie Ihre Lösungen mit Microsoft Visual Studio. | Microsoft MorphX ist die wichtigste Entwicklungsumgebung, aber einige Entwicklungsaktivitäten erfolgen in Visual Studio. | Visual Studio ist die einzige Entwicklungsumgebung. | Vertraute Dynamics AX 2012-Konzepte bleiben erhalten und werden nahtlos an das Visual Studio-Framework und die Paradigmen angepasst. Es ermöglicht eine Standardinteroperabilität mit anderen .NET-Sprachen und -Projekten. |
| Compile Common Intermediate Language (CIL) für alle Funktionen. | X++ wird zu p-Code kompiliert. | Der nagelneue X++-Compiler generiert CIL für alle Funktionen. CIL ist die Intermediate-Language, die bereits von anderen .NET-basierten Sprachen verwendet wird. | CIL ist schneller, kann Klassen in verwalteten Dynamic Link Librarys (DLLs) effizienter referenzieren und kann auf einer größere Toolbasis von .NET-Hilfsprogrammen ausgeführt werden. |
| Im Microsoft Dynamics AX-Client sind BI-Berichte und -Visualisierungen eingebettet. | Nicht verfügbar | Erstellen Sie die intuitive und flüssige Visualisierungen. | Sie ermöglichen bessere Entscheidungen auf Grundlage von BI. |
| Integration in Microsoft Office. | Nicht verfügbar | Neue Funktionen umfassen die Excel-Datenkonnektor-Anwendung, die **Arbeitsmappen-Designer**-Seite, die Export-API und die Dokumentverwaltung. | Sie können Produktivitätslösungen für die Endbenutzer erstellen. |
| Automatisieren Sie Builds, Tests und Bereitstellungen. | Teilweise verfügbar | Stellen Sie die Entwicklertopologie über die "Developer and Build"-VM bereit. Konfigurieren Sie die Build-WM für die automatische Erkennung und das Erstellen von Modulen aus Visual Studio Online (VSO) und führen Sie Tests aus. C\#- und X++-Modulkompilierung und -Referenzen werden unterstützt. | Es erhöht die Entwicklerproduktivität, indem es die Kosten und den Aufwand für das Testen und die Validierung verringert. |
| Anpassen mit Overlays und Erweiterungen. | Erweiterungen sind nicht verfügbar. | Die aktuelle Version von Dynamics AX-hat ein neues Anpassungsmodell. | Sie können Quellcode und Metadaten von Modellelementen anpassen, die von Microsoft oder von Drittanbietern bereitgestellt werden. |
| Erstellen Sie neue Steuerelemente und Benutzeroberflächenelemente, indem Sie X++ und ein modernes Internet-Framework verwenden. | Benutzerdefinierte Steuerelemente basieren auf externen Frameworks wie Microsoft ActiveX und Windows Presentation Foundation (WPF). | Es ist einfacher, Steuerelemente in der aktuellen Version zu erstellen. Das X++-Framework kann für das Anwendungsverhalten und die Geschäftslogik verwendet werden, und ein HTML/JavaScript-basierter Client ermöglicht moderne Visualisierungen. | Ihre Steuerelemente können so konzipiert werden, das sie wie die vordefinierten Dynamics AX-Steuerelemente aussehen und sich auch so verhalten. |
| Prüfen und Anpassen der Leistung mit neuen Tools. | PerfSDK, Datenerweiterungs-Toolkit, Ablaufverfolgungsparser-Webanwendung und PerfTimer sind nicht verfügbar. | PerfSDK, Datenerweiterungs-Toolkit, Ablaufverfolgungsparser-Webanwendung und PerfTimer sind neu. | Mit dem Software Development Kit (SDK) können Sie alle wichtigen Geschäftsprozesse für die Leistung und einem Einzelbenutzer- und, falls zutreffend, einen Mehrbenutzen Testlauf testen und überprüfen. Mit dem Datenerweiterungs-Toolkit können Sie alle Leistungstests ausweiten, die Masterdaten und buchungsbezogenen Daten korrekt erweitern müssen. Mit dem Ablaufverfolgungs-Parser können Sie einen Einzelbenutzerleistungstest oder eine Mehrbenutzerlauf überprüfen. Mit PerfTimer können Sie sehen, ob eine Abfrage oder ein bestimmter Methodenaufruf ein Performanceproblem verursacht. Daher müssen Sie keine Verfolgung vornehmen und alles einzeln analysieren. |
| Anzeigen einer aktualisierbarer Ansicht mithilfe von OData. | Nicht verfügbar | Die aktuelle Version von Dynamics AX bietet einen öffentlichen OData-Endpunkt, der den Zugriff auf Dynamics AX-Daten auf konsistente Art für breites Spektrum von Kunden ermöglicht. | Ihre Lösungen können mit RESTful-Diensten interagieren, Daten bereitstellen und eine breite Integration über HTTP ermöglichen. |
| Nutzen Sie den Business Connector, um Geschäftslogiken zu erstellen und Integrationsszenarien zu unterstützen. | Der Business Connector ist verfügbar, um X++-Code vom verwalteten Code aufzurufen. Es wird empfohlen, den Business Connector nur zu verwenden, um die Geschäftslogik in C\# zu erstellen. Eine Verwendung für Integrationsszenarien wird nicht empfohlen. | Der Business Connector wird nicht mehr unterstützt. Die Erstellungsanforderung gelten, weil X++ in verwalteten Code kompiliert wird. Daher ist die Interoperabilität einfacher. Die Integrationsszenarien werden über OData unterstützt. | Sie können den Business Connector nicht weiter verwenden. |
| Wählen Sie "Skala" (die Anzahl der Dezimalstellen) für echte Datenbankfelder und erweiterten Datentypen (EDTs) aus. | Skala 16 steht für die standardmäßige Skala und kann nicht durch den Entwickler geändert werden. | EDTs und Felder haben nun eine Skalaeigenschaft, die auf das einzelne Feld und den EDT angewendet werden kann. Der Standardwert ist 6 und nicht 16. | Die Leistung bei NCCI-Tabellen (speicherinterne Tabellen in SQL) ist bei Sortierung nach Größe bei einem kleinen Skala höher. Ändern Sie den Skala, wenn dies bei Ihrer Verwendung von einzelnen Felder erforderlich ist. |

## <a name="financial-management"></a>Finanzverwaltung

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Exportieren Sie Kontostrukturen in Microsoft Excel.</td>
<td>Nicht verfügbar</td>
<td>Sie können eine ausgewählte Kontostruktur nun nach Excel exportieren.</td>
<td>Zahlreiche Kunden haben die Möglichkeit angefordert, Kontostrukturen zur einfacheren Filterung nach Excel exportieren zu können.</td>
</tr>
<tr>
<td>Zeigen Sie Sachkonten und erweiterte Regelstrukturen an, die einer Kontostruktur auf einer einzelnen Seite zugeordnet sind.</td>
<td> Der Benutzer muss auf mehrere Formularen navigieren, um die Sach- und die Kontostruktur anzuzeigen, die verwendet werden.</td>
<td>Es wurden zur Kontostrukturseite Infoboxen hinzugefügt.</td>
<td>Es ist einfacher, auf wichtige Informationen zuzugreifen, wenn Kontostrukturen definiert und bearbeitet werden.</td>
</tr>
<tr>
<td>Anzeigen von Sachkonten angezeigt, die einem Kontenplan auf einer einzelnen Seite zugeordnet sind.</td>
<td>Der Benutzer muss zu jedem Unternehmen navigieren und das Sachkontoformular öffnen, um das Diagramm des Kontos zu finden, das dem Sachkonto zugeordnet ist.</td>
<td>Es wurden zur Kontostrukturseite <strong>Kontenpläne</strong> hinzugefügt.</td>
<td> Es ist einfacher, auf wichtige Informationen zuzugreifen, wenn Kontenpläne definiert und zugewiesen werden.</td>
</tr>
<tr>
<td>Anzeigen von Abschlussbogenanpassungen und Abschlussbuchungen in unterschiedliche Spalten auf der Listenseite <strong>Zwischenbilanz</strong>.</td>
<td>Der Benutzer sieht beide Arten von Buchungen in einer Spalte.</td>
<td>Ein zusätzlicher Parameter wurde zur Listenseite <strong>Zwischenbilanz</strong> hinzugefügt.</td>
<td>So ist eine präzisere Datenanalyse möglich. Außerdem wird er für gesetzlich vorgeschriebene Berichte in einigen Ländern/Regionen benötigt.</td>
</tr>
<tr>
<td>Verwenden Sie die neue <strong>Globale allgemeine Erfassungen</strong>-Seite.</td>
<td>Nicht verfügbar</td>
<td>Neue <strong>Globale allgemeine Erfassungen</strong>-Seite für allgemeine Erfassungen. Berechtigungen für diese Seite werden zur Rolle <strong>Buchhalter</strong> hinzugefügt.</td>
<td>Ermöglicht einem Buchhalter für gemeinsame Dienste allgemeine Erfassungen über Unternehmen hinweg einzugeben, ohne das Formular zu verlassen oder den Unternehmenskontext wechseln Quellunternehmenskontomüssen.</td>
</tr> 
<tr>
<td>Verwenden Sie die neue <strong>Buchhaltungsquellen-Explorer</strong>-Seite.</td>
<td>Für Dynamics AX 2012 R3 CU10 verfügbar.</td>
<td>Neue <strong>Buchhaltungsquellen-Explorer</strong>-Seite und Aktionen zur Navigation von der <strong>Zwischenbilanz</strong>-Listenseite und der Seite <strong>Belegtransaktionen</strong>.</td>
<td>Ermöglicht die detaillierte Anzeige von Informationen zur Quelle einer Zwischenbilanz oder eines Buchhaltungseintrags im Hauptbuch oder für Ad-hoc-Analysen.</td>
</tr>
<tr>
<td>Zusätzliche Buchungsebenen hinzufügen.</td>
<td>Zusätzliche Buchungsebenen war eine Entwicklerfunktion.</td>
<td>Jetzt sind zehn Buchungsebenen verfügbar.</td>
<td>Die meisten Kunden fügen zusätzliche Buchungsebenen hinzu.</td>
</tr>
<tr>
<td>Verwenden der Option "Zugehöriger Beleg".</td>
<td>Nicht verfügbar</td>
<td>Die Option "Zugehöriger Beleg" ist für Benutzer verfügbar, um den Beleg im Gegenkonto des Unternehmenskontos beim Buchen von Intercompany-Transaktionen zu sehen. Über "Zugehöriger Belege" können Benutzer auf Details klicken und schnell zum und Beleg für das Gegenkontos des Unternehmen springen.</td>
<td>Bei der Buchung von Intercompany-Transaktionen konnten Benutzer den im Gegenkonto des Unternehmens gebuchten Beleg nicht sehen oder nachverfolgen.</td>
</tr>
<tr>
<td>Massen-Finanzperiodenabschluss</td>
<td>Nicht verfügbar</td>
<td>Die Benutzer können den Zugriff auf das Modul aktualisieren und den Periodenstatus für mehrere Unternehmen gleichzeitig ändern.</td>
<td>Vor der Funktion mussten Benutzer das angemeldete Unternehmen ändern, zum Sachkontokalenderformular wechseln und den Modulzugriff und den Periodenstatus manuell aktualisieren.</td>
</tr>
<tr>
<td>Wechselkurse über Oanda.</td>
<td>Konfigurieren des Wechselkursanbieter für den Import von Kursen von Oanda war eine Entwicklerfunktion.</td>
<td>Wenn Benutzer einen Schlüssel für Oanda haben, können sie diesen beim Konfigurieren des Wechselkursanbieters eingeben.</td>
<td>Benutzer können die Funktionalität direkt nutzen, indem sie regelmäßig Wechselkurse von Oanda importieren.</td>
</tr>
<tr>
<td>Filtern von Finzanzberichten (Management Reporter) auf Basis von Dimensionen, Attributen, Daten und Szenarien.</td>
<td> Die gesamte Filterung von Management Reporter-Berichten wird über das Design des Berichts gesteuert. Wenn ein Benutzer mit Betrachtungsrechten beispielsweise einen Bericht für ein anderes Datum anzeigen möchte, muss ein Berichtsdesigner die Änderung vornehmen.</td>
<td>Berichtsoptionen wurden hinzugefügt, damit unterschiedliche Filter angewendet werden können, wenn ein Benutzer einen Bericht anzeigt. Ein neuer Bericht wird anschließend auf Basis dieser Filter generiert.</td>
<td>Kunden mit Finanzberichten können verschiedene Filterdimensionen, Daten, Attribute und Szenarien anwenden, ohne, dass Aktualisierungen für die Berichtsentwürfe erforderlich sind.</td>
</tr>
<tr>
<td>Anzeigen von Finanzberichten (Management Reporter) innerhalb des Microsoft Dynamics AX-Clients.</td>
<td>Ein separater Webclient wurde verwendet, um Management Reporter-Berichte anzuzeigen.</td>
<td>Alle Finanzberichte können im Dynamics AX-Client angezeigt werden. Der Benutzer wählt einen Bericht aus und der Bericht wird im Client angezeigt.</td>
<td>Sie können nun Finanzberichte anzeigen, ohne auf einen anderen Client/eine andere Anwendung zugreifen zu müssen.</td>
</tr>
<tr>
<td>Drucken von Finanzberichten (Management Reporter) innerhalb des Microsoft Dynamics AX-Clients.</td>
<td>Das Drucken eines Berichts über die Druckoptionen des Browsers druckt nur das, was Benutzer auf dem Bildschirm sehen kann.</td>
<td>Benutzer können die Detailsstufe und Seiteneinrichtung eines Berichts über die Druckoption im Finanzbericht im Dynamics AX-Client nutzen.</td>
<td>Gedruckte Berichte sehen wie gewünscht aus.</td>
</tr><tr>
<td>Analysieren Sie Finanzdaten, indem Sie das Inhaltspack "Monitor financial performance" für Power BI verwenden.</td>
<td>Nicht verfügbar</td>
<td>Wählen Sie auf PowerBI.com <strong>Daten erhalten</strong> und dann das Inhaltspack <strong>Dynamics AX – Financial performance</strong>. Geben Sie die URL für Ihren Dynamics AX-Endpunkt ein, um die Daten im Dashboard anzuzeigen.</td>
<td>Mit drei bis vier Klicks können Organisationen ein Power BI-Dashboard bereitstellen, das wichtige Finanzdaten enthält. Der Inhalt kann durch die Organisation personalisiert werden.</td>
</tr>
<tr>
<td>Nachverfolgen Finanzperiodenabschlussprozessen.</td>
<td>Nicht verfügbar</td>
<td>Abschlussvorlagen und -zeitpläne können über die Finanzperiodenabschlusskonfiguration erstellt werden. Verwenden Sie den <strong>Finanzperiodenabschluß</strong> Arbeitsbereich, um den Status von Abschlusszeitplänen für mehrere Unternehmen zu verfolgen.</td>
<td>Dieser Arbeitsbereich macht manuelle Systeme zur Definition, Planung und Kommunikation von Abschlussaktivitäten überflüssig. Daher wird die Anzahl der für den Abschluss erforderlichen Tage verringert.</td>
</tr>
<tr>
<td>Überwachen des Budgets gegenüber den tatsächlichen Zahlen und erstellen von Sachkontoprognosen über den Arbeitsbereich <strong>Sachkontobudgets und Planungen</strong> und zusätzlichen Abfrageformularen.</td>
<td>Nicht verfügbar</td>
<td> Auf den Arbeitsbereich kann über das Dynamics AX-Dashboard zugegriffen werden. Es enthält Links zu mehreren neuen Abfrageseiten ein: <strong>Zusammenfassung des Budgets und der tatsächlichen Aktivitäten</strong>, <strong>Zusammenfassung der Budgetsteuerungs-Nachverfolgungsdaten</strong>, <strong>Budgeterfassungseinträge</strong> und <strong>Budgetpläne</strong>.</td>
<td>Neue Abfrageseiten ermöglichen den einfachen Zugriff auf die Budgetinformationen. Der Arbeitsbereich kombiniert alle Budgetwartungs- und -überwachungsaufgaben an einem Ort und kann von Budget-Managern oder Buchhaltungs-Managern leicht verwendet werden.</td>
</tr>
<tr>
<td>Erstellen von Layouts für Budgetpläne und Planungen.</td>
<td>Das <strong>Budgetplan</strong>-Dokument wird als Liste der Positionen angezeigt, die ein Gültigkeitsdatum und Beträge für Kombinationen von Finanzdimensionen haben. Der Benutzer muss Excel-Vorlagen erstellen und verwenden, um Budgetplandaten in einer Pivottabelle anzuzeigen.</td>
<td>Eine unbegrenzte Anzahl Layouts ist für Haushaltspläne und Planungen verfügbar. Sie können ausgewählte Finanzdimensionen, benutzerdefinierte Spalten und andere Zeilenattribute (wie Kommentare, Projekte und Anlagen) im Layout kombinieren. Benutzer können das Layout für das Budgetplandokument spontan wechseln und Daten bearbeiten, indem sie ein beliebiges Layout auswählen. Die Konfiguration der Budgetplanung wird vereinfacht, indem Szenarioeinschränkungen beseitigt und Layouts verwendet werden. Diese definieren, welche Daten in jeder Phase des Budgetplandokuments angezeigt und bearbeitet werden können.</td>
<td>Dies bietet die Möglichkeit, Budgetpläne Flexibilität zu erstellen und zu bearbeiten, indem Sie Excel und den Dynamics AX-Client verwenden. Vorlagen für Excel-Arbeitsmappen können generiert werden, indem die Budgetplan-Layouteinstellung verwendet werden.</td>
</tr>
<tr>
<td>Drucken Sie den Bericht <strong>Kreditorenrechnungsbuchungen</strong>, indem Sie Informationen aus dem Bericht <strong>Detaillierte Fälligkeitsdatenliste</strong> verwenden, der die überfälligen Tage umfasst.</td>
<td>Sie müssen zwei verschiedene Berichte drucken: <strong>Detaillierte Fälligkeitsdatenliste</strong> und <strong>Kreditorenrechnungsbuchungen</strong>.</td>
<td>Die Informationen in den beiden Berichten wurden zum Bericht <strong>Kreditorenrechnungsbuchungen</strong> konsolidiert. Bericht <strong>Detaillierte Fälligkeitsdatenliste</strong> ist veraltet.</td>
<td>Es diese Weise erübrigt es sich, zwei separate Berichte zu drucken.</td>
</tr>
<tr>
<td>Generieren von gesetzlich vorgeschriebenen Berichten direkt im PDF-Format.</td>
<td>Sie müssen erst einen gesetzlichen Bericht in einem Format generieren und diesen dann im PDF-Format exportieren.</td>
<td>Das PDF-Format ist das Standardformat für gesetzlich vorgeschriebene Berichte.</td>
<td>Der Bericht bietet eine einheitliche Anzeige auf dem Computerbildschirm und im Ausdruck.</td>
</tr>
<tr>
<td>Führen Sie den Mehrwertsteuerausgleichsprozess als Stapelverarbeitungsvorgang aus.</td>
<td>Nicht verfügbar</td>
<td>Auf der <strong>Mehrwertsteuer-Abrechnungszeitraum</strong>-Seite können Sie angeben, dass der Ausgleichsprozess im Stapelverarbeitungsmodus ausgeführt werden soll.</td>
<td>Für Perioden, die mehrere Steuerbuchungen haben, kann der Ausgleichsprozess zeitaufwendig sein, und es kann besser sein, den Prozess im Hintergrund als Stapelverarbeitung auszuführen.</td>
</tr>
</tbody>
</table>

## <a name="foundation"></a>Stiftungen

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Greifen Sie jederzeit und überall auf den Client zu.</td>
<td>Der AX 2012-Desktopclient bietet alle Formulare. Er kann jedoch nur auf Computer ausgeführt werden, die Microsoft Windows ausführen und muss installiert werden. Oft werden Terminalserver mit dem Desktopclient verwendet, um einen Zugriff über ein WAN zu ermöglichen. Der Enterprise Portal-Webclient stellt einen reduzierten Satz an Formularen bereit.</td>
<td>Die beiden AX 2012-Clients wurden durch einen einzigen, standardbasierten Webclient ersetzt, der alle Funktionen des Desktopclient über den Enterprise Portal-Client bereitstellt.</td>
<td>Dies vermeidet Entwicklungsaufwand durch zwei verschiedene Benutzeroberflächen. Mit einer Standardweboberflächen ist kein Terminalserver mehr erforderlich.</td>
</tr>
<tr>
<td>Mehr Produktivität mit der neuen Aufgabenaufzeichnung.</td>
<td>Die AX 2012-Aufgabenaufzeichnung erfordert direkten Zugriff auf einen AOS-Compuer (Application Object Server) und erweiterte Rechte. Er bietet keine Bearbeitungsoptionen.</td>
<td>Die neue Aufgabenaufzeichnung kann direkt aus dem Webclienten heraus verwendet werden. Der Zugriff auf die Aufgabenaufzeichnung erfordert keine Administratorrechte. Aufgezeichnete Schritte können bei der Aufzeichnung direkt angezeigt werden. Es wurden neue Bearbeitungsoptionen eingeführt. Die Aufgabenaufzeichnung unterstützt mehr Szenarien zusätzlich zu den vorhandenen Geschäftsprozessmodellierer-Szenarien.</td>
<td>Die neue Aufgabenaufzeichnung bietet eine vereinfachte Umgebung und neue Funktionen in Dynamics AX. Einige dieser Funktionen sind jetzt schon verfügbar. In der Zukunft folgen weitere.</td>
</tr>
<tr>
<td>Unterstützen Sie Benutzer dabei, die anstehenden Arbeiten und Arbeitsbereiche besser zu verstehen.</td>
<td>Rollencenter enthalten eine Übersicht mit Informationen zur Stellenfunktion eines Benutzers im Unternehmen bzw. in der Organisation.</td>
<td>Arbeitsbereiche sind ein neues Konzept in Dynamics AX, das Rollencenter als die primäre Möglichkeit zum Navigieren zu Aufgaben und bestimmte Seiten ersetzen sollen. Sie bieten eine einseitige Übersicht über eine Geschäftsaktivität und helfen Benutzern den aktuellen Status, die bevorstehende Auslastung und die Leistung des Prozesses oder Benutzers zu überblicken. Arbeitsbereiche sind präziser als AX 2012-Rollencenter und die Benutzer haben Zugriff auf mehrere Arbeitsbereiche.</td>
<td>Arbeitsbereiche sollen die Benutzerproduktivität erhöhen. Entwickler müssen einen Arbeitsbereichs für jede wichtige "Aktivität" im Produkt erstellen. Ältere Rollencenter aus AX 2012 werden in der Regel durch mehrere Arbeitsbereiche in der aktuellen Version von Dynamics AX ersetzt.</td>
</tr>
<tr>
<td>Formulare an der Browsergröße oder Gerätegröße ausrichten.</td>
<td>In AX 2012 waren Formularinhalt über Spalten in einem festen Layout definiert. Die Formularhöhe/-breite wurde weitgehend anhand der Steuerelemente auf dem Formular definiert.</td>
<td>Mit dem Wechsel zum Web im neuesten Dynamics AX basieren Formulardimensionen jetzt auf der Viewportgröße des Browsers oder Gerätes. Steuerelemente und Layoutparameter wurden geändert oder zur besseren Reaktion auf die Viewportgröße hinzugefügt.</td>
<td>Formularinhalte müssen responsiver sein, um die verfügbare Höhe/Breite des Browsers oder des Gerätes optimal zu nutzen. Dies erfordert möglicherweise Änderungen bei der Formularmodellierung.</td>
</tr>
<tr>
<td>Verwenden von Mustern für eine erweiterte Entwicklungsumgebung.</td>
<td>Formularvorlagen standen als Ausgangspunkt für die Entwicklung von Formularen in AX 2012 auf Basis einer Formatvorlage zur Verfügung. Der Form Style Checker ist ein optionales Add-in, das Informationen zur Abweichung des Formulars von der Vorlage enthält.</td>
<td>In der aktuellen Version von Dynamics AX werden Formularmuster eingeführt. Formularmuster sind Kombinationen aus Formularvorlagen und Form Style Checker, die eng in der Entwicklung einbezogen sind. Muster wurden auf Formularebene (wie in AX 2012) definiert. Es gibt nun auf Gruppen- und Registerkartenebene Untermuster.</td>
<td>Formulare, die mit Mustern arbeiten, haben viele Vorteile. Sie bieten beispielsweise eine konsistentere Benutzeroberfläche, eine einfachere Entwicklung, einfachere Upgrade Pfade und eine bessere Responsivität des Formularlayouts.</td>
</tr>
</tbody>
</table>

## <a name="help"></a>Hilfe

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Zugriff auf geführte Verfahrensweisen (Aufgabenleitfäden) und grundlegende Themen über <strong>Hilfe</strong>.</td>
<td>Das Hilfesystem von AX 2012 verweist auf HTML-Themen, die auf einem lokalen Webserver gespeichert werden. Kunden und Partner können ihre eigene Hilfe erstellen.</td>
<td>Das Hilfesystem in der aktuellen Version von Dynamics AX zeigt Aufgabenleitfäden an, die in Microsoft Dynamics Lifecycle Services (LCS) BPM gespeichert sind. Das Hilfesystem enthält auch Themen aus der Microsoft-Docs-Seite. Weitere Informationen finden Sie unter <a href="help-overview.md" data-raw-source="[Help system](help-overview.md)">Hilfesystem</a> und <a href="new-task-guides-available-february-2016.md" data-raw-source="[New task guides (February 2016)](new-task-guides-available-february-2016.md)">Neue Aufgabenleitfäden (Februar 2016)</a>.</td>
<td>Ein Aufgabenleitfaden ist eine kontrollierte, geführte, interaktive Erfahrung, die Sie durch die Schritte einer Aufgabe oder eines Geschäftsprozesses führt. Sie können die von Microsoft bereitgestellten Aufgabenleitfäden herunterladen und anpassen. Das Thema ermöglicht schnellere und flexiblere Möglichkeiten zur Erstellung, Bereitstellung und Aktualisierung der Produktdokumentation. So können wir besser sicherstellen, dass Zugriff auf den neuesten technischen Informationen enthalten.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Human Capital Management

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Übertragen von Fähigkeiten und Zertifikaten auf um Teilnehmer nach Kursabschluss.</td>
<td>Dies ist ein manueller Prozess.</td>
<td>Wenn ein Kurs abgeschlossen ist, wird eine neue Option verfügbar, um die Datensätze eines Teilnehmers mit den neuen Qualifikationen und den Zertifikaten zu aktualisieren.</td>
<td>Sie bietet eine neue und effiziente Möglichkeit, um Mitarbeiterdatensätze zu aktualisieren.</td>
</tr>
<tr>
<td>Beschäftigung schnell überprüfen.</td>
<td>Dies ist ein manueller Prozess.</td>
<td>Ihre Personalverwaltungsabteilung kann Beschäftigungen schnell überprüfen, indem sie einen Arbeitsbereich oder die Mitarbeiterseite verwendet.</td>
<td>Ihre Personalverwaltungsabteilung muss nicht mehr auf mehrere Seiten zugreifen, um das Startdatum, den Manager, die Monate in der Position und die Vergütungsdaten zu überprüfen.</td>
</tr>
<tr>
<td>Mitarbeiter können Informationen im System anzeigen, aktualisieren und löschen.</td>
<td>Die ist verfügbar, bietet jedoch begrenzten Anzeigen und Aktualisierungsfunktionen.</td>
<td>Diese Funktion ist aktiviert und ermöglicht Mitarbeitern und Auftragnehmern die Anzeige eine breiten Palette von Personendaten. Optional kann ein Workflow verwendet werden, wenn Informationen erstellt, aktualisiert oder gelöscht werden.</td>
<td>Ein Mitarbeiter kann seine Informationen kontrollieren. Dies gilt für die Aktualisierung von Adress- oder Kontaktinformationen, für Bewerbungen, für Umfragen und für die Aktualisierung des Bildes. Wenn ein Workflow aktiviert ist, können Informationen von einem Genehmiger geprüft werden, oder auf Basis Ihre Geschäftsprozesse automatisch genehmigt werden.</td>
</tr>
<tr>
<td>Manager können Mitarbeiterinformationen bearbeiten oder anzeigen.</td>
<td>Die ist verfügbar, bietet jedoch begrenzten Anzeigen und Aktualisierungsfunktionen.</td>
<td>Je nach Konfigurationseinstellungen und Sicherheit können Manager Mitarbeiterinformationen anzeigen oder bearbeiten.</td>
<td>Manager können auf wichtige Mitarbeiterdaten zugreifen, sodass sie eine bessere Entscheidungen zur Ressourcenplanung, Leistung und Mitarbeiterentwicklung treffen können.</td>
</tr>
<tr>
<td>Nutzen Sie die Manager-Self-service-Funktionen.</td>
<td>Nicht verfügbar</td>
<td>Manager können nun Anforderungen für die Einstellung, Übertragung und Beendigung von neue Arbeitsverhältnissen (Mitarbeiter und Auftragnehmer) einreichen. Manager können außerdem eine neue Position anfordern, die Dauer einer Positionen verlängern oder die Anforderung ändern.</td>
<td>Diese Szenarien standen zuvor nur für die Personalverwaltung zur Verfügung. Diese Szenarien bietet leistungsstarke Tools für Manager in einer Organisation. Optionale Workflows können zu angemessenen Prüfung und Genehmigung aktiviert werden.</td>
</tr>
<tr>
<td>Zugriff auf die Ergebnisse der Vergütungsverarbeitung.</td>
<td>Ergebnisse sind nur zum Zeitpunkt der Verarbeitung verfügbar.</td>
<td>Auf die Ergebnisse der Vergütungsverarbeitung kann nun jederzeit zugegriffen werden, nachdem der Prozess ausgeführt wurde.</td>
<td>Sie ermöglichen eine ausgezeichnete Überwachung des Prozesses und das Ergebnisse des Prozesses. Sie bietet auch eine umfangreiche Ansicht der Daten, bevor Mitarbeiterdatensätze aktualisiert werden.</td>
</tr>
<tr>
<td>Zugriff auf die Ergebnisse der Vorteilsverarbeitung.</td>
<td>Ergebnisse sind nur zum Zeitpunkt der Verarbeitung verfügbar.</td>
<td>Auf die Ergebnisse der Vorteilsverarbeitung kann nun jederzeit zugegriffen werden, nachdem der Prozess ausgeführt wurde.</td>
<td>Er enthält eine umfangreiche Ansicht der Daten, die von Vorteilsregistrierungen und Kostenänderungen aktualisiert werden.</td>
</tr>
<tr>
<td>Anzeigen von "Gültigkeitsdatum"-Zeitachsenänderungen.</td>
<td>Nicht verfügbar</td>
<td>Dieses Vergleichstool ist für Mitarbeiter, Positionen und Einzelvorgänge verfügbar. Es bietet eine umfangreiche Ansicht von Änderungen von einer Version eines Datensatzes zu einer anderen.</td>
<td>Es spart Ihnen Zeit, wenn Sie Änderungen anzeigen, die im Laufe der Zeit für den Mitarbeiter, den Positionen und zu den Einzelvorgangsdatensätzen aufgetreten sind. Es ermöglicht Ihnen den schnellen Vergleich von zwei Versionen eines Datensatzes oder aller Datensätze.</td>
</tr>
<tr>
<td>Anzeigen von Mitarbeiter nach Unternehmen.</td>
<td>Dies ist ein manuellen Prozess, der über Filter ausgeführt wird.</td>
<td>Mitarbeiter- und Auftragnehmerlisten werden automatisch nach den Unternehmen gefiltert, bei dem Sie angemeldet sind.</td>
<td>Sie finden hier eine gefilterte Ansicht von Mitarbeitern, die im angemeldeten Unternehmen beschäftigt sind. Eine ungefilterte Ansicht aller Mitarbeiter und Auftragnehmer, ist weiterhin in der Arbeitskräfteliste verfügbar. In der aktuellen Version von Dynamics AX, ändert das System das Unternehmen nicht basierend auf dem Mitarbeiter, der in der Liste ausgewählt ist.</td>
</tr>
<tr>
<td>Aktualisieren der Kursteilnehmerliste.</td>
<td>Nicht verfügbar</td>
<td>Kursteilnehmer können aus der Teilnehmerliste entfernt werden.</td>
<td>Es bietet eine einfache Möglichkeit, Kursteilnehmer zu aktualisieren, die versehentlich erfasst wurden.</td>
</tr>
<tr>
<td>Vergütungsereignisse in einer Gruppe verwalten.</td>
<td>Nicht verfügbar</td>
<td>Diese Funktion rationalisiert die Verarbeitung von Vergütungsänderungen für Mitarbeiter.</td>
<td>Sie enthält einen einfachen, fortschrittlichen Prozess zum Aktualisieren von Mitarbeiterdatensätzen über den Vergütungsarbeitsbereich und die zugehörigen Seiten.</td>
</tr>
</tbody>
</table>

## <a name="inventory-management"></a>Lagerverwaltung

Es wurden keine neuen Funktionen hinzugefügt.

## <a name="localization"></a>Lokalisierung

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Konfigurieren und Generieren von elektronischen Dokumenten, um die gesetzlichen Anforderungen in zahlreichen Ländern/Regionen zu erfüllen.</td>
<td>Elektronische Dokumente werden in X++ oder als Extensible Stylesheet Language Transformations (XSLT) fest codiert. Alle Formatanpassungen erfordern Entwicklungsaufwand. Der Zugriff auf die Daten und Formatierung sind nicht isoliert. Eine angepasste Formatbereitstellung erfordert ein neues Microsoft Dynamics AX-Hotfixpaket, das das vorhandene Format überschreibt. Benutzerdefinierte Änderungen jedes Formats müssen manuell auf den Quellcode eines neuen Microsoft Dynamics AX-Hotfixpakets übertragen werden.</td>
<td>Die elektronische Berichterstellung (Electronic Reporting, EB) ist ein neues Tool zum Konfigurieren und Generieren elektronischer Dokumente, das sich an geschäftlichen Benutzer statt an Entwickler wendet. Mit ER können Sie Datenmodelle einrichten, die domänenspezifisch und unabhängig von der Microsoft Dynamics AX-Datenbank als Datenquellen für Dokumentformate sind. Ein geschäftlicher Benutzer kann die Formate auf Grundlage dieser domänenspezifischen Datenmodelle konfigurieren (beispielsweise für Zahlungen, Intrastat-Berichte oder Steuererklärungen). Der Benutzer konfigurierten die Formate, indem er einfache visuelle Tools verwendet, die Excel ähneln. ER unterstützt derzeit die Generierung elektronischer Dokumente im Text-, XML- und Excel-Format. Diese Dokumente können gleichzeitig generiert und in ZIP-Dateien gepackt werden. Datenmodelle und Stile unterstützen die Verwaltung. Formatversionen können Gültigkeitszeiträume haben. Jede Datenmodell- oder Formatversion wird in einer separaten Konfiguration gespeichert und an die Partner und Kunden über LCS verteilt. Partner und Kunden können Microsoft-Datenmodelle und Formate anpassen, oder ihre eigenen erstellen. ER erspart Partnern und Kunden Konfigurationsänderungen bei Abweichungen zu den Microsoft-Konfigurationen. Dies vereinfacht die Aktualisierung auf neue Versionen von Microsoft-Konfigurationen. Über LCS können Partner ihre Datenmodell- und Formatkonfigurationen mit anderen Partnern und Kunden teilen. Diese können sie genauer anpassen und gemeinsam verwenden. Deltaanpassung und einfaches Upgrade für die gesamte Anpassungskette.</td>
<td>ER vereinfacht die Erstellung, die Verwaltung und die Aktualisierung des elektronischen Dokumentformats, um rechtliche Anforderungen in zahlreichen Ländern/Regionen zu erfüllen. ER gestaltet den Prozess der Erstellung oder Änderung von elektronischen Dokumentformaten schneller und einfacher. Diese Änderungen können von den geschäftlichen Benutzern anstelle von Entwickler vorgenommen werden. ER macht es für die Partnern und die Kunden schneller und einfacher, ihre Formatanpassungen auf neue Versionen von Formaten, die von Microsoft oder Partnern freigegeben werden, zu aktualisieren ER bietet Microsoft und Partnern eine übergreifende Möglichkeit (über LCS) zur Verteilung von Konfigurationen für elektronische Dokumente an andere Partner und an Kunden. ER macht es Partnern und Kunden leichter, elektronische Dokumentformate für ihre speziellen geschäftlichen Anforderungen anzupassen, zu aktualisieren und zu verteilen.</td>
</tr>
<tr>
<td>(MEX) Erstellen von gesetzlich vorgeschriebenen mexikanisches Mehrwertsteuerberichten.</td>
<td>Sie müssen <strong>Verkäufe und Einkäufe MwSt.</strong>-Berichte generieren, indem Sie die Funktionalität für nicht realisierte Mehrwertsteuer nutzen. So können Benutzer Buchungen zu den realisierten und nicht realisierten Abschnitten anhand des Status erkennen.</td>
<td><strong>Verkäufe und Einkäufe MwSt.</strong>-Berichte wurden geändert und berücksichtigen jetzt die Funktion "Mehrwertsteuer nach vereinnahmten Geldern" nur für bestimmte Ausgleichsperioden für die Definition nicht realisierter und realisierte Mehrwertsteuercodes.</td>
<td>Änderungen in der Konfiguration von Mehrwertsteuercodes sind erforderlich, damit Benutzer diese Berichte ordnungsgemäß generieren können. Eine Funktion "Mehrwertsteuer nach vereinnahmten Geldern" ist erforderlich, und der Benutzer muss separate Ausgleichsperioden konfigurieren (unrealisiert und realisiert), um die Buchungen in den zugehörigen Abschnittsbereichen zu identifizieren.</td>
</tr>
<tr>
<td>(JPN) Verwalten des japanischen Erklärungsdokumentes für Anlagen mit Sonderabschreibungen.</td>
<td>Nicht verfügbar</td>
<td>Wichtige Erklärungsinformationen werden zur besseren Wartung zentral in einem einzelnen Dokument gespeichert.</td>
<td>Die Dokumentenkompatibilität und die Vereinfachung der Verwaltung reduzieren Probleme bei Prüfungen.</td>
</tr>
<tr>
<td>(JPN) Prüfen von JBA-Zeichen für das Bankkonto.</td>
<td>Nicht verfügbar</td>
<td>Sie können überprüfen, ob Kana-Namensfelder nur die Zeichen enthalten, die über das JBA-Bankformat zulässig sind.</td>
<td>Dies verringert die Unterbrechungen für Benutzer während der Generierung der Zahlungsdatei aufgrund unzulässiger Zeichen.</td>
</tr>
<tr>
<td>(JPN) Ausgleich der japanischen Centdifferenz für Anlagen am Ende des Geschäftsjahrs.</td>
<td>Nicht verfügbar</td>
<td>Auf der <strong>Anlagevermögenparameter</strong>-Seite können Sie festlegen, dass am Ende des Finanzzeitraums oder Geschäftsjahrs ausgeglichen wird.</td>
<td>Dies bietet mehr Flexibilität um lokalen Verfahren zu entsprechen.</td>
</tr>
<tr>
<td>(JPN) Generieren der japanischen Serie 16-Anhangtabellen für die Unternehmenssteuererklärung bei einem zusammengefassten Betrag für Anlagenhaupttypen.</td>
<td>Nicht verfügbar</td>
<td>Über die Wertmodellen einer Anlage können Sie die Zusammenfassung nach Haupttyp auswählen. Standardmäßig werden diese Funktionen für neu erstellte Anlagen verwendet.</td>
<td>Für große Unternehmen, die tausenden Anlagen haben, reduzieren die zusammengefassten Berichte die Größe des generierten Berichts erheblich.</td>
</tr>
<tr>
<td>(JPN) Start der Zuteilung einer speziellen Abschreibungsreserve vom nächsten Geschäftsjahr für Anlagen in Japan.</td>
<td>Nicht verfügbar</td>
<td>In den Wertmodellen einer Anlage, die ein geeignetes außerordentliches Abschreibungsprofil besitzt, können Sie festlegen, dass Zuteilung ab dem nächsten Finanzzeitraum oder dem nächsten Geschäftsjahr beginnt.</td>
<td>Dies bietet mehr Flexibilität um lokalen Verfahren zu entsprechen.</td>
</tr>
<tr>
<td>(JPN) Generieren eines japanischen Verbrauchssteuerberichtes, der die überarbeiteten Steuersätze umfasst.</td>
<td>Der Verbrauchssteuerbericht ist für ein Steuersatz von 5 Prozent verfügbar.</td>
<td>Der Verbrauchssteuerbericht enthält einen Abschnitt für den überarbeiteten Steuersatz (beispielsweise 8 Prozent).</td>
<td>Das Layout wurde neu von der Behörde angekündigt.</td>
</tr>
<tr>
<td>(EU) Konfigurieren von Rundungseinstellungen für die zusammenfassende Meldung.</td>
<td>Rundungseinstellungen für die zusammenfassende Meldung für verschiedene Länder/Regionen sind in X++ oder in XSLTs (Extensible Stylesheet Language Transformations) fest eingetragen.</td>
<td>Für Außenhandelsparameter wurden Rundungseinstellungen hinzugefügt. Sie können die Rundungsgenauigkeit, das Rundungsverfahren, die Genauigkeit der Ausgabe und das Verhalten für Beträge unterhalb der Rundungsgenauigkeit konfigurieren.</td>
<td>Die vereinheitlicht und vereinfacht die Konfiguration von der zusammenfassenden Meldungen für die EU. Anpassung der Rundungseinstellungen erfordert keine Entwicklungsaktivitäten mehr.</td>
</tr>
<tr>
<td>(EU) Konfigurieren von Steuerschuldumkehr-Anwendbarkeitsregeln.</td>
<td>Steuerschuldumkehr-Anwendbarkeitsregeln sind für das inländische Steuerschuldumkehr-Szenario fest eingetragen. Der Anwendbarkeitsschwellenwert kann pro Artikelgruppe eingerichtet werden. Diese Funktionalität steht nur in Großbritannien zur Verfügung.</td>
<td>Sie können Steuerschuldumkehr-Anwendbarkeitsregeln pro Dokumenttyp (Einkauf/Verkauf, Kreditorenrechnung, Freitextrechung etc.) und eine Steuerschuldumkehrgruppe mit Artikeln, Artikelgruppen und Einkauf/Verkauf-Kategorien konfigurieren. Die Anwendbarkeitsregeln haben ein Gültigkeitsdatum. Sie können auch einzelnen Mehrwertsteuercodes in Mehrwertsteuergruppen für die Steuerschuldumkehr markieren. Der Verkaufsrechnungserfassungsbericht wurde mit Details zur angewendeten Steuerschuldumkehr angepasst. Die Funktionalität ist für alle europäischen Länder/Regionen verfügbar.</td>
<td>Diese Änderung vereinheitlicht die Konfiguration der Steuerschuldumkehr-Anwendbarkeitsregeln und unterstützt die Anwendung von innerstaatlichen Steuerschuldumkehrrichtlinien in europäischen Ländern.</td>
</tr>
<tr>
<td>(DE) Generierung der deutschen Protokolldatei (GDPdUGoBD)</td>
<td>Benutzer können Definition der Tabellen mit Finanzdaten einrichten, die in einem von den deutschen Prüfern und Behörden anerkannten Format exportiert werden.</td>
<td>Die Funktion ist als elektronische Berichterstellungskonfiguration implementiert wurden. Die Funktionalität steht in Deutschland und Österreich zur Verfügung.</td>
<td>Diese Änderung bietet dem Benutzer viel mehr Möglichkeiten zum Formatieren von Daten und für Transformationen. Sie bietet alle Vorteile von elektronischen Reporting-Konfiguration (z. B. der einfache Konfigurationsaustausch, die Versionierung usw.).</td>
</tr>
<tr>
<td>(FR) Bericht "Summen- und Saldenliste mit Gruppensummenkonten"</td>
<td>Saldenliste mit Gruppensummenkonten ist als SSRS-Bericht (LedgerAccountSum_FR) implementiert.</td>
<td>Saldenliste mit Gruppensummenkontenbericht ist als Management Reporter Bericht implementiert (verfügbar im Ordner mit den lokalisierten LCS Asset-Bibliothek-Finanzberichten).</td>
<td>Dadurch können Benutzer alle Vorteile und Freiheiten bei der Anpassungen von Finanzberichten in Management Reporter nutzen.</td>
</tr>
<tr>
<td>(EU) Zahlungsavis, Begleitzettel und Kontrollbericht für Zahlungen.</td>
<td>Diese Berichte und SSRS-Berichte werden implementiert.</td>
<td>Diese Berichte wurden als Open XML-Vorlagen für die Verwendung in Microsoft Excel implementiert.</td>
<td>Elektronische Zahlungskonfigurationen enthalten Zahlungsdateiformateinrichtungen und -vorlagen. Dadurch können Benutzer alle Vorteile und Freiheiten bei der Anpassungen von Berichten aus der elektronische Berichterstellung nutzen.</td>
</tr>
<tr>
<td>(EU) Konfigurieren von Rundungseinstellungen für Intrastat.</td>
<td>Rundungseinstellungen für die Intrastat-Berichterstellung für verschiedene Länder/Regionen sind in X++ oder in XSLTs (Extensible Stylesheet Language Transformations) fest eingetragen.</td>
<td>Für Außenhandelsparameter wurden Rundungseinstellungen hinzugefügt. Sie können die Rundungsgenauigkeit, das Rundungsverfahren, die Genauigkeit der Ausgabe und das Verhalten für Beträge unterhalb der Rundungsgenauigkeit konfigurieren.</td>
<td>Die vereinheitlicht und vereinfacht die Konfiguration der Intrastat-Berichterstellung. Anpassung der Rundungseinstellungen erfordert keine Entwicklungsaktivitäten mehr.</td>
</tr>
<tr>
<td>(EU) Einrichten von Intrastat-Warencodes in Kategoriehierarchien.</td>
u<td>Intrastat-Warencodes ist eine separate Liste. Zwar gibt es eine Kategoriehierarchie vom Typ Warencode, doch diese Warencodes können in den Kategorien "Retail HQent" und "Vertrieb" übernommen werden.</td>
<td>Separate Liste mit Intrastat-Warencodes ist mit der Produkthierarchie von Typ Warencode zusammengeführt worden.</td>
<td>Dies vereinheitlicht den Ansatz zum Zuweisen von Warencodes an veröffentlichte Produkte und Kategorien in Verkaufs- und Einkaufsbelegen.</td>
</tr>
<tr>
<td>(EU) Mengen in zusätzlichen Maßeinheiten für Intrastat über Einheitkonvertierungseinstellungen berichten.</td>
<td>Intrastat-Warencodes hat ein Textfeld für zusätzliche Einheiten. Die <strong>Produkt</strong>-karte hat ein Feld für die Menge der zusätzlichen Einheiten in Kilogramm.</td>
<td>Zusätzliche Einheiten für Intrastat Warencodes werden aus der Einheitenliste ausgewählt. Die Menge der zusätzlichen Einheiten wird über die Konvertierungseinstellungen berechnet.</td>
<td>Dies vereinheitlicht den Ansatz zur erneuten Berechnung von Buchung für weitere Einheiten.</td>
</tr>
<tr>
<td>(EU) Zuweisen einer standardmäßigen Intrastat-Transportmethode für die Lieferung.</td>
<td>Nicht verfügbar</td>
<td>Ein Feld für den standardmäßigen Transport wurde zur Lieferart hinzugefügt.</td>
<td>Dies vereinfacht die Vorbereitung der Intrastat-Berichte.</td>
</tr>
<tr>
<td>(EU) Markieren veröffentlichter Produkt, um die Aufführung in Intrastat-Berichten zu verhindern.</td>
<td>Nicht verfügbar</td>
<td>Eine Option zur Ausnahme eines Artikels aus der Intrastat-Berichtserstellung wurde zum veröffentlichten Produkt hinzugefügt.</td>
<td>Dies vereinfacht die Vorbereitung der Intrastat-Berichte.</td>
</tr>
</tbody>
</table>

## <a name="manufacturing"></a>Fertigung

| Wie können Sie vorgehen? | Dynamics AX 2012 |
|------------------|------------------|
| Führen Sie eine Prüfung der Materialverfügbarkeit für Produktionsaufträge auf einer separaten Seite aus, die vom Arbeitsbereich **Produktionsverwaltung** geöffnet wird. | Nicht verfügbar |
| Starten und Anzeigen der Fortschritts von Produktionseinzelvorgängen, indem Sie die neue Seite **Einzelvorgangslistengerät** verwenden. | Das **Einzelvorgangserfassung**-Formular ist vorrangig für große Terminalbildschirme gedacht und die Benutzeroberfläche wird in der Regel über Mausklicks verwendet. |

## <a name="master-planning-and-forecasting"></a>Produktprogrammplanung und Bedarfsplanung

| Wie können Sie vorgehen? | Dynamics AX 2012 | Dynamics AX 7.0 | Warum ist dieses wichtig? |
|------------------|------------------|-----------------|------------------------|
| Warnen des Benutzers, wenn ein Auftrag oder Produktionsauftrag nicht zur Lieferung bis zum eingeplanten Datum bereit ist. | Die Warnungen, die von der Produktprogrammplanung erstellt werden, werden als *Verfügbarkeitsmeldungen* bezeichnet. Eine *Verfügbarkeit* ist ein Vertrag zwischen zwei Parteien, eine Anlage für einen Preis zu kaufen oder zu verkaufen, der heute vereinbart wird (der *Verfügbarkeitspreis*), obwohl Lieferung und Zahlung zu einem späteren Zeitpunkt stattfinden (das *Lieferdatum*). | *Verfügbarkeitsmeldungen* und *Verfügbarkeitsdaten* wurden in *berechnete Verzögerungen* und *verzögerte Datumsangaben*, umbenannt. | Die Terminologie, die in AX 2012 verwendet wird, war ungenau und führte zu falschen Übersetzungen. |
| Sorgen Sie für schnellen Einblick in den Status eines Produktprogrammplanungslaufs, in dringenden Bestellvorschläge und in Bestellvorschläge, die Verzögerungen verursachen. | Die Information ist verfügbar, aber sie ist auf mehrere Formulare verteilt. | Der **Produktprogrammplanung**-Arbeitsbereich bietet auf einen Blick Informationen darüber, wann der letzte Produktprogrammplanungslauf abgeschlossen wurde, ob dabei Fehler aufgetreten sind, wie die dringenden Bestellvorschläge aussehen und welche Bestellvorschläge Verzögerungen verursachen. | Sie profitieren von dem Überblick, den der Arbeitsbereich bereitstellt. Relevante Information werden zusammengeführt und verbessern die Produktprogrammplanung und steigern die Produktivität. |
| Verwendung von Excel zur Aktualisierung von Bedarfsplanungen. | Nicht verfügbar | Sie können die nahtlose Integration mit Excel nutzen, wenn Sie Bedarfsplanungen eingeben, Aktualisierungen durchführen und Bedarfsplanungen löschen. | So steigern Sie die Leistungsfähigkeit und Produktivität. |
| Die Möglichkeit den zukünftigen Bedarf zu schätzen und Bedarfsplanungen basierend auf früheren Buchungsdaten zu erstellen. | In Microsoft Dynamics AX 2012 R3, werden die in Planungsmodelle aus Microsoft SQL Server Analysis Service verwendeten, um Bedarfsplanungsvorhersagen zu erstellen. | Kalkulieren Sie den zukünftigen Bedarf mithilfe der Leistung und der Erweiterbarkeit eines Microsoft Azure Machine Learning-Clouddienstes. Er ist bedienungsfreundlich und erweitert die Planzahlenmodelle in Machine Learning für die Kundenanforderungen. Die Dienst führt eine bestmögliche Modellauswahl durch und bietet Key Performance Indicators (KPIs) an. Mit diesen kann die Prognosegenauigkeit berechnet werden. | Generieren Sie genauere Planungen mit den Machine Learning-Techniken. |
| Optimierung von Auftragsdatum und die Menge basierend auf einer visuellen Übersicht der zusammenhängender Aktivitäten aus dem Produktprogrammplanungslauf. | Der Diagramm zum Überblick der Aktivitäten ist nur verfügbar. Es zeigt alle zugehörigen Aktivitäten. Falls Aktivitäten angewendet werden, werden sie sofort von der Ansicht entfernt. | Das Aktionsdiagramm bietet einen besseren Überblick. Es schließt Optionen ein, mit denen Sie nur angewandte Aktivitäten und direkt zugeordnete Aktivitäten anzeigen können. Falls Aktivitäten angewendet werden, werden sie abgeblendet angezeigt. Daher wird der Überblick erhalten. Zusätzliche Informationen werden dem Funktionsdiagramm hinzugefügt, um die Daten auf einer Seite anzuzeigen. | Sie profitieren von Produktivitätsverbesserung, da Sie sich nur auf die relevanten Aktivitäten konzentrieren können. |

## <a name="procurement-and-sourcing"></a>Beschaffung

| Wie können Sie vorgehen? | Dynamics AX 2012 | Dynamics AX 7.0 | Warum ist dieses wichtig? |
|------------------|------------------|-----------------|------------------------|
| Verwenden Sie den **Bestellungsvorbereitung**-Arbeitsbereich, um einen schnellen Einblick in den Status von Bestellungen zu erhalten, die vorbereitet werden. | Nicht unterstützt | Der **Bestellungsvorbereitung**-Arbeitsbereich bietet einen Überblick der Aufträge vom Zeitpunkt der Erstellung als Entwurf über den Workflowgenehmigungsstatus bis zur Bestätigung. | Ihre Einkaufsabteilung muss nicht mehr Informationen aus mehreren Seiten suchen. Sie profitiert von dem Überblick, den der Arbeitsbereich bereitstellt. |
| Verwenden Sie den **Bestellungszugang und Weiterverfolgung**-Arbeitsbereich, um schnellen Einblick in Bestellungen zu erhalten, die gerade im Zugang sind. | Nicht unterstützt | Der **Bestellungszugang und Weiterverfolgung**-Arbeitsbereich bietet einen Überblick über bestätigten Bestellungen, die Zugänge oder Lieferungen aufweisen. Der Arbeitsbereich umfasst Listen von Buchen-Bis-Zugängen und ausstehenden Zugängen, um beim proaktiven Prüfung und bei der Nachverfolgung durch den Lieferanten weiterzuhelfen. Der Arbeitsbereich listet auch Bestellungen auf, bei denen die Eingangsregistrierung am Lagerort ausgeführt wurde, um sicherzustellen, dass der Zugang gebucht wird. Bestellungsrücksendung, die noch nicht geliefert wurden, sind auch zur Prüfung verfügbar. | Ihre Einkaufsabteilung profitiert von dem Überblick, den der Arbeitsbereich bereitstellt. Relevante Information werden zusammengeführt und verbessern die Weiterverfolgung und steigern die Produktivität. |
| Senden Sie Bestellungen zur Bestätigung an ein Kreditorenportal , das im Dynamics AX-Client gehostet wird. Lassen Sie den Kreditor bestätigen oder ablehnen. | Nicht unterstützt | Die Kreditorenportalbenutzeroberfläche ermöglicht Kreditoren Bestellungen als empfangen oder abgelehnt zu erhalten. Ist ermöglicht dem Kreditor außerdem eine Übersicht über alle bestätigten Bestellungen für ein Konto. Der Einkaufsvertreter kann Bestellung übermitteln und eine Bestätigung vom Kreditor anfordern. Der Kreditor muss ein registrierter Microsoft Azure Active Directory (Azure AD)-Benutzer in Dynamics AX und eine Kontaktperson für den Kreditor sein und eine dedizierte Sicherheitsrolle haben. | Ihre Einkaufsabteilung profitiert von weniger Belegen und Aufwand zur manuellen Nachverfolgung von Bestellungen. Eine zentrale Information verringert Missverständnisse zwischen Debitor und Kreditor. |

## <a name="projects"></a>Projekte

| Wie können Sie vorgehen? | Dynamics AX 2012 | Dynamics AX 7.0 | Warum ist dieses wichtig? |
|------------------|------------------|-----------------|------------------------|
| Buchen Sie Arbeitskräfte als Ressourcen für Projekte. | Ähnlich Ressourcen, werden Arbeitskräfte zusätzlich zu den Ressourcen direkt für Projekte gebucht. | Die Ressourcentabelle, in der Ressourcen für die Fertigung und Produktion gespeichert werden, kann nun verwendet werden, um Arbeitskräfte als Ressourcen für ein Projekt zu reservieren. | Wenn Sie Projekte buchen, müssen Sie nur Ressourcen buchen. |

## <a name="retail-sales-marketing-and-customer-service"></a>Einzelhandelsverkauf, Marketing und Kundendienst

### <a name="retail-hq"></a>Retail HQ

Ein über Microsoft Azure gehostetes Retail HQ bietet eine zentralisierte Verwaltung und Übersicht aller Aspekte von Commerce-Abläufen über einen Webclient.

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Durchführen von Verkaufsförderungsvorgängen.</td>
<td>Benutzer müssen auf mehrere Formulare zugreifen, um diese Daten zu verwalten:
<ul>
<li>Kategorienverwaltung</li>
<li>Produktverwaltung</li>
<li>Kanalspezifische Produktattribute</li>
<li>Sortimente</li>
<li>Katalogverwaltung</li>
<li>Bausätze</li>
<li>Preise und Rabatte</li>
</ul></td>
<td>Der <strong>Kategorie- und Produktverwaltung</strong>-Arbeitsbereich ermöglicht die folgenden Funktionen:
<ul>
<li>Sortimentsverwaltung.</li>
<li>Sortimentslebenszyklusnachverfolgung.</li>
<li>Verwalten von freigegebenen Produkten.</li>
</ul>
Der <strong>Produktpreise und -rabatte</strong>-Arbeitsbereich ermöglicht die folgenden Funktionen:
<ul>
<li>Verwalten von Preisen und Rabatten für einen angegebenen Kanal und eine Kategorie.</li>
<li>Verwalten von Kategoriepreisregeln.</li>
<li>Preis- und Rabattprioritäten, über die Sie Prioritäten zu Preisgruppen und den Rabatten zuweisen können, damit Sie die Reihenfolge steuern können, in der sie angewendet werden.</li>
<li>Zugehörigkeits- und Katalograbattverwaltung.</li>
</ul>
Der <strong>Katalogverwaltung</strong>-Arbeitsbereich ermöglicht die folgenden Funktionen:
<ul>
<li>Zusammenfassung der aktiven Kataloge.</li>
<li>Kataloglebenszyklusnachverfolgung an einem Ort.</li>
</ul></td>
<td><ul>
<li>Arbeitsbereiche verbessern die Effizienz und Produktivität der Arbeitskräfte, indem sie Aufgaben und Aktivitäten ihrer Verkaufsrolle zentral durchführen können.</li>
<li>Die Preis- und Rabattprioritätsfunktion gibt Debitoren mehrere Kontrolle darüber, wie Preise und Rabatte verwendet werden. Die Funktion ermöglicht neue Szenarien, in denen höhere Ladenpreise Einheitspreisen vorgezogen werden.</li>
</ul></td>
</tr>
<tr>
<td>Verwalten von Einzelhandelskanalbereitstellungen und -vorgängen.</td>
<td>Der Benutzer muss auf mehrere Formulare zugreifen, um die folgenden Aufgaben auszuführen:
<ul>
<li>Erstellen und Konfigurieren neuer Kanäle und verbundener Entitäten.</li>
<li>Verwalten der täglichen Shopaktionen.</li>
<li>Verarbeiten Sie Einzelhandelstransaktionen in Microsoft Dynamics AX, erstellen Sie Einzelhandelsabrechnungen und aktualisieren Sie Microsoft Dynamics AX Bestände und Finanzkennzahlen.</li>
</ul>
</td>
<td>Der <strong>Kanalbereitstellung</strong>-Arbeitsbereich ermöglicht die folgenden Aufgaben:
<ul>
<li>Erstellen neuer Kanäle und verbundener Entitäten.</li>
<li>Nachverfolgen des Status der Ladengeschäftkonfiguration.</li>
<li>Durchführen der erforderlichen Schritte, um eine Aufgabe abzuschließen, oder Bereitstellen von Informationen, um die Aufgabe abzuschließen.</li>
<li>Nachverfolgen des Status von Geräten und direktes Validieren und Herunterladen der Retail Modern POS (MPOS)-Programminstallation in den Filialen.</li>
<li>Zugreifen auf alle zugehörigen Seiten.</li>
</ul>Der 
<strong>Einzelhandelsshopleitung</strong>-Arbeitsbereich ermöglicht die folgenden Aufgaben:
<ul>
<li>Verwalten von Arbeitskräften und der POS-Berechtigungen der Arbeitskräfte.</li>
<li>Nachverfolgen des Schichtstatus für einen bestimmte Shopgruppe oder einen Shop.</li>
<li>Direkt Validieren und Herunterladen der MPOS-Programminstallation in den Filialen.</li>
<li>Drucken von Berichten und der Zugriff die entsprechenden Seiten.</li>
</ul>Der Finanzdaten für den 
<strong>Einzelhandelsshop</strong>-Arbeitsbereich ermöglicht die folgenden Aufgaben:
<ul>
<li>Erstellen, Kalkulieren und Buchen von Aufstellungen für einen bestimmten Kanal.</li>
<li>Planen von Stapelverarbeitungsaufträgen zur Aktualisierung des Lagers und zur Kalkulation und Buchung von Aufstellungen.</li>
<li>Nachverfolgung offener Aufstellungen.</li>
<li>Nachverfolgen des Schichtstatus für einen bestimmte Shopgruppe oder einen Shop.</li>
<li>Drucken von Berichten und schneller Zugriff auf die entsprechenden Seiten.</li>
</ul></td>
<td>Arbeitsbereiche verbessern die Effizienz und Produktivität der Arbeitskräfte, indem sie die misten Aufgaben und Aktivitäten der Kanalbereitstellung, Shopverwaltung und Finanzverwaltung zentral durchführen können.</td>
</tr>
<tr>
<td>Verwalten des IT-Betriebs im Einzelhandel</td>
<td>Der Benutzer muss auf mehrere Formulare zugreifen.</td>
<td>Der <strong>Retail IT</strong> Arbeitsbereich ermöglicht Commerce Data Exchange-Abfragen an einem einzigen Ort für einen angegebenen Kanal. So können Sie die folgenden Aufgaben ausführen:
<ul>
<li>Downloadsitzungen.</li>
<li>Uploadsitzungen.</li>
<li>Nachverfolgen von fehlerhaften Sitzungen und Fortführen oder neu Starten.</li>
<li>Anzeigen oder Ausführen von kommenden Einzelvorgängen.</li>
</ul></td>
<td>Arbeitsbereiche verbessern die Effizienz und Produktivität der Arbeitskräfte, indem sie Aufgaben und Aktivitäten des IT-Betriebs im Einzelhandel.</td>
</tr>
<tr>
<td>Import-/Exportieren von Daten nach Datenentitäten.</td>
<td>AX 2012 unterstützt standardmäßig die Microsoft Dynamics Retail Management System (RMS) -Migration über das Data Import/Export Framework.</td>
<td>Einzelhandeltsdatenentitäten wurden erweitert, alle Master- und Referenzdaten zu unterstützen, die zum Einzelhandel gehören. Es gibt außerdem eine erweiterte Unterstützung für Datenentitäten in der gesamten Dynamics AX-Lösung.</td>
<td>Datenentitäten ermöglichen Kunden das Metadatum-gesteuerte Importieren und Exportieren von Daten. OData-Entitäten ermöglichten die Integration von Dynamics AX mit Programmen von Drittanbietern.</td>
</tr>
<tr>
<td>Durchführen von intelligenten Analysen mit BI-Berichten aus Microsoft Dynamics AX und dem POS-Client.</td>
<td>Es stehen über 25 Backofficeberichte und fünf kanalseitige Berichte zur Verfügung.</td>
<td>Es stehen über 30 Backofficeberichte und 10 kanalseitige Berichte zur Verfügung.</td>
<td>Diese Berichte bieten den Kunden mehr BI-Informationen zur Vorhersage von Trends, Nutzung von Einblicken und bestmöglichen Arbeit.</td>
</tr>
<tr>
<td>Analysieren Sie Retail Channel-Umsatzdaten mit dem Power BI-Inhaltspaket "Monitor Retail Channel performance".</td>
<td>Nicht verfügbar</td>
<td>Wählen Sie auf PowerBI.com <strong>Daten erhalten</strong> und dann das Inhaltspack <strong>Dynamics AX – Monitor Retail Channel performance</strong>. Geben Sie die URL für Ihren Dynamics AX-Endpunkt ein, um die Daten im Dashboard anzuzeigen.</td>
<td>Mit drei bis vier Klicks können Organisationen ein Power BI-Dashboard bereitstellen, das wichtige Finanzdaten enthält. Der Inhalt kann durch die Organisation personalisiert werden. Darüber hinaus können Benutzer Power BI-Dashboardflächen in ihre personalisierten Arbeitsbereiche in Dynamics AX einbetten, sodass sie analytische Informationen mit einem Blick sehen.</td>
</tr>
<tr>
<td>Konfigurieren von Verbraucherberechtigungen.</td>
<td>Nicht verfügbar</td>
<td>Kunden können auswählen, ob POS-Vorgänge für Verbraucher verfügbar sein können. Einzelhandel-Server: verwendet Berechtigungen für API-Anrufe.</td>
<td>Er bietet die Möglichkeit, Berechtigungen auf Verbraucherebene zu konfigurieren.</td>
</tr>
<tr>
<td>Verwalten und überprüfen von Entitätskonfigurationen.</td>
<td>Nicht verfügbar</td>
<td>Die Funktion Konfigurationsmanager und -validierer ermöglicht die folgenden Funktionen:
<ul>
<li>Hochladen von Massenkonfigurationsdaten</li>
<li>Validierung von Geschäftsentitäten</li>
</ul></td>
<td>Sie bietet die Möglichkeit, die Konfiguration zu laden, und den Status und Vollständigkeit der Konfiguration für die verschiedenen Konfigurationselemente zu überprüfen.</td>
</tr>
</tbody>
</table>

### <a name="retail-hardware-station"></a>Retail-Hardwarestation

| Wie können Sie vorgehen? | Dynamics AX 2012 | Dynamics AX 7.0 | Warum ist dieses wichtig? |
|------------------|------------------|-----------------|------------------------|
| Aktivieren von POS-Geräten, um Peripheriegeräte wie Drucker, Kassenladen oder Zahlungsgeräte zu verbinden. | Das MPOS-Hardwareprofil wird verwendet, um die Geräte anzugeben, die verwendet werden. | Ein hinzugefügtes Hardwareprofil unterstützt mehr unterschiedliche Hardware. Ein neues Hardware-Stationsprofil unterstützt eine eindeutige Terminalkennung für jede Hardware-Station, wenn elektronische Überweisungsbuchungen (EFT) verarbeitet werden. Die Unterstützung für elektronische Überweisung wurde in Hardwarestation zusammengeführt, um die Beteiligung von MPOS bei der Zahlungsverarbeitung zu reduzieren. | Sie bietet eine größere Flexibilität für Implementierungen. Sie bietet auch eine höhere Sicherheit und reduzierte die Sichtbarkeit von Kreditkartendaten. |

### <a name="retail-server-and-data-management"></a>Einzelhandel-Server und Datenverwaltung

Die Einzelhandel-Server und Datenverwaltung bietet Kunden und Unternehmen die Möglichkeit, eine Einkaufserfahrung für mehrere Kanäle (online, im Shop und Call-Center) zu erstellen.

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Stellen Sie eine Verbindung mit einer Commerce Runtime-(CRT)-Datenbank her, die Geschäftsdaten für den Kanal mithilfe von CRT-Diensten speichert.</td>
<td>OData V3 wird unterstützt.</td>
<td>OData V4 wird unterstützt.</td>
<td>Kann dafür sorgen, dass der Kunde die aktuellen OData-Standards nutzt. Sorgt außerdem für eine robuste Mehrkanalerfahrung, indem es den Vertrieb über die Kanäle (im Shop, mobil und online) integriert.</td>
</tr>
<tr>
<td>Unterstützung von Einzelhandels-Diensten als hostbarer Dienstsatz.</td>
<td>Die E-Commerce API wird nicht über Einzelhandel-Server unterstützt.</td>
<td>Die E-Commerce API ist jetzt über Einzelhandel-Server verfügbar, um Onlineszenarien zu unterstützen.</td>
<td>Er bietet gehostete und skalierbare E-Commerce-Dienste, die mit Onlineshops von Drittanbietern verwendet werden können.</td>
</tr>
<tr>
<td>Verschieben Sie Daten zwischen dem Microsoft Dynamics AX Back-Office und Kanälen, indem Commerce Data Exchange verwenden.</td>
<td>Commerce Data Exchange ist ein System, das Daten zwischen Microsoft Dynamics AX und den Handelskanälen wie Online-Shops oder Filialen überträgt. Weitere Informationen finden Sie unter <a href="/dynamicsax-2012/appuser-itpro/commerce-data-exchange">Commerce Data Exchange [AX 2012]</a>.</td>
<td>Es besteht eine funktionale Parität mit Microsoft Dynamics AX 2012 CU8. Beachten Sie jedoch die folgenden Details:
<ul>
<li>Commerce Data Exchange wurde für die Cloud überarbeitet.</li>
<li>Der Async-Dienst arbeitet mit einem direkten Datenbankzugriff der Kanaldatenbank.</li>
<li>Commerce Data Exchange: Echtzeit-Service wird als Microsoft Dynamics AX Custom Service gehostet.</li>
<li>MPOS verwaltet die Synchronisierung zwischen Offlinen Datenbanken und Einzelhandl-Server.</li>
</ul></td>
<td>Commerce Data Exchange wurde für die Cloud-Plattform neu entwickelt. Es verwaltet auch weiterhin den Datenaustausch zwischen Microsoft Dynamics AX und Einzelhandelskanälen, wie Onlineshops oder physische Shops.</td>
</tr>
<tr>
<td>Unterstützung von Plug & Play und halb-integrierten, kanalübergreifenden Zahlungen über das Zahlung-SDK.</td>
<td>AX 2012 bietet die folgenden Funktionen:
<ul>
<li>Unterstützung für alle Kanäle: POS, E-Commerce und Callcenter.</li>
<li>Unterstützung für Karten und fehlende Karten.</li>
<li>Seite für die Annahme einer Zahlung.</li>
<li>Peripheriunterstützung von LS5300 und MX925 als Beispielcode im Retail SDK.</li>
</ul></td>
<td>Die aktuelle Version von Dynamics AX unterstützt alle vorhandenen Microsoft Dynamics AX for Retail 2012 Kredit-/Debitkartenfunktionen und vier neue Erweiterungen.</td>
<td>Die Kunden können Kredit-/Debitkartenbuchungen für Zahlungen verarbeiten.</td>
</tr>
<tr>
<td>Aktivieren von Geräten mit einem Microsoft-Konto verwenden (Microsoft Azure Active Directory (Azure AD)).</td>
<td>Nicht verfügbar</td>
<td>Die Funktionen stehen bereit:
<ul>
<li>Erweiterte Sicherheit über die Azure AD-basierte Aktivierung für die Cloud</li>
<li>Erweiterte Sicherheit für die Tokenverwaltung.</li>
<li>Verbessertes Zuverlässigkeit, Problembehandlung und Fehlerbenachrichtigung während der Aktivierung</li>
<li>Vereinfachte IT-Verwaltungsaufgaben bei der Aktivierung.</li>
<li>Überprüftes Gefahrenmodell und Korrektur von Sicherheitsproblemen.</li>
</ul></td>
<td>Es bietet folgende Vorteile:
<ul>
<li>Die Sicherheit wird durch Azure AD und Gerät-Token/IDs erhöht (RS-Aufrufe, die ein Token verwenden, benutzerspezifischer Anwendungsspeicher)</li>
<li>Die nicht autorisierte Remote Verwendung von MPOS (Brick-Device) wird verhindert.</li>
<li>MPOS-Geräte werden zu PCI-Kompatibilitätszwecken nachverfolgt.</li>
<li>Physische Geräte werden einer Geschäftseinheit über ein Gerätentoken zugeordnet (Register).</li>
<li>Es werden beim ersten Kontakt mit MPOS Einstellungen für die reibungslose MPOS-Funktionalität initialisiert (Nummernkreise und Hardwareprofile).</li>
<li>Geräteinformationen werden aus dem Hauptsitz gemeldet.</li>
</ul></td>
</tr>
<tr>
<td>Verwalten von umfangreichen Medieninhalt zum Erstellen und das Bereitstellen über die Mediengalerie.</td>
<td>Nicht verfügbar</td>
<td><ul>
<li>Unterstützung des Hochladens von Bildern und anzeigen, verwalten und löschen über die Mediengalerie für extern gehostete und im Einzelhandel gehostete Bilder.</li>
<li>Unterstützung des Hochladens von Bildern und anzeigen von Entitätsseiten (<strong>Produkte</strong>, <strong>Kataloge</strong> usw.) über das Verknüpfung eines Bilds aus dem Katalog und das Hochladen eines Bildes vom Desktop aus.</li>
<li>Optimieren der Bilder für die Miniaturansicht, Sondergrößen und Originalgröße.</li>
<li>Massenverknüpfung von Entitäten über eine Vorlage und Hintergrundaufträge zur Massenzuordnung.</li>
<li>Microsoft Excel-Integration beseitigt die Attributgruppeneinschränkung für Benennungskonventionen und vordefinierte Pfade.</li>
<li>Unterstützung von Offlinebildern und sicheren Bildern für persönliche Informationen Inhalte wie im Einzelhandel gehostete Kombinationen aus Mitarbeiter- und Kundenbildern..</li>
</ul></td>
<td><ul>
<li>Er behebt problematische Punkte rund um extern gehostete Bilder. Sie müssen nicht mehr hin und her wechseln und alle werden an einem einzigen Ort verwalten.</li>
<li>Er stellt leistungsstarkes Content Management über die Mediengalerie zum Hochladen und externen Hosten von Bildern bereit und bietet Filter für die Verwaltung und Suche von Bildern.</li>
<li>Es ermöglicht Massenzuordnungen zwischen extern gehosteten Bildern und Entitäten wie Produkten und Katalogen.</li>
<li>Er unterstützt das Einzelhandel-gehostete Speichern von Bildern und die Excel-Integration für eine einfache Aktualisierung.</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="rich-clientele-experience"></a>Umfangreiche Kundenerfahrung

Einzelhändler bietet interaktive mobile Erfahrungen an jedem Ort, jederzeit und auf jedem Gerät. Diese Funktionalität ermöglicht eine erweiterte Einkaufs- und Shop-Erfahrungen über alle Kanäle.

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Suchen, navigieren oder scannen von Produkten, hinzufügen von Produkten zum Einkaufskorb, Zahlungen und Kaufen über eine intuitive, Touch-freundliche, umfangreiche und interaktive Benutzererfahrung auf MPOS.</td>
<td>AX 2012 ermöglicht die folgenden Funktionen:
<ul>
<li>Ausführen von Verkäufen, Rückgaben und Stornierungen.</li>
<li>Erstellen, Ändern und Annehmen von Kundenaufträgen.</li>
<li>Durchführen von Schicht- und Kassenladenvorgängen.</li>
<li>Annehmen und Erhalten von Aufträge und prüfen von Bestandsmengen.</li>
<li>Anzeigen von Shop-Berichten.</li>
</ul></td>
<td>Funktionalität entspricht AX 2012 MPOS  Dies umfasst die folgende Funktionalitäten:
<ul>
<li>Kundensuche über Shop/Kanäle hinweg.</li>
<li>Die Möglichkeit, Kundenaufträge zu erstellen, ohne auf Echtzeitdienste zuzugreifen.</li>
<li>Verbessertes Gerätenaktivierungsworkflows, Stati und Fehlermeldungen.</li>
<li>Erweiterbarkeitsverbesserungen wie Pre-Post-Trigger und Aktivitäten zur besseren Anpassung.</li>
</ul></td>
<td>Das Verkaufspersonal kann Verkaufsbuchungen und Kundenaufträge verarbeiten und führt täglichen Arbeitsgänge und die Lagerverwaltung aus, indem es mobile Geräte an beliebiger Stelle im Shop verwendet.</td>
</tr>
<tr>
<td>Starten von POS als Internetanwendung über Cloud POS.</td>
<td>Nicht verfügbar</td>
<td>Funktionalität entspricht MPOS. Dies umfasst die folgende Funktionalitäten:
<ul>
<li>Geräteaktivierung über AAD</li>
<li>Responsives Layout</li>
<li>Unterstützung von Edge, Internet Explorer und Chrome.</li>
</ul></td>
<td>Eine POS-Internetanwendung, die Funktionen bereitstellt, die mit MPOS kompatibel sind und die plattform- und browserübergreifend und ohne Bereitstellungskosten verwendet werden kann.</td>
</tr>
<tr>
<td>Integration in Content Management-Systemen, um eine kanalübergreifende E-Commerce-Website zu erstellen.</td>
<td>Microsoft SharePoint und Drittanbietern-Schaufenster werden unterstützt.</td>
<td>Eine E-Commerce-Plattform wird bereitgestellt, die Drittanbieter-Schaufenster unterstützt. Der Plattform enthält die folgenden Funktionen:
<ul>
<li>Eine umfangreicher Kunden-API.</li>
<li>Authentifizierungsintegration mit beliebigen Open-ID-Anbietern von Drittanbietern.</li>
<li>Zahlungsintegration.</li>
</ul></td>
<td>Die Kunden haben nun die Flexibilität, das Content Management-System ihrer Wahl zu verwenden.</td>
</tr>
<tr>
<td>Ansprechen von Kunden über Postversandkataloge, vereinfachter Betrieb über eine schnelle Auftragserfassung, Verkaufsberatung und Lieferung über ein Callcenter.</td>
<td><ul>
<li>Callcenterkanal</li>
<li>Postversandkataloge</li>
<li>Schnelle Auftragserfassung und Verkaufsberatung</li>
<li>Erweiterte Lieferung</li>
<li>Kundendienst</li>
<li>Integrierte Preisgestaltung und Aktionen/Rabatte</li>
</ul></td>
<td>Funktionsparität mit der AX 2012-Callcenter-Lösung mit Ausnahme von Preisüberschreibungen.</td>
<td>Callcenter sind ein Einzelhandelskanal, bei dem Arbeitskräfte Aufträge von Kunden telefonisch entgegennehmen und Aufträge erstellen.</td>
</tr>
</tbody>
</table>

### <a name="commerce-essentials"></a>Handelsgrundlagen

Ein Konfigurationsoption für den Einzelhandel und den Handel vereinfacht einzelhandelsspezifische Bereitstellungen.

| Wie können Sie vorgehen? | Dynamics AX 2012 | Dynamics AX 7.0 | Warum ist dieses wichtig? |
|------------------|------------------|-----------------|------------------------|
| Verwenden Sie das Handelsgrundlagen-Dashboard. | Eine Bereichsseite mit Links zu Menüoptionen ist verfügbar. | Das Handelsgrundlagen-Dashboard enthält Links zu allgemeine Aufgaben, einschließlich Links zu den Arbeitsbereichen, zum Power BI-Websteuerelement, zu den Favoriten, den kürzlich besuchten Seiten und den aktuellen Arbeitsaufgaben. | Das erweiterte Dashboard ermöglicht Arbeitskräften dabei, effizienter zu arbeiten und bietet einen flexiblen Startpunkt für jede einzelhandelsspezifische Aufgabe. |
| Nutzen Sie Datenentitäten für den Zugriff auf Kontoenänderungen. | Kontoenänderungen werden in einen Ordner im Dateisystem exportiert. | Kontoenänderungen sind über Datenentitäten zugreifbar. | Diese Funktion bietet eine größere Flexibilität beim Verschieben von Daten zwischen getrennten Systemen. Diese Funktion kann über OData erweitert werden. |
| Nutzen Sie Cloud POS und MPOS. | Nur Enterprise POS (EPOS) wird standardmäßig unterstützt. | MPOS und Cloud POS ersetzen den EPOS-Client. Der E-Commerce-Kanal wurde standardmäßig zu den Handelsgrundlagen hinzugefügt. | Diese Funktion ermöglicht eine bessere vordefinierte Kanalunterstützung mit schnellen Bereitstellungen von POS-Clients. |
| Implementieren und Verwalten eine Architektur mit zwei Ebenen. | Das Datenimport-/Exportframework bietet die Möglichkeit, Daten zwischen AX 2012 und Drittanbietersystemen zu verschieben. | Datenentitäten wurden erstellt, um eine Zweistufenarchitektur zu unterstützen. | Datenentitäten und OData-Anwendungen bieten eine Abstraktionsebene, um Szenarien mit zwei Ebenen einfacher zu implementieren und zu verwalteten. |
| Vereinfachte Formulare. | Benutzerdefinierter Code ist erforderlich, um die Benutzeroberfläche zu vereinfachen. | Formulars und Menüerweiterungen stellen standardisierte Vereinfachungen der Benutzeroberfläche bereit. | Diese Funktion bietet eine schnellere und einfachere Methode, um Formulare auf Grundlage der Anforderungen des Einzelhändlers anzupassen. |

### <a name="pos-task-recorder"></a>POS-Aufgabenaufzeichnung

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Erstellen und Teilen von Aufgabenleitfäden und Dokumenten für Modern POS.</td>
<td>Nicht verfügbar</td>
<td>die MPOS-Aufgabenaufzeichnung unterstützt die folgenden Funktionen:
<ul>
<li>Erstellen von Aufgabenaufzeichnungen für verschiedene Aufgaben, die in MPOS ausgeführt werden.</li>
<li>Generieren eines Dokuments, das Schritte und Screenshots umfasst, und Zuordnen zu einem Knoten in Geschäftsprozessmodell.</li>
</ul></td>
<td>Partner und unabhängige Softwarehersteller (ISVs) können MPOS anpassen und unterstützende Dokumente für die Benutzerschulung bereitstellen.</td>
</tr>
</tbody>
</table>

### <a name="extensibility"></a>Erweiterbarkeit

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Unterstützen von erweiterbaren und einfacher bereitstellbaren Einzelhandelskomponenten im Hauptsitz, in Callcentern, beim E-Commerce und im POS.</td>
<td>Die Komponenten können über das Retail-SDK erweitert werden. Keine Verpackungs- und Bereitstellungsfunktionen werden unterstützt.</td>
<td>Extensibility-Hooks wurden für verschiedene Komponenten verbessert, um die Code-Isolierung und Serviceability zu verbessern. Nachfolgend einige der Funktionen, die enthalten sind:
<ul>
<li>Workflow, Aktivität und Betrieb.</li>
<li>Pre-Trigger und Post-Trigger, die die einfache Erweiterung eines Workflows ermöglichen.</li>
<li>Anwendungs- und Betriebs-Trigger.</li>
</ul>
E steht ein Framework bereit, um diese Komponenten über MSBuild zu erstellen und zu packen und dann nahtlos Anpassung über Microsoft Dynamics Lifecycle Services (LCS) bereitzustellen.</td>
<td>Einzelhändler haben bestimmte Anforderungen (je nach Marktsegment und geografischer Region). Durch eine leicht erweiterbare Plattform ermöglichen wir die Verwendung in verschiedenen Segmenten und Märkten. Da Einzelhandel auch sehr verteilte Architektur nutzen, verbessert die Möglichkeit der nahtlosen Bereitstellung die Produktivität erheblich.</td>
</tr>
</tbody>
</table>

### <a name="lifecycle-management"></a>Lebenszyklusverwaltung

Lifecycle Services (LCS) bietet verschiedene Dienst, mit denen Kunden und Partner den Lebenszyklus des Systems komplett verwalten können.

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Verwalten des Programms über Cloudbereitstellungsdienste.</td>
<td>Nicht verfügbar</td>
<td>Die folgenden Topologien können mit einer Cloud bereitgestellt werden:
<ul>
<li>Retail One-Box Test-Topologie.</li>
<li>Retail Multi-Box Hochverfügbarkeits-Topologie.</li>
<li>Entwicklertopologie mit dem Retail-SDK.</li>
</ul>
Es gibt eine verbesserte "low-touch" Clientkomponenteninstallation über die Self-Service-Installation:
<ul>
<li>Retail Modern POS.</li>
<li>Retail Hardware Station.</li>
<li>Unterstützung für den Upload und die Verteilung von benutzerdefinierten Paketen über die Self-Service-Installation.</li>
</ul></td>
<td>Die Cloudbereitstellungsdienste bieten die folgenden Vorteile:
<ul>
<li>Erheblich reduzierter Bereitstellungsaufwand und -komplexität für Einzelhandel-Hauptsitz-Komponenten.</li>
<li>Native Bereitstellung die öffentlich Microsoft Azure-Cloud</li>
<li>Verbesserte Self-Service-Installation von In-Store-Komponenten, um die Konfiguration einfacher und intuitiver vorzunehmen</li>
</ul></td>
</tr>
<tr>
<td>Überwachen des Status des Systems, und Diagnose von Fehlern und Problemen</td>
<td>Diese Funktionen erfordern <a href="https://www.microsoft.com/en-us/download/details.aspx?id=58205">System Center 2012 Management Pack für Microsoft Dynamics AX 2012 R3 CU8 Retail.</a></td>
<td>Überwachen sowie Diagnose für Einhelhandel-Komponenten ist jetzt über das Dashboard in <strong>Betriebseinblick</strong> in LCS verfügbar.</td>
<td>Das <strong>Betriebseinblick</strong>-Dashboard ist ein Cloud-basiertes Überwachungsportal, das die Installation der System Center Operations Manager (SCOM)-Infrastruktur überflüssig macht.</td>
</tr>
<tr>
<td>Erstellen, Konfigurieren, Hochladen und Installieren von Retail-Hardwarestation und Geräten per Self-Service.</td>
<td>Über die Verwendung des Installations-Packers und des Enterprise Portals kann der Benutzer eine automatisierte Installation und Konfiguration aller auf einem bestimmten Computer erforderlichen Komponenten (je nach definierter Topologie) ausführen.</td>
<td>Da es nur zwei Installationspakete gibt (eines für den MPOS-Client und eines für die Retail-Hardwarestation), reduziert der Self-Service den Arbeitsaufwand für die Installation dieser Clientkomponenten.</td>
<td>Der Self-Service minimiert die Anforderungen und vereinfacht die Installation für den Benutzer.</td>
</tr>
</tbody>
</table>

## <a name="sales"></a>Verk.

<table>
<thead>
<tr>
<th>Wie können Sie vorgehen?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Warum ist dieses wichtig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Hier können Sie einen kurzen Überblick über Lieferalternativen für zugesagte Aufträge abrufen.</td>
<td>Wenn die Produktverfügbarkeit eingeschränkt ist, und das angeforderte Lieferdatum des Kunden für eine oder mehrere Produkte im Auftrag nicht erfüllt werden kann, wird die Einhaltung der Lieferzusagen problematisch. Um Alternativen zu suchen um das angeforderte Lieferdatum des Kunden einzuhalten, oder dem Kunden eine akzeptable und zuverlässige Lösung anzubieten, muss der Auftragsbearbeiter möglicherweise mehrere Formulare öffnen. Jedes stellt nur einen Teil der erforderlichen Informationen bereit. Ein Formular zeigt die verfügbare Menge standortübergreifend an, ein anderes zeigt die verfügbare Menge in der Intercompany-Einstellung an, ein drittes Formular bietet die Möglickeit, das früheste Verfügbarkeitsdatum für einen Standort/Variante zu berechnen und ein viertes zeigt Lieferbestellungen. Daher sind die Benutzer nicht sicher, ob sie alle relevanten Optionen berücksichtigt haben. Die Benutzer fühlen sich nicht sicher, da zahlreiche Unterbrechungen während des Lieferzusageablaufs auftreten (z. B. das Öffnen und Schließen von Seiten und Abrufen von Optionen und Informationen).</td>
<td>Auf Grundlage die vorhandenen Algorithmen für die Berechnung des Lieferdatums bietet die Seite <strong>Lieferungsalternativen</strong> mehr Benutzerfreundlichkeit bei Lieferzusagen:
<ul>
<li>Sie konsolidiert relevante Informationen aus mehreren Formularen an einem Ort.</li>
<li>Sie bietet "einsatzbereite" alternative Lieferungspakete, wie eine Kombination aus Standort/Lagerort/Variante/Transportmodus auf Basis der schnellsten Lieferung (frühestes verfügbares Datum), aus denen der Benutzer wählen kann.</li>
<li>Der Benutzer kann Optionen aus der Simulationsoberfläche auswählen und diese auf die Auftragsposition übertragen.</li>
</ul></td>
<td>Unternehmen, die einen hohen Kundenservice anbieten und gleichzeitig eine Bestandsoptimierungsstrategie nutzen möchten, müssen in der Lage sein, Lieferungen zuverlässig und wettbewerbsfähig zuzusagen. Schließlich benötigt der Kunde für seinen eigenen Betrieb eine pünktliche Lieferung. Die <strong>Lieferungsalternativen</strong>-Aufgabenseite gestaltet die Lieferzusagen schneller, einfacher und systematischer, indem die beste alternativen Auftragslieferdaten interaktiv ermittelt und empfohlen werden.</td>
</tr>
</tbody>
</table>

## <a name="service-management"></a>Serviceverwaltung

Es wurden keine neuen Funktionen hinzugefügt.

## <a name="transportation-management"></a>Transportverwaltung

Es wurden keine neuen Funktionen hinzugefügt.

## <a name="travel-and-expense"></a>Reisekosten und Spesen

Es wurden keine neuen Funktionen hinzugefügt.

## <a name="warehouse-management"></a>Lagerortverwaltung

| Wie können Sie vorgehen? | Dynamics AX 2012 | Dynamics AX 7.0 | Warum ist dieses wichtig? |
|------------------|------------------|-----------------|------------------------|
| Herunterladen, installieren und konfigurieren des Warehouse Mobile Devices Portals. | Sie können das Portal während des Microsoft Dynamics AX-Installationsvorgangs über die Standardeinrichtung herunterladen, einrichten und konfigurieren. Es wurde für die selbstständige lokale Bereitstellung und Konfiguration entworfen. | Sie können ein eigenständiges Installationsprogramm über eine Menüoption in der Lagerortverwaltung herunterladen. Es wurde für die selbstständige lokale Bereitstellung und Konfiguration entworfen. | Wenn Sie die Verwendung der Funktionen für mobile Geräte einrichten, müssen Sie Warehouse Mobile Devices Portal lokal einrichten und konfigurieren und eine Verbindung zu Dynamics AX in der Cloud abrufen. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Neuerungen oder Änderungen in Finance and Operations – Startseite](whats-new-changed.md)

[Neuer Aufgabenleitfaden verfügbar (Februar 2016)](new-task-guides-available-february-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
