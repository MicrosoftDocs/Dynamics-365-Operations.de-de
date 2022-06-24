---
title: Debitoren-Buchungsprofile
description: Dieser Artikel umfasst Debitorenbuchungsprofile, die zum Steuern von Debitorenbuchungen auf das Hauptbuch dienen.
author: JodiChristiansen
ms.date: 12/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0563040590eefab57706b183281c47a82e46076
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891694"
---
# <a name="customer-posting-profiles"></a>Debitoren-Buchungsprofile

[!include [banner](../includes/banner.md)]

Dieser Artikel umfasst Debitorenbuchungsprofile, die zum Steuern von Debitorenbuchungen auf das Hauptbuch dienen.

## <a name="customer-posting-profiles"></a>Debitoren-Buchungsprofile

Debitoren-Buchungsprofile ermöglichen das Zuweisen von Hauptbuchkonten und Dokumenteinstellungen zu allen Debitoren, einer Debitorengruppe oder einem bestimmten Debitor. Diese Einstellungen werden verwendet, wenn Verkaufsauftragsrechnungen, Freitextrechnungen, Projektrechnungen, Zahlungserfassungen, Mahnschreiben und Zinsrechnungen erstellt werden. 

Das Buchungsprofil wird im **Sachkonto- und Mehrwertsteuer**-Inforegister auf der **Debitorenparameterseite** definiert. Es wird dann automatisch in die Kopfzeile neuer Dokumente eingefügt. Sie können es dort ändern, wenn ein anderes Buchungsprofil erforderlich ist. 

Organisationen, die Vorauszahlungen von Kunden akzeptieren, konfigurieren häufig ein zweites Buchungsprofil für Vorauszahlungen und verknüpfen es in den Parametern als Standard-Buchungsprofil für Vorauszahlungen. Weitere Informationen finden Sie unter [Debitorenvorauszahlungen](customer-prepayments.md).

Sie können auch Buchungsdefinitionen zu Buchungsarten auf der Seite **Transaktionsbuchungsdefinitionen** zuordnen. Buchungsdefinitionen dienen statt Buchungsprofilen zum Steuern von Debitorenbuchungen auf das Hauptbuch. Weitere Informationen unter [Buchungsdefinitionen](../general-ledger/posting-definitions.md).

## <a name="creating-a-posting-profile"></a>Buchungsprofil erstellen
Hier können Sie die Sachkonten angeben, die bei Buchungen mit dem ausgewählten Buchungsprofil verwendet werden. Wählen Sie einen Kontocode und ggf. eine Konto- oder Gruppennummer für das ausgewählte Buchungsprofil aus. Während des Buchungsprozesses wird für jede Buchung das am besten geeignete Buchungsprofil gesucht. Hierzu wird nach einem möglichst spezifischen Kontocode, einer möglichst spezifischen Kontonummer oder nach einer möglichst spezifischen Kombination aus Gruppe und Nummer gesucht. Dabei gilt folgende Priorität:

| Kontocode-Feldwert | Konto-/Gruppennummer-Feldwert                | Suchpriorität |
|--------------------------|-------------------------------------------------|-----------------|
| Tabelle                    | Bestimmtes Debitorenkonto                       | 1               |
| Gruppe                    | Dem Debitor zugeordnete Debitorengruppe | 2               |
| Alle                      | Leer                                           | 3               |

Wenn alle Debitorenbuchungen das gleiche Buchungsprofil besitzen sollen, richten Sie nur ein Buchungsprofil mit der Angabe **Alle** im Feld **Kontocode** ein. Geben Sie die folgenden Werte an, um das Buchungsprofil einzurichten.

<table>
<thead>
<tr>
<th>Feld</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr>
<td>Buchungsprofil</td>
<td>Hier können Sie einen Code für das Buchungsprofil eingeben. Sie können beispielsweise zwei Buchungsprofile erstellen, um ein Konto für Debitorensaldos in der Landeswährung und ein weiteres Konto für Debitorensaldos in einer Fremdwährung zu erhalten. Das erste Konto können Sie dann mit "Landeswährung", das zweite mit "Fremdwährung" benennen.</td>
</tr>
<tr>
<td>Description</td>
<td>Geben Sie eine Beschreibung des Buchungsprofils ein. Es wird nur verwendet, um das Buchungsprofil besser zu identifizieren, wenn Sie es auf dieser Seite anzeigen.</td>
</tr>
<tr>
<td>Kontocode</td>
<td>Geben Sie an, ob sich das Buchungsprofil für einen einzelnen Debitor, für eine Debitorengruppe oder für alle Debitoren gelten soll:
<ul>
<li><b>Tabelle</b> – Das Buchungsprofil gilt für einen einzelnen Debitor. Wählen Sie das Debitorenkonto im Feld <b>Konto-/Gruppennummer</b> aus.</li>
<li><b>Gruppe</b> – Das Buchungsprofil gilt für eine Debitorengruppe. Wählen Sie das Debitorengruppe im Feld <b>Konto-/Gruppennummer</b> aus.</li>
<li><b>Alle</b> – Das Buchungsprofil gilt für alle Debitoren. Lassen Sie das<b>Konto-/Gruppennummer</b> Feld leer.</li>
</ul>
</td>
</tr>
<tr>
<td>Konto-/Gruppennummer</td>
<td>Wurde im Feld <b>Kontocode</b> die Option <b>Tabelle</b> ausgewählt, wählen Sie die Kontonummer des Debitors aus, der dem Buchungsprofil zugeordnet ist. Wurde <b>Grupe</b> ausgewählt, wählen Sie die Debitorengruppe aus. Wenn <b>Alle</b> ausgewählt wurden, lassen Sie das Feld leer.</td>
</tr>
<tr>
<td>Sammelkonto</td>
<td>Wählen Sie das Hauptkonto aus, das als Debitorenhandelskonto für die Debitoren verwendet werden soll, die dem Buchungsprofil zugeordnet sind. Dieses Konto ist das Konto für die <b>Debitorensaldo</b> Buchungsart.</td>
</tr>
<tr>
<td>Liquiditätskonto für Zahlungen</td>
<td>Wählen Sie das Liquiditätssachkonto aus, das für Cashflowplanungen verwendet wird. Dieses Feld wird nur angezeigt, wenn Cashflow-Planungen aktiviert werden.</td>
</tr>
<tr>
<td>Mehrwertsteuervorauszahlungen</td>
<td><p>Wählen Sie das Konto für die Mehrwertsteuer auf eingegangene Vorauszahlungen aus.</p>
<p><strong>Hinweis</strong>: Geben Sie auf der Seite <b>Debitorenkontenparameter</b> das Buchungsprofil an, das verwendet werden soll, wenn eine Zahlung als Vorauszahlung markiert ist.</p>
</td>
</tr>
<tr>
<td>Konto für Diskontverbindlichkeiten</td>
<td>Wählen Sie das Sachkonto für Diskontverbindlichkeiten aus.</td>
</tr>
<tr>
<td>Mahnschreibensequenz</td>
<td>Wählen Sie die Kennung der Mahnschreibensequenz aus, die für Debitoren mit dem Buchungsprofil verwendet werden soll.</td>
</tr>
<tr>
<td>Zinscode</td>
<td>Wählen Sie den Zinscode aus, der bei der Zinsberechnung für Debitoren mit dem Buchungsprofil verwendet werden soll.</td>
</tr>
</tbody>
</table>

