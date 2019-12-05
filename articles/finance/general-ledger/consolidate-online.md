---
title: Online Finanzkonsolidierungen
description: In diesem Thema wird die Online-Finanzkonsolidierungen und Währungsumrechnung im Hauptbuch behandelt.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 86be6d4cc0af3f2fd92523d4ecd3825f2383fc48
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770734"
---
# <a name="online-financial-consolidations"></a>Online Finanzkonsolidierungen

[!include [banner](../includes/banner.md)]

In diesem Thema wird die Online-Finanzkonsolidierungen und Währungsumrechnung im Hauptbuch behandelt. Bevor Sie dieses Thema lesen, sollten Sie unbedingt das Thema [Finanzielle Konsolidierungen und Währungsumrechnung – Übersicht](financial-consolidations-currency-translation.md) lesen.

Nachdem Sie die Einstellungen abgeschlossen haben, geben Sie die Details der Konsolidierung auf der Seite **Konsolidieren [online]** ein. Wenn Sie fertig sind, können Sie auch **OK** oder **Charge** klicken, um die Konsolidierung zu verarbeiten.

## <a name="criteria"></a>Kriterien
Auf der Registerkarte **Kriterien** auf der Seite **Konsolidieren [online]** definieren Sie die Konten, Zeiträume und die Art von Daten, die konsolidiert werden soll.

![Registerkarte „Kriterien“](./media/criteria-consolidate-online.png "Registerkarte „Kriterien“")

Hier ist eine Erläuterung der Konfiguration in dieser Registerlarte:

- **Beschreibung** – Geben Sie eine präzise Beschreibung für die Periode ein, die zum Konsolidieren ist.
- **Hauptkonto** – Verwenden Sie die Felder in diesem Abschnitt, um die Hauptkonten zu definieren, die verarbeitet werden.

    - **Von**  und **Bis** geben einen Bereich von Konten zum Verarbeiten an. Werden diese Felder nicht ausgefüllt, werden alle Konten von allen Unternehmen auf das Konsolidierungsunternehmen verschoben. Wenn Sie vier Unternehmen konsolidieren, und in jedem Unternehmen ein anderer Kontenplan vorhanden ist, werden die Konten von allen vier Unternehmen im konsolidierten Unternehmen erstellt.
    - **Konsolidierungskonto verwenden** – Wenn Sie die Option auf **Ja** setzen, wird das Feld **Auswahlquelle für Konsolidierungskonto** verfügbar. In diesem Feld wählen Sie aus, ob alle Konten mit dem Konsolidierungskonto konsolidiert werden soll, das auf der Seite **Hauptkonten** festgelegt wurde, oder Sie ein anderes Konto von einer der  Konsolidierungskontogruppen auswählen möchten.
    - **Konsolidierungskontengruppe** – Wählen Sie die Gruppe aus, die für die Hauptkontozuordnung für die Konsolidierung zu verwenden ist.

- **Konsolidierungsperiode** – Verwenden Sie die Felder in diesem Abschnitt, um die Konsolidierungsperiode zu definieren.

    - **Von** und **Bis** – Geben Sie einen Datumsbereich für die Konsolidierung an. Wenn Sie dieses Feld leer lassen, wird die Konsolidierung für alle Perioden im Sachkontokalender verarbeitet, die für das Unternehmen definiert sind. Dieses Feld sollte nicht unausgefüllt bleiben.
    - **Istbeträge einbeziehen** – Legen Sie diese Option auf **Ja** fest, um die tatsächlichen Daten konsolidieren zu können.
    - **Budgetbeträge einbeziehen** – Legen Sie diese Option auf **Ja** fest, um Daten aus dem Budgetregister zu konsolidieren.
    - **Erstellen Sie Salden für die Konsolidierung neu** – Es empfiehlt sich nicht, dass Sie Option auf **Ja** festlegen. Stattdessen erstellen Sie Salden als separater Stapelverarbeitungsauftrag.

- **Budgetmodelle** – Wenn Sie ausgewählt haben, dass Budgetdaten zusammengeführt werden sollen, verwenden Sie die Felder in diesem Abschnitt, um Budgetmodelle zu definieren.

    - **Von**  und **Bis** geben einen Bereich von Modellen zum Verarbeiten an.
    - **Budgetkurstyp** – Wählen Sie den Typ des Budgetsatzes aus, um für Währungsumrechnung von Budgetdaten zu verwenden.

