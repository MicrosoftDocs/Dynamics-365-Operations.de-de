---
title: Kosten- und Datenkontrolle
description: In diesem Thema wird die Kosten- und Datenkontrolle in der Anlagenverwaltung erläutert.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 826e0aab8c717bb951d80aff61b2d72dad802189706f720c48e72c8a1c393ead
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731912"
---
# <a name="cost-and-date-control"></a>Kosten- und Datenkontrolle

[!include [banner](../../includes/banner.md)]

In der Anlagenverwaltung können Sie Kosten berechnen, um sich so einen Überblick über die Istkosten im Vergleich zu den Budgetkosten für Anlagen, funktionale Standorte und Arbeitsaufträge zu verschaffen. Istkosten basieren auf gebuchten Transaktionen.

Sie können auch eine Datumsberechnung vornehmen, wenn Sie geplante Start- und Enddaten mit tatsächlichen Start- und Enddaten für Arbeitsaufträge vergleichen möchten.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Kostenkontrolle für Anlagen, funktionale Standorte und Arbeitsaufträge

Die Berechnungen für Anlagen, Technische Standorte und Arbeitsaufträge sind nahezu identisch. Der einzige Unterschied besteht darin, dass Sie bei Anlagen und funktionalen Standorten auch Teilanlagen und Teilstandorte in Ihre Kalkulation einbeziehen können. Das Datum ist das Transaktionsdatum, an dem die Registrierung erfasst wurde.

1. Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagen** > **Kostensteuerung für Anlagen** oder **Kostensteuerung für funktionalen Standort**, oder auf **Anlagenverwaltung** > **Abfragen** > **Arbeitsaufträge** > **Kostensteuerung für Arbeitsaufträge**.

2. Wählen Sie im Dialogfeld **Kostensteuerung für Anlagen** / **Kostensteuerung für funktionalen Standort** / **Kostensteuerung für Arbeitsaufträge** einen zu berechnenden Zeitbereich aus.

3. Bei Bedarf wählen Sie eine Finanzdimensionsgruppe aus, die in die Berechnung einbezogen werden soll.

4. Wählen Sie „Ja“ auf der Umschaltfläche **Null überspringen** aus, wenn keine Ergebnisse mit Kosten von Null angezeigt werden sollen.

5. Sie können das Feld **Ebene** verwenden, um anzugeben, wie detailliert die Kostensteuerungspositionen bezüglich funktionaler Standorte sein sollen. 

    Wenn Sie beispielsweise die Zahl „1“ im Feld einfügen und eine funktionale Standorthierarchie auf mehreren Ebenen haben, werden alle Kostenkontrollpositionen für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher werden die Stunden in einer Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt.

    Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Kostenkontrollpositionen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.

6. Wählen Sie „Ja“ für die Umschaltschaltfläche **Offene zugesagte Kosten anzeigen** aus, wenn diese Spalte in die Berechnung einbezogen werden soll.

7. Wählen Sie „Ja“ auf der Schaltfläche **Teilanlagen einbeziehen** Umschalten, um die mit Teilanlagen verbundenen Kosten als separate Zeilen anzuzeigen.

8. Wenn Sie die Suche einschränken möchten, können Sie bestimmte Anlagen / Technische Standorte / Arbeitsaufträge auf den **Sätzen auswählen, die mit** FastTab versehen werden sollen.

9. Klicken Sie auf **OK**, um die Berechnung zu starten.

    In der folgenden Abbildung wird ein Beispiel des Dialogfelds **Kostensteuerung für Anlagen** angezeigt.

    ![Dialogfeld „Kostensteuerung für Anlagen“.](media/01-controlling-and-reporting.png)

10. Klicken Sie auf der Seite **Kostensteuerung für Anlagen** auf die **Gruppieren nach…**-Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen. Die ausgewählten **Gruppieren nach…**-Schaltflächen werden hervorgehoben. Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.

## <a name="example-of-calculation-results-in-asset-cost-control"></a>Beispiel für Berechnungsergebnisse in Kostensteuerung für Anlagen

