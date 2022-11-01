---
title: Währungsneubewertung für Kreditoren- und Debitorenkonten
description: Dieser Artikel gibt Informationen zum Prozess der Neubewertung der Fremdwährung, der ausgeführt wird, um den Wert offener Buchungen in "Kreditoren" und "Debitoren" zu aktualisieren.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustExchRateAdjustment, VendExchRateAdjustment
audience: Application User
ms.reviewer: kfend
ms.custom: 14211
ms.assetid: defb1ea5-1f3e-4859-87d8-3f9954d3f388
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73f20323ff2eb36c89f4fb2848a056c2cb24ec30
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715720"
---
# <a name="currency-revaluation-for-accounts-payable-and-accounts-receivable"></a>Währungsneubewertung für Kreditoren- und Debitorenkonten

[!include [banner](../includes/banner.md)]

Schwankungen in den Wechselkursen sorgen langfristig für Veränderungen im theoretischen Wert (Buchwert) offener Buchungen in Fremdwährungen. Dieser Artikel gibt Informationen zum Prozess der Neubewertung der Fremdwährung, der ausgeführt wird, um den Wert offener Buchungen in "Kreditoren" und "Debitoren" zu aktualisieren. 

Der theoretische Wert oder Buchwert offener Transaktionen in Fremdwährungen verändert sich über längere Zeiträume wegen Schwankungen der Wechselkurse. Um den Wert offener Transaktionen in "Kreditoren" und "Debitoren" zu aktualisieren, führen Sie den Prozess zur Neubewertung der Fremdwährung aus. Neubewertung der Fremdwährung kann sowohl für "Kreditoren" als auch "Debitoren" ausgeführt werden. Der Prozess verwendet einen neuen Wechselkurs zur Neubewertung der offenen Beträge oder der nicht ausgeglichenen Beträge an einem bestimmten Datum. Die Unterschiede zwischen der ursprünglichen gebuchten Beträge und die vorkalkulierten Beträge einen neu führen unrealisierten Gewinn oder ein Verlust für alle offenen Posten. Die Kreditoren und Debitoruntergeordneten sachkonten werden dann aktualisiert, um den unrealisierten Gewinn oder der Verlust widerzuspiegeln, und ein wird Buchhaltungseintrags im Hauptbuch gebucht.

## <a name="simulate-a-foreign-currency-revaluation"></a>Simulieren einer Neubewertung der Fremdwährung
Bevor Fremdwährungsbeträge in offenen Debitorentransaktionen neu bewertet werden, können Sie einen Simulationsbericht der Neubewertung der Fremdwährung für dasselbe Datum und dieselbe Methode ausführen. Um den Simulationsbericht auf der Seite **Neubewertung der Fremdwährung** auszuführen, klicken Sie auf die Schaltfläche **Simulation**. Der Bericht bietet eine Vorschau des Betrags des unrealisierten Gewinns/Verlusts, auf Grundlage der Parameter, die für die Simulation definiert werden.

## <a name="process-a-foreign-currency-revaluation"></a>Eine Neubewertung der Fremdwährung verarbeiten
Mithilfe von **Neubewertung der Fremdwährung** Seite unter **Periodische Aufgaben** um offene Posten neu bewerten. Sie können den Prozess in die Echtzeit ausführen oder ihn planen, damit er als Stapel ausgeführt wird. Wenn Sie die Einstellungen für definieren der Neubewertungsprozess, achten Sie darauf, um zu prüfen, ob Sie einen Bericht der Ergebnisse drucken möchten. Der Neubewertungsbericht kann nicht erneut gedruckt werden, nachdem der Vorgang abgeschlossen ist. Wenn Sie den Bericht zur Neubewertung der Fremdwährung generieren, wird er verschiedene Salden auf der Debitoren- bzw. Kreditorenebene und der Währungsebene anzeigen:

-   Die Salden von Debitoren oder Kreditoren mit Fremdwährungstransaktionen, die neu bewertet wurden. Die folgenden Salden werden angezeigt:
    -   Der gesamte ursprüngliche Saldo in der Fremdwährung.
    -   Der Gesamtbetrag in Fremdwährung in der Buchhaltungswährung, seit der vorherigen Neubewertung.
    -   Der Gesamtbetrag in Fremdwährung in der Buchhaltungswährung, seit der aktuellen Neubewertung.
    -   Die Differenz zwischen der vorherigen und aktuellen Neubewertung. Diese Differenz ist der zusätzliche unrealisierte Gewinn oder Verlust.
-   Der gesamte unrealisierte Gewinn oder Verlust für jede Währung.

Jedes Mal, wenn Sie eine Neubewertung der Fremdwährung ausführen, wird ein Datensatz gespeichert. Vom Datensatz auf der Seite **Bewertung der Fremdwährung** wählen Sie die Option **Transaktionen** aus, um die detaillierte Liste der Transaktionen anzuzeigen, die wegen der Neubewertung erstellt wurden. Jede Belegbuchung stellt den offenen Posten angezeigt, der neu bewertet wurde. Wenn ein offener Posten mehrmals neu bewertet wurde, finden Sie zwei Datensätze, die den gleichen Beleg verwenden. Ein Datensatz ist für die Stornierung des vorherigen unrealisierten Gewinn- oder Verlustbeträge, und ein neuer Datensatz ist für den unrealisierten Gewinn oder der Verlust. Um den Neubewertungsprozess auszuführen, klicken Sie auf die Schaltfläche **Neubewertung der Fremdwährung**. Definieren Sie entsprechende Einstellungen für die folgenden Parameter:

