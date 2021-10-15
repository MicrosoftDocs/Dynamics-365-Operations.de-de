---
title: Intercompany-Batch- und -Seriennummern
description: In diesem Thema wird erläutert, was geschieht, wenn Sie Chargennummern und Seriennummern für Intercompany-Aufträge registrieren.
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
ms.openlocfilehash: 4da936263bb57c24eeb7021ac61b3945bb2777fb
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548297"
---
# <a name="intercompany-batch-and-serial-numbers"></a>Intercompany-Batch- und -Seriennummern

[!include [banner](../../includes/banner.md)]

Unternehmen, die Serien- oder Chargennummern zum Verfolgen von Artikeln einsetzen, müssen auch die Serien-/Chargennummern von entnommenen Artikeln verfolgen. Die Intercompany-Funktionalität automatisiert die Übergabe/den Abruf von Serien- und Chargennummern zwischen Unternehmen. Werden die Chargen- und Seriennummern für Artikel auf einem Intercompany-Auftrag erfasst, kann die Anwendung so eingestellt werden, dass diese Nummern automatisch an die Intercompany-Bestellung und den Originalauftrag übergeben werden. Hierfür müssen die entsprechenden Parameter für den Auftrag auf der Seite **Intercompany** festgelegt werden:

- Wenn Sie auf der Seite **Bestellrichtlinien** das Feld **Chargennummer** auswählen, wird die Chargennummer beim Buchen des Lieferscheins des Intercompany-Auftrags mit den Lagerbuchungen der Intercompany-Bestellpositionen synchronisiert.
- Wird das Feld **Seriennummer** aktiviert, werden die Seriennummern beim Buchen des Lieferscheins des Intercompany-Auftrags mit den Lagerbuchungen der Intercompany-Bestellpositionen synchronisiert.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
