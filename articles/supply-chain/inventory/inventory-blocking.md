---
title: Sperrung von Lagerbestand
description: Dieses Thema gibt einen Überblick über die Sperrung von Lagerbestand, die Teil des Qualitätsprüfungsprozesses in Supply Chain Management ist. Sie können die Sperrung von Lagerbestand verwenden, um die Verarbeitung oder den Verbrauch von Artikeln zu verhindern.
author: perlynne
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d07313050b59a32756fa5e31037f1831a2cbe862
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829883"
---
# <a name="inventory-blocking"></a>Sperrung von Lagerbestand

[!include [banner](../includes/banner.md)]

Dieses Thema gibt einen Überblick über die Sperrung von Lagerbestand, die Teil des Qualitätsprüfungsprozesses in Supply Chain Management ist. Sie können die Sperrung von Lagerbestand verwenden, um die Verarbeitung oder den Verbrauch von Artikeln zu verhindern.

Sie können Lagerartikel auf die folgenden Arten sperren:

- Manuell
- Per Erstellung eines Qualitätsprüfungsauftrags
- Per Nutzung eines Vorgangs, bei dem ein Qualitätsprüfungsauftrag generiert wird
- Mithilfe der Lagerstatussperrung

## <a name="blocking-items-manually"></a>Manuelle Sperrung von Artikeln

Sie können eine bestimmte Menge eines Artikels sperren, indem Sie auf der Seite **Sperrung von Lagerbestand** eine Transaktion erstellen. Es können nur Artikel manuell gesperrt werden, die als verfügbarer Lagerbestand vorhanden sind. Bei manuell gesperrten Mengen müssen Sie entscheiden, ob Planungsaktivitäten erwartete Zugänge als eine zu erwartende verfügbare Menge einbeziehen. Bei erwarteten Zugängen handelt es sich um gesperrte Artikel, von denen Sie erwarten, dass sie nach Abschluss der Prüfung als verfügbarer Lagerbestand vorhanden sind. Sie können das erwartete Datum beibehalten. Standardmäßig ist die Option **Erwartete Zugänge** für Artikel ausgewählt, die durch eine Testbestellung gesperrt sind. Sie können eine manuelle Sperre für eine Menge stornieren, indem Sie die Transaktion auf der Seite **Sperrung von Lagerbestand** löschen.

## <a name="blocking-items-by-creating-a-quality-order"></a>Sperren von Artikeln per Erstellung einer Testbestellung

Sie können Artikel angeben, die überprüft werden müssen, indem Sie eine Testbestellung auf der Seite **Testbestellungen** erstellen. Wenn Sie eine Testbestellung erstellen, wird die Menge, die Sie für einen Artikel angeben, gesperrt. Der Musteraufnahmeplan, der einer Testbestellung zugeordnet ist, steuert nur die Menge der Artikel, die überprüft werden müssen, nicht die Menge, die gesperrt wird. Die Menge, die in der Testbestellung eingegeben wird, ist die Menge, die gesperrt wird, ungeachtet der Menge, die gemäß der Angaben des Musteraufnahmeplans zur Prüfung eingereicht werden sollte.

> [!NOTE]
> Die Verwendung sowohl des Chargenablaufdatums als auch der Funktionen zum Sperren des Bestandsstatus wird von der Masterplanung nicht unterstützt. Dies kann zu einem doppelten Ausschluss des Lagerbestands führen, der während der Masterplanung auftreten kann. Wir empfehlen, dass Sie sich beim Sperren abgelaufener Chargen anstelle des Inventarstatus auf Chargenverfügungscodes verlassen.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Sperrung von Artikeln mithilfe eines Prozesses, bei dem eine Testbestellung generiert wird

Wenn ein Qualitätsprozess angibt, dass ein Artikel überprüft werden muss, wird eine Menge des Artikels automatisch gesperrt. Wenn also ein Qualitätsauftrag automatisch erzeugt wird, steuert der Stichprobenplan für Artikel, der mit dem Qualitätsauftrag verknüpft ist, sowohl die Menge der gesperrten Artikel als auch die Menge, die geprüft werden muss. Wenn die Option **Vollständige Sperrung** auf der Seite **Artikelmusteraufnahme** ausgewählt ist, wird die gesamte Menge beispielsweise einer Bestellposition während der Überprüfung gesperrt, unabhängig von der Menge der Artikelmusteraufnahme.

