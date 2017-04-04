---
title: Bestandsobjektwerte
description: "Dieser Artikel erläutert, wie die Werte eines Bestandsobjekts berechnet werden."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>Bestandsobjektwerte

Dieser Artikel erläutert, wie die Werte eines Bestandsobjekts berechnet werden. 

Neuen Funktionen, die Bezeichnung ** physische Menge ** lassen Sie die Werte eines bestimmten Bestandsobjekts finden. Ein Kostenobjekt stellt die Entitätsebene dar, in der Bestandsbuchhaltung ausgeführt wird. Weitere Informationen zu den Kostenobjekten finden Sie unter [Kostenobjekte](cost-object.md). Damit die Werte eines bestimmten Bestandsobjekts anzuzeigen, klicken Sie ** physische Menge ** ** Kostenträger ** auf der Seite. Das hier, wie der Wert eines Bestandsobjekts berechnet wird: Bestandsobjekt. Wert = Kostenträger. Durchschnittliches Einheitenkosten × Bestandsobjekt. Menge die folgenden Beispielsshows, wie die Werte eines Bestandsobjekts und des Kostenträgers berechnet werden. Zwei Produktzugangsereignisse werden auf Artikel A erfasst:

-   Produktzugang 1: Menge = 100. Stk, Betrag = 00 Euro, = 1, Standort, Lagerort =11, Charge Nein. = B1
-   Produktzugang 2: Menge = 50. Stk, Betrag = $800,00 = 1, Standort, Lagerort =11, Charge Nein. = B2

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
<td>A:</td>
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



<a name="see-also"></a>Siehe auch
--------

[Cost objects](cost-object.md)

[Cost entries](cost-entries.md)

[Die neu in und Microsoft Dynamics AX ist /dynamics365/operations/dev-itpro/get-started/what] "geändert wurde - neu-geändert)


