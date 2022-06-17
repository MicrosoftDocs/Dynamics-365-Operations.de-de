---
title: Umsatzerkennung bei Aufträgen
description: In diesem Artikel werden die grundlegenden Funktionen für die Erkennung von Umsatzerlösen für Aufträge und Rechnungen beschrieben. Umsatzerkennung ist für den Auftrag und für die entsprechende Rechnung verfügbar, die aus dem Auftrag erstellt wird.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 5df7341160940f5c5db0dd4c5d86e4d9698d22e2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899956"
---
# <a name="revenue-recognition-on-sales-orders"></a>Umsatzerkennung bei Aufträgen

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Die Funktion zur Umsatzerkennung kann nicht mithilfe der Funktionsverwaltung aktiviert werden. Derzeit erfolgt die Aktivierung mit Konfigurationsschlüsseln.

In diesem Artikel werden die grundlegenden Funktionen für die Erkennung von Umsatzerlösen für Aufträge und Rechnungen beschrieben. Umsatzerkennung ist für den Auftrag und für die entsprechende Rechnung verfügbar, die aus dem Auftrag erstellt wird. Der Auftrag kann auch in einem Aufwandsprojekt erstellt werden.

> [!NOTE]
> In den Abbildungen dieses Artikels sind Spalten ausgeblendet oder wurden Rastern hinzugefügt, um die Konzepte hervorzuheben. Daher können sich die Seiten und Daten in den Abbildungen von der Anzeige im Produkt unterscheiden.

## <a name="enter-a-sales-order"></a>Eingeben eines Auftrags

Es wird der folgende Auftrag mit drei Artikeln eingegeben, für die Umsatzerlöserkennung eingerichtet wird.

[![Eingeben eines Auftrags.](./media/revenue-recognition-so-basic-sales-order-header.png)](./media/revenue-recognition-so-basic-sales-order-header.png)

Es gibt zwei grundlegende Konzepte zur Umsatzerlöserkennung:

- **Feststellen des Umsatzerlöspreises.** Der Umsatzerlöspreis wird anhand der Einstellung „Freigegebene Produkte“ berechnet. Dem Debitoren wird der Umsatzerlöspreis niemals angezeigt, er wird nur für die Buchhaltung der Auftragsrechnung verwendet. Die Auftragspositionen und Dokumente, die im Zuge des Verkaufs gedruckt werden, zeigen weiterhin den Listenpreis/Einheitenpreis.
- **Legen Sie fest, wann die Umsatzerkennung stattfinden soll.** Ein Umsatzerlöszeitplan wird verwendet, um festzustellen, wann Umsatz erfasst werden soll.

    In diesem Beispiel wird der erste Artikel, S0001, einem Umsatzerlöszeitplan **1O** (einzelnes Vorkommen) zugewiesen. Diese Position stellt ein Szenario vom Typ „Meilenstein“ dar, in dem der Umsatzerlös erfasst wird, sobald die Installation in der Zukunft ausgeführt wird. Daher wird Umsatzerlös verzögert, bis die Installation abgeschlossen ist.

    Der zweite Artikel, S0008, ist ein Serviceelement, das als „Unterstützung nach Vertragsabschluss“-Artikel (PCS) eingerichtet wird. Die fortwährenden Engineeringservices werden dem Debitoren über einen Zeitraum von 12 Monaten bereitgestellt. Folglich wird dem Produkt standardmäßig ein **12M**-Umsatzerlöszeitplan zugewiesen. Da es sich um einen PCS-Artikel handelt, muss das Vertragsstart- und -enddatum definiert werden. Standardmäßig wird das Vertragsstart- und -enddatum auf der Registerkarte „Artikeldetails – Einstellungen“ angezeigt. Im Umsatzerlöszeitplan ist die Einstellung für **12M** definiert, sodass die Vertragsbedingungen automatisch wie in der folgenden Abbildung dargestellt ausgefüllt werden.

    [![Umsatzerlöszeitpläne.](./media/revenue-recognition-so-basic-revenue-schedules.png)](./media/revenue-recognition-so-basic-revenue-schedules.png)

    Der dritte Artikel, S0012, ist Hardware und standardmäßig ist kein Umsatzerlöszeitplan zugeordnet. Der Umsatzerlös für die Hardware wird erkannt, sobald der Artikel fakturiert wird.

## <a name="confirm-the-sales-order"></a>Auftrag bestätigen

