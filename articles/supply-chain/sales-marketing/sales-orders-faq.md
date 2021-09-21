---
title: Häufig gestellte Fragen zu Kundenaufträgen
description: Auf dieser Seite werden häufig gestellte Fragen behandelt, die bei der Arbeit mit Aufträgen in Dynamics 365 Supply Chain Management vorkommen.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d75022dcc476052040b16c9033cf5ff2a697ae6c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476435"
---
# <a name="sales-order-faqs"></a>Häufig gestellte Fragen zu Aufträgen

Auf dieser Seite werden häufig gestellte Fragen behandelt, die bei der Arbeit mit Aufträgen in Dynamics 365 Supply Chain Management vorkommen.

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Kann ich eine Bestellung mit einem Auftrag verknüpfen, um die Nachfrage zu befriedigen?

Sie können einer Bestellung auf Grundlage eines Auftrags erstellen. Weitere Informationen finden Sie unter [Erstellen einer Bestellung auf Grundlage eines Auftrags](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order).

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>Kann ich eine Rücklieferung oder einen Auftrag nicht stornieren oder löschen?

Sie können nur Aufträge und Rücklieferungsaufträge stornieren, die sich im *Erstellt*-Zustand befinden. Weitere Informationen finden Sie unter [Stornieren einer Rücklieferung](/dynamics365/supply-chain/service-management/cancel-return-order).

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Kann ich einen in Rechnung gestellten Auftrag wiederherstellen, der gelöscht wurde?

Wenn ein in Rechnung gestellter Auftrag versehentlich gelöscht wurde, können Sie ihn wiederherstellen oder seine Details anzeigen.

Gehen Sie zu **Kundenkonto \> Transaktionen \> Originaldokument \> Details anzeigen**. Suchen Sie die gesuchte Rechnung und wählen Sie sie aus, um die Details anzuzeigen. Diese Details enthalten die Auftragsreferenz. Sie sollten von der Seite auch auf die Auftragsdetails zugreifen können.

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>Wie lösche ich einen verwaisten Auftragsdatensatz?

Führen Sie den periodischen Einzelvorgang *Auftragslöschung* aus, um verwaiste Auftragsdatensätze zu bereinigen, indem Sie zu einem der folgenden Orte gehen:

- Klicken Sie auf Vertrieb und Marketing \> Periodische Aufgaben \> Bereinigen \> Aufträge löschen
- Retail und Commerce \> Retail und Commerce IT \> Bereinigen \> Aufträge löschen

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Gibt es eine Möglichkeit, Provisionen für bereits gebuchte Rechnungen zu berechnen?

Supply Chain Management unterstützt derzeit die Berechnung von Provisionen für gebuchte Rechnungen nicht.
