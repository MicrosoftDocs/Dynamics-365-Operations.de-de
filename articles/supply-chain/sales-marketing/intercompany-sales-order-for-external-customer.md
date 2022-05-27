---
title: Einen Intercompany-Auftrag für einen externen Debitor erstellen und abrechnen
description: In diesem Thema wird erläutert, wie Sie einen Intercompany-Auftrag für einen externen Debitor erstellen und abrechnen.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c8a22ded1a6242e4062e1ce9e0ce624d4579fba9
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669376"
---
# <a name="create-and-invoice-an-intercompany-sales-order-for-an-external-customer"></a>Einen Intercompany-Auftrag für einen externen Debitor erstellen und abrechnen

[!include [banner](../../includes/banner.md)]

Sie können den Intercompany-Handel verwenden, um den Verkauf eines Produkts von einer juristischen Person an eine andere juristische Person in derselben Organisation zu erfassen.

Mit dem Erstellen des Originalauftrags kann automatisch eine Intercompany-Bestellung für den Intercompany-Kreditor erstellt werden. Damit wird automatisch ein Intercompany-Auftrag in der juristischen Person des Intercompany-Kreditors erstellt.

Die folgende Abbildung zeigt den Fluss der Posten an, wenn Sie einen Auftrag für einen externen Debitor erstellen, aber das Produkt muss von einer anderen juristischen Person Ihrer Organisation bestellt werden, bevor Sie das Produkt an den Debitor liefern können. In diesem Fall wird eine Intercompany-Bestellung für das Kreditorenkonto erstellt, das die andere juristische Person darstellt. Wiederum wird ein Intercompany-Auftrag in der anderen juristische Person für das Debitorenkonto erstellt, das Ihre juristische Person darstellt. Beim Fakturieren einer Intercompany-Bestellung wird die Rechnung für den Originalauftrag automatisch gebucht, wenn es sich um eine Direktlieferung handelt.

![Externer Intercompany-Verkaufsprozess](media/intercompanyexternalsalesprocess.png)

Wenn Sie bei Verwendung der Direktlieferung auf der Seite **Rechnung buchen** im Feld **Menge** die Option **Lieferschein** ausgewählt, basiert die Intercompany-Kreditorenrechnung auf dem zuvor gebuchten Intercompany-Produktzugang.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt werden, um die Intercompany-Rechnungen automatisch zu buchen und zu drucken.

1. Wechseln Sie zu **Vertrieb und Marketing \> Debitoren \> Alle Debitoren**.
1. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Allgemein**, und wählen Sie **Intercompany** aus.
1. Gehen Sie zu **Beschaffung \> Kreditoren \> Alle Kreditoren**.
1. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Allgemein**, und wählen Sie **Intercompany** aus.
1. Aktivieren Sie auf der Seite **Intercompany** entweder für den Kreditor oder den Debitor im Bereich **Bestellrichtlinien** in der Feldgruppe **Intercompany-Bestellung (Direktlieferung)** das Kontrollkästchen **Rechnung automatisch buchen**.
1. Aktivieren Sie im Bereich **Bestellrichtlinien** in der Feldgruppe **Originalauftrag (Direktlieferung)** das Kontrollkästchen **Rechnung automatisch buchen**. Aktivieren Sie das Kontrollkästchen, wenn die Rechnung für den Originalauftrag automatisch gedruckt werden soll, wenn Sie die Intercompany-Kreditorenrechnung buchen.

> [!NOTE]
> Die Druckeinstellungen für die Rechnung werden durch die Einstellungen für das Modul, das Dokument oder die Buchung auf der Seite **Druckverwaltungseinstellungen** bestimmt.

## <a name="create-an-original-sales-order-for-an-external-customer"></a>Originalauftrag für einen externen Debitor erstellen

Führen Sie diese Schritte unter „Juristische Person A“ aus. Dieses Verfahren entspricht dem mit 1 beschrifteten Feld in der Abbildung.

