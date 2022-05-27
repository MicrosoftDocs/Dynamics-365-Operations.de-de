---
title: Positionsplanung
description: Ausgaben, die Arbeitskräften zugeordnet sind, machen häufig einem Großteil der Kosten einer Organisation aus. Mit der Positionsplanung können Sie diese Ausgaben planen und in die Planung von Budgets einbeziehen.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPositionForecast
audience: Application User
ms.reviewer: kfend
ms.custom: 64413
ms.assetid: 35e791d2-1905-4808-a579-7f181ddddd91
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9cd30292c38d1cad6aeacebc1e335d28fd6c26dc
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723222"
---
# <a name="position-forecasting"></a>Positionsplanung

[!include [banner](../includes/banner.md)]

Ausgaben, die Arbeitskräften zugeordnet sind, machen häufig einem Großteil der Kosten einer Organisation aus. Mit der Positionsplanung können Sie diese Ausgaben planen und in die Planung von Budgets einbeziehen.

## <a name="position-forecasting-in-budget-planning"></a>Positionsplanung in der Budgetplanung

[![Komponenten der Positionsprognose.](./media/graphic-top.png)](./media/graphic-top.png) 

Die Positionsplanung verwendet drei Hauptkomponenten, um genaue Budgetbeträge für Positionsausgaben bereitzustellen. Diese Beträge können in einen Budgetplan für Budgetberechnungen einfließen. 

Der Hauptbestandteil ist die **Planungsposition**, die alle Kostendaten darstellt, die einer einzelnen Position zugeordnet sind. Sie können mehrere Versionen einer Planungsposition erstellen, indem Sie ein anderes Budgetplanszenario zu jeder Version zuweisen. Mehrere Versionen lassen einen sich wiederholenden Ansatz für die Budgetierung zu und ermöglichen Ihnen den Vergleich von Was-Wenn-Szenarios. Jede Planungsposition hat eine entsprechende Position in der Personalverwaltung.

Ein **Budgetkostenelement** ist eine Einstellungskomponente, die spezifische Kosten darstellt, die einer Position, wie Grundlohn, vom Arbeitgeber bezahlte Krankenversicherung, Mobiltelefonzulagen usw. zugeordnet ist. Ein Budgetkostenelement umfasst das Hauptkonto, das für die Kosten und die Optionen zur Berechnung verwendet wird. Jedes Budgetkostenelement kann mehreren Planungspositionen zugewiesen werden. 

Eine **Vergütungsgruppe** ist eine optionale Einstellungskomponente, die verwendet wird, um einen Satz von Budgetkostenelementen und Planberechnungen auf die Positionen anzuwenden, die ähnliche Lohnmerkmale haben. Eine Vergütungsgruppe kann ein Vergütungsraster von Lohnsätzen enthalten. Wenn die Gruppe einer Planungsposition zugeordnet ist, können eine Ebene und ein Schritt im Raster die Einnahmen der Planungsposition zuweisen. Der Satz von Kostenelementen wird automatisch hinzugefügt.

### <a name="position-forecasting-processes"></a>Positionsplanungsprozesse

[![Illustration von Positionsprognoseprozessen.](./media/graphic1b.png)](./media/graphic1b.png) 

In einem typischen Prozess für die Positionsplanung erstellen Sie zunächst die Einstellungskomponenten (Budgetkostenelemente und Vergütungsgruppen). Planungspositionen werden dann anhand von vorhandenen Positionen generiert. Sie können Anpassungen nach Bedarf vornehmen. So können Sie Positionen hinzufügen oder beenden, Lohnsätze und Vorteilskosten ändern sowie Lohnerhöhungen hinzufügen. Sie können mehrere Versionen einer Planungsposition erstellen, um den Vergleich verschiedener Budgetszenarios zu vereinfachen. Danach können Sie die Planungspositionen in die Budgetpläne einfügen und die Kosten aus den Prognosepositionen als Budgetplanpositionen einführen.

Sie können zusätzliche Planungspositionsversionen erstellen, während Budgetpläne überarbeitet werden. Diese neuen Versionen bieten eine Basis für die Überarbeitungen.

## <a name="position-forecasting-setup"></a>Einrichten der Positionsplanung
[![Illustration mit Hervorhebung – Setup.](./media/graphic2-1024x327.png)](./media/graphic2.png)

### <a name="budget-cost-elements"></a>Budgetkostenelemente

Budgetkostenelemente werden verwendet, um Kostendetails für eine Planungsposition zu definieren. Diese Details enthalten die Art der Kosten, wie die Kosten berechnet werden und ob die Kosten mehreren Datumsangaben zugewiesen werden, wenn die Planungsposition in einem Budgetplan enthalten ist. 

