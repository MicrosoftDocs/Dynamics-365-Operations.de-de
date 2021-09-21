---
title: Importierte Bestellungen weisen falsche Positionsnummern auf.
description: Wenn Bestellungen über die Datenverwaltung importiert werden, folgen die Bestellpositionsnummern nicht dem in den Systemparametern definierten Inkrement.
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
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476399"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>Importierte Bestellungen weisen falsche Positionsnummern auf.

## <a name="symptoms"></a>Symptome

Standardmäßig verwenden automatisch generierte Positionsnummern für Bestellpositionen, die über die *Bestellpositionen V2*-Datenentität importiert werden nicht das in den Systemparametern angegebene Systempositionsnummerninkrement. Wenn Sie manuell eine Bestellung erstellen und Positionen über die Benutzeroberfläche hinzufügen, werden die Positionsnummern korrekt erhöht. Wenn Sie jedoch das Datenverwaltungs-Framework (DMF) verwenden, werden sie nicht korrekt inkrementiert.

Dieses Problem tritt auf, weil das System beim Importieren von Positionen über DMF die DMF-Methode zum Zuweisen verwendet, wenn in der importierten Entität noch keine Positionsnummern zugewiesen sind. Diese Methode erhöht die Positionsnummern immer um eins.

## <a name="workaround"></a>Problemumgehung

Stellen Sie sicher, dass die gewünschten Positionsnummern bereits in den Feldern für Positionsnummern der Datenentität angegeben sind, wenn Sie die Bestellpositionen importieren. In diesem Fall überschreibt DMF die Positionsnummern nicht.
