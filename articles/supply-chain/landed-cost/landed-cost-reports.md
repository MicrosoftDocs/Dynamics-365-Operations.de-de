---
title: Berichte über kalkulierte Kosten
description: Dieses Thema beschreibt, wie Sie die verschiedenen Arten von Berichten finden und verwenden, die für das Modul Gesamttransportkosten verfügbar sind.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 41588b7dc037f6d748bac818f8707540ce8afe8d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020958"
---
# <a name="landed-cost-reports"></a>Gesamttransportkosten-Berichte

[!include [banner](../../includes/banner.md)]

## <a name="outstanding-invoices"></a>Ausstehende Rechnungen

Der Bericht „Ausstehende Rechnungen“ enthält eine Liste aller ausstehenden Rechnungen der verschiedenen Kostenstufen, die mit jeder Fahrt verbunden sind. Er wird verwendet, um die Fahrt und die Kalkulationen zusammen mit der Liste der Ledger-Transaktionen regelmäßig abzustimmen. Nachdem eine Gemeinkostenzahl kalkuliert wurde, wird sie aus dem Bericht entfernt.

Um einen Bericht über ausstehende Rechnungen zu erstellen, gehen Sie wie folgt vor.

1. Gehen Sie zu **Gesamttransportkosten \> Berichte \> Nachverfolgung \> Ausstehende Rechnungen**.
1. Geben Sie in der Dialogbox **Ausstehende Rechnungen** im Feld **Am Datum** ein Datum an. Alle Rechnungen, die an oder vor diesem Datum ausstehend waren, werden in die Ausgabe einbezogen.
1. Wählen Sie unter **Anzeigen** eine der folgenden Optionen:

    - **Kosten nicht kalkuliert** - Schließt Kosten für fakturierte Sendungen ein, die einen geschätzten Kostenwert, aber keine tatsächlichen Kosten haben.
    - **Kosten nicht kalkuliert** - Schließen Sie Kosten ein, die zwar kalkuliert wurden, für die aber noch keine Einkaufsbestellung eingegangen ist.
    - **Alles nicht kalkuliert** - Schließt die Ergebnisse sowohl der Option **Kosten nicht kalkuliert** als auch der Option **Bestand nicht kalkuliert** ein.

1. Legen Sie die Option **Neue Kosten einbeziehen** auf *Ja* fest, um Kosten einzubeziehen, für die noch keine Kalkulation vorliegt und für die noch kein Bestand eingegangen ist. Wenn Sie sie auf *Nein* festlegen, enthält der Bericht nur Kosten, die bereits kalkuliert wurden.
1. Aktivieren Sie im Bereich **Ansicht** jede Art von Detail, das Sie in den Bericht aufnehmen wollen.
1. Wie bei anderen Berichtstypen in Microsoft Dynamics 365 Supply Chain Management wählen Sie im Inforegister **Ziel** das Ausgabeformat des Berichts.
1. Wie bei anderen Berichtstypen im Supply Chain Management verwenden Sie die Registerkarte **Einzuschließende Datensätze**, um die Datensätze, die in den Bericht aufgenommen werden sollen, weiter einzuschränken.
1. Klicken Sie auf **OK**, um den Bericht zu generieren.

## <a name="activityprovider-analysis-reports"></a>Aktivitäts-/Lieferanten-Analyseberichte

Mit den Aktivitäts-/Provider-Analyseberichten können Sie die Genauigkeit Ihrer Zeitschätzungen für jeden Provider überprüfen.

Um einen Aktivitäts-/Anbieter-Analysebericht zu erstellen, gehen Sie wie folgt vor.