Bestimmte Felder definieren das Verhalten des Budgetkostenelements. Jedem Budgetkostenelement wird der Budgetkostentyp **Einnahmen**, **Vergütung**, **Steuern** oder **Sonstiges** zugewiesen. Die Budgetkostentypen werden hauptsächlich verwendet, um Summen zu berechnen. Der Wert **Planungspositionsüberschreibung** gibt an, ob die Beträge im Element in der Planungsposition geändert werden können. Das Feld **Zuordnungsmethode** wird verwendet, wenn eine Planungsposition zu einem Budgetplan hinzugefügt wird. Sie können den Kostenbetrag auf separate Budgetplanpositionen mit unterschiedlichen Daten auf einer monatlichen, vierteljährlichen, wöchentlichen oder zweiwöchentlichen Grundlage aufteilen. Wenn Sie ein Startdatum auswählen, ordnen Sie die Kosten als einzelnen Betrag an dem Startdatum zu, das in der Planungsposition festgelegt ist. 

Die Berechnung des Kostenbetrags des Budgetkostenelements verwendet Gültigkeitsdaten, um die Verwendung des gleichen Kostenelements in verschiedenen Perioden zu ermöglichen. Ein einzelnes Hauptkonto wird in jeder Periode zugewiesen, zusammen mit einem Prozentsatz oder einem jährlichen Betrag, der den Kostenbetrag angibt. Ein Budgetkostenelement kann einen Prozentsatz anderer Kostenelemente oder des jährlichen Betrags, aber nicht beides verwenden. Sie können auch eine jährliche Grenze angeben. 

Wenn das Kostenelement auf einem Prozentsatz basiert, müssen Sie die Budgetkostenelemente angeben, die als Grundlage für die Berechnung verwendet werden.

**Beispiel** 

Jodis Organisation bietet eine Ausbildungsvergütung von 5 Prozent des Grundlohns eines Mitarbeiters. Jodi möchte ein Budgetkostenelement für diese Kosten erstellen. Sie erstellt ein neues Budgetkostelement und weist den Budgetkostentyp **Vergütung** zu.

Jodis möchte nicht, dass Manager den Betrag der Vergütung ändern. Daher wählt sie **Kostenänderungen nicht zulassen** im Feld **Planungspositionsüberschreibung** aus. Die Organisation wünscht, dass diese Kosten jeden Monat gleichmäßig zugewiesen werden. Daher wählt Jodi **Vierteljährlich** im Feld **Zuordnungsmethode** aus. 

Danach fügt Jodi eine Kostenberechnungsposition hinzu, legt die Datumsangaben und ein Hauptkonto fest und gibt als Prozentsatz **5,00** ein. Die Organisation hat eine Kapazität von 5.000 Euro pro Jahr für diese Vergütung. Daher gibt Jodi diesen Betrag als das jährliche Limit ein. 

Schließlich fügt Jodi alle Einkommenkostenelemente hinzu, die als Berechnungsgrundlage für den Grundlohn verwendet werden. Das Budgetkostenelement kann jetzt verwendet werden.

### <a name="compensation-groups"></a>Vergütungsgruppen

Vergütungsgruppen können verwendet werden, um Planungspositionen zu gruppieren, die ähnliche Vergütungsattribute haben. Sie können auch verwendet werden, um die Einnahmen einer Planungsposition und die jährlichen Erhöhungen zu definieren und einen Satz allgemeiner Budgetkostenelemente zuzuweisen. 

Eine Grundfunktion von Vergütungsgruppen ist, einen Satz Budgetkostenelemente zu einer Prognoseposition zuzuweisen. Daher können Vergütungsgruppen verwendet werden, um Gemeinkosten wie Vergütungspläne und Steuern hinzuzufügen. Ein Manager, der eine Planungsposition erstellt, muss nicht alle Kostenelemente kennen, die hinzugefügt werden müssen. Stattdessen können die Kostenelemente hinzugefügt werden, wenn die Vergütungsgruppe aktiviert ist. Die Elemente werden in den Vergütungsgruppeneinstellungen auf der Registerkarte **Budgetkostenelemente** hinzugefügt. 

Vergütungsgruppen können die Ertragswerte für eine Planungsposition außerdem bestimmen. Sie richten eine Gruppe ein, um entweder eine stündliche Grundlage oder eine Basis des jährlichen Gehalts zu verwenden, um Planungspositionseinkommen zu berechnen. Auf der Registerkarte **Vergütungssatztabellen** bestimmt ein Vergütungsraster von Lohnsätzen die Einnahmen, die einer Planungsposition hinzugefügt werden, auf einer zugewiesene Ebene und einem zugewiesenen Schritt. Diese Raster können auf vorhandenen Vergütungsrastern in der Personalverwaltung basieren. Alternativ können Sie neue Vergütungsraster für die Budgetplanung erstellen. 

