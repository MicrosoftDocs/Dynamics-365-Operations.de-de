---
title: Intercompany-Kosten synchronisieren
description: In diesem Thema wird erläutert, wie Sie Intercompany-Kosten synchronisieren.
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
ms.openlocfilehash: 2c7f60786743cf750b2bb17ccc0dadf71d859766
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678574"
---
# <a name="synchronize-intercompany-charges"></a>Intercompany-Kosten synchronisieren

[!include [banner](../../includes/banner.md)]

Belastungen werden nur zwischen dem Intercompany-Auftrag und der Intercompany-Bestellung synchronisiert, und die Synchronisierung findet immer statt.

Wenn das Feld **Preisbearbeitung zulassen** für den Intercompany-Auftrag oder die Intercompany-Bestellung aktiviert ist, können Sie dem Intercompany-Auftrag bzw. der Intercompany-Bestellung manuell eine Belastung hinzufügen. Andernfalls ist dies nicht möglich.

Wenn das Feld **Preisbearbeitung zulassen** auf dem Intercompany-Auftrag nicht aktiviert ist, können Sie dem Intercompany-Auftrag keinen sonstigen Zuschlag manuell hinzufügen.

Wenn das Feld **Preisbearbeitung zulassen** für die Intercompany-Bestellung nicht aktiviert ist, ist es nicht möglich, der Intercompany-Bestellung eine Belastung hinzuzufügen.

Wenn das Feld **Preisbearbeitung zulassen** sowohl für die Intercompany-Bestellung als auch den Intercompany-Auftrag aktiviert ist, können Sie der Bestellung und dem Auftrag manuell Belastungen hinzufügen. Dies kann jedoch dazu führen, dass viele Belastungen falsch hinzugefügt werden.

Um derartige Konflikte zu vermeiden, empfiehlt es sich, das Hinzufügen von Belastungen nur für den Intercompany-Auftrag bzw. nur für die Intercompany-Bestellung zuzulassen, jedoch nicht für beide.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
