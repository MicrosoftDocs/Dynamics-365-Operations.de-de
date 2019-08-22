---
title: Löschungsregeln
description: Dieser Artikel enthält Informationen zu Löschungsregeln und die verschiedenen Optionen für die Berichterstellung zu Löschungen.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a26c0d311191e28987f1754863140d8f755910b9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839448"
---
# <a name="elimination-rules"></a>Löschungsregeln

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Löschungsregeln und die verschiedenen Optionen für die Berichterstellung zu Löschungen.

Löschungsbuchungen sind erforderlich, wenn eine übergeordnete juristische Person Geschäftsbeziehungen mit mindestens einer Tochterfirma der juristischen Person unterhält und konsolidierte Finanzberichte verwendet. Konsolidierte Finanzaufstellungen müssen nur Buchungen enthalten, die zwischen der konsolidierten Organisation und anderer Entitäten außerhalb der Organisation auftreten. Daher müssen Buchungen zwischen juristischen Personen, die zu derselben Organisation gehören, aus dem Hauptbuch entfernt oder gelöscht werden, sodass diese nicht in Finanzberichten angezeigt werden. Es gibt mehrere Möglichkeiten, Löschungen zu melden:

-   Eine Löschungsregel kann in einem Konsolidierungs- oder Unternehmen mit Löschungseinträgen erstellt und verarbeitet werden.
-   Finanzberichterstellung kann verwendet werden, um die Beseitigungskonten und Dimensionen auf einer bestimmten Zeile oder einer Spalte anzuzeigen.
-   Eine separate juristische Person kann verwendet werden, um manuell Buchungseinträge zu buchen, um Löschungen zu verfolgen.

Dieses Thema befasst sich mit Löschungsregeln, die in einem Konsolidierungs- oder Unternehmen mit Löschungseinträgen verarbeitet werden. Sie können Löschungsregeln einrichten, um Löschungsbuchungen in einer juristischen Person zu erstellen, die als Ziel für Löschungen angegeben ist. Diese als Ziel angegebene juristische Person wird als juristische Person für Löschungen bezeichnet. Löschungserfassungen können entweder im Zuge des Konsolidierungsprozesses oder unter Verwendung eines Löschungserfassungsvorschlags generiert werden. Vor dem Einrichten von Löschungsregeln sollten Sie sich mit den folgenden Begriffen vertraut machen:

-   **Juristische Person der Quelle** – Die juristische Person, in der die gelöschten Beträge gebucht wurden.
-   **Juristische Person des Ziels** – Die juristische Person, in der die Löschungsregeln gebucht werden.
-   **Juristische Person mit Löschungseinträgen** – Die juristische Person, die als Ziel für Löschungen angegeben ist.
-   **Konsolidierte juristische Person** – Die juristische Person, die erstellt wird, um die finanziellen Ergebnisse einer Gruppe juristischer Personen zu melden. Die Finanzdaten der juristischen Personen werden in dieser juristischen Person konsolidiert. Anschließend wird anhand der kombinierten Daten ein Finanzbericht erstellt.

