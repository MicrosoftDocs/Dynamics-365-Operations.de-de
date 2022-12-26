---
title: Online Finanzkonsolidierungen
description: In diesem Artikel werden die Online-Finanzkonsolidierungen im Hauptbuch behandelt.
author: aprilolson
ms.date: 12/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 5843ac78adf32e738d9882c7f4e9e04a79200700
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838278"
---
# <a name="online-financial-consolidations"></a>Online Finanzkonsolidierungen

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Online-Finanzkonsolidierungen im Hauptbuch behandelt. Bevor Sie dieses Artikels lesen, sollten Sie unbedingt den Artikel [Finanzielle Konsolidierungen und Währungsumrechnung – Übersicht](financial-consolidations-currency-translation.md) lesen.

Nachdem Sie die Einstellungen abgeschlossen haben, geben Sie die Details der Konsolidierung auf der Seite **Konsolidieren [online]** ein. Wenn Sie fertig sind, können Sie auch **OK** oder **Charge** klicken, um die Konsolidierung zu verarbeiten.

## <a name="criteria"></a>Kriterien
Auf der Registerkarte **Kriterien** auf der Seite **Konsolidieren [online]** definieren Sie die Konten, Zeiträume und die Art von Daten, die konsolidiert werden soll.

![Registerkarte „Kriterien“.](./media/criteria-consolidate-online.png "Registerkarte „Kriterien“")

Hier ist eine Erläuterung der Konfiguration in dieser Registerlarte:

- **Beschreibung** – Geben Sie eine präzise Beschreibung für die Periode ein, die zum Konsolidieren ist.
- **Hauptkonto** – Verwenden Sie die Felder in diesem Abschnitt, um die Hauptkonten zu definieren, die verarbeitet werden.

    - **Von** und **Bis** geben einen Bereich von Konten zum Verarbeiten an. Werden diese Felder nicht ausgefüllt, werden alle Konten von allen Unternehmen auf das Konsolidierungsunternehmen verschoben. Wenn Sie vier Unternehmen konsolidieren, und in jedem Unternehmen ein anderer Kontenplan vorhanden ist, werden die Konten von allen vier Unternehmen im konsolidierten Unternehmen erstellt.
    - **Konsolidierungskonto verwenden** – Wenn Sie die Option auf **Ja** setzen, wird das Feld **Auswahlquelle für Konsolidierungskonto** verfügbar. In diesem Feld wählen Sie aus, ob alle Konten mit dem Konsolidierungskonto konsolidiert werden soll, das auf der Seite **Hauptkonten** festgelegt wurde, oder Sie ein anderes Konto von einer der Konsolidierungskontogruppen auswählen möchten.
    - **Konsolidierungskontengruppe** – Wählen Sie die Gruppe aus, die für die Hauptkontozuordnung für die Konsolidierung zu verwenden ist.

