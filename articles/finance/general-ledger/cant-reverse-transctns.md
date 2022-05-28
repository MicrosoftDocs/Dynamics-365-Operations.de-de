---
title: Warum kann ich diese Buchung nicht stornieren?
description: In diesem Thema werden verschiedene Gründe beschrieben, warum Buchungen nicht storniert werden können. Es führt auch Lösungen für dieses Problem auf.
author: kweekley
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e18caf1dbdf8191713c17b1793f5da44cf2f182b
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724528"
---
# <a name="why-cant-i-reverse-this-transaction"></a>Warum kann ich diese Buchung nicht stornieren?

[!include [banner](../includes/banner.md)]

In diesem Thema werden verschiedene Gründe beschrieben, warum Buchungen nicht storniert werden können. Es führt auch Lösungen für dieses Problem auf.

## <a name="symptom"></a>Symptom

Es kann vorkommen, dass Unternehmen eine von ihnen gebuchte Buchung stornieren müssen. Gelegentlich verhindert das System, dass diese Buchungen storniert gemacht werden. Dieses Verhalten kann zwei Fragen aufwerfen:

- Warum kann ich die Buchung nicht stornieren?
- Wie wirkt sich die Funktion zur Massenstornierung auf dieses Verhalten aus?

## <a name="resolution"></a>Lösung

Buchungen müssen bestimmte Kriterien erfüllen, bevor sie storniert werden können. Die restlichen Abschnitte dieses Themas enthalten die Überprüfung für jedes Modul. Obwohl sich dieses Thema auf Buchungen in Microsoft Dynamics 365 Finance konzentriert, können einige der Konzepte und Überprüfungen auf andere Apps angewendet werden, wie z. B. Dynamics 365 Supply Chain Management.

Darüber hinaus kann sich die Umgebung, in der eine Buchung storniert wird, darauf auswirken, ob sie storniert werden kann. Beispielsweise kann eine als Scheck gebuchte Kreditorenzahlung nur vom Abschnitt **Schecks** auf der Buchungsseite für die Bankkonten aus storniert werden. Von der Seite **Belegbuchungen** im Hauptbuch aus kann sie nicht storniert werden.

Wenn die Funktion **Massenstornierung für mehrere Dokumente** (auch bekannt als Massenstornierungsfunktion) im Workspace **Funktionsverwaltung** aktiviert ist, beeinflusst sie, wie viele Buchungen storniert werden können und wo sie storniert werden können. Diese Funktion bietet zwei Vorteile, wenn sie aktiviert ist:

- Bei einigen Arten von Buchungen können mehrere Buchungen gleichzeitig ausgewählt und aus der Erfassung, aus der sie gebucht wurde oder von der Seite **Belegbuchungen** aus storniert werden. Die einzelnen Buchungen müssen jedoch vor dem Aktivieren der Funktion stornierbar gewesen sein. Bevor diese Funktion eingeführt wurde, mussten Buchungen einzeln storniert werden.
- *Manche* Buchungen in untergeordneten Sachkonten können aus der Erfassung (allgemeine Erfassung) oder der Seite **Belegbuchungen** aus storniert werden. Sie müssen nicht von der Seite des untergeordneten Sachkontos aus storniert werden. Beispielsweise konnte ein Kreditorenrechnungserfassung bisher nur von der Seite **Kreditorenbuchung** aus storniert werden. Es kann jetzt jedoch auch von der Hauptbuchseite, aus der Erfassung oder der Seite **Belegbuchungen** aus storniert werden. In jedem Abschnitt dieses Themas werden die Arten von Buchungen erläutert, für die dieser Vorteil nicht gilt.

Die Massenstornierungsfunktion ermöglicht **nicht** die Stornierung mehrerer Arten von Buchungen. Wenn ein Buchungstyp zuvor nicht storniert werden konnte, kann er auch nach dem Aktivieren der Funktion nicht storniert werden. Beispielsweise können Kreditorenrechnungen für Bestellungen nicht storniert werden, unabhängig davon, ob die Massenstornierungsfunktion aktiviert ist.

Weitere Informationen zur Massenstornierungsfunktion finden Sie unter [Buchungserfassung stornieren](reverse-journal-posting.md).

## <a name="general-ledger"></a>Hauptbuch

Hauptbuchregulierungen werden nur unter Verwendung von Sachkonten erfasst. Daher aktualisieren sie nur das Hauptbuch.

