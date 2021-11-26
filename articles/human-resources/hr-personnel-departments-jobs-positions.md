---
title: Verwalten der Belegschaft mittels Abteilungen, Stellen und Positionen
description: Dieses Thema beschreibt grundlegende Informationen über Abteilungen, Stellen und Positionen, die innerhalb der Personalverwaltung als Organisationselemente verwaltet werden.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 51335cba0e0dce755ce36fbe13c6294fca58d797
ms.sourcegitcommit: 1cc56643160bd3ad4e344d8926cd298012f3e024
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2021
ms.locfileid: "7731807"
---
# <a name="organize-your-workforce-by-using-departments-jobs-and-positions"></a>Verwalten der Belegschaft mittels Abteilungen, Stellen und Positionen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Abteilungen, Stellen und Positionen sind Organisationselemente, die innerhalb der Personalverwaltung verwaltet werden. Dieses Thema behandelt die grundlegenden Informationen zu diesen Elementen. 

Im folgenden Beispiel werden die Konzepte veranschaulicht, die in diesem Artikel beschrieben werden.

|**Abteilung**|**Position**|**Job**|
|---|---|---|
|**Umsatz**|Verkaufsleiter (Osten)|Verkaufsleiter|
|**Verkäufe**|Verkaufsleiter (Westen)|Verkaufsleiter|
|**Verkäufe**|Verkaufsleiter (Zentral)|Verkaufsleiter|
|**Buchhaltung**|Supervisor Buchhaltung|Leiter Buchhaltung|
|**Buchhaltung**|Buchhaltung-A|Sachbearbeiter Buchhaltung|
|**Personalverwaltung**|Leiter der Personalabteilung (Ost)|Leiter der Personalabteilung|
|**Personalverwaltung**|Leiter der Personalabteilung (Westen)|Leiter der Personalabteilung|
|**Personalverwaltung**|Leiter der Personalabteilung (zentral)|Leiter der Personalabteilung|


##  <a name="departments"></a>Abteilungen

Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen Funktionsbereich einer Organisation darstellt, die für einen bestimmten Bereich der Organisation, beispielsweise Vertrieb oder Buchhaltung zuständig ist. Eine Abteilung wird verwendet, um zu Funktionsbereiche zu berichten und sie kann Gewinn- und Verlustzuständigkeit haben. Eine Abteilung kann möglicherweise auch eine Gruppe von Kostenstellen umfassen. Verkäufe, Buchhaltung und Personalverwaltung sind einige Beispiele von Abteilungen in einer Organisation.

## <a name="jobs-and-positions"></a>Stellen und Positionen
Ein Einzelvorgang ist eine Sammlung von Aufgaben und Zuständigkeiten, die für eine Person, die eine Tätigkeit ausführt, obligatorisch sind. Eine Position ist eine einzelne Instanz eines Einzelvorgangs. Zuständigkeitsbereiche, Arbeitsaufgaben, Stellenfunktionen, Qualifikationen, Bescheinigungen und Ausbildungsinformationen, die für eine Stelle erforderlich sind, sind auch für Positionen erforderlich, die einer Stelle zugeordnet sind.
### <a name="job-tasks"></a>Arbeitsaufgaben
Sie können Arbeitsaufgaben erstellen, die die grundlegenden Aufgaben beschreiben, die eine Arbeitskraft in einer Position für diesen Einzelvorgang ausführen muss. Die gleiche Arbeitsaufgabe kann mehreren Einzelvorgängen hinzugefügt werden, und Positionen für diese Einzelvorgänge erben die Arbeitsaufgaben. Beispiele für Stellenaufgaben sind in der folgenden Tabelle aufgeführt.

