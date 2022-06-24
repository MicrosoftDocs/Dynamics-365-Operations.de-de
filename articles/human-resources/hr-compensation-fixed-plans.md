---
title: Feste Vergütungspläne erstellen
description: In diesem Artikel wird beschrieben die Komponenten, die müssen eingerichtet werden, bevor Sie einen festen Vergütungsplan erstellen und Mitarbeiter registrieren können.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable, HcmCompensationWorkspace
audience: Application User
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: f254afc37d5afae48c3b2b3b16bd86634ac9aa3a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875741"
---
# <a name="create-a-fixed-compensation-plans"></a>Feste Vergütungspläne erstellen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Feste Vergütung bezieht sich auf das reguläre Bruttogehalt oder den Lohn eines Mitarbeiters. In diesem Artikel wird beschrieben die Komponenten, die müssen eingerichtet werden, bevor Sie einen festen Vergütungsplan erstellen und Mitarbeiter registrieren können.

Für Ihre Mitarbeiter können feste Vergütungsbeträge berechnet werden, die auf Faktoren wie Leistung, Region und Budgeterweiterungen basieren. Dynamics 365 Human Resources unterstützt die Kompensationsarten „Schritt“, „Klasse“ und „Bereich“.

## <a name="fixed-compensation-components"></a>Feste Vergütungskomponenten
### <a name="compensation-levels"></a>Vergütungsstufen

Sie können die **Vergütungsstufen** für bestimmte Stellen verwenden, um sicherzustellen, dass die Mitarbeiter, die für diese Einzelvorgänge vorgesehen, fair bezahlt werden. Auf der Seite **Vergütungsstufen** können Sie die Vergütungsstufen einrichten, die für jeden Schritt, Grad und Gehaltsplan erforderlich sind. Verwenden Sie die Schaltflächen **Nach oben** bzw. **Nach unten**, um die Stufen in der richtigen Reihenfolge nach Typ anzuordnen. Indem Sie Vergütungsstufen für eine Stelle festlegen, können Sie sicherstellen, dass alle Mitarbeiter, die diese Stelle innehaben, auf derselben Vergütungsstufe bezahlt werden.

### <a name="reference-points"></a>Referenzpunkte

**Referenzpunkte** sind die Spalten im Raster, die die Vergütungsbereiche für jede Stufe definieren. Die Vergütungsstufe ist die Zeile im Raster. Typische Referenzpunkte für einen Plan für Gradtypen sind ein Minimumwer, ein Mittelwert und ein Maximalwert. Dient zum Erstellen von Referenzpunkten für eine **Referenzpunkteinstellung**.

### <a name="compensation-grids"></a>Vergütungsraster

Nachdem Sie die Stufen und die Referenzpunkte eingerichtet haben, können diese zu einem **Vergütungsraster** kombiniert werden. Definieren Sie auf der Seite **Vergütungsraster** Informationen zum Raster. Geben Sie beispielsweise an, zu welchem Zweck das Raster entworfen wurde, mit welchem Plantyp es verwendet wird und welche Referenzpunkte oder Spalten im Raster erforderlich sind. Wenn Sie diese Informationen eingegeben haben, klicken Sie auf **Vergütungsstruktur**, um Stufen und Beträge im Raster hinzuzufügen. 

**Tipp:** Verwenden Sie die Funktion **Massenänderung** für die Vergütungsstruktur, um erste Beträge festzulegen. Erhöhen Sie diese dann schrittweise auf der Basis von Prozentsätzen oder Beträgen für Ihre Stufen oder Referenzpunkte.

### <a name="pay-frequencies"></a>Lohnzahlungshäufigkeit

Die **Lohnzahlungshäufigkeit** wird verwendet, um festzulegen, wie der Lohn oder das Gehalt eines Mitarbeiters angegeben wird (beispielsweise 10 EUR pro Stunde oder 50.000 EUR pro Jahr). Außerdem wird mit dieser Funktion die Umrechnung zwischen Stunden-, Wochen-, Monats- (12 Monate) und Jahressätzen definiert. Wenn beispielsweise ein Unternehmen, das eine 38-Stunden-Woche für seine Stundenlohnmitarbeiter verwendet, eine Lohnzahlungshäufigkeit mit dem Stundensatz 1 einrichtet, dann liegt der Wochensatz bei 38, der Monatssatz bei 164,6666666667 und der Jahressatz bei 1.976. Diese Umrechnungsraten werden verwendet, um die verschiedenen Lohnsätze zu berechnen, die im Datensatz für die feste Vergütung eines Mitarbeiters angezeigt werden.

