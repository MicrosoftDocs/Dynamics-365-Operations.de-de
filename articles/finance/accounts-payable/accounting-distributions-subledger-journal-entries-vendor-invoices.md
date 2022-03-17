---
title: Buchhaltungsverteilungen und Erfassungseinträge für Kreditorenrechnungen
description: Mithilfe von Buchhaltungsverteilungen wird definiert, wie ein Betrag kalkuliert wird, beispielsweise wie Ausgaben, Steuern oder Zuschläge auf einer Kreditorenrechnung kalkuliert werden. Jeder Betrag, der kalkuliert werden muss, wenn die Kreditorenrechnung journalisiert wird, enthält eine oder mehrere Buchhaltungsverteilungen.
author: sunfzam
ms.date: 02/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f10ddf113f59da4800a97a48300ab1310bfb42dd
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358180"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Buchhaltungsverteilungen und Erfassungseinträge für Kreditorenrechnungen

[!include [banner](../includes/banner.md)]

Mithilfe von Buchhaltungsverteilungen wird definiert, wie ein Betrag kalkuliert wird, beispielsweise wie Ausgaben, Steuern oder Zuschläge auf einer Kreditorenrechnung kalkuliert werden. Jeder Betrag, der kalkuliert werden muss, wenn die Kreditorenrechnung journalisiert wird, enthält eine oder mehrere Buchhaltungsverteilungen. 

## <a name="accounting-distributions"></a>Buchhaltungsverteilungen 

Sie können die folgenden Schaltflächen auf der Seite "Kreditorenrechnung" verwenden, um die Buchhaltungsverteilungen für jeden Betrag auf der Kreditorenrechnung anzuzeigen und eventuell zu ändern.
-   **Beträge verteilen** - Dient zum Anzeigen und Ändern der Buchhaltungsverteilungen für eine einzelne Position und alle untergeordneten Positionen wie Steuern oder Zuschläge. Sie können die buchhalterischen Verteilungen für die untergeordnete Zeile auch direkt über die Seite **Mehrwertsteuer-Transaktionen** oder die Seite **Belastungen-Transaktionen** einsehen und ändern.
    -   Ändern Sie Kopfzeilenbeträge von Kreditorenrechnungen wie Zuschläge oder Währungsrundungsbeträge.
    -   Ändern Sie Kreditorenrechnungspositionsbeträge.
-   **Verteilungen anzeigen** – Dient zum Anzeigen der Buchhaltungsverteilungen für alle Positionen im Dokument. Sie können die Buchhaltungsverteilungen in dieser Ansicht nicht ändern.
    -   Zeigen Sie die Kopfzeilen- und Positionsbeträge an.

Wenn die Kreditorenrechnung sich auf eine Bestellung bezieht, können Sie die Buchhaltungsverteilungen für Positionen unterteilen und ändern, die einen Artikel enthalten, der nicht gelagert ist. Wenn die Kreditorenrechnungsposition auf keine Bestellposition verweist, können Sie eine Buchhaltungsverteilung auch löschen. Sie können Positionen für Belastungen, Steuern und Positionsrabatte nicht aufteilen oder löschen. Sie können das Sachkonto ändern, aber Sie können die Beträge oder Prozentsätze nicht ändern.
> [!NOTE]                                                                                                                                 
> Wenn die übergeordnete Position einen Artikel enthält, der nicht auf Lager ist, und die Buchhaltungsverteilungen aufgeteilt werden, wird die untergeordnete Position automatisch aufgeteilt, damit sie den Finanzdimensionen der übergeordneten Position entspricht. Die Buchhaltungsverteilungen für die untergeordnete Position können nicht zusätzlich aufgeteilt oder gelöscht werden. Je nach den Einstellungen der untergeordneten Position ist es jedoch eventuell möglich, das Sachkonto für die Buchhaltungsverteilungen der untergeordneten Position zu ändern.