- **Konsolidierungsperiode** – Verwenden Sie die Felder in diesem Abschnitt, um die Konsolidierungsperiode zu definieren.

    - **Von** und **Bis** – Geben Sie einen Datumsbereich für die Konsolidierung an. Wenn Sie dieses Feld leer lassen, wird die Konsolidierung für alle Perioden im Sachkontokalender verarbeitet, die für das Unternehmen definiert sind. Dieses Feld sollte nicht unausgefüllt bleiben.
    - **Konsolidierungsbetrag auswählen von** – Verwenden Sie dieses Feld, um anzugeben, ob die Beträge in Buchhaltungswährung oder die Beträge in Berichtswährung von den Quellunternehmen verwendet werden, um die Beträge in Buchhaltungswährung des Konsolidierungsunternehmens zu aktualisieren.

        - Wählen Sie **Buchhaltungswährung** um die Buchhaltungswährungsbeträge aus dem Quellunternehmen zu verwenden, um die Buchhaltungswährungsbeträge im Konsolidierungsunternehmen zu verwenden. Wenn dieser Wert ausgewählt ist, verwenden Sie das Feld **Konsolidierte Buchhaltungswährung**, um festzulegen, wie die Buchhaltungswährungen in der Konsolidierungsgesellschaft berechnet werden.
        - Wählen Sie **Berichtswährung** um die Berichtswährungsbeträge aus dem Quellunternehmen zu verwenden, um die Buchhaltungswährungsbeträge im Konsolidierungsunternehmen zu berechnen.

            - Wenn die Berichtswährung vom Quellunternehmen der Buchhaltungswährung des Konsolidierungsunternehmens entspricht, werden die Berichtswährungsbeträge aus dem Quellunternehmen ind Konsolidierungsunternehmen kopiert.
            - Wenn die Berichtswährung des Quellunternehmens von der Buchhaltungswährung des Konsolidierungsunternehmens abweicht, werden die Werte mithilfe der Wechselkursinformationen umgerechnet, die auf der Registerkarte **Währungsumrechnung** dieser definiert sind Seite zur Berechnung der Konsolidierungsunternehmenswerte.

    - **Buchungswährung konsolidieren** – Dieses Feld ist nur verfügbar, wenn das Feld **Konsolidierungsbetrag auswählen aus** auf **Buchhaltungswährung** eingestellt ist. Verwenden Sie es, um anzugeben, ob die Beträge in Buchhaltungswährung von den Quellfirmen durch Wechselkurse umgerechnet oder in die Konsolidierungsfirma kopiert werden. Wählen Sie **Währungsumrechnung verwenden**, um die Wechselkursinformationen zu verwenden, die auf der Registerkarte **CWährungsumrechnung** definiert sind, um die Konsolidierungsbuchhaltung zu berechnen Salden. Wählen Sie **Betrag in Buchhaltungswährung verwenden** um die Buchhaltungswährungsbeträge aus dem Quellunternehmen zum Konsolidierungsunternehmen zu kopieren.

        - Wenn die Buchhaltungswährung vom Quellunternehmen der Buchhaltungswährung des Konsolidierungsunternehmens entspricht, werden die Währungsbeträge aus dem Quellunternehmen ind Konsolidierungsunternehmen kopiert.
        - Wenn die Buchhaltungswährung des Quellunternehmens von der Buchhaltungswährung des Konsolidierungsunternehmens abweicht, werden die Werte mithilfe der Wechselkursinformationen umgerechnet, die auf der Registerkarte **Währungsumrechnung** dieser definiert zur Berechnung der Konsolidierungsunternehmenswerte.

    - **Istbeträge einbeziehen** – Legen Sie diese Option auf **Ja** fest, um die tatsächlichen Daten konsolidieren zu können.
    - **Budgetbeträge einbeziehen** – Legen Sie diese Option auf **Ja** fest, um Daten aus dem Budgetregister zu konsolidieren.
    - **Erstellen Sie Salden für die Konsolidierung neu** – Es empfiehlt sich nicht, dass Sie Option auf **Ja** festlegen. Stattdessen erstellen Sie Salden als separater Stapelverarbeitungsauftrag.

- **Budgetmodelle** – Wenn Sie ausgewählt haben, dass Budgetdaten zusammengeführt werden sollen, verwenden Sie die Felder in diesem Abschnitt, um Budgetmodelle zu definieren.

    - **Von** und **Bis** geben einen Bereich von Modellen zum Verarbeiten an.
    - **Budgetkurstyp** – Wählen Sie den Typ des Budgetsatzes aus, um für Währungsumrechnung von Budgetdaten zu verwenden.

## <a name="financial-dimensions"></a>Finanzdimensionen
**Finanzdimensionen** Auf der Registerkarte definieren Sie die Dimensionen, die im Konsolidierungsunternehmen einbezogen werden sollen. Wenn Sie eine Dimension auswählen, legen Sie das Feld **Spezifikation** auf **Dimension** fest, und definieren Sie dann die Reihenfolge der Dimension im Konsolidierungsunternehmen.

![Registerkarte „Finanzdimensionen“.](./media/financial-dimensions-cons.png "Registerkarte „Finanzdimensionen“")

Unabhängig von der Reihenfolge, die Sie definieren, ist immer **Hauptkonto** das erste Segment.