## <a name="fixed-compensation-plans"></a>Pläne für feste Vergütung
Sie können den Plan für feste Vergütung so anlegen, dass alle von Ihnen konfigurierten Komponenten darin kombiniert werden. Um einen Plan für feste Vergütung zu erstellen, öffnen Sie die Seite **Pläne für feste Vergütung**. Hier können Sie einen Namen und eine Beschreibung für den Plan eingeben, auswählen, um welchen Plantyp es sich handelt (Schritt, Klasse oder Bereich), die Lohnzahlungshäufigkeit für den Lohnsatz des Mitarbeiters auswählen (Betrag pro Stunde, pro Jahr usw.) und einige Optionen festlegen, mit denen gesteuert wird, wie die Vergütung verarbeitet wird. 

Über die Einstellung **Außerhalb des zulässigen Bereichs** können Sie angeben, wie strikt sichergestellt werden soll, dass Vergütungsbeträge zwischen dem Mindest- und dem Höchstbetrag liegen. Durch die Toleranzeinstellung **Hart** wird durchgesetzt, dass die Vergütung innerhalb des Bereichs liegt, der für eine bestimmte Stufe definiert wurde. Wenn Sie als Toleranz die Option **Weich** festlegen, werden Sie gewarnt, wenn der Vergütungsbetrag außerhalb des Bereichs liegt. Allerdings können Sie den Vorgang fortsetzen. Wenn Sie als Toleranz **Keine** festlegen, können Sie jeden Vergütungsbetrag für einen Mitarbeiter eingeben, ohne dass eine Warn- oder Fehlermeldung angezeigt wird. 

Über die **Einstellungsregel** können Sie festlegen, ob alle Mitarbeiter unabhängig von ihrem Einstellungsdatum die gleiche Erhöhung erhalten sollen (**Einstellungsregel** = **Keine**) oder ob Mitarbeiter basierend auf der Länge ihrer Beschäftigungsdauer in diesem Zyklus einen Prozentsatz der Prämie erhalten sollen (**Einstellungsregel**  = **Prozent**). 

Eine **Bereichsauslastungsmatrix** ist hilfreich, wenn Sie entweder den Zeitraum verkürzen möchten, nach dem Mitarbeiter den Mittelwert ihres Bereichs erreichen, oder wenn Sie den Zeitraum verlängern möchten, nach dem Mitarbeiter den maximalen Referenzpunkt im Bereich erreichen können. Beispiel: Sie möchten Mitarbeitern, die in den unteren 25 Prozent ihres jeweiligen Bereichs liegen, 110 Prozent ihrer Erfolgsprämie zuteilen, während Mitarbeiter, die in den obersten 25 Prozent ihres Bereichs liegen, nur 80 Prozent ihrer Erfolgsprämie erhalten sollen, damit sie nicht so schnell das Maximum erreichen. 

Nachdem Sie die Grundlagen eines Plan für feste Vergütung definiert haben, können Sie die Vergütungsstruktur für den Plan einrichten. Klicken Sie auf **Vergütung einrichten**. Es öffnet sich ein Dialogfeld mit drei Optionen:

-   **Erstellen Sie eine neue Vergütungsmatrix**, indem Sie eine Referenzpunkteinstellung auswählen und dem Raster einen Namen geben.
-   **Erstellen Sie eine neue Vergütungsmatrix**, indem Sie eine Kopie eines vorhandenen Rasters erstellen, das Sie als Ausgangspunkt verwenden können.
-   **Verwenden Sie eine vorhandene Vergütungsmatrix**, die bereits definiert wurde. Alle Vergütungspläne, die dasselbe Raster verwenden, erhalten Updates, wenn dieses Raster geändert wird.

Nachdem Sie eine Option ausgewählt haben, wird die Seite **Vergütungsstruktur** geöffnet. Hier können Sie Änderungen am neuen Vergütungsraster oder am vorhandenen Vergütungsraster vornehmen.

## <a name="fixed-compensation-enrollment"></a>Registrierung für feste Vergütung
### <a name="determine-who-is-eligible-for-the-plan"></a>Bestimmen der Berechtigung für einen Plan

