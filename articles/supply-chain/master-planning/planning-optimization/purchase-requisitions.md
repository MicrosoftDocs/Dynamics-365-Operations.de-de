---
title: Bestellanforderungen
description: Dieser Artikel beschreibt Bestellanforderungen.
author: t-benebo
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: d9d55186307b18f4c3be78ae0828b08d3c987aad
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740683"
---
# <a name="purchase-requisitions"></a>Bestellanforderungen

[!include [banner](../../includes/banner.md)]

Die Masterplanung kann genehmigte Bestellanforderungen auffüllen. Um Bestellanforderungen abzudecken, müssen Benutzer daher keinen Workflow zum Erstellen von Bestellungen verwenden. Stattdessen können Bestellanforderungen durch die Masterplanung abgedeckt werden. Aufgrund dieser Funktionalität kann eine Bestellanforderung abhängig vom Wert von **Geplante Auftragsart**, der für das zugehörige Produkt festgelegt wird, eine Bestellung, einen Umlagerungsauftrag oder einen Produktionsauftrag erzeugen.

## <a name="enable-master-plans-to-include-requisitions"></a>Aktivieren von Masterplänen einschließlich Anforderungen

Führen Sie die folgenden Schritte aus, um Anforderungen in die Abdeckungsberechnung für einen Masterplan einzubeziehen.

1. Wechseln Sie zu **Masterplanung** \> **Einrichten** \> **Pläne** \> **Masterpläne**.
1. Erstellen Sie einen Masterplan oder wählen Sie einen aus.
1. Legen Sie im Inforegister **Allgemein** die Option **Anforderungen einbeziehen** auf *Ja* fest.
1. Wiederholen Sie die Schritte 2 und 3 für jeden weiteren Masterplan, in den Sie Anforderungen einbeziehen möchten.

## <a name="approved-requisitions-time-fence"></a>Genehmigter Anforderungsplanungszeitraum

Die Option *Zeitraum für genehmigte Anforderungen* legt fest, wie lange (in Tagen) ein Masterplan die Nachfrage aus genehmigten Wiederbeschaffungsanforderungen enthält. Sie können einen genehmigten Zeitraum für Anforderungen sowohl auf der Ebene der Deckungsgruppe als auch auf der Ebene des Masterplans festlegen.

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a>Festlegen des Zeitraums für genehmigte Anforderungen für eine Abdeckungsgruppe

1. Gehen Sie zu **Produktprogrammplanung** \> **Einrichten** \> **Deckung** \> **Deckungsgruppen**.
1. Erstellen oder Sie eine Abdeckungsgruppe oder wählen Sie eine aus.
1. Legen Sie im Inforegister **Sonstiges** das Feld **Zeitraum für genehmigte Anforderungen (Tage)** auf die Anzahl der Tage fest, die in den Zeitraum aufgenommen werden sollen.
1. Wiederholen Sie die Schritte 2 und 3 für jede zusätzliche Abdeckungsgruppe, für die Sie einen Zeitraum für genehmigte Anforderungen festlegen möchten.

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a>Festlegen des Zeitraums für genehmigte Anforderungen für einzelne Masterpläne

Wenn Sie für einen einzelnen Masterplan einen Zeitraum für eine genehmigte Anforderung festlegen, überschreibt die Einstellung die Zeitraumeinstellung für jede anwendbare Abdeckungsgruppe.

1. Wechseln Sie zu **Masterplanung** \> **Einrichten** \> **Pläne** \> **Masterpläne**.
1. Erstellen Sie einen Masterplan oder wählen Sie einen aus.
1. Legen Sie im Inforegister **Planungszeiträume in Tagen** das Feld **Zeitraum für genehmigte Anforderungen (Tage)** auf die Anzahl der Tage fest, die in den Zeitraum aufgenommen werden sollen.
1. Wiederholen Sie die Schritte 2 und 3 für jeden zusätzliche Masterplan, für den Sie einen Zeitraum für genehmigte Anforderungen festlegen möchten.

> [!IMPORTANT]
> Zeiträume für genehmigte Anforderungen werden für die Planungsoptimierung nicht unterstützt. Bis sie unterstützt werden, werden alle Werte ignoriert, die Sie in das Feld **Zeitraum für genehmigte Anforderungen (Tage)** eingeben.

## <a name="independent-supply-regardless-of-coverage-code"></a>Unabhängige Lieferung, unabhängig vom Abdeckungscode

Bestellanforderungen werden unabhängig vom Abdeckungscode immer von unabhängigen geplanten Aufträgen abgedeckt. Dieses Verhalten gewährleistet eine eindeutige Rückverfolgbarkeit und Workflows zwischen Bestellanforderungen und Wiederbeschaffungsaufträgen.

### <a name="example-1"></a>Beispiel 1

Ein Produkt ist für die Option **Abdeckungscode** mit einem Wert von *Min./Max.* eingerichtet. Es hat die folgenden Bestands- und Anforderungsstatus:

- Verfügbare Menge im Bestand = 10.
- Minimale Bestandsmenge = 15.
- Maximale Bestandsmenge = 20.
- Es ist eine Bestellanforderung für ein Stück vorhanden. Sie hat als gewünschtes Datum den heutigen Tag.

Wenn die Masterplanung ausgeführt wird, werden zwei geplante Aufträge erstellt: einer für 10 Stück, um den Bestand auf die maximale Menge aufzufüllen, und einer für ein Stück, um die Bestellanforderung aufzufüllen.

### <a name="example-2"></a>Beispiel 2

Ein Produkt ist für die Option **Abdeckungscode** mit einem Wert von *Min./Max.* eingerichtet. Es hat die folgenden Bestands- und Anforderungsstatus:

- Verfügbare Menge im Bestand = 17.
- Minimale Bestandsmenge = 15.
- Maximale Bestandsmenge = 20.
- Es ist eine Bestellanforderung für ein Stück vorhanden. Sie hat als gewünschtes Datum den heutigen Tag.

Wenn die Masterplanung ausgeführt wird, wird ein geplanter Auftrag für ein Stück erstellt, um die Bestellanforderung aufzufüllen.

### <a name="example-3"></a>Beispiel 3

Ein Produkt ist für die Option **Abdeckungscode** mit einem Wert von *Zeitraum* und eine Periodenlänge von sieben Tagen eingerichtet. Es hat die folgenden Bestands-, Auftrags- und Anforderungsstatus:

- Verfügbare Menge im Bestand = 0.
- Es ist ein Auftrag für fünf Stück vorhanden. Er enthält als voraussichtliches Versanddatum das heutige Datum plus einen Tag.
- Es ist eine Bestellanforderung für drei Stück vorhanden. Sie hat als angefordertes Datum das heutige Datum plus drei Tage.

Wenn die Masterplanung ausgeführt wird, werden zwei geplante Aufträge erstellt: einer für drei Stück, um die Bestellanforderung aufzufüllen, und einer für fünf Stück, um den Auftragsbedarf aufzufüllen.

> [!NOTE]
> Nachdem ein geplanter Auftrag, der an eine Bestellanforderung gebunden ist, umgewandelt wurde, behält das Planungsmodul den Bedarfsverursacher für die Bestellanforderung bei. Wenn später festgestellt wird, dass dem umgewandelten Auftrag eine Menge fehlt, die zur Erfüllung der Bestellanforderung erforderlich ist, erstellt das System einen neuen geplanten Auftrag für die Differenz.

Weitere Informationen zu Bestellanforderungen finden Sie unter [Übersicht über Bestellanforderung](../../procurement/purchase-requisitions-overview.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]