In der folgenden Tabelle werden die Buchungsarten aufgeführt, die möglicherweise gelöscht werden müssen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Buchungstyp</th>
<th>Beispiel:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Auftragserfassung und -fakturierung (zentralisierte Abwicklung)</td>
<td>Sie verkaufen ein Produkt an einen Debitor im Auftrag einer anderen juristischen Person Ihrer Organisation.</td>
</tr>
<tr class="even">
<td>Auftragserfassung (Intercompany/Intracompany) und Fakturierung</td>
<td>Sie verkaufen Produkte zwischen juristischen Personen in der Organisation.</td>
</tr>
<tr class="odd">
<td>Bestellungen (zentralisierte Abwicklung)</td>
<td>Sie kaufen Inventar, Material, Dienstleistungen, Anlagen und andere Produkte von einem Kreditor im Auftrag einer anderen juristischen Person Ihrer Unternehmens ein.</td>
</tr>
<tr class="even">
<td>Lagerverwaltung (Intercompany/Intracompany)</td>
<td><ul>
<li>Sie übertragen den Bestand einer juristischen Person in die Anlagen einer anderen juristischen Person Ihrer Organisation.</li>
<li>Sie übertragen den Bestand einer juristischen Person in den Bestand einer anderen juristischen Person Ihrer Organisation.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Nachverfolgung von transportiertem Lagerbestand</td>
<td>Sie übertragen Artikel zwischen Lagerorten derselben juristischen Person, aber an unterschiedlichen geografischen Standorten.</td>
</tr>
<tr class="even">
<td>Kreditoren (zentralisierte Rechungsabwicklung)</td>
<td>Sie erfassen eine Rechnung im Auftrag einer anderen juristischen Person Ihrer Organisation.</td>
</tr>
<tr class="odd">
<td>Kreditoren (zentralisierte Zahlungsabwicklung)</td>
<td>Sie zahlen eine Rechnung im Auftrag einer anderen juristischen Person Ihrer Organisation.</td>
</tr>
<tr class="even">
<td>Bargeldverwaltung und Vermögen (zentralisierte Verarbeitung)</td>
<td><ul>
<li>Sie verarbeiten Steuerzahlungen, Steuererstattungen, Zinsen, Kredite, Vorschüsse, Dividendenzahlungen und bereits bezahlten Lizenzgebühren oder Provisionen.</li>
<li>Sie zahlen Ausgabe im Auftrag einer anderen juristischen Person Ihrer Organisation. Die Rechnung wird in die Bücher der als Ziel vorgesehenen juristischen Person eingegeben und muss zwischen den juristischen Personen ausgeglichen werden. Beispielsweise zahlt eine juristische Person die Spesenabrechnung eines Mitarbeiters einer anderen juristischen Person. In diesem Fall enthält die Spesenabrechnung des Mitarbeiters Ausgaben, die einer anderen juristischen Person zugeordnet sind.</li>
<li>Sie übertragen Bargeld von einer juristischen Person zu anderen in der Organisation.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Debitoren (zentralisierte Abwicklung)</td>
<td>Sie erhalten Bargeld für die Debitorenrechnung einer anderen juristischen Person, und Sie zahlen den Scheck auf das Bankkonto dieser juristischen Person ein.</td>
</tr>
<tr class="even">
<td>Lohn (zentralisierte Abwicklung, Intercompany/Intracompany)</td>
<td><ul>
<li>Sie zahlen die Vergütung einer anderen juristischen Person. Eine juristische Person zahlt z. B. den Lohn für ihre eigenen Mitarbeiter, stellt jedoch einer anderen juristischen Person die Arbeit, die ein Mitarbeiter für diese im betreffenden Abrechnungszeitraum geleistet hat, in Rechnung. Oder ein Mitarbeiter arbeitet jeweils halbtags für die juristischen Personen A und B, und die Sozialleistungen betreffen die gesamte Bezahlung. In diesem Fall enthält der Lohn des Mitarbeiters Lohn von beiden juristischen Personen. Es werden nicht nur die Gehälter gebucht, sondern auch Steuern, Sozialleistungen, Abzüge und Rückstellungen für Gehälter.</li>
<li>Sie übertragen Arbeit von einer Abteilung oder einem Geschäftsbereich in eine/n andere/n.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Anlagen (Intercompany/Intracompany)</td>
<td>Sie übertragen Anlagen in das Anlagevermögen oder in den Bestand einer anderen juristischen Person.</td>
</tr>
<tr class="even">
<td>Umlagen (Intercompany/Intracompany)</td>
<td>Sie verarbeiten geschäftliche Umlagen. Umlagen sind Aktivitäten für ein beliebiges aufgeteiltes Konto. Das Ursprungsmodul spielt hierbei keine Rolle.</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Beispiel:
Ihre juristische Person, juristische Person A, verkauft Produkte an eine andere juristische Person in der Organisation, juristische Person B. Das folgende Beispiel veranschaulicht, wie Buchungen, die zwischen den beiden juristischen Personen vorkommen, gelöscht werden müssen:

-   Juristische Person A verkauft ein Produkt, das 10,00 kostet, für 10,00 an die juristische Person B.
-   Juristische Person A verkauft ein Produkt, das 10,00 kostet, für 10,00 an die juristische Person B plus 2,00 an tatsächlichen Versandkosten.
-   Juristische Person A verkauft ein Produkt, das 10,00 kostet, an die juristische Person B für 15,00, und realisiert beim Verkauf einen Gewinn.
-   Juristische Person A verkauft ein Produkt, das 10,00 kostet, an die juristische Person B für 15,00, und realisiert beim Verkauf die Hälfte des Gewinns. Juristische Person B realisiert beim Verkauf die andere Hälfte des Gewinns. Daher wird der Umsatzerlös geteilt. Geteilte Umsatzerlöse sind ein Anreiz, bei einer anderen juristischen Person in der Organisation zu bestellen anstatt bei einer externen Organisation.

