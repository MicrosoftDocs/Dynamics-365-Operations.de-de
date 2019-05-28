---
title: Bestandsobjektwerte
description: Dieser Artikel erläutert, wie die Werte eines Bestandsobjekts berechnet werden.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e92c7889b11208c4d2b48eb279a104a7c226f904
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547858"
---
# <a name="inventory-object-values"></a>Bestandsobjektwerte

[!include [banner](../includes/banner.md)]

Dieser Artikel erläutert, wie die Werte eines Bestandsobjekts berechnet werden. 

Eine Neuen Funktionen mit der Bezeichnung, **physische Menge** zeigt die Werte eines bestimmten Bestandsobjekts an. 

Ein Kostenobjekt stellt die Entitätsebene dar, in der Bestandsbuchhaltung ausgeführt wird. Weitere Informationen zu den Kostenobjekten finden Sie unter [Kostenobjekte](cost-object.md). 

Damit die Werte eines bestimmten Bestandsobjekts anzuzeigen, klicken Sie **Physische Menge** auf der Seite **Kostenträger**. Hier wird dargestellt, wie der Wert eines Bestandsobjekts berechnet wird: 

Bestandsobjekt. Wert = Kostenträger. Durchschnittliche Einheitenkosten × Bestandsobjekt. Menge 

Die folgenden Beispiele zeigen, wie die Werte eines Bestandsobjekts und des Kostenträgers berechnet werden. Zwei Produktzugangsereignisse werden auf Artikel A erfasst:

-   Produktzugang 1: Menge = 100 PCs, Betrag = 1.000,00 €, Standort = 1, Lagerort =11, Chargennummer = B1
-   Produktzugang 2: Menge = 50 PCs, Betrag = 800,00 €, Standort = 1, Lagerort =11, Chargennummer = B2

In der folgenden Tabelle wird das Berechnungsergebnis für einen Kostenträger angezeigt. Das Ergebnis sehen Sie auf der Seite **Kostenobjekt**.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekttyp</th>
<th>Artikelnummer</th>
<th>Standort</th>
<th>Menge</th>
<th>Lagereinheit</th>
<th>Wert</th>
<th>Durchschnittliche Einheitenkosten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kostenobjekt</td>
<td>A:</td>
<td>1</td>
<td>150</td>
<td>Stck.</td>
<td><p>1800,00 €</p></td>
<td><p>12,00 €</p></td>
</tr>
</tbody>
</table>

In der folgenden Tabelle wird das Berechnungsergebnis für ein Bestandsobjekt angezeigt. Das Ergebnis sehen Sie, wenn Sie auf der Seite **Physische Menge** auf der Seite **Kostenobjekt** klicken.

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekttyp</th>
<th>Artikelnummer</th>
<th>Standort</th>
<th>Lagerort</th>
<th>Chargennummer</th>
<th>Menge</th>
<th>Lagereinheit</th>
<th>Wert</th>
<th>Durchschnittliche Einheitenkosten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bestandsobjekt</td>
<td>A:</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>Stck.</td>
<td><p>1200,00 €</p></td>
<td><p>12,00 €</p></td>
</tr>
<tr class="even">
<td>Bestandsobjekt</td>
<td>H</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>Stck.</td>
<td><p>600,00 €</p></td>
<td><p>12,00 €</p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Kostenobjekte](cost-object.md)

[Kosteneinträge](cost-entries.md)

[Neuheiten und Änderungen](../../fin-and-ops/get-started/whats-new-changed.md)



