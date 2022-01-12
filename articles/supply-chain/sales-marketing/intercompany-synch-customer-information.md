---
title: Intercompany-Debitoreninformationen synchronisieren
description: In diesem Thema wird die Synchronisierung von Debitoreninformationen für Intercompany-Aufträge erläutert.
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c82216c8391f6c447bec74f25cd16b9db18d468d
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548290"
---
# <a name="synchronize-intercompany-customer-information"></a>Intercompany-Debitoreninformationen synchronisieren

[!include [banner](../../includes/banner.md)]

Kundeninformationen werden synchronisiert, wenn das Feld **Debitoreninformationen** synchronisiert, bei der Erstellung des Auftrags oder bei einer Änderung des Debitors, der Kreditorenreferenzoder oder der Debitormaterialanforderungsnummer vorgenommen wird.

Der Wert in den Synchronisierungsfeldern kann immer geändert werden. Allerdings kann durch Auswahl dieses Parameters nur festgelegt werden, ob der Wert in die anderen Intercompany-Aufträge kopiert werden soll. Wenn Sie das Feld **Debitoreninformationen** für den Intercompany-Auftrag aktiviert haben, wird eine Änderung am Intercompany-Auftrag mit der Intercompany-Bestellung synchronisiert. Wenn Sie das Feld **Debitoreninformationen** auch für die Intercompany-Bestellung aktiviert haben, wird sie ebenfalls mit dem ursprünglichen Auftrag synchronisiert.

> [!NOTE]
> Wenn Sie das Feld **Debitoreninformationen** sowohl für die Intercompany-Bestellung als auch den Intercompany-Auftrag aktiviert haben, werden die von einer Person in einem Unternehmen vorgenommenen Aktualisierungen durch die von einer anderen Person in einem anderen Unternehmen für denselben Auftrag vorgenommenen Aktualisierungen aufgehoben.

Die optimale Methode besteht in der Aktivierung des Felds **Debitoreninformationen** für die Intercompany-Bestellung. Dadurch wird die Synchronisierung zwischen dem ursprünglichen Auftrag und der Intercompany-Bestellung und von der Intercompany-Bestellung zum Intercompany-Auftrag aktiviert.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]