Wenn Sie zusätzliche Details zum Umsatzerlöspreis und zum Umsatzerlöszeitplan anzeigen möchten, verwenden Sie die Schaltflächen in der Gruppe **Umsatzerkennung** auf der Registerkarte **Verwalten** im Aktionsbereich des Auftrags. Da der Auftrag zu diesem Zeitpunkt noch nicht bestätigt wurde, sind die Schaltflächen für die Umsatzerkennung nicht verfügbar. Die Schaltflächen sind im Laufe der Auftragsphasen bis zur Auftragserfüllung verfügbar oder nicht verfügbar.

[![Auftragskopf.](./media/revenue-recognition-so-basic-sales-order-header-02.png)](./media/revenue-recognition-so-basic-sales-order-header-02.png)

Die ersten drei Schaltflächen enthalten Details zum Umsatzerlöspreis für die Artikel im Auftrag, der für die Umsatzerlöserkennung eingerichtet wurde.

- **Umsatzerlöspreiszuteilung** – Diese Schaltfläche wird verfügbar, nachdem der Auftrag bestätigt wurde oder wenn die Rechnung gebucht wird. Mit der Auftragsbestätigung und der Rechnungsbuchung wird der Umsatzerlös berechnet, um den Preis zu erfassen, der im Buchhaltungseintrag erkannt oder verzögert wird. Je nach den Einstellungen kann sich der berechnete Umsatzerlöspreis vom Stückpreis unterscheiden, der dem Debitor angezeigt wird.
- **Preis mit neuen Auftragspositionen erneut zuteilen** – Diese Schaltfläche wird verfügbar, nachdem der Auftrag bestätigt wurde oder wenn die Rechnung gebucht wird. Der Neuzuteilungsprozess wird verwendet, um den nach dem Hinzufügen einer neuen Position zum aktuellen Auftrag (nach der Fakturierung) oder zu einem neuen Auftrag zu erfassenden Umsatzerlös neu zu berechnen. In beiden Szenarien verursacht die Einführung eines neuen Artikels eine Änderung des Vertrags. Daher muss der Umsatzerlöspreis neu zugeordnet werden.
- **Umsatzerlöspreiszuteilung aktualisieren** – Diese Schaltfläche wird verfügbar, nachdem der Auftrag bestätigt wurde, sie ist jedoch nicht mehr verfügbar, nachdem der Auftrag in Rechnung gestellt wurde. Die Aktualisierung wird verwendet, um die Umsatzerlöspreiszuteilung erneut auszuführen, ohne dass der Auftrag bestätigt werden muss. Nachdem der Auftrag fakturiert wurde, kann der Umsatzerlöspreis nicht neu berechnet werden.

Die letzten beiden Schaltflächen enthalten Details zum Umsatzerlöszeitplan für die Artikel im Auftrag, die einen Umsatzerlöszeitplan haben.

- **Erwarteter Umsatzerkennungszeitplan** – Diese Schaltfläche wird verfügbar, nachdem der Auftrag bestätigt wurde, sie ist jedoch nicht mehr verfügbar, nachdem der Auftrag in Rechnung gestellt wurde. Dies öffnet eine Seite, auf der der Zeitplan des erwarteten Umsatzerlöses angezeigt wird. Der endgültige Zeitplan ändert sich möglicherweise noch, da der voraussichtliche Zeitplan das angeforderte Lieferdatum verwendet, während der endgültige Zeitplan das tatsächliche Versanddatum verwendet.
- **Umsatzerkennungszeitplan** – Diese Schaltfläche wird verfügbar, nachdem der Auftrag fakturiert wurde. Der endgültige Umsatzerkennungszeitplan wird nicht bei der Bestätigung oder der Erstellung eines Lieferscheins erstellt. Er wird erst erstellt, wenn der Auftrag fakturiert wurde.

Im folgenden Beispiel erfolgte die Umsatzerlöspreiszuteilung, nachdem der Auftrag bestätigt wurde. Beachten Sie, dass der Gesamtbetrag im Feld **Zu erkennender Umsatzerlös** der Summe der Auftragspositionen entsprechen muss, die dem Debitor in Rechnung gestellt werden, obwohl die Umsatzerlöspreise unterschiedlich zugewiesen sind. Beispielsweise beträgt die Summe der Auftragspositionen, abzüglich Steuern, 1.499 US-Dollar. Daher muss die Summe der Werte **Zu erkennender Umsatzerlös** auch 1.499 US-Dollar betragen.

