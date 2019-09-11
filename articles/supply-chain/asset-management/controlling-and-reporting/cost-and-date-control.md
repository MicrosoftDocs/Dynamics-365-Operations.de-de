---
title: Kosten- und Datenkontrolle
description: In diesem Thema wird die Kosten- und Datenkontrolle in der Anlagenverwaltung erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918394"
---
# <a name="cost-and-date-control"></a>Kosten- und Datenkontrolle

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In der Anlagenverwaltung können Sie Kosten berechnen, um sich so einen Überblick über die Istkosten im Vergleich zu den Budgetkosten für Anlagen, funktionale Standorte und Arbeitsaufträge zu verschaffen. Istkosten basieren auf gebuchten Transaktionen. Sie können auch eine Datumsberechnung vornehmen, wenn Sie geplante Start- und Enddaten mit tatsächlichen Start- und Enddaten für Arbeitsaufträge vergleichen möchten.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Kostenkontrolle für Anlagen, funktionale Standorte und Arbeitsaufträge

Die Berechnungen für Anlagen, Technische Standorte und Arbeitsaufträge sind nahezu identisch. Der einzige Unterschied besteht darin, dass Sie bei Anlagen und Technischen Standorten auch Teilanlagen und Teilstandorte in Ihre Kalkulation einbeziehen können. Das Datum ist das Transaktionsdatum, an dem die Registrierung erfasst wurde.

1. Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagen** > **Kostensteuerung für Anlagen** oder **Kostensteuerung für funktionalen Standort**, oder auf **Anlagenverwaltung** > **Abfragen** > **Arbeitsaufträge** > **Kostensteuerung für Arbeitsaufträge**.

2. Wählen Sie im Dialogfeld **Kostensteuerung für Anlagen** / **Kostensteuerung für funktionalen Standort** / **Kostensteuerung für Arbeitsaufträge** eine zu berechnende Periode aus.

3. Bei Bedarf wählen Sie eine Finanzdimensionsgruppe aus, die in die Berechnung einbezogen werden soll.

4. Wählen Sie „Ja“ auf der Umschaltfläche **Null überspringen** aus, wenn keine Ergebnisse mit Kosten von Null angezeigt werden sollen.

5. Sie können das Feld **Ebene** verwenden, um anzugeben, wie detailliert die Kostensteuerungspositionen bezüglich funktionaler Standorte sein sollen. Wenn Sie beispielsweise die Zahl „1“ im Feld einfügen und eine funktionale Standorthierarchie auf mehreren Ebenen haben, werden alle Kostenkontrollpositionen für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher werden die Stunden in einer Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt. Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Kostenkontrollpositionen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.

6. Wählen Sie „Ja“ für die Umschaltschaltfläche **Offene zugesagte Kosten anzeigen** aus, wenn diese Spalte in die Berechnung einbezogen werden soll.

7. Wählen Sie „Ja“ auf der Schaltfläche **Teilanlagen einbeziehen** Umschalten, um die mit Teilanlagen verbundenen Kosten als separate Zeilen anzuzeigen.

8. Wenn Sie die Suche einschränken möchten, können Sie bestimmte Anlagen / Technische Standorte / Arbeitsaufträge auf den **Sätzen auswählen, die mit** FastTab versehen werden sollen.

9. Klicken Sie auf **OK**, um die Berechnung zu starten.

In der folgenden Abbildung wird ein Beispiel des Dialogfelds **Kostensteuerung für Anlagen** angezeigt.

![Abbildung 1](media/01-controlling-and-reporting.png)

10. In den Aktivitätsbereichsgruppen **Gruppieren nach…** auf der Seite **Kostensteuerung für Anlagen** klicken Sie auf die entsprechenden Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen. Die ausgewählten Aktionsbereichschaltflächen werden hervorgehoben. Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.

In der folgenden Abbildung wird ein Beispiel der Berechnungsergebnisse in **Kostensteuerung für Anlagen** angezeigt.

![Abbildung 2](media/02-controlling-and-reporting.png)

Eine weitere Möglichkeit der Erstellung einer Kostenberechnung ist die Mehrfachauswahl von Anlagen in **Alle Anlagen** oder **Aktive Anlagen**. Klicken Sie anschließend auf die Schaltfläche **Kostensteuerung** auf der Registerkarte **Allgemein** . Im Dialogfeld **Kostensteuerung für Anlagen** werden die ausgewählten Anlagen automatisch in das Feld **Anlage** im Inforegister **Einzuschließende Datensätze** eingefügt. Klicken Sie auf **OK**, und eine Kostenberechnung für die ausgewählten Anlagen wird angezeigt. Das gleiche Verfahren kann für Technische Standorte in **Alle Technischen Standorte** oder **Aktive Technische Standorte** und für Arbeitsaufträge in **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** durchgeführt werden.

>[!NOTE]
>Das Feld **Ursprüngliches Budget** zeigt Budgetkosten aus der Arbeitsauftragsplanung. Das Feld **Zugesagte Kosten** zeigt den Ausgabengesamtbetrag an, dessen Zahlung eine juristische Person zugesagt hat. Das Feld **Offene zugesagte Kosten** zeigt die Zahlungszusagen für Artikel, Stunden und Dienstleistungen an, die Sie bestellt oder erhalten, aber noch nicht bezahlt haben. Wenn alle Verbrauchserfassungen gebucht wurden, sind die zugehörigen Kosten im Feld **Istkosten** enthalten.

## <a name="work-order-date-control"></a>Datumskontrolle für Arbeitsaufträge

Verwenden Sie diese Seite, um einen Überblick über die erwarteten Start- und Enddaten im Vergleich zu den tatsächlichen Start- und Enddaten für Arbeitsaufträge zu erhalten.

1. Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Arbeitsaufträge** > **Datumskontrolle für Arbeitsaufträge**.

2. Klicken Sie auf **Berechnen**.

3. Wählen Sie einen funktionalen Standort im Feld **Funktionaler Standort** aus.

4. Fügen Sie die Periode für die Berechnung in den Feldern **Anfangsdatum** und **Enddatum** ein. Alle Arbeitsaufträge mit dem erwarteten Start innerhalb der Periode werden einbezogen.

5. Klicken Sie auf **OK**.

6. In den Aktivitätsbereichsgruppen **Gruppieren nach…** klicken Sie auf die entsprechenden Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen. Die ausgewählten Aktionsbereichschaltflächen werden hervorgehoben. Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.

In der folgenden Abbildung wird ein Beispiel der Berechnungsergebnisse in **Datumskontrolle für Arbeitsaufträge** angezeigt.

![Abbildung 3](media/03-controlling-and-reporting.png)

- Das Feld **Durchschn. Startverzögerung** zeigt die Differenz in Tagen zwischen dem geplanten Startdatum für einen Arbeitsauftrag im Vergleich zum tatsächlichen Startdatum an. Wenn beispielsweise das tatsächliche Startdatum zwei Tage vor dem geplanten Startdatum war, wird „-2“ in diesem Feld angezeigt.  
- Das Feld **Durchschn. Endverzögerung** zeigt die Differenz in Tagen zwischen dem geplanten Enddatum für einen Arbeitsauftrag im Vergleich zum tatsächlichen Enddatum an. Wenn beispielsweise das tatsächliche Enddatum drei Tage nach dem geplanten Enddatum war, wird „3“ in diesem Feld angezeigt.  
- Die Felder **Vorkommen** zeigen die Zahl der Häufigkeitsabweichungen in Bezug auf das geplante und das tatsächliche Startdatum und das geplante und tatsächliche Enddatum des Arbeitsauftrags an.

