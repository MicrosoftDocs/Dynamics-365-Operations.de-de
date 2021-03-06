---
title: Stornierte Produktzugänge aktualisieren den Status der Transaktion nicht auf Registriert
description: Nachdem Sie Produktzugänge bei einer eingehenden Ladung storniert haben, aktualisiert das System automatisch den Status der Transaktion im Bestand von „Erhalten“ auf „Bestellt“.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294081"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>Stornierte Produktzugänge aktualisieren den Status der Transaktion nicht auf Registriert

## <a name="symptoms"></a>Symptome

Nachdem Sie die Aktion **Produktzugänge stornieren** bei einer eingehenden Ladung ausgeführt haben, aktualisiert das System automatisch den Status der Bestandstransaktionen von *Eingegangen* auf *Bestellt*.

## <a name="resolution"></a>Lösung

Wenn Lieferscheine für ausgehende Ladungen storniert werden, bleibt der Status von Bestandstransaktionen *Kommissioniert*. Wenn jedoch Produktzugänge von einer eingehenden Ladung storniert werden, wird der Status von Bestandstransaktionen nicht auf *Registriert* zurückgesetzt. Daher muss die Arbeitskraft am Lagerort nach der Stornierung eines Produktzugangs aus einer eingehenden Ladung die Artikelmengen für die Ladungen neu registrieren.

Weitere Informationen finden Sie unter [Artikelmengen registrieren, die mit einer eingehenden Ladung ankommen](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).
