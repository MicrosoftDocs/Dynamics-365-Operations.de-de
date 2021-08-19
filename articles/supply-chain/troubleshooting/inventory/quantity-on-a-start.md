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
ms.openlocfilehash: 4625570cb706199dca78f23b1864ca1d81cc66e896cf10d6d5f16cf1a9d1dc16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713493"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Die Menge eines begonnen Quarantäneauftrags wird nicht aktualisiert, wenn der Auftrag aufgeteilt wird

KB-Nummer: 4613113

## <a name="symptoms"></a>Symptome

Wenn Sie einen Quarantäneauftrag anlegen und versuchen, ihn aufzuteilen, wird die Auftragsmenge nicht auf die nach der Aufteilung verbleibende Menge aktualisiert.

## <a name="resolution"></a>Lösung

Das System ändert die ursprüngliche Menge aus einem Quarantäneauftrag nicht, um sicherzustellen, dass Sie die ursprüngliche Menge verfolgen können, die für diesen Quarantäneauftrag erstellt wurde. Das System verfolgt jedoch die Menge, die von einem Quarantäneauftrag abgetrennt wird. Für diese Verfolgung wird ein Datenbankfeld mit dem Namen `QuantityThatHasSplitIntoOtherQuarantineOrders` verwendet. Dieses Feld ist jedoch auf der Benutzeroberfläche (UI) nicht sichtbar.
