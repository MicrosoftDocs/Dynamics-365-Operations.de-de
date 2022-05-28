---
title: Intercompany-Batch- und -Seriennummern
description: In diesem Thema wird erläutert, was geschieht, wenn Sie Chargennummern und Seriennummern für Intercompany-Aufträge registrieren.
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
ms.openlocfilehash: 9d5e6ddd0bf9ab9dd032e3ab8d1e11d53fba639e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672933"
---
# <a name="intercompany-batch-and-serial-numbers"></a>Intercompany-Batch- und -Seriennummern

[!include [banner](../../includes/banner.md)]

Unternehmen, die Serien- oder Chargennummern zum Verfolgen von Artikeln einsetzen, müssen auch die Serien-/Chargennummern von entnommenen Artikeln verfolgen. Die Intercompany-Funktionalität automatisiert die Übergabe/den Abruf von Serien- und Chargennummern zwischen Unternehmen. Werden die Chargen- und Seriennummern für Artikel auf einem Intercompany-Auftrag erfasst, kann die Anwendung so eingestellt werden, dass diese Nummern automatisch an die Intercompany-Bestellung und den Originalauftrag übergeben werden. Hierfür müssen die entsprechenden Parameter für den Auftrag auf der Seite **Intercompany** festgelegt werden:

- Wenn Sie auf der Seite **Bestellrichtlinien** das Feld **Chargennummer** auswählen, wird die Chargennummer beim Buchen des Lieferscheins des Intercompany-Auftrags mit den Lagerbuchungen der Intercompany-Bestellpositionen synchronisiert.
- Wird das Feld **Seriennummer** aktiviert, werden die Seriennummern beim Buchen des Lieferscheins des Intercompany-Auftrags mit den Lagerbuchungen der Intercompany-Bestellpositionen synchronisiert.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