Mit den Gültigkeitsdaten und den Ablaufdaten in den Vergütungssatztabellen können Sie Lohnsätze an einem beliebigen Datum ändern. Diese Funktion ist hilfreich, wenn bei einer Verhandlung eine pauschale Erhöhung mitten in einem Budgetzyklus ausgehandelt wurde. In diesem Fall Ändern Sie das Ablaufdatum der vorhandenen Tabelle Tag vor dem Datum der Satzänderung und fügen eine neue Satztabelle hinzu, die am neuen Datum beginnt. Wenn Sie eine neue Satztabelle erstellen, wenn Sie den Wert **Erstellen eines neuen Vergütungsraster von einem vorhandenen Raster** wählen, können Sie eine vorhandene Satztabelle aus der Personalverwaltung auswählen. Wählen Sie in der Satztabelle, die erstellt wird, die Option **Massenänderung**, um einen Prozentsatz oder eine feste Betragserhöhung oder -verringerung auf alle Sätze des Rasters anzuwenden. 

Die Felder **Zeitplan für Erhöhungen** und **Datum der Erhöhung** in der Vergütungsgruppe werden verwendet, wenn Sie Lohnerhöhungen erstellen müssen, weil Positionen von einem Schritt zum nächsten wechseln. Eine jährliche Lohnerhöhung ist ein typisches Szenario. Der Zeitplan für Erhöhungen bestimmt, ob das Jahrestagsdatum der Position oder ein einzelnes allgemeines Datum für die Schritterhöhung verwendet wird. Der Zeitplan gilt für alle Planungspositionen in der Vergütungsgruppe. 

Das Einkommenskostenelement, das für die Lohngruppe aktiviert ist, wird verwendet, wenn Sie Einkünfte für die Planungspositionen in der Gruppe erstellen, einschließlich ihres Grundlohns und aller Schritterhöhungen. Das Feld **Plan für feste Vergütung** verknüpft die Vergütungsgruppe mit einem Plan für feste Vergütung in der Personalverwaltung. Dieser Link kann Informationen bezüglich fester Vergütung einer Arbeitskraft einer Planungsposition zuweisen und kann das Budget genauer machen. Bedenken Sie, dass die Struktur für das Vergütungsraster (die Ebenen und die Schritte) für die Vergütungsgruppe mit der Struktur des festen Vergütungsplans übereinstimmen soll. Andernfalls kann das System die Vergütungsgruppe und den festen Vergütungsplan nicht ordnungsgemäß verknüpfen.

## <a name="creating-forecast-positions"></a>Planungspositionen erstellen
[![Illustration mit Hervorhebung „Prognosepositionen erstellen“.](./media/graphic3-1024x327.png)](./media/graphic3.png)

### <a name="creating-forecast-positions-for-existing-positions"></a>Erstellen von Planungspositionen für vorhandene Positionen

Für die genauste Budgetplanung können Sie Planungspositionen erstellen, indem Sie Details vorhandener Positionen verwenden, unabhängig davon, ob die Position gerade ausgefüllt ist oder nicht. 

Die Funktion **Vorhandene Positionen hinzufügen** zeigt alle Positionen für eine Organisation an. Wenn Sie das Datum **Per Datum** festlegen, können Sie die Liste der Positionen ändern, sodass sie die Positionen enthält, die an einem Datum in der Vergangenheit existierten oder in der Zukunft existieren (beispielsweise Start des nächsten Budgetzyklus). Wählen Sie einen Budgetplanungsprozess und ein Budgetplanszenario, wählen Sie Positionen in der Liste und klicken Sie dann auf **OK**, um Planungspositionen für die ausgewählten Positionen zu erstellen. Beachten Sie, dass Sie nur eine geplante Position für jede vorhandene Position in einem Budgetplanungsprozess und -szenario erstellen können. Sie können jedoch weitere Versionen erstellen, indem Sie verschiedene Budgetplanszenarios zuweisen. 

Wenn Budgetkostenelemente der Position in der Personalverwaltung zugewiesen wurden, werden diese Budgetkostenelemente auch der Planungsposition zugewiesen und die standardmäßigen Beträge verwendet. Das Feld **Zugewiesene Arbeitskraft** in der Prognoseposition wird auf den Namen der Arbeitskraft festgelegt, die der Position zugewiesen wird, wenn eine Arbeitskraft zugewiesen ist. Dieses Feld ist ein einfaches Textfeld. Kein direkter Link wird erstellt. 