-   **Methode** – Die Methode, die beim ausgewählten Einzelvorgang zur Neubewertung der Fremdwährung verwendet wird:
    -   **Standard** – Einzelvorgänge zur Neubewertung der Fremdwährung werden immer gebucht, unabhängig davon, ob das Ergebnis ein Gewinn oder ein Verlust ist.
    -   **Minimum** – Einzelvorgänge zur Neubewertung der Fremdwährung werden nur gebucht, wenn das Ergebnis ein Verlust ist.
    -   **Rechnungsdatum** – Bei Einzelvorgängen zur Neubewertung der Fremdwährung wird der ursprüngliche Wechselkurs der Transaktionen verwendet, die gemäß dem ursprünglichen Wert in der Buchhaltungswährung neu bewertet werden. Die Auswirkungen früherer Neubewertungen der Fremdwährung werden storniert.
-   **Bewertungsstichtag** – Das Datum, an dem nach allen Transaktionen gesucht wird, die an diesem Datum offene (nicht ausgeglichene) Beträge aufweisen. Fremdwährungsbeträge werden mithilfe der Wechselkurse neu bewertet, die auf der Seite **Währungswechselkurse** für den Bewertungsstichtag eingegeben wurden. Wenn Fremdwährungsbeträge an einem Bewertungsstichtag neu bewertet werden, wird dieses Datum als Datum der letzten Neubewertung der Fremdwährung für die regulierten Buchungen festgelegt. Sollten Sie eine Neubewertung der Fremdwährung für einen Bewertungsstichtag ausführen, der vor dem Datum der letzten Neubewertung der Fremdwährung von bereits regulierten Transaktionen liegt, reguliert der periodische Einzelvorgang keine Transaktionen, die am früheren Bewertungsstichtag offen sind, aber die ein aktuelleres letztes Datum für die Neubewertung der Fremdwährung haben.
-   **Kursdatum** – Das Datum, anhand dessen der Wechselkurs bestimmt wird, der bei der Neubewertung der Fremdwährung verwendet wird.
-   **Verwenden des Buchungsprofils aus** – Das Buchungsprofil, das verwendet wird, um das standardmäßige Hauptkonto einzugeben für "Debitoren" oder "Kreditoren" für die Buchhaltungseinträge der Transaktionen zur Neubewertung der Fremdwährung:
    -   **Buchung** – Das Buchungsprofil der Debitorentransaktion wird verwendet.
    -   **Auswählen** – Geben Sie das Buchungsprofil im Feld **Buchungsprofil** ein.
-   **Buchungsprofil** – Wenn die Option **Auswahl** im Feld **Verwenden des Buchungsprofils aus** ausgewählt wird, bestimmt das Buchungsprofil, das sie in diesem Feld eingeben, das Buchungsprofil der Transaktionen zur Neubewertung der Fremdwährung.
-   **Finanzdimensionen**: Die Finanzdimensionen, die bei den Buchungseinträgen der Transaktionen zur Neubewertung der Fremdwährung gebucht werden. Die Finanzdimensionen werden nicht anhand der Regeln für die Kontostruktur geprüft. Die Kontostruktur, die zum Zeitpunkt der Rechnungsstellung vorhanden war, entspricht möglicherweise nicht den Regeln, die bei der Neubewertung gegolten haben. Es gibt keine Möglichkeit, bestimmte Finanzdimensionen im Neubewertungsprozess auszuwählen, sodass die Prüfung der Kontostruktur übersprungen wird.  
    -   **Kein** – Keine Finanzdimensionen werden gebucht. Wenn Sie eine erforderliche Finanzdimension in der Kontostruktur haben, wird der Neubewertungsprozess weiterhin ausgeführt und er erstellt Buchhaltungseinträge, die keine Finanzdimensionen haben. Sie erhalten zuerst einen Warnmeldung, um die Neubewertung stornieren zu können.
    -   **Tabelle** – Die Finanzdimensionen des Debitorenkontos oder Kreditorenkontos werden bei den Transaktionen zur Neubewertung der Fremdwährung gebucht.
    -   **Buchung** – Die Finanzdimensionen der Transaktion, die neu bewertet wird, werden bei den Transaktionen zur Neubewertung der Fremdwährung gebucht. Standardmäßig werden die Finanzdimensionen aus dem Sachkonto für Debitoren und Kreditoren der ursprünglichen Transaktion für das Hauptkonto für Debitoren und Kreditoren der Neubewertungstransaktion verwendet. Die Finanzdimensionen des Sachkontos für Ausgaben/Anlage/Umsatz der ursprünglichen Transaktion werden außerdem für das Hauptkonto für unrealisierten Gewinn/Verlust der Neubewertungstransaktion verwendet.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
