---
title: Die Menge eines begonnen Quarantäneauftrags wird nicht aktualisiert, wenn der Auftrag aufgeteilt wird
description: Wenn Sie einen Quarantäneauftrag anlegen und versuchen, ihn aufzuteilen, wird die Auftragsmenge nicht auf die nach der Aufteilung verbleibende Menge aktualisiert.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026554"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Die Menge eines begonnen Quarantäneauftrags wird nicht aktualisiert, wenn der Auftrag aufgeteilt wird

KB-Nummer: 4613113

## <a name="symptoms"></a>Symptome

Wenn Sie einen Quarantäneauftrag anlegen und versuchen, ihn aufzuteilen, wird die Auftragsmenge nicht auf die nach der Aufteilung verbleibende Menge aktualisiert.

## <a name="resolution"></a>Lösung

Das System ändert die ursprüngliche Menge aus einem Quarantäneauftrag nicht, um sicherzustellen, dass Sie die ursprüngliche Menge verfolgen können, die für diesen Quarantäneauftrag erstellt wurde. Das System verfolgt jedoch die Menge, die von einem Quarantäneauftrag abgetrennt wird. Für diese Verfolgung wird ein Datenbankfeld mit dem Namen `QuantityThatHasSplitIntoOtherQuarantineOrders` verwendet. Dieses Feld ist jedoch auf der Benutzeroberfläche (UI) nicht sichtbar.
