---
title: Buchhaltungsverteilungen und Erfassungseinträge im untergeordneten Sachkonto für Kreditorenrechnungen
description: Mithilfe von Buchhaltungsverteilungen wird definiert, wie ein Betrag kalkuliert wird, beispielsweise wie Ausgaben, Steuern oder Zuschläge auf einer Kreditorenrechnung kalkuliert werden. Jeder Betrag, der kalkuliert werden muss, wenn die Kreditorenrechnung journalisiert wird, enthält eine oder mehrere Buchhaltungsverteilungen.
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8e38e6a571bb7f08b32548bcb4af823807a4340
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177989"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a>Buchhaltungsverteilungen und Erfassungseinträge im untergeordneten Sachkonto für Kreditorenrechnungen

[!include [banner](../includes/banner.md)]

Mithilfe von Buchhaltungsverteilungen wird definiert, wie ein Betrag kalkuliert wird, beispielsweise wie Ausgaben, Steuern oder Zuschläge auf einer Kreditorenrechnung kalkuliert werden. Jeder Betrag, der kalkuliert werden muss, wenn die Kreditorenrechnung journalisiert wird, enthält eine oder mehrere Buchhaltungsverteilungen. 

<a name="accounting-distributions"></a>Buchhaltungsverteilungen 
-------------------------

Sie können die folgenden Schaltflächen auf der Seite "Kreditorenrechnung" verwenden, um die Buchhaltungsverteilungen für jeden Betrag auf der Kreditorenrechnung anzuzeigen und eventuell zu ändern.
-   **Beträge verteilen** - Dient zum Anzeigen und Ändern der Buchhaltungsverteilungen für eine einzelne Position und alle untergeordneten Positionen wie Steuern oder Zuschläge. Sie können auch die Buchhaltungsverteilungen für die untergeordnete Position direkt von der Seite "Mehrwertsteuerbuchungen" oder der Seite "Belastungsbuchungen" aus anzeigen und ändern.
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
<li>Das Feld "Hauptkonto", wenn "Einkaufswendungen für Produkt" auf der Seite "Buchung" ausgewählt ist.</li>
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
<li>Das Feld "Hauptkonto", wenn "Einkaufsaufwendungen für Ausgaben" auf der Seite "Buchung" ausgewählt ist.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Wenn das Hauptkonto ein Zuordnungskonto ist, verwenden Sie den Standardwert der Zuweisungskontodefinition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Kreidtorenrechnungsposition.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</li>
</ol></td>
</tr>
<tr class="odd">
<td>Anlagen</td>
<td><ol>
<li>Die Buchhaltungsverteilung für die Bestellposition, wenn die Kreditorenrechnung auf eine Bestellposition verweist.</li>
<li>Wenn "Anschaffung" im Feld "Buchungsart" im Formular "Kreditorenrechnung" ausgewählt ist, das Feld "Hauptkonto", wenn "Anschaffung" auf der Seite "Anlagenbuchungsprofile" ausgewählt ist.</li>
<li>Wenn "Anschaffungsänderung" im Feld "Buchungsart" ausgewählt ist, das Feld "Hauptkonto", wenn "Anschaffungsänderung" auf der Seite "Anlagenbuchungsprofile" ausgewählt ist.</li>
</ol></td>
<td><ol>
<li>Verwenden Sie die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</li>
</ol></td>
</tr>
<tr class="even">
<td>Das Projekt, das in der Kreditorenrechnungsposition definiert ist</td>
<td><ol>
<li>Die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</li>
<li>Wenn "Saldo" im Feld "Kosten buchen - Artikel" auf der Seite "Projektgruppen" ausgewählt ist, das Feld "Hauptkonto", wenn "Kosten" auf der Seite "Sachkontobuchungseinstellungen" ausgewählt ist.</li>
<li>Wenn "Gewinn und Verlust" im Feld "Kosten buchen - Artikel" auf der Seite "Projektgruppen" ausgewählt ist, das Feld "Hauptkonto", wenn "Kosten - Artikel" auf der Seite "Sachkontobuchungseinstellungen" ausgewählt ist.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Positionsrabatt</td>
<td><ol>
<li>Die Buchhaltungsverteilung für die Bestellposition, wenn die Rechnungsposition auf eine Bestellposition verweist.</li>
<li>Das Feld "Hauptkonto", wenn "Rabatt" auf der Seite "Buchung" ausgewählt ist.</li>
<li>Wenn ein Hauptkonto im Buchungsprofil nicht definiert ist, die Buchhaltungsverteilung des erweiterten Preises in der Bestellposition.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Verwenden Sie die Finanzdimensionen aus den Buchhaltungsverteilungen für den erweiterten Preis in der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die Finanzdimensionswerte für die Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</li>
</ol></td>
</tr>
<tr class="even">
<td>"Einkaufskosten", das auf der Registerkarte "Preis und Rabatt" der Bestellposition eingegeben wird</td>
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
<li>Wenn "Sachkonto" im Feld "Solltyp" im Formular "Belastungscode" ausgewählt ist, das Feld "Sollkonto" auf der Seite "Belastungscode".</li>
<li>Wenn "Artikel" im Feld "Solltyp" im Formular "Belastungscode" ausgewählt ist, die Buchhaltungsverteilung für den erweiterten Preis in der Bestellposition.</li>
<li>Wenn "Debitor/Kreditor" im Feld "Solltyp" im Formular "Belastungscode" ausgewählt ist, das Feld "Habenkonto" auf der Seite "Belastungscode".</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Verwenden Sie die Finanzdimensionen aus den Buchhaltungsverteilungen für den erweiterten Preis in der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</li>
</ol></td>
</tr>
<tr class="even">
<td>Steuer, mit der folgenden Bedingung:
<ul>
<li>Die Option "US-Steuerregeln anwenden" ist auf der Seite "Hauptbuchparameter" ausgewählt.</li>
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
<li>Die Option "US-Steuerregeln anwenden" wird auf der Seite "Hauptbuchparameter" deaktiviert.</li>
<li>Das Feld "Verbrauchssteuer (USA)" für die Mehrwertsteuergruppe wird auf der Seite "Mehrwertsteuergruppen" deaktiviert.</li>
</ul></td>
<td><ol>
<li>Wenn der Steuerbetrag wiederherstellbar ist, das Feld "Vorsteuer" auf der Seite "Sachkontobuchungsgruppen".</li>
<li>Wenn der Steuerbetrag nicht erstattungsfähig ist, der erweiterte Preis oder die Buchhaltungsverteilung für die Belastung.</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Verwenden Sie die Finanzdimensionen aus dem erweiterten Preis oder der Buchhaltungsverteilung für die Belastung in der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</li>
</ol></td>
</tr>
<tr class="even">
<td>Steuer, mit den folgenden Bedingungen:
<ul>
<li>Die Option "US-Steuerregeln anwenden" wird auf der Seite "Hauptbuchparameter" deaktiviert.</li>
<li>Das Feld "Verbrauchssteuer (USA)" für die Mehrwertsteuergruppe wird auf der Seite "Mehrwertsteuergruppen" ausgewählt.</li>
</ul></td>
<td><ol>
<li>Wenn der Steuerbetrag wiederherstellbar ist, das Feld "Vorsteuer" auf der Seite "Sachkontobuchungsgruppen".</li>
<li>Wenn der Steuerbetrag nicht wiederherstellbar ist, das Feld "Verbrauchssteuerausgaben (USA)" auf der Seite "Sachkontobuchungsgruppen".</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Verwenden Sie die Finanzdimensionen aus dem erweiterten Preis oder der Buchhaltungsverteilung für die Belastung in der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kopfgebühr</td>
<td><ol>
<li>Wenn "Sachkonto" im Feld "Solltyp" im Formular "Belastungscode" ausgewählt ist, das Feld "Sollkonto" auf der Seite "Belastungscode".</li>
<li>Wenn "Debitor/Kreditor" im Feld "Solltyp" im Formular "Belastungscode" ausgewählt ist, das Feld "Habenkonto" auf der Seite "Belastungscode".</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Wenn das Hauptkonto ein Zuordnungskonto ist, verwenden Sie den Standardwert der Zuweisungskontodefinition.</li>
<li>Verwenden Sie die Finanzdimensionsstandardvorlagewerte aus dem Kreditorenrechnungskopf.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</li>
</ol></td>
</tr>
<tr class="even">
<td>Kopfrabatt</td>
<td><ol>
<li>Das Feld "Hauptkonto" für die Buchungsart "Kreditorenrechnungsrabatt" auf der Seite "Konten für automatische Buchungen".</li>
</ol></td>
<td><ol>
<li>Wenn die Rechnungsposition auf eine Bestellposition verweist, verwenden Sie die Buchhaltungsverteilung für die Bestellposition.</li>
<li>Verwenden Sie die Finanzdimensionen aus den Buchhaltungsverteilungen für den erweiterten Preis in der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die Finanzdimensionswerte der Kreditorenrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Hauptkonto auf der Seite "Kontenplan".</li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a>Verteilen von Steuern
------------------

