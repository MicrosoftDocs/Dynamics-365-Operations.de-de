---
title: Richten der Komponenten eines Einzelvorgangs
description: "In diesem Thema werden die Begriffselemente, die ein Einzelvorgang enthalten kann und enthält Beispiele dafür, wie Sie die Elemente in der Organisation verwendet werden können."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: d96b1f01a5cb4370436888deae8fd4835a0dbb80
ms.openlocfilehash: b8143db5b133337603a7f2f46028d91bb81cd947
ms.lasthandoff: 03/31/2017


---

# <a name="setting-up-the-components-of-a-job"></a>Richten der Komponenten eines Einzelvorgangs

In diesem Thema werden die Begriffselemente, die ein Einzelvorgang enthalten kann und enthält Beispiele dafür, wie Sie die Elemente in der Organisation verwendet werden können. 

Vor der Erstellung von Stellen können, müssen einige Referenzinformationen einzurichten. Sie können einen Auftrag erstellen, der lediglich einen Namen hat. Allerdings vom Einschließen von zusätzliche Informationen, z eine Berufsbezeichnung, stellen Sie die Standardwerte für Positionen verfügbar, die der Stelle zugewiesen sind. Darüber hinaus können einige der Informationen, die Sie eingeben, werden verwendet, um Vergütungspläne für bestimmte Stellen zu filtern. Wenn Sie Beschäftigungsberechtigung einrichten möchten, die Sie verwenden können, um Vergütungspläne für einen bestimmten Einzelvorgang zu filtern, sollten Sie Stellenfunktionen und Stellentypen ein, bevor Sie zugehörige Stellenbezeichnungen einzurichten. Mithilfe dieser Standardwerte, verfügbaren Sie eine Zeitersparnis haben, als Sie Positionen zum Einzelvorgang hinzufügen. 

Einige Einzelvorgangsdetails, wie die Position, Typ und Funktion, sind Datum-effektiv. Beim Erstellen, Einzelvorgangs- heute jedoch nicht diese Details auf später hinzufügen und Sie dann den Einzelvorgang zum Erstellungsdatum berücksichtigen, werden diese Informationen nicht. Daher sollten Sie einigen dieser Referenzinformationen erstellen, bevor sie benötigt werden. Deshalb, können Sie die neuen Informationen Einzelvorgänge hinzufügen, sobald Sie diese erstellen.

## <a name="job-titles"></a>Positionen
Vor der Erstellung von Stellen sind zugehörige Stellenbezeichnungen einzurichten. Positionen erben die Stellenbezeichnungen von den Stellen, denen die Positionen zugeordnet sind. 

Verwalten Sie Positionen mithilfe der Titel ** ** Seite bei, die geöffnet werden können, indem die Suchfunktion verwenden. Auf der Titel ** ** Seite geben Sie die Positionen ein, die Sie einplanen, für die Einzelvorgänge zu verwenden.

## <a name="job-types"></a>Stellentypen
Sie können Einzelvorgangstypen, um ähnliche Stellen in Kategorien zu gruppieren. Stellentypen sind nicht erforderlich. Planen Sie jedoch, Stellentypen zur Einrichtung von Berechtigungsregeln für die Vergütungsverwaltung zu verwenden, richten Sie vor der Einrichtung von Stellen zunächst Stellentypen ein. Beispiele für Stellentypen sind ganztägig und Teilzeit- oder Gehalt Stundenlohn und. Verwalten Sie Stellentypen hinzu, indem Sie die Einzelvorgangstypen ** ** Seite. Auf der Einzelvorgangstypen ** ** Seite geben Sie einen Namen und eine kurze Beschreibung des Stellentyps ein. Wählen Sie im ** Befreiungsstatus ** Feld eine der folgenden Optionen aus, um den Befreiungsstatus Messe-Arbeitsnormen-Tat (FLSA) von Einzelvorgängen anzugeben, die den entsprechenden Einzelerfassungstyp haben:

-   ** Ausgenommene ** – Stellen sind gemäß dem FLSA-Gesetz gemäß dem FLSA-Gesetz Überstunden befreit.
-   ** Nicht ausgenommene ** – Stellen sind nicht von Überstunden befreit gemäß dem FLSA-Gesetz ausgenommen.
-   ** Trägt nicht ** – Eine Abdeckung durch das FLSA-Gesetzt trifft nicht zu auf.

