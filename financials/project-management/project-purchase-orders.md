---
title: "Bestellungen für ein Projekt"
description: "In diesem Artikel werden die verschiedenen Methoden beschrieben, die Sie verwenden können, um Bestellungen für ein Projekt zu erstellen. Die Methode, die Sie verwenden, wird durch den Zweck der Bestellung, durch den Verbrauchszeitpunkt der eingekauften Artikel und dem Zeitpunkt der Fakturierung für ein Projekt bestimmt."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2a0c21c2937600d1e31f9326970e52e3bdcff90c
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="purchase-orders-for-a-project"></a>Bestellungen für ein Projekt

[!include[banner](../includes/banner.md)]


In diesem Artikel werden die verschiedenen Methoden beschrieben, die Sie verwenden können, um Bestellungen für ein Projekt zu erstellen. Die Methode, die Sie verwenden, wird durch den Zweck der Bestellung, durch den Verbrauchszeitpunkt der eingekauften Artikel und dem Zeitpunkt der Fakturierung für ein Projekt bestimmt.

In Microsoft Dynamics 365 for Operations können Sie mehrere Methoden verwenden, um Bestellungen für ein Projekt zu erstellen. Die Methode, die Sie verwenden, wird durch den Zweck der Bestellung, durch den Verbrauchszeitpunkt der eingekauften Artikel oder dem Zeitpunkt der Fakturierung der eingekauften Artikel für ein Projekt bestimmt.

### <a name="methods-for-creating-a-purchase-order"></a>Methoden zum Erstellen einer Bestellung

Im Projektverwaltungs- und Buchhaltungsmodul stehen die folgenden Methoden zum Erstellen einer Bestellung zur Verfügung. Der Zweck der Bestellung bestimmt, wann eine Bestellung verbraucht wird, und damit, wann ein Projekt mit Artikeln belastet wird.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Methode</th>
<th>Verwendungszweck</th>
<th>Verbrauch von Artikeln</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Erstellen einer Bestellung direkt über ein Projekt.</td>
<td>Verwenden Sie diese Methode, um Artikel von einem externen Kreditor für den Verbrauch in einem Projekt zu erwerben. Sie können die Bestellung auf zwei Arten erstellen:
<ul>
<li>Aus dem Projekt selbst: In diesem Fall wurde das Projekt für die Bestellung bereits definiert.</li>
<li>Per Navigation zur Projektbestellung Hierbei müssen Sie sowohl den Kreditor als auch das Projekt auswählen, für den bzw. das die Bestellung erstellt werden soll.</li>
</ul></td>
<td>Artikel werden verbraucht, wenn die Kreditorenrechnung aktualisiert wird.</td>
</tr>
<tr class="even">
<td>Bestellung aus einem Auftrag erstellen  </td>
<td>Verwenden Sie diese Methode, wenn Sie einen Auftrag über eon Projekt erstellen.</td>
<td>Artikel werden verbraucht, wenn die Rechnung für den Auftrag an den Debitor gestellt wird.</td>
</tr>
<tr class="odd">
<td>Bestellung aus einem Artikelbedarf erstellen  </td>
<td>Verwenden Sie diese Methode, wenn Sie einen Artikelbedarfs über ein Projekt erstellen.</td>
<td>Artikel werden verbraucht, wenn der Lieferschein des Artikelbedarfs aktualisiert wird.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Wenn die Kreditorenrechnung oder der Lieferschein aktualisiert wird, werden Sie aufgefordert, den Lieferschein für den Artikelbedarf zu aktualisieren.




