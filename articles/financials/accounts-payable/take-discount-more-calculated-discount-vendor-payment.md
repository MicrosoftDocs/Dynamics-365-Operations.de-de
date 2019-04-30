---
title: Nehmen Sie einen Rabatt, der höher ist, als der berechnete Rabatt für eine Kreditorenzahlung
description: Dieser Artikel führt Sie durch ein Szenario, in dem ein Skonto für einen Betrag übernommen wird, der höher als der ursprünglich auf der Rechnung verfügbare Rabatt ist Dieses Szenario kann eintreten, wenn eine Organisation eine Vereinbarung mit dem Kreditor getroffen hat, einen geringen Betrag zu zahlen als auf der Rechnung vermerkt.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 730ea9bb23368d24c5a09f98fbf6bbb41d685702
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/25/2019
ms.locfileid: "896096"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a>Nehmen Sie einen Rabatt, der höher ist, als der berechnete Rabatt für eine Kreditorenzahlung

[!include [banner](../includes/banner.md)]

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



