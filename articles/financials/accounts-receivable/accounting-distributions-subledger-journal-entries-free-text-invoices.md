---
title: "Buchhaltungsverteilungen und Erfassungseinträge im untergeordneten Sachkonto für Freitextrechnungen"
description: "Mithilfe von Buchhaltungsverteilungen wird definiert, wie ein Betrag kalkuliert wird, beispielsweise wie Umsatzerlöse, Steuern oder Zuschläge auf einer Freitextrechnung kalkuliert werden. Jeder Betrag, der kalkuliert werden muss, wenn die Freitextrechnung journalisiert wird, enthält eine oder mehrere Buchhaltungsverteilungen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6485642d27156dfb37f9e30335369e3287f92148
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a>Buchhaltungsverteilungen und Erfassungseinträge im untergeordneten Sachkonto für Freitextrechnungen

[!include[banner](../includes/banner.md)]


Mithilfe von Buchhaltungsverteilungen wird definiert, wie ein Betrag kalkuliert wird, beispielsweise wie Umsatzerlöse, Steuern oder Zuschläge auf einer Freitextrechnung kalkuliert werden. Jeder Betrag, der kalkuliert werden muss, wenn die Freitextrechnung journalisiert wird, enthält eine oder mehrere Buchhaltungsverteilungen.

<a name="accounting-distributions"></a>Buchhaltungsverteilungen
------------------------

Sie können die folgenden Schaltflächen auf der Seite "Freitextrechnung" verwenden, um die Buchhaltungsverteilungen für jeden Betrag auf der Freitextrechnung anzuzeigen und eventuell zu ändern.

-   **Beträge verteilen**– Dient zum Anzeigen und Ändern der Buchhaltungsverteilungen für eine einzelne Position und alle untergeordneten Positionen wie Steuern oder Belastungen. Sie können auch die Buchhaltungsverteilungen für die untergeordnete Position direkt von der Seite "Mehrwertsteuerbuchungen" oder der Seite "Belastungsbuchungen" aus anzeigen und ändern.
    -   Ändern Sie Kopfzeilenbeträge von Freitextrechnungen wie Zuschläge oder Währungsrundungsbeträge.
    -   Ändern von Freitextrechnungpositionsbeträgen.
-   **Verteilungen anzeigen** – Dient zum Anzeigen der Buchhaltungsverteilungen für alle Positionen im Dokument. Sie können die Buchhaltungsverteilungen in dieser Ansicht nicht ändern.
    -   Zeigen Sie die Kopfzeilen- und Positionsbeträge an.

## <a name="distributing-amounts"></a>Beträge verteilen
Wenn Sie eine Freitextrechnung eingeben, wird jeder Betrag wie folgt verteilt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Typ des Geldbetrags</th>
<th>Wo das Hauptkonto angezeigt wird</th>
<th>Prioritätsreihenfolge, die bestimmt, welche standardmäßige Finanzdimension angezeigt wird</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Freitextrechnungsposition</td>
<td>Das Sachkonto in der Freitextrechnungsposition</td>
<td><ol>
<li>Wenn das Hauptkonto ein Zuordnungskonto ist, verwenden Sie den Standardwert der Zuweisungskontodefinition.</li>
<li>Wenn das Hauptkonto kein Zuweisungskonto ist, verwenden Sie die Standardvorlage für Finanzdimensionen in der Freitextrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Freitextrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Sachkonto auf der Seite "Kontenplan".</li>
</ol></td>
</tr>
<tr class="even">
<td>Freitextrechnungsposition für eine Kombination aus Anlagennummer und Wertmodell
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Hinweis </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Das Hauptkonto in der Freitextrechnungsposition ist das Anlagenveräußerungskonto.</td>
</tr>
</tbody>
</table>
</div></td>
<td>Das Sachkonto in der Freitextrechnungsposition</td>
<td><ol>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Freitextrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Sachkonto auf der Seite "Kontenplan".</li>
</ol></td>
</tr>
<tr class="odd">
<td>Rabattbetrag der Freitextrechnung</td>
<td>Das Feld "Hauptkonto für Debitorenrabatte" auf der Skonti Seite.</td>
<td><ol>
<li>Wenn das Hauptkonto ein Zuordnungskonto ist, verwenden Sie den Standardwert der Zuweisungskontodefinition.</li>
<li>Wenn das Hauptkonto kein Zuweisungskonto ist, verwenden Sie die Standardvorlage für Finanzdimensionen in der Freitextrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Freitextrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Sachkonto auf der Seite "Kontenplan".</li>
</ol></td>
</tr>
<tr class="even">
<td>Mehrwertsteuerbetrag der Freitextrechnung</td>
<td>Das Feld Mehrwertsteuer in der Sachkontobuchungsgruppenseite.</td>
<td><ol>
<li>Verwenden Sie die Finanzdimensionen, die im Freitextrechnungspositionsbetrag oder den Verteilungen für den Positionsbetrag der Zuschläge definiert sind.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Freitextrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Sachkonto auf der Seite "Kontenplan".</li>
</ol></td>
</tr>
<tr class="odd">
<td>Positionsbetrag der Zuschläge der Freitextrechnung</td>
<td>Das Habenkontofeld in der Belastungscodeseite.</td>
<td><ol>
<li>Wenn das Hauptkonto ein Zuordnungskonto ist, verwenden Sie den Standardwert der Zuweisungskontodefinition.</li>
<li>Wenn das Hauptkonto kein Zuweisungskonto ist, verwenden Sie die Standardvorlage für Finanzdimensionen in der Freitextrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte in der Freitextrechnungsposition.</li>
<li>Verwenden Sie die standardmäßigen Finanzdimensionswerte aus dem Sachkonto auf der Seite "Kontenplan".</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>Verteilen von Steuern
Buchhaltungsverteilungen für Steuern können erst erstellt werden, nachdem Steuern berechnet wurden. Zum Berechnen der Mehrwertsteuer müssen Sie auf der Seite "Freitextrechnung" eine der folgenden Aufgaben ausführen:
-   Zeigen Sie den Mehrwertsteuercode an.
-   Zeigen Sie die Rechnungssumme an.
-   Zeigen Sie den Cashflow an.
-   Zeigen Sie die Buchhaltungsverteilungen für die gesamte Freitextrechnung an.
-   Zeigen Sie die Erfassung im untergeordneten Sachkonto an.

## <a name="subledger-journals-for-free-text-invoices"></a>Erfassungen im untergeordneten Sachkonto für Freitextrechnungen
Bevor Sie eine Freitextrechnung buchen, können Sie den vollständigen Buchhaltungseintrag der Rechnung anzeigen, der Soll- und Habenbeträge enthält, um sicherzustellen, dass die Rechnung auf die richtigen Konten gebucht wird. Diese Ansicht des vollständigen Buchhaltungseintrags wird als Erfassung im untergeordneten Sachkonto bezeichnet. Wenn der Erfassungseintrag im untergeordneten Sachkonto falsch ist, wenn Sie ihn in der Vorschau anzeigen, bevor Sie die Freitextrechnung journalisieren, können Sie den Erfassungseintrag im untergeordneten Sachkonto nicht ändern. Stattdessen müssen Sie die Buchhaltungsverteilungen oder das Buchungsprofil ändern. Die Buchhaltungsverteilungen dienen dazu, eine Seite des Buchhaltungseintrags, der Soll- oder Habenbetrag, zu definieren. Der Ausgleichskontoeintrag in der Erfassung im untergeordneten Sachkonto wird aus den Buchungsprofilen erstellt, beispielsweise aus dem Debitorenkonto oder der Steuer.




