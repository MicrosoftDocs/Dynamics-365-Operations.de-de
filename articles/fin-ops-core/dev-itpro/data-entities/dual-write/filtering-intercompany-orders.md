---
title: Intercompany-Aufträge filtern, um die Synchronisierung von Aufträgen und Auftragspositionen zu vermeiden
description: In diesem Thema wird beschrieben, wie Intercompany-Aufträge gefiltert werden, um die Synchronisierung von Aufträgen und Auftragspositionen zu vermeiden.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701032"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>Intercompany-Aufträge filtern, um die Synchronisierung von Aufträgen und Auftragspositionen zu vermeiden

[!include [banner](../../includes/banner.md)]

Sie können Intercompany-Aufträge filtern, um die Synchronisierung der Entitäten **Orders** und **OrderLines** zu vermeiden. In einigen Szenarien sind die Intercompany-Auftragsdetails in der Kundenbindungs-App nicht erforderlich.

Jede der Common Data Service-Standardentitäten wird mit Verweisen auf das Feld **IntercompanyOrder** erweitert und die Zuordnungen für duales Schreiben werden geändert, um auf die zusätzlichen Felder in den Filtern zu verweisen. Das Ergebnis ist, dass die Intercompany-Aufträge nicht mehr synchronisiert werden. Dieser Prozess vermeidet unnötige Daten in der Kundenbindungs-App.

1. Fügen Sie einen Verweis auf **IntercompanyOrder** zu **CDS-Auftragskopfzeilen** hinzu. Eine Auffüllung erfolgt nur bei Intercompany-Aufträgen. Das Feld **IntercompanyOrder** ist in **SalesTable** verfügbar.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Staging dem Ziel zuordnen, SalesOrderHeader":::
    
2. Nachdem **CDS-Auftragskopfzeilen** erweitert wurde, ist das Feld **IntercompanyOrder** im Mapping verfügbar. Wenden Sie einen Filter mit `INTERCOMPANYORDER == ""` als Abfragezeichenfolge an.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Kundenauftragskopfzeilen, Abfrage bearbeiten":::

3. Fügen Sie einen Verweis auf **IntercompanyInventTransId** zu **CDS-Auftragspositionen** hinzu.  Eine Auffüllung erfolgt nur bei Intercompany-Aufträgen. Das Feld **InterCompanyInventTransID** ist in **SalesLine** verfügbar.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Staging dem Ziel zuordnen, SalesOrderLine":::

4. Nachdem **CDS-Auftragspositionen** erweitert wurde, ist das Feld **IntercompanyInventTransId** im Mapping verfügbar. Wenden Sie einen Filter mit `INTERCOMPANYINVENTTRANSID == ""` als Abfragezeichenfolge an.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Auftragspositionen, Abfrage bearbeiten":::

5. Erweitern Sie **Verkaufsrechnungskopfzeile V2** und **Verkaufsrechnungspositionen V2** auf die gleiche Weise, auf die Sie die Common Data Service-Entitäten in den Schritten 1 und 2 erweitert haben. Fügen Sie dann die Filterabfragen hinzu. Die Filterzeichenfolge für **Verkaufsrechnungskopfzeile V2** ist `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`. Die Filterzeichenfolge für **Verkaufsrechnungspositionen V2** ist `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Staging dem Ziel zuordnen, Verkaufsrechnungskopfzeilen":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Verkaufsrechnungskopfzeilen, Abfrage bearbeiten":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Verkaufsrechnungspositionen, Abfrage bearbeiten":::

6. Die Entität **Angebote** hat keine Intercompany-Beziehung. Wenn jemand ein Angebot für einen Ihrer Intercompany-Kunden erstellt, können Sie alle diese Kunden über das Feld **Kundengruppe** in eine Kundengruppe einordnen.  Kopfzeilen und Positionen können erweitert werden, um das Feld **CustGroup** hinzuzufügen und anschließend zu filtern, um diese Gruppe nicht einzuschließen.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Staging dem Ziel zuordnen, Verkaufsangebotskopfzeile":::

7. Nachdem Sie die Entität **Zitate** erweitert haben, wenden Sie einen Filter mit `CUSTGROUP !=  "<company>"` als Abfragezeichenfolge an.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Verkaufsangebotskopfzeile, Abfrage bearbeiten":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]