Wenn Sie Mitarbeiter für einen Plan für feste Vergütung registrieren, müssen Sie als Erstes bestimmen, wer für die im Plan definierte Vergütung berechtigt ist. Erst nachdem Sie die Berechtigung bestimmt haben, können Sie Mitarbeitern den Plan zuweisen. Um Beschäftigungsberechtigung einzurichten, öffnen Sie die Seite **Berechtigungsregeln**. Hier erstellen Sie eine neue Berechtigungsregel für den Vergütungsplan und legen die Kriterien fest, die für einen Mitarbeiter angewendet werden müssen, damit er in einen Plan aufgenommen werden kann. Sie können die Berechtigung nach Abteilung, Gewerkschaft, Vergütungsregion (Standort), Stelle, Stellenfunktion, Stellentyp oder Vergütungsstufe begrenzen. Mitarbeiter können nur für einen Vergütungsplan registriert werden, wenn sie alle Bedingungen erfüllen, die über die Berechtigungsregel festgelegt wurden. 

**Hinweis:** Berechtigungsregeln werden sowohl für Pläne für eine feste Vergütung als auch für Pläne für eine variable Vergütung verwendet, um die Berechtigung zu ermitteln. 

Die Berechtigungsregel berücksichtigt den Wert bestimmter Felder in den Datensätzen **Stelle**, **Position** und **Mitarbeiter**, um festzustellen, ob ein Mitarbeiter für einen Vergütungsplan berechtigt ist.

-   Auf der Seite **Stelle** berücksichtigt die Berechtigungsregel die folgenden Felder:
    -   Feld **Stelle**
    -   Auf der Registerkarte **Stellenklassifizierung**: die Felder **Funktion** und **Stellentyp**
    -   Auf der Registerkarte **Vergütung**: das Feld **Ebene**
-   Auf der Seite **Positionen** berücksichtigt die Berechtigungsregel die Felder **Abteilung** und **Vergütungsregion**.

Die Berechtigungsregel berücksichtigt außerdem Gewerkschaften für diesen Mitarbeiter. (Klicken Sie auf der Seite **Mitarbeiter** auf der Registerkarte **Arbeitskraft** auf **Persönliche Informationen** &gt; **Gewerkschaften**).

### <a name="define-fixed-compensation-actions"></a>Definieren von Aktivitäten bezüglich fester Vergütung

Die Option **Aktivitäten bezüglich fester Vergütung** wird verwendet, wenn Sie die Einstellungen für die feste Vergütung eines Mitarbeiters einrichten oder ändern. Über die Aktivitäten bezüglich fester Vergütung können Sie aussagekräftige Namen für die Arten von Aktivitäten angeben, die ein Leiter für Vergütungen/Bezüge ausführen kann. Unterschiedliche Aktivitätstypen basieren jeweils auf einer speziellen Logik, sodass sie zu bestimmten Zeiten verwendet werden können. 

Wenn beispielsweise die feste Vergütung für einen Mitarbeiter eingerichtet wurde, können nur Aktivitäten vom Typ **Einstellen/Neu einstellen** verwendet werden. In diesem Fall empfiehlt es sich, drei unterschiedliche Aktivitäten vom Typ **Einstellen/Neu einstellen** zu erstellen und sie **Einstellen**, **Neu einstellen** und **Versetzen** zu nennen. Sie haben dann eine aussagekräftigere Beschreibung dazu, warum ein Mitarbeiter eine feste Vergütung erhalten hat oder diese geändert wurde.

### <a name="enroll-the-employee"></a>Registrieren des Mitarbeiters

Sie können nun einen Mitarbeiter zu einem Plan für feste Vergütung zuweisen. Öffnen Sie die Seite **Mitarbeiter**, und wählen Sie den Mitarbeiter aus, der für den Vergütungsplan registriert werden soll. Klicken Sie im Aktivitätsbereich auf **Kompensation** &gt; **Fester Plan**. Sie können nun eine neue Aktivität feste Kompensation für diesen Mitarbeiter erstellen. 

**Hinweis:** Im Feld **Vergütungsplan** werden nur die Pläne angezeigt, für die ein Mitarbeiter laut den Berechtigungsregeln berechtigt ist, die für den jeweiligen Plan eingerichtet wurden. Wenn für einen Plan keine Berechtigungsregel eingerichtet wurde, sind keine Mitarbeiter für diesen Plan berechtigt. 

Es wird überprüft, ob der Vergütungsbetrag, der für einen Vergütungsplan dieser Klasse oder dieses Bereichs angegeben ist, innerhalb der Mindestwert- und Höchstwert-Referenzpunkte für die gegebene Vergütungsstufe bezüglich der Stelle des Mitarbeiters liegt. Wenn der Vergütungsbetrag außerhalb des zulässigen Bereichs liegt, wird eine Warn- oder eine Fehlermeldung angezeigt, abhängig von der Toleranzstufe, die für den Plan für feste Vergütung festgelegt wurde.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