1. Je nachdem, welche Art von Bericht Sie erstellen möchten, führen Sie einen der folgenden Schritte aus:

    - Gehen Sie zu **Gesamttransportkosten \> Berichte \> Analyse der Aktivität/des Anbieters nach Aktivität**. In diesem Fall werden die Zeitschätzungen nach Aktivität gruppiert.
    - Gehen Sie zu **Gesamttransportkosten \> Berichte \> Analyse der Aktivität/des Anbieters nach Anbieter**. In diesem Fall werden die Zeitschätzungen nach Anbieter gruppiert.

    Es erscheint entweder die Dialogbox **Analyse der Aktivität/des Providers nach Aktivität** oder die Dialogbox **Analyse der Aktivität/des Providers nach Provider**. Beide Dialogfelder bieten die gleichen Optionen.

1. Wie bei anderen Arten von Berichten im Supply Chain Management verwenden Sie das Inforegister **Ziel**, um das Ausgabeformat des Berichts auszuwählen.
1. Wie bei anderen Berichtstypen im Supply Chain Management verwenden Sie die Registerkarte **Einzuschließende Datensätze**, um die Datensätze, die in den Bericht aufgenommen werden sollen, weiter einzuschränken.
1. Klicken Sie auf **OK**, um den Bericht zu generieren.

## <a name="voyage-costing-reports"></a>Berichte zur Kalkulation von Fahrten

Die Berichte zur Fahrtkalkulation zeigen die Kosten der Artikel und die Importkosten pro Palette, Transportcontainer oder Fahrt an, abhängig von den Optionen, die Sie beim Erstellen des Berichts auswählen. In jedem Fahrtkalkulationsbericht können Sie die geschätzten Kosten einer Fahrt im Vergleich zu den tatsächlichen Kosten sehen, und er kann nach den verschiedenen identifizierenden Faktoren aufgeschlüsselt werden.

Um einen Bericht zur Kalkulation einer Fahrt zu erstellen, gehen Sie wie folgt vor.

1. Je nachdem, welche Art von Bericht Sie erstellen möchten, führen Sie einen der folgenden Schritte aus:

    - Gehen Sie zu **Gesamttransportkosten \> Berichte \> Kalkulation \> Fahrtkalkulation nach individuellen Kosten**. In diesem Fall zeigt die Option „Individuelle Kosten“ die importierten Kalkulationen pro Kostenbereich pro Kostenartencode an.
    - Gehen Sie zu **Gesamttransportkosten \> Berichte \> Kalkulation \> Kalkulation der Fahrt nach Berichtsart**. In diesem Fall werden die Importkosten nach den verschiedenen Berichtskategorien aufgeschlüsselt. Die Kalkulationen werden nach Berichtskategorien gruppiert.

    Es erscheint entweder die Dialogbox **Fahrtkalkulation nach Einzelkosten** oder die Dialogbox **Fahrtkalkulation nach Berichtskategorie**. Diese Dialogfelder sind ähnlich aufgebaut. Etwaige Unterschiede werden im weiteren Verlauf dieser Anleitung erläutert.

1. Wenn Sie die Dialogbox **Fahrtkalkulation nach Berichtskategorie** geöffnet haben, wählen Sie im Feld **Kosten** einen der folgenden Werte:

    - **Kostenwert** - Der Wert wird entweder mit Hilfe der Autokalkulation berechnet oder manuell im Kostenbereich erstellt.
    - **Geschätzt** - Nach dem Eingang der Waren wird der geschätzte Kostenwert festgelegt.
    - **Ist** - Nachdem die Bestellung fakturiert wurde, werden die tatsächlichen Kosten auf die Kosten der Rechnung festgelegt.
    - **Beste** - Das System verwendet diejenige der drei vorherigen Optionen, die am genauesten ist. (Wir empfehlen, diese Option zu wählen.)