## <a name="distributing-amounts"></a>Beträge verteilen
Wenn Sie eine Kreditorenrechnung eingeben, wird jeder Betrag wie folgt verteilt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Typ der Kreditorenrechnungsposition</th>
<th>Prioritätsreihenfolge, die bestimmt, von wo aus das Hauptkonto angezeigt wird</th>
<th>Prioritätsreihenfolge, die bestimmt, welche standardmäßige Finanzdimension angezeigt wird</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Produkt auf Lager</td>
<td><ol>
<li>Die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Das Feld <strong>Hauptkonto</strong>, wenn „Einkaufswendungen für Produkt“ auf der Seite <strong>Buchung</strong> ausgewählt ist.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Kreidtorenrechnungsposition.</li>
</ol></td>
</tr>
<tr class="even">
<td>Eine Beschaffungskategorie oder ein nicht gelagertes Produkt</td>
<td><ol>
<li>Die Buchhaltungsverteilung für die Bestellposition, wenn die Kreditorenrechnung auf eine Bestellposition verweist.</li>
<li>Das Feld <strong>Hauptkonto</strong>, wenn „Einkaufsaufwendungen für Ausgaben“ auf der Seite <strong>Buchung</strong> ausgewählt ist.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Wenn das Hauptkonto ein Zuordnungskonto ist, verwenden Sie den Standardwert der Zuweisungskontodefinition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Kreidtorenrechnungsposition.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite <strong>Kontenplan</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Anlage</td>
<td><ol>
<li>Die Buchhaltungsverteilung für die Bestellposition, wenn die Kreditorenrechnung auf eine Bestellposition verweist.</li>
<li>Wenn <strong>Zugang</strong> im Feld <strong>Transaktionsart</strong> auf der Seite <strong>Lieferantenrechnung</strong> ausgewählt ist, das Feld <strong>Hauptkonto</strong>, wenn <strong>Zugang</strong> auf der Seite <strong>Anlagenbuchungsprofile</strong> ausgewählt ist.</li>
<li>Wenn <strong>Akquisitionsanpassung</strong> im Feld <strong>Transaktionsart</strong> ausgewählt ist, wird das Feld <strong>Hauptkonto</strong>, wenn <strong>Akquisitionsanpassung</strong> auf der Seite <strong>Anlagenbuchungsprofile</strong> ausgewählt ist.</li>
</ol></td>
<td><ol>
<li>Verwenden Sie die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite <strong>Kontenplan</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Das Projekt, das in der Kreditorenrechnungsposition definiert ist</td>
<td><ol>
<li>Die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</li>
<li>Wenn <strong>Saldo</strong> im Feld <strong>Kosten buchen – Artikel</strong> auf der Seite <strong>Projektgruppen</strong> ausgewählt ist, das Feld <strong>Hauptkonto</strong>, wenn <strong>Kosten</strong> auf der Seite <strong>Sachkontobuchungseinstellungen</strong> ausgewählt ist.</li>
<li>Wenn <strong>Gewinn und Verlust</strong> im Feld <strong>Kosten buchen – Artikel</strong> auf der Seite <strong>Projektgruppen</strong> ausgewählt ist, das Feld <strong>Hauptkonto</strong>, wenn <strong>Kosten – Artikel</strong> auf der Seite <strong>Sachkontobuchungseinstellungen</strong> ausgewählt ist.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Positionsrabatt</td>
<td><ol>
<li>Die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</li>
<li>Das Feld <strong>Hauptkonto</strong>, wenn <strong>Rabatt</strong> auf der Seite <strong>Buchung</strong> ausgewählt ist.</li>
<li>Wenn ein Hauptkonto im Buchungsprofil nicht definiert ist, die Buchhaltungsverteilung des erweiterten Preises in der Bestellposition.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Verwenden Sie die Finanzdimensionen aus den Buchhaltungsverteilungen für den erweiterten Preis in der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die Finanzdimensionswerte für die Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite <strong>Kontenplan</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>„Einkaufskosten“, die auf der Registerkarte <strong>Preis und Rabatt</strong> der Bestellposition eingegeben wird</td>
<td><ol>
<li>Die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</li>
<li>Die Buchhaltungsverteilung des erweiterten Preises in der Bestellposition.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Verwenden Sie die Finanzdimensionen aus den Buchhaltungsverteilungen für den erweiterten Preis in der Kreditorenrechnungsposition.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Positionszuschlag</td>
<td><ol>
<li>Die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</li>
<li>Wenn <strong>Sachkonto</strong> im Feld <strong>Belastungsart</strong> auf der Seite <strong>Gebührencode</strong> ausgewählt ist, das Feld <strong>Sachkonto</strong> auf der Seite <strong>Gebührencode</strong>.</li>
<li>Wenn <strong>Element</strong> im Feld <strong>Belastungsart</strong> auf der Seite <strong>Belastungscode</strong> ausgewählt ist, wird die Buchhaltungsverteilung für den erweiterten Preis auf der Bestellzeile angezeigt.</li>
<li>Wenn <strong>Kunde/Lieferant</strong> im Feld <strong>Belastungstyp</strong> auf der Seite <strong>Rechnungscode</strong> ausgewählt ist, das Feld <strong>Kreditkonto</strong> auf der Seite <strong>Rechnungscode</strong>.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Verwenden Sie die Finanzdimensionen aus den Buchhaltungsverteilungen für den erweiterten Preis in der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite <strong>Kontenplan</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Steuer, mit der folgenden Bedingung:
<ul>
<li>Die Option <strong>U.S. Besteuerungsregeln anwenden</strong> ist auf der Seite <strong>Hauptbuch Parameter</strong> aktiviert.</li>
</ul></td>
<td><ol>
<li>Die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</li>
<li>Die Buchhaltungsverteilungen für den erweiterten Preis oder die Belastung.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Verwenden Sie die Finanzdimensionen aus den Buchhaltungsverteilungen für den erweiterten Preis in der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Steuer, mit den folgenden Bedingungen:
<ul>
<li>Die Option <strong>U.S. Besteuerungsregeln anwenden</strong> ist auf der Seite <strong>Parameter für das Hauptbuch</strong> deaktiviert.</li>
<li>Das Feld <strong>Verbrauchssteuer</strong> für die Mehrwertsteuergruppe wird auf der Seite <strong>Mehrwertsteuergruppen</strong> deaktiviert.</li>
</ul></td>
<td><ol>
<li>Wenn der Steuerbetrag wiederherstellbar ist, das Feld <strong>Vorsteuer</strong> auf der Seite <strong>Sachkontobuchungsgruppen</strong>.</li>
<li>Wenn der Steuerbetrag nicht erstattungsfähig ist, der erweiterte Preis oder die Buchhaltungsverteilung für die Belastung.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Verwenden Sie die Finanzdimensionen aus dem erweiterten Preis oder der Buchhaltungsverteilung für die Belastung in der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite <strong>Kontenplan</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Steuer, mit den folgenden Bedingungen:
<ul>
<li>Die Option „US-Steuerregeln anwenden“ wird auf der Seite <strong>Hauptbuchparameter</strong> deaktiviert.</li>
<li>Das Feld <strong>Verbrauchssteuer</strong> für die Mehrwertsteuergruppe wird auf der Seite <strong>Mehrwertsteuergruppen</strong> ausgewählt.</li>
</ul></td>
<td><ol>
<li>Wenn der Steuerbetrag wiederherstellbar ist, das Feld <strong>Vorsteuer</strong> auf der Seite <strong>Sachkontobuchungsgruppen</strong>.</li>
<li>Wenn der Steuerbetrag nicht wiederherstellbar ist, das Feld <strong>Verbrauchssteuerausgaben</strong> auf der Seite <strong>Sachkontobuchungsgruppen</strong>.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Verwenden Sie die Finanzdimensionen aus dem erweiterten Preis oder der Buchhaltungsverteilung für die Belastung in der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite <strong>Kontenplan</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kopfgebühr</td>
<td><ol>
<li>Wenn <strong>Sachkonto</strong> im Feld <strong>Belastungstyp</strong> auf der Seite <strong>Belastungscode</strong> ausgewählt ist, das Feld <strong>Belastungskonto</strong> auf der Seite <strong>Belastungscode</strong>.</li>
<li>Wenn <strong>Kunde/Lieferant</strong> im Feld <strong>Belastungstyp</strong> auf der Seite <strong>Rechnungscode</strong> ausgewählt ist, das Feld <strong>Kreditkonto</strong> auf der Seite <strong>Rechnungscode</strong>.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Wenn das Hauptkonto ein Zuordnungskonto ist, verwenden Sie den Standardwert der Zuweisungskontodefinition.</li>
<li>Verwenden Sie die Finanzdimensionsstandardvorlagewerte aus dem Kreditorenrechnungskopf.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite <strong>Kontenplan</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Kopfrabatt</td>
<td><ol>
<li>Das Feld <strong>Hauptkonto</strong> für die <strong>Buchungsart Kreditorenrechnungsrabatt</strong> auf der Seite <strong>Konten für automatische Buchungen</strong>.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Verwenden Sie die Finanzdimensionen aus den Buchhaltungsverteilungen für den erweiterten Preis in der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite <strong>Kontenplan</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a>Verteilen von Steuern

