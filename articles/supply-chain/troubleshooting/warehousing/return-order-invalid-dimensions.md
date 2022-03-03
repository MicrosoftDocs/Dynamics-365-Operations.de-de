---
title: Ladezeile kann aufgrund ungültiger Lagerdimensionen nicht erstellt werden
description: Wenn Sie versuchen, einen Retourenauftrag an das Lager freizugeben, erhalten Sie möglicherweise eine Fehlermeldung über ungültige Lagerbestandsdimensionen. Entfernen Sie diese aus der Auftragszeile.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b02408b61b07b272a7e7d52004dc2492d60ef28c
ms.sourcegitcommit: 0d14c4a1e6cf533dd20463f1a84eae8f6d88f71b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119211"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Ladeposition für Retourenauftrag kann aufgrund ungültiger Lagerdimensionen nicht erstellt werden

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, einen Rücklieferungs-Verkaufsauftrag an das Lagerort freizugeben, erhalten Sie möglicherweise die folgende Fehlemeldung:

> Sie können keine Ladezeile für diese Auftragszeile erstellen, da sie Bestandsdimensionen enthält, die ungültig sind. Sie können sich nicht auf Bestandsdimensionen beziehen, die sich in der Reservierungshierarchie unterhalb der Dimension Lagerplatz befinden. Entfernen Sie die ungültigen Dimensionen aus der Auftragszeile.

## <a name="resolution"></a>Lösung

Leider unterstützt das Produkt keine Ladungsverarbeitung für einen Rückgabeprozess. Daher können Sie den Verkaufsauftrag für die Rücklieferung nicht an das Lagerort freigeben.

Bei Verkaufsauftragstransaktionen können Sie nicht auf Bestandsdimensionen verweisen, die sich in der Reservierungshierarchie unterhalb der Dimension **Ort** befinden. Die Lösung ist, die ungültigen Dimensionen aus der Auftragszeile zu entfernen.
