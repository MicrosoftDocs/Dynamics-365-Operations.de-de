---
title: Geplante Aufträge werden für den Lagerbestand mit Fertigungsaufträgen erzeugt
description: Planaufträge werden generiert, obwohl Sie Elemente auf Lager haben und bereits Produktionsaufträge für sie existieren
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476493"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>Geplante Aufträge werden für den Lagerbestand mit Fertigungsaufträgen erzeugt

## <a name="symptoms"></a>Symptome

Planaufträge werden generiert, obwohl Sie Elemente auf Lager haben und bereits Produktionsaufträge für sie existieren.

## <a name="resolution"></a>Lösung

Sie können dieses Problem möglicherweise beheben, indem Sie den Wert **Positive Tage** für die betreffenden Gruppen auf der Seite **Deckungsgruppe** erhöhen. Diese Änderung bewirkt, dass das System ermittelt, ob der vorhandene Bestand für den Bedarf verwendet werden kann. Dann wird für die Elemente, die auf Lager sind, kein neuer Planauftrag generiert.