Wenn die Massenstornierungsfunktion deaktiviert ist, können die meisten Hauptbuchregulierungen einzeln von der Seite **Buchungen für \<main account\>** für das Sachkonto (**LedgerTransAccount**) durchgeführt werden. (Der genaue Titel der Seite variiert je nach ausgewähltem Hauptkonto.) Die Seite zeigt jede Buchung, die auf das Hauptkonto gebucht wurde. Es wird normalerweise von der Seite **Zwischenbilanzliste** oder über **Buchungen** auf der Seite **Belegbuchungen** geöffnet.

Wenn die Massenstornierungsfunktion aktiviert ist, können jetzt ein oder mehrere Hauptbuchbelege von der Seite **Belegbuchungen** und aus dem Journal, aus dem die Buchung gebucht wurde, storniert werden. Ausnahmen sind Neubewertungen der Fremdwährung im Hauptbuch, Konsolidierungen und Jahresabschlussbuchungen. Diese Buchungen werden von den Seiten, auf denen der Jahresabschluss ausgeführt wurde, storniert.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Warum Buchungen nicht storniert werden können

Buchungen können aus folgenden Gründen nicht storniert werden:

- Allgemeine Erfassung:

    - Der Finanzzeitraum ist gesperrt oder dauerhaft geschlossen:

        - Wenn das Stornierungsdatum in einem nicht offenen Finanzzeitraum liegt, kann die Buchung nicht storniert werden.
        - Wenn die Buchung die Eingabe eines Stornierungsdatums unterstützt, kann die Buchung trotzdem storniert werden, indem das Stornierungsdatum in einen offenen Zeitraum geändert wird.

    - Der Jahresabschlussprozess wurde ausgeführt:

        - Das Buchhaltungsdatum der Buchung liegt in einem Geschäftsjahr, das einen Jahresabschluss hinter sich hat. Obwohl ein Zeitraum im Geschäftsjahr möglicherweise noch offen ist, kann die Buchung nicht storniert werden, wenn der Jahresabschlussprozess für das Geschäftsjahr ausgeführt wurde. Das Geschäftsjahr hat einen anderen Status als die darin enthaltenen Zeiträume.
        - Der Jahresabschluss kann storniert werden, und dann kann die Buchung storniert werden. Dieser Ansatz ist möglicherweise keine Option. Je nach Status des Geschäftsjahresabschlussprozesses ist es möglicherweise einfacher, eine Stornierung manuell in einen offenen Zeitraum des abgeschlossenen Geschäftsjahrs oder des nächsten Geschäftsjahres einzugeben. Wenn eine neue Buchung in eine offene Periode des Geschäftsjahres gebucht wird, die den Jahresabschlussprozess durchlaufen hat, muss der Jahresabschluss erneut ausgeführt werden.

    - Die Buchungsstornierung ist bereits in Bearbeitung:

        - Wenn die Buchung gerade storniert wird, muss dieser Prozess abgeschlossen werden. Ein separater Stornierungsprozess ist nicht möglich. 
        - Nachdem die Stornierung abgeschlossen ist, kann eine stornierte Buchung wieder storniert werden (d. h. die Stornierung kann storniert werden).

    - Sachkontoausgleich:

        - Wenn eine oder mehrere Zeilen der Buchung unter Verwendung der periodischen Aufgabe **Sachkontoausgleich** (**Hauptbuch \> Periodische Aufgaben \> Sachkontoausgleich**) ausgeglichen wurden, damit der Datensatz LedgerTransSettlement in der Tabelle vorhanden ist, kann die Buchung nicht storniert werden.
        - Der Sachkontoausgleich kann storniert werden, und dann kann der Beleg storniert werden.

    - Intercompany:

        - Wenn es sich bei der Buchung um eine Intercompany-Buchung handelt, kann sie nicht storniert werden.
        - Die Buchung ist **keine** Intercompany-Buchung, wird aber auf ein „Fällig an“ oder „Fällig von“-Hauptkonto gebucht, das auf der Seite **Intercompany-Einstellungen** festgelegt wurde.

    - Abgrenzungen:

        - Wenn der abgegrenzte Hauptbuchbeleg storniert wird, werden die abgegrenzte Buchung und alle dazugehörigen Teilbuchung der Abgrenzung storniert.
        - Die einzelnen Teilbuchungen der Abgrenzung können nicht storniert werden.

- Umsatzerkennungserfassungen:

    - Umsatzerkennungsbuchungen können nicht storniert werden.
    - Wenn Umsätze über die Umsatzerkennungserfassung erfasst werden, wird der Beleg nur auf Sachkonten gebucht. Auf Seiten wie **Belegbuchungen** erscheinen die Buchungen daher so, als ob es sich nur um Hauptbucheinträge handelte.

