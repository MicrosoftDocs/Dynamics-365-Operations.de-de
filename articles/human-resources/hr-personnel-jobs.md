---
title: Einrichten von Komponenten eines Einzelvorgangs
description: In diesem Artikel werden die Begriffselemente, die ein Einzelvorgang enthalten kann beschriben und es enthält Beispiele dafür, wie die Elemente in der Organisation verwendet werden können.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 02475cdc23565c1d49c9f1bb6901101b16acf3a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009179"
---
# <a name="set-up-the-components-of-a-job"></a>Einrichten von Komponenten eines Einzelvorgangs

In diesem Artikel werden die Begriffselemente, die ein Einzelvorgang enthalten kann beschriben und es enthält Beispiele dafür, wie die Elemente in der Organisation verwendet werden können. 

Bevor Sie einen Vorgang erstellen, müssen Sie gewisse Referenzinformationen einrichten. Sie können einen Einzelvorgang erstellen, der lediglich einen Namen hat. Allerdings vom Einschließen von zusätzliche Informationen, wie einer Berufsbezeichnung, stellen Sie die Standardwerte für Positionen verfügbar, die der Stelle zugewiesen sind. Darüber hinaus können einige der Informationen, die Sie eingeben, verwendet werden, um Vergütungspläne für bestimmte Stellen zu filtern. Wenn Sie Berechtigungen einstellen möchten, die Sie zum Filtern von Vergütungsplänen für eine bestimmte Stelle verwenden können, richten Sie vor der Einrichtung von Stellen zunächst Stellenfunktionen und Stellenarten ein. Mithilfe dieser Standardwerte, sparen Sie Zeit, wenn Sie dem Einzelvorgang Positionen hinzufügen. 

Einige Einzelvorgangsdetails, wie die Position, Typ und Funktion, sind Datum-effektiv. Wenn Sie heute einen Einzelvorgang erstellen, aber diese Details später hinzufügen und Sie dann den Einzelvorgang ab dem Erstellungsdatum ansehen, werden diese Informationen nicht erscheinen. Daher sollten Sie einigen dieser Referenzinformationen erstellen, bevor sie benötigt werden. So können Sie die neuen Informationen Einzelvorgängen hinzufügen, sobald Sie diese erstellen.

## <a name="job-titles"></a>Stellenbezeichnungen
Vor der Erstellung von Stellen sind zugehörige Stellenbezeichnungen einzurichten. Positionen erben die Stellenbezeichnungen von den Stellen, denen die Positionen zugeordnet sind. 

Verwalten Sie Positionen mithilfe der **Titel**-Seite, die Sie öffnen können, indem Sie die Suchfunktion verwenden. Auf der **Titel** Seite geben Sie die Positionen ein, die Sie einplanen und für die Einzelvorgänge verwenden möchten.

## <a name="job-types"></a>Stellentypen
Verwenden Sie Stellentypen als Gruppe, um ähnliche Stellen in Kategorien zu klassifizieren. Stellentypen sind nicht erforderlich. Planen Sie jedoch, Stellentypen zur Einrichtung von Berechtigungsregeln für die Vergütungsverwaltung zu verwenden, richten Sie vor der Einrichtung von Stellen zunächst Stellentypen ein. Beispiele für Stellentypen sind Voll- und Teilzeit oder festes Salär und Stundenlohn. Verwalten Sie Stellentypen mithilfe der Seite **Stellenarten**. Geben Sie auf der Seite **Stellenarten** einen Namen und eine kurze Beschreibung des Positionstyps ein. Wählen Sie im Feld **Status befreit** eine der folgenden Optionen aus, um den Ausnahmezustand des Fair Labor Standards Act (FLSA) für Stellen anzugeben, die zu folgenden Stellenarten gehören:

-   **Befreit** – – Stellen sind gemäß dem FLSA-Gesetz von Überstunden befreit.
-   **Nicht Befreit** – – Stellen sind gemäß dem FLSA-Gesetz nicht von Überstunden befreit.
-   **Nicht anwendbar** – Eine Abdeckung durch das FLSA-Gesetzt trifft nicht zu.

