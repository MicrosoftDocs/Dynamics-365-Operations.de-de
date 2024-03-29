---
title: Seite mit Lieferantentransaktionen
description: Dieser Artikel enthält Informationen zur Kreditorenbuchungslistenseite für Microsoft Dynamics 365 Finance.
author: sunfzam
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 34d9fd29f6a28bdd8c62e9460093544699dfeb2c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859942"
---
# <a name="vendor-transactions-list-page"></a>Seite mit Lieferantentransaktionen

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Ausgleiche anzeigen

Die Registerkarte **Ausgleiche anzeigen** im Aktivitätsbereich bietet schnellen Zugriff auf die Ausgleichshistorie und zu detaillierte Informationen über die Ausgleichsbuchung. Sie können zusätzliche Buchungen, die mit der ausgewählten Buchung zusammenhängen, mögliche auch anzeigen, da sie Bestandteil desselben Ausgleichs waren, oder es sind sie Zahlungen, die in derselben Zahlungserfassung erstellt wurden.

1. Wählen Sie **Kreditorenkonten \> Alle Kreditoren** aus.
2. Wählen Sie einen Lieferant, der Transaktionen aufweist, und klicken Sie dann im Aktivitätsbereich, auf der Registerkarte **Lieferant**, wählen Sie **Buchungen** aus.
3. Wählen Sie eine Transaktion aus und klicken Sie dann im Aktivitätsbereich und wählen **Ausgleiche anhzeigen** aus.

    Das Dialogfeld **Ausgleich anzeigen** wird geöffnet und zeigt die ausgewählte Buchung und alle Dokumente an, die ausgeglichen werden. Dieses Dialogfeld zeigt die Ausgleichshistorieansicht, allerdings werden alle zugeordneten Dokumente einbezogen.

4. Im Dialogfeld können verschiedene Funktionen ausführen. Wählen Sie einen oder mehrere Belege aus und wählen Sie dann eine der folgenden Schaltflächen:

    - **Zugehöriges anzeigen** – Zeigt alle Zahlungserfassungstransaktionen und allgemeinen Erfassungstransaktionen für den Kreditor an, die in den Erfassungen erstellt wurden, in denen die in der Liste angezeigten Dokumente erstellt wurden. Wenn zum Beispiel eine Zahlung angezeigt wird, werden alle Zahlungen in der Zahlungserfassung, in der sie erstellt wurde, angezeigt. Wenn eine Rechnung oder Zahlung angezeigt wird und in einer allgemeinen Erfassung erstellt wurde, werden alle Dokumente in der allgemeinen Erfassung, in der sie erstellt wurde, angezeigt. Darüber hinaus werden alle Ausgleiche in Zusammenhang mit Dokumentenlisten angezeigt. Während Sie verwandte Zahlungen anzeigen, ändert die Bezeichnung dieser Schaltfläche zu **Ausgleiche anzeigen**. Wählen Sie **Ausgleiche anzeigen**, um nur die Buchungen anzuzeigen, die angezeigt wurden, als Sie  das Dialogfeld **Ausgleiche anzeigen** geöffnet haben.
    - **Verlauf anzeigen** – Zeit den Ausgleichsverlauf für die Belege an. Klicken Sie auf **Schließen**, um die Dialogfelder zu schließen.
    - **Buchhaltung anzeigen** - Alle Belege anzeigen, die zu den ausgewählten Dokumenten gehören. Klicken Sie auf **Schließen**, um die Dialogfelder zu schließen.
    - **Exportieren** – Exportiert die ausgewählten Belege in Microsoft Excel.
    - **Ausgleichen von Transaktionen** – Diese Schaltfläche wird angezeigt, wenn das ursprüngliche Dokument, das ausgewählt wurde, nicht vollständig ausgeglichen wurde. Wenn Sie diese Schaltfläche auswählen, wird das Dialogfeld **Transaktion ausgleichen** angezeigt, in dem Sie Buchungen für den Ausgleich auswählen können.
    - **Ausgleich rückgängig machen** – Diese Schaltfläche wird nur angezeigt, wenn das ursprünglich ausgewählte Dokument vollständig ausgeglichen wurde. Wenn Sie diese Schaltfläche auswählen wird das Dialogfeld **Ausgleiche rückgängig machen** angezeigt, in dem Sie die Ausgleiche rückgängig machen können, die für das Dokument ausgeführt wurden.

## <a name="global-transactions"></a>Globale Transaktionen

Die Schaltfläche **Globale Transkationen** wird auch auf der Listenseite **Lieferantentransaktionen** angezeigt. Mit dieser Schaltfläche können Sie die Transaktionen für einen Kreditor für alle juristischen Personen anzeigen. Die Listenseite **Kreditorentransaktionen** zeigt Transaktionen nur für die juristischen Personen, für die der Benutzer Zugriff hat, basierend auf den Sicherheitseinstellungen.

Die Listenseite enthält alle Transaktionen für Lieferanten, die dieselbe Kennung wie der Lieferant hat, mit dem Sie mit gestartet haben. Wenn beispielsweise Lieferant US-001 in einer juristischen Personen dieselbe Kennung wie DE-001 Lieferant in einer anderen juristischen Person hat, werden alle Transaktionen für beide Lieferanten-IDs angezeigt.

Die Menüs auf der Listenseite **Lieferantentransaktionen** variieren, je nach der juristischen Person für die Buchung. Wenn zum Beispiel eine Funktion nur für schweizerische juristische Personen verfügbar ist, werden die Menüoptionen für diese Funktion, wenn eine schweizerischen Buchung ausgewählt wurde.

Wenn Sie auf die Funktion zugreifen wollen, führen sie die folgenden Schritte aus.

