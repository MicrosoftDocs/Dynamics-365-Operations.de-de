---
title: Asynchrone Debitoren in synchrone Debitoren konvertieren
description: In diesem Artikel wird erläutert, wie Sie in Microsoft Dynamics 365 Commerce asynchrone Debitoren in synchrone Debitoren umwandeln.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: b442bfc0685706359771e4d9e2729565d3652a60
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278191"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Asynchrone Debitoren in synchrone Debitoren konvertieren

[!include [banner](includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie in Microsoft Dynamics 365 Commerce asynchrone Debitoren in synchrone Debitoren umwandeln.

Wenn Sie asynchrone Debitoren in synchrone Debitoren umwandeln möchten, führen Sie folgende Schritte aus.

1. Führen Sie in der Commerce-Zentrale den **P-Einzelvorgang** aus, um die asynchronen Debitoren an die Commerce-Zentrale zu senden.
1. Führen Sie den Einzelvorgang **Debitoren und Geschäftspartner im asynchronen Modus synchronisieren** zum Erstellen von Debitorenkonto-IDs aus. (Dieser Einzelvorgang hieß früher **Debitoren und Geschäftspartner aus dem asynchronen Modus synchronisieren** .)
1. Führen Sie den Einzelvorgang **1010** zum Synchronisieren der neuen Debitorenkonto-IDs mit den Kanälen aus.

Wenn eine Bestellung auf einen asynchronen Debitoren oder eine asynchrone Adresse verweist, die noch nicht mit der Commerce-Zentrale synchronisiert wurde, wird der Debitor oder die Adresse im Rahmen des Batch-Einzelvorgnags **Bestellungen synchronisieren** synchronisiert. Wenn eine Cash-and-Carry-Transaktion auf einen asynchronen Debitoren oder eine asynchrone Adresse verweist, wird der Debitor oder die Adresse vor der Tagesendbuchung (EOD) synchronisiert.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Debitorenverwaltung in Geschäften](customer-mgmt-stores.md)

[Asynchroner Debitorerstellungsmodus](async-customer-mode.md)

[Debitorattribute](dev-itpro/customer-attributes.md)

[Ausschluss von Offlinedaten](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