Wenn ein Budgetkostenfaktor aktiviert ist, wird der jährliche Betrag der festen Vergütung der Prognoseposition zugeordnet, indem das ausgewählte Kostenelemente verwendet wird, vorausgesetzt, dass die zugewiesene Arbeitskraft einen festen Vergütungsplan hat. Wenn die Arbeitskraft keinen festen Vergütungsplan hat oder wenn keine Arbeitskraft zugewiesen ist, wird der Standardbetrag für das Budgetkostenelement verwendet. 

Wenn die Option **Vergütungsgruppe zuweisen** auf **Ja** festgelegt ist, wenn die Arbeitskraft, die der Position zugewiesen ist, einen Schritt-basierten festen Vergütungsplan hat, der mit einer Vergütungsgruppe (wie im Vorfeld beschrieben) verknüpft ist, werden die Ebene und der Schritt von der Arbeitskraft der Planungsposition zusammen mit der Vergütungsgruppe zugewiesen. Das Budgetkostenelement vom Typ Einkünfte aus der Vergütungsgruppe wird der Planungsposition hinzugefügt, und der Lohnsatz der Ebene und des Schritts aus der Vergütungsgruppe werden verwendet. 

Die Einstellung der Option **Vergütungsgruppe zuweisen** besitzt Vorrang vor der Einstellung der **Budgetkostenelementzuweisung**. Bis zu zwei Einstellungen können gleichzeitig verwendet werden. 

[![„Zuordnen einer Vergütungsgruppe“ Diagramm](./media/graphic4.png)](./media/graphic4.png) 

Eine weitere Option ist, ein Jahrestagsdatum zuzuweisen. Das ausgewählte Datum (reguliertes Startdatum, Arbeitskraftstartdatum, Beschäftigungsstartdatum oder Dienstalter) aus der zugewiesenen Arbeitskraft wird dann als Jahrestag der Planungsposition festgelegt und wird zu Informationszwecken verwendet und wenn Lohnerhöhungen generiert werden.

### <a name="creating-new-forecast-positions"></a>Neue Planungspositionen erstellen

Sie können neue Planungspositionen auf zwei Arten erstellen: über das Kopieren einer Position der vorhandenen Planung und mithilfe einer vollständig neuen Planungsposition. 

Wenn eine Planungsposition aktiviert ist, wählen Sie **Ausgewählte Planungsposition kopieren**, um eine neue Planungsposition zu erstellen, deren Planungsstatuns dessen **Vorgeschlagen** ist. Diese Planungsposition hat alle gleichen Daten wie die Planungsposition, die kopiert wurde, außer die zugewiesene Arbeitskraft und eventuelle Hinweise auf Budgetkostenelemente. Beachten Sie, dass eine entsprechende neue Position auch in der Personalverwaltung erstellt wird. Diese Position hat die Beschreibung **Durch Planung erstellt**. 

Sie können auch eine vollständig neue Planungsposition erstellen. Wählen Sie einen vorhandenen Einzelvorgang aus, und auch wählen Sie den Budgetplanungsprozess aus und das Budgetplanszenario. Sie können ggf. weitere Details hinzufügen, die Sie hinzufügen möchten. Noch einmal wird gleichzeitig eine neue Position in der Personalverwaltung erstellt.

## <a name="working-with-forecast-positions"></a>Arbeiten mit Planungspositionen
[![Illustration mit Hervorhebung „Prognosepositionen ändern“.](./media/graphic5-1024x327.png)](./media/graphic5.png)

### <a name="multiple-versions-of-a-forecast-position"></a>Mehrere Versionen einer Planungsposition

Sie können Planungspositionen ändern, um entweder bekannte Änderungen für den Budgetzyklus anzuwenden oder vorgeschlagene Änderungen zu modellieren. Häufig wird eine Basislinie von Planungspositionen erstellt, werden Kopien für diese Planungspositionen erstellt und dann zum Modellieren von verschiedenen Gruppen von Änderungen verwendet. Die Kopien werden einem anderen Budgetplanszenario zugewiesen, sind jedoch mit den Planungspositionen identisch, aus denen sie kopiert wurden, zumindestens bis Änderungen vorgenommen werden. Die Vorlagen und Kopien teilen die gleiche Position in der Personalverwaltung. 

Die Funktion **In Szenario kopieren** stellt diese Funktionalität bereit. Beachten Sie, dass jede Personalverwaltungsposition nur eine Planungsposition in jedem Budgetplanszenario haben kann.

### <a name="modifying-forecast-positions"></a>Ändern von Planungspositionen