## <a name="posting-examples"></a>Buchungsbeispiele

Die folgende Tabelle zeigt Beispiele für die Standardbuchungsarten mit beispielhaften Hauptkonten und Beschreibungen. Die Spalte **Soll/Haben** gibt an, ob die Transaktion in der Regel Soll oder Haben oder in einigen Fällen beides gebucht werden kann. Die Spalte **Clearingkonto** gibt an, dass es sich bei der Buchungsart um ein Verrechnungskonto handelt. Dies bedeutet, dass der auf diesem Konto gebuchte Betrag automatisch storniert wird, wenn eine spätere Transaktion gebucht wird. 

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontenart | Soll/Haben | Clearingkonto | Description |
|--------------|----------------------|---------------------------|--------------|--------------|------------------|-------------|
| Debitorensaldo | 130100 | Debitorenhandelskonto | Anlage | Beides | Nein | Geben Sie das Konto im Feld **Sammelkonto** an.|
| Kein | 110110 | Bankkonto | Anlage | Beides | Nein | Geben Sie das Hauptkonto im **Liquiditätskonto für Zahlungen**-Bereich an. Dieses Konto wird nicht zum Buchen verwendet. Es wird nur für die Cashflow-Prognose verwendet. |
| Mehrwertsteuervorauszahlungen | 202900 | Mehrwertsteuerüberschreibung | Passivposten | Beides | Ja | Wählen Sie das Konto für die Mehrwertsteuer auf eingegangene Vorauszahlungen aus. |
| Konto für Diskontverbindlichkeiten | 250600 | Aufgeschobene Einnahmen und Rabatte | Passivposten | Beides | Ja | Wählen Sie das Sachkonto für Diskontverbindlichkeiten aus.|     

### <a name="table-restrictions"></a>Tabelleneinschränkungen

Hier können Sie für Buchungen mit dem ausgewählten Buchungsprofil angeben, ob die Buchungen automatisch ausgeglichen werden, ob eine Zinsberechnung erfolgt und ob Mahnschreiben erstellt werden. Darüber hinaus können Sie das Konto auswählen, das beim Abschließen von Buchungen mit dem ausgewählten Buchungsprofil verwendet wird.

Geben Sie die folgenden Werte an, um das Buchungsprofil einzurichten:

| Feld                 | Beschreibung                                           |
|-----------------------|-------------------------------------------------------|
| Ausgleich        | Aktivieren Sie diese Option, um den automatischen Ausgleich von Buchungen mit diesem Buchungsprofil zu aktivieren. Wenn die Option deaktiviert ist, müssen Sie die Buchungen manuell ausgleichen, indem Sie die Seite **Offene Buchungen ausgleichen** oder **Debitorenzahlungen eingeben** verwenden. |
| Interesse          | Aktivieren Sie diese Option, wenn für Debitorenkonten mit diesem Profil Zinsen auf Außenstände berechnet werden sollen. Ist diese Option deaktiviert, werden für diese Debitoren keine Zinsen berechnet.                                           |
| Mahnschreiben | Aktivieren Sie diese Option, wenn für Debitorenkonten mit diesem Profil Mahnschreiben generiert werden sollen. Ist diese Option deaktiviert, werden für diese Debitoren keine Mahnschreiben generiert.                                                 |
| Schließen             | Wählen Sie ein Buchungsprofil aus, das geändert werden soll, wenn Buchungen mit diesem Buchungsprofil abgeschlossen werden. Eine Buchung gilt als abgeschlossen, wenn sie vollständig ausgeglichen wurde.             |



Weitere Informationen finden Sie unter [Überfällige Debitorenzahlungen](../cash-bank-management/tasks/customer-payment-overview.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
