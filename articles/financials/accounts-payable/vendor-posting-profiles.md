---
title: Kreditoren-Buchungsprofile
description: Händlerbuchungsprofile steuern die Buchung von Händlertransaktionen im Hauptbuch.
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3f62df7ec5627556561db950d54ff4347d2b4d6
ms.sourcegitcommit: ce84a1faeda6013ef6a90038d811a72f375b604e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/12/2019
ms.locfileid: "1625894"
---
# <a name="vendor-posting-profiles"></a>Kreditoren-Buchungsprofile

[!include [banner](../includes/banner.md)]

Händlerbuchungsprofile steuern die Buchung von Händlertransaktionen im Hauptbuch.

<a name="vendor-posting-profiles"></a>Kreditoren-Buchungsprofile
-----------------------

Kreditoren-Buchungsprofile ermöglichen das Zuweisen von Hauptbuch-Sachkonten und Dokumenteinstellungen zu allen Kreditoren, einer Kreditorengruppe oder einem bestimmten Kreditor. Diese Einstellungen werden verwendet, wenn Sie Bestellungen, Kreditorenrechnungen und Barzahlungen erstellen. Bei einigen Buchungen können Sie ein Buchungsprofil auswählen, das sich von auf dieser Seite für Buchungen eingerichteten Buchungsprofilen unterscheidet und Vorrang vor diesen hat. Das Buchungsprofil wird im **Sachkonto- und Mehrwertsteuer** Inforegister auf der **Kreditorenparameterseite** definiert. Das Buchungsprofil wird dann automatisch in den Kopf neuer Dokumente einbezogen. Dort können Sie es bei Bedarf zu einem anderen Buchungsprofil ändern.

Sie können auch Buchungsdefinitionen zu Buchungsarten auf der Seite **Transaktionsbuchungsdefinitionen** zuordnen. Buchungsdefinitionen dienen zum Steuern von Kreditorenbuchungen auf das Hauptbuch anstelle von Buchungsprofilen.

## <a name="creating-a-posting-profile"></a>Buchungsprofil erstellen
### <a name="setup"></a>**Einstellungen**

Hier können Sie die Sachkonten angeben, die bei Buchungen mit dem ausgewählten Buchungsprofil verwendet werden. Wählen Sie einen Kontocode und ggf. eine Konto- oder Gruppennummer für das ausgewählte Buchungsprofil aus. Während des Buchungsprozesses wird für jede Buchung das am besten geeignete Buchungsprofil gesucht. Hierzu wird nach einem möglichst spezifischen Kontocode, einer möglichst spezifischen Kontonummer oder nach einer möglichst spezifischen Kombination aus Gruppe und Nummer gesucht. Dabei gilt folgende Priorität.

| **Kontocode**-Feldwert | **Konto-/Gruppennummer**-Feldwert        | Suchpriorität |
|------------------------------|---------------------------------------------|-----------------|
| **Tabelle**                    | Bestimmtes Kreditorenkonto                     | 1               |
| **Gruppieren**                    | Kreditorengruppe, die dem Kreditor zugeordnet ist. | 2               |
| **Alle**                      | Leer                                       | 3               |