Änderungen, die an Planungspositionen vorgenommen werden, sind auf diese Planungspositionen beschränkt. Die Änderungen wirken sich nicht auf die Positionsdatensätze in der Personalverwaltung aus. Die meisten Änderungen werden auf die Planungsposition beschränkt, die bearbeitet wird. Das bedeutet, die Änderungen sind spezifisch für den Budgetplanungsprozess und das Budgetplanszenario, die zugewiesen werden. Ausnahmen sind Änderungen an den Feldern, die für die Position für Prozesse und Szenarien freigegeben werden. Diese Felder enthalten die Felder auf der Registerkarte **Allgemeines** und der Registerkarte **Finanzdimensionen** . Wenn diese Felder geändert werden, gelten die neuen Werte für die Position in allen Budgetplanungsszenarien. Daher können Sie mit diesen Feldern schnell alle Versionen aktualisieren.

#### <a name="budget-cost-elements"></a>Budgetkostenelemente

Budgetkostenelemente stellen die wichtigsten Informationen für Budgetpläne bereit: den Budgetbetrag und das Hauptkonto. Der Budgetbetrag ist der Betrag, der an den Haushaltsplan gesendet wird, wenn eine Planungsposition in einem Plan enthalten ist. Der Budgetbetrag wird berechnet und kann nicht direkt geändert werden. Dieser Betrag ist entweder der jährliche Betrag oder eine Berechnung des Prozentsatzes der Basiselemente des jährlichen Betrags (wie in den Einstellungen des Budgetkostenelements definiert). Die Betrag wird dann durch die Anzahl der Tage im Datumsbereich des Elements (Startdatum bis Enddatum) und auch durch den Wert des **Vollzeitäquivalentst** (FTE) für die Planungsposition dargestellt. 

Beispiel: Eine Budgetkostenelementposition vom 1. Januar 2017 bis zum 30. Juni 2017, deren jährlicher Betrag 100.000 und deren FTE-Wert **0,50** lauten, wird wie folgt berechnet: 100.000 × (181 Tage ÷ 365 Tage) × 0,50 = 24.794,52. 

Die Positionen des Budgetkostenelements müssen neu berechnet werden, wenn der FTE-Wert in der Planungsposition geändert wird. Die Positionen müssen auch neu berechnet werden, wenn die Aktivierungsdaten oder die Deaktivierungsdaten geändert werden. Änderungen dieser Daten können eine Aktualisierung der Start- und Enddatumsangaben im Budgetkostenelement verursachen, die innerhalb der Daten der Planungsposition sein müssen. Wenn eine Neuberechnung erforderlich ist, wird die Schaltfläche **Neu berechnen** verfügbar, und die Meldung „Erfordert eine Berechnung“ wird angezeigt. Die Neuberechnung wird auch erforderlich, wenn Sie einen Budgetkostenelement hinzufügen oder entfernen.

**Beispiel** 

Die Organisation erwägt zwei Optionen für das Reduzieren der Kosten einer Buchhalterposition. Eine Option ist, die Position nach einem halben Jahr zu beenden. Die andere Option ist, die Position für das gesamte Jahr in Teilzeit zu ändern. Brad hat eine Planungsposition für die vorhandene Buchhalterposition in einem Basisszenario erstellt. Brad kopiert diese Basisplanungsposition in Szenario A, legt das Rückzugsdatum 31. Mai fest und berechnet neu. Brad kopiert dann die Basisplanungsposition in Szenario B, ändert den FTE-Wert in **0,50** und berechnet neu. Brad besitzt nun drei Versionen, die jeweils Kostensummen aufweisen, die mit den Optionen abgestimmt sind.

#### <a name="assigning-a-compensation-group"></a>Zuweisen einer Vergütungsgruppe

Wenn Sie erstmals eine Vergütungsgruppe zu einer Planungsposition zuweisen, werden die standardmäßigen Budgetkostenelemente aus der Vergütungsgruppe hinzugefügt. Wenn Kostenelemente bereits zur Planungsposition zugewiesen sind, verbleiben diese Kostenelemente. Wenn eine Vergütungsgruppe bereits zugewiesen wurde und geändert wird, werden die vorhandenen Budgetkostenelemente entfernt und mit dem Satz aus der Vergütungsgruppe ersetzt. 

Wenn Sie eine Ebene und einen Schritt für die Vergütung auswählen, wird ein Budgetkostenelement vom Typ Einkünfte (wie in der Vergütungsgruppe definiert) hinzugefügt. Der jährliche Betrag wird durch die Verwendung des Satzes in der ausgewählten Ebene und im ausgewählten Schritt und die jährlichen Stunden in der Vergütungsgruppe berechnet (oder für ein jahresbasiertes Gehalt mit dem Gesamtbetrag der Ebene und des Schritts). Noch einmal wird dieser Betrag über den Datumsbereich der Kostenelementposition und den FTE-Wert der Planungsposition angegeben.

