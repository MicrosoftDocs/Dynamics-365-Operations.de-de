---
title: Kostenberechnungsstufe
description: In diesem Thema wird die Stücklistenebene beschrieben, die als Kostenberechnungsstufe bezeichnet wird. Diese Stücklistenstufe schließt Produktions- und Chargenaufträge von ihren Berechnungen aus.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f7cde239107528a6bc2aeb0e424d024d4f3fb2a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839486"
---
# <a name="cost-calculation-level"></a>Kostenberechnungsstufe

Die Stücklistenebene (BOM) die **Kostenberechnungsstufe** benannt ist, schließt Fertigungsaufträge und Chargenaufträge von den Berechnungen aus. Das System verwendet diese Ebene, wenn es Kostenberechnungen in Kalkulationsversionen ausführt. In Prozessen wie Neuberechnung und Bestandsabschluss verwendet das System die **Kostenstufe** Stücklistenebene.

Das folgende einfache Szenario zeigt die Unterschiede zwischen der Stücklistenebene **Kostenberechnungsstufe** und **Kostenstufe**.

Sie haben drei Produkte: A, B und C. Produkt C ist die Komponente von Produkt B und Produkt B ist die Komponente von Produkt A.

- **Kostenstufe** weist die folgenden Stücklistenebenen zu:

    - **Produkt A:** 0
    - **Produkt B:** 1
    - **Produkt C:** 2

- **Kostenberechnungsstufe** weist die folgenden Stücklistenebenen zu:

    - **Produkt A:** 0
    - **Produkt B:** 1
    - **Produkt C:** 2

Anschließend wird ein Fertigungsauftrag für Produkt C erstellt und Produkt A zur Fertigungsauftragsstückliste hinzugefügt. Nachdem die Bestellung geschätzt wurde, werden die Stücklistenebenen folgendermaßen aktualisiert:

- **Kostenstufe** weist die folgenden Stücklistenebenen zu:

    - **Produkt B:** 1
    - **Produkt C:** 2
    - **Produkt A:** 3

- **Kostenberechnungsstufe** weist die folgenden Stücklistenebenen zu:

    - **Produkt A:** 0
    - **Produkt B:** 1
    - **Produkt C:** 2

Dieses Verhalten stellt sicher, dass Änderungen an Fertigungsauftragsstücklisten keine Auswirkungen auf nachfolgende Kostenberechnungen haben.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]