- Neubewertung der Fremdwährung:

    - Neubewertungsbuchungen der Fremdwährungen können storniert werden, jedoch nur aus der Hauptbuchseite **Neubewertung der Fremdwährung**, von der aus die Neubewertung durchgeführt wurde.
    - Die Stornierung kann nur abgeschlossen werden, wenn sie in einen offenen Finanzzeitraum gebucht wurde.

- Konsolidierung:

    - Konsolidierungsbuchungen können storniert werden, jedoch nur von der Seite **Konsolidierungsbuchungen** aus.
    - Die Stornierung kann nur abgeschlossen werden, wenn sie in einen offenen Finanzzeitraum gebucht wurde.

- Jahresabschluss:

    - Jahresabschlussbuchungen (sowohl Abschluss- als auch Primobuchungen) können auf folgende Weise storniert werden:

        - Wenn die Funktion zur Erweiterung des Hauptbuchjahresabschlusses deaktiviert ist, wählen Sie die Option **Vorherigen Abschluss rückgängig machen** im Dialogfeld **Jahresabschluss** aus.
        - Wenn die Funktion für die Erweiterung des Hauptbuchjahresabschlusses aktiviert ist, wählen Sie die Unternehmens- und Geschäftsjahresdatensätze aus, die auf der Seite **Jahresabschluss** für den Jahresabschluss erstellt wurden und wählen Sie dann **Jahresschluss rückgängig machen**.

    - Beachten Sie, dass die Stornierung des Jahresabschlusses die Abschluss- und Primobuchungen tatsächlich löscht. Ein Stornierungsbeleg wird nie gebucht.

## <a name="accounts-payable"></a>Kreditorenkonten

Mehrere Buchungsarten aktualisieren das untergeordnete Kreditorenkontensachkonto. Beispiele sind Kreditorenrechnungen, Kreditorenrechnungserfassungen und Spesenabrechnungen.

Wenn die Massenstornierungsfunktion deaktiviert ist, können Buchungen einzeln von der Seite **Kreditorenbuchungen** oder von der Seite **Bankkonto** für Scheckzahlungen storniert werden.

Wenn die Massenstornierungsfunktion aktiviert ist, können jetzt ein oder mehrere Kreditorenkontobuchungen auch von der Seite **Belegbuchungen** und aus der Erfassung, aus der die Buchung gebucht wurde, storniert werden. Kreditorenzahlungen können jedoch weiterhin nur vom Bankkonto aus storniert werden. Darüber hinaus können Kreditorenbuchungen nicht von der Seite **Buchungen für \<main account\>** für das Hauptbuch storniert werden. Sie können nur von der Seite **Belegbuchungen** aus storniert werden.

Beachten Sie, dass einige Buchungen überhaupt nicht storniert werden können. Beispiele hierfür sind Kreditorenrechnungen für Bestellungen und elektronische Kreditorenzahlungen.

### <a name="reasons-why-vouchers-cant-be-reversed"></a>Warum Belege nicht storniert werden können

Belege können aus folgenden Gründen nicht storniert werden:

- Der Finanzzeitraum ist gesperrt oder geschlossen:

    - Wenn das Stornierungsdatum in einem nicht offenen Finanzzeitraum liegt, kann die Buchung nicht storniert werden.
    - Wenn die Buchung die Eingabe eines Stornierungsdatums unterstützt, kann die Buchung trotzdem storniert werden, indem das Stornierungsdatum in einen offenen Zeitraum geändert wird.

- Der Jahresabschlussprozess des Hauptbuchs wurde ausgeführt:

    - Das Buchhaltungsdatum der Buchung liegt in einem Geschäftsjahr, das im Hauptbuch abgeschlossen ist. Obwohl ein Zeitraum im Geschäftsjahr möglicherweise noch offen ist, kann die Buchung nicht storniert werden, wenn der Jahresabschlussprozess für das Geschäftsjahr ausgeführt wurde. Das Geschäftsjahr hat einen anderen Status als die darin enthaltenen Zeiträume.
    - Der Jahresabschluss kann storniert werden, und dann kann die Buchung storniert werden. Dieser Ansatz ist möglicherweise keine Option. Je nach Status des Geschäftsjahresabschlussprozesses ist es möglicherweise einfacher, eine Stornierung manuell in einen offenen Zeitraum des abgeschlossenen Geschäftsjahrs oder des nächsten Geschäftsjahres einzugeben. Wenn eine neue Buchung in eine offene Periode des Geschäftsjahres gebucht wird, die den Jahresabschlussprozess durchlaufen hat, muss der Jahresabschluss erneut ausgeführt werden.

