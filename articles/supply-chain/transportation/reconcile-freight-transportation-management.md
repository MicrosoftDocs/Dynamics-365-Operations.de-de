---
title: Fracht in der Transportverwaltung abstimmen
description: Dieser Artikel beschreibt den Frachtabstimmungsprozess.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff29de62de12e8ca8bea0f374921a51b5819222e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844222"
---
# <a name="reconcile-freight-in-transportation-management"></a>Fracht in der Transportverwaltung abstimmen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt den Frachtabstimmungsprozess.

Die Frachtabstimmung kann manuell oder automatischen durchgeführt werden. Um die automatische Frachtabstimmung zu verwenden, müssen Sie einen Überwachungsmaster einrichten. In ihm können Sie die Kriterien definieren, die festlegen, welche Fracht automatisch abgestimmt wird.

## <a name="the-freight-reconciliation-process"></a>Der Frachtabstimmungsprozess

Frachtkosten werden vom den Tarifmodul berechnet, das dem relevanten Spediteur zugeordnet ist. Wenn ein Ladung bestätigt ist, wird ein Frachtbrief erstellt und die Frachtkosten werden an diesen übertragen. Die Frachtkosten werden je nach Konfiguration für den regulären Abrechnungsprozess als sonstige Zuschläge auf das entsprechende Quelldokument umgelegt (Bestellung, Auftrag und/oder Umlagerungsauftrag). Der Frachtabstimmungsprozesse (auch Abgleichsprozess genannt) kann starten sobald die Frachtrechnung vom Spediteur eingeht. Die Rechnung elektronisch oder auf Papier erhalten werden. Wenn die Rechnung auf Papier erhalten wird, können Sie mit dem Frachtbrief als Vorlage eine elektronische Rechnung generieren.

