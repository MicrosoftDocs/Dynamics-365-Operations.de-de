---
title: Produktionsaufträge werden nicht auf der Seite Markierung angezeigt
description: Einige Produktionsaufträge werden nicht auf der Seite Beschriftung angezeigt. In diesem Thema werden die drei Produktkonfigurationen erläutert, die nicht zum Markieren verfügbar sind.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476390"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>Produktionsaufträge werden nicht auf der Seite Markierung angezeigt

## <a name="symptoms"></a>Symptome

Bei der diskreten Fertigung werden einige Fertigungsaufträge nicht auf der **Markierung**-Seite angezeigt.

## <a name="resolution"></a>Lösung

Produkte, die die folgende Konfigurationen haben, sind nicht für die Markierung verfügbar. Daher werden sie nicht auf der Seite **Beschriftung** angezeigt:

- Die Produkte sind als Produkte vom Typ *Artikelgewicht* definiert.
- Sie sind für die erweiterten Lagerort-Prozesse aktiviert.
- Sie sind so konfiguriert, dass sie nach dem Prinzip *Standardkosten* gesteuert werden.
