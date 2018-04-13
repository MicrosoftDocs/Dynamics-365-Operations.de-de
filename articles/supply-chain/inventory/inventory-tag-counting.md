---
title: Markierungsinventur
description: "Dieser Artikel enthält Informationen zu Umlagerungen, die Sie verwenden, um die tatsächlichen Inhalt eines Lagerorts mit dem verfügbaren Lagerbestand zu vergleichen."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0687058bc76c3ed0dad57b76d54ad57c00987f42
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="inventory-tag-counting"></a>Markierungsinventur

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [retail name](../includes/retail-name.md)]

Dieser Artikel enthält Informationen zu Umlagerungen, die Sie verwenden, um die tatsächlichen Inhalt eines Lagerorts mit dem verfügbaren Lagerbestand zu vergleichen.

Wenn Sie Positionen in der markierungsbasierte **Zählvorgang** Seite erstellen, platzieren Sie eine Markierungsnummer Nummer auf jedem Lagerartikel, wie einer Zahl zwischen 1 und 500. Während der Zählung die Artikelnummer und die Anzahl auf einer entsprechenden Markierung ein. Diese Markierung kann als Grundlage für die Eingabe in der Markierungsinventurerfassung verwendet werden. Nach dem Buchen der Markierungs-Inventurerfassung wird eine neue Inventurerfassung auf der Seite **Inventur**erstellt. Die neue Erfassung basiert auf den Positionen der Markierungs-Inventurerfassung, die Sie selbst erstellt haben. Um Inventurartikel für eine bestimmte Lagerdimension zu markieren, wählen Sie die Dimension auf der Seite **Dimension anzeigen**aus, die angezeigt wird, wenn Sie die Markierungs-Inventurerfassung erstellen. Um beispielsweise Artikel an einem bestimmten Lagerort zu inventarisieren, aktivieren Sie das **Lagerort**-Kontrollkästchen. Wenn der **Artikel während der Inventur sperren**-Schieberegler auf der **Parameter für Lager- und Lagerortverwaltung**-Seite aktiviert ist, können Artikel nicht innerhalb der Inventur physisch aktualisiert werden. Allerdings werden Artikel in den Markierungs-Inventurerfassungen nicht während der Inventur gesperrt. Lagerbuchungen werden nicht erstellt, bis die Positionen der Markungsinventur an eine Inventurerfassung übermittelt und gebucht sind. Wenn Markierungen nach dem Zufallsprinzip eingegeben werden und Sie fehlende Markierungen ermitteln möchten, klicken Sie auf den Spaltenkopf **Markierung**, damit die Positionen sortiert werden.

<a name="see-also"></a>Siehe auch
--------

[Permanente Inventur](../warehousing/cycle-counting.md)

