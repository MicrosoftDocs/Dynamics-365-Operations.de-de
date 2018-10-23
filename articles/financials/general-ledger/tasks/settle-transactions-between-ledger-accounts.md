--- 
title: Ausgleichen von Buchungen zwischen Sachkonten
description: Diese Prozedur zeigt das Ausgleichen von Buchungen zwischen Sachkonten und das Stornieren eines Sachkontoausgleichs.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4c200c07ad576073ab5410b52ec237d31b2415d2
ms.openlocfilehash: 4aff64fa1c017f295752e913de7fb320f0662ef8
ms.contentlocale: de-de
ms.lasthandoff: 10/03/2018

---
# <a name="settle-transactions-between-ledger-accounts"></a>Ausgleichen von Buchungen zwischen Sachkonten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt das Ausgleichen von Buchungen zwischen Sachkonten und das Stornieren eines Sachkontoausgleichs. Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet.


## <a name="settle-transaction-between-ledger-accounts"></a>Ausgleichen von Transaktionen zwischen Sachkonten
1. Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Sachkontoausgleiche".
2. Suchen Sie in der Liste die Transaktion, die Sie auszugleichen möchten.
   > [!NOTE]
   > Der Saldo muss null sein.  
3. Klicken Sie auf "Einschließen"..
4. Klicken Sie auf "Annehmen".

## <a name="cancel-a-ledger-settlement"></a>Stornieren eines Sachkontoausgleichs

1. Wechseln Sie zu "Hauptbuch" > "Abfragen und Berichte" > "Zwischenbilanz".
2. Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf "Parameter".
3. Klicken Sie auf Aktualisieren.
4. Suchen Sie in der Liste das Konto, das die auszugleichende Transaktion hat.
5. Klicken Sie auf "Alle Transaktionen".
6. Verwenden Sie einen Filter, um die Buchung in der Liste zu suchen.
7. Klicken Sie auf "Sachkontoausgleiche".
8. Markieren Sie in der Liste die ausgewählte Zeile.


