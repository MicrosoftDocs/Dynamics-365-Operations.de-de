---
title: Angeben zur Entsorgung zurückgelieferter Artikel
description: Angeben zur Entsorgung zurückgelieferter Artikel.
author: sorenva
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3123f49ef5fbd07afa61b035a2f6dd4c0af2ce40
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679218"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>Angeben zur Entsorgung zurückgelieferter Artikel

[!include [banner](../includes/banner.md)]

Wenn Sie eine Rücklieferung verarbeiten, muss mittels eines Ursachencodes angegeben werden warum das Produkt zurückgegeben wird. Sie müssen auch einen Dispositionscode und eine Dispositionsaktivität angeben, um zu bestimmen, wie mit dem zurückgelieferten Produkt verfahren werden soll.

Ein Dispositionscode kann beim Erstellen der Rücklieferung, beim Erfassen des Wareneingangs oder beim Ausführen einer Lieferscheinaktualisierung eines Wareneingangs sowie beim Beenden eines Quarantäneauftrags angewendet werden.

Sie haben die Möglichkeit zum Erstellen beliebiger Dispositionscodes, die für die verwendeten Geschäftsprozesse benötigt werden. In der folgenden Tabelle finden Sie eine Reihe häufig verwendeter Codes für die Disposition zurückgelieferter Artikel:

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Dispositionstyp</p></th>
<th><p>Allgemeiner Code</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Abgang</p></td>
<td><p>AV</p></td>
<td><p>Ausschuss/Vernichtung</p></td>
</tr>
<tr class="even">
<td><p>Abgang</p></td>
<td><p>WZ</p></td>
<td><p>Spende für wohltätige Zwecke</p></td>
</tr>
<tr class="odd">
<td><p>Abgang</p></td>
<td><p>ED</p></td>
<td><p>Entsorgung durch Dritte</p></td>
</tr>
<tr class="even">
<td><p>Abgang</p></td>
<td><p>AM</p></td>
<td><p>Altmaterial</p></td>
</tr>
<tr class="odd">
<td><p>Abgang</p></td>
<td><p>VD</p></td>
<td><p>Verkauf durch Dritte (Sekundärmärkte)</p></td>
</tr>
<tr class="even">
<td><p>Reparatur/Abänderung</p></td>
<td><p>NB</p></td>
<td><p>Nachbesserung</p></td>
</tr>
<tr class="odd">
<td><p>Reparatur/Abänderung</p></td>
<td><p>AÜ</p></td>
<td><p>Aufbereitung/Überholung</p></td>
</tr>
<tr class="even">
<td><p>Reparatur/Abänderung</p></td>
<td><p>AÄ</p></td>
<td><p>Abänderung</p></td>
</tr>
<tr class="odd">
<td><p>Reparatur/Abänderung</p></td>
<td><p>RP</p></td>
<td><p>Reparatur</p></td>
</tr>
<tr class="even">
<td><p>Reparatur/Abänderung</p></td>
<td><p>RK</p></td>
<td><p>Rücklieferung an Kreditor</p></td>
</tr>
<tr class="odd">
<td><p>Sonstiges</p></td>
<td><p>KÄ</p></td>
<td><p>Keine Änderung</p></td>
</tr>
<tr class="even">
<td><p>Sonstiges</p></td>
<td><p>WV</p></td>
<td><p>Wiederverkauf</p></td>
</tr>
<tr class="odd">
<td><p>Sonstiges</p></td>
<td><p>AT</p></td>
<td><p>Austausch</p></td>
</tr>
<tr class="even">
<td><p>Sonstiges</p></td>
<td><p>SO</p></td>
<td><p>Sonstiges</p></td>
</tr>
</tbody>
</table>


Für jeden Dispositionscode, den Sie definieren, müssen Sie eine Dispositionsaktivität auswählen. Die Dispositionsaktivität bestimmt die physischen und die finanziellen Auswirkungen der Dispositionscodes. Beispielsweise bestimmt die Dispositionsaktivität die physische Handhaben der zurückgelieferten Artikel, die finanziellen Auswirkungen des zurückgegebenen Artikels und wenn ein Ersetzungsartikel an den Debitor gesendet werden muss. Sie können eine unbegrenzte Anzahl Dispositionscodes gemäß Ihren Geschäftsanforderungen definieren, es bestehen jedoch nur sechs vordefinierte Dispositionsaktivitäten, von denen Sie auswählen können. Die folgende Tabelle enthält die Dispositionsaktivitäten und deren Definitionen.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Dispositionsaktivität</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Entlastung</strong></p></td>
<td><p>Den Artikel zum Lager zurücksenden und dem Debitor gutschreiben.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nur gutschreiben</strong></p></td>
<td><p>Schreiben Sie den Artikel dem Debitor gut, ohne den Artikel einzufordern oder zu erwarten, dass er zurückgeliefert wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Ausschuss</strong></p></td>
<td><p>Verschrotten Sie den Artikel und schreiben Sie ihn dem Debitor gut.</p></td>
</tr>
<tr class="even">
<td><p><strong>Ersatz und Entlastung</strong></p></td>
<td><p>Geben Sie den Artikel dem Lager zurück, erstellen Sie einen Ersetzungsauftrag und schreiben Sie ihn dem Debitor gut.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Ersatz und Aussonderung</strong></p></td>
<td><p>Verschrotten Sie den Artikel, erstellen Sie einen Ersetzungsauftrag und schreiben Sie ihn dem Debitor gut.</p></td>
</tr>
<tr class="even">
<td><p><strong>Rückgabe an den Debitor</strong></p></td>
<td><p>Lehnen Sie den zurückgesendeten Artikel ab und senden Sie ihn dem Debitor zurück.</p></td>
</tr>
</tbody>
</table>

## <a name="select-a-disposition-code-for-a-quarantine-order"></a>Auswählen eines Dispositionscodes für einen Quarantäneauftrag

1. Wechseln Sie zu **Lagerverwaltung** \> **Periodisch** \> **Qualitätsmanagement** \> **Quarantäneaufträge**.
1. Wählen Sie für einen vorhandenen Quarantäneauftrag auf der Registerkarte **Übersicht** im Feld **Dispositionscode** eine Option aus.

## <a name="see-also"></a>Siehe auch

[Formular "Quarantäneauftrag"](/dynamicsax-2012//quarantine-order-form)

[Dispositionscodes (Formular)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
