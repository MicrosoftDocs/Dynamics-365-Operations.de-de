---
title: Standardgegenkonten für Kreditorenrechnungs- und Rechnungsgenehmigungserfassungen
description: Dieser Artikel hilft Ihnen, zu entscheiden, wohin Standardkonten für Rechnungserfassungen zugewiesen werden sollten.
author: abruer
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.form: LedgerJournalTable
ms.openlocfilehash: ed75e0a3b9994d061e94d07ffcc43e3b73bec55e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281671"
---
# <a name="default-offset-accounts-for-vendor-invoice-and-invoice-approval-journals"></a>Standardgegenkonten für Kreditorenrechnungs- und Rechnungsgenehmigungserfassungen

[!include [banner](../includes/banner.md)]

Standardgegenkonten werden auf den folgenden Kreditorenrechnungserfassungs-Seiten verwendet:

-   Rechnungserfassung
-   Rechnungsgenehmigungs-Erfassung

Verwenden Sie die folgende Tabelle, um zu entscheiden, wohin Standardkonten für Rechnungserfassungen zugewiesen werden sollten.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Standardgegenkonten hier einrichten</th>
<th>Wo Standardkonten bereitgestellt werden</th>
<th>Wie sich diese Option auf die Verarbeitung auswirkt</th>
<th>Wann Sie diese Option verwenden sollten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Kreditorengruppe</strong> – Richten Sie Standardgegenkonten für Kreditorengruppen auf der Seite <strong>Standardkontoeinstellungen</strong> ein, die Sie von der Seite <strong>Kreditorengruppen</strong> aus öffnen können.</td>
<td><ul>
<li>Kreditorenkonto</li>
<li>Erfassungseinträge für Kreditorenkonten in der Kreditorengruppe, wenn keine Standardkonten für Kreditorenkonten angegeben werden</li>
</ul></td>
<td>Die Standardgegenkonten für Kreditorengruppen werden auf der Seite <strong>Standardkontoeinstellungen</strong> als Standardgegenkonten für Kreditoren angezeigt. Sie können diese Seite über die Listenseite <strong>Alle Kreditoren</strong> öffnen.</td>
<td>Verwenden Sie diese Option, wenn Sie im Laufe der Zeit in der Regel für dieselben Arten von Produkten oder Dienstleistungen von denselben Kreditorengruppen bezahlen.</td>
</tr>
<tr class="even">
<td><strong>Kreditorenkonto</strong> – Richten Sie Standardkonten für Kreditorenkonten auf der Seite <strong>Standardkontoeinstellungen</strong> ein, die Sie von der Seite <strong>Kreditoren</strong> aus öffnen können.</td>
<td>Erfassungseinträge für das Kreditorenkonto</td>
<td>Die Standardgegenkonten für Kreditorenkonten werden als Standardgegenkonten für Erfassungseinträge für das Kreditorenkonto anzeigt.</td>
<td>Verwenden Sie diese Option, wenn Sie im Laufe der Zeit in der Regel für dieselben Arten von Produkten oder Dienstleistungen von denselben Kreditoren bezahlen.</td>
</tr>
<tr class="odd">
<td><strong>Erfassungsnamen</strong> – Richten Sie Standardgegenkonten für Erfassungen auf der Seite <strong>Erfassungsnamen</strong> ein. Wählen Sie die Option <strong>Festes Gegenkonto</strong> aus. Beachten Sie, dass Sie keine Standardgegenkonten zu Erfassungsnamen angeben können, wenn der Erfassungstyp der Erfassungsnamen <strong>Rechnungsbuch</strong> oder <strong>Genehmigung</strong> ist.</td>
<td><ul>
<li>Erfassungskopf, der den gleichen Erfassungsnamen verwendet</li>
<li>Erfassungseinträge in Erfassungen, die den Erfassungsnamen verwenden</li>
</ul></td>
<td>Wenn die Option <strong>Festes Gegenkonto</strong> auf der Seite <strong>Erfassungsnamen</strong> ausgewählt ist, setzt das Gegenkonto für den Erfassungsnamen das Standardgegenkonto für den Kreditor oder die Kreditorengruppe außer Kraft.</td>
<td>Verwenden Sie diese Option, um Erfassungen für bestimmte Kosten und Ausgaben einzurichten, die für bestimmte Konten berechnet werden, unabhängig davon, wer der Kreditor ist, oder zu welcher Kreditorengruppe er gehört.</td>
</tr>
<tr class="even">
<td><strong>Erfassungsnamen</strong> – Richten Sie Standardgegenkonten für Erfassungen auf der Seite <strong>Erfassungsnamen</strong> ein. Deaktivieren Sie die Option <strong>Festes Gegenkonto</strong>. Beachten Sie, dass Sie keine Standardgegenkonten zu Erfassungsnamen angeben können, wenn der Erfassungstyp der Erfassungsnamen <strong>Rechnungsbuch</strong> oder <strong>Genehmigung</strong> ist.</td>
<td><ul>
<li>Erfassungskopf</li>
<li>Erfassungseinträge in Erfassungen, die den Erfassungsnamen verwenden</li>
</ul></td>
<td>Diese Standardeinträge werden auf Erfassungskopfseiten verwendet, und das Gegenkonto auf der Erfassungskopfseite wird als Standardeintrag auf den Erfassungsbelegseiten verwendet. Standardkonten von der Seite <strong>Erfassungsnamen </strong>werden nur verwendet, wenn für das Kreditorenkonto keine Standardkonten eingerichtet werden.</td>
<td>Verwenden Sie diese Option, um Standardkonten einzurichten, die verwendet werden, wenn kein standardmäßiges Kreditorengegenkonto zugewiesen wird.</td>
</tr>
<tr class="odd">
<td><strong>Erfassungskopf</strong> – Richten Sie ein Standardgegenkonto für eine Erfassung als ein Standardeintrag auf den Erfassungsbelegseiten ein. Beachten Sie, dass Sie keine Standardgegenkonten auf dem Erfassungskopf angeben können, wenn der Erfassungstyp der Erfassungsnamen <strong>Rechnungsbuch</strong> oder <strong>Genehmigung</strong> ist.</td>
<td>Erfassungseinträge in der Erfassung</td>
<td>Das Standardgegenkonto für eine Erfassung wird als Standardeintrag auf den Erfassungsbelegseiten verwendet.</td>
<td>Verwenden Sie diese Option, um die Dateneingabe zu beschleunigen, wenn die meisten Einträge in einer Erfassung das gleiche Gegenkonto haben.</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
