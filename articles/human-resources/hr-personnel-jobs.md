---
title: Komponenten einer Stelle einrichten
description: In diesem Thema werden die Begriffselemente, die ein Einzelvorgang enthalten kann beschriben und es enthält Beispiele dafür, wie die Elemente in der Organisation verwendet werden können.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle, HcmPersonnelManagementWorkspace, HCMJobFamily
audience: Application User
ms.author: twheeloc
ms.search.scope: Human Resources
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a4aa7369c84836154b8217a5b70267021f4028b1
ms.sourcegitcommit: 4f84540e6121ca3d5ae52ee07e414116d423cefa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/03/2022
ms.locfileid: "7948474"
---
# <a name="set-up-the-components-of-a-job"></a>Komponenten einer Stelle einrichten

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema werden die Begriffselemente, die ein Einzelvorgang enthalten kann beschriben und es enthält Beispiele dafür, wie die Elemente in der Organisation verwendet werden können. 

Bevor Sie einen Vorgang erstellen, müssen Sie gewisse Referenzinformationen einrichten. Sie können einen Einzelvorgang erstellen, der lediglich einen Namen hat. Allerdings vom Einschließen von zusätzliche Informationen, wie einer Berufsbezeichnung, stellen Sie die Standardwerte für Positionen verfügbar, die der Stelle zugewiesen sind. Darüber hinaus können einige der Informationen, die Sie eingeben, verwendet werden, um Vergütungspläne für bestimmte Stellen zu filtern. Wenn Sie Berechtigungen einstellen möchten, die Sie zum Filtern von Vergütungsplänen für eine bestimmte Stelle verwenden können, richten Sie vor der Einrichtung von Stellen zunächst Stellenfunktionen und Stellenarten ein. Mithilfe dieser Standardwerte, sparen Sie Zeit, wenn Sie dem Einzelvorgang Positionen hinzufügen. 

Einige Einzelvorgangsdetails, wie die Position, Typ und Funktion, sind Datum-effektiv. Wenn Sie heute einen Einzelvorgang erstellen, aber diese Details später hinzufügen und Sie dann den Einzelvorgang ab dem Erstellungsdatum ansehen, werden diese Informationen nicht erscheinen. Daher sollten Sie einigen dieser Referenzinformationen erstellen, bevor sie benötigt werden. So können Sie die neuen Informationen Einzelvorgängen hinzufügen, sobald Sie diese erstellen.

## <a name="job-titles"></a>Stellenbezeichnungen
Vor der Erstellung von Stellen sind zugehörige Stellenbezeichnungen einzurichten. Positionen erben die Stellenbezeichnungen von den Stellen, denen die Positionen zugeordnet sind. 

Verwalten Sie Positionen mithilfe der **Titel**-Seite, die Sie öffnen können, indem Sie die Suchfunktion verwenden. Auf der Seite **Titel** geben Sie die Positionen ein, die Sie einplanen und für die Einzelvorgänge verwenden möchten.

## <a name="job-types"></a>Stellentypen
Verwenden Sie Stellentypen als Gruppe, um ähnliche Stellen in Kategorien zu klassifizieren. Stellentypen sind nicht erforderlich. Planen Sie jedoch, Stellentypen zur Einrichtung von Berechtigungsregeln für die Vergütungsverwaltung zu verwenden, richten Sie vor der Einrichtung von Stellen zunächst Stellentypen ein. Beispiele für Stellentypen sind Voll- und Teilzeit oder festes Salär und Stundenlohn. Verwalten Sie Stellentypen mithilfe der Seite **Stellenarten**. Geben Sie auf der Seite **Stellenarten** einen Namen und eine kurze Beschreibung des Positionstyps ein. Wählen Sie im Feld **Status befreit** eine der folgenden Optionen aus, um den Ausnahmezustand des Fair Labor Standards Act (FLSA) für Stellen anzugeben, die zu folgenden Stellenarten gehören:

-   **Befreit** – – Stellen sind gemäß dem FLSA-Gesetz von Überstunden befreit.
-   **Nicht Befreit** – – Stellen sind gemäß dem FLSA-Gesetz nicht von Überstunden befreit.
-   **Nicht anwendbar** – Eine Abdeckung durch das FLSA-Gesetzt trifft nicht zu.

## <a name="job-family"></a>Stellenfamilie
Eine Stellenfamilie ist eine Gruppe von Stellen, die ähnliche Tätigkeiten enthalten und ähnliche Ausbildung, Fähigkeiten, Kenntnisse und Fachkenntnisse erfordern. Eine Stellenfamilie kann mit einer Stelle auf dem Inforegister **Stellenklassifizierung** der Seite **Stellen** und dem Inforegister **Allgemein** der Seite **Alle Positionen**. Stellenfamilien können breit oder spezifisch sein, je nach Ihren Geschäfts- und Berichtsanforderungen. Einige Beispiele für breite Stellenfamilien sind **Facharbeiter** und **Ungelernte Arbeitskräfte**. Einige Beispiele für bestimmte Stellenfamilien sind **Buchhaltung**, **Fertigung** und **Vertrieb**.