#### <a name="generating-increases"></a>Generieren von Erhöhungen

Jährliche Erhöhungen (eine pro Kalenderjahr) können für Planungspositionen automatisch erstellt werden, die eine schrittbasierte zugewiesene Vergütungsgruppe haben. Klicken Sie auf **Erhöhungen generieren**, um ein Budgetkostenelement vom Typ Einkünfte im nächst höheren Schritt hinzuzufügen. Das Startdatum des neuen Budgetkostenelements vom Typ Einkünfte ist das Datum für geplante Erhöhungen, das in der Planungsposition angezeigt wird. Es gibt zwei Möglichkeiten, dieses Datum anhand der Vergütungsgruppe festzulegen. Wenn der Zeitplan für Erhöhungen der Vergütungsgruppe auf **Allgemeines Datum** gesetzt ist, wird das Datum der Erhöhung in der Vergütungsgruppe angegeben. Wenn der Zeitplan für Erhöhungen auf **Jahrestag** gesetzt ist, wird das Jahrestagsfeld aus der Planungsposition verwendet, und der Budgetzyklus stellt das Jahr bereit. Sind mehrere Kalenderjahre in einem Budgetzyklus enthalten, werden mehrere Erhöhungen hinzugefügt. 

Das Enddatum des aktuellen Budgetkostenelements vom Typ Einkünfte wird mit dem Tag vor dem Datum der Erhöhung aktualisiert. Der Neuberechnungsvorgang wird automatisch verwendet, wenn Erhöhungen generiert werden. Daher müssen Sie nicht manuell neu berechnen. 

Wenn Sie ein zweites Mal auf **Erhöhungen generieren** klicken, wird der Prozess erneut ausgeführt, aber es werden keine weiteren Datensätze hinzugefügt. Nur eine Erhöhung pro Kalenderjahr wird erstellt.

#### <a name="changes-from-other-pages"></a>Änderungen aus anderen Seiten

Aktualisierungen der Planungspositionen können auch aus anderen Bereichen stammen, beispielsweise aus den Seiten für die Einstellungen von Budgetkostenelementen und Vergütungsgruppen. Sie können Planungspositionen auch ändern, indem Sie die Massenaktualisierung verwenden. 

Zwei Optionen stehen auf der Seite mit den Einstellungen für das **Budgetkostenelement** zur Verfügung: **Zu Positionen hinzufügen** und **Positionen aktualisieren**. Die Option **Zu Positionen hinzufügen** fügt das Budgetkostenelement zu den ausgewählten Planungspositionen hinzu. Wenn das Element bereits einer Planungsposition zugewiesen ist, wird diese Planungsposition übersprungen. Die Option **Positionen aktualisieren** wendet die aktuellen Werte (Hauptkonto, Prozentsatz, jährlicher Betrag usw.) auf die ausgewählten Planungspositionen an. 

Jeder Prozess hat eine ähnliche Seite, auf der Sie Planungspositionen auswählen können. Auf der Seite **Zu Positionen hinzufügen** werden alle Planungspositionen angezeigt, die zur Auswahl stehen, während auf der Seite **Positionen aktualisieren** nur die Planungspositionen angezeigt werden, denen bereits ein Budgetkostenelement zugewiesen ist. (Daher bietet die **Positionen aktualisieren** Seite Ihnen die Möglichkeit, zu erfragen, der bereits den Planungspositionen zugeordneten Ausgaben ist). Sie verschieben Planungspositionen eines oberen Raster ein im unteren Raster, in die Aktualisierung einzubeziehen. 

Beachten Sie, dass die Funktion **Datum ändern** in der Registerkarte **Kostenberechnung** sofort das Start- und Enddatum des Budgetkostenelements in den Planungspositionen ändert. Es stehen keine Auswahloptionen zur Verfügung. 

Auf der Seite **Vergütungsgruppe** wendet die Funktion zum **Aktualisieren von Positionssätzen** die aktuellen Sätze aus der Vergütungssatztabelle auf die Planungspositionen an, die der Gruppe zugewiesen sind. Die Sätze werden aktualisiert und zusätzliche Kostenelementpositionen werden für alle neuen Satztabellenpositionen hinzugefügt (auf Grundlage der Datumsangaben). Allerdings werden die Budgetkostenelemente und die Kostenfaktoren und die Daten der Erhöhung nicht aktualisiert. Sie können auswählen, welcher Budgetplanungsprozess und welches Budgetplanszenario aktualisiert werden sollen. Daher können Sie ein Szenario aktualisieren, aber andere Szenarien für den Vergleich unverändert lassen. 

Wenn Sie Planungspositionen auswählen und dann auf **Massenaktualisierung** klicken, können Sie mehr als eine Planungsposition gleichzeitig hinzufügen oder ändern. Viele Optionen sind verfügbar. Eine Option auf der Registerkarte **Finanzdimensionen** unterscheidet sich leicht von den anderen und ist mit Budgetkostenelementen verbunden. Sie können Budgetkostenelemente hinzufügen, indem Sie die Option **Budgetstandardwerte** auf **Ja** setzen. Wenn keine Budgetkostenelemente ausgewählt werden, sondern **Budgetstandardwerte** auf **Ja** gesetzt wird, werden alle Kostenelemente, die derzeit zugewiesen sind, entfernt. 

Der Neuberechnungsvorgang wird automatisch auf jede Planungsposition angewendet, die geändert wurde.

## <a name="bringing-forecast-positions-into-budget-plans"></a>Einfügen von Planungspositionen in Budgetpläne

[![Illustration mit Hervorhebung „Zum Budgetplan hinzufügen“.](./media/graphic6-1024x327.png)](./media/graphic6.png)

Der Zweck der Erstellung und Änderung von Planungspositionen ist, sie Budgetplänen hinzuzufügen, damit die Budgetpläne die genausten Budgetbeträge enthalten. Es gibt zwei Methoden zum Hinzufügen von Planungspositionen zu Budgetplänen. Sie können entweder einen Generierungs- oder einen Auswahlprozess im Budgetplan verwenden.

### <a name="generating-a-budget-plan-from-forecast-positions"></a>Generieren eines Budgetplans aus Planungspositionen

Die Funktion **Budgetplan aus Planpositionen generieren** erstellt oder aktualisiert Budgetpläne so, dass sie die Budgetbeträge und FTE-Anzahlen aus den Planungspositionen enthalten. Die Budgetbeträge aus der Planungsposition werden zu den Budgetplanpositionsbeträgen und werden nach Finanzdimensionswerten und Gültigkeitsdatum zusammengefasst. Der Generierungsprozess weist die Quellplanungsposition zur Budgetplanposition zu. Um die Position anzuzeigen, können Sie entweder die Planungsposition als Zeile im Budgetplanlayout hinzufügen oder die Abfrage **Budgetplanpositionen** verwenden. Um diese Zuweisung zu überspringen, legen Sie die Option **Position in Budgetplanposition einbeziehen** auf **Nein** fest. 

Sie können ein Budgetplan-FTE-Szenario auswählen, um die Anzahl der Vollzeitbeschäftigten in den Budgetplan einzubeziehen. Sie können nur Szenarien des Mengentyps auswählen, die im Layout des Zielbudgetplans enthalten sind. Wenn Sie ein FTE-Szenario auswählen, müssen Sie auch ein FTE-Hauptkonto angeben. Dieses Konto wird verwendet, um die Positionen des Mengen der Budgetplanpositionen zu erstellen. 

Der Budgetplanungsprozess und das Budgetplanszenario, die in der Quelle ausgewählt werden, bestimmen den Budgetplanungsprozess und das Budgetplanszenario im Zielszenario. Da diese Attribute den Planungspositionen zugewiesen werden, müssen sie mit dem Budgetplan synchronisiert sein. Daher können die Attribute nicht im Ziel bearbeitet werden. 

Was andere Generierungsprozesse angeht, sind drei Optionen verfügbar:

-   **Neuen Budgetplan erstellen** - Dient zum Erstellen eines neuen Plan, der über die Attribute verfügt, die im Bereich **Vorgabe** aktiviert sind.
-   **Vorhandenes Budgetplanszenario ersetzen** - Löscht alle Daten im Zielbudgetplan im ausgewählten Budgetplanszenario und erstellt neue Positionen, die die ausgewählten Planungspositionsdaten haben.
-   **Vorhandenes Budgetplanszenario aktualisieren, neue Daten hinzufügen** - Aktualisiert vorhandene Positionen im Zielplan, damit diese mit den Quellpositionen übereinstimmen, und fügt auch neue Positionen für neue Daten hinzu. Der Abgleich basiert auf Sachkonto, Datum, Budgetklasse und anderen Werte, wie Planungsposition. Alle Positionen, die eine Positionsnummer haben, die mit der Quellpositionsnummer übereinstimmt, werden durch die neuen Positionen aus der Quelle ersetzt.

### <a name="selecting-forecast-positions"></a>Auswählen von Planungspositionen

