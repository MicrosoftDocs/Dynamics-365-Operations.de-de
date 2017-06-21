---
title: "Nehmen Sie einen Rabatt, der höher ist, als der berechnete Rabatt für eine Kreditorenzahlung"
description: "Dieser Artikel führt Sie durch ein Szenario, in dem ein Skonto für einen Betrag übernommen wird, der höher als der ursprünglich auf der Rechnung verfügbare Rabatt ist Dieses Szenario kann eintreten, wenn eine Organisation eine Vereinbarung mit dem Kreditor getroffen hat, einen geringen Betrag zu zahlen als auf der Rechnung vermerkt."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 08d7c4981aba7e7c092a6f21d3b63635e76437bf
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a>Nehmen Sie einen Rabatt, der höher ist, als der berechnete Rabatt für eine Kreditorenzahlung

[!include[banner](../includes/banner.md)]


Dieser Artikel führt Sie durch ein Szenario, in dem ein Skonto für einen Betrag übernommen wird, der höher als der ursprünglich auf der Rechnung verfügbare Rabatt ist Dieses Szenario kann eintreten, wenn eine Organisation eine Vereinbarung mit dem Kreditor getroffen hat, einen geringen Betrag zu zahlen als auf der Rechnung vermerkt. 

Kreditor 3051 gibt Fabrikam ein Skonto von 4 Prozent, wenn eine Rechnung in sieben Tagen beglichen wird. Am 29. Juni gibt April eine Rechnung für 1.000,00 ein. Der Händler gewährt April einen Rabatt von 60,00 anstelle des standardmäßigen Rabatts von 40,00, der für die Rechnung verfügbar ist. April erfasst eine einmalige Zahlung, indem er die Zahlungserfassung "Kreditoren" verwendet. Sie gibt den Kreditor für die Zahlung ein und öffnet anschließend die Seite **Buchungen ausgleichen**. Sie markiert die Rechnung und ändert den Wert im Feld **Skontobetrag** in **60,00**.
| Markieren     | Skonto verwenden | Beleg   | Konto | Datum      | Fälligkeitsdatum  | Rechnung | Betrag in Buchungswährung | Währung | Auszugleichender Betrag |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Ausgewählt | Normal            | Inv-10040 | 3051    | 6/29/2015 | 7/29/2015 | 10040   | 1.000,00                       | USD      | 940,00           |

Rabattinformationen werden am unteren Rand der Seite **Buchungen ausgleichen** angezeigt.
|                              |           |
|------------------------------|-----------|
| Skontodatum           | 7/12/2015 |
| Skontobetrag         | 60,00     |
| Skonto verwenden            | Normal    |
| Verwendetes Skonto          | 0,00      |
| Zu verwendender Skontobetrag | 60,00     |

April bucht die Zahlungserfassung. Die Rechnung wird vollständig mit einer Zahlung von 940,00 und einem Rabatt von 60,00 ausgeglichen.




