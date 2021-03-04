---
title: Ausgleichen von Buchungen zwischen Sachkonten
description: Diese Prozedur zeigt das Ausgleichen von Buchungen zwischen Sachkonten und das Stornieren eines Sachkontoausgleichs.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb53e9fee35712343f034389f00f3d4539cc652d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443597"
---
# <a name="settle-transactions-between-ledger-accounts"></a>Ausgleichen von Buchungen zwischen Sachkonten

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]