Buchhaltungsverteilungen für Steuern können erst erstellt werden, nachdem Steuern berechnet wurden. Zum Berechnen der Mehrwertsteuer müssen Sie auf der Seite "Kreditorenrechnung" eine der folgenden Aufgaben ausführen:
-   Zeigen Sie die Rechnungssumme an.
-   Zeigen Sie den Mehrwertsteuercode an.
-   Zeigen Sie die Erfassung im untergeordneten Sachkonto an.
-   Zeigen Sie die Ansichtsbuchhaltungsverteilungen für die vollständige Kreditorenrechnung an.
-   Sperren Sie die Kreditorenrechnung.
-   Buchen Sie die Kreditorenrechnung.

## <a name="subledger-journals-for-vendor-invoices"></a>Untergeordnete Sachkonten für Kreditorenrechnungen
Bevor Sie eine Kreditorenrechnung buchen, können Sie den vollständigen Buchhaltungseintrag der Rechnung anzeigen, der Soll- und Habenbeträge enthält, um sicherzustellen, dass die Rechnung auf die richtigen Konten gebucht wird. Diese Ansicht des vollständigen Buchhaltungseintrags wird als Erfassung im untergeordneten Sachkonto bezeichnet. 

Wenn der Erfassungseintrag im untergeordneten Sachkonto falsch ist, wenn Sie ihn in der Vorschau anzeigen, bevor Sie die Kreditorenrechnung journalisieren, können Sie den Erfassungseintrag im untergeordneten Sachkonto nicht ändern. Stattdessen müssen Sie die Buchhaltungsverteilungen oder das Buchungsprofil ändern. Die Buchhaltungsverteilungen dienen dazu, eine Seite des Buchhaltungseintrags, der Soll- oder Habenbetrag, zu definieren. Der Ausgleichskontoeintrag in der Erfassung im untergeordneten Sachkonto wird aus den Buchungsprofilen erstellt, beispielsweise aus dem Kreditorenkonto oder der Steuer.