- Die Erfassungseintrag in untergeordnetem Sachkonto wurde nicht in das Hauptbuch übertragen:

    - Dieser Grund gilt nur für Kreditorenrechnungen ohne Bestellung.
    - Verwenden Sie die Seite **Erfassungseinträge in untergeordnetem Sachkonto noch nicht übertragen**, um den Eintrag in das Hauptbuch zu übertragen. Die Kreditorenrechnung ohne Bestellung kann dann von der Seite **Kreditorenbuchungen** aus storniert werden.

- Ausgleich:

    - Die Buchung (z. B. eine Rechnung oder Zahlung) wird ausgeglichen oder zum Ausgleich vorgemerkt.

        - Sie können überprüfen, ob eine Buchung ausgeglichen oder zum Ausgleich vorgemerkt ist, indem Sie **Ausgleiche anzeigen** oder **Ausgleiche \> Ausgleichsverlauf** auf der Seite **Kreditorenbuchungen** auswählen.
        - Sie können einen Ausgleich auch aus der Seite **Kreditorenbuchungen** (**Ausgleich \> Ausgleich rückgängig machen**) stornieren, wenn eine der Buchungen storniert werden muss.

- Der Beleg enthält mehr als eine Buchungen eines untergeordneten Sachkontos, die unter Verwendung derselben Belegnummer eingegeben wurde (Ein-Beleg-Problem).
- Die Rechnung wurde nicht genehmigt:

    - Wenn das Kontrollkästchen **Genehmigung** auf der Rechnung nicht aktiviert ist, kann die Rechnung nicht storniert werden.

        - In diesem Fall bezieht sich die Genehmigung nicht auf Genehmigungen im Workflowprozess, sondern auf die Option **Genehmigung** auf der Rechnung. Diese Option wird verwendet, um zu verhindern, dass eine Rechnung bezahlt wird. Es wird normalerweise für Rechnungen des Kreditorenrechnungsbuch verwendet.

- Die Buchung befindet sich im Rechnungspool:

    - Eine Rechnung im Pool kann nicht direkt von der Seite **Kreditorenbuchungen** aus storniert werden. Stattdessen muss sie durch den Stornierungsprozess auf der Seite **Rechnungsgenehmigungserfassung** storniert werden.

- Zu der Buchung gibt es eine korrigierte übergeordnete Rechnung (indische Lokalisierung).
- Die Buchung hat einen Solawechselstatus von **Rechnung eingereicht**.
- Die Buchung wird für einen teilweisen Steuerausgleich verwendet.
- Die Buchung enthält ein Kreditorenkonto, wird jedoch von einer falschen Seite storniert, wie z. B. von der Seite **Buchungen für \<main account\>**:

    - Aus diesem Grund können einige Buchungen von untergeordneten Sachkonten nur von bestimmten Seiten aus storniert werden, selbst wenn die Massenstornierungsfunktion aktiviert ist.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Buchungstypen, die nicht storniert werden können

Die folgenden Buchungstypen können nicht storniert werden:

- Neubewertung der Fremdwährung:

    - Anders als Neubewertungen der Fremdwährung für das Hauptbuch können Neubewertungen der Fremdwährung für Kreditoren- und Debitorenkonten nicht storniert werden. Stattdessen muss die Neubewertung unter Verwendung des Rechnungsdatums erneut durchgeführt werden. In diesem Fall verwendet die Neubewertung den Wechselkurs vom Rechnungsdatum und bringt den nicht realisierten Gewinn oder Verlust im Wesentlichen auf 0 (Null). Daher ähnelt das Ergebnis dem Ergebnis der Stornierung der vorherigen Neubewertung. Beachten Sie jedoch, dass derselbe Betrag nicht storniert wird, wenn der Standardwechselkurs auf der Rechnung geändert wurde.

- Kreditorenrechnung mit Bestellung:

    - Zum Stornieren der Kreditorenrechnung muss eine Gutschrift erstellt werden. Weitere Informationen zum Anlegen einer Stornierungsbuchung finden Sie unter [Einkaufsrücklieferung erstellen](../../supply-chain/procurement/tasks/create-purchase-return-order.md).

- Solawechsel
- Exportlieferung mit Bankbürgschaft

## <a name="accounts-receivable"></a>Debitorenkonten