### <a name="example"></a>Beispiel

Im folgenden Beispiel wird ein Qualitätsprüfungsauftrag generiert, wenn ein Lieferschein für eine Bestellung gebucht wird. Auf der Seite **Qualitätszuordnungen** haben Sie angegeben, dass das Buchen eines Lieferscheins für eine Bestellung der Prozess ist, der eine Testbestellung aktiviert.

|Einrichten |Benutzeraktivität |Ergebnis |
|----|---|---|
| Eine Qualitätszuordnung gibt an, dass beim Buchen eines Lieferscheins für eine Bestellung eine Testbestellung generiert werden muss. In den Einstellungen für die Artikelmusteraufnahme der Testbestellung ist angegeben, dass 10 Prozent der Menge der Bestellposition geprüft werden müssen. Weil darüber hinaus die Option **Vollständige Sperrung** bei den Einstellungen für die Artikelmusteraufnahme ausgewählt ist, muss die gesamte Menge der Bestellposition während der Prüfung unabhängig von der zur Prüfung eingereichten Menge gesperrt werden. | Der Lieferschein wird gebucht. | Ein Qualitätsprüfungsauftrag wird generiert. Zehn Prozent der Bestellmenge für den Artikel wird Prüfung eingereicht. Die Gesamtmenge der Bestellposition wird gesperrt. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Sperrung von Artikeln mithilfe der Lagerstatussperrung

Sie können angeben, welche Lagerstatus Sperrenstatus sind, indem Sie den Parameter **Sperrung von Lagerbestand** auf der Seite **Lagerstatus** verwenden.  Sie können Lagerstatus nicht als Sperrenstatus für Produktionsaufträge, Aufträge, Umlagerungsaufträge, ausgehende Transaktionen oder Projektintegrationen verwenden. Für ausgehende Arbeit verwenden Sie Artikel, die den Bestandsstatus "verfügbar" aufweisen. Wenn Artikel den Status **Kaputt** haben und der Produktprogrammplan für diese Artikel ausgeführt wird, werden die Artikel als fehlend betrachtet und der Bestand wird automatisch aufgefüllt.

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>Seien Sie vorsichtig, wenn Sie Artikel sperren, die sowohl die Sperrung des Bestands als auch die Sperrung des Qualitätsauftrags verwenden

Sie können einen Qualitätsauftrag erstellen, der mit einem Bestand verbunden ist, der einen Bestandsstatus hat, bei dem der Parameter **Bestandsblockierung** aktiviert ist. In diesem Fall erzeugt der Qualitätsauftrag einen zusätzlichen Datensatz für die Bestandssperre, zusätzlich zu dem, der durch den Bestandsstatus erstellt wird. Da für den Qualitätsauftrag Bestandsblockierung der Parameter **Erwartete Eingänge** aktiviert ist, erzeugt dies eine zusätzliche Transaktion *Bestellter Bestand*, die ebenfalls durch den Bestandsstatus blockiert ist. Diese Kombination kann zu Schwierigkeiten beim Verständnis der Bedeutung der generierten Bestandstransaktionen führen, weil es so aussieht, als ob die gesperrte Gesamtmenge die Gesamtmenge im Lagerbestand übersteigt. Untersuchen wir die Transaktionen am Beispiel eines Eingangs von 10 Stück des Artikels A0001 mit einem generierten Qualitätsauftrag zur Entnahme von 1 Stück. Das Verhalten hängt auch davon ab, ob die Option **Bestellte Artikel reservieren** auf der Seite **Parameter der Bestands- und Lagerortverwaltung** aktiviert ist.

>[!NOTE]
>Wenn Sie Bestandssperre und Qualitätsaufträge zusammen verwenden, empfehlen wir dringend, die Option **Bestellte Artikel reservieren** aktiviert zu haben.

