---
title: Bestandsmenge wird aufgrund unzureichender Transaktionen nicht aktualisiert
description: Die Bestandsmenge –1 % kann nicht aktualisieren werden, weil es nicht genügend Bestandstransaktionen für Artikel %2 gibt, die die angegebenen Dimensionen aufweisen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476395"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>Das System kann die Lagerbestandsmenge aufgrund unzureichender Transaktionen nicht aktualisieren.

## <a name="symptoms"></a>Symptome

Dieses Problem kann auftreten, wenn das System eine Bestandsmenge nicht aktualisieren kann, weil es nicht genügend Bestandstransaktionen gibt, die die angegebenen Dimensionen haben. Möglicherweise erhalten Sie die folgende Fehlermeldung:

> Bestandsmenge -%1 konnte nicht aktualisiert werden, da nicht genügend Bestandstransaktionen für Element %2 mit den Dimensionen Größe=%3, Farbe=%4, Zugänge=%5, Standort=%6, Lagerort=%7, Ort=%8, Bestandsstatus=Verfügbar, Ladungsträger=%9, Chargennummer=%10 für Referenz-ID %11 auf Los-ID %12.

## <a name="resolution"></a>Lösung

Stellen Sie sicher, dass keine Bestandstransaktionen die Menge physisch reservieren. Diese Transaktionen könnten z. B. Qualitätsaufträge, Bestandssperrsätze oder Ausgabeaufträge öffnen.
