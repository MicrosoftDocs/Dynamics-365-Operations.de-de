---
title: Debitoren-Buchungsprofile
description: Kundenbuchungsprofile steuern die Buchungen von Kundentransaktionen im Hauptbuch.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ccd663a769aa98afb800f6fcd6217f39bb513597
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="customer-posting-profiles"></a>Debitoren-Buchungsprofile

[!include[banner](../includes/banner.md)]


Kundenbuchungsprofile steuern die Buchungen von Kundentransaktionen im Hauptbuch.

<a name="customer-posting-profiles"></a>Debitoren-Buchungsprofile
-------------------------

Debitoren-Buchungsprofile ermöglichen das Zuweisen von Hauptbuchkonten und Dokumenteinstellungen zu allen Debitoren, einer Debitorengruppe oder einem bestimmten Debitor. Diese Einstellungen werden verwendet, wenn Aufträge, Freitextrechnungen, Barzahlungen, Mahnschreiben und Zinsrechnungen erstellen werden. Bei einigen Buchungen können Sie ein Buchungsprofil auswählen, das sich von den in diesem Formular für Buchungen eingerichteten Buchungsprofilen unterscheidet und Vorrang vor diesen hat. 

Das Buchungsprofil wird im Sachkonto- und Mehrwertsteuer-Inforegister auf der Debitorenparameterseite definiert. Das Buchungsprofil wird dann automatisch in den Kopf neuer Dokumente einbezogen. Dort können es bei Bedarf zu einem anderen Buchungsprofil ändern.

Sie können auch Buchungsdefinitionen zu Buchungsarten auf der Seite "Transaktionsbuchungsdefinitionen" zuordnen. Buchungsdefinitionen dienen zum Steuern von Debitorenbuchungen auf das Hauptbuch anstelle von Buchungsprofilen.

## <a name="creating-a-posting-profile"></a>Buchungsprofil erstellen
Hier können Sie die Sachkonten angeben, die bei Buchungen mit dem ausgewählten Buchungsprofil verwendet werden. Wählen Sie einen Kontocode und ggf. eine Konto- oder Gruppennummer für das ausgewählte Buchungsprofil aus. Während des Buchungsprozesses wird für jede Buchung das am besten geeignete Buchungsprofil gesucht. Hierzu wird nach einem möglichst spezifischen Kontocode, einer möglichst spezifischen Kontonummer oder nach einer möglichst spezifischen Kombination aus Gruppe und Nummer gesucht. Dabei gilt folgende Priorität:

| **Kontocode**-Feldwert | **Konto-/Gruppennummer**-Feldwert            | Suchpriorität |
|------------------------------|-------------------------------------------------|-----------------|
| **Tabelle**                    | Bestimmtes Debitorenkonto                       | 1               |
| **Gruppe**                    | Dem Debitor zugeordnete Debitorengruppe | 2               |
| **Alle**                      | Leer                                           | 3               |

Wenn alle Debitorenbuchungen das gleiche Buchungsprofil besitzen sollen, richten Sie nur ein Buchungsprofil mit der Angabe "Alle" im Feld "Kontocode" ein. Geben Sie die folgenden Werte an, um das Buchungsprofil einzurichten:

