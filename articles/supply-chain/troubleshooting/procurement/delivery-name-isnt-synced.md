---
title: Der Lieferungsname wird nicht synchronisiert, nachdem die Lieferadresse einer Bestellung geändert wurde
description: Nachdem Sie die Lieferadresse in einem Bestellkopf geändert haben, wird der Lieferungsname nicht synchronisiert.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476412"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>Der Lieferungsname wird nicht synchronisiert, nachdem die Lieferadresse einer Bestellung geändert wurde

## <a name="symptoms"></a>Symptome

Die Adresse in der Kopfzeile einer Bestellung wird auf eine Adresse aktualisiert, die keine Lieferadresse ist. Obwohl die Adresse in der Bestellung aktualisiert wird, wird der Lieferungsname nicht basierend auf der aktualisierten Adresse aktualisiert.

## <a name="resolution"></a>Lösung

Dieses Verhalten ist beabsichtigt. Die ausgewählte Adresse muss als Lieferadresse klassifiziert werden. Andernfalls wird der Lieferungsname nicht basierend auf der ausgewählten Adresse aktualisiert.