[![Frachtabstimmungsprozess.](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Manuelle Abstimmung

Wenn Sie die Fracht manuell abstimmen, müssen Sie jede Rechnungsposition mit der Frachtbriefposition oder den-positionen für die zu fakturierende Ladung abgleichen. Diesen Abgleich führen Sie auf der Seite **Frachtbrief- und Rechnungsabgleich** durch. Wenn der Betrag der Rechnungsposition nicht mit dem Frachtbriefbetrag übereinstimmt, müssen Sie einen Abstimmungsgrund für die Abweichung auswählen. Sind mehrere Gründe für die Abstimmung zutreffen, können Sie die nicht abgeglichenen Mengen auf diese Gründe verteilen. Der Abstimmungsgrund bestimmt, wie die Differenzbeträge im Hauptbuch gebucht werden. Bei die Abstimmung des gesamten Rechnungsbetrags gebucht wird, wird dieser zur Genehmigung gesendet. Dann wird die Erfassung gebucht. Die folgende Abbildung zeigt, wie eine Frachtrechnung generiert und eine Frachtabstimmung ausgeführt wird.

[![Frachtabstimmungsaufgaben.](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)

## <a name="automatic-reconciliation"></a>Automatische Abstimmung

Um die automatische Abstimmung zu verwenden, müssen Sie den Zeitplan für die Abstimmung und die zu verwendenden Rechnungen und Spediteure angeben. Der Abgleich der Rechnungspositionen und Frachtbriefe wird entsprechend der Einrichtung des Überwachungsmasters und der Frachtbriefart ausgeführt. Nach dem Ausführen der automatischen Abstimmung müssen Sie alle Rechnungen bearbeiten, die das System nicht zuordnen kann. Sie müssen diese Rechnungen dann manuell verarbeiten, bevor Sie alle Rechnung für die Zahlung buchen können.

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a>Abgleichen von Frachtbriefen mit Frachtrechnungen mithilfe einer automatischen oder manuellen Abstimmung

*Abgleichen* ist der Prozess des Findens der Frachbriefe, die jeder Frachtrechnung entsprechen. Dies kann durch Abgleichen der einzelnen Rechnungspositionen (manuelles Abgleichen) oder durch gleichzeitiges Abgleichen aller verfügbaren Rechnungen (automatisches Abgleichen) erfolgen.

### <a name="auto-matching"></a>Automatisches Abgleichen

Wenn mehrere Frachtrechnungen mit demselben Frachtbrief abgeglichen werden, funktioniert der automatische Abgleich wie folgt:

1. Alle nicht abgeglichenen Frachtrechnungen werden nach Betrag sortiert, wobei der größte Betrag zuerst angezeigt wird.
1. Die Frachtrechnungen werden nacheinander abgeglichen, bis auf dem Frachtbrief kein positiver Betrag mehr vorhanden ist.
1. Abhängig von der Einrichtung des Überwachungsmasters und dem Restbetrag auf den Frachtrechnungen wird der Restbetrag festgelegt.

### <a name="manual-matching"></a>Manuelle Zuordnung

Alle Frachtbriefe mit positiven Beträgen stehen zum Abgleich zur Verfügung. Ähnlich wie beim automatischen Abgleich kann der Benutzer nur Frachtrechnungen mit negativen Beträgen mit Frachtbriefen abgleichen, die nicht vollständig abgeglichen wurden.

### <a name="example"></a>Beispiel

Angenommen, Ihnen liegt ein Frachtbrief (FB) über einen Betrag von 1.500 vor und Sie haben für den Frachtbrief drei Frachtrechnungen erstellt mit einer Rechnungsposition für jede Rechnung und mit folgenden Einstellungen:

- Ursprünglicher Frachtbrief (FB): Betrag 1.500
- Rechnung 1 (Inv1): Betrag 1.000
- Rechnung 2 (Inv2): Betrag 600
- Rechnung 3 (Inv3): Betrag –100

#### <a name="automatic-matching-result"></a>Ergebnis des automatischen Abgleichs

Der automatische Abgleich wird in der folgenden Reihenfolge ausgeführt:

1. Alle Frachtrechnungen absteigend nach Betrag sortieren: Inv1 -> Inv2 -> Inv3.
1. Gleichen Sie Inv1 mit FB ab. Für Inv1 wird ein Betrag von 1.000 abgeglichen und auf dem FB verbleibt ein Betrag von 500. Der Status wird daher auf *Teilweise abgeglichen* gesetzt.
1. Gleichen Sie Inv2 mit FB ab. Für Inv2 wird ein Betrag von 500 abgeglichen und auf dem FB verbleibt ein Betrag von 0. Der Status wird daher auf *Vollständig abgeglichen* gesetzt.
1. Da der FB jetzt vollständig abgeglichen wurde, wird Inv3 nicht verarbeitet.

#### <a name="manual-matching-result"></a>Ergebnis des manuellen Abgleichs

Beim manuellen Abgleich variieren die Ergebnisse in Abhängigkeit von der Reihenfolge des Abgleichs, wie in den folgenden Beispielfällen dargestellt.

##### <a name="manual-matching-case-1"></a>Manueller Abgleich Fall 1

Eine Möglichkeit zum manuellen Abgleich für dieses Beispiel besteht darin, wie folgt vorzugehen:

1. Gleichen Sie den FB mit Inv1 ab. Auf dem FB verbleibt ein Betrag von 500, sodass der Status auf *Teilweise abgeglichen* gesetzt wird.
1. Gleichen Sie Inv2 mit FB ab. Für Inv2 wird ein Betrag von 500 abgeglichen und auf dem FB verbleibt ein Betrag von 0. Der Status wird daher auf *Vollständig abgeglichen* gesetzt.
1. Wenn Sie Inv3 manuell abgleichen, werden Sie keine nicht nicht abgeglichenen Frachtbriefe finden.

Dieser Fall entspricht im Wesentlichen dem automatischen Abgleich.

##### <a name="manual-matching-case-2"></a>Manueller Abgleich Fall 2

Eine weitere Möglichkeit zum manuellen Abgleich für dieses Beispiel besteht darin, wie folgt vorzugehen:

1. Gleichen Sie Inv3 mit dem FB ab. Jetzt verbleibt auf dem FB ein Betrag von 1.600, was der Subtraktion von –100 von 1.500 entspricht. Sowohl der FB als auch Inv3 haben eine abgeglichene Menge von –100.
1. Gleichen Sie Inv1 und Inv 2 nacheinander mit FB ab. Der FB ist vollständig abgeglichen.

Wie dieses Beispiel zeigt, sollte der Abgleich von Frachtrechnungen mit negativen Beträgen nur manuell erfolgen. Dadurch wird sichergestellt, dass es immer möglich ist, die Frachtrechnungen mit negativen Beträgen mit einem nicht vollständig abgeglichenen Frachtbrief abzugleichen, da Sie so die Reihenfolge des Abgleichs steuern können.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]