<table>
<thead>
<tr class="header">
<th>Feld</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Buchungsprofil</strong></td>
<td>Hier können Sie einen Code für das Buchungsprofil eingeben. Sie können beispielsweise zwei Buchungsprofile erstellen, um ein Konto für Debitorensaldos in der Landeswährung und ein weiteres Konto für Debitorensaldos in einer Fremdwährung zu erhalten. Das erste Konto können Sie dann mit "Landeswährung", das zweite mit "Fremdwährung" benennen.</td>
</tr>
<tr class="even">
<td><strong>Beschreibung</strong></td>
<td>Geben Sie eine Beschreibung des Buchungsprofils ein. Es wird nur verwendet, um das Buchungsprofil besser zu identifizieren, wenn Sie es auf dieser Seite anzeigen.</td>
</tr>
<tr class="odd">
<td><strong>Kontocode</strong></td>
<td>Geben Sie an, ob sich das Buchungsprofil für einen einzelnen Debitor, für eine Debitorengruppe oder für alle Debitoren gelten soll:
<ul>
<li><strong>Tabelle</strong> – Das Buchungsprofil gilt für einen einzelnen Debitor. Wählen Sie das Debitorenkonto im Feld 'Konto-/Gruppennummer' aus.</li>
<li><strong>Gruppe</strong> – Das Buchungsprofil gilt für eine Debitorengruppe. Wählen Sie das Debitorengruppe im Feld 'Konto-/Gruppennummer' aus.</li>
<li><strong>Alle</strong> – Das Buchungsprofil gilt für alle Debitoren. Lassen Sie die "Konto-/Gruppennummer"-Feld leer.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Konto-/Gruppennummer</strong></td>
<td>Wurde im Feld "Kontocode" die Option "Tabelle" ausgewählt, wählen Sie die Kontonummer des Debitors aus, der dem Buchungsprofil zugeordnet ist. Wurde "Grupe" ausgewählt, wählen Sie die Debitorengruppe aus. Wurde "Alle" ausgewählt, lassen Sie das Feld leer.</td>
</tr>
<tr class="odd">
<td><strong>Sammelkonto</strong></td>
<td>Wählen Sie das Sachkonto aus, das als Debitorensammelkonto für die Debitoren verwendet werden soll, die dem Buchungsprofil zugeordnet sind.</td>
</tr>
<tr class="even">
<td><strong>Konto ausgleichen</strong></td>
<td>Wählen Sie das Liquiditätssachkonto aus, das für Cashflowplanungen verwendet wird. Dieses Feld wird nur angezeigt, wenn Cashflow-Planungen aktiviert werden.</td>
</tr>
<tr class="odd">
<td><strong>Mehrwertsteuervorauszahlungen</strong></td>
<td>Wählen Sie das Konto für die Mehrwertsteuer auf eingegangene Vorauszahlungen aus.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Hinweis" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Hinweis</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Geben Sie auf der Seite "Debitorenkontenparameter" das Buchungsprofil an, das verwendet werden soll, wenn eine Zahlung als Vorauszahlung markiert ist.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Konto für Diskontverbindlichkeiten</strong></td>
<td>Wählen Sie das Sachkonto für Diskontverbindlichkeiten aus.</td>
</tr>
<tr class="odd">
<td><strong>Mahnschreibensequenz</strong></td>
<td>Wählen Sie die Kennung der Mahnschreibensequenz aus, die für Debitoren mit dem Buchungsprofil verwendet werden soll.</td>
</tr>
<tr class="even">
<td><strong>Zinscode</strong></td>
<td>Wählen Sie den Zinscode aus, der bei der Zinsberechnung für Debitoren mit dem Buchungsprofil verwendet werden soll.</td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a>**Tabelleneinschränkungen**

Hier können Sie für Buchungen mit dem ausgewählten Buchungsprofil angeben, ob die Buchungen automatisch ausgeglichen werden, ob eine Zinsberechnung erfolgt und ob Mahnschreiben erstellt werden. Darüber hinaus können Sie das Konto auswählen, das beim Abschließen von Buchungen mit dem ausgewählten Buchungsprofil verwendet wird.

Geben Sie die folgenden Werte an, um das Buchungsprofil einzurichten:

| Feld                 | Beschreibung                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ausgleich**        | Aktivieren Sie diese Option, um den automatischen Ausgleich von Buchungen mit diesem Buchungsprofil zu aktivieren. Wenn die Option deaktiviert ist, müssen Sie die Buchungen manuell ausgleichen, indem Sie die Seite "Offene Buchungen ausgleichen" oder "Debitorenzahlungen eingeben" verwenden. |
| **Interesse**          | Aktivieren Sie diese Option, wenn für Debitorenkonten mit diesem Profil Zinsen auf Außenstände berechnet werden sollen. Ist diese Option deaktiviert, werden für diese Debitoren keine Zinsen berechnet.                                           |
| **Mahnschreiben** | Aktivieren Sie diese Option, wenn für Debitorenkonten mit diesem Profil Mahnschreiben generiert werden sollen. Ist diese Option deaktiviert, werden für diese Debitoren keine Mahnschreiben generiert.                                                 |
| **Schließen**             | Wählen Sie ein Buchungsprofil aus, das geändert werden soll, wenn Buchungen mit diesem Buchungsprofil abgeschlossen werden. Eine Buchung gilt als abgeschlossen, wenn sie vollständig ausgeglichen wurde.                                                                           |



Weitere Informationen finden Sie unter [Überfällige Debitorenzahlungen](../cash-bank-management/tasks/customer-payment-overview.md).


