---
title: Mehrwertsteuerzahlungen und Rundungsregeln
description: In diesem Artikel wird beschrieben, wie sich die Rundungsregeleinstellung auf die Mehrwertsteuer-Behörden und auf die Rundung des Mehrwertsteuersaldos während der Abrechnung und Buchung der Mehrwertsteuer auswirkt.
author: ShylaThompson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998dbd01352d3fa5040187e81b564d14133464db
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4443744"
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

1. Klicken Sie auf **Steuer** > **Indirekte Steuern** > **Mehrwertsteuer** > **Mehrwertsteuerbehörden**.
2. Wählen Sie im Inforegister **Allgemein** im Feld **Rundungsart** die Option **Normal** aus.
3. Geben Sie im Feld **Rundung** die Zahl 1,00 ein.
4. Wenn die Mehrwertsteuer an das Finanzamt abgeführt werden soll, wechseln Sie zu **Steuer** > **Meldungen** > **Mehrwertsteuer** > **Mehrwertsteuer abrechnen und buchen**. Im Mehrwertsteuer-Abrechnungskonto können Sie sehen, dass der Steuerverbindlichkeitsbetrag von **98.765,43** auf **98.765** abgerundet wird.

Die folgende Tabelle zeigt, wie ein Betrag von 98.765,43 gerundet wird. Dabei wird jede Rundungsmethode angewendet, die im Feld **Rundungsart** auf der Seite **Steuerbehörden** verfügbar ist.

> [!NOTE]                                                                                  
> Wenn der Rundungswert auf 0,00 eingestellt ist, gilt Folgendes:
>
> - Bei normaler Rundung ist das Rundungsverhalten das Gleiche wie für **Rundung = 0,01**.
> - Für **Option der Rundungsart**, **Abrunden**, **Aufrunden** und **Eigener Vorteil** ist das Verhalten mit dem für **Rundung = 1,00** identisch.

| Option der Rundungsart                | Rundungswert = 0,01 | Rundungswert = 0,10 | Rundungswert = 1,00 | Rundungswert = 100,00 | Rundungswert = 0,00   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| Normal                              | 98,765.43              | 98,765.40              | 98,765.00              | 98,800.00                | 98,765.43                |
| Abwärts                            | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Aufrunden                         | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |
| Eigener Vorteil, für ein Guthaben | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Eigener Vorteil, für ein Debitorensaldo  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |

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
- [Mehrwertsteuerübersicht](indirect-taxes-overview.md)
- [Eine Mehrwertsteuerzahlung erstellen](tasks/create-sales-tax-payment.md)
- [Mehrwertsteuerbuchungen in Dokumenten erstellen](tasks/create-sales-tax-transactions-documents.md)
- [Vorgenommene Mehrwertsteuerbuchungen anzeigen](tasks/view-posted-sales-tax-transactions.md)
- [Rundungsfunktion](https://msdn.microsoft.com/library/aa850656.aspx)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]