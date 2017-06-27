---
title: "Vergütungspläne"
description: "Manager Vergütungen und Leistungen können die Vergütungsverwaltung verwenden, um die festen und variablen Vergütungspläne für die Mitarbeiter der Organisation verwalten und verarbeiten."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3892bfab6aecd8db388d5308b36500eee70cb423
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="compensation-plans"></a>Vergütungspläne

[!include[banner](includes/banner.md)]


Manager Vergütungen und Leistungen können die Vergütungsverwaltung verwenden, um die festen und variablen Vergütungspläne für die Mitarbeiter der Organisation verwalten und verarbeiten.

### <a name="introduction"></a>Einführung

Die Vergütungsverwaltung dient zum Steuern der Abwicklung des Grundlohns und der Prämien. Sie steuern den festen Grundlohn eines Mitarbeiters und dessen Lohnsteigerungen nach Plänen für feste Vergütung. Die Zahlung leistungsbezogener Prämien, wie Boni, Leistungsprämien, Aktienoptionen und -überlassungen sowie Einmalprämien werden durch Pläne für variable Vergütung gesteuert. 

Die Mitarbeiter können einem oder mehreren Plänen beider Arten zugeordnet werden. Ein Mitarbeiter muss die folgenden Bedingungen erfüllen, um für die Registrierung in einem Vergütungsplan berechtigt zu sein:
-   Der Mitarbeiter muss eine aktive Positionszuweisung haben.
-   Der Mitarbeiter muss den Kriterien entsprechen, die durch Berechtigungsregeln für einen Vergütungsplan definiert werden.

## <a name="compensation-setup"></a>Vergütungseinstellungen
Die folgende Tabelle listet Komponenten des Vergütungsprozess auf, die Bestandteile der Vergütungspläne Ihres Unternehmens sein können.