Verschiedene Buchungsarten aktualisieren das untergeordnete Kreditorenkontensachkonto. Beispiele sind Debitorenrechnungen aus Aufträgen, Debitorenrechnungen, die über die allgemeine Erfassung erfasst werden, Freitextrechnungen, Debitorenzahlungen und Abschreibungen.

Wenn die Massenstornierungsfunktion deaktiviert ist, können Buchungen einzeln von der Seite **Debitorenbuchungen** oder von der Seite **Bankkonten** für Einzahlungen storniert werden. Informationen zum Stornieren einer Zahlung finden Sie im Abschnitt [Bargeld- und Bankverwaltung](cant-reverse-transctns.md#cash-and-bank-management) weiter unten in diesem Thema.

Wenn die Massenstornierungsfunktion aktiviert ist, können jetzt ein oder mehrere Debitorenkontobuchungen auch von der Seite **Belegbuchungen** und aus der Erfassung, aus der sie gebucht wurde, storniert werden. Einzahlungen können jedoch weiterhin nur vom Bankkonto aus storniert werden, und Freitextrechnungen können nur von der ursprünglichen Seite storniert werden (wenn die Korrekturfunktion aktiviert ist). Darüber hinaus können Debitorenbuchungen immer noch nicht von der Seite **Buchungen für \<main account\>** für das Hauptbuch storniert werden. Sie können jedoch von der Seite **Belegbuchungen** aus storniert werden.

Beachten Sie, dass einige Buchungen nicht storniert werden können. Beispiele sind Debitorenrechnungen und Abschreibungen für Aufträge.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Warum Buchungen nicht storniert werden können

Buchungen können aus folgenden Gründen nicht storniert werden:

- Der Finanzzeitraum ist gesperrt oder dauerhaft geschlossen:

    - Wenn das Stornierungsdatum in einem nicht offenen Finanzzeitraum liegt, kann die Buchung nicht storniert werden.
    - Wenn die Buchung die Eingabe eines Stornierungsdatums unterstützt, kann die Buchung trotzdem storniert werden, indem das Stornierungsdatum in einen offenen Zeitraum geändert wird.

- Der Jahresabschlussprozess des Hauptbuchs wurde ausgeführt:

    - Das Buchhaltungsdatum der Buchung liegt in einem Geschäftsjahr, das einen Hauptbuchjahresabschluss hinter sich hat. Obwohl ein Zeitraum im Geschäftsjahr möglicherweise noch offen ist, kann die Buchung nicht storniert werden, wenn der Jahresabschlussprozess für das Geschäftsjahr ausgeführt wurde. Das Geschäftsjahr hat einen anderen Status als die darin enthaltenen Zeiträume.
    - Der Jahresabschluss kann storniert werden, und dann kann die Buchung storniert werden. Dieser Ansatz ist möglicherweise keine Option. Je nach Status des Geschäftsjahresabschlussprozesses ist es möglicherweise einfacher, eine Stornierung manuell in einen offenen Zeitraum des abgeschlossenen Geschäftsjahrs oder des nächsten Geschäftsjahres einzugeben. Wenn eine neue Buchung in eine offene Periode des Geschäftsjahres gebucht wird, die den Jahresabschlussprozess durchlaufen hat, muss der Jahresabschluss erneut ausgeführt werden.

- Die Erfassungseintrag in untergeordnetem Sachkonto wurde nicht in das Hauptbuch übertragen:

    - Dieser Grund gilt nur für Freitextrechnungen.
    - Verwenden Sie die Seite **Erfassungseinträge in untergeordnetem Sachkonto noch nicht übertragen**, um den Eintrag in das Hauptbuch zu übertragen. Die Freitextrechnung kann dann storniert oder korrigiert werden, wenn die Korrekturfunktion aktiviert ist.

- Ausgleich:

    - Die Buchung (z. B. eine Rechnung oder Zahlung) wird ausgeglichen oder zum Ausgleich vorgemerkt.

        - Sie können überprüfen, ob eine Buchung ausgeglichen oder zum Ausgleich vorgemerkt ist, indem Sie **Ausgleiche anzeigen** oder **Ausgleiche \> Ausgleichsverlauf** auf der Seite **Debitorenbuchungen** auswählen.
        - Sie können einen Ausgleich auch aus der Seite **Debitorenbuchungen** (**Ausgleich \> Ausgleich rückgängig machen**) stornieren, wenn eine der Buchungen storniert werden muss.

- Die Buchung enthält mehr als eine Buchungen eines untergeordneten Sachkontos, die unter Verwendung derselben Belegnummer eingegeben wurde (Ein-Beleg-Problem).
- Die Rechnung wurde nicht genehmigt:

    - Wenn das Kontrollkästchen **Genehmigung** auf der Rechnung nicht aktiviert ist, kann die Rechnung nicht storniert werden.

        - In diesem Fall bezieht sich die Genehmigung nicht auf Genehmigungen im Workflowprozess, sondern auf die Option **Genehmigung** auf den Buchungspositionen. Diese Option wird verwendet, um zu verhindern, dass eine Rechnung bezahlt wird. Obwohl diese Option normalerweise in Kreditorenkonten verwendet wird, ist sie auch für Debitorenrechnungen verfügbar, die über Erfassungen erfasst werden.

- Zu der Buchung gibt es eine korrigierte übergeordnete Rechnung (indische Lokalisierung).
- Die Buchung enthält ein Debitorenkonto, wird jedoch von einer falschen Seite storniert, wie z. B. von der Seite **Buchungen für \<main account\>**:

    - Aus diesem Grund können einige Buchungen von untergeordneten Sachkonten nur von bestimmten Seiten aus storniert werden, selbst wenn die Massenstornierungsfunktion aktiviert ist.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Buchungstypen, die nicht storniert werden können

Die folgenden Buchungstypen können nicht storniert werden:

- Neubewertung der Fremdwährung:

    - Anders als Neubewertungen der Fremdwährung für das Hauptbuch können Neubewertungen der Fremdwährung für Kreditoren- und Debitorenkonten nicht storniert werden. Stattdessen muss die Neubewertung unter Verwendung des Rechnungsdatums erneut durchgeführt werden. In diesem Fall verwendet die Neubewertung den Wechselkurs vom Rechnungsdatum und bringt den nicht realisierten Gewinn oder Verlust im Wesentlichen auf 0 (Null). Daher ähnelt das Ergebnis dem Ergebnis der Stornierung der vorherigen Neubewertung. Beachten Sie jedoch, dass derselbe Betrag nicht storniert wird, wenn der Standardwechselkurs auf der Rechnung geändert wurde.

- Eine Buchung, für die es eine angepasste Quellensteuer gibt
- Debitorenrechnung für Auftrag:

    - Zum Stornieren der Buchung muss eine Gutschrift oder eine Rücklieferung erstellt werden. Informationen zum Erstellen der Stornierungsbuchung finden Sie unter [Verkaufsreklamationen](../../supply-chain/warehousing/sales-returns.md).

- Wechsel
- Kassenbuchungen
- Erweiterte Regulierung
- Zinsrechnung
- Mahnschreiben
- Bankbürgschaften
- Exportlieferung
- Umsatzerkennungserfassungen:

    - Wenn Sie Umsätze über die Umsatzerkennungserfassung erfassen, werden die Belege auf Sachkonten gebucht. Daher erscheinen sie so, als seien es nur Hauptbucheinträge. Diese Einträge können nicht storniert werden, da der Umsatzzeitplan nicht erneut geöffnet wird, um den Umsatz erneut zu erfassen.

## <a name="cash-and-bank-management"></a>Bargeld- und Bankverwaltung

Mehrere Buchungstypen aktualisieren das untergeordnete Banksachkonto über das Hauptbuch. Beispiele sind Kreditorenzahlungen, Debitorenzahlungen und Banküberweisungen.

Wenn die Massenstornierungsfunktion deaktiviert ist, können Buchungen einzeln von der Seite **Bankkonten** für Schecks und Einzahlungen und von der Seite **Debitorenbuchungen** für Debitorenzahlungen storniert werden.

Wenn die Massenstornierungsfunktion aktiviert ist, können jetzt ein oder mehrere Zahlungsbuchungen auch von der Seite **Belegbuchungen** und aus der Erfassung, aus der die Buchung gebucht wurde, storniert werden. Einzahlungen können jedoch weiterhin nur vom Bankkonto aus storniert werden. Darüber hinaus können Bankbuchungen immer noch nicht von der Hauptbuchseite **Buchungen für \<main account\>** storniert werden. Sie können jedoch von der Seite **Belegbuchungen** aus storniert werden.

Beachten Sie, dass einige Buchungen nicht storniert werden können. Beispiele hierfür sind elektronische Kreditorenzahlungen.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Warum Buchungen nicht storniert werden können

Buchungen können aus folgenden Gründen nicht storniert werden:

- Der Finanzzeitraum ist gesperrt oder dauerhaft geschlossen:

    - Wenn das Stornierungsdatum in einem nicht offenen Finanzzeitraum liegt, kann die Buchung nicht storniert werden.
    - Wenn die Buchung die Eingabe eines Stornierungsdatums unterstützt, kann die Buchung trotzdem storniert werden, indem das Stornierungsdatum in einen offenen Zeitraum geändert wird.

- Der Jahresabschlussprozess des Hauptbuchs wurde ausgeführt:

    - Das Buchhaltungsdatum der Buchung liegt in einem Geschäftsjahr, das einen Hauptbuchjahresabschluss hinter sich hat. Obwohl ein Zeitraum im Geschäftsjahr möglicherweise noch offen ist, kann die Buchung nicht storniert werden, wenn der Jahresabschlussprozess für das Geschäftsjahr ausgeführt wurde. Das Geschäftsjahr hat einen anderen Status als die darin enthaltenen Zeiträume.
    - Der Jahresabschluss kann storniert werden, und dann kann die Buchung storniert werden. Dieser Ansatz ist möglicherweise keine Option. Je nach Status des Geschäftsjahresabschlussprozesses ist es möglicherweise einfacher, eine Stornierung manuell in einen offenen Zeitraum des abgeschlossenen Geschäftsjahrs oder des nächsten Geschäftsjahres einzugeben. Wenn eine neue Buchung in eine offene Periode des Geschäftsjahres gebucht wird, die den Jahresabschlussprozess durchlaufen hat, muss der Jahresabschluss erneut ausgeführt werden.

- Ausgleich:

    - Die Buchung (Zahlung) wird ausgeglichen oder zum Ausgleich vorgemerkt.

        - Sie können überprüfen, ob eine Buchung ausgeglichen oder zum Ausgleich vorgemerkt ist, indem Sie **Ausgleiche anzeigen** oder **Ausgleiche \> Ausgleichsverlauf** auf der Seite **Kreditorenbuchungen** oder **Debitorenbuchungen** auswählen.
        - Sie können einen Ausgleich auch aus der Seite **Kreditorenbuchungen** oder **Debitorenbuchungen** (**Ausgleich \> Ausgleich rückgängig machen**) stornieren, wenn eine der Buchungen storniert werden muss.

- Die Buchung enthält mehr als eine Buchungen eines untergeordneten Sachkontos, die unter Verwendung derselben Belegnummer eingegeben wurde (Ein-Beleg-Problem).
- Transferbuchungen:

    - Wenn die Buchung mit einer Transferzahlung zusammenhängt, kann sie nicht storniert werden.
    - Muss die Transferzahlung storniert werden, so muss die Zahlung zunächst vom Transferkonto an die Bank verrechnet werden. Die Zahlung kann dann storniert werden, sofern sie die anderen Überprüfungskriterien erfüllt.

- Die Buchung enthält ein Bankkonto, wird aber von der Seite **Buchungen für \<main account\>** oder aus einem falschen untergeordneten Sachkonto storniert, wie Debitoren- oder Kreditorenkonten:

    - Aus diesem Grund können einige Buchungen von untergeordneten Sachkonten nur von bestimmten Seiten aus storniert werden, selbst wenn die Massenstornierungsfunktion aktiviert ist.

- Neubewertung der Fremdwährung – Bank:

    - Die Bankneubewertung der Fremdwährung kann storniert werden. Die Stornierung kann jedoch verhindert werden, wenn Sie die Stornierungsschritte nicht in der chronologischen Reihenfolge ausführen. Wenn Sie die Neubewertung beispielsweise im März und April durchgeführt haben, kann die Neubewertung vom März nicht storniert werden, bis die Neubewertung vom April rückgängig gemacht wird.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Buchungstypen, die nicht storniert werden können

Die folgenden Buchungstypen können nicht storniert werden:

- Kreditorenzahlungen, die als elektronische Überweisungen (EFTs) getätigt wurden
- Solawechsel
- Wechsel

## <a name="fixed-assets"></a>Anlagevermögen

Mehrere Buchungstypen aktualisieren das untergeordnete Anlagensachkonto. Beispiele sind Anschaffungen und Abschreibungen.

Wenn die Massenstornierungsfunktion deaktiviert ist, können Buchungen, je nach Buchungstyp, einzeln von der Seite **Kreditorenbuchungen**, von der Seite **Anlagenbuchungen** oder aus dem Anlagenleasing storniert werden.

Wenn die Massenstornierungsfunktion aktiviert ist, können jetzt ein oder mehrere Anlagenbuchungen auch von der Seite **Belegbuchungen** in der Erfassung, aus der die Buchung gebucht wurde, storniert werden.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Warum Buchungen nicht storniert werden können

Buchungen können aus folgenden Gründen nicht storniert werden:

- Der Finanzzeitraum ist gesperrt oder dauerhaft geschlossen:

    - Wenn das Stornierungsdatum in einem nicht offenen Finanzzeitraum liegt, kann die Buchung nicht storniert werden.
    - Wenn die Buchung die Eingabe eines Stornierungsdatums unterstützt, kann die Buchung trotzdem storniert werden, indem das Stornierungsdatum in einen offenen Zeitraum geändert wird.

- Der Jahresabschlussprozess des Hauptbuchs wurde ausgeführt:

    - Das Buchhaltungsdatum der Buchung liegt in einem Geschäftsjahr, das im Hauptbuch abgeschlossen ist. Obwohl ein Zeitraum im Geschäftsjahr möglicherweise noch offen ist, kann die Buchung nicht storniert werden, wenn der Jahresabschlussprozess für das Geschäftsjahr ausgeführt wurde. Das Geschäftsjahr hat einen anderen Status als die darin enthaltenen Zeiträume.
    - Der Jahresabschluss kann storniert werden, und dann kann die Buchung storniert werden. Dieser Ansatz ist möglicherweise keine Option. Je nach Status des Geschäftsjahresabschlussprozesses ist es möglicherweise einfacher, eine Stornierung manuell in einen offenen Zeitraum des abgeschlossenen Geschäftsjahrs oder des nächsten Geschäftsjahres einzugeben. Wenn eine neue Buchung in eine offene Periode des Geschäftsjahres gebucht wird, die den Jahresabschlussprozess durchlaufen hat, muss der Jahresabschluss erneut ausgeführt werden.

- Anschaffungen:

    - Wenn die Anschaffung auf einer Kreditorenrechnung einer Bestellung erfolgt ist, muss die Stornierung durch Eingabe einer Kreditorengutschrift erfolgen. Weitere Informationen zur Eingabe von Stornierungsbuchungen finden Sie unter [Einkaufsrücklieferung erstellen](../../supply-chain/procurement/tasks/create-purchase-return-order.md).
    - Die Anschaffung erfolgte im Rahmen einer Projektbuchung.
    - Die Anschaffung kann nicht storniert werden, nachdem die Abschreibung für die Anlage gebucht wurde. Die Abschreibung muss rückgängig gemacht werden, bevor die Anschaffung rückgängig gemacht werden kann.
    - Wenn der Status des Wertmodells oder des Abschreibungsbuchs für eine Anlage nicht offen ist, kann die Buchung nicht storniert werden.

- Abgänge:

    - Der Abgang erfolgt über eine Freitextrechnung:

        - Die Korrektur einer Freitextrechnung ist gesperrt, wenn sie eine Anlage enthält. Wenn die Anlage jedoch über eine Erfassung abgegeben wird, kann die Freitextrechnung aus dem Anlagendatensatz storniert werden.

    - Wenn der Status des Wertmodells oder des Abschreibungsbuchs für eine Anlage nicht offen ist, kann die Buchung nicht storniert werden.

- Abschreibung:

    - Die Abschreibung **kann** storniert werden, wenn auch nachträgliche Abschreibungen gebucht werden. Sie erhalten jedoch eine Warnung, da dieser Ansatz keine bewährte Methode ist.
    - Wenn der Status des Wertmodells oder des Abschreibungsbuchs für eine Anlage nicht offen ist, kann die Buchung nicht storniert werden.

- Buchungen (oder Stornierungsbuchungen) für eine bestimmte Anlage und ein Anlagebuch existieren ab dem Buchungsdatum des Belegs oder später.
- Die Buchung enthält eine Anlage, wird aber von der Seite **Buchungen für \<main account\>** oder aus einem falschen untergeordneten Sachkonto storniert, wie Debitoren- oder Kreditorenkonten:

    - Aus diesem Grund können einige Buchungen von untergeordneten Sachkonten nur von bestimmten Seiten aus storniert werden, selbst wenn die Massenstornierungsfunktion aktiviert ist.
    - Erfolgt eine Anschaffung auf einer Kreditorenrechnung ohne Bestellung oder einer Kreditorenrechnungserfassung, kann sie nur von der Seite **Kreditoenbuchungen** in den Kreditorenkonten storniert werden.
    - Wenn eine Anlage aus einem Anlagenleasing angeschafft wird, kann dieser von der Seite **Verbindlichkeitsbuchungen** im Anlagenleasing storniert werden.