## <a name="financial-dimensions"></a>Finanzdimensionen
**Finanzdimensionen** Auf der Registerkarte definieren Sie die Dimensionen, die im Konsolidierungsunternehmen einbezogen werden sollen. Wenn Sie eine Dimension auswählen, legen Sie das Feld **Spezifikation** auf **Dimension** fest, und definieren Sie dann die Reihenfolge der Dimension im Konsolidierungsunternehmen.

![Registerkarte „Finanzdimensionen“](./media/financial-dimensions-cons.png "Registerkarte „Finanzdimensionen“")

Unabhängig von der Reihenfolge, die Sie definieren, ist immer **Hauptkonto** das erste Segment.

## <a name="legal-entities"></a>Juristische Personen
Auf der Registerkarte **Juristische Personen** definieren Sie die Dimensionen, die im Konsolidierungsunternehmen einbezogen werden sollen. Sie können auch den Besitzprozentsatz dieser Unternehmen definieren. Wenn Sie einem Besitz von weniger als 100 Prozent angeben, wird der angegebene Prozentsatz auf das Konsolidierungsunternehmen zusammengefasst. Für alle Übersetzungsdifferenzen wird das Feld **Kontenart für Konvertierungsdifferenzen** verwendet, um das Hauptkonto aus der Einstellung auf der Seite**Konten für automatische Buchungen** auszuwählen.

![Registerkarte „Juristischen Personen“](./media/legal-entities-cons.png "Registerkarte „Juristische Personen“")

![Seite „Konten für automatische Buchungen“](./media/accounts-for-automatic-cons.png "Seite „Konten für automatische Buchungen“")

## <a name="elimination"></a>Löschung
Auf der Registerkarte **Löschung** haben Sie drei Optionen zum Verarbeiten von Vorkalkulationen:

- Dient zum Auswählen der Löschungsregel, und dann im Feld **Vorschlagsoptionen** aus, wählen Sie **Nur Vorschlag** aus. Diese Option verarbeitet die Löschung während des Konsolidierungsprozesses, wird aber nicht alle in einem Schritt buchen. Sie können die Erfassung später buchen.
- Dient zum Auswählen der Löschungsregel, und dann im Feld **Vorschlagsoptionen** wählen Sie **Nur Vorschlag** aus. Diese Option verarbeitet die Löschung während des Konsolidierungsprozesses und wird alle in einem Schritt buchen.
- Führen Sie den Löschungvorschlag getrennt vom Konsolidierungsprozesses als indem Sie die Löschungserfassung ausführen.

![Registerkarte „Löschung“](./media/elimination-cons-onl.png "Registerkarte „Löschung“")

Weitere Informationen zur Löschung finden Sie unter [Löschungsrichtlinien](./elimination-rules.md)

## <a name="currency-translation"></a>Währungsumrechnung
Auf der Registerkarte **Währungsumrechnung** definieren Sie die juristische Person, das Konto und den Wechselkurstyp und den Wechselkurs. Drei Optionen stehen im Feld **Wechselkurs übernehme** zur Verfügung:

- **Konsolidierungsdatum** – Das Datum der Konsolidierung wird verwendet, um den Wechselkurs zu erhalten. Der Kurs der Entität entspricht der Spot- oder Monatendkurs. Sie sehen eine Vorschau des Satzes, aber Sie können ihn nicht bearbeiten.
- **Buchungsdatum** – Das Datum jeder Buchung wird verwendet, um einen Wechselkurs auszuwählen. Diese Option ist für Anlagen häufig und wird oft als historischer Satz bezeichnet. Sie können eine Vorschau des Satzes nicht finden, da es viele Sätze für die verschiedenen Buchungen im Kontenbereich gibt.
- **Benutzerdefinierter Satz** – Wenn Sie diese Option aktivieren, können Sie den Wechselkurs eingeben, den Sie wünschen. Diese Option kann für durchschnittliche Wechselkurse hilfreich sein oder wenn Sie mit einem festen Wechselkurs konsolidieren.

![Registerkarte „Währungsumrechnung“](./media/currency-translation-cons-online.png "Registerkarte „Währungsumrechnung“")

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Weitere Informationen zur Konsolidierung und Währungsumrechnung finden Sie im übergeordneten Thema dieses Themas, [Finanzkonsolidierungen und Übersicht zur Währungsumrechnung](./financial-consolidations-currency-translation.md).

Informationen zum Szenarien, in denen Sie möglicherweise Finanzaufstellungen generieren können, finden Sie unter [Konsolidierte Finanzaufstellungen erstellen](./generating-consolidated-financial-statements.md).
