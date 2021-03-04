---
title: Inventarverfügbarkeit in dualem Schreiben
description: Dieses Thema bietet Informationen zum Prüfen der Bestandverfügbarkeit in dualem Schreiben.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4452999"
---
# <a name="inventory-availability-in-dual-write"></a>Inventarverfügbarkeit in dualem Schreiben

[!include [banner](../../includes/banner.md)]

Mithilfe der Bestandverfügbarkeit können Sie Ihr Inventar überprüfen, bevor Sie ein Produkt zu den Formularen **Zitate**, **Aufträge** oder **Rechnungen** in Microsoft Dynamics 365 Sales hinzufügen. Zum Beispiel ist die Überprüfung des Inventars und die Bestimmung eines Erfüllungstermins eine Schlüsselaufgabe in [Aussicht auf Bargeld](dual-write-prospect-to-cash.md) Prozess.

Wenn Sie nicht über genügend Bestand verfügen, können Sie einen Liefertermin basierend auf den projizierten Bestandeinnahmen und -Problemen schätzen. Sie können auch die ATP-Informationen des Produkts überprüfen, in denen Sie die ATP-Menge in dem vordefinierten Zeitrahmen finden.

## <a name="on-hand-inventory"></a>Verfügbarer Lagerbestand

In der Kopfzeile der Seiten **Angebote**, **Aufträge** und **Rechnungen** in Dynamics 365 Sales wurde eine neue Schaltfläche **Lagerbestand** hinzugefügt. Wenn Sie auf die Schaltfläche klicken, wird ein Dialogfeld angezeigt, in dem Sie das Unternehmen und das Produkt angeben können, für das Sie dann den Lagerbestand überprüfen möchten. Dieses Dialogfeld zeigt die gleichen Informationen wie [Lagerbestand](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Das Dialogfeld gibt die Inventarinformationen von Dynamics 365 Supply Chain Management zurück. Diese Informationen umfassen die folgenden Mengen:

- Verfügbare Menge
- Die verfügbare Menge in Reserve
- Die verfügbare Menge
- Bestellte Menge
- Die Auftragsmenge
- Reservierte bestellte Menge
- Die insgesamt verfügbare Menge

## <a name="atp-information"></a>VfZ-Informationen

In Sales wurde eine neue Schaltfläche **ATP-Informationen** wurde zu den Seite **Zitate**, **Aufträge**, und **Rechnungen** hinzugefügt. Wenn Sie auf diese Schaltfläche klicken, wird ein Dialogfeld angezeigt, in dem Sie das Unternehmen, Produkt, Lagerstandort, Lagerbestand und bestellte Menge angeben können.. Dieses Dialogfeld hat dieselben Einstellungen wie in [Bestellung vielversprechend](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Das Dialogfeld gibt die ATP-Informationen aus dem Supply Chain Management zurück. Diese Informationen umfassen die folgenden Mengen:

- VfZ-Menge
- Zugangsmenge
- Abgangsmenge
- Verfügbare Menge


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]