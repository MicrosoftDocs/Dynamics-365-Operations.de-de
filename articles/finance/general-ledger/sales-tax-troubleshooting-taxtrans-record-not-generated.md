---
title: TaxTrans-Datensatz wird nicht generiert
description: Dieses Thema enthält Informationen zur Fehlerbehebung, die helfen können, wenn ein TaxTrans-Datensatz nicht generiert wird.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947643"
---
# <a name="taxtrans-record-isnt-generated"></a>TaxTrans-Datensatz wird nicht generiert

[!include [banner](../includes/banner.md)]

Wenn Sie **Gebuchte Mehrwertsteuer** für eine Transaktion wählen, aber die Seite **Gebuchte Mehrwertsteuer** entweder keine Steuerzeilen anzeigt oder eine Steuerzeile fehlt, wurde der **TaxTrans** Datensatz möglicherweise nicht erzeugt.

[![Seite „Gebuchte Mehrwertsteuer“, die keine Zeilen enthält](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

Um dieses Problem zu beheben, führen Sie die Schritte in den folgenden Abschnitten wie erforderlich aus.

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>Prüfen Sie die Mehrwertsteuer, bevor Sie die Transaktion buchen

1. Bevor Sie die Transaktion buchen, wählen Sie auf der Seite **Rechnung buchen** die Schaltfläche **Mehrwertsteuer**, um die Berechnung zu überprüfen.

    [![Schaltfläche „Mehrwertsteuer“ auf der Seite „Rechnung buchen“](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. Prüfen Sie auf der Seite **Vorläufige Transaktionen der Mehrwertsteuer** das Ergebnis der Berechnung. Wenn keine Steuer berechnet wird, siehe [Steuer wird nicht berechnet oder der Steuerbetrag ist Null](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>Finden Sie den TaxTrans-Datensatz in allen gebuchten Mehrwertsteuer

1. Gehen Sie zu **Steuern** \> **Abfragen und Berichte** \> **Umsatzsteuer-Abfragen** > **Umsatzsteuer**.
2. Wählen Sie in der Spaltenüberschrift **Beleg** das Filtersymbol, um den Datensatz **TaxTrans** zu finden.
3. Wenn Sie die gesuchten Mehrwertsteuersätze finden, überprüfen Sie das Datum. Wenn das Datum von dem Datum der Journalüberschrift abweicht, erstellen Sie eine Microsoft-Serviceanfrage für zusätzliche Unterstützung.

    [![Veröffentlichte Umsatzsteuer-Seite](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>Debuggen, um Details zu prüfen

1. Informationen darüber, wie Sie Fehler beheben und feststellen können, ob **TmpTaxWorkTrans** und **TaxUncommitted** korrekt erzeugt werden, finden Sie unter [Feldwert in TaxTrans ist falsch](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).
2. Wenn **TaxTmpWorkTrans** oder **TaxUncommitted** korrekt generiert wird, fügen Sie einen Haltepunkt bei **TaxPost ::SaveAndPost()** und **Tax ::SaveAndPost** ein, um den Grund zu debuggen, warum **TaxTrans** nicht eingefügt wird.

    [![Haltepunkte im Code hinzugefügt](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![Ergebnisse der hinzugefügten Haltepunkte](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>Ermitteln Sie, ob eine Anpassung vorliegt

Wenn Sie die Schritte in den vorherigen Abschnitten ausgeführt haben, aber kein Problem gefunden haben, stellen Sie fest, ob eine Anpassung vorhanden ist. Wenn keine Anpassung vorhanden ist, erstellen Sie eine Microsoft Service-Anfrage für weiteren Support.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