[![Umsatzerlöspreiszuteilung.](./media/revenue-recognition-so-basic-revenue-price-allocation.png)](./media/revenue-recognition-so-basic-revenue-price-allocation.png)

Der erwartete Umsatzerlöserkennungszeitplan wird ebenfalls erstellt. Der Umsatzerlöszeitplan verwendet den Wert **Zu erkennender Umsatzerlös** als den Betrag, der verzögert werden soll. Artikel S0001 verzögert 321,21 US-Dollar anstelle von 300 US-Dollar und Artikel S0008 verzögert 160,61 US-Dollar anstatt 100 US-Dollar. Artikel S0012 wird nicht im erwarteten Zeitplan angezeigt, da der Umsatzerlös verzögert wird. Wenn die Buchung stattfindet, bucht Artikel S0012 1.017,18 US-Dollar direkt auf das Umsatzerlössachkonto.

[![Erwarteter Umsatzerlöserkennungszeitplan.](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)

## <a name="create-the-packing-slip"></a>Lieferschein erstellen

Im nächsten Schritt kann der Lieferschein für den Auftrag erstellt werden. Es wird kein Umsatzerlös erkannt, wenn der Lieferschein gebucht wird. Wenn der Auftrag nicht bestätigt wurde, löst die Buchung des Lieferscheins keine Umsatzerlöspreisberechnung aus. Darüber hinaus wird auch die Erstellung des erwarteten oder endgültigen Umsatzerkennungszeitplans nicht ausgelöst. Wenn die Artikelmodellgruppe so eingerichtet ist, dass der Umsatzerlös für den Lieferschein verzögert wird, wird sie weiterhin mithilfe der aktuellen Buchungsprofilsachkonten und nicht mit den neuen verzögerten Umsatzerlöskonten buchen, die in der Rechnung verwendet werden.

## <a name="create-the-invoice"></a>Erstellen der Rechnung

Im letzten Schritt wird der Auftrag in Rechnung gestellt. Wenn Sie sich den Beleg der Rechnung ansehen, erkennen Sie, dass der Umsatzerlös für die Artikel S0001 und S0008 verzögert wurde (321,21 US-Dollar + 160,61 US-Dollar = 481,82 US-Dollar), und der verbleibende Betrag für Artikel S0012 wurde zum Umsatzerlös (1.017,18) gebucht. Diese Werte ergeben zusammen 1.499 US-Dollar, was der Summe der Auftragspositionen entspricht.

[![Buchungen für Beleg.](./media/revenue-recognition-so-voucher-transactions.png)](./media/revenue-recognition-so-voucher-transactions.png)

Nachdem die Rechnung erstellt wurde, sind die Schaltflächen **Umsatzerlöspreiszuteilung**, **Preis mit neuen Auftragspositionen erneut zuteilen** und **Umsatzerlöserkennungszeitplan** für die Umsatzerlöserkennung verfügbar, doch die Schaltflächen **Umsatzerlöspreiszuteilung aktualisieren** und **Erwarteter Umsatzerlöserkennungszeitplan** sind nicht verfügbar.

[![Verfügbarkeit der Umsatzerlöserkennungsschaltflächen.](./media/revenue-recognition-so-basic-after-invoice-buttons.png)](./media/revenue-recognition-so-basic-after-invoice-buttons.png)

Die Schaltfläche **Umsatzerlöspreiszuteilung** ist weiterhin verfügbar, sodass Sie die Umsatzerlöspreisberechnung anzeigen können. Wenn nach seiner Bestätigung nichts am Auftrag geändert wurde, ändert das Buchen der Rechnung nicht den berechneten Betrag im Feld **Zu erkennender Umsatzerlös**.

Der erwartete Umsatzerkennungszeitplan wird entfernt und durch den endgültigen Umsatzerkennungszeitplan ersetzt. Die Umsatzerlöszeitplandetails werden für jede Auftragsposition verwaltet und verwendet, um den verzögerten Umsatzerlös für den tatsächlichen Umsatzerlös freizugeben, während die vertraglichen Verpflichtungen eingehalten werden.

[![Endgültiger Umsatzerlöserkennungszeitplan.](./media/revenue-recognition-so-revenue-recognition-schedule.png)](./media/revenue-recognition-so-revenue-recognition-schedule.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
