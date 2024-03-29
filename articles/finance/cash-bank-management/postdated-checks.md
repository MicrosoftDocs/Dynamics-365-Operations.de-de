---
title: Vordatierte Schecks
description: Dieser Artikel enthält Informationen über die Unterstützung bei vordatierten Prüfungen. Vordatierte Schecks werden ausgestellt, um Zahlungen zu einem späteren Zeitpunkt zu leisten und zu empfangen.
author: angelad116
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: kfend
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d32ed9de66bc92e17c5515a4266f41aaeb9f2c1
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151360"
---
# <a name="postdated-checks"></a>Vordatierte Schecks

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen über die Unterstützung bei vordatierten Prüfungen. Vordatierte Schecks sind Schecks, die ausgestellt werden, um Zahlungen zu einem späteren Datum leisten oder erhalten zu können. Daher kann der Scheck nicht bis zum angegebene Datum eingewechselt werden.

Dynamics 365 Finance unterstützt den vollständigen Verwaltungszyklus für vordatierte Prüfungen in Debitoren und Kreditoren wie in der folgenden Tabelle dargestellt.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Szenario</th>
<th>Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Einrichten von vordatierten Schecks</td>
<td>Sie müssen eine neue Zahlungsmethode einrichten und definieren die Zahlungsroutine für das Vorbereiten für ausgegebene Schecks, Erhaltene Schecks und Quellensteuer.</td>
</tr>
<tr class="even">
<td>Erfassen und Buchen eines vordatierten Schecks für einen Kreditor</td>
<td>Erfassung eines vordatierten Schecks, bevor der Scheck an einen Kreditor ausgestellt wird. Wenn die Zahlung gebucht wird, werden die die Verbindlichkeiten dem Kreditor gegenüber erkannt, doch der Betrag wurde dem Bankkonto noch nicht gutgeschrieben. Stattdessen wird ein Verrechnungskonto für diesen Zweck verwendet. </td>
</tr>
<tr class="odd">
<td>Erfassen und Buchen eines vordatierten Schecks von einem Debitor</td>
<td>Sie können die Details eines vordatierten Schecks erfassen, den Sie von einem Debitor erhalten haben. Wenn die Zahlung gebucht wird, werden die die Verbindlichkeiten dem Kreditor gegenüber erkannt, doch der Betrag wurde dem Bankkonto noch nicht gutgeschrieben. Stattdessen wird ein Verrechnungskonto für diesen Zweck verwendet.</td>
</tr>
<tr class="even">
<td>Erfassen und Buchen eines vordatierten Ersatzschecks für einen Kunden oder einen Händler.</td>
<td>
Wenn Ihr Originalscheck an einen Händler oder von einem Kunden verloren ging oder beschädigt wird, können Sie für den Kreditor einen vordatierten Ersatzscheck ausstellen. Geben Sie beim Erfassen der Scheckdetails einen Verweis auf den Originalscheck an, und weisen Sie darauf hin, dass der neue Scheck als Ersatz für das Original gilt. Sie können den Ersatzscheck auch buchen.</td>
</tr>
<tr class="odd">
<td>Übertragen eines vordatierten Debitorenschecks an einen Kreditor</td>
<td>Wenn Sie von einem Kunden einen vordatierten Scheck erhalten, können Sie diesen Scheck als Zahlung an einen Kreditor übermitteln.</td>
</tr>
<tr class="even">
<td>Ausgleichen eines vordatierten Schecks für einen Kreditor</td>
<td>Verwenden Sie das Formular , um einen rückdatierten Scheck auszugleichen, der für einen Debitor oder Kreditor auf ein Transferkonto gebucht wurde. Wenn der Scheck ausgeglichen wird, ist die Bank schließlich Soll oder Haben für das Verrechnungskonto, das zuvor verwendet wurde.</td>
</tr>
<tr class="odd">
<td>Stornieren eines vordatierten Schecks für einen Kreditor</td>
<td>Sie können einen gebuchten vordatierten Scheck in diesen Fällen stornieren: - Die Bank verweigert die Annahme des Schecks.
- Der Scheck wurde auf eine falsche Rechnung angewendet.
- Für den Betrag des Schecks wird eine Barzahlung geleistet.
  </td>
  </tr>
  <tr class="even">
  <td>Beenden der Zahlung eines vordatierten Schecks.</td>
  <td>Sie können die Zahlung für einen vordatierten Scheck stoppen, der für einen Kreditor ausgestellt wurde. Gründe dafür können eine mangelnde Deckung, eine Änderung der vertraglichen Vereinbarungen mit dem Kreditor, die Lieferung fehlerhafter Waren durch den Kreditor oder die Rückgabe von Waren an den Kreditor sein. Sie können Zahlungen nur für Schecks stoppen, die noch nicht verrechnet wurden.</td>
  </tr>
  </tbody>
  </table>



Weitere Informationen finden Sie in folgenden Themen:

[Vordatierte Schecks einrichten](tasks/set-up-postdated-checks.md)

[Einen vordatierten Scheck für einen Debitor erfassen und buchen](tasks/register-post-postdated-check-customer.md)

[Einen vordatierten Scheck von einem Debitor ausgleichen](tasks/settle-postdated-check-customer.md)

[Einen vordatierten Scheck für einen Kreditor erfassen und buchen](tasks/register-post-postdated-check-vendor.md) 

[Einen vordatierten Scheck für einen Kreditor ausgleichen](tasks/settle-postdated-check-vendor.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
