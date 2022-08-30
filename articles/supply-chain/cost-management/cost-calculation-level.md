---
title: Kostenberechnungsstufe
description: In diesem Artikel wird die Stücklistenebene beschrieben, die als Kostenberechnungsstufe bezeichnet wird. Diese Stücklistenstufe schließt Produktions- und Chargenaufträge von ihren Berechnungen aus.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: e63a868696e36c1d4f5d19ea87bdf4d682c39f8c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334954"
---
# <a name="cost-calculation-level"></a>Kostenberechnungsstufe

[!include [banner](../includes/banner.md)]

Die Stücklistenebene (BOM) die **Kostenberechnungsstufe** benannt ist, schließt Fertigungsaufträge und Chargenaufträge von den Berechnungen aus. Das System verwendet diese Ebene, wenn es Kostenberechnungen in Kalkulationsversionen ausführt. In Prozessen wie Neuberechnung und Bestandsabschluss verwendet das System die **Kostenstufe** Stücklistenebene.

## <a name="turn-the-cost-calculation-level-feature-on-or-off"></a>Die Funktion „Kostenberechnungsstufe“ ein- oder ausschalten

Um diese Funktion nutzen zu können, muss sie für Ihr System aktiviert werden. Ab Supply Chain Management Version 10.0.29 ist die Funktion standardmäßig aktiviert. Administratoren können diese Funktionalität an- oder ausschalten, indem Sie nach der Funktion *Kostenberechnungsstufe* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

## <a name="example-scenario"></a>Beispielszenario

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