Im folgenden Screenshot wird ein Beispiel der Berechnungsergebnisse in **Kostensteuerung für Anlagen** angezeigt.

- Das Feld **Ursprüngliches Budget** zeigt Budgetkosten aus der Arbeitsauftragsplanung. 
- Das Feld **Zugesagte Kosten** zeigt den Ausgabengesamtbetrag an, dessen Zahlung eine juristische Person zugesagt hat. 
- Das Feld **Offene zugesagte Kosten** zeigt die Zahlungszusagen für Artikel, Stunden und Dienstleistungen an, die Sie bestellt oder erhalten, aber noch nicht bezahlt haben. 
- Wenn alle Verbrauchserfassungen gebucht wurden, werden die zugehörigen Kosten im Feld **Istkosten** angezeigt.

![Beispiel Berechnungsergebnisse in Kostensteuerung für Anlagen.](media/02-controlling-and-reporting.png)

Eine weitere Möglichkeit der Erstellung einer Kostenberechnung ist die Mehrfachauswahl von Anlagen in **Alle Anlagen** oder **Aktive Anlagen**. Klicken Sie anschließend auf die Schaltfläche **Kostensteuerung** auf der Registerkarte **Allgemein** . Im Dialogfeld **Kostensteuerung für Anlagen** werden die ausgewählten Anlagen automatisch in das Feld **Anlage** auf dem Inforegister **Einzuschließende Datensätze** eingefügt. Klicken Sie auf **OK**, und eine Kostenberechnung für die ausgewählten Anlagen wird angezeigt. Das gleiche Verfahren kann für Technische Standorte in **Alle Technischen Standorte** oder **Aktive Technische Standorte** und für Arbeitsaufträge in **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** durchgeführt werden.

## <a name="work-order-date-control"></a>Datumskontrolle für Arbeitsaufträge

Verwenden Sie diese Seite, um einen Überblick über die erwarteten Start- und Enddaten im Vergleich zu den tatsächlichen Start- und Enddaten für Arbeitsaufträge zu erhalten.

1. Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Arbeitsaufträge** > **Datumskontrolle für Arbeitsaufträge**.

2. Klicken Sie auf **Berechnen**.

3. Wählen Sie einen funktionalen Standort im Feld **Funktionaler Standort** aus.

4. Fügen Sie den Bereich für die Berechnung in den Feldern **Anfangsdatum** und **Enddatum** ein. Alle Arbeitsaufträge mit dem erwarteten Startdatum innerhalb des Bereichs werden einbezogen.

5. Klicken Sie auf **OK**.

6. Klicken Sie auf die **Gruppieren nach…**-Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen. Die ausgewählten **Gruppieren nach…**-Schaltflächen werden hervorgehoben. Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.

## <a name="example-of-calculation-results-in-work-order-date-control"></a>Beispiel für Berechnungsergebnisse in Datumskontrolle für Arbeitsaufträge

Im folgenden Screenshot wird ein Beispiel der Berechnungsergebnisse in **Datumskontrolle für Arbeitsaufträge** angezeigt.

- Das Feld **Durchschn. Startverzögerung** zeigt die Differenz in Tagen zwischen dem geplanten Startdatum für einen Arbeitsauftrag im Vergleich zum tatsächlichen Startdatum an. Wenn beispielsweise das tatsächliche Startdatum zwei Tage vor dem geplanten Startdatum war, wird „-2“ in diesem Feld angezeigt.  
- Das Feld **Durchschn. Endverzögerung** zeigt die Differenz in Tagen zwischen dem geplanten Enddatum für einen Arbeitsauftrag im Vergleich zum tatsächlichen Enddatum an. Wenn beispielsweise das tatsächliche Enddatum drei Tage nach dem geplanten Enddatum war, wird „3“ in diesem Feld angezeigt.  
- Die Felder **Vorkommen** zeigen die Zahl der Häufigkeitsabweichungen in Bezug auf das geplante und das tatsächliche Startdatum und das geplante und tatsächliche Enddatum des Arbeitsauftrags an.

![Beispiel Berechnungsergebnisse in Datumskontrolle für Arbeitsaufträge.](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]