---
title: Intercompany-Aufträge filtern, um die Synchronisierung von Aufträgen und Auftragspositionen zu vermeiden
description: In diesem Artikel wird erläutert, wie Sie Intercompany-Aufträge filtern, damit die Entitäten „Orders“ und „OrderLines“ nicht synchronisiert werden.
author: negudava
ms.date: 11/09/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: negudava
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f5b7831e103aaa219394099b79537bf0842d9be8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289279"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>Intercompany-Aufträge filtern, um die Synchronisierung von Aufträgen und Auftragspositionen zu vermeiden

[!include [banner](../../includes/banner.md)]

Sie können Intercompany-Aufträge filtern, sodass die Tabellen **Orders** und **OrderLines** nicht synchronisiert werden. In einigen Szenarien sind die Intercompany-Auftragsdetails in der Kundenbindungs-App nicht erforderlich.

Jede der Dataverse-Standardentitäten wird mit Verweisen auf die Spalte **IntercompanyOrder** erweitert und die Zuordnungen für duales Schreiben werden geändert, sodass auf die zusätzlichen Spalten in den Filtern verwiesen wird. Daher werden die Intercompany-Aufträge nicht mehr synchronisiert. Dieser Prozess vermeidet unnötige Daten in der Kundenbindungs-App.

1. Erweitern Sie die Tabelle **CDS-Auftragskopfzeilen** durch Hinzufügen eines Verweises auf die Spalte **IntercompanyOrder**. Diese Spalte wird nur für Intercompany-Aufträge ausgefüllt. Die Spalte **IntercompanyOrder** ist in der Tabelle **SalesTable** verfügbar.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Staging der Zielseite für CDS-Auftragskopfzeilen zuordnen.":::

2. Nachdem **CDS-Auftragskopfzeilen** erweitert wurde, ist die Spalte **IntercompanyOrder** in der Zuordnung verfügbar. Wenden Sie einen Filter mit `INTERCOMPANYORDER == ""` als Abfragezeichenfolge an.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Dialogfeld „Abfrage bearbeiten“ für CDS-Auftragskopfzeilen.":::

3. Erweitern Sie die Tabelle **CDS-Auftragspositionen** durch Hinzufügen eines Verweises auf die Spalte **IntercompanyInventTransId**. Diese Spalte wird nur für Intercompany-Aufträge ausgefüllt. Die Spalte **IntercompanyInventTransId** ist in der Tabelle **SalesLine** verfügbar.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Staging der Zielseite für CDS-Auftragspositionen.":::

4. Nachdem **CDS-Auftragspositionen** erweitert wurde, ist die Spalte **IntercompanyInventTransId** in der Zuordnung verfügbar. Wenden Sie einen Filter mit `INTERCOMPANYINVENTTRANSID == ""` als Abfragezeichenfolge an.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Dialogfeld „Abfrage bearbeiten“ für CDS-Auftragspositionen.":::

5. Wiederholen Sie die Schritte 1 und 2, um die Tabelle **Verkaufsrechnungskopfzeile V2** zu erweitern und eine Filterabfrage hinzuzufügen. In diesem Fall verwenden Sie `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` als Abfragezeichenfolge für den Filter.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Staging der Zielseite für Verkaufsrechnungskopfzeile V2.":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Dialogfeld „Abfrage bearbeiten“ für Verkaufsrechnungskopfzeile V2.":::

6. Wiederholen Sie die Schritte 3 und 4, um die Tabelle **Verkaufsrechnungspositionen V2** zu erweitern und eine Filterabfrage hinzuzufügen. In diesem Fall verwenden Sie `INTERCOMPANYINVENTTRANSID == ""` als Abfragezeichenfolge für den Filter.

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Dialogfeld „Abfrage bearbeiten“ für Verkaufsrechnungspositionen V2.":::

7. Die Tabelle **Angebote** hat keine Intercompany-Beziehung. Wenn jemand ein Angebot für einen Ihrer Intercompany-Kunden erstellt, können Sie alle diese Kunden über die Spalte **CustGroup** in eine Kundengruppe einordnen. Sie können die Kopfzeile und die Positionen erweitern, indem Sie die Spalte **CustGroup** hinzufügen, und filtern Sie dann so, dass die Gruppe nicht enthalten ist.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Staging der Zielseite für CDS-Verkaufsangebotskopf.":::

8. Nachdem Sie die **Angebote** erweitert haben, wenden Sie einen Filter mit `CUSTGROUP != "<company>"` als Abfragezeichenfolge an.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Dialogfeld „Abfrage bearbeiten“ für CDS-Verkaufsangebotskopf.":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