Alle diese Buchungen erzeugen Intercompany-Buchungen, die auf Konten vom Typ "Fällig bis" und "Fällig von" ausgeführt werden. Darüber hinaus können diese Buchungen Zu- oder Abschläge für den Fall enthalten, dass der Betrag des Intercompany-Verkaufs und die Kosten der verkauften Waren nicht übereinstimmen.

## <a name="set-up-elimination-rules"></a>Sie können Löschungsregeln einrichten.
Wenn wir Löschungsregeln in Microsoft Dynamics 365 for Finance and Operations einrichten, empfehlen wir, dass Sie eine Finanzdimension speziell für Löschungszwecke erstellen. Die meisten Debitoren nennen ihn Handelspartner oder ähnlich. Wenn Sie sich entscheiden, die eine Finanzdimension nicht zu verwenden, müssen Sie darauf achten, Hauptkonten anzuzeigen, die nur für Intercompany-Buchungen bestimmt sind. 

Die Einstellung für die Löschungen wird im Aufsetzbereich des Konsolidierungsmoduls gefunden. Nachdem Sie eine Beschreibung für die Regel eingeben, müssen Sie das Unternehmen wählen, zu dem die Löschungserfassung gebucht wird. Dies sollte ein Unternehmen sein, das **Für finanziellen Löschungsprozess verwenden** in den Einstellungen für die juristische Person ausgewählt wurde. 

Sie können ein Datum nach Bedarf festlegen, an dem die Löschungsregel wirksam wird und an dem sie abläuft. Sie müssen **Aktiv** auf **Ja** setzen,  wenn Sie  möchten, dass sie im Löschungsvorschlagsprozess verfügbar sein sollen. Wählen Sie ein Journal aus, das einen Typ **Löschung**  hat.

Nachdem Sie die Grundlagen definiert haben, können Sie die tatsächlichen Verarbeitungsregeln definieren, indem Sie **Positionen** anklicken. Es gibt zwei Optionen für Löschungen, nämlich den Nettoveränderungsbetrag eliminieren oder einen festen Betrag definieren. 

Wählen Sie Ihr Quellkonto aus. Sie können Platzhalter wie Sternchen wie einen (\*) verwenden. Im Beispiel würde 1\* alle Konten auswählen, die mit 1 als Quelle für die Zuordnung der Daten beginnen. 

Nachdem Sie Ihre Quellkonten ausgewählt haben, bestimmen die **Kontospezifikation** das Konto vom Zielunternehmen, das verwendet wird. Wählen Sie **Quelle** aus, wenn Sie dasselbe Hauptkonto verwendet werden soll, das im Konto **Quelle** definiert ist. Wenn Sie auswählen **Benutzerdefiniert** auswählen, dann müssen Sie ein Zielkonto angeben. 

Die Dimensionsspezifikation funktioniert genau gleich. Wenn Sie **Quelle** auswählen, verwendet er die gleichen Dimensionen im Zielunternehmen wie im Ausgangsunternehmen. Wenn Sie **Benutzerdefiniert** auswählen, müssen Sie die Dimensionen im Zielunternehmen angeben, indem Sie auf die **Zieldimensionen** Menüoption klicken. 

Wählen Sie Quelldimensionen und Finanzdimensionen und die Werte aus, die als Quelle der Löschung verwendet werden.

## <a name="process-elimination-transactions"></a>Löschungsbuchung verarbeiten
Es gibt zwei Möglichkeiten, Löschungsbuchungen zu verarbeiten, nämlich während des Online-Konsolidierungsprozesses oder durch die Erstellung eines Löschungsjournals und mithilfe des Löschungsvorschlagsprozesses. Dieser Bereich bezieht sich auf das Erstellen der Erfassung sowie dem Betriebs der Löschungsprozesses. 

In einem Unternehmen, das als Unternehmen mit Löschungseinträgen definiert wird, wählen Sie im Konsolidierungsmodul **Löschungserfassung** aus. Klicken Sie nach Auswahl des Erfassungsnamen auf **Positionen**. Sie können den Vorschlag ausführen, indem Sie das Menü **Vorschläge** auswählen und dann  **Löschungsvorschlag löschen** auswählen.

Wählen Sie das Unternehmen, das die Quelle der konsolidierten Daten ist, und wählen Sie dann die Regel aus, die Sie bearbeiten möchten. Geben Sie ein Startdatum ein, um die Suche für Löschungsbeträge zu starten und ein Enddatum, um die Suche nach den Löschungsbeträgen zu beenden. Geben Sie im Feld **Datum für Sachkontobuchung** das Datum ein, an dem die Löschungserfassung im Hauptbuch gebucht werden soll. Klicken Sie auf **OK**, und Sie können die Beträge anzeigen und die Erfassung buchen.