Sie können Budgetbeträge von Planungspositionen direkt zu einem Budgetplan hinzufügen. Verwenden Sie die Funktion **Positionen hinzufügen** über den Budgetplanpositionen, um die einzubeziehenden Planungspositionen auszuwählen. 

Die Budgetplanszenarios, die Sie auswählen können, wenn die Quelle auf die Szenarios eingeschränkt wird, die im Layout des Plans enthalten sind. Mit einer Option auf der Registerkarte **Vorgabe** können Sie angeben, dass das FTE-Szenario und -Hauptkonto verfügbar sind, um FTE-Anzahlen einzubeziehen, dass sie jedoch nicht erforderlich sind. 

Dieses Auswahlverfahren verhält sich wie die Option **Vorhandenes Budgetplanszenario aktualisieren, neue Daten hinzufügen** für einen Generierungsprozess. Die gesamten vorhandenen Budgetplanpositionen, bei denen die Planungsposition hinzugefügt wird, werden entfernt und durch neue Positionen ersetzt, die auf dem aktuellen Status der Planungsposition basieren.

#### <a name="date-options"></a>Datumsoptionen

Für den Generierungs- und Auswahlprozess bestimmt das Startdatum für die Position des Budgetkostenelements das Gültigkeitsdatum der entsprechenden Budgetplanposition. Das Feld **Zuordnungsmethode** auf der Seite für die Einstellungen des Budgetkostenelements gibt die Zuordnungsmethode an:

-   **Startdatum** - Das Startdatum des Budgetkostenelements wird als Gültigkeitsdatum der Budgetplanposition verwendet.
-   **Monatlich** - Der Budgetbetrag wird gleichmäßig durch die Anzahl der Monate im Datumsbereich dividiert, um einen typischen monatlichen Betrag zu erstellen, der am ersten Tag des Monats zugewiesen wird. Wenn die erste Periode ein Teilmonat ist, wird der Betrag für diesen Monat aufdie Anzahl von Tagen aufgeteilt, die die Kosten in diesem Monat aktiv sind, und das Ergebnis wird dem Startdatum zugewiesen. Der Betrag des letzten Monats ist die Differenz zwischen dem gesamten Budgetbetrag und der Summe aller anderen Monate. Daher wirkt sich die Rundung möglicherweise auf den Betrag des letzten Monats aus.
-   **Vierteljährlich** - Diese Methode ist die gleiche wie **Monatlich**, aber die Berechnungen werden für dreimonatige Perioden ausgeführt.
-   **Wöchentlich** - Die Logik ähnelt der Logik der Methoden **Monatlich** und **Vierteljährlich**. Der Budgetbetrag wird gleichmäßig durch die Anzahl der Wochen im Datumsbereich dividiert, um einen typischen wöchentlichen Betrag zu erstellen, der am ersten Tag der Woche zugewiesen wird. Wenn die erste Periode eine Teilwoche ist, wird der Betrag für diese Woche aufdie Anzahl von Tagen aufgeteilt, die die Kosten in dieser Woche aktiv sind, und das Ergebnis wird dem Startdatum zugewiesen. Der Betrag der letzten Woche ist die Differenz zwischen dem gesamten Budgetbetrag und der Summe aller anderen Wochen. Daher wirkt sich die Rundung möglicherweise auf den Betrag der letzten Woche aus.
-   **Zweiwöchentlich** - Diese Methode ist die gleiche wie **Wöchentlich**, aber die Berechnungen werden für zweiwöchige Perioden ausgeführt.

#### <a name="changing-budget-plan-lines-that-have-forecast-positions"></a>Ändern von Budgetplanpositionen, die Planungspositionen haben

Budgetplanpositionen zeigen die Quelle der Budgetbeträge an (die Planungspositionsnummer), werden jedoch nicht verknüpft. Daher werden Änderungen an der Planungsposition nicht in der Budgetplanposition angezeigt, und Änderungen an der Budgetplanposition werden in der Planungsposition angezeigt. Wenn Sie eine Planungsposition ändern und die Aktualisierungen in einen Budgetplan aufgenommen werden soll, müssen Sie die Planungsposition erneut in den Plan aufnehmen. Allerdings müssen Sie berücksichtigen, dass dieser Prozess alle Positionen entfernt, in denen diese Planungsposition zugewiesen ist. Daher werden die Änderungen, die Sie an diesen Positionen vorgenommen haben, entfernt. 

Um festzustellen, in welche Budgetpläne eine Planungsposition eingefügt wurde, können Sie in den Bericht **Planpositionen nach Budgetplan** generieren. Alternativ können Sie in der Prognoseposition die Infobox **Zugeordnete Budgetpläne** öffnen, um die Pläne anzuzeigen.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