1. Legen Sie die Option **Pro Artikel** auf *Ja* fest, um die Kalkulation für jeden Artikel anzuzeigen. Legen Sie sie auf *Nein* fest, um die Kalkulation pro Fahrt anzuzeigen.
1. Wählen Sie im Bereich **Ansicht** die Kategorien, nach denen die Kalkulation aufgeschlüsselt werden soll.
1. Wählen Sie im Bereich **Dimensionen** die Dimensionen aus, die in den Bericht aufgenommen werden sollen.
1. Wie bei anderen Arten von Berichten im Supply Chain Management verwenden Sie das Inforegister **Ziel**, um das Ausgabeformat des Berichts auszuwählen.
1. Wie bei anderen Berichtstypen im Supply Chain Management verwenden Sie die Registerkarte **Einzuschließende Datensätze**, um die Datensätze, die in den Bericht aufgenommen werden sollen, weiter einzuschränken.
1. Klicken Sie auf **OK**, um den Bericht zu generieren.

## <a name="shipping-container-receipts-list"></a>Liste der Versandcontainerzugänge

Die Liste der Transportcontainer-Eingänge enthält alle nicht eingegangenen Mengen, die an oder vor einem erwarteten Datum fällig sind. Lagerort-Mitarbeiter können diesen Bericht verwenden, um die erwarteten Waren auf einem Transportcontainer zu identifizieren. Er kann auch verwendet werden, um Waren manuell zu validieren, wenn sie in einem Transportcontainer eingehen.

Führen Sie die folgenden Schritte aus, um eine Transportcontainer-Eingangsliste zu erstellen.

1. Gehen Sie zu **Gesamttransportkosten \> Berichte \> Tracking \> Transportcontainer-Eingangsliste**.
1. Geben Sie in der Dialogbox **Liste der Transportcontainer-Eingänge** im Feld **Erwartetes Datum** ein Datum an. Alle Mengen, die an oder vor diesem Datum nicht empfangen wurden, werden in der Ausgabe berücksichtigt.
1. Wählen Sie im Bereich **Dimensionen** die Dimensionen aus, die in den Bericht aufgenommen werden sollen.
1. Wie bei anderen Arten von Berichten im Supply Chain Management verwenden Sie das Inforegister **Ziel**, um das Ausgabeformat des Berichts auszuwählen.
1. Wie bei anderen Berichtstypen im Supply Chain Management verwenden Sie die Registerkarte **Einzuschließende Datensätze**, um die Datensätze, die in den Bericht aufgenommen werden sollen, weiter einzuschränken.
1. Klicken Sie auf **OK**, um den Bericht zu generieren.

## <a name="expected-delivery-report"></a>Bericht zur erwarteten Lieferung

Der Bericht über die erwartete Lieferung enthält grundlegende Informationen über die Fahrt, den Transportcontainer, die Palette, die Artikel und das erwartete Lieferdatum.

Um einen Bericht über die erwartete Lieferung zu erstellen, gehen Sie wie folgt vor.

1. Gehen Sie zu **Gesamttransportkosten \> Berichte \> Nachverfolgung \> Erwartete Lieferung**.
1. Wählen Sie in der Dialogbox **Erwartete Lieferung** im Feld **Erwartetes Datum** das Datum, an dem die Lieferung der Waren an das endgültige Ziellagerort erwartet wird. Jede Zeile der Fahrt, die ein erwartetes Datum an oder vor diesem Datum hat und noch nicht empfangen wurde, wird in die Ausgabe einbezogen.
1. Optional: Wählen Sie im Feld **Lieferantenkonto** ein Lieferantenkonto aus, um nur Lieferungen von einem bestimmten Lieferanten einzuschließen.
1. Wählen Sie im Bereich **Dimensionen** die Dimensionen aus, die in den Bericht aufgenommen werden sollen.
1. Wie bei anderen Arten von Berichten im Supply Chain Management verwenden Sie das Inforegister **Ziel**, um das Ausgabeformat des Berichts auszuwählen.
1. Wie bei anderen Berichtstypen im Supply Chain Management verwenden Sie die Registerkarte **Einzuschließende Datensätze**, um die Datensätze, die in den Bericht aufgenommen werden sollen, weiter einzuschränken.
1. Klicken Sie auf **OK**, um den Bericht zu generieren.
