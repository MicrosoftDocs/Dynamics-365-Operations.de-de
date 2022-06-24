---
title: Degressive Abschreibung nach einer Teilung reduzieren
description: In diesem Artikel wird die Methode beschrieben, die im Anlagevermögen verwendet wird, um die Abschreibung nach der Aufteilung einer Anlage mithilfe der Methode zum Reduzieren des Saldos zu berechnen.
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 539967a9a73da91f6b49c1bb89f404267ae0a804
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883299"
---
# <a name="reduce-balance-depreciation-after-a-split"></a>Degressive Abschreibung nach einer Teilung reduzieren

[!include [banner](../includes/banner.md)]

In diesem Artikel wird die Methode beschrieben, die im Anlagevermögen verwendet wird, um die Abschreibung nach der Aufteilung einer Anlage in eine andere Anlage mithilfe der Methode zum Reduzieren des Saldos zu berechnen. Das im Anlagenbuch konfigurierte Abschreibungsjahr ist das Geschäftsjahr. Weitere Informationen finden Sie unter [Reduzierung der degressiven Abschreibung](reduce-balance-depreciation.md) und [Aufteilen einer Anlage](tasks/split-fixed-asset.md).

Wenn Sie eine Anlage während eines Finanzzeitraums aufteilen, der später als der Zeitraum ist, in dem die Anlage erworben wurde, wird der Nettobuchwert (NBV) der Anlage für das Vorjahr durch die reduzierte degressive Abschreibung berücksichtigt. Es werden auch die Anschaffungs- und Abschreibungsregulierungstransaktionen berücksichtigt, die aus der Transaktion generiert wurden, mit der die Anlage aufgeteilt wurde. Bei diesem Verhalten wird davon ausgegangen, dass die Anlage in einem Geschäftsjahr angeschafft und in einem späteren Geschäftsjahr aufgeteilt wurde. Der Betrag, der nach der Aufteilung für die ursprüngliche Anlage abgeschrieben werden muss, spiegelt den NBV der Anlage vor der Aufteilung der Anlage und die für die Aufteilung gebuchte Anschaffungs- und Abschreibungsregulierungstransaktion wider.

Beispielsweise gelten die folgenden Bedingungen:

- Der Finanzzeitraum dauert vom 30. Juni bis zum 1. Juli.
- Der Prozentsatz des reduzierenden Saldos beträgt 18 Prozent, und eine Anlage wird im Juni 2019 zu einem Kaufpreis von 10.000 USD erworben.
- Die Abschreibung im ersten Geschäftsjahr beträgt 18.000 USD, die monatliche Abschreibung entspricht 150 USD, und die Anlage wird dann bis November 2019 in Höhe von 738,75 USD abgeschrieben.
- Im November 2019 werden 80 Prozent der Anlage auf eine andere Anlage aufgeteilt.

[![Degressive Abschreibung nach einer Teilung reduzieren.](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

Der für die ursprüngliche Anlage abzuschreibende Betrag beträgt 1.822,25 USD. Dieser Betrag entspricht dem NBV vor der Buchung der Aufteilungstransaktion (9.111,25 USD) zuzüglich der Anschaffungsregulierung, die während der Buchung der Aufteilungstransaktion generiert wird (-8.000 USD), zuzüglich der Abschreibungsregulierung, die während der Aufteilungstransaktion generiert wird (711 USD). Daher beträgt die Abschreibung für das zweite Jahr (1.822,25 × 18 Prozent) ÷ 12 = 27,33 USD.

Der Abschreibungsbetrag für die neue Anlage im ersten Jahr beträgt (8.000 × 18 Prozent) ÷ 12 = $120.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
