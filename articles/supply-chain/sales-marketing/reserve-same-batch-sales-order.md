---
title: Reservieren derselben Charge für einen Auftrag
description: In diesem Artikel wird beschrieben, wie ein Produkt eingerichtet wird, um Bestandreservationen für eine einzelne Bestandcharge zu ermöglichen.
author: omulvad
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0937be76aa687ed986ff83e67f2db3e2dadd0f0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807655"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a>Reservieren derselben Charge für einen Auftrag

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie ein Produkt eingerichtet wird, um Bestandreservationen für eine einzelne Bestandcharge zu ermöglichen.

Mit der Reservierung derselben Charge können Sie Bestand für eine Auftragsposition aus einer einzelnen Lagercharge reservieren. Zum Beispiel kann ein Debitor, der Tapete bestellt, fordern, dass der gesamte Auftrag aus derselben Charge oder demselben Los stammt, damit Unterschiede zwischen den Rollen vermieden werden. Damit ein Produkt die Reservierung derselben Charge verwendet, müssen die folgenden Einstellungen in den Artikelmodellgruppen, der Rückverfolgungsangabengruppe und der Lagerdimensionsgruppe, die alle dem Produkt zugewiesen werden, aktiviert sein:

- **Artikelmodellgruppen** – Für die Artikelmodellgruppe müssen die Felder **Auswahl derselben Charge** und **Bedarf konsolidieren** in der Feldgruppe **Reservierung** für Bestandsrichtlinien aktiviert werden.
- **Rückverfolgungsangabengruppen** – Für die Rückverfolgungsangabengruppe muss das Feld **Disposition nach Dimensionen** für die Chargennummer aktiviert werden.
- **Lagerdimensionsgruppen** – Für die Lagerdimensionsgruppe muss das Feld **Disposition nach Dimensionen** für **Standort** und **Lagerort** aktiviert werden.

Beim Reservieren von Bestand für ein Produkt in einer Auftragsposition, die für die Auswahl derselben Charge eingerichtet ist, versucht das System die aus einer einzelnen Lagercharge bestellte Menge zu reservieren. Dabei werden auch bestimmte Chargenattributanforderungen berücksichtigt. Kann die Menge nicht durch eine Charge abgedeckt werden kann, wird die Seite **Reservierungskonflikt aufgrund identischer Charge** angezeigt. Diese Seite beschreibt die Probleme und auch die Aktivitäten, die Sie ausführen können, um mit der Reservierung fortzufahren. Die folgenden Umstände könnten verhindern, dass die Charge reserviert werden kann:

- Im Chargendispositionscode ist die Einstellung **Reservierung sperren** für Verkäufe mit dem Status **Gesperrt** gekennzeichnet.
- Die Charge ist abgelaufen (unter Berücksichtigung des Ablaufdatums und aller zutreffenden Verkaufstage für Debitoren). Der Artikel kann nach wie vor für die Reservierung berücksichtigt werden, wenn die Lagermodellgruppe für den Artikel First Expiry First Out (FEFO)-datumsgesteuert ist und Mindesthaltbarkeitsdatum als Kommissionierungskriterium ausgewählt wird.
- Die verbleibende Haltbarkeitsdauer der Charge ist unzureichend (dabei werden das Ablauf- bzw. Mindesthaltbarkeitsdatum sowie alle Verkaufstage für Debitoren berücksichtigt).

Für Elemente, die einer Speicherdimensionsgruppe zugeordnet sind, bei der **Benutzerfehlerprotokoll für Lagerortverwaltungsprozesse verwenden** aktiviert ist, können Sie bestimmte Chargennummern mithilfe einer Reservierungshierarchie reservieren, wenn die Chargennummern-Inventardimension über der Standortdimension definiert ist. Dieser Typ der Reservierungshierarchie wird auch als eine Reservierungshierarchie *Charge oberhalb \[Lagerplatz\]* bezeichnet. Auf der Seite **Chargenreservierung** für Verkaufs- und Transportauftragspositionen können Sie auch mehrere Positionen basierend auf den verfügbaren Chargennummern auswählen und reservieren. Weitere Informationen dazu, was zu tun ist, wenn Sie eine Reservierungshierarchie verwenden, deren Chargennummer unter dem Lagerplatz liegt (*Charge unterhalb \[Lagerplatz\]*), finden Sie unter [Flexible Reservierungsrichtlinie für Dimensionen auf Lagerebene](../warehousing/flexible-warehouse-level-dimension-reservation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