## <a name="job-functions"></a>Stellenfunktionen
Einzelvorgangsverknüpfungen beschreiben funktionale übergeordnete Kategorien und ordnen übergeordnete Aufgaben zu. Stellenfunktionen sind nicht erforderlich. Sie können, Stellenfunktionen werden zusammen mit Stellentypen verwenden, um Vergütungspläne für bestimmte Stellen zu filtern. Sie ordnen Stellenfunktionen und Stellentypen Vergütungsplänen zu, indem Sie im Formular Berechtigungsregeln ** Berechtigungsregeln ** Seite einrichten. Sie können einen Satz Ebenen einem Vergütungsplan dann zugeordnet werden, die für eine bestimmte Kombination eines Stellentyps und der Stellenfunktion gelten, die über eine Berechtigungsregel definiert wurde. (Diese Funktionen gelten für feste Vergütungen und Plänen für variable Vergütung" zu. Planen Sie jedoch, Stellenfunktionen verwenden, wenn von Berechtigungsregeln für die Vergütungsverwaltung einrichten, sollten von Stellenfunktionen einrichten, bevor Sie zugehörige Stellenbezeichnungen einzurichten. Die folgende Tabelle enthält einige Beispiele von Stellenfunktionen anzeigen.

| Stelle           | Stellenfunktion         |
|---------------|----------------------|
| Verkaufsleiter | Mittelstufenmanager    |
| Sachbearbeiter Buchhaltung    | Artikeln        |

Verwalten Sie Stellenfunktionen hinzu, indem Sie die Stellenfunktionen ** ** Seite. ** Stellenfunktionen ** Auf der Seite geben Sie einen Kennungscode und eine kurze Beschreibung für die Stellenfunktion ein.

## <a name="job-tasks"></a>Arbeitsaufgaben
Arbeitsaufgaben beschreiben die grundlegenden Aufgaben, die einer Arbeitskraft, die in einer Position für einen Einzelvorgang wird, abschließen muss. Dieselbe Arbeitsaufgabe kann zu mehreren Einzelvorgängen und den Auftragspositionen für die Stellen hinzugefügt werden, für die diese Arbeitsaufgaben verwendet. Die folgende Tabelle enthält einige Beispiele von Arbeitsaufgaben angezeigt.

<table>
<thead>
<tr class="header">
<th>Stelle</th>
<th>Arbeitsaufgabe</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Verkaufsleiter</td>
<td><ul>
<li><strong>Perf-Prüfung</strong> – Lesen der jedes Arbeitsleistung Verkäufers.</li>
<li><strong>ABS-Prüfung</strong> – Dient zum Genehmigen oder Ablehnen von Abwesenheitsanforderungen oder die die Erfassungen eines Verkäufers zurück.</li>
</ul></td>
</tr>
<tr class="even">
<td>Sachbearbeiter Buchhaltung</td>
<td><strong>Flosse-Bericht</strong> Vorhandene – wöchentliche Finanzberichte die Leiterin der Finanzabteilung.</td>
</tr>
</tbody>
</table>

Verwalten Sie Arbeitsaufgaben hinzu, indem Sie die Arbeitsaufgaben ** ** Seite. Auf der Arbeitsaufgaben ** ** Seite geben Sie einen Namen und eine Beschreibung für die Arbeitsaufgabe ein. Geben Sie den Hinweis ** ** Feld können Sie optional zusätzliche Informationen eingeben. Die Hinweise können für einen bestimmten Einzelvorgang aktualisiert werden, ohne die Hinweise ändern, die Sie hier eingegeben haben.

## <a name="areas-of-responsibility"></a>Zuständigkeitsbereiche
Zuständigkeitsbereiche dienen, um die Arbeitsrollen, Prozessen und Produkten anzugeben, dass eine Arbeitskraft, die in einer Position für einen Einzelvorgang für ist, zuständig ist. Beispiel für einen Einzelvorgang, der Buchhalter der Bezeichnung "," kann ein Produkt für Finanzberichte Zuständigkeitsbereich "A". Sie verwalten Zuständigkeitsbereiche hinzu, indem Sie die Zuständigkeitsbereiche ** ** Seite verwenden, denen Sie suchen können, indem Sie die Suchfunktion verwenden. Auf der Zuständigkeitsbereiche ** ** Seite geben Sie einen Namen und eine Beschreibung für die Zuständigkeit ein. Geben Sie den Hinweis ** ** Feld können Sie optional zusätzliche Informationen eingeben. Die Hinweise können für einen bestimmten Einzelvorgang aktualisiert werden, ohne die Hinweise ändern, die Sie hier eingegeben haben.