Verwalten Sie Stellenfamilien mithilfe der Seite **Stellenfamilie**, die Sie öffnen können, indem Sie die Suchfunktion verwenden. Geben Sie auf der Seite **Stellenfamilie** der Familie einen eindeutigen Namen und geben Sie eine detaillierte Beschreibung ein, die Sie für Ihre Stellen verwenden möchten.

## <a name="job-functions"></a>Stellenfunktionen
Stellenfunktionen beschreiben funktionale übergeordnete Kategorien und ordnen übergeordnete Aufgaben zu. Stellenfunktionen sind nicht erforderlich. Sie können Stellenfunktionen zusammen mit Stellentypen verwenden, um Vergütungspläne nach bestimmten Stellen zu filtern. Sie ordnen Stellenfunktionen und Stellentypen Vergütungsplänen zu, indem Sie im Formular auf der Seite **Berechtigungsregeln** Berechtigungsregeln einrichten. Sie können mit dem Vergütungsplan auch mehrere Ebenen verknüpfen, die für eine bestimmte, über eine Berechtigungsregel definierte Stellenfunktion/Stellentyp-Kombination gelten. (Diese Funktion gilt für feste Vergütungspläne und variable Vergütungspläne) Planen Sie jedoch, Stellenfunktionen zur Einrichtung von Berechtigungsregeln für die Vergütungsverwaltung zu verwenden, richten Sie vor der Einrichtung von Stellen zunächst Stellenfunktionen ein. Beispiele für Stellenfunktionen finden Sie in der folgenden Tabelle.

| Stelle           | Stellenfunktion         |
|---------------|----------------------|
| Verkaufsleiter | Manager auf mittlerer Ebene    |
| Sachbearbeiter Buchhaltung    | Professionals        |

Verwalten Sie Stellenfunktionen mithilfe der Seite **Stellenfunktionen**. Geben Sie auf der Seite **Stellenarten** einen Namen und eine kurze Beschreibung des Positionstyps ein.

## <a name="compensation"></a>Vergütung
Um einem Mitarbeiter, der eine Position in einer Stelle hat, einen festen Vergütungsplan zuzuweisen, müssen Sie die Vergütungsstufen für die Stelle festlegen. Die **Vergütungsstufe** wird verwendet, wenn Mindest-, Mittel- und Höchstbeträge in einer Vergütungsstruktur (Vergütungsraster) festgelegt sind. Beim Anlegen eines festen Vergütungsplans wird die Vergütungsstruktur ausgewählt. Die Vergütungsstruktur enthält auch die Vergütungsstufe. Wenn Sie einen festen Vergütungsplan für einen Mitarbeiter auswählen, hängen die zur Auswahl stehenden Vergütungsstufen von der Stelle ab, der die Position des Mitarbeiters zugeordnet ist. Weitere Informationen über das Einrichten von Vergütungen finden Sie unter [Vergütungspläne](hr-compensation-overview.md).

## <a name="job-skills"></a>Stellenqualifikationen
Stellenqualifikationen beschreiben die Fähigkeiten, die zur Ausübung einer Stelle erforderlich sind. Jeder Stellenqualifikation muss eine Qualifikationsstufe zugeordnet werden. Die Qualifikationsstufen sind benutzerdefiniert. Sie geben an, welches Wissen oder Können für die Qualifikation erforderlich ist. Unternehmen können beispielsweise numerische Stufen wie 1 bis 5 einrichten, wobei **1** auf einen Anfänger hinweist und **5** auf einen Experten hinweist. Alternativ können Unternehmen Stufen einrichten, die als **Anfänger**, **Mittelstufe** oder **Experte** gekennzeichnet sind. Nachdem die Qualifikationsstufe festgelegt wurde, kann auch die Wichtigkeit der Qualifikation eingestellt werden. Wenn zum Beispiel ein Buchhalter über solide Kenntnisse in Microsoft Excel verfügt, kann eine Qualifikation, die **Excel-Kenntnisse** genannt wird, erstellt werden. Die Qualifikationsstufe kann dann auf **Mittelstufe** und die Wichtigkeit kann auf **Am wichtigsten** eingestellt werden.

Die Qualifikationen, die in einer Stelle vorhanden sind, können in der Qualifikationszuordnung verwendet werden. Die Qualifikationszuordnung kann die Qualifikation, die für eine Stelle erforderlich sind, und die Qualifikation, die einer Arbeitskraft zugeordnet sind, vergleichen. Sie kann dann eine prozentuale Übereinstimmung basierend auf überlappenden Qualifikationen bestimmen. Weitere Informationen zur Qualifikationszuordnung finden Sie unter [Qualifikationen konfigurieren](hr-develop-skills.md). 

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
<li><strong>Leistungsbeurteilung</strong> – Überprüfung der Arbeitsleistung jedes Verkäufers&#39;.</li>
<li><strong>ABS-Überprüfung</strong> – Genehmigen oder Ablehnen der Abwesenheitsanforderungen oder -erfassungen jedes Verkäufers&#39;.</li>
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
Im Artikel [Definieren neuer Stellen](./hr-personnel-define-jobs.md) finden Sie die detaillierte Prozedur zum Erstellen einer neuen Stelle. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
