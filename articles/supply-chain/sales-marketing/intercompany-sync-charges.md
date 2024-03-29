---
title: Intercompany-Kosten synchronisieren
description: In diesem Artikel wird erläutert, wie Sie Intercompany-Kosten synchronisieren.
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
ms.openlocfilehash: e7b3de3d7da7be6c1c8b5c3842862e7bccd78277
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857285"
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