<table>
<thead>
<tr class="header">
<th>Einzelvorgang</th>
<th>Arbeitsaufgabe</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Verkaufsleiter</td>
<td><ul>
<li><span class="input">Leistungsbeurteilung</span> – Überprüfung der Arbeitsleistung jedes Verkäufers.</li>
<li><span class="input">ABS-Überprüfung</span> – Genehmigen oder Ablehnen der Abwesenheitsanforderungen oder -erfassungen jedes Verkäufers.</li>
</ul></td>
</tr>
<tr class="even">
<td>Sachbearbeiter Buchhaltung</td>
<td><span class="input">FIN-Bericht</span> – Wöchentliche Finanzberichte dem Leiter der Finanzabteilung präsentieren.</td>
</tr>
</tbody>
</table>

### <a name="job-functions"></a>Stellenfunktionen

Stellenfunktionen sind wie Arbeitsaufgaben. Eine Stellenfunktion beschreibt eine oder mehrere Aufgaben, Pflichten und Zuständigkeiten, die einer Stelle zugewiesen sind. Stellenfunktionen können Einzelvorgängen zugewiesen werden und verwendet werden, um Berechtigungsregeln für Vergütungspläne einzurichten und zu implementieren. Beispiele für Stellenfunktionen sind in der folgenden Tabelle aufgeführt.

| Einzelvorgang           | Stellenfunktion                                                |
|---------------|-------------------------------------------------------------|
| Verkaufsleiter | Verw-Personen – Verwaltet Personen, die Ihnen unterstellt sind.               |
| Sachbearbeiter Buchhaltung    | FIN-Überprüfung – Verwalten von Finanzdaten für eine Gruppe von Konten. |

### <a name="job-types"></a>Einzelvorgangstypen

Verwenden Sie Stellentypen, um ähnliche Stellen in Kategorien zu klassifizieren. Stellentypen können, wie Stellenfunktionen, Stellen zugewiesen und verwendet werden, um Berechtigungsregeln für Vergütungspläne einzurichten und zu implementieren. Die folgende Liste enthält einige Beispiele für Stellentypen:
-   Vollzeit
-   Teilzeit
-   Lohn
-   Stundenlohn

### <a name="areas-of-responsibility"></a>Zuständigkeitsbereiche

Verwenden Sie Zuständigkeitsbereiche, um die Arbeitsrollen, Prozesse und Produkte anzugeben, für die eine Arbeitskraft in einer Position für diesen Einzelvorgang zuständig sein würde. Ein Beispiel für einen Zuständigkeitsbereich für eine Stelle mit dem Titel "Buchhalter" könnte "Finanzberichterstellung für Produkt A" sein.

## <a name="positions"></a>Positionen

Positionen ist ein wichtiges Element der untergeordneten Ebene einer Organisationshierarchie. Eine Position ist eine einzelne Instanz eines Einzelvorgangs. Beispielsweise ist die Position, "Verkaufsleiter (Ost) derzeit eine der Positionen, die der Stelle "Verkaufsleiter zugeordnet wird. Positionen sind in einer Abteilung und werden Arbeitskräften zugewiesen.
### <a name="position-creation-and-maintenance"></a>Erstellung und Verwaltung von Positionen

-   Sie können eine Historie von positionsbezogenen Systemänderungen in einer einfach zugänglichen Listenseite anzeigen.
-   Sie können Ursachencodes erstellen, die Ihre Benutzer auswählen können, wenn sie Positionen erstellen oder ändern.
-   Sie können Mitarbeiteraktivitätstypen erstellen und einen Nummernkreis den Mitarbeiteraktivitäten zuweisen.
-   Sie können den Workflow so einrichten, dass Positionshinzufügungen und -änderungen Genehmigung erfordern können.

### <a name="position-duration"></a>Positionsdauer
Jede Position hat einen Zeitraum, in dem die Position gültig ist. Diese Zeit wird als Dauer bezeichnet. Beispielsweise haben Sommerpositionen eine Dauer vom 1. Mai 2015 bis zum 31. August 2015.

### <a name="worker-assignments"></a>Arbeitskraftzuweisungen
Wenn Sie eine Arbeitskraft einer Position zuweisen, füllen Sie diese Position aus. Sie können Arbeitskräfte mehreren Positionen zuordnen, aber nur eine Arbeitskraft gleichzeitig kann einer Position zugewiesen werden.

