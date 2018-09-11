--- 
title: Ausgleichen von Buchungen zwischen Sachkonten
description: Diese Prozedur zeigt das Ausgleichen von Buchungen zwischen Sachkonten und das Stornieren eines Sachkontoausgleichs.
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 97a28069f8d560c98099a667852c932ba7658996
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="settle-transactions-between-ledger-accounts"></a>Ausgleichen von Buchungen zwischen Sachkonten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt das Ausgleichen von Buchungen zwischen Sachkonten und das Stornieren eines Sachkontoausgleichs. Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet.


## <a name="settle-transaction-between-ledger-accounts"></a>Ausgleichen von Transaktionen zwischen Sachkonten
1. Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Sachkontoausgleiche".
2. Suchen Sie in der Liste die Transaktion, die Sie auszugleichen möchten.
    * Der Saldo muss null sein.  
3. Klicken Sie auf "Einschließen"..
4. Klicken Sie auf "Annehmen".

## <a name="cancel-a-ledger-settlement"></a>Stornieren eines Sachkontoausgleichs
1. Schließen Sie die Seite.
2. Wechseln Sie zu "Hauptbuch" > "Abfragen und Berichte" > "Zwischenbilanz".
3. Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf "Parameter".
4. Klicken Sie auf Aktualisieren.
5. Suchen Sie in der Liste das Konto, das die auszugleichende Transaktion hat.
6. Klicken Sie auf "Alle Transaktionen".
7. Verwenden Sie einen Filter, um die Buchung in der Liste zu suchen.
8. Klicken Sie auf "Sachkontoausgleiche".
9. Markieren Sie in der Liste die ausgewählte Zeile.