1. Wählen Sie **Kreditorenkonten** \> **Alle Kreditoren aus**.
2. Wählen Sie einen Lieferant  und klicken Sie dann im Aktivitätsbereich, auf der Registerkarte **Lieferant** unter **Transaktionen** auf Gruppe und wählen Sie **Globale Transaktionen**.

## <a name="more-transaction-filters"></a>Weitere Transaktionsfilter

Der Filter zum Anzeigen offener Buchungen ist durch einen neuen Filter ersetzt, mit dem Sie mehr  Kombinationen von Buchungen anzeigen können. Die folgenden Option stehen im Feld **Anzeigen** zur Verfügung:

- **Alle** – Hiermit können Sie die offenen und geschlossenen Transaktionen für den ausgewählten Kreditor anzeigen (offen oder geschlossen).
- **Geschlossen** – Zeigt nur Transaktionen, die vollständig ausgeglichen und geschlossen wurden.
- **Offen** – Zeigt nur Transaktionen, die nicht vollständig ausgeglichen und geschlossen wurden.
- **Offen, einschließlich geschlossen am oder nach Datum** – Nur Transaktionen anzeigen, die an oder nach einem angegeben Datum nicht vollständig ausgeglichen wurden. Wenn Sie diese Option auswählen, können Sie das Datum ändern, das neben dem Filter angezeigt wird. Buchungen, die einen Wert nach dem **Letzter Ausgleichsdatum** nach oder an dem von Ihnen definierten Datum aufweisen, werden in der Liste angezeigt, wenn dieser Posten vollständig auf dem aktuellen Datum ausgeglichen werden. Allerdings wird der Saldo die Saldenliste ab dem aktuellen Datum, und nicht ab dem ausgewählten Datum.

Aktivieren Sie das Kontrollkästchen **Währungsneubewertungen ausblenden**, um Transaktionen für Währungsumrechnungen auszublenden.

## <a name="modify-due-dates-and-discount-dates"></a>Ändern von Fälligkeitsdatum und Skontodatum

Sie können Fälligkeitsdatum und Skontodatum für offene Debitorbuchungen aktualisieren. In der Freigabe 8.1 können Sie nun Fälligkeitsdaten der Listenseite **Lieferantentransaktionen** hinzufügen. Wenn Sie auf dem Fälligkeitsdatum in der Listenseite **Kreditorenbuchungen** klicken, können Sie Zahlungsbedingungen, Fälligkeitsdatum, Skontodatum und Skontobedingungen im Dialogfeld **Fälligkeitsdatum- und -Skontodatumsangaben aktualisieren** auch ändern.

### <a name="activate-the-feature"></a>Aktivieren der Funktion

Um Fälligkeitsdatem der Listenseite **Lieferantentransaktionen** hinzuzufügen und Zahlungseinstellungen für eine Transaktion mithilfe des Dialogfelds **Fälligkeitsdatum- und -Skontodatumsangaben aktualisieren** zu ändern, folgend Sie den folgenden Schritten.

1. Wechseln Sie zu **Kreditorenkonten \> Einstellung \> Kreditorenkontenparameter**.
2. Auf der Registerkarte **Ausgleiche** setzen Sie die Option **Fälligkeitsdatum anzeigen und bearbeiten zulassen** auf **Ja**.
3. Um diese Funktion zu aktivieren, wurden neue Felder der Lieferantentransaktionen hinzugefügt. Diese Felder werden ausgefüllt, wenn eine neue Buchung abgeschlossen ist. Sie werden auch ausgefüllt, wenn Sie das Dialogfeld **Aktualisierungsfälligkeitsdatum und Skontodatumsangaben** öffnen. Wenn Sie die Option **Fälligkeitsdatum anzeigen und bearbeiten zulassen** auf **Ja** festlegen, können Sie das Dialogfeld **Aktualisierungszahlungsinformation** finden.  Um vorhandene Buchungen sofort zu aktualisieren, wählen Sie **Alle vorhandenen Buchungen aktualisieren** aus. Alternativ, um nur die Felder für neue Buchungen zu füllen, wählen Sie **Fahren Sie fort ohne Aktualisierung**.

Das Fälligkeitsdatum wird nun der Listenseite **Lieferantentransaktionen** hinzugefügt, und Sie können die Skontodatumsangaben und das Fälligkeitsdatum für Transaktionen einfacher ändern.

### <a name="modify-the-payment-settings"></a>Ändern der Zahlungseinstellungen

Die Listenseite **Lieferantentransaktionen** zeigt alle Transaktionen für einen Lieferanten. Wenn Sie das Fälligkeitsdatum für eine Transaktion auswählen, wird ein Dialogfeld angezeigt. Dieses Dialogfeld zeigt das Basisdatum für das Fälligkeitsdatum und Rabattberechnungen, das Fälligkeitsdatum, die Zahlungsbedingungen, die Skontobedingungen, und die Skontodatumsangaben an.

Jedes Feld hat Auswirkungen auf eine andere Buchung, wenn Sie sie bearbeiten:

- **Grunddatum bearbeiten** - Das Fälligkeits- und das Skontodatum werden geändert, wenn das Grunddatum dem Dokumentdatum entspricht.
- **Bearbeiten Sie das Fälligkeitsdatum:** - Nur das Fälligkeitsdatum wird geändert
- **Bearbeiten Sie das Skontodatum** - Nur das Skontodatum werden geändert.
- **Zahlungsbedingungen ändern** - Das Fälligkeitsdatum wird geändert, basierend auf dem Grunddatum und dem Zahlungsbedingungen.
- **Bearbeiten Sie die Skontobedingungen** - Die Skonti werden basierend auf dem Grunddatum und den Skontobedingungen geändert.

Um die Bearbeitung der Zahlungseinstellungen abzuschließen wählen Sie **Schließen**, um die Änderungen zu speichern.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