### <a name="reporting-relationships"></a>Berichtsbeziehungen
Positionen sind wichtiges Elemente der untergeordneten Ebene einer Organisationshierarchie. Auf der Seite **Position** können Sie die Position angeben, der eine Position untergeordnet ist. Wenn Sie eine Arbeitskraft einer Position zuweisen, die einer andere Position untergeben ist, erstellen Sie Berichtbeziehung zwischen den Arbeitskräften, die den beiden Positionen zugewiesen werden. Beispielsweise ist Stellung "Buchhalter-A" der Stellung "Buchhaltungs-Vorgesetzter" untergeben. Ana Bowman wird der Position „Buchhaltungs-Vorgesetzter“ zugewiesen und Felix Hendersen wird der Position „Buchhalter-A“ zugewiesen. Das bedeutet, dass Felix Henderson Ana Bowman unterstellt ist. 

Wenn Ihre Organisation eine Matrixhierarchie oder eine andere benutzerdefinierte Hierarchie verwendet, können Sie Positionshierarchietypen einrichten und dann Berichtsbeziehungen zu den Positionen für jede Hierarchie hinzufügen, Sie einrichten. Beispielsweise ist Olivia Wilson eine Generaldirektorin bei Adventure Works und wird der Position „Generaldirektor“ zugewiesen. Olivia verwaltet die Entwicklung eines Produkts, das verwendet wird, um Produkte zu säubern. Olivia fordert jemanden von der Buchhaltung an, um mit den Finanzen zum Entwickeln des Produkts zu helfen. Daher hat sie Felix Henderson herangezogen, um dies zu übernehmen. Felix ist direkt Ana Bowman unterstellt, arbeitet aber auch mit Olivia Wilson an der Arbeit, die den Finanzen zum Entwickeln des Gerätereinigers zugeordnet ist. 

Für das vorherige Beispiel würden Sie die folgenden Aufgaben ausführen, um das Arbeitsverhältnis zwischen Felix Henderson und Ana Bowman einzurichten:
1.  Erstellen Sie einen benutzerdefinierten Positionshierarchietyp mit der Bezeichnung "Gerät" erstellt, um eine Hierarchie zu erstellen, die die Positionen enthält, die für die Arbeit an dem Gerätereinigerprodukt zuständig sind.
2.  Weisen Sie die Generaldirektorposition als die Position zu, der die Buchhalter-A-Position in der Hierarchie "Geräte" unterstellt sein soll.

Verwenden Sie die Seite **Positionshierarchie**, um die Berichtstruktur von Positionen anzuzeigen. Wenn Sie mehrere Positionshierarchien haben, können Sie die Hierarchie für jeden Hierarchietyp in der **Positionshierarchie** anzeigen. Sie können auch nach einer Position mit der Positionskennung oder dem Namen der Arbeitskraft, die der Position zugeordnet ist, suchen. Die **Positionshierarchie** ist eine Organisationshierarchie.

## <a name="date-effective-records"></a>Gültigkeitsdatum (Datensätze)
Für einige Datensätze können Sie zukünftige Änderungen am Datensatz angeben. Die folgenden Informationen haben ein Gültigkeitsdatum.

<table>
<thead>
<tr class="header">
<th>Datensätze</th>
<th>Informationen zum Gültigkeitsdatum</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Einzelvorgänge</td>
<td><ul>
<li>Einige detaillierte Stellendaten</li>
<li>Stellenklassifizierungsinformationen</li>
<li>Vergütungsinformationen</li>
</ul></td>
</tr>
<tr class="even">
<td>Positionen</td>
<td><ul>
<li>Einige detaillierte Positionsinformationen</li>
<li>Arbeitskraftzuweisungen</li>
<li>Dauerangaben für Positionen</li>
<li>Positionshierarchien</li>
</ul></td>
</tr>
</tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