1. Wechseln Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.
1. Erstellen Sie den ursprünglichen Auftrag auf der Seite mit der Liste **Alle Verkaufsaufträge**. Die Feldwerte werden vom Debitorenkonto in den Auftrag kopiert.
1. Wählen Sie im Aktionsbereich auf der Seite **Auftrag** die Option **Kopfzeilenansicht** aus.
1. Aktivieren Sie im Inforegister **Intercompany-Einstellungen** das Kontrollkästchen **Intercompany-Aufträge automatisch erstellen**.
1. Wenn der Intercompany-Kreditor die Ware direkt an den externen Debitor liefern soll, aktivieren Sie das Kontrollkästchen **Direktlieferung**.
1. Wenn Sie mit der Eingabe des Auftrags fertig sind, schließen Sie die Seite **Auftrag**.

Die Intercompany-Bestellung wird automatisch für alle Artikel erstellt, denen ein Intercompany-Kreditor zugewiesen ist. Anschließend wird der Intercompany-Auftrag erstellt. In einer Informationsnachricht werden Sie darüber informiert, dass eine Intercompany-Bestellung und ein Intercompany-Auftrag erstellt wurden. Die Nachricht enthält auch Links zu diesen Aufträgen. Wenn ein Artikel nicht gefunden wurde, wird eine rote Warnung angezeigt, die darauf hinweist, dass der Auftragserstellungsprozess nicht abgeschlossen wurde.

> [!NOTE]
> Wenn Sie mehrere Aufträge in unterschiedlichen juristischen Personen erstellen und die Artikel in einer der juristischen Personen nicht gefunden wurden, wird die Auftragserstellung auch für die juristischen Personen gestoppt, die die Aufträge erfüllen könnten.

## <a name="invoice-an-intercompany-sales-order"></a>Intercompany-Auftrag fakturieren

Bei der Fakturierung eines Intercompany-Auftrags wird die zugehörige Intercompany-Bestellung automatisch fakturiert. Handelt es sich beim ursprünglichen Auftrag um einen Direktlieferungsauftrag, wird der Originalauftrag automatisch fakturiert.

Führen Sie diese Schritte unter „Juristische Person B“ aus. Dieses Verfahren entspricht dem mit 2 beschrifteten Feld in der Abbildung.

1. Wechseln Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.
1. Wählen Sie auf der Seite mit der Liste **Alle Aufträge** den Intercompany-Auftrag aus.
1. Wählen Sie im Aktionsbereich die Registerkarte **Rechnung** und dann **Rechnung** aus.
1. Aktivieren Sie das Kontrollkästchen **Buchung**.
1. Wählen Sie den Auftrag und anschließend **OK** aus.

Die Debitorenrechnung für den Intercompany-Auftrag wird automatisch unter „Juristische Person B“ gebucht. Die Intercompany-Kreditorenrechnung wird automatisch unter „Juristische Person A“ erstellt und gebucht. Ist der Originalauftrag als Direktlieferung eingerichtet, wird die Debitorenrechnung für den Originalauftrag unter „Juristische Person A“ erstellt.

> [!NOTE]
> Bisher konnte bei Intercompany-Verkaufsszenarien der Verkaufsauftrag nicht erfolgreich fakturiert werden, wenn der Workflow für die Einkaufsrechnung des Kreditors in der Intercompany-Einkaufsfirma konfiguriert war. Daher musste der Workflow für die Einkaufsrechnungen des Kreditors für die Intercompany einkaufende Firma ausgeschaltet werden. 
> 
> Diese Einschränkung wurde durch eine neue Funktion in Version 10.0.25 behoben. Intercompany Verkaufsaufträge können jetzt fakturiert werden, wenn der Workflow für Einkaufsrechnungen in der Firma des Einkäufers konfiguriert ist.
> 
> Um diese Funktion zu aktivieren, gehen Sie folgendermaßen vor.
>
> 1. Wählen Sie die juristische Entität des Intercompany-Verkaufs.  
> 2. Gehen Sie zu **Debitorenkonten \> Debitoren \> Alle Debitoren**.
> 3. Wählen Sie den Debitor für die Firma, die intercompany Einkäufe tätigt.
> 4. Gehen Sie auf **Allgemein \> Einrichten \> Intercompany**.
> 5. Wählen Sie auf der Registerkarte **Richtlinien für Bestellungen** den Parameter **Workflow für Einkaufsrechnungen zwischen Kreditor und Unternehmen umgehen**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