Wenn alle Kreditorenbuchungen das gleiche Buchungsprofil besitzen sollen, richten Sie nur ein Buchungsprofil mit der Angabe **Alle** im Feld **Kontocode** ein. Geben Sie die folgenden Werte an, um das Buchungsprofil einzurichten.

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
<td>Hier können Sie einen Code für das Buchungsprofil eingeben. Sie können z. B. zwei Buchungsprofile erstellen, um ein Konto für Kreditorensalden in der Landeswährung und ein weiteres Konto für Kreditorensalden in einer Fremdwährung zu erhalten. Das erste Konto können Sie dann mit "Landeswährung", das zweite mit "Fremdwährung" benennen.</td>
</tr>
<tr class="even">
<td><strong>Beschreibung</strong></td>
<td>Geben Sie eine Beschreibung des Buchungsprofils ein.</td>
</tr>
<tr class="odd">
<td><strong>Kontocode</strong></td>
<td>Geben Sie an, ob sich das Buchungsprofil auf einen bestimmten Kreditor, eine Kreditorengruppe oder alle Kreditoren bezieht:
<ul>
<li><strong>Tabelle</strong> – Das Buchungsprofil gilt für einen einzelnen Kreditor. Wählen Sie das Kreditorenkonto im Feld <strong>Konto-/Gruppennummer</strong> aus.</li>
<li><strong>Gruppe</strong> – Das Buchungsprofil gilt für eine Kreditorengruppe. Wählen Sie das Kreditorengruppe im Feld <strong>Konto-/Gruppennummer</strong> aus.</li>
<li><strong>Alle</strong> – Das Buchungsprofil gilt für alle Kreditoren. Lassen Sie das<strong>Konto-/Gruppennummer</strong> Feld leer.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Konto-/Gruppennummer</strong></td>
<td>Wurde im Feld <strong>Kontocode</strong> die Option <strong>Tabelle</strong> ausgewählt, wählen Sie die Kontonummer des Kreditors aus, der dem Buchungsprofil zugeordnet ist. Wenn Sie <strong>Gruppe</strong> ausgewählt haben, wählen Sie eine Kreditorengruppe aus. Wenn <strong>Alle</strong> ausgewählt wurden, lassen Sie das Feld leer.</td>
</tr>
<tr class="odd">
<td><strong>Sammelkonto</strong></td>
<td>Wählen Sie das Sachkonto aus, das als Sammelkonto für die Kreditoren verwendet werden soll, auf die sich das Buchungsprofil bezieht. Der Parameter <strong>Keine manuellen Eingaben zulassen</strong> für dieses Hauptkonto wird markiert. Wenn Sie anschließend das Konto vom Buchungsprofil entfernen, überprüfen Sie die Einstellung <strong>Keine manuellen Eingaben zulassen</strong>  auf der Seite <strong>Hauptkonten</strong>. 
<p><strong>HInweis</strong> Wenn die Option <strong>Buchungsdefinitionen verwenden</strong> auf der Seite <strong>Hauptbuchparameter</strong> aktiviert ist, wird die Buchungsdefinition für Kreditorenrechnungen anstatt des Sammelkontos verwendet.</p>
</td>
</tr>
<tr class="even">
<td><strong>Konto ausgleichen</strong></td>
<td>Wählen Sie das Liquiditätssachkonto aus, das für Cashflowplanungen verwendet wird. Dieses Feld ist nur verfügbar wenn Cashflowplanungen aktiviert sind.</td>
</tr>
<tr class="odd">
<td><strong>Mehrwertsteuervorauszahlungen</strong></td>
<td>Wählen Sie das Konto für die Mehrwertsteuerzahlungen aus, die vorab eingehen.
<p><strong>Hinweis</strong> Das Buchungsprofil, das verwendet wird, wenn die Zahlung im Feld <strong>Buchungsprofil</strong> mit <strong>Erfassungsbeleg für Vorauszahlung</strong> im Bereich <strong>Sachkonto und Mehrwertsteuer</strong> der <strong>Kreditorenparameterseite</strong> als Vorauszahlung gekennzeichnet ist.</p>
</td>
</tr>
<tr class="even">
<td><strong>Wareneingang</strong></td>
<td>Wählen Sie das Sachkonto aus, auf das Informationen zu nicht genehmigten Kreditorenrechnungen gebucht werden. Die Informationen werden in der Rechnungsbucherfassung erfasst. Ein Benutzer gibt z. B. grundlegende Informationen zu Kreditorenrechnungen ein, wenn diese im Rechnungsbuch eingehen. Beim Buchen des Rechnungsbuchs erfolgen die Buchungen auf dem Konto, das hier und im Feld <strong>Gegenkonto</strong> eingegeben wird. Wenn die Rechnungen genehmigt werden, wird die Verbindlichkeit aus dem Eingangskonto in das Sammelkonto des Kreditors übertragen.</td>
</tr>
<tr class="odd">
<td><strong>Gegenkonto</strong></td>
<td>Wählen Sie das Sachkonto aus, das zum Aufrechnen nicht genehmigter Kreditorenrechnungen verwendet wird, die über das Rechnungsbuch aktualisiert werden. Das Gegenkonto dient als Gegenkonto für Buchungen, die auf Eingangskonten gebucht werden. Daher enthält das Konto Kreditoreneinkäufe, die noch nicht genehmigt wurden.</td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a>**Tabelleneinschränkungen**

Hier können Sie für Buchungen mit dem ausgewählten Buchungsprofil angeben, ob die Buchungen automatisch ausgeglichen werden, ob eine Zinsberechnung erfolgt und ob Mahnschreiben erstellt werden. Darüber hinaus können Sie das Konto auswählen, das beim Abschließen von Buchungen mit dem ausgewählten Buchungsprofil verwendet wird.

Geben Sie die folgenden Werte an, um das Buchungsprofil einzurichten

| Feld          | Beschreibung                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ausgleich** | Aktivieren Sie diese Option, um den automatischen Ausgleich von Buchungen mit diesem Buchungsprofil zu aktivieren. Ist diese Option deaktiviert, müssen die Buchungen manuell mithilfe der Seite **Offene Buchungen ausgleichen** ausgeglichen werden. |
| **Stornieren**     | Aktivieren Sie diese Option, wenn Sie in der Lage sein möchten, Buchungen mit diesem Buchungsprofil zu stornieren.                                                                                                               |
| **Schließen**      | Wählen Sie ein Buchungsprofil aus, das geändert werden soll, wenn Buchungen mit diesem Buchungsprofil abgeschlossen werden. Eine Buchung gilt als abgeschlossen, wenn sie vollständig ausgeglichen wurde.                                       |