<table>
<thead>
<tr class="header">
<th>Komponente</th>
<th>Weitere Informationen...</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aktivitäten bezüglich fester Vergütung</td>
<td>Aktivitäten bezüglich fester Vergütung werden aus zwei Gründen eingerichtet:
<ul>
<li>Aktivitäten können die Art der Informationen angeben, die erfasst werden muss, wenn sich die Vergütung eines Mitarbeiters ändert. So können z. B. festlegen, dass der Grund eine Änderung (z. B. eine Beförderung oder Zurückstufung) erfasst wird.</li>
<li>Die Aktivitäten werden auf einen Ereignisprozesses angewendet, wenn feste Vergütungspläne berechnet werden.  Aktivitäten können sicherstellen, dass eine Berechnung angewendet wird, wenn feste Vergütungspläne verarbeitet werden. Aktivitäten vom Typ Vergleich vergleichen beispielsweise die Bezahlung eines Mitarbeiters mit dem Mindestreferenzpunkt für die Stufe des Mitarbeiters und stellen sicher, dass dem Mitarbeiter mindestens das Minimum gezahlt wird.</li>
</ul></td>
</tr>
<tr class="even">
<td>Ebenen</td>
<td>Ebenen werden Stellen zugeordnet, und alle mit der Stelle verknüpften Positionen übernehmen die Stellenreferenz. Sie können eigenständige Ebenen für die drei Arten von Vergütungsplänen erstellen: Abschluss, Bereich und Schritt.</td>
</tr>
<tr class="odd">
<td>Matrix für Bereichsauslastung</td>
<td>Eine Bereichsauslastungsmatrix unterstützt Sie bei der Verschiebung von Mitarbeitern zum Kontrollpunkt für ihre Stellen. Darüber hinaus kann auch durch die Bereichsauslastung die Fairness des Lohnsatzes innerhalb des Unternehmens kontrolliert werden, ohne dabei die Leistung eines einzelnen Mitarbeiters oder die Leistung des gesamten Unternehmens zugrunde zu legen. So erhalten Mitarbeiter, die in ihrem Bereich geringer bezahlt werden, eine höhere prozentuale Steigerung als Mitarbeiter, die höher im Bereich bezahlt werden. Auf diese Weise können Sie Eigenkapitalunterschiede systematisch ausgleichen. Die Bereichsauslastung wird wie folgt berechnet: (Fester Lohnsatz - Bereichs-Minimum) ÷ (Höchstwert des Bereichs - Mindestwert des Bereichs).</td>
</tr>
<tr class="even">
<td>Referenzpunkteinstellungen</td>
<td>Eine Referenzpunkteinstellung umfasst eine Gruppe von Referenzpunkten, bei denen es sich um Bereiche in einer Lohnsatzmatrix handelt. Jeder Bereich kann einem Lohnsatz zugeordnet werden. Beispielsweise haben Abschlusspläne häufig Referenzpunkte zum Minimum, Mittelwert und Maximum.</td>
</tr>
<tr class="odd">
<td>Vergütungsmatrix</td>
<td>Eine Vergütungsmatrix ist eine Gruppe von Referenzpunkten und Ebenen, die Sie verwenden, um eine Vergütungsstruktur zu erstellen.</td>
</tr>
<tr class="even">
<td>Vergütungsstruktur</td>
<td>Eine Vergütungsstruktur ist eine Vergütungsmatrix, der Lohnsätze mit Referenzpunkten für jede Stufe zugeordnet sind.</td>
</tr>
<tr class="odd">
<td>Berechtigungsregeln</td>
<td>Berechtigungsregeln werden verwendet, um Mitarbeiter in bestimmten Stellen, Stellenfunktionen, Stellentypen, Abteilungen, Gewerkschaften oder Vergütungsregionen, die durch bestimmte Vergütungspläne abgedeckt werden, zu identifizieren. Sie müssen Berechtigungsregeln für Variablen und feste Vergütung erstellen, um Mitarbeiter im Plan zu erfassen. Nachdem Sie die Berechtigungsregeln für einen Vergütungsplan festgelegt haben, können Sie die Stufen des Plans definieren, die für die entsprechenden Stellen gelten sollen.</td>
</tr>
<tr class="even">
<td>Lohnzahlungshäufigkeit</td>
<td>Lohnzahlungshäufigkeiten werden verwendet, um den Zeitraum zu definieren, für die der Vergütungseinstellungen angegeben wird.  Beispielsweise hilft Ihnen die Lohnzahlungshäufigkeit zu verstehen, ob der Kompensationsbetrag als jährliches Gehalt oder als Stundenlohn  angegeben ist. Zahlungshäufigkeiten werden auch verwendet, um Umrechnungsfaktoren einzurichten, um Vergütung von monatlich, wöchentlich, zweiwöchentlich und stundenbasiert in eine jährliche Lohnzahlungshäufigkeit umzuwandeln.</td>
</tr>
<tr class="odd">
<td>Ausgleichsregionen</td>
<td>Vergütungsregionen werden verwendet, um Mitarbeitervergütungen auf Basis des Standorts des Arbeitsplatzes anzugeben.</td>
</tr>
<tr class="even">
<td>Kontrollpunkt</td>
<td>Der Kontrollpunkt definiert, wie der ideale Lohnsatz für alle Mitarbeiter einer Vergütungsstufe aussieht. Bei bewerteten Planungsstrukturen stellen die Kontrollpunkte üblicherweise die Bereichsmitte dar. Bei flexiblen Strukturen wird nur selten auf Kontrollpunkte zurückgegriffen. Sie können den Kontrollpunkt für einen Plan für feste Vergütung im Formular "Pläne für feste Vergütung" angeben.</td>
</tr>
<tr class="odd">
<td>Stellenfunktionen</td>
<td>Stellenfunktionen werden verwendet, um Vergütungspläne für bestimmte Stellen zu klassifiziert und zu filtern.</td>
</tr>
<tr class="even">
<td>Einzelvorgangstypen</td>
<td>Stellentypen werden verwendet, um Vergütungspläne für bestimmte Stellen zu klassifiziert und zu filtern.</td>
</tr>
<tr class="odd">
<td>Typen für variable Vergütung</td>
<td>Die Typen für variable Vergütungen, z. B. eine Aktienprämien oder Bargeldprämien, werden in Plänen für variable Vergütung angewendet.</td>
</tr>
<tr class="even">
<td>Vergütungsraster</td>
<td>Vergütungsraster enthalten die Vergütungsstruktur.  Vergütungsraster können durch mindestens eine Vergütung verwendet werden.</td>
</tr>
<tr class="odd">
<td>Leistungspläne</td>
<td>Leistungspläne werden verwendet, um Leistung einer Verteilungsmatrix zuzuordnen, um den Plan in einer Strategie für leistungsbezogene Bezahlung zu verwenden.</td>
</tr>
<tr class="even">
<td>Leistungsbewertungen</td>
<td>Leistungsbewertungen werden in Leistungsplänen verwendet, um den Betrag für eine Verdienst- oder eine Leistungsprämie zu ermitteln.</td>
</tr>
</tbody>
</table>

## <a name="process-events"></a>Prozessereignisse
Ein Prozessereignis kalkuliert Vergütungsinformationen für eine bestimmte Periode für alle Mitarbeiter, die für einen oder mehrere Pläne mit fester oder variabler Vergütung registriert sind. Ein Prozessereignis kann mehrmals zum Testen oder Aktualisieren berechneter Vergütungsergebnisse ausgeführt werden.

<a name="compensation-events"></a>Vergütungsereignisse
-------------------

Jedes Mal, wenn ein Prozessereignis ausgeführt wird, wird ein Kompensationsereignis erstellt.  Kompensationsereignisse enthalten die Ergebnisse des Kompensationsprozesses für jeden Mitarbeiter, das in diesen Prozessereignis enthalten ist.  Wenn die Berechnungen korrekt sind, können Sie das Prozessereignis laden, um die Vergütungsdatensätze für die Mitarbeiter zu aktualisieren, die vom Prozessereignis betroffen sind.

## <a name="recommendations"></a>Empfehlungen
Nachdem Sie ein Prozessereignis ausgeführt haben, können Sie Anpassungen an Lohnsteigerung oder Prämienbetrag eines Mitarbeiters basierend auf den berechneten Richtlinien des Prozessereignisses empfehlen. Um Empfehlungen für Mitarbeiter zu machen, müssen Sie Empfehlungen aktivieren, wenn Sie Vergütungspläne einrichten oder das Prozessereignis erstellen.




