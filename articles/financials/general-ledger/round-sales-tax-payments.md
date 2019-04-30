---
title: Mehrwertsteuerzahlungen und Rundungsregeln
description: In diesem Artikel wird beschrieben, wie sich die Rundungsregeleinstellung auf die Mehrwertsteuer-Behörden und auf die Rundung des Mehrwertsteuersaldos während der Abrechnung und Buchung der Mehrwertsteuer auswirkt.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1c1bb1c792eb79888a1df209f2eebaf14a38dd
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/14/2019
ms.locfileid: "842437"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Mehrwertsteuerzahlungen und Rundungsregeln

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie sich die Rundungsregeleinstellung auf die Mehrwertsteuer-Behörden und auf die Rundung des Mehrwertsteuersaldos während der Abrechnung und Buchung der Mehrwertsteuer auswirkt.

In regelmäßigen Abständen muss Mehrwertsteuer gemeldet werden und an die Steuerbehörde abgeführt werden. Dazu öffnen werden, indem die Informationen zur Bank und Beitragsmehrwertsteuerprozess in der Mehrwertsteuerseite ausführt. Die Mehrwertsteuer für einen Zeitraum wird mit den Mehrwertsteuerkonten ausgeglichen und der Mehrwertsteuersaldo wird zum Konto "Mehrwertsteuerabrechnung" gebucht. Der Mehrwertsteuersaldo, der im Konto "Mehrwertsteuerabrechnung" gebucht wird, kann je nach Anforderung der Steuerbehörden gerundet werden, indem eine Rundungsregel für die Mehrwertsteuerseite eingerichtet wird. 

Die Rundungsdifferenz wird zum Konto "Rundung Mehrwertsteuer" gebucht, das im Feld "Konten für automatische Buchungen" im "Hauptbuch" ausgewählt wird.

Das Beispiel unten veranschaulicht, wie der Rundenregel bei "Mehrwertsteuerbehörde" funktioniert.

## <a name="examples"></a>Beispiele

Die Gesamtumsatzsteuer für eine Periode zeigt ein Guthaben von -98.765,43 an. Die juristische Person hat mehr Mehrwertsteuer eingenommen, als sie bezahlt hat. Daher schuldet die juristische Person der Steuerbehörde Geld. 

Die juristische Person möchte eine Rundungsmethode verwenden, mit der der Saldo auf die nächsten 1,00 gerundet wird. Der Benutzer, der für die Mehrwertsteuerbuchhaltung zuständig ist, führt die folgenden Schritte aus.

1.  Klicken Sie auf "Steuer" &gt; "Indirekte Steuern" &gt; "Mehrwertsteuer" &gt; "Mehrwertsteuerbehörden".
2.  Wählen Sie im Inforegister "Allgemein" im Feld "Rundungsart" die Option "Normal" aus.
3.  Geben Sie im Feld "Rundung" die Zahl 1,00 ein.
4.  Wenn die Mehrwertsteuer an das Finanzamt abgeführt werden soll, öffnen Sie die Seite "Mehrwertsteuer abrechnen und buchen". (Klicken Sie auf "Steuer" &gt; "Erklärungen" &gt; "Mehrwertsteuer" &gt; "Mehrwertsteuer abrechnen und buchen".)
5.  Im Mehrwertsteuer-Abrechnungskonto wird der Steuerverbindlichkeitsbetrag von 98.765,43 auf 98.765 abgerundet.

Die folgende Tabelle zeigt, wie ein Betrag von 98.765,43 gerundet wird. Dabei wird jede Rundungsmethode angewendet, die im Feld "Rundungsart" auf der Seite "Steuerbehörden" verfügbar ist.

| Option der Rundungsart                | Rundungswert = 0,01 | Rundungswert = 0,10 | Rundungswert = 1,00 | Rundungswert = 100,00 |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| Normal                              | 98.765,43              | 98.765,40              | 98.765,00              | 98.800,00                |
| Abwärts                            | 98.765,43              | 98.765,40              | 98.765,00              | 98.700,00                |
| Aufrunden                         | 98.765,43              | 98.765,50              | 98.766,00              | 98.800,00                |
| Eigener Vorteil, für ein Guthaben | 98.765,43              | 98.765,40              | 98.765,00              | 98.700,00                |
| Eigener Vorteil, für ein Debitorensaldo  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a>Kein Runden, da die Rundung 0,00

Rundung(1,0151, 0,00) = 1,0151 Rundung(1,0149, 0,00) = 1,0149

### <a name="normal-round-and-round-precision-is-001"></a>Normale Rundung und Rungungsgenauigkeit ist 0,01

<table>
  <tr>
    <td>Rundung
    </td>
    <td>Berechnungsprozess
    </td>
  </tr>
    <tr>
    <td>Rundung(1,015, 0,01) = 1,02
    </td>
    <td>
      <ol>
        <li>Rundung(1,015 / 0,01, 0) = Rundung(101,5, 0) = 102
        </li>
        <li>102 * 0.01 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>Rundung(1,014 0,01) = 1,01
    </td>
    <td> <ol>
        <li>Rundung(1,014 / 0,01, 0) = Rundung(101,4, 0) = 101
        </li>
        <li>101 * 0.01 = 1.01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>Rundung(1,011 0,02) = 1,02
    </td>
    <td> <ol>
        <li>Rundung(1,011 / 0,02, 0) = Rundung(50,55, 0) = 51
        </li>
        <li>51 * 0.02 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>Rundung(1,009, 0,02) = 1,00
    </td>
    <td> <ol>
        <li>Rundung(1,009 / 0,02, 0) = Rundung(50,45, 0) = 50
        </li>
        <li>50 * 0.02 = 1.00
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> Wenn Sie "Eigener Vorteil" auswählen, erfolgt die Rundung immer zum Vorteil der juristischen Person. 

Weitere Informationen finden Sie in folgenden Themen:
- [Mehrwertsteuerüberblick](indirect-taxes-overview.md)
- [Eine Mehrwertsteuerzahlung erstellen](tasks/create-sales-tax-payment.md)
- [Mehrwertsteuerbuchungen in Dokumenten erstellen](tasks/create-sales-tax-transactions-documents.md)
- [Vorgenommene Mehrwertsteuerbuchungen anzeigen](tasks/view-posted-sales-tax-transactions.md)
- [Rundungsfunktion](https://msdn.microsoft.com/en-us/library/aa850656.aspx)