## <a name="legal-entities"></a>Juristische Personen
Auf der Registerkarte **Juristische Personen** definieren Sie die Dimensionen, die im Konsolidierungsunternehmen einbezogen werden sollen. Sie können auch den Besitzprozentsatz dieser Unternehmen definieren. Wenn Sie einem Besitz von weniger als 100 Prozent angeben, wird der angegebene Prozentsatz auf das Konsolidierungsunternehmen zusammengefasst. Für alle Übersetzungsdifferenzen wird das Feld **Kontenart für Konvertierungsdifferenzen** verwendet, um das Hauptkonto aus der Einstellung auf der Seite **Konten für automatische Buchungen** auszuwählen.

![Registerkarte „Juristischen Personen“.](./media/legal-entities-cons.png "Registerkarte „Juristische Personen“")

![Seite „Konten für automatische Buchungen“.](./media/accounts-for-automatic-cons.png "Seite „Konten für automatische Buchungen“")

## <a name="elimination"></a>Löschung
Auf der Registerkarte **Löschung** haben Sie drei Optionen zum Verarbeiten von Vorkalkulationen:

- Dient zum Auswählen der Löschungsregel, und dann im Feld **Vorschlagsoptionen** aus, wählen Sie **Nur Vorschlag** aus. Diese Option verarbeitet die Löschung während des Konsolidierungsprozesses, wird aber nicht alle in einem Schritt buchen. Sie können die Erfassung später buchen.
- Dient zum Auswählen der Löschungsregel, und dann im Feld **Vorschlagsoptionen** wählen Sie **Nur Vorschlag** aus. Diese Option verarbeitet die Löschung während des Konsolidierungsprozesses und wird alle in einem Schritt buchen.
- Führen Sie den Löschungvorschlag getrennt vom Konsolidierungsprozesses als indem Sie die Löschungserfassung ausführen.

![Registerkarte „Löschung“.](./media/elimination-cons-onl.png "Registerkarte „Löschung“")

Weitere Informationen zur Löschung finden Sie unter [Löschungsrichtlinien](./elimination-rules.md)

## <a name="currency-translation"></a>Währungsumrechnung
Auf der Registerkarte **Währungsumrechnung** definieren Sie die juristische Person, das Konto und den Wechselkurstyp und den Wechselkurs. Wenn das Konsolidierungsunternehmen anderen Hauptkonten als das Quellunternehmen zugeordnet ist, muss das Hauptkonto des Konsolidierungsunternehmens in den Feldern **Von Datum** und **Bis Datum** nicht die Hauptkonten des Quellunternehmens. Für jede Zeile der juristischen Person und Hauptkonten sind im Feld **Wechselkurs anwenden von** drei Optionen verfügbar:

- **Konsolidierungsdatum** – Das Datum, das im Feld **Konsolidierungszeitraum bis** auf der Registerkarte **Kriterien** für die Konsolidierung werden zum Abrufen des Wechselskures verwendet. Der Kurs der Entität entspricht der Spot- oder Monatendkurs. Sie sehen eine Vorschau des Satzes, aber Sie können ihn nicht bearbeiten.
- **Buchungsdatum** – Das Datum jeder Buchung wird verwendet, um einen Wechselkurs auszuwählen. Diese Option ist für Anlagen häufig und wird oft als historischer Satz bezeichnet. Sie können eine Vorschau des Satzes nicht finden, da es viele Sätze für die verschiedenen Buchungen im Kontenbereich gibt.
- **Benutzerdefinierter Satz** – Wenn Sie diese Option aktivieren, können Sie den Wechselkurs eingeben, den Sie wünschen. Diese Option kann für durchschnittliche Wechselkurse hilfreich sein oder wenn Sie mit einem festen Wechselkurs konsolidieren.

![Registerkarte „Währungsumrechnung“.](./media/currency-translation-cons-online.png "Registerkarte „Währungsumrechnung“")

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Weitere Informationen zur Konsolidierung und Währungsumrechnung finden Sie im übergeordneten Artikel [Finanzkonsolidierungen und Übersicht zur Währungsumrechnung](./financial-consolidations-currency-translation.md).

Informationen zum Szenarien, in denen Sie möglicherweise Finanzaufstellungen generieren können, finden Sie unter [Konsolidierte Finanzaufstellungen erstellen](./generating-consolidated-financial-statements.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
