---
title: Intercompany-Lieferscheine
description: In diesem Artikel wird beschrieben, wie Lieferscheine für Intercompany-Transaktionen generiert und gedruckt werden.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3516058bbf925df4b0a0c75286a3d97457cc1e69
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900853"
---
# <a name="intercompany-packing-slips"></a>Intercompany-Lieferscheine

## <a name="generate-intercompany-packing-slips"></a>Intercompany-Lieferscheine generieren

[!include [banner](../../includes/banner.md)]

Wenn Sie mit Direktlieferung arbeiten, wird der Lieferschein immer automatisch für die Intercompany-Bestellung und den Originalauftrag generiert, wenn der Lieferschein für den Intercompany-Auftrag generiert wird. Die Rechnung für die Intercompany-Bestellung basiert auf dem Lieferschein für die Intercompany-Bestellung, die zuvor generiert wurde.

Aktualisierungen des Lieferscheins für den Intercompany-Auftrag werden in der Intercompany-Bestellung und im Originalauftrag angezeigt.

Wenn Sie nicht mit Direktlieferung arbeiten, müssen Sie den Lieferschein für den Intercompany-Auftrag, die Intercompany-Bestellung und den Originalauftrag manuell generieren.

## <a name="print-intercompany-packing-slips"></a>Intercompany-Lieferscheine drucken

[!include [banner](../../includes/banner.md)]

Bei Verwendung von Direktlieferungen kann ein Lieferschein für die Intercompany-Bestellung und den Originalauftrag beim Buchen des Lieferscheins für den Intercompany-Auftrag automatisch gedruckt werden.

Um Lieferscheine automatisch zu drucken, wählen Sie auf der Seite **Intercompany** für Bestellungen beide Felder für **Lieferschein automatisch drucken** aus.

Wird der Lieferschein für den Intercompany-Auftrag aktualisiert, werden die Änderungen automatisch in der Intercompany-Bestellung und im Originalauftrag berücksichtigt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