### <a name="example-with-reserve-ordered-items-enabled"></a>Beispiel mit „Bestellte Artikel reservieren“ aktiviert

Wenn **Bestellte Artikel reservieren** aktiviert ist, haben alle Transaktionen zur Bestandssperrung entweder den Status *Reserviert physisch* oder *Reserviert bestellt*.

| Referenz der Bestandstransaktion | Zugang | Abgang | Leistung | Standort | Lagerort | Bestandsstatus | Ziel | Ladungsträger | Kommentar |
|---|---|---|---|---|---|---|---|---|---|
| Bestellung | Eingekauft | | 10 Pcs | 2 | 24 | Sperrung | RECV | receiptLp1 | | 
| Sperrung von Lagerbestand | | Physisch reserviert | -9 Pcs | 2 | 24 | Sperrung | | | Transaktion, die durch die Bestandssperrung erzeugt wird |
| Sperrung von Lagerbestand | | Physisch reserviert | -1 Pcs | 2 | 24 | Sperrung | RECV | receiptLp1 | Transaktion, die durch die Qualitätsauftragsstichproben-Sperrung erzeugt wird |
| Sperrung von Lagerbestand | Bestellt | | 1 Pcs | 2 | 24 | Sperrung | RECV | receiptLp1 | Erwartete Eingänge aus der Qualitätsauftragsstichproben-Sperrung |
| Sperrung von Lagerbestand | | Bestellt reserviert | 1 Pcs | 2 | 24 | Sperrung | | | Transaktion, die durch die Bestandssperrung erzeugt wird

### <a name="example-with-reserve-ordered-items-disabled"></a>Beispiel mit „Reservierte bestellte Artikel“ deaktiviert

Wenn **Bestellte Artikel reservieren** deaktiviert ist, können die erwarteten Eingänge nicht reserviert werden, da sie sich im Status *Bestellt* befinden, so dass einige Sperren im Status *Auf Bestellung* verbleiben.

| Referenz für Bestandstransaktionen | Zugang | Abgang | Leistung | Standort | Lagerort | Bestand Status | Ziel | Ladungsträger | Kommentar |
|---|---|---|---|---|---|---|---|---|---|
| Bestellung | Eingekauft | | 10 Pcs | 2 | 24 | Sperrung | RECV | receiptLp1 | |
| Sperrung von Lagerbestand | | Physisch reserviert | -9 Pcs | 2 | 24 | Sperrung | | | Transaktion, die durch die Bestandssperrung erzeugt wird |
| Sperrung von Lagerbestand | | Physisch reserviert | -1 Pcs | 2 | 24 | Sperrung | RECV | receiptLp1 | Transaktion, die durch die Qualitätsauftragsstichproben-Sperrung erzeugt wird |
| Sperrung von Lagerbestand | Bestellt | | 1 Pcs | 2 | 24 | Sperrung | RECV | receiptLp1 | Erwartete Eingänge aus der Qualitätsauftragsstichproben-Sperrung |
| Sperrung von Lagerbestand | | In Auftrag | 1 Pcs | 2 | 24 | Sperrung | RECV | receiptLp1 | Transaktion, die durch die Bestandssperrung erzeugt wird

Beachten Sie den Unterschied im Transaktionsstatus und in den Dimensionen zwischen den beiden Fällen. Aus diesem Grund empfehlen wir, die Option **Bestellte Artikel reservieren** zu aktivieren.

<!-- KFM: (Enable this section when the feature leaves private preview)

### Disable expected receipts from quality orders that sample blocked inventory feature

To simplify the inventory transactions in the case of quality orders that sample inventory blocked as a consequence of inventory status, the system provides a feature that disables expected receipts from such quality orders. As the expected receipt is in any case immediately blocked by inventory status blocking, there is no reduction of on-hand inventory because of this change.

-->

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Erstellen und Verwalten einer Sperrung von Lagerbestand](tasks/create-maintain-inventory-blocking.md)

[Qualitätsmanagementprozesse](quality-management-processes.md)

[Überprüfen Sie die Qualität von Waren](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]