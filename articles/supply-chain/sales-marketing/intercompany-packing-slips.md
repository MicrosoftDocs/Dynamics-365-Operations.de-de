---
title: Intercompany-Lieferscheine
description: In diesem Thema wird beschrieben, wie Lieferscheine für Intercompany-Transaktionen generiert und gedruckt werden.
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
ms.openlocfilehash: 72d052d2daba90d49ba372fb3fb480bdd0877398
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548293"
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
