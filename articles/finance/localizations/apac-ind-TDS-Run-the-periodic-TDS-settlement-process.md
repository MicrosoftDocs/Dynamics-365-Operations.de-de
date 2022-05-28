---
title: Den periodischen TDS-Ausgleichsprozess ausführen
description: In diesem Thema wird erklärt, wie die periodische Quellenbesteuerung (TDS) ausgeglichen wird.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 6c0aca4d0a916b21ca5ac6ee14e6ab658e0bae26
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726433"
---
# <a name="run-the-periodic-tds-settlement-process"></a>Den periodischen TDS-Ausgleichsprozess ausführen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie die periodische Quellenbesteuerung (TDS) ausgeglichen wird.

1. Gehen Sie zu **Steuer \> Erklärungen \> Quellensteuer \> Quellensteuerzahlung**.

    [![Dialogfeld „Quellensteuerzahlung“.](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)

2. Wählen Sie im Dialogfeld **Quellensteuerzahlung** im Feld **Steuertyp** **TDS** aus.
3. Wählen Sie im Feld **Steuerkontonummer (TAN)** die Steuerkontonummer (TAN) aus, für die der Ausgleichsprozess ausgeführt werden soll.
4. Wählen Sie im Feld **Quellensteuerkomponentengruppe** die TDS-Komponentengruppe aus, für die der Ausgleichsprozess ausgeführt werden soll.
5. Wählen Sie im Feld **Ausgleichsperiode** die TDS-Ausgleichsperiode aus, für die der Ausgleichsprozess ausgeführt werden soll.

    > [!NOTE]
    > Der TDS-Ausgleichsprozess wird für alle Perioden ausgeführt, die für die TDS-Ausgleichsperiode in der Registerkarte **Perioden** der Seite **Quellensteuerausgleichsperioden** eingerichtet sind (**Steuer \> Indirekte Steuern \> Quellensteuern \> Quellensteuerausgleichsperioden**).

6. Wählen Sie im Feld **Startdatum** das Startdatum aus, ab dem aus der TDS-Ausgleichsprozess ausgeführt werden soll.

    Für eine bestimmten Periode innerhalb der Ausgleichsperiode wird das für die Periode festgelegte Startdatum als „Ab“-Datum verwendet. Die TDS-Ausgleichsperiode hat zum Beispiel zwei Perioden: 1. bis 30. April 2009 und 1. bis 31. Mai 2009. Wenn Sie **06.04.2009** als Starttermin im Feld **Startdatum** auswählen, beginnt der Ausgleichsprozess trotzdem ab dem 1. April 2009.

    Wenn Sie eine spätere Periode in das Feld **Startdatum** eingeben, aber keine vorherige Periode innerhalb der Ausgleichsperiode ausgleichen, erfolgt der Ausgleich nicht für frühere Perioden. Zum Beispiel: Die TDS-Ausgleichsperiode umfasst drei Perioden: 1. bis 30. April 2009, 1. bis 31. Mai 2009 und 1. bis 30. Juni 2009. Wenn Sie **01.05.2009** als Startdatum im Feld **Startdatum** angeben, läuft der Ausgleichsprozess nur vom 1. bis 31. Mai 2009. Der Ausgleich erfolgt nicht vom 1. bis 30. April 2009.

7. Wählen Sie im Feld **Buchungsdatum** das Buchungsdatum für die TDS-Ausgleichsbuchung aus.
8. Wählen Sie im Feld **Quellensteuerzahlungsversion** die TDS-Ausgleichsversion aus:

     - **Original**: Verwenden Sie diese Option, um den TDS-Ausgleichsprozess zum ersten Mal auszuführen. Die Originalzahlungsversion wird nur einmal verwendet, um den TDS-Ausgleichsprozess für eine Kombination aus einer TAN, einer Quellensteuerkomponentengruppe und einer Quellensteuerausgleichsperiode auszuführen.
    - **Letzte Versionen**: Verwenden Sie diese Option, wenn der TDS-Ausgleichsprozess bereits für die angegebene Periode ausgeführt wurde. Nehmen Sie rückdatierte Buchungen mit auf, die gebucht wurden, nachdem der Ausgleichsprozess zuvor für die Periode ausgeführt wurde. Mit dieser Option können Sie den Ausgleichsprozess beliebig oft ausführen.

9. Aktivieren Sie das Kontrollkästchen **Aktualisieren**, um den TDS-Ausgleichsprozess auszuführen und die Beträge auf die Sachkonten zu buchen. Wenn dieses Kontrollkästchen deaktiviert ist, wird der Ausgleichsprozess nicht ausgeführt und die Finanzbuchungen werden nicht generiert.
10. Wählen Sie **OK** aus, um den TDS-Ausgleichsprozess auszuführen und den Quellensteuerzahlungsbericht zu generieren. Der Status von TDS-Buchungen, die im Ausgleichsprozess enthalten sind, wird als angezeigt **Ausgeglichen** auf der Seite **Ausgleich** angezeigt (gehen Sie zu **Kreditorenkonten \> Zahlungen \> Kreditorenzahlungserfassung**, wählen Sie **Positionen**, **Funktionen** und dann **Ausgleich**).

### <a name="important-points"></a>Wichtige Punkte

- Wenn während des Ausgleichsprozesses keine Quellensteuerkomponentengruppe ausgewählt wird, erfolgt der Ausgleich für alle Quellensteuerkomponentengruppen für die ausgewählte TAN und Ausgleichsperiode. Für jede Quellensteuerkomponentengruppe wird auf der Seite **Bearbeiten offener Posten** eine eigene Position erstellt.
- Der Ausgleichsprozess basiert auf der Steuerschuldnerkategorie für eine Ausgleichsperiode. Buchungen, deren Steuerschuldnerkategorie **Unternehmen** lautet, sind ausgeglichen und werden auf der Seite **Bearbeiten offener Posten** als eine Position angezeigt. Buchungen, deren Steuerschuldnerkategorie nicht **Unternehmen** lautet, sind ausgeglichen und werden auf der Seite **Bearbeiten offener Posten** als eine Position angezeigt.
- Das Fälligkeitsdatum für die ausgeglichenen TDS-Buchungspositionen auf der Seite **Bearbeiten offener Posten** basiert auf den Zahlungsbedingungen, die auf der Seite **Kreditoren** für den TDS-Behördenkreditor festgelegt sind. Wenn die Zahlungsbedingungen für den TDS-Behördenkreditor nicht definiert sind, wird der letzte Tag der Ausgleichsperiode als Fälligkeitsdatum angezeigt.