Buchhaltungsverteilungen für Steuern können erst erstellt werden, nachdem Steuern berechnet wurden. Um die Mehrwertsteuer zu berechnen, müssen Sie eine der folgenden Aufgaben auf der Seite **Lieferantenrechnung** ausführen:
-   Zeigen Sie die Rechnungssumme an.
-   Zeigen Sie den Mehrwertsteuercode an.
-   Zeigen Sie die Erfassung im untergeordneten Sachkonto an.
-   Zeigen Sie die Ansichtsbuchhaltungsverteilungen für die vollständige Kreditorenrechnung an.
-   Sperren Sie die Kreditorenrechnung.
-   Buchen Sie die Kreditorenrechnung.

## <a name="subledger-journals-for-vendor-invoices"></a>Untergeordnete Sachkonten für Kreditorenrechnungen
Bevor Sie eine Kreditorenrechnung buchen, können Sie den vollständigen Buchhaltungseintrag der Rechnung anzeigen, der Soll- und Habenbeträge enthält, um sicherzustellen, dass die Rechnung auf die richtigen Konten gebucht wird. Diese Ansicht des vollständigen Buchhaltungseintrags wird als Erfassung im untergeordneten Sachkonto bezeichnet. 

Wenn der Erfassungseintrag im untergeordneten Sachkonto falsch ist, wenn Sie ihn in der Vorschau anzeigen, bevor Sie die Kreditorenrechnung journalisieren, können Sie den Erfassungseintrag im untergeordneten Sachkonto nicht ändern. Stattdessen müssen Sie die Buchhaltungsverteilungen oder das Buchungsprofil ändern. Die Buchhaltungsverteilungen dienen dazu, eine Seite des Buchhaltungseintrags, der Soll- oder Habenbetrag, zu definieren. Der Ausgleichskontoeintrag in der Erfassung im untergeordneten Sachkonto wird aus den Buchungsprofilen erstellt, beispielsweise aus dem Kreditorenkonto oder der Steuer.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
