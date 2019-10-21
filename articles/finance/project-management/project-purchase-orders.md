---
title: Bestellungen für ein Projekt
description: In diesem Artikel werden die verschiedenen Methoden beschrieben, die Sie verwenden können, um Bestellungen für ein Projekt zu erstellen. Die Methode, die Sie verwenden, wird durch den Zweck der Bestellung, durch den Verbrauchszeitpunkt der eingekauften Artikel und dem Zeitpunkt der Fakturierung für ein Projekt bestimmt.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174557"
---
# <a name="purchase-orders-for-a-project"></a>Bestellungen für ein Projekt

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die verschiedenen Methoden beschrieben, die Sie verwenden können, um Bestellungen für ein Projekt zu erstellen. Die Methode, die Sie verwenden, wird durch den Zweck der Bestellung, durch den Verbrauchszeitpunkt der eingekauften Artikel und dem Zeitpunkt der Fakturierung für ein Projekt bestimmt.

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

Weitere Informationen finden Sie unter[Entgegennehmen eines Artikel in Bestellungsanforderung](tasks/receive-items-purchase-order-item-requirement.md).