## <a name="job-functions"></a>Stellenfunktionen
Stellenfunktionen beschreiben funktionale übergeordnete Kategorien und ordnen übergeordnete Aufgaben zu. Stellenfunktionen sind nicht erforderlich. Sie können Stellenfunktionen zusammen mit Stellentypen verwenden, um Vergütungspläne nach bestimmten Stellen zu filtern. Sie ordnen Stellenfunktionen und Stellentypen Vergütungsplänen zu, indem Sie im Formular auf der Seite **Berechtigungsregeln** Berechtigungsregeln einrichten. Sie können mit dem Vergütungsplan auch mehrere Ebenen verknüpfen, die für eine bestimmte, über eine Berechtigungsregel definierte Stellenfunktion/Stellentyp-Kombination gelten. (Diese Funktion gilt für feste Vergütungspläne und variable Vergütungspläne) Planen Sie jedoch, Stellenfunktionen zur Einrichtung von Berechtigungsregeln für die Vergütungsverwaltung zu verwenden, richten Sie vor der Einrichtung von Stellen zunächst Stellenfunktionen ein. Beispiele für Stellenfunktionen finden Sie in der folgenden Tabelle.

| Stelle           | Stellenfunktion         |
|---------------|----------------------|
| Verkaufsleiter | Manager auf mittlerer Ebene    |
| Sachbearbeiter Buchhaltung    | Professionals        |

Verwalten Sie Stellenfunktionen mithilfe der Seite **Stellenfunktionen**. Geben Sie auf der Seite **Stellenarten** einen Namen und eine kurze Beschreibung des Positionstyps ein.

## <a name="job-tasks"></a>Arbeitsaufgaben
Sie können Arbeitsaufgaben erstellen, die die grundlegenden Aufgaben beschreiben, die eine Arbeitskraft in einer Position für diesen Einzelvorgang ausführen muss. Die gleiche Arbeitsaufgabe kann mehreren Einzelvorgängen hinzugefügt werden, und Positionen für diese Einzelvorgänge erben die Arbeitsaufgaben. Beispiele für Stellenaufgaben finden Sie in der folgenden Tabelle.

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
<li><strong>Leistungsbeurteilung</strong> – Überprüfung der Arbeitsleistung jedes Verkäufers.</li>
<li><strong>ABS-Überprüfung</strong> – Genehmigen oder Ablehnen der Abwesenheitsanforderungen oder -erfassungen jedes Verkäufers.</li>
</ul></td>
</tr>
<tr class="even">
<td>Sachbearbeiter Buchhaltung</td>
<td><strong>FIN-Bericht</strong> – Wöchentliche Finanzberichte dem Leiter der Finanzabteilung präsentieren.</td>
</tr>
</tbody>
</table>

Verwalten Sie Stellenaufgaben mithilfe der Seite **Stellenaufgaben**. Geben Sie auf der Seite **Stellenaufgabe** einen Namen und eine kurze Beschreibung des Positionsaufgaben ein. Im Feld **Hinweise** können Sie optional zusätzliche Informationen eingeben. Die Hinweise können für einen bestimmten Einzelvorgang aktualisiert werden, ohne die zu Hinweise ändern, die Sie hier eingegeben haben.

## <a name="areas-of-responsibility"></a>Zuständigkeitsbereiche
Verwenden Sie Zuständigkeitsbereiche, um die Arbeitsrollen, Prozesse und Produkte anzugeben, für die eine Arbeitskraft in einer Position für diesen Einzelvorgang zuständig sein würde. Ein Beispiel für einen Zuständigkeitsbereich für eine Stelle mit dem Titel "Buchhalter" könnte "Finanzberichterstellung für Produkt A" sein. Sie verwalten Zuständigkeitsbereiche mithilfe der Seite **Bereiche der Zuständigkeit**, die Sie mithilfe der Suchfunktion finden. Geben Sie auf der Seite **Zuständigkeitsbereiche** einen Namen und eine kurze Beschreibung der Zuständigkeit ein. Im Feld **Hinweise** können Sie optional zusätzliche Informationen eingeben. Die Hinweise können für einen bestimmten Einzelvorgang aktualisiert werden, ohne die zu Hinweise ändern, die Sie hier eingegeben haben.

## <a name="steps-for-creating-a-job"></a>Schritte zum Erstellen einer Stelle
Im Artikel [Definieren neuer Stellen](../fin-and-ops/hr/tasks/define-new-jobs.md) finden Sie die detaillierte Prozedur zum Erstellen einer neuen